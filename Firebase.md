# Firebase

## Firebase Functions

* [Documentazione ufficiale](https://firebase.google.com/docs/functions)

### Aggiungere Firebase Functions a un progetto esistente

Installare globalmente (o aggiornare) il pacchetto `firebase-tools`:

```
nvm use stable

npm install -g firebase-tools
```

```
cd nomeprogetto

firebase login

firebase init functions
```

### Aggiunta dipendenze

```
cd functions
npm install moment
cd ..
```

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
