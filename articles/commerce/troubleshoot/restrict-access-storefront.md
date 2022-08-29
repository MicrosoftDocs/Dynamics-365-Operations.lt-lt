---
title: Apriboti prieigą prie parduotuvės tikrinimo arba kūrimo metu
description: Šiame straipsnyje paaiškinama, kaip riboti prieigą prie parduotuvėsfrontės Microsoft Dynamics 365 Commerce, kol vyksta vidinis tikrinimas ar kūrimas.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: e382f01f82b368ad89f7abf122bf806dca4f0340
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292033"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>Apriboti prieigą prie parduotuvės tikrinimo arba kūrimo metu

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip riboti prieigą prie parduotuvėsfrontės Microsoft Dynamics 365 Commerce, kol vyksta vidinis tikrinimas ar kūrimas.

## <a name="description"></a>aprašymas

Vidinio tikrinimo arba aktyvaus kūrimo metu galite norėti apriboti prieigą prie jūsų svetainės, kad išoriniai vartotojai negalėtų pasiekti publikuotų parduotuvės puslapių.

## <a name="resolution"></a>Skiriamoji geba

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a>Nustatyti „Azure AD” B2C naudojant standartinius vartotojų srautus

Informacijos apie tai, kaip konfigūruoti jūsų el. prekybos svetainės „Azure Active Directory” B2C („Azure AD” B2C), ieškokite [„Commerce” B2C nuomotojo sąranka](../set-up-b2c-tenant.md).

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a>Apriboti vartotojo prieigą prie parduotuvės puslapių ir blokuoti naujų vartotojų kūrimą

Norėdami apriboti vartotojo prieigą prie parduotuvės puslapių „Commerce” svetainių daryklėje, atlikite šiuos veiksmus.

1. Nueikite į savo svetainę.
1. Pasirinkite **Puslapiai**, tada pasirinkite puslapį, kurio vartotojų prieigą apribosite.
1. Pasirinkite modulio arba fragmento vietą, tada pasirinkite **Redaguoti**.
1. Ypatybių srityje pasirinkite **Reikia prisijungti?**, tada pasirinkite **Baigti redaguoti**.
1. Pasirinkite **Publikuoti**.

Norėdami blokuoti naujų vartotojų kūrimą „Azure AD”, atlikite šiuos veiksmus.

1. Eikite į [„Azure“ portalą](https://portal.azure.com/).
1. Pasirinkite „Azure AD” B2C programą, kurią sukūrėte jūsų svetainės prieigai.
1. Kairiojoje naršymo srityje pasirinkite **Vartotojų srautai**.
1. Puslapio **Vartotojo srautai** viršuje pasirinkite **Naujas vartotojo srautas**.
1. Puslapyje **Pasirinkti vartotojo srauto tipą** pasirinkite **Peržiūra**.
1. Puslapio viduryje pasirinkite **Prisijungti prie v2**. Tada atlikite veiksmus, pateiktus [„Commerce” B2C nuomotojo sąranka](../set-up-b2c-tenant.md), norėdami konfigūruoti srautą kaip jūsų svetainės standartinį „Azure AD” B2C vartotojų srautą tikrinimo ar kūrimo metu.

## <a name="additional-resources"></a>Papildomi ištekliai

[„Commerce” B2C nuomotojo sąranka](../set-up-b2c-tenant.md)

[Vartotojo registracijos pasirinktinių puslapių sąranka](../custom-pages-user-logins.md)
