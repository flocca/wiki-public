# NativeScript

## Installazione degli strumenti

### macOS Catalina

Seguire le istruzioni avanzate qua:

https://docs.nativescript.org/angular/start/ns-setup-os-x

Quando richiesto, utilizzare pip3 al posto di pip:

```
pip3 install six
```

## Aggiornare gli strumenti

Aprire un terminale e accertarsi di avere l'ultima versione LTS di Node.js installata e selezionata.

```
nvm ls-remote --lts
nvm list
node --version
```

Eventualmente installarla e selezionarla:

```
nvm install lts/dubnium
nvm use lts/dubnium
```

Verificare l'installazione di NativeScript:
```
tns doctor
```

Eventualmente utilizzare la guida per l'installazione per correggere errori.

Eventualmente aggiornare gli strumenti di NativeScript:
```
npm install -g nativescript
```

## Aggiornare le applicazioni

```
cd HelloWorld/
tns update
```

## Eseguire l'applicazione utilizzando PREVIEW

```
cd HelloWorld/
tns preview
```

## Eseguire l'applicazione in un emulatore Android

```
cd HelloWorld/
tns run android
```

Per eseguirla in modalità debugging:

```
cd HelloWorld/
tns debug android
```

## Eseguire l'applicazione in un emulatore iOS

```
cd HelloWorld/
tns run ios
```

Per eseguirla in modalità debugging:

```
cd HelloWorld/
tns debug ios
```

## Creare una nuova app

Scaricare e installare NativeScript Sidekick se non è già stato fatto, da qua:

https://www.nativescript.org/nativescript-sidekick

Per eseguirlo con il giusto ambiende di Node, lanciarlo da linea di comando:

```
nvm use stable

/Applications/NativeScript\ Sidekick.app/Contents/MacOS/NativeScript\ Sidekick
```

# Android

## com.android.builder.dexing.DexArchiveMergerException

La prima compilazione per Android genererà questo errore:

```
D8: Cannot fit requested classes in a single dex file (# methods: 98777 > 65536)
com.android.builder.dexing.DexArchiveMergerException: Error while merging dex archives: 
The number of method references in a .dex file cannot exceed 64K.
```

Per risolvere, aggiungere l'opzione `multiDexEnabled true` al file `app/App_Resources/Android/app.gradle`:

```
android {
  defaultConfig {
    minSdkVersion 17
    multiDexEnabled true
    generatedDensities = []
  }
  aaptOptions {
    additionalParameters "--no-version-vectors"
  }
}
```

## Link utili in fase di sviluppo

- [RadListView for Vue](https://docs.nativescript.org/vuejs/ns-ui/ListView/overview)
- [NativeScript App Templates](https://github.com/NativeScript/nativescript-app-templates)
- [NativeScript-Vue Docs](https://nativescript-vue.org/en/docs/introduction/)
- [CSS Themes for NativeScript Apps (outdated)](https://docs.nativescript.org/ui/theme)
- [nativescript-plugin-firebase Docs](https://github.com/EddyVerbruggen/nativescript-plugin-firebase/tree/master/docs)
- [Firebase Functions Samples](https://github.com/firebase/functions-samples)
- https://docs.nativescript.org/api-reference/interfaces/_ui_frame_.navigationentry
- https://docs.nativescript.org/api-reference/interfaces/_ui_frame_.navigationtransition
- https://docs.nativescript.org/api-reference/modules/_ui_enums_.animationcurve

## Theme

- [NativeScript Theme: Core V2](https://github.com/NativeScript/theme)
- [CSS Themes for NativeScript Apps](https://docs.nativescript.org/ui/theme)

### Light/Dark mode

Per impostare il tema chiaro/scuro della app, inserire la class `.ns-dark` o `.ns-light` nell'elemento `<Frame>` in `app.js`:

```
new Vue({
  template: `
    <Frame class="ns-dark">
      <Home />
    </Frame>`,
```
