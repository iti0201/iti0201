## ITI0201<br />Robotite Programmeerimine

---
## Robotite programmeerimise alused

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

---
## Müra

---?image=assets/image/std_deviation.png&size=auto 80%
---?image=assets/image/noise_filter.jpg&size=auto 80%

---
## Keskmistamine

---?image=assets/image/average.png&size=auto 80%

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

## Braitenbergi käitumised

---?image=assets/image/braitenberg_vehicles.png&size=auto 80%

---
## Olekumasinad (FSM)

---?image=assets/image/state_diagram.png&size=auto 20%
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
