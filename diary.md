
de
Programm mit Node laufen lassen:  node file.js

Absoluter Pfad
Beginnt mit / und fängt dann bei root an

HA zum 22.12
Welche Tests braucht Fence?
trivialCase()
normalCase
errorCase

fuzzyNumerArrayCompare? Nein, ist doch schon in numberArrayCompare, als tolerantArrayCompare




tolerantArrayCompare() ersetzt doch schon roundNumbers()?
roundNumber() und testRoundNumers() kann auch ausgekoppelt werden


roundNumbers ist notwendig, da sonst beim 3.Parameter für tolerantArrayCompare die Toleranz zu detailliert angegeben werden muss.
roundNumbers ist nicht notwendig, wenn man dem User den Hinweis gibt, dass die Toleranz mindestens 0.6 betragen  muss, also soviel wie die Rundung in roundNumber
>>nochmal über Rundung nachdenken, wie gross muss die Toleranz mind. Sein?

roundNumbers noch auskoppeln!!!

round-numbers erhält die Parameter in fence/test.js in normalCase

tmux split windows: prefix % und prefix =

die funktion mit try/catch hält die Hand raus

--save –dev  wird als development dep in packjson aufgenommen$PAT$4

for (var line = "#"; line.length <= 8; line += "#")
console.log(line);

common.js Zwischending von require

./ sucht im aktuellen Verz

ls –s   funktioniert wie kopieren in cmd

node_modules/.bin/browserify index.js – o browserified.js
file erstellen: .gitignore
node_modules zu .gitignore hinzufügen

>>>>NODE<<<<
Javascript ist als Sprache für den Browser entwickelt worden, Node ist eine Laufzeitumgebung für Javascript, die nicht im Browser ausgeführt wird, sondern z.B. auf dem Server
Mit Javascript und Node.js kann man also mit Javascript serverseitige Anwendungen bauen. Node.js ist eine serverseitige Laufzeitumgebung für Javascript.
NPM, Node Package Manager, is the largest Ecosystem of opensource libraries in the world.
Verschiedene Versionen von Node zum Download
LTS: LongTermSupport
NVM: Node Version Manager
is a simple bash script, meaning it runs on mac and linux, but not on windows
nvm install can install many different versions of node. When you want to use a special one, only do nvm use 7 and the system uses version 7.
nvm ls: hier sehe ich welche Versionen installiert sind
nvm use default: wendet die aktuellste Node version an, die auf meinem System installiert ist
node --version: zeigt an, welche version ich gerade benutze
node: so wird node gestartet, jetzt kann ich z.B. eingeben 1+6 und dann gibt node mir das Ergebnis, also 7, aus
das wird REPL genannt, Read Evaluation Print Loop,
Strg C press to exit 2 times!
cat app.js: so guckt man sich den Inhalt einer Datei in node an.

DATA TYPES
String, number, boolean

COMPARISONS

===

!===

IF / ELSE

var moonPhase = "mostly full";
if (moonPhase === "full"){
      console.log("Howwwwlll!!");
} else if (moonPhase === "mostly full"){
      console.log("Arms and legs are getting hairier");
} else if (moonPhase === "mostly new"){
      console.log("Back on two feet");
} else {
    console.log("Invalid moon phase");
}

To say "both must be true," we can use &&.
To say "either can be true," we can use ||.
To say "I want to make sure this is the opposite of what it really is," we can use !.
To say "these should not be equal to each other," we can use !==.

Deployment
eine Anwendung wird tatsächlich ausgeführt

Versionsnummern
Hinweise unter semver.org (Major, minor, patchi)
patch - erhöhen bei Fehlerkorrekturen
minor _ erhöhen bei API-kompatiblen Änderungen, d.h. die Version ist noch abwärts kompatibel
major - erhöhen bei API-inkompatiblen Änderungen

https://vimeo.com/150758542

^4.3.1 das ^^4.3.1 das ^4.3.1 das ^4.3.1 das ^bedeutet: verwende diese Version oder irgendeine Version, die höher ist als die angegebene, die aber noch kompatibel mit dieser ist.
Golo Boden rät aber dazu die Version zu fixieren. Falls man nämlich zeitlich etwas versetzt die depency mit flexibler Versionsnummer angibt, könnte es passieren, dass sich plötzlich die Versionsnummer eines Moduls geändert hat und die Anwendung also auf verschiedenen Rechnern mit in verschiedenen Versionen läuft. Dies dürfte zwar theoretisch kein Problem sein, ist es aber doch in der Praxi AAuch könnte es passieren, dass die Anwendung beim Entwickler mit einer anderen Versionsnumer läuft als beim Kunden.  
                
                }




Betahaus 12.1.17
A

Wir wollten uns per SSh verbinden.
Mit ifconfig und „my public ip“ haben wir die IP Adresse herausgefunden

➜  ~ ssh pair@10.167.196.120

es gab folgende Fehlermeldung

ssh: connect to host 10.167.196.120 port 22: Connection refused

mit dem cmd netstat –plunt  haben wir uns die verfügbaren Ports angeschaut
Port 22 schien nicht offen zu sein.

Wir denken, dass es an der Betahaus Firewall liegt und mindestens Port 22 nicht offen ist.

B

Wir haben auf meinem Rechner den Befehl 
node_modules/.bin/browserified. index.js –o browserified.js
eingegeben, der die letzten Tage nur Fehlermeldungen ergab, jetzt klappte es sofort, die Datei browserified.js entstand.

Wir  liessen dann, die Datei index.html im Browser laufen und erhielten folgende Fehlermeldung in der Konsole:

Uncought Reference Error: ctx is not defined

Wir dachten uns, dass es etwa mit dem require zu tun haben müsste, das die Variablendeklaration nicht ausreichend ist.

Auf einer Website gab es auch einen Trick. Man sollte var in der Variablendeklaration von ctx durch die method „window“ ersetzen. Also:

Statt: 
var ctx = canvas.getContext(„2d“);

das:
window.ctx = canvas.getContext(„2d“);

dies funktioniert im Browser, die Sinuskurve wird angezeigt

allerdings gibt es eine Fehlermeldung:
die Zeichencodierung des HTML Dokuments wurde nicht deklariert etc..

