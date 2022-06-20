---
title: Apdoroti atsietus grąžinimus su Dynamics 365 Commerce Adyen mokėjimo jungtimi
description: Šiame straipsnyje aprašoma, kaip veikia atsieti grąžinimai, Microsoft Dynamics kai naudojama "365" mokėjimo jungtis Adyen.
author: BrianShook
ms.date: 10/07/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 634b30de7adbfb0c316fe14456581ea8eb89d070
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885202"
---
# <a name="process-unlinked-refunds-with-the-dynamics-365-commerce-payment-connector-for-adyen"></a>Apdoroti atsietus grąžinimus su Dynamics 365 Commerce Adyen mokėjimo jungtimi

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip veikia atsieti grąžinimai, [Microsoft Dynamics kai naudojama "365" mokėjimo jungtis Adyen](adyen-connector.md). Taip pat apžvelgiama galimybė apdoroti grąžinimą pagal naują mokėjimo metodą pardavimo vietoje (POS) arba skambučių centre.

"Dynamics 365" mokėjimo jungtis, skirta Adyen, palaiko galimybę apdoroti grąžinimus naudojant kitą mokėjimo būdą, nei buvo naudojama pradinės operacijos metu. Nors mes rekomenduojame naudoti [susietus grąžinimus](linked-refunds.md) siekiant apdoroti grąžinimą pagal pateiktą kilmės mokėjimo būdą, kai kuriuose scenarijuose reikalingas grąžinimas kitokiu metodu. Pavyzdžiui, pradinio mokėjimo metu naudota kortelė gali būti pasibaigusi arba būti pamesta, arba ją galbūt atšaukė vartotojas.

## <a name="prerequisites"></a>Būtinieji komponentai

Kad "Dynamics 365" Adyen mokėjimo jungtis galėtų apdoroti nesusietas lėšas, turi būti įvykdytos šios būtinosios sąlygos:

- Nustatyti [mokėjimo metodai](../payment-methods.md).
- Nustatyti [daugiakanalius mokėjimus](../omni-channel-payments.md).

## <a name="additional-configuration"></a>Papildoma konfigūracija

„Dynamics 365“ mokėjimo jungtis, skirta „Adyen“, pateikia parengtą naudoti kiekvieno čia aprašyto palaikomo grąžinimo scenarijaus įdiegtį, kuri apibūdinama sekančiame skyriuje. Klientai, kurie nenaudoja "Dynamics 365" mokėjimo jungties, skirtos Adyen, įdiegties, nepanaudodami "Dynamics 365" mokėjimo jungties, turi nustatyti jungtį, palaikančią kredito kortelių atpažinimo ženklą.

## <a name="supported-refund-scenarios"></a>Palaikomi grąžinimo scenarijai

Dynamics 365 Commerce palaiko anksčiau aprobuotų ir patvirtintų operacijų grąžinimus. Grąžinimą gali sudaryti arba pilnas grąžinimas, arba dalinis operacijos grąžinimas. Grąžinimai negali viršyti visos pradinio mokėjimo autorizavimo sumos. Atsieti grąžinimai palaikomi tik EKA ir skambučių centre.

## <a name="enable-unlinked-refunds-functionality"></a>Įjungti atsietų grąžinimų funkciją

Norėdami įgalinti atsietų grąžinimų funkcionalumą „Commerce” būstinėje, atlikite šiuos žingsnius.

1. Eikite į **Mažmeninė prekyba ir prekyba \> „Headquarters“ sąranka \> Parametrai \> „Commerce“ bendrinami parametrai**.
1. Tada skirtuke **Integruotas kanalas** nustatykite parinkties **Naudoti integruoto kanalo mokėjimus** parinktį į **Taip**.

### <a name="supported-payment-method-variants"></a>Palaikomi mokėjimo būdo variantai

Šie atsiskaitymo būdų variantai palaiko atsietus grąžinimus:

- Kortelės
- Piniginė

Ne visi mokėjimo būdo variantai palaiko atsietus grąžinimus. Toliau esančioje lentelėje pateikiamas bendrųjų mokėjimo būdų sąrašas ir parodomas kiekvieno metodo palaikymo galimybės susietiems ir atsietiems grąžinimams.

| Mokėjimo būdas        | Susietas grąžinimas | Atsietas grąžinimas |
|-----------------------|:-------------:|:---------------:|
| amexcommercial        | Taip           | Taip             |
| amexconsumer          | Taip           | Taip             |
| amexcorporate         | Taip           | Taip             |
| amexdebit             | Taip           | Taip             |
| amexprepaid           | Taip           | Taip             |
| amexprepaidreloadable | Taip           | Taip             |
| amexsmallbusiness     | Taip           | Taip             |
| aptikti              | Taip           | Taip             |
| maestro               | Taip           | Taip             |
| maestrouk             | Taip           | Taip             |
| mc                    | Taip           | Taip             |
| mcalphabankbonus      | Taip           | Taip             |
| mcprepaidanonymous    | Taip           | Taip             |
| visa                  | Taip           | Taip             |
| visaalphabankbonus    | Taip           | Taip             |
| visacheckout          | Taip           | Taip             |
| visadankort           | Taip           | Taip             |
| visahipotecario       | Taip           | Taip             |
| visasaraivacard       | Taip           | Taip             |
| vpay                  | Taip           | Taip             |
| givex                 | **Ne**        | Taip             |
| svs                   | **Ne**        | Taip             |
| cup                   | Taip           | Taip             |
| Diners                | Taip           | Taip             |
| interac               | **Ne**        | Taip             |
| jcb                   | Taip           | Taip             |
| jcb_applepay          | Taip           | Taip             |
| unionpay              | Taip           | Taip             |

### <a name="process-an-unlinked-refund-in-pos"></a>Apdoroti atsietą grąžinimą per EKA

Klientas grąžina prekę EKA kasininkui per leidžiamą grąžinimo laikotarpį ir turi galiojantį kvitą. Apdorojant grąžinimo procesą, **Grąžinimo mokėjimo** dialogo lange yra parinktis **Pasirinkti mokėjimo būdą**. Kasininkas gali pasirinkti mokėjimo metodą iš palaikomų mokėjimo grąžinimo metodų (kortele ir pinigais).

### <a name="process-an-unlinked-refund-in-call-center"></a>Apdoroti atsietą grąžinimą per skambučių centrą

Kai atsietas grąžinimas apdorojamas pagal skambučių centro užsakymą, skambučių centro darbuotojas pasirenka mokėjimo būdą, kuris skiriasi nuo pirminio metodo. Tada darbuotojas raginamas gauti administratoriaus nepaisymo asmens identifikavimo numerį (PIN). Kad būtų galima apdoroti kitą grąžinimo mokėjimo būdą, reikalingas PIN kodas.

#### <a name="set-up-an-administrator-override-pin-for-call-center"></a>Nustatyti skambučių centro administratoriaus nepaisymo PIN kodą.

Norėdami nustatyti administratoriaus nepaisymo skambučių centro PIN kodą "Commerce" skyriuje, atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir Prekyba \> Kanalo nustatymas \> Skambučių centro nustatymas** arba ieškokite "Nepaisyti leidimų".
1. Pasirinkite vaidmenį, kuriam bus suteikti atsieti grąžinimo apdorojimo leidimai.
1. „FastTab“ skirtuke **Grąžinimai** parinktyje **Leisti alternatyvų mokėjimą** nustatykite į **Taip**.

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365 Payment Connector“, skirta sprendimui „Adyen“](adyen-connector.md)

[Susietas anksčiau patvirtintų ir patvirtintų operacijų grąžinimas](linked-refunds.md)
