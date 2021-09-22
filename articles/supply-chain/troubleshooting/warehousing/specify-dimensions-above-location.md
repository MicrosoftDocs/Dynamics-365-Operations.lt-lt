---
title: Negalima išleisti dalinio kiekio įkėlimo naudojant paketų hierarchiją
description: Naudojant prekę su paketo virš rezervavimo hierarchija, krovinio eilutės turi nurodyti dimensijas virš vietos, kad būtų paskirstytos atsargos.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eb7e71cc271903cb689c33777b72862246f2dd42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477067"
---
# <a name="cant-release-a-load-for-partial-quantity-with-batch-above-reservation-hierarchy"></a>Negalima išleisti dalinio kiekio įkėlimo naudojant paketų rezervavimo hierarchiją

## <a name="symptoms"></a>Požymiai

Jums naudojant prekę, turinčią *paketas aukščiau* rezervavimo hierarchiją, puslapyje **Krovinio planavimo darbo sritis** esanti komanda **Išleisti į sandėlį** neveikia, jeigu bandote išleisti krovinį daliniam kiekiui. Galbūt gausite tolesnį klaidos pranešimą:

> Gaunu tolesnį klaidos pranešimą: „Tam kad būtų priskirtos prie bangos, krovinio eilutės turi nurodyti dimensijas virš vietos. Norėdami priskirti šias dimensijas, rezervuokite ir iš naujo sukurkite krovinio eilutę.

Tačiau, kai naudojate prekę, turinčią *paketas žemiau* rezervavimo hierarchiją, galite išleisti krovinį daliniam kiekiui iš **Krovinio planavimo darbo srities** puslapio.

## <a name="cause"></a>Priežastis

Kai dimensija yra virš **Vietos** dimensijos rezervacijos hierarchijoje, ji turi būti nurodytas prieš išleidimą į sandėlį. Atsargas galima sėkmingai paskirstyti tik tada, jei dimensijose aukščiau vietos nėra tarpų.

## <a name="resolution"></a>Sprendimas

Rezervuojant ir iš naujo **Vietos** sukurdami krovinio eilutę įsitikinkite, kad visos dimensijos virš vietos yra priskirtos.
