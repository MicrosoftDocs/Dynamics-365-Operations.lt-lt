---
title: Konsolidavimo ir šalinimo peržiūra
description: Šiame straipsnyje pateikta bendra informacija apie konsolidavimą ir pašalinimo procesą. Jame pateikti atsakymai į dažnai užduodamus klausimus.
author: panolte
ms.date: 11/11/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidate
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13151"
- intro-internal
ms.assetid: 9d8f55cb-b2cf-4e01-89cf-0e21f5c8ae1f
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 757c7634fc929ead018d1ddcca4cc223c1a95638
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779913"
---
# <a name="consolidation-and-elimination-overview"></a>Konsolidavimo ir šalinimo peržiūra

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikta bendra informacija apie konsolidavimą ir pašalinimo procesą. Jame pateikti atsakymai į dažnai užduodamus klausimus.

Konsoliduojant duomenis kelių dukterinių įmonių finansiniai rezultatai sujungiami į vienos konsoliduotos įmonės rezultatus. Dukterinės įmonės gali būti kitose versijose arba sistemose, jos gali nevisiškai priklausyti savininkui ir jos gali naudoti kitas valiutas. Yra kelios duomenų konsolidavimo parinktys:

-   **Konsoliduoti internetu** – pasirinkus šią pasirinktį konsoliduojami dienos balansai pagal pasirinktas sąskaitas ir dimensijas ir saugomi konsoliduotoje įmonėje.
-   **Finansinės ataskaitos** – pasirinkus šią pasirinktį įjungiamas operacijų ir balansų konsolidavimas, kuris gali būti generuojamas bet kuriuo metu. Galima sukurti kelių lygių hierarchijas ir peržiūrėti kelias ataskaitų valiutas.
-   **Konsoliduoti su importu** – pasirinkus šią pasirinktį į konsoliduotą įmonę importuojami balansai.
-   **Įmonės balansų eksportavimas** – pasirinkus šią pasirinktį pateikiamas įmonės balansų eksportavimo failas. Tada failą galima importuoti į kitus egzempliorius ar sistemas. Finansines ataskaitas taip pat galima naudoti norint eksportuoti balansus į „Microsoft Excel“ failą.

Apie pašalinimus galima paskelbti keliais būdais:

-  Pašalinimo taisykles galima nustatyti sistemoje ir apdoroti vykstant konsolidavimo procesui arba pateikiant pašalinimo pasiūlymą. Taisykles galima registruoti bet kurioje įmonėje, kurios juridinio subjekto nustatymuose pažymėta **Naudoti finansinio pašalinimo procesui**.
-   Galima sukurti atskirą įmonę ir naudoti ją norint rankiniu būdu nustatyti ir registruoti pašalinimo operacijas. Šią įmonę galima naudoti konsolidavimo procese arba finansinėse ataskaitose.
-  Sąskaitas ir finansines dimensijas, kurios naudojamos norint nustatyti vidinės įmonės veiklą, galima filtruoti eilutės apraše arba finansinių ataskaitų stulpelio apraše ir galima naudoti visas detalizavimo galimybes. Apskaičiuotą stulpelį ar eilutę tada galima naudoti norint pašalinti sąskaitas ir finansines dimensijas iš konsoliduotos bendrosios sumos.

Yra daug konsolidavimo scenarijų ir kiekvienu atveju scenarijus galima tvarkyti skirtingais būdais.

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai
Norėčiau registruoti pašalinimus duomenų bazėje. Kokios galimos pasirinktys?
 - Galite rinktis iš kelių pasirinkčių. Galite naudoti pasirinktį **Konsoliduoti internetu** ir įtraukti pašalinimus proceso metu arba kaip pasiūlymą. Operacijos bus užregistruotos konsoliduotoje įmonėje. Taip pat galite turėti atskirą įmonę, kurioje rankiniu būdu kursite pašalinimus, ir naudoti tą įmonę finansinėse ataskaitose arba vykdant konsolidavimo procesą.

Mums reikia konsoliduotų rezultatų keliomis ataskaitų valiutomis.
 - Pasirinktis **Finansinės ataskaitos** turi neribotas ataskaitų valiutas. Duomenys konvertuojami generuojant ataskaitą, priklausomai nuo nustatyto pagrindinės sąskaitos valiutos kurso tipo ir valiutos konvertavimo būdo. Tačiau, kadangi pasirinktis **Konsoliduoti internetu** turi tik vieną ataskaitų valiutą, jei naudojate šią pasirinktį, kiekvienai ataskaitų valiutai reikalinga konsoliduota įmonė. Rekomenduojama pasirinkti būdą **Finansinės ataskaitos**.

Noriu matyti kiekvienos įmonės operacijos lygio informaciją.
 - Pasirinktis **Finansinės ataskaitos** yra sprendimas, nes operacijos lygio informaciją galima peržiūrėti apie tiek įmonių, kiek jų įtraukta į ataskaitų medžio aprašą.

Mes naudojame biudžeto planavimą arba biudžeto kontrolę ir tai turi būti konsoliduota.
 - Pasirinktis **Finansinės ataskaitos** yra sprendimas, skirtas konsoliduoti bet kokius biudžeto planavimo arba biudžeto kontrolės duomenis.

Mūsų filialai išsidėstę visame pasaulyje ir mes turime kelis sąskaitų planus. Koks yra geriausias būdas konsoliduoti mūsų duomenis?
- Kai reikia tvarkyti kelis sąskaitų planus galite naudoti kelias pasirinktis. Galite naudoti pasirinktį **Konsoliduoti internetu**, o po to pasirinkti naudoti pagrindinėje sąskaitoje arba konsolidavimo sąskaitos grupėje nurodytą konsolidavimo sąskaitą. Taip pat galite naudoti pasirinktį **Finansinės ataskaitos**, įtraukti keletą nuorodų į eilutės apibrėžimo finansines dimensijas ir susieti sąskaitas.

Mes reikalaujame kelių lygių konsolidavimo. Kitaip tariant, pirmiausia konsoliduojame visus mūsų Europos filialus į Britanijos svarą (GBP). Tada paimame tuos duomenis ir konvertuojame konsoliduotą sumą į JAV dolerius. Kaip galime tai padaryti?
- Kai reikalingi keli konsolidavimo lygiai ir kiekvienam lygiui naudojamos skirtingos valiutos, turite naudoti pasirinktį **Konsoliduoti internetu**. Turi būti sukurtos kelios konsoliduotos įmonės, kurių skirtingos apskaitos ir ataskaitų valiutos. Konsolidavimą tada reikia paleisti kelis kartus. Pasirinkus pasirinktį **Finansinės ataskaitos** visada konvertuojama iš kiekvienos šaltinio įmonės apskaitos valiutos į pasirinktą valiutą.

Mes turime filialų kitoje sistemoje. Kaip galime juos konsoliduoti?
- Naudodami pasirinktį **Konsoliduoti su importu** perkelkite balansus į konsoliduojamą įmonę.

Kai kurie iš mūsų filialų nevisiškai priklauso savininkui. Koks yra geriausias būdas juos konsoliduoti?
- Turite kelias iš dalies savininkams priklausančių filialų pasirinktis. Naudodami pasirinktį **Finansinės ataskaitos** galite nurodyti ataskaitų medžio aprašą ir nuosavybės teisę. Taip pat norėdami pateikti iš dalies priklausančią sumą galite naudoti apskaičiuotą eilutę arba stulpelį. Kaip atskirą eilutę ataskaitoje jūs net galite parodyti mažumos palūkanas. Taip pat galite naudoti pasirinktį **Konsoliduoti internetu**. Skirtuke **Juridiniai subjektai** yra stulpelis **Nuosavybė**, kuriame galite nurodyti pirminei įmonei priklausančią procentinę dalį.

Mūsų organizacija turi rodyti konsolidacijas pagal verslo struktūros vienetus arba pagal tai, kaip norima naudoti organizacijos hierarchijas.
- Pasirinktis **Finansinės ataskaitos** yra sprendimas. Apie organizacijas, turinčias juridinių subjektų arba finansinių dimensijų, gali būti paskelbta finansinėse ataskaitose. Taip pat naudodami juridinių subjektų ir dimensijų reikšmių kombinaciją turintį ataskaitų medžio aprašą galite sukurti savo kelių lygių hierarchijas.

Mes turime daugiau nei vieną sistemos egzempliorių.
- Naudodami pasirinktį **Įmonės balansų eksportavimas**, skirtą eksportuoti iš vieno egzemplioriaus, o po to kitame egzemplioriuje naudodami pasirinktį **Konsoliduoti su importu** galite konsoliduoti duomenis.

Ar galiu atlikti konsolidavimą su savo biudžetu **ŠABLONO** būsenoje? 
- Negalėsite apdoroti ar užbaigti savo biudžetų konsolidavimo įmonėje. Rekomenduojame naudoti „Financial Reporting“ tam, kad konsoliduotumėte šablono biudžetus.

Daugiau informacijos rasite [Valiutos kurso pasikeitimas konsoliduotoje įmonėje](../general-ledger/currency-revaluation-consolidation-company.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
