---
title: Justix i Ubuntu
permalink: /standalone
---

# Instal·lació del progrmaari de JustiX a Ubuntu i derivades

JustiX es basa en Ubuntu Mate 20.04, pel que és totalment compatible amb qualsevol sabor d'Ubuntu o distribució derivada (Xubuntu, Kubuntu, LinuX Mint, KDE Neon, etc.)

Així que si teniu ja instal·lada una Ubuntu 20 i voleu disposar del mateix programari que s'utikitza als cicles, disposeu d'una sèrie de metapaquets autònoms o *standalone* que incorporen tot el programari de cada cicle sense arrossegar al darrere tot l'entorn d'escriptori Mate.

Si voleu instal·lar-vos el programari als vostres Ubuntu, ho podeu fer en tres senzills passos:

1. Afegir els fonts de programari (ppa) de l'IES El Just als vostres equips
2. Instal·lar el metapaquet de fonts de programari externes 
3. Actualitzar la caché de paquets i instal·lar el metapaquet del cicle

## 1. Afegint el ppa de l'IES

Per afegir els orígens de programari de l'IES, que es troben a Launchpad, farem, com a usuaris adminitradors del nostre equip:

```
sudo add-apt-repository ppa:ieseljust/focal
```

Amb açò, modificareu els `sources.list` del vostre equip per accedir al programari de JustiX. En afegir el ppa, la caché de paquets s'actualitza automàticament.

## 2. Instal·lar el metapaquet de fonts externes per a JustiX

Aquest paquet us instal·la els diversos orígens d'on obtenim programari que no està disponible directament en Ubuntu, o que es troba en versions més recents. Per instal·lar-lo:

```
sudo apt install justix-external-sources
```

Una vegada instal·lat, actualitzem la caché de paquets si no s'ha fet amb un `sudo apt update`.

## 3. Instal·lació dels metapaquets

Els metapaquets necessaris per a una instal·lació autònoma acaben amb el sufix `-standalone`. 

El primer que instal·larem serà el paquet genèric de cicles, en la seua versió autònoma. Açò ens instal·la algunes utilitats generals.


```
sudo apt install justix-cicles-meta-standalone
```

I ara instal·larem el paquet corresponent al nostre cicle:

* Per a CFGM d'SMX:

```
sudo apt install justix-smx-meta-standalone
```

* Per a CFGM d'ASIX:

```
sudo apt install justix-asix-meta-standalone
```


* Per a CFGM de DAM:

```
sudo apt install justix-dam-meta-standalone
```
