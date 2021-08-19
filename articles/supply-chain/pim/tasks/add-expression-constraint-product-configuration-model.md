---
title: Įtraukti išraiškos apribojimą į produkto konfigūravimo modelį
description: Ši procedūra nurodo, kaip į produkto konfigūracijos modelį galima įtraukti naują apribojimo išraišką.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 859c25fd361063d4c5a8544c4b488adfab4238e6cc079fa96efe1c71777779e9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730327"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Įtraukti išraiškos apribojimą į produkto konfigūravimo modelį

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip į produkto konfigūracijos modelį galima įtraukti naują apribojimo išraišką. Jame parodoma, kaip galima įgalioti, kad kampo apsauga turi būti taikoma garsiakalbiui, jei vartotojas pasirinko priekines metalo groteles. Procedūros metu naudojamas aukščiausios klasės garsiakalbio komponentas demonstracinės įmonės USMF.

## <a name="create-an-expression-constraint"></a>Kaip sukurti išraiškos apribojimą

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Produkto konfigūracijos modeliai**.
3. Sąraše raskite ir pasirinkite norimą įrašą.
    * Šiame pavyzdyje naudojamas aukščiausios klasės garsiakalbio modelis.  
4. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.
5. Išplėskite **skyrių** Apribojimai.
6. Pasirinkite **Įtraukti**.
7. Pasirinkite **Kurti**.
8. Lauke **Pavadinimas** įveskite reikšmę.

## <a name="enter-expression"></a>Įvesti išraišką

1. Pasirinkite **Redaguoti išraišką**.
    * Jei atrakinsite vartotojo sąsają užduočių įrašymo metu šiame etape, galite naudoti „IntelliSense“ ir simbolių sąrašą apribojimo išraiškai sukurti.  
2. Lauke **„ConstraintBody“** įveskite, 'Implies[FrontGrill=="Metal", CornerProtection] '.
    * Šios išraiškos logika nurodo: jei priekyje grotelės yra metalinės, tada turi būti pasirinkta kampo apsaugos pasirinktis.  
3. Pasirinkite **Tikrinti**.
    * Patikrinimo funkcija patikrina apribojimo išraišką, ar joje nėra sintaksės klaidų.  
4. Pasirinkite **Uždaryti**.
5. Pasirinkite **Gerai**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]