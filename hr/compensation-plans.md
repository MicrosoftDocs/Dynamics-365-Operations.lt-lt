---
title: "Kompensacijų planai"
description: "Kompensacijų ir išmokų vadovai gali naudoti Kompensavimo valdymą, skirtą prižiūrėti ir apdoroti organizacijos darbuotojų pastoviųjų ir kintamųjų atlyginimo dalių planus."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3892bfab6aecd8db388d5308b36500eee70cb423
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="compensation-plans"></a>Kompensacijų planai

[!include[banner](includes/banner.md)]


Kompensacijų ir išmokų vadovai gali naudoti Kompensavimo valdymą, skirtą prižiūrėti ir apdoroti organizacijos darbuotojų pastoviųjų ir kintamųjų atlyginimo dalių planus.

### <a name="introduction"></a>Įžanga

Kompensacijų valdymas naudojamas kontroliuoti pagrindinio užmokesčio ir premijų pristatymui. Darbuotojo fiksuotas pagrindinis užmokestis ir nuopelnų padidėjimai kontroliuojami naudojant pastoviosios kompensacijos dalies planus. Skatinamųjų išmokų, pvz., priedų, apdovanojimų už našumą, akcijų pasirinkimo sandorių, subsidijų bei vienkartinių premijų mokėjimas valdomas naudojant kintamosios kompensacijos dalies planus. 

Darbuotojai gali būti registruojami vienam arba keliems abiejų tipų planams. Kad turėtų teisę registruotis kompensavimo planui, darbuotojas turi atitikti toliau nurodytus reikalavimus.
-   Darbuotojui turi būti priskirtos aktyvios pareigos.
-   Darbuotojas turi atitikti kriterijus, kuriuos apibrėžia kompensavimo plano tinkamumo taisyklės.

## <a name="compensation-setup"></a> Kompensavimo sąranka
Toliau pateiktoje lentelėje išvardijami kompensavimo proceso komponentai, kurie gali būti itin svarbūs nustatant jūsų įmonės kompensavimo planus.

<table>
<thead>
<tr class="header">
<th>Komponentas</th>
<th>Daugiau informacijos...</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pastoviosios atlyginimo dalies veiksmai</td>
<td>Pastoviosios kompensavimo dalies veiksmais pasiekiama toliau nurodytų dviejų tikslų.
<ul>
<li>Veiksmai gali nurodyti, kokią informaciją reikia įrašyti, kai pasikeičia darbuotojo kompensavimas. Pavyzdžiui, galite reikalauti, kad būtų įrašoma pokyčio priežastis, pvz., paaukštinimas arba pažeminimas pareigose.</li>
<li>Veiksmai gali užtikrinti, kad, apdorojant pastoviosios kompensacijos dalies planus, būtų taikomas skaičiavimas.  Pvz., tipo Kapitalas veiksmai darbuotojų užmokestį palygins su darbuotojo lygio minimaliu atskaitos tašku ir užtikrins, kad darbuotojui būtų mokamas bent minimumas.</li>
</ul></td>
</tr>
<tr class="even">
<td>Lygiai</td>
<td>Lygiai yra susieti su darbais ir visomis pareigomis, kurios yra susijusios su darbo nuoroda. Galite kurti šių trijų kompensavimo planų atskirus lygius: Kategorijų, Intervalų ir Pakopų.</td>
</tr>
<tr class="odd">
<td>Diapazono realizavimo matrica</td>
<td>Diapazono realizavimo matrica padeda darbuotojus perkelti į jų darbų kontrolinį tašką. Taip pat galite naudoti diapazono realizavimą, norėdami valdyti mokėjimo koeficiento kapitalą įmonės viduje neatsižvelgiant į kiekvieno darbuotojo darbą ar visos įmonės darbą. Pavyzdžiui, darbuotojai, kuriems sumokama mažiau, nei numatyta pagal diapazoną, gauna didesnio procento padidinimą, nei tie darbuotojai, kuriems pagal diapazoną mokama daugiau. Tokiu būdu galite sistematiškai balansuoti kapitalo skirtumus. Diapazono realizavimas apskaičiuojamas taip: (Fiksuotas užmokesčio tarifas – Diapazono minimumas) ÷ (Diapazono maksimumas – Diapazono minimumas).</td>
</tr>
<tr class="even">
<td>Atskaitos taškų nustatymai</td>
<td>Atskaitos taškų sąranka apima atskaitos taškų, sudarančių intervalus mokėjimo koeficientų matricoje, rinkinį. Kiekvieną diapazoną galima susieti su užmokesčio tarifu. Pvz., kategorijų planų atskaitos taškai dažnai bus Minimumo, Vidurio ir Maksimumo.</td>
</tr>
<tr class="odd">
<td>Kompensavimo matrica</td>
<td>Kompensavimo matrica yra atskaitos taškų ir lygių rinkinys, kurį naudojate kurdami kompensavimo struktūrą.</td>
</tr>
<tr class="even">
<td>Kompensavimo struktūra</td>
<td>Kompensavimo struktūra yra kompensavimo matrica, kurioje užmokesčio tarifai susieti su kiekvieno lygio atskaitos taškais.</td>
</tr>
<tr class="odd">
<td>Tinkamumo taisyklė</td>
<td>Tinkamumo taisyklės naudojamos identifikuoti konkrečių darbų, darbų funkcijų, darbų tipų, skyrių, profesinių sąjungų ar kompensavimo regionų darbuotojams, kuriems taikomi konkretūs kompensavimo planai. Norėdami darbuotojus užregistruoti į planą, turite sukurti tiek kintamosios, tiek pastoviosios kompensavimo dalies planų tinkamumo taisykles. Kai nurodytos kompensavimo plano tinkamumo taisyklės, galite apibrėžti lygius, kurie turėtų būti taikomi darbams, kuriems taikomas planas.</td>
</tr>
<tr class="even">
<td>Išmokų dažnumas</td>
<td>Darbo užmokesčio dažniai yra naudojami apibrėžti laikotarpiui, kuriam nurodytas kompensavimas.  Pvz., darbo užmokesčio dažnis padeda suprasti, ar kompensacijos suma nurodyta kaip metinis atlyginimas ar kaip valandinis darbo užmokesčio tarifas. Darbo užmokesčio dažniai taip pat naudojami nustatyti konvertavimo koeficientams, kuriais kompensavimo sumos iš mėnesinio, savaitinio, dvisavaitinio ir valandinio užmokesčio dažnių konvertuojamos į metinį užmokesčio dažnį.</td>
</tr>
<tr class="odd">
<td>Kompensacijos sritys</td>
<td>Kompensavimo regionai naudojami darbuotojo kompensacijai nurodyti pagal darbo vietą.</td>
</tr>
<tr class="even">
<td>Kontrolinis taškas</td>
<td>Kontrolinis taškas apibrėžia jūsų manymu idealų mokėjimo tarifą visiems darbuotojams atlyginimo lygyje. Kategorijų plano struktūrų kontroliniai taškai paprastai yra diapazonų vidurio taškai. Intervalų struktūrose kontroliniai taškai naudojami retai. Pastoviosios kompensacijos dalies kontrolinį tašką galite nurodyti Pastoviosios kompensacijos dalies planų formoje.</td>
</tr>
<tr class="odd">
<td>Užduoties funkcijos</td>
<td>Darbų funkcijos naudojamos norint kompensavimo planus klasifikuoti ir filtruoti tam tikriems darbams.</td>
</tr>
<tr class="even">
<td>Užduočių tipai</td>
<td>Darbų tipai naudojami norint kompensavimo planus klasifikuoti ir filtruoti tam tikriems darbams.</td>
</tr>
<tr class="odd">
<td>Kintamosios atlyginimo dalies tipai</td>
<td>Kintamosios kompensacijos dalies tipai, pvz., akcijų ar grynųjų pinigų premijos, yra nustatomos kintamosios kompensacijos dalies planuose.</td>
</tr>
<tr class="even">
<td>Kompensavimo tinkleliai</td>
<td>Kompensavimo tinkleliuose yra kompensavimo struktūra.  Kompensavimo tinklelius gali naudoti vienas ar keli kompensavimo planai.</td>
</tr>
<tr class="odd">
<td>Veiklos efektyvumo planai</td>
<td>Našumo planai naudojami našumui susieti su paskirstymo matrica, kad galėtumėte naudoti planą su mokėjimo už našumą strategija.</td>
</tr>
<tr class="even">
<td>Veiklos efektyvumo vertinimas</td>
<td>Našumo vertinimai naudojami našumo planuose premijos ar našumo apdovanojimui nustatyti.</td>
</tr>
</tbody>
</table>

## <a name="process-events"></a>Apdorojimo įvykiai
Apdorojimo įvykis skaičiuoja tam tikro laikotarpio kompensavimo informaciją visiems darbuotojams, kurie yra įtraukti į vieną ar daugiau pastoviosios ar kintamosios atlyginimo dalies planų. Galite pakartotinai paleisti apdorojimo įvykį, jei norite patikrinti ar atnaujinti kompensacijų skaičiavimo rezultatus.

<a name="compensation-events"></a>Kompensavimo įvykiai
-------------------

Kiekvieną kartą vykdant apdorojimo įvykį, sukuriamas kompensavimo įvykis.  Kompensavimo įvykiuose yra kiekvieno darbuotojo, įtraukto į tą apdorojimo įvykį, kompensavimo proceso rezultatai.  Kai skaičiavimai yra teisingi, galite įkelti kompensavimo įvykį, kad atnaujintumėte darbuotojų, kuriuos paveikė apdorojimo įvykis, kompensacijų įrašus.

## <a name="recommendations"></a> Rekomendacijos
Paleidę apdorojimo įvykį, pagal apskaičiuotas apdorojimo įvykio gaires galite rekomenduoti koreguoti darbuotojo nuopelnų padidėjimą ar premijos sumą. Norėdami teikti rekomendacijas dėl darbuotojų, nustatydami kompensavimo planus arba apdorojimo įvykį turite įgalinti rekomendacijas.




