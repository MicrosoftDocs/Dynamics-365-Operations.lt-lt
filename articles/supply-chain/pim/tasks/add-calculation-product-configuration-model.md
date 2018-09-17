--- 
title: "Įtraukti skaičiavimą į produktų konfigūravimo modelį"
description: "Ši procedūra nurodo, kaip į produkto konfigūracijos modelį įtraukti naują skaičiavimą."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2db8fb922b085a7f118822ef4fd974ac338f4d99
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Įtraukti skaičiavimą į produktų konfigūravimo modelį

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra nurodo, kaip į produkto konfigūracijos modelį įtraukti naują skaičiavimą. Joje rodoma, kaip sukurti loginę išraišką naudojant „If“ operatorių, norint nustatyti baltų garsiakalbių aukštį į 10, o visų likusių – 15. Procedūros metu naudojamas aukščiausios klasės garsiakalbio komponentas demonstracinės įmonės USMF.


## <a name="add-a-calculation"></a>Įtraukti skaičiavimą

## <a name="create-calculation-expression"></a>Kurti skaičiavimo išraišką
1. Spustelėkite Redaguoti išraišką.
2. Lauke „ConstraintBody“ įveskite 'If[CabinetFinish=="White", 10, 15]'.
3. Spustelėkite Tikrinti.
4. Spustelėkite Uždaryti.
5. Spustelėkite GERAI.


