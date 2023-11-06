# A01U - Activitat 1 - Primera activitat amb ***```git```***

## ***QUATRE*** pre-requisits:

***Requisit* 1.** Tenir instal·lat l'**```IDE```** **```Visual Studio Code```**. Un **```IDE```** és un **Entorn integrat de desenvolupament** (de les sigles en anglès: ***Integrated Development Environment***).

> ### Per fer la instal·lació del **```Visual Studio Code```** podeu seguir els [Passos per instal·lar l'**IDE** **```Visual Studio Code```**](./manuals/vsc-instalar.md)

***Requisit* 2.** Tenir instal·lat el **sistema de control de versions** **```git```**. Consisteix en una aplicació que **gestiona de canvis en arxius i directoris**.

> ### Per fer la instal·lació del **sistema de control de versions** **```git```** podeu seguir les [Passos per instal·lar el **sistema de control de versions** **```git```**](./manuals/git-instalar-git.md)

Aquí teniu un [Git Tutorial (w3schools.com)](https://www.w3schools.com/git/default.asp?remote=github)

***Requisit* 3.** Tenir un compte de [**```github.com```**](https://github.com/), podeu seguir els passos de [**Getting started with your GitHub account**](https://docs.github.com/en/get-started/onboarding/getting-started-with-your-github-account)


***Requisit* 4.** Tenir creat al vostre ordinador l'**estructura inicial**, cal que seguiu els passos de [Passos per crear **l'estructura inicial**](./manuals/crea-creacio-estructura.md) 

> ### Abans de començar cal fer la [Comprovació de que ho teniu ben instal·lat](./manuals/ctrl-comprovacio-tot-ben-installat.md)

Un cop ja teniu els **dos programes instal·lats**, el **compte creat** [**```github.com```**](https://github.com/) i **l'estructura inicial** creada, ja podeu començar aquesta activitat.

## Objectiu:

Crear un projecte amb el nom **```el-meu-primer-repositori```**, amb:
* un **repositori local** i
* un **repositori remot**,
* que estiguin **vinculats**.

Fent servir **```git```** com a **sistema de control de versions** i l'**IDE** **```Visual Studio Code```**.

## **Pas 1.** Crear un **repositori local** al vostre ordinador.

> ## NOTA: **Bona pràctica** 
> 
>  Com a **bona pràctica**, us recomano, crear sempre una carpeta pel ***repositori local***, amb el mateix nom que el vostre ***repositori remot***.

Nom de la carpeta per crear el vostre **repositori local**: **```el-meu-primer-repositori```**.

![Alt text](./images/a01u-01-crear-nova-carpeta.png)

Dins de la carpeta **```c:\smx2\repos```**, crearem la carpeta **```el-meu-primer-repositori```**.

![Alt text](./images/a01u-02-crear-carpeta.png)

Ara obrirem la carpeta **```c:\smx2\repos\el-meu-primer-repositori```** des de el **```Visual Studio Code```**.


![Alt text](./images/a01u-03-obrir-carpeta-a-code_01.png)

Per fer-ho, seleccionada la carpeta **```c:\smx2\repos\el-meu-primer-repositori```**, pitjarem el botó dret del ratolí, i seleccionarem l'opció **```Show more options```**, perquè ens mostri més opcions del menú contextual.

![Alt text](./images/a01u-04-obrir-carpeta-a-code_02.png)

I a continuació seleccionarem l'opció **```Open with Code```**, per que ens obri el **```Visual Studio Code```** situat ja en aquesta carpeta.

La primera vegada que obrim qualsevol carpeta amb **```Visual Studio Code```**, aquest ens pregunta si ***Confiem en els autors dels fitxers d'aquesta carpeta***, li diem que ***sí***, és a dir, pressionem el botó ![Alt text](./images/code-boto-trust-authors.png). 

![Alt text](./images/a01u-05-I-trust-the-authors.png)

I ja tenim el **```Visual Studio Code```** obert i situat a la carpeta **```c:\smx2\repos\el-meu-primer-repositori```**.

![Alt text](./images/a01u-06-obert-per-primera-vegada.png)

## **Pas 2.** Crear un **repositori remot** al vostre compte de [**```github.com```**](https://github.com/).

Des de el vostre compte de [**```github.com```**](https://github.com/),
desplegant el símbol **```+```** ![sdad](./images/github-boto-+-afegir.png) i escollirem l'opció **New repository**, per crear un nou repositori.

![Alt text](./images/a01u-07-nou-repositori.png)

A la finestra **Create a new repository**, en el camp **```Repository name```** escriurem el nom del repositori que volem crear, en el nostre cas, i seguint les bones pràctiques comentades, serà el nom del projecte **```el-meu-primer-repositori```**.

![Alt text](./images/a01u-08-nom-repositori.png)

A continuació marquem l'opció **```Private```**. 
> ## NO cal marcar l'opció **```Add a README.md file```**.

![Alt text](./images/a01u-09-nou-repositori-privat.png)

I per últim pressionem el botó **```Create repository```**, per crear el nou repositori.

Un cop creat el nou repositori ens apareix el següent:

![Alt text](./images/a01u-10-inici-nou-repositori.png)



Si ens desplacem una mica cap avall, veurem un seguit de comandes a la secció amb el titol **```... or create a new repository on the command line```**

![Alt text](./images/a01u-11-comandes-nou-repositori.png)

Aquestes son les comandes, i cal copiar-les totes per poder-les fer servir a continuació.

```
echo "# el-meu-primer-repositori" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/<usuariGithub>/el-meu-primer-repositori.git
git push -u origin main
```

> Si no us funciona el botó de copiar, sempre podeu seleccionar les comandes i amb el botó dret del ratolí copiar-les al porta-papers del sistema operatiu.
>
> ![Alt text](./images/a01u-12-copiar-comandes-nou-repositori.png)

## **Pas 3.** Vincular el vostre **repositori local** amb el vostre **repositori remot** creat al compte de [**```github.com```**](https://github.com/).

Un cop que hem copiat totes aquestes comandes, passarem al **```Visual Studio Code```**.

I com ja s'ha vist anteriorment, obrirem una **finestra de terminal**.

![Alt text](./images/a01u-13-obrir-terminal-vsc.png)

Un cop oberta la **finestra de terminal** podeu enganxar totes les comandes, col·loqueu-vos a sobre de la **finestra de terminal** i  pressionant el botó dret del ratolí se us enganxaran les comandes que heu copiat anteriorment. 

![Alt text](./images/a01u-14-comandes-copiades-terminal-vsc.png)

Si a continuació pressioneu la tecla <kbd>Intro</kbd>

La primera vegada us apareixerà aquesta finestra, per validar l'usuari i la contrasenya.

![Alt text](./images/a01u-15-validacio-usuari-github.png)

![Alt text](./images/a01u-16-validacio-usuari-01.png)

![Alt text](./images/a01u-17-validacio-exitosa.png)

![Alt text](./images/a01u-18-git-push-fet.png)

