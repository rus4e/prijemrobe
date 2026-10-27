# Prijem Robe AI — Pilot za testiranje

Pilot aplikacija za probu u prijemu robe, napravljena za telefon i računar. Sadrži MINI tok za skeniranje i sastavljanje spiskova i PRO tok za kataloški prijem i poređenje sa otpremnicom.

## Početak

- Otvori `index.html` za početni ekran.
- **Novi prijem** vodi u MINI skener i ručni unos.
- **Arhiva** otvara lokalne i sačuvane spiskove.
- **Katalog** i **Kontrola otpremnice** vode u PRO.
- U PRO delu možeš da uvezeš objedinjeni MINI CSV, fotografišeš kutije za barkod i OCR količina, uneseš/učitaš otpremnicu i uporediš stavke.

## Važno za testiranje

- Aplikacija je bez prijave. Podaci ostaju u lokalnom pregledaču uređaja; nema naloga ni automatske sinhronizacije između telefona.
- Za prenos ili spajanje prijema koristi CSV izvoz/uvoz u MINI delu.
- Dozvola za kameru radi na HTTPS adresi. Ako je aplikacija postavljena na GitHub Pages, koristi dobijenu `https://` adresu, ne lokalni `file://` prikaz.
- Prvo učitavanje OCR i barkod biblioteka zahteva internet. OCR količine je pomoćna procena: proveri svaku prepoznatu količinu i ispravi je pre čuvanja ili poređenja.
- Pilot nema server zaštićen lozinkom. Za probu koristi testne podatke i nemoj unositi poverljive podatke radnje ili kupaca.
- Brisanje podataka pregledača može obrisati lokalne prijeme. Izvezi važne spiskove u CSV.

## Predlog kratke probe

1. Napravi novi prijem, skeniraj ili pronađi artikal i pokušaj da ga uneseš ponovo.
2. Pretraži spisak, promeni količinu, sačuvaj ga pod imenom i ponovo učitaj.
3. Izvezi CSV sa jednog uređaja, uvezi ga u MINI na drugom i proveri zbir.
4. U PRO delu probaj da pročitaš barkod i jasno odštampanu količinu sa kutije.
5. Unesi nekoliko stavki otpremnice i uporedi ih sa fizičkim prijemom.

Korisna povratna informacija sadrži model telefona/računara, pregledač, šta si uradio, šta se desilo i šta si očekivao. Ne šalji fotografije ili fajlove sa stvarnim podacima dobavljača bez prethodnog uklanjanja tih podataka.

## Postavljanje na GitHub Pages

Raspakuj sadržaj ovog foldera u koren ranije pripremljenog repozitorijuma, sa `index.html`, `mini.html`, `pro.html`, `manifest.webmanifest`, `sw.js`, `icons/` i `assets/` direktno u korenu. Sačuvaj/otpremi fajlove u granu `main`, a u podešavanjima GitHub Pages izaberi `main` i `/(root)`. Kada Pages završi objavu, otvori HTTPS adresu na telefonu i izaberi instalaciju/dodavanje na početni ekran.

## Sadržaj paketa

- `index.html` — početni ekran
- `mini.html` — mobilni prijem, duplikati, pretraga, zvučni signal, sačuvani spiskovi i CSV objedinjavanje
- `pro.html` — fizički prijem, OCR barkoda/količina, katalog i poređenje sa otpremnicom
- `assets/` — odobreni logo i fotografije pozadine
- `manifest.webmanifest`, `sw.js`, `icons/` — instalacija kao PWA i osnovno keširanje

Prijava i ekran zaključavanja nisu uključeni; logovanje je odloženo. Fix Price oznaka je uklonjena.
