---
title: Užduoties komponentų nustatymas
description: Šiame straipsnyje aprašomi abstraktūs elementai, kurie gali sudaryti užduotį, ir pateikiami pavyzdžiai, kaip tuos elementus galite naudoti savo organizacijoje.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: anbichse
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 69759c0488563a904f6e80afacb1802611ab1930
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419709"
---
# <a name="set-up-the-components-of-a-job"></a>Užduoties komponentų nustatymas

Šiame straipsnyje aprašomi abstraktūs elementai, kurie gali sudaryti užduotį, ir pateikiami pavyzdžiai, kaip tuos elementus galite naudoti savo organizacijoje. 

Prieš kurdami užduotis turite nustatyti tam tikrą nuorodos informaciją. Galite kurti užduotį, kuri turi tik pavadinimą. Tačiau įtraukdami papildomą informaciją, pvz., pareigas, turite pateikti numatytąsias užduočiai priskirtų pareigų vertes. Be to, kai kurią informaciją, kurią įvedate, galima naudoti kompensavimo planams į konkrečias užduotis filtruoti. Jei norite nustatyti tinkamumą, kurį galite naudoti kompensavimo planams į konkrečią užduotį filtruoti, prieš nustatydami užduotis turite nustatyti užduočių funkcijas ir tipus. Nustatę šias numatytąsias reikšmes sutaupysite laiko, kai užduotį įtraukiate pareigas. 

Kai kuri užduoties informacija, pvz., pareigos, tipas ir funkcija, turi galiojimo datą. Jei šiandien sukuriate užduotį, bet šios informacijos iš karto neįtraukiate, o tada peržiūrite užduotį jos sukūrimo dieną, ši informacija nebus rodoma. Todėl turėtumėte sukurti dalį šios nuorodos informacijos, nes jos gali prireikti vėliau. Tokiu būdu informaciją galite įtraukti į naujas užduotis tada, kai jas kuriate.

## <a name="job-titles"></a>Pareigos
Tam, kad galėtumėte kurti darbo vietas, turite nustatyti tų darbo vietų pareigas. Pareigoms suteikiami darbo vietų, su kuriomis tos pareigos susietos, pareigų pavadinimai. 

Tvarkykite pareigas puslapyje **Pareigos**, kurį galite atidaryti naudodami ieškos funkciją. Puslapyje **Pareigos** įveskite pareigas, kurias planuojate priskirti užduotims.

## <a name="job-types"></a>Užduočių tipai
Užduočių tipai naudojami panašioms užduotims į kategorijas sugrupuoti. Užduočių tipai nėra būtini. Tačiau jei užduočių tipus planuojate naudoti nustatydami kompensavimo valdymo tinkamumo taisykles, užduočių tipus turite nustatyti prieš nustatydami užduotis. Kai kurie užduočių tipų pavyzdžiai: visa darbo diena ar ne visa darbo diena arba atlyginimas ir valandinis užmokestis. Užduočių tipus galite tvarkyti puslapyje **Užduočių tipai**. Puslapyje **Užduočių tipai** įveskite užduoties tipo pavadinimą ir trumpą aprašymą. Lauke **Neapmokestinimo būsena** pasirinkite vieną iš toliau nurodytų parinkčių, kad nurodytumėte šio tipo užduočių Sąžiningo darbo standartų akto (FLSA) neapmokestinimo būseną.

-   **Neapmokestinama** – pagal FLSA užduočių viršvalandžiai nėra apmokestinami.
-   **Apmokestinama** – pagal FLSA užduočių viršvalandžiai yra apmokestinami.
-   **Netaikoma** – FLSA netaikomas.

## <a name="job-functions"></a>Užduoties funkcijos
Užduočių funkcijos nurodo aukšto lygio funkcines kategorijas susieja aukšto lygio pareigas. Užduočių funkcijos nėra būtinos. Užduočių funkcijas ir užduočių tipus galite naudoti norėdami filtruoti kompensavimo planus, ieškodami konkrečių užduočių. Užduočių funkcijos ir užduočių tipai susiejami su kompensavimo planais nustatant tinkamumo taisykles puslapyje **Tinkamumo taisyklės**. Tada prie kompensavimo plano galite pridėti lygių, taikomų konkrečiam užduoties tipo ir užduoties funkcijos junginiui, kurį apibrėžėte naudodami tinkamumo taisyklę, rinkinį. (Šios funkcijos taikoms tiek pastoviosios atlyginimo dalies planams, tiek kintamosios atlyginimo dalies planams.) Tačiau, jei užduočių funkcijas planuojate naudoti nustatydami kompensavimo valdymo tinkamumo taisykles, užduočių funkcijas turite nustatyti prieš nustatydami užduotis. Tolesnėje lentelėje pateikta keletas užduočių funkcijų pavyzdžių.

| Užduotis           | Užduoties funkcija         |
|---------------|----------------------|
| Pardavimo vadybininkas | Vidurinio lygio vadovas    |
| Buhalteris    | Specialistai        |

Užduočių funkcijas galite tvarkyti puslapyje **Užduočių funkcijos**. Puslapyje **Užduočių funkcijos** įveskite užduoties funkcijos identifikavimo kodą ir trumpą aprašymą.

## <a name="job-tasks"></a>Darbo užduotys
Darbo užduotys apibūdina pagrindines užduotis, kurias atitinkamoms pareigoms priskirtas darbuotojas turi atlikti. Tą pačią darbo užduotį galima įtraukti į kelias užduotis ir užduočių, kurios naudoja tas darbo užduotis, pareigas. Tolesnėje lentelėje pateikta keletas darbo užduočių pavyzdžių.

<table>
<thead>
<tr class="header">
<th>Užduotis</th>
<th>Darbo užduotis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pardavimo vadybininkas</td>
<td><ul>
<li><strong>Efektyvumo apžvalga</strong> – peržiūrėti kiekvieno pardavėjo darbo efektyvumą.</li>
<li><strong>Neatvykimų apžvalga</strong> – patvirtinti arba atmesti kiekvieno pardavėjo prašymus leisti neatvykti arba registracijas.</li>
</ul></td>
</tr>
<tr class="even">
<td>Buhalteris</td>
<td><strong>Finansinės ataskaitos</strong> – pateikti savaitės finansines ataskaitas vyriausiajam finansininkui.</td>
</tr>
</tbody>
</table>

Darbo užduotis galite tvarkyti puslapyje **Darbo užduotys**. Puslapyje **Darbo užduotys** įveskite darbo užduoties pavadinimą ir aprašymą. Lauke **Pastaba** galite pasirinktinai įvesti papildomą informaciją. Galima naujinti konkrečios užduoties pastabas, nepakeičiant čia įvestų pastabų.

## <a name="areas-of-responsibility"></a>Atsakomybės ribos
Atsakomybės ribos naudojamos užduotį atliekančio darbuotojo darbo vaidmenims, procesams ir produktams, už kuriuos jis yra atsakingas, apibrėžti. Pvz., jei užduotis pavadinta „Buhalteris“, viena atsakomybės sritis gali būti apibrėžta kaip „A produkto finansinės ataskaitos“. Atsakomybės sritis galite tvarkyti puslapyje **Atsakomybės sritys**, kurį galite rasti naudodami ieškos funkciją. Puslapyje **Atsakomybės sritys** įveskite atsakomybės pavadinimą ir aprašymą. Lauke **Pastaba** galite pasirinktinai įvesti papildomą informaciją. Galima naujinti konkrečios užduoties pastabas, nepakeičiant čia įvestų pastabų.

## <a name="steps-for-creating-a-job"></a>Užduoties kūrimo veiksmai
Nuoseklios naujos užduoties kūrimo procedūros žr. straipsnyje [Naujų užduočių nustatymas](../fin-and-ops/hr/tasks/define-new-jobs.md). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]