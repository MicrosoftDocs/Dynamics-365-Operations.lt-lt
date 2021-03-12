---
title: Ciklo skaičiavimas
description: Šiame straipsnyje aprašoma, kaip ciklo skaičiavimą galite naudoti su sandėliavimo sprendimu, prieinamu modulyje Sandėlio valdymas. Šis straipsnis netaikomas sandėliavimo sprendimui, kuris prieinamas modulyje Atsargų valdymas.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca5ae06a2a6cbe410fadf464bc49071122d0342b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973815"
---
# <a name="cycle-counting"></a>Ciklo skaičiavimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip ciklo skaičiavimą galite naudoti su sandėliavimo sprendimu, prieinamu modulyje Sandėlio valdymas. Šis straipsnis netaikomas sandėliavimo sprendimui, kuris prieinamas modulyje Atsargų valdymas.

Ciklo skaičiavimas yra sandėlio procesas, kurį galite naudoti norėdami audituoti turimas atsargų prekes. Ciklo skaičiavimo procesą galima apibūdinti tolesniais trimis veiksmais.

1.  **Ciklo skaičiavimo darbo kūrimas** – ciklo skaičiavimo darbas gali būti sukuriamas automatiškai, atsižvelgiant į prekių ribinių reikšmių parametrus, arba naudojant ciklo skaičiavimo planą. Taip pat ciklo skaičiavimo darbą galite kurti rankiniu būdu, naudodami prekės arba sandėlio parametrus puslapyje **Ciklų skaičiavimo darbas pagal prekę** arba **Ciklų skaičiavimo darbas pagal vietą**.
2.  **Ciklo skaičiavimo apdorojimas** – kai ciklo skaičiavimo darbas sukurtas, jį atliekate suskaičiuodami prekes sandėlio vietoje ir mobiliuoju įrenginiu įvesdami rezultatą į „Dynamics 365 Supply Chain Management“. Taip pat galite skaičiuoti prekes sandėlio vietoje nekurdami ciklo skaičiavimo darbo. Šis procesas vadinamas *ciklo skaičiavimu vietoje*.
3.  **Apskaičiuotos reikšmės skirtumų pašalinimas** – atlikus ciklo skaičiavimą, visų prekių, kurių apskaičiuota reikšmė skiriasi, darbo būsena puslapyje **Visi darbai** bus **Laukiama peržiūros**. Šiuos skirtumus pašalinti galite puslapyje **Peržiūros laukiantis ciklo skaičiavimo darbas**.

Toliau pateiktoje iliustracijoje parodytas ciklo skaičiavimo procesas. ![Ciklo skaičiavimo proceso eiga](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a>Būtinosios ciklo skaičiavimo sąlygos
Pateiktoje lentelėje parodytos būtinosios sąlygos, kurias reikia įvykdyti prieš naudojant ciklo skaičiavimą.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Būtinoji sąlyga</th>
<th>Prekės/Paslaugos pavadinimas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Prekė</td>
<td>Prekė privalo turėti įgalintus sandėlio valdymo procesus.</td>
</tr>
<tr class="even">
<td>Sandėlis</td>
<td>Sandėlis privalo turėti įgalintus sandėlio valdymo procesus. Norėdami įgalinti sandėlio valdymo procesus, puslapyje <strong>Sandėliai</strong> pasirinkite sandėlį, tada pasirinkite parinktį <strong>Naudoti sandėlio valdymo procesus</strong>. Jei norite leisti darbuotojams perkelti padėklus ciklo skaičiavimo metu, „FastTab“ skirtuke <strong>Sandėlio valdymas</strong> pasirinkite parinktį <strong>Leisti perkelti padėklus atliekant ciklo skaičiavimą</strong>.</td>
</tr>
<tr class="odd">
<td>Darbo telkiniai</td>
<td>Nebūtina: sukurkite darbo telkinį, kuriame būtų atskirtas sandėlio darbas, atsižvelgiant į darbo tipą (šiuo atveju ciklo skaičiavimo darbas).</td>
</tr>
<tr class="even">
<td>Vietos</td>
<td>Įgalinkite ciklo skaičiavimą vietose. Norėdami įgalinti sandėlio vietos ciklo skaičiavimą, puslapyje <strong>Vietos profiliai</strong> pasirinkite parinktį <strong>Leisti ciklo skaičiavimą</strong>.</td>
</tr>
<tr class="odd">
<td>Sandėlio valdymo parametrai</td>
<td>Nustatykite ciklo skaičiavimo parametrus. Puslapyje <strong>Sandėlio valdymo parametrai</strong> nurodykite ciklo skaičiavimo numatytąjį koregavimo tipo kodą, darbo klasės ID ir darbo prioritetą.</td>
</tr>
<tr class="even">
<td>Mobilusis įrenginys</td>
<td><ul>
<li>Puslapyje <strong>Mobiliojo įrenginio meniu elementai</strong> sukurkite vieno iš toliau nurodytų metodų meniu elementą.
<ul>
<li>Vartotojo nurodomas ciklo skaičiavimas</li>
<li>Sistemos nurodomas ciklo skaičiavimas</li>
<li>Ciklo skaičiavimo grupavimas</li>
<li>Atrinkti ciklo skaičiavimą</li>
</ul>
</li>
<li>Nustatykite mobiliojo įrenginio meniu.</li>
<li>Sukurkite darbo vartotojo paskyrą ir priskirkite mobiliojo įrenginio meniu darbo vartotojo ID.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Susijusi nustatymo užduotis</td>
<td>Nustatykite sandėlio vietos ciklo skaičiavimo planą.</td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a>Automatinis ciklo skaičiavimo darbo kūrimas
Planuoti pasikartojantį ciklo skaičiavimo darbo kūrimą galima dviem būdais: nustatyti ciklo skaičiavimo ribines reikšmes arba nustatyti ciklo skaičiavimo planus.

-   Ciklo skaičiavimo ribinė vertė rodo atsargų prekių kiekį arba procentinę ribą. Ciklo skaičiavimo darbas automatiškai sukuriamas pasiekus ribinę vertę.
-   Ciklo skaičiavimo planu ciklo skaičiavimo darbas kuriamas nedelsiant arba reguliariai, naudojant paketinę užduotį. Kai sukuriamas ciklo skaičiavimo darbas, skaičiavimo darbo eilutėje pateikiama informacija apie skaičiuotiną vietą. Turimos atsargos, susietos su šia vieta, neblokuojamos ir todėl jas galima pasirinkti rezervavimui ir siuntimo apdorojimui, nors ir egzistuoja atidarytas skaičiavimo darbas.

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a>Ciklo skaičiavimo darbo kūrimas, atsižvelgiant į prekių ribinių reikšmių parametrus

Ciklo skaičiavimo darbą galima kurti tada, kai prekių skaičius neviršija konkrečios vietos ribinės reikšmės. Pavyzdžiui, vietoje, kurios ciklo skaičiavimo ribinis kiekis yra 40, yra 60 prekių. Pardavimo užsakymo operacijos metu iš vietos paimamos 25 prekės ir padedamos laikino sandėliavimo vietoje. Kadangi naujasis prekių skaičius (35) yra mažesnis už ribinį kiekį, todėl vietos ciklo skaičiavimo darbas sukuriamas automatiškai.

### <a name="schedule-cycle-counting-work"></a>Ciklo skaičiavimo darbo planavimas

Ciklo skaičiavimo planus galite nustatyti norėdami ciklo skaičiavimo darbą kurti nedelsiant arba reguliariai. Nustatydami ciklo skaičiavimo planus, galite valdyti darbo telkinį, kuriam sukurtas ciklo skaičiavimo darbas, maksimalų sukurtų skirtingose vietose esančių prekių ciklo skaičiavimų skaičių ir dienų skaičių, po kurio vėl skaičiuojama sandėlio vieta. Pavyzdžiui, prekė yra trijose sandėlio vietose ir maksimalus ciklo skaičiavimų skaičius nustatytas į **2**. Šiuo atveju, kai paleidžiate ciklo skaičiavimo planą, sukuriami du tų dviejų vietų, kuriose yra prekė, ciklo skaičiavimai. Kitas pavyzdys – dienų tarp ciklo skaičiavimų skaičių nustatote į **5**. Tokiu atveju ciklo skaičiavimo darbas sukuriamas kas penkias dienas. Tačiau jei ciklo skaičiavimo darbas apdorojamas 3 dieną, kitas ciklo skaičiavimo darbas bus sukurtas po penkių dienų nuo paskutinio ciklo skaičiavimo – 8 dieną.

## <a name="create-cycle-counting-work-manually"></a>Ciklo skaičiavimo darbo kūrimas rankiniu būdu
Norėdami ciklo skaičiavimo darbą sukurti rankiniu būdu, galite naudoti puslapį **Ciklo skaičiavimo darbas pagal prekę** arba **Ciklo skaičiavimo darbas pagal vietą**. Galite nurodyti maksimalų kurtiną ciklo skaičiavimų skaičių. Pavyzdžiui, jei sandėlio vadovas nurodo reikšmę, lygią **5**, sukuriamas penkių vietų ciklo skaičiavimo darbas, net jei prekė yra 10-yje skirtingų vietų. Taip pat galite pasirinkti darbo telkinio ID ir jam priskirti sukurtus ciklo skaičiavimo darbo ID. Kai apdorojamas ciklo skaičiavimo darbo telkinio ID, šiam darbo telkiniui priskirti ciklo skaičiavimo darbo ID apdorojami kaip grupė.

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a>Ciklo skaičiavimo atlikimas naudojant mobilųjį įrenginį
Ciklo skaičiavimo darbo apdorojimo naudojant „Supply Chain Management“ mobiliajame įrenginyje metodai yra keli.

-   **Nurodomas vartotojo** – darbuotojas gali nurodyti ciklo skaičiavimo darbo ID, kurio būsena yra **Atviras**.
-   **Nurodomas sistemos** – darbuotojui ciklo skaičiavimo darbo ID priskiria „Supply Chain Management‟.
-   **Ciklo skaičiavimo grupavimas** – darbuotojas gali grupuoti konkrečius tam tikros vietos, zonos ar darbo telkinio ciklo skaičiavimo darbo ID.
-   **Ciklo skaičiavimas vietoje** – darbuotojas gali bet kada skaičiuoti prekes sandėlio vietoje nekurdamas ciklo skaičiavimo darbo. Norėdamas ciklo skaičiavimą atlikti vietoje, darbuotojas įveda vietos ID.

Toliau pateiktu pavyzdžiu parodoma, kaip galima atlikti ciklo skaičiavimą vietoje naudojantis mobiliuoju įrenginiu. Instrukcijos, kurias darbuotojas mato įrenginyje, skiriasi ir priklauso nuo ciklo skaičiavimo vietoje meniu elemento nustatymo.

1.  Mobiliajame įrenginyje pasirinkite meniu elementą, kad apdorotumėte ciklo skaičiavimo vietoje darbą.
2.  Užregistruokite vietą, kurios ciklo skaičiavimą reikia atlikti.
3.  Užregistruokite ir patvirtinkite prekės numerį ir suskaičiuotą prekės kiekį. **Pastaba.** Ciklo skaičiavimo darbo būsena atnaujinama į **Laukiama peržiūros** arba **Uždarytas** (puslapyje **Visi darbai**), atsižvelgiant į puslapyje **Darbuotojas** nustatytus parametrus.
4.  Pasirenkama: kartokite 3 veiksmą su likusiomis vietos prekėmis ir patvirtinkite, kad nėra papildomų prekių, kurias reikėtų suskaičiuoti.

## <a name="resolve-cycle-counting-differences"></a>Ciklo skaičiavimo skirtumų pašalinimas
Jei darbo vartotojo ID parinktis **Yra ciklo skaičiavimo prižiūrėtojas** nustatyta į **Ne**, ciklo skaičiavimo skirtumas atsiranda toliau nurodytais atvejais.

-   Apskaičiuota reikšmė nėra nuokrypio ribose, nurodytose lauke **Maksimali procentinė riba** arba **Maksimali kiekio riba** (puslapyje **Darbo vartotojai**). Pavyzdžiui, vietoje turimų atsargų kiekis yra 50, o darbo vartotojo nuokrypio riba yra 10. Jei darbo vartotojas įveda reikšmę, kuri nėra nuo 40 iki 60, fiksuojamas skirtumas.
-   Apskaičiuota reikšmė skiriasi nuo turimų atsargų kiekio, o nuokrypio ribų nenustatyta.

Koreguoti apskaičiuotos reikšmės skirtumus ir patvirtinti apskaičiuotą reikšmę galite puslapyje **Laukiantis peržiūros ciklo skaičiavimas**. Modifikuotą prekės kiekio skaičių patikrinti galite puslapyje **Turimos atsargos pagal vietą**. Apskaičiuota reikšmė atmetama, jei skirtumo patvirtinti negalima.

## <a name="additional-resources"></a>Papildomi ištekliai
[Mobiliųjų įrenginių nustatymas darbui sandėlyje](configure-mobile-devices-warehouse.md)



