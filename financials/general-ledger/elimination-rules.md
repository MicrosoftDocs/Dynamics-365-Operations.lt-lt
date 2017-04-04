---
title: "Pašalinimo taisyklės"
description: "Šioje temoje pateikta informacija apie šias taisykles ir įvairių variantų dėl apie panaikinimą."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: db4b05bc55d735513d7580ca5908a1e84eb760c6
ms.openlocfilehash: 152b63fdfc78b3c4e79b93340d18c5cf69257024
ms.lasthandoff: 03/31/2017


---

# <a name="elimination-rules"></a>Pašalinimo taisyklės

Šioje temoje pateikta informacija apie šias taisykles ir įvairių variantų dėl apie panaikinimą.

Šalinimo operacijų reikalaujama, kai pirminis juridinis subjektas bendradarbiauja su vienu ar daugiau filialo juridinių subjektų ir naudoja konsoliduotas finansines ataskaitas. Konsoliduotose finansinėse ataskaitose turi būti nurodytos tik tos operacijos, kurios vyksta tarp konsoliduotos organizacijos ir kitų ne tos organizacijos objektų. Todėl sandorius tarp juridinių asmenų, kurie yra dalis tos pačios organizacijos turi būti pašalintas, arba pašalintas, DK, todėl jos nerodomos dėl finansinių ataskaitų. Skelbti apie pašalinimus galima keliais būdais.

-   Konsolidavimo ar pašalinimo įmonėje galima sukurti ir apdoroti pašalinimo taisyklę.
-   Galima naudoti finansines ataskaitas ir konkrečioje eilutėje arba stulpelyje rodyti pašalinimų sąskaitas ir dimensijas.
-   Galima naudoti atskirą juridinį subjektą ir rankiniu būdu registruoti operacijų įrašus siekiant sekti pašalinimus.

Šioje temoje dėmesys skiriamas pašalinimo taisyklėms, kurios apdorojamos konsolidavimo arba pašalinimo įmonėje. Galite nustatyti šalinimo taisykles, kad sukurtumėte šalinimo operacijas juridiniame subjekte, kuris nurodytas kaip šalinimo paskirties juridinis subjektas. Šis paskirties juridinis subjektas vadinamas šalinimo juridiniu subjektu. Šalinimo žurnalus galima generuoti konsolidavimo proceso metu arba naudojant šalinimo žurnalo pasiūlymą. Prieš nustatydami pašalinimo taisykles, turite susipažinti su šiomis sąlygomis:

-   **Šaltinio juridinis subjektas** – juridinis subjektas, kur užregistruotos šalinimo sumos.
-   **Paskirties juridinis subjektas** – juridinis subjektas, kur užregistruotos šalinimo taisyklės.
-   **Šalinimo juridinis subjektas** – juridinis subjektas, nurodytas kaip šalinimo paskirties juridinis subjektas.
-   **Konsoliduotas juridinis subjektas** – juridinis subjektas, sukurtas norint pranešti juridinių subjektų grupės finansinius rezultatus. Juridinių subjektų finansiniai duomenys konsoliduojami šiame juridiniame subjekte, tada naudojant sujungtus duomenis sukuriama finansinė ataskaita.

Pateiktoje lentelėje parodyti operacijų, kurias gali reikėti pašalinti, tipai.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Operacijos tipas</th>
<th>Pavyzdys</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pardavimo užsakymo įrašas ir SF išrašymas (centralizuotas vykdymas)</td>
<td>Galite parduoti produktą klientui kito jūsų organizacijos juridinio subjekto vardu.</td>
</tr>
<tr class="even">
<td>Pardavimo užsakymo įrašas (vidinės įmonės / tarp įmonių) ir SF išrašymas</td>
<td>Galima parduoti produktų tarp savo organizacijos juridinių subjektų.</td>
</tr>
<tr class="odd">
<td>Pirkimo užsakymai (centralizuotas vykdymas)</td>
<td>Atsargos, reikmenys, paslaugos, ilgalaikis turtas ir kiti produktai perkami iš tiekėjo kito jūsų organizacijos juridinio subjekto vardu.</td>
</tr>
<tr class="even">
<td>Atsargų valdymas (įmonės viduje / tarp įmonių)</td>
<td><ul>
<li>Vieno juridinio subjekto atsargas galite perkelti į kito savo organizacijos juridinio subjekto ilgalaikį turtą.</li>
<li>Vieno juridinio subjekto atsargas galite perkelti į kito savo organizacijos juridinio subjekto atsargas.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tranzitinis atsargų sekimas</td>
<td>Galite perkelti prekes tarp to paties juridinio subjekto sandėlių skirtingose geografinėse vietovėse.</td>
</tr>
<tr class="even">
<td>Centralizuotas mokėtinų sumų SF vykdymas</td>
<td>SF galite įrašyti kito savo organizacijos juridinio subjekto vardu.</td>
</tr>
<tr class="odd">
<td>Centralizuotas mokėtinų sumų mokėjimo vykdymas</td>
<td>SF galite apmokėti kito savo organizacijos juridinio subjekto vardu.</td>
</tr>
<tr class="even">
<td>Grynųjų pinigų valdymas ir iždas (centralizuotas apdorojimas)</td>
<td><ul>
<li>Galite apdoroti mokesčių mokėjimą, mokesčių grąžinimą, palūkanų išlaidas, panaudą, avansą, dividendų mokėjimą ir iš anksto sumokėtus naudojimosi turtu mokesčius arba komisinius.</li>
<li>Galite sumokėti kito savo organizacijos juridinio subjekto vardu. SF įvedama paskirties juridinio subjekto knygose, o jūs turite sudengti tarp juridinių subjektų. Pavyzdžiui, vienas juridinis subjektas apmoka darbuotojo išlaidų ataskaitą kitame juridiniame subjekte. Šiuo atveju darbuotojo išlaidų ataskaitoje yra išlaidų, susijusių su kitu juridiniu subjektu.</li>
<li>Savo organizacijoje galite perkelti grynuosius pinigus iš vieno juridinio subjekto į kitą.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Gautinos sumos (centralizuotas vykdymas)</td>
<td>Galite gauti grynųjų pinigų pagal kito juridinio subjekto kliento SF ir deponuoti čekį to juridinio subjekto banko sąskaitoje.</td>
</tr>
<tr class="even">
<td>Algalapis (centralizuotas vykdymas, vidinėje įmonėje / tarp įmonių)</td>
<td><ul>
<li>Galite mokėti kito juridinio subjekto atlyginimą. Pvz., juridinis subjektas gali mokėti savo darbuotojams atlyginimą, bet atskaityti už darbą, kurį darbuotojas atliko kitam juridiniam subjektui, apdorodamas algalapius. Arba darbuotojas pusę dienos dirbo juridiniame subjekte A, o kitą pusę – juridiniame subjekte B ir išmokos priklauso visam mokėjimui. Tokiais atvejais darbuotojo užmokestis apima mokėjimą iš abiejų juridinių subjektų. Užregistruojami ne tik atlyginimai, bet ir mokesčiai, išmokos, atskaitymai ir atlyginimų kaupimas.</li>
<li>Galite perkelti darbą iš vieno padalinio į kitą.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Ilgalaikis turtas (vidinės įmonės / tarp įmonių)</td>
<td>Galite perkelti ilgalaikį turtą į kito juridinio subjekto ilgalaikį turtą ar atsargas.</td>
</tr>
<tr class="even">
<td>Paskirstymai (vidinės įmonės / tarp įmonių)</td>
<td>Galite apdoroti įmonės paskirstymą. Paskirstymas yra bet kurios paskirstomos sąskaitos veikla nepaisant parengimo modulio.</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Pavyzdys
Jūsų juridinis subjektas (juridinis subjektas A) parduoda daiktus kitam jūsų organizacijos juridiniam subjektui (juridinis subjektas B). Pateiktame pavyzdyje parodyta, kaip gali tekti pašalinti dviejų juridinių subjektų atliekamas operacijas:

-   Juridinis subjektas A parduoda daiktą, kuris kainuoja 10,00, juridiniam subjektui B už 10,00.
-   Juridinis subjektas A parduoda daiktą, kuris kainuoja 10,00, juridiniam subjektui B už 10,00 bei apmoka faktines siuntimo išlaidas (2,00).
-   Juridinis subjektas A parduoda daiktą, kuris kainuoja 10,00, juridiniam subjektui B už 15,00 ir pripažįsta šio pardavimo maržą.
-   Juridinis subjektas A parduoda daiktą, kuris kainuoja 10,00, juridiniam subjektui B už 15,00 ir pripažįsta pusę šio pardavimo maržos. Juridinis subjektas B pripažįsta kitą šio pardavimo maržos pusę. Todėl įplaukos išskaidomos. Įplaukų išskaidymas suteikia stimulą užsakyti iš kito organizacijos juridinio subjekto, o ne išorinės organizacijos.

Visos šios operacijos sukuria vidinės įmonės operacijas, kurios užregistruojamos sąskaitose iki ir nuo. Be to, šios operacijos gali apimti antkainio ir kainos sumažinimo sumas, kai vidinės įmonės pardavimo suma nėra lygi parduotų prekių išlaidoms.

## <a name="set-up-elimination-rules"></a>Nustatyti pašalinimo taisykles
Kuriant šias taisykles Dynamics 365 operacijoms, rekomenduojame kad jums sukurti finansinių aspektų specialiai pašalinimo tikslais. Dauguma klientų gali prireikti prekybos partneris ar kažkas panašaus. Jei nusprendžiate nenaudoti finansinių aspektų, tada būtinai turi pagrindinės sąskaitos, būdingas tik vid. 

Pašalinimų nustatymą randamas nustatymo srityje konsolidavimo modulis. Po to, kai jūs įveskite taisyklės aprašymą, jūs turite pasirinkti įmonę, kuri sukurtame pašalinimo žurnale registruos. Tai turėtų būti bendrovės, kuri turi **naudoti finansų pašalinimo proceso** pasirinktas juridinio asmens nustatymo. 

Jei reikia, gali nustatyti datą, pašalinimo taisyklė įsigalioja ir kai ji yra pasibaigęs. Turite nustatyti **veiklioji** į **taip** jei norite, kad jį būtų galima pašalinti pasiūlymo procesą. Pasirinkite žurnalo pavadinimas, kuris yra tam tikros rūšies **pašalinti**.

Kai apibrėžėte pagrindai, galite nustatyti faktiško perdirbimo taisykles spustelėdami **linijos**. Yra du variantai, panaikinimą, panaikinti grynojo pokyčio dydį arba nustatyti tam tikros sumos. 

Pasirinkite savo pirminę sąskaitą. Galite naudoti žvaigždutę (\*) kaip pakaitos simbolį. Pvz., 1\* pasirinkite visų sąskaitų, kurios paleidžiamos su 1 kaip šaltinio duomenų paskirstymo. 

Po to, kai jūs pasirinkote savo šaltinio sąskaitos, ir **sąskaitos specifikacija** nustato sąskaitą iš paskirties vietos bendrovės, kuri yra naudojama. Pasirinkite **šaltinio** jei norite naudoti patį nurodyta sąskaita į **šaltinio** sąskaitos. Jei pasirinksite **nustatyta vartotojo**, tada jūs turite nurodyti paskirties abonemento. 

Dimensijos specifikacijos veikia tokiu pačiu būdu. Jei pasirinksite **šaltinio**, jis bus naudojamas tų pačių dydžių įmonėje kaip pirminę įmonę. Jei pasirinksite **nustatyta vartotojo**, jums reikės nurodyti dimensijas įmonėje spustelėdami į **paskirties dimensijos** meniu punktą. 

Pasirinkite šaltinio matmenis ir finansinės dimensijos ir reikšmes, kurios naudojamos kaip šaltinio, panaikinimą.

## <a name="process-elimination-transactions"></a>Apdoroti pašalinimo operacijas
Yra du būdai, kaip proceso pašalinimo operacijos, konsoliduoti internete proceso metu arba sukurtame pašalinimo žurnale sukurdami ir paleisdami pašalinimo pasiūlymo procesą. Šiame skyriuje pagrindinis dėmesys skiriamas žurnalo kūrimo ir veikia pašalinimo procesas. 

Įmonė apibrėžiama kaip įmonė panaikinimo, pasirinkite **sukurtame pašalinimo žurnale** konsolidavimo modulyje. Kai pasirinksite žurnalo pavadinimo, spustelėkite **linijos**. Galite paleisti pasiūlymo pasirinkdami į **pasiūlymų** meniu ir pasirinkę **pašalinti pasiūlymą**.

Pasirinkite įmonę, kuri yra konsoliduotų duomenų šaltinį, o tada pasirinkite taisyklę, kad norite apdoroti. Įveskite pradėti pašalinimo sumos ieškoti pradžios datą ir pabaigos datą, pabaigos paieškos data panaikinimo sumas. Į **GL registravimo data** lauke yra data, naudojama registruojant DK žurnalą. Po to, kai spustelite **gerai**, galite peržiūrėti sumas ir registruoti į žurnalą.


