---
title: "Pagrindinis mobiliųjų programų puslapis"
description: "Šioje temoje aprašoma mobilioji programa „Microsoft Dynamics 365 for Unified Operations“ ir pateikiami saitai į išteklius, kurie gali padėti programą įdiegti jūsų organizacijoje."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f4736a7041c746350fa073bd58929c840f7689bf
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="mobile-app-home-page"></a>Pagrindinis mobiliųjų programų puslapis

[!INCLUDE [banner](../includes/banner.md)]

Šioje temoje aprašoma mobilioji programa „Microsoft Dynamics 365 for Unified Operations“ ir pateikiami saitai į išteklius, kurie gali padėti programą įdiegti jūsų organizacijoje.

> [!NOTE]
> Anksčiau mobilioji programa vadinosi *„Microsoft Dynamics 365 for Finance and Operations‟*.

<a name="overview"></a>Apžvalga
--------

Mobilioji programa jūsų organizacijai suteikia galimybę pasiekti savo verslo procesus mobiliuosiuose įrenginiuose. Kai jūsų IT administratorius jūsų organizacijoje įjungia mobiliųjų darbo sričių funkciją, vartotojai gali prisijungti prie programos ir iš karto pradėti vykdyti verslo procesus iš savo mobiliųjų įrenginių. Mobilioji programa apima toliau nurodytas funkcijas, kurios gali padėti padidinti efektyvumą.

- Vartotojai gali peržiūrėti, redaguoti ir naudoti verslo duomenis net jei jų tinklo ryšys yra kintamas arba jų mobilieji įrenginiai yra visiškai neprisijungę. Kai įrenginys iš naujo užmezga ryšį, atsijungus atliktos duomenų operacijos yra automatiškai sinchronizuojamos su „Dynamics 365 for Finance and Operations“.
- IT administratoriai arba kūrėjai gali kurti ir publikuoti mobiliąsias darbo sritis, kurios pritaikytos jų organizacijai. Programa naudoja jūsų esamą kodo turtą. Todėl jums nereikia iš naujo diegti tikrinimo procedūrų, verslo logikos arba saugos konfigūracijos.
- IT administratoriai arba kūrėjai gali lengvai kurti mobiliąsias darbo sritis naudodami nurodymo ir spustelėjimo tipo darbo sričių dizaino įrankį, įtrauktą į žiniatinklio klientą.
- IT administratoriai arba kūrėjai gali pasirinktinai optimizuoti darbo sričių naudojimo neprisijungus galimybes naudodami verslo logikos išplėtimo sistemą. Kadangi duomenys toliau apdoroti, kai įrenginys neprisijungęs, jūsų mobilieji scenarijai bus vaizdingi ir sklandūs net jei įrenginiai ne visada prijungti prie tinklo.

## <a name="elements-of-the-mobile-app"></a>Mobiliosios programos elementai
Mobiliosios programos naršymą sudaro keturios pagrindinės koncepcijos: ataskaitų sritis, darbo sritis, puslapiai ir veiksmai. 

[![Mobiliosios programos naršymo sąvokos](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

1. Paleidus programą atidaroma **ataskaitų sritis**.
2. Ataskaitų srityje galite peržiūrėti paskelbtų **darbo sričių** sąrašą.
3. Kiekvienoje darbo srityje rodomas sąrašas, kuriame pateikti tos darbo srities **puslapiai**.
4. Būdami puslapyje, galite atlikti kelis veiksmus. Štai keletas pavyzdžių:

    - Peržiūrėti išsamius duomenis.
    - Atidaryti kitus susijusių duomenų, pvz., objekto informacijos arba eilučių, puslapius.
    - Peržiūrėti puslapyje pasiekiamų **veiksmų** sąrašą. Veiksmais galima kurti arba redaguoti esamus duomenis.

## <a name="implementation-process"></a>Diegimo procesas
Tolesnėje iliustracijoje parodytas mobiliųjų darbo sričių, kurias teikia „Microsoft“, ir pasirinktinių mobiliųjų darbo sričių diegimo procesas. 

![Mobiliųjų programų diegimo procesas](./media/Mobile-implementation-process-5.png)

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
<td>Įdiekite „Finance and Operations“ savo organizacijoje.</td>
<td><ul><li>Jei dar neįdiegėte kokios nors „Microsoft Dynamics 365‟ versijos, žr. <a href="../deployment/deploy-demo-environment.md">Visuotinis demonstracinės aplinkos diegimas</a>.</li><li>Norėdami peržiūrėti mobiliųjų sričių, kurias galima naudoti, sąrašą, žr. <a href="mobile-workspaces-released.md">Neseniai išleistos mobiliosios darbo sritys</a>.</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>Sistemos administratorius</td>
<td><strong>Jei naudojate „Microsoft Dynamics 365 for Operations“ 1611 versiją:</strong> atsisiųskite ir įdiekite KB, kurie įgalina „Microsoft“ teikiamas mobiliąsias darbo sritis.</td>
<td>Daugiau informacijos ieškokite šiose temose:
<ul>

<li><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Išlaidų valdymo mobilioji darbo sritis</a></li>
<li><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Turimų atsargų mobilioji darbo sritis</a></li>
<li><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Pardavimo užsakymų mobilioji darbo sritis</a></li>
<li><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Tiekėjo bendradarbiavimo mobilioji darbo sritis</a></li>
<li><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Projekto laiko įrašų mobilioji darbo sritis</a></li>
<li><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Išlaidų valdymo mobilioji darbo sritis</a></li>

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
<td>Sukurkite diegiamą paketą, kuriame yra pasirinktinės mobiliosios darbo sritys, ir įkelkite paketą į „Microsoft Dynamics“ „Lifecycle Services“ (LCS).</td>
<td><a href="../deployment/create-apply-deployable-package.md">Diegiamo paketo kūrimas</a></td>
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
<td><ul>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850662">„Android“ telefonams</a></li>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850663">Telefonams „iPhone“</a></li></ul>
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

