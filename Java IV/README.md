# Java IV — Festivali që përshtatet në çdo ekran

## Çfarë mëson
Flexbox, Grid, media queries dhe pamje responsive.

Referencë tematike: kap. 6–7 të librit.

## Çfarë realizova
- Ndërtova 6 karta aktivitetesh shkencore me strukturë semantic HTML.
- Krijova një menu lundrimi fleksibile duke përdorur **Flexbox**.
- Përdora **CSS Grid** dhe Media Queries për të siguruar layout responsive sipas rezolucionit të ekranit.
- Trajtova imazhet në mënyrë fleksibile (`width: 100%`, `height: auto`) dhe shmanga lartësitë fikse në tekst.
- Zgjodha sfidën e titullit të gjatë duke përdorur rregullat CSS `overflow-wrap: break-word;` dhe `word-break: break-word;`.

## Hapat e hapjes
1. Klono ose shkarko projektin në kompjuterin tënd.
2. Hap skedarin `index.html` direkt në çfarëdo shfletuesi (Chrome, Firefox, Edge).
3. Për të testuar rezolucionet responsive, hap *Developer Tools* në shfletues (shtyp `F12` ose `Ctrl+Shift+I` / `Cmd+Option+I`) dhe aktivizo *Toggle Device Toolbar*.

## Rezultatet e Testimit

| Hyrje (Ekrani) | Rezultati i Pritur | Rezultati i Marrë | Statusi |
| :--- | :--- | :--- | :--- |
| **360 px** | Shfaqet saktësisht **1 kolonë** | Shfaqet 1 kolonë me renditje vertikale pa scroll horizontal | ✅ Sukses |
| **768 px** | Shfaqen saktësisht **2 kolona** | Shfaqen 2 kolona me hapësirë te barabartë gapa | ✅ Sukses |
| **1280 px** | Shfaqen saktësisht **3 kolona** | Shfaqen 3 kolona në rrjetë uniforme | ✅ Sukses |
| **Tastiera (Tab)** | Lundrim i përdorshëm në menu dhe te lidhjet | Fokus visual i qartë te skeda aktive dhe tek butoni `skip` | ✅ Sukses |

## Reflektim individual

### Kur do të zgjidhje Flexbox dhe kur Grid?
- **Flexbox** është zgjidhja më e mirë për mezuara **një-dimensionale** (ose me një rresht ose me një kolonë). Është ideal për elemente të tilla si meny lundrimi, shiritë mjetesh (toolbars), apo shtrirje vertikale brenda vetë përmbajtjes së një karte sepse lejon fleksibilitet të lartë në rregullimin e hapësirave.
- **CSS Grid** është ideal për strukturime **dydimensionale** (rreshta dhe kolona njëkohësisht). Është zgjidhja e duhur për të kontrolluar pamjen e përgjithshme të faqes, si p.sh. rrjeta e kartave të aktiviteteve (grid layout), ku na duhet të specifikojmë numrin e kolonave në varësi të gjerësisë së ekranit.

## Deklarimi i AI / Burimeve
- Ky projekt u zhvillua me ndihmën e asistentit AI për strukturimin e kodit HTML/CSS dhe dokumentimin e procesit të testimit në README.md.
