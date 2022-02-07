---
layout: page
theme: jekyll-theme-dinky
title: "X-Carve"
permalink: /x-carve/
---

# **X-Carve**

Design max mål med easel eller fusion 360: **750x750 mm**

Design max mål med VCarve: **600x600 mm**

### Før du starter:

**X-carven må kun betjenes af brugere i labbet der har taget kørekort i brugen af den!**
- Henvend dig til en af de ansatte i labbet for at få mere at vide

Hvis muligt, læg materiale under det materiale du ønsker at carve i, i tilfælde af at x-carven fræser igennem, for at beskytte underlaget.

X-carven må **KUN** bruges til at carve i:
- Ubehandlet træ
- Plastik
- Voks
- Akryl
- MDF
- Aluminium

Mål dit materiale, både bredde, længde og dybde og notér målene ned.
- **NB!** De mål du noterer ned er stadig kun målene på materialet du gerne vil carve i, **IKKE** det materiale du
lægger under.

Spænd materialet fast med clamps der står i holderen ved siden af X-carven.

Vælg dit ønskede bit:
- **Sæt dig ind i hvilke bits der passer til det du skal bruge!**

- [Klik her for et skema over bits og materialer](https://inventables.zendesk.com/hc/en-us/articles/360021943493-Color-Coded-Bit-Chart-Choosing-the-Right-Bit?utm_source=Intercom&utm_medium=email%20XC%20Owner&utm_campaign=%3E%205%20carves%20bit%20poster%20download "Bit skema")
- [Klik her for en tutorial i bits!](https://inventables.zendesk.com/hc/en-us/articles/360012849233-Carving-Bits-101-Bit-Basics "Bits 101")
- [Klik her for eksempelfotos med forskellige bits og materialer!](https://www.inventables.com/projects/carving-bits-101?ref=EaselLive&utm_source=YouTube&utm_medium=Easel%20Live&utm_campaign=13_bits101_project "Bit eksempelfotos")
- [Læs kapitel 8(side 12) i denne X-carve quick-start guide](https://www.jesspublib.org/_uploads/X-Carve-Quick-Start-1.pdf "X-cave quick start")
- Bits kan også findes i holderen ved siden af x-carven. Ekstra bits kan findes i kassen under x-carven.

Montér bittet:
-	Hold den gule knap på venstre side af fræseren inde.

-	Brug den store fastnøgle eller det lasercuttede håndtag der begge ligger i holderen ved siden af x-carven til at løsne den sorte bolt, som bittet skal sættes i.

-	Indsæt dit bit i fræseren. Sørg for at holderen i fræseren er langt nok nede til at kunne nå og fastspænde bittet.

-	Brug fastnøglen eller håndtaget til at fastspænde bittet.Sørg for stadig at holde den gule knap inde.

Sørg for at hastigheden der indstilles på fræseren ikke er højere end 2!

Tænd for x-carven bagpå x-controlleren, dvs. kassen til venstre på maskinen.

[Læs mere om X-carven i denne quick start guide.](https://www.jesspublib.org/_uploads/X-Carve-Quick-Start-1.pdf)

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

**NB!** Tjek under *Cut Settings* øverst til højre at *depth per pass* ikke er højere end 0.8 mm. Hvis *depth per pass* er mere end 0.8, så ændrer *Cut Settings* fra *recommended* til *custom* og sæt *depth per pass* ned til 0.8.

**NB!** Hvis du carver i akryl, så sæt *Cut Settings* øverst til højre fra *recommended* til *custom* og sæt *depth per pass* ned til mellem 0.5 - 0.3 mm.

Vælg størrelsen på det bit du har monteret i carven øverst til højre.

Lav dit design! Nedenfor er en video, der introducerer simple funktioner i easel:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=nNSqHzCvgrU
" target="_blank"><img src="http://img.youtube.com/vi/nNSqHzCvgrU/0.jpg"
alt="Easel tutorial" width="480" height="360" border="10" /></a>

(Easel's interface har ændret sig en smule siden denne video blev lavet, men funktionerne er stadig de samme.)

For mere avancerede Easel tutorials, [klik her.](https://inventables.zendesk.com/hc/en-us/sections/360002650993-Easel-Tutorials "Easel tutorials")

Placér dit design på easel, sådan at det ikke rammer nogle af de clamps du har sat
materialet fast med.

Du kan selv vælge hvor dit nulpunkt i easel skal ligge på x-carven, så placér materialet ift. nulpunktet i easel, og så placér nulpunktet tilsvarene på x-carven når den skal indstilles.

Når du mener dit design er klar til at blive carvet tryk på *Carve* i øverste højre hjørne.
  Første gang du trykker her vil easel bede dig om at installerer driveren til easel.

#### Carve i easel

Følg instruktionerne i easel.

Tjek at maskinen reagerer på både x, y og z aksen.

#### Hvis X-carven ikke reagerer

Hvis maskinen reagerer på alle akser, så spring dette afsnit over og gå til **Carve i easel fortsat**.

Hvis maskinen **ikke** reagerer på x,y og z akserne, så **gem dit design!** Gå derefter ind under
*Machine* -> *Set up your machine* og indsæt følgende oplysninger:

- *Choose your machine type:* X-Carve (pre-November 2021)

- *Motion controller:* x-controller

- *Rail size:* 1000mmx1000mm

- *Z Axis:* Belt Drive W/ACME threaded rod

- *Spindle:* Dewalt 611

- *Belts:* 2GT 6mm

- Sæt flueben ved *Dust shoe*

- Tryk *Confirm settings*

Test igen at carven virker i både på x,y og z aksen med pilene og tryk *yes*, hvis de gør.

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

#### Home:

-	Her finder carven dens absolutte nulpunkt på x, y og z aksen.

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

#### XY zero
Find det punkt på materialet der skal bruges som det der svarer til 0,0 i easel.
- Hvis du lægger materialet med hjørnet i L-formen der er monteret i arbejdsområdet på carven kan du trykke *Use last XY*. **NB!** Hvis det ikke virker bør du henvende dig til en ansat i labbet (Fysisk eller på mail: ddlabau@gmail.com).

- Eller hvis du selv vil vælge hvor XY-koordinatet skal være på materialet skal du placere bittet over netop det punkt på materialet du ønsker skal svare til 0,0 i easel, og tryk *set XY zero*.

#### Tænd for Sponsuger:
- Løs skruerne på dust shoe holderne på hver side af fræseren.

-	Klik *dust shoen* ud af krogen til venstre og sæt den på holderne.

-	Spænd holderne fast.

-	Tryk på den grønne knap med gummiovertrækket på sponsugeren.

-	Bekræft i easel at *dust shoe* er påmonteret.

- Luk døren til grovlabbet for ikke at forstyrre andre i labbet.

#### Fræser:

-	**TAG SIKKERHEDSBRILLER PÅ!**

- **TAG HØREVÆRN PÅ!**

-	Tjek at hastigheden på fræseren ikke er sat for lavt.

- Tjek at kontakten på fræseren er sat på *on*.

-	Start fræseren ved at trykke på *Turn spindle on* i easel.

- Tjek at fræseren kører og bekræft dette ved at trykke på *The spindle is on*.


#### Før du trykker *Carve*!

-	**Hvis du kan se at dit carve kommer til at tage længere tid, så sørg for at computeren ikke går i slumretilstand eller slukker inden for den tid det tager (*Start* -> *Settings* -> *System* -> *Power & sleep*)**

- Mens X-carven kører må den **ikke efterlades uden opsyn**. Man behøver ikke at blive i grovlabbet, men bliv i det mindste i labbet, så der kan holdes øje med maskinen. Husk altid sikkerhedsbriller og høreværn når du går ind i grovlabbet igen.

-	Hvis du kan se at der går noget galt i  løbet af dit carve, så stop X-carven på den store røde knap til venstre på X-Carven hurtigst muligt. Carvet kan også stoppes i easel på x’et i  øverste højre hjørne, men den røde knap er oftest hurtigst.

- Hvis der går noget galt med selve X-carven under dit carve, så oplys labbet om problemet til DD Lab's mail: ddlabau@gmail.com

- Du kan nu trykke *Carve* i easel.

### Import Gcode

Easel er begrænset til kun at lave 2D modeller, altså carvinger der er
”lige-op-og-ned”, så det er godt til at skære ting ud og til at indgravere simple
designs (f.eks. tekst og former).

Hvis du i stedet vil carve f.eks. en 3D model, så kan du importere Gcode ind i easel,
og dermed carve mere komplekse designs.

3D modeller kan f.eks. laves i [Fusion 360,](https://www.autodesk.com/products/fusion-360/students-teachers-educators "Download fusion 360") der er gratis for studerende, eller et andet 3D modelleringsprogram.

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

- [Klik her for en guide i at lave toolpaths til 3D modeller i VCarve](../master/FræsningAf3DModeller.md)
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

Tryk på *”it looks great”* (hvis det rent faktisk ser godt ud) i easel.

Fræseren sidder tit så tæt på materialet, at du hverken kan få dit materiale ud eller
få *dust shoe* af fræseren.

Tryk derfor på *Carve* igen og brug pilene til højre til at flytte fræseren op og væk
fra materialet.

Tryk derefter på krydset for at annullere det påbegyndte carve.

Sluk for x-carven på kontakten bagpå x-controlleren (den sorte kassse) til venstre på
x-carven.

Tænd evt. igen for sponsugeren og brug børsten til at få de sidste materialerester der sidder i materialet ud. Sæt *dust shoe* tilbage i krogen når du er færdig.

Afmonter alle clamps og tag dit carve.

Afmonter bittet og sæt det tilbage hvor du tog det, **pas på** det kan være varmt.

Sluk for X-controlleren.

Sluk for computeren.

Gør rent efter dig med den rigtige støvsuger, der står i grovlabbet!

## Udfyld spørgeskemaet og anmod om kørekort til X-carve
[Link til spørgeskemaet](https://goo.gl/forms/n9OnE0x5juWclPxJ3 "X-carve kørekort")
