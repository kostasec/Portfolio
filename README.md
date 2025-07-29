# Projekat: Atlantis Logistic – Baza podataka i dokumentacija

## Sadržaj
- [Struktura fajlova projekta](#struktura-fajlova-projekta)
  - [1. ddl.sql](#1-ddlsql)
  - [2. indexes.sql](#2-indexessql)
  - [3. initialData.sql](#3-initialdatasql)
  - [4. storedProcedures.sql](#4-storedproceduressql)
  - [5. ER-Model.jpg](#5-er-modeljpg)
  - [6. ProjectDocumentation-AtlantisLogistic.pdf](#6-projectdocumentation-atlantislogisticpdf)

---

## Struktura fajlova projekta

### 1. `ddl.sql`
Sadrži kompletan DDL skript, koji obuhvata:
- Kreiranje svih tabela sistema (npr. `Client`, `Employee`, `Vehicle`, `Service`, itd.)
- Definisanje primarnih i stranih ključeva
- Postavljanje ograničenja i drugih pravila integriteta
- Redosledno brisanje i kreiranje objekata kako bi skripta mogla da se izvrši u celini

### 2. `indexes.sql`
Fajl sadrži SQL naredbe za kreiranje **indeksa** nad kolonama koje se često koriste u `JOIN`, `WHERE` ili `ORDER BY` uslovima.
Cilj je da se ubrza pretraga i optimizuje performansa baze, posebno za tabele sa velikim brojem redova.

### 3. `initialData.sql`
Ovaj fajl se koristi za inicijalno punjenje baze, uključuje:
- Vrednosti za šifarnike (`VATCodeList`, `VATExemptionReason`)
- Početne vrednosti kao što su test klijenti, zaposleni i usluge
- Osnovne zavisnosti potrebne za validaciju unosa i pravilno funkcionisanje aplikacije

### 4. `storedProcedures.sql`
Ovaj fajl sadrži definicije svih **procedura** koje automatizuju deo logike sistema koja je potrebna kako bi se određene funkcije izvršavale na aplikativnom sloju:
- Umetanje kompleksnih entiteta (npr. faktura sa više stavki)
- Validacija podataka pre unosa
- Logika poslovnih pravila
- Proceduralno rukovanje transakcijama i referencijalnim vezama

### 5. `ER-Model.jpg`
Grafički prikaz **ER dijagrama** baze podataka:
- Prikazuje entitete, njihove atribute i veze među njima
- Koristi se kao vizuelna pomoć u razumevanju strukture baze

### 6. `ProjectDocumentation-AtlantisLogistic.pdf`
Zvanična projektna dokumentacija u PDF formatu, koja sadrži:
- Opis poslovnog sistema i potreba firme
- Objašnjenje strukture baze i dizajn u skladu sa normalnim formama (do BCNF)
- ER dijagram i relacioni model

---

> Ovi fajlovi zajedno predstavljaju potpunu implementaciju baze podataka i dokumentaciju poslovnog sistema **Atlantis Logistic**, spremnu za integraciju sa aplikacionim slojem.
