--- 
title: "Įtraukti išraiškos apribojimą į produkto konfigūravimo modelį"
description: "Ši procedūra nurodo, kaip į produkto konfigūracijos modelį galima įtraukti naują apribojimo išraišką."
author: ShylaThompson
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8db46c5b8361c96745b440c0d0684e18c06a6c6f
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Įtraukti išraiškos apribojimą į produkto konfigūravimo modelį

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


