---
title: Nustatyti įsigijimo kategorijų hierarchijų strategijas
description: Naudokite šią procedūrą norėdami nustatyti taisykles užsisakyti produktų kategorijoje.
author: kamaybac
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 242dd46e8b54504924f5bd13404dd9780c112cff8339d0a645785b2d4243871a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760447"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Nustatyti įsigijimo kategorijų hierarchijų strategijas

[!include [banner](../../includes/banner.md)]

Naudokite šią procedūrą norėdami nustatyti taisykles užsisakyti produktų kategorijoje. Taisyklės nustatomos konkrečiai pirkimo strategijai. Kategorijos prieigos taisyklė nurodo, prie kurių įsigijimo kategorijų darbuotojai turės prieigą kurdami paraišką. Kai kuriama paraiška, taikytinos pirkimo strategijos ir kategorijos prieigos taisyklės nustatomos pagal juridinį subjektą ir veiklos vienetą, kuriam darbuotojas priskirtas. Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF. Šią užduotį paprastai atlieka pirkimo vadovas.


## <a name="find-the-procurement-policy"></a>Rasti įsigijimo strategiją
1. Naršymo srityje pasirinkite **Moduliai > Įsigijimas ir šaltinio pasirinkimas > Sąranka > Strategijos > Pirkimo strategijos**.
2. Spustelėkite įsigijimo strategijos USMF strategijos saitą. Šiai strategijai reikės pridėti taisyklę. Tai turi būti aktyvi strategija.  

## <a name="create-a-category-access-rule"></a>Sukurti kategorijos prieigos taisyklę
1. Išplėskite „FastTab“ skirtuką **Strategijos taisyklės**.
2. Sąraše **Strategijos taisyklės tipas** pasirinkite **Kategorijos prieigos strategijos taisyklė**. Jei mygtukas **Sukurti strategijos taisyklę** yra pritemdytas, taip yra todėl, kad prieigos prie kategorijos strategijos taisyklė jau yra aktyvi. Patikrinkite laukus **Įsigaliojimo data** ir **Galiojimo data**, kad nustatytumėte, kuri tai strategijos taisyklė, tada pasirinkite ją ir spustelėkite **Naikinti strategijos taisyklę**. Jei mygtukas **Sukurti strategijos taisyklę** pasiekiamas, jums nereikia nieko daryti.  
3. Spustelėkite **Kurti strategijos taisyklę**.
4. Lauke **Įsigaliojimo data** įveskite datą ir laiką. Laikas neturi sutapti su kita jau aktyvia taisykle.  
5. Pasirinkite kategoriją, kuriai bus taikoma taisyklė. Pasižymėkite, kokia tai kategorija, nes jos prireiks vėliau. Pasirinkus kategoriją, jos pirminė kategorija arba kategorijos taip pat įtraukiamos į sąrašą Pasirinktos kategorijos. Pažymėkite žymės langelį **Įtraukti subkategorijas**, norėdami taisyklę taikyti visoms pasirinktos kategorijos subkategorijoms.
6. Spustelėkite dešiniąją rodyklę, kad pridėtumėte prie sąrašo **Pasirinktos kategorijos**.  
4. Spustelėkite **Gerai**. Jei parinktį **Įtraukti pirminę taisyklę** nustatysite į Taip, strategijos taisyklė, kurią nustatote pirminei kategorijai, taip priskiriama jos antrinėms kategorijoms, jei antrinėms kategorijoms nenurodytos strategijos taisyklės.

## <a name="create-a-category-policy-rule"></a>Sukurti kategorijos strategijos taisyklę
1. Sąraše **Strategijos taisyklės tipas** pasirinkite **Kategorijos strategijos taisyklė**. Jei mygtukas **Kurti strategijos taisyklę** patamsintas, pasirinkite aktyvią strategijos taisyklę ir tada spustelėkite **Panaikinti strategijos taisyklę**.  
2. Spustelėkite **Kurti strategijos taisyklę**.
3. Lauke **Įsigaliojimo data** įveskite datą ir laiką.
4. Spustelėkite **Pridėti**.
5. Lauke **Kategorija** pasirinkite tą pačią kategoriją, kurią naudojote nustatydami **Kategorijos prieigos taisyklė**.
6. Lauke **Tiekėjo pasirinkimas** pasirinkite parinktį. Pasirinkite taisyklę, norėdami valdyti, kokius kategorijos tiekėjus galima pasirinkti kuriant paraiškas.  
7. Spustelėkite **Uždaryti**. Jūsų nustatytos strategijos taisyklės taikomos tipo Suvartojimas paraiškoms. Jei norite apibrėžti tipo Papildymas paraiškų strategijas, sukurkite Strategijos taisyklių tipo taisyklę pavadinimu „Papildymo kategorijos prieigos strategijos taisyklė“.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]