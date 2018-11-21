## ITI0201<br />Robotite Programmeerimine

---
### Planeerimine ja navigatsioon

---
## Meeleolu tekitamiseks...

---
![A value driven agent](https://www.youtube.com/embed/V8utFzn7DJk)

---?image=assets/image/trolley_problem.png&size=auto 35%

@snap[north]
The trolley problem
@snapend

---
## Ajakava

Nädal |  | Tegevus
------|--|--------
@size[large](**12**) | @size[large](@color[goldenrod](Loeng)) | @size[large](Planeerimine ja navigatsioon)
  | @size[large](@color[darkgreen](Praktikum)) | @size[large]("Labürint" arendamine ja kaitsmine)
  | @size[large](@color[cornflowerblue](Kodutöö)) | @size[large]("Labürint" arendamine)
@size[large](**13**) | @size[large](@color[goldenrod](Loeng)) | @size[large](---)
  | @size[large](@color[darkgreen](Praktikum)) | @size[large]("Labürint" arendamine ja kaitsmine)
  | @size[large](@color[cornflowerblue](Kodutöö)) | @size[large]("Labürint" arendamine)

---
## Labürint

Kasutage pronkstaseme lahendamisel simulaatoris võtit `--blind`

---
## Kauguse skaneerimine

---?gist=GertKanter/97a6dca93af5c107dc5ec20db2556f79&lang=python
@snap[north]
@size[smaller](http://gist.github.com/GertKanter/97a6dca93af5c107dc5ec20db2556f79)
@snapend
---?gist=GertKanter/1d9a07f1931707fe9a7c7289cc463954&lang=python

---?image=assets/image/15.png&size=auto 60%
---?image=assets/image/10.png&size=auto 60%
---?image=assets/image/9.png&size=auto 60%
---?image=assets/image/8.png&size=auto 60%

---
## Kalibreerimine

Roboti miinimumkiiruse saab enne skaneerimist välja selgitada.

---
## Protseduuriline vs OOP

Klassidel põhinev lahendus sobib robotite programmeerimiseks suurepäraselt.

---
## Protseduuriline

---?gist=GertKanter/d5e7f69eb45ca6f10a76a8e229c22e75&lang=python

---
## OOP

---?gist=GertKanter/8b0b43fd7ee6086659475b9884f90637&lang=python

---
## Kaardistamine

---?image=assets/image/tln_map.png&size=auto 80%

---
## Diskreetne vs pidev kaart

---?image=assets/image/discrete.png&size=auto 60%

---
## Ainus-hüpotees veendumus (single-hypothesis belief) vs multi

---?image=assets/image/multibelief.png&size=auto 90%

---
## Tõenäosuslik kaart

---?image=assets/image/probabilistic.png&size=auto 70%

---
## Tõenäosuslik kaart rinnetega

---?image=assets/image/occupancy_probabilistic.png&size=auto 60%

@snap[north]
Otsingurinded punasega märgitud
@snapend

---?image=assets/image/occupancy_probabilistic2.png&size=auto 60%
---?image=assets/image/occupancy_probabilistic3.png&size=auto 60%
---?image=assets/image/occupancy_probabilistic4.png&size=auto 60%
---?image=assets/image/occupancy_probabilistic5.png&size=auto 60%
---?image=assets/image/occupancy_probabilistic6.png&size=auto 60%

---
## Rinde avastamisalgoritm

---?image=assets/image/frontier_algo.png&size=auto 90%

---
## Labürindi avastamine

---?image=assets/image/maze_exploration.png&size=auto 90%
---?image=assets/image/frontier_prio.png&size=auto 40%

---
## Kaardistamine kasutades eelteadmisi

---?image=assets/image/knowledge.png&size=auto 50%

@snap[north]
Sirgete seintega ruumi kaardistamine
@snapend

---?image=assets/image/lawnmower.png&size=auto 50%

@snap[north]
Robot peab "silmuse sulgema" laadimisjaama minnes
@snapend

---?image=assets/image/lawnmower2.png&size=auto 50%

@snap[north]
Lisatud maamärgid aitavad navigeerida
@snapend

---
## Ülekattega kaardistamine

---?image=assets/image/mapping_overlap.png&size=auto 90%

---
## Kaardistamine (SLAM)

---?image=assets/image/mapping1.png&size=auto 70%
---?image=assets/image/mapping2.png&size=auto 70%
@snap[north]
Soovitud liikumine
@snapend
---?image=assets/image/mapping3.png&size=auto 70%
@snap[north]
Tegelik liikumine
@snapend
---?image=assets/image/mapping4.png&size=auto 60%
@snap[north]
Soovitud vs tegelik tuvastus
@snapend
---?image=assets/image/mapping5.png&size=auto 70%
@snap[north]
Võimalikud poosid
@snapend
---?image=assets/image/mapping6.png&size=auto 90%
---?image=assets/image/mapping7.png&size=auto 90%
---?image=assets/image/mapping8.png&size=auto 30%
---?image=assets/image/mapping9.png&size=auto 60%
---?image=assets/image/slam_algo.png&size=auto 90%

---
## Planeerimine

---
@ul
- Teekonna planeerimiseks kasutatakse robootikas paljusid erinevaid algoritme.
- Üks lihtsamatest algoritmidest, mis annab lühima tee, on Dijkstra algoritm.
- Väga populaarsed on ka näiteks A\* ja D\* algoritmid.
@ulend

---?image=assets/image/dijkstra.png&size=auto 60%
@snap[north]
Lühim tee S->G
@snapend
---?image=assets/image/dijkstra2.png&size=auto 60%
---?image=assets/image/dijkstra_algo.png&size=auto 90%
---?image=assets/image/dijkstra3.png&size=auto 60%
---?image=assets/image/dijkstra4.png&size=auto 90%

---
## Kaaludega kaardid

---?image=assets/image/dijkstra5.png&size=auto 50%
@snap[north]
Vasakul "/" == 4, paremal "/" == 2
@snapend

---
## Dekompositsioonil põhinevad kaardid

---?image=assets/image/dijkstra6.png&size=auto 80%
---?image=assets/image/dijkstra7.png&size=auto 80%

---
## A\* algoritm

---?image=assets/image/astar.png&size=auto 80%
---?image=assets/image/astar2.png&size=auto 80%
---?image=assets/image/astar2_1.png&size=auto 80%

---
## Pisut keerulisem näide

---?image=assets/image/astar3.png&size=auto 60%
---?image=assets/image/astar4.png&size=auto 90%

---
## Lisamaterjalid

Võite huvi korral lugeda "õpikust" (Elements of Robotics) juurde

- 9\. peatükk - **Mapping**
- 10\. peatükk - **Mapping-Based Navigation**
