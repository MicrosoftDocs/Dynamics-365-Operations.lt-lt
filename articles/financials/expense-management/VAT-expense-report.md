---
title: "PVM susigrąžinimas modulyje Išlaidų valdymas"
description: "Šioje temoje paaiškinama, kaip susigrąžinti lėšas už atitinkamas pridėtinės vertės mokesčio (PVM) operacijas."
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: d1c9357f8f51e1a87aebeb8f802dbe3b5fdd5aa0
ms.contentlocale: lt-lt
ms.lasthandoff: 03/13/2018

---

# <a name="vat-recovery-in-expense-management"></a>PVM susigrąžinimas modulyje Išlaidų valdymas

Norėdama susigrąžinti lėšas už atitinkamas pridėtinės vertės mokesčio (PVM) operacijas, įmonė ar organizacija turi nustatyti, rinkti, patikrinti ir pateikti tikslią informaciją. Šis procesas apima kelias užduotis ir, atsižvelgiant į jūsų įmonės dydį, gali apimti kelis darbuotojus ar vaidmenis.

Norint susigrąžinti PVM naudojant modulį Išlaidų valdymas, reikia įvykdyti tolesnes būtinąsias sąlygas.

- Reikia sukurti išlaidų kategorijoms priskirtų šalių / regionų mokesčių kodus.
- Kiekvienam mokesčių kodui reikia sukurti PVM grupę.
- Kiekvienai PVM grupei reikia sukurti prekės PVM kodą.

Kai būtinosios sąlygos įvykdytos, atlikdami šiuos veiksmus darbuotojai prašo grąžinti lėšas už PVM operacijas.

1. Išlaidų ataskaitoje įveskite mokesčių informaciją apie kredito kortelių operacijas, kad nustatytumėte atitinkamą PVM grąžinimą.
2. Įsitikinkite, kad įvesta visa mokesčių informacija, tada išlaidų ataskaitą registruokite.
3. Apdorokite išlaidas, už kurias galima susigrąžinti tarptautinį PVM.
4. Trečiosios šalies tiekėjui nusiųskite PVM susigrąžinimo duomenis, kad pateiktumėte tarptautinio lėšų susigrąžinimo prašymą.
5. Apdorokite išlaidas, kad susigrąžintumėte vietinį PVM.

Tolesniuose skyriuose pateikiami pavyzdžiai, rodantys, kaip „Contoso“ darbuotojai atlieka kiekvieną veiksmą.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Išlaidų ataskaitoje įveskite mokesčių informaciją apie kredito kortelių operacijas, kad nustatytumėte atitinkamą PVM grąžinimą

Nancy, JAV gyvenanti „Contoso“ pardavimo atstovė, neseniai grįžo iš darbo kelionės į Jungtinę Karalystę. Keliaudama ji patyrė asmeninių išlaidų už maistą, kurias apmokėjo kredito kortele. Dabar Nancy turi sukurti išlaidų ataskaitą, kad suderintų savo išlaidas.

Išlaidų ataskaitoje įvesdama informaciją, Nancy puslapio **Redaguoti išlaidų ataskaitą** lauke **Šalis / regionas** pasirenka **Jungtinė Karalystė**. Tada filtruojamas PVM grupių sąrašas, kad jame būtų rodomos tik Jungtinei Karalystei taikomos grupės. Nancy pasirenka PVM grupę **Jungtinė Karalystė 001**, tada – prekės PVM grupę **Maitinimo išlaidos**. Tada ji įtraukia naują operaciją, susijusią su jos apgyvendinimu. Kadangi su apgyvendinimu Jungtinėje Karalystėje susijusi tik viena PVM grupė ir prekės PVM grupė, ši informacija automatiškai įvedama Nancy'ės išlaidų ataskaitoje.

Pagal „Contoso“ strategiją visos išlaidos turi turėti atitinkamą kvitą. Todėl, įrašiusi savo išlaidų ataskaitą, Nancy gauna pranešimą, kad ji turi pridėti kvitą už kiekvieną operaciją, kurią nurodė išlaidų ataskaitoje. Nancy patikrina, ar prie išlaidų ataskaitos pridėjo skaitmeninį kiekvienos operacijos kvito vaizdą, ir pateikia ataskaitą patvirtinti. Tada ji tarnybinio biuro apdorojimo komandai nusiunčia popierinius kvitus. Ši komanda PVM susigrąžinimo duomenis nusiųs trečiosios šalies tiekėjui, „Contoso“ vardu teikiančiam tarptautinio PVM susigrąžinimo prašymus.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Įsitikinkite, kad įvesta visa mokesčių informacija, tada išlaidų ataskaitą registruokite

April, „Contoso“ modulio Mokėtinos sumos koordinatorė, turi įvesti bet kokią išlaidų ataskaitoje trūkstamą mokesčių informaciją, kad ataskaitą būtų galima registruoti. Ji atidaro puslapį **Išsami išlaidų ataskaitos informacija** ir mato Nancy'ės patvirtintą išlaidų ataskaitą. April tada atidaro išlaidų ataskaitą, kad peržiūrėtų išsamią informaciją apie operacijas. Ji mato, kad Nancy vienai iš operacijų neįvedė prekės PVM grupės. Kadangi ši informacija nėra pateikta, April negali registruoti išlaidų ataskaitos. Todėl April atidaro modulio Išlaidų valdymas puslapį **Mokesčių konfigūracijos** ir suranda atitinkamą prekės PVM grupę, skirtą šiai šaliai / regionui ir operacijos tipui. April išlaidų ataskaitą dabar gali registruoti didžiojoje knygoje.

Kai April užregistruoja išlaidų ataskaitą, sukuriamas PVM susigrąžinimo darbo elementas. Šis darbo elementas priskiriamas tarnybinio biuro apdorojimo komandos nariui. April gauna pranešimą, patvirtinantį, kad ataskaita užregistruota sėkmingai. Šiame pranešime taip pat pateikiamas PVM operacijų, kurių lėšas nustatyta grąžinti, skaičius.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Apdorokite išlaidas, už kurias galima susigrąžinti tarptautinį PVM

Arnie's, „Contoso“ tarnybinio biuro apdorojimo komandos narys, turi patvirtinti, kad į išlaidų ataskaitas įtraukta visa reikiama informacija dėl PVM susigrąžinimo. Jis atidaro puslapį **Išlaidų mokesčių susigrąžinimas** ir pasirenka Nancy'ės pateiktą išlaidų ataskaitą. Arnie'is patikrina, ar pridėti visi reikiami kvitai ir ar įvesti teisingi PVM grupė bei prekės PVM kodai.

Iš Nancy'ės gavęs popierinius kvitus, Arnie's juos sutikrina su skaitmeniniais kvitais ir išlaidų ataskaitos būseną pakeičia į **Paruošta sugrąžinti**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Trečiosios šalies tiekėjui nusiųskite PVM susigrąžinimo duomenis, kad pateiktumėte tarptautinio lėšų susigrąžinimo prašymą

Kai Arnie'is yra pasirengęs išlaidų ataskaitos duomenis nusiųsti trečiosios šalies tiekėjui, kuris pateiks PVM susigrąžinimo prašymus, jis atidaro puslapį **Išlaidų mokesčių susigrąžinimas**. Jis puslapį filtruoja, kad jame būtų rodomos tik tos išlaidų ataskaitos, kurios pažymėtos **Paruošta sugrąžinti**. Tada Arnie'is pasirenka **Failas** &gt; **Eksportuoti į „Excel“**. PVM informacija iš išlaidų ataskaitų eksportuojama į „Microsoft Excel“ darbalapį. Arnie'is šį darbalapį pateikia trečiosios šalies tiekėjui ir įtraukia pranešimą, nurodantį, kad popieriniai kvitai išsiųsti per kurjerį.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Apdorokite išlaidas, kad susigrąžintumėte vietinį PVM

Arnie's turi patikrinti, ar galima susigrąžinti PVM už išlaidų ataskaitų operacijas ir ar prie ataskaitų pridėti skaitmeniniai kvitai. Norėdamas pradėti apdoroti išlaidas, už kurias galima susigrąžinti vietinį PVM, Arnie's atidaro puslapį **Išlaidų mokesčių susigrąžinimas** ir pasirenka išlaidų ataskaitą, kurią reikia patikrinti. Jis patikrina, ar kvitai yra įmonės, o ne darbuotojo vardu. Norint susigrąžinti PVM, kvitai turi būti įmonės vardu. Tada Arnie'is patvirtina, kad buvo pritaikyti teisingi PVM grupė ir prekės PVM kodai.

Gavęs popierinius kvitus, Arnie'is išlaidų ataskaitos būseną pakeičia į **Paruošta sugrąžinti**. Tada susigrąžinimo prašymą jis gali pateikti atitinkamai mokesčių inspekcijai. Šiuo atveju atitinkama JAV mokesčių inspekcija yra „Internal Revenue Service“ (IRS).

