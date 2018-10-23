## ITI0201<br />Robotite Programmeerimine

---
### Liikumine, odomeetria ja juhtimine

---
## Meeleolu tekitamiseks...

---
![Self solving Rubik's cube](https://www.youtube.com/embed/xCoH2AORcEQ)

---
## Ajakava

Nädal |  | Tegevus
------|--|--------
@size[large](**8**) | @size[large](@color[goldenrod](Loeng)) | @size[large](Liikumine, odomeetria ja juhtimine)
  | @size[large](@color[darkgreen](Praktikum)) | @size[large]("Objektid" arendamine ja kaitsmine)
  | @size[large](@color[cornflowerblue](Kodutöö)) | @size[large]("Objektid" arendamine)
@size[large](**9**) | @size[large](@color[goldenrod](Loeng)) | @size[large](---)
  | @size[large](@color[darkgreen](Praktikum)) | @size[large]("Objektid" arendamine ja kaitsmine)
  | @size[large](@color[cornflowerblue](Kodutöö)) | @size[large]("Objektid" arendamine)

---
### Objektid (3 nädalat)

Tase | Kirjeldus
-----|----------
@color[goldenrod](Pronks<br />@size[smaller]([1. tase])) | Ühe objekti tuvastamine ja lähedale sõitmine
@color[silver](Hõbe<br />@size[smaller]([2. tase])) | Kujundi keskele sõitmine
@color[gold](Kuld<br />@size[smaller]([3. tase])) | Kompaktse kujundi keskele sõitmine
@color[firebrick](Eliit<br />@size[smaller]([4. tase])) | Objekti transportimine määratud alasse

---
## Olekuautomaadid meeldetuletus

---?image=assets/image/fsm_elevator.png&size=auto 80%

---
## Liikumine

---
$$s=vt$$

Teepikkus on võrdne kiiruse ja aja korrutisega.

---
Millised probleemid on selle valemiga robootika kontekstis?

---
Roboti liikumist mõjutavad mitmed tegurid
@ul
- ükski elektriline või mehaaniline komponent ei ole täiesti identne teisega
- keskkond (pind, millel robot sõidab) mõjutab tegelikku kiirust
- konarused ja muud takistused mõjutavad kiirust
@ulend

---
Tuletame roboti oleku hindamise protsessi tahvlile...

---
## Odomeetria

---
Roboti poosi (koordinaate ja orientatsiooni) kirjeldatakse 2D robotite korral kolme väärtusega:

x koordinaat (meetrites)

y koordinaat (meetrites)

$\theta$ lengerdusnurk (yaw) (radiaanides)

---
Kui on oluline ka kõrgus ja nurk 3-mõõtmelises maailmas, siis kirjeldatakse poosi nii:

x, y, z koordinaat

pöörde- (roll), kallutus- (pitch) ja lengerdusnurk (yaw)

---?image=assets/image/state.png&size=auto 70%
---?image=assets/image/state_vector.png&size=auto 30%

---
## Juhtimine (PID)

---
## Lisamaterjalid

Võite huvi korral lugeda "õpikust" (Elements of Robotics) juurde

- 5\. peatükk - **Robotic Motion and Odometry**
- 6\. peatükk - **Control**
