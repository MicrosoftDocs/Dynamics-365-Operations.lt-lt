--- 
title: "Įtraukti skaičiavimą į produktų konfigūravimo modelį"
description: "Ši procedūra nurodo, kaip į produkto konfigūracijos modelį įtraukti naują skaičiavimą."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 9ac2d9bcc316a57941136c248a0c5ff030a1fe49
ms.contentlocale: lt-lt
ms.lasthandoff: 07/28/2017

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Įtraukti skaičiavimą į produktų konfigūravimo modelį

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra nurodo, kaip į produkto konfigūracijos modelį įtraukti naują skaičiavimą. Joje rodoma, kaip sukurti loginę išraišką naudojant „If“ operatorių, norint nustatyti baltų garsiakalbių aukštį į 10, o visų likusių – 15. Procedūros metu naudojamas aukščiausios klasės garsiakalbio komponentas demonstracinės įmonės USMF.


## <a name="add-a-calculation"></a>Įtraukti skaičiavimą

## <a name="create-calculation-expression"></a>Kurti skaičiavimo išraišką
1. Spustelėkite Redaguoti išraišką.
2. Lauke „ConstraintBody“ įveskite 'If[CabinetFinish=="White", 10, 15]'.
3. Spustelėkite Tikrinti.
4. Spustelėkite Uždaryti.
5. Spustelėkite GERAI.


