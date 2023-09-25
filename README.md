# Explicaci� de git

[Git Tutorial](https://www.w3schools.com/git/default.asp?remote=github)


<details>
<summary>Index</summary>

1. [Instal�lar **```git```** a **```Windows```**](./README.md#installar-git-a-windows-1)

1. [Comanda **```git status```** per veure l'estat del repositori](./README.md#comanda-git-status-per-veure-lestat-del-repositori-1)

1. [Inicialitzar un repositori](./README.md#inicialitzar-un-repositori-1)

1. [Afegir fitxers, i comanda **```commit```**.](./README.md#afegir-fitxers-i-comanda-commit-1)

1. [Setting your commit email address](./README.md#setting-your-commit-email-address-1)

1. [Setting your username in Git](./README.md#setting-your-commit-email-address-1)

1. [Creaci� d'un usuari a github.com](./README.md#creacic3b3-dun-usuari-a-githubcom-1)

1. [Creaci� d'un repositori a la vostre compta a github.com](./README.md#creaci�-dun-repositori-a-la-vostre-compta-a-githubcom-1)

1. [Com convidar a un col�laborador a un repositori a la vostre compta a github.com](./README.md#com-convidar-a-un-collaborador-a-un-repositori-a-la-vostre-compta-a-githubcom-1)

1. [Inviting collaborators to a personal repository](./README.md#inviting-collaborators-to-a-personal-repository)
</details>

## Instal�lar git a Windows

* Descarregar el programa ```git``` des de la web [Git-2.39.1-64-bit.exe](https://github.com/git-for-windows/git/releases/download/v2.39.1.windows.1/Git-2.39.1-64-bit.exe)

* P?gina web oficial de [GitHub](https://github.com)

**1.** Crear la carpeta contenidora del nostre projecte.


Per tal de unificar la nostra explicaci�, crearem una carpeta que anomenarem **```<CognomAlmune>-primer-repositori```**, (on <CognomAlmune> �s el nom de l'alumne, sense el cognom, per exemple amb el meu cas seria **```pardo-primer-repositori```**) i ser? la que farem servir per guardar i centralitzar el projecte o repositori **```<CognomAlmune>-primer-repositori```**. En el meu cas, la crear? dins de la unitat D: del meu portatil.

Per fer-ho executarem les seg�ents comandes.
```sh
~$ mkdir <CognomAlmune>-primer-repositori
~$ mkdir <CognomAlmune>-primer-repositori
~$ cd <CognomAlmune>-primer-repositori
~/<CognomAlmune>-primer-repositori $ pwd
\d\<CognomAlmune>-primer-repositori
```

# Comanda **```git status```** per veure l'estat del repositori

Existeix una comanda que ens mostra en quin estat es troba el nostre repositori.

Un cop ja siguem dins de la carpeta que acabem de crear podem provar d'executar la comanda **``git status``** que ens mostrar? quin �s l'estat del repositori.

```sh
~/<CognomAlmune>-primer-repositori $ git status
fatal: not a git repository (or any of the parent directories): .git
~/<CognomAlmune>-primer-repositori $
```

Obtenim un error, que ens diu que no �s un repositori. Aix? �s normal, ja que per defecte, cap carpeta �s un repositori.

# Inicialitzar un repositori

Per fer que la nostra carpeta sigui un repositori, �s a dir, per dir-li a **```git```** que volem que porti el control dels canvis al fitxers, cal que executem la comanda **```git init```**.

```sh
~/<CognomAlmune>-primer-repositori $ git init
Initialised empty Git repository in /d/<CognomAlmune>-primer-repositori/.git/
~/<CognomAlmune>-primer-repositori $ 
```

Ens mostra el missatge (**```Initialised empty Git repository in /d/<CognomAlmune>-primer-repositori/.git/```**), �s a dir, que s'ha inicialitzat com a repositori buit la ruta (**``/d/<CognomAlmune>-primer-repositori/.git/``**).`

Tanmateix, si mirem el contingut de la carpeta **```<CognomAlmune>-primer-repositori```** amb un **```ls -l```** o amb un **```dir```**, veiem que, aparentment no hi ha res creat.

```sh
~/<CognomAlmune>-primer-repositori $ ls -l
total 0
~/<CognomAlmune>-primer-repositori $
```

Per? si executem la comanda perqu? mostri els fitxers ocults **```ls -la```** o **```dir /a```**, llavors s� que veiem que hi ha una carpeta nova anomenada **```.git```**, el que passa �s que �s oculta.

```sh
~/<CognomAlmune>-primer-repositori $ ls -a
total 12
drwxrwxr-x 3 user user 4096 Sep 24 13:00 .
drwxrwxrwx 7 user user 4096 Sep 24 13:00 ..
drwxrwxr-x 7 user user 4096 Sep 24 13:00 .git
~/<CognomAlmune>-primer-repositori $ 
```

Aquesta carpeta **```.git```** �s la que cont� tota la informaci� de **```git```** sobre el projecte. Cada vegada que es facin canvis, ja sigui afegint fitxers, modificant el contingut dels fitxers, creant o esborrant subcarpetes ,etc aquests canvis s'aniran guardant en aquesta carpeta. Per tant, **�s important** que no l'esborreu, ni li feu res, ja que �s **imprescindible** per poder interactuar amb **```git```**.

Si accedim a aquesta carpeta **```.git```** amb un **```cd .git```**, i llistem el contingut amb **```ls -l```** o amb **```dir```** podrem veure tot el contingut que necessita **```git```** per funcionar.

```sh
~/<CognomAlmune>-primer-repositori $ cd .git
~/<CognomAlmune>-primer-repositori/.git$ ls -l
total 32
drwxrwxr-x 2 user user 4096 Sep 24 13:00 branches
-rw-rw-r-? 1 user user   92 Sep 24 13:00 config
-rw-rw-r-? 1 user user   73 Sep 24 13:00 description
-rw-rw-r-? 1 user user   23 Sep 24 13:00 HEAD
drwxrwxr-x 2 user user 4096 Sep 24 13:00 hooks
drwxrwxr-x 2 user user 4096 Sep 24 13:00 info
drwxrwxr-x 4 user user 4096 Sep 24 13:00 objects
drwxrwxr-x 4 user user 4096 Sep 24 13:00 refs
~/<CognomAlmune>-primer-repositori/.git$ 
```

Per?, si ara tornem enrere, amb **```cd ..```**, �s a dir, a la carpeta **```pardo-act01```** i executem la comanda **```git -status```**, la resposta rebuda �s una altra.

```sh
~/<CognomAlmune>-primer-repositori/.git$ cd ..
~/<CognomAlmune>-primer-repositori $ git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)

~/<CognomAlmune>-primer-repositori $
```

Ens mostra els seg�ents missatges que volen dir:

* **```On branch main```**, que ens trobem a la branca (**```branch```**) principal (**```main```**)
* **```No commits yet```**, que encara no hi ha res per confirmar (**```commit```**) i per �ltim,
* **```(create/copy files and use "git add" to track)```**, que si volem afegir fitxers perqu? comenci a gestionar la tra�abilitat d'aquests, cal que fem servir la comanda **```git add```** per afegir els fitxers a la llista dels fitxers que volem afegir al repositori.

Per tant, fins ara no hem fet res m�s que indicar quina �s la carpeta del nostre repositori. Per? ja estem preparats per crear i/o modificar fitxers i dur el control dels canvis que fem sobre aquests.


# Afegir fitxers, i comanda **```commit```**.

Per comen�ar crearem tres fitxers.

**```index.html```**, **```main.js```** i **```styles.css```**.

El primer l'anomenem **```index.html```** ([pardo-primer-repositori (codepen.io)](https://codepen.io/joanpardo/pen/QWBzLwp)), i afegim el text b?sic per crear una p?gina web.

```html
<html lang="ca">
  <head>
    <meta charset="utf-8">
    <title>Activitat primer repositori</title>
  </head>
  <body>
  
  </body>
</html>
```
Un cop que hem creat, modificat i guardat aquest primer fitxer, anem a veure qu? �s el que ens diu **```git```**.

```sh
~/<CognomAlmune>-primer-repositori $ vi index.html
```


```sh
~/<CognomAlmune>-primer-repositori $ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html

nothing added to commit but untracked files present (use "git add" to track)
~/<CognomAlmune>-primer-repositori $ 
```

Ara apareix una secci� **```Untracked files```**, �s a dir, una apartat a on ens mostra aquells fitxers, que no estan **marcats** per controlar els seus els canvis, �s a dir que **NO tenen de tra�a**. �s a dir, que el fitxer **```index.html```**, no est? marcat per controlar els canvis que es facin sobre ell.

A part, apareix la seg�ent explicaci�:
```sh
use "git add ..." to include in what will be committed

```


La comanda **```git add ...```** afegeix un fitxer al repositori local i el prepara per a la confirmaci�. Per eliminar o treure un fitxer, cal fer servir **```git reset HEAD <<nomFitxer>>```**.

�s a dir, que cal fer servir "**```git add ...```**" per incloure els fitxers que volem que **```git```** comenci a controlar.

I per �ltim ens indica:

```sh
nothing added to commit but untracked files present (use "git add" to track)
```

Que tot i que hi ha **fitxers sense tra�a** (**```untracked files```**), no hi ha res afegit per **confirmar**, �s a dir per incloure en el seg�ent control. I ens indica que cal fer per afegir fitxers al control, "**```(use "git add" to track)```**, �s a dir feu servir **```git add```** per afegir fitxers a tra�ar.

Fixeu-vos que aquests fitxers sense tra�a, apareixen de color vermell, i en el nostre cas apareix el fitxer **```index.html```** que acabem d'afegir, per? com que no l'hem afegit al control de tra�a, **``git``** encara no el `t� a la llista de fitxers a controlar. Ara mateix, per molt que nosaltres el modifiquem, **``git``** mai el detectar?, ni controlar? els canvis`que pateixi.

## Afegir fitxers

Perqu? **```git```** tingui present el fitxer **```index.html```**, cal afegir-lo, i per aix� existeix la comanda **```git add <pathspec>```**.

```sh
~/<CognomAlmune>-primer-repositori $ git add index.html
```

```sh
~/<CognomAlmune>-primer-repositori $ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm ??cached ..." to unstage)
        new file:   index.html

~/<CognomAlmune>-primer-repositori $ 
```

Un cop afegit el fitxer **```index.html```**, si tornem a executar la comanda **```git status```**, ara apareix un nou missatge "**```Changes to be committed```**" �s a dir, canvis per ser controlats. I el fitxer **```index.html```** ja apareix com a fitxer nou i de color verd.

Ara �s el moment de fer un **```commit```**. Un **```commit```** o **confirmaci�** �s un **punt de control** en el nostre projecte. Acabarem tenint molts **```commit```**'s, cada vegada que fem alguna cosa important o prou rellevant. Com un petit **punt de control** al qual sempre podrem tornar. Per tant, �s recomanable realitzar aquests **```commit```**'s, per exemple cada vegada es crea un nou fitxer, o afegim una �nica funci� de **```javascript```**, o hem modificat alguns estils, etc. �s a dir, cal fer un **```commit```** cada vegada que es vulgui crear un **punt de control**, que volem recordar, o al que volem poder tornar m�s endavant.
Per fer-ho, cal fer servir, la comanda git **```commit```** amb el par?metre **```-m```**, per afegir-li un **missatge**, comentari o nom que l'identifiqui. I tot i que �s possible no afegir cap missatge, �s molt recomanable, afegir-ne un que sigui �til i descriptiu sobre el que acabem de fer. Com per exemple, "**```Creat el fitxer index.html```**".
Aix? ens ser? molt �til per m�s endavant, per quan veiem el log dels **```commit```**'s, puguem recon?ixer a cadascun d'ells i saber que �s el que vam fer just en aquell moment.

```sh
~/<CognomAlmune>-primer-repositori $ git commit -m "Creat el fitxer index.html"
[main (root-commit) 74859bc] Creat el fitxer index.html
1 file changed, 10 insertions(+)
create mode 100644 index.html

~/<CognomAlmune>-primer-repositori $ 
```

> ## Si us apareix un error a l'hora de fer el **```commit```**, reviseu els seg�ents punts:
> 
> ### [Setting your commit email address](./README.md#setting-your-commit-email-address-1)
> 
> ### [Setting your username in Git](./README.md#setting-your-commit-email-address-1)




Ara afegirem dos fitxers m�s: **```main.js```** i **```styles.css```**

```sh
~/<CognomAlmune>-primer-repositori $ touch main.js
~/<CognomAlmune>-primer-repositori $ touch styles.css
~/<CognomAlmune>-primer-repositori $ ls -l
-rw-rw-r-? 1 user user 130 Sep 24 13:00 index.html
-rw-rw-r-? 1 user user   0 Sep 24 13:00 main.js
-rw-rw-r-? 1 user user   0 Sep 24 13:00 styles.css

~/<CognomAlmune>-primer-repositori $ 
```

I de moment els deixem buits i anem a veure qu? ha passat al git.

```sh
~/<CognomAlmune>-primer-repositori $ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
           main.js
           styles.css

nothing added to commit but untracked files present (use "git add" to track)

~/<CognomAlmune>-primer-repositori $
```

Abans de seguir cal confirmar que tenim la nostra instal�laci� de git al nostre ordinador ben configurat.


## [Setting your commit email address](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/setting-your-commit-email-address)

## [Setting your username in Git](https://docs.github.com/en/get-started/getting-started-with-git/setting-your-username-in-git)

# Creaci� d'un usuari a [github.com](https://github.com/)

[Signing up for a new GitHub account](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account)


# Creaci� d'un repositori a la vostre compta a [github.com](https://github.com/)

[Create a repo](https://docs.github.com/en/get-started/quickstart/create-a-repo)

# Com convidar a un col�laborador a un repositori a la vostre compta a [github.com](https://github.com/)

[Inviting collaborators to a personal repository](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository)

