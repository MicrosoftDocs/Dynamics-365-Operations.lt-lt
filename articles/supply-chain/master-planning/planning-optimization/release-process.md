---
title: Planavimo optimizavimo išleidimo procesas ir išleidimo retrospektyva
description: Šioje temoje pateikiama informacija apie Planavimo optimizavimo paleidimo procesą ir jo paleidimo retrospektyvą.
author: ChristianRytt
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: f9674bb68d7f577a6efdef3416d1731d743d0555
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087171"
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
| <p>Pridėtas planavimo prioritetinis palaikymas gamybos užsakymams. | Galima su 10.0.25 versija kaip funkcijos, pavadintos, dalis *Prioritetinis MRP palaikymas planavimo optimizavimui*. | 2021 m. lapkričio 12–18 d |
| <p>Bendras našumas, kokybės ir stabilumo patobulinimai. | Funkcijos valdyti nereikia. | 2021 m. lapkričio 12–18 d |
| <p>Pridėtas proceso laiko skaičiavimo formulių palaikymas, gamybos maršrutas su persidengimu ir gamybos operacijos numeris poreikio operacijose.</p><p>Patobulinti klaidų pranešimai dėl gamybos planavimo, susijusių su skirtuoju laiku, pajėgumu nepavyko rasti ir cikliniu maršrutu.</p><p>Patobulintas nuoseklumas apskaičiuojant gavimo ir išdavimo datas tiek planuojamuose, tiek patvirtintuose užsakymuose.</p><p>Bendras našumas, kokybės ir stabilumo patobulinimai. | Funkcijos pavadinimas: *Neribotas pajėgumo planavimas Planavimo optimizavimui* | 2021 m. spalio 22–27 d |
| <p>Pridėtas palaikymas skaičiuojant apdorojimo laiką, atsižvelgiant į laužo procentą.</p><p>Pridėta operacijų skaičiaus ir medžiagų naudojimo palaikymas planuojant. | Funkcijos pavadinimas: *Neribotas pajėgumo planavimas Planavimo optimizavimui* | 2021 m. spalio 5–7 d |
| <p>Pridėtas gamybos maršrutų užduočių tipų palaikymas: **Eilė prieš**, **po**, ir **Transporto laikas**.</p><p>Bendras našumas, kokybės ir stabilumo patobulinimai. | Funkcijos pavadinimas: *Neribotas pajėgumo planavimas Planavimo optimizavimui* | 2021 m. rugsėjo 25–30 d |
| <p>Įtrauktas bendrųjų planų su **Planavimo metodu** palaikymas nustatytas į *Operacijų planavimas*.</p><p>Puslapyje **Maršruto grupės** atsižvelkite į žymės langelių **Aktyvavimas**, **Darbo laikas** ir **Pajėgumas** eilėms su *Nustatymo* arba *Proceso* lauko **Maršruto/užduoties tipu**. </p><p>Bendras našumas, kokybės ir stabilumo patobulinimai. | <p>Operacijų planavimas yra prieinamas funkcijų valdymo 10.0.20 versijoje.</p><p>Funkcijos pavadinimas: *Neribotas pajėgumo planavimas Planavimo optimizavimui*</p>  | 2021 m. rugsėjo 9–17 d |
| Bendras našumas, kokybės ir stabilumo patobulinimai. | Funkcijos valdyti nereikia. | 2021 m. rugpjūčio 25-30 d. |
| <p>Įtrauktas **gamybos laiko** laukas į suplanuotus užsakymus.</p><p>Bendras našumas, kokybės ir stabilumo patobulinimai.</p> | Funkcijos valdyti nereikia. | 2021 m. rugpjūčio 12-17 dienos |
| <p>Įtraukta išteklius neriboto pajėgumo planavimo išteklių tipo reikalavimai.</p><p>Pagerintas išteklius neriboto pajėgumo planavimo išteklių ir kalendoriaus efektyvumas.</p><p>Daugiau informacijos žr. [Planavimas, naudojant neribotą pajėgumą](infinite-capacity-planning.md). | <p>Prieinama funkcijos valdymo versijoje 10.0.20.</p><p>Funkcijos pavadinimas: *Neribotas pajėgumo planavimas Planavimo optimizavimui*</p> | 2021 m. liepos 6-12 dienos |
| Bendrieji kokybės patobulinimai. | Funkcijos valdyti nereikia. | 2021 m. liepos 6-12 dienos |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
