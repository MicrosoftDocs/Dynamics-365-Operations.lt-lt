---
title: KS versijos išskleidimas
description: Šiame straipsnyje paaiškinamas bendrojo planavimo scenarijus, apimantis KS versijos išskleidimą.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be4dfc85ad7ab01df9a95a394896873e2d649e12
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575104"
---
# <a name="explosion-of-a-bom-version"></a>KS versijos išskleidimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinamas bendrojo planavimo scenarijus, apimantis KS versijos išskleidimą.

Komplektavimo specifikacijos (KS) versijos poreikio išskleidimas sukuria kiekvienos KS eilutės poreikį tam tikroje teritorijoje ir, galbūt, tam tikrame sandėlyje. Teritorijai būdingoje KS galima nustatyti konkretų kiekvienos KS eilutės sandėlį. Taip pat kiekvienos KS eilutės prekės dimensijos parametrai nurodo, ar sandėlis būtinas. Gautas kiekvienos KS eilutės prekės poreikis savo ruožtu tampa papildomo poreikio išskleidimo pradžios tašku. Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.

-   Teritorijos dimensija yra privaloma ir turi būti įvesta poreikio operacijoje.
-   Teritorijos dimensija yra nuosekli. Todėl teritorija žemesnio lygio poreikiui yra ta pati, kaip pradinio poreikio operacijos teritorija.

Tolesniame paveikslėlyje parodyta, kaip vyksta bendrojo planavimo poreikio išskleidimas. ![Poreikio išplėtimas naudojantis KS versija.](./media/multisitedemandexplosionscenariousingbomversion.gif)

## <a name="additional-resources"></a>Papildomi ištekliai

[KS versijos nustatymas](master-plan-bom-version-determined.md)

[Bendrojo planavimo ir kelių teritorijų funkcijos apžvalga](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]