# Vuetify.js

## Installare Vue CLI versione 3

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

# Nuovo progetto utilizzando Vue UI

Avviare Vue UI:
```
vue ui
```

Dal **Gestore Progetti Vue**, scegliere **Crea**, spostarsi nella cartella **src** e premere **Crea un nuovo progetto qui**.

* Dettagli
  * Cartella del progetto: *nomeprogetto*
  * Gestore pacchetti: *yarn*
  * Git repository: *Inizializza il repository git (consigliato)*

* Presets
  * Seleziona un preset: *Modalità manuale*

* Funzionalità
  * Babel
  * Router
  * Vuex
  * CSS Pre-processors
  * Linter / Formatter

* Configurazione
  * Pick a CSS pre-processor: Sass/SCSS (with node-sass)
  * Pick a linter / formatter config: ESLint + Airbnb config
  * Lint on save

Premere **Crea Progetto** poi **Continua senza salvare**.

Dal menu **Plugin**, premere il pulsante **Aggiungi plugin** e inserire `vuetify` nel campo di ricerca.

Selezionare e installare il plugin ```vue-cli-plugin-vuetify```.

Verrà chiesto di selezionare un `preset`, scegliere `Configure (advanced)`.

Attivare tutte le opzioni eccetto `Use fonts as a dependency` e scegliere `Italy` come locale.

Premere **Completa l'installazione**. Completata l'installazione premere **Continua**.
