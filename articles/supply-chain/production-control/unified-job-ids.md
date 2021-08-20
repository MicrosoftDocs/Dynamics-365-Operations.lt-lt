---
title: Bendra užduočių ID numerių seka
description: Ši funkcija suteikia bendrą, suvienodintą numeraciją, kuri sugeneruoja užduočių ID gamybos kontrolės, gamybos vykdymo ir laiko bei dalyvavo moduliams.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8ff8fae0bb20b11b15c7520fbb14727ff0372ca0255adc82599c6680a64671af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748720"
---
# <a name="unified-number-sequence-for-job-ids"></a>Bendra užduočių ID numerių seka

[!include [banner](../includes/banner.md)]

Ši funkcija suteikia bendrą, suvienodintą numeraciją, kuri sugeneruoja užduočių ID gamybos kontrolės, gamybos vykdymo ir laiko bei dalyvavo moduliams. Anksčiau galėjote pasirinkti skirtingą numeraciją kiekvienam šių modulių, tad galėdavo būti nesuderinamų užduočių ID, jei dvi ar daugiau numeracijų naudojo tą patį formatą. Toks nesuderinamumas gali sugadinti duomenis.

## <a name="turn-on-this-feature-for-your-system"></a>Šios funkcijos įjungimas sistemoje

Jei jūsų sistemoje dar nėra šioje temoje aprašytos funkcijos, eikite į [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ir įjunkite funkciją *Suvienodinta užduočių ID numeracija*.

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a>Suvienodintos užduočių ID numeracijos nustatymas

Įgalinus šią funkciją, esami **Užduoties identifikacijos** numeracijos parametrai, esantys gamybos kontrolės, gamybos vykdymo ir laiko bei dalyvavimo modulių parametrų puslapiuose, bus nerekomenduojami ir bus įtrauktas naujas laukas **Suvienodinti užduočių ID**. Reikšmę **Suvienodinti užduočių ID** bendrai naudoja visi trys moduliai ir taip užtikrinama, kad visi moduliai nurodo tą pačią numeraciją. Todėl užduočių ID bus unikalūs visuose trijuose moduliuose, tad niekada neatsiras nesuderinamumas.

Norėdami nustatyti suvienodintą užduočių ID numeraciją:

1. Įjunkite funkciją, kaip aprašyta ankstesniame skyriuje.
1. Nustatykite numeraciją, kurią norite naudoti savo vieningiems užduočių ID, arba sukurkite naują. Daugiau informacijos žr. skyriuje [Numeracijos apžvalga](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).
1. Eikite į **Gamybos kontrolės parametrai**, **Gamybos vykdymo parametrai** arba **Laiko bei dalyvavimo parametrai** puslapį. Nesvarbu, kurį puslapį pasirinksite, nes kai nustatote parametrą bet kuriame šių puslapių, visi kiti puslapiai atsinaujina automatiškai.
1. Atidarykite skirtuką **Numeracijos** pasirinktame parametrų puslapyje.
1. Priskirkite **Numeracijos kodą**, kurį anksčiau nustatėte tinklelio eilutėje **Suvienodinti užduočių ID**.
