---
title: Justix DAM meta
permalink: /dam
---

# Programari per a DAM/DAW

El programari per a DAM i 1r curs de DAW s'afig amb el paquet `justix-dam-meta`. Per instal·lar-lo, des de la línia d'ordres farem (bé com a l'usuari `eljust` o com a `alumne`):

```
sudo apt install justix-dam-meta
```

El programari instal·lat és el següent:

## Bases de dades

| Aplicació  |  Descripció |
|-----------|------------|
| mysql-workbench-community | Client de MySQL |
| mongodb-org  |   Base de dades mongoDB |
| mysql-server | Servidor de MySQL |

Respecte a la versió anterior, Ubuntu 20.04 no incorpora MySQL Workbench als seus repositoris, pel que s'ha reemplaçat per l'edició *Community*, des d'un repositori extern.

## Eines de desenvolupament genèriques

| Aplicació | Descripció| 
|-----------|------------|
| Visual Studio Code | Editor de codi |
| justix-pseint | Eina pseint per treballara mb diagrames de flux |

A més, a la base de Justix es disposa d'Ubuntu Make, que ens permet instal·lar (tant com a usuari `eljust` com `alumne`) diverses eines tant relacionades amb les BD com IDEs, com l'Android Studio, el DBeaver o Eclipse, entre molts altres.

## Desenvolupament Java

| Aplicació | Descripció |
| -----------|------------|
| Netbeans | Entorn de Desenvolupament Integrat |
| default-jre | Entorn d'execució de Java |
| oracle-java10-installer | Instal·lador de Java 10 |
| openjdk-11-jdk | Versió lliure del Java Developement Kit 11 |
| gradle | Gestor de projectes i dependències per a java |

A més, s'incorpora l'eina `ghex` per analitzar codi compilat.

També s'incorpora el dimoni de paquets *Snap*, ja que Netbeans s'instal·la mitjançant aquest sistema, de manera que disposem de la última versió disponible.
