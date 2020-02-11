# SVG Glitch

### Aufgabe:
Experimentieren mit SVG-Code, um die Art und Weise herauszufinden, wie SVG aufgebaut ist und welche Tags für die Darstellung nötig sind. Außerdem sollte durch verschiedene Attribute herausgefunden werden, wie sich SVGs glitchen lassen.

### Workshop

Zunächst suchte ich im Internet nach geeigneten SVGs. Diese fand ich letztendlich bei https://ionicons.com/. Zunächst öffnete ich das SVG in Visual Studio Code, um den Quellcode des Bildes einzusehen. Für diese Aufgabe wählte ich ein Fahrrad aus, welches ich animieren wollte. An dem Fahrrad selbst änderte ich nur die Farbe. Dies kann man in dem Tag `use` mit dem Attribut `fill` ändern.Ursprünglich wollte ich erreichen, dass sich die Räder des Fahrrads nach hinten drehen, während sich das Fahrrad nach vorne bewegt. Dies stellte sich jedoch etwas schwierig heraus, da ich bei dem Versuch einzelne Pfade eines ganzen SVGs diese Pfade daraus entfernt habe und diese nicht mehr den ursprünglichen Platz einnehmen konnten. Darum entschied ich mich für ein zweites Fahrrad, das ich ebenfalls animierte, das im Windschatten des anderen Fahrrads fahren sollte.

Für die zwei Fahrräder benutzte ich ein gemeinsames `svg`Tag, in welchem beide Fahrräder enthalten sind. Für den Text benutzte ich ein neues `svg`tag in der gleichen Datei. So konnte ich die Richtung der Animation leichter für die jeweiligen Komponenten steuern. Hierfür benutzte ich das tag `animate transform`. Hierbei sind die Attribute `from`, `to`, `begin`, `dur` und `repeatCount`.

* `from`: Gibt den Startpunkt der Animation an
* `to`: Gibt den Endunkt der Animation an
* `begin`: Gibt an, nach wie vielen Sekunden die Animation starten soll
* `dur`: Gibt an, wie lange die Animation dauern soll
* `repeatCount`: Gibt an, wie oft sich die Animation wiederholen soll.

Mit dem tag `filter`können außerdem auch Filter in die SVGs integriert werden. Dies habe ich ebenfalls getan, was in einer Verpixelung sichtbar wird. Dieser Filter wurde von CodePen.io übernommen.




### Endprojekt

Im Hinblick auf mein Endsemesterprojekt wollte ich etwas erstellen, das mehr glitcht und für den Betrachter interessanter wirkt. Darum habe ich mir zum Ziel gesetzt, einen im Hintergrund liegenden Strich zu generieren, der den Glitch-Effekt zusätzlich unterstützt.
Auf der Suche nach dem passenden Icon bin ich erneut auf https://ionicons.com/ gelandet. Dieses mal entschied ich mich für einen Geist, da ich finde, dass dieses Icon gut zu dem Glitch-Thema insgesamt passt. Zu Beginn sah alles noch sehr langweilig aus, da der Effekt noch nicht genügend wie ein Glitch aussah. Aus diesem Grund versucht ich mit Hilfe des Internets einen Effekt zu erzeugen, der dies spannender macht und gleichzeitig meine eigenen Vorstellungen erfüllen würde. Hierbei bin ich ebenfalls auf CodePen.io und fand ein für mich passendes Glitch. Da ich mich selbst an die Herausforderung wagen wollte, einen Glitch-Effekt zu erzeugen, orientierte ich mich zwar an dem Beispiel, änderte jedoch viele Komponenten um es an meine individuellen Vorstellungen anzupassen.

Für den Text benutze ich wieder, wie bereits in dem Workshop, den `animateTransform`, sowie auch den `filter`tag. Dadurch animierte ich den text und lies ihn verpixelter aussehen.

Für den Geist nutzte ich wieder ein separates `SVG`tag. Ich bin der Meinung, dass ich somit besser auf die einzelnen Komponenten zugreifen kann.

Mit dem tag `linearGradient` erzeugte ich den Farbverlauf in dem Geist und färbte ihn in den Farben meiner Wahl. Mit `feFlood` generierte ich den klassischen Glitch-Effekt mit dem rot-grünen Rand. Darum wählte ich die Farben schwarz, grün und rot.

Um den Balken auf verschiedene Höhen zu setzen, kontrollierte ich die Höhe bzw. Position mit dem Attribut `values`, die dazugehörigen Zeiten, sodass sich das Ganze auch in einem schnelleren Tempo bewegt, definierte ich über das Attribut `keyTimes` und mithilfe von `repeatCount="indefinite` hört die Animation erstmal nicht auf. `feMerge` ist das Kernattribut des Filters und erbt somit die vorangegangenen Werte der anderen tags innerhlab des `filter`tags.








