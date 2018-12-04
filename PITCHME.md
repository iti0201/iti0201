## ITI0201<br />Robotite Programmeerimine

---
### Hägus loogika, pilditöötlus ja varia

---
## Meeleolu tekitamiseks...

---
![Robot catches itself before it falls](https://www.youtube.com/embed/VYPqxfzc15g)

---
## Ajakava

Nädal |  | Tegevus
------|--|--------
@size[large](**14**) | @size[large](@color[goldenrod](Loeng)) | @size[large](Hägus loogika, pilditöötlus ja varia)
  | @size[large](@color[darkgreen](Praktikum)) | @size[large]("Labürint" arendamine ja kaitsmine)
  | @size[large](@color[cornflowerblue](Kodutöö)) | @size[large]("Labürint" arendamine)
@size[large](**15**) | @size[large](@color[goldenrod](Loeng)) | @size[large](---)
  | @size[large](@color[darkgreen](Praktikum)) | @size[large]("Labürint" arendamine ja kaitsmine)
  | @size[large](@color[cornflowerblue](Kodutöö)) | @size[large]("Labürint" arendamine)

---
## Hägus loogika (fuzzy logic)

---
### Hägus loogika
@ul
- Hariliku (Boole'i) loogikaga on võimalik kirjeldada väärtusi jah/ei (tõene/väär jne).
- Hägus loogikaga on võimalik kirjeldada ka vahepealseid väärtusi nagu nt "väga soe" ja "päris jahe" ning neid matemaatiliselt formuleerida.
@ulend

---?image=assets/image/fuzzy_rules.png&size=auto 10%
@snap[north]
Kiirushoidja loogika
@snapend
---?image=assets/image/fuzzify.png&size=auto 55%
@snap[north]
Hägustamine
@snapend

---
Lähenemine objektile

@ul
- If **far** then **very fast**
- If **far** and **closing** then **fast**
- If **closing** then **cruise**
- If **closing** and **near** then **slow**
- If **near** then **stop**
@ulend

---?image=assets/image/defuzzify.png&size=auto 55%
@snap[north]
Selgendamine (konkreetse väärtuse leidmine)
@snapend

---?image=assets/image/certainty_areas.png&size=auto 55%
@snap[north]
Järeldamine (0.4 = cruise, 0.2 = fast)
@snapend

---
Olgu `\(w\)` ja `\(h\)` kolmnurga laius ja kõrgus.

Trapetsi pindala, mille kõrgus on piiratud joonega kõrgusel `\(h´\)` on antud valemiga

$$wh´(1 - \frac{h´}{2h})$$

---
Kui `\(w=50, h=1, h´_{c}=0.4\)` (cruise) `\(,h´_{f}=0.2\)` (fast), siis

`$$ a_{c} = 50 \times 0.4 (1 - \frac{0.4}{2}) = 16 $$`


`$$ a_{f} = 50 \times 0.2 (1 - \frac{0.2}{2}) = 9 $$`

---
Konkreetse väärtuse leidmiseks arvutatakse massikese.

Selleks summeeritakse trapetsite aluste keskpunktide kaalutud pindalad ja jagatakse pindalade summaga.


`$$ \frac{16 \times 50 + 9 \times 75}{16 + 9} = 59 $$`

---
## Pilditöötlus

---?image=assets/image/image_matrices.png&size=auto 35%
@snap[north]
Pildimaatriksid
@snapend

---?image=assets/image/histogram.png&size=auto 35%
@snap[north]
Histogramm
@snapend

---
## Lisamaterjalid

_Elements of Robotics_

- 11\. peatükk - **Fuzzy Logic Control**
- 12\. peatükk - **Image Processing**

---
## Teemad, mis jäid aines käsitlemata

---
@ul
- Närvivõrgud (ptk 13)
- Masinõpe (ptk 14)
- Parverobootika (ptk 15)
- Manipulaatori kinemaatika (ptk 16)
@ulend

