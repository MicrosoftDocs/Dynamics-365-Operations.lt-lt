---
title: Prisijungimo saitas nukreipia atgal į el. prekybos svetainę
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti, kai prisijungimo saitas nukreipia atgal į el. prekybos svetainę, o ne prisijungimo puslapį.
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
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e83b381e73d28dce0a438a37d5f8ed23b4957adf
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350383"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>Prisijungimo saitas nukreipia atgal į el. prekybos svetainę

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti, kai prisijungimo saitas nukreipia atgal į el. prekybos svetainę, o ne prisijungimo puslapį.

## <a name="description"></a>Aprašymas

Sukonfigūravę naują „Microsoft Azure Active Directory B2C“ („Azure AD B2C“) nuomininką „Commerce“ svetainių daryklėje, nuorodą **Prisijungti** pasirinkę vartotojai nukreipiami atgal į pagrindinį el. prekybos nukreipimo puslapį, o ne prisijungimo puslapį.

## <a name="resolution"></a>Sprendimas

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a>Patvirtinti, kad atsakymo URL tinkamai sukonfigūruotas „Azure AD” B2C programoje

Norėdami patvirtinti, kad atsakymo URL tinkamai sukonfigūruotas „Azure AD” B2C programoje, atlikite šiuos veiksmus.

1. Eikite į [„Azure“ portalą](https://portal.azure.com/).
1. Pasirinkite „Azure AD” B2C programą, kurią sukūrėte jūsų svetainės prieigai.
1. Pasirinkite programą, kurią sukūrėte „Azure AD” B2C nustatymo metu.
1. Dalyje **Atsakymo URL** patikrinkite, kad sąraše yra ir svetainės domeno URL, ir el. prekybos sugeneruoto URL įrašai, kaip parodyta toliau pateiktos iliustracijos pavyzdyje.

    ![„Azure AD” B2C atsakymo URL įrašai.](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> Svetainės domeno URL ir el. prekybos sugeneruotas URL turi būti tinkamo URL formato, kuris neįtraukia priekinių arba pabaigos pasvirųjų brūkšnių.

## <a name="additional-resources"></a>Papildomi ištekliai

[Žiniatinklio programos užregistravimas „Azure Active Directory” B2C](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[„Commerce” B2C nuomotojo sąranka](../set-up-b2c-tenant.md)