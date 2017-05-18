---
title: "Projekto laiko įrašo darbo sritis, skirta programai „Dynamics 365 for Operations“"
description: "Šioje temoje pateikiama informacija apie projekto laiko įrašo mobiliąją darbo sritį. Šioje darbo srityje vartotojai gali įvesti ir įrašyti laiką pagal projektą, naudodami savo mobilųjį įrenginį."
author: annbe
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e3e0be36c045acc3750efbb739d79d81ab937c65
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="project-time-entry-mobile-workspace"></a>Projekto laiko įrašo mobilioji darbo sritis

[!include[banner](../includes/banner.md)]

„[!include[banner](../includes/banner.md)]“


Šioje temoje pateikiama informacija apie projekto laiko įrašo mobiliąją darbo sritį, kurią galima naudoti mobiliojoje programoje „Dynamics 365 for Operations“. Šioje darbo srityje vartotojai gali įvesti ir įrašyti laiką pagal projektą, naudodami savo mobilųjį įrenginį.

<a name="overview-of-the-project-time-entry-mobile-workspace"></a>Projekto laiko įrašo mobiliosios darbo srities apžvalga
---------------------------------------------------

Atlikdami kasdienes užduotis projekto ištekliai dažnai būna teritorijoje arba kelionėje. Mobilioji darbo sritis **Projekto laiko įrašas** vartotojams suteikia galimybę įvesti savo apmokamą arba neapmokamą laiką pagal projektą savo pasirinktame mobiliajame įrenginyje. Todėl projekto ištekliai laiko įrašus gali įrašyti visada ir visur. Taip pat jie gali peržiūrėti jau įrašytus laiko įrašus. 

Tiksliau sakant, mobilioji darbo sritis **Projekto laiko įrašas** suteikia toliau nurodytas funkcijas.

-   Įvesti bet kurios pasirinktos dienos valandų, sugaištų tam tikrai užduočiai atlikti, skaičių.
-   Ieškoti pagal projekto pavadinimą arba klientą ir rasti projektą, kuriam reikia priskirti laiko įrašą.
-   Nurodyti sugaišto laiko kategoriją ir veiklą.
-   Įrašyti projekto laiką kaip apmokamą arba neapmokamą.
-   Pasirinktinai įvesti bet kokių išorinių arba vidinių komentarų.

Norėdami diegti mobiliąją darbo sritį **Projekto laiko įrašas**, žr. tolesnius šios temos skyrius.

## <a name="prerequisites"></a>Būtinieji komponentai
Prieš diegdami mobiliąją darbo sritį **Projekto laiko įrašas**, patikrinkite, ar sistemos administratorius nustatė toliau nurodytus būtinuosius komponentus.

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
<td>Jei jūsų organizacijoje dar neįdiegta „Dynamics 365 for Operations“, jūsų sistemos administratorius turėtų peržiūrėti temą <a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">„Microsoft Dynamics 365 for Operations“ demonstracinės aplinkos diegimas</a>.</td>
</tr>
<tr class="even">
<td>Reikia įdiegti KB 4018050.</td>
<td>Sistemos administratorius</td>
<td>KB 4018050 yra X++ atnaujinimas arba metaduomenų karštoji pataisa, kurioje yra mobilioji darbo sritis <strong>Projekto laiko įrašas</strong>. Norėdamas įdiegti KB 4018050, sistemos administratorius turi atlikti tolesnius veiksmus.
<ol>
<li>Atsisiųskite KB 4018050 iš „Microsoft Dynamics“ „Lifecycle Services“ (LCS).</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Įdiekite metaduomenų karštąją pataisą</a>.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Sukurkite diegiamą paketą</a>, kuriame yra modeliai <strong>ApplicationSuite</strong> ir <strong>ProjectMobile</strong>, o tada įkelkite diegiamą paketą į LCS.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Taikykite diegiamą paketą</a> savo „Dynamics 365 for Operations“ sistemai.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobilioji darbo sritis <strong>Projekto laiko įrašas</strong> turi būti publikuojama mobiliojoje programoje „Dynamics 365 for Operations“.</td>
<td>Sistemos administratorius</td>
<td><ol>
<li>Atidarykite „Dynamics 365 for Operations“ savo naršyklėje.</li>
<li>Puslapio <strong>Sistemos parametrai</strong> skirtuke <strong>Valdyti mobiliąsias darbo sritis</strong> pasirinkite darbo sritį <strong>Projekto laiko įrašas</strong>.</li>
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

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Laiko įvedimas naudojant mobiliąją darbo sritį Projekto laiko įrašas
1.  Savo mobiliajame įrenginyje pasirinkite darbo sritį **Projekto laiko įrašas**.
2.  Pasirinkite **Laiko įrašas**. Matysite dabartinės savaitės kalendoriaus datas.
3.  Pasirinkite datą ir pasirinkite **Veiksmai** &gt; **Naujas įrašas**.
4.  Įveskite valandų, kurias reikia įrašyti, skaičių.
5.  Pasirinkite laiko įrašo projektą. Matysite projektų, kurie įkelti į jūsų programą ir kuriuos galima tvarkyti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 50 prekių, tačiau kūrėjas šį skaičių gali keisti. Norėdami daugiau informacijos, kūrėjai turėtų peržiūrėti [„Dynamics 365 for Operations“ mobilioji platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
6.  Jei jūsų projektas nėra įtrauktas į sąrašą, pasirinkite **Ieškoti**, kad galėtumėte atlikti paiešką tinkle programoje „Dynamics 365 for Operations“. Ieškokite pagal pavadinimą arba perjunkite iešką pagal projekto pavadinimą arba klientą.
7.  Pasirinkite kategoriją. Matysite kategorijų, kurios įkeltos į jūsų programą ir kurias galima tvarkyti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 50 prekių, tačiau kūrėjas šį skaičių gali keisti. Norėdami daugiau informacijos, kūrėjai turėtų peržiūrėti [„Dynamics 365 for Operations“ mobilioji platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
8.  Jei jūsų kategorija nėra įtraukta į sąrašą, pasirinkite **Ieškoti**, kad galėtumėte atlikti paiešką tinkle programoje „Dynamics 365 for Operations“. Ieškokite pagal kategoriją arba perjunkite iešką pagal kategorijos pavadinimą.
9.  Pasirinkite veiklą. Matysite veiklų, kurios įkeltos į jūsų programą ir kurias galima tvarkyti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 50 prekių, tačiau kūrėjas šį skaičių gali keisti. Norėdami daugiau informacijos, kūrėjai turėtų peržiūrėti [„Dynamics 365 for Operations“ mobilioji platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
10. Jei jūsų veikla nėra įtraukta į sąrašą, pasirinkite **Ieškoti**, kad galėtumėte atlikti paiešką tinkle programoje „Dynamics 365 for Operations“. Ieškokite pagal veiklos numerį arba perjunkite iešką pagal paskirtį.
11. Pasirinkite eilutės ypatybę.
12. Pasirinktinai: įveskite bet kokių išorinių arba vidinių komentarų.
13. Pasirinkite **Atlikta**.






