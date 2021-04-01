---
title: Prisijunkite, norėdami naudoti įvertinimus ir atsiliepimus
description: Šioje temoje paaiškinama, kaip sutikti naudoti įvertinimus ir apžvalgas savo „Microsoft Dynamics 365 Commerce“ svetainėje.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 6c54a8fa01badb6a383c41dc979e71d82a25ef97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251240"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip sutikti naudoti įvertinimus ir apžvalgas savo „Microsoft Dynamics 365 Commerce“ svetainėje.

## <a name="overview"></a>Peržiūra

Įvertinimų ir apžvalgų sprendimas yra daugiakanalis sprendimas, kurį galite padaryti pasiekiamą „Dynamics 365 Commerce“, naudojant „Microsoft Dynamics Lifecycle Services“ (LCS). LCS yra administravimo portalas, kurį prekybininkai naudoja valdyti savo aplinką nuo jos parengimo iki jos ekspoatacijos nutraukimo.

Jei norite naudoti įvertinimų ir apžvalgų sprendimą savo „Commerce“ svetainėje, turite pasirinkti įvertinimus ir apžvalgas diegiant savo „e-Commerce“ svetainę „Dynamics 365 Commerce“.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite

Norėdami sutikti naudoti įvertinimus ir apžvalgas savo svetainėje, atlikite šiuos veiksmus.

1. Vykdykite veiksmus, nurodytus temoje [Naujos el. prekybos svetainės diegimas](deploy-ecommerce-site.md).
1. Kol jūs vis dar esate LCS portale, eikite į **„Retail“ diegimo sąranka \> Kiti parametrai**.
1. Parinktį **Įjungti įvertinimų ir apžvalgų paslaugą** nustatykite kaip **Taip**.
1. Lauke **AAD saugos grupė, skirta įvertinimų ir apžvalgų moderatoriui (saugos grupės objekto ID)**, įveskite „Microsoft Azure Active Directory“ („Azure AD“) saugos grupės, apimančios įvertinimų ir atsiliepimų moderatorių vaidmenį, ID.

    ![Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite](media/LCS_RnR_Preference.png)

1. Baikite el. prekybos inicijavimo procesą.

> [!NOTE] 
> Jei jau esate „Dynamics 365 Commerce“ klientas, įdiegėte „e-Commerce“ svetainę, bet nepasirinkote įvertinimų ir apžvalgų, o norite naudoti paketo „Dynamics 365 Commerce“ įvertinimus ir apžvalgas, pateikite aptarnavimo užklausą. Norėdami gauti informacijos apie tai, kaip pateikti aptarnavimo užklausą, žr. [Pateikti aptarnavimo užklausų procesą](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Papildomi ištekliai

[Įvertinimų ir atsiliepimų apžvalga](ratings-reviews-overview.md)

[Įvertinimų ir atsiliepimų tvarkymas](manage-reviews.md)

[Įvertinimų ir atsiliepimų konfigūravimas](configure-ratings-reviews.md)

[Produktų įvertinimų sinchronizavimas sprendime „Dynamics 365 Commerce“](sync-product-ratings.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]