# Eventi e Comandi

### @activities 1
## Introducion 
Differenza tra eventi e comandi

## Eventi
###Introducion Step @unplugged
Un evento è qualcosa che accade durante il gioco, come un giocatore che cammina o vola.
Utiliazziamo gli eventi per generare gli animali. 


###Step 1: Il giocatore cammina
Genera 1 pecora dove c'e il giocatore, quando il giocatore cammina


```blocks
player.onTravelled(WALK, function () {
    mobs.spawn(SHEEP, pos(0, 0, 0))
})

```
###Step2: Il giocatore cammina e genera più pecore
Genera 2 pecore dove c'è il giocatore, quando il giocatore cammina
```blocks
player.onTravelled(WALK, function () {
    for (let index = 0; index < 2; index++) {
        mobs.spawn(SHEEP, pos(0, 0, 0))
    }
})
```

## Comandi
### Introducion Step  
I comandi sono un insieme di istruzioni che viene attivata ed eseguita quando scrivi il nome del comando nella chat.
Utilizziamo un comando per generare gli animali

### Step 1: Spawna i maiali @showhint
Ora impariamo a Spawnare i Maiali. 
Ti serve il blocco Spawn e devi scegliere l'uovo di maiale.
Inserisci il blocco Spawn nel comando chat. Scegli l'uovo di maiale dall'inventario del comando e indicare le coordinate. Scegli le coordinate 1,0,1 per generare un maiale accanto al tuo giocatore.
```blocks
player.onChat("run", function () {
	mobs.spawn(PIG, pos(1, 0, 1))
})
```

### Step 2: Spawna 10 maiali
Spawniamo più di un maiale.
Non copiare 10 volte il blocco Spawn, usa un ripeti e indica quante volte vuoi ripetere l'istruzione.
Inserisci il blocco ripeti nel comando chat, scrivi 10 per ripetere 10 volte e inserisci all'interno il comando Spawn.
```blocks
player.onChat("run", function () {
// @highlight
	for (let i = 0; i < 10; i++) {
       mobs.spawn(PIG, pos(1, 0, 1))
}

blocks.place(GRASS, pos(0, 0, 0))
```
``||loops:repeat 10 times||``



## Fine del tutorial
### Introducion Step: Fine del tutorial  
Hai imparato la differenza tra eventi e comandi

### Finish: Fine tutorial
Complimenti! Hai terminato il tutorial!
