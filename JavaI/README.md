# Java I — Pasaporta Digjitale

## Çfarë realizova

Krijova një pasaportë digjitale për personazhin e sajuar **Arta Orbitë**,
e cila kandidon si udhërrëfyese e një kampusi imagjinar.

Projekti përmban:
- `index.html` — faqja kryesore me prezantimin dhe 3 aftësi.
- `rreth.html` — histori e shkurtër për personazhin.
- `kontakt.html` — faqe shtesë e sfidës së transferimit.

Të gjitha të dhënat për personazhin janë të sajuara.

## Si hapet projekti

Hap folderin `JavaI` përmes një serveri lokal dhe hap `index.html`.

## Testet

### Testi 1 — Hapja e faqes kryesore
**Hyrje:** Hapet `index.html` përmes serverit lokal.

**Rezultat i pritur:** Shfaqet pasaporta e Arta Orbitës me prezantimin dhe 3 aftësitë.

**Rezultat i marrë:** Faqja u hap me sukses.

### Testi 2 — index.html → rreth.html
**Hyrje:** Klikohet "Rreth Artës".

**Rezultat i pritur:** Hapet `rreth.html` pa 404.

**Rezultat i marrë:** `rreth.html` u hap me sukses.

### Testi 3 — rreth.html → index.html
**Hyrje:** Klikohet "Kthehu në faqen kryesore".

**Rezultat i pritur:** Kthehet te `index.html` pa 404.

**Rezultat i marrë:** Kthimi funksionoi.

### Testi 4 — Network
Në DevTools → Network kontrollohet dokumenti i hapur përmes serverit lokal.

- URL: adresa lokale e `index.html`
- Method: `GET`
- Status: `200 OK`

URL-ja varet nga serveri lokal që përdoret.

## Reflektim individual

**Cili ndryshim është ruajtur lokalisht por ende nuk shihet në GitHub?**

Një ndryshim i ruajtur në skedarin lokal, por pa `commit` dhe `push`,
mbetet vetëm në kompjuter dhe nuk shihet ende në GitHub.

## Dallimi mes skedarit lokal, commit-it dhe push-it

- **Skedari lokal:** versioni i projektit në kompjuter.
- **Commit:** regjistron ndryshimet në historinë lokale të Git-it.
- **Push:** dërgon commit-et lokale në GitHub.

## AI / Burimet

AI u përdor për ndihmë në strukturimin dhe kontrollimin e shembullit
HTML dhe README-së.

Burim tematik: udhëzuesi i lëndës dhe kapitujt 1–3 të referencës së kursit.
