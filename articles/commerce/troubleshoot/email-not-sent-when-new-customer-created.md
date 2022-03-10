---
title: Sukūrus naujus klientus, pasisiųstas el. laiškas neišsiųstas
description: Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, jei pasisveikinimo el. laiškas nėra siunčiamas, kai sukuriamas naujas klientas Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 1a4faf6cd189f69232e7f9ab8d0e79b320cfe2d9
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349929"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Sukūrus naujus klientus, pasisiųstas el. laiškas neišsiųstas

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, jei pasisveikinimo el. laiškas nėra siunčiamas, kai sukuriamas naujas klientas Microsoft Dynamics 365 Commerce.

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
