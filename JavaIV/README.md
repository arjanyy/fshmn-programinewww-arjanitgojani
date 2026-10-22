# Java IV — Festivali që përshtatet në çdo ekran

## Çfarë realizova

- Një faqe me menu fleksibile (Flexbox) dhe gjashtë karta aktivitetesh.
- Kartat vendosen me Grid: 1 kolonë nën 600 px, 2 kolona nga 600 deri në 899 px, 3 kolona nga 900 px.
- Çdo kartë ka imazh, titull, kategori, orar dhe lidhje "Shiko detajet".
- Imazhet janë SVG lokale në `assets/` dhe kanë `width: 100%; height: auto`, pra shkallëzohen me kartën.
- Asnjë tekst nuk ka lartësi fikse. Titujt e gjatë thyhen me `overflow-wrap: anywhere`.
- Menuja përdor lidhje `<a>` të vërteta, ka fokus të dukshëm dhe lidhjen "Kalo te përmbajtja".

## Si hapet

1. Hap dosjen `JavaIV/`.
2. Hap `index.html` në shfletues (dy herë klik ose Live Server në VS Code).
3. Për testim: F12, pastaj ikona e pajisjeve (Ctrl+Shift+M) dhe vendos gjerësinë 360, 768 ose 1280.

## Testet

| Hyrja (gjerësia) | Rezultati i pritur | Rezultati i marrë |
| --- | --- | --- |
| 360 px | 1 kolonë, pa scroll horizontal | _plotëso pas testit_ |
| 768 px | 2 kolona, pa scroll horizontal | _plotëso pas testit_ |
| 1280 px | 3 kolona, pa scroll horizontal | _plotëso pas testit_ |
| Tab në menu | fokusi kalon nëpër lidhje me kornizë të verdhë | _plotëso pas testit_ |
| Titulli 100-karakterësh (karta 6) | teksti thyhet brenda kartës | _plotëso pas testit_ |

## Rastet e pranimit

- [ ] Në 360/768/1280 px shfaqen përkatësisht 1/2/3 kolona.
- [ ] Nuk ka scroll horizontal në faqen e plotë.
- [ ] Menuja mbetet e përdorshme me tastierë.

## Sfida e transferimit

Karta e gjashtë ka një titull me saktësisht 100 karaktere. Ai thyhet në disa rreshta dhe karta bëhet më e lartë, por nuk del jashtë saj. Kartat e tjera në të njëjtin rresht shtrihen sa karta më e lartë.

## Reflektim individual

Kur do të zgjidhje Flexbox dhe kur Grid?

Flexbox e përdor kur elementet janë në një drejtim, për shembull menuja në një rresht ose brendësia e kartës (imazhi, teksti dhe lidhja njëra nën tjetrën). Grid e përdor kur duhet të organizoj faqen në rreshta dhe kolona njëkohësisht, si këtu që kartat ndahen në 1, 2 ose 3 kolona sipas ekranit. Në këtë detyrë i përdora të dyja: Grid për kartat dhe Flexbox brenda tyre.

## Deklarimi i AI/burimeve

- Burime: libri i lëndës (kap. 6–7) dhe fleta e ushtrimit.
- AI: skicën e kodit HTML/CSS e hartova me ndihmën e Claude (Anthropic). E lexova, e kuptova dhe e testova vetë në shfletues.
- _Ndrysho këtë pjesë që të përputhet saktësisht me atë që ke bërë ti._
