# Stylelint

Aksel har sin egen Stylelint-config som sikrer at man bruker riktige css-variabler og følger beste praksis når det kommer til bruk av Aksel sin CSS.

[Docs](https://aksel.nav.no/grunnleggende/kode/stylelint)

## Installere stylelint

```
npm install @navikt/aksel-stylelint stylelint
yarn add @navikt/aksel-stylelint stylelint
pnpm add @navikt/aksel-stylelint stylelint
```

For de som bruker `vscode`, kan stylelint-extension også anbefales.

## Sette opp linting

```diff
{
  "name": "demo",
  "private": true,
  "version": "0.0.0",
  "type": "module",
  "scripts": {
+   "lint": "stylelint '**/*.css'"
  },
+ "stylelint": {
+   "extends": [
+     "@navikt/aksel-stylelint/recommended"
+   ]
+ },
  "dependencies": {
    "@navikt/aksel-stylelint": "^7.35.1",
    "stylelint": "^16.26.1"
  }
}

```

## Teste linter

Vi har satt opp noen vanlige feil som vår stylelint-config vil advare/varsle om.

```
npm run lint
yarn lint
pnpm run lint
```

## [Neste steg ->](/6-Aksel-CLI/README.md)
