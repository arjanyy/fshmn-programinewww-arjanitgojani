# Java III · Klinika e CSS: shpëto afishen

Afishe për klubin e debatit: titull, datë, vend, përshkrim dhe lidhje regjistrimi. Vetëm HTML + CSS, pa varësi të jashtme dhe pa asete.

## Skedarët

- `index.html`: afishja (HTML semantik: `header`, `main`, `article`, `footer`, `time`, listë etiketash).
- `style.css`: CSS i jashtëm me variabla (`--brand`, `--space-m`, …) dhe klasa të ripërdorshme (`.tag`, `.btn`, `.afisha`).
- `Fillimi/gabime.css`: versioni i riparuar; `Fillimi/gabime-demo.html` e provon.

## Etiketat

Tri etiketa: **Falas**, **Vende të kufizuara: 20** (kornizë me pika) dhe **Edhe online**. Dallohen me tekst dhe me stilin e kornizës, jo vetëm me ngjyrë.

## Diagnoza e gabime.css

1. **Dy rregulla konfliktuale:** `#poster { color: white }` dhe `.poster { color: #17263c }`. Fiton `#poster`, sepse specificiteti i ID-së (1,0,0) është më i lartë se i klasës (0,1,0). Teksti dilte i bardhë mbi sfond të bardhë. Rregulluar duke lënë një rregull të vetëm me klasë.
2. **Tejkalimi i gjerësisë:** me `content-box`, `700px + 80px + 80px = 860px`. Rregulluar me `box-sizing: border-box`, `width: 100%`, `max-width: 700px` dhe `padding: clamp(...)`.

Pa `!important`.

## width / padding / border me box-sizing

- `content-box` (parazgjedhja): `width` mat vetëm përmbajtjen. Gjerësia e vërtetë = width + padding + border.
- `border-box`: `width` përfshin padding dhe border. Një kuti me `width: 100%` mbetet 100% edhe me padding.
- Në `style.css` përdor `* { box-sizing: border-box; }` dhe `max-width` për afishen.

## Fokusi

`a:focus-visible` ka kontur 3px portokalli me `outline-offset`. Shihet kur shtyp Tab (edhe lidhja "Kalo te përmbajtja" shfaqet me Tab).

## Reflektim individual

Fitoi rregulli `#poster`, sepse kaskada krahason fillimisht specificitetin (ID kundër klasë), e vetëm nëse janë të barabartë merr parasysh renditjen. Pra `.poster` nuk mund ta mposhtte, edhe nëse shkruhet më poshtë. Zgjidhja e pastër është të mos kemi dy rregulla për të njëjtën veti, jo `!important`.
