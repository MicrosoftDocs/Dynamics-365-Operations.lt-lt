---
title: Atliekant pradinį diegimą nepavyko sukonfigūruoti „Commerce” svetainių daryklės saugos grupės
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai „Microsoft Azure Active Directory” („Azure AD”) „Commerce” svetainių daryklės saugos grupė neodoma kaip parinktis, kai kuriate el. prekybos komponentus „Microsoft Dynamics Lifecycle Services” (LCS) pirmą kartą diegdami naują el. prekybos nuomininką.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36ea43e19f395e3914d3eda1a9b8f5487b0926c5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585450"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Atliekant pradinį diegimą nepavyko sukonfigūruoti „Commerce” svetainių daryklės saugos grupės

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai „Microsoft Azure Active Directory” („Azure AD”) „Commerce” svetainių daryklės saugos grupė neodoma kaip parinktis, kai kuriate el. prekybos komponentus „Microsoft Dynamics Lifecycle Services” (LCS) pirmą kartą diegdami naują el. prekybos nuomininką.

## <a name="description"></a>Aprašymas

Kai kuriate el. prekybos komponentus, diegdami naują el. prekybos nuomininką, kuriame yra „Commerce“ svetainių daryklės komponentas, „Azure AD“ saugos grupė nerodoma kaip parinktis dialogo lange.

## <a name="resolution"></a>Sprendimas

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>Parengti el. prekybos svetainę tinkamo nuomininko vartotoju

1. Eikite į [„Azure“ portalą](https://portal.azure.com/).
1. Nuomininke, kuriam buvo parengtas jūsų el. prekybos svetainės LCS projektas, vykdykite instrukcijas, pateiktas [Pagrindinės grupės kūrimas ir narių įtraukimas naudojant „Azure Active Directory”](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).
1. Eikite į [LCS](https://lcs.dynamics.com/) ir prisijunkite naudodami sąskaitą, naudojančią tą patį nuomininką kaip ir ką tik sukurta „Azure AD” saugos grupė. Sąskaita turi turėti prieigą peržiūrėti „Azure AD” saugos grupę.
1. Norėdami sukonfigūruoti el. prekybos svetainę, užbaikite sąrankos veiksmus. Kai parengiate el. prekybos komponentus, saugos grupė turėtų būti rodoma kaip dialogo lango parinktis.

> [!NOTE]
> Norėdami užtikrinti, kad dialogo lange esantis laukas būtų užpildytas saugos grupių sąrašu, įvesdami sukurtos „Azure AD” saugos grupės pavadinimą, turite pasirinkti **Įvesti**. Ieškos rezultatuose bus pateiktos visos „Azure AD” saugos grupės, kurios prasideda ieškos tekstu ir prie kurių vartotojas turi prieigą. Galite naudoti trumpesnį ieškos terminą, kad būtų galima gauti platesnes ieškos rezultatų.

## <a name="additional-resources"></a>Papildomi ištekliai

[Pagrindinės grupės kūrimas ir narių įtraukimas naudojant „Azure Active Directory”](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[Naujo el. prekybos nuomotojo diegimas](../deploy-ecommerce-site.md)
