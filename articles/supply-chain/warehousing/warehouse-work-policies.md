---
title: Sandėlio darbo strategijų apžvalga
description: Sandėlio darbo strategijos kontroliuoja, ar sandėlio darbą kuria gamybos sandėlio procesai, remdamiesi darbo užsakymo tipu, atsargų vieta ir produktu.
author: johanhoffmann
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 0a9e05fd2a08921d2718fc239afd56a957f80915
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865117"
---
# <a name="warehouse-work-policies-overview"></a>Sandėlio darbo strategijų apžvalga

[!include [banner](../includes/banner.md)]

„Microsoft Dynamics 365 for Finance and Operations“ sandėlio darbo strategijos kontroliuoja, ar sandėlio darbą kuria gamybos sandėlio procesai, remdamiesi darbo užsakymo tipu, atsargų vieta ir produktu.

Ši darbo strategija nustato, ar kuriamas gamybos sandėlio procesų sandėlio darbas. Galite nustatyti darbo strategiją naudodami **darbo užsakymų tipų**, **atsargų vietos** ir **produkto** derinį. Pavyzdžiui, produktas L0101 paskelbtas pagamintu išeigos vietoje 001. Vėliau pagaminta prekė panaudojama vykdant kitą gamybos užsakymą išeigos vietoje 001. Šiuo atveju galite nustatyti darbo strategiją, kurią taikant bei produktą L0101 paskelbus pagamintu išeigos vietoje 001 nebus sukuriamas pagamintų prekių sandėliavimo darbas. Darbo strategija yra atskiras objektas, kurį galima apibrėžti naudojant tolesnę informaciją.

-   **Darbo strategijos pavadinimas**(unikalus darbo strategijos identifikatorius)
-   **Darbo užsakymų tipai** ir **Darbo kūrimo metodas**
-   **Atsargų vietos**
-   **Produktai.**

## <a name="work-order-types"></a>Darbo užsakymo tipai
Galite rinktis iš tolesnių darbo užsakymų tipų.

-   Baigtos prekės atidėtos
-   Sudėtinis produktas ir šalutinis produktas atidėti
-   Žaliavų paėmimas

Lauke **Darbo kūrimo metodas** nustatyta reikšmė **Niekada**. Ši reikšmė nurodo, kad darbo strategija neleis sandėlyje kurti pasirinkto darbo užsakymo tipo darbo.

## <a name="inventory-locations"></a>Atsargų vietos
Galite pasirinkti vietą, kuriai darbo strategija taikoma. Jei su darbo strategija nesusiejama jokia vieta, darbo strategija netaikoma jokiam procesui. Puslapyje **Vietos** galite pažymėti arba atžymėti tam tikros vietos darbo strategiją.

## <a name="products"></a>Produktai
Galite pasirinkti produktą, kuriam darbo strategija taikoma. Darbo strategiją galite taikyti visiems produktams arba pasirinktiems produktams.

## <a name="example"></a>Pavyzdys
Šiame pavyzdyje nurodyti du gamybos užsakymai, PRD-001 ir PRD-00*2*. Gamybos užsakymui PRD-001 priskirta operacija, pavadinimu **Surinkimas**, kurioje produktas SC1 yra paskelbiamas baigtu vietoje O1. Gamybos užsakymui PRD-002 priskirta operacija, pavadinimu **Dažymas**, ir ją vykdant naudojamas produktas SC1 iš vietos O1. Gamybos užsakymas PRD-002 taip pat naudoja žaliavas RM1 iš vietos O1. RM1 saugomos sandėlio vietoje BULK-001 ir bus paimtos bei perkeltos į vietą O1, naudojant žaliavų paėmimo sandėlio darbą. Paėmimo darbas yra generuojamas, kai bus paleidžiama gamyba PRD-002. 

[![Sandėlio darbo strategijos](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png) 

Kai šiuo atveju planuojate konfigūruoti sandėlio darbo strategiją, turėtumėte atsižvelgti į tolesnę informaciją.

-   Sandėlio darbas, skirtas pagamintoms prekėms atidėti, nėra būtinas, kai produktą SC1 skelbiate baigtu iš gamybos užsakymo PRD-001 į vietą O1. Tai yra todėl, kad gamybos užsakymo PRD-002 operacija **dažymo** naudoja SC1 toje pačioje vietoje.
-   Žaliavų paėmimo sandėlio darbas yra būtinas, norint žaliavas RM1 perkelti iš sandėlio vietos BULK-001 į vietą O1.

Čia pateikiamas darbo strategijos, kurią galite nustatyti atsižvelgdami į šiuos aspektus, pavyzdys.


|                                       |                                       |
|---------------------------------------|---------------------------------------|
| <strong>Darbo strategijos pavadinimas</strong><br> | <strong>Darbo užsakymo tipai</strong><br> |
|         Sandėliavimo darbo nėra 01     `          |     - Pagamintų prekių sandėliavimas<br>      |
|                                       |    <strong>Vietos</strong><br>     |
|                                       |                 - O1                  |
|                                       |    <strong>Produktai</strong> <br>     |
|                                       |                 - SC1                 |

Tolesnėse procedūrose pateikiamos nuoseklios instrukcijos apie tai, kaip nustatyti šio scenarijaus sandėlio darbo strategijos. Taip pat aprašytas sąrankos pavyzdinis, kuriuo parodoma, kaip gamybos užsakymą skelbti baigtus vietoje, kuri nėra kontroliuojama pagal numerio lentelę.

## <a name="set-up-a-warehouse-work-policy"></a>Sandėlio darbo strategijos nustatymas
Sandėlio procesai ne visada apima sandėlio darbą. Apibrėždami darbo strategiją, galite neleisti konkrečiose vietose kurti tam tikro produktų rinkinio žaliavų paėmimo ir pagamintų prekių padėjimo darbo. Kuriant šią procedūrą naudota demonstracinių duomenų įmonė yra USMF. 

VEIKSMAI (21)

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| 1.  | Eikite į Sandėlio valdymas &gt; Nustatymas &gt; Darbas &gt; Darbo strategijos.        |
| 2.  | Spustelėkite Naujas.                                                                 |
| 3.  | Lauke Darbo strategijos pavadinimas įveskite „Atidėjimo darbo nėra‟.                    |
| 4.  | Spustelėkite Įrašyti.                                                                |
| 5.  | Spustelėkite Pridėti.                                                                 |
| 6.  | Sąraše pažymėkite pasirinktą eilutę.                                        |
| 7.  | Lauke Darbo užsakymo tipas pasirinkite Baigtos prekės atidėtos.            |
| 8.  | Spustelėkite Pridėti.                                                                 |
| 9.  | Sąraše pažymėkite pasirinktą eilutę.                                        |
| 10. | Lauke Darbo užsakymo tipas pasirinkite Sudėtinis produktas ir šalutinis produktas atidėti. |
| 11. | Išplėskite dalį Atsargų vietos.                                    |
| 12. | Spustelėkite Pridėti.                                                                 |
| 13. | Sąraše pažymėkite pasirinktą eilutę.                                        |
| 14. | Sandėlių sąraše įveskite „51‟.                                         |
| 15. | Lauke Vieta įveskite arba pasirinkite „001‟.                              |
| 16. | Išplėskite sekciją Produktai.                                               |
| 17. | Lauke Produktų pasirinkimas pasirinkite Pasirinkta.                         |
| 18. | Spustelėkite Pridėti.                                                                 |
| 19. | Sąraše pažymėkite pasirinktą eilutę.                                        |
| 20. | Lauke Prekės numeris įveskite arba pasirinkite „L0101‟.                         |
| 21. | Spustelėkite Įrašyti.                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Gamybos užsakymo skelbimas baigtu vietoje, kuri nėra kontroliuojama pagal numerio lentelę
Šioje procedūroje parodytas skelbimo baigtu vietoje, kuri nėra kontroliuojama pagal numerio lentelę, pavyzdys. Norint atlikti šią užduotį, būtina tinkama darbo strategija. Kaip nustatyti darbo strategiją, parodyta ankstesnėje procedūroje. 

VEIKSMAI (25)

<table>
<tbody>
<tr>
<td colspan="3"><strong>Antrinė užduotis: išeigos vietos nustatymas.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Eikite į Organizacijos administravimas &gt; Ištekliai &gt; Išteklių grupės.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Sąraše pasirinkite išteklių grupę &#39;5102&#39;.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Spustelėkite Redaguoti.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Lauke Išeigos sandėlis įveskite &#39;51&#39;.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Lauke Išeigos vieta įveskite &#39;001&#39;.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>001 vieta nėra kontroliuojama pagal numerio lentelę. Ne pagal numerio lentelę kontroliuojamą išeigos vietą galite nustatyti tik jei yra tinkama vietos darbo strategija.</td>
</tr>
<tr>
<td colspan="3"><strong>Antrinė užduotis: gamybos užsakymo sukūrimas ir jo skelbimas baigtu.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Uždarykite puslapį.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Eikite į Gamybos kontrolė &gt; Gamybos užsakymai &gt; Visi gamybos užsakymai.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Spustelėkite Naujas gamybos užsakymas.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Lauke Prekės numeris įveskite &#39;L0101&#39;.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Spustelėkite Kurti.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Veiksmų srityje spustelėkite Gamybos užsakymas.</td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td>Spustelėkite Įvertinti.</td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td>Spustelėkite Gerai.</td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td>Spustelėkite Pradėti.</td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td>Spustelėkite skirtuką Bendra.</td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td>Lauke Automatinis KS suvartojimas pasirinkite &#39;Niekada&#39;.</td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td>Spustelėkite GERAI.</td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td>Spustelėkite Paskelbti baigtu.</td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td>Spustelėkite skirtuką Bendra.</td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td>Lauke Leisti klaidą pasirinkite Taip.</td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td>Spustelėkite Gerai.</td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td>Veiksmų srityje spustelėkite Sandėlis.</td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td>Spustelėkite Darbo informacija.</td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td>Kai gamybos užsakymas buvo paskelbtas baigtu, nebuvo sugeneruota jokio padėjimo darbo. Taip nutinka, nes yra apibrėžta darbo strategija, pagal kurią negalima generuoti darbo, kai produktas L0101 paskebiamas baigtu 001 vietoje.</td>
</tr>
</tbody>
</table>



