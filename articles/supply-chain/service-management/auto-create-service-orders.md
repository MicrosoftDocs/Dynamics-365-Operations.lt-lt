---
title: Automatinis aptarnavimo užsakymų kūrimas
description: Galite generuoti aptarnavimo užsakymus, pagrįstus aptarnavimo sutartimi, skirta galiojančiam aptarnavimo sutarties laikotarpiui.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08fb7363ab87fd6a7f3d38406e72b1f542dc2c2a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433772"
---
# <a name="automatically-create-service-orders"></a>Automatinis aptarnavimo užsakymų kūrimas 

[!include [banner](../includes/banner.md)]


Galite generuoti aptarnavimo užsakymus, pagrįstus aptarnavimo sutartimi, skirta galiojančiam aptarnavimo sutarties laikotarpiui.

Aptarnavimo užsakymai, kurie generuojami iš aptarnavimo sutarties, pridedami prie tos aptarnavimo sutarties.

Aptarnavimo užsakymai generuojami automatiškai, naudojant šiuos parametrus:

  - Aptarnavimo sutarties intervalas, kuris nustatytas aptarnavimo sutarties eilutėse. Aptarnavimo sutarties intervalas rodo dažnumą, kuriuo sukuriamos aptarnavimo užsakymo eilutės. Daugiau informacijos žr. [Aptarnavimo intervalai](service-intervals.md).

  - Laikotarpis, nustatomas apibrėžti aptarnavimo laikotarpį laukuose **Pradžios data** ir **Pabaigos data**, esančiuose formoje **Kurti aptarnavimo užsakymus**. Daugiau informacijos žr. [Automatiškai kurti aptarnavimo užsakymus](create-service-orders-automatically.md).

  - Parinktis **Jungti aptarnavimo užsakymus** aptarnavimo sutarties antraštėje. Ši parinktis apibrėžia, ar aptarnavimo užsakymo eilutės, sugeneruotos iš aptarnavimo sutarties, sujungia aptarnavimo užsakymus pagal darbuotoją, aptarnavimo užduotį, aptarnavimo objektą arba aptarnavimo sutartį. Daugiau informacijos žr. [Jungti aptarnavimo užsakymus](combine-service-orders.md).

  - Parinktis **Laiko langas** aptarnavimo sutarties eilutėje. Laiko langas apibrėžia, kiek aptarnavimo užsakymo eilutė gali būti perkelta, atsižvelgiant į jos apskaičiuotą datą. Daugiau informacijos žr. [Laiko langai](time-windows.md).


> [!NOTE]
> <P>Jeigu aptarnavimo užsakymui nurodyta diena neatidaryta kalendoriuje, kurį pasirinkote formoje <STRONG>Aptarnavimo valdymo parametrai</STRONG>, gausite pranešimą, kad yra kalendoriaus konfliktas. Galima saugiai nepaisyti pranešimo; aptarnavimo užsakymas bus sukurtas net jei diena kalendoriuje uždaryta.</P>

## <a name="example-1"></a>1 pavyzdys

Aptarnavimo sutartis galioja nuo 2012 m. sausio 1 d. iki 2012 m. gruodžio 31 d. Jei aptarnavimo laikotarpis, kurį nurodėte formoje **Kurti aptarnavimo užsakymus** yra nuo 2012 m. lapkričio 1 d. iki 2013 m. vasario 1 d., aptarnavimo užsakymai kuriami nuo 2012 m. lapkričio 1 d. iki 2012 iki 2012 m. gruodžio 31 d.

## <a name="example-2"></a>2 pavyzdys

Aptarnavimo sutartis galioja nuo 2012 m. sausio 1 d. iki 2012 m. gruodžio 31 d. Dvi aptarnavimo sutarties eilutės pridėtos prie aptarnavimo sutarties. Pirmosios aptarnavimo sutarties eilutės pradžios data yra 2012 m. sausio 2 d., o pabaigos data yra 2012 m. kovo 1 d. Antrosios aptarnavimo sutarties eilutės pradžios data yra 2012 m. balandžio 1 d., o pabaigos data yra 2012 m. gruodžio 31 d. Formoje **Kurti aptarnavimo užsakymus** galite nurodyti laikotarpį nuo 2012 m. spalio 1 d. iki 2012 m. gruodžio 31 d. Todėl aptarnavimo užsakymai generuojami tik antrai sutarties eilutei, nes pirmos sutarties eilutės pradžios data ir pabaigos data yra ankstesnės nei aptarnavimo užsakyme nurodytas laikotarpis.

  


