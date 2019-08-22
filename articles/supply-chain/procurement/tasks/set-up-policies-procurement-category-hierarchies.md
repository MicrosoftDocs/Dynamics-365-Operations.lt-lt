---
title: Nustatyti įsigijimo kategorijų hierarchijų strategijas
description: Naudokite šią procedūrą norėdami nustatyti taisykles užsisakyti produktų kategorijoje.
author: mkirknel
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 230794eacd5e9911496dd3826f08126cc21494cb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844182"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Nustatyti įsigijimo kategorijų hierarchijų strategijas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Naudokite šią procedūrą norėdami nustatyti taisykles užsisakyti produktų kategorijoje. Taisyklės nustatomos konkrečiai pirkimo strategijai. Kategorijos prieigos taisyklė nurodo, prie kurių įsigijimo kategorijų darbuotojai turės prieigą kurdami paraišką. Kai kuriama paraiška, taikytinos pirkimo strategijos ir kategorijos prieigos taisyklės nustatomos pagal juridinį subjektą ir veiklos vienetą, kuriam darbuotojas priskirtas. Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF. Šią užduotį paprastai atlieka pirkimo vadovas.


## <a name="find-the-procurement-policy"></a>Rasti įsigijimo strategiją
1. Pasirinkite **Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.
2. Spustelėkite įsigijimo strategijos USMF strategijos saitą. Tai yra strategija, į kurią įtrauksite į taisyklę. Tai turi būti aktyvi strategija.  

## <a name="create-a-category-access-rule"></a>Sukurti kategorijos prieigos taisyklę
1. Išplėskite dalį **Policy rules**.
2. Sąraše **Strategijos taisyklės tipas** pasirinkite **Kategorijos prieigos strategijos taisyklė**. Jei mygtukas **Create policy rule** patamsintas, taip yra todėl, kad jau yra aktyvi kategorijos prieigos strategijos taisyklė. Patikrinkite laukus **Effective** data ir **Expiration**data, kad nustatytumėte, kuri tai strategijos taisyklė, tada pasirinkite jį ir spustelėkite **Retire policy rule**. Jei mygtuką **Create policy rule** galima naudoti, jums nereikia atlikti jokių veiksmų.  
3. Spustelėkite **Create policy rule**.
4. Lauke **Effective date** įveskite datą ir laiką. Laikas turi negali sutapti su kita jau suaktyvinta taisykle.  
5. Pasirinkite kategoriją, kuriai bus taikoma taisyklė. Pasižymėkite, kuri tai kategorija, nes jos reikės vėliau. Pasirinkus kategoriją, jos pirminė kategorija arba kategorijos taip pat įtraukiamos į sąrašą Pasirinktos kategorijos. Pažymėkite žymės langelį **Include subcategories**, norėdami taisyklę taikyti visoms pasirinktos kategorijos subkategorijoms.
6. Spustelėkite dešiniąją rodyklę, kad pridėtumėte prie sąrašo **Selected categories**.  
4. Spustelėkite **Gerai**. Jei parinktį **Include parent rule** nustatysite į Taip, strategijos taisyklė, kurią nustatote pirminei kategorijai, taip priskiriama jos antrinėms kategorijoms, jei antrinėms kategorijoms nenurodytos strategijos taisyklės.

## <a name="create-a-category-policy-rule"></a>Sukurti kategorijos strategijos taisyklę
1. Sąraše **Strategijos taisyklės tipas** pasirinkite **Kategorijos strategijos taisyklė**. Jei mygtukas **Create policy rule** patamsintas, pasirinkite aktyvią strategijos taisyklę ir tada spustelėkite **Retire policy rule**.  
2. Spustelėkite **Create policy rule**.
3. Lauke **Effective date** įveskite datą ir laiką.
4. Spustelėkite **Pridėti**.
5. Pasirinkite tą pačią kategoriją **Category **, kurią naudojote nustatydami kategorijos prieigos taisyklę **Category access rule**.
6. Lauke **Vendor selection**pasirinkite parinktį. Pasirinkite taisyklę, norėdami valdyti, kokius kategorijos tiekėjus galima pasirinkti kuriant paraiškas.  
7. Spustelėkite **Uždaryti**. Jūsų nustatytos strategijos taisyklės taikomos tipo Suvartojimas paraiškoms. Jei norite nustatyti strategijas tipo Papildymas paraiškoms, kurkite taisyklę, skirtą strategijos taisyklės tipui, kuris vadinamas „Papildymo kategorijos prieigos strategijos taisyklė“.  

