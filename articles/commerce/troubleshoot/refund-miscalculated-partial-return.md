---
title: Grąžintini mokesčiai yra perskaičiuoti remiantis grąžintau kiekiu
description: Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti kasininkams matyti neteisingus grąžinamus mokesčius iš kasos aparato (EKA) grąžinamų prekių kiekio.
author: gvrmohanreddy
ms.date: 03/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c8ecaa0cb73d06ac66b57cce815264e841a2259b
ms.sourcegitcommit: 94ebdaae6dc996b205ac78ed546e38f91f4f46ed
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/28/2022
ms.locfileid: "8489728"
---
# <a name="refundable-charges-are-miscalculated-based-on-the-quantity-returned"></a>Grąžintini mokesčiai yra perskaičiuoti remiantis grąžintau kiekiu

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti kasininkams matyti neteisingus grąžinamus mokesčius iš kasos aparato (EKA) grąžinamų prekių kiekio.

## <a name="description"></a>Aprašymas

Klientas grąžina dalinį prekių, nupirktų pagal pardavimo užsakymą, kuriame yra eilutės lygio grąžintinos išlaidos, kiekį. Tačiau vietoj to, kad būtų rodomas dalinis grąžinimas, EKA visus mokesčius rodo kaip grąžintinas.

Pavyzdžiui, klientas perka penkių prekių kiekį ir $5 prekių, o bendros išlaidos $25. Tada klientas grąžina tris iš penkių prekių. Tačiau, kasininkas rodomas $25 EKA grąžinamas mokestis, o ne tikėtinos $15 grąžinamos trijų prekių mokestis.

## <a name="resolution"></a>Paaiškinimas

### <a name="turn-on-the-enable-refunding-charges-based-on-the-refunded-quantity-feature"></a>Įjungti grąžinimo išlaidų įgalinimo remiantis grąžinimo kiekio funkcija

Pagal versiją Microsoft Dynamics 365 Commerce 10.0.26 įgalinti grąžinimo išlaidas, remiantis grąžinamo kiekio funkcija, leidžia apskaičiuoti eilutės lygio grąžinamus mokesčius pagal prekių kiekį, **kuris** grąžinamas.

Norėdami įgalinti grąžinimo **išlaidų įgalinimo remiantis "Commerce Headquarters" grąžinimo** kiekio funkcija, atlikite šiuos veiksmus.

1. Atidarykite **funkcijų valdymo darbo** sritį (**sistemos administratoriaus \> darbo sričių \> funkcijų valdymas**).
1. Galimų funkcijų sąraše ieškokite ir pasirinkite funkciją Įgalinti **grąžinimo mokesčius, remiantis grąžinamo kiekio** funkcija.
1. Dešiniajame lange pasirinkite Įgalinti **dabar**.
