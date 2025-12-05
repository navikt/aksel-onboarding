# Sette opp et nytt prosjekt med Aksel

Her er det satt opp boilerplate for en enkel [Vite-app](https://vite.dev/). Målet her er å installere Aksel-pakker, og bruke de i appen.

> [!NOTE]
> Alle pakker fra Aksel følger samme versjon. Det betyr at hvis man er på versjon 7.32.0 av @navikt/ds-react, må @navikt/ds-css også være på samme versjon.

## Steg 1: Installer avhengigheter

Installer pakkene med din "package manager"

```bash
npm install
yarn install
pnpm i
```

## Steg 2: Start appen

Start og verifiser at appen kjører riktig

```bash
npm run dev
yarn dev
pnpm run dev
```

## Steg 3: Installer Aksel-pakker

Stopp appen, og installer Aksel-pakker

```bash
npm install @navikt/ds-react @navikt/ds-css @navikt/aksel-icons
yarn add @navikt/ds-react @navikt/ds-css @navikt/aksel-icons
pnpm add @navikt/ds-react @navikt/ds-css @navikt/aksel-icons
```

## Steg 4: Legg til CSS

Legg til all designsystem-styling. Dette kan enten gjøres med `@import` i root-css, eller direkte `import` i `main.tsx`

```css
// index.css
@import "@navikt/ds-css";
```

eller

```tsx
// main.tsx
import "@navikt/ds-css";
```

## Steg 5: Bruk komponenter

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

## Steg 6: Bruk ikoner

[Aksel har også en egen ikonpakke med over 900 ikoner tilgjengelig](https://aksel.nav.no/komponenter/ikoner).

> [!TIP]
> Bruk [ikonsøket på aksel.nav.no](https://aksel.nav.no/ikoner) for å finne riktig ikon. Der kan du enkelt kopiere import-navnet (f.eks. `PencilIcon`).

```tsx
import { PencilIcon } from "@navikt/aksel-icons";

const ExampleWithIcon = () => {
  return (
    <Button icon={<PencilIcon title="a11y-title" />}>Rediger søknad</Button>
  );
};
```

## Steg 7: Design Tokens

Vi bruker Design Tokens (CSS-variabler) for å sikre konsistent bruk av farger, avstander, skygger og typografi. Unngå hardkodede hex-koder eller pixel-verdier der det er mulig.

[Se oversikt over alle tokens her](https://aksel.nav.no/grunnleggende/styling/design-tokens).

Eksempel:

```css
.my-component {
  background-color: var(--a-surface-subtle);
  padding: var(--a-spacing-4);
  border-radius: var(--a-border-radius-medium);
  color: var(--a-text-default);
}
```

## [Neste steg ->](/5-Stylelint/README.md)
