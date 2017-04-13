---
title: "Sudėtinių dalių darbo"
description: "Šioje temoje aprašoma konceptualus elementų, kad darbas gali būti ir pateikiami pavyzdžiai, kaip jūs galite naudoti šiuos elementus jūsų organizacijoje."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: d96b1f01a5cb4370436888deae8fd4835a0dbb80
ms.openlocfilehash: b8143db5b133337603a7f2f46028d91bb81cd947
ms.lasthandoff: 03/31/2017


---

# <a name="setting-up-the-components-of-a-job"></a>Sudėtinių dalių darbo

Šioje temoje aprašoma konceptualus elementų, kad darbas gali būti ir pateikiami pavyzdžiai, kaip jūs galite naudoti šiuos elementus jūsų organizacijoje. 

Prieš kurdami darbo vietas, turite nustatyti kai kurių nuorodos informacija. Galite sukurti darbo, kuris turi tik pavadinimą. Vis dėlto, įskaitant papildomos informacijos, pvz., darbo pavadinimas, pateikiate numatytąsias reikšmes į pozicijas, kurios yra priskirtos darbo. Be to, tam tikra informacija, kurią įvedate galima filtruoti kompensavimo planus iki konkrečių darbo vietų. Jei norite nustatyti tinkamumą, kad galite naudoti norėdami filtruoti kompensavimo planus į konkrečią darbo vietą, jūs turėtumėte nustatyti darbo funkcijų ir užduočių tipai prieš nustatydami darbo vietų. Turėdami šias numatytąsias vertes galima, Jūs sutaupysite laiko, jei norite pridėti pozicijas darbo. 

Kai kurie darbo informaciją, pavyzdžiui, darbo pavadinimas, tipas ir funkcija, yra datos-veiksminga. Jei šiandien užduočiai kurti, bet nėra įtraukti šiuos duomenis vėliau, o tada pažvelgti į darbą nuo sukūrimo datą, šie duomenys nebus rodomi. Todėl, turite sukurti tam tikrą atskaitos informaciją prieš jums reikia. Tokiu būdu, jūs galite įtraukti informaciją į naujų darbo vietų juos kurdami.

## <a name="job-titles"></a>Pareigos
Tam, kad galėtumėte kurti darbo vietas, turite nustatyti tų darbo vietų pareigas. Pareigoms suteikiami darbo vietų, su kuriomis tos pareigos susietos, pareigų pavadinimai. 

Išlaikyti darbo antraštines naudojant į **pavadinimai** puslapį, kuriame galite atidaryti naudodami paieškos funkciją. Dėl to ** pavadinimai ** puslapyje, įveskite pavadinimai, kad jūs planuojate naudoti savo darbams.

## <a name="job-types"></a>Užduočių tipai
Galite naudoti užduočių tipai panašūs darbai sugrupuoti į kategorijas. Užduočių tipai nebūtini. Tačiau jei užduočių tipus planuojate naudoti nustatydami kompensavimo valdymo tinkamumo taisykles, užduočių tipus turite nustatyti prieš nustatydami užduotis. Užduočių tipai pavyzdžiai darbą visą darbo dieną, ar mokėti atlyginimą ir kas valandą. Galite išlaikyti užduočių tipai naudojant į **darbo tipai** puslapis. Dėl į **darbo tipai** puslapyje, įveskite vardą ir trumpą aprašymą apie užduoties tipas. – Į **atleisti statuso** srityje, pasirinkite vieną iš šių parinkčių nurodyti teisingą darbo standartų įstatymas (FLSA) neapmokestinimo būsena tokia darbo užduočių:

-   **Atleisti** – darbo vietų yra atleidžiami nuo viršvalandžius pagal į FLSA.
-   **Neatleistos** – darbas nėra atleistos nuo viršvalandžius pagal į FLSA.
-   **Netaikoma** -FLSA padengimo nėra taikoma.

## <a name="job-functions"></a>Užduoties funkcijos
Darbas sankryžas apibūdinti aukšto lygio funkcinės kategorijas ir susiję aukšto lygio pareigas. Nebūtini darbo funkcijoms. Darbo funkcijas, kartu su darbo tipus, galite filtruoti kompensavimo planus iki konkrečių darbo vietų. Galite susieti darbo funkcijų ir užduočių tipai su kompensavimo planus nustatant tinkamumo taisyklės į **tinkamumo taisyklės** puslapis. Tada, galite pridėti kompensavimo planą, taikomos konkrečios užduoties tipas ir darbo funkcijos, jūsų nustatytų per tinkamumo taisyklė derinys lygių rinkinį. (Šios funkcijos taikomos pastoviųjų atlyginimo dalių planai bei planų kintamosios atlyginimo dalies.) Tačiau, jei jūs planuojate naudoti darbo funkcijas, jei norite nustatyti tinkamumo finansuoti kompensavimo valdymo, turėtumėte nustatyti darbo funkcijas prieš nustatydami darbo vietų. Lentelėje pateikta keletas pavyzdžių darbo funkcijas.

| Užduotis           | Užduoties funkcija         |
|---------------|----------------------|
| Pardavimo vadybininkas | Vidutinio lygio vadovas    |
| Buhalteris    | Specialistams        |

Galite išlaikyti užduočių funkcijų naudojant į **užduočių funkcijų** puslapis. Dėl to **užduočių funkcijų** puslapyje, įveskite identifikavimo kodas ir trumpas darbo funkcijos.

## <a name="job-tasks"></a>Darbo užduotys
Darbo uždaviniai apibūdina pagrindinio užduotis, kurias turi atlikti darbuotojas, kuris yra darbo padėtyje. Tą pačią užduotį užduotį galima įtraukti kelias užduotis ir pozicijoms dėl užduotis, kurios naudoja šias darbo užduotis. Lentelėje pateikta keletas darbo užduočių pavyzdžių.

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
<li><strong>PERF-apžvalgos</strong> – peržiūrėti kiekvieno pardavėjo darbo našumą.</li>
<li><strong>ABS-apžvalgos</strong> – patvirtinti arba atmesti kiekvieno pardavėjo prašymų leisti neatvykti arba registracijų.</li>
</ul></td>
</tr>
<tr class="even">
<td>Buhalteris</td>
<td><strong>FIN-ataskaita</strong> – vyriausiasis finansų pareigūnas pateikia savaitinės finansinės ataskaitos.</td>
</tr>
</tbody>
</table>

Galite išlaikyti darbo užduotis naudojant į **darbo užduotys** puslapis. Dėl to **darbo užduotis** puslapyje, įveskite pavadinimą ir aprašymą darbo užduotis. – Į **Pastaba** lauką, galite pasirinktinai įvesti papildomos informacijos. Pastabos gali būti atnaujintas specifiniam darbui nekeičiant pažymi, kad įvedėte čia.

## <a name="areas-of-responsibility"></a>Atsakomybės ribos
Nurodyti darbuotojų funkcijas, procesus ir produktus, kad darbuotojas, kuris yra darbo padėtyje yra atsakingas už naudojate atsakomybės sritis. Pavyzdžiui, už darbą, kad pavadintas "Buhalteris", viena iš atsakomybės sričių gali būti "Finansinės atskaitomybės produkto A." Galite išlaikyti atsakomybės sritis naudojant į **atsakomybės sritis** puslapį, kuriame galite rasti naudodami paieškos funkciją. Dėl į **atsakomybės sritis** puslapyje, įveskite pavadinimą ir aprašymą, atsakomybė. – Į **Pastaba** lauką, galite pasirinktinai įvesti papildomos informacijos. Pastabos gali būti atnaujintas specifiniam darbui nekeičiant pažymi, kad įvedėte čia.


