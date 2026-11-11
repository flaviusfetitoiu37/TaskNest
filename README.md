# TaskNest

Aplicatie web pentru organizarea activitatilor de zi cu zi: sarcini, liste partajate, buget personal si rezervari simple de resurse.

Proiect la Tehnologii Web, anul universitar 2026-2027. Tema aleasa: P4, Organizarea activitatilor cotidiene.

## Problema

Cine isi organizeaza viata in familie sau cu colegii de apartament ajunge sa foloseasca mai multe lucruri deodata: o aplicatie de notite pentru sarcini, un grup de chat pentru lista de cumparaturi si un tabel pentru cheltuieli. Informatiile se pierd, nu sunt la zi si nu se stie cine a facut ce. TaskNest le aduna intr-un singur loc.

## Obiective

- Un utilizator nou isi poate face cont si prima lista in mai putin de un minut.
- O lista poate fi partajata cu alt utilizator, iar amandoi vad aceleasi modificari.
- Bugetul lunar se actualizeaza automat cand adaugi o cheltuiala.
- Doua rezervari pentru aceeasi resursa nu se pot suprapune.
- Interfata se foloseste bine si pe telefon, si pe calculator (verificata la 360 px si la 1280 px latime).

Fiecare obiectiv are un scenariu de test in [use-cases.md](docs/use-cases.md).

## Utilizatori vizati

- **Utilizator inregistrat**: isi gestioneaza sarcinile, bugetul si rezervarile.
- **Proprietar de lista**: cel care a creat lista, poate invita sau scoate membri.
- **Membru al unei liste**: poate vedea si modifica sarcinile din lista in care a fost invitat.
- **Administrator**: gestioneaza utilizatorii si resursele care se pot rezerva.

## Echipa si responsabilitati

| Membru | Responsabilitati |
|--------|------------------|
| Flavius Fetitoiu | Frontend in React, wireframe-uri, interfata responsive, accesibilitate |
| Victor Florea | Backend in .NET, baza de date PostgreSQL, autentificare |

## Functionalitati

Obligatorii:
1. Inregistrare, autentificare si cont de utilizator
2. Sarcini: adaugare, editare, bifare, stergere
3. Liste partajate, cu invitarea altor utilizatori
4. Buget personal: venituri, cheltuieli, categorii, total lunar

Optionale:
5. Rezervari de resurse, fara suprapuneri
6. Statistici simple despre sarcini si cheltuieli

## Tehnologii

- Frontend: React
- Backend: ASP.NET Core (.NET), API REST
- Baza de date: PostgreSQL
- Autentificare: JWT
- Versionare: Git si GitHub

Motivele alegerii sunt in [implementation-plan.md](docs/implementation-plan.md).

## Documentatie

- [Cerinte functionale si nefunctionale](docs/requirements.md)
- [Scenarii de utilizare](docs/use-cases.md)
- [Wireframe-uri](docs/wireframes/README.md)
- [Arhitectura aplicatiei](docs/architecture.md)
- [Modelul de date si endpoint-uri](docs/data-model.md)
- [Plan de implementare](docs/implementation-plan.md)
