## ITI0201<br />Robotite Programmeerimine

---
### Lokaliseerimine ja kaardistamine

---
## Meeleolu tekitamiseks...

---
![Robat](https://www.youtube.com/embed/LzGGuzvYSH8)

---
## Ajakava

Nädal |  | Tegevus
------|--|--------
@size[large](**10**) | @size[large](@color[goldenrod](Loeng)) | @size[large](Lokaliseerimine ja kaardistamine)
  | @size[large](@color[darkgreen](Praktikum)) | @size[large]("Objektid" arendamine ja kaitsmine)
  | @size[large](@color[cornflowerblue](Kodutöö)) | @size[large]("Labürint" arendamine)
@size[large](**11**) | @size[large](@color[goldenrod](Loeng)) | @size[large](---)
  | @size[large](@color[darkgreen](Praktikum)) | @size[large]("Labürint" arendamine ja kaitsmine)
  | @size[large](@color[cornflowerblue](Kodutöö)) | @size[large]("Labürint" arendamine)

---
### Labürint (6 nädalat)

Tase | Kirjeldus
-----|----------
@color[goldenrod](Pronks<br />@size[smaller]([1. tase])) | U-kujuliste pööretega labürindi läbimine
@color[silver](Hõbe<br />@size[smaller]([2. tase])) | Labürindi väljapääsu leidmine
@color[gold](Kuld<br />@size[smaller]([3. tase])) | Labürindi kaardistamine (kõikide ruutude külastamine)
@color[firebrick](Eliit<br />@size[smaller]([4. tase])) | Labürindis lokaliseerimine (peale kaardistamist)

---
## Navigatsioon

Edukaks navigeerimiseks on vaja nelja (toimivat) komponenti:
@ul
- Tajumine (perception)
- Lokaliseerimine (localization)
- Tunnetus ehk kognitsioon (cognition)
- Liikumise juhtimine (motion control)
@ulend

---
## Lokaliseerimine

---?image=assets/image/localization.png&size=auto 60%

---
## Odomeetria viga

---?image=assets/image/errorprop.png&size=auto 60%
---?image=assets/image/errorprop2.png&size=auto 60%

---
## Kaardistamise protseduur

---?image=assets/image/mapping.png&size=auto 60%

---
## Miks kaarti üldse koostada?

---
@ul
- Ilmutatud kujul kaardiga on roboti kontseptuaalne asukoht väga selgelt arusaadav ka inimesele.
- Kaardi olemasolu võimaldab robotit rakendada erinevates keskkondades - lihtsalt on vaja laadida uus kaart robotisse ja robot saab uues keskkonnas tööle hakata.
- Kui kaardi ehitab robot, siis seda kaarti saavad kasutada ka inimesed.
@ulend

---
## Veendumuse esitus (belief representation)

@ul
- Millisel kujul kaarti sisemiselt meeles peetakse?
- Kuidas robot oma veendumust kaardil paiknemise suhtes hindab?
- Kas erinevad hinnangud on üldse kvantifitseeritud?
@ulend

---
## Kaardi esitusviisid

---?image=assets/image/maprepr.png&size=auto 60%

---
## Kaardi esitus

@ul
- Kaardi täpsus peab olema valitud vastavalt roboti missiooni eesmärkide täitmise täpsusele.
- Kaardi täpsus ja kaardil esitatavad andmed peavad ühilduma roboti sensoritelt saadavate andmetega.
- Kaardi esituse keerukus mõjutab otseselt kaardistamise, lokaliseerimise ja navigeerimise arvutuslikku keerukust.
@ulend

---
## Pidevkoordinaatidega kaart

---?image=assets/image/mapcontinuous.png&size=auto 60%

---
## Joontel põhinev kaart

---?image=assets/image/maplines.png&size=auto 60%

---
## Dekompositsioonil põhinev kaart

---?image=assets/image/mapdecomp.png&size=auto 60%

---
## Fikseeritud dekompositsioon

---?image=assets/image/fixeddecomp.png&size=auto 60%

---
## Paindlik dekompositsioon

---?image=assets/image/flexdecomp.png&size=auto 60%

---
## Occupancy grid map

---?image=assets/image/occupancy.png&size=auto 60%

---
## Topoloogiline esitus

---?image=assets/image/topological.png&size=auto 60%

---
## Probleemid

@ul
- Dünaamiline maailm - inimesed, autod jne liiguvad kaardistamise ajal
- Maamärkide varjamine  - nt muuseumirobotite ümber on alati palju inimesi, mis teeb lokaliseerimise väga keeruliseks
- Sõlmpunktide (node) määramine avatud kaardil - kuidas määrata sõlmpunkte nt avatud pargis?
@ulend

---
## Kaardi avastamine

---
![Kaardi avastamine](https://www.youtube.com/embed/op0L0LyGNwY)

---
## Multirobot kaardistamine

---
![Multirobot kaardistamine](https://www.youtube.com/embed/8Adrn29BVbM)

---
## 3D SLAM

---
![3D SLAM](https://www.youtube.com/embed/Win0V53K8fM)

---
## Asendi määramine vs odomeetria

---?image=assets/image/odomvsperception.png&size=auto 40%
---?image=assets/image/odomvsperception2.png&size=auto 60%

---
## Seina järgimine

---?image=assets/image/wallfollowing.png&size=auto 60%
---?image=assets/image/wallfollowing_algo.png&size=auto 60%
---?image=assets/image/wallfollowing_loop.png&size=auto 60%
---?image=assets/image/wallfollowing_dir.png&size=auto 60%
---?image=assets/image/wallfollowing_dir_algo.png&size=auto 60%
---?image=assets/image/wallfollowing_dir_fail.png&size=auto 60%
---?image=assets/image/wallfollowing_pledge.png&size=auto 60%
---?image=assets/image/wallfollowing_pledge_algo.png&size=auto 60%

---
## Lokaliseerimine

---?image=assets/image/localization_1.png&size=auto 20%
---?image=assets/image/localization_2.png&size=auto 20%
---?image=assets/image/localization_3.png&size=auto 20%
---?image=assets/image/localization_4.png&size=auto 60%
---?image=assets/image/localization_5.png&size=auto 60%
---?image=assets/image/localization_6.png&size=auto 60%
---?image=assets/image/localization_7.png&size=auto 60%
---?image=assets/image/localization_8.png&size=auto 60%

---
## Sensorite määramatus (uncertainty)

---
Kui arvestada sensorite määramatusega, siis võime muuta tõenäosusi näiteks järgmiselt:
- Tuvastab uksena, kui on uks: 0.9
- Tuvastab seinana, kui on uks: 0.1
- Tuvastab seinana, kui on sein: 0.9
- Tuvastab uksena, kui on sein: 0.1

---?image=assets/image/localization_9.png&size=auto 60%

---
## Pronks labürint

---?image=assets/image/siksak.png&size=auto 60%

---
## Labürint

@ul
- Kas kindlasti peab kaardistama?
- Kas kindlasti peab odomeetriat arvutama?
- Kuidas oleks otstarbekas kaarti esitada?
- Milline on mõistlik viis lokaliseerimiseks?
@ulend

---
## Kokkuvõtlikult

@ul
- Kaardistamine ja lokaliseerimine on mobiilsete robotite jaoks kriitilise tähtsusega funktsionaalsus. Ilma kaardita ei ole võimalik navigeerida.
- Kaartide kvaliteet sõltub sensorite täpsusest ja arvutusvõimsusest. Kui soovitakse kaardistada reaalajas, siis arvutusvõimsus mängib rolli "isegi tänapäeval".
@ulend

---
## Lisamaterjalid

Võite huvi korral lugeda "õpikust" (Elements of Robotics) juurde

- 7\. peatükk - **Local Navigation: Obstacle Avoidance**
- 8\. peatükk - **Localization**
- 9\. peatükk - **Mapping**
