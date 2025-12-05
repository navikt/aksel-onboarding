# Sette opp et nytt prosjekt med Aksel

Her er det satt opp boilerplate for en enkel [Vite-app](https://vite.dev/). Målet her er å installere Aksel-pakker, og bruke de i appen.

## Steg 1

Installer pakkene med din "package manager"

```
npm install
yarn install
pnpm i
```

## Steg 2

Start og verifiser at appen kjører riktig

```
npm run dev
yarn dev
pnpm run dev
```

## Steg 3

Stopp appen, og installer Aksel-pakker

```
npm install @navikt/ds-react @navikt/ds-css @navikt/aksel-icons
yarn add @navikt/ds-react @navikt/ds-css @navikt/aksel-icons
pnpm add @navikt/ds-react @navikt/ds-css @navikt/aksel-icons
```

## Steg 4: CSS

Legg til all designsystem-styling. Dette kan endte gjøes med `@import` i root-css, eller direkte `import` i `main.tsx`

```
// index.css
@import "@navikt/ds-css";

// eller

// main.tsx
import "@navikt/ds-css";
```

## Steg 5: Komponenter

Alt er da klart for å bruke komponentene fra Aksel 🎉

Test å importere + rendre en komponent fra Aksel. Du finner alle komponentene til Aksel under [denne oversikten](https://aksel.nav.no/komponenter/core).

```tsx
import { LocalAlert } from "@navikt/ds-react";

const Example = () => {
  return (
    <LocalAlert status="announcement">
      <LocalAlert.Header>
        <LocalAlert.Title>
          Nyhet! Nå kan du ettersende vedlegg digitalt
        </LocalAlert.Title>
      </LocalAlert.Header>
      <LocalAlert.Content>
        Kunngjøringer brukes for å formidle noe om appen eller systemet, eller
        endringer som påvirker brukerne. Eksempelvis planlagt vedlikehold eller
        driftsmeldinger.
      </LocalAlert.Content>
    </LocalAlert>
  );
};
```

### Steg 6: Ikoner

[Aksel har også en egen ikonpakke med over 900 ikoner tilgjengelig](https://aksel.nav.no/komponenter/ikoner).

```tsx
import { PencilIcon } from "@navikt/aksel-icons";

const ExampleWithIcon = () => {
  return (
    <Button icon={<PencilIcon title="a11y-title" />}>Rediger søknad</Button>
  );
};
```
