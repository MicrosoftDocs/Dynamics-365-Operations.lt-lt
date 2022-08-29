---
title: Sukūrus naujų klientų, nesiunčiamas pasisveikinimo el. laiškas
description: Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, jei pasisveikinimo el. laiškas nėra siunčiamas, kai sukuriamas naujas klientas Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 5aa7d864555f96194500989e2d7ad200d8892121
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219410"
---
# <a name="welcome-email-isnt-sent-when-new-customers-are-created"></a>Pasisveikimo el. laiškas, kai sukuriami nauji klientai, nesiunčiamas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, jei pasisveikinimo el. laiškas nėra siunčiamas, kai sukuriamas naujas klientas Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Aprašymas

Kai "Commerce Headquarters" sukuriamas naujas klientas, klientui nesiunčiamas pasveikinimo el. laiškas, **net** jei ir sukonfigūruotas kliento sukurto el. paštu siunčiamo pranešimo tipo el. laiškas.

## <a name="resolution"></a>Paaiškinimas

### <a name="associate-an-email-notification-profile-under-commerce-parameters"></a>Susieti el. paštu siunčiamo pranešimo šabloną pagal "Commerce" parametrus

1. Būstinę eikite į "Retail" **ir "Commerce \> Headquarters" nustatymo \> " \> Commerce" parametrai \> bendrieji parametrai**.
2. El. **paštu siunčiamo pranešimo šablono** išplečiamajame sąraše pasirinkite el. paštu siunčiamo pranešimo šabloną, kuriame yra kliento sukurto pranešimo tipo ir kliento sukurto el. laiško šablono susiejimas.  

> [!NOTE] 
> Kai įgalinsite kliento sukurtus pranešimus, klientai, sukurti visuose juridinio subjekto kanaluose, gaus kliento sukurtą el. laišką. Šiuo metu kliento sukurti pranešimai negali būti apriboti vienu kanalu.

Daugiau informacijos rasite operacijų įvykių [el. laiškų šablonų kūrimas](../email-templates-transactions.md). 

## <a name="additional-resources"></a>Papildomi ištekliai

[El. paštu siunčiamo pranešimo šablono nustatymas](../email-notification-profiles.md)
