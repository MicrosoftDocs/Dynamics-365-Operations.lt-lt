---
title: Grąžintini mokesčiai yra neteisingai apskaičiuoti remiantis grąžintu kiekiu
description: Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti kasininkams matyti neteisingus grąžinamus mokesčius iš kasos aparato (EKA) prekių kiekio, kuris grąžinamas.
author: gvrmohanreddy
ms.date: 03/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 7a84207f587a826b9acdfd818c64220c5327bde1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890248"
---
# <a name="refundable-charges-are-miscalculated-based-on-the-quantity-returned"></a>Grąžintini mokesčiai yra neteisingai apskaičiuoti remiantis grąžintu kiekiu

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti kasininkams matyti neteisingus grąžinamus mokesčius iš kasos aparato (EKA) prekių kiekio, kuris grąžinamas.

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
