---
title: Justix ASIX meta
permalink: /asix
---

# Programari per a ASIX

El programari per a ASIX s'afig amb el paquet `justix-asix-meta`, i conté eines relacionades amb l'edició de codi i gestió de bases de dades necessaris per al mòdul.

Per instal·lar-lo, des de la línia d'ordres farem (bé com a l'usuari `eljust` o com a `alumne`):

```
sudo apt install justix-asix-meta
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

A més, a la base de Justix es disposa d'Ubuntu Make, que ens permet instal·lar (tant com a usuari `eljust` com `alumne`) diverses eines tant relacionades amb les BD com IDEs, com l'Android Studio o el DBeaver.
