---
title: Dvigubo rašymo sąranka iš „Lifecycle Services“
description: Šioje temoje paaiškinama, kaip nustatyti dvigubo rašymo ryšį iš „Microsoft Dynamics Lifecycle Services” (LCS).
author: laneswenka
ms.date: 08/03/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 9f461837c65c30eace3358c231618aedf428f487
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675302"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Dvigubo rašymo sąranka iš „Lifecycle Services“

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje paaiškinama, kaip įgalinti dvigubą rašymą iš „Microsoft Dynamics Lifecycle Services” (LCS).

## <a name="prerequisites"></a>Būtinieji komponentai

Turite užbaigti „Power Platform” integravimą, kaip aprašyta šiose temose:

+ [„Power Platform” Integravimas – Įgalinti aplinkos diegimo metu](../../power-platform/enable-power-platform-integration.md#enable-during-deploy)
+ [„Power Platform” Integravimas – Įgalinti po aplinkos diegimo](../../power-platform/enable-power-platform-integration.md#enable-after-deploy)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>Dvigubo rašymo nustatymas naujoms „Dataverse” aplinkoms

Norėdami nustatyti dvigubą rašymą iš LCS **Aplinkos informacijos** puslapio, atlikite šiuos veiksmus:

1. Puslapyje **Aplinkos informacija** išplėskite skyrių **„Power Platform” Integravimas**.

2. Pasirinkite **Dvigubo rašymo programos** mygtuką.

    ![„Power Platform“ Integravimas.](media/powerplat_integration_step2.png)

3. Peržiūrėkite sąlygas ir nuostatas, o tada pasirinkite **Konfigūruoti**.

4. Norėdami tęsti pasirinkite **GERAI**.

5. Eigą galite stebėti periodiškai atnaujindami aplinkos informacijos puslapį. Įprastai nustatymas trunka ne daugiau kaip 30 minučių.  

6. Užbaigę nustatymą, gausite pranešimą, ar procesas buvo sėkmingas. Jei nustatymas nepavyko, rodomas susijęs klaidos pranešimas. Prieš pereidami prie kito veiksmo, turite ištaisyti klaidas, jei jų yra.

7. Pasirinkite **Saitas į „Power Platform” aplinką**, kad sukurtumėte saitą tarp „Dataverse” ir dabartinės aplinkos duomenų bazių. Įprastai tai trunka mažiau nei 5 minutes.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Saitas į Power Platform aplinką.":::

8. Užbaigus susiejimą, rodomas hipersaitas. Naudokite saitą, kad prisiregistruotumėte prie dvigubo rašymo administravimo srities „Finance and Operations” aplinkoje. Iš ten galite nustatyti objektų susiejimus.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Dvigubo rašymo nustatymas esamai „Dataverse” aplinkai

Norėdami nustatyti dvigubą rašymą esamai „Dataverse” aplinkai, turite sukurti „Microsoft” [palaikymo kvitą](../../lifecycle-services/lcs-support.md). Į kvitą turi būti įtraukta:

+ Jūsų „Finance and Operations” aplinkos ID.
+ Jūsų aplinkos pavadinimas iš „Lifecycle Services”.
+ „Dataverse” organizacijos ID arba „Power Platform” aplinkos ID iš „Power Platform” administravimo centro. Savo kvite pateikite užklausą, kad ID būtų egzempliorius, naudotas „Power Platform” integravimui.

> [!NOTE]
> Negalite atsieti aplinkos naudodami LCS. Norėdami atsieti aplinką, aplinkoje Finance and Operations atidarykite darbo sritį **Duomenų integravimas** ir pasirinkite **Atsieti**.

## <a name="linking-mismatch"></a>Susiejimų neatitikimas

Gali būti, kad jūsų LCS aplinka susieta su vienu „Dataverse“ egzemplioriumi, o jūsų dvigubo rašymo aplinka susieta su kitu „Dataverse“ egzemplioriumi. Šis susiejimo neatitikimas gali sukelti netikėtą veikimo būdą ir gali baigtis duomenų siuntimą į netinkamą aplinką. Dvigubo rašymo atveju rekomenduojama aplinka yra ta, kuri sukurta kaip integravimo dalis, ir ilgalaikio, tai bus vienintelis būdas nustatyti ryšį „Power Platform“ tarp aplinkos.

Jei jūsų aplinkoje yra susiejimų neatitikimas, LCS rodo įspėjimą jūsų aplinkos informacijos puslapyje, panašią į „Microsoft" aptiko, kad jūsų aplinka susieta su dvigubo rašymo vieta į kitą paskirties vietą, nei nurodyta integravimą; tai „Power Platform“ nerekomenduojama":

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform nesutampa integravimo saitas.":::

Aptinkant šią klaidą yra dvi pasirinktys, paremtos jūsų poreikiais:

+ [Atsiekite ir atsiekite dvigubo rašymo aplinkas (iš naujo nustatykite arba keiskite susiejimą), kaip nurodyta](relink-environments.md#scenario-reset-or-change-linking) LCS aplinkos informacijos puslapyje. Tai geriausia pasirinktis, kadangi galite ją vykdyti be „Microsoft“ palaikymo.  
+ Jei norite išsaugoti savo saitą dvigubo rašymo metu, galite paprašyti pagalbos iš „Microsoft" palaikymo, kad pakeist būtų galima pakeisti integravimą, kad jūsų esama aplinka būtų naudojama kaip „Power Platform“ ir „Dataverse“ dokumentuota ankstesniame skyriuje.  

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
