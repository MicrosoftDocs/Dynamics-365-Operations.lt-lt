---
title: Mobiliosios programos pagrindinis puslapis
description: Šioje temoje aprašoma mobiliųjų įrenginių programėlė „Finance and Operations“ („Dynamics 365“) ir pateikiamos nuorodos į išteklius, kurie jums gali padėti tai įgyvendinti savo organizacijoje.
author: ChrisGarty
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: intro-internal
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: cgarty
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: e13e99515d52e1e24970908a106ae99a7e8b0d80
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360821"
---
# <a name="mobile-app-home-page"></a>Mobiliosios programos pagrindinis puslapis

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma mobiliųjų įrenginių programėlė **„Finance and Operations“ („Dynamics 365“)** ir pateikiamos nuorodos į išteklius, kurie jums gali padėti tai įgyvendinti savo organizacijoje.

## <a name="overview"></a>Apžvalga

Mobilioji programa jūsų organizacijai suteikia galimybę pasiekti savo verslo procesus mobiliuosiuose įrenginiuose. Kai jūsų IT administratorius jūsų organizacijoje įjungia mobiliųjų darbo sričių funkciją, vartotojai gali prisijungti prie programos ir iš karto pradėti vykdyti verslo procesus iš savo mobiliųjų įrenginių. Mobilioji programa apima toliau nurodytas funkcijas, kurios gali padėti padidinti efektyvumą.

- Vartotojai gali peržiūrėti, redaguoti ir naudoti verslo duomenis net jei jų tinklo ryšys yra kintamas arba jų mobilieji įrenginiai yra visiškai neprisijungę. Kai įrenginys iš naujo užmezga ryšį, atsijungus atliktos duomenų operacijos yra automatiškai sinchronizuojamos.
- IT administratoriai arba kūrėjai gali kurti ir publikuoti mobiliąsias darbo sritis, kurios pritaikytos jų organizacijai. Programa naudoja jūsų esamą kodo turtą. Todėl jums nereikia iš naujo diegti tikrinimo procedūrų, verslo logikos arba saugos konfigūracijos.
- IT administratoriai arba kūrėjai gali lengvai kurti mobiliąsias darbo sritis naudodami nurodymo ir spustelėjimo tipo darbo sričių dizaino įrankį, įtrauktą į žiniatinklio klientą.
- IT administratoriai arba kūrėjai gali pasirinktinai optimizuoti darbo sričių naudojimo neprisijungus galimybes naudodami verslo logikos išplėtimo sistemą. Kadangi duomenys toliau apdoroti, kai įrenginys neprisijungęs, jūsų mobilieji scenarijai bus vaizdingi ir sklandūs net jei įrenginiai ne visada prijungti prie tinklo.

## <a name="elements-of-the-mobile-app"></a>Mobiliosios programos elementai
Mobiliosios programos naršymą sudaro keturios pagrindinės koncepcijos: ataskaitų sritis, darbo sritis, puslapiai ir veiksmai. 

[![Mobiliosios programos naršymo sąvokos.](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

1. Paleidus programą atidaroma **ataskaitų sritis**.
2. Ataskaitų srityje galite peržiūrėti paskelbtų **darbo sričių** sąrašą.
3. Kiekvienoje darbo srityje rodomas sąrašas, kuriame pateikti tos darbo srities **puslapiai**.
4. Būdami puslapyje, galite atlikti kelis veiksmus. Štai keletas pavyzdžių:

    - Peržiūrėti išsamius duomenis.
    - Atidaryti kitus susijusių duomenų, pvz., objekto informacijos arba eilučių, puslapius.
    - Peržiūrėti puslapyje pasiekiamų **veiksmų** sąrašą. Veiksmais galima kurti arba redaguoti esamus duomenis.

## <a name="implementation-process"></a>Diegimo procesas
Tolesnėje iliustracijoje parodytas mobiliųjų darbo sričių, kurias teikia „Microsoft“, ir pasirinktinių mobiliųjų darbo sričių diegimo procesas. 

[![Mobiliųjų programų diegimo procesas.](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)

Šioje lentelėje pateikiami saitai į išteklius, kurie gali padėti įdiegti mobiliąsias darbo sritis, kurias teikia „Microsoft“, ir pasirinktines mobiliąsias darbo sritis. Skaičiai pirmajame stulpelyje atitinka sunumeruotus veiksmus ankstesnėje iliustracijoje.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Žingsnis</th>
<th>Vaidmuo</th>
<th>Veiksmas</th>
<th>Ištekliai, kurie gali padėti atlikti veiksmus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Sistemos administratorius</td>
<td>Programos „Finance and Operations“ diegimas jūsų organizacijoje.</td>
<td><ul><li>Jei dar neįdiegėte&#39;kokios nors „Microsoft Dynamics 365“ versijos, žr. <a href="../deployment/deploy-demo-environment.md">Visuotinis demonstracinės aplinkos diegimas</a>.</li><li>Norėdami peržiūrėti mobiliųjų sričių, kurias galima naudoti, sąrašą, žr. <a href="mobile-workspaces-released.md">Neseniai išleistos mobiliosios darbo sritys</a>.</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>Sistemos administratorius</td>
<td><strong>Jei&#39;naudojate „Microsoft Dynamics 365 for Operations“ 1611 versiją:</strong> atsisiųskite ir įdiekite KB, kurie įgalina „Microsoft“ teikiamas mobiliąsias darbo sritis.</td>
<td>Daugiau informacijos ieškokite šiose temose:
<ul>

<li><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Išlaidų valdymo mobilioji darbo sritis</a></li>
<li><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Turimų atsargų mobilioji darbo sritis</a></li>
<li><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Pardavimo užsakymų mobilioji darbo sritis</a></li>
<li><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Tiekėjo bendradarbiavimo mobilioji darbo sritis</a></li>
<li><a href="/dynamics365/project-operations/prod-pma/project-time-entry-mobile-workspace">Projekto laiko įrašų mobilioji darbo sritis</a></li>
<li><a href="/dynamics365/project-operations/prod-exp/expense-management-mobile-workspace">Išlaidų valdymo mobilioji darbo sritis</a></li>

</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>Sistemos administratorius</td>
<td>Publikuokite „Microsoft“ teikiamas mobiliąsias darbo sritis.</td>
<td><a href="publish-mobile-workspace.md">Darbo srities publikavimas</a>
</td>
</tr>
<tr class="even">
<td>4</td>
<td>Kūrėjas arba nepriklausomas programinės įrangos tiekėjas (ISV)</td>
<td>Naudokite mobiliąją platformą pasirinktinėms mobiliosioms darbo sritims kurti.</td>
<td><a href="platform/mobile-platform-home-page.md">Mobilioji platforma</a></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV</td>
<td>Sukurkite diegiamą paketą, kuriame yra pasirinktinės mobiliosios darbo sritys, ir įkelkite paketą į „Microsoft Dynamics Lifecycle Services“ (LCS).</td>
<td><a href="../deployment/create-apply-deployable-package.md">Visuotinai diegiamo paketo kūrimas</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>Sistemos administratorius</td>
<td>Taikykite diegiamą paketą, kuriame yra nepriklausomo programinės įrangos tiekėjo (ISV) teikiamos pasirinktinės darbo sritys.</td>
<td><a href="../deployment/apply-deployable-package-system.md">Visuotinai diegiamo paketo taikymas</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Sistemos administratorius</td>
<td>Publikuokite ISV teikiamas pasirinktines mobiliąsias darbo sritis.</td>
<td><a href="publish-mobile-workspace.md">Mobiliosios darbo srities publikavimas</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Vartotojas</td>
<td>Atsisiųskite ir įdiekite mobiliąją programą.</td>
<td>
<a href="https://go.microsoft.com/fwlink/?linkid=850662">„Finance and Operations“ programa, skirta „Android“</a><BR/>
<a href="https://go.microsoft.com/fwlink/?linkid=850663">„Finance and Operations“ programa, skirta „iOS“</a><BR/>
(„Windows Phone“ nepalaikomas)
</td>
</tr>
<tr class="odd">
<td>9</td>
<td>Vartotojas</td>
<td>Prisijunkite ir naudokite mobiliąją programą. Į programą įtrauktos sistemos administratoriaus paskelbtos mobiliosios darbo sritys.</td>
<td>Norėdami peržiūrėti „Microsoft“ teikiamų mobiliųjų sričių sąrašą, žr. <a href="mobile-workspaces-released.md">Neseniai išleistos mobiliosios darbo sritys</a>.
</td>
</tr>
</tbody>
</table>

## <a name="troubleshooting"></a>Trikčių šalinimas
[Mobiliosios platformos ištekliai](platform/mobile-platform-home-page.md#troubleshooting-the-app)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]