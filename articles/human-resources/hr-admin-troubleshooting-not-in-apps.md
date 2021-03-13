---
title: „Human Resources“ nėra „Microsoft Dynamics 365“ programose
description: Šiame straipsnyje aiškinama, ką daryti, jei klientas nemato programos „Dynamics 365 Human Resources“ tarp „Microsoft Dynamics 365“ programų.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d78199cf0e76ffd0676a26961a8e646938dc7333
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113601"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>„Human Resources“ nėra „Microsoft Dynamics 365“ programose

**Išduoti**

Klientas nematys „Dynamics 365 Human Resources“ tarp „Microsoft Dynamics 365“ programų.

**Nutarimas**

Vartotojas turi būti įtrauktas į „Microsoft Power Apps“ aplinkai skirtą vaidmenį Aplinkos kūrėjas.

1. Vartotojas administratorius, turintis „Power Apps“ 2 plano licenciją, turi atidaryti [„Power Apps“ administravimo portalą](https://preview.admin.powerapps.com/).

2. Pasirinkite **Aplinkos**, tada pasirinkite „Human Resources“ tinkamą aplinką.

3. Skirtuke **Sauga**, pateikiamame skirtuke **Aplinkos vaidmenys**, pasirinkite **Aplinkos kūrėjas**.

    ![Skirtukas Aplinkos vaidmenys](media/environment-roles.png)

4. Skirtuke **Vartotojai** įtraukite vartotoją arba savo organizaciją.

    ![Skirtukas Vartotojai](media/environment-maker.png)

5. Pasirinkite **Įrašyti**.

6. Dabar vartotojas turi prisijungti prie [Microsoft Dynamics 365](https://home.dynamics.com/).

7. Pasirinkite **Sinchronizuoti**, kad atnaujintumėte vartotojo programas.

    ![Sinchronizavimo mygtukas](media/get-more.png)

    Baigus sinchronizuoti, „Human Resources“ bus rodoma pagrindiniame puslapyje.
