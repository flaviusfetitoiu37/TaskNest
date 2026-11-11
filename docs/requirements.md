# Cerinte

Prioritati: P1 = obligatoriu, P2 = important, P3 = optional.

## Cerinte functionale

| ID | Cerinta | Prioritate |
|----|---------|------------|
| RF-01 | Utilizatorul isi poate face cont cu e-mail si parola | P1 |
| RF-02 | Utilizatorul se poate autentifica si deconecta | P1 |
| RF-03 | Utilizatorul poate adauga, edita, bifa si sterge o sarcina | P1 |
| RF-04 | O sarcina are titlu, descriere, termen si stare (facuta sau nu) | P1 |
| RF-05 | Utilizatorul poate crea, redenumi si sterge liste | P1 |
| RF-06 | Proprietarul unei liste poate invita alti utilizatori dupa e-mail | P1 |
| RF-07 | Membrii unei liste vad si modifica aceleasi sarcini | P1 |
| RF-08 | Proprietarul poate scoate un membru din lista | P2 |
| RF-09 | Utilizatorul poate adauga venituri si cheltuieli cu suma, data si categorie | P1 |
| RF-10 | Aplicatia arata totalul lunii si cat a ramas disponibil | P1 |
| RF-11 | Utilizatorul poate seta o limita lunara pe categorie | P2 |
| RF-12 | Sarcinile pot fi filtrate dupa stare si termen | P2 |
| RF-13 | Utilizatorul poate rezerva o resursa pe un interval orar | P3 |
| RF-14 | Rezervarile care se suprapun sunt respinse | P3 |
| RF-15 | Administratorul poate adauga si dezactiva resurse | P3 |
| RF-16 | Aplicatia afiseaza statistici despre sarcini si cheltuieli | P3 |

## Cerinte nefunctionale

| ID | Cerinta | Prioritate |
|----|---------|------------|
| RN-01 | Parolele se salveaza ca hash, nu in clar | P1 |
| RN-02 | Frontend-ul comunica cu serverul prin HTTPS si API REST | P1 |
| RN-03 | Un utilizator poate accesa doar listele si datele proprii sau partajate cu el | P1 |
| RN-04 | Interfata este responsive, de la 360 px latime | P1 |
| RN-05 | HTML semantic, etichete la formulare, navigare cu tastatura, contrast bun | P1 |
| RN-06 | Mesajele de eroare sunt clare | P1 |
| RN-07 | Datele se valideaza si in frontend, si in backend | P2 |
| RN-08 | Operatiile obisnuite raspund in sub o secunda | P2 |
| RN-09 | Codul e pe GitHub, cu commit-uri de la toti membrii | P1 |
| RN-10 | Aplicatia se poate porni local dupa instructiunile din README | P2 |

## Ce intra si ce nu intra in proiect

Intra: conturi de utilizator, sarcini, liste partajate, buget personal cu categorii, rezervari simple, statistici de baza.

Nu intra: plati online, aplicatie mobila nativa, integrari cu servicii externe, notificari push.
