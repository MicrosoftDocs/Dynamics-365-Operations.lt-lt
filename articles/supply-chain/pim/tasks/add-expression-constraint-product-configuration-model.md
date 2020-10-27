---
title: Įtraukti išraiškos apribojimą į produkto konfigūravimo modelį
description: Ši procedūra nurodo, kaip į produkto konfigūracijos modelį galima įtraukti naują apribojimo išraišką.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c43d7f768069c5ef201a2823a9aa626b38220073
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986484"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Įtraukti išraiškos apribojimą į produkto konfigūravimo modelį

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip į produkto konfigūracijos modelį galima įtraukti naują apribojimo išraišką. Jame parodoma, kaip galima įgalioti, kad kampo apsauga turi būti taikoma garsiakalbiui, jei vartotojas pasirinko priekines metalo groteles. Procedūros metu naudojamas aukščiausios klasės garsiakalbio komponentas demonstracinės įmonės USMF.


## <a name="create-an-expression-constraint"></a>Kaip sukurti išraiškos apribojimą
1. Spustelėkite Produkto varianto modelio aprašą.
2. Spustelėkite Produkto konfigūracijos modeliai.
3. Sąraše raskite ir pasirinkite norimą įrašą.
    * Šiame pavyzdyje naudojamas aukščiausios klasės garsiakalbio modelis.  
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Išplėskite skyrių Apribojimai.
6. Spustelėkite Pridėti.
7. Spustelėkite Kurti.
8. Lauke Pavadinimas surinkite reikšmę.

## <a name="enter-expression"></a>Įvesti išraišką
1. Spustelėkite Redaguoti išraišką.
    * Jei atrakinsite vartotojo sąsają užduočių įrašymo metu šiame etape, galite naudoti „IntelliSense“ ir simbolių sąrašą apribojimo išraiškai sukurti.  
2. Lauke „ConstraintBody“ įveskite 'Implies[FrontGrill=="Metal", CornerProtection]'.
    * Šios išraiškos logika nurodo: jei priekyje grotelės yra metalinės, tada turi būti pasirinkta kampo apsaugos pasirinktis.  
3. Spustelėkite Tikrinti.
    * Patikrinimo funkcija patikrina apribojimo išraišką, ar joje nėra sintaksės klaidų.  
4. Spustelėkite Uždaryti.
5. Spustelėkite GERAI.

