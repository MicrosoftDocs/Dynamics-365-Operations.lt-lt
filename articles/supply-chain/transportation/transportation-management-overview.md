---
title: Transportavimo valdymo peržiūra
description: Šioje temoje apžvelgiamos „Supply Chain Management“ transportavimo valdymo funkcijos.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench, TMSLoadBuildTemplateApply, WHSLoadTemplate, TMSTransportationStatus, TMSLoadSeal, TMSLoadBuildProposal, TMSLoadBuildWorkbench, TMSLoadBuildStrategy, TMSLoadBuildStrategyAttributeValue
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8afb7d28d9dd6487e00a2bf7e813069aac386c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807733"
---
# <a name="transportation-management-overview"></a>Transportavimo valdymo apžvalga

[!include [banner](../includes/banner.md)]

Šioje temoje apžvelgiamos „Supply Chain Management“ transportavimo valdymo funkcijos.

Modulis Transportavimo valdymas suteikia galimybę naudoti jūsų įmonės transportavimo operacijas bei leidžia identifikuoti gaunamų ir siunčiamų užsakymų tiekėjų ir maršruto planavimo sprendimus. Pavyzdžiui, galite identifikuoti greičiausią maršrutą arba mažiausią siuntos kainą. Toliau pateikiamoje lentelėje aprašomi pagrindiniai modulio Transportavimo valdymas naudojimo scenarijai.

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
<td>Pristatant / paimant galima naudoti pačios įmonės&#39;transporto priemonių parką, o pristatymo išlaidos perkeliamos klientams.</td>
<td>Vykstant siuntimo procesams, naudodami Transportavimo valdymą galite nustatyti transportavimo išlaidas ir jas perkelti klientams. Tačiau nebūtina&#39;atlikti vežėjo sąskaitų faktūrų derinimo proceso.</td>
</tr>
<tr class="odd">
<td>Pristatant / paimant galima naudoti pačios įmonės&#39;transporto priemonių parką, tačiau pristatymo išlaidos nėra&#39;perkeliamos vartotojams, nes į produktų kainas įtrauktas transportavimas.</td>
<td>Daugelio Transportavimo valdymo funkcijų&#39;nereikia. Tačiau naudodami Transportavimo valdymą galite nustatyti transportavimo tarifus ir atitinkamai pakoreguoti pardavimo kainą.</td>
</tr>
<tr class="even">
<td>Logistikos paslaugą teikia kitas tos pačios įmonės juridinis subjektas.</td>
<td><ul>
<li>Naudoti Transportavimo valdymą galite kitą juridinį subjektą traktuodami kaip bet kokį kitą vežėją. Ekonominių operacijų tarp juridinių subjektų automatizuoti&#39;negalite. Todėl šias operacijas turite tvarkyti rankiniu būdu (pvz., sukurdami pirkimo užsakymą).</li>
<li>Juridiniame subjekte, teikiančiame logistikos paslaugas, naudojant Transportavimo valdymą galima nustatyti transportavimo tarifus.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-supply-chain-management"></a>Transportavimo planavimas „Supply Chain Management“
Naudojant Transportavimo valdymą, planuoti transportavimą galima pagal užsakymus arba pagal siuntas, kurios sukuriamos pagal tuos užsakymus. Siuntos tam tikru metu egzistuoja visada, tačiau, planuojant transportavimą, jos nebūtinos. Perkėlimo užsakymai yra siuntimo scenarijaus dalis ir juos planuoti galima kartu su pardavimo užsakymais. 

![Krovinio iliustracija](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Gavimų transportavimas
Kai užsakote prekes iš tiekėjo, o prekės turi būti pristatytos į jūsų sandėlį, galite patys suorganizuoti prekių transportavimą. Naudodami „Supply Chain Management“ galite planuoti gaunamo krovinio transportavimą ir gavimą. Toliau pateiktoje iliustracijoje pavaizduota gaunamo krovinio transportavimo planavimo verslo proceso eiga. 

![Gaunamų krovinių transportavimo verslo procesų srautas](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Siuntimų transportavimas
Galite planuoti ir apdoroti siunčiamą krovinį, norėdami siųsti klientui konkrečias prekes iš įmonės sandėlio. Naudodami „Supply Chain Management“ galite planuoti siunčiamo krovinio transportavimą ir siuntimą. Toliau pateiktoje iliustracijoje pavaizduota siunčiamų krovinių apdorojimo siųsti verslo proceso eiga. 

![Siunčiamų krovinių planavimas ir apdorojimas](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Krovinio kūrimas
„Supply Chain Management‟ galima naudoti krovinio kūrimo strategiją, kuri vadinasi Tūriu pagrįsta krovinio kūrimo strategija. Naudojant šią strategiją galima naudoti maksimalias aukščio ir svorio reikšmes, nurodytas krovinio šablone, arba galima nepaisyti parametrų įvedant naujas reikšmes. Norėdami naudoti šią strategiją, pasirinkite ją lauke **Krovinio kūrimo strategija**, esančiame puslapio **Krovinio kūrimo darbo sritis** „FastTab“ skirtuke **Nustatymas**. Be to, galite įtraukti savo krovinio kūrimo strategijas sukurdami naują klasę programos objektų medyje (AOT).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]