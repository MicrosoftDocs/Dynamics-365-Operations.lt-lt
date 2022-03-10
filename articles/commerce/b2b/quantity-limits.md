---
title: Nustatykite produkto kiekio apribojimus B2B el. komercijos saitams
description: Šioje temoje aprašoma, kaip nustatyti produkto kiekio apribojimus verslo su verslu (B2B) el. komercijos saitams.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2c8adaad2afee3b735c69a501d7949a807f4e770
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323385"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a>Nustatykite produkto kiekio apribojimus B2B el. komercijos saitams

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip nustatyti produkto kiekio apribojimus verslo su verslu (B2B) el. komercijos saitams.

Didžioji dalis produktų turi matavimo vienetą, kuris nustato jų grupes. Grupavimas paveikia tai, kaip produktai gali būti parduoti. Kai kurie produktai gali turėti papildomą grupavimą kiekiams. Šis grupavimas nustato, ar produktai gali būti parduoti kaip atskiri vienetai ar kartu ir ar esama minimalaus ar maksimalaus kiekio apribojimo, kurio būtina laikytis.

Kiekio apribojimo funkcija užtikrina, kad minimalus, maksimalus, keletas ir standartinis kiekis, kuris yra konfigūruojamas „Microsoft Dynamics 365 Commerce“ (numatytuose užsakymo nustatymuose ar „Commerce“ vietos kūrimo saito nustatymuose) yra taikomas kliento užsakymams, kurie yra daromi el. komercijos saite. Produkto kiekio apribojimai šiuo metu nėra palaikomi prekybos taške ir skambučių centruose.

Daugelis mažmeninės veiklos prekybininkų suteikia galimybę klientų užsakymams (taip pat žinomiems kaip specialūs užsakymai) atitikti įvairius produktus ir įgyvendinti reikalavimus. Toliau nurodomi įprasti scenarijai.

- Klientas nori konkrečių variantų produktų, kurių daugelis turi būti parduodami kaip keli.
- Klientas nori atsiimti produktus parduotuvėje arba vietoje, kuri nėra parduotuvė arba vieta, kurioje klientas tuos produktus nusipirko. Nepaisant to, pakavimo standartai parduotuvėms skiriasi nuo pakavimo standartų interneto prekybos platinimui.
- Klientas nori pirkti limituoto leidimo produktą, kuris turėtų maksimalų kiekio apribojimą prekėms, kurias galima įsigyti.

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a>Įjunkite numatytą užsakymo nustatymų funkciją „Commerce“ būstinėje

Prieš tai, kai galite nustatyti produkto kiekio apribojimus, numatyta užsakymo nustatymų funkcija turi būti įjungta „Commerce“ būstinėje.

Norėdami įjungti numatytą užsakymo nustatymų funkciją, atlikite šiuos veiksmus.

1. Eikite į **Sistemos administravimas \> Darbo sritys \> Funkcijų valdymas**.
1. Raskite ir pasirinkite **Palaikyti saitą ir numatytus užsakymo nustatymus tinkintame užsakyme** funkciją.
1. Dešiniosios juostos apačioje rinkitės **Įjungti dabar**. 

## <a name="define-quantity-settings"></a>Nustatykite kiekio nustatymus 

Galite nustatyti kiekio nustatymus **Numatyti užsakymo nustatymai** puslapyje.

Norėdami nustatyti kiekio nustatymus, atlikite šiuos veiksmus. 

1. Eikite į produktą **Mažmeninė prekyba ir komercija\> Produktai ir kategorijos \> Išleisti produktai pagal kategorijas**.
1. Rinkitės išleistą produktą.
1. Veiksmų juostoje **Valdyti inventorių** skirtuke, **Užsakymo nustatymai** grupėje, rinkitės **Numatyto užsakymo nustatymai**. 
1. Puslapyje **Numatyto užsakymo nustatymai**, „FastTabe“ **Prekybos užsakymas** skyriuje **Prekybos kiekis**, nustatykite produkto pardavimo kiekius:

    - **Keli** – Kiekis, kurį produktas gali būti paverstas į kelis.
    - **Minimalus užsakymo kiekis** – Minimalus produktų skaičius, kuris turi būti įsigytas.
    - **Maksimalus užsakymo kiekis** – Maksimalus produktų skaičius, kurį galima įsigyti.
    - **Standartinis užsakymo kiekis** – Numatytas kiekis, kuris yra automatiškai įvedamas, kai produktas yra pasirinktas.

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a>Įjunkite B2B užsakymo kiekių apribojimų funkciją „Commerce“ saito kūrimo įrankyje

Norėdami įjungti B2B užsakymo kiekių apribojimų funkciją „Commerce“ saito kūrimo įrankyje, atlikite šiuos žingsnius.

1. Eikite į **Saito nustatymai \> Plėtiniai**
1. Skyriuje **Įjungti užsakymo kiekio apribojimus**, rinkitės **Įjungti B2B klientams** iškrentančiame meniu. 

> [!NOTE] 
> Naujinti saito kūrimo įrankio nustatymai įsigalioja po to, kai app.settings.json failas buvo atnaujintas. Dėl daugiau informacijos, žr. [SDK ir modulio bibliotekos naujinimai](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="additional-resources"></a>Papildomi ištekliai

[B2B el. prekybos svetainės nustatymas](set-up-b2b-site.md)

[Valdyti B2B verslo partnerius naudojant klientų hierarchijas](partners-customer-hierarchies.md)

[Verslo partnerio vartotojų valdymas B2B el. prekybos svetainėse](manage-b2b-users.md)

[Konfigūruoti kliento sąskaitos mokėjimo metodą B2B el. komercijos saitams](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
