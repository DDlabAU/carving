# **X-Carve**

Design max mål med easel eller 360 fusion: **750x750 mm**

Design max mål med VCarve: **600x600 mm**

### Før du starter:

**X-carven må kun betjenes af brugere i labbet der har taget kørekort i brugen af den!**
- Henvend dig til en af de ansatte i labbet for at få mere at vide

Hvis muligt, læg materiale under det materiale du ønsker at carve i, i tilfælde af at x-carven carver
igennem, for at beskytte underlaget.

Mål dit materiale, både bredde, længde og dybde og noter målene ned.
- **NB!** De mål du noterer ned er stadig kun målene på materialet du gerne vil carve i, **IKKE** det materiale du
lægger under.

Spænd materiale fast med clamps der ligger i en kasse under X-carven.

Vælg dit ønskede bit:
- **Sæt dig ind i hvilke bits der passer til det du skal bruge!**

- [Klik her for en tutorial i bits!](https://inventables.desk.com/customer/portal/articles/2850808?b_id=9562&t=0 "Bits 101")
- [Klik her for eksempelfotos med forskellige bits og materialer!](https://inventables.desk.com/customer/portal/articles/2918214-bit-and-material-pairings---photos "Bit eksempelfotos")

- Bits kan findes i en kasse under x-carven.

Monter bittet:
-	Indsæt dit bit i fræseren.

-	Hold den gule knap på fræseren inde.

-	Brug den store fastnøgle i det sorte etui i en kasse under x-carven til at spænde bittet fast.

Sørg for at *dust shoe* og holderne til dust shoe **IKKE** sidder på før du begynder at
klargøre x-carven.

Tænd for x-carven bagpå x-controlleren, dvs. kassen til venstre på maskinen.


### Easel

Easel er online software, du både kan bruge til at designe dit carve og som post
processor til at printe dit carve til X-carven.

- [Link til Easel](http://easel.inventables.com/ "Easel X-Carve")

Du kan lave din egen profil og lave dit design på din egen computer og så enten
logge ind på din easel account på computeren i grovlabbet (husk at logge ud efter
du har carvet). Du kan også bruge DD Labs easel konto der er på computeren i
grovlabbet (passwordet er indtastet, bare påbegynd at skrive ddlabs mail: ddlabau@gmail.com).

#### Easel setup

Skriv målene på dit materiale samt materialetypen ind i menuen øverst til højre i easel.

**NB!** Hvis du carver i akryl, så sæt *Cut Settings* øverst til højre fra *recommended* til *custom* og sæt *depth per pass* ned til mellem 0.5 - 0.3 mm.

Vælg det bit du har monteret i carven øverst til højre.

Lav dit design: [Tutorial til de simple funktioner i easel](https://inventables.desk.com/customer/en/portal/articles/2440798-designing-in-easel "Easel Tutorial")

Placer dit design på easel, sådan at det ikke rammer nogle af de clamps du har sat
materialet fast med.

Du kan senere vælge at dit nulpunkt i easel skal ligge et andet sted på x-carven, så
placer materialet ift. nulpunktet i easel, og så placer nulpunktet tilsvarene på x-carven når den skal nulstilles.

Når du mener dit design er klar til at blive carvet tryk på *Carve* i øverste højre hjørne.

#### Carve i easel

Følg instruktionerne i easel.

Tjek at maskinen reagerer på både x, y og z aksen.

#### Hvis X-carven ikke reagerer

Hvis maskinen reagerer på alle akser, så spring dette afsnit over og gå til **Carve i easel fortsat**.

Hvis maskinen **ikke** reagerer på x,y,z akse, så **gem dit design!** Gå derefter ind under
*Machine* -> *Set up your machine* og indsæt følgende oplysninger:

- *Machine Type:* x-carve

- *Motion controller:* x-controller

- *Rail size:* 1000mmx1000mm

- *Lead screw:* ACME threaded rod

- *Spindle:* Dewalt 611

- Sæt flueben ved *Dust shoe*

- Tryk *Confirm settings*

Test at carven virker i både x,y,z retninger med pilene og tryk *yes*, hvis de gør.

Vælg *spindle control preference:* Automatic og tryk *save spindle preference*

Sørg for at kontakten på fræseren er sat på *on*.

Test herefter fræseren ved at trykke *Turn spindle on* og tjek at fræseren kører. Tjek ligeledes at fræseren slukker ved at trykke på *Turn spindle off*. Tryk derefter *Continue*.

Tryk *enable homing*, og *start homing sequence.*

Herefter vil carven begynde sin homing proces (jf. home nedenfor).

##### Setup Machine probe
Tryk *yes* til *"do you have a probe?”* og udfør herefter proceduren, som vist på skærmen.

-	Tag den lille ting med den røde og sorte ledning og med en klips og en metalcylinder
i hver ende.

-	Sæt stikket i den lille indgang ved siden af fræseren.

-	Sæt clipsen fat om metalstykket hvor du spændte bittet, og tjek det af i easel.

-	Rør metalcylinderen på bittet og tjek at det registreres i easel.

-	Tryk *continue*

Tryk *run the test carve*, men i stedet for faktisk at køre det, trykker du på det
lille stafeli i øverste venstre hjørne og vælger din sketch fra tidligere.

#### Carve i easel fortsat
Du har nu trykket *Carve* og tjekket at X-carven reagerer på både x,y, og z aksen.

Følg herefter instruktionerne på skærmen, hvor du bliver bedt om at tjekke at du har det rigtige materiale, materialetykkelse, har fastspændtmaterialet og angivet det rigtige bit...

Herefter vil X-carven begynde sin probing sequence (jf. probe nedenfor).

##### Home:

-	Her finder carven dens nulpunkt på x, y og z aksen.

-	Sørg for at hverken dust shoe eller holdere dertil er sat på under denne proces.

#### Probe:

-	Følg punkterne på skærmen.

-	Sørg for at bittet er over materialet (det behøver ikke være der hvor du ønsker
nulpunktet skal være, bare over materialet) med pilene til højre på skærmen.

-	Brug den lille ting med den røde og sorte ledning, med hhv. en klips og en metal
cylinder fastgjort dertil.

-	Indsæt stikket i den lille indgang til højre for selve fræseren på x-carven.

-	Sæt klipsen rundt om metal delen hvor du spændte bittet fast og tjek det af på
listen i easel.

-	Rør sæt metalcylinderne op mod bittet og sørg for at de registeres på listen i
easel.

-	Læg metalcylinderne under bittet oven på materialet og tjek det af på listen i
easel.

-	Tryk *start probing*.

-	Når den er færdig tag proben af x-carven og tryk *Z-probe is put away*.

Placer bittet over nettop det punkt du ønsker skal være 0,0 i easel, og tryk *set
XY zero*.

#### Tænd for Sponsuger:

-	Slide *dust shoe*-holderne på hver side af fræseren, så magneterne vender indad.

-	Før du spænder holderne fast, klik *dust shoen* ud af krogen til venstre og sæt den
på holderne.

-	Spænd holderne fast.

-	Tryk på den grønne knap med gummiovertrækket på sponsugeren.

-	Bekræft i easel at *dust shoe* er påmonteret.

#### Fræser:

-	**TAG SIKKERHEDSBRILLER PÅ!**

- **TAG HØREVÆRN PÅ!**

-	Tjek at hastigheden på fræseren ikke er sat for lavt.

- Tjek at kontakten på fræseren er sat på *on*.

-	Start fræseren ved at trykke på *Turn spindle on* i easel.

- Tjek at fræseren kører og bekræft dette ved at trykke på *The spindle is on*.


#### Begynd dit carve!

-	**Hvis du kan se at dit carve kommer til at tage lang tid, så sørg for at computeren ikke går i slumretilstand eller slukker inden for den tid det tager (*Start* -> *Settings* -> *System* -> *Power & sleep*)**

-	Hvis du kan se at der går noget galt i  løbet af dit carve, så stop X-carven på
den store røde knap til venstre på X-Carven eller stop den i easel på x’et i  øverste
højre hjørne.

### Import Gcode

Easel er begrænset til kun at lave 2D modeller, altså carvinger der er
”lige-op-og-ned”, så det er godt til at skære ting ud og til at indgravere simple
designs (f.eks. tekst og former).

Hvis du i stedet vil carve f.eks. en 3D model, så kan du importere Gcode ind i easel,
og dermed carve mere komplekse designs.

3D modeller kan f.eks. laves i Fusion 360, der er gratis for studerende, eller et
andet 3D modelleringsprogram.

I fusion 360 kan du selv lave såkaldte ”CAM toolpaths” som er den path, som fræseren
skal bevæge sig i for at carve den ønskede 3D model. Dette er dog ret kompliceret og
tager noget tid at sætte sig ind i, men [her er en tutorial](http://evanandkatelyn.com/2018/01/fusion-360-cam-tutorial-for-cnc-beginners/ "fusion 360 CAM tutorial") .

Når du har lavet dine toolpaths, så er der her en video tutorial, der forklarer hvordan gcode fra fusion
360 bedst importeres ind i easel:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=DFwXdnKzg2I
" target="_blank"><img src="http://img.youtube.com/vi/DFwXdnKzg2I/0.jpg"
alt="Import gcode from fusion 360" width="480" height="360" border="5" /></a>

I labbet har vi også softwaren *VCarve* som næsten kan lave *CAM Toolpaths* for dig.

Så hvis du i din 3D modelleringssoftware (Enten Fusion 360 eller en anden
modelleringssoftware), eksporterer din 3D model til f.eks. SVT eller OBJ format,
så kan du bruge VCarve på computeren inde i grovlabbet.

- [Klik her for nogle tutorials til VCarve](http://support.vectric.com/tutorials/V8/VCarveProCategoryIndex.html "VCarve tutorials")
- [Klik her for en tutorial til specifikt at lave paths til en 3D model i VCarve](http://support.vectric.com/tutorials/V8/Import3D/Import3D_GS.html "Importer 3D model i VCarve")

#### Når du har lavet dine paths f.eks. i vcarve og eksporteret modellen til gcode

- Importer i easel: *Import* -> *G-code* -> *Vælg fil*.

- Følg punkterne under: *Før du starter* ovenfor.

- Tryk *Carve* i øverste højre hjørne.

- Tryk *I understand*

- Tjek at du har sikret materialet.

- Vælg probe og udfør probe procedure, som beskrevet ovenfor.


### Efter du har carvet:

Sluk for sponsugeren på den røde knap.

Tryk på *”it looks great”* (altså hvis det rent faktsik ser godt ud) i easel.

Fræseren sidder tit så tæt på materialet, at du hverken kan få dit materiale ud eller
få *dust shoe* af fræseren.

Tryk derfor på *Carve* igen og brug pilene til højre til at flytte fræseren op og væk
fra materialet så du kan få det ud og få *dust shoe* af.

Tryk derefter på krydset for at annullere det påbegyndte carve.

Sluk for x-carven på kontakten bagpå x-controlleren (den sorte kassse) til venstre på
x-carven.

Tag *dust shoe* og holdere af fræseren og tænd evt. igen for sponsugeren og brug børsten
til at få det sidste savsmuld der sidder i materialet ud. Sæt *dust shoe* tilbage i
krogen når du er færdig.

Afmonter alle clamps og tag dit carve.

Afmonter bittet og sæt det tilbage hvor du tog det.

Sluk for computeren.

Gør rent efter dig med den rigtige støvsuger, der står i grovlabbet!
