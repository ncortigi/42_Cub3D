🇮🇹✨  
> Realizzato insieme a [@minestrinad](https://github.com/minestrinad) 🚀

# Cub3D

🎮 **Cub3D** è un progetto della scuola 42 ispirato al leggendario Wolfenstein 3D, che mira a creare una rappresentazione grafica 3D di un labirinto in prima persona utilizzando i principi del Ray-Casting. Il progetto è scritto in C e utilizza la libreria miniLibX per la grafica.

## 🎯 Obiettivo

L'obiettivo principale di Cub3D è migliorare le competenze nella programmazione in C, negli algoritmi e nella progettazione grafica. Il progetto invita a esplorare concetti matematici per creare algoritmi eleganti ed efficienti.  
La parte obbligatoria prevede l'implementazione di un labirinto 3D base con texture sui muri, colori per pavimento e soffitto e controlli di movimento del giocatore.  
La parte bonus introduce funzionalità extra come collisioni con i muri, minimappa, porte, sprite animati e rotazione del punto di vista tramite mouse.

## 🚀 Come iniziare

È necessario creare una cartella "minilibx-linux" nella root della repository con all'interno scaricata la minilibx.

Per compilare il progetto, usa il Makefile con i seguenti comandi:

- `make all` — Compila il progetto
- `make clean` — Rimuove i file oggetto
- `make fclean` — Rimuove file oggetto ed eseguibile
- `make re` — Ricompila il progetto

Per eseguire il programma, fornisci un file di descrizione della scena in formato `.cub` come primo argomento:

```bash
./cub3D mappa.cub
```

## 🗺️ File di Descrizione della Scena

Il file `.cub` definisce il labirinto e le sue caratteristiche. Gli elementi principali sono:

- **Texture:**
  - Nord: `NO ./percorso_texture_nord`
  - Sud: `SO ./percorso_texture_sud`
  - Ovest: `WE ./percorso_texture_ovest`
  - Est: `EA ./percorso_texture_est`

- **Colori:**
  - Pavimento: `F R,G,B`
  - Soffitto: `C R,G,B`

- **Mappa:**
  - `0` = spazio vuoto, `1` = muro, `N`, `S`, `E`, `W` = posizione e orientamento iniziale del giocatore

Esempio:
```plaintext
NO ./percorso_texture_nord
SO ./percorso_texture_sud
WE ./percorso_texture_ovest
EA ./percorso_texture_est
F 220,100,0
C 225,30,0
        1111111111111111111111111
        1000000000110000000000001
        1011000001110000000000001
        1001000000000000000000001
111111111011000001110000000000001
100000000011000001110111111111111
11110111111111011100000010001
11110111111111011101010010001
11000000110101011100000010001
10000000000000001100000010001
10000000000000001101010010001
11000001110101011111011110N0111
11110111111101011111011101001
11111111111111111111111111111
```

## 🎮 Controlli

- W, A, S, D: Muovi il punto di vista
- Frecce (Dx e Sx): Ruota la visuale a sinistra/destra
- ESC: Chiudi la finestra ed esci
- Clic sulla X rossa della finestra: Chiudi la finestra ed esci

## ✨ Funzionalità Bonus

- Collisioni con i muri
- Minimappa
- Rotazione della visuale tramite mouse  

## 🏁 Conclusione

Cub3D è una sfida che unisce grafica, matematica e programmazione. Seguendo i principi del Ray-Casting, offre un'esperienza pratica nella creazione di un labirinto 3D. Esplora le possibilità, sii creativo con le texture e divertiti a costruire il tuo primo RayCaster con miniLibX! 🎉
