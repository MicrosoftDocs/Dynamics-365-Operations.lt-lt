---
title: Sukonfigūrus šabloną nepakanka klasterio darbo
description: Jei konfigūruojate klasterio šabloną, galite gauti klaidos pranešimą, kuriame teigiama, kad nepakanka darbo. Redaguokite profilį ir nustatykite Aktyvinti pozicijas kaip Ne.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 139fd72e571c8ef83af2fd0e497cf334b6ef0ea4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477058"
---
# <a name="not-enough-work-found-for-cluster-when-using-system-directed-cluster-picking"></a>Buvo rasta nepakankamai darbo klasteriui, kai naudojamas sistemos nurodomas klasterio paėmimas

## <a name="symptoms"></a>Požymiai

Jums naudojant *Sistemos kreipiamą klasterio paėmimo* procesą, jei konfigūruojate klasterio profilį, kai pavyzdžiui, 10 padėčių gali būti paimtos, procesas veikia kaip planuota, kai yra pakankamai darbo siekiant paimti iki 10 padėčių. Tačiau jei reikia paimti tik aštuonias pareigas, gausite tokį klaidos pranešimą:

> Klasteriui rasta nepakankamai darbo.

## <a name="resolution"></a>Sprendimas

Siekiant ištaisyti šią problemą, redaguokite klasterio profilį ir nustatykite **Įjungti padėtis** parinktį į *Ne*.
