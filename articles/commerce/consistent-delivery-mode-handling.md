---
title: Nuolatinio pristatymo būdo tvarkymo kanale įjungimas
description: Šiame straipsnyje aprašoma, kaip įgalinti nuoseklų pristatymo režimo tvarkymą, siekiant išspręsti galimas problemas, susijusias su mokesčių srautais Microsoft Dynamics 365 Commerce el. komercijos kanaluose.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 43450c9d380bd57c234bb1c9acfbe296ab115f14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279656"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>Nuolatinio pristatymo būdo tvarkymo kanale įjungimas 

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip įgalinti nuoseklų pristatymo režimo tvarkymą, siekiant išspręsti galimas problemas, susijusias su mokesčių srautais Microsoft Dynamics 365 Commerce el. komercijos kanaluose.

El Dynamics 365 Commerce. komercijos kanaluose, pagal numatytuosius nustatymus, neišsiųstos antraštės lygio išlaidos nėra taikomos. Dėl to el. komercijos kanaluose gali kilti viena arba abi šios problemos:

- Neatsiųstos antraštės lygio išlaidų nėra.
- Pristatymo būdų mokesčiai neatitinka pristatymo būdo ir užsakymo tikrinimo suvestinės.

Norėdami išspręsti šias problemas, turite įjungti kanalo funkcijos **funkciją Įgalinti nuoseklaus pristatymo režimo** tvarkymą. Ši funkcija užtikrina, kad el. komercijos kanaluose atsiras nesusiųstos antraštės lygio išlaidos, o pardavimo užsakymo pristatymo informacija tvarkoma pagal tą pačią užklausos darbo eigą.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Įjungti nuosekliojo pristatymo režimo valdymą kanalo funkcijai įjungti

Norėdami įgalinti nuoseklų **pristatymo režimo tvarkymą "** Commerce Headquarters" kanalų funkcijose, atlikite šiuos veiksmus.

1. Atidarykite **funkcijų valdymo darbo** sritį (**sistemos administravimo \> darbo sričių \> funkcijų valdymas**).
1. Galimų funkcijų sąraše ieškokite ir pasirinkite Įgalinti nuoseklų **pristatymo režimo tvarkymą kanale**.
1. Dešiniajame lange pasirinkite Įgalinti **dabar**.
