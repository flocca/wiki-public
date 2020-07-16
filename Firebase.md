# Firebase

## Aggiungere Firebase a un progetto esistente

Installare globalmente (o aggiornare) il pacchetto `firebase-tools`:

```
nvm use stable

npm install -g firebase-tools
```

```
cd nomeprogetto

firebase login

firebase init
```

Selezionare quali funzionalità utilizzare (Firestore, Functions, Hosting, Storage, Emulators).

Scegliere **Use an existing project** e selezionare il progetto (selezionare la versione development se ci sono più ambienti).

Firestore Setup:

* Confermare l'utilizzo del file `firestore.rules` per le regole di Firestore.
* Confermare l'utilizzo del file `firestore.indexes.json` per gli indici di Firestore.

Functions Setup:

* Selezionare `Javascript` come linguaggio per Cloud Functions.
* Consentire l'utilizzo di ESLint premento `y`.
* Consentire l'installazione delle dipendenze premento `y`.

Hosting Setup:

* Utilizzare la directory `dist` al posto di `public` suggerita.
* Configurare come single app premendo `y`.

Storage Setup:

* Confermare l'utilizzo del file `storage.rules` per le regole di Storage.

Emulators Setup:

* Selezionare quali emulatori configurare : Functions, Firestore, Hosting.
* Confermare la porta `5001` per Functions.
* Correggere la porta in `8090` per Firestore.
* Confermare la porta `5000` per Hosting.
* Confermare l'abilitazione della Emulator UI.
* Conferma l'utilizzo di una porta casuale per l'Emulator UI.
* Conferma il download degli emulatori ora con `y`.


### Aggiunta dipendenze

```
cd functions
npm install moment
cd ..
```

## Firebase Hosting

## Firebase Functions

* [Documentazione ufficiale](https://firebase.google.com/docs/functions)

### Deploy

Versione di sviuluppo (development):

```
firebase use development
firebase deploy --only functions
```

Versione di produzione (production):

```
firebase use production
firebase deploy --only functions
```
