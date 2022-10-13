---
title: Klientų skirstymo pagal terminus momentinės kopijos
description: Šiame straipsnyje pateikiama informacija apie klientų skirstymo pagal terminus momentines kopijas. Senstanti momentinė nuotrauka apskaičiuoja amžiaus balansą klientų grupėms vienu kartu.
author: JodiChristiansen
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.search.form: ''
ms.openlocfilehash: 88145cdccfe3f1d0d3de4e31dfa519b27df6550a
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643691"
---
# <a name="customer-aging-snapshots"></a>Klientų skirstymo pagal terminus momentinės kopijos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie klientų skirstymo pagal terminus momentines kopijas. Senstanti momentinė nuotrauka apskaičiuoja amžiaus balansą klientų grupėms vienu kartu. Galite sukurti skirstymo pagal terminus momentinės kopijos įrašus visiems klientams arba klientams, esantiems klientų telkinyje.

Informacija iš senėjimo momentinių nuotraukų rodoma **Pagal terminus suskirstytų balansų** sąrašo puslapyje ir **Surinkimo** puslapyje. Prieš naudodami sąrašo puslapį turite sukurti skirstymo pagal laikotarpius **Senėjimo balansų** momentinę kopiją. Sąrašo puslapyje informacija rodoma tik tiems klientams, kuriems buvo sukurta skirstymo pagal terminus momentinė kopija.

**Kliento kredito ir mokėjimų priežiūros** darbo sritis taip pat rodo klientų kurti terminus. Daugiau informacijos rasite [kreditų ir rinkinių valdymo „Power BI“ turinyje](credit-collections-power-bi.md).

> [!NOTE]
> Norėdami sumažinti laiką, kurio reikia skirstymo pagal terminus momentinę kopiją sukurti, **funkcijų** valdymo darbo srityje įjunkite toliau nurodytas funkcijas: **·** 
> **Skirstymo pagal terminus našumo pagerinimas Klientų skirstymo pagal terminus efektyvumas naudojant klientų telkinius**  
> Kai įgalintos abi priemonės, **kuriant skirstymo pagal** terminus momentinę kopiją galima naudoti klientų telkinius. 

Kurdami skirstymo pagal terminus klientų momentinę kopiją, naudokite šiuos laukus, kad įvesdami informaciją apie ją:

- Lauke **Skirstymo pagal terminus laikotarpio apibrėžimas** rinkitės savo sukurtą skirstymo pagal terminus senėjimo nuotrauką. Kiekvienos senėjimo pagal terminus laikotarpio apibrėžties galite turėti vieną momentinę kopiją. Skirstymo pagal terminus momentinė kopija ir skirstymo pagal terminus laikotarpio apibrėžimas turi būti sukurti atskirai.
- **Baseino ID** – Šis laukas nėra privalomas. Galite naudoti telkinį norėdami nustatyti klientų rinkinį, kuris turi būti apdorotas skirstymo pagal terminus momentinę kopiją. Jei renkatės klientų telkinį, šiame lauke skirstymo pagal terminus momentinės kopijos procesas kuriamas tik toms kliento sąskaitoms, kurios yra klientų telkinio dalis. Pasirinkto kliento telkinio tipas turi būti **Skirstymo pagal terminus momentinės kopijos** tipas. Jei šį lauką paliksite tuščią, bus sukurta visų klientų sąskaitų skirstymo pagal terminus momentinė kopija.


- **Kriterijai** – skirstymo pagal terminus momentinė kopija bus pagal jūsų pasirinktą datą:

    - **Operacijos data** –skirstykite visas operacijas pagal terminų atlikimo datą.
    - **Terminas** – skirstykite visas operacijas pagal jų terminų atlikimą.
    - **Dokumento data** – skirstykite visas operacijas jų dokumento datą.

- **Skirstymas į terminus pagal** – Rinkitės naudotiną datą **Esamos datos** laukelyje skirstymo pagal terminus momentinėje ekrano nuotraukoje. Pagal šią datą apskaičiuojami skirstymo pagal terminus laikotarpiai. 

    - **Šios dienos data** – naudokite sistemos datą. Rinkitės šią parinktį, jei nustatyta, kad apdorojimas bus vykdomas atliekant pasikartojančią paketinę užduotį. Tada kiekvieną kartą, kai paleidžiate paketą, naudojama sistemos data, kada buvo paleista.
    - **Pasirinkta data** – naudokite nurodytą datą. Jei pasirenkate šią parinktį, taip pat turite įvesti skirstymo pagal terminus datą.

   Pavyzdžiui, dabartinis skirstymo pagal terminus laikotarpis yra 30 dienų. Jei šiame lauke renkatės **Šiandienos data** dabartinis skirstymo pagal terminus laikotarpis prasideda šiandienos datą ir apima ankstesnes 29 dienas. Jei šiame lauke renkatės **Pasirinkta data** ir įvedate datą, dabartinis skirstymo pagal nurodytus terminus laikotarpis prasideda šiandienos datą ir apima ankstesnes 29 dienas.

- **Naujinimo surinkimo būsena** – Nustatykite šią parinktį į **Taip** norėdami atnaujinti operacijų surinkimo būseną **Kolekcijos** puslapyje iš **Žadėti sumokėti** į **Žadėti sumokėti sulūžusį** jei skirstymo pagal terminus data yra pasibaigusi datai lauke **Pažadas sumokėti** laukelį. Nustatykite šią pasirinktį **Ne**, jei norite, kad mokėjimų priežiūros būsena nepakito **Kolekcijų** puslapyje.
- **Įtraukite klientus, kurių balansas lygus nuliui** – nustatykite šią pasirinktį kaip **Taip**, norėdami įtraukti visus klientus, neatsižvelgiant į jų balansą. Jei įtraukite visus klientus, **·** **rekomenduojame įjungti ir klientų skirstymo pagal terminus našumo patobulinimą, ir klientų skirstymo pagal terminus našumo patobulinimą, naudojant klientų telkinių** funkcijas. Nustatykite šią parinktį į **Ne** jei norite įtraukti tik klientus, kurie turi balansą. Šis parametras padės pagreitinti našumą, nes praleidžiami klientai, neturiys balanso.
- **Apeiti kredito limito skaičiavimus skirstymo pagal terminus metu –** **·** **jei ši parinktis** nustatyta kaip Taip, skirstymo pagal terminus procesas neatskaičiuos važtaraščio tarpinės sumos, **·** **atviro** užsakymo tarpinės sumos ir kiekvieno kliento kreditas. Šie balansai rodomi balanso pagal terminą **puslapyje**, "FactBox" dalyje Kredito **limitas**. Kad būtų greičiau našumas skirstymo pagal terminus proceso metu, nustatykite šią pasirinktį **kaip Taip**. Nustatykite, kad **vykdant** skirstymo pagal terminus procesą balansai būtų perskaičiuoti. 
- **Įmonių diapazonas** – skirtuke **Įmonių diapazonas** pasirinkite juridinius subjektus (įmones), kurie bus įtraukti į skirstymo pagal terminus momentinę kopiją. Pasirinkti galima tik juridinius subjektus, nustatytus centralizuotiems mokėjimams. Pasirinktų juridinių subjektų operacijos įtraukiamos į klientų, kurie turi tokį patį šalies ID visuose juridiniuose subjektuose, skirstymo pagal terminus laikotarpius. Dabartinės sumos yra verčiamos į juridinio subjekto valiutą, prie kurio esate prisiregistravę, kai kuriate skirstymo pagal terminus momentinę kopiją, apskaitos valiuta.

Rekomenduojame suplanuoti šį procesą, kad jis būtų vykdomas pakete.

> [!NOTE]
> Norėdami pagerinti paketo našumą kurdami skirstymo pagal terminus momentines kopijas, lauke **Maksimalus paketinių užduočių skaičius** įveskite skaičių, kuris yra **numatytųjų rinkinių nustatymų** „FastTab“ laukelyje **Rinkiniai** puslapyje **gautinų sumų parametrai**. Amžiaus kliento **balansų** lauke rekomenduojame pradėti nuo 12 iki **20** **datos ir koreguoti vertę,** kad būtų optimizuotas jūsų situacijos apdorojimas. Nerekomenduojame nustatyti šios vertės daugiau nei **30**, nes tai turės įtakos našumui. 

