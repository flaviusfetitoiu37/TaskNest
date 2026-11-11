# Scenarii de utilizare

## UC-01: Cont nou si prima lista

Actor: utilizator nou. Conditie de start: nu are cont.

1. Deschide pagina de inregistrare.
2. Completeaza numele, e-mailul si parola, apoi apasa "Creeaza cont".
3. Sistemul valideaza datele si creeaza contul.
4. Utilizatorul intra direct in aplicatie, pe pagina principala.
5. Apasa "Lista noua", scrie "Cumparaturi" si confirma.
6. Lista apare pe pagina.

Daca e-mailul exista deja sau parola e prea scurta, apare un mesaj de eroare, iar datele completate ramin in formular.

Cum verificam: in baza de date exista utilizatorul si lista lui, iar lista se vede si dupa reincarcarea paginii.

## UC-02: Lista partajata

Actori: proprietarul listei si un coleg invitat. Conditie de start: amandoi au cont, iar proprietarul are o lista.

1. Proprietarul deschide lista si apasa "Invita".
2. Scrie e-mailul colegului si confirma.
3. Colegul se autentifica si vede lista la el pe pagina principala.
4. Colegul adauga sarcina "Cumpara lapte".
5. Proprietarul reincarca lista si vede sarcina noua, cu numele celui care a adaugat-o.

Daca e-mailul nu apartine niciunui cont, apare mesajul "Utilizator inexistent".

Cum verificam: ambii vad aceleasi sarcini, iar un utilizator care nu a fost invitat primeste eroare 403 cand incearca sa deschida lista.

## UC-03: Bugetul lunii

Actor: utilizator autentificat.

1. Deschide pagina "Buget".
2. Adauga un venit de 2000 RON, categoria "Salariu".
3. Adauga o cheltuiala de 150 RON, categoria "Mancare".
4. Pagina arata venituri 2000, cheltuieli 150, disponibil 1850 si cheltuielile pe categorii.

Daca suma e negativa sau lipseste categoria, tranzactia e respinsa cu un mesaj clar.

Cum verificam: disponibilul este egal cu veniturile minus cheltuielile pentru luna aleasa.

## UC-04: Rezervarea unei resurse

Actor: utilizator autentificat. Conditie de start: administratorul a adaugat resursa "Masina de spalat".

1. Utilizatorul deschide "Rezervari" si alege resursa.
2. Alege data si intervalul 18:00 - 19:00.
3. Sistemul verifica daca intervalul e liber si salveaza rezervarea.
4. Rezervarea apare in orarul resursei.

Daca intervalul se suprapune cu o alta rezervare, cererea e respinsa si se afiseaza intervalele libere.

Cum verificam: nu pot exista doua rezervari suprapuse pentru aceeasi resursa.
