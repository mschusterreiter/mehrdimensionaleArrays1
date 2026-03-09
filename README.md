
# Übung 17 - Mehrdimensionale Arrays


## 1. Aufgabe

Setzen Sie folgendes Klassendiagramm um:

<p align="center">
  <img src="/assets/images/UML1.png" alt="Bildbeschreibung" />
</p>

**Beschreibung:**

- `addMatrices(int[][] matrixA, int[][] matrixB)`: Addiert zwei Matrizen und gibt die Summe als Matrix zurück. Prüfen Sie, ob die beiden Matrizen die richtigen Dimensionen haben. 
- `subMatrices(int[][] matrixA, int[][] matrixB)`: Subtrahiert zwei Matrizen und gibt die Differenz als Matrix zurück. Prüfen Sie, ob die beiden Matrizen die richtigen Dimensionen haben.
- `multiplyMatrices(int[][] matrixA, int[][] matrixB)`: Multipliziert zwei Matrizen und gibt das Produkt zurück. Prüfen Sie, ob die beiden Matrizen die richtigen Dimensionen haben.
- `transposeMatrix(int[][] matrix)`: Transponiert die angegebene Matrix und gibt diese zurück.
- `scalarMultiplication(int[][] matrix, int scalar)`: Skaliert die angegebene Matrix und gibt diese zurück.
- `isSquareMatrix(int[][] matrix)`: Prüft, ob die angegebene Matrix quadratisch ist. Wenn ja, soll `true` zurückgegeben werden, sonst `false`. 
- `identityMatrix(int size)`: Erzeugt eine Einheitsmatrix der Größe `size`. Eine Einheitsmatrix ist eine quadratische Matrix, bei der alle Elemente auf der Hauptdiagonalen den Wert `1` haben. Alle anderen Elemente haben den Wert `0`. 
- `isSymmetricMatrix(int[][] matrix)`: Prüft, ob die angegebene Matrix symmetrisch ist. Wenn ja, soll `true` zurückgegeben werden, sonst `false`. Eine Matrix ist symmetrisch, wenn sie gleich ihrer transponierten Matrix ist. 
- `determinant(int[][] matrix)`: Berechnet die Determinante der angegeben Matrix. Es ist ausreichend, wenn die Methode für `n = 1, 2, 3` funktioniert. 
**Zusatz:** Sollten Sie die Determinante auch für höhere Dimensionen berechnen wollen, verwenden Sie die Laplace-Erweiterung.

**Hinweis:** Wenn Sie nicht wissen, wie die einzelnen Operationen durchgeführt werden, schauen Sie sich die Wikipedia Einträge dazu an. Die sind (ausnahmsweise) ganz in Ordnung und erklären die Operationen (teilweise) anhand von Beispielen. 

Um Ihr Programm zu testen, erstellen Sie eine `Main`-Klasse, welche die `main`-Methode beinhaltet:
- `main(String[] args)`: Testen Sie Ihr Programm.

## 2. Aufgabe

Setzen Sie folgendes Klassendiagramm um:

<p align="center">
  <img src="/assets/images/UML2.png" alt="Bildbeschreibung" />
</p>

Hinweis für alle Klassen: Benötigte `getter` und `setter` sind zu implementieren.

Beschreibung der `Auto`-Klasse:

- Keine der Eigenschaften darf leer (d.h. auch nicht nur whitespaces) oder null sein.
- Das Kennzeichen muss zudem mindestens zwei Buchstaben und eine Zahl beinhalten. Außerdem muss das erste Zeichen ein Buchstabe sein. Um zu überprüfen, ob ein String einen Buchstaben oder eine Zahl enthält, können Sie sogenannte Regular Expressions verwenden: 

<p align="center">
  <img src="/assets/images/COD1.png" alt="Bildbeschreibung" />
</p>

Beschreibung der `Parkhaus`-Klasse:

- Die Eigenschaften `zeilen` und `spalten` dürfen nur Werte annehmen, die größer `0` sind. 
- Im Konstruktor wird die Eigenschaft `parkhaus` erstellt. Die Größe des Parkhauses entspricht den Werten von `zeilen` und `spalten`.
- `parkAuto(Auto auto, int zeile, int spalte)`: Parkt das angegebene Auto an der angegebenen Stelle im Parkhaus. Dies ist nur möglich, wenn der jeweilige Parkplatz auch frei ist. Kann das Auto geparkt werden, liefert die Methode `true`, sonst `false`. 
- `removeAuto(int zeile, int spalte)`: Entfernt das Auto, an der angegebenen Stelle im Parkhaus. Zurückgeliefert wird jenes Auto, welches entfernt wurde. 
- `getAuto(int zeile, int spalte)`: Gibt das Auto an der angegebenen Stelle zurück.
- `isParkplatzFrei(int zeile, int spalte)`: Liefert `true`, wenn der angegebene Parkplatz leer ist. Wenn nicht, wird `false` zurückgegeben. 
- `findFreeParkplatz()`: Liefert ein `int[]`, welches die Zeile und Spalte vom ersten freien Parkplatz im Parkhaus beinhaltet- Sollte kein Parkplatz frei sein, soll im zurückgegebenen Array nur das erste Element mit dem Wert `-1` befüllt werden. 
- `countFreeParkplaetze()`: Liefert die Anzahl an freien Parkplätzen im Parkhaus.
- `countBesetzteParkplaetze()`: Liefert die Anzahl an besetzten Parkplätzen im Parkhaus.
- `listParkedAutos()`: Gibt ein `Auto[]` zurück, welches alle Autos aus dem Parkhaus enthält.
- `isParkplatzValid(int zeile, int spalte)`: Liefert `true`, wenn der angegebene Parkplatz gültig ist. Wenn nicht, wird `false` zurückgegeben. 
- `moveAuto(int aktZeile, int aktSpalte, int neuZeile, int neuSpalte)`: Verschiebt ein Auto von einem aktuellen Parkplatz auf einen anderen freien Parkplatz. Liefert `true`, wenn das Auto verschoben werden konnte. Wenn nicht, wird `false` zurückgegeben. 
- `findAuto(String kennzeichen)`: Sucht im Parkhaus nach dem Auto mit dem angegebenen Kennzeichen. Wurde das Auto gefunden, wird ein `int[]`, welches die Zeile und Spalte vom Parkplatz des Autos im Parkhaus beinhaltet zurückgegeben. Konnte das Auto nicht gefunden werden, soll der erste Eintrag im `int`-Array `-1` sein. 
- `clearParkhaus()`: Alle Autos werden aus dem Parkhaus entfernt. Zurückgegeben wird ein `Auto[]`, welches alle Autos beinhaltet, die entfernt werden mussten. 
- `printStatus()`: Gibt Infos wie die freien und besetzten Parkplätze des Parkhauses aus. Außerdem soll von jedem besetzten Parkplatz die Stelle im Parkhaus, sowie das Kennzeichen des zugehörigen Autos ausgegeben werden. 

Um Ihr Programm zu testen, erstellen Sie eine `Main`-Klasse, welche die `main`-Methode beinhaltet:
- `main(String[] args)`: Testen Sie Ihr Programm.
