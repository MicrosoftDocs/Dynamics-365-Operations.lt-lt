---
title: Dalinis transportuojamo krovinio siuntimas
description: Šioje temoje paaiškinama, kaip galima siųsti krovinio dalį ir atidėti krovinio pajėgumo planavimą.
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 179a784f1f02ed0840ba5219c350e274272b59eb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818949"
---
# <a name="partial-shipment-of-a-transport-load"></a>Dalinis transportuojamo krovinio siuntimas

[!include[banner](../includes/banner.md)]

Nustatę dalinį krovinių siuntimą, galite tvarkyti krovinius, kai pajėgumo negalima nustatyti, kol visos pardavimo eilutės nėra įtrauktos į krovinį. Tokiu atveju procesą galima baigti, kai žinomas tikslus padėklų skaičius. Todėl jūs neturite nuspręsti, kurie padėklai bus priskirti tam tikriems kroviniams iki to momento, kai krovinys bus faktiškai iškrautas iš etapais suskirstytų atsargų.

Ši funkcija suteikia alternatyvą griežtesnei struktūrai, kurią naudojant turite nustatyti, kurie padėklai bus priskirti tam tikriems kroviniams, prieš sukuriant išrinkimo arba krovimo darbą. Naudojant šią funkciją vartotojai gali konfigūruoti atskirus krovinių dalinio siuntimo patvirtinimą. Tada gali būti vykdomi tų krovinių krovimo procesai. Todėl transportavimo planavimo padalinys gali planuoti krovinius neturėdamas atsižvelgti į atskirų krovinių pajėgumą.

Pakrovimo metu darbuotojai gali nurodyti naują transportuojamą krovinį, į kurį galima pakrauti padėklą. Taip pat jie gali nurodyti esamą transportuojamą krovinį. Šie duomenys gali būti įrašomi naudojant mobilųjį įrenginį. Todėl keli sandėlio darbuotojai gali įkelti atsargų iš tų pačių krovinių ar iš kitų krovinių į tą patį sunkvežimį. Tada krovinius galima visiškai arba iš dalies išsiųsti.

> [!NOTE] 
> Norint įkelti atsargas iš krovinio į konkrečią transporto priemonę ir iš dalies išsiųsti krovinį, reikia sugeneruoti darbą naudojant darbo šablono pakrovimo klasę. Įprastas paėmimo darbas, kurio tipas **Paėmimas**, negali būti įkeltas į transporto priemonę, pvz., sunkvežimį.

## <a name="set-up-transport-loads-for-partial-shipment"></a>Transportuojamų krovinių dalinio siuntimo nustatymas

Transportuojamų krovinių dalinio siuntimo nustatymą sudaro dvi toliau nurodytos procedūros.

### <a name="set-the-loading-strategy"></a>Krovimo strategijos nustatymas

Turite įjungti dalinį krovimą nustatydami krovimo strategiją. Sukūrę krovinį galite nustatyti krovimo strategiją.

1. Pasirinkite **Sandėlio valdymas** \> **Kroviniai** \> **Visi kroviniai**.
2. Pasirinkite krovinį, tada spustelėkite **Antraštė**.
3. Lauke **Krovimo strategija** pasirinkite **Leidžiamas dalinis krovinių siuntimas**.

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a>Transporto priemonės krovimo meniu elemento kūrimas

Turite sukurti naują meniu elementą, kad būtų galima pakrauti transporto priemones. Transporto priemonė suteikia galimybę grupuoti darbo eilutes iš vieno krovinio arba kelių krovinių. Visas į transporto priemonę pakrautas krovinys gali būti išsiųstas naudojant mobilųjį skaitytuvą.

1. Pasirinkite **Sandėlio valdymas** \> **Sąranka** \> **Mobilusis įrenginys** \> **Mobiliojo įrenginio meniu elementai**.
2. Pasirinkite **Naujas**, tada lauke **Būdas** pasirinkite **Darbas**.
3. Nustatykite pasirinkties **Naudoti esamą darbą** padėtį **Taip**.
4. Skirtuko **Bendra** lauke **Nukreipė** pasirinkite **Transportuojamų krovinių krovimas**.
5. Norėdami įjungti siuntos patvirtinimą mobiliajame skaitytuve, lauke **Leidžiamas siuntų patvirtinimo tipas** pasirinkite **Transportuojamas krovinys**.

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a>Transportuojamo krovinio siuntimo patvirtinimas iš kliento

Šis sąranka suteikia galimybę patvirtinti transportuojamą krovinio, kuris apima visą krovinį arba iš dalies pakrautą krovinį, siuntimą.

1. Pasirinkite **Sandėlio valdymas** \> **Kroviniai** \> **Transportuojami kroviniai**.
2. Veiksmų srities skirtuko **Siuntimas ir gavimas** grupėje **Patvirtinimas** spustelėkite **Transportas**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]