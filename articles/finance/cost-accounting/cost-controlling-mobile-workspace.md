---
title: Mobilioji darbo sritis Išlaidų kontrolė
description: Šioje temoje pateikiama informacija apie mobiliąją darbo sritį Savikainos kontrolė. Ši darbo sritis išlaidų centro vadovams suteikia galimybę peržiūrėti informaciją apie išlaidų centro efektyvumą bet kuriuo metu ir bet kurioje vietoje.
author: AndersGirke
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMMobileCostObjectOverviewDetailsCurrentPeriod, CAMMobileCostObjectList, CAMMobileCostObjectOverviewDetailsPreviousPeriod, CAMMobileCostObjectOverview, CAMMobileCostObjectOverviewDetailsYearToDate, CAMMobileCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 569f932b256054f2d93a6d699ca5d5af3da08ca6
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897941"
---
# <a name="cost-controlling-mobile-workspace"></a>Mobilioji darbo sritis Išlaidų kontrolė

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie mobiliąją darbo sritį **Savikainos kontrolė**. Ši darbo sritis išlaidų centro vadovams suteikia galimybę peržiūrėti informaciją apie išlaidų centro efektyvumą bet kuriuo metu ir bet kurioje vietoje.

Ši mobili darbo sritis skirta naudoti kartu su mobiliųjų įrenginių programėle „Finance and Operations“.

## <a name="overview"></a>Peržiūra
Mobilioji darbo sritis **Išlaidų kontrolė** suteikia esamo išlaidų centrų efektyvumo momentinį rodinį, palygindama faktines išlaidas ir biudžeto išlaidas. Galite detalizuoti atskirų išlaidų elementų būseną.

Pavyzdžiui, darbuotojas gauna kvietimą į tarptautinę konferenciją, bet organizacija turi padengti visas kelionės išlaidas. Darbuotojas klausia savo vadovo, ar jis gali dalyvauti konferencijoje. Vadovas greitai atidaro mobiliąją darbo sritį **Išlaidų kontrolė** savo mobiliajame įrenginyje, kad peržiūrėtų biudžetą ir nuspręstų, ar darbuotojas gali dalyvauti konferencijoje.

### <a name="data-security"></a>Duomenų sauga
Duomenys mobiliojoje darbo srityje **Išlaidų kontrolė** apsaugoti naudojant vartotojo kredencialus. Išlaidų centro vadovai gali peržiūrėti tik savo išlaidų centro duomenis. Prieigos lygio apsauga valdoma modulyje **Išlaidų apskaita**.

Išlaidų buhalteriai nurodo mobiliosios darbo srities **Išlaidų kontrolė** konfigūraciją modulyje **Išlaidų apskaita**. Kai darbo sritis publikuojama mobiliojoje programoje, ją galima pasiekti programoje. Todėl visi išlaidų centrų vadovai organizacijoje duomenis gali peržiūrėti tuo pačiu formatu.

### <a name="actions-views-and-links"></a>Veiksmai, rodiniai ir saitai
Mobiliojoje darbo srityje **Savikainos kontrolė** pateikiami šie veiksmai, rodiniai ir nuorodos:

-   **Veiksmai**

    -   Naudokite **Pasirinkti konfigūraciją**, kad pasirinktumėte maketą.
    -   Naudokite **Pasirinkti išlaidų objektą**, kad pasirinktumėte išlaidų centrus, pagal kuriuos norite filtruoti duomenis.
    
        > [!NOTE]
        > Sąraše rodomi išlaidų centrai priklauso nuo modulyje **Kaštų apskaita** suteiktos prieigos.

-   **Rodiniai:** priklausomai nuo pasirinktų veiksmų ir konfigūracijos modulyje **Kaštų apskaita**, galite peržiūrėti toliau nurodytą kortelių informaciją.

    -   Faktinis, palyginti su biudžeto (dabartinis laikotarpis)
    -   Faktinis, palyginti su patikslinto biudžeto (dabartinis laikotarpis)
    -   Faktinė ir biudžeto sumos (ankstesnis laikotarpis)
    -   Faktinė ir patikslinta biudžeto sumos (ankstesnis laikotarpis)
    -   Faktinė ir biudžeto sumos (nuo metų pradžios iki šios dienos)
    -   Faktinė ir patikslinta biudžeto sumos (nuo metų pradžios iki šios dienos)

    Šios sumos rodomos kiekvienoje kortelėje: Faktinė, Biudžeto, Nuokrypio ir Nuokrypio %.

-   **Saitai**

    -   Dabartinio laikotarpio informacija
    -   Ankstesnio laikotarpio informacija
    -   Informacija nuo metų pradžios iki šiandien

    Pasirinkus saitą, rodoma kiekvieno išlaidų elemento kortelė. Šios sumos rodomos kiekvienoje kortelėje: Faktinė, Biudžeto, Biudžeto nuokrypio, Biudžeto nuokrypio %, Patikslinta biudžeto, Patikslinta biudžeto nuokrypio ir Patikslinta biudžeto nuokrypio %.
    
    [![Išlaidų elemento kortelė](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>Būtinieji komponentai
Būtinosios sąlygos skiriasi priklausomai nuo jūsų organizacijoje visuotinai įdiegtos „Microsoft Dynamics 365“ versijos.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a>Būtinosios sąlygos, jeigu naudojate „Microsoft Dynamics 365 Finance“
Jei jūsų organizacijoje įdiegtas „Finance“, sistemos administratorius turi paskelbti mobiliąją darbo sritį **Savikainos kontrolė**. Instrukcijų ieškokite dalyje [Mobiliosios darbo srities publikavimas](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Būtinosios sąlygos, jei naudojate 1611 versiją su 3 platformos naujinimu arba naujesnę versiją
Jei jūsų organizacijoje visuotinai įdiegta 1611 versija su 3 platformos naujinimu arba naujesnė versija, sistemos administratorius turi įvykdyti tolesnes būtinąsias sąlygas.

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

<td>KB 4013633 yra X++ naujinimas arba karštoji metaduomenų pataisa su mobiliąja darbo sritimi <strong>Savikainos kontrolė</strong>. Norėdamas įdiegti KB 4013633, sistemos administratorius turi atlikti tolesnius veiksmus.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Atsisiųsti metaduomenų karštąją pataisą iš „Microsoft Dynamics Lifecycle Services“ (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Įdiekite metaduomenų karštąją pataisą</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Sukurkite diegiamą paketą</a>, kuriame yra modelis <strong>SCMMobile</strong>, o tada įkelkite diegiamą paketą į LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Visuotinai diegiamo paketo taikymas</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Mobiliosios darbo srities <strong>Savikainos kontrolė</strong> publikavimas</td>
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

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a>Išlaidų centro efektyvumo peržiūra naudojant išlaidų kontrolės mobiliąją darbo sritį

1.  Savo mobiliajame įrenginyje pasirinkite darbo sritį **Išlaidų valdymas**.
2.  Pasirinkite **Išlaidų objekto valdymas**.
3.  Pasirinkite **Veiksmai**.
4.  Pasirinkite **Pasirinkti konfigūraciją**, kad pasirinktumėte išlaidų valdymo maketą.
5.  Pasirinkite **Atlikta**.
6.  Pasirinkite **Veiksmai**.
7.  Pasirinkite **Pasirinkti išlaidų objektą**, kad pasirinktumėte išlaidų centrus, prie kurių turite prieigą.
8.  Pasirinkite **Atlikta**.
9.  Peržiūrėkite bendrą išlaidų centro efektyvumą.
10. Pasirinkite saitą **Dabartinio laikotarpio informacija**.
11. Peržiūrėkite atskirų išlaidų elementų efektyvumą.
12. Taip pat galite ieškoti konkrečių išlaidų elementų.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]