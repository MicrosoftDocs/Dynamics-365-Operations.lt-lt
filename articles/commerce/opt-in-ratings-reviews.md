---
title: Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite
description: Šiame straipsnyje paaiškinama, kaip pasirinkti naudoti savo svetainės vertinimus ir apžvalgas Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 00fd30ded916cc6b587ceff67728e7d964714716
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269168"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite

[!include [banner](includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip pasirinkti naudoti savo svetainės vertinimus ir apžvalgas Microsoft Dynamics 365 Commerce.

Įvertinimų ir apžvalgų sprendimas yra daugiakanalis sprendimas, kurį galite padaryti pasiekiamą „Dynamics 365 Commerce“, naudojant „Microsoft Dynamics Lifecycle Services“ (LCS). LCS yra administravimo portalas, kurį prekybininkai naudoja valdyti savo aplinką nuo jos parengimo iki jos eksploatacijos nutraukimo.

Jei norite naudoti įvertinimų ir apžvalgų sprendimą savo „Commerce“ svetainėje, turite pasirinkti įvertinimus ir apžvalgas diegiant savo „e-Commerce“ svetainę „Dynamics 365 Commerce“.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite

Norėdami sutikti naudoti įvertinimus ir apžvalgas savo svetainėje, atlikite šiuos veiksmus.

1. Vykdykite veiksmus, nurodytus temoje [Naujos el. prekybos svetainės diegimas](deploy-ecommerce-site.md).
1. Kol jūs vis dar esate LCS portale, eikite į **„Retail“ diegimo sąranka \> Kiti parametrai**.
1. Parinktį **Įjungti įvertinimų ir apžvalgų paslaugą** nustatykite kaip **Taip**.
1. **AAD saugos grupėje, skirtaje įvertinimui ir peržiūrų moderatoriaus** laukui, įveskite "Microsoft Azure Active Directory " (Azure AD) saugos grupės, kurioje yra vertinimai ir peržiūros moderatoriai, ID.

    ![Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite.](media/LCS_RnR_Preference_2.png)

1. Baikite el. prekybos inicijavimo procesą.

> [!NOTE] 
> Jei jau esate „Dynamics 365 Commerce“ klientas, įdiegėte „e-Commerce“ svetainę, bet nepasirinkote įvertinimų ir apžvalgų, o norite naudoti paketo „Dynamics 365 Commerce“ įvertinimus ir apžvalgas, pateikite aptarnavimo užklausą. Norėdami gauti informacijos apie tai, kaip pateikti aptarnavimo užklausą, žr. [Pateikti aptarnavimo užklausų procesą](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Papildomi ištekliai

[Įvertinimų ir atsiliepimų apžvalga](ratings-reviews-overview.md)

[Įvertinimų ir atsiliepimų tvarkymas](manage-reviews.md)

[Įvertinimų ir atsiliepimų konfigūravimas](configure-ratings-reviews.md)

[Produktų įvertinimų sinchronizavimas sprendime „Dynamics 365 Commerce“](sync-product-ratings.md)

[Neautomatinio vadovo įvertinimų ir atsiliepimų publikavimo įjungimas](manual-publish-rating-reviews.md)

[Įvertinimų ir atsiliepimų importavimas ir eksportavimas](import-export-reviews.md)

[Ryšių tarp tarnybų autentifikavimo konfigūravimas](service-to-service-auth.md)

[DUK apie įvertinimus ir apžvalgas](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
