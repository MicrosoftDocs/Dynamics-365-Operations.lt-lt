---
title: Klientų skirstymo pagal terminus momentinės kopijos
description: Šioje temoje pateikiama informacijos apie kliento snėjimo momentines nuotaukas. Senstanti momentinė nuotrauka apskaičiuoja amžiaus balansą klientų grupėms vienu kartu.
author: JodiChristiansen
ms.date: 05/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 54db3e53cd31936ce80f0cdf1147535216d0d4b4
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723001"
---
# <a name="customer-aging-snapshots"></a>Klientų skirstymo pagal terminus momentinės kopijos

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacijos apie kliento snėjimo momentines nuotaukas. Senstanti momentinė nuotrauka apskaičiuoja amžiaus balansą klientų grupėms vienu kartu. Galite sukurti skirstymo pagal terminus momentinės kopijos įrašus visiems klientams arba klientams, esantiems klientų telkinyje.

Informacija iš senėjimo momentinių nuotraukų rodoma **Pagal terminus suskirstytų balansų** sąrašo puslapyje ir **Surinkimo** puslapyje. Prieš naudodami sąrašo puslapį turite sukurti skirstymo pagal laikotarpius **Senėjimo balansų** momentinę kopiją. Sąrašo puslapyje informacija rodoma tik tiems klientams, kuriems buvo sukurta skirstymo pagal terminus momentinė kopija.

**Kliento kredito ir mokėjimų priežiūros** darbo sritis taip pat rodo klientų kurti terminus. Daugiau informacijos rasite [kreditų ir rinkinių valdymo „Power BI“ turinyje](credit-collections-power-bi.md).

> [!NOTE]
> Norėdami sumažinti laiką, reikalingą kuriant skirstymo pagal terminus momentinę kopiją, įjunkite funkcijų valdymo darbo srityje funkciją **Klientų skirstymo pagal** terminus **Efektyvumo patobulinimas** darbo srityje. Tačiau, kai ši funkcija įjungta, nenaudokite klientų telkinių. Jei pasirinktas klientų telkinys, priemonė neveiks, bet vis tiek galite kurti skirstymo pagal terminus momentinę kopiją.

Kurdami skirstymo pagal terminus klientų momentinę kopiją, naudokite šiuos laukus, kad įvesdami informaciją apie ją:

- Lauke **Skirstymo pagal terminus laikotarpio apibrėžimas** rinkitės savo sukurtą skirstymo pagal terminus senėjimo nuotrauką. Kiekvienos senėjimo pagal terminus laikotarpio apibrėžties galite turėti vieną momentinę kopiją. Skirstymo pagal terminus momentinė kopija ir skirstymo pagal terminus laikotarpio apibrėžimas turi būti sukurti atskirai.
- **Baseino ID** – Šis laukas nėra privalomas. Galite naudoti telkinį norėdami nustatyti klientų rinkinį, kuris turi būti apdorotas skirstymo pagal terminus momentinę kopiją. Jei renkatės klientų telkinį, šiame lauke skirstymo pagal terminus momentinės kopijos procesas kuriamas tik toms kliento sąskaitoms, kurios yra klientų telkinio dalis. Pasirinkto kliento telkinio tipas turi būti **Skirstymo pagal terminus momentinės kopijos** tipas. Jei šį lauką paliksite tuščią, bus sukurta visų klientų sąskaitų skirstymo pagal terminus momentinė kopija.

    > [!NOTE]
    > Jei **klientų skirstymo pagal terminus našumo** patobulinimo funkcija įjungta, nepasirinkite klientų telkinio.

- **Kriterijai** – skirstymo pagal terminus momentinė kopija bus pagal jūsų pasirinktą datą:

    - **Operacijos data** –skirstykite visas operacijas pagal terminų atlikimo datą.
    - **Terminas** – skirstykite visas operacijas pagal jų terminų atlikimą.
    - **Dokumento data** – skirstykite visas operacijas jų dokumento datą.

- **Skirstymas į terminus pagal** – Rinkitės naudotiną datą **Esamos datos** laukelyje skirstymo pagal terminus momentinėje ekrano nuotraukoje. Pagal šią datą apskaičiuojami skirstymo pagal terminus laikotarpiai. 

    - **Šios dienos data** – naudokite sistemos datą. Rinkitės šią parinktį, jei nustatyta, kad apdorojimas bus vykdomas atliekant pasikartojančią paketinę užduotį. Tada kiekvieną kartą, kai paleidžiate paketą, naudojama sistemos data, kada buvo paleista.
    - **Pasirinkta data** – naudokite nurodytą datą. Jei pasirenkate šią parinktį, taip pat turite įvesti skirstymo pagal terminus datą.

    Pavyzdžiui, dabartinis skirstymo pagal terminus laikotarpis yra 30 dienų. Jei šiame lauke renkatės **Šiandienos data** dabartinis skirstymo pagal terminus laikotarpis prasideda šiandienos datą ir apima ankstesnes 29 dienas. Jei šiame lauke renkatės **Pasirinkta data** ir įvedate datą, dabartinis skirstymo pagal nurodytus terminus laikotarpis prasideda šiandienos datą ir apima ankstesnes 29 dienas.

- **Naujinimo surinkimo būsena** – Nustatykite šią parinktį į **Taip** norėdami atnaujinti operacijų surinkimo būseną **Kolekcijos** puslapyje iš **Žadėti sumokėti** į **Žadėti sumokėti sulūžusį** jei skirstymo pagal terminus data yra pasibaigusi datai lauke **Pažadas sumokėti** laukelį. Nustatykite šią pasirinktį **Ne**, jei norite, kad mokėjimų priežiūros būsena nepakito **Kolekcijų** puslapyje.
- **Įtraukite klientus, kurių balansas lygus nuliui** – nustatykite šią pasirinktį kaip **Taip**, norėdami įtraukti visus klientus, neatsižvelgiant į jų balansą. Jei įtraukite visus klientus, rekomenduojame įjungti **klientų skirstymo pagal terminus našumo patobulinimo** funkciją ir nenaudoti klientų telkinių. Nustatykite šią parinktį į **Ne** jei norite įtraukti tik klientus, kurie turi balansą. Šis parametras padeda pagreitinti našumą, nes praleidžiami klientai, neturint balanso.
- **Įmonių diapazonas** – skirtuke **Įmonių diapazonas** pasirinkite juridinius subjektus (įmones), kurie bus įtraukti į skirstymo pagal terminus momentinę kopiją. Pasirinkti galima tik juridinius subjektus, nustatytus centralizuotiems mokėjimams. Pasirinktų juridinių subjektų operacijos įtraukiamos į klientų, kurie turi tokį patį šalies ID visuose juridiniuose subjektuose, skirstymo pagal terminus laikotarpius. Dabartinės sumos yra verčiamos į juridinio subjekto valiutą, prie kurio esate prisiregistravę, kai kuriate skirstymo pagal terminus momentinę kopiją, apskaitos valiuta.

Rekomenduojame suplanuoti šį procesą, kad jis būtų vykdomas pakete.

> [!NOTE]
> Norėdami pagerinti paketo našumą kurdami skirstymo pagal terminus momentines kopijas, lauke **Maksimalus paketinių užduočių skaičius** įveskite skaičių, kuris yra **numatytųjų rinkinių nustatymų** „FastTab“ laukelyje **Rinkiniai** puslapyje **gautinų sumų parametrai**. Lauke **Amžiaus kliento balansai** rekomenduojame pradėti nuo numatytosios vertės **100** ir tada koreguoti vertę, kad būtų optimizuotas jūsų situacijos apdorojimas.

