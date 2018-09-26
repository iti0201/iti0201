## ITI0201<br />Robotite Programmeerimine

---
## Robotite programmeerimise alused

---

Registreerige ennast ainele

[http://ained.ttu.ee](http://ained.ttu.ee)

keskkonnas!

---
## Ajakava

Nädal |  | Tegevus
------|--|--------
**4** | @size[smaller](@color[goldenrod](Loeng)) | @size[smaller](Robotite programmerimise alused)
  | @size[smaller](@color[darkgreen](Praktikum)) | ---
  | @size[smaller](@color[cornflowerblue](Kodutöö)) | ---
**5** | @size[smaller](@color[goldenrod](Loeng)) | ---
  | @size[smaller](@color[darkgreen](Praktikum)) | @size[smaller]("Simulatsioon")
  | @size[smaller](@color[cornflowerblue](Kodutöö)) | @size[smaller]("Joonejärgija" arendamine)

---
### Simulatsioon (1 nädal)

Tase | Kirjeldus
-----|----------
@color[goldenrod](Pronks<br />@size[smaller]([1. tase])) | Sõida robotiga seinani ja peatu ettemääratud kaugusel.
@color[silver](Hõbe<br />@size[smaller]([2. tase])) | Sõida robotiga seina juurde, pööra ja sõida ümber seina.
@color[gold](Kuld<br />@size[smaller]([3. tase])) | -
@color[firebrick](Eliit<br />@size[smaller]([4. tase])) | -

---
## Arendustsükkel

@ul
- Arendamine
- Robotil testimine
- Valmis!
@ulend

---
## Ainult ideaalses maailmas!

---
## Analüüs

@ul
- Probleemi analüüsimine
- Arendamine
- Simulatsioon
- Päris robotil testimine
@ulend

---
## Tegelikkus

@ul
- Analüüsi ignoreerimine. (halb!)
- Pidev tagasipöördumine eelmistesse etappidesse. (hea!)
@ulend

---
## Probleemi analüüsimine

Ülesande tükeldamine hoomatavateks tükkideks

---?image=assets/image/tomatoes.jpg&size=auto 90%
---?image=assets/image/tomatoes2.jpg&size=auto 90%
---?image=assets/image/greenhouse.jpg&size=auto 90%

---
![Fruit picking](https://www.youtube.com/embed/UaL3UxUclKY)

---
## Arendamine

---?image=assets/image/pycharm.png&size=auto 90%
---?image=assets/image/git.png&size=auto 50%

---
## Simulatsioon

---?image=assets/image/gazebo.png&size=auto 50%
---?image=assets/image/ros.png&size=auto 50%

---
## Robotil testimine

Lahenduse robotil testimine toimub praktikumides.

---
## Simulatsioon

---
Mis toimub n-ö kapoti all?

Kõik info on avalik, st ei ole tegemist "musta kastiga", mille sisu ei ole teada.

---
Koodisalved asuvad

[http://github.com/iti0201](http://github.com/iti0201)

---?image=assets/image/gazebo_world.png&size=auto 80%

---
## Simulatsiooni maailm

*.world* laiendiga fail

---?gist=GertKanter/6bb4a8434f29342865df956daeea172e&lang=xml

---
## Roboti mudel

*.sdf* laiendiga fail

---?gist=GertKanter/f069765cabb003d2f85457fb46dd8031&lang=xml

---
## Komponendid

@ul
- Sim: Algoritm (Python) @fa[arrows-h] PyBot (API) @fa[arrows-h] ROS @fa[arrows-h] Gazebo
- Robot: Algoritm (Python) @fa[arrows-h] PyBot (API) @fa[arrows-h] Robot (UART)
@ulend

---
## Roboti juhtimismeetodid

Kuidas läheneda roboti algoritmi programmeerimisele?

---
## Reaktiivne juhtimine

---?image=assets/image/reactive.png&size=auto 50%

---
## Reaktiivne juhtimine

@ul
- Act = Tegevus
- Sense = Sensorite lugemine
@ulend

---
## Sense-Plan-Act

---?image=assets/image/spa.png&size=auto 50%

---
## Sense-Plan-Act

@ul
- Sense = Sensorite lugemine
- Plan = Mõtleme järgmise sammu
- Act = Täiturite juhtimine (mootorid jne)
@ulend

---
## Hübriidjuhtimine

---?image=assets/image/hybrid.png&size=auto 50%

---
## Hübriidjuhtimine

@ul
- Act = Tegevus
- Plan = Planeerimine
- Sense = Sensorite lugemine
@ulend

---
## Hübriidjuhtimine

Robot kasutab planeerimist, et valida milline käitumine on antud hetkel sobivaim ja seejärel rakendab reaktiivset juhtimist.

---
## Mall

---
## "vabastiil"

---

@ul
- @size[smaller](Loe kaugusandurist lugem x, kui lugem > 10 cm, siis...)
- @size[smaller](Saada mootoritele käsk sõita otse)
- @size[smaller](Oota 10 sekundit)
- @size[smaller](Vaata kas oled kohal? Kui ei, siis mine kaks rida ülespoole.)
- @size[smaller](Saada mootoritele käsk pöörata paremale 90 kraadi kiirusega z rad/s.)
- @size[smaller](Oota 3 sekundit)
- @size[smaller](Saada mootoritele käsk sõita y cm otse)
- @size[smaller](Oota 5 sekundit)
- @size[smaller](....)
@ulend

---
## Sense-Plan-Act

---?gist=GertKanter/8b0b43fd7ee6086659475b9884f90637&lang=py

---
## Head programmeerimistavad

@ul
- Ära korda ennast! (DRY (Don't Repeat Yourself))
- Ära korda ennast! (DRY (Don't Repeat Yourself))
- Muutujatele pane võimalikult lühikesed, aga maksimaalselt informatiivsed nimed!
@ulend

---
## Näide
@ul
- variable_to_count_number_of_objects?
- counter?
- object_count
@ulend

---
## PiBot programmeerimine

---?image=assets/image/pibot_side.jpg&size=auto 90%
---?image=assets/image/pibot_bottom.jpg&size=auto 90%
---?image=assets/image/pibot_front.jpg&size=auto 90%
---?image=assets/image/pibot_front_ir.jpg&size=auto 90%
---?image=assets/image/pibot_rear.jpg&size=auto 90%

---
Kuidas praktikas programmeerimine välja näeb?

---
## PiBot
Programmeerimisjuhend on (API)

[https://github.com/iti0201/robot](https://github.com/iti0201/robot)

---
## Praktikum

---
Praktikum on eelkõige mõeldud päris robotil testimiseks ja töö kaitsmiseks.

**See tähendab, et eelnevalt on vaja teha algoritm/lahendus valmis.**

---
## Praktikumi põrandaplaan

---?image=assets/image/floorplan.png&size=auto 60%

---
## Protsess

---
@ul
- Lahenduse lähtekood on Gitlab-is üleval.
- Võtate vaba roboti ja vaatate, mis roboti kood on (roboti peal kirjas).
- Panete roboti platsile algasendisse.
- Kasutate laadimisarvutil skripti (*load.sh*), mis laeb teie lahenduse lähtekoodi robotisse (skriptil määrate parameetritega oma uni-id, ülesande koodi ja roboti koodi).
- Robot hakkab teie lähtekoodile vastavalt ülesannet lahendama.
@ulend

---?image=assets/image/upload.png&size=auto 60%

---
## Silumine

Roboti väljatrüki saab laadida oma Gitlab-i kasutades laadimisarvuti skripti (*fetch.sh*)

---
## Kaine mõistus

@ul
- Ära lõhu robotit!
- Ära vääna või painuta robotite küljes olevaid komponente!
- Ole robotiga ettevaatlik!
- **Kui ei ole kindel, kuidas mingit probleemi lahendada, siis küsi juhendajalt!**
@ulend

---
## Robootikatarkvara arhitektuurid

---
Põhieesmärk on jagada roboti alamkomponendid eraldi mooduliteks

@ul
- Keerukuse mõttes lihtsamad komponendid
- Paremini jälgitav süsteem
- Kergemini silutav (debug)
- Selgemini jagatav (kes/mis vastutab mille eest)
@ulend

---
## Ajalugu

---?image=assets/image/shakey.jpg&size=auto 90%

---
## STRIPS planeerija

[https://en.wikipedia.org/wiki/STRIPS](https://en.wikipedia.org/wiki/STRIPS)
[https://github.com/tansey/strips](https://github.com/tansey/strips)

---
## Alamkihtide arhitektuur

"Subsumption architecture" - Rodney Brooks

---?image=assets/image/subsumption.png&size=auto 60%
---?image=assets/image/subsumption2.png&size=auto 60%

---
## Kolmekihiline arhitektuur

---?image=assets/image/arch1.png&size=auto 50%

@snap[south]
@size[smaller](LAAS architecture for autonomous systems)
@snapend

---
## Autonoomia kihid

---?image=assets/image/autonomy_layers.png&size=auto 60%

---
## Tasemed vs ülesanded

@ul
- Joonejärgija - reaktiivne juhtimine (umbes 1 tase)
- Objektid - reaktiivne/proaktiivne juhtimine (1+2 tase)
- Labürint - reaktiivne/proaktiivne juhtimine (1+2+3 tase)
@ulend

---
## Grace kasutusmall

---?image=assets/image/grace.jpg&size=auto 70%
---?image=assets/image/grace2.png&size=auto 80%
---?image=assets/image/grace3.png&size=auto 80%

---
## Robotiarhitektuuride disainimine

---
Arhitektuuri ülesanne on muuta roboti tarkvara ja arendamine:
@ul
- lihtsamaks
- turvalisemaks ja ohutumaks
- paindlikumaks
@ulend

---
## Arhitektuuri kriteeriumite küsimused

---
@ul
- Milliseid ülesandeid robot hakkab täitma?
- Pikaajalised? Lühiajalised?
- Kasutajapoolt alustatud? Roboti enda poolt alustatud?
- Kas ülesanded on korduvad või erinevad?
@ulend

---
@ul
- Millised tegevused on vajalikud ülesannete täitmiseks?
- Kuidas neid tegevusi modelleeritakse?
- Kuidas tegevusi koordineeritakse?
- Kui kiiresti peab robot neid tegevusi tegema?
@ulend

---
## Implementatsioonid

---
Olemas on palju erinevaid arhitektuure:

@ul
- aRDnet
- OROCOS
- YARP
- Smartsoft
- ROS
- GenoM
- BRICS
- ...
@ulend

---
## Lisamaterjalid

Võite huvi korral lugeda "õpikust" (Elements of Robotics)

1. peatüki - **Robots and Their Applications**
