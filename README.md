

# Gøy med Pycom og Python
Devicene dere har fått utdelt er FiPy som støtter en rekke nettverksteknologier. I tillegg har dere fått et sensor-board som har blant annet lyssensorer, temperatursensor og akselorimeter. I tillegg har sensorboardet en usb-kontakt som gjør at du kan programere

Dokumentasjonen på devicene finner dere her:
https://docs.pycom.io/

Jeg har testet gjennom det enkleste tenkelige programmet og har beskrevet prosessen her, for en rask start:

## Install.
Dere trenger en editor med support for PyCom sine devicer. Det er to alternativ:
- MS Visual Studio Code med plugin
- Atom med PyMakr plug-in.

Jeg beskriver kun prosessen for Atom .

- Last ned Atom fra atom.io
- Installere PyCom plugin fra Atom -> Preferences -> Install. Søk opp offisiell "PyCom" plug-in. Installer denne.

## RGB-blink
For å komme igang skal vi kjøre et lite program som blinker dioden i forskjellige farger.
Jeg har laget et repo med koden tilgjengelig. Koden ligger i dir "RGB-blink". Editoren skal kjenne igjen koden som et PyCom prosjekt.

Prosjektet består av to filer:
- pymakr.conf som inneholder konfigurasjonen.
- main.py som inneholder programkoden.

For å kjøre kode på FiPy må du først finne adressen til porten den er koblet i. Kjør:

"ls /dev/cu.usbmodemPy*"

Hos meg ble dette: "/dev/cu.usbmodemPyfaa1b1""

Oppdater property "address" i pymakr.conf med denne verdien. Address kan også inneholde en IP-addresse hvis devicen er satt opp med nettverk.

Test oppsettet ved å trykke connect i editoren. Høyreklikk på main.py og vel "run"

Dokumentasjonen fra produsenten finner dere her:
https://docs.pycom.io/gettingstarted/programming/first-project

## Sensoravlesning
For å finne ut hvordan du leser av sensorer kan du lese følgende dokumentasjon:
https://docs.pycom.io/tutorials/pysense
https://startiot.telenor.com/learning/pysense-quick-start-guide/


## Managed IoT:
Telenor har laget en tjeneste som kan motta informasjon fra sensorer trådløst.  
https://startiot.telenor.com/
