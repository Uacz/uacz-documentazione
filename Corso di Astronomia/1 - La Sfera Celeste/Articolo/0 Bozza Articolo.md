## L'Astrometria: Definizione e Ruolo dei Sistemi di Coordinate Altazimutali ed Equatoriali

### 1. La Rappresentazione della Volta Celeste e i Fondamenti dell'Astrometria

Quando eleviamo lo sguardo al cielo notturno, l'occhio umano percepisce l'universo come se fossimo situati al centro di una vasta semisfera. Su questa volta celeste, tutti i corpi appaiono proiettati alla medesima distanza. La branca dell'astronomia che si dedica a **calcolare con precisione la posizione degli astri sulla sfera celeste** è definita **Astrometria**. 
Per descrivere la posizione di un qualsiasi astro, è necessario impiegare **due coordinate**. Tuttavia, è fondamentale tenere presente che questo sistema di coordinate è dinamico, poiché la volta celeste stessa sembra muoversi — un moto apparente causato, in realtà, dalla rotazione della Terra.

Prima di affrontare i sistemi specifici, è utile richiamare i concetti fondamentali di geometria sferica. Un **Cerchio Massimo** è l'intersezione della sfera con un piano che passa per il suo centro (ad esempio, ABCDA). Al contrario, un **Cerchio Piccolo** è l'intersezione con un piano che non passa per il centro (come EFGHE). Un esempio significativo di cerchio piccolo è l'**Almucàntarat** (termine derivato dall'arabo), il parallelo della sfera celeste che individua tutti i punti con la **medesima altezza ($h$)**. In questo contesto, il **Meridiano Locale** è il cerchio massimo della sfera celeste che funge da proiezione del meridiano geografico dell'osservatore, passando per i poli celesti e i poli dell'orizzonte, noti come **Zenith** (sopra l'osservatore) e **Nadir** (sotto l'osservatore).

### 2. Il Sistema Altazimutale: Legato all'Osservatore

Il primo sistema di riferimento che analizziamo è quello **Altazimutale**, che utilizza l'orizzonte locale come piano di riferimento. Le due coordinate impiegate sono l'**Altitudine** (o Altezza) e l'**Azimut** (un termine che significa "direzioni" in arabo). L'Azimut viene misurato in gradi, partendo da **Nord ($0^\circ$ o $360^\circ$)** e proseguendo attraverso l'Est ($90^\circ$), il Sud ($180^\circ$), e l'Ovest ($270^\circ$).

Questo sistema ha il grande pregio di essere **facile da capire e da usare**. Nonostante la sua semplicità, il sistema Altazimutale presenta limiti operativi significativi: le sue coordinate **dipendono dalla latitudine e dalla longitudine** dell'osservatore, e soprattutto, le stelle **cambiano continuamente posizione**. Questi fattori lo rendono **difficile da usare con un telescopio manuale** per il tracciamento celeste.

### 3. Il Sistema Equatoriale: Il Riferimento Fissato

In contrapposizione, il **Sistema di Coordinate Equatoriali** proietta i riferimenti terrestri sull'intera sfera celeste. Le sue coordinate sono la **Declinazione ($\delta$)** e l'**Ascensione Retta ($\alpha$)**.

La **Declinazione** rappresenta l'angolo tra l'equatore celeste e l'oggetto, misurata in gradi da $0^\circ$ fino a $90^\circ$ (per i poli celesti). Un punto di riferimento essenziale per l'Ascensione Retta è il **Punto Vernale** (o Punto Gamma $\Upsilon$ o Punto d'Ariete), definito come quel punto della Sfera Celeste in cui il Sole, durante il suo moto apparente annuale, **transita sull’Equatore in Primavera**. Si osserva che l'angolo che si forma tra l'eclittica (il percorso apparente del Sole) e l'equatore celeste è di **$23,5^\circ$**.

I vantaggi di questo sistema sono evidenti per la comunità scientifica globale. Le coordinate equatoriali **sono le stesse per ogni osservatore**. Se un astrofilo scopre una nuova cometa, è sufficiente che fornisca la sua declinazione e ascensione retta per permetterne l'individuazione da parte di chiunque abbia interesse, sia che si trovi in Australia, Giappone, o America. Inoltre, l'utilizzo di una montatura equatoriale permette di **muovere il telescopio in una sola direzione** per seguire il moto apparente dell'oggetto celeste. Nonostante la loro stabilità, queste coordinate sono **un po' più difficili da comprendere** e non sono _completamente_ fisse nel tempo: variazioni sottili impongono di considerare il **Moto Proprio delle Stelle** e il fenomeno della **Processione degli Equinozi**.

### 4. Il Tempo Siderale e il Moto del Sole

Il sistema Equatoriale è intimamente legato al moto terrestre. La Terra compie una rotazione di $360^\circ$ attorno al suo asse in 24 ore. Poiché l'anno di rivoluzione (anno siderale) dura circa 365,26 giorni, in un giorno la Terra si sposta approssimativamente di **un grado lungo la sua traiettoria** orbitale.

Analizzando il rapporto tra rotazione e tempo, si scopre che 15 gradi di rotazione equivalgono a un'ora. Di conseguenza, la Terra impiega circa **4 minuti** per compiere quel grado in più richiesto per riallinearsi con il Sole. Questo significa che, ogni giorno, il **Sole sorge 4 minuti prima**, determinando un cambiamento costante nella visibilità delle costellazioni.

### 5. Utilizzo Pratico: Sincronizzazione della Montatura Equatoriale

Le montature equatoriali, in particolare quelle manuali, utilizzano il **Cerchio di Declinazione** e il **Cerchio di Ascensione Retta (AR)**. Queste scale graduate sono particolarmente utili sui telescopi manuali per localizzare oggetti deboli che non sono visibili a occhio nudo.

Per procedere al puntamento preciso, la montatura deve essere stazionata sul meridiano locale e la scala di Ascensione Retta deve essere sincronizzata con l'**Ora Siderale Locale (TSL)**.

Il calcolo del TSL si effettua partendo dal Tempo Siderale a Greenwich (TSG) — ricavabile da tabelle o software — e applicando una correzione basata sulla propria longitudine ($\lambda$). La formula prevede di sommare o sottrarre $\lambda/15$ (dove $\lambda$ è la longitudine in gradi), a seconda che ci si trovi a est (sommare) o a ovest (sottrarre) di Greenwich. Ad esempio, a Catanzaro (longitudine $16,6^\circ$ Est), la correzione è di circa 1,11 ore (1 ora e 7 minuti).

Una volta completato l'allineamento polare (l'Asse AR deve essere allineato con il Polo Nord Celeste, ad esempio puntando la Stella Polare), si imposta l'orario del meridiano locale (corrispondente al TSL) sul **riferimento principale (punto 1)** della scala di AR, senza muovere il telescopio. Questo riferimento principale è quello che verrà utilizzato sia per l'azzeramento sia per la lettura della scala durante l'uso normale. Il riferimento secondario (punto 2), tipicamente ruotato di $90^\circ$, è invece un ausilio utile solo per particolari procedure avanzate o di verifica, come i movimenti di $90^\circ$ (6 ore) sull'asse di AR.

Per puntare un oggetto:

1. Si punta inizialmente una stella luminosa di cui si conoscono le coordinate.
2. Si regolano i cerchi graduati sui valori di Declinazione e Ascensione Retta di tale stella.
3. Successivamente, si ruotano i due assi del telescopio fino a far corrispondere i valori delle scale a quelli dell'oggetto desiderato.

Nel movimento: la scala di AR è graduata in ore, minuti e secondi, mentre la declinazione è in gradi, primi e secondi. Ruotando in AR verso **Est**, l'AR aumenta, puntando oggetti che devono ancora culminare; ruotando verso **Ovest**, l'AR diminuisce, puntando oggetti che sono già passati al meridiano. Infine, quando la Declinazione è a $0^\circ$, si sta puntando l'equatore celeste.