---
title: Aptarnavimo lygis ir aprašas
description: Šiame straipsnyje paaiškinamas turto valdymo paslaugų lygis ir aprašymas.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 753ad36b1d01d1ce0594f477cf863ca0e4a1ac75
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879198"
---
# <a name="service-level-and-description"></a>Aptarnavimo lygis ir aprašas

[!include [banner](../../includes/banner.md)]

 

Sukūrę darbo užsakymą galbūt norėsite nustatyti darbo užsakymo aptarnavimo lygius ir į jį įtraukti bendrą aprašą. Darbo užsakymo aptarnavimo lygius galite kurti puslapyje **Darbo užsakymo aptarnavimo lygiai**, o aprašus – puslapyje **Darbo užsakymo aprašas**.

## <a name="create-a-service-level"></a>Aptarnavimo lygio kūrimas

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Aptarnavimo lygis**.
2. Pasirinkite **Naujas**.
3. Lauke **Aptarnavimo lygis** įveskite aptarnavimo lygį (pvz., skaičių).
4. Tada lauke **Pavadinimas** įveskite pavadinimą.

    „FastTab“ **Darbo užsakymai** galite nustatyti numatomas pradžios ir pabaigos datas ir laiką. Šio „FastTab“ laukai nustato laikotarpį, kuriuo darbo užsakymai turėtų būti pradėti ir užbaigti. Jie naudojami rankiniu būdu sukurtuose darbo užsakymuose ir darbo užsakymuose, kurie kuriami pagal priežiūros užklausas. 

5. Lauke **Pradžios diena** įveskite dienų skaičių, kad nustatytumėte laikotarpį, kuriuo turėtų prasidėti darbo užsakymas. Dienų skaičius skaičiuojamas nuo darbo užsakymo sukūrimo datos. Pavyzdžiui, jei darbo užsakymas turėtų būti pradėtas jį sukūrus, įveskite **0**. Jei darbo užsakymas turėtų būti pradėtas per vieną savaitę nuo jo sukūrimo, įveskite **7**.
6. Jei be darbo užsakymo pradžios datos norite nustatyti jo pradžios laiką, nustatykite parinkties **Nustatyti pradžios laiką** nuostatą **Taip**. Tada lauke **Pradžios laikas** įveskite pradžios laiką. Jei nustatysite parinkties nuostatą **Ne**, bus naudojamas dabartinis dienos laikas.
7. Lauke **Pabaigos diena** įveskite dienų skaičių, kad nustatytumėte laikotarpį, kuriuo turėtų pasibaigti darbo užsakymas. Dienų skaičius skaičiuojamas nuo darbo užsakymo pradžios datos. Pavyzdžiui, jei darbo užsakymas turėtų būti užbaigtas per vieną savaitę nuo jo pradžios datos, įveskite **7**.
8. Jei be darbo užsakymo pabaigos datos norite nustatyti jo pabaigos laiką, nustatykite parinkties **Nustatyti pabaigos laiką** nuostatą **Taip**. Tada lauke **Pabaigos laikas** įveskite pabaigos laiką. Jei nustatysite parinkties nuostatą **Ne**, bus naudojamas dabartinis dienos laikas.
9. Pasirinkite **Įrašyti**.

![Darbo užsakymų paslaugos lygio puslapis.](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a>Aprašo kūrimas

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Aprašai**.
2. Pasirinkite **Naujas**.
3. Lauke **Aprašas** įveskite aprašą.
4. Pasirinkite **Įrašyti**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]