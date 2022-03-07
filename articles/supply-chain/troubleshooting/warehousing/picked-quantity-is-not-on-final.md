---
title: Negalima patvirtinti siuntos, nes prekės nebuvo paimtos
description: Negalima patvirtinti siuntos, nes prekės nebuvo paimtos
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7b57d3151852c9a2880185b7d9414e4246b7efb6429fcfce04c7cdae4ee00e37
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760929"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>Negalima patvirtinti siuntos, nes prekės nebuvo paimtos

Klaidos kodas: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Požymiai

Kai bandote patvirtinti siuntą, sistema rodo šį klaidos pranešimą:

> Kai kurios prekės, kurias reikia pakrauti %1, dar nepaimtos ir neperkeltos į galutinę siuntimo vietą.

Todėl negalite patvirtinti krovinio siuntimo.

## <a name="cause"></a>Priežastis

Dabartinės krovinio arba siuntos būsenos patvirtinti negalima, nes gali būti viena iš šių sąlygų:

- Susijęs darbas dar neparinktas ir perkeltas į galutinę siuntimo vietą.
- Paimtas darbo kiekis neatitinka sukurto darbo kiekio krovinio eilutėje.
- Vietos nurodymas buvo sukonfigūruotas su pakavimo vieta kaip galutine siuntimo vieta naudojant Bangos šablono krovimą į konteinerius.

## <a name="resolution"></a>Sprendimas

Krovinio ar siuntimo būsena šiuo metu yra, kai siuntos patvirtinimas nesėkmingas. Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:

- Peržiūrėkite savo krovinio eilutes bei įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka.
- Atšaukite darbo ID, kurios buvo sukurtos su pakavimo vieta kaip galutine siuntimo vieta, perkonfigūruokite vietos nurodymą ir iš naujo išleiskite krovinį.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Peržiūrėkite savo krovinio eilutes bei įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka

Naudokite toliau pateiktą procedūrą savo krovinio eilučių peržiūrai ir įsitikinkite, kad visi susiję darbai buvo užbaigti galutinėje siuntimo vietoje ir tai, kad kiekiai atitinka.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.
1. „FastTab” **Krovinio eilutės** patikrinkite pakrovimo eilutę.
1. Pasižymėkite lauko Darbo **sukurtas kiekis** vertę.
1. Veiksmų srities skirtuko **Pakrovimas** grupėje **Susijusi informacija** pasirinkite **Darbas**.
1. Patikrinkite, ar darbas užbaigtas galutinėje siuntimo vietoje ir ar paimtas darbo kiekis atitinka krovinio eilutėje sukurtą darbo kiekį.
1. Pakartokite šią procedūrą visose krovinio eilutėse, norėdami įsitikinti, kad visi kriterijai yra įvykdyti.

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a>Atšaukite darbo ID, kurios buvo sukurtos su pakavimo vieta kaip galutine siuntimo vieta, perkonfigūruokite vietos nurodymą ir iš naujo išleiskite krovinį

Naudokite toliau pateiktą procedūrą, kad atšauktumėte darbo ID, kurių pakavimo vieta yra ir galutinė išdavimo vietą, kai naudojamas automatinis krovimas į konteinerius.

1. Eiti į **Sandėlio valdymo \> periodines užduotis \> Valyti darbą \> Atšaukti**.
1. Atidaromas **Atšaukti darbą** dialogo langas. Lauke **Darbo ID** nurodykite darbo, kurį norite atšaukti, ID. Pasirinkto darbo ID privalo turėti vieną iš šių **Darbo būsenos** reikšmių: *Atidaryta*, *Progresuojanti*, *Atšaukta*, *Sujungta* ar *Uždaryta*.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Taip**, kad patvirtintumėte, kad norite atšaukti darbą.
1. Pakartokite šią procedūrą kitoms darbo ID, jei reikia.

Dėl platesnės informacijos, žr. [Darbo sandėlyje atšaukimas dėl išimčių tvarkymo](../../warehousing/cancel-warehouse-work.md).

Naudokite tolesnę procedūrą, kad iš naujo sukonfigūruotumėte vietos nurodymą, jog jis nebenaudotų pakavimo vietos kaip galutinės siuntimo vietos, kai nustatytas bangos šablono automatinis krovimas į konteinerius.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.
1. Lauke **Darbo užsakymo tipas** pasirinkite *Pardavimo užsakymai*.
1. Pasirinkite vietos nurodymą, kurį naudojate automatiniam krovimui į konteinerius.
1. „FastTab“ įrankių juostoje **Vietos nurodymo veiksmai** pasirinkite **Redaguoti užklausą**.
1. Užklausų rengyklės dialogo lango skirtuke **Diapazonas** suraskite eilutę, kurios **Laukas** nustatytas į *Vietos profilį* ir patikrinkite, ar tos eilutės laukas **Kriterijai** nėra nustatytas į vietos profilį, kurio **Vietos tipas** yra *Pakavimas*. Pakoreguokite lauką **Kriterijai**, kad pataisytumėte galutinę padėjimo vietą.

Naudokite toliau pateiktą procedūrą, kad iš naujo išleistumėte krovinį ir sukurtumėte darbo ID su teisinga galutine siuntimo vieta.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Krovinio planavimo darbo sritis**.
1. Skyriuje **Kroviniai** raskite krovinį, kurį reikia išleisti.
1. Skyriaus **Kroviniai** įrankių juostoje pasirinkite **Išleidimas \> Išleidimas į sandėlį**, kad išleistumėte pasirinktą krovinį į sandėlį.
1. Pakartokite šią procedūrą kitiems kroviniams, jei reikia.
