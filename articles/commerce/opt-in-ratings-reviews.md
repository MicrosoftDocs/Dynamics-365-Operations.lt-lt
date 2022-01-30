---
title: Prisijunkite, norėdami naudoti įvertinimus ir atsiliepimus
description: Šioje temoje paaiškinama, kaip sutikti naudoti įvertinimus ir apžvalgas savo „Microsoft Dynamics 365 Commerce“ svetainėje.
author: gvrmohanreddy
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fd6715539693389f25800a40c0beffcdc1b0de72
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968008"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip sutikti naudoti įvertinimus ir apžvalgas savo „Microsoft Dynamics 365 Commerce“ svetainėje.

Įvertinimų ir apžvalgų sprendimas yra daugiakanalis sprendimas, kurį galite padaryti pasiekiamą „Dynamics 365 Commerce“, naudojant „Microsoft Dynamics Lifecycle Services“ (LCS). LCS yra administravimo portalas, kurį prekybininkai naudoja valdyti savo aplinką nuo jos parengimo iki jos eksploatacijos nutraukimo.

Jei norite naudoti įvertinimų ir apžvalgų sprendimą savo „Commerce“ svetainėje, turite pasirinkti įvertinimus ir apžvalgas diegiant savo „e-Commerce“ svetainę „Dynamics 365 Commerce“.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite

Norėdami sutikti naudoti įvertinimus ir apžvalgas savo svetainėje, atlikite šiuos veiksmus.

1. Vykdykite veiksmus, nurodytus temoje [Naujos el. prekybos svetainės diegimas](deploy-ecommerce-site.md).
1. Kol jūs vis dar esate LCS portale, eikite į **„Retail“ diegimo sąranka \> Kiti parametrai**.
1. Parinktį **Įjungti įvertinimų ir apžvalgų paslaugą** nustatykite kaip **Taip**.
1. Lauke **AAD saugos grupė, skirta įvertinimų ir apžvalgų moderatoriui (saugos grupės objekto ID)**, įveskite „Microsoft Azure Active Directory“ („Azure AD“) saugos grupės, apimančios įvertinimų ir atsiliepimų moderatorių vaidmenį, ID.

    ![Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite.](media/LCS_RnR_Preference.png)

1. Baikite el. prekybos inicijavimo procesą.

> [!NOTE] 
> Jei jau esate „Dynamics 365 Commerce“ klientas, įdiegėte „e-Commerce“ svetainę, bet nepasirinkote įvertinimų ir apžvalgų, o norite naudoti paketo „Dynamics 365 Commerce“ įvertinimus ir apžvalgas, pateikite aptarnavimo užklausą. Norėdami gauti informacijos apie tai, kaip pateikti aptarnavimo užklausą, žr. [Pateikti aptarnavimo užklausų procesą](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Papildomi ištekliai

[Įvertinimų ir atsiliepimų apžvalga](ratings-reviews-overview.md)

[Įvertinimų ir atsiliepimų tvarkymas](manage-reviews.md)

[Įvertinimų ir atsiliepimų konfigūravimas](configure-ratings-reviews.md)

[Produktų įvertinimų sinchronizavimas sprendime „Dynamics 365 Commerce“](sync-product-ratings.md)

[Neautomatinio vadovo įvertinimų ir atsiliepimų publikavimo įjungimas](manual-publish-rating-reviews.md)

[Importuoti ir eksportuoti įvertinimus ir apžvalgas](import-export-reviews.md)

[Konfigūruoti paslaugos autentifikavimą](service-to-service-auth.md)

[DUK apie įvertinimus ir apžvalgas](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
