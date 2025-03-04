# Monopoly_SE2
Herzlich Willkommen, zu unserer softwareseitigen Entwicklung vom Spiel Monopoly für SE2 von Aahil Mohammad, Fabio Sapia, Richard Gietzelt, Batuhan Dag.

## Vorwort
Als ersten Schritt unserer softwareseitigen Implementierung eines Brettspiels, im Kurs Software Engineering II, haben wir Monopoly als Spiel gewählt, da es eine Vielzahl an relevanten Anforderungen und Herausforderungen bietet. Die Komplexität der Spielregeln softwareseitig zu modellieren, sowie die dynamischen Spielerinteraktionen, sowie der zahlreichen Statusänderungen hat es für uns zu einem spannenden Projekt gemacht, welches wir im nachfolgenden Repository dokumentiert festgehalten haben.

## Spielablauf
Es beginnt damit, dass jeder Spieler ein Startkapital von 1.500 Monopoly-Dollar erhält. Der Spielablauf gestaltet sich kundenbasiert: Die Spieler würfeln und verschieben ihre Spielfigur entsprechend der Augenzahlen auf den Würfeln. Je nachdem auf welchem Feld sie landen, führen sie spezifische Aktionen aus, die die Dynamik und Strategie des Spiels bestimmen.

Die Feldaktionen selbst sind vielfältig und umfassen unterschiedliche Möglichkeiten, zum Beispiel, wenn ein Spieler auf einem unbebauten Grundstück landet, hat er die Wahl, dieses zu kaufen oder es zur Auktion freizugeben, falls kein Interesse am Kauf besteht. Wenn ein Spieler jedoch alle Grundstücke eines Farbblocks besitzt, kann er Häuser und Hotels darauf bauen, um die Mieteinnahmen zu erhöhen. Landet ein Spieler auf ein Grundstück eines anderen Spielers, ist er verpflichtet die Miete zu bezahlen. Dabei spielt es eine Rolle, ob ein Gebäude darauf gebaut wurde.

Zusätzlich existieren noch Ereignis- und Gemeinschaftsfelder. Landet ein Spieler auf so einem Feld ist er ebenfalls verpflichtet die Leistung zu erfüllen, die auf den dazugehörigen Karten geschrieben ist. Steuerfelder sind ebenfalls Verpflichtend, hier muss der Spieler ein bestimmten Betrag oder einen prozentualen Anteil von seinem Kapital abgeben, wenn er auf so einem Feld landet.

Ein weiteres Sonderfeld ist das Gefängnisfeld. Wenn ein Spieler in das Gefängnis geschickt wird, hat er so lange auszusetzen, bis er dreimal einen Pasch gewürfelt hat oder im Vorhinein eine entsprechende Karte gezogen hat, die „du kommst aus dem Gefängnis raus“ Karte.

Ein wichtiger strategischer Aspekt ist das Bauen von Gebäuden. Wie anfangs erwähnt hat der Spieler die Möglichkeit Häuser auf seine Grundstücke zu bauen, wenn er alle Grundstücke des Farbblocks besitzt. Es können maximal 4 Häuser darauf gebaut werden, um die Mieteinnahmen zu erhöhen.

Eine Auswahl, die die Spieler treffen können um an zusätzliches Kapital zu gelangen ist es, Hypotheken auf ihre Grundstücke zu veranlassen. Als Folge draus entsteht, dass alle Mieteinnahmen aussetzen, bis die Hypothek abbezahlt wurde.

Das Spiel endet für einen Spieler, wenn dieser bankrott geht, sprich: Wenn er seine Schulden nicht mehr begleichen kann. Seine Vermögensgegenstände (Gebäude, Grundstücke, etc…) gehen, falls vorhanden, an die Gläubiger über. Falls keine Gläubiger vorhanden sind, geht der Besitz an die Bank.

Das Ziel des Spiels ist dabei, durch kluge Investitionen und strategisches Bauen das Spiel zu dominieren und alle Mitspieler in den Bankrott zu treiben.

## Data dictionary

Unser Data Dictionary beschreibt die Hauptkomponenten unsere softwareseitigen Implementierung von Monopoly. Es stellt sicher, dass alle Attribute und Funktionen konsistent dokumentiert und für die spätere Implementierung bereit sind.
Im Folgenden sind die wichtigsten Entitäten, die wir näher beschrieben haben.
Use Case Diagramm:

## Klassendiagramm

Beim Klassendiagramm haben wir uns auf die Daten aus dem Data Dictionary, sowie den Use Cases bezogen, um so die richtigen Beziehungen und Kardinalitäten aufzuzeigen. Das Klassendiagramm zeigt alle Entitäten und in was für Beziehungen sie untereinander stehen. Zum Beispiel das Spiel selbst, welches seine verschiedenen Attribute und Methoden besitzt und das Spielfeld, welches in einer 1 zu 1 Beziehung steht.

Anhand des Klassendiagramms wird die Komplexität deutlich, Monopoly softwareseitig umzusetzen. Wir sind daher auch gemeinsam als Team explizit über die Entitäten drüber gegangen, um zu gewährleisten, dass alle Attribute und Methoden korrekt und vollständig aufgeführt werden.

Als Sequenz haben wir uns für die „Spieler steht auf einem Sonderfeld“ Möglichkeit entschieden. Das Sequenzdiagramm hat uns dabei geholfen, die Abfolge der Methodenaufrufe, sowie die Nachrichten zwischen den Objekten zu verstehen. Diese Diagramme helfen uns später in der Implementierungsphase, die einzelnen Abläufe genau programmieren zu können.

**Ablauf:**
1. Aktion auf dem Spielfeld: Der Spieler betritt ein Spielfeld und löst die Methode *Aktion ausführen()* aus.
2. Sonderfeld: Wenn es sich um ein Sonderfeld handelt, wird eine spezifische „Sonderaktion“ ausgeführt.
3. Grundstücksfeld: Hier gibt es mehrere Möglichkeiten:
- falls das Grundstück niemandem gehört, wird dem Spieler die Option angeboten, das Grundstück zu kaufen. Akzeptiert er -> Zahlung und das Eigentum wird übertragen
- Gehört das Grundstück einem anderen Spieler, wird die Miete berechnet und der aktuelle Spieler muss diese zahlen. Die Miete wird dem Besitzer gutgeschrieben
- Gehört das Grundstück dem Spieler selbst, ist keine Aktion erforderlich

Learning: 

Klassendiagramm finden Sie hier: 



