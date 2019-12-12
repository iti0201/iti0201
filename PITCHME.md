## ITI0201<br />Robotite Programmeerimine

---
### Robot Operating System (ROS)

---
## Meeleolu tekitamiseks...

---
![ROAM exoskeleton](https://www.youtube.com/embed/Rr_5XjJUfQ0)

---
![Ski robot challenge](https://www.youtube.com/embed/6yj4S9nfgY4)

---
![SEWBO](https://www.youtube.com/embed/sjjzo3c7b_8)

---
![DelFly Nimble](https://www.youtube.com/embed/CEhu-FePBC0)

---
## Ajakava

Nädal |  | Tegevus
------|--|--------
@size[large](**16**) | @size[large](@color[goldenrod](Loeng)) | @size[large](Robot Operating System ülevaade)
  | @size[large](@color[darkgreen](Praktikum)) | @size[large]("Labürint" kaitsmine)

---
## ROS

---
[ETH Zurich slaidid](http://www.rsl.ethz.ch/education-students/lectures/ros.html)

---
## ROS2

---
ROS1 ehitati PR2 roboti kasutusmalli jaoks

---?image=assets/image/pr2.jpg&size=auto 75%

---
ROS1 algne kasutusmall
@ul
- üksainus robot
- tööjaam pardaarvuti
- puudusid reaalajanõuded
- suurepärane võrguühendus (kaabel või väga hea wifi)
- põhirakendused uurimistöös
@ulend

---
ROS2 põhilised panused
@ul
- multirobotsüsteemid
- sardsüsteemid ja -platvormid
- reaalajasüsteemid
- mitteideaalsed võrguühendused
- tootestamisega arvestamine
@ulend

---
ROS2 omadused
@ul
- Puudub _roscore_ (ROS Master)
- C++14 (tulevikus plaanis C++17)
- Python3.6+
- DDS (väga ulatuslikud seadistusvõimalused)
- Turvalisus (hea ühilduvus algusest peale Secure ROS laiendusega)
@ulend

---?image=assets/image/api_levels.png&size=auto 75%
---?image=assets/image/dds_vendors.png&size=auto 75%
---?image=assets/image/net_spectrum.png&size=auto 75%
---?image=assets/image/bridge.png&size=auto 75%
