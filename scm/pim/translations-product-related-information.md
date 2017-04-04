---
title: DUK apie vertimai gaminio
description: "Šioje temoje aprašoma, kaip valdyti produktų, prekės dimensijų verčių ir produktų atributų vertimus."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: a9c991a5afaebd10b8812dfc1d67120ed4ebdfd2
ms.lasthandoff: 03/31/2017


---

# <a name="product-related-translations-faq"></a>DUK apie vertimai gaminio

Šioje temoje aprašoma, kaip valdyti produktų, prekės dimensijų verčių ir produktų atributų vertimus. 

<a name="what-product-related-data-can-be-translated"></a>Kokie gaminio duomenys gali būti išversti?
--------------------------------------------

Galite išversti šią produkto informacija:
-   Produktų pavadinimus ir aprašus.
-   Aprašymus, draugiškus pavadinimus ir pagalbinius produktų atributų verčių tekstus.
-   Produkto dimensijų verčių pavadinimus ir apibūdinimus.

Produkto informaciją galite išversti į bet kurią puslapyje **Teksto vertimas** esančią kalbą. Daugiau informacijos žr. tolesnėje dalyje **Kaip kurti su produktu susijusios informacijos vertimus**.

## <a name="where-can-i-view-the-translated-information"></a>Kur galiu peržiūrėti išverstą informaciją?
Produktų informacijos vertimus galite peržiūrėti bet kokiame išoriniame šaltinio dokumente, pvz. sąskaitoje faktūroje, kuriame naudojama verstina informacija norima kalba.

## <a name="how-do-i-create-translations-for-productrelated-information"></a>Kaip sukurti productrelated informacijos vertimus?
Norėdami sukurti produkto vertimus, atlikite šiuos veiksmus:
1.  Spustelėkite **produkto informacijos valdymo**&gt;**bendras**&gt;**išleisti produktai**.
2.  Pasirinkti gaminį, ir į veiksmų sritį, – į **kalbų** grupės, spustelėkite **vertimų**.
3.  Puslapio **Teksto vertimas** lauke **Kalbos** pasirinkite kalbą. Jei norite pridėti daugiau kalbų, plėsti ir **kalbos** srityje, ir tada spustelėkite **gerai**.
4.  Įveskite vertimus grupės **Išverstas tekstas** laukuose **Nusidėvėjimas** ir **Produkto pavadinimas**.

Norėdami sukurti produkto atributų vertimus, atlikite šiuos veiksmus:
1.  Spustelėkite **produkto informacijos valdymo**&gt;**bendras**&gt;**išleisti produktai**.
2.  Dalyje **Sąranka** spustelėkite **Atributai** ir tada spustelėkite **Atributai**.
3.  Puslapyje **Atributai** spustelėkite **Versti**.
4.  Puslapio **Teksto vertimas** lauke **Kalbos** pasirinkite kalbą. Jei norite pridėti daugiau kalbų, plėsti ir **kalbos** srityje, ir tada spustelėkite **gerai**.
5.  Įveskite vertimus grupės **Išverstas tekstas** laukuose **Nusidėvėjimas**, **Patogus pavadinimas** ir **Žinyno tekstas**.

Norėdami sukurti produkto dimensijų vertimus, atlikite šiuos veiksmus:
1.  Spustelėkite **produkto informacijos valdymo**&gt;**bendras**&gt;**išleisti produktai**.
2.  Pasirinkite produktą ir tada spustelėkite **Produkto dimensijos**.
3.  Pasirinkite vieną iš nuorodų į produkto dimensijas: **Konfigūracijos**, **Dydžiai**, **Spalvos** arba **Stilius**.
4.  Pasirinkite dimensijos reikšmę ir tada spustelėkite **Versti**.
5.  Puslapio **Teksto vertimas** lauke **Kalbos** pasirinkite kalbą. Jei norite pridėti daugiau kalbų, plėsti ir **kalbos** srityje, ir tada spustelėkite **gerai**.
6.  – Į **išverstas tekstas** grupė, įveskite vertimų į **pavadinimas** ir **Aprašymas** laukus.

## <a name="can-the-names-of-product-variants-be-translated"></a>Ar gali būti išversti produkto variantų pavadinimai?
Produkto variantai yra paremti jau išleisto produkto dimensijų reikšmėmis. Produkto variantų pavadinimai sudaryti pagal produkto dimensijų reikšmių kombinacijas. Kai išverčiamos dimensijų vertės, susietos su produkto variantu, rodoma išversta produkto varianto pavadinimo versija.  

**Pavyzdys**  

Jūsų produktas yra įvairių dydžių ir spalvų marškinėliai, ir variantų pavadinimai yra sudaromi remiantis šia informacija:
-   Produkto numeris: \#3
-   Matmenys: dydis ir spalva
-   Dydžio vertės: mažas, vidutinis, didelis
-   Spalvos dimensijos vertės: raudona, žalia, juoda

Pavadinimas produkto variantas, kuris yra pagrįstas dimensija vertina šaulių ir raudona yra **\#3:Small:Red**.  

Klientas nori pirkti mažų, raudonų marškinėlių ir marškinėlių pavadinimas sąskaitoje faktūroje turi būti rašytas prancūziškai. Versti prancūzų dimensijų vertes, mažas ir raudona, ir produkto rūšies pavadinimas **\#3: Petit: Rouge**.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Tip</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Norėdami nustatyti kliento pageidaujamą kalbą, atlikite šiuos veiksmus:
<ol>  
<li>Spustelėkite <strong>pardavimo ir rinkodaros</strong>&gt;<strong>bendras</strong>&gt;<strong>Klientai</strong>&gt;<strong>visi</strong> <strong>klientų</strong>.</li>
<li>Dukart spustelėkite klientą, kad atidarytumėte puslapį <strong>Klientai</strong>. Skirtuko <strong>Bendra</strong> lauke <strong>Kalbos</strong> pasirinkite <strong>kalbą</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>Kas atsitinka, jei klientas pageidauja kalbos, kurios vertimų nėra?
Jei vertimų nėra kliento pageidaujama kalba, pavadinimai ir aprašai rodomi bendra jūsų įmonės kalba.

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>Ar galiu tvarkyti eilės dimensijų reikšmių vertimus vienu metu?
Dimensijų vertės yra skirtos konkrečiam produktui, todėl galite valdyti dimensijų vertes atskiriems produktams. Tačiau jei jūs sukuriate dimensijų verčių grupę ir sukuriate verčių grupėje esančių verčių vertimus, tampa lengviau valdyti vertimus.   

**Example**  

Jūsų įmonė gamina įvairių stilių marškinėlius ir kiekvieno stiliaus marškinėliai yra dydžių Mažas, Vidutinis ir Didelis. Dydžiai yra surinkti į vieną dimensijų verčių grupę. Pridėję naują marškinėlių stilių galite jį susieti su dimensijų verčių grupe, naudojama dydžiams, kad visi dydžiai taptų galimi naujam produktui. Taip pat galite pridėti arba bet kuriuo metu pakeisti dydžių vertimus dimensijų vertės grupėje.  

Dimensijos vertė, susijusi su produktu per dimensijų variantų grupę, turi būti tvarkoma produkto variantų grupėje.   
Norėdami kurti dimensijų verčių grupę, atlikite šiuos veiksmus:
1.  Spustelėkite **produkto informacijos valdymo**&gt;**parametrai**&gt;**variantas grupės**.
2.  Pasirinkite **Dydžio** **grupės**, **Spalvų grupės** arba **Stilių grupės**.
3.  Spustelėkite **naujas**, ir tada įveskite grupės pavadinimą į **dydis****grupės**, **spalvų grupės**, arba **stilius** lauko. Spustelėkite **Dydžiai**, **Spalvos** arba **Stiliai**, norėdami kurti grupių eilutes.
4.  – Į **dydis****grupės** linijas, **spalvos****grupės****linijos**, arba **stiliaus grupių eilučių** spustelėkite **New**, ir tada sukurti dydžių, spalvų ir stilių grupių.

Norėdami valdyti verčių vertimus dimensijų verčių grupėje, atlikite šiuos veiksmus:
1.  Atlikite ankstesnėje procedūroje, skirtoje dimensijų vertės grupės kūrimui, nurodytus veiksmus, kad atidarytumėte puslapį **Dydžių grupės eilutės**, **Spalvų grupės eilutės** arba **Stilių grupės eilutės**.
2.  Spustelėkite **Teksto vertimas**. – Į **teksto vertimas** p., į **išverstą tekstą** grupė, įveskite vertimų į **pavadinimas** ir **Aprašymas** laukus.

## <a name="when-can-translations-of-productrelated-information-be-managed"></a>Kai productrelated informacijos vertimus galima valdyti?
Produktų informacijos vertimai gali būti tvarkomi bet kuriuo metu. Atnaujinus su produktu susijusios dimensijos vertės vertimus, produkto informacija atnaujinama, nepriklausomai nuo to, ar produktas įtrauktas į operacijas.




