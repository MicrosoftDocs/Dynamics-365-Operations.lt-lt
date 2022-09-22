---
title: Planavimo optimizavimo išleidimo procesas ir išleidimo retrospektyva
description: Šiame straipsnyje pateikiama informacija apie paleidimo procesą ir planavimo optimizavimo paleidimo retrospektyvą.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 2f91c46367ee2f881476a496555f15454c9f6baa
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542326"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Planavimo optimizavimo išleidimo procesas ir išleidimo retrospektyva

[!include [banner](../../includes/banner.md)]

"Microsoft" kas mėnesį atnaujina Planavimo optimizavimą. Tačiau, atsižvelgdami į verslo reikalavimus, mes kartais išleidžiame papildomus suplanuotų paleidimų atnaujinimus.

Kiekvienas paleidimas publikuojamas atskiriems regionams, kuriuose galimas Planavimo optimizavimas. Paprastai procesas užtrunka tris dienas.

Atnaujinant Planavimo optimizavimą, pagrindinis planavimas gali veikti lėčiau nei paprastai.

Aplinkos, kurios naudoja Planavimo optimizavimą, automatiškai gauna naujausią leidimą. Nereikia jokio vartotojo veiksmo: paslauga atnaujinama automatiškai. Tačiau kai kurie lūžio pakeitimo funkcionalumai nevisada automatiškai įstūmiami į aplinkas. Pagal numatytuosius nustatymus visi pakeitimai, kurie laikomi lūžio atveju, yra išjungiami ir turi būti aiškiai įjungti naudojant [priemonių valdymą](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Todėl šie pakeitimai nebus rodomi aplinkose, kol nepasirinksite juos įgalinti.

Kadangi atnaujinant Planavimo optimizavimą jūsų aplinkoje pranešimai nerodomai, todėl norėdami nustatyti, kada buvo išleisti pakeitimai ir kokią funkciją jie turi, galite peržiūrėti toliau pateiktoje lentelėje pateiktas išleidimo pastabas. Šioje lentelėje pateikiami keitimai, kurie buvo išleisti Planavimo optimizavimui, neatsižvelgiant į tai, ar šie pakeitimai yra susieti su funkcijų valdymo priemone, ir paleidimo data.

<!-- KFM: Add this? [Use batch disposition codes to mark batches as available or unavailable](../../inventory/batch-disposition-codes.md) --> 

| Pakeitimai | Funkcijų valdymo duomenys | Išleidimo datos |
|---|---|---|
| <p>Bendras našumas, kokybės ir stabilumo patobulinimai. | Funkcijos valdyti nereikia. | 2022 m. rugpjūčio 29 d. – rugsėjo 3 d. |
| <p>Bendras našumas, kokybės ir stabilumo patobulinimai.<p>[Planavimo optimizavimo centralizuota kalendoriaus priežiūra](../supply-chain-calendars-master-planning.md)<p>[Esamo tiekimo optimizavimo pasiūlymų planavimas](../action-messages.md)<p>[Subrangos planavimo optimizavimo palaikymas](../../production-control/manage-subcontract-work-production.md) | Funkcijos valdyti nereikia. | 2022 m. kovo 7–11 d. |
| <p>Įtrauktas gamybos užsakymų planavimo prioritetas. | Prieinamas su versija 10.0.25 *kaip funkcijos, pavadintos prioriteto valdoma mRP palaikavimu planavimo optimizavimui, dalis*. | 2021 m. lapkričio 12–18 d. |
| <p>Bendras našumas, kokybės ir stabilumo patobulinimai. | Funkcijos valdyti nereikia. | 2021 m. lapkričio 12–18 d. |
| <p>Įtrauktas proceso laiko skaičiavimo formulių, gamybos maršruto su persidengimu ir gamybos operacijos numerio palaikymas poreikio operacijose.</p><p>Išplėstiniai klaidų pranešimai, skirti gamybos planavimui, susijusiam su skirtasis laikas, pajėgumu, nepavyko rasti ir ciklinio maršruto.</p><p>Patobulintas vientisumas skaičiuojant gavimo datas ir išdavimo datas suplanuotuose užsakymuose ir patvirtintiuose užsakymuose.</p><p>Bendras našumas, kokybės ir stabilumo patobulinimai. | Funkcijos pavadinimas: *Neribotas pajėgumo planavimas Planavimo optimizavimui* | 2021 m. spalio 22–27 d. |
| <p>Pridėtas palaikymas siekiant įtraukti nurašymo procentą skaičiuojant apdorojimo laiką.</p><p>Įtrauktas operacijos numerio ir medžiagų naudojimo palaikymas planavimo metu. | Funkcijos pavadinimas: *Neribotas pajėgumo planavimas Planavimo optimizavimui* | 2021 m. spalio 5–7 d. |
| <p>Įtrauktas gamybos maršruto užduočių tipų palaikymas: eilė **prieš**, **eilė po** ir **transportavimo laikas**.</p><p>Bendras našumas, kokybės ir stabilumo patobulinimai. | Funkcijos pavadinimas: *Neribotas pajėgumo planavimas Planavimo optimizavimui* | 2021 m. rugsėjo 25–30 d. |
| <p>Įtrauktas bendrųjų planų su **Planavimo metodu** palaikymas nustatytas į *Operacijų planavimas*.</p><p>Puslapyje **Maršruto grupės** atsižvelkite į žymės langelių **Aktyvavimas**, **Darbo laikas** ir **Pajėgumas** eilėms su *Nustatymo* arba *Proceso* lauko **Maršruto/užduoties tipu**. </p><p>Bendras našumas, kokybės ir stabilumo patobulinimai. | <p>Operacijų planavimas yra prieinamas funkcijų valdymo 10.0.20 versijoje.</p><p>Funkcijos pavadinimas: *Neribotas pajėgumo planavimas Planavimo optimizavimui*</p>  | 2021 m. rugsėjo 9–17 d |
| Bendras našumas, kokybės ir stabilumo patobulinimai. | Funkcijos valdyti nereikia. | 2021 m. rugpjūčio 25-30 d. |
| <p>Įtrauktas **gamybos laiko** laukas į suplanuotus užsakymus.</p><p>Bendras našumas, kokybės ir stabilumo patobulinimai.</p> | Funkcijos valdyti nereikia. | 2021 m. rugpjūčio 12-17 dienos |
| <p>Įtraukta išteklius neriboto pajėgumo planavimo išteklių tipo reikalavimai.</p><p>Pagerintas išteklius neriboto pajėgumo planavimo išteklių ir kalendoriaus efektyvumas.</p><p>Daugiau informacijos žr. [Planavimas, naudojant neribotą pajėgumą](infinite-capacity-planning.md). | <p>Prieinama funkcijos valdymo versijoje 10.0.20.</p><p>Funkcijos pavadinimas: *Neribotas pajėgumo planavimas Planavimo optimizavimui*</p> | 2021 m. liepos 6-12 dienos |
| Bendrieji kokybės patobulinimai. | Funkcijos valdyti nereikia. | 2021 m. liepos 6-12 dienos |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
