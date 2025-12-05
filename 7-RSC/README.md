# React Server Components

Aksels komponenter kan brukes i RSC uten noe ekstra oppsett, da mest relevant for Next app-dir prosjekter. Men en typisk "gotcha" er bruk av "dot"-notasjon for komponenter. Disse er ikke støttet med RSC, men vi tilbyr direkte import av komponenter som løser dette.

```diff
-import { LocalAlert } from "@navikt/ds-react";
+import { LocalAlert, LocalAlertHeader } from "@navikt/ds-react/LocalAlert";

export const Demo = () => {
  return (
    <LocalAlert>
-     <LocalAlert.Header>...</LocalAlert.Header>
+     <LocalAlertHeader>...</LocalAlertHeader>
    </LocalAlert>
  );
};
```
