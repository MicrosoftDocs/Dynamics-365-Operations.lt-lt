---
title: Mažmeninės prekybos operacijų finansinių dimensijų redagavimas
description: Šioje temoje aprašoma, kaip redaguoti mažmeninės prekybos operacijų finansines dimensijas „Microsoft Dynamics 365 Commerce“.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5a5a82adbad16d8fea2ccf60ae0dbfbd2fd9f3c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010180"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>Mažmeninės prekybos operacijų finansinių dimensijų redagavimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip redaguoti mažmeninės prekybos operacijų finansines dimensijas „Microsoft Dynamics 365 Commerce“.

## <a name="edit-financial-dimensions"></a>Finansinių dimensijų redagavimas

Norėdami „Commerce“ būstinėje redaguoti mažmeninės prekybos operacijų finansines dimensijas, atlikite nurodytus veiksmus.

1. Atidarykite puslapį **Finansinių dimensijų konfigūravimas, kad būtų galima integruoti programas**.
1. Pasirinkite aktyvų įrašą **Numatytųjų dimensijų integravimas**.
1. Įsitikinkite, kad „FastTab“ **Finansinės dimensijos** visos dimensijos, kurias norite redaguoti „Excel“ darbalapyje, yra sąraše **Pasirinkta**. Daugiau informacijos žr. skyriuje [Duomenų objektai](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).
1. Atsisiųskite ir atidarykite „Excel“ failą iš puslapio **Išrašai**, puslapio **Mažmeninės prekybos operacijos** arba plytelės **Operacijų tikrinimo klaidos** darbo srityje **Parduotuvės finansai**.
1. Norėdami pakeisti operacijos finansinę dimensiją, pasirinkite **Dizainas**, tada pasirinkite pieštuko simbolį, esantį prie eilutės **Operacijos (patikrinamos)**.
1. Suraskite ir pasirinkite lauką **FinancialDimensionDisplayValue**, pasirinkite „Excel“ darbalapio antraštės dalyje esantį langelį ir pasirinkite **Įtraukti žymą**.
1. Pasirinkite langelį, esantį po langeliu, kurį pasirinkote ankstesniame veiksme, pasirinkite **Įtraukti vertę** ir tada pasirinkite **Atnaujinti**. Finansinės dimensijos įtraukiamos į „Excel“ darbalapį ir jas galima redaguoti bei publikuoti.
1. Norėdami pakeisti operacijų eilučių dimensijas, pasirinkite eilutę **Pardavimo operacijos (patikrinama)**, pasirinkite pieštuko simbolį ir pakartokite 6 ir 7 veiksmus.
1. Norėdami pakeisti mokėjimo eilučių dimensijas, pasirinkite eilutę **Mokėjimo operacijos (patikrinama)**, pasirinkite pieštuko simbolį ir pakartokite 6 ir 7 veiksmus.

## <a name="additional-resources"></a>Papildomi ištekliai

[Atsiskaitymo grynaisiais ir grynųjų pinigų valdymo operacijų redagavimas ir tikrinimas](edit-cash-trans.md)

[Internetinio užsakymo ir asinchroninio kliento užsakymo operacijų redagavimas ir tikrinimas](edit-order-trans.md)

[„Excel“ darbaknygės kūrimas norint redaguoti mažmeninės prekybos operacijas](create-excel-edit.md)

[Laukų įtraukimas į „Excel“ darbaknygę norint redaguoti mažmeninės prekybos operacijas](add-fields-excel.md)
