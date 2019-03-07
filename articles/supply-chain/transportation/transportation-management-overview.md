---
title: Transportavimo valdymo peržiūra
description: Šioje temoje apžvelgiamos „Microsoft Dynamics 365 for Finance and Operations“ transportavimo valdymo funkcijos.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 918167a3ab72b3d3665cf710d8e509417b94a056
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "355615"
---
# <a name="transportation-management-overview"></a>Transportavimo valdymo peržiūra

[!include [banner](../includes/banner.md)]

Šioje temoje apžvelgiamos „Microsoft Dynamics 365 for Finance and Operations“ transportavimo valdymo funkcijos.

Modulis Transportavimo valdymas suteikia galimybę naudoti jūsų įmonės transportavimo operacijas bei leidžia identifikuoti gaunamų ir siunčiamų užsakymų tiekėjų ir maršruto planavimo sprendimus. Pavyzdžiui, galite identifikuoti greičiausią maršrutą arba mažiausią siuntos kainą. Toliau pateikiamoje lentelėje aprašomi pagrindiniai „Microsoft Dynamics 365 for Finance and Operations“ modulio Transportavimo valdymas naudojimo scenarijai.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenarijus</th>
<th>Kuo gali būti naudingas modulis Transportavimo valdymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Transportavimo veikloms naudojami išoriniai logistikos teikėjai.</td>
<td>Transportavimo valdymo naudojimas gaunamam ir / arba siunčiamam transportavimui.</td>
</tr>
<tr class="even">
<td>Pristatant / paimant galima naudoti pačios įmonės transporto priemonių parką, o pristatymo išlaidos perkeliamos klientams.</td>
<td>Vykstant siuntimo procesams, naudodami Transportavimo valdymą galite nustatyti transportavimo išlaidas ir jas perkelti klientams. Tačiau nebūtina atlikti vežėjo sąskaitų faktūrų derinimo proceso.</td>
</tr>
<tr class="odd">
<td>Pristatant / paimant galima naudoti pačios įmonės transporto priemonių parką, tačiau pristatymo išlaidos nėra perkeliamos vartotojams, nes į produktų kainas įtrauktas transportavimas.</td>
<td>Daugelio Transportavimo valdymo funkcijų nereikia. Tačiau naudodami Transportavimo valdymą galite nustatyti transportavimo tarifus ir atitinkamai pakoreguoti pardavimo kainą.</td>
</tr>
<tr class="even">
<td>Logistikos paslaugą teikia kitas tos pačios įmonės juridinis subjektas.</td>
<td><ul>
<li>Naudoti Transportavimo valdymą galite kitą juridinį subjektą traktuodami kaip bet kokį kitą vežėją. Ekonominių operacijų tarp juridinių subjektų automatizuoti negalite. Todėl šias operacijas turite tvarkyti rankiniu būdu (pvz., sukurdami pirkimo užsakymą).</li>
<li>Juridiniame subjekte, teikiančiame logistikos paslaugas, naudojant Transportavimo valdymą galima nustatyti transportavimo tarifus.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-finance-and-operations"></a>Transportavimo valdymas sprendime „Finance and Operations“
Naudojant Transportavimo valdymą, planuoti transportavimą galima pagal užsakymus arba pagal siuntas, kurios sukuriamos pagal tuos užsakymus. Siuntos tam tikru metu egzistuoja visada, tačiau, planuojant transportavimą, jos nebūtinos. Perkėlimo užsakymai yra siuntimo scenarijaus dalis ir juos planuoti galima kartu su pardavimo užsakymais. 

![Krovinio iliustracija](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Gavimų transportavimas
Kai užsakote prekes iš tiekėjo, o prekės turi būti pristatytos į jūsų sandėlį, galite patys suorganizuoti prekių transportavimą. Naudodami „Finance and Operations‟ galite planuoti gaunamo krovinio transportavimą ir gavimą. Toliau pateiktoje iliustracijoje pavaizduota gaunamo krovinio transportavimo planavimo verslo proceso eiga. 

![Gaunamų krovinių transportavimo verslo procesų srautas](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Siuntimų transportavimas
Galite planuoti ir apdoroti siunčiamą krovinį, norėdami siųsti klientui konkrečias prekes iš įmonės sandėlio. Naudodami „Finance and Operations‟ galite planuoti siunčiamų krovinių transportavimą ir pristatymą. Toliau pateiktoje iliustracijoje pavaizduota siunčiamų krovinių apdorojimo siųsti verslo proceso eiga. 

![Siunčiamų krovinių planavimas ir apdorojimas](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Krovinio kūrimas
Sprendime „Finance and Operations‟ galima naudoti krovinio kūrimo strategiją, kuri vadinasi Tūriu pagrįsta krovinio kūrimo strategija. Naudojant šią strategiją galima naudoti maksimalias aukščio ir svorio reikšmes, nurodytas krovinio šablone, arba galima nepaisyti parametrų įvedant naujas reikšmes. Norėdami naudoti šią strategiją, pasirinkite ją lauke **Krovinio kūrimo strategija**, esančiame puslapio **Krovinio kūrimo darbo sritis** „FastTab“ skirtuke **Nustatymas**. Be to, galite įtraukti savo krovinio kūrimo strategijas sukurdami naują klasę programos objektų medyje (AOT).



