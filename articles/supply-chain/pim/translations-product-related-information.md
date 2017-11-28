---
title: DUK apie su produktais susijusius vertimus
description: "Šioje temoje aprašoma, kaip valdyti produktų, prekės dimensijų verčių ir produktų atributų vertimus."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3a1bfd4bd5f396c05277159ac112eaa8197d5818
ms.openlocfilehash: 2c58e3e2f60c00d8d834c1d80b347e2e7087809d
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="product-related-translations-faq"></a>DUK apie su produktais susijusius vertimus

[!include[banner](../includes/banner.md)]


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

## <a name="how-do-i-create-translations-for-product-related-information"></a>Kaip sukurti produktų informacijos vertimus?
Norėdami sukurti produkto vertimus, atlikite šiuos veiksmus:
1.  Spustelėkite **Produktų informacijos valdymas** &gt; **Bendra** &gt; **Patvirtinti produktai**.
2.  Pasirinkite produktą ir veiksmų srities grupėje **Kalbos** spustelėkite **Vertimai**.
3.  Puslapio **Teksto vertimas** lauke **Kalbos** pasirinkite kalbą. Norėdami įtraukti daugiau kalbų, išplėskite lauką **Kalbos**, tada spustelėkite **Gerai**.
4.  Įveskite vertimus grupės **Išverstas tekstas** laukuose **Nusidėvėjimas** ir **Produkto pavadinimas**.

Norėdami sukurti produkto atributų vertimus, atlikite šiuos veiksmus:
1.  Spustelėkite **Produktų informacijos valdymas** &gt; **Bendra** &gt; **Patvirtinti produktai**.
2.  Dalyje **Sąranka** spustelėkite **Atributai** ir tada spustelėkite **Atributai**.
3.  Puslapyje **Atributai** spustelėkite **Versti**.
4.  Puslapio **Teksto vertimas** lauke **Kalbos** pasirinkite kalbą. Norėdami įtraukti daugiau kalbų, išplėskite lauką **Kalbos**, tada spustelėkite **Gerai**.
5.  Įveskite vertimus grupės **Išverstas tekstas** laukuose **Nusidėvėjimas**, **Patogus pavadinimas** ir **Žinyno tekstas**.

Norėdami sukurti produkto dimensijų vertimus, atlikite šiuos veiksmus:
1.  Spustelėkite **Produktų informacijos valdymas** &gt; **Bendra** &gt; **Patvirtinti produktai**.
2.  Pasirinkite produktą ir tada spustelėkite **Produkto dimensijos**.
3.  Pasirinkite vieną iš nuorodų į produkto dimensijas: **Konfigūracijos**, **Dydžiai**, **Spalvos** arba **Stilius**.
4.  Pasirinkite dimensijos reikšmę ir tada spustelėkite **Versti**.
5.  Puslapio **Teksto vertimas** lauke **Kalbos** pasirinkite kalbą. Norėdami įtraukti daugiau kalbų, išplėskite lauką **Kalbos**, tada spustelėkite **Gerai**.
6.  Įveskite vertimus grupės **Išverstas tekstas** laukuose **Pavadinimas** ir **Aprašas**.

## <a name="can-the-names-of-product-variants-be-translated"></a>Ar gali būti išversti produkto variantų pavadinimai?
Produkto variantai yra paremti jau išleisto produkto dimensijų reikšmėmis. Produkto variantų pavadinimai sudaryti pagal produkto dimensijų reikšmių kombinacijas. Kai išverčiamos dimensijų vertės, susietos su produkto variantu, rodoma išversta produkto varianto pavadinimo versija.  

**Pavyzdys**  

Jūsų produktas yra įvairių dydžių ir spalvų marškinėliai, ir variantų pavadinimai yra sudaromi remiantis šia informacija:
-   Produkto numeris: \#3
-   Matmenys: dydis ir spalva
-   Dydžio vertės: mažas, vidutinis, didelis
-   Spalvos dimensijos vertės: raudona, žalia, juoda

Produkto varianto, pagrįsto dimensijų reikšmėmis Mažas ir Raudona, pavadinimas yra **\#3:Small:Red**.  

Klientas nori pirkti mažų, raudonų marškinėlių ir marškinėlių pavadinimas sąskaitoje faktūroje turi būti rašytas prancūziškai. Dimensijų reikšmes Mažas ir Raudona išverčiate į prancūzų kalbą, produkto varianto pavadinimas – **\#3:Petit:Rouge**.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Patarimas</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Norėdami nustatyti kliento pageidaujamą kalbą, atlikite šiuos veiksmus:
<ol>  
<li>Spustelėkite <strong>Pardavimas ir rinkodara</strong> &gt; <strong>Bendra</strong> &gt; <strong>Klientai</strong> &gt; <strong>Visi</strong> <strong>klientai</strong>.</li>
<li>Dukart spustelėkite klientą, kad atidarytumėte puslapį <strong>Klientai</strong>. Skirtuko <strong>Bendra</strong> lauke <strong>Kalbos</strong> pasirinkite <strong>kalbą</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>Kas atsitinka, jei klientas pageidauja kalbos, kurios vertimų nėra?
Jei vertimų nėra kliento pageidaujama kalba, pavadinimai ir aprašai rodomi bendra jūsų įmonės kalba.

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>Ar galiu tvarkyti eilės dimensijų reikšmių vertimus vienu metu?
Dimensijų vertės yra skirtos konkrečiam produktui, todėl galite valdyti dimensijų vertes atskiriems produktams. Tačiau jei jūs sukuriate dimensijų verčių grupę ir sukuriate verčių grupėje esančių verčių vertimus, tampa lengviau valdyti vertimus.   

**Pavyzdys**  

Jūsų įmonė gamina įvairių stilių marškinėlius ir kiekvieno stiliaus marškinėliai yra dydžių Mažas, Vidutinis ir Didelis. Dydžiai yra surinkti į vieną dimensijų verčių grupę. Pridėję naują marškinėlių stilių galite jį susieti su dimensijų verčių grupe, naudojama dydžiams, kad visi dydžiai taptų galimi naujam produktui. Taip pat galite pridėti arba bet kuriuo metu pakeisti dydžių vertimus dimensijų vertės grupėje.  

Dimensijos vertė, susijusi su produktu per dimensijų variantų grupę, turi būti tvarkoma produkto variantų grupėje.   
Norėdami kurti dimensijų verčių grupę, atlikite šiuos veiksmus:
1.  Spustelėkite **Produktų informacijos valdymas** &gt; **Sąranka** &gt; **Variantų grupės**.
2.  Pasirinkite **Dydžio** **grupės**, **Spalvų grupės** arba **Stilių grupės**.
3.  Spustelėkite **Nauja**, tada įveskite grupės pavadinimą lauke **Dydžių** **grupė**, **Spalvų grupė** arba **Stilių grupė**. Spustelėkite **Dydžiai**, **Spalvos** arba **Stiliai**, norėdami kurti grupių eilutes.
4.  Puslapyje **Dydžių** **grupės** eilutės, **Spalvų** **grupės** **eilutės** arba **Stilių grupės eilutės** spustelėkite **Nauja**, tada sukurkite grupių dydžius, spalvas ir stilius.

Norėdami valdyti verčių vertimus dimensijų verčių grupėje, atlikite šiuos veiksmus:
1.  Atlikite ankstesnėje procedūroje, skirtoje dimensijų vertės grupės kūrimui, nurodytus veiksmus, kad atidarytumėte puslapį **Dydžių grupės eilutės**, **Spalvų grupės eilutės** arba **Stilių grupės eilutės**.
2.  Spustelėkite **Teksto vertimas**. Puslapio **Teksto vertimas** grupės **Išverstas tekstas** laukuose **Pavadinimas** ir **Aprašas** įveskite vertimus.

## <a name="when-can-translations-of-product-related-information-be-managed"></a>Kada gali būti valdomi produktų informacijos vertimai?
Produktų informacijos vertimai gali būti tvarkomi bet kuriuo metu. Atnaujinus su produktu susijusios dimensijos vertės vertimus, produkto informacija atnaujinama, nepriklausomai nuo to, ar produktas įtrauktas į operacijas.






