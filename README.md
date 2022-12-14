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


### Zum Spiel <a name="ZumSpiel"></a>
