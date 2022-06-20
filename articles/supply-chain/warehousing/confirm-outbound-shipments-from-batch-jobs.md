---
title: Patvirtinti siunčiamas siuntas naudojant paketines užduotis
description: Šiame straipsnyje aprašoma, kaip nustatyti paketinę užduotį, kuri automatiškai patvirtina paruoštų išsiųsti krovinių išsiuntimo užsakymo siuntas.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 00749a69b17b0064290d7b41ccb2171386716302
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875107"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Patvirtinti siunčiamas siuntas naudojant paketines užduotis

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti paketinę užduotį, kuri automatiškai patvirtina paruoštų išsiųsti krovinių išsiuntimo užsakymo siuntas. Čia aprašyta pakuotės užduotis taikoma tik persiunčiamiems užsakymo siuntimams, o ne prekybos užsakymams.

## <a name="turn-the-confirm-outbound-shipments-from-batch-jobs-feature-on-or-off"></a>Įjungti arba išjungti paketinių užduočių funkciją patvirtinti siunčiamas siuntas

Norint naudoti šiame straipsnyje aprašytas funkcijas, *jūsų sistemai turi būti įjungta funkcija Patvirtinti siunčiamas siuntas* iš paketinių užduočių. Kaip ir tiekimo grandinės valdymo versija 10.0.21 ši funkcija įjungiama pagal numatytąjį nustatymą. Kaip ir tiekimo grandinės valdymas 10.0.25 ši funkcija yra privaloma ir jos išjungti negalima. Jei naudojate senesnę nei 10.0.25 versiją, *·*[tada administratoriai gali įjungti arba išjungti šią funkciją ieškodami siunčiamų siuntų patvirtinimo iš paketinių užduočių funkcijų funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo srityje.

## <a name="process-outbound-shipments"></a>Apdoroti siunčiamas siuntas

Pakuotės darbo vykdančio išorės siuntimo patvirtinimą paruoštiems siųsti kroviniams nustatymui:

1. Eikite į **Sandėlio valdymas \> Periodinės užduotys \> Išorės siuntimų apdorojimas**.
1. **Siutimo patvirtinimo** langas atsidaro. „FastTab„ **Įtrauktini įrašai** pasirinkite **Filtruoti**.
1. Užklausos redagavimo langas atsidaro. **Diapazonas** skirtuke, įtraukite eilutę su šiomis vertėmis:
    - **Lentelė** - *Kroviniai*
    - **Pristatymų lentelė** - *Kroviniai*
    - **Laukelis** - *Krovinio būsena*
    - **Kriterijai** - *Pakrauta*
1. Pasirinkite **Gerai** grįžimui į **Siuntimo patvirtinimo** teksto langelį.
1. **Vykdyti fone** „FastTab“, nustatykite **Paketo apdorojimą** į **Taip**.
1. **Vykdyti fone** „FastTab“, pasirinkite **Pakartojimas**.
1. **Nustatyti pakartojimą** langas atsidaro. Vykdykite tvarkaraštį, kaip būtina jūsų organizacijoje.
1. Pasirinkite **Gerai** grįžimui į **Siuntimo patvirtinimo** teksto langelį.
1. Pasirinkite **Gerai** **Siuntimo patvirtinimo** teksto langelyje ir įtraukite pakuotės užduotį į pakuotės eilę.

Norėdami gauti daugiau informacijos, žr. [Paketo apdorojimo apžvalgą](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]