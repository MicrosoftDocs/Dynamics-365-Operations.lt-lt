---
title: Negalite patvirtinti siuntos, nes krovimo linijose nurodytas kiekis lygus nuliui
description: Negalite patvirtinti siuntos, nes krovimo linijose nurodytas kiekis lygus nuliui.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 15aa7f5e72ff8f2c027b5b020a23328978aa02b0
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344239"
---
# <a name="you-cant-confirm-a-shipment-because-load-lines-have-zero-quantity"></a>Negalite patvirtinti siuntos, nes krovimo linijose nurodytas kiekis lygus nuliui

Klaidos kodas: WAX:LoadTableWarningAllLinesZero, WAX2543

## <a name="symptoms"></a>Požymiai

Kai bandote patvirtinti siuntą, sistema rodo šį klaidos pranešimą:

> Visų krovinio %1 eilučių kiekis yra nulinis.  
> Nepavyko patvirtinti krovinio %1 siuntimo.

Todėl negalite patvirtinti krovinio siuntimo.

## <a name="cause"></a>Priežastis

Sistema įvertina, ar krovinio eilutės siuntimas gali būti patvirtintas, remiantis sukurtų darbų ID, krovinio eilutės kiekiu ir pristatymo neatlikimo procentu. Jei sistema nustato, kad nėra darbo ID, o pristatymo neatlikimo procentas nustatytas kaip 100 procentų, siuntos patvirtinti negalite.

Pavyzdžiui, šis išdavimas gali atsirasti, jei darbas buvo atšauktas, o pristatymo eilutėje pristatymo procentinė dalis yra 100 procentų.

## <a name="resolution"></a>Sprendimas

Krovinio ar siuntimo būsena šiuo metu yra, kai siuntos patvirtinimas nesėkmingas. Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:

- Peržiūrėkite savo krovinio eilutes, kad įsitikintumėte, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir kad kiekiai atitinka.
- Peržiūrėkite krovinio eilutes, kad įsitikintumėte, jog pristatymo neatlikimo procentai ir kiekiai yra sulygiuoti su paimtu darbu.

### <a name="review-your-load-lines-to-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Peržiūrėkite savo krovinio eilutes, kad įsitikintumėte, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir kad kiekiai atitinka

Naudokite toliau pateiktą procedūrą savo krovinio eilučių peržiūrai, kad įsitikintumėte, jog visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Atidarykite pakrovimo, kuriam siuntimo patvirtinti nepavyksta, parinktį.
1. „FastTab” **Krovinio eilutės** patikrinkite pakrovimo eilutę.
1. Pasižymėkite lauko Darbo **sukurtas kiekis** vertę.
1. Veiksmų srities skirtuko **Pakrovimas** grupėje **Susijusi informacija** pasirinkite **Darbas**.
1. Patikrinkite, ar darbas užbaigtas galutinėje siuntimo vietoje ir ar paimtas darbo kiekis atitinka krovinio eilutėje sukurtą darbo kiekį.
1. Jei radote neatitikimą, atšaukite reikiamą darbą, perkonfigūruoti vietos nuostatas ir iš naujo paleiskite krovinį. Instrukcijas rasite [Negalite patvirtinti siuntos, nes prekės nebuvo paimtos](picked-quantity-is-not-on-final.md).
1. Pakartokite šią procedūrą visose krovinio eilutėse, norėdami įsitikinti, kad visi kriterijai yra įvykdyti.

### <a name="review-your-load-lines-to-make-sure-that-the-underdelivery-percentage-and-quantities-are-aligned-with-the-picked-work"></a>Peržiūrėkite krovinio eilutes, kad įsitikintumėte, jog pristatymo neatlikimo procentai ir kiekiai yra sulygiuoti su paimtu darbu

Naudokite šią procedūrą, norėdami peržiūrėti krovinio eilutes, kad įsitikintumėte, jog pristatymo neatlikimo procentai ir kiekiai yra sulygiuoti su paimtu darbu.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Atidarykite pakrovimo, kuriam siuntimo patvirtinti nepavyksta, parinktį.
1. Krovinio **eilučių** „FastTab" pasirinkite prekės, viršijančios pristatymo pateisavimo procentinę dalį, krovinio eilutę.
1. Koreguokite lauko Pristatymo **Pristatymas ne iki galo** vertę arba **lauką** Kiekis.

> [!TIP]
> Jei išdavimas vis tiek nėra fiksuotas, gali tekti atlikti daugiau susijusių pardavimo užsakymų arba perkėlimo užsakymų paėmimo darbų, kol turimas kiekis nesulygiuotas su kroviniu arba siunta.
