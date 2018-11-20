## ITI0201<br />Robotite Programmeerimine

---
### Planeerimine ja navigatsioon

---
## Meeleolu tekitamiseks...

---
![Robat](https://www.youtube.com/embed/LzGGuzvYSH8)

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
## Protseduuriline vs OOP

Klassidel põhinev lahendus sobib robotite programmeerimiseks suurepäraselt.

---
## Protseduuriline

---?gist=GertKanter/d5e7f69eb45ca6f10a76a8e229c22e75&lang=python

---
## OOP

---?gist=GertKanter/8b0b43fd7ee6086659475b9884f90637&lang=python

---
## Diskreetne vs pidev kaart

---?image=assets/image/discrete.png&size=auto 90%

---
## Tõenäosuslik kaart

---?image=assets/image/probabilistic.png&size=auto 90%

---
## Tõenäosuslik kaart rinnetega

---?image=assets/image/occupancy_probabilistic.png&size=auto 90%
---?image=assets/image/occupancy_probabilistic2.png&size=auto 90%
---?image=assets/image/occupancy_probabilistic3.png&size=auto 90%
---?image=assets/image/occupancy_probabilistic4.png&size=auto 90%
---?image=assets/image/occupancy_probabilistic5.png&size=auto 90%
---?image=assets/image/occupancy_probabilistic6.png&size=auto 90%

---
## Rinde avastamisalgoritm

---?image=assets/image/frontier_algo.png&size=auto 90%

---
## Labürindi avastamine

---?image=assets/image/maze_exploration.png&size=auto 90%

---
## Kaardistamine koos kitsendustega arvestamisega

---?image=assets/image/knowledge.png&size=auto 90%

---
## Laadimisjaamaga rakendus

---?image=assets/image/lawnmower.png&size=auto 90%
---?image=assets/image/lawnmower2.png&size=auto 90%

---
## Ülekattega kaardistamine

---?image=assets/image/mapping_overlap.png&size=auto 90%

---
## Ainus-hüpotees veendumus (single-hypothesis belief) vs multi

---?image=assets/image/multibelief.png&size=auto 90%

---
## Kaardistamine

---?image=assets/image/mapping1.png&size=auto 70%
---?image=assets/image/mapping2.png&size=auto 70%
---?image=assets/image/mapping3.png&size=auto 70%
---?image=assets/image/mapping4.png&size=auto 70%
---?image=assets/image/mapping5.png&size=auto 90%
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

---?image=assets/image/dijkstra.png&size=auto 70%
---?image=assets/image/dijkstra2.png&size=auto 70%
---?image=assets/image/dijkstra_algo.png&size=auto 90%
---?image=assets/image/dijkstra3.png&size=auto 70%
---?image=assets/image/dijkstra4.png&size=auto 70%

---
## Muutuva hinnaga kaardid

---?image=assets/image/dijkstra5.png&size=auto 90%

---
## Dekompositsioonil põhinevad kaardid

---?image=assets/image/dijkstra6.png&size=auto 90%
---?image=assets/image/dijkstra7.png&size=auto 90%

---
## A*

---?image=assets/image/astar.png&size=auto 90%
---?image=assets/image/astar2.png&size=auto 90%

---
## Pisut keerulisem näide

---?image=assets/image/astar3.png&size=auto 90%
---?image=assets/image/astar4.png&size=auto 90%

---
## Lisamaterjalid

Võite huvi korral lugeda "õpikust" (Elements of Robotics) juurde

- 9\. peatükk - **Mapping**
- 10\. peatükk - **Mapping-Based Navigation**
