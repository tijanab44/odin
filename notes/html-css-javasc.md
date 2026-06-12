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
boilerplate znaci sablon, mozes ga dobiti tako sto ces kliknuti ! + Enter i voila tu je sablon

unutar body najcesce pravimo ove sekcije, i da se podsjetim
<p> za paragraf </p>, <strong> bold tekst </strong>, <h1> ili <h2> ili.. <em> italic </em> ,  
<p>Lorem ipsum <em>dolor sit</em> amet, consectetur adipiscing elit.</p> ---> ovo je nesting elements (el unutar el)
parent /child

Ctrl + / - da zakomentiras nesto
ili ono poznato <!-- ... -->

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

OVO MI NISTA NIJE JASNO ---->
- good commit messages (on GitHub)
to ti mogu gledati ako apliciras za posao recimo, istoriju commit-ova na gh
Having a good commit message history will allow you (or other developers working on your code) to quickly see what changes were made and why. This is useful if a bug is found in the code that needs to be fixed!
example of a bad commit message:
fix a bug
dobar commit:
Add missing link and alt text to the company's logo
Screen readers won't read the images to users with disabilities without this information.
-When writing code, it’s considered best practice to commit every time you have a meaningful change in the code. This will create a timeline of your progress and show that your finished code didn’t appear out of nowhere.
(Koliko sam shvatila, commit je ova poruka da znas sta si promijenila..?? i treba commit-ovati (cuvati) svaki pt kada nesto znacajno uradis - promijenis u kodu)


