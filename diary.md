##removes newline characters in bash!!
cat code.js |  while read line; do echo -n "$line "; done


in placeNumberAtRandomFreePosition
Verständnisfrage: while means until condition is met?
###CODECADEMY


##WHILE LOOP
while(bool === true);
ist dasselbe wie:
while(bool);


SoloLoop = function(){
    while(weather) {
        console.log("Looped once!");
        weather = false; 
    }
};

soloLoop(); 
MAKE SURE to set your condition to false in the body of your loop. Otherwise, you'll loop forever!


## ARRAY
a=[], b={};
a.push(b);    
// a[0] === b;

how to add an object to an array:
var myObj = {key:"label", sortable:true, resizeable:true};
var newArray = [[2,3,true,5],[myObj]];

var dog = {
      species: "greyhound",
        weight: 60,
          age: 4
};

var species = dog["species"];
var weight = dog.weight;
var age = dog.age;

Object literal  and dot.notation(constructor notation)
The method we've used to create objects uses object literal notation—that is, creating a new object with {  } and defining properties within the brackets.
Another way of creating objects without using the curly brackets {  } is to use the keyword new. This is known as creating an object using a constructor.
The new keyword creates an empty object when followed by Object(). The general syntax is:
var objectName = new Object();
We then have to fill this object with properties and labels. 

###METHODS
We can think of properties as variables associated with an object. Similarly, a method is just like a function associated with an object.

var bob = new Object();
bob.name = "Bob Smith";
bob.age = 30;
// this time we have added a method, setAge
bob.setAge = function (newAge){
      bob.age = newAge;
};
// here we set bob's age to 40
bob.setAge(40);
// bob's feeling old.  Use our method to set bob's age to 20
bob.setAge(20);

##using this.

setAge = function (newAge) {
      this.age = newAge;
};
// now we make bob
var bob = new Object();
bob.age = 30;
bob.setAge = setAge;
  
  var susan = new Object();
  susan.age = 25;
  susan.setAge = setAge;

  susan.setAge(35);

}}
Pipe symbol in JS::w
vim
de  delete till end of word
d$  delete till end of sentence

eg 5 | 0
that's an nice way to convert floating-point number to int, or use parseInt()

Hausaufgabe 9.2.
clear the array and set first two 2 between null
>> schreibt man i<=width, dann werden die Arrays untereinander, ein Array pro Zeile, angezeigt,
schreibt man i<width, dann stehen alle Arrays in einer Zeile ???

wie übergebe ich den Wert von placeNumberRandomly() an field?

### SSH

ssh pair@terrorbird.local
tmux -S /tmp/pair new
chmod 777 /tmp/pair

svg ist eine xml Datei

Nur eine Zeile in Vim kopieren: strg V

aus VIM kopieren markieren, dann :w xsel --clipboard und paste an die Stelle
git rebase --interactive HEAD~3

D###Copy directory:###Copy directory:IARY 7.2.2017
trying to use sed to replace Zeichenfläche 345-neu.svg by 345.svg
command: for file in *.svg ; do mv $file ${file//Zeichen/XYZ} ; done
changes Zeichenfläche 347-neu.svg to XYZfläche 347-neu.svg
###Copy directory:
made a new Zip-folder just for testing, changed  Zeichenfläche 347.png to Zeichenfläche 347-neu.png
next try:
ls *.png | sed 's/[^0-9]*\([0-9]*\.png\)/cat "&" | \..\/node_modules\/.bin\/pretty-xml > ..\/images\/\1/' 
>above worked as far as it sorted out all .png files instead of .svg
next try -g, option for global, so the command should not only work on first part but on whole line of command, I tried:
ls *.png | sed 's/[^0-9]*\([0-9]*\.png\)/cat "&" | \..\/node_modules\/.bin\/pretty-xml > ..\/images\/\1/g' | sh
it worked just as the line without g .. and didnt give an errormessage

>>remove everything from the line till the last forward slash:
echo Zeichenfläche/457-/neu/.png | sed 's/^.*\///'
result: .png

echo Zeichenfläche457 | sed 's/[^0-9]*\([0-9]*\).*/\1/'
result: 457

echo Zeichenfläche457.png | sed 's/[^0-9]*\([0-9]*\.png\).*/\1/'
result: 457.png

echo Zeichenfläche457-neu.png | sed 's/[^0-9]*\([0-9]*\.png\).*/\1/g' //hier ist nur eine Capturegroup ([0-9]*\.png\) referenced, und das bei der \1/, das bedeutet wahrscheinlich, das auch nur eine Stelle ersetzt wird, man muss also noch sowas wie \1/\2/ hinzufügen..probieren wir mal :)
result: Zeichenfläche457.png

Triumpf!!
echo Zeichenfläche457-neu.png | sed 's/[^0-9]*\([0-9]*\).*\(\.png\)/\1\2/'
result: 457.png

try to enter a second part to line [^0-9]*\([0-9]*\.png\)/

TMUX.conf

unbind C-b
set -g prefix C-a
bind C-a send-prefix






copy only content:
cp -R <sourcedir>/ <destdir>
copy whole directory:
cp -R <sourcedir> <destdir>

###Backslash: alt + shift + 7

###sed
-e:  multiple commands may be specified using the -e options
>> In a context address, any character other than a backslash (``\') or newline character may be used to delimit the regular expression.
Also, putting a backslash character before the delimiting character causes the character to be treated literally.  For example, in the
context address \xabc\xdefx, the RE delimiter is an ``x'' and the second ``x'' stands for itself, so that the regular expression is
``abcxdef''.
important:
>>you can easily search for all characters except those in square brackets by putting a "^" as the first character after the "[". To match all characters except vowels use "[^aeiou]". 
                              

execute files:
.js : node
.sh : bash


diff file1 file2
ps -a|grep vim
kill filename

make a file executable..
chmod +x process-images.sh

execute file
and the program has to be executed with `./scriptname.sh nameOfZipFile`.
 

which bash
<html>
  
    <head>
var canvas;
var ctx;

function drawGameCanvas() {

// Get the canvas element.
canvas = document.getElementById("gameBoard");

// Make sure you got it.
if (canvas.getContext) {
    // Specify 2d canvas type.
    ctx = canvas.getContext("2d");

    // Play the game until the ball stops.
    gameLoop = setInterval(drawBall, 16);

    // Add keyboard listener.
    window.addEventListener('keydown', whatKey, true);
}
}
>>>TMUX
split screen horizontally: ctrl b shift + quotationmark
toggel between windows: ctrl b + o
close current pane: ctrl b + x

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

this vim command pipes the buffer of a file through a command, in this case a prettyfier..and gives the result iinto the same file:

:%!node_modules/.bin/pretty-xml

bash script 
(pipes buffer of file through command and writes it into the bash):
cat new_images/1.svg | node_modules/.bin/pretty-xml

pipe all files of new_images through pretty-xml command and show in bash
cat new_images/* | node_modules/.bin/pretty-xml

copy the content of one directory into the current directory (without hidden files though):
cp ../images/* .

pipe all files of a directory through a command and write the result into a new file all.svg
cat ./* | ../node_modules/.bin/pretty-xml > ../pretty_images/all.svg

pipe a file of a directory through a command and write the result into a new file x.svg
cat ./9.svg | ../node_modules/.bin/pretty-xml > ../pretty_images/9.svg

:e filename      - edit another file
:split filename  - split window and load another file
ctrl-w up arrow  - move cursor up a window
ctrl-w ctrl-w    - move cursor to another window (cycle)
ctrl-w_          - maximize current window
ctrl-w=          - make all equal size
10 ctrl-w+       - increase window size by 10 lines
:vsplit file     - vertical split
:sview file      - same as split, but readonly
:hide            - close current window
:only            - keep only this window open
:ls              - show current buffers
:b 2             - open buffer #2 in this window

