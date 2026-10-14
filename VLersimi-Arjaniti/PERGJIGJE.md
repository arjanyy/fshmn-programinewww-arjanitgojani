# Përgjigjet — Prova 1

## P1.7

Çfarë bën box-sizing: border-box? Jep një shembull nga faqja jote që përfshin width, padding dhe border. Përgjigju në 2–3 fjali.

Përgjigjja ime: `box-sizing: border-box` siguron që gjerësia (width) dhe lartësia (height) e një elementi të llogaritin dhe të përfshijnë automatikisht `padding` dhe `border`, në vend që t'i shtojnë ato jashtë përmasave të përcaktuara. Për shembull, te klasa `.cards` kemi `width: 100%`, `padding: 2rem` dhe `border: 2px solid navy`; me `border-box`, gjerësia totale mbetet fiks 100% pa u zmadhuar më tej, duke parandaluar overflow-in e padëshiruar horizontal (daljen nga ekrani).

## P1.8

Pse përdoret a për lidhjen Detaje, ndërsa button për një veprim si “Shfaq/Fshih tekstin”? Referoju një lidhjeje nga faqja jote. Nuk duhet të implementosh buton ose JavaScript.

Përgjigjja ime: Elementi `<a>` (anchor) përdoret ekskluzivisht për navigim – për të kaluar nga një faqe në tjetrën ose te një seksion tjetër brenda faqes. Për shembull `<a href="#info">Detaje</a>` të çon menjëherë te seksioni me ID info. Elementi `<button>`, nga ana tjetër, përdoret për të shkaktuar një veprim (action) ose ndërveprim të ri në ndërfaqe (psh. ekzekutimi i një skripti për shfaqje/fshehje formash ose tekstesh).