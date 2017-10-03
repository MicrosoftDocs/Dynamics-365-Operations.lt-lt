--- 
title: "Pardavimo kainos pasirinkimo kriterijų kūrimas"
description: "Šioje procedūroje parodoma, kaip kurti pardavimo kainos pasirinkimo kriterijus, skirtus atributais pagrįstiems pardavimo kainos modeliams."
author: YuyuScheller
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 633628e6250baa74df544e814ce6e9656a2f0b06
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="create-sales-price-selection-criteria"></a>Pardavimo kainos pasirinkimo kriterijų kūrimas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip kurti pardavimo kainos pasirinkimo kriterijus, skirtus atributais pagrįstiems pardavimo kainos modeliams. Norint paleisti šią procedūrą, reikia, kad būtų galimas bent vienas pardavimo kainos modelis. Šiame pavyzdyje naudojamas kainos modelio, skirtas demonstracinių duomenų įmonės USMF garsiakalbio sprendimo pardavimo kainos modeliui. Paprastai šią procedūrą atlieka produktų vadovas.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Naujo esamo pardavimo kainos modelio kriterijaus įtraukimas
1. Spustelėkite Produkto varianto modelio aprašą.
2. Spustelėkite Produkto konfigūracijos modeliai.
3. Sąraše pasirinkite garsiakalbio sprendimo produkto modelio eilutę, bet nespustelėkite modelio pavadinimo nuorodos.
4. Veiksmų srityje spustelėkite Modelis.
5. Spustelėkite Kainos modelio kriterijai.
6. Spustelėkite Naujas.
7. Lauke Pavadinimas įveskite 10 klientų grupė.
    * Kainos modelio kriterijaus pavadinimas padeda nustatyti pagrindinius pasirinkimo kriterijus.  
8. Lauke Kainos modelis įveskite arba pasirinkite reikšmę.
9. Lauke Užsakymo tipas pasirinkite Pardavimo užsakymas.
    * Užsakymo tipas nustato duomenų bazės laukus, kuriuos bus galima naudoti teikiant pasirinkimo užklausą.  
10. Lauke Galioja nuo įveskite datą.
11. Lauke Galioja iki įveskite datą.
12. Spustelėkite Įrašyti.

## <a name="create-the-query-for-the-selection-criteria"></a>Pasirinkimo kriterijų užklausos kūrimas
1. Spustelėkite Redaguoti.
2. Lauke Lentelė pasirinkite Klientai. 
3. Lauke Laukas pasirinkite Klientų grupė.
    * Šiame pavyzdyje nustatydami pasirinkimo kriterijus mes naudosime konkrečią klientų grupę.  
4. Lauke Kriterijai pasirinkite 10 klientų grupė. 
5. Spustelėkite GERAI.


