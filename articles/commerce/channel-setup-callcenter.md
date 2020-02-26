---
title: Skambučių centro kanalo nustatymas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują skambučių centro kanalą.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6ec42ab920868f541eeac54556f4f24cb1efaa3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002455"
---
# <a name="set-up-a-call-center-channel"></a>Skambučių centro kanalo nustatymas


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują skambučių centro kanalą.

## <a name="overview"></a>Peržiūrėti

Programoje „Dynamics 365 Commerce“ skambučių centras yra mažmeninės prekybos kanalo tipas, kurį galima nustatyti programoje. Nustačius skambučių centro objektų kanalą, sistema leidžia susieti tam tikrus duomenis ir užsakymų apdorojimą pagal numatytuosius pardavimo užsakymus. Programoje „Commerce“ įmonė gali nurodyti keletą skambučių centro kanalų. 

Prieš kurdami naują skambučių centro kanalą, įsitikinkite, kad įvykdėte [Būtinosios kanalo nustatymo sąlygos](channels-prerequisites.md).

## <a name="create-and-configure-a-new-call-center-channel"></a>Naujo skambučių centro kanalo kūrimas ir konfigūravimas

Norėdami sukurti ir sukonfigūruoti naują skambučių centro kanalą, atlikite tolesnius veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Kanalai \> Skambučių centras \> Visi skambučių centrai**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Lauke **Pavadinimas** įveskite naujo kanalo pavadinimą.
1. Pasirinkite atitinkamą **Juridinis asmuo** iš išplečiamojo meniu.
1. Pasirinkite atitinkamą **Sandėlis** vieta iš išplečiamojo meniu.
1. Lauke **Numatytasis klientas** pateikite galiojantį numatytąjį klientą.
1. Lauke **El. paštu siunčiamo pranešimo šablonas** pateikite galiojantį el. siunčiamo pranešimo šabloną.
1. Pateikite **Kainos perrašymas** informacinį kodą. Atkreipkite dėmesį, kad pirmiausia gali reikti sukurti informacinį kodą.
1. Nurodykite **Sulaikymo kodas** informacinį kodą. Atkreipkite dėmesį, kad pirmiausia gali reikti sukurti informacinį kodą.
1. Nurodykite **Kreditas** informacinį kodą. Atkreipkite dėmesį, kad pirmiausia gali reikti sukurti informacinį kodą.
1. Pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas naujo skambučių centro kanalo kūrimas.

![Naujas skambučių centro kanalas](media/channel-setup-callcenter-1.png)

Toliau pateiktame vaizde parodytas skambučių centro kanalo pavyzdys.

![Skambučių centro kanalo pavyzdys](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Papildoma kanalų sąranka

Papildomos užduotys, reikalingos skambučių centro kanalo sąrankai, apima mokėjimo metodų ir pristatymo būdų nustatymą.

Toliau pateiktame paveiksle rodomi **Pristatymo būdai** ir **Mokėjimo metodai** nustatymo parinktys, esančios skirtuke **Nustatyti**.

![Papildomi skambučių centro kanalo nustatymo veiksmai](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Nustatyti mokėjimo būdus

Norėdami nustatyti kiekvieno mokėjimo tipo, palaikomo šiame kanale, mokėjimo metodus, atlikite toliau nurodytus veiksmus.

1. Veiksmų srityje pasirinkite skirtuką **Sąranka**, tada pasirinkite **Mokėjimo metodai**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Naršymo srityje pasirinkite pageidaujamą mokėjimo metodą.
1. Skyriuje **Bendri** nurodykite **Operacijos pavadinimas** ir konfigūruokite kitus pageidaujamus nustatymus.
1. Konfigūruokite visus papildomus parametrus, kurių reikia mokėjimo tipui.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas mokėjimas grynaisiais pinigais pavyzdys.

![Mokėjimo metodų pavyzdys](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Nustatyti pristatymo būdus

Galite peržiūrėti sukonfigūruotus pristatymo būdus pasirikdami **Pristatymo būdai** skirtuke **Nustatymas**, esančiame **Veiksmų sritis**.  

Norėdami pakeisti arba įtraukti pristatymo būdą, atlikite toliau nurodytus veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Atsargų valdymas \> Pristatymo būdai**.
1. Veiksmų srityje pasirinkite **Naujas**, kad sukurtumėte naują pristatymo režimą, arba pasirinkite esamą režimą.
1. Skyriuje **Mažmeninės prekybos kanalai** pasirinkite **Įtraukti eilutę**, kad galėtumėte įtraukti kanalą. Kanalų įtraukimas naudojant organizacijos mazgus, užuot įtraukus kiekvieną kanalą atskirai, gali racionalizuoti kanalų įtraukimą.

Toliau pateiktame vaizde parodytas pristatymo būdo pavyzdys.

![Nustatyti pristatymo būdus](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Būtinosios kanalo nustatymo sąlygos](channels-prerequisites.md)

[Skambučių centro pardavimo funkcijos](call-center-functionality.md)

[Skambučių centro užsakymo apdorojimo parinkčių nustatymas](set-up-order-processing-options.md)

[Skambučių centro katalogai](call-center-catalogs.md)

[Įspėjimų dėl apgaulės nustatymas ir jų naudojimas](set-up-fraud-alerts.md)

[Skambučių centrų tęstinumo programų nustatymas](set-up-continuity-program.md)
