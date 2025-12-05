# CLI

Aksel har et eget CLI-verktøy som er utrolig nyttig for å migrere mellom versjoner. Når vi gjør større "breaking" endringer, lager vi som oftest "codemods" der det er mulig. Dette er scripts som automagiskt oppdaterer endringer i koden din mellom versjoner.

[Docs](https://aksel.nav.no/grunnleggende/kode/kommandolinje)

## Steg 1: Installer avhengigheter

Før du kjører migreringen, installer avhengighetene:

```bash
npm install
yarn install
pnpm install
```

## Steg 2: Kjør migrering

Migreringen `v8-primitive-spacing` som vi tester her endrer alle "primitive"-komponentene våre sin "spacing"-attributt fra legacy: "4, 8, 12" etc til "space-16, space-32, space-48" etc

(`--force` skipper bare git-sjekk her)

```
npx @navikt/aksel@latest codemod v8-primitive-spacing --force
yarn dlx @navikt/aksel@latest codemod v8-primitive-spacing --force
pnpm dlx @navikt/aksel@latest codemod v8-primitive-spacing --force
```

### Du finner alle migreringene tilgjengelig med:

```
npx @navikt/aksel@latest codemod help
yarn dlx @navikt/aksel@latest codemod help
pnpm dlx @navikt/aksel@latest codemod help
```

## [Neste steg ->](/7-RSC/README.md)
