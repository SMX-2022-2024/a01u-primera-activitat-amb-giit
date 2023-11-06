## Comprovació de que ho teniu ben instal·lat.

Abans de començar. us recomano que tingueu activades les següents opcions.

**Previ 1.** Activada l'opció de **mostrar** el **fitxers ocults**.

![Alt text](../images/ctrl-00-1-conf-hidden-files.png)

**Previ 2.** Activada l'opció de **mostrar** l'**extensió dels fitxers**.

![Alt text](../images/ctrl-00-2-conf-show-extension-files.png)


## Ara si que ja podem procedir amb la comprovació.


**1.** Pressioneu <kbd>Windows</kbd> + <kbd>R</kbd>

![Alt text](../images/ctrl-01-pri-act-1r-control.png)

**2.** Al quadre de text **Open** o **Abrir**, escriviu **```cmd```** i pressioneu <kbd>Enter</kbd>

![Alt text](../images/ctrl-02-cmd.png)

**3.** A la finestra amb la línia de comandes escriviu **```open```** i pressioneu <kbd>Enter</kbd>, això us farà que s'obri l'**IDE** **```Visual Studio Code```**.

![Alt text](../images/ctrl-03-1a-exe-code.png)

I si és la primera execució, com es pot veure, us apareixerà la **finestra de benvinguda** com es pot veure.

Desmarqueu el ***check box*** de l'opció **```Show welcome page on startup```**, per què no us aparegui aquesta **finestra de benvinguda** cada vegada que obriu el **```Visual Studio Code```**, i tanqueu la **finestra de benvinguda** amb <kbd>Ctrl</kbd> +  <kbd>W</kbd>.

![Alt text](../images/ctrl-04-exec-neta.png)

A continuació obrirem una **finestra de terminal**, per veure si tenim correctament instal·lat **```git```**.

Per fer-ho podeu desplegar el menú Terminal, que veureu desplegant l'opció dels **```tres punts```** ![boto-tres-punts](../images/code-boto-tres-punts.png), i de l'opció **```Terminal```**, escollir **```New Terminal```**. O bé pressionar la següent combinació de tecles <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>ñ</kbd>.

![Alt text](../images/ctrl-05-abrir-terminal.png)

Per obrir una **finestra de terminal**.

![Alt text](../images/ctrl-06-abrir-terminal-ps-1r-cop.png)

Com es pot veure, la primera vegada ens obrirà una **finestra de terminal** de **```PS```** (**```Power Shell```**).

Per fer que cada vegada ens obri una **finestra de terminal** de git bash, cal que modifiquem la configuració del **```Visual Studio Code```**. 

Desplegarem el simbol de <kbd>+</kbd> que es veu al costat de la paraula **```powershell```**, ![Alt text](../images/code-boto-+-terminal.png).

I del desplegable que apareixerà seleccionarem la opció **```Select Default Profile```**, per poder seleccionar quin volem que sigui el perfil per defecte que s'obri.

![Alt text](../images/ctrl-07-canviar-obrir-terminal-defecte.png)

I seleccionem l'opció ![icona](../images/code-icona-git-bash.png) **```Git Bash```**.

![Alt text](../images/ctrl-08-terminal-defecte-gitbash.png)

Sembla que no ha fet res.

![Alt text](../images/ctrl-09-terminal-defecte-gitbash.png)

Pero si tanquem la **finestra de terminal** de **```PS```** (**```Power Shell```**) amb el botó ![boto-tanca](../images/code-icona-tanca-terminal-ps.png) per tancar la **finestra de terminal** de **```PS```**.

I tornem a obrir una **finestra de terminal**
![Alt text](../images/ctrl-05-abrir-terminal.png)


![Alt text](../images/ctrl-10-obrir-terminal-gitbash.png)

Si s'obre una **finestra de terminal** de **```bash```**, és que ja ho teniu tot funcionant correctament!

## Comprovació de configuració de ***nom d'usuari*** i ***correu*** de **```git```**.

Ara cal comprovar que teniu ben configurat el programa de **```git```**, pel que fa referència al vostre usuari de [**```github.com```**](https://github.com/).

Seguiré l'exemple pressuposant que el següent:

|Clau|Valor|
|----|----|
|**usuari de github**|**```joanpardogine```**|
|l'**adreça del compte de correu electrònic** del compte de [**```github.com```**](https://github.com/)|**```joanpardogine@ginebro.cat```**|

Cadascú en el seu cas, cal que feu servir el vostre usuari i l'**adreça del compte de correu electrònic**

### Comprovació **usuari de github**

Per veure si tenim l'**usuari de github** configurat cal executar la comanda:

```
git config --global user.name
```

![Alt text](../images/ctrl-11-check-git-user-blank.png)

Si NO us apareix res, significa que no està configurat.

Per configurar-lo cal executar la comanda següent:

```
git config --global user.name <nomUsuari>
```

Per exemple en el meu cas:

```
git config --global user.name joanpardogine
```

![Alt text](../images/ctrl-12-congfig-git-user-joanpardogine.png)

I per comprovar que s'ha configurat correctament tornem a executar la comanda:

```
git config --global user.name
```

I en aquest cas, si està configurar, ens mostrarà el nom que acabem de configurar. 

### Comprovació **correu de github**

Per veure si tenim el **correu de github** configurat cal executar la comanda:

```
git config --global user.email
``` 

![Alt text](../images/ctrl-13-check-git-email-blank.png)

Si NO us apareix res, significa que no està configurat.

Per configurar-lo cal executar la comanda següent:

```
git config --global user.email <correu de github>
```

Per exemple en el meu cas:

```
git config --global user.email joanpardogine@ginebro.cat
```

![Alt text](../images/ctrl-14-check-git-email.joanpardogine.png)


Ara si que si heu arribat a aquest punt, ja ho teniu **TOT** i ben instal·lat, ara ja podeu tancar el **```Visual Studio Code```**. Per fer-ho cal pressionar <kbd>Alt</kbd> + <kbd>F4</kbd>.
