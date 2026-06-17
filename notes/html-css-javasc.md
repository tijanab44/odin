 Odin project

Web page - A document that can be displayed in a web browser. These are also often called just "pages". Such documents are written in the HTML language
Website - A collection of web pages grouped together into a single resource, with links connecting them together. Often called a "site".
Web server - A computer that hosts a website on the Internet.
Web service - A software that responds to requests over the Internet to perform a function or provide data. A web service is typically backed by a web server, and may provide web pages for users to interact with.

GitHub is a service that allows you to upload, host, and manage your code using Git with a nice web interface.
this commands will configure Git: 
git config --global user.name "Your Name"
git config --global user.email yourname@example.com

Change the default branch for Git using this command:
git config --global init.defaultBranch main

To verify that things are working properly, enter these commands and verify whether the output matches your name and email address.
git config --get user.name
git config --get user.email

Pravimo ssh kljuc koji sluzi kao sifra da ne bismo morali svaki put username i password da kucamo
ls ~/.ssh/id_ed25519.pub
If a message appears in the console containing the text “No such file or directory”, then you do not yet have an Ed25519 SSH key, and you will need to create one

To create a new SSH key:
ssh-keygen -t ed25519
...
Now you need to copy your public SSH key:
cat ~/.ssh/id_ed25519.pub




repoz pravis 



HTML

void elements: <br> <img>
You can think of elements as containers for content.
html tag - (opening and closing tags) - to su blokovi koji definisu(daju) strukturu kontentu neke stance

JavaSC sluzi da napravis sajt vise interaktivnim

HTML fajl koji sadrzi homepage uvijek treba da imenujemo index.html
Svaki html fajl mora da ima ovo


<!DOCTYPE html>

<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>My First Webpage</title>
  </head>

  <body>
  </body>
</html>

-ovo lang = "en" to ti je atribut za taj tag, i to znas

If we didn’t include a <title> element, the webpage’s title would default to its file name. In our case that would be index.html, which isn’t very meaningful for users; this would make it very difficult to find our webpage if the user has many browser tabs open.

Shortcuts: za fajl sa .html ekstenzijom, mozes da iskoristis shortcut ! + Enter i da dobijes boilerplate(sablon) ovaj <!DOCTYPE.. itd, cio ovaj prvi dio

suma sumarum: 
doctype nam sluzi za verziju html-a
boilerplate znaci sablon, mozes ga dobiti tako sto ces kliknuti **! + Enter** i voila imas sablon 

unutar body najcesce pravimo ove sekcije, i da se podsjetim
<p> za paragraf </p>, <strong> bold tekst </strong>, h1 ili h2 ili za italic em UNUTAR UGLASTIH ZAGRADA SVE.......................
<p>Lorem ipsum <em>dolor sit</em> amet, consectetur adipiscing elit.</p> ---> ovo je nesting elements (el unutar el)
parent /child

Ctrl + / - da zakomentiras nesto
ili ono poznato <!-- neki tekst.. -->

-LISTS: 
unordered - <ul> , <li>
ordered <ol> , <li>
-Linkovi:
potreban nam je anchor element
<a>Odin Project</a>
medjutim ako kliknemo na ovo nece se nista desiti, dok ovaj anchor ne povezemo sa nekim linkom preko 'href' - hypertext reference
<a href="https://www.theodinproject.com/about">About The Odin Project</a>
ovo ce nas vec dovesti do linka 
znaci 'href' za destinaciju linka, a da specificiramo izvor koristimo 'target' , ako nema po default-u je _self sto cini da se link otvori u current tabu. da bi ga otvorili u novom tabu, stavimo target="_blank"
rel je za relaciju izmedju tr stranice i linkovanog doc
-Absolute links- to su linkovi do drugih web stranica, kao sto smo imali gore za ovaj Odin project
-Relative links - kada void do druge stranice naseg web sajta, i posto su relativni, imace isti dome te dvije stranice..

-To go to the parent directory we need to use two dots in the relative filepath like this: ../      pr:
<img src="../images/dog.jpg">
-Besides the src attribute, every image element should also have an alt (alternative text) attribute. -koristi se da opise sliku

Ovo mi nista nije jasno ---->
- good commit messages (on GitHub)
to mozes da provjeris, istoriju commit-ova na gh
Having a good commit message history will allow you (or other developers working on your code) to quickly see what changes were made and why. This is useful if a bug is found in the code that needs to be fixed!
example of a bad commit message:
fix a bug
dobar commit:
Add missing link and alt text to the company's logo
Screen readers won't read the images to users with disabilities without this information.
-When writing code, it’s considered best practice to commit every time you have a meaningful change in the code. This will create a timeline of your progress and show that your finished code didn’t appear out of nowhere.
(Koliko sam shvatila, commit je ova poruka da znas sta si promijenila..?? i treba commit-ovati (cuvati) svaki put kada nesto znacajno uradis - promijenis u kodu)

JavaSC [case sensitive]
-to make the webpage interactive
-declaring variables with let and const
-The simplest way to get started is to create an HTML file with the JavaScript code inside of it. Use the VS Code snippet ! + TAB to create the basic HTML skeleton in a file on your computer somewhere. Be sure to include the <script> tag

let koristimo kada imamo varijablu koju bi posle mogli i da promijenimo recimo :
let age = 10;
age = 30;
a kada zelimo da varijabla ostane ista npr pi = 3.14 stavljamo const
const pi = 3.14;
[ -let, which we can re-assign.
  -const which we can’t re-assign ]

dakle, let, const i var(slicno kao let.. it is not used anymore)

varijable trebaju da se sastoje samo od slova, brojeva(samo da ne pocinje brojem) i karakteri $ i _

alert(2 + 2 + '1' ); // "41" and not "221"
alert('1' + 2 + 2); // "122" and not "14"
alert( 6 - '2' ); // 4, converts '2' to a number
alert( '6' / '2' ); // 3, converts both operands to numbers
let y = -2;
alert( +y ); // -2

increment -> ++ decrement--> --
What’s the difference between prefixing and postfixing increment/decrement operators?
-kada je prefix, onda se doda/oduzme 1 i to se ubraja u rezultat, a ako je post(sufix) onda je vrijesnost rezultata ostaje ona sto je bila pa nakon sto se upise ta vr, onda se poveca tek za 1
% ost pri dijeljenju 


Node.js (or just “Node”) is a JavaScript runtime environment that allows you to run JavaScript outside of your web browser.
that allows you to run JavaScript outside of your web browser.

A value in JavaScript is always of a certain type.
There are eight basic data types in JavaScript.
We can put any type in a variable.

NUMBER type
STRING type
let str = "Hello";
let str2 = 'Single quotes are ok too';
let phrase = `can embed another ${str}`;
BOOLEAN
NULL
UNDEFINED
The meaning of undefined is “value is not assigned”
If a variable is declared, but not assigned, then its value is undefined
OBJECT (do sad su bili 'primitivni' tipovi, jer njihova vrijednost moze da sadrzi samo jednu stvar-string, broj..)
Type of operator - 



