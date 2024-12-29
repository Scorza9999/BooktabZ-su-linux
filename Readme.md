# Guida su come effetturare il setup di BooktabZ su linux
BooktabZ, la piattaforma della Zanichelli per accedere ai propri libri offline è disponibile nativamente su distro derivate da Ubuntu.

Esistono più modi per installare questo software, anche se non si usa necessariamente Ubuntu o derivate. In ogni caso, è possibile che delle dipendenze siano assenti dal proprio sistema; nel caso installarle attraverso il proprio package manager

***

## Installazione su distro derivate da Arch Linux:
Ufficialmente non è supportato, tuttavia esiste una versione di BooktabZ presente nell' AUR al seguente link: 
https://aur.archlinux.org/packages/booktab

## Installazione su distro derivate da Ubuntu
BooktabZ è supportato nativamente. Per installare il software:
1. Si va al seguente link: https://booktab.it/download/
2. Si scarica la versione per linux
3. Si esegue il pacchetto .deb
#### Il metodo appena descritto potrebbe funzionare anche per Debian, tuttavia non ho testato

*** 

### Altri sistemi operativi/Installazioni precedenti non riuscite
Se la tua distro non è basata su Debian o Arch, come Fedora, oppure l'installazione con i metodi precedenti non ha funzionato, si dovrà installare la versione di Booktabz per Windows ed eseguirla attraverso Wine oppure Bottles. 

## Booktabz con Wine
1. Scaricare Wine (nel caso non fosse già installato) con:
  `sudo apt install wine`
  `sudo dnf install wine`
  `sudo pacman -S wine`
  a seconda della propria distribuzione (in ordine: Debian e derivati, Fedora, Arch Linux e derivati)
2. Scaricate dal seguente sito BooktabZ per Windows: https://booktab.it/download/
3. Aprite il terminale e eseguite con wine Booktabz per Windows con il seguente comando:
   `wine [percorso_booktabz_windows]`
   dove percorso_booktabz_windows è la posizione nel vostro filesystem in cui avete salvato il programma per Windows.
4. **Se non dovesse funzionare correttamente**, installa le dipendenze necessarie attraverso il proprio package manager.
