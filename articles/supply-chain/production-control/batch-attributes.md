---
title: Paketo atributai
description: Šioje temoje pateikiama informacija apie paketo atributus. Paketo atributai yra žaliavų ir pagamintų produktų, kurie sudaro atsargų paketus, savybės. Šioje temoje taip pat aiškinama, kaip priskirti paketo atributus ir kaip galima jų ieškoti rezervuojant paketus.
author: ShylaThompson
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 370893e415a79091404f1c4eb0404ba8fd5b9ff2
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433943"
---
# <a name="batch-attributes"></a>Paketo atributai

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie paketo atributus. Paketo atributai yra žaliavų ir pagamintų produktų, kurie sudaro atsargų paketus, savybės. Šioje temoje taip pat aiškinama, kaip priskirti paketo atributus ir kaip galima jų ieškoti rezervuojant paketus.

Paketo atributai yra žaliavų ir pagamintų produktų, kurie sudaro atsargų paketus, savybės. Paketo atributai gali skirtis, atsižvelgiant į tokius veiksnius, kaip aplinkos sąlygos, žaliavų, naudojamų gaminant paketą, kokybė arba baigto produkto rezultatas. Naudojamų paketo atributų skaičius ir tipas skirtingose pramonės šakose gali būti labai įvairus. Štai du pavyzdžiai, kaip naudoti paketo atributus:

-   Sūrio pramonėje pieno, kuris yra viena iš žaliavų, naudojamų sūriui gaminti, atributai gali būti, pvz., riebalų kiekis ir procentinis svoris. Sūrio, gaminamo iš pieno, atributai gali būti kiti, pvz., drėgmė ir amžius.
-   Plieno pramonėje pagamintos geležies atributai gali būti, pvz., magnio, sidabro ir cinko kiekis procentais.

Norėdami geriau valdyti atributų skaičių ir tipus, galite naudoti paketo atributų grupes. Tokiu būdu jums nereikės įtraukti kiekvieno atributo atskirai.

## <a name="assign-batch-attributes"></a>Paketo atributų priskyrimas
Galite priskirti paketo atributus atskiriems produktams, esantiems atsargų paketuose, arba galite juos priskirti produktams, susietiems su konkrečiais klientais. Kad galėtumėte priskirti paketo atributą kliento lygiu, turite priskirti jį produkto lygiu. Produkto paketo dimensija sekimo dimensijų grupėje turi būti nustatyta kaip **Aktyvi**. Norėdami priskirti paketo atributą atskiram produktui, naudokite konkretaus produkto puslapį. Jei atributas būdingas klientui skirtam produktui, naudokite konkretaus kliento puslapį. Kai įtraukiate atributą į produktą, taip pat apibrėžiate kitus parametrus. Štai keletas pavyzdžių:

-   Mažiausias ir didžiausias atributo, kurio tipas **Sveikasis skaičius** arba **Trupmena** diapazonas.
-   Atributo, kurio tipas **Sveikasis skaičius** arba **Trupmena**, nuokrypio veiksmai. Jei atributo vertė nepatenka į mažiausią ir didžiausią diapazoną, veiksmas gali būti įspėjimas arba klaidos pranešimas.
-   Atributo tikslinė vertė. Ši vertė yra optimali atributo vertė, ir ji taikoma visiems atributų tipams.

Galite pasiekti produktų, kuriuos pasirinkote dalies Produkto informacijos valdymas puslapyje **Patvirtinti produktai**, puslapius. Produktui priskyrę paketo atributus, puslapyje **Atsargų paketo atributai** galite į atributus įtraukti tam tikras vertes.

## <a name="reserve-batches"></a>Paketų rezervavimas
Galite ieškoti paketo atributuose, kai atliekate pardavimo užsakymo paketo rezervavimus, kad įvykdytumėte kliento užsakymą, arba kai išrenkate ir rezervuojate paketus gamybos užsakymui. Ieška padės rasti atsargų paketą, kuriame yra produktas su paketo atributu, kurio norite. Radę paketą ar paketus galite rezervuoti produktą į atsiradusią atsargų operacijos eilutę.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]