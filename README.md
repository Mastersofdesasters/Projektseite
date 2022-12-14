# Projektseite
## [_Spielkonzept_](#Spielkonzept)
## [_Programm_](#Programm)
## [_Code_](#Code)
## [_Zum Spiel_](#ZumSpiel)


### Spielkonzept <a name="Spielkonzept"></a>
Bei unserem Spiel handelt es sich um ein 2D - Jump and Run - Spiel mit der Hauptspielfigur Schnappi dem Krokodil. Der Sinn des Spiels ist es, dass Schnappi, indem der Spieler ihn von Block zu Block springen lässt, die letzte Plattform erreicht, ohne vorher zu fallen. Gelingt dies dem Spieler nicht, so fängt das Spiel von vorne an. Gelingt es ihm, so wird er zum nächsten Level weitergeleitet. Gespielt wird mit den Pfeil-Tasten, damit lässt sich Schnappi nach links, rechts, oben oder unten bewegen. Hier einmal ein Bild von unserem ersten und für den Spieler einfachsten Level:
![Screenshot (19)](https://user-images.githubusercontent.com/111355300/203500186-cdef4137-061c-4a36-b179-4e5d06a89f58.png)



### Programm <a name="Programm"></a>
Wir haben unser Spiel mit dem Programm [Snap](https://snap.berkeley.edu/) programmiert. Dafür hatten wir uns entschieden, nachdem wir auch andere Programme wie [Greenfoot](https://www.greenfoot.org/door) angesehen und ausprobiert hatten. Mit [Snap](https://snap.berkeley.edu/) kamen wir jedoch am besten zurecht, da es ineinzelne Kategorien mit verständlichen Befehlen aufgeteilt ist, wie z.B. "Control" oder "Sensing". Bevor wir angefangen haben, zu programmieren, haben wir uns noch einige Youtube-Videos angeschaut, um eine erste Idee von Snap und den möglichen Befehlen zu bekommen.
[Snap](https://snap.berkeley.edu/) ist die Nachfolgeversion von BYOB (Build your own blocks) und baut auf der Programmiersprache Scratch auf. Designt wurde es von Brian Harvey und Jens Mönig und 2011 von der University of California, Berkeley, publiziert. Daher auch der Name "Snap Berkeley".

### Code <a name="Code"></a>

**Bewegungen**

1. Erscheinung / Kostüm Schnappis: Für das Krokodil-Kostüm von Schnappi haben wir ein passendes Bild aus dem Internet ausgesucht, in das Skript eingefügt und es mit der Bearbeitungsfunktion für die Sprites / Figuren ausgeschnitten. Dieses Kostüm bleibt immer das gleiche:
![image](https://user-images.githubusercontent.com/111355300/207529841-3040670e-0dd4-4d34-8e74-1dc8298042a4.png)


2. Bewegung entlang der x-Achse: Hierfür haben wir mit den Pfeiltasten gearbeitet und die Befehle unten im Bild zusammengefügt:
![image](https://user-images.githubusercontent.com/111355300/207528400-32f858e1-2e25-4601-a9b7-ce27af363491.png)

3. Bewegung entlang der y-Achse: Hierfür haben wir ebenfalls mit den Pfeiltasten gearbeitet, bzw. mit denen für oben und unten. Wird die obere Taste gedrückt, dann führt Schnappi jedoch eine Bewegung sowohl in x- als auch in y-Richtung aus. Diese soll das Springen (s.u.) realistischer erscheinen lassen, als wenn Schnappi nur nach oben und unten springen würde. Der zugehörige Code ist im Bild zu sehen:
![image](https://user-images.githubusercontent.com/111355300/207529126-b06e81bf-8b86-45d4-a271-d5bc10b8e38d.png)
![image](https://user-images.githubusercontent.com/111355300/207529251-7d00b5c2-9e52-477e-8387-02767ddaa4f7.png)


4. Das Springen: Das Springen war das Komplizierteste, dafür haben wir uns im Internet, bei ehemaligen Schülern und Herrn Buhl Beispiele angeschaut. Das Ziel war, dasss Schnappi mit einer Schwerkraft springt und grüne Farbblöcke so als Plattform erkennt, dass er auf diesen stehen bleibt oder wenn er auf dem Zielobjekt ,,Plattform" landet. Ansonsten sollte er fallen. Zuerst haben wir eine Geschwindigkeit in y-Richtung festgelegt, die sich zurücketzt, sodass Schanppi nicht ins Unendliche fliegt,  mit der Varibale ,,speedY". Damit der folgende Vorgang die ganze Zeit ausgeführt wird, ahben wir ein ,,forever" eingefügt. danach haben wir gesagt, er soll fallen bis er den Rand der Stage berührt, dies passiert sobald er nicht mehr einen grünen Farbblock oder die Plattform berührt und y-Geschwindigkeit wird geändert. Um die Bewegung realistischer aussehen zu lassen, haben wir mithilfe der Variablen "Readyforjump" und dem Befehl "Key 'Up Arrow' pressed" den Springvorgang modelliert. 
Dieser Vorgang wird aktiviert für jedes Level, sobald dieses vom Spieler ausgewählt wurde. Im unteren Bild beispielhaft für Level 1 zu sehen.

![image](https://user-images.githubusercontent.com/111355300/207529476-f2014cfb-19b4-48bb-b401-506099bc7585.png)

**Level**
Alle folgenden Befehle liegen nicht mehr in dem Skript von Schnappi, sondern in den Skripten der Stage und der jeweiligen Sprites.
Generell haben wir für Startbildschirm, Auswahl der Level etc. mit den zusammengehörenden Befehlen "Broadcas" und "When I receive" gearbeitet. Außerdem haben wir die Befehle "Hide" und "Show" für die jeweiligen Sprites benutzt.
1. Startbildschirm: Mithilfe der Bearbeitungsfunktion haben wir einen Startbildschirm entworfen. Auf diesem befindet sich ein Sprite mit dem Namen "Startbutton". Wenn dieser vom Spieler gedrückt wird, broadcastet er "Startbutton gedrückt".
![Screenshot (25)](https://user-images.githubusercontent.com/111355300/207534364-491d6481-d3a2-44d8-b989-5c24364db1cd.png)

2. Levelauswahl: Das Skript der Stage "received" dann diese Information und daraufhin verschwindet der gesamte Startbildschirm mit dem Befehl "Hide", während der Bildschirm für die Levelauswahl erscheint. Dort befinden sich drei Sprites, jeweils eines pro Level:
![Screenshot (26)](https://user-images.githubusercontent.com/111355300/207534551-11160155-3b4e-4eb0-90a6-344b70920bc0.png)

Anschließend hat der Leser die Möglichkeit, zwischen den drei Leveln auszuwählen, wobei Level 1 das einfachste und Level 3 das schwierigste ist. 
Hier sind einmal die Bildschirme der Level zu sehen:
Level 1: 
Level 2
Level 3
Analog zum Startbildschirm broadcastet der vom Spieler angeklickte Sprite "Show Level ..." bspw. "Show Level 1"
BIld
Dieser Broadcast wird in der Stage wieder received und daraufhin verschwindet der Bildschirm der Levelauswahl und dessen gesamte Sprites durch den Befehl "Hide". Nun erscheint Schnappi und das Level. Außerdem wird der Broadcast auch in Schnappis Stage mit "When I receive" empfangen, sodass dadurch der oben beschriebene Befehl für das Springen aktiviert wird.
Bild
Alle anderen Befehle werden mit den Tasten ausgeführt und sind unabhängig vom Broadcast / When I receive. Nun kann der Spieler anfangen, zu spielen.

### Zum Spiel <a name="ZumSpiel"></a>
