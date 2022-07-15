# First Quest - Linux Ninja, Git Warrior, Docker Shaman

## Learning Path

### 1. Linux
VM cu o distributie de linux / [WSL](https://docs.microsoft.com/en-us/windows/wsl/about):
- (recomandare personala) Debian based - Ubuntu
- masina virtuala va fi de folos si mai tarziu dar e mai hungry decat WSL
- nu recomand git bash, ii lipsesc multe bash utilities
- **puncte bonus**: deschis un shell in VM fara GUI

[LinuxJourney](https://linuxjourney.com/):
- toate sectiunile din Grasshopper + Journeyman/The Filesystem
- restul sunt optionale, le faceti daca va permite timpul
- exercitiile si quizzurile sunt foarte utile, nu sariti peste ele
- `man` and `help` are your allies 

Foarte util:
- [archWiki](https://wiki.archlinux.org/)

### 2. Git
[freeCodeCamp git crash course](https://www.youtube.com/watch?v=RGOj5yH7evk)
- atentie la workflow
- (recomandare personala) comenzile de git din terminal, dar si extensia de VSCode e utila uneori

Foarte util: 
- [github get started guide](https://docs.github.com/en/get-started) - ! github flow !
- [visual git guide](http://marklodato.github.io/visual-git-guide/index-en.html)
- [interactive visual guide](http://onlywei.github.io/explain-git-with-d3)

### De retinut
- apreciem o documentare si o documentatie buna
- **puncte bonus**: documentatia in [markdown](https://www.markdownguide.org/)

## Exercitiul 0:

Creati un cont personal de GitHub (daca nu aveti deja) si dati fork la proiect. De acum veti lucra pe copia voastra a acestui repo.
- va faceti setupul de git pe VM 
- operatiile pe remote le veti face prin SSH 
- Flutter-WhatsAppClone e playground-ul vostru - daca incercati lucruri noi, pe langa cele din cursuri, va puteti face un branch nou dedicat taskului de learning

**DEADLINE 14.07 EOD**   
**Prezentare 15.07**

## Exercitiul 1:
Primul exercitiu se concentreaza pe concepte si tool-uri din linux si abordeaza partea de automatizare. Programele pe care le veti folosi ca sa il rezolvati fac parte din toolbox-ul unui DevOps Engineer. 
Exercitiile le parcurgeti gradual si le implementati in commituri (nu toata rezolvarea intr-un singur commit). Este foarte important sa respectati workflow-ul: commituri mici, mesage de commit detaliate, branchuri noi daca simtiti nevoia etc. Pentru exercitiul acesta se va lua in considerare si modul in care a fost folositi git.
 
### Partea 1: Users, groups and permissions
In VM, creati userul `alex` si userul `alina`, apoi grupurile `devops` si `engineer`:
- setati parole pentru ambii useri
- `devops` este account's primary group pentru userul `alex`
- `engineer` este suplementary group pentru userii `alex` si `alina`
- modificati ca ownerul acestui repo sa fie `alex`
- blocati userul `alina`

La final verificati daca aceste modificari s-au facut. Unde/cum puteti sa le vedeti? Faceti un cleanup complet si resetati permisiunile.

**Puncte bonus**: creati un sudo user care are **setata specific** permisiunea de a executa comenzile de `systemctl start/stop/restart` pentru OpenSSH daemon.

### Partea 2:  Working with files
In directorul `/part2` exista 100 fisiere, fiecare fisier contine 500 de stringuri cu caractere random. Printre aceste stringuri se afla 10 adrese de tipul `<nume>@gmail.com` (``<nume>`` contine doar caractere alfanumerice). 
- scrieti un shell script care sa gaseasca aceste adrese si sa le returneze intr-un fisier, impreuna cu numele fisierelor in care au fost gasite
- modificati scriptul si adaugati un parametru pentru a putea cauta si dupa alte mailuri (eg. `@yahoo.com`)

**Puncte bonus:**
- ordonati in fisier adresele de mail gasite
- inlocuiti adresele pe care le gasiti in `<nume>@yahoo.com` in fisiere

### **BONUS**: 
In directorul `/bonus1` exista doua fisiere:
- `text1` contine 500 de stringuri cu caractere random
- `text2` contine aceleasi stringuri ca cele din `text1` cu exceptia unui singur string modificat
Scrieti un shell script care sa gaseasca acest string modificat si sa returneze atat varianta sa din `text1` cat si cea din `text2`.

### De retinut:
- ne-ar placea sa vedem si un README pentru exercitiu in care sa intelegem mai bine cum ati gandit si rezolvat taskurile
- comentarii in cod 
