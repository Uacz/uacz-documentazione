---
tags:
  - spettrografia
  - spettroscopia
  - definizione
---
### Teorema di Nyquist–Shannon

In elaborazione dei segnali:

> per ricostruire correttamente un segnale, esso deve essere campionato ad almeno **due campioni per ogni dettaglio minimo**.
> Mi dice il limite minimo, oltre la quale misurare diventa impossibile, ma non la configurazione migliore per misurare

Fondamentalmente è come dire che per tracciare una retta servono due punti. Specificando un po' di più, due campioni sono il minimo indispensabile per distinguere un massimo da un minimo, un fronte da un bordo, una riga da un rumore.
Se si campiono meno di due volte si ha aliasing, ovvero il segnale viene interpretato male, viene "sfocato". Come quando una telecamera non acquisisce tutti i fotogrammi necessari a riprodurre il movimento della ruota ed essa sembra ferma o gira più lentamente oppure gira all'indietro. 

Applicato alla spettroscopia:
- il “segnale” è il **profilo della riga spettrale**    
- il “dettaglio minimo” è la sua **larghezza FWHM**.    

Facciamo tre casi:

#### Caso 1 : Riga su 1 pixel (Sotto campionamento)

Se la riga cada tutta su un pixel non possiamo sapere quanto è larga, se è centrato o se è simmetrica. In pratica non posso misurare la posizione.
Immaginiamo sopra i catini dei pixel e sotto la riga


```
|_______|_______|_______|
            /\ 
           /  \
__________/____\________
```

produce, ad esempio, questo

```
0   150   0   
```
#### Caso 2 : Riga su 2 pixel (limite di Nyquist)

Posso effettivamente riconoscerla e posso stimare grossolanamente il centro. Posso vedere solo se la curva sta salendo o scendendo, non posso determinare la forma.

```
|____|____|____|____|
         /\ 
        /  \
_______/____\__________
```

```
0   80  70 0   
```
Ovvero: prima sale e poi scende


#### Caso 3 : Riga su 3 pixel (Situazione ideale)
Vedo la forma e posso misurare la FWHM e il centro. La risoluzione dello strumento può essere utilizzato per fare fitting della curva

```
|___|__|__|__|___|
        /\ 
       /  \
______/____\_______

```

```
0   25   70   25   0
```

Ovvero: vedo la campana!

#### Caso 4 : Riga su 6 pixel  (Sovra campionamento)
La riga è più spalmata e non guadagno risoluzione reale. In pratica spalmo il segnale peggiorando il rapporto segnale/rumore perché la stessa luce è distribuita su più pixel.

```
|_|_|_|_|_|_|_|_|_|
        /\ 
       /  \
______/____\______


```

```
5   45   70   25   5
```

Ovvero: non miglioro ma distorgo

### Regola pratica in spettroscopia

Una riga spettrale deve essere campionata da:
$$\text{FWHM} \ge 2 \text{ pixel} \quad \text{(minimo teorico)}$$

Nella pratica:
- **2 px** → limite di Nyquist (rischio aliasing),    
- **2,5–3 px** → campionamento ottimale,    
- **>4 px** → oversampling (più rumore, nessun guadagno reale).
    

> ridurre troppo la dispersione (Å/px troppo piccoli) **non aumenta automaticamente la risoluzione**, se la riga resta più stretta di ~2 pixel

## Nuovo esempio con due righe

### 1. La riga doppia “vera” (nel mondo fisico)

Immagina **due righe spettrali molto vicine**, ad esempio un doppietto.

Fisicamente lo spettro è così:

```
        /\      /\
       /  \    /  \
______/____\__/____\______
```

Due collinette separate, con:
- due massimi,
- una piccola valle in mezzo.
    **Se riesci a vedere la valle**, stai risolvendo le due righe.

---

# 2. La riga doppia e il sensore: entrano i pixel


## Caso A – Campionamento pessimo (una riga per pixel)
Pixel grandi:

```
|_______|_______|_______|
           /\  /\
          /  \/  \
_________/________\_____

```

Cosa succede:
- entrambe le righe cadono **nello stesso pixel**
- il pixel misura la **somma della luce**

Misura
```
0   180   0
```

Il sensore vede **una sola riga** ovvero le due righe sono **fisicamente presenti**,  ma **digitalmente indistinguibili**.

---

## Caso B – Campionamento al limite (Nyquist)

Pixel un po’ più piccoli:

```
|_____|_____|_____|_____|
        /\  /\
       /  \/  \
______/________\_______

```

Dati:

```
5   100   85   00   0
```

Ora:
- vedi una **spalla**, intuisci qualcosa di strano,  ma **non puoi dire con certezza** che siano due righe
- 
---

## Caso C – Campionamento adeguato (risoluzione vera)

Pixel ancora più piccoli:

```
|___|___|___|___|___|
       /\    /\
      /  \__/  \
_____/__________\_____
```

Dati:

```
0   70   40   70   0
```

Qui:
- vedi **due massimi**    e c’è una **valle** tra loro. E quindi si può misurare:  
    - distanza        
    - larghezza        
    - intensità relativa     

 In questo caso si dice che **Le righe sono risolte**.
---

## Caso D – Oversampling

Pixel molto piccoli. Questa volta, per maggiore chiarezza, cambiamo il tipo di grafico. I _p_ sono i pixel

``` nginx
p1  0   |
p2 10   |▁
p3 30   |▃▃▃
p4 55   |▆▆▆▆▆▆
p5 70   |▇▇▇▇▇▇▇
p6 60   |▇▇▇▇▇▇
p7 45   |▅▅▅▅▅
p8 40   |▅▅▅▅
p9 45   |▅▅▅▅▅
p10 60  |▇▇▇▇▇▇
p11 70  |▇▇▇▇▇▇▇
p12 55  |▆▆▆▆▆▆
p13 30  |▃▃▃
p14 10  |▁
p15 0   |
```

Dati:

```
0  10  30  55  70  60  45  40  45  60  70  55  30  10  0
```

La curva non è più simmetrica. Sto sovra campionando e sto perdendo il segnale fisico, non aumentando la risoluzione
    


==Come faccio a capire se sto campionando bene o sovra/sotto campionando? ==
- **LAMPADA DI CALIBRAZIONE**
oppure 
> _Se riduco la dispersione del 20%, vedo più dettagli o solo più rumore?_
- Se vedi **più dettagli** → prima eri sottocampionato. 
- Se vedi **la stessa forma** → stai già campionando bene.
- Se vedi **più rumore** → stai sovracampionando.
oppure *matematicamente*

$$FWHM_{px} ​= \frac {Δλ}{D}​$$
con 
- dispersione D (Å/px)    
- FWHM fisica stimata $\Delta\lambda$ (in Å )
deve essere uguale a 3 px (servono 3 punti indipendenti per disegnare la curva) **PER SINGOLA RIGA** (per una doppia riga mi servono 4 pixel per determinare la valle)

---

# Dove nasce davvero la risoluzione

Ora il punto fondamentale:

> **La risoluzione non è “vedere due righe”  
> è vedere la valle tra di loro**

---

## Collegamento tra Campionamento, [[Dispersione]] e [[Risoluzione]]

Possiamo riassumere così:

|Concetto|Domanda a cui risponde|
|---|---|
|Dispersione|Quanto è “stirato” lo spettro sul sensore?|
|Risoluzione|Qual è la minima differenza in λ distinguibile?|
|Nyquist|Il sensore sta campionando correttamente quella informazione?|

