---
title: "Retrospektyvinių duomenų importavimas į poreikio prognozėms generuoti"
description: "Norint generuoti tikslias poreikio prognozes, reikia retrospektyvinių poreikio duomenų pagal prekę arba prekių paskirstymo raktą. Šioje temoje paaiškinama, kaip naudoti duomenų objektus norint importuoti retrospektyvinius poreikio duomenis iš bet kurios sistemos, kad turėtumėte ilgesnę poreikio prognozės duomenų retrospektyvą."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e7975003620d951717c66144c8d0521de0f69158
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="import-historical-data-for-demand-forecasts"></a>Retrospektyvinių duomenų importavimas į poreikio prognozėms generuoti

[!include [banner](../includes/banner.md)]

Norint užtikrinti poreikio prognozių tikslumą, jums reikia kiek įmanoma daugiau retrospektyvinių poreikio duomenų pagal prekę arba prekių paskirstymo raktą. Jei retrospektyviniai poreikio duomenys dar neimportuoti, importuokite juos naudodami „Microsoft Dynamics 365 for Finance and Operations“ duomenų objektą **Retrospektyvinis išorinis poreikis** (ReqDemPlanHistoricalExternalDemandEntity).

Darbo srityje **Duomenų valdymas** galite peržiūrėti visų objekto laukų apžvalgą.

1. Atidarykite darbo sritį **Duomenų valdymas**.
2. Spustelėkite plytelę **Duomenų objektai**.
3. Objektų sąraše ieškokite objekto **Retrospektyvinis išorinis poreikis**.
4. Spustelėkite **Paskirties laukai**. Šie objekto laukai yra privalomi: teritorija (**DeliveringSiteId**), data (**DemandDate**), kiekis (**DemandQuantity**) ir prekės numeris (**ItemNumber**) arba prekių paskirstymo raktas (**ProductAllocationKeyId**).

Norint naudoti duomenų objektą, reikalingas „Microsoft Excel“ failas arba kableliais atskirtų verčių (CSV) failas, kuriame yra retrospektyviniai poreikio duomenys. Toliau pateikiamame pavyzdyje parodyta, kaip importuoti duomenis iš CSV failo.

## <a name="example"></a>Pavyzdys

Kaip pavyzdį galite naudoti toliau nurodytą failą. Atsisiųskite [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast). Šiame faile yra prekės D0001 retrospektyviniai poreikio duomenys. Jame yra tik šie privalomi laukai: teritorija, kiekis ir poreikio data.

1. Pasirinkite įmonę, į kurią norite importuoti į retrospektyvinius poreikio duomenis.
2. Atidarykite darbo sritį **Duomenų valdymas**.
3. Spustelėkite plytelę **Importuoti**.
4. Įveskite importavimo projekto pavadinimą, pavyzdžiui, **Prekės D0001 retrospektyvinio poreikio importavimas**.
5. Lauke **Šaltinio duomenų formatas** pasirinkite importuojamo failo formatą. Šiame pavyzdyje norėdami importuoti failą HistoricalDemandData, pvz., pasirinkite **CSV**.
6. Lauke **Objekto pavadinimas** pasirinkite **Retrospektyvinis išorinis poreikis**.
7. Įrašykite failą kompiuteryje ir tada jį įkelkite.
8. Spustelėkite **Importuoti**.
9. Automatiškai atidaromas puslapis **Vykdymo suvestinė**. Patikrinkite importuotus duomenis puslapyje.

Importavus retrospektyvinius poreikio duomenis, galima generuoti pagrindinę poreikio prognozę.

## <a name="additional-resources"></a>Papildomi ištekliai

[Pagrindinės statistinės prognozės generavimas](generate-statistical-baseline-forecast.md)

