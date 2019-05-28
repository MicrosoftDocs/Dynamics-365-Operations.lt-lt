---
title: Įtraukti skaičiavimą į produktų konfigūravimo modelį
description: Ši procedūra nurodo, kaip į produkto konfigūracijos modelį įtraukti naują skaičiavimą.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9754c46010e7bbdb2edef0d6e68162f344bb1257
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570416"
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

