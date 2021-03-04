---
title: Naujo dokumento vartotojo sąsaja funkcijoje Verslo dokumentų valdymas
description: Šioje temoje pateikiama informacija apie tai, kaip naudoti naujo dokumento vartotojo sąsają (UI) elektroninių ataskaitų (ER) sistemos funkcijoje Verslo dokumentų valdymas.
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2cb6e0da4af07b9b8486bf1e5bda29523cbd08e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681357"
---
# <a name="new-document-user-interface-in-business-document-management"></a>Naujo dokumento vartotojo sąsaja funkcijoje Verslo dokumentų valdymas

[!include [banner](../includes/banner.md)]

Verslo dokumentų valdymas leidžia verslo vartotojams redaguoti verslo dokumentų šablonus naudojant „Microsoft 365 service“ paslaugą arba atitinkamą „Microsoft Office“ darbalaukio programą. Redagavimas gali būti dizaino keitimai arba nauji diegimai arba vartotojai gali įtraukti vietos rezervavimo ženklų, kad galėtų įtraukti papildomų duomenų, nekeisdami šaltinio kodo. Norėdami gauti daugiau informacijos apie tai, kaip naudotis funkcija Verslo dokumentų valdymas, žr. [Funkcijos Verslo dokumentų valdymas apžvalga](er-business-document-management.md).

Naujo dokumento vartotojo sąsaja (UI) yra aiškesnė ir patogesnė naudoti. Srityje **Verslo dokumentas** rodomi tik tie šablonai, kurie yra pasiekiami dabartiniam tiekėjui.

Paspaudę mygtuką **Naujas dokumentas**, vartotojai gali kurti ir redaguoti šabloną elektroninių ataskaitų (ER) formato konfigūracijoje, kurią pateikia kitas teikėjas. Šioje temoje pateikiamame pavyzdyje teikėjas yra „Microsoft“.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Naujo dokumento vartotojo sąsajos įjungimas funkcijoje Verslo dokumentų valdymas

Norėdami pradėti naudoti naujo dokumento vartotojo sąsają funkcijoje Verslo dokumentų valdymas, turite įjungti funkciją **Į „Office“ panaši vartotojo sąsaja funkcijoje Verslo dokumentų valdymas** darbo srityje **Funkcijų valdymas**.

Atlikite tolesnius veiksmus, norėdami įjungti šią funkciją visiems juridiniams subjektams.

1. Darbo srityje **Funkcijų valdymas** skirtuke **Nauja** sąraše pasirinkite funkciją **Į „Office“ panaši vartotojo sąsaja funkcijoje Verslo dokumentų valdymas**.
2. Pasirinkite **Įjungti dabar**, kad įjungtumėte pasirinktą funkciją.
3. Norėdami pasiekti naują funkciją, atnaujinkite puslapį.

### <a name="edit-templates-that-are-owned-by-other-providers"></a>Šablonų, priklausančių kitiems teikėjams, redagavimas

1. Darbo srityje **Verslo dokumentų valdymas** pasirinkite **Naujas dokumentas**.

    ![Darbo sritis Verslo dokumentų valdymas](./media/BDM_overview_new_template1.png)

2. Dialogo lange pasirinkite dokumentą, kurį norite naudoti kaip šabloną, tada pasirinkite **Kurti dokumentą**.

    ![Verslo dokumentų dialogo langas](./media/BDM_overview_new_template2.png)

3. Naujo dialogo lango lauke **Pavadinimas** pakeiskite pavadinimą į norimą pavadinimą. Pavadinimo tekstas naudojamas automatiškai sukurtai naujai ER formato konfigūracijai pavadinti. Šios konfigūracijos (**Kliento laisvos formos sąskaitos-faktūros ataskaitos (GER) kopija**) juodraščio versijoje bus suredaguotas šablonas ir ji bus naudojama vykdant šį ER formatą, skirtą dabartiniam vartotojui. Originalus šablonas iš pagrindinio ER formato konfigūracijos bus naudojamas visiems kitiems vartotojams skirtam ER formatui vykdyti.
4. Lauke **Pavadinimas** pakeiskite redaguojamo šablono, kuris bus automatiškai sukurtas, pirmo pataisymo pavadinimą.
5. Lauke **Komentaras** atnaujinkite redaguojamo šablono, kuris bus automatiškai sukurtas, pataisymo pastabas.
6. Pasirinkite **Gerai**, kad patvirtintumėte redagavimo proceso pradžią.

    ![Dokumento kūrimo dialogo langas](./media/BDM_overview_new_template3.png)

Paspaudus mygtuką **Naujas dokumentas**, sukuriamas ir redaguojamas šablonas ER formato konfigūracijoje, kurią pateikia kitas teikėjas. Šiame pavyzdyje teikėjas yra „Microsoft“. Pasirinkę **Naujas dokumentas**, peržiūrėsite visus šablonus, priklausančius dabartiniam ir kitiems teikėjams. Pasirinktas šablonas atidaromas ir jį galima redaguoti. Redaguotas šablonas bus išsaugotas naujoje automatiškai sugeneruotoje ER formato konfigūracijoje.

Daugiau informacijos žr. [Verslo dokumentų valdymo apžvalga](er-business-document-management.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]