---
title: Atliekant pradinį diegimą nepavyko sukonfigūruoti „Commerce” svetainių daryklės saugos grupės
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai „Microsoft Azure Active Directory” („Azure AD”) „Commerce” svetainių daryklės saugos grupė nerodoma kaip parinktis, kai kuriate el. prekybos komponentus „Microsoft Dynamics Lifecycle Services” (LCS) pirmą kartą diegdami naują el. prekybos nuomininką.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: f930cac61b747037b9fbecc7397a9b1b7db5dabd8a86b63a61c92ac7abe17516
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765175"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Atliekant pradinį diegimą nepavyko sukonfigūruoti „Commerce” svetainių daryklės saugos grupės

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai „Microsoft Azure Active Directory” („Azure AD”) „Commerce” svetainių daryklės saugos grupė nerodoma kaip parinktis, kai kuriate el. prekybos komponentus „Microsoft Dynamics Lifecycle Services” (LCS) pirmą kartą diegdami naują el. prekybos nuomininką.

## <a name="description"></a>Aprašymas

Kai kuriate el. prekybos komponentus, diegdami naują el. prekybos nuomininką, kuriame yra „Commerce“ svetainių daryklės komponentas, „Azure AD“ saugos grupė nerodoma kaip parinktis dialogo lange.

## <a name="resolution"></a>Sprendimas

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>Parengti el. prekybos svetainę tinkamo nuomininko vartotoju

1. Eikite į [„Azure“ portalą](https://portal.azure.com/).
1. Nuomininke, kuriam buvo parengtas jūsų el. prekybos svetainės LCS projektas, vykdykite instrukcijas, pateiktas [Pagrindinės grupės kūrimas ir narių įtraukimas naudojant „Azure Active Directory”](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).
1. Eikite į [LCS](https://lcs.dynamics.com/) ir prisijunkite naudodami sąskaitą, naudojančią tą patį nuomininką kaip ir ką tik sukurta „Azure AD” saugos grupė. Sąskaita turi turėti prieigą peržiūrėti „Azure AD” saugos grupę.
1. Norėdami sukonfigūruoti el. prekybos svetainę, užbaikite sąrankos veiksmus. Kai parengiate el. prekybos komponentus, saugos grupė turėtų būti rodoma kaip dialogo lango parinktis.

> [!NOTE]
> Norėdami užtikrinti, kad dialogo lange esantis laukas būtų užpildytas saugos grupių sąrašu, įvesdami sukurtos „Azure AD” saugos grupės pavadinimą, turite pasirinkti **Įvesti**. Ieškos rezultatuose bus pateiktos visos „Azure AD” saugos grupės, kurios prasideda ieškos tekstu ir prie kurių vartotojas turi prieigą. Galite naudoti trumpesnį ieškos terminą, kad būtų galima gauti platesnes ieškos rezultatų.

## <a name="additional-resources"></a>Papildomi ištekliai

[Pagrindinės grupės kūrimas ir narių įtraukimas naudojant „Azure Active Directory”](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[Naujo el. prekybos nuomotojo diegimas](../deploy-ecommerce-site.md)