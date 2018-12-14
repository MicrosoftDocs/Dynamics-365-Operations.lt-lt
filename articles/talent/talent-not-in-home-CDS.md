---
title: "Tarp „Microsoft Dynamics 365“ programų nėra „Talent“ (CDS1.0)"
description: "Šioje temoje aiškinama, ką daryti, jei klientas nemato programos „Microsoft Dynamics 365 for Talent“ tarp „Microsoft Dynamics 365“ programų."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.contentlocale: lt-lt
ms.lasthandoff: 12/04/2018

---

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a>Tarp „Microsoft Dynamics 365“ programų nėra „Talent“ (CDS1.0)

[!include [banner](includes/banner.md)]

**Problema**

Klientas nemato programos „Microsoft Dynamics 365 for Talent“ tarp „Microsoft Dynamics 365“ programų.

**Skiriamoji geba**

Vartotojas turi būti įtrauktas į „Microsoft PowerApps“ aplinkai skirtą vaidmenį Aplinkos kūrėjas.

1. Administratoriaus vartotojas, turintis „PowerApps“ 2 plano licenciją, turi atidaryti [„PowerApps“ administravimo portalą](https://preview.admin.powerapps.com/).
2. Pasirinkite **Aplinkos**, tada pasirinkite „Talent“ tinkamą aplinką.
3. Skirtuke **Sauga**, pateikiamame skirtuke **Aplinkos vaidmenys**, pasirinkite **Aplinkos kūrėjas**.

    ![Skirtukas Aplinkos vaidmenys](media/environment-roles.png)

4. Skirtuke **Vartotojai** įtraukite vartotoją arba savo organizaciją.

    ![Skirtukas Vartotojai](media/environment-maker.png)

5. Pasirinkite **Įrašyti**.
6. Dabar vartotojas turi prisijungti prie [„Microsoft Dynamics 365“](https://home.dynamics.com/).
7. Pasirinkite **Sinchronizuoti**, kad atnaujintumėte vartotojo programas.

    ![Sinchronizavimo mygtukas](media/get-more.png)

    Baigus sinchronizuoti, „Talent“ bus rodoma pagrindiniame puslapyje.

