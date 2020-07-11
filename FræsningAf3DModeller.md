# Fræsning af 3D modeller med VCarve
Vetric VCarve er software vi har tilgængeligt i labbet på computeren i CNC-rummet. VCarve bruges til at lave designs der kan fræses på enten X-carven eller carveyen. Programmet kan oversætte dit design til *paths*/gcode der kan importeres i easel, hvorefter man sætter maskinen op som sædvaneligt når man bruger easel.

## 3D modeller
En af de features har er at importere 3D modeller ind i VCarve, der så kan behandle dem, så de kan fræses i easel på en af de to fræsere der er tilgængelige i labbet, hhv. X-carve og carvey. Det er den feature denne guide vil hjælpe med.

3D modellerne der kan importeres ind i VCarve skal være på et af følgende filformater: .v3m, .STL eller .OBJ. Hvis du vil lave dine egne 3D modeller er blender.org eller tinkercad.com gode gratis muligheder eller Autodesks Fusion360, som er lidt mere avanceret, og som er gratis for studerende.

Husk at fræseren kun kan fræse oppefra, hvilket betyder at indgraveringer på bagsiden af 3D modellen ikke er muligt. I tilfælde heraf bør materialet vendes efter den ene side er fræset, og en ny path bør udregnes for bagsiden.

## Importér 3D modellen ind i VCarve
Når VCarve åbnes kan der startes et nyt fræsningsprojekt ved at trykke på *Create a new file* under *Startup Tasks*.

Herefter vil der til højre kunne ses et arbejdsområde, hvor projektet kan laves på, og til venstre vil der være en menu.

#### Setup projekt
I menuen til venstre kaldet *Job Setup* skal I angive dimensionerne på det materiale I ønsker at fræse i under punktet *Job size*. Vær opmærksom på at det er den rigtige måleenhed der er angivet. De andre indstillinger i *Job setup* behøver du ikke nødvendigvis at ændre. Tryk derefter på *OK*.

Arbejdsområdet til højre har nu ændret dimensioner, så det svarer til det du angav i *Job Setup*. Du kan nu importere din 3D model ind på arbejdsområdet. Dette gøres ved at åbne fanebladet kaldet *modelling* der Er placeret nederst i menuen til venstre. I den menu der kommer frem kan du trykke på det første ikon, hvorefter du kan lokalisere den fil du gerne vil fræse. En todimensionel repræsentation af den model du har valgt vil da blive vist på arbejdsområdet.
For at se en tredimensionel version, tryk på det firkantede ikon med en streg ned igennem øverst i vinduet, længst til højre.

#### Placér og transformér din model på arbejdsområdet
Du kan nu flytte rundt og ændre størrelsen på modellen på arbejdsområdet som du ønsker ved at trykke på modellen og trække den til den ønskede størrelse og placering på materialet. VCarve har også funktioner der automatisk kan centrere modellen på materialet. Tryk på fanebladet kaldet *Drawing*, der er placeret nederst i menuen til venstre. Under menuen *Transform Objects* er der forskellige funktioner der angiver placering og størrelse på modellen.

For at bestemme tykkelsen på modellen skal du åbne *Modelling* fanen igen og tryk på ikonet med en skruenøgle. Hvor der står *Shape Height* kan du bestemme den højde du ønsker modellen skal have. De resterende menuer behøver du ikke nødvendigvis at ændre på.

#### Setup Materiale
Yderst til højre i vinduet er der et faneblad kaldet *toolpaths*. Tryk her for at åbne menuen, som du skal bruge til at bestemme hvordan du vil fræse din model.

Først skal du sætte materialet op. Tryk på *Set...* øverst under menuen *Material setup*. Tjek at følgende indstilligner er valgt i menuen:
- Tjek at det er den rigtige tykkelse på dit materiale som er angivet.
- Tjek at XY datum er angivet som det nederste venstre hjørne.
- Tjek at Z-zero står som materialets overflade.
- Tjek at afstanden modellen bliver placeret fra overfladen er større end nul. Dvs. der hvor der står *Gap above model* skulle gerne mindst være 0.5-1 mm.
- Tjek at *Clearance* under menuen *Rapid Z Gaps above material* er større end den højde de clamps du bruger stikker op over materialet. Dette gøres, så når fræseren gør større bevægelser vil den løfte bittet op over disse clamps, så de ikke bliver ramt.
- Tjek at X og Y under menuen *Home/Start position* begge er sat til 0.

#### Toolpaths
Det smarte ved at bruge VCarve til at forberede 3D modeller til at blive carvet er at det er nemt at lave *toolpaths*. *Toolpaths* er det der bestemmer hvordan maskinen bevæger sig for at fræse modellen ud, hvilke stier og hastigheder den skal følge. Det er *toolpaths* som til sidst kan eksporteres fra VCarce og importeres ind i easel for at carve modellerne.

Hvis man skal fræse en detaljeret 3D model er det en god ide at lave 3 toolpaths. En der gør *roughing*, som grovt tager overskydende materiale over modellen, *finishing*, som detaljeret udformer modellen og *profiling*, hvis nødvendigt udskærerer modellen fra materialet.

 **1. Roughing**

En roughing toolpath bør med et grovt bit fjerne store dele af materialet for at komme ned til hvor modellen er i materialet.

Roughing laves ved at trykke på ikonet i *Toolpaths* fanen, som ligner en lagdelt pyramide i materialet. Her skal du gøre følgende:
- Vælge det bit du skal bruge. Til roughing vil det ofte været et tykt bit der kan fjerne meget materiale hurtigt. Sæt dig ind i hvilket bit der passer til dit materiale. Se afsnittet nedenfor.
- Vær opmærksom på når du vælger bit at *depth per pass* ikke er højere end 0.8 mm.
- Under menuen *Machining limit boundary* skal den sættes til *model boundary*. Tjek også her at *boundary offset* mindst er bittets radius.
- Tjek at *Machining allowance* er større end 0.

Resten af indstillingerne for roughing toolpath behøver du ikke nødvendigvis at ændre. Tryk efterfølgende på *Calculate*, hvorefter du vil kunne se en simulation af denne toolpath.


 **2. Finishing**

 En finishing toolpath bør med et fint bit fræse alle modellens detaljer.

 Finishing laves ved at trykke på ikonet i *Toolpaths* fanen, som ligner en halv kugle i materialet. Her skal du gøre følgende:
 - Vælge det bit du skal bruge. Til finishing vil det ofte været et meget fint bit der kan komme ned og fræse de nødvendige detaljer. Sæt dig ind i hvilket bit der passer til dit materiale. Se afsnittet nedenfor.
 - Under menuen *Machining limit boundary* skal den sættes til *model boundary*. Tjek også her at *boundary offset* mindst er bittets radius.
 - Under menuen *Area machine strategy* vælg *Raster*.

Tryk efterfølgende på *Calculate*, hvorefter du vil kunne se en simulation af denne toolpath.

 **3. Profile**

En profile toolpath vil skære hele vejen igennem materialet, så modellen kan sepereres fra materialet hvis dette er ønsket.

For at lave en profiling toolpath bliver du nødt til først at lave en vektor der er omkredsen af din model, som fræseren kan følge. Dette gøres ved igen at åbne fanen *Modeling*, som er placeret i vinduets øverste venstre hjørne. Her markerer du modellen du arbejder med under *Components* og tryk på ikonet der ligner en model med en optrukket omkreds. Når musen holdes over ikonet står der *Create vector boundary around selected components*. Når dette er gjort vil du på arbejdsområdet se den optrukne omkreds rundt om modellen. Tryk på denne omkreds, så den er markeret med en stiblet linje og vend tilbage til *toolpaths* fanen til højre i vinduet.

Profiling laves herefter ved at trykke på ikonet i *Toolpaths* fanen, som ligner en omkreds af en firkant der er fræset ned i materialet. Her skal du gøre følgende:
- Vælge det bit du skal bruge. Til profiling vil det bør der bruges et bit der er så stort som muligt, men som stadig kan komme ind i hjørnerne i din model. Sæt dig ind i hvilket bit der passer til dit materiale. Se afsnittet nedenfor.
- Under menuen *Machiune Vectors* vælg *Outside/Right*
- Tilføj evt. tabs, som vil holde dit projekt på plads ligesom i easel.

Tryk efterfølgende på *Calculate*, hvorefter du vil kunne se en simulation af denne toolpath.

#### Vælg de rigtige bits!
 - **Sæt dig ind i hvilke bits der passer til det du vil lave!**
 - Det skal være det rigtige type og tykkelse bit til det materiale du har valgt og det design du gerne vil fræse.
 - [Klik her for et skema over bits og materialer](https://inventables.zendesk.com/hc/en-us/articles/360021943493-Color-Coded-Bit-Chart-Choosing-the-Right-Bit?utm_source=Intercom&utm_medium=email%20XC%20Owner&utm_campaign=%3E%205%20carves%20bit%20poster%20download "Bit skema")
 - [Klik her for en tutorial i bits!](https://inventables.zendesk.com/hc/en-us/articles/360012849233-Carving-Bits-101-Bit-Basics "Bits 101")
 - [Klik her for eksempelfotos med forskellige bits og materialer!](https://www.inventables.com/projects/carving-bits-101?ref=EaselLive&utm_source=YouTube&utm_medium=Easel%20Live&utm_campaign=13_bits101_project "Bit eksempelfotos")
 - [Læs kapitel 8(side 12) i denne X-carve quick-start guide](https://www.jesspublib.org/_uploads/X-Carve-Quick-Start-1.pdf "X-cave quick start")


#### Export from VCarve to Easel
Hver toolpath du har lavet skal exportéres fra VCarve, importéres ind i easel og carves individuelt en efter en. Toolpaths'ne skal carves i den rækkeflølge de blev lavet: Roughing, finishing og til sidst profiling.

Følgende trin skal derfor gentages for alle tre toolpaths:
- **Eksportér**: Tryk på ikonet i fanen *Toolpaths*,  der ligner en diskette. Vælg herefter den toolpath du vil eksportere. Vælg gcode som *Post processor* og tryk på *Save Toolpath(s)*.
- **Importér**: I easel under menuen *File* vælges *Import gcode* Herefter skal du lokalisere den gemte toolpath på din computer.
- **Carve**: Tryk på *Carve* i øverste højre hjørne i easel og følg instruktioner som når easel normalvis bruges til at fræse.


## Video guides:
Nedenfor er der nogle udvalgte video guides der dækker det basale om at fræse 3D modeller med VCarve samt nogle af de andre af de mange features i VCarve. [Andre video guides til VCarve kan findes her](https://www.youtube.com/playlist?list=PLLdEiXEsoRequgz4yFZJZpFWLbSaMOVYA).

Vær opmærksom på at interfacet i videoerne godt kan afvige en smule fra versionen af vetric VCarve, som er tilgængelig i labbet.

**Roughing, finishing and profiling af 3D modeller:**

Følgende video går igennem punkterne gennemgået i denne guide.

 <a href="http://www.youtube.com/watch?feature=player_embedded&v=owL7AhCR710
 " target="_blank"><img src="http://img.youtube.com/vi/owL7AhCR710/0.jpg"
 alt="roughing, Finishing and profiling" width="480" height="360" border="5" /></a>


**Slicing 3D model i flere stykker:**

Eftersom fræserne kun fræser oppefra kan det være nyttigt at opdele sin 3d model i flere stykker, hvis de skal have detaljer på begge sider, eller hvis man ikke har et materiale der er tykt nok til hele ens model. Stykkerne vil dermed blive udskåret seperat fra hinanden og kan efterfølgende limes sammen.

<a href="http://www.youtube.com/watch?feature=player_embedded&v=2b_bR-iy2V4
" target="_blank"><img src="http://img.youtube.com/vi/2b_bR-iy2V4/0.jpg"
alt="Slicing 3D model i flere stykker" width="480" height="360" border="5" /></a>

**Import, export og behandling af diverse filtyper:** (.v3m, .stl, .tif og .jpg)

3D model filtyper som .v3m, .STL eller .OBJ er ikke de eneste filtyper, der kan importeres ind i VCarve.

<a href="http://www.youtube.com/watch?feature=player_embedded&v=Jh2EaoDPXyU
" target="_blank"><img src="http://img.youtube.com/vi/Jh2EaoDPXyU/0.jpg"
alt="Import, export og behandling af diverse filtyper" width="480" height="360" border="5" /></a>
