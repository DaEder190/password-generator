Verwendung von GitHub für PRE/SYP
Was bietet GitHub und wie muss mit GitHub für Projekt verwendet werden.

Vorweg, diese Dokument wurde mit Markdown erstellt. Alle Dokumente, Kommentare etc. werden auf GitHub damit geschrieben werden (Text mit einfachen Markup, sehr intuitiv und leicht zu verwenden).

Jeder kann seine geliebte IDE für das jeweilige Projekt verwenden. Für dieses Tutorial wird von mir Visual Studio Code verwendet.

Git und GitHub
GitHub verwendet unter der Haube Git. GitHub kann als Codemanagmentplatform betrachtet werden und stellt rund um Git noch viele weitere Features für eine produktive Projektentwicklung zu Verfügung.

Branches
Git nutzt das Konzept Branching um es zu ermöglichen, verschiedene Änderungen am Sourcecode wieder zusammenzuführen. Dabei können Mergekonflikte auftreten welche uns dabei unterstützen.

Beispiel
Unser GitHub Repo bietet uns ein Menü (rotes Rechteck, oben) welches unter Code (rotes Rechteck, unten) den Inhalt des Repos anzeigt. Man kann dadurch per Browser durch die Dateien des Repos navigieren.

alt text

Einen neuen Branch "dev" Remote anlegen
Per Klick auf Branch kommt man auf die Branch-Übersicht.

<img src="images/image-333.png" alt="alt text" width="300"/>
Wir legen einen neuen Branch dev an, der den Entwicklungsstand des Projektes repräsentiert. Dieser muss main als Source gesetzt haben. alt text

Per Fetch oder Sync kann der Remote neu erstellte Branch lokal gesichtet werden.

<img src="images/image.png" alt="alt text" width="250"/>
Branch wechseln
Damit kann dieser jetzt im VSCode ausgewählt werden. alt text

Dieser wird im VSCode unten Links angezeigt. alt text

Mit der zu empfehlenden Git-Graph-Extension sieht man alle lokalen Branches und auch welchen man ausgewählt hat. alt text

Issue anlegen
Alle Product-Backlog Items im Sinne von Scrum werden auf GitHub als Issues angelegt. Wir legen Testweise gemeinsam ein Issue an dafür legen wir anschließend einen neuen Branch an und können diesen wie oben geleert lokal auschecken.

alt text

Wir legen ein neues Issue an. Jedes Issue muss einen Titel besitzen, dieser sollte einen möglichst hohen Wiedererkennungswert besitzen. Die Beschreibung kann sehr umfangreich sein und sollte Klarheit über die anstehende Änderung bringen. Zusätzlich sollte jedes Issue am Ende auch jemanden zugeordnet sein.

alt text

Da uns GitHub mit Issues Gestaltunsspielraum für die Organisation der Typen oder Arten von Issues bietet haben wir folgende Regel für PRE/SYP definiert.

Es gibt für uns nur folgende Typen von Issues:

User-Stories [Story]
Tasks [Task]
Bugs [Bug]
Jedes Issue muss an erster Stelle den Typ im Titel des Issues stehen haben. Damit Sorgen wir für Übersichtlichkeit und leichteres auffinden von Issues.

alt text

Branch für Issue anlegen
alt text

Für die Erstellung des Branches und deren Namen ist wichtig zu wissen, das jedes Issue von GitHub automatisch einen sogenannten Primary-Key bekommt (hier eins, #1) damit passiert die Zuordnung zwischen Branch und Ticket.

Man weiß also immer welche Codeänderung auf Basis welcher Anforderung passiert ist und umgekehrt.

Aufpassen es muss der Source-Branch auf dev geändert werden. Es müssen immer alle Feature Branches von dev weggehen.

<img src="images/image-17.png" alt="alt text" width="250px" />
Für den Namen der Branches benötigen wir ebenfalls eine Namenskonvention die wie folgt definiert wurde:

task/1-{abgekürzte-aufgabe}
bug/1-{abgekürzte-aufgabe}
Eine User-Story sollte immer auf Tasks aufgeteilt werden somit wird es dafür keinen Branch geben. Kleine User-Stories besitzen vielleicht nur einen Task.

Wir sehen, dass dadurch der erstellte Branch mit dem erstellten Task (Issue) verknüpft wurde.

alt text

Jetzt kann lokal auf diesen Feature-Branch gewechselt werden. Änderungen können vorgenommen werden und diese auch anschließend Committed und Remote Ge-Pushed.

Nochmals Schritt für Schritt:

Git-Fetch alt text

Branch wechseln alt text

Branch Checkout alt text

Jetzt können wir Änderungen auf diesen Branch lokal vornehmen.

alt text

Änderungen Committen
Hier sollte man zu Beginn der Comitt Nachricht mit #{Nummer} die Nummer des Tickets referenzieren. Wenn man die Committs auf dev oder main sich mal anschaut erleichtet es einem die Suche. alt text

Per Sync Remote stellen.
alt text

Jetzt sollten die Änderungen auf GitHub auf diesen Branch ersichtlich sein.

Es kann auf GitHub über den Code-Explorer nachgeschaut werden. alt text

Branching-Strategies
Zusammenfassend haben wir jetzt kennengelernt, dass wir nicht direkt am main Branch arbeiten dürfen und uns einen dev Branch anlegen. Der main ist also nur für den Kunden. Was auf main steht ist beim Kunden.

Der dev Branch dient für die Entwicklung und für das Team. Damit sich das Team nicht gegenseitig bei der Integration immer alles zerschießt, sollte man Branches verwenden.

Wir verwenden für PRE/SYP die sogenannte Gitflow Workflow Branching-Strategy. Hier nochmal eine Übersicht:

alt text

Links
GitHub Dokumentation
Git-Buch
