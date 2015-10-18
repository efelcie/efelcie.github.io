---
layout:     post
categories: kanban lean agile








title:      Vorsicht mit Kanban in der IT!
summary:
            Kaban in der IT hat viel weniger mit dem klassischen Kanban gemeinsam als man vermuten würde. Wer das nicht beachtet, macht sich falsche Hoffnungen.


author:     Peter Flucher
date:       2015-10-18

---


## Die Geschichte von Kanban

  In meinem Kühlschrank gibt es Platz für vier Liter Milch. Wenn ich einkaufen gehe, kaufe ich exakt soviel Liter Milch wie fehlen nach. Jedoch ich kaufe niemals mehr. Was ich, und viele andere wahrscheinlich auch, hier machen, nennt sich im Management "Kanban".

  Kanban kommt aus dem japanischen und bedeutet Karte oder Beleg. Die Karte diente als eine Referenz auf das Ding. In meinem Fall gäbe es im System vier Karten. Jeder Liter Milch im Kühlschrank besetzt eine Karte. An den "freien" Karten sehe ich wie viel Liter Milch ich Kaufen soll.

  ![Kanban-Prozess mit Milch.](/images/kanbanshop.jpg)

  Wenn ich ins Geschäft gehe, wiederholt sich der Vorgang. Auch das Geschäft hat einen bestimmten Platz für Milch. Wenn ich hier Milch entnehme, wird der leere Platz wieder aufgefüllt. Letztlich steuere ich als Kunde, wie viel Milch produziert wird. Das nennt man **Pull-Prinzip**.

  > Es müsste doch möglich sein, den Materialfluss
  > in der Produktion nach dem Supermarkt-Prinzip zu
  > organisieren, das heißt, ein Verbraucher entnimmt
  > aus dem Regal eine Ware bestimmter Spezifikation
  > und Menge; die Lücke wird bemerkt und wieder 
  > aufgefüllt.
  >
  > -- Taiichi Ohno



## Das Toyota-Produktions-System

  In der Autoproduktion wurde das System von Taiichi Ohno 1947 bei Toyota entwickelt. Und noch heute wendet es Toyota, mittlerweile der größte Autokonzern der Welt, erfolgreich an.

  Wenn einem Toyota ein Teil in der Werkstatt ausgetauscht werden muss entnimmt die Werkstatt den Teil aus dem Lager. Automatisch bekommt das nächste lokale Toyota-Lager den Auftrag den Teil nachzuliefern. Von dort geht der Auftrag zum nächst größeren Lager bis es irgendwann einmal in einem Toyota-Werk landet. In dem Werk wird dann genau das benötigte Teil nach produziert.
  
  Der Aufstieg von Toyota war so Erfolgreich, dass er genau erforscht und oft kopiert wurde. Im Jahr 1990 erschien ein Buch mit dem Titel "The Machine that changed the World : The Story of Lean Production."[^Womack] Seit dem spricht man in diesem Zusammenhang auch von **Lean Management**.





## *Kanban* in der Software-Entwicklung

### Agile Methoden

  Ebenfalls in den 1990er-Jahren entwickelte sich in der Software-Industrie Methoden die sehr viele Parallelen zu *Lean Management* haben. Man nennt diese Art der Softwareentwicklung **agil**. Zwei Gemeinsamkeiten sind z.B. dass beide Ansätze sich sehr stark am Kunden orientieren und so wenig wie möglich "Müll" erzeugen wollen.

  Im Jahr 2007 stellte *David Anderson* *Kanban* für die IT vor. (Ich unterscheide zwischen Taiichi Ohnos Kanban [kanban] und David Andersons *Kanban* [kænbæn] in kursiv und amerikanischer Aussprache.) Anderson geht es nicht darum Kanban eins zu eins zu übersetzen, sondern er sucht nach Wegen Softwareproduktion zu verbessern. Dabei fällt ihm auf, dass einige Element aus Kanban gut funktionieren und die Elemente auf viel weniger Widerstand bei der Implementation stoßen als zum Beispiel *Scrum*.


### 6 Praktiken des *Kanban*

  Anderson beschrieb sechs Praktiken, die Unternehmen in ihre Arbeitsweise integrieren, wenn sie *Kanban* machen:

  1. Visualisiere den Fluss der Arbeit!

  2. Begrenze die Menge angefangener Arbeit!

  3. Miss und steuere den Fluss!

  4. Mache die Regeln für den Prozess explizit!

  5. Fördere Leadership auf allen Ebenen in der Organisation!

  6. Verwende Modelle, um Chancen für kollaborative Verbesserungen zu erkennen!


### *Kanban*-Board

  Populärstes Merkmal von *Kanban* ist das sogenannte *Kanban-Board*, eine Tafel mit Spalten und Post-its. Die Einfachste Version des Kanban-Board ist die dreispaltige Version mit den Spalten *To Do*, *Doing* und *Done*. Das Board stellt den Arbeitsfluss da. In der Software-Entwicklung beginnt es mit dem Product-Backlog, einer Sammlung von Problemen die gelöst werden müssen, und endet mit deren Implementierung. Dazwischen gibt es mehrere Stufen die das Item durchlaufen muss. Jede Stufe hat äquivalent zu den Karten in Kanban, eine bestimmte Anzahl an freien Plätzen für Aufgaben.

  ![Einfaches Kanbanboard.](/images/kanbanboard.jpg)



## Die Unterschiede zwischen *Kanban* und Kanban

  Ziel von *Kanban* ist es, wie in Kanban möglichst wenig Schmutz zu erzeugen und das System zu optimieren. Jedoch obwohl die Systeme ähnlich sind, ist die Funktionsweise anders. 


### Laubsauger

  Denken wir an eine Laubsauger. Ein Laubsauger erzeugt einen Unterdruck und bewegt so die Blätter. Bei den meisten Geräten ist es möglich den Ventilator in die andere Richtung laufen zu lassen. Aus dem Laubsauger wird ein Laubbläser. Hier wird ein Überdruck erzeugt mit dem die Blätter bewegt werden.


### *Kanban* ist kein Pull-System

  Auch wenn Anderson behauptet sein *Kanban*-System wäre ein Pull-System. Stimmt das? Ich behaupte nein. Was Anderson als Pull beschreibt, ist das Begrenzen der Buffer. Aber den Input vom Kunden finden wir auf der linken Seite, im (oft unbegrenzten) Product-Backlog. Der Backlog benötigt eine separate Feedback-Schleife um sich an den Kundenbedürfnissen zu orientieren.

  Man könnte meinen, im Prinzip ist es egal, wie das Druckgefälle in einem System entsteht. Wichtig ist, der Durchfluss. Und wie Anderson beweist, der Durchfluss ist wichtig.

  Ein vergleichbares System ist unter dem Namen ConWIP (Constant Work-In-Process) bekannt. Hier darf ein neuer Auftrag ins System, wenn ein alter das System verlässt.[^Conwip]
  Würde man *Kanban* als ConWIP System betrachten, würde es *nach* dem Backlog beginnen und *vor* der Done Spalte enden. Auf einem vereinfachten Kanbanboard wäre es nur die Spalte "Doing".



### Informationsfluss

  Doch der entscheidende Unterschied zwischen einem Pull und einem Push System ist der Fluss der Information. Kanban ist ein System in dem Information zurück fließen kann. In *Kanban* optimiert den Durchfluss, lässt den Kunden jedoch nicht selektieren welches Item er benötigt.


### Ring vs. Kette


  Da die Unterscheidung von Push und Pull auch in Experten-Kreisen zu Verwirrung sorgt führe ich hier eine neue Unterscheidung ein.[^Pushpull]
  In *Kanban* (wie auch in ConWIP) existiert eine große Feedback-Schleife. Es ist eine Art **Ring**. Die Feedback Schleife ist zu einem Teil *außerhalb* des abgebildeten Systems.

  ![Informationsfluss in Kanban.](/images/kanbankettering.jpg)

  In Kanban gibt es eine **Kette** von Feedback-Schleifen. Das Feedback läuft rückwärts durch das System. Das hat mehrere Vorteile:

1. Das Feedback läuft nur so viele Stationen wie notwendig.

2. Die Stationen, die näher am Kunden sind, bekommen "unverfälschteres" Feedback.

3. Der Kunde *zieht* sich genau das, was er benötigt. Es ist keine externe Steuerung notwendig.

4. Der Begriff *Lean*, also schlank, kann auf den gesamten Produktions-Prozess angewendet werden. Es ist weniger "Müll" im Backlog.




  
## Mit Vorsicht zu genießen!

  *Kanban* ist ein Weg, wie man mit vergleichsweise geringem Aufwand, die Effizienz in Projektteams steigern kann. 

  Jedoch suggeriert *Kanban*, durch seinen Namen, eine Nähe zu der Idee von Taiichi Ohno, die sich nicht ganz nachvollziehen lässt. Einige Elemente fehlen ganz, andere Elemente, die zur Wirkung von *Kanban* beitragen, wie ein *Kanbanboard* haben anderen Ursprung.

  Das alles ist so lange kein Problem, solange man nicht denkt, man würde mit *Kanban* den Geist von Ohno implementieren. Die Elemente die Eric Rise in *Lean Start-Up*[^Ries] an Toyota lobt, implementiert man durch *Kanban* **nicht** automatisch.

  

## Fußnoten

[^Pushpull]: Hopp, J. Wallace; Spearman, Mark L.: To Pull or Not to Pull: What is the Question? In Manufacturing & Service Operations Management: Volume 6 Issue 2, March 2004 <http://www2.isye.gatech.edu/~jvandeva/Classes/6203/2007/PushPull.pdf>. 

[^Conwip]: Conwip. Auf Wikipedia (de) <https://de.wikipedia.org/wiki/Conwip>

[^Womack]: Womack, James; Jones, Daniel; Roos, Daniel: The Machine that changed the World : The Story of Lean Production. New York: Harper Collins, 1990 – ISBN 978-0-06097-417-6. <http://www.amazon.de/Machine-That-Changed-World-Revolutionizing/dp/0743299795> (Amazon)

[^Ries]: Eric Ries: *The Lean Startup: How Constant Innovation Creates Radically Successful Businesses* 2011, <http://www.amazon.de/Lean-Startup-Innovation-Successful-Businesses/dp/0670921602/ref=sr_1_2?ie=UTF8&qid=1444573396&sr=8-2&keywords=lean+startup>. (Amzazon.de)