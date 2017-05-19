---
title: "Mobilioji darbo sritis Pardavimo užsakymai"
description: "Šioje temoje pateikiama informacija apie pardavimo užsakymų mobiliąją darbo sritį, kurią galima naudoti mobiliojoje programoje „Microsoft Dynamics 365 for Operations“. Ši darbo sritis suteikia galimybę bet kur ir bet kada peržiūrėti naujausią pardavimo užsakymų informaciją."
author: YuyuScheller
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 119b80e5d8067ffbf75d8b067f4803558c2c94b0
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="sales-orders-mobile-workspace"></a>Mobilioji darbo sritis Pardavimo užsakymai

[!include[banner](../includes/banner.md)]


Šioje temoje pateikiama informacija apie pardavimo užsakymų mobiliąją darbo sritį, kurią galima naudoti mobiliojoje programoje „Microsoft Dynamics 365 for Operations“. Ši darbo sritis suteikia galimybę bet kur ir bet kada peržiūrėti naujausią pardavimo užsakymų informaciją. 

<a name="overview-of-the-sales-orders-mobile-workspace"></a>Pardavimo užsakymų mobiliosios darbo srities apžvalga
---------------------------------------------

Mobilioji darbo sritis **Pardavimo užsakymai** prisijungia prie „Microsoft Dynamics 365 for Operations“ ir suteikia jums galimybę peržiūrėti išsamią informaciją apie kiekvieną pardavimo užsakymą. Ši informacija apima užsakymo būseną, kliento kontaktinę informaciją ir užsakymo priėmėjo kontaktinę informaciją. Mobilioji darbo sritis **Pardavimo užsakymai** pateikia momentinį pardavimo užsakymų rodinį. Galite peržiūrėti visus užsakymus, pardavimo užsakymus pagal klientą arba informaciją apie konkretų pardavimo užsakymą. Mobilioji darbo sritis pateikia du rodinius, kad galėtumėte išsamiai analizuoti pardavimo užsakymus.

### <a name="view-all-sales-orders"></a>Peržiūrėti visus pardavimo užsakymus

Šiame rodinyje pateikiami visi pardavimo užsakymai.

-   Naudodami vieną iš šių filtrų, pasirinkite norimus peržiūrėti pardavimo užsakymus.
    -   Ieškoti pagal pardavimo užsakymą
    -   Ieškoti pagal kliento sąskaitą
    -   Ieškoti pagal kliento pavadinimą
    -   Ieškoti pagal būseną
    -   Ieškoti pagal išleidimo būseną
    -   Ieškoti pagal sukūrimo datą ir laiką
-   Pasirinkę pardavimo užsakymus, galite peržiūrėti išsamią konkrečių užsakymų informaciją. Tiksliau sakant, galite peržiūrėti šią informaciją:
    -   kliento pavadinimą ir adreso informaciją;
    -   įvairias pardavimo užsakymo datas, pvz., pageidaujamą siuntimo datą ir patvirtintą siuntimo datą;
    -   užsakymo priėmėjo kontaktinę informaciją;
    -   kliento kontaktinę informaciją;
    -   Užsakymo eilutės
    -   siuntas, parodančias kaip ir kada pardavimo užsakymas buvo pristatytas.

### <a name="view-orders-for-a-customer"></a>Kliento užsakymų rodinys

Šiame rodinyje pateikiami pardavimo užsakymai pagal klientą.

-   Naudodami šiuos filtrus peržiūrėkite kliento užsakymus.
    -   Ieškoti pagal pavadinimą
    -   Ieškoti pagal sąskaitą
-   Kai pasirenkate klientą, galite peržiūrėti šią informaciją:
    -   kliento pavadinimą ir grupę;
    -   kliento kontaktinę informaciją;
    -   kliento pardavimo užsakymus ir išsamią tų pardavimo užsakymų informaciją;
        -   kliento pavadinimą ir adreso informaciją;
        -   įvairias pardavimo užsakymo datas;
        -   užsakymo priėmėjo kontaktinę informaciją;
        -   kliento kontaktinę informaciją;
        -   Užsakymo eilutės
        -   siuntas, parodančias kaip ir kada pardavimo užsakymas buvo pristatytas.

## <a name="prerequisites"></a>Būtinieji komponentai
Prieš naudodami mobiliąją darbo sritį **Pardavimo užsakymai**, patikrinkite, ar sistemos administratorius nustatė toliau nurodytus būtinuosius komponentus.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Būtinoji sąlyga</th>
<th>Vaidmuo</th>
<th>aprašymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Reikia įdiegti „Dynamics 365 for Operations“ 1611 versiją ir 3 arba naujesnį platformos naujinimą.</td>
<td>Sistemos administratorius</td>
<td>Jei jūsų organizacijoje dar neįdiegta „Dynamics 365 for Operations“, sistemos administratorius turėtų peržiūrėti temą <a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">„Microsoft Dynamics 365 for Operations“ demonstracinės aplinkos diegimas</a>.</td>
</tr>
<tr class="even">
<td>Reikia įdiegti KB 4013633.</td>
<td>Sistemos administratorius</td>
<td>KB 4013633 (X ++ naujinimas arba metaduomenų karštoji pataisa) yra keturios mobiliosios darbo sritys, skirtos tiekimo grandinei valdyti. Norėdamas įdiegti KB 4013633, sistemos administratorius turi atlikti tolesnius veiksmus.
<ol>
<li>Atsisiųskite KB 4013633 iš „Microsoft Dynamics“ „Lifecycle Services“ (LCS).</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">Įdiekite metaduomenų karštąją pataisą</a>.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">Sukurkite diegiamą paketą</a>, kuriame yra modelis <strong>SCMMobile</strong>, o tada įkelkite diegiamą paketą į LCS.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">Taikykite diegiamą paketą</a> savo „Dynamics 365 for Operations“ sistemai.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobilioji darbo sritis <strong>Pardavimo užsakymai</strong> turi būti publikuojama mobiliojoje programoje „Dynamics 365 for Operations“.</td>
<td>Sistemos administratorius</td>
<td><ol>
<li>Atidarykite „Dynamics 365 for Operations“ savo naršyklėje.</li>
<li>Puslapyje <strong>Sistemos parametrai</strong> pasirinkite <strong>Valdyti mobiliąsias darbo sritis</strong>.</li>
<li>Pasirinkite darbo sritį <strong>Pardavimo užsakymai</strong>.</li>
<li>Spustelėkite <strong>Publikuoti mobiliąją darbo sritį</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Mobiliosios programos „Dynamics 365 for Operations“ atsisiuntimas ir diegimas
Iš mobiliųjų įrenginių programėlių parduotuvės atsisiųskite ir įdiekite mobiliąją programą „Dynamics 365 for Operations“.

-   „Android“: [„Dynamics 365 for Operations“ „Google Play“ parduotuvėje](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   „iPhone“: [„Dynamics 365 for Operations“ „iTunes “ programų parduotuvėje](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Prisijungimas prie mobiliosios programos „Dynamics 365 for Operations“
1.  Paleiskite programą savo mobiliajame įrenginyje.
2.  Įveskite savo „Dynamics 365 for Operations‟ URL.
3.  Įveskite įmonę, prie kurios norite prisijungti. Pavyzdžiui, įveskite **USMF**.
4.  Pirmą kartą prisijungus būsite paraginti įvesti savo „Dynamics 365 for Operations“ paskyros vartotojo vardą ir slaptažodį. Įveskite savo kredencialus.
5.  Prisijungę matysite galimas savo įmonės darbo sritis. Atkreipkite dėmesį, kad sistemos administratoriui paskelbus naują darbo sritį vėliau, galite patraukti, norėdami atnaujinti mobiliųjų darbo sričių sąrašą. 

    [![Patraukite norėdami atnaujinti](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-mobile-workspace"></a>Informacijos apie kliento pardavimo užsakymus peržiūra naudojant mobiliąją darbo sritį
1.  Savo mobiliajame įrenginyje pasirinkite darbo sritį **Pardavimo užsakymai**.
2.  Pasirinkite **Peržiūrėti kliento užsakymus**.
3.  Norėdami rasti klientą, naudokite sąskaitos arba kliento pavadinimo informaciją.
4.  Pasirinkite klientą.
5.  Pasirinkite **Kontaktinė informacija** arba **Pardavimo užsakymai**. Pasirinkus **Pardavimo užsakymai**, rodomas kliento pardavimo užsakymų sąrašas.
6.  Pasirinkite **Pardavimo užsakymas**. Dabar galite peržiūrėti informaciją apie pardavimo užsakymo eilutes, siuntas, kliento kontaktinę informaciją ir užsakymo priėmėjo kontaktinę informaciją.





