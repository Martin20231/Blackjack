# Beginner Black Jack

Das Array "variant" enthält vier Unicode-Zeichen, die Herz, Pik, Karo bzw. Multiplikationssymbole darstellen.

Das Array "werte" enthält 13 Strings, die die Werte von Spielkarten darstellen, von "Zwei" bis "Ass" und einschließlich "König", "Dame" und "Bube".

Das Array "chip_wert" enthält vier Zahlen, die die Werte verschiedener Arten von Spielchips darstellen, mit Werten von 1, 5, 25 und 100.

Vier Konstanten sind definiert, "chip_weiß", "chip_rot", "chip_grün" und "chip_schwarz", mit Werten von 1, 5, 25 bzw. 100. Diese Konstanten stellen wahrscheinlich die Werte bestimmter Arten von Glücksspielchips dar.

Es werden vier Variablen definiert, "anz_weiß", "anz_rot", "anz_grün" und "anz_schwarz", mit Anfangswerten von 10, 8, 6 bzw. 3. Diese Variablen können die Anzahl der dem Spieler zur Verfügung stehenden Chips des jeweiligen Typs darstellen.

Vier weitere Variablen, "anz_weiß1", "anz_rot1", "anz_grün1" und "anz_schwarz1", sind ebenfalls definiert, aber sie werden mit 0 initialisiert und ihr Zweck ist ohne weiteren Kontext nicht sofort klar.

Zwei weitere Variablen, "chipGesamtStart_spieler" und "einsatz_geld", sind mit Anfangswerten von 500 bzw. 0 definiert. Diese Variablen können die Gesamtzahl der Chips, die der Spieler hat, und den aktuellen Betrag der Chips, die er setzt, darstellen.

Schließlich aktualisiert das Programm den Textinhalt eines HTML-Elements mit der ID "geld_spieler", um die aktuelle Gesamtzahl der Chips des Spielers anzuzeigen.

Wenn die Funktion "klick_weiß" ausgeführt wird, subtrahiert sie zunächst 1 von der Variablen "anz_weiß" und prüft, ob der resultierende Wert kleiner als 1 ist. Ist dies der Fall, wird eine Warnmeldung angezeigt, um den Benutzer darüber zu informieren, dass er keine weißen Chips mehr hat. Die Schaltfläche "chip_weiß_stop" wird ebenfalls deaktiviert, indem ihre onclick-Eigenschaft auf null gesetzt wird.

Anschließend wird die Variable "chipGesamtStart_spieler" aktualisiert, indem der Wert eines weißen Chips abgezogen wird. Der Gesamtwert der vom Spieler gesetzten Chips wird berechnet, indem die Anzahl der aktuell gesetzten weißen Chips mit dem Wert eines weißen Chips multipliziert wird. Dieser Wert wird zu den Variablen "einsatz_geld" und "einsatz_geld_cpu" addiert, die den Betrag der vom Spieler bzw. von der CPU gesetzten Chips darstellen.

Der Textinhalt mehrerer HTML-Elemente wird dann aktualisiert, um diese Änderungen widerzuspiegeln. Das Element "anzahl_chip_weiß" zeigt die verbleibende Anzahl weißer Chips an, das Element "geld_spieler" zeigt die Gesamtanzahl der Chips des Spielers an, und die Elemente "geld_einsatz_spieler" und "geld_einsatz_cpu" zeigen den Betrag der vom Spieler bzw. von der CPU gesetzten Chips an.

Erreicht die Gesamtzahl der Chips des Spielers den Wert 0, wird eine Warnmeldung angezeigt, die den Spieler darüber informiert, dass er das Spiel verloren hat.

Die Funktion "klick_rot" funktioniert ähnlich wie die Funktion "klick_weiß", allerdings mit Variablen und Elementen, die sich auf die roten Chips beziehen.


Dies sind zwei weitere JavaScript-Funktionen zur Verarbeitung von Benutzereingaben in einem Tippspiel. Die erste Funktion, "klick_grün()", wird ausgelöst, wenn der Benutzer auf den grünen Chip klickt. Sie verringert die Anzahl der grünen Chips des Spielers ("anz_grün"), prüft, ob der Spieler noch grüne Chips übrig hat, und deaktiviert die grüne Chip-Schaltfläche, falls nicht. Außerdem wird der Wert eines grünen Chips von der Gesamtzahl der Chips des Spielers abgezogen ("chipGesamtStart_spieler"), der Gesamtwert des Spielereinsatzes anhand der Anzahl der grünen Chips und ihres Wertes berechnet ("summeChips"), dieser Wert zum Gesamteinsatz des Spielers addiert ("einsatz_geld"), derselbe Wert zum Gesamteinsatz des Computers addiert ("einsatz_geld_cpu") und die entsprechenden HTML-Elemente aktualisiert, um diese Änderungen widerzuspiegeln. Wenn der Spieler keine Chips mehr hat, wird eine Warnung angezeigt, die darauf hinweist, dass er das Spiel verloren hat.

Die zweite Funktion, "klick_schwarz()", ist der ersten ähnlich, behandelt aber den Fall, dass der Benutzer auf den schwarzen Chip klickt. Sie dekrementiert die Anzahl der schwarzen Chips des Spielers ("anz_schwarz"), prüft, ob der Spieler noch schwarze Chips übrig hat, und deaktiviert die Schaltfläche für schwarze Chips, falls nicht. Anschließend wird die Anzahl der Chips des Spielers aktualisiert, der Gesamteinsatz auf der Grundlage der Anzahl der schwarzen Chips und ihres Wertes berechnet, die Gesamteinsatzbeträge des Spielers und des Computers aktualisiert und die entsprechenden HTML-Elemente aktualisiert. Wenn der Spieler keine Chips mehr hat, wird eine Warnung angezeigt, die besagt, dass er das Spiel verloren hat.

Dieser Abschnitt des Codes enthält die Implementierung der Spiellogik und die zugehörigen Variablen zur Verfolgung von Gewinnen und Verlusten.

wins_gesamt_spieler, wins_gesamt_cpu, lose_gesamt_spieler und lose_gesamt_cpu sind Variablen, die dazu dienen, die Anzahl der Gewinne und Verluste für jeden Spieler zu verfolgen.
Die Funktion start_function() ist die Hauptfunktion des Spiels, die aufgerufen wird, wenn der Spieler auf die Schaltfläche "Start" klickt. Sie prüft, ob der Spieler mindestens 10 € gesetzt hat, und gibt andernfalls eine Warnung zurück.
Vier Arrays werden definiert, um die verschiedenen Kartentypen im Spiel darzustellen: variant, werte, karten_farben und karten_werte. Diese Arrays werden verwendet, um zufällige Karten für den Spieler und die CPU zu erzeugen.
Mehrere Variablen werden definiert, um die Kartendecks des Spielers und der CPU darzustellen: deck_cpu, deck_cpu1, deck_spieler, deck_spieler1 und deck_spieler2.
Zufallszahlen werden generiert, um den Typ und den Wert der Karten für den Spieler und die CPU zu repräsentieren, indem die Funktion Math.random() und die Längen der Arrays variant und werte verwendet werden.

In diesem Teil des Codes werden die Karten für den CPU und den Spieler gezogen und in die entsprechenden Decks gespeichert. Dazu werden zunächst leere Arrays für die Decks erstellt. Anschließend werden Zufallszahlen erzeugt, um die Variante und den Wert jeder Karte aus den entsprechenden Arrays zu wählen. Mit diesen Werten wird dann für jede Karte ein Array erstellt und in das jeweilige Deck gespeichert. Insgesamt werden zwei Karten für den Spieler und zwei Karten für den CPU gezogen und in die Decks gespeichert.

Dieser Abschnitt des Codes ist für die Anzeige der Karten des Spielers und der CPU sowie für die Berechnung ihrer Punkte verantwortlich.

Der erste Teil verwendet die Methode document.querySelector(), um die Elemente mit der Klasse karte_spieler und karte_cpu auszuwählen, und setzt dann deren textContent auf eine Zeichenkette, die die Karten jedes Decks enthält, getrennt durch ein | Zeichen.

Im zweiten Teil werden vier Variablen definiert, um die Punkte jedes Decks zu speichern, die auf 0 initialisiert werden.

Schließlich gibt es eine Funktion namens werte_rechner(x, y), die zwei Parameter benötigt, x und y. Diese Funktion nimmt ein Kartenobjekt aus einem Deck, sucht seinen Wert und fügt ihn dem angegebenen y-Parameter hinzu. Der Wert der Karte wird durch ihr zweites Element (d.h. ihren Rang) bestimmt, das mit einer Reihe von if-Anweisungen verglichen wird. Wenn der Rang "Zwei" ist, wird der Wert 2 zu y addiert, und so weiter, bis alle möglichen Ränge ausgewertet worden sind. Der aktualisierte Wert von y wird von der Funktion zurückgegeben.

Das Codeschnipsel berechnet die Gesamtpunkte für die CPU und den Spieler auf der Grundlage der vom Stapel gezogenen Karten. Er berechnet zunächst die Punkte für die CPU, indem er die Funktion werte_rechner() mit den beiden Karten der CPU aufruft und sie addiert, um die Gesamtpunkte zu erhalten. Anschließend wird die Gesamtpunktzahl für die CPU auf der Webseite angezeigt.

Als nächstes wird eine Funktion namens klicke_hit() definiert, die ausgeführt wird, wenn der Spieler auf die Schaltfläche "Hit" klickt. Die Funktion erstellt eine neue Karte für den Spieler und schiebt sie in das Array deck_spieler2.

Nach der Definition der Funktion klicke_hit() prüft der Code, ob die Schaltfläche "Hit" mit dem Attribut onclick angeklickt wurde. Wurde die Schaltfläche angeklickt, ruft er die Funktion klicke_hit() auf, die dem Deck des Spielers eine neue Karte hinzufügt. Anschließend wird die Gesamtpunktzahl des Spielers berechnet, indem die Funktion werte_rechner() mit den drei Karten des Spielers aufgerufen und die Gesamtpunktzahl addiert wird. Die Gesamtpunktzahl des Spielers wird auf der Webseite angezeigt.

Wenn die Schaltfläche "Treffer" nicht angeklickt wurde, wird davon ausgegangen, dass der Spieler keine weitere Karte ziehen möchte. Daher wird die Gesamtpunktzahl des Spielers berechnet, indem die Funktion werte_rechner() mit den beiden Karten des Spielers aufgerufen und die Gesamtpunktzahl addiert wird. Anschließend wird die Gesamtpunktzahl für den Spieler auf der Webseite angezeigt.

Insgesamt implementiert das Codeschnipsel ein einfaches Kartenspiel, bei dem der Spieler und die CPU Karten von einem Stapel ziehen, und der Gewinner ist derjenige, der die höchste Gesamtpunktzahl erreicht, ohne 21 zu überschreiten.

Dieser Codeabschnitt ist verantwortlich für die Anzeige und Änderung der Gewinn- und Verlustzahlen sowie für die Benachrichtigung des Spielers über den Gewinner. Wenn der Spieler gewinnt, wird der Gewinnzähler erhöht, der Gesamteinsatz des Spielers wird zu seinen Chips hinzugefügt und der Einsatz wird auf Null zurückgesetzt. Wenn der Spieler verliert, wird der Verlustzähler erhöht und der Einsatz wird auf Null zurückgesetzt. Wenn ein Spieler fünf Siege erreicht, wird eine Benachrichtigung ausgegeben. Wenn der Computer gewinnt, wird eine Benachrichtigung ausgegeben, dass der Computer gewonnen hat. Wenn der Spieler gewinnt, wird eine Benachrichtigung ausgegeben, dass der Spieler gewonnen hat.
