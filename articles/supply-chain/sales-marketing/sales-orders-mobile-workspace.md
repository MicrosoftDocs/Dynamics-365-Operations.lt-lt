---
title: Mobilioji darbo sritis Pardavimo užsakymai
description: Šioje temoje pateikiama informacijos apie mobiliąją darbo sritį Pardavimo užsakymai. Ši darbo sritis suteikia galimybę bet kur ir bet kada peržiūrėti naujausią pardavimo užsakymų informaciją.
author: Mirzaab
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 9dbef5a3071eea0514bc656477001358c6a5b561
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910334"
---
# <a name="sales-orders-mobile-workspace"></a>Mobilioji darbo sritis Pardavimo užsakymai

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacijos apie mobiliąją darbo sritį **Pardavimo užsakymai**. Ši darbo sritis suteikia galimybę bet kur ir bet kada peržiūrėti naujausią pardavimo užsakymų informaciją. 

Ši mobili darbo sritis skirta naudoti kartu su mobiliųjų įrenginių programėle „Finance and Operations“.

## <a name="overview"></a>Peržiūra
Mobiliojoje darbo srityje **Pardavimo užsakymai** galite peržiūrėti išsamią informaciją apie kiekvieną pardavimo užsakymą. Ši informacija apima užsakymo būseną, kliento kontaktinę informaciją ir užsakymo priėmėjo kontaktinę informaciją. Mobilioji darbo sritis **Pardavimo užsakymai** pateikia momentinį pardavimo užsakymų rodinį. Galite peržiūrėti visus užsakymus, pardavimo užsakymus pagal klientą arba informaciją apie konkretų pardavimo užsakymą. 

Mobilioji darbo sritis pateikia du rodinius, kad galėtumėte išsamiai analizuoti pardavimo užsakymus.

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
Būtinosios sąlygos skiriasi priklausomai nuo jūsų organizacijoje visuotinai įdiegtos „Microsoft Dynamics 365“ versijos.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Būtinosios sąlygos naudojant „Supply Chain Management” 
Jei jūsų organizacijoje įdiegtas „Supply Chain Management”, sistemos administratorius turi publikuoti mobiliąją darbo sritį **Pardavimo užsakymai**. Instrukcijų ieškokite dalyje [Mobiliosios darbo srities publikavimas](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Būtinosios sąlygos, jei naudojate „Dynamics 365 for Operations“ 1611 versiją su 3 platformos naujinimu arba naujesnę versiją
Jei jūsų organizacijoje visuotinai įdiegta „Dynamics 365 for Operations“ 1611 versija su 3 platformos naujinimu arba naujesnė versija, sistemos administratorius turi įvykdyti tolesnes būtinąsias sąlygas. 

<table>
<thead>
<tr class="header">
<th>Būtinoji sąlyga</th>
<th>Vaidmuo</th>
<th>aprašymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Įdiegti KB 4013633.</td>
<td>Sistemos administratorius</td>

<td>KB 4013633 yra X++ naujinimas arba karštoji metaduomenų pataisa su mobiliąja darbo sritimi <strong>Pardavimo užsakymai</strong>. Norėdamas įdiegti KB 4013633, sistemos administratorius turi atlikti tolesnius veiksmus.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Atsisiųsti metaduomenų karštąją pataisą iš „Microsoft Dynamics Lifecycle Services“ (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Įdiekite metaduomenų karštąją pataisą</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Sukurkite diegiamą paketą</a>, kuriame yra modelis <strong>SCMMobile</strong>, o tada įkelkite diegiamą paketą į LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Visuotinai diegiamo paketo taikymas</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publikuoti mobiliąją darbo sritį <strong>Pardavimo užsakymai</strong>.</td>
<td>Sistemos administratorius</td>
<td>Žr. <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiliosios darbo srities publikavimas</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobiliosios programos atsisiuntimas ir diegimas
Mobiliosios programos „Finance and Operations“ atsisiuntimas ir diegimas.

-   [„Android“ telefonams](https://go.microsoft.com/fwlink/?linkid=850662)
-   [„iPhone“ telefonams](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Prisijunkite prie mobiliosios programos

1.  Paleiskite programą savo mobiliajame įrenginyje.
2.  Įveskite savo „Dynamics 365“ URL.
3.  Kai prisijungsite pirmą kartą, bus rodomas raginimas įvesti savo vartotojo vardą ir slaptažodį. Įveskite savo kredencialus.
4.  Prisijungus rodomos galimos jūsų įmonės darbo sritys. Atkreipkite dėmesį, kad sistemos administratoriui paskelbus naują darbo sritį vėliau turėsite atnaujinti mobiliųjų darbo sričių sąrašą.

[![Patraukite norėdami atnaujinti](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-sales-order-mobile-workspace"></a>Informacijos apie kliento pardavimo užsakymus peržiūra naudojant mobiliąją darbo sritį Pardavimo užsakymai

1.  Savo mobiliajame įrenginyje pasirinkite darbo sritį **Pardavimo užsakymai**.
2.  Pasirinkite **Peržiūrėti kliento užsakymus**.
3.  Norėdami rasti klientą, naudokite sąskaitos arba kliento pavadinimo informaciją.
4.  Pasirinkite klientą.
5.  Pasirinkite **Kontaktinė informacija** arba **Pardavimo užsakymai**. Pasirinkus **Pardavimo užsakymai**, rodomas kliento pardavimo užsakymų sąrašas.
6.  Pasirinkite **Pardavimo užsakymas**. Dabar galite peržiūrėti informaciją apie pardavimo užsakymo eilutes, siuntas, kliento kontaktinę informaciją ir užsakymo priėmėjo kontaktinę informaciją.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]