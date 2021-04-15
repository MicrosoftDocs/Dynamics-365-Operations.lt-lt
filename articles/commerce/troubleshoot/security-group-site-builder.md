---
title: Atliekant pradinį diegimą nepavyko sukonfigūruoti „Commerce” svetainių daryklės saugos grupės
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai „Microsoft Azure Active Directory” („Azure AD”) „Commerce” svetainių daryklės saugos grupė nerodoma kaip parinktis, kai kuriate el. prekybos komponentus „Microsoft Dynamics Lifecycle Services” (LCS) pirmą kartą diegdami naują el. prekybos nuomininką.
author: Reza-Assadi
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
ms.openlocfilehash: aa00e9331693600ced2f4ead399a0c005b77ad08
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801512"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Atliekant pradinį diegimą nepavyko sukonfigūruoti „Commerce” svetainių daryklės saugos grupės

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai „Microsoft Azure Active Directory” („Azure AD”) „Commerce” svetainių daryklės saugos grupė nerodoma kaip parinktis, kai kuriate el. prekybos komponentus „Microsoft Dynamics Lifecycle Services” (LCS) pirmą kartą diegdami naują el. prekybos nuomininką.

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
