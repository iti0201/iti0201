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

---
@ul
- Juhul, kui eesolev auto on _kaugel eemal_ või kui taga on auto _lähedal_, siis säti kiirus _""tempokalt"_ peale.
- Juhul, kui eesolev auto on _lähedal_, siis säti kiirus _"aeglaselt"_ peale.
@ulend
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
@snap[north span-100]
@size[30px](Selgendamine (konkreetse väärtuse leidmine&#41;)
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

---?image=assets/image/noisy_image.png&size=auto 35%
@snap[north]
Müraga pildid
@snapend

---?image=assets/image/intensity_avg.png&size=auto 35%
@snap[north]
Pikslite keskmistamine
@snapend

---?image=assets/image/box_filter.png&size=auto 35%
@snap[north]
Box filter
@snapend

---
nn kast-filter: `$$ \begin{bmatrix} 1 & 1 & 1 \\ 1 & 1 & 1 \\ 1 & 1 & 1 \end{bmatrix} $$`

`$$ \begin{multline} g(r,c) = ( \\
     f(r-1, c-1) + f(r - 1, c) + f(r - 1, c + 1) + \\
     f(r, c-1) + f(r, c) + f(r,c+1) + \\
     f(r+1,c-1) + f(r+1,c) + f(r+1,c+1)) / 9
     \end{multline} $$`

---?image=assets/image/weighted_filter.png&size=auto 35%
@snap[north]
Weighted filter
@snapend

---
Kaaludega filter: `$$ \begin{bmatrix} 1 & 1 & 1 \\ 1 & 8 & 1 \\ 1 & 1 & 1 \end{bmatrix} $$`
`$$ \begin{multline} g(r,c) = ( \\
     f(r-1, c-1) + f(r - 1, c) + f(r - 1, c + 1) + \\
     f(r, c-1) + 8 \cdot f(r, c) + f(r,c+1) + \\
     f(r+1,c-1) + f(r+1,c) + f(r+1,c+1)) / 16
     \end{multline} $$`

---?image=assets/image/image_matrices.png&size=auto 35%
@snap[north]
Binaarsete piltide maatriksid
@snapend

---?image=assets/image/histogram.png&size=auto 35%
@snap[north]
Histogramm
@snapend

---
```plaintext
for each pixel p
    bin_number = intensity(p) / number_of_bins
    bins[bin_number] = bins[bin_number] + 1
```

---?image=assets/image/edge_intensity.png&size=auto 35%
@snap[north span-100]
@size[30px](Servaga pilt (b=serva intensiivsus&#41;)
@snapend

---?image=assets/image/edge_derivatives.png&size=auto 35%
@snap[north span-100]
@size[30px](Serva intensiivsuse tuletised (a=esimene tuletis, b=teine tuletis&#41;)
@snapend

---
@snap[north span-100]
Sobel filter
@snapend

`\( \begin{bmatrix} -1 & -2 & -1 \\ 0 & 0 & 0 \\ 1 & 2 & 1 \end{bmatrix} \)` (horisontaalne)

`\( \begin{bmatrix} -1 & 0 & 1 \\ -2 & 0 & 2 \\ -1 & 0 & -1 \end{bmatrix} \)` (vertikaalne)

---?image=assets/image/sobel_edge.png&size=auto 35%
@snap[north span-100]
@size[30px](Sobel filtri tulemused (a=horisontaalne, b=vertikaalne&#41;)
@snapend

---?image=assets/image/sobel_diagonal.png&size=auto 65%
@snap[north span-100]
@size[30px](Kaldservaga pildil rakendamine (a=horisontaalne, b=vertikaalne&#41;)
@snapend

---?image=assets/image/valve_original.png&size=auto 55%
---?image=assets/image/valve_sobel.png&size=auto 55%

---
## Lisamaterjalid

_Elements of Robotics_

- 11\. peatükk - **Fuzzy Logic Control**
- 12\. peatükk - **Image Processing**

---
### Teemad, mis jäid aines käsitlemata

@ul
- Närvivõrgud (ptk 13)
- Masinõpe (ptk 14)
- Parverobootika (ptk 15)
- Manipulaatori kinemaatika (ptk 16)
@ulend

---
## Tagasiside

---
Negatiivsed
@ul
- Probleemid robotitega (puudulikud andurid, mootorid jne)!
- Raske aine!
- "1" saamine liiga raske!
- Probleemid tiimikaaslastega!
- Vähe näitekoodi!
- Simulatsioonile halb ligipääs!
- Pikad järjekorrad päris robotile!
- Aine võiks olla 2. või 3. semestril!
@ulend

---
Positiivsed
@ul
- Põnevad ja huvitavad ülesanded!
- Vahva näha koodi päris robotil töötamas!
- Programmeerimisele lisaks ka praktiline külg!
- Tiimitöö!
- Kõik on abivalmid!
- Eksamit pole!
@ulend

---
"Robootika on nagu filter, mis eemaldab ebakompetentsed õpilased õpilaste nimekirjast." - Anonymous (2018)

---
Järgmisel korral ROS (Robot Operating System) ülevaade.
