# Java V — Formulari i misionit sekret

## Çfarë mëson

Formularë semantikë, validim HTML dhe tabela të dhënash.

Referencë tematike: kap. 5 të librit.

## Skenari

Një klub organizon një mision në kampus dhe kërkon regjistrime të sakta, pa dërguar të dhëna reale.

## Shënime para kodimit (Analiza)

* **Hyrjet (Inputs):** Pseudonimi (3–20 karaktere), Email i sajuar, Persona (1–5), Kategoria (Art/Shkencë), Pranim i rregullave (Checkbox).
* **Daljet (Outputs):** Ridrejtimi te `pranuar.html` përmes metodës GET ku vlerat shfaqen te URL-ja.
* **Rast normal:** Pseudonimi `Arbër`, Email `student@example.org`, Persona `3`, Kategoria `Art`, Checkbox `I zgjedhur`. Formulari dërgohet me sukses.
* **Rast kufitar 1:** Numri i personave vendoset `1` ose `5` (pranohen), ndërsa me `0` apo `6` formulari bllokohet nga validimi HTML.
* **Rast kufitar 2:** Pseudonimi me `3` karaktere (pranohet) kundrejt `2` karaktereve (bllokohet nga `minlength`).

## Kërkesat për studentin

1. Ndërto formular me pseudonim 3–20 karaktere, email, grup 1–5 persona, kategori dhe pranim të rregullave.
2. Çdo kontroll ka label; radio-t kanë fieldset/legend. Përdor required, type, min/max dhe minlength/maxlength.
3. Krijo tabelë me tri orare; përdor caption, th dhe scope.
4. Butoni submit demonstron validimin vendas. Me të dhëna valide kalon te pranuar.html përmes GET; shpjego se kjo nuk ruan regjistrim në server.
5. Përdor vetëm të dhëna të sajuara; shëno se vlerat GET shfaqen në URL.

## Rastet e pranimit

- [x] Formulari bosh nuk kalon.
- [x] Email pa format email-i dhe grup 0 ose 6 nuk kalojnë.
- [x] Të dhënat valide çojnë te faqja e demonstrimit; tabela ka tituj kolonash.

## Dorëzimi dhe GitHub

Puno në JavaV/ të repository-t individual.

## Reflektim individual

Pse required në frontend nuk provon që të dhënat në një sistem real janë të sigurta?

**Përgjigje:**
Validimi me atributin `required` në front-end ekzekutohet vetëm brenda shfletuesit të përdoruesit. Kjo nuk garanton sigurinë e të dhënave sepse:
1. Përdoruesit ose sulmuesit mund ta fshijnë apo modifikojnë lehtësisht atributin `required` nga kodi HTML duke përdorur mjetet e zhvilluesit (Developer Tools) në shfletues.
2. Të dhënat mund të dërgohen te serveri direkt përmes kërkesave HTTP (si me cURL apo Postman) pa kaluar fare përmes formularit HTML.

Prandaj, në sisteme reale, siguria e të dhënave arrihet vetëm me validim dhe pastrim të rreptë (sanitization) në server (back-end).

