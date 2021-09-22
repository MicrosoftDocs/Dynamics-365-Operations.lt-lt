---
title: Apdorojant perkėlimą atsargų savininkas neleidžiamas
description: Galite gauti klaidą, „Atsargų savininkas %1neleidžiamas". Šiuo metu „Warehouse management“ procesas palaiko tik inventorių, kurį valdo juridinis asmuo.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4ee29cfc7bad990cd1ee5deaa98fca217af772ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477068"
---
# <a name="inventory-owner-not-allowed-when-processing-movements-in-the-warehouse-app"></a>Apdorojant perkėlimą atsargų savininkas neleidžiamas sandėlio programoje

## <a name="symptoms"></a>Požymiai

Apdorojus perkėlimą „Warehouse management“ mobilioje programoje, gali būti rodomas šis klaidos pranešimas:

> Šio proceso metu %1 atsargų savininkas neleidžiamas.

## <a name="cause"></a>Priežastis

Tai nutinka, nes **Savininkas**, kai „Warehouse management“ mobiliųjų įrenginių programėlė naudojama perkėlimams atlikti. Įprastas inventoriaus perkelimo žurnalas iš „Supply Chain Management“ kliente ima dirbti kaip numatyta ir gali būti publikuotas tik jei **Savininko** dimensija užpildyta.

## <a name="resolution"></a>Sprendimas

„Microsoft“ įvertino šią klaidą ir nustatė jos funkcijos apribojimą. Šiuo metu sandėlio valdymo procesas palaiko tik inventorių, kurį valdo juridinis asmuo.
