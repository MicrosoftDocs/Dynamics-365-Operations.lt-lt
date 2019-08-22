---
title: Produktų ciklo būsenos
description: Šioje temoje paaiškinamos turto ciklo būsenos ir ciklo modeliai modulyje „Turto valdymas“.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dc72c61ed4dbb04122c6859123307dc79f2b233
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783451"
---
# <a name="asset-lifecycle-states"></a>Produktų ciklo būsenos

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Šioje temoje paaiškinamos turto ciklo būsenos ir ciklo modeliai modulyje „Turto valdymas“. Turto ciklo būsenos naudojamos apibrėžti, ar turtas aktyvus, ar neaktyvus. Pavyzdžiui, galite sukonfigūruoti tokias turto ciklo būsenas kaip **Sukurta**, **Aktyvi** ir **Nutraukta**.

> [!NOTE]
> - Užklausų ciklo būsenos yra susietos su turto ciklo būsenomis. Todėl pakeitus užklausos būseną į naują užklausos ciklo būseną, turto, susieto su šia užklausa, būsena keičiama į naują turto ciklo būseną. Pavyzdžiui, jei užklausos ciklo būsena keičiama į **Gaunama**, susieto turto ciklo būsena keičiama į ciklo būseną, kuri yra pasirinkta lauke **Gaunamo turto ciklo būsena**, kuris yra puslapio **Turto ciklo būsenos modeliai** „FastTab“ skirtuke **Turto ciklo būsena**. 


Turto ciklo būsenos gali būti nustatomos turto ciklo modeliuose, kuriuose galite apibrėžti reikiamas įvairių turto tipų ciklo būsenas. Pirmiausia nustatote ciklo būsenas. Tada sukuriate ciklo modelį ir pasirenkate jo ciklo būsenas.

1. Pasirinkite **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.
2. Pasirinkite **New**, kad sukurtumėte naują gyvavimo stadiją.
3. Lauke **Ciklo būsena** įveskite ciklo būsenos stadijos ID.
4. Lauke **Name** įveskite aprašomąjį pavadinimą.

    Lauke **Ciklo modeliai** rodomas turto ciklo modelių, kurie naudoja turto ciklo būseną, skaičius.

5. Nustatykite parinktį **Aktyvus** kaip **Taip**, jei ši ciklo būsena turėtų būti aktyvios ciklo būsenos (kitaip tariant, jei darbo užsakymai gali būti kuriami su turtu, esančiu šios ciklo būsenos).
6. Nustatykite parinktį **Naikinti atviras kalendoriaus eilutes** kaip **Taip**, jei atviros turto kalendoriaus eilutės, turinčios turto ciklo būsena **Sukurta**, turėtų būti naikinamos, kai yra šios ciklo būsenos. Šis parametras yra naudingas, jei norite išvalyti bet kokius atvirus priežiūros grafikus, kurie nebeatitinka turto (pvz., jei turtas nebeaktyvus).

> [!NOTE]
> Turto ciklo būsenos, turto ciklo modeliai ir turto tipai yra susieti. Jie yra naudojami taip pat, kaip ir darbo užsakymo ciklo būsenos, darbo užsakymo ciklo modeliai ir darbo užsakymų tipai. 


Sukūrę reikiamas turto ciklo būsenas, galite nustatyti ciklo būsenas turto ciklo modeliuose.

1. Pasirinkite **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.
2. Pasirinkite **New**, kad sukurtumėte naują turto ciklo modelį.
3. Lauke **Ciklo būsena** įveskite ciklo modelio ID.
4. Lauke **Name** įveskite aprašomąjį pavadinimą.

    Lauke **Ciklo būsenos** rodomas turto ciklo būsenų, kurios yra pasirinktos turto ciklo modelyje, skaičius. Lauke **Turto tipai** rodomas ciklo modelį naudojančių turto tipų skaičius.

5. „FastTab“ skirtuke **Ciklo būsenos** pasirinkite turto ciklo būsenas, kurias reikėtų įtraukti į turto ciklo modelį:

    - Norėdami naudoti modelio ciklo būseną, pasirinkite ją skyriuje **Lifecycle states remaining**, tada pasirinkite dešiniosios rodyklės mygtuką ![Dešinioji rodyklė](media/15-setup-for-objects.png), kad perkeltumėte ją į skyrių **Lifecycle states selected**.
    - Norėdami naudoti visas pasiekiamas ciklo būsenas modelyje, pasirinkite mygtuką **All available lifecycle states**![Visos pasiekiamos ciklo būsenos](media/20-setup-for-objects.png). Visos būsenos perkeliamos į skyrių **Lifecycle states selected**.
    - Norėdami pašalinti ciklo būseną iš modelio, pasirinkite ją skyriuje **lifecycle states selected**, tada pasirinkite kairiosios rodyklės mygtuką ![Kairioji rodyklė](media/16-setup-for-objects.png), kad perkeltumėte ją į skyrių **Lifecycle states remaining**.

6. Pasirinkite **Lifecycle state updates**, kad apibrėžtume turto ciklo būsenas, kurios gali eiti po pasirinktos ciklo būsenos.
7. Galite naudoti „FastTab“ skirtuką **Asset state**, jei tvarkote turtą, kurį gaunate taisyti. Skyriuje **Gaunama / siunčiama** galite pasirinkti turto ciklo būsenas, kad nurodytumėte darbo eigą, susijusią su turtu, kurį gavote taisyti. Jei siūlote paskolos turtą klientams arba padaliniams, skyriuje **Paskola** galite pasirinkti paskolos turto ciklo būsenas.
