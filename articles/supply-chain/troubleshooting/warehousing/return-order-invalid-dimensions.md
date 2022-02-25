---
title: Negalima sukurti krovinio eilutės, nes yra netinkamų atsargų dimensijų
description: Bandant išleisti grąžinamą pardavimo užsakymą į sandėlį, gali būti, kad įvyko klaida dėl netinkamų atsargų dimensijų. Pašalinti juos iš užsakymo eilutės.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b02408b61b07b272a7e7d52004dc2492d60ef28c
ms.sourcegitcommit: 0d14c4a1e6cf533dd20463f1a84eae8f6d88f71b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119217"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>Negalima sukurti krovinio pardavimo užsakymo gražinimą, nes yra netinkamų atsargų dimensijų

## <a name="symptoms"></a>Požymiai

Bandant išleisti grąžinimo pardavimo užsakymą į sandėlį, galite gauti šią klaidos žinutę:

> Gaunu tolesnį klaidos pranešimą: „Negalite sukurti krovinio eilutės šiam užsakymo eilutei, nes joje esantys inventoriaus matmenys negalioja. Negalite susieti inventoriaus matmenų, kurios yra nustatytos po vietos matmenimis rezervacijos hierarchijoje. Pašalinkite negaliojančius matmenis iš prekybos eilutės.

## <a name="resolution"></a>Sprendimas

Deja, produktas nepalaiko krovinio apdorojimo prekybos grąžinimo procese. Dėl to, negalite išleisti grąžinimo prekybos užsakymo į sandėlį.

Prekybos užsakymo perlaidose, negalite nurodyti inventoriaus matmenų, kurie yra žemiau **Vietos** matmenų rezervacijos hierarchijoje. Išsprendimas skirtas pašalinti negaliojančius matmenis iš prekybos eilutės.
