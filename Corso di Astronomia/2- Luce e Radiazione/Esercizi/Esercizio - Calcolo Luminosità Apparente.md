
### Come viene calcolata la scala di magnitudine apparente?

Sappiamo che una stella di magnitudine 1 è più luminosa di una stella di magnitudine 2. Ma di quanto più luminosa?

La scala di magnitudine è logaritmica, dove una differenza di 5 magnitudini corrisponde sempre a un cambiamento di luminosità di un fattore di 100. Ciò significa che una stella di magnitudine 1 è 100 volte più luminosa di una stella di magnitudine 6, e analogamente, una stella di magnitudine 2 è 100 volte più luminosa di una stella di magnitudine 7.

![Figura3](../../../Utils/Risorse/magnitudine2.png)
Una mappa tipica delle costellazioni. In basso a sinistra, puoi vedere una scala delle magnitudini da uno a sei. Una stella di magnitudine uno è 100 volte più luminosa di una stella di magnitudine sei.


---

## **1. Il fattore di luminosità tra magnitudini**

Per definizione, **una differenza di 5 magnitudini corrisponde a un fattore 100 di luminosità**.  
Perciò, il fattore di luminosità associato a **1 magnitudine** è:

$100^{1/5}≈2.5118864315≈2.512$

Spesso viene approssimato a **2,5** per semplicità, ma il valore reale è **2,512**.

Da questo valore derivano i fattori per 2, 3, 4 e 5 magnitudini:

- **1 magnitudine** → 2,512
    
- **2 magnitudini** → 2.5122≈6.31
    
- **3 magnitudini** → 2.5123≈15.85
    
- **4 magnitudini** → 2.5124≈39.81
    
- **5 magnitudini** → 2.5125≈100
    

Ogni salto di magnitudine si **compone** col precedente (non si somma: si moltiplica).

---

## **2. Esempio introduttivo**

Se una stella ha magnitudine **1** e un’altra **3**, la differenza è:

$$3−1=2$$

Quindi la stella di magnitudine 3 appare:

$$2.512^2 \approx 6.31$$

volte **meno luminosa** della stella di magnitudine 1.

---

## **3. Confronto tra Luna Piena e Venere**

Usiamo magnitudini tipiche:

- **Luna Piena**: –12.7
    
- **Venere**: –4.6
    

La differenza di magnitudine è:

$$−4.6−(−12.7)=8.1$$

Per sapere quanto è più luminosa la Luna, usiamo il fattore 2.512:

$$2.512^{8.1} \approx 1700$$

**La Luna Piena è circa 1.700 volte più luminosa di Venere.**

---

## **4. Formula generale della scala delle magnitudini**

Per confrontare le luminosità apparenti di due oggetti A e B:

$$\frac{I_A}{I_B} = 2.512^{(m_B - m_A)}$$

dove

- $IA,IB$ = intensità (o luminosità apparente),
    
- $mA,mB$​ = magnitudini apparenti.










 Derivazione completa del fattore di luminosità dalla formula di Pogson


## 1. Formula di Pogson

La relazione tra magnitudine e flusso luminoso è:

$$m_2 - m_1 = -2.5 \log_{10}\left(\frac{F_2}{F_1}\right)$$

---

## 2. Ricaviamo il rapporto di luminosità

Partendo da:

$$m_2 - m_1 = -2.5 \log_{10}\left(\frac{F_2}{F_1}\right)
$$
Isoliamo il logaritmo:

$$\log_{10}\left(\frac{F_2}{F_1}\right) = -\frac{m_2 - m_1}{2.5}
$$
Applichiamo l'esponenziale:

$$2.5\frac{F_2}{F_1} = 10^{-\frac{m_2 - m_1}{2.5}}$$

Con:

Δm=m2−m1

la formula generale diventa:

$$\frac{F_2}{F_1} = 10^{-0.4\,\Delta m}$$

---

## 3. Fattore luminoso per 1 magnitudine

Per una differenza di 1 magnitudine:

Δm=1

Allora:

$$\frac{F_2}{F_1} = 10^{-0.4}$$

Il **fattore per cui l'oggetto più luminoso è più brillante** è il reciproco:

$$R_1 = 10^{0.4} = 2.5118864315 \approx 2.512$$

---

## 4. Da Pogson: 5 magnitudini = fattore 100

Per definizione:

$$R_5 = 100$$

Poiché i fattori si **moltiplicano**:

$$R_1^5 = 100$$

Ricaviamo il fattore per 1 magnitudine:

$$R_1 = 100^{1/5}$$

Poiché:

$$100 = 10^2$$

abbiamo:

$$R_1 = (10^2)^{1/5} = 10^{2/5}$$

e poiché:

$$\frac{2}{5} = 0.4$$

segue:

$$R_1 = 10^{0.4} \approx 2.512$$

---




