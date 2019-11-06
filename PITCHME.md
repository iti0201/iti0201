## ITI0201<br />Robotite Programmeerimine

---
### Sensorid, müra, reaktiivne käitumine, olekumasinad

---
## Meeleolu tekitamiseks...

---
![Self solving Rubik's cube](https://www.youtube.com/embed/xCoH2AORcEQ)

---?image=assets/image/self-solving-rubiks-cube-robot-designboom-5.jpg&size=auto 60%
---?image=assets/image/solve.jpg&size=auto 60%

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

---?image=assets/image/ir_characteristics.png&size=auto 80%
---?image=assets/image/ir_sensor_work.gif&size=auto 60%

---
## IR kitsaskohad

---?image=assets/image/sonar.png&size=auto 40%
---?image=assets/image/sonar2.png&size=auto 40%

---
## Müra

---?image=assets/image/std_deviation.png&size=auto 80%
---?image=assets/image/noise_filter.jpg&size=auto 80%

---
## Keskmistamine

---?image=assets/image/average.png&size=auto 80%

---
## Filtreerimine

---
@ul
- @size[xx-large](t=0: input=100  buffer=[100, 100, 100], avg=100  =>  output=100)
- @size[xx-large](t=1: input=103  buffer=[103, 100, 100], avg=101  =>  output=103)
- @size[xx-large](t=2: input=106  buffer=[106, 103, 100], avg=103  =>  output=106)
- @size[xx-large](t=3: input=2550  buffer=[2550, 106, 103], avg=920  =>  output=106)
- @size[xx-large](t=4: input=112  buffer=[112, 2550, 106], avg=923  =>  output=106)
- @size[xx-large](t=5: input=115  buffer=[115, 112, 2550], avg=926  =>  output=106)
- @size[xx-large](t=6: input=118  buffer=[118, 115, 112], avg=115  =>  output=118)
@ulend

---
@ul
- @size[xx-large](t=0: input=100  buffer=[100, 100, 100], avg=100  =>  output=100)
- @size[xx-large](t=1: input=103  buffer=[103, 100, 100], avg=101  =>  output=103)
- @size[xx-large](t=2: input=106  buffer=[106, 103, 100], avg=103  =>  output=106)
- @size[xx-large](t=3: input=2550  buffer=[2550, 106, 103], avg=920  =>  output=106)
- @size[xx-large](t=4: input=2550  buffer=[2550, 2550, 106], avg=1735  =>  output=106)
- @size[xx-large](t=5: input=2550  buffer=[2550, 2550, 2550], avg=2550  =>  output=2550)
@ulend

---
## Reaktiivne käitumine

---
## Braitenbergi sõiduk

---?image=assets/image/braitenberg.png&size=auto 80%

---
## Käitumine: arglik

---?image=assets/image/timid.png&size=auto 60%

---

## Käitumine: paranoiline

---?image=assets/image/paranoid.png&size=auto 60%

---
## Pööramine

---?image=assets/image/turning.png&size=auto 60%

---
## Joonejärgija

---?image=assets/image/warehouse.png&size=auto 60%
---?image=assets/image/linefollowing.png&size=auto 60%
---?image=assets/image/lf_algo.png&size=auto 80%
---?image=assets/image/lf_gradient.png&size=auto 40%

---
## Braitenbergi käitumised

---?image=assets/image/braitenberg_vehicles.png&size=auto 80%

---
## Olekumasinad (FSM)

---?image=assets/image/state_diagram.png&size=auto 20%

---?gist=GertKanter/0358f059c69296d61c422cbc48c166a9&lang=py
---?gist=GertKanter/d570522f3c2a1410f463228461e6c46d&lang=py
---?gist=GertKanter/172763f3f730269a0b6b47b83bb76527&lang=py

---?image=assets/image/fsm_persistent_braitenberg.png&size=auto 50%
---?image=assets/image/fsm_search_approach.png&size=auto 80%
---?image=assets/image/algo_persistent.png&size=auto 80%
---?image=assets/image/algo_search_approach.png&size=auto 80%

---
## Lisamaterjalid

Võite huvi korral lugeda "õpikust" (Elements of Robotics) juurde

- 2\. peatükk - **Sensors**
- 3\. peatükk - **Reactive Behavior**
- 4\. peatükk - **Finite State Machines**
