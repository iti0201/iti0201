## ITI0201<br />Robotite Programmeerimine

---
### Liikumine, odomeetria ja juhtimine

---
## Meeleolu tekitamiseks...

---
![Robots teaching themselves to see](https://www.youtube.com/embed/OplLXzxxmdA)

---
![Parkour Atlas](https://www.youtube.com/embed/LikxFZZO2sk)

---
![Precise Hopping with Salto-1P](https://www.youtube.com/embed/ZFGxnF9SqDE)

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

---?image=assets/image/fsm_elevator.png&size=auto 90%

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
Kiirus ei ole konstantne.

---
Tuletame roboti oleku hindamise protsessi tahvlile...

---
## Odomeetria

---
Roboti poosi (koordinaate ja orientatsiooni) kirjeldatakse 2D robotite korral kolme väärtusega:

**x koordinaat** *(meetrites)*

**y koordinaat** *(meetrites)*

**$\theta$ lengerdusnurk (yaw)** *(radiaanides)*

---
Kui on oluline ka kõrgus ja nurk 3-mõõtmelises maailmas, siis kirjeldatakse poosi nii:

**x, y, z koordinaat**

**pöörde- (roll), kallutus- (pitch) ja lengerdusnurk (yaw)**

---?image=assets/image/state.png&size=auto 70%
---?image=assets/image/state_vector.png&size=auto 30%
---?image=assets/image/90deg.png&size=auto 70%

---
### Pöördemaatriks (rotation matrix) 2D

---?image=assets/image/rotation.png&size=auto 30%
---

### Forward kinematic model
---?image=assets/image/state_derivative.png&size=auto 30%

---
@ul
- l - ratta kaugus telje keskkohast
- r - ratta diameeter
- θ - roboti nurk
- φ1 - vasaku ratta kiirus
- φ2 - parema ratta kiirus
@ulend

---?image=assets/image/state_derivative_wheelspeed.png&size=auto 70%
---?image=assets/image/state_derivative_wheelspeed2.png&size=auto 70%

---
## Juhtimine (PID)

---
Tagasisideta (open loop)

*versus*

tagasisidestatud (closed loop) juhtimine.

---
Näiteid tagasisideta juhtimisest?
@ul
- pesumasin
- röster
- pesukuivati
- ...
@ulend

---
Kuidas sõita "täpselt"?

---
Juhime mootorite kiirust dünaamiliselt vastavalt hetkkiirusele.

---
Kuidas seda teha?

---
Kasutame tagasiside saamiseks rataste enkoodreid.

[https://github.com/iti0201/robot](https://github.com/iti0201/robot)

---?image=assets/image/closed_loop.png&size=auto 40%
---?image=assets/image/feedback_algo.png&size=auto 60%
---?image=assets/image/on_off_controller.png&size=auto 60%
---?image=assets/image/on_off_plot.png&size=auto 50%

---
## PID juhtimine

---
PID = proportsionaal-integraal-diferentsiaalregulaator ehk PID-kontroller

---
## Proportsionaalne (P) kontroller, P-regulaator

---?image=assets/image/p_controller.png&size=auto 50%
---?image=assets/image/p_controller_neg_08.png&size=auto 70%
---?image=assets/image/p_gain.png&size=auto 70%

---
## Proportsionaalne-integraal (PI) kontroller, PI-regulaator

---?image=assets/image/pi_controller.png&size=auto 40%
---?image=assets/image/pi_algo.png&size=auto 60%
---?image=assets/image/pi_plot.png&size=auto 60%

---
## PID-kontroller

---?image=assets/image/pid_controller.png&size=auto 10%
---?image=assets/image/pid_algo.png&size=auto 70%
---?image=assets/image/pid_plot.png&size=auto 60%

---
Hea juhtimisalgoritm
@ul
- Hea juhtimisalgoritm peaks kiiresti koonduma ja vältima järske muutusi.
- Juhtimisalgoritm tuleb kohandada vastavalt süsteemile.
@ulend

---
## Näide: püsikiirusehoidja

---?image=assets/image/cruise_diagram.png&size=auto 60%
---?image=assets/image/cruise_slope.png&size=auto 60%
---?image=assets/image/cruise_fsm.png&size=auto 50%


---
Tagasisidestatud süsteemide kohta on värske allikas

[http://www.cds.caltech.edu/~murray/amwiki/index.php/Second_Edition](http://www.cds.caltech.edu/~murray/amwiki/index.php/Second_Edition)

---
## Koordinaatsüsteemid

---?image=assets/image/frames.png&size=auto 70%
---?image=assets/image/frames2.png&size=auto 30%
---?image=assets/image/frames3.png&size=auto 70%
---?image=assets/image/frames_cyclic.png&size=auto 70%


---
## Kuidas tuvastada objekte?

---?image=assets/image/object_detection.png&size=auto 70%

---
## Lisamaterjalid

Võite huvi korral lugeda "õpikust" (Elements of Robotics) juurde

- 5\. peatükk - **Robotic Motion and Odometry**
- 6\. peatükk - **Control**
