# Ruegen-Ranger-Pretest Codebuch #
Codebuch Stand 2021-01-07<br>
erstellt von Artur Stolinsky (as383@hdm-stuttgart.de)

## Inhalt
- Edgelist_Rügen-Ranger_Pretest.csv (Edgelist)
- Nodelist_Rügen-Ranger_Pretest.csv (Nodelist)
- Codebuch.md (Codierung der Datensätze)

## Ursprung und Datenerhebung

Im Pretest werden exemplarisch zehn vom Presserat öffentlich gerügte Artikel in einem Gesamtnetzwerk dargestellt. Die Daten wurden auf der Website des Presserats unter folgendem Link erhoben: (https://www.presserat.de/ruegen-presse-uebersicht.html). Die Artikel aus dem Pretest stammen von 1990 und 2020.

Das Netzwerk ist ein *gerichtetes three-mode Akteursnetzwerk*. Ausgangsgangspunkt für das Netzwerk ist der Presserat.

## Weitere Anmerkungen

Dieses Codebuch kann auch für das gesamte Projekt verwendet werden. Die Edges und Nodes bleiben dieselben, nur der Umfang des Gesamtnetzwerks ist erhöht.

# Nodes und dazugehörige Attribute


0 = Ziffer<br>
1 = Publikationsmedium


### Ziffern Pressekodex

Diese Nodes stehen für einzelne Ziffern des Pressekodex, gegen die verstoßen worden ist. Sie werden im Netzwerk zwischen dem Presserat und den gerügten Artikeln dargestellt. Ziffern, gegen die von keinem Artikel verstoßen worden sind, werden nicht in Nodelist und Netzwerk berücksichtigt. Die Ziffern 3, 5 und 14 - 16 werden nicht berücksichtigt.
Diese Kategorie besitzt folgende ***Attribute***:

**id**

eindeutige Codierung des Knoten, wird als "Ziffer" + Zahl angegeben (z.B. Ziffer10)

**name**

Vollständiger Name des Knotens (z.B. Pressekodex Ziffer 1)

**type**

Unterscheidung zwischen Ziffer und Publikationsmedium

0 = Ziffer<br>
1 = Publikationsmedium


### Publikationsmedium

Diese Nodes stehen für die Artikel, die eine Rüge vom Presserat erhalten haben. Sie werden außen im Netzwerk dargestellt. Diese Kategorie besitzt folgende ***Attribute***:

**id**

Anzeigename, entweder vollständig oder als Abkürzung (z.B. Bild, WAZ)

**name**

Vollständiger Name des Publikationsmediums + Online/Offline (z.B. Grazia Magazin Online, Westfälischa Abendzeitung Offline)

**region**

Handelt es sich um ein regionales oder überregionales Publikationsmedium?

1 = überregional<br>
2 = regional

**type**

Unterscheidung zwischen Presserat, Ziffer und Publikationsmedium

0 = Ziffer<br>
1 = Publikationsmedium

**published**

Definiert die Verfügbarkeit des Artikels

1 = online<br>
2 = offline


# Edge-Attribute

**weight**

Art der Rüge

1 = öffentliche Rüge<br>
2 = nicht-öffentliche Rüge

**year**

Definiert das Jahr, in dem die Rüge erteilt worden ist

**az**

Aktenzeichen (z.B. (0031/20/2))

**code**

Codierung des gerügten Artikels (z.B. Bild/1990/1)
