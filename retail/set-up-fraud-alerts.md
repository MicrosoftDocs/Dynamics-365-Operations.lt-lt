---
title: "Įspėjimų dėl apgaulės nustatymas"
description: "Šioje temoje paaiškinama, kaip nustatyti taisykles, kad klientų aptarnavimo atstovai užsakymų apdorojimo metu būtų įspėjami apie galimai apgaulingą informaciją. Galite apibrėžti konkrečius kodus, kurie būtų naudojami norint automatiškai arba rankiniu būdu sulaikyti įtartinus užsakymus."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail Version
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7255f2b7e49f56a731d0e3745b4752091013668b
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-fraud-alerts"></a>Įspėjimų dėl apgaulės nustatymas

[!include[banner](includes/banner.md)]


Šioje temoje paaiškinama, kaip nustatyti taisykles, kad klientų aptarnavimo atstovai užsakymų apdorojimo metu būtų įspėjami apie galimai apgaulingą informaciją. Galite apibrėžti konkrečius kodus, kurie būtų naudojami norint automatiškai arba rankiniu būdu sulaikyti įtartinus užsakymus. 

Prieš nustatydami ir naudodami apgaulės patikros taisykles, turite įgalinti apgaulės patikrą ir apibrėžti pagrindines apgaulės patikros reikšmes skambučių centro parametruose. Naudojami du toliau nurodyti apgaulės taisyklių tipai.

-   **Statinės taisyklės** naudoja konkrečią reikšmę, pvz., telefono numerį, kuris buvo įtrauktas į juodąjį sąrašą.
-   **Dinaminės taisyklės** gali būti sudarytos iš kintamųjų ir sąlygų.

Prieš kurdami dinaminę taisyklę, turite sukurti kintamuosius ir sąlygas, apibrėžiančias, kam taisyklė yra taikoma ir kada ji turėtų būti taikoma. Pavyzdžiui, norite sukurti taisyklę, pagal kurią klientui 1202 pateikus 1 000,00 arba didesnės vertės užsakymą, pardavimo užsakymas turėtų būti sulaikomas, kol bus patikrintas kliento mokėjimas. Šiuo atveju kintamieji yra klientas 1202 ir užsakymo bendroji suma 1 000,00. Sąlyga nurodo, kad klientui 1202 pateikus užsakymą, kurio bendra suma yra lygi arba didesnė nei 1 000,00, pardavimo užsakymas turi būti sulaikytas, kol bus patikrintas kliento mokėjimas.




