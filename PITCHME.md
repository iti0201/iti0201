## ITI0201<br />Robotite Programmeerimine

---
## Robotite programmeerimise alused

---
## Meeleolu tekitamiseks...

---
![Cocktail Bot 4.0](https://www.youtube.com/embed/C2OCmsdcZTg)

---
## Ajakava

Nädal |  | Tegevus
------|--|--------
@size[large](**6**) | @size[large](@color[goldenrod](Loeng)) | @size[large](Sensorid, reaktiivne käitumine, olekumasinad)
  | @size[large](@color[darkgreen](Praktikum)) | @size[large]("Joonejärgija" arendamine ja kaitsmine)
  | @size[large](@color[cornflowerblue](Kodutöö)) | @size[large]("Joonejärgija" arendamine)
@size[large](**7**) | @size[large](@color[goldenrod](Loeng)) | @size[large](---)
  | @size[large](@color[darkgreen](Praktikum)) | @size[large]("Joonejärgija" arendamine ja kaitsmine)
  | @size[large](@color[cornflowerblue](Kodutöö)) | @size[large]("Objektid" arendamine)

---
### Joonejärgija (2 nädalat)

Tase | Kirjeldus
-----|----------
@color[goldenrod](Pronks<br />@size[smaller]([1. tase])) | Ovaalikujulisel rajal sõitmine
@color[silver](Hõbe<br />@size[smaller]([2. tase])) | Ristmikutega rajal sõitmine
@color[gold](Kuld<br />@size[smaller]([3. tase])) | Takistustega rajal sõitmine
@color[firebrick](Eliit<br />@size[smaller]([4. tase])) | -

---
## Head programmeerimistavad

@ul
- Ära korda ennast! (DRY (Don't Repeat Yourself))
- Muutujatele pane võimalikult lühikesed, aga maksimaalselt informatiivsed nimed!
@ulend

---
## DRY

---?gist=GertKanter/4b34713f677b15e112ab7973272d82a8&lang=py

---?gist=GertKanter/be7eb891d17e191ff1d92e3044713e9a&lang=py

---
## Keerukus

@ul
- Ärge tehke liiga keerulisi funktsioone!
- Vältige liiga pikaks venivaid funktsioone (nn "spagettkoodi").
- Selle saavutamiseks tükeldage loogika funktsioonideks ja kutsuge välja neid funktsioone.
@ulend

---
## Sensorid

---
Sensorid jagunevad kaheks
@ul
- Propriotseptiivsed (ingl proprioceptive) - roboti sisemist olekut mõõtvad andurid
- Eksterotseptiivsed (ingl exteroceptive) - robotit ümbritseva maailma mõõtvad andurid
@ulend

---
## Propriotseptiivsed andurid

---
Näiteks
@ul
- robotmanipulaatori lülide servomootorite hetkeasendid, hetkkiirused, jõumomendid
- robotplatvormi servomootorite hetkkiirused, asendid
- toiteaku pinge
- güroskoop
- kompass
@ulend

---
## Eksterotseptiivsed andurid

---
Näiteks
@ul
- taktiilsed andurid (puuteandurid)
- infrapunaandurid
- ultraheliandurid
- lidarid (laserkaugusmõõtjad)
@ulend

---
## IR karakteristik

---?image=assets/image/ir_characterics.png&size=auto 80%

---
## Müra

---?image=assets/image/std_deviation.png&size=auto 80%
---?image=assets/image/noise_filter.jpg&size=auto 80%

---
## Keskmistamine

---?image=assets/image/average.png&size=auto 80%

---
## Reaktiivne käitumine

...

---
## Olekumasinad (FSM)

...

---
## Lisamaterjalid

Võite huvi korral lugeda "õpikust" (Elements of Robotics) juurde

- 2\. peatükk - **Sensors**
- 3\. peatükk - **Reactive Behavior**
- 4\. peatükk - **Finite State Machines**
