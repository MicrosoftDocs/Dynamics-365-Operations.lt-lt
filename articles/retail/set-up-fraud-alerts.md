---
title: "Įspėjimų dėl apgaulės nustatymas"
description: "Šioje temoje paaiškinama, kaip nustatyti taisykles, kad klientų aptarnavimo atstovai užsakymų apdorojimo metu būtų įspėjami apie galimai apgaulingą informaciją. Galite apibrėžti konkrečius kodus, kurie būtų naudojami norint automatiškai arba rankiniu būdu sulaikyti įtartinus užsakymus."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 09d80015298c3d0219b6ffb290dc456990536a62
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-fraud-alerts"></a>Įspėjimų dėl apgaulės nustatymas

[!include[banner](includes/banner.md)]


Šioje temoje paaiškinama, kaip nustatyti taisykles, kad klientų aptarnavimo atstovai užsakymų apdorojimo metu būtų įspėjami apie galimai apgaulingą informaciją. Galite apibrėžti konkrečius kodus, kurie būtų naudojami norint automatiškai arba rankiniu būdu sulaikyti įtartinus užsakymus. 

Prieš nustatydami ir naudodami apgaulės patikros taisykles, turite įgalinti apgaulės patikrą ir apibrėžti pagrindines apgaulės patikros reikšmes skambučių centro parametruose. Naudojami du toliau nurodyti apgaulės taisyklių tipai.

-   **Statinės taisyklės** naudoja konkrečią reikšmę, pvz., telefono numerį, kuris buvo įtrauktas į juodąjį sąrašą.
-   **Dinaminės taisyklės** gali būti sudarytos iš kintamųjų ir sąlygų.

Prieš kurdami dinaminę taisyklę, turite sukurti kintamuosius ir sąlygas, apibrėžiančias, kam taisyklė yra taikoma ir kada ji turėtų būti taikoma. Pavyzdžiui, norite sukurti taisyklę, pagal kurią klientui 1202 pateikus 1 000,00 arba didesnės vertės užsakymą, pardavimo užsakymas turėtų būti sulaikomas, kol bus patikrintas kliento mokėjimas. Šiuo atveju kintamieji yra klientas 1202 ir užsakymo bendroji suma 1 000,00. Sąlyga nurodo, kad klientui 1202 pateikus užsakymą, kurio bendra suma yra lygi arba didesnė nei 1 000,00, pardavimo užsakymas turi būti sulaikytas, kol bus patikrintas kliento mokėjimas.




