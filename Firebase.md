# Firebase

## Firebase Functions

Installare globalmente (o aggiornare) il pacchetto `firebase-tools`:

```
nvm use stable
npm install -g firebase-tools
```

```
firebase login

firebase init functions
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
