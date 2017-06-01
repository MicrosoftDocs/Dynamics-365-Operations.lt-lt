---
title: "Mobilioji darbo sritis Išlaidų kontrolė"
description: "Šioje temoje pateikiama informacija apie išlaidų kontrolės mobiliąją darbo sritį, kurią galima naudoti mobiliojoje programoje „Microsoft Dynamics 365 for Operations“. Ši darbo sritis išlaidų centro vadovams suteikia galimybę peržiūrėti informaciją apie išlaidų centro efektyvumą bet kuriuo metu ir bet kurioje vietoje."
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 09383c24b0dd2ad61a836f6c8dc97f4389915772
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="cost-controlling-mobile-workspace"></a>Mobilioji darbo sritis Išlaidų kontrolė

[!include[banner](../includes/banner.md)]


Šioje temoje pateikiama informacija apie išlaidų kontrolės mobiliąją darbo sritį, kurią galima naudoti mobiliojoje programoje „Microsoft Dynamics 365 for Operations“. Ši darbo sritis išlaidų centro vadovams suteikia galimybę peržiūrėti informaciją apie išlaidų centro efektyvumą bet kuriuo metu ir bet kurioje vietoje. 

<a name="overview-of-the-cost-controlling-mobile-workspace"></a>Išlaidų kontrolės mobiliosios darbo srities apžvalga
-------------------------------------------------

Mobilioji darbo sritis **Išlaidų kontrolė** suteikia esamo išlaidų centrų efektyvumo momentinį rodinį, palygindama faktines išlaidas ir biudžeto išlaidas. Galite detalizuoti atskirų išlaidų elementų būsenas. 

Pavyzdžiui, darbuotojas gauna kvietimą į tarptautinę konferenciją, bet organizacija turi padengti visas kelionės išlaidas. Darbuotojas klausia savo vadovo, ar jis gali dalyvauti konferencijoje. Vadovas greitai atidaro mobiliąją darbo sritį **Išlaidų kontrolė** savo mobiliajame įrenginyje, kad peržiūrėtų biudžetą ir nuspręstų, ar darbuotojas gali dalyvauti konferencijoje.

### <a name="data-security"></a>Duomenų sauga

Duomenys mobiliojoje darbo srityje **Išlaidų kontrolė** apsaugoti naudojant vartotojo kredencialus. Išlaidų centro vadovai gali peržiūrėti tik savo išlaidų centro duomenis. Prieigos lygio apsauga valdoma modulyje **Išlaidų apskaita**. 

Išlaidų buhalteriai nurodo mobiliosios darbo srities **Išlaidų kontrolė** konfigūraciją modulyje **Išlaidų apskaita**. Kai darbo sritis publikuojama mobiliojoje programoje „Microsoft Dynamics 365 for Operations“, programoje ją galima pasiekti. Todėl visi išlaidų centrų vadovai organizacijoje duomenis gali peržiūrėti tuo pačiu formatu.

### <a name="actions-views-and-links"></a>Veiksmai, rodiniai ir saitai

Mobiliojoje darbo srityje **Išlaidų kontrolė**, skirtoje programai „Dynamics 365 for Operations“, pateikiami toliau nurodyti veiksmai, rodiniai ir saitai.

-   **Veiksmai**
    -   Naudokite **Pasirinkti konfigūraciją**, kad pasirinktumėte maketą.
    -   Naudokite **Pasirinkti išlaidų objektą**, kad pasirinktumėte išlaidų centrus, pagal kuriuos norite filtruoti duomenis. **Pastaba:** sąraše rodomi išlaidų centrai priklauso nuo modulyje **Išlaidų apskaita** suteiktos prieigos.
-   **Rodiniai:** priklausomai nuo pasirinktų veiksmų ir konfigūracijos modulyje **Išlaidų kontrolė**, galite peržiūrėti toliau nurodytą kortelių informaciją.
    -   Faktinė ir biudžeto sumos (dabartinis laikotarpis)
    -   Faktinė ir patikslinta biudžeto sumos (dabartinis laikotarpis)
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
    
    [![Išlaidų elemento kortelė](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="prerequisites"></a>Būtinieji komponentai
Prieš naudodami mobiliąją darbo sritį **Išlaidų kontrolė**, patikrinkite, ar sistemos administratorius nustatė toliau nurodytus būtinuosius komponentus.

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
<td>Jei jūsų organizacijoje dar neįdiegta „Dynamics 365 for Operations“, sistemos administratorius turėtų peržiūrėti temą <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">„Microsoft Dynamics 365 for Operations“ demonstracinės aplinkos diegimas</a>.</td>
</tr>
<tr class="even">
<td>Reikia įdiegti KB 4013633.</td>
<td>Sistemos administratorius</td>
<td>KB 4013633 (X ++ naujinimas arba metaduomenų karštoji pataisa) yra keturios mobiliosios darbo sritys, skirtos tiekimo grandinei valdyti. Norėdamas įdiegti KB 4013633, sistemos administratorius turi atlikti tolesnius veiksmus.
<ol>
<li>Atsisiųskite KB 4013633 iš „Microsoft Dynamics“ „Lifecycle Services“ (LCS).</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Įdiekite metaduomenų karštąją pataisą</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Sukurkite diegiamą paketą</a>, kuriame yra modelis <strong>SCMMobile</strong>, o tada įkelkite diegiamą paketą į LCS.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Taikykite diegiamą paketą</a> savo „Dynamics 365 for Operations“ sistemai.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobilioji darbo sritis <strong>Išlaidų kontrolė</strong> turi būti publikuojama mobiliojoje programoje „Dynamics 365 for Operations“.</td>
<td>Sistemos administratorius</td>
<td><ol>
<li>Atidarykite „Dynamics 365 for Operations“ savo naršyklėje.</li>
<li>Puslapyje <strong>Sistemos parametrai</strong> pasirinkite <strong>Valdyti mobiliąsias darbo sritis</strong>.</li>
<li>Pasirinkite darbo sritį <strong>Išlaidų objekto peržiūra</strong>.</li>
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





