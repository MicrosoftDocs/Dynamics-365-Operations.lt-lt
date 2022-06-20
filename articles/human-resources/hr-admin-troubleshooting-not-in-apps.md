---
title: „Human Resources“ nėra „Microsoft Dynamics 365“ programose
description: Šiame straipsnyje paaiškinama, ką daryti, jei "Microsoft Dynamics 365 Human Resources " nėra įtraukta į sąrašą iš Microsoft Dynamics 365 programėlių.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2d520ac06bcc0990714929c0fdd622516eda5f30
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872245"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>„Human Resources“ progrmaos nėra „Microsoft Dynamics 365“ programose


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Problema**

Klientas nematys „Dynamics 365 Human Resources“ tarp „Microsoft Dynamics 365“ programų.

**Nutarimas**

Vartotojas turi būti įtrauktas į „Microsoft Power Apps“ aplinkai skirtą vaidmenį Aplinkos kūrėjas.

1. Vartotojas administratorius, turintis „Power Apps“ 2 plano licenciją, turi atidaryti [„Power Apps“ administravimo portalą](https://preview.admin.powerapps.com/).

2. Pasirinkite **Aplinkos**, tada pasirinkite „Human Resources“ tinkamą aplinką.

3. Skirtuke **Sauga**, pateikiamame skirtuke **Aplinkos vaidmenys**, pasirinkite **Aplinkos kūrėjas**.

    ![Skirtukas Aplinkos vaidmenys.](media/environment-roles.png)

4. Skirtuke **Vartotojai** įtraukite vartotoją arba savo organizaciją.

    ![Skirtukas Vartotojai.](media/environment-maker.png)

5. Pasirinkite **Įrašyti**.

6. Dabar vartotojas turi prisijungti prie [Microsoft Dynamics 365](https://home.dynamics.com/).

7. Pasirinkite **Sinchronizuoti**, kad atnaujintumėte vartotojo programas.

    ![Sinchronizavimo mygtukas.](media/get-more.png)

    Baigus sinchronizuoti, „Human Resources“ bus rodoma pagrindiniame puslapyje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
