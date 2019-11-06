# Töökindla lahenduse "checklist"

## Müraga toimetulek 

Kuivõrd andurid on mürarikkad, siis tuleb sisendandmeid filtreerida (näiteks kasutada puhvrit). Filtreerima peab ainult kaugusandurite väärtuseid. Koodrite ja kompassi väärtused filtreeritakse "madalamas" kihis meie eest juba ära.

Filtri realiseerimine ja kasutamine on kirjeldatud [loengumaterjalides](https://github.com/iti0201/iti0201/tree/lecture-02).

Filtri puhvri pikkus mõjutab kui kiiresti robot uuele tegelikule väärtusele reageerib ja kui mürakindel ta on. Mida pikem puhver, seda mürakindlam, aga seda tuimem on filtri väljund.

### Filtri näide
```
Sisendjada [0.1 0.1 0.1 0.9 0.1 0.1 0.1 0.1 0.1] => peale filtreerimist [0.1 0.1 0.1 0.1 0.1 0.1 0.1 0.1 0.1]
```

### Testimine müraga simulaatoris
Müraga testimiseks kasutage võtit `--noise`.

## Nägemisulatus on piiratud
Kuna robotil on päriselus piiratud nägemisulatus, siis tuleks arvestada ainult nt 0.5 meetrise nägemisulatusega [testimiseks `--blind`]

## Mootorite juhtimine
Kuivõrd päriselus mootorid töötavad väga erinevalt (sõltub aku toitepingest jne), siis tuleb täpseks juhtimiseks kasutada tagasisidestatud juhtimist.
See tähendab, et
* Ei saa lihtsalt juhtida otse mootori protsenti muutes
* Mootori juhtimine arvestab koodritest arvutatud hetkkiirusi (vaata `get_right_wheel_encoder()` ja `get_left_wheel_encoder()` funktsioonid)
* Kasutama peaks lihtsat regulaatorit, mille abil juhtida mootori %-i
* st et määrate soovitud kiiruse hoopis kraadi/sekundis, mitte       protsentides ja siis    vaatate koodri väärtuste põhjal, kas tegelik       kiirus (kraadi/sekundis) on suurem või    väiksem kui soovitud kiirus:
   kui tegelik kiirus on liiga väike, siis %-ile +1
   kui tegelik kiirus on liiga suur, siis %-ile -1

Loengumaterjalides on kirjeldatud nt P-, PI-regulaator ja PID-regulaator, mida saab võtta aluseks oma juhtimi

### Mootorite testimine
Päriseluga rohkem sarnaste mootorite testimiseks saab kasutada võtit `--realmotors`

## Olekumasin
Ülesande loogika defineerimiseks olekumasinat (state machine) - kirjeldatud ja näide olemas loengumaterjalides

### Näide
```
state = "searching"
if state == "searching":
    # spin around very slowly
    # ...
    if object_in_front:
        state = "approaching"
elif state == "approaching":
    # drive towards object (in a straight line!)
    # ...
    if not object_in_front:
        state = "searching"
```

## Testimine realistlikumalt simuleeritud robotiga

Kuivõrd päriselus on roboti andurid mürarikkad ja mootorid mitteideaalsed, siis on mõistlik proovida enne roboti peal rakendamist oma algoritmi järjest keerukamate simulatsiooni "võtmetega".
See tähendab, et käsk käivitamiseks on `robot_test uniid O1 1 --blind --noise --realmotors`

Kõik korraga saab panna peale päriselu meenutavad sätted peale "--realism" võtmega.

- `--blind` => max nägemiskaugus laseril piiratud 0.5 meetrile
- `--noise` => kaugusanduritel müra
- `--realmotors` => mootorid ei toimi ideaalselt

## Loogiline ülesehitus

Nagu loenguslaididel kirjeldatud, siis võiks järgida Sense-Plan-Act loogikat ja ehitada oma lahendus üles näiteks nii
```
# Initialize values
laser_buffer_length = 1
laser_buffer = [0] * laser_buffer_length

while True:
    # Sense
    laser_value = noise_filter(.....)

    # Plan
    if state == "somestate":
        # do something...
        pass
    elif state == "otherstate":
        # do something else...
	pass

    # Act
    robot.set_left_wheel_speed(motor_controller(.......))
    robot.set_right_wheel_speed(motor_controller(.......))
```
