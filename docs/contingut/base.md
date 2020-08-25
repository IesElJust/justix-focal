---
title: Justix base
permalink: /base
---

# Contingut de la iso i primers passos

La iso de Justix disposa del programari bàsic per començar a treballar, i realitza certs ajustos al sistema per al millor funcionament possible de l'aula.

![Escriptori](https://raw.githubusercontent.com/IesElJust/justix-focal/master/docs/_img/escriptori.png)

De manera predeterminada, i **tot i que en la instal·lació se us demana un usuari d'administració, Justix crea dos usuaris**:

* Usuari `eljust` amb password `eljust`, com a usuari administrador del sistema, i
* Usuari `alumne` amb password `alumne`, com a usuari administrador amb permissos restringits. Aquest usuari podrà actualitzar l'equip i instal·lar només alguns paquets.

## Instal·lació a l'aula

Per a la instal·lació a l'aula, s'usaran les imatges crades a partir de la ISO, tenint en compte els següents aspectes:

* Els ordinadors per defecte es diuen *justix*. Quan arranquem per primera vegada com a administradors, comprovarà que el nom és aquest i ens demanarà que el canviem, segon el nom d'ordinador a l'aula.
* Caldrà canviar amb `passwd` la contrassenya de l'usuari administrador.
* Els alumnes podran modificar-se també la seua contrassenya d'accés.
* A cada aula de cicles, faltarà per instal·lar el metapaquet corresponent al cicle en qüestió.
* Per als ordinadors del professor, s'instal·larà el paquet `justix-profe`, que afig un parell d'eines com l'`arpon`, per evitar atacs ARP i el `Cluster-ssh`, per accedir als equips de l'aula de forma més fàcil. A més, aquest paquet crea els usuaris genèrics **profe**, **fol** i **angles**, sense permissos d'administració.

## Instal·lació des de la iso

Per tal d'instal·lar *Justix* a un ordinador d'escriptori, caldrà descarregar [la imatge iso](https://www.dropbox.com/sh/zveu1qd6nrcr2ay/AAAKf_XAN0r0ZGVuU_GJY_RQa?dl=0) i generar un USB d'arrencada amb ella.

Si s'inicia la imatge en mode *live*, és a dir, en lloc de l'instal·lador, arrancant directament el sistema des de l'USB, l'usuari per accedir al sistema serà l'usuari ***eljust***, amb contrassenya ***eljust***. En aquest mode, per tal de fer la instal·lació, no disposem d'un accés directe a l'escriptori, sinò que s'ha d'invocar l'instal·lador des de la línia d'ordres. Per a això, obrirem el Tilix, i llançarem l'ordre:

```
sudo ubiquity
```
Amb això se'ns iniciarà l'assistent d'instal·lació.

Cal recordar que, tot i que ens demanarà en una pantalla de configuració el nom d'usuari administrador i la contrassenya, la instal·lació de base de Justix sobreescriu aquests amb els usuaris `eljust` (administrador) i `alumne`.

## Entorn d'escriptori

L'entorn d'escriptori de Justix és Ubuntu Mate, personalitzada de manera que:

* Disposa d'una barra superior amb el menú principal, els escriptoris, rellotge i la safata del sistema.
* A la part inferior disposem d'un *dock* amb accessos directes a les aplicacions més comunes, i que farà també de barra de tasques.
* De manera predeterminada, utilitza l'emulador de terminal *Tilix*, que ens permet partir la pantalla en diverses particions, tant horitzontals com verticals.

## L'usuari alumne

L'usuari predeterminat *alumne* pot realitzar diverses accions amb `sudo`, entre elles:

* Actualitzar i netejar el sistema (`update`, `upgrade`, `dist-upgrade` i `clean`),
* Actualitzar els paquets *Snap* (`snap refresh`)
* Instal·lar els metapaquets corresponents als diferents cicles (`justix-asix-meta`, `justix-dam-meta` i `justix-smx-meta`),
* Executar *qemu* com a root,
* Actualitzar l'*Extension Pack* de Virtualbox, que requereix permís d'administrador,
* Instal·lar aplicacions de desenvolupament amb d'Ubuntu Make (`umake`),
* Treballar amb *Mininet* (`mn` i `mnexec`)
* Treballar amb Docker

## Eines comunes
   
La instal·lació de base de Justix aporta una sèrie d'utilitats d'ús comú  i per millorar el sistema que no venen per defecte en Ubuntu:

| Aplicació | Descripció |
|-----------|------------|
| tilix     | Terminal de tipus mosaic, com a alternativa al mate-terminal, que ens permet partir la finestra tant com desitgem |
| vim       | Editor de text |
| tree      | Llistat de directoris en forma d'arbre |
| Oracle Virtualbox 6.1 | Programari de virtualització  |
| docker-ce | Interfície en línia d'ordres pe gestionar imatges i contenidors Docker |
| docker-compose | Eina per crear i executar aplicacions multi-contenidor amb Docker |

A més, es descarrega i instal·la automàticament el pack d'extensions de virtualbox, per al qual s'ha d'acceptar la llicència prèviament. Per altra banda, es configura l'usuari *alumne* com a membre del grup *docker*, de manera que pot utilitzar aquest sense necessitat d'executar-lo com a *sudo*. 

## Utilitats de xarxa

A través del paquet `justix-network-pack`, s'instal·la el següent programari:

| Aplicació | Descripció |
|-----------|------------|
| nmap  | Analitzador de xarxa |
| openssh-server    | Servidor d'SSH |
| filezilla | Client d'FTP |
| google-chrome-stable | Navegador web |


Per a informació més detallada dels paquets, podeu consultar la documentació de la versió 18.04.