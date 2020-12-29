---
title: Pardavimo kainos pasirinkimo kriterijų kūrimas
description: Šioje procedūroje parodoma, kaip kurti pardavimo kainos pasirinkimo kriterijus, skirtus atributais pagrįstiems pardavimo kainos modeliams.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ae444008e550d808a02d55dad02cc1b52874f0d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433584"
---
# <a name="create-sales-price-selection-criteria"></a>Pardavimo kainos pasirinkimo kriterijų kūrimas

[!include [banner](../../includes/banner.md)]

Šioje procedūroje parodoma, kaip kurti pardavimo kainos pasirinkimo kriterijus, skirtus atributais pagrįstiems pardavimo kainos modeliams. Norint paleisti šią procedūrą, reikia, kad būtų galimas bent vienas pardavimo kainos modelis. Šiame pavyzdyje naudojamas kainos modelio, skirtas demonstracinių duomenų įmonės USMF garsiakalbio sprendimo pardavimo kainos modeliui. Paprastai šią procedūrą atlieka produktų vadovas.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Naujo esamo pardavimo kainos modelio kriterijaus įtraukimas
1. Spustelėkite Produkto varianto modelio aprašą.
2. Spustelėkite Produkto konfigūracijos modeliai.
3. Sąraše pasirinkite garsiakalbio sprendimo produkto modelio eilutę, bet nespustelėkite modelio pavadinimo nuorodos.
4. Veiksmų srityje spustelėkite Modelis.
5. Spustelėkite Kainos modelio kriterijai.
6. Spustelėkite Naujas.
7. Lauke Pavadinimas įveskite „10 klientų grupė“.
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

