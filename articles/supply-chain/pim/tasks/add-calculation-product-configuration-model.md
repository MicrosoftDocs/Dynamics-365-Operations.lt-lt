---
title: Įtraukti skaičiavimą į produktų konfigūravimo modelį
description: Ši procedūra nurodo, kaip į produkto konfigūracijos modelį įtraukti naują skaičiavimą.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32bc2ac5815c2739147664f1e1df2528178db51e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213405"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Įtraukti skaičiavimą į produktų konfigūravimo modelį

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip į produkto konfigūracijos modelį įtraukti naują skaičiavimą. Joje rodoma, kaip sukurti loginę išraišką naudojant „If“ operatorių, norint nustatyti baltų garsiakalbių aukštį į 10, o visų likusių – 15. Procedūros metu naudojamas aukščiausios klasės garsiakalbio komponentas demonstracinės įmonės USMF.


## <a name="add-a-calculation"></a>Įtraukti skaičiavimą

## <a name="create-calculation-expression"></a>Kurti skaičiavimo išraišką
1. Spustelėkite Redaguoti išraišką.
2. Lauke „ConstraintBody“ įveskite 'If[CabinetFinish=="White", 10, 15]'.
3. Spustelėkite Tikrinti.
4. Spustelėkite Uždaryti.
5. Spustelėkite GERAI.

