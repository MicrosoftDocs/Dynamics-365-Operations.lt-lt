---
title: „Human Resources“ nėra „Microsoft Dynamics 365“ programose
description: Šiame straipsnyje aiškinama, ką daryti, jei klientas nemato programos „Dynamics 365 Human Resources“ tarp „Microsoft Dynamics 365“ programų.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: d39e6ef4168f08f20b92979a296ed088744ad0da
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010012"
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
