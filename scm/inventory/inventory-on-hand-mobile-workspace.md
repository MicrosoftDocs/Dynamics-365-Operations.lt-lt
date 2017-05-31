---
title: "Turimų atsargų mobilioji darbo sritis"
description: "Šioje temoje pateikiama informacija apie turimų atsargų mobiliąją darbo sritį, kurią galima naudoti mobiliojoje programoje „Microsoft Dynamics 365 for Operations“. Ši darbo sritis mobiliojoje aplinkoje suteikia įžvalgų apie rezervuotas ir turimas atsargas bet kur ir bet kada."
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
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7387df37e047d5ab7a90b696a6ffa249094499c4
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-on-hand-mobile-workspace"></a>Turimų atsargų mobilioji darbo sritis

[!include[banner](../includes/banner.md)]


Šioje temoje pateikiama informacija apie turimų atsargų mobiliąją darbo sritį, kurią galima naudoti mobiliojoje programoje „Microsoft Dynamics 365 for Operations“. Ši darbo sritis mobiliojoje aplinkoje suteikia įžvalgų apie rezervuotas ir turimas atsargas bet kur ir bet kada.

<a name="overview-of-the-inventory-on-hand-mobile-workspace"></a>Turimų atsargų mobiliosios darbo srities apžvalga
--------------------------------------------------

Paprastai įmonės kas dieną apdoroja daug atsargų siuntų ir gavimų. Dėl šių perkėlimų nuolat kinta turimų atsargų būsena. Mobilioji darbo sritis **Turimos atsargos** suteikia galimybę peržiūrėti turimų atsargų būseną visose įmonėse, todėl galite sužinoti naujausią informaciją apie atsargų duomenis savo pasirinktame mobiliajame įrenginyje. Nepriklausomai nuo to, ar dirbate sandėlyje, pirkimo, pardavimo, gamybos arba vadovybės skyriuje, ar turite kitų vaidmenų, turimų atsargų duomenis galite pasiekti bet kur ir bet kada. 

Mobilioji darbo sritis pateikia visų objektų turimų atsargų būsenos momentinį rodinį. Ji suteikia galimybę peržiūrėti visų objektų turimas atsargas, esamus medžiagų rezervavimus ir nerezervuotas turimas atsargas. Taip pat galite įvesti prekių numerius ir pateikti turimų atsargų užklausą bei atlikti filtruotą turimų produktų ar jų variantų iešką. 

Tiksliau sakant, mobilioji darbo sritis suteikia toliau nurodytas funkcijas.

-   Galite ieškoti pagal produkto numerį arba produkto pavadinimą, kad rastumėte produktus, kurių turimų atsargų būseną norite peržiūrėti.

-   Galite peržiūrėti toliau nurodytą informaciją apie pasirinktus produktus.
    -   Turimos atsargos pagal teritoriją
    -   Turimos atsargos pagal sandėlį
    -   Turimos atsargos pagal vietą
    -   Turimos atsargos pagal paketą (skirta paketais valdomiems produktams)
    -   Turimos atsargos pagal atsargų būseną
    
-   Produkto turimos atsargos rodomos toliau nurodytais būdais.
    -   Pagal faktines atsargas (Šis rodinys nurodo bendrą sumą.)
    -   Pagal faktines rezervuotas atsargas (Šis rodinys nurodo rezervuotą sumą.)
    -   Pagal turimas faktines atsargas (Šis rodinys nurodo turimą sumą, kuri nėra rezervuota.)

## <a name="prerequisites"></a>Būtinieji komponentai
Prieš naudodami mobiliąją darbo sritį **Turimos atsargos**, patikrinkite, ar sistemos administratorius nustatė toliau nurodytus būtinuosius komponentus.

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
<td>Reikia įdiegti „Microsoft Dynamics 365 for Operations“ 1611 versiją ir 3 arba naujesnį platformos naujinimą.</td>
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
<td>Mobilioji darbo sritis <strong>Turimos atsargos</strong> turi būti publikuojama mobiliojoje programoje „Dynamics 365 for Operations“.</td>
<td>Sistemos administratorius</td>
<td><ol>
<li>Atidarykite „Dynamics 365 for Operations“ savo naršyklėje.</li>
<li>Puslapyje <strong>Sistemos parametrai</strong> pasirinkite <strong>Valdyti mobiliąsias darbo sritis</strong>.</li>
<li>Pasirinkite darbo sritį <strong>Turimos atsargos</strong>.</li>
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

## <a name="view-the-onhand-inventory-for-a-product-by-using-the-inventory-onhand-mobile-workspace"></a>Produkto turimų atsargų peržiūra naudojant mobiliąją darbo sritį Turimos atsargos
1.  Savo mobiliajame įrenginyje pasirinkite darbo sritį **Turimos atsargos**.
2.  Pasirinkite **Patikrinti turimas prekės atsargas**. Matysite produktų, kurie įkelti į jūsų programą ir kuriuos galima tvarkyti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 50 prekių, tačiau kūrėjas šį skaičių gali keisti. Norėdami daugiau informacijos, kūrėjai turėtų peržiūrėti [„Dynamics 365 for Operations“ mobilioji platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
3.  Jei jūsų prekė nėra įtraukta į sąrašą, pasirinkite **Ieškoti daugiau**, kad galėtumėte atlikti paiešką tinkle programoje „Dynamics 365 for Operations“. Ieškokite pagal produkto numerį arba perjunkite iešką pagal produkto pavadinimą.
4.  Pasirinkite produktą. Jei prekei priskirtas vaizdas, jis bus rodomas.
5.  Pasirinkite vieną iš tolesnių parinkčių, kad peržiūrėtumėte turimų atsargų būseną.
    -   Peržiūrėti turimas atsargas pagal teritoriją
    -   Peržiūrėti turimas atsargas pagal sandėlį
    -   Peržiūrėti turimas atsargas pagal vietą
    -   Peržiūrėti turimas atsargas pagal paketą (skirta paketais valdomiems produktams)
    -   Peržiūrėti turimas atsargas pagal atsargų būseną

    Produkto turimos atsargos rodomos toliau nurodytais būdais.
    -   Pagal faktines atsargas (Šis rodinys nurodo bendrą sumą.)
    -   Pagal faktines rezervuotas atsargas (Šis rodinys nurodo rezervuotą sumą.)
    -   Pagal turimas faktines atsargas (Šis rodinys nurodo turimą sumą, kuri nėra rezervuota.)






