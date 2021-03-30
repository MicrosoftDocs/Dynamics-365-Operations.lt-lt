---
title: Patvirtinti siunčiamas siuntas naudojant paketines užduotis
description: Ši tema aprašo, kaip nustatyti pakuotės užduotį, kuri automatiškai tvirtina išorės perdavimo užsakymo siuntimus paruoštiems siųsti kroviniams.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: f4c4fd5e8cdea9a7fc05ec9cbc7866c44c6f78b2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243972"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Patvirtinti siunčiamas siuntas naudojant paketines užduotis

[!include [banner](../includes/banner.md)]

Ši tema aprašo, kaip nustatyti pakuotės užduotį, kuri automatiškai tvirtina išorės perdavimo užsakymo siuntimus paruoštiems siųsti kroviniams. Čia aprašyta pakuotės užduotis taikoma tik persiunčiamiems užsakymo siuntimams, o ne prekybos užsakymams.

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a>Įjunkite išorės siuntimų patvirtinimą pakuotės užduočių funkcijai

Norėdami pasinaudoti šia funkcija, ją turite įjungti savo sistemoje. Administratoriai gali naudoti [Funkcijas valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) puslapį tam, kad patikrintų funkcijos būseną ir įjungtų ją, jei reikia. Ši funkcija yra tokia:

- **Modulis** - *Sandėlio valdymas*
- **Funkcijos pavadinimas** - *Išorės siuntimų patvirtinimas pakuotės užduočių funkcijai*

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