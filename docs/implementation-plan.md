# Plan de implementare

## De ce aceste tehnologii

- **React** pentru frontend: interfata se imparte in componente reutilizabile (liste, sarcini, formulare) si se face usor responsive.
- **ASP.NET Core** pentru backend: structura clara pe controllere si servicii, iar autentificarea cu JWT si validarea sunt deja bine sustinute.
- **Entity Framework Core**: migrari pentru schema bazei de date si interogari scrise direct in C#.
- **PostgreSQL**: baza relationala, potrivita pentru datele noastre, care au multe legaturi (utilizatori, liste, sarcini, tranzactii).
- **JWT**: nu avem nevoie de sesiuni pe server, ceea ce merge bine cu un frontend si un backend separate.
- **Git si GitHub**: istoricul arata contributia fiecaruia.

## Versionare

- `main` contine doar cod stabil.
- `develop` este ramura in care adunam functionalitatile.
- Fiecare functionalitate se face pe o ramura `feature/<nume>`, de exemplu `feature/auth` sau `feature/budget`.
- Modificarile ajung in `develop` prin Pull Request, verificat de cel putin un alt membru.
- Mesajele de commit sunt scurte si au prefix: `feat:`, `fix:` sau `docs:`.
- Fiecare face commit-uri din contul lui.

## Etape

| Etapa | Termen | Ce facem |
|-------|--------|----------|
| 1 | Saptamana 4 | Alegerea si definirea proiectului |
| 2 | Saptamana 7 | Conceptul, documentatia, wireframe-urile, arhitectura si modelul de date |
| 3 | Saptamana 10 | Prototip functional: autentificare, sarcini, liste partajate, buget de baza |
| 4 | Saptamana 14 | Rezervari, statistici, testare, corecturi si prezentarea finala |

## Ordinea lucrului

1. Configurarea proiectelor (React, ASP.NET Core, PostgreSQL), migrarile si autentificarea
2. Sarcinile si listele, apoi partajarea listelor
3. Bugetul: tranzactii, categorii, totaluri
4. Rezervarile, cu verificarea suprapunerilor
5. Statisticile, finisarea interfetei si accesibilitatea

Functionalitatile obligatorii se termina inaintea celor optionale.

## Cine ce face

| Membru | Responsabilitati |
|--------|------------------|
| Flavius Fetitoiu | Frontend React, interfata responsive, accesibilitate, legarea de API |
| Victor Florea | Backend ASP.NET Core, model de date, migrari PostgreSQL, JWT |

## Riscuri

- **Timpul limitat.** Facem intai functionalitatile obligatorii si trecem la cele optionale doar daca ramane timp.
- **Legatura dintre React si .NET** (CORS, JWT, formatul datelor). Definim endpoint-urile din timp, in `data-model.md`, si le testam cu Swagger.
- **Doi utilizatori care modifica aceeasi lista in acelasi timp.** Reincarcam datele dupa fiecare operatie si, daca e nevoie, adaugam un camp de versiune ca sa detectam conflictele.
- **Medii de lucru diferite.** Punem in README pasii de pornire si rulam PostgreSQL local sau in Docker.
