---
title: Konteinerio veiklų objektas
description: Šiame straipsnyje pateikiama informacija apie konteinerių veiklą, kuri naudojama konteinerių siuntimo eigai sekti.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 6a518003f8624ef05ac86be1b963c3f916420278
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/15/2022
ms.locfileid: "9167580"
---
# <a name="container-activities-entity"></a>Konteinerio veiklų objektas

[!include [banner](../includes/banner.md)]

Konteinerių veikla naudojama siuntimo konteinerių eigai sekti. Sukuriamas kiekvienos atkarpos, priskirtos ciklo šablonui, kuris pasirenkamas kuriant siuntimo konteinerį, įrašas. Įrašai taip pat sukuriami, kai siuntimo konteineris sukuriamas naudojant duomenų objektą.

Informacija apie tranzitinį siuntimo konteinerio eigą dažnai gaunamas iš išorinio šaltinio. Konteinerių veiklos objektas leidžia išoriniam šaltiniui, pavyzdžiui, krovinių ekspeditorių, tiesiogiai atnaujinti įrašą. Todėl nereikia rankiniu būdu atnaujinti duomenų.

## <a name="container-activities-itmcontaineractivityentity"></a>Konteinerių veikla (ITMContainerActivityEntity)

Norėdami sukurti papildomų veiklos įrašų, galite naudoti`ITMContainerActivityEntity` konteinerio veiklos objektą (). Krovinių ekspeditoriai taip pat gali perduoti atnaujinimus patvirtintai faktinės **pabaigos datos vertei**.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Faktinė pabaigos data | ITMContainerActivityTable.ActualEndDate | Datetime | Ne | Ne |
| Pristatymo būdas | ITMContainerActivityTable.DlvModeId | Nvarchar(10) | Ne | Ne |
| Numatyta pabaigos data | ITMContainerActivityTable.EsimatedDate | Datetime | Ne | Ne |
| Eilutės numeris | ITMContainerActivityTable.LineNum | Skaitinis(32, 16) | **Taip** | Ne |
| Pastabos | ITMContainerActivityTable.Notes | nvarchar(MAKS) | Ne | Ne |
| Veikla | ITMContainerActivityTable.ShipActivityId | Nvarchar(10) | Ne | **Taip** |
| Gabenimo konteineris | ITMContainerActivityTable.ShipContainerId | Nvarchar(20) | **Taip** | **Taip** |
| Reisas | ITMContainerActivityTable.ShipId | Nvarchar(20) | **Taip** | **Taip** |
| Atkarpa | ITMContainerActivityTable.ShipLegId | Nvarchar(20) | Ne | **Taip** |
| Paslaugos teikėjas | ITMContainerActivityTable.ShipServiceProvider | Nvarchar(20) | Ne | Ne |
| Temperatūra | ITMContainerActivityTable.ShipTemperioture | Skaitinis(32, 6) | Ne | Ne |
| Laivas | ITMContainerActivityTable.ShipVesselId | Nvarchar(20) | Ne | Ne |
| Pradžios data | ITMContainerActivityTable.StartDate | Datetime | Ne | Ne |

## <a name="tracking-control"></a>Sekimo kontrolė

Sekimo valdymo centras įgalina nurodyto šaltinio lauko atnaujinimą, jį suaktyvina nurodyto tikslinio lauko atnaujinimas. Jei šaltinio lauko vertė ir paskirties lauko vertė atnaujinamos naudojant konteinerio veiklos objektą, paskirties lauke bus rodoma objekto vertė. Ši veikimo būdas susijęs su sekimo kontrolės įrašais, kurių **gamybos laiko** tipo vertė *Kurti*.

Išlaidų sričių, **·** *·* *kurių* būsenos atnaujinimo kūrimo tipo vertė arba tuščia (tai vartotojo nustatyta vertė), sistema atnaujins reiso būseną arba paskirties lauką pagal sekimo kontrolės konfigūraciją.

## <a name="calculated-fields"></a>Suskaičiuoti laukai

Šių konteinerio veiklos įrašo laukų vertės apskaičiuojamos remiantis kitų laukų vertėmis. Nors šie apskaičiuoti laukai nėra įtraukti į duomenų objektą, jie bus nustatyti, jei laukai, pagal kuriuos pagrįsti skaičiavimai, pateikiami.

- **Numatytos dienos** = **Numatoma pabaigos data** – **pradžios data**
- **Faktinės dienos** = **faktinė pabaigos data** – **pradžios data**
