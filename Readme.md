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

## BooktabZ attraverso Bottles
Prima di proseguire, esistono versioni di Bottles non distribuite attraverso flatpak (come sull'AUR, su Fedora...), tuttavia (quando ho scritto questa guida) gli sviluppatori di Bottles distribuiscono solo su flatpak. In questa guida, installerò attraverso flatpak

1. Installa flatpak
   `sudo apt install flatpak`
   `sudo dnf install flatpak`
   `sudo pacman -S install flatpak`
2. Installa Bottles con flatpak
   `flatpak install flathub bottles`
3. Apri Bottles nella GUI
4. Crea una nuova bottiglia con bottles
5. Assegna a questa bottiglia un nome e configura l'ambiente come applicazione
6. Una volta completata la creazione, clicca sulla bottiglia appena creata e aggiungi un programma (oppure avvia un eseguibile). Questo eseguibile è BooktabZ per Windows.
7. Avvia la bottiglia (se non fosse partita) e installa in questo modo BooktabZ.
8. Con Bottles (al momento di scrittura) non è necessaria l'installazione di ulteriori componenti, tuttavia se in futuro fosse necessario, si installano attraverso la GUI

***

# Se nessuno di questi metodi funzionasse, si dovrà installare una macchina virtuale con una distro supportata ufficialmente oppure Windows
Se questa fosse l'unica opzione, consiglio l'uso di KVM e QEMU (opzionalmente anche Virt-Manager per avere una GUI) in modo che le prestazioni siano migliori di VirtualBox
