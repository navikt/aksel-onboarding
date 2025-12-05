# Package manager

I Nav er det en god miks av npm, yarn, pnpm + flere mer nisje package-managers brukt.

Historiskt sett er det litt flere som bruker yarn da node-modules installering vare en del raskere før og yarn støttet "workspaces" før npm. Men i 2025 er dette mer preferanse enn noe annet.

Etter du har installert Nodejs, skal "npm" være med på kjøpet. For å bruker `yarn` eller `pnpm` må du manuelt slå disse på.

```
// Enable yarn
corepack enable yarn

// Enable pnpm
corepack enable pnpm
```

## Lock-filer

Vi anbefaler å alltid sjekke inn "lock"-filer i prosjekter:
`yarn.lock`, `package-lock.json`, `pnpm-lock.yaml` etc

Dette lar deg kjøre `install` scripts i "CI"-modus, f.eks `pnpm install --frozen-lockfile`, samt gjøre sikkerhetssjekker på koden.

## [Neste steg ->](/3-Package-registry/README.md)
