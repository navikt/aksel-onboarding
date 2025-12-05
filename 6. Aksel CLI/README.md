# CLI

Aksel har et eget CLI-verktøy som er utrolig nyttig for å migrere mellom versjoner. Når vi gjør større "breaking" endringer, lager vi som oftest "codemods" der det er mulig. Dette er scripts som automagiskt oppdaterer endringer i koden din mellom versjoner.

[Docs](https://aksel.nav.no/grunnleggende/kode/kommandolinje)

## Installere CLI

```
npm install -D @navikt/aksel
yarn add -D @navikt/aksel
pnpm add -D @navikt/aksel
```

## Kjøre migrering

Migreringen `v8-primitive-spacing` som vi tester her endrer alle "primitive"-komponentene våre sin "spacing"-attributt fra legacy: "4, 8, 12" etc til "space-16, space-32, space-48" etc

```diff
{
  "name": "demo",
  "private": true,
  "version": "0.0.0",
  "type": "module",
  "scripts": {
+   "migrate": "@navikt/aksel codemod v8-primitive-spacing --force"
  },
}
```
