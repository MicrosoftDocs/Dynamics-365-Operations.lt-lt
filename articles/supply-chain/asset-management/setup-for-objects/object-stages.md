---
title: Produktų ciklo būsenos
description: Šioje temoje paaiškinamos turto ciklo būsenos ir ciklo modeliai modulyje „Turto valdymas“.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55139c6458e569b15518f0f11f1c12c3a26cae2f26c6a2046a7ebdc1277cb144
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722468"
---
# <a name="asset-lifecycle-states"></a>Produktų ciklo būsenos

[!include [banner](../../includes/banner.md)]

 

Šioje temoje paaiškinamos turto ciklo būsenos ir ciklo modeliai modulyje „Turto valdymas“. Turto ciklo būsenos naudojamos apibrėžti, ar turtas aktyvus, ar neaktyvus. Pavyzdžiui, galite sukonfigūruoti tokias turto ciklo būsenas kaip **Sukurta**, **Aktyvi** ir **Nutraukta**.

> [!NOTE]
> - Užklausų ciklo būsenos yra susietos su turto ciklo būsenomis. Todėl pakeitus užklausos būseną į naują užklausos ciklo būseną, turto, susieto su šia užklausa, būsena keičiama į naują turto ciklo būseną. Pavyzdžiui, jei užklausos ciklo būsena keičiama į **Gaunama**, susieto turto ciklo būsena keičiama į ciklo būseną, kuri yra pasirinkta lauke **Gaunamo turto ciklo būsena**, kuris yra puslapio **Turto ciklo būsenos modeliai** „FastTab“ skirtuke **Turto ciklo būsena**. 


Turto ciklo būsenos gali būti nustatomos turto ciklo modeliuose, kuriuose galite apibrėžti reikiamas įvairių turto tipų ciklo būsenas. Pirmiausia nustatote ciklo būsenas. Tada sukuriate ciklo modelį ir pasirenkate jo ciklo būsenas.

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turtas** \> **Ciklo būsenos**.
2. Pasirinkite **Naujas**, kad sukurtumėte naują gyvavimo stadiją.
3. Lauke **Ciklo būsena** įveskite ciklo būsenos stadijos ID.
4. Lauke **Pavadinimas** įveskite aprašomąjį pavadinimą.

    Lauke **Ciklo modeliai** rodomas turto ciklo modelių, kurie naudoja turto ciklo būseną, skaičius.

5. Nustatykite parinktį **Aktyvus** kaip **Taip**, jei ši ciklo būsena turėtų būti aktyvios ciklo būsenos (kitaip tariant, jei darbo užsakymai gali būti kuriami su turtu, esančiu šios ciklo būsenos).
6. Nustatykite parinktį **Naikinti atviras kalendoriaus eilutes** kaip **Taip**, jei atviros turto kalendoriaus eilutės, turinčios turto ciklo būsena **Sukurta**, turėtų būti naikinamos, kai yra šios ciklo būsenos. Šis parametras yra naudingas, jei norite išvalyti bet kokius atvirus priežiūros grafikus, kurie nebeatitinka turto (pvz., jei turtas nebeaktyvus).

> [!NOTE]
> Turto ciklo būsenos, turto ciklo modeliai ir turto tipai yra susieti. Jie yra naudojami taip pat, kaip ir darbo užsakymo ciklo būsenos, darbo užsakymo ciklo modeliai ir darbo užsakymų tipai. 


Sukūrę reikiamas turto ciklo būsenas, galite nustatyti ciklo būsenas turto ciklo modeliuose.

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **turtas** \> **ciklo modeliai**.
2. Pasirinkite **Naujas**, kad sukurtumėte naują turto ciklo modelį.
3. Lauke **Ciklo būsena** įveskite ciklo modelio ID.
4. Lauke **Pavadinimas** įveskite aprašomąjį pavadinimą.

    Lauke **Ciklo būsenos** rodomas turto ciklo būsenų, kurios yra pasirinktos turto ciklo modelyje, skaičius. Lauke **Turto tipai** rodomas ciklo modelį naudojančių turto tipų skaičius.

5. „FastTab“ skirtuke **Ciklo būsenos** pasirinkite turto ciklo būsenas, kurias reikėtų įtraukti į turto ciklo modelį:

    - Norėdami modeliui naudoti ciklo būseną, pasirinkite ją **Likusios ciklo būsenos** skyriuje, o tada pasirinkite dešinės rodyklės mygtuką ![Rodyklė dešinėn.](media/15-setup-for-objects.png) jos perkėlimui į **Pasirinktos ciklo būsenos** skyrių.
    - Norėdami naudoti visas pasiekiamas ciklo būsenas modelyje, pasirinkite mygtuką **Visos pasiekiamos ciklo būsenos**![Visos pasiekiamos ciklo būsenos.](media/20-setup-for-objects.png). Visos būsenos perkeliamos į skyrių **Pasirinktos ciklo būsenos**.
    - Norėdami pašalinti ciklo būseną iš modelio, pasirinkite ją **pasirinktos ciklo būsenos** skyriuje, o tada pasirinkite kairės rodyklės mygtuką ![Rodyklė kairėn.](media/16-setup-for-objects.png) jos perkėlimui į **Likusios ciklo būsenos** skyrių.

6. Pasirinkite **Ciklo būsenos naujinimai**, kad apibrėžtume turto ciklo būsenas, kurios gali eiti po pasirinktos ciklo būsenos.
7. Galite naudoti „FastTab“ skirtuką **Turto būsena**, jei tvarkote turtą, kurį gaunate taisyti. Skyriuje **Gaunama / siunčiama** galite pasirinkti turto ciklo būsenas, kad nurodytumėte darbo eigą, susijusią su turtu, kurį gavote taisyti. Jei siūlote paskolos turtą klientams arba padaliniams, skyriuje **Paskola** galite pasirinkti paskolos turto ciklo būsenas.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]