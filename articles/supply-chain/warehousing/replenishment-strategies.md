---
title: Papildymo strategijos
description: Šiame skyriuje aprašyta informacija apie papildymo strategijas ir paaiškinta, kaip galite naudoti papildymo strategijos laukelį bangos paklausos papildymo šablono eilutės siekiant pasirinkti, kaip atliekamas papildymas.
author: mirzaab
manager: tfehr
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 45b3b1a4d2e92a52ee69c17865634a6578181ac7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646138"
---
# <a name="replenishment-strategies"></a>Papildymo strategijos

[!include [banner](../includes/banner.md)]

Šablonai, kurie nustatyti **Papildymo šablonuose** puslapyje apima bangos paklausos papildymo šablono eilutes, leidžiančias jums pasirinkti, kaip papildymas atliekamas. Kiekviena eilutė apima **Papildymo strategijos** laukelį.

Strategija *Bangos paklausos kokybė* yra nustatytoji. Tai papildymo strategija naudojama anksčiau įžanogs **Papildymo strategijos** laukelyje. Ji naudoja papildymo vietos kryptis, kad rastų papildytinas vietas. Ji tada pildo tas vietas, kol paklausa bus padengta.

Strategija *Maksimali vietos talpa* pristato keletą naujų funkcijų. Kaip *Bangos paklausos kokybės* strategija ji naudoja papildymo vietos kryptis, kad rastų papildytinas vietas ir tada pildo jas iki kol padengs paklausą. Jis skiriasi nuo *Bangos paklausos kiekio* strategijos, kurioje visos papildymo vietos yra pildomos iki jų maksimalios talpos kaip nustatyta vietos talpos apribojimuose. Strategija *Maksimali vietos talpa* stengiasi sukurti darbą tam, kad paimtų šį būtiną kiekį, kartu su papildomu kiekiu ir užpildytų pildomas vietas. Nepaisant to, kai kuriais atvejais tai nepavyksta. Pavyzdžiui, palaidos vietos gali neturėti pakankamai inventoriaus, kad padengtų papildomą kiekį. Tais atvejais, sistema aptinka problemą ir bando atkurti.

Piko seansas yra vienas pavyzdys, kai *Maksimali vietos talpos* strategija yra svarbesnė nei *Bangos paklausos kiekio* strategija. Piko sezono metu, kai kurios prekės gali būti parduodamos dideliais kiekiais. Dėl to, jums gali reikėti aktyviai pildyti atitinkamas paėmimo vietas kaip įmanoma labiau siekiant sumažinti darbo skaičiaus ID sukuriamą papildymo metu.

> [!IMPORTANT]
> Norėdami pasinaudoti visa *Maksimalios vietos talpos* strategija, turite nustatyti iš naujo talpos apribojimus atitinkamoms vietoms. Kitu atveju, ši strategija veiks kaip *Bangos paklausos kokybė* strategija.

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a>Įjunkite papildymą iki maksimalaus pagal talpos apribojimų funkciją

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Adminsitratoriai gali naudoti [Funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo erdvę tam, kad patikrintų funkcijos būseną ir ją įjungtų, jei jos reikia. Ten ši funkcija pateikiama taip:

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Pildymas iki maksimalaus pagal talpos apribojimus*

## <a name="set-up-replenishment-strategies"></a>Papildymo strategijos nustatymas

Norėdami prieiti prie šablonų, eikite į **Sandėlio valdymas \> Nustatymai \> Pildymas \> Pildymo šablonai**. Skyriuje **Peržiūra** pasirinkite ar sukurkite bangos paklausos papildymo šabloną, kuriame **Papildymo tipo** laukelis nustatytas į *Bangos paklausa*. Tuomet nustatykite papildymo šablono eilutes **Papildymo šablono išsami informacija** skyriuje. Kiekvienai eilutei **Papildymo strategijos** laukelyje pasirinkite papildymo strategiją, kurią norite naudoti.

![Papildymo šablonų puslapis](media/ReplenTempWaveDmdMaxLocCap.png "Papildymo šablonų puslapis")

Jei **Papildymo strategijos** stulpelis nepasirodo tinklelyje **Papildymo šablono išsamios informacijos** skyriuje, įsitikinkite, kad funkcija buvo įjungta ir kad pasirinktas papildymo šablonas turi papildymo tipą *Bangos paklausa*.

> [!NOTE]
> Strategija *Bangos paklausos kokybė* yra nustatytoji. Dėl to, turite tik naujinti papildymo šablono eilutes, kuriose norite naudoti *Maksimalio vietos talpos* strategiją vietoje kitos.

## <a name="example-scenarios"></a>Scenarijų pavyzdžiai

### <a name="example-1"></a>1 pavyzdys

Šiame pavyzdyje yrar tik vienas papildymo šablonas, kuris turi vieną šablono eilutę.

Sukuriate prekybos užsakymą 130 vienetams (vnt) prekei A0001. Prieš jums išleidžiant užsakymą į sandėlį, jis nustatytas tokiu būdu:

- Yra tik viena bendra vieta ir joje yra 500 vnt esančio turimo inventoriaus.
- Yra trys paėmimo vietos, kurių kiekvienoje kiekis yra 100 vnt. (Atminkite, kad talpos apribojimų reikia *Maksimalios vietos talpos* strategijai.)
- Papildymo padėjimo vietos yra tokios pačios kaip paėmimo.
- Papildymo vienetas yra dėžė (1 dėžė = 20 vnt).

Užsakymo metu, tolesnis inventorius turimas prekybos paėimimo vietoje:

- **Pick-001:** 20 vnt (1 dėžė)
- **Pick-002:** 0 vnt
- **Pick-003:** 0 vnt

Iš pradžių, papildymo strategija nustatyta į *Bangos paklausos kokybė*.

Po prekybos užsakymo išleidimo į sandėlį ir bangos tvarkymo vykdymo bangai, gaunate šį papildymo darbą:

- **Papildymo darbas 1:** Imkite 4 dėžes iš bendros vietos ir padėkite jas į vietą pick-001.
- **Papildymo darbas 2:** Imkite 2 dėžes iš bendros vietos ir padėkite jas į vietą pick-002.

Gaunate du papildymo darbo ID, nes privalote papildyti dvi vietas ir keli padėjimai nepalaikomi.

Jei nustatote papildymo strategiją į *Maksimali vietos talpa* gaunate šį papildymo darbą:

- **Papildymo darbas 1:** Imkite 4 dėžes iš bendros vietos ir padėkite jas į vietą pick-001.
- **Papildymo darbas 2:** Imkite 5 dėžes iš bendros vietos ir padėkite jas į vietą pick-002.

[![1 pavyzdys](media/ReplenTemp_example_1.png "1 pavyzdys")](media/ReplenTemp_example_1_large.png)

### <a name="example-2"></a>2 pavyzdys

Šis pavyzdys rodo, kas atsitinka, kai bendra vieta neturi pakankamai inventoriaus, kad jis padengtų papildomą kiekį. Jis naudoja tą patį scenarijų kaip pavyzdyje 1, bet bendra vieta turi 160 vnt. (8 dėžes).

Strategija *Bangos paklausos kiekis* sukuria tą patį darbą, kaip ir padarė pavyzdyje 1.

Nepaisant to, kadangi *Maksimali vietos talpos* strategija bando sukurti darbo ID kaip padarė pavyzdyje e 1, ji gali nepavykti. Tuo metu, sistema bando atkurti.

Priklausomai nuo **Leisti atskyrimą** parinkties nustatymų vietos kryptyse papildymo paėmimui, galimos dvi išeitys:

- Jei **Leisti atskyrimą** parinktis nustatyta į *Taip*, sukuriamas tolesnis papildymo darbas:

    - **Papildymo darbas 1:** Imkite 4 dėžes iš bendros vietos ir padėkite jas į vietą pick-001.
    - **Papildymo darbas 2:** Imkite 4 dėžes iš bendros vietos ir padėkite jas į vietą pick-002.

- Jei **Leisti atskyrimą** parinktis nustatyta į *Ne*, sukuriamas tolesnis papildymo darbas:

    - **Papildymo darbas 1:** Imkite 4 dėžes iš bendros vietos ir padėkite jas į vietą pick-001.
    - **Papildymo darbas 2:** Imkite 2 dėžes iš bendros vietos ir padėkite jas į vietą pick-002.

Pasekmė skiriasi dėl informacijos, kuri prieinama jums sukūrus darbą. Kai **Leisti atskyrimą** nustayta į *Taip* vieto kryptyse papildymo paėmimui, žinote, kad sugebėjote surasti 160 vnt. Dėl to, galite sukurti darbą tam kiekiui. Nepaisant to, kai **Leisti atskyrimą** parinktis nustatyta į *Ne*, nežinote apie esančius 160 vnt. Kadangi papildomas kiekis, kurį nusprendėte papildyti buvo 3 dėžės, numetėte papildomą kiekį ir bandote ankstesnį kiekį dar kartą.

[![2 pavyzdys](media/ReplenTemp_example_2.png "2 pavyzdys")](media/ReplenTemp_example_2_large.png)

Dėl to, kad gautumėte maksimalų kiekį vietų papildymui, turite nustatyti **Leisti atskyrimą** parinktį į *Taip* vietos kryptyse papildymui.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]