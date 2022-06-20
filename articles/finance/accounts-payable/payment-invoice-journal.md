---
title: Mokėjimų grafiko taikymas SF žurnalui
description: Šiame straipsnyje aprašoma, kaip įtraukti mokėjimą į tiekėjo SF žurnalą.
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
ms.openlocfilehash: f3ae08ea46be66dd8bf26f7f91bd73f6c5b9192f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863136"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>Mokėjimų grafiko taikymas SF žurnalui

[!include [banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 finansų išleidimo 10.0.25 **mokėjimo grafikas dabar palaikomas tiekėjo SF žurnale**.

Norėdami naudoti šią funkciją, funkcijų valdymo srityje turite įjungti **mokėjimo grafiko taikykite SF** žurnalo funkciją.

Įgalinus funkciją, į SF žurnalo **puslapį** įtraukiamas naujas mokėjimų **grafiko** laukas. Kai kuriate SF žurnalo eilutę, jei mokėjimo sąlygos tvarkomos tiekėjui ir mokėjimo grafike pasirinktos mokėjimo sąlygos, **·** **mokėjimo grafiko laukas atnaujinamas SF žurnalo** puslapyje.

Galite keisti naudojamą mokėjimo grafiką, atsižvelgiant į savo verslo poreikius. Registruojant tiekėjo SF žurnalą, atviros tiekėjo operacijos bus kuriamos pagal mokėjimo grafiką.

 - Norėdami peržiūrėti kelias tiekėjo atviras operacijas **\>, sugeneruotas pagal mokėjimo grafiką, \>** eikite į Mokėtinų sumų SF Atviros tiekėjo SF ir įveskite SF numerį arba tiekėjo kodą.
 - Norėdami peržiūrėti arba konfigūruoti mokėjimo grafiką, eikite į mokėtinų **sumų \> mokėjimo nustatymo mokėjimo \> grafiką**.
 - Norėdami konfigūruoti mokėjimo sąlygas ir priskirti mokėjimo grafiką, eikite į mokėtinų **\> sumų mokėjimo nustatymo \> mokėjimo sąlygas**.
 - Norėdami tvarkyti tiekėjo mokėjimo sąlygas, **\>** eikite į Mokėtinos sumos Visi tiekėjai, pasirinkite tiekėjo sąskaitą, **·** **tada skirtuke Mokėjimas nustatykite mokėjimo lauką.**

Mokėjimo grafiko priemonė taip pat galima tiekėjo **SF registro procese**. Jei SF registro žurnale pasirinktas mokėjimo grafikas, registruojant SF registrą **nebus** sugeneruotos kelios tiekėjo mokėjimo eilutės. Tiekėjo mokėjimo eilutės bus sugeneruotos patvirtinus SF.

## <a name="limitation"></a>Apribojimai

Jei sf antraštėje yra laukiančios tiekėjo SF mokėjimo grafikas, yra išplėstinis puslapis, kuriame vartotojai gali redaguoti mokėjimo eilutes. (Pvz., vartotojai gali redaguoti kiekvienos mokėjimo eilutės terminą ir vertę.) Iš SF žurnalo sugeneruotos mokėjimo eilutės turės vertę iš mokėjimo grafiko.

Šią funkciją bus galima naudoti tiekėjo SF **žurnale ir** būsimuose **leidime** laukiančios SF.
