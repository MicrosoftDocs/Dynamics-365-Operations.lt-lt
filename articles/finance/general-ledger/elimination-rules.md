---
title: Pašalinimo taisyklės
description: Šioje temoje pateikta informacija apie pašalinimo taisykles ir įvairias pašalinimo ataskaitų pasirinktis.
author: aprilolson
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c31df2526f3b852bbc2b5086ce2154310118352d43c9f8803b72d49df4a450b5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755647"
---
# <a name="elimination-rules"></a>Pašalinimo taisyklės

[!include [banner](../includes/banner.md)]

Šioje temoje pateikta informacija apie pašalinimo taisykles ir įvairias pašalinimo ataskaitų pasirinktis.

Šalinimo operacijų reikalaujama, kai pirminis juridinis subjektas bendradarbiauja su vienu ar daugiau filialo juridinių subjektų ir naudoja konsoliduotas finansines ataskaitas. Konsoliduotose finansinėse ataskaitose turi būti nurodytos tik tos operacijos, kurios vyksta tarp konsoliduotos organizacijos ir kitų ne tos organizacijos objektų. Todėl tos pačios organizacijos juridinių subjektų operacijos turi būti pašalintos iš DK, kad nebūtų rodomos finansinėse ataskaitose. Skelbti apie pašalinimus galima keliais būdais.

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
Nustatant pašalinimo taisykles, rekomenduojame sukurti finansinę dimensija, skirtą tik šalinimo veiksmams atlikti. Dauguma klientų pavadina ją Prekybos partneris arba panašiai Jei nuspręsite nenaudoti finansinės dimensijos, būtinai turėkite dvi pagrindines sąskaitas, skirtas tik vidinės įmonės operacijoms. 

Pašalinimo sąranką galima rasti modulio Konsolidavimas srityje Sąranka. Įvedę taisyklės aprašą, turite pasirinkti įmonę, kurioje pašalinimo žurnalas bus registruojamas. Tai turi būti įmonė, kurios juridinio subjekto sąrankoje pažymėta parinktis **Naudoti finansinio pašalinimo procese**. 

Jei reikia, galite nustatyti pašalinimo taisyklės galiojimo pradžios ir pabaigos datas. Turite nustatyti parinkties **Aktyvus** reikšmę **Taip**, jei norite, kad ją būtų galima naudoti pašalinimo pasiūlymo proceso metu. Pasirinkite žurnalo, kurio žurnalo tipas **Pašalinimas**, pavadinimą.

Nurodę pagrindinę informaciją, galite nustatyti pačias apdorojimo taisykles, spustelėdami **Eilutės**. Galimos dvi šalinimo parinktys: grynojo pokyčio sumos pašalinimas arba fiksuotos sumos nustatymas. 

Pasirinkite šaltinio sąskaitą. Žvaigždutę (\*) galite naudoti kaip universalųjį simbolį. Pvz., nurodžius 1\*, kaip paskirstymo duomenų šaltinis būtų pasirinktos visos sąskaitos, kurios prasideda 1. 

Pasirinkus šaltinio sąskaitas, **Sąskaitos specifikacija** nustato naudojamą paskirties įmonės sąskaitą. Pasirinkite **Šaltinis**, jei norite naudoti tą pačią pagrindinę sąskaitą, nurodytą sąskaitoje **Šaltinis**. Jei pasirinksite **Nurodyta vartotojo**, turite nurodyti paskirties sąskaitą. 

Dimensijos specifikacijos funkcija tokia pati. Jei pasirinkite **Šaltinis**, ji naudos tas pačias paskirties įmonės dimensijas, kurios naudojamos šaltinio įmonėje. Jei pasirinksite **Nurodyta vartotojo**, turėsite nurodyti paskirties įmonės dimensijas, spustelėdami meniu elementą **Paskirties dimensijos**. 

Pasirinkite šaltinio dimensijas ir finansines dimensijas bei vertes, kurios naudojamos kaip pašalinimo šaltinis.

## <a name="process-elimination-transactions"></a>Apdoroti pašalinimo operacijas
Pašalinimo operacijas galima apdoroti dviem būdais: vykdant konsolidavimo tinkle procesą arba sukuriant pašalinimo žurnalą ir paleidžiant pašalinimo pasiūlymo procesą. Šio skyriaus tikslas yra sukurti žurnalą ir paleisti pašalinimo procesą. 

Įmonėje, kuri nurodyta kaip pašalinimo įmonė, modulyje Konsolidavimas pasirinkite **Pašalinimo žurnalas**. Pasirinkę žurnalo pavadinimą spustelėkite **Eilutės**. Pasiūlymą galite paleisti pasirinkę meniu **Pasiūlymai** ir tada pasirinkę **Pašalinimo pasiūlymas**.

Pasirinktie įmonę, kuri yra konsoliduotų duomenų šaltinis, o tada pasirinktie taisyklę, kurią norite apdoroti. Įveskite pradžios datą, kad pradėtumėte ieškoti pašalinimo sumų, ir įveskite pabaigos datą, kad pabaigtumėte pašalinimo sumų iešką. Lauke **DK registravimo data** nurodyta data naudojama registruojant žurnalą DK. Spustelėję **Gerai** galite peržiūrėti sumas ir registruoti žurnalą.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]