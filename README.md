# Java III — Klinika e CSS: shpëto afishen

## Diagnostikimi i `gabime.css`
1. **Konflikti i specifikitetit:** Selektoi `#poster` kishte specifikitet më të lartë se `.poster`, duke mbajtur ngjyrën e tekstit të bardhë mbi sfond të bardhë.
2. **Overflow (Tejkalimi):** Përdorimi i `width: 700px;` fiks dhe `padding: 80px;` e bënte gjerësinë $860\text{px}$, duke e shkatërruar pamjen në ekrane më të vogla se 360px.
3. **Zgjidhja:** Është përdorur `max-width: 100%`, `box-sizing: border-box;` dhe janë hequr gjerësitë fikse pa përdorur `!important`.

## Shpjegimi i Box Model
Në CSS standard, gjerësia totale llogaritet:
$$\text{Gjerësia Totale} = \text{width} + \text{padding-left} + \text{padding-right} + \text{border-left} + \text{border-right}$$

Përdorimi i `box-sizing: border-box;` e ndryshon këtë sjellje, duke përfshirë `padding` dhe `border` brenda gjerësisë së caktuar (`width`), duke parandaluar kështu deljen e elementit nga ekrani.