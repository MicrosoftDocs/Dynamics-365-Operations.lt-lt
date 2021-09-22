---
title: Sertifikato maršruto klaida naujinant arba perkeliant į WMS
description: Jei atnaujinant arba perkeliant į WMS programa rodo klaidą „Trust anchor for certification path" nerasta, šiame puslapyje pateikiama informacija, kaip išspręsti problemą.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2cff41455268c43bdd99e285b9675f0c69be7de7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477066"
---
 # <a name="trust-anchor-for-certification-path-not-found-when-updating-and-migrating-to-wms"></a>Atnaujinant ir perkeliant į WMS nepavyko rasti sertifikato maršruto pasitikėjimo prieraišo

## <a name="symptoms"></a>Požymiai

Naujinant ir perkeliant į išplėstinį „warehouse management“ (WMS), „warehouse management“ programa gali parodyti tokį klaidos pranešimą:

> Gaunu tolesnį klaidos pranešimą: „java.security.cert.certPathValidatorException: Pasitikėjimo inkaras sertifikavimo keliui nerastas.

## <a name="cause"></a>Priežastis

Taip nutinka, nes vietiniame aplinkoje 8+ nepasitikima „Android“ pasirašytų sertifikatų.

## <a name="resolution"></a>Sprendimas

Naudokite išorės (viešąją) seritfikavimo įstaigą (CA). Šios trikties pašalinimas yra prieinamas „Warehouse Management“ 1.9.0.0 programose versijoje. Norėdami gauti daugiau informacijos apie šią problemą ir kaip ją išspręsti, nustatydami programos ryšį, žr. [Pasitikėjimo inkaras sertifikavimo keliui nerastas nustatant programos ryšį](certification-path-app-connection-error.md).
