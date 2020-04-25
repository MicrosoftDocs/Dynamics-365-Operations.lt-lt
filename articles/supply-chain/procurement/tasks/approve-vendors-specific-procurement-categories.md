---
title: Konkrečių įsigijimo kategorijų tiekėjų tvirtinimas
description: Šioje temoje aiškinama, kaip patvirtinti konkrečių įsigijimo kategorijų Dynamics 365 Supply Chain Management tiekėjus.
author: mkirknel
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e53102d732e9befcaca183adfd2a756c12e0162b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204935"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>Konkrečių įsigijimo kategorijų tiekėjų tvirtinimas

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip patvirtinti konkrečių įsigijimo kategorijų Dynamics 365 Supply Chain Management tiekėjus. Sukūrus pirkimo paraišką, gali reikėti pasirinkti patvirtintą arba pageidaujamą tiekėją, atsižvelgiant į tai, kaip nustatytos pirkimo strategijos. Šioje procedūroje parodoma, kaip nurodyti, kad konkrečios įsigijimo kategorijos tiekėjas yra patvirtintas arba pageidaujamas. Šią užduotį paprastai atlieka pirkimų profesionalai. Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF.

1. Naršymo srityje eikite į **Moduliai > Įsigijimas ir išteklių paskirstymas > Tiekėjai > Visi tiekėjai**.
2. Pasirinkite tiekėją, kurį norite nustatyti kaip patvirtintą arba pageidaujamą kategorijos tiekėją.
3. Veiksmų srityje spustelėkite **Bendra**.
4. Pažymėkite **Kategorijos**.
5. Pažymėkite **Įtraukti kategoriją**.
6. Lauke **Kategorija** pažymėkite **BIURO IR STALO PRIEDAI (BIURO IR STALO PRIEDAI)**.
7. Lauke **Tiekėjų kategorijos būsena** pažymėkite **Pageidaujama**. Galima nurodyti daugiau nei vieną pageidaujamą kategorijos tiekėją.  
8. Pasirinkite **Įrašyti**.
9. Naršymo srityje eikite į **Moduliai > Įsigijimas ir išteklių paskirstymas > Įsigijimo kategorijos**.
10. Medyje pažymėkite **KORP. ĮSIGIJIMO KATEGORIJOS\BIURO IR STALO PRIEDAI**.
11. Išplėskite skyrių **Tiekėjai**. Patikrinkite, ar jūsų pasirinktas tiekėjas rodomas kaip pageidaujamas kategorijos Biuro ir stalo reikmenys tiekėjas. Jei vykdote šią procedūrą kaip užduoties vadovą, gali reikėti pažymėti mygtuką **Atrakinti**, kad galėtumėte slinkti žemyn tiekėjų sąrašu.  Šiame puslapyje taip pat galima įtraukti pageidaujamų ir patvirtintų tiekėjų.  
12. Medyje išplėskite **BIURO IR STALO PRIEDAI** ir pažymėkite **Žirklės**.
13. Lauke **Paveldimi tiekėjai iš pirminės kategorijos:** pažymėkite **Ne**.
14. Lauke **Paveldimi tiekėjai iš pirminės kategorijos:** pažymėkite **Taip**.

