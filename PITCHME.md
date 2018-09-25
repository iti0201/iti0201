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

Algoritm (Python) @fa[arrows-h] PyBot (API) @fa[arrows-h] ROS @fa[arrows-h] Gazebo

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
- @size[smaller](Loe kaugusandurist lugem x)
- Saada mootoritele käsk sõita otse
- Oota 10 sekundit
- Vaata kas oled kohal? Kui ei, siis mine kaks rida ülespoole.
- Saada mootoritele käsk pöörata paremale 90 kraadi kiirusega z rad/s.
- Oota 3 sekundit
- Saada mootoritele käsk sõita y cm otse
- Oota 5 sekundit
- ....
@ulend

---
## SPA

---

---?gist=GertKanter/8b0b43fd7ee6086659475b9884f90637&lang=py

---
## PiBot programmeerimine

---
Kuidas praktikas programmeerimine välja näeb?

---
## PiBot
Programmeerimisjuhend on siin-link (pibot_api.pdf)

---
## Praktikum

---
## Robootikatarkvara arhitektuurid

---
## Simulatsiooni virtuaalmasin

---

