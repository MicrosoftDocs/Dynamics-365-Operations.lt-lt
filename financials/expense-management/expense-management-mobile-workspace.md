---
title: "Mobilioji darbo sritis Išlaidų valdymas"
description: "Šioje temoje pateikiama informacija apie išlaidų valdymo mobiliąją darbo sritį, kurią galima naudoti mobiliojoje programoje „Microsoft Dynamics 365 for Operations“. Ši darbo sritis vartotojams suteikia galimybę fiksuoti ir įkelti kvitą, kad jie galėtų jį pridėti prie išlaidų ataskaitos vėliau. Mobilioji darbo sritis taip pat vartotojams suteikia galimybę greitai kurti išlaidų eilutę naudojant pridėtą kvitą."
author: annbe
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: end user, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4e3202de8e5288bbd52e8c28922374de147cc99f
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="expense-management-mobile-workspace"></a>Mobilioji darbo sritis Išlaidų valdymas

[!include[banner](../includes/banner.md)]


Šioje temoje pateikiama informacija apie išlaidų valdymo mobiliąją darbo sritį, kurią galima naudoti mobiliojoje programoje „Microsoft Dynamics 365 for Operations“. Ši darbo sritis vartotojams suteikia galimybę fiksuoti ir įkelti kvitą, kad jie galėtų jį pridėti prie išlaidų ataskaitos vėliau. Mobilioji darbo sritis taip pat vartotojams suteikia galimybę greitai kurti išlaidų eilutę naudojant pridėtą kvitą.

<a name="overview-of-the-expense-management-mobile-workspace"></a>Išlaidų valdymo mobiliosios darbo srities apžvalga
---------------------------------------------------

Daugelis organizacijų reikalauja, kad prie kompensacijai gauti darbuotojo pateikiamos išlaidų ataskaitos būtų pridėta su kelionėmis arba verslu susijusio kvito kopija. Mobilioji darbo sritis **Išlaidų valdymas** vartotojams suteikia galimybę greitai kurti naujas išlaidų eilutes pasirinktame mobiliajame įrenginyje naudojant pridėtą kvito nuotrauką. Taip pat vartotojai gali nufotografuoti kvitą ir kopiją pridėti prie išlaidų ataskaitos vėliau. Tiksliau sakant, mobilioji darbo sritis **Išlaidų valdymas** vartotojams suteikia galimybę atlikti tolesnius veiksmus.

-   Nufotografuokite kvitą ir tada nuotrauką įkelkite į „Microsoft Dynamics 365 for Operations“. Tada vartotojas gali tą nuotrauką pridėti išlaidų ataskaitos vėliau.
-   Įkelkite failą kaip kvito nuotrauką. Tada vartotojas gali tą failą pridėti išlaidų ataskaitos vėliau.
-   Sukurkite naują išlaidų eilutę naudodami pridėtą kvitą. Tada vartotojas gali eilutės elementą pridėti prie išlaidų ataskaitos vėliau ir pateikti ją patvirtinti bei kompensacijai gauti.

Likusiuose šios temos skyriuose paaiškinama, kaip diegti ir naudoti mobiliąją darbo sritį **Išlaidų valdymas**.

## <a name="prerequisites"></a>Būtinieji komponentai
Prieš diegdami mobiliąją darbo sritį **Išlaidų valdymas**, patikrinkite, ar sistemos administratorius nustatė toliau nurodytus būtinuosius komponentus.

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
<td>Jei jūsų organizacijoje dar neįdiegta „Dynamics 365 for Operations“, jūsų sistemos administratorius turėtų peržiūrėti temą <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">„Microsoft Dynamics 365 for Operations“ demonstracinės aplinkos diegimas</a>.</td>
</tr>
<tr class="even">
<td>Reikia įdiegti KB 4019015.</td>
<td>Sistemos administratorius</td>
<td>KB 4019015 (X ++ naujinimas arba metaduomenų karštoji pataisa) yra keturios mobiliosios darbo sritys, skirtos tiekimo grandinei valdyti. Norėdamas įdiegti KB 4019015, sistemos administratorius turi atlikti tolesnius veiksmus.
<ol>
<li>Atsisiųskite KB 4019015 iš „Microsoft Dynamics“ „Lifecycle Services“ (LCS).</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Įdiekite metaduomenų karštąją pataisą</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Sukurkite diegiamą paketą</a>, kuriame yra modelis <strong>ApplicationSuite</strong> ir <strong>ExpenseMobile</strong>, o tada įkelkite diegiamą paketą į LCS.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Taikykite diegiamą paketą</a> savo „Dynamics 365 for Operations“ sistemai.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobilioji darbo sritis <strong>Išlaidų valdymas</strong> turi būti publikuojama mobiliojoje programoje „Dynamics 365 for Operations“.</td>
<td>Sistemos administratorius</td>
<td><ol>
<li>Atidarykite „Dynamics 365 for Operations“ savo naršyklėje.</li>
<li>Puslapyje <strong>Sistemos parametrai</strong> pasirinkite <strong>Valdyti mobiliąsias darbo sritis</strong>.</li>
<li>Pasirinkite darbo sritį <strong>Išlaidų valdymas</strong>.</li>
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

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Kvito kopijos kūrimas naudojant mobiliąją darbo sritį Išlaidų valdymas
1.  Savo mobiliajame įrenginyje pasirinkite darbo sritį **Išlaidų valdymas**.
2.  Pasirinkite **Kvito kopija**.
3.  Pasirinkite **Fotografuoti** arba **Pasirinkti vaizdą**.
4.  Jei pasirinkote **Fotografuoti**, atlikite tolesnius veiksmus.
    1.  Atidaromas jūsų mobiliojo įrenginio fotoaparatas, kad galėtumėte nufotografuoti kvitą. Nufotografavę spustelėkite **Gerai**, kad nuotrauką priimtumėte.
    2.  Pasirinktinai: įveskite nuotraukos pavadinimą ir bet kokias pastabas.

     **Arba**, jei pasirinkote **Pasirinkti vaizdą**, atlikite tolesnius šiuos veiksmus.
    1.  Sąraše pasirinkite vaizdą.
    2.  Pasirinktinai: įveskite vaizdo pavadinimą ir bet kokias pastabas.

5.  Pasirinkite **Atlikta**.

## <a name="quick-expense-entry-by-using-the-expense-management-mobile-workspace"></a>Greitas išlaidų įrašymas naudojant mobiliąją darbo sritį Išlaidų valdymas
1.  Savo mobiliajame įrenginyje pasirinkite darbo sritį **Išlaidų valdymas**.
2.  Pasirinkite **Greitas išlaidų įrašas**.
3.  Pasirinkite išlaidų kategoriją. Matysite išlaidų kategorijų, kurios įkeltos į jūsų programą ir kurias galima tvarkyti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama iki 50 prekių, tačiau kūrėjas šį skaičių gali keisti. Norėdami daugiau informacijos, kūrėjai turėtų peržiūrėti [„Dynamics 365 for Operations“ mobilioji platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform). Jei jūsų kategorija nėra įtraukta į sąrašą, pasirinkite **Ieškoti**, kad galėtumėte atlikti paiešką tinkle programoje „Dynamics 365 for Operations“. Ieškokite pagal išlaidų kategoriją arba perjunkite iešką pagal išlaidų tipą.
4.  Įveskite išlaidų operacijos datą.
5.  Pasirinktinai: įveskite išlaidų prekybininką.
6.  Įveskite išlaidų sumą.
7.  Pasirinkite išlaidų valiutą. Matysite išlaidų kodų, kurie įkelti į jūsų programą ir kuriuos galima tvarkyti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama iki 400 valiutų, tačiau kūrėjas šį skaičių gali keisti. Norėdami daugiau informacijos, kūrėjai turėtų peržiūrėti [„Dynamics 365 for Operations“ mobilioji platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform). Jei jūsų valiuta nėra įtraukta į sąrašą, pasirinkite **Ieškoti**, kad galėtumėte atlikti paiešką tinkle programoje „Dynamics 365 for Operations“. Ieškokite pagal valiutą arba perjunkite iešką pagal pavadinimą.
8.  Pasirinkite **Fotografuoti** arba **Pasirinkti vaizdą**.
9.  Jei pasirinkote **Fotografuoti**, atidaromas jūsų mobiliojo įrenginio fotoaparatas, kad galėtumėte nufotografuoti kvitą. Nufotografavę spustelėkite **Gerai**, kad nuotrauką priimtumėte.  Arba, jei pasirinkote **Pasirinkti vaizdą**, sąraše pasirinkite vaizdą.
10. Pasirinkite **Atlikta**.






