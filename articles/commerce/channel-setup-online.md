---
title: Interneto kanalo nustatymas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują interneto kanalą.
author: samjarawan
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: f32872fcc27e2e74300c4f18dfa08d666e4ad8a8
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092117"
---
# <a name="set-up-an-online-channel"></a>Interneto kanalo nustatymas

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują interneto kanalą.

„Dynamics 365 Commerce“ palaiko kelis mažmeninės prekybos kanalus. Šie mažmeninės prekybos kanalai apima interneto parduotuves, skambučių centrus ir mažmeninės prekybos parduotuves (taip pat vadinamas fizinėmis parduotuvėmis). Internetinė parduotuvė suteikia klientams galimybę pirkti produktus internete, todėl klientai gali juos pirkti ne tik iš fizinės parduotuvės, bet ir iš internetinės parduotuvės.

Norėdami sukurti internetinę parduotuvę „Commerce“, pirmiausia turite sukurti interneto kanalą. Prieš kurdami naują interneto kanalą, įsitikinkite, kad įvykdėte [Būtinosios kanalo nustatymo sąlygos](channels-prerequisites.md).

Kad galėtumėte kurti naują svetainę, programoje „Commerce“ reikia sukurti bent vieną internetinę parduotuvę. Norėdami sužinoti daugiau, žr. [El. prekybos svetainės kūrimas](create-ecommerce-site.md).

## <a name="create-and-configure-a-new-online-channel"></a>Naujo interneto kanalo kūrimas ir konfigūravimas

Norėdami sukurti ir sukonfigūruoti naują interneto kanalą, atlikite tolesnius veiksmus.

1. Naršymo srityje eikite **Moduliai \>Kanalai \>Internetinės parduotuvės**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Lauke **Pavadinimas** įveskite naujo kanalo pavadinimą.
1. Išplečiamajame sąraše **Juridinis subjektas** įveskite atitinkamą juridinį subjektą.
1. Išplečiamajame sąraše **Sandėlis** įveskite atitinkamą sandėlį.
1. Lauke **Parduotuvės laiko juosta** pasirinkite atitinkamą laiko juostą.
1. Lauke **Valiuta** pasirinkite atitinkamą valiutą.
1. Lauke **Numatytasis klientas** pateikite galiojantį numatytąjį klientą.
1. Lauke **Kliento adresų knygelė** nurodykite galiojančią adresų knygelę.
1. Lauke **Funkcijų šablonas** pasirinkite funkcijų šabloną, jei taikoma.
1. Lauke **El. paštu siunčiamo pranešimo šablonas** pateikite galiojantį el. siunčiamo pranešimo šabloną.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas naujo interneto kanalo kūrimas.

![Naujas interneto kanalas.](media/channel-setup-online-1.png)

Toliau pateiktame vaizde parodytas interneto kanalo pavyzdys.

![Interneto kanalo pavyzdys.](media/channel-setup-online-2.png)

## <a name="assign-the-channel-to-a-commerce-scale-unit"></a>Priskirkite kanalą komercijos masto vienetui

Jūsų naujas kanalas turi būti priskirtas komercijos masto vienetui. Instrukcijas žr [Konfigūruokite kanalus, kad būtų naudojamas komercijos masto vienetas](../fin-ops-core/dev-itpro/deployment/initialize-retail-channels.md#configure-channels-to-use-commerce-scale-unit).

## <a name="set-up-languages"></a>Kalbų nustatymas

Jei jūsų el. prekybos svetainė palaikys kelias kalbas, išplėskite **Kalbos** skyrių ir prireikus pridėkite papildomų kalbų.

## <a name="set-up-payment-account"></a>Mokėjimo sąskaitos nustatymas

Iš skyriaus **Mokėjimo sąskaita** galite įtraukti trečiosios šalies mokėjimų teikėją. Informaciją, kaip nustatyti „Adyen“ mokėjimo jungtį, žr. [„Dynamics 365“ mokėjimo jungtis, skirta „Adyen“](./dev-itpro/adyen-connector.md).

## <a name="additional-channel-setup"></a>Papildoma kanalų sąranka

Papildomos užduotys, reikalingos interneto kanalo sąrankai, apima mokėjimo metodų, pristatymo būdų ir išpildymo grupių priskyrimo nustatymą.

Toliau pateiktame paveiksle rodomos sąrankos parinktys **Pristatymo būdai**, **Mokėjimo metodai** ir **Vykdymo grupių priskyrimas**, esančios skirtuke **Nustatyti**.

![Papildomi interneto kanalo nustatymo veiksmai.](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a>Nustatyti mokėjimo būdus

Norėdami nustatyti kiekvieno mokėjimo tipo, palaikomo šiame kanale, mokėjimo metodus, atlikite toliau nurodytus veiksmus.

1. Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Mokėjimo metodai**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Naršymo srityje pasirinkite pageidaujamą mokėjimo metodą.
1. Skyriuje **Bendri** nurodykite **Operacijos pavadinimas** ir konfigūruokite kitus pageidaujamus nustatymus.
1. Konfigūruokite visus papildomus parametrus, kurių reikia mokėjimo tipui.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas mokėjimas grynaisiais pinigais pavyzdys.

![Mokėjimo metodų pavyzdys.](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Nustatyti pristatymo būdus

Galite peržiūrėti sukonfigūruotus pristatymo būdus pasirikdami **Pristatymo būdai** skirtuke **Nustatymas**, esančiame **Veiksmų sritis**.  

Norėdami pakeisti arba įtraukti pristatymo būdą, atlikite toliau nurodytus veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Atsargų valdymas \> Pristatymo būdai**.
1. Veiksmų srityje pasirinkite **Naujas**, kad sukurtumėte naują pristatymo režimą, arba pasirinkite esamą režimą.
1. Skyriuje **Mažmeninės prekybos kanalai** pasirinkite **Įtraukti eilutę**, kad galėtumėte įtraukti kanalą. Kanalų įtraukimas naudojant organizacijos mazgus, užuot įtraukus kiekvieną kanalą atskirai, gali racionalizuoti kanalų įtraukimą.

Toliau pateiktame vaizde parodytas pristatymo būdo pavyzdys.

![Nustatyti pristatymo būdus.](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a>Vykdymo grupės priskyrimo nustatymas

Norėdami nustatyti vykdymo grupės priskyrimą, atlikite toliau nurodytus veiksmus.

1. Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Vykdymo grupės priskyrimas**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Išplečiamajame sąraše **Vykdymo grupė** pasirinkite vykdymo grupę.
1. Išplečiamajame sąraše **Aprašas** įveskite aprašą.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas vykdymo grupės priskyrimo sąrankos pavyzdys.

![Vykdymo grupės priskyrimo nustatymas.](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Kanalų apžvalga](channels-overview.md)

[Būtinosios kanalo nustatymo sąlygos](channels-prerequisites.md)

[Mažmeninės prekybos kanalo nustatymas](channel-setup-retail.md)

[Skambučių centro kanalo nustatymas](channel-setup-callcenter.md)

[„Dynamics 365“ mokėjimo jungtis, skirta sprendimui „Adyen“](./dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
