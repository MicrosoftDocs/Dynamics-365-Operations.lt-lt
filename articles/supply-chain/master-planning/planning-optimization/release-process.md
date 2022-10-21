---
title: Planavimo optimizavimo išleidimo procesas ir išleidimo retrospektyva
description: Šiame straipsnyje pateikiama informacija apie paleidimo procesą ir planavimo optimizavimo paleidimo retrospektyvą.
author: t-benebo
ms.date: 10/14/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: e2437214b4a2a850f121bb86272bf7dc3d313507
ms.sourcegitcommit: b3579ac62e1ea15664a114abcc2409cad76d4f19
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/14/2022
ms.locfileid: "9682566"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Planavimo optimizavimo išleidimo procesas ir išleidimo retrospektyva

[!include [banner](../../includes/banner.md)]

"Microsoft" kas mėnesį atnaujina Planavimo optimizavimą. Tačiau, atsižvelgdami į verslo reikalavimus, mes kartais išleidžiame papildomus suplanuotų paleidimų atnaujinimus.

Kiekvienas paleidimas publikuojamas atskiriems regionams, kuriuose galimas Planavimo optimizavimas. Paprastai procesas užtrunka tris dienas.

Atnaujinant Planavimo optimizavimą, pagrindinis planavimas gali veikti lėčiau nei paprastai.

Aplinkos, kurios naudoja Planavimo optimizavimą, automatiškai gauna naujausią leidimą. Nereikia jokio vartotojo veiksmo: paslauga atnaujinama automatiškai. Tačiau kai kurie lūžio pakeitimo funkcionalumai nevisada automatiškai įstūmiami į aplinkas. Pagal numatytuosius nustatymus visi pakeitimai, kurie laikomi lūžio atveju, yra išjungiami ir turi būti aiškiai įjungti naudojant [priemonių valdymą](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Todėl šie pakeitimai nebus rodomi aplinkose, kol nepasirinksite juos įgalinti.

Kadangi atnaujinant Planavimo optimizavimą jūsų aplinkoje pranešimai nerodomai, todėl norėdami nustatyti, kada buvo išleisti pakeitimai ir kokią funkciją jie turi, galite peržiūrėti toliau pateiktoje lentelėje pateiktas išleidimo pastabas. Šioje lentelėje pateikiami keitimai, kurie buvo išleisti Planavimo optimizavimui, neatsižvelgiant į tai, ar šie pakeitimai yra susieti su funkcijų valdymo priemone, ir paleidimo data.

| Pakeitimai | Funkcijų valdymo duomenys | Išleidimo datos |
|---|---|---|
| <p>[Paketo perdavimo kodai](../../inventory/batch-disposition-codes.md)</p><p>Įtraukti turimų atsargų ir atsargų operacijų parametrus į bendrąjį planą</p><p>Bendras našumas, kokybės ir stabilumo patobulinimai</p> | Nereikia jokio priemonių valdymo | 2022 m. spalio 10–14 d. |
| <p>[Išteklių planavimas, kai pajėgumas ribotas](finite-capacity.md)</p><p>Bendras našumas, kokybės ir stabilumo patobulinimai</p> | Nereikia jokio priemonių valdymo | 2022 m. rugsėjo 19–23 d. |
| Bendras našumas, kokybės ir stabilumo patobulinimai | Nereikia jokio priemonių valdymo | 2022 m. rugpjūčio 29 d. – rugsėjo 3 d. |
| <p>[Centralizuoto kalendoriaus priežiūra](../supply-chain-calendars-master-planning.md)</p><p>[Pasiūlymai, kaip optimizuoti esamą tiekimą](../action-messages.md)</p><p>[Subrangos palaikymas](../../production-control/manage-subcontract-work-production.md)</p><p>Bendras našumas, kokybės ir stabilumo patobulinimai</p> | Nereikia jokio priemonių valdymo | 2022 m. kovo 7–11 d. |
| Gamybos užsakymų planavimo prioriteto palaikymas | Prieinamas su versija 10.0.25 *kaip funkcijos, pavadintos prioriteto valdoma mRP palaikavimu planavimo optimizavimui, dalis*. | 2021 m. lapkričio 12–18 d. |
| Bendras našumas, kokybės ir stabilumo patobulinimai | Nereikia jokio priemonių valdymo | 2021 m. lapkričio 12–18 d. |
| <p>Laiko skaičiavimo formulių, gamybos maršruto su persidengimu ir gamybos operacijos numerio palaikymas poreikio operacijose</p><p>Išplėstiniai klaidų pranešimai, skirti gamybos planavimui, susijusiam su skirtasis laikas, pajėgumu, nepavyko rasti ir ciklinių maršrutų</p><p>Patobulintas vientisumas skaičiuojant gavimo datas ir išdavimo datas suplanuotuose užsakymuose ir patvirtintiuose užsakymuose</p><p>Bendras našumas, kokybės ir stabilumo patobulinimai</p> | Funkcijos pavadinimas: *Neribotas pajėgumo planavimas Planavimo optimizavimui* | 2021 m. spalio 22–27 d. |
| <p>Palaikymas siekiant atsižvelgti į nurašymo procentą skaičiuojant apdorojimo laiką</p><p>Operacijos numerio ir medžiagų naudojimo palaikymas planavimo metu</p> | Funkcijos pavadinimas: *Neribotas pajėgumo planavimas Planavimo optimizavimui* | 2021 m. spalio 5–7 d. |
| <p>Gamybos maršruto užduočių tipų: eilė **prieš**, eilė **po** ir transportavimo **laikas**</p><p>Bendras našumas, kokybės ir stabilumo patobulinimai</p> | Funkcijos pavadinimas: *Neribotas pajėgumo planavimas Planavimo optimizavimui* | 2021 m. rugsėjo 25–30 d. |
| <p>Bendrojo planų palaikymo metodas, **kai planavimo metodas** nustatytas kaip *Operacijų planavimas*</p><p>Maršrutų **grupių puslapyje**, eilučių **·** **·** **·** **, kurių maršruto/užduoties tipas Nustatymas arba Procesas, žymės langelių Aktyvinimas, Darbo** *laikas ir Pajėgumas* parametrų *nustatymas* </p><p>Bendras našumas, kokybės ir stabilumo patobulinimai</p> | <p>Funkcijų valdymo operacijų planavimas galimas versijoje 10.0.20</p><p>Funkcijos pavadinimas: *Neribotas pajėgumo planavimas Planavimo optimizavimui*</p> | 2021 m. rugsėjo 9–17 d |
| Bendras našumas, kokybės ir stabilumo patobulinimai | Nereikia jokio priemonių valdymo | 2021 m. rugpjūčio 25-30 d. |
| <p>Įtrauktas **gamybos laiko** laukas į suplanuotus užsakymus.</p><p>Bendras našumas, kokybės ir stabilumo patobulinimai.</p> | Nereikia jokio priemonių valdymo | 2021 m. rugpjūčio 12-17 dienos |
| <p>Neriboto pajėgumo planavimo įtraukti išteklių tipo reikalavimai</p><p>Patobulintas išteklių efektyvumas ir kalendoriaus efektyvumas planuojant neribotą pajėgumą</p><p>Daugiau informacijos ieškokite Planavimas su [neribotu pajėgumu](infinite-capacity-planning.md)</p> | <p>Yra funkcijų valdymo versijoje 10.0.20</p><p>Funkcijos pavadinimas: *Neribotas pajėgumo planavimas Planavimo optimizavimui*</p> | 2021 m. liepos 6-12 dienos |
| Bendrieji kokybės patobulinimai | Nereikia jokio priemonių valdymo | 2021 m. liepos 6-12 dienos |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
