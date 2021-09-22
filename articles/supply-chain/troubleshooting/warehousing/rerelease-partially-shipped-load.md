---
title: Negalite iš naujo išleisti dalinio siųsto krovinio į sandėlį
description: Ankstesnėse versijose, naudojant tam tikras funkcijas, kuriose yra nebaigtų rezervavimų, iš naujo išduoti iš dalies išsiųsto krovinio. Tai buvo ištaisyta.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0380e1963a38f2be55b31e06b3845f935661eed2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477109"
---
# <a name="cant-re-release-a-partially-shipped-load-to-the-warehouse"></a>Negalite iš naujo išleisti dalinio siųsto krovinio į sandėlį

## <a name="symptoms"></a>Požymiai

Negalite išleisti dalinio siųsto krovinio į sandėlį. Jums atliekant išleidimą į sandėlį, rodomas pranešimas „Veiksmas užbaigtas“, bet nieko nevyksta ir likusiam kiekiui nėra sukuriamas joks darbas. Ši problema atsitinka jums naudojant transportavimo krovinio funkciją ir kai yra nebaigta rezervacija.

## <a name="resolution"></a>Sprendimas

[KB problema 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) („Dalinai siunčiami kroviniai gali būti iš naujo suplanuojami bangai arba pakartotinai apdorojami") yra ištaisyta [versijoje 10.0.15](/dynamics365/supply-chain/get-started/whats-new-scm-10-0-15).
