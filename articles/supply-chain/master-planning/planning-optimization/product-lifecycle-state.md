---
title: Išmesti produktus, kurie turi konkrečias produkto gyvavimo ciklo būsenas
description: Šioje temoje paaiškinama, kaip išmesti produktus pagal jų gyvavimo ciklo būseną naudojant „Planning Optimization“ funkcijas.
author: ChristianRytt
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7028a509aa884589958542f7ec627d69dffcfcec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839252"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a>Išmesti produktus, kurie turi konkrečias produkto gyvavimo ciklo būsenas

[!include [banner](../../includes/banner.md)]

Išleisti produktai ir išleistų produktų versijos įskaitant **Produkto gyvavimo ciklo būsenos** laukelį. Šis laukelis jums leidžia valdyti, tarp kitų dalykų, kurie produktai yra įskaityti pagrindinio planavimo metu. Galite įtraukti, pašalinti ir redaguoti gyvavimo ciklo būsenas kaip būtina patekę į **Produkto informacijos valdymas \> Nustatymai \> Produkto gyvavimo būsena**. Kiekvienai produkto gyvavimo ciklo būsenai, nustatykite **Aktyvus planavimui** parinktį į *Taip* jei produktai, turintys šią būseną, turi būti įtraukti pagrindinio planavimo metu. Nustačius parinktį į *Ne*, susieti produktai ir variantai bus išmesti iš visų pagrindinių planavimų ir visų skaičiavimų medžiagų važtaraštyje (BOM) lygmeniu.

Išleisti produktai ir variantai, kai **Produkto gyvavimo ciklo būsenos** laukelis yra paliktas tuščias yra apdorojami taip tarsi produkto gyvavimo būsena, kai **Aktyvus planavimui** parinktis yra nustatyta į *Taip*. Kitaip tariant, jie bus įtraukti pagrindinio planavimo metu.

> [!NOTE]
> Norėdami padėti išvengti nereikalingų tiekimo siūlymų, stipriai rekomenduojame jums susieti visus negaliojančius išleistus produktus ir variantus su produkto gyvavimo ciklo būsena, kai **Aktyvus planavimui** parinktis nustatyta į *Ne*. Šis būdas yra ypač svarbus jums dirbant su produkto konfigūravimo variantais, kurie nėra panaudojami iš naujo, nes jis jums padės apsisaugoti nuo šiukšlių.

## <a name="related-resources"></a>Susiję ištekliai

Daugiau informacijos apie produktų gyvavimo ciklo būsenas rasite [Produkto gyvavimo ciklo būsenų apžvalga](../../pim/product-lifecycle.md).

Dėl išsamios informacijos apimančios žingsnius produkto gyvavimo ciklo būsenų naudojimui siekiant išmesti produktus ir pagrindinio planavimo ir BOM-level skaičiuokles, žr. [Sukurti produkto gyvavimo ciklo būseną siekiant išmesti produktus iš pagrindinio planavimo](../../pim/tasks/exclude-products-master-planning.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]