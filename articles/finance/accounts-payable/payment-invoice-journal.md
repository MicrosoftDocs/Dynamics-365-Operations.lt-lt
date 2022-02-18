---
title: Taikykite mokėjimo grafiką sąskaitų faktūrų žurnale
description: Šioje temoje aprašoma, kaip įtraukti mokėjimą į tiekėjo sąskaitų faktūrų žurnalą.
author: sunfzam
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: bd288ac48ef59d8e2a4e0922aa652276dddb666d
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075737"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>Taikykite mokėjimo grafiką sąskaitų faktūrų žurnale

[!include [banner](../includes/preview-banner.md)]

„Microsoft“.Dynamics 365 Finance leidimas 10.0.25, mokėjimo grafikas dabar palaikomas tiekėjo sąskaitų faktūrų žurnale.

Norėdami naudoti šią funkciją, turite įjungti **Taikyti mokėjimo grafiką sąskaitų faktūrų žurnale** Funkcijų valdymo funkcija.

Įjungus funkciją, naujas **Mokėjimo planas** laukas pridedamas prie **Sąskaitų faktūrų žurnalas** puslapį. Kai kuriate sąskaitos faktūros žurnalo eilutę, jei mokėjimo sąlygos palaikomos tiekėjui, o mokėjimo sąlygos pasirenkamos mokėjimo grafike, **Mokėjimo planas** laukas atnaujintas **Sąskaitų faktūrų žurnalas** puslapį.

Naudojamą mokėjimo grafiką galite pakeisti pagal savo verslo poreikius. Tiekėjo sąskaitų faktūrų žurnalo registravimo metu tiekėjo atviros operacijos bus sukurtos pagal mokėjimo grafiką.

Norėdami peržiūrėti kelias atidarytas tiekėjo operacijas, kurios buvo sugeneruotos pagal mokėjimų tvarkaraštį, eikite į **Mokėtinos sąskaitos \> Sąskaitos faktūros \> Atidaryti tiekėjo sąskaitas faktūras** ir įveskite sąskaitos faktūros numerį arba tiekėjo paskyrą.

Norėdami peržiūrėti arba konfigūruoti mokėjimo grafiką, eikite į **Mokėtinos sąskaitos \> Mokėjimo sąranka \> Mokėjimo planas**.

Norėdami sukonfigūruoti mokėjimo sąlygas ir priskirti mokėjimo grafiką, eikite į **Mokėtinos sąskaitos \> Mokėjimo nustatymas \> Mokėjimo sąlygos**.

Norėdami išlaikyti pardavėjo mokėjimo sąlygas, eikite į **Mokėtinos sąskaitos \> Visi pardavėjai**, pasirinkite tiekėjo paskyrą, tada **Mokėjimas** skirtuką, nustatykite **Mokėjimo sąlygos** lauke.

Mokėjimo tvarkaraščio funkcija taip pat pasiekiama **Pardavėjo sąskaitų faktūrų registras** procesas. Jei sąskaitų faktūrų registro žurnale pasirenkamas mokėjimo grafikas, bus naudojamos kelios tiekėjo mokėjimo eilutės **ne** sugeneruoti, kai registruojamas sąskaitų faktūrų registras. Tiekėjo mokėjimo eilutės bus sugeneruotos, kai sąskaita faktūra bus patvirtinta.

## <a name="limitation"></a>Apribojimai

Jei laukiančios tiekėjo sąskaitos faktūros mokėjimo grafikas yra sąskaitos faktūros antraštėje, yra išplėstinis puslapis, kuriame naudotojai gali redaguoti mokėjimo eilutes. (Pavyzdžiui, vartotojai gali redaguoti kiekvienos mokėjimo eilutės mokėjimo datą ir vertę.) Mokėjimo eilutės, sugeneruotos iš sąskaitų faktūrų žurnalo, turės vertę iš mokėjimo grafiko.

Ši funkcija bus prieinama tiekėjo sąskaitų faktūrų žurnalui ir laukiančioms sąskaitoms faktūroms būsimame leidime.
