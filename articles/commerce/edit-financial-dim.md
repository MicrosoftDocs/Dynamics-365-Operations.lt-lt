---
title: Mažmeninės prekybos operacijų finansinių dimensijų redagavimas
description: Šiame straipsnyje aprašoma, kaip redaguoti mažmeninės prekybos operacijų finansines dimensijas „Microsoft Dynamics 365 Commerce“.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
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
ms.openlocfilehash: bcd4bdb29a967130f4ad57a57b67f56a8ea81d89
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848930"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>Mažmeninės prekybos operacijų finansinių dimensijų redagavimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip redaguoti mažmeninės prekybos operacijų finansines dimensijas „Microsoft Dynamics 365 Commerce“.

## <a name="edit-financial-dimensions"></a>Finansinių dimensijų redagavimas

Norėdami „Commerce“ būstinėje redaguoti mažmeninės prekybos operacijų finansines dimensijas, atlikite nurodytus veiksmus.

1. Atidarykite puslapį **Finansinių dimensijų konfigūravimas, kad būtų galima integruoti programas**.
1. Pasirinkite aktyvų įrašą **Numatytųjų dimensijų integravimas**.
1. Įsitikinkite, kad „FastTab“ **Finansinės dimensijos** visos dimensijos, kurias norite redaguoti „Excel“ darbalapyje, yra sąraše **Pasirinkta**. Daugiau informacijos žr. skyriuje [Duomenų objektai](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]