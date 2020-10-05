# Vue.js

## Installazione e aggiornamento

Installare globalmente Vue CLI versione 3 se non lo si è già fatto (è richiesto Node.js versione 8.11.0+):

```
nvm use stable

# Mostra la versione attualmente installata (globalmente)
npm list -g @vue/cli

# Aggiornare eventualmente la versione installata (globalmente)
npm update -g @vue/cli

# Nel caso non fosse già installato, installarlo:
npm install -g @vue/cli
```

Verificare eventualmente la versione di Vue CLI installata:

```
vue --version
```

Creare il progetto utilizzando la GUI:

```
vue ui
```

## Components (Componenti)

* [La guida ufficiale](https://vuejs.org/v2/guide/components.html)

### Suggerimenti

* Non modificare le proprietà direttamente nel componente. Le proprietà servono per comunicare (passare dati) al figlio. Usare invece gli eventi per comunicare dal componente figlio verso il padre.
  * [Vue Error: Avoid Mutating a Prop Directly](https://michaelnthiessen.com/avoid-mutating-prop-directly/)

## Vue + Firebase

### Vuex Easy Firestore
*"In just 4 lines of code, get your vuex module in complete 2-way sync with firestore"*.
* [GitHub](https://github.com/mesqueeb/vuex-easy-firestore)
* [Documentazione](https://mesqueeb.github.io/vuex-easy-firestore/)
