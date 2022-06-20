---
title: Sukūrus naujų klientų, nesiunčiamas pasisveikinimo el. laiškas
description: Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, jei pasisveikinimo el. laiškas nėra siunčiamas, kai sukuriamas naujas klientas Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 8e95b33d4b8a9af13c613ab89dd33de6b4934694
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853688"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Sukūrus naujų klientų, nesiunčiamas pasisveikinimo el. laiškas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, jei pasisveikinimo el. laiškas nėra siunčiamas, kai sukuriamas naujas klientas Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Aprašymas

Kai "Commerce Headquarters" sukuriamas naujas klientas, klientui nesiunčiamas pasveikinimo el. laiškas, **net** jei ir sukonfigūruotas kliento sukurto el. paštu siunčiamo pranešimo tipo el. laiškas.

## <a name="resolution"></a>Paaiškinimas

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>Nustatykite teisingą kliento sukurto el. paštu siunčiamo pranešimo tipo el. laiško ID vertę

Norėdami nustatyti teisingą kliento sukurto **el** . paštu siunčiamo pranešimo **tipo vertę** būstinėje, atlikite šiuos veiksmus.

1. Eikite į " **Retail" ir "Commerce \> Headquarters" nustatymo " \> Commerce" el. paštu siunčiamo pranešimo šabloną**.
1. Kairiojoje naršymo srityje pasirinkite el. paštu siunčiamo pranešimo šabloną.
1. Dalyje **Mažmeninės prekybos įvykio pranešimų parametrai kliento** sukurto el **. pašto** pranešimo tipui nustatykite el. laiško **ID** lauką **NewCust**.

## <a name="additional-resources"></a>Papildomi ištekliai

[El. paštu siunčiamo pranešimo šablono nustatymas](../email-notification-profiles.md)
