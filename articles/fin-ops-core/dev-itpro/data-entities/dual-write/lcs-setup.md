---
title: Dvigubo rašymo sąranka iš „Lifecycle Services“
description: Šioje temoje paaiškinama, kaip nustatyti dvigubo rašymo ryšį iš „Microsoft Dynamics Lifecycle Services” (LCS).
author: laneswenka
ms.date: 05/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 53e82fbf8cff834c9eb0d14a0597561158b85fa1
ms.sourcegitcommit: 6744cc2971047e3e568100eae338885104c38294
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/20/2022
ms.locfileid: "8783207"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Dvigubo rašymo sąranka iš „Lifecycle Services“

[!include [banner](../../includes/banner.md)]



Šioje temoje paaiškinama, kaip įgalinti dvigubą rašymą iš „Microsoft Dynamics Lifecycle Services” (LCS).

## <a name="prerequisites"></a>Būtinieji komponentai

Klientai turi užbaigti integravimą Power Platform, kaip aprašyta šiose temose:

- Jei dar nenaudosite ir norite Microsoft Power Platform išplėsti savo finansų ir operacijų aplinkas įtraukdami platformos pajėgumus, [Power Platform žr. Integravimas – Įgalinti diegiant aplinką](../../power-platform/enable-power-platform-integration.md#enable-during-deploy).
- Jei jau turite ir aplinkas Dataverse Power Platform, ir norite jas sujungti su finansų ir operacijų aplinka, [Power Platform žr. integravimą – Įgalinti po aplinkos diegimo](../../power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="set-up-dual-write-for-new-or-existing-dataverse-environments"></a>Nustatyti dvigubo rašymo naujam arba esamai aplinkai Dataverse sąlygas

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

8. Užbaigus susiejimą, rodomas hipersaitas. Norėdami prisijungti prie dvigubo rašymo administravimo srities finansų ir operacijų aplinkoje, naudokite saitą. Iš ten galite nustatyti objektų susiejimus.

## <a name="linking-mismatch"></a>Susiejimų neatitikimas

Gali būti, kad jūsų dvigubo rašymo aplinka susieta su egzemplioriumi Dataverse, o LCS nėra nustatyta integruoti Power Platform. Šis susiejimo neatitikimas gali sukelti netikėtą veikimo būdą. Rekomenduojama, kad LCS aplinkos informacija atitiktų tai, prie ko esate prisijungę dvigubo rašymo būdu, kad tą patį ryšį galėtų naudoti verslo įvykiai, virtualios lentelės ir priedai.

Jei jūsų aplinkoje yra susiejimų neatitikimas, LCS rodo perspėjimą, panašią į šį jūsų aplinkos informacijos puslapį: "Microsoft Power Platform " aptiko, kad jūsų aplinka susieta naudojant dvigubo rašymo paskirtį į kitą paskirties vietą, nei nurodyta integravimui; nerekomenduojama."

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform nesutampa integravimo saitas.":::

Jei gaunate šį perspėjimą, bandykite naudoti vieną iš šių sprendimų:

- Jei jūsų LCS Power Platform aplinka niekada nebuvo nustatyta integruoti, galite prisijungti prie egzemplioriaus, Dataverse sukonfigūruoto naudojant dvigubo rašymo procesą, naudodami šiame straipsnyje pateiktas instrukcijas.
- Jei jūsų LCS Power Platform aplinka jau nustatyta integruoti, turite atsieti dvigubo rašymo ir iš naujo prisijungti prie tos, kurią nurodė LCS [naudodamas scenarijų: iš naujo nustatykite arba pakeiskite susiejimą](relink-environments.md#scenario-reset-or-change-linking).

Praeityje buvo galima rankinio palaikymo kvito pasirinktis, bet anksčiau buvo prieš 1 pasirinktį.  "Microsoft" nebepalaiko rankinio perėjimo prašymų per Support bilietų.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
