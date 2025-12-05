# Package registry

I Nav publiserer vi pakker til Github npm registry, og ikke npm direkte i de fleste tilfeller.
[Docs](https://aksel.nav.no/god-praksis/artikler/github-npm-registry)

For å da installere pakker i `@navikt`-scope, trenger du en `.npmrc`-fil med registry og token lagt til.

> [!IMPORTANT]
> .npmrc-filer med token skal ikke sjekkes inn i git!

```.npmrc
; .npmrc
//npm.pkg.github.com/:_authToken=TOKEN
@navikt:registry=https://npm.pkg.github.com
```

## Token

For å hente pakker fra Github npm registry trenger man en token. Denne genererer du under ["developer settings" i Github](https://github.com/settings/tokens) med "read:packages". Etter token er generert må du også tillate den SSO for Navikt-organisasjonen. Se screenshot

![alt text](<Screenshot 2025-12-05 at 12.24.56.png>)

![alt text](<Screenshot 2025-12-05 at 12.25.50.png>)
