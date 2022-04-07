---
title: Retrospektyvinių duomenų importavimas į poreikio prognozėms generuoti
description: Norint generuoti tikslias poreikio prognozes, reikia retrospektyvinių poreikio duomenų pagal prekę arba prekių paskirstymo raktą. Šioje temoje paaiškinama, kaip naudoti duomenų objektus norint importuoti retrospektyvinius poreikio duomenis iš bet kurios sistemos, kad turėtumėte ilgesnę poreikio prognozės duomenų retrospektyvą.
author: t-benebo
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c52d27d6e3aa8a20d6cc1dc81e4ade981c6a8091
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/23/2022
ms.locfileid: "8470407"
---
# <a name="import-historical-data-for-demand-forecasts"></a>Retrospektyvinių duomenų importavimas į poreikio prognozėms generuoti

[!include [banner](../includes/banner.md)]

Norint užtikrinti poreikio prognozių tikslumą, jums reikia kiek įmanoma daugiau retrospektyvinių poreikio duomenų pagal prekę arba prekių paskirstymo raktą. Jei retrospektyviniai poreikio duomenys dar neimportuoti, importuokite juos naudodami „Dynamics 365 Supply Chain Management“ duomenų objektą **Retrospektyvinis išorinis poreikis** (ReqDemPlanHistoricalExternalDemandEntity).

Darbo srityje **Duomenų valdymas** galite peržiūrėti visų objekto laukų apžvalgą.

1. Atidarykite darbo sritį **Duomenų valdymas**.
2. Pasirinkite **Duomenų objektai** plytelę.
3. Objektų sąraše ieškokite objekto **Retrospektyvinis išorinis poreikis**.
4. Pasirinkite **Paskirties laukai**. Šie objekto laukai yra privalomi: teritorija (**DeliveringSiteId**), data (**DemandDate**), kiekis (**DemandQuantity**) ir prekės numeris (**ItemNumber**) arba prekių paskirstymo raktas (**ProductAllocationKeyId**).

Norint naudoti duomenų objektą, reikalingas „Microsoft Excel“ failas arba kableliais atskirtų verčių (CSV) failas, kuriame yra retrospektyviniai poreikio duomenys. Toliau pateikiamame pavyzdyje parodyta, kaip importuoti duomenis iš CSV failo.

Norėdami gauti daugiau informacijos apie duomenų importavimą, įskaitant duomenų valymą po importavimo, žiūrėkite [Duomenų importavimo ir eksportavimo užduočių apžvalga](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) ir susijusias temas.

Taip pat žiūrėkite [Pagrindinės statistinės prognozės generavimas](generate-statistical-baseline-forecast.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]