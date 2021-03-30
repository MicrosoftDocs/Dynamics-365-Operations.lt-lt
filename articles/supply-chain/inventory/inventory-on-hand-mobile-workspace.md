---
title: Turimų atsargų mobilioji darbo sritis
description: Šioje temoje pateikiama informacija apie mobiliąją darbo sritį Turimos atsargos. Ši darbo sritis mobiliojoje aplinkoje suteikia įžvalgų apie rezervuotas ir turimas atsargas bet kur ir bet kada.
author: Mirzaab
manager: tfehr
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 2c84b868247503f8fcb8f718f4ce9bd6ccb56c99
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217130"
---
# <a name="inventory-on-hand-mobile-workspace"></a>Turimų atsargų mobilioji darbo sritis

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie mobiliąją darbo sritį **Turimos atsargos**. Ši darbo sritis suteikia įžvalgų apie rezervuotas ir turimas atsargas bet kur ir bet kada.

Ši mobili darbo sritis skirta naudoti kartu su mobiliųjų įrenginių programėle „Finance and Operations“.

## <a name="overview"></a>Peržiūra
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
Būtinosios sąlygos skiriasi ir priklauso nuo jūsų organizacijoje įdiegtos „Supply Chain Management” versijos.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Būtinosios sąlygos naudojant Tiekimo grandinės valdymą
Jei jūsų organizacijoje visuotinai įdiegta „Supply Chain Management“, sistemos administratorius turi paskelbti mobiliąją darbo sritį **Turimos atsargos**. Instrukcijų ieškokite dalyje [Mobiliosios darbo srities publikavimas](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-platform-update-3-or-later"></a>Būtinosios sąlygos, jei naudojate 3 platformos naujinimą arba naujesnę versiją 
Jei jūsų organizacijoje visuotinai įdiegta 3 platformos naujinimo arba naujesnė versija, sistemos administratorius turi įvykdyti tolesnes būtinąsias sąlygas. 

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

<td>KB 4013633 yra X++ naujinimas arba metaduomenų karštoji pataisa, kurioje yra mobilioji darbo sritis <strong>Turimos atsargos</strong>. Norėdamas įdiegti KB 4013633, sistemos administratorius turi atlikti tolesnius veiksmus.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Atsisiųsti metaduomenų karštąją pataisą iš „Microsoft Dynamics Lifecycle Services“ (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Įdiekite metaduomenų karštąją pataisą</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Sukurkite diegiamą paketą</a>, kuriame yra modelis <strong>SCMMobile</strong>, o tada įkelkite diegiamą paketą į LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Visuotinai diegiamo paketo taikymas</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Paskelbkite mobiliąją darbo sritį <strong>Turimos atsargos</strong>.</td>
<td>Sistemos administratorius</td>
<td>Žr. <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiliosios darbo srities publikavimas</a>.</td>
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

## <a name="view-the-on-hand-inventory-for-a-product-by-using-the-inventory-on-hand-mobile-workspace"></a>Produkto turimų atsargų peržiūra naudojant mobiliąją darbo sritį Turimos atsargos

1.  Savo mobiliajame įrenginyje pasirinkite darbo sritį **Turimos atsargos**.

2.  Pasirinkite **Patikrinti turimas prekės atsargas**. Matysite produktų, kurie įkelti į jūsų programą ir kuriuos galima tvarkyti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 50 prekių, tačiau kūrėjas šį skaičių gali keisti. Norėdami gauti daugiau informacijos, programuotojai turėtų peržiūrėti temą [Mobilioji platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
3.  Jei jūsų prekės nėra sąraše, pasirinkite **Ieškoti daugiau**. Ieškokite pagal produkto numerį arba perjunkite iešką pagal produkto pavadinimą.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]