# SVG Glitch

#### Aufgabe:
Experimentieren mit SVG-Code, um die Art und Weise herauszufinden, wie SVG aufgebaut ist und welche Tags für die Darstellung nötig sind. Außerdem sollte durch verschiedene Attribute herausgefunden werden, wie sich SVGs glitchen lassen.

### Workshop

Zunächst suchte ich im Internet nach geeigneten SVGs. Diese fand ich letztendlich bei https://ionicons.com/. Zunächst öffnete ich das SVG in Visual Studio Code, um den Quellcode des Bildes einzusehen. Für diese Aufgabe wählte ich ein Fahrrad aus, welches ich animieren wollte. An dem Fahrrad selbst änderte ich nur die Farbe. Dies kann man in dem Tag `use` mit dem Attribut `fill` ändern.Ursprünglich wollte ich erreichen, dass sich die Räder des Fahrrads nach hinten drehen, während sich das Fahrrad nach vorne bewegt. Dies stellte sich jedoch etwas schwierig heraus, da ich bei dem Versuch einzelne Pfade eines ganzen SVGs diese Pfade daraus entfernt habe und diese nicht mehr den ursprünglichen Platz einnehmen konnten. Darum entschied ich mich für ein zweites Fahrrad, das ich ebenfalls animierte, das im Windschatten des anderen Fahrrads fahren sollte.

Für die zwei Fahrräder benutzte ich ein gemeinsames `svg`Tag, in welchem beide Fahrräder enthalten sind. Für den Text benutzte ich ein neues `svg`tag in der gleichen Datei. So konnte ich die Richtung der Animation leichter für die jeweiligen Komponenten steuern. Hierfür benutzte ich das tag `animate transform`. Hierbei sind die Attribute `from`, `to`, `begin`, `dur` und `repeatCount`.

`from`: Gibt den Startpunkt der Animation an

`to`: Gibt den Endunkt der Animation an

`begin`: Gibt an, nach wie vielen Sekunden die Animation starten soll

`dur`: Gibt an, wie lange die Animation dauern soll

Mit dem tag `filter`können außerdem auch Filter in die SVGs integriert werden. Dies habe ich ebenfalls getan, was in einer Verpixelung sichtbar wird. Dieser Filter wurde von CodePen.io übernommen.
