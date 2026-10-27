# Prijem Robe AI — pilot V2

Testna PWA verzija za mobilni prijem i PRO kontrolu otpremnice.

## MINI tok prijema

1. Sa početne strane izaberi **Novi prijem**.
2. Na prvoj strani proveri generisani broj prijema, izaberi datum i pritisni **Počni prijem**.
3. Na stranici skenera pokreni kameru. Kada se očita barkod, zvučni signal potvrđuje očitavanje.
4. Otvara se kartica artikla sa LK/šifrom, barkodom, nazivom i količinom. Unesi količinu i pritisni **Dodaj u prijem**.
5. Aplikacija se vraća na skener; dodati artikal se nalazi u spisku ispod skenera. Ponovljeni artikal daje upozorenje i količina se sabira.
6. Ručni unos otvara istu karticu artikla. U **Arhivi** možeš da imenuješ i sačuvaš spisak, pretražuješ ga i izvoziš/objedinjuješ CSV fajlove.

## PRO

PRO ima katalog, uvoz objedinjenog prijema iz MINI CSV-a, skeniranje barkodova i OCR prepoznavanje jasno označene količine sa kutije. Otpremnicu možeš fotografisati/učitati i uporediti sa fizičkim prijemom. OCR je pomoćna procena: proveri i ispravi količine i stavke pre poređenja.

## Testiranje i objava

- Aplikacija je bez prijave i bez sinhronizacije uživo. Prijemi se čuvaju lokalno u pregledaču uređaja; CSV služi za prenos i objedinjavanje između uređaja.
- Za kameru i instalaciju PWA koristi HTTPS GitHub Pages adresu, ne lokalni `file://` fajl.
- Prvo učitavanje barkod/OCR biblioteka zahteva internet.
- Koristi testne podatke. Ova probna verzija nema server ni korisničke naloge; brisanje podataka pregledača može ukloniti lokalne prijeme.
- Za GitHub Pages otpremi sadržaj ovog foldera u koren repozitorijuma, sa `index.html`, `mini.html`, `pro.html`, `manifest.webmanifest`, `sw.js`, `assets/` i `icons/` direktno u root-u. Izaberi granu `main` i `/ (root)` kao Pages izvor.

Za prijavu problema zapiši model uređaja, pregledač, korake i šta si očekivao da se dogodi. Ukloni podatke dobavljača sa snimaka/fajlova pre slanja.
