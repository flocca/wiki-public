# Laravel Valet

## Installazione (macOS Big Sur su M1)

Installare Homebrew (con Rosetta).

Avviare un terminale con Rosetta:

```
brew install php
brew install composer
```

Aggiungere ```~/.composer/vendor/bin``` al path:

```
# vim ~/.zshrc
export PATH=$HOME/bin:$HOME/.composer/vendor/bin:/usr/local/bin:$PATH
```

Installare Valet:

```
composer global require laravel/valet
```

Eseguire l'installazione di Valet:

```
valet install
```

Verificare che Valet sia installato pingando un indirizzzo ```*.test```:

```
ping prova.test
```

## Versione PHP

Per sapere quale versione di PHP stiamo utilizzando:

```
valet use
```

Per utilizzare (e installare) un'altra versione:

```
valet use php@7.4
```

Per tornare ad utilizzare l'ultima versione fornita tramite Homebrew:

```
valet use php
```

## Reset dell'installazione

```
composer global update
# valet uninstall --force
valet install
```

## Aggiornamento

```
composer global update
valet install
```
