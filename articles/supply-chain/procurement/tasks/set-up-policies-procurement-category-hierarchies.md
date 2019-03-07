---
title: Nustatyti įsigijimo kategorijų hierarchijų strategijas
description: Naudokite šią procedūrą norėdami nustatyti taisykles užsisakyti produktų kategorijoje.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1fdf357466de12bd0188fc43cd266c67af762c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "323162"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Nustatyti įsigijimo kategorijų hierarchijų strategijas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Naudokite šią procedūrą norėdami nustatyti taisykles užsisakyti produktų kategorijoje. Taisyklės nustatomos konkrečiai pirkimo strategijai. Kategorijos prieigos taisyklė nurodo, prie kurių įsigijimo kategorijų darbuotojai turės prieigą kurdami paraišką. Kai kuriama paraiška, taikytinos pirkimo strategijos ir kategorijos prieigos taisyklės nustatomos pagal juridinį subjektą ir veiklos vienetą, kuriam darbuotojas priskirtas. Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF. Šią užduotį paprastai atlieka pirkimo vadovas.


## <a name="find-the-procurement-policy"></a>Rasti įsigijimo strategiją
1. Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Sąranka > Strategijos > Pirkimo strategijos.
2. Spustelėkite įsigijimo strategijos USMF strategijos saitą.
    * Tai yra strategija, į kurią įtrauksite į taisyklę. Tai turi būti aktyvi strategija.  

## <a name="create-a-category-access-rule"></a>Sukurti kategorijos prieigos taisyklę
1. Pasirinkite kategorijos prieigos strategijos taisyklę.
    * Jei mygtukas Kurti strategijos taisyklę patamsintas, taip yra todėl, kad jau yra aktyvi kategorijos prieigos strategijos taisyklė. Patikrinkite laukus Įsigaliojimo data ir Galiojimo data, kad nustatytumėte, kuri tai strategijos taisyklė, tada pasirinkite jį ir spustelėkite Naikinti strategijos taisyklę. Jei mygtuką Kurti strategijos taisyklę galima naudoti, jums nereikia atlikti jokių veiksmų.  
2. Spustelėkite Kurti strategijos taisyklę.
3. Lauke Įsigaliojimo data įveskite datą ir laiką.
    * Laikas turi negali sutapti su kita jau suaktyvinta taisykle.  
    * Pasirinkite kategoriją, kuriai bus taikoma taisyklė. Pasižymėkite, kuri tai kategorija, nes jos reikės vėliau. Pasirinkus kategoriją, jos pirminė kategorija arba kategorijos taip pat įtraukiamos į sąrašą Pasirinktos kategorijos.  
    * Pažymėkite žymės langelį Įtraukti subkategorijas, norėdami taisyklę taikyti visoms pasirinktos kategorijos subkategorijoms.  
4. Spustelėkite Pridėti.
    * Jei parinktį Įtraukti pirminę taisyklę nustatysite į Taip, strategijos taisyklė, kurią nustatote pirminei kategorijai, taip priskiriama jos antrinėms kategorijoms, jei antrinėms kategorijoms nenurodytos strategijos taisyklės.  
5. Spustelėkite GERAI.

## <a name="create-a-category-policy-rule"></a>Sukurti kategorijos strategijos taisyklę
1. Pasirinkti kategorijos strategijos taisyklę
    * Jei mygtukas Kurti strategijos taisyklę patamsintas, pasirinkite aktyvią strategijos taisyklę ir tada spustelėkite Panaikinti strategijos taisyklę.  
2. Spustelėkite Kurti strategijos taisyklę.
3. Lauke Įsigaliojimo data įveskite datą ir laiką.
4. Spustelėkite Pridėti.
5. Pasirinkite tą pačią kategoriją, kurią naudojote nustatydami kategorijos prieigos taisyklę.
6. Lauke Tiekėjo pasirinkimas pasirinkite parinktį.
    * Pasirinkite taisyklę, norėdami valdyti, kokius kategorijos tiekėjus galima pasirinkti kuriant paraiškas.  
7. Spustelėkite Uždaryti.
    * Jūsų nustatytos strategijos taisyklės taikomos tipo Suvartojimas paraiškoms. Jei norite nustatyti strategijas tipo Papildymas paraiškoms, kurkite taisyklę, skirtą strategijos taisyklės tipui, kuris vadinamas „Papildymo kategorijos prieigos strategijos taisyklė“.  

