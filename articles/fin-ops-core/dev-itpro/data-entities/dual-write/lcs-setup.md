---
title: Dvigubo rašymo sąranka iš „Lifecycle Services“
description: Šioje temoje paaiškinama, kaip nustatyti dvigubo rašymo ryšį iš „Microsoft Dynamics Lifecycle Services” (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103574"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Dvigubo rašymo sąranka iš „Lifecycle Services“

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje paaiškinama, kaip įgalinti dvigubą rašymą iš „Microsoft Dynamics Lifecycle Services” (LCS).

## <a name="prerequisites"></a>Būtinieji komponentai

Turite užbaigti „Power Platform” integravimą, kaip aprašyta šiose temose:

+ [„Power Platform” Integravimas – Įgalinti aplinkos diegimo metu](../../power-platform/overview.md#enable-during-environment-deployment)
+ [„Power Platform” integravimas – Nustatyti po aplinkos diegimo](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>Dvigubo rašymo nustatymas naujoms „Dataverse” aplinkoms

Norėdami nustatyti dvigubą rašymą iš LCS **Aplinkos informacijos** puslapio, atlikite šiuos veiksmus:

1. Puslapyje **Aplinkos informacija** išplėskite skyrių **„Power Platform” Integravimas**.

2. Pasirinkite **Dvigubo rašymo programos** mygtuką.

    ![„Power Platform“ integravimas](media/powerplat_integration_step2.png)

3. Peržiūrėkite sąlygas ir nuostatas, o tada pasirinkite **Konfigūruoti**.

4. Norėdami tęsti pasirinkite **GERAI**.

5. Eigą galite stebėti periodiškai atnaujindami aplinkos informacijos puslapį. Įprastai nustatymas trunka ne daugiau kaip 30 minučių.  

6. Užbaigę nustatymą, gausite pranešimą, ar procesas buvo sėkmingas. Jei nustatymas nepavyko, rodomas susijęs klaidos pranešimas. Prieš pereidami prie kito veiksmo, turite ištaisyti klaidas, jei jų yra.

7. Pasirinkite **Saitas į „Power Platform” aplinką**, kad sukurtumėte saitą tarp „Dataverse” ir dabartinės aplinkos duomenų bazių. Įprastai tai trunka mažiau nei 5 minutes.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Saitas į Power Platform aplinką":::

8. Užbaigus susiejimą, rodomas hipersaitas. Naudokite saitą, kad prisiregistruotumėte prie dvigubo rašymo administravimo srities „Finance and Operations” aplinkoje. Iš ten galite nustatyti objektų susiejimus.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Dvigubo rašymo nustatymas esamai „Dataverse” aplinkai

Norėdami nustatyti dvigubą rašymą esamai „Dataverse” aplinkai, turite sukurti „Microsoft” [palaikymo kvitą](../../lifecycle-services/lcs-support.md). Į kvitą turi būti įtraukta:

+ Jūsų „Finance and Operations” aplinkos ID.
+ Jūsų aplinkos pavadinimas iš „Lifecycle Services”.
+ „Dataverse” organizacijos ID arba „Power Platform” aplinkos ID iš „Power Platform” administravimo centro. Savo kvite pateikite užklausą, kad ID būtų egzempliorius, naudotas „Power Platform” integravimui.

> [!NOTE]
> Negalite atsieti aplinkos naudodami LCS. Norėdami atsieti aplinką, aplinkoje Finance and Operations atidarykite darbo sritį **Duomenų integravimas** ir pasirinkite **Atsieti**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
