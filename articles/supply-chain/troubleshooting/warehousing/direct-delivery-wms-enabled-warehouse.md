---
title: WMS įgalinto sandėlio tiesioginio pristatymo apdoroti nepavyko
description: Jei sandėlyje yra įgalinta WMS, jis nepalaiko tiesioginio pristatymo. Dėl to, norėdami naudoti tiesioginį pristatymą, turite pasirinkti ne WMS prekę ir sandėlį.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 090e17091e9fb92c2065679bb9b04637214e2eea
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477144"
---
# <a name="direct-delivery-not-able-to-process-for-wms-enabled-warehouse"></a>WMS įgalinto sandėlio tiesioginio pristatymo apdoroti negalima

## <a name="symptoms"></a>Požymiai

Jei prekė įtraukiama į tiesioginio pristatymo iš sandėlio, kuriame įgalintas „warehouse management“ (WMS), pardavimo eilutę, gaunate tokį klaidos pranešimą:

> Gaunu tolesnį klaidos pranešimą: „Tiesioginis pristatymas negali apdoroti sandėlio 1%, nes jam įjungtas „warehouse management“. Prašome nurodyti kitą sandėlį, kuris nėra įjungtas „warehouse management".

## <a name="resolution"></a>Sprendimas

„Microsoft“ įvertino šią klaidą ir nustatė jos funkcijos apribojimą. Šiuo metu, WMS nepalaiko tiesioginio pristatymo. Dėl to, norėdami naudoti tiesioginį pristatymą, turite pasirinkti ne WMS prekę ir sandėlį.
