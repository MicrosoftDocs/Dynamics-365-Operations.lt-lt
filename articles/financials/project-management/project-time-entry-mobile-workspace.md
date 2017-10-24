---
title: "Projekto laiko įrašų mobilioji darbo sritis"
description: "Šioje temoje pateikiama informacija apie projekto laiko įrašo mobiliąją darbo sritį. Šioje darbo srityje vartotojai gali įvesti ir įrašyti laiką pagal projektą, naudodami savo mobilųjį įrenginį."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 2acf5a982988fe00492523ed5ce77d6de4a9e146
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="project-time-entry-mobile-workspace"></a>Projekto laiko įrašų mobilioji darbo sritis

[!include[banner](../includes/banner.md)]

Šioje temoje pateikiama informacijos apie mobiliąją darbo sritį **Projektų laiko įvedimas**. Šioje darbo srityje vartotojai gali įvesti ir įrašyti laiką pagal projektą, naudodami savo mobilųjį įrenginį.

Ši mobilioji darbo sritis skirta naudoti kartu su mobiliąja programa „Microsoft Dynamics 365 for Unified Operations“. 

## <a name="overview"></a>Apžvalga
Atlikdami kasdienes užduotis projekto ištekliai dažnai būna teritorijoje arba kelionėje. Mobilioji darbo sritis **Projekto laiko įrašas** vartotojams suteikia galimybę įvesti savo apmokamą arba neapmokamą laiką pagal projektą savo pasirinktame mobiliajame įrenginyje. Todėl projekto ištekliai laiko įrašus gali įrašyti visada ir visur. Taip pat jie gali peržiūrėti jau įrašytus laiko įrašus. 

Mobiliojoje darbo srityje **Projektų laiko įvedimas** vartotojai gali atlikti tolesnes konkrečias užduotis.

-   Įvesti bet kurios pasirinktos dienos valandų, sugaištų tam tikrai užduočiai atlikti, skaičių.
-   Ieškoti pagal projekto pavadinimą arba klientą ir rasti projektą, kuriam reikia priskirti laiko įrašą.
-   Nurodyti sugaišto laiko kategoriją ir veiklą.
-   Įrašyti projekto laiką kaip apmokamą arba neapmokamą.
-   Pasirinktinai įvesti bet kokių išorinių arba vidinių komentarų.

## <a name="prerequisites"></a>Būtinieji komponentai
Būtinosios sąlygos skiriasi priklausomai nuo jūsų organizacijoje visuotinai įdiegtos „Microsoft Dynamics 365“ versijos.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Būtinosios sąlygos, jeigu naudojate „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.) 
Jei jūsų organizacijoje visuotinai įdiegtas „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.), sistemos administratorius turi publikuoti mobiliąją darbo sritį **Projektų laiko įvedimas**. Instrukcijų ieškokite dalyje [Mobiliosios darbo srities publikavimas](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Būtinosios sąlygos, jei naudojate „Microsoft Dynamics 365 for Operations“ 1611 versiją su 3 platformos naujinimu arba naujesnę versiją
Jei jūsų organizacijoje visuotinai įdiegta „Microsoft Dynamics 365 for Operations‟ 1611 versija su 3 platformos naujinimu arba naujesnė versija, sistemos administratorius turi įvykdyti tolesnes būtinąsias sąlygas. 

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

<td>Įdiegti KB 4018050.</td>
<td>Sistemos administratorius</td>
<td>KB 4018050 yra X++ atnaujinimas arba metaduomenų karštoji pataisa, kurioje yra mobilioji darbo sritis <strong>Projekto laiko įrašas</strong>. Norėdamas įdiegti KB 4018050, sistemos administratorius turi atlikti tolesnius veiksmus.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Atsisiųsti metaduomenų karštąsias pataisas iš „Microsoft Dynamics Lifecycle Services“ (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Įdiekite metaduomenų karštąją pataisą</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Sukurkite diegiamą paketą</a>, kuriame yra modeliai <strong>ApplicationSuite</strong> ir <strong>ProjectMobile</strong>, o tada įkelkite diegiamą paketą į LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Visuotinai diegiamo paketo taikymas</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publikuoti mobiliąją darbo sritį <strong>Projektų laiko įvedimas</strong>.</td>
<td>Sistemos administratorius</td>
<td>Žr. <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiliosios darbo srities publikavimas</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobiliosios programos atsisiuntimas ir diegimas

Atsisiųskite ir įdiekite mobiliąją programą „Dynamics 365 for Unified Operations“:

-   [„Android“ telefonams](https://go.microsoft.com/fwlink/?linkid=850662)
-   [„iPhone“ telefonams](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Prisijunkite prie mobiliosios programos
1.  Paleiskite programą savo mobiliajame įrenginyje.
2.  Įveskite savo „Dynamics 365“ URL.
3.  Kai prisijungsite pirmą kartą, bus rodomas raginimas įvesti savo vartotojo vardą ir slaptažodį. Įveskite savo kredencialus.
4.  Prisijungus rodomos galimos jūsų įmonės darbo sritys. Atkreipkite dėmesį, kad sistemos administratoriui paskelbus naują darbo sritį vėliau turėsite atnaujinti mobiliųjų darbo sričių sąrašą.

[![Patraukite norėdami atnaujinti](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Laiko įvedimas naudojant mobiliąją darbo sritį Projekto laiko įrašas
1.  Savo mobiliajame įrenginyje pasirinkite darbo sritį **Projekto laiko įrašas**.
2.  Pasirinkite **Laiko įrašas**. Rodomos šios savaitės kalendoriaus datos.
3.  Pasirinkite datą ir pasirinkite **Veiksmai** &gt; **Naujas įrašas**.
4.  Įveskite valandų, kurias reikia įrašyti, skaičių.
5.  Pasirinkite laiko įrašo projektą. Sąraše rodomi projektai, įkelti į jūsų programą naudoti neprisijungus. Pagal numatytuosius parametrus įkeliama 50 prekių, tačiau kūrėjas šį skaičių gali keisti. Norėdami gauti daugiau informacijos, žr. [Mobilioji platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  Jei jūsų projekto sąraše nėra, pasirinkite **Ieškoti**. Ieškokite pagal pavadinimą arba perjunkite iešką pagal projekto pavadinimą arba klientą.
7.  Pasirinkite kategoriją. Sąraše rodomos kategorijos, įkeltos į jūsų programą naudoti neprisijungus. Pagal numatytuosius parametrus įkeliama 50 prekių, tačiau kūrėjas šį skaičių gali keisti. Norėdami gauti daugiau informacijos, žr. [Mobilioji platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  Jei jūsų kategorijos sąraše nėra, pasirinkite **Ieškoti**. Ieškokite pagal kategoriją arba perjunkite iešką pagal kategorijos pavadinimą.
9.  Pasirinkite veiklą. Sąraše rodomos veiklos, įkeltos į jūsų programą naudoti neprisijungus. Pagal numatytuosius parametrus įkeliama 50 prekių, tačiau kūrėjas šį skaičių gali keisti. Norėdami gauti daugiau informacijos, žr. [Mobilioji platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. Jei jūsų veiklos sąraše nėra, pasirinkite **Ieškoti**. Ieškokite pagal veiklos numerį arba perjunkite iešką pagal paskirtį.

11. Pasirinkite eilutės ypatybę.
12. Pasirinktinai: įveskite bet kokių išorinių arba vidinių komentarų.
13. Pasirinkite **Atlikta**.

