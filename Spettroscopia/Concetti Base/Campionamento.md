---
tags:
  - spettrografia
  - spettroscopia
  - definizione
---

Campionare significa **trasformare qualcosa di continuo in una serie di misure discrete**, cioè in **punti separati**, perché **uno strumento reale non può misurare tutto in modo continuo**.

## Esempio
La temperatura varia in maniera continua ogni secondo passando, per esempio, da 20.1 °C a 20.2 °C, poi a 20.3 °C e così via.
Se la misuro nella giornata avrò qualcosa come
- alle 10:00 → 20 °C    
- alle 11:00 → 21 °C    
- alle 12:00 → 22 °C    

Quindi ho **campionato** la temperatura, che significa non conoscere tutto l'andamento, ma solo che sta aumentando. Poi posso ricostruire tutti i punti facendo fitting.

## Campionamento in uno spettro

In spettroscopia:
- l’asse orizzontale è la **lunghezza d’onda**,    
- l’asse verticale è l’**intensità**.

Il sensore CCD/CMOS è fatto di **pixel** e ogni pixel misura la luce **in un intervallo finito di lunghezze d’onda**. Quindi, in pratica ogni pixel è **un campione** dello spettro.

Quindi
- 1 Å/pixel  --> ogni campione rappresenta 1 Å di spettro.

## Differenza con la [[Risoluzione]]

- **Risoluzione** → quanto è piccolo il dettaglio _fisico_ che lo strumento può distinguere
- **Campionamento** → quanto finemente avviene la _misura_