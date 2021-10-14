---
title: Pardavimo kainos pasirinkimo kriterijų kūrimas
description: Šioje procedūroje parodoma, kaip kurti pardavimo kainos pasirinkimo kriterijus, skirtus atributais pagrįstiems pardavimo kainos modeliams.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed7083f289948033782f74dd9ed1b3c2d2a73aea
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568452"
---
# <a name="create-sales-price-selection-criteria"></a>Pardavimo kainos pasirinkimo kriterijų kūrimas

[!include [banner](../../includes/banner.md)]

Šioje procedūroje parodoma, kaip kurti pardavimo kainos pasirinkimo kriterijus, skirtus atributais pagrįstiems pardavimo kainos modeliams. Norint paleisti šią procedūrą, reikia, kad būtų galimas bent vienas pardavimo kainos modelis. Šiame pavyzdyje naudojamas kainos modelio, skirtas demonstracinių duomenų įmonės USMF garsiakalbio sprendimo pardavimo kainos modeliui. Paprastai šią procedūrą atlieka produktų vadovas.

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Naujo esamo pardavimo kainos modelio kriterijaus įtraukimas

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Produkto konfigūracijos modeliai**.
1. Sąraše pasirinkite garsiakalbio sprendimo produkto modelio eilutę, bet rinkitės modelio pavadinimo nuorodos.
1. Veiksmų srityje pasirinkite **Modelis**.
1. Rinkitės **Kainos modelio kriterijus**.
1. Pasirinkite **Naujas**.
1. Lauke **Pavadinimas** įveskite „10 klientų grupė“.
    * Kainos modelio kriterijaus pavadinimas padeda nustatyti pagrindinius pasirinkimo kriterijus.  
1. Lauke **Kainos modelis** įveskite arba pasirinkite reikšmę.
1. Lauke **Užsakymo tipas** pasirinkite *Pardavimo užsakymas*.
    * Užsakymo tipas nustato duomenų bazės laukus, kuriuos bus galima naudoti teikiant pasirinkimo užklausą.  
1. Lauke **Galioja nuo** įveskite datą.
1. Lauke **Galioja iki** įveskite datą.
1. Pasirinkite **Įrašyti**.

## <a name="create-the-query-for-the-selection-criteria"></a>Pasirinkimo kriterijų užklausos kūrimas

1. Pasirinkite **Redaguoti**.
2. Lauke **Lentelė** pasirinkite *Klientai*.
3. Lauke **Laukas** pasirinkite *Klientų grupė*.
    * Šiame pavyzdyje nustatydami pasirinkimo kriterijus mes naudosime konkrečią klientų grupę.  
4. Lauke **Kriterijai** pasirinkite *10 klientų grupė*.
5. Pasirinkite **Gerai**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]