//NOCH NCIHT FINAL, MUSS NOCH FLÜSSIG LESBAR GESCHRIEBEN WERDEN



# Technical Review Memo of Team eiBoard
## Date 
16.15-
## Participants 
Developers Frontend: Eileen, Niklas
Developers Backend: Matteo, Julian
Projectmanagement: Marius

(roles, e.g., who make notes, who moderates/time keeper)
## Goal/Focus
**Eileen**

Main screen wo man landet wenn man sich einloggt.
menü -> unsicher ob so passt fpr alle

sieht evtl buggy aus. Menü schliesen über "drei punkte" burger menu
zurückpfeil manchaml buggy
navigation bei create task macht noch umwege

menü muss noch über schieben geschlossen werden (muss über punkte gehen)
nuees passwort erstellen: dippelt eingeben um zu testen dass es passt (Sicherheitstest)



**Niklas**

adaptive liste ide später vom bakcend gefüllt wird und infos auf seite gibt tasklist object

todo_list_screeen.dart

liste wird nach zeiten gefiltert. Backend braucht funktion zum feststellen was aktuelles datum ist, welche aufgben überfällig sind, welche bis heute und bis in deiser woche erledigt weden müssern.
task_list_object.dart
backend_rapla.dart

listenobjekte aus backend holen

liste füüllen über frontend

zukunft:
listenelemente alles was bearbeitet wird wird über liste zum backend transportiert.

Styleattributes taken care of
data taken care of (list attributes-> cannot put a number instead string)




**Julian**
1. Thema: Unit Tests Backend
  Hauptsächlich Unit Tests für services da dort datenfluss und methoden definiert.
  Um aktionen auf db durchzuführen.
  
  Entry Service: 4 methoden: save delete, findbyID und getallentries
  arbeit mit gemockten repositorys da viel einfcher.
  
  Bei safe: es gibt neuen eintrag -> gemocktes repository überprüft entry return und ob beide entries die gleichen sind.
  bei delete: entryID wird gelöscht und bestätigen lassen, dass 
  find byid 
 chekcen ob gefundener eintrag dem eintrrag entspricht der ersellt wurde
 
 falls nicht gibt: exception throw
liste -> neuer eintrag- bei find all: -> gibt liste zutrück
allentries list wird überprüft ob die liste gleich der entry list ist.
Erster eintrag der jeweiligen lsite wird überprüft ob es das selbe ist um zu vermeden, dass liste gleich lang aber nicht identisch


getDay ist hashmap. liste und datum in hashmap sollen übergeben werden. anschließend wird geprüft ob die services die geholt werden mit den appointments übereinstimmen.

dasselbe auch für die ganze Woche. auch überprüfung ob appointments übereinstimmen.

//personenliste wird um eins erhöht. Wird geprüft und eine weitere person hinugefügt und gechaut ob es sich um eins erhöht.
zwei personen ausserhalb methode, innerhalb von testmethode wird eine angelegt und geschaut ob sich liste um eins erhöht

getAllUsers wird dann auf die Anzahl der einträge geprüft

deleteById überprüft, dass Liste 6personen groß ist, löscht sich eine und wird geprüft ob liste -1.
Und ob bei aufruf der id der gelöscthten person exception geworfen wird.

paar tests noch für setter und getter.

GUTE punkte abgedeckt mit unit test / vulnerable punkte




2. Jenkins pipelines
wenn maven bentutzt wird, muss das maven plugin installiert sein.
maven integration und pipelin maven plugin
desweiteren muss man bei konfig hilfsprogramme muss man noch die ganzen dependencys/installationswege angeben.
Häufig direkt von seite installieren und wählt version aus und setzt kürzel wie man drauf zugreift.

desweiteren muss man maven im jenkins image installieren über **docker exec -u** dann kann man user festlegen mit dem man in docker geht (0 ist admin) 
- it um nachher wieder rasuzukommen, dann id , dann bash und dann kommt man in den docker container. über apt - get install maven -> maven wird im container installiert.

jenkins pipeline aufgesetzt mit maven

zukunft: wenn tests erfolgreich soll neunes docker image gebildet, und in registry gepusht werden. alter container vom backend löschn und neuen container hochfahren.



**Matteo** 
Controller und Swagger
DateController.java

controller: dafür da als restschnittstelle. Stellen unsere daten dar.
wenn man lecture an einem tag eingibt. Dann bekommt man die Vorlesungen von dem Tag zurück.
Mit dozenten (Raum) und weiteren Infos. (Auch als filter verwendbar)
response code. 200 OK returns lectures of the given day, 406 wrong date format usw.
bis jetz kommt nur 200 Ok zurück


über ceykloak support abgesichert. bis jetzt kann noch jeder auf die endpunkte zugreifen.


weiteren controller wenn man ganze woche will. man gibt tag der woche an und bekommt die woche dafür zurück.

Noch ein paar fehler. Tage werden nicht als einzelen objekte zurückgeliefert sondern hängen noch zusammen (muss geändert werden)


für frontend: über swagger sieht man wie das zurückgegebene daenobjekt aussieht. z.b. lectureList


entry controller: wird gelöscht werden

user controller: endpunkte: liste von allen usern holen, user löschen / einfügen, user nach id anzeigen lassen usw


Person.java
mit flutter aus blobb bild erwtellen/bild wird als blobb gespeochert

zukunft: event und task controller sowie modellklassen




//of the review meeting (including why do you choose this part for review)
## Components for Review
**Eileen**
page.dart
main page
menu


**Niklas**



**Julian**
unit tests. backend, jenkins, docker.
jenkinsfile
unit test files: 




**Matteo** 


## Criteria of review 
**Eileen**


**Niklas**



**Julian**




**Matteo** 



(per component, if each component has different criteria), e.g., code quality, performance, security, scalability, maintainability, or any other relevant factors.
## Review methodology

**Eileen**
Showing live demo.
Running through code

**Niklas**
Showing live demo.
Running through code

**Julian**
Showing live demo.
Running through code
describing how to go into docker.

**Matteo** 
Showing live demo.
Running through code



e.g. formal inspections, walkthroughs, code reviews, etc.
## Outcome from the meeting
e.g., action items (with responsible person and deadline), best practices, lessons learned.

person service test noch mcoken
alle unit tests mocken

code ist clean/übersichtlich, gute variablennamen
z.T. noch kommentare und markierkommentare löschen
frontend datenbearbeitung werden ausgegraut wenn fertig bearbeitet aber trotzdem angezeigt


nächste schritte wurden besprochen, die teams haben sich ausgetauscht was sie noch/als nächstes machen werden.
Stylingoptionen besprochen.
einzelne stylebugs besprochen



zurückpfeile und burger menü sieht teils noch animiert aus. Sehr ähnlich zu smartphone app. in webapp eher noch alleinstellungsmerkmal


frontend kann noch nicht auf backend zugreifen
cors policy. vom frontend auf backend noch einrichten

jeder eintrag braucht noch eine ID (User, Todo-Karte usw)


was noch genmacht werden musss: alles an mysql anbinden um daten abzusichern
keycloak anbinden
frontend muss dann mit dem user bei keycloak authentifizieren. evtl. controller zum passwort ändern.


für projektmanagement fehlt noch metrikzeugs (vor zwei vorlesungen)