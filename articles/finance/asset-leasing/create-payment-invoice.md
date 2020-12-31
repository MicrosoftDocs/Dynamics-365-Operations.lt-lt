---
title: Mokėjimo SF kūrimas
description: Šioje temoje paaiškinama, kaip kurti mėnesines nuomos SF. Galite kurti atskiros nuomos SF arba galite naudoti paketinį procesą, kad sukurtumėte kelių nuomų SF.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 32618814d00cb1e1f1082169a64b187cce1e76b4
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446180"
---
# <a name="create-payment-invoices"></a>Mokėjimo SF kūrimas

[!include [banner](../includes/banner.md)]

Galite kurti mėnesines atskiros nuomos SF arba galite naudoti paketinį procesą, kad sukurtumėte kelių nuomų SF. Tolesnė procedūra nurodo, kaip sukurti atskirą nuomos mokesčio įrašą, kai puslapyje **Nuomos knygų sąranka** parametras **Mokėti tiekėjui** yra įjungtas.

1. Puslapyje **Nuomos suvestinė** pasirinkite nuomą, tada – **Knygos \> Mokėjimo grafikas**.
2. Pasirinkite mokėjimą, kurį reikia atlikti, tada pasirinkite **Kurti žurnalą**. Gausite pranešimą, kuriame bus nurodoma, kad buvo sukurtas žurnalas pagal pasirinktą mokėjimą.
3. Pasirinkite **SF žurnalai**, tada pasirinkite SF, kuri turi būti apmokėta.
4. Skirtuke **Eilutės** peržiūrėkite žurnalo įrašą, prieš jį registruodami didžiojoje knygoje.

    > [!NOTE]
    > Pagal numatytuosius parametrus sukurtose tiekėjo SF eilutėse naudojamas tiekėjo registravimo šablonas iš puslapio **Mokėtinų sumų parametrai**.

5. Pasirinkite tinkamą žurnalą, tada pasirinkite SF, kuri turi būti apmokėta.

    Šiame pavyzdyje nuomos knygos parametras **Mokėti tiekėjui** yra įjungtas. Todėl SF bus SF žurnale. Skyriuje **Apžvaga** pateikiama žurnalo įrašo suvestinė, o skyriuje **Eilutės** rodoma informacija apie faktines žurnalo eilutes.

    > [!NOTE]
    > Jei parametras **Mokėti tiekėjui** yra išjungtas, mokėjimo žurnalo įrašai bus pateikti nuomos knygos puslapyje **Turto nuoma**, o sistema sukurs turto nuomos įrašą vietoj SF. Nuomos mokesčio įrašas bus užregistruotas žurnalo pavadinime, kuris nurodytas lauke **Mėnesinis nuomos žurnalas**.

6. Užregistravę operaciją, galite peržiūrėti operacijos informaciją ir nuomos įsipareigojimo balansinę vertę nuomos knygoje pasirinkdami **Įsipareigojimų operacijos**.

    Mokėjimo grafike bus pažymėtas žymės langelis **Žurnalas užregistruotas**, o eilutėje bus rodomas SF žurnalo numeris. Kai sukurtas mokėjimo žurnalas ir to žurnalo įrašas, reikia atšaukti įrašą, kad būtų galima jį sukurti iš naujo.
