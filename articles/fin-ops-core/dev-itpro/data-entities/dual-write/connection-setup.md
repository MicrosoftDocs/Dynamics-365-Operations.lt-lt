---
title: Palaikomi dvigubo rašymo nustatymo scenarijai
description: Šioje temoje aprašomi scenarijai, palaikomi dvigubo rašymo nustatymui.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d7ff514768ee8e4797b591da89e190a855385885
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172859"
---
# <a name="supported-scenarios-for-dual-write-setup"></a>Palaikomi dvigubo rašymo nustatymo scenarijai

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Galite nustatyti dvigubo rašymo ryšį tarp „Finance and Operations“ aplinkos ir „Common Data Service“ aplinkos.

+ **„Finance and Operations“ aplinka** suteikia pamatinę platformą **„Finance and Operations“ programoms** (pvz., „Microsoft Dynamics 365 Finance“, „Dynamics 365 Supply Chain Management“, „Dynamics 365 Retail“ ir „Dynamics 365 Human Resources“).
+ **„Common Data Service“ aplinka** suteikia pamatinę platformą **modeliu grįstoms „Dynamics 365“ programoms** („Dynamics 365 Sales“, „Dynamics 365 Customer Service“, „Dynamics 365 Field Service“, „Dynamics 365 Marketing“ ir „Dynamics 365 Project Service Automation“).

Nustatymo mechanizmas skiriasi, atsižvelgiant į jūsų prenumeratą ir aplinką.

+ Naudojant naujus „Finance and Operations“ programų egzempliorius, dvigubo rašymo ryšio nustatymas pradedamas „Microsoft Dynamics“ aplinkoje „Lifecycle Services“ (LCS). Jei turite licenciją, skirtą „Microsoft Power Platform“, gausite naują „Common Data Service“ aplinką, jei jūsų nuomotojas neturi aplinkos.
+ Esamose egzempliorių „Finance and Operations“ programose dvigubo rašymo ryšio nustatymas pradedamas „Finance and Operations“ aplinkoje.

Palaikomi toliau nurodyti nustatymo scenarijai:

+ [Naujas „Finance and Operations“ programos egzempliorius ir naujas modeliu grįstas programos egzempliorius](#new-new)
+ [Naujas „Finance and Operations“ programos egzempliorius ir esantis modeliu grįstas programos egzempliorius](#new-existing)
+ [Naujas „Finance and Operations“ programos egzempliorius, kuriame yra demonstraciniai duomenys, ir naujas modeliu grįstas programos egzempliorius](#new-demo-new)
+ [Naujas „Finance and Operations“ programos egzempliorius, kuriame yra demonstraciniai duomenys, ir esamas modeliu grįstas programos egzempliorius](#new-demo-existing)
+ [Esamas „Finance and Operations“ programos egzempliorius ir naujas modeliu grįstas programos egzempliorius](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a>Naujas „Finance and Operations“ programos egzempliorius ir naujas modeliu grįstas programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kuri neturi duomenų, egzemplioriaus ir naujo modeliu grįsto egzemplioriaus „Dynamics 365“ programoje, atlikite veiksmus, nurodytus [Dvigubo rašymo nustatymas „Lifecycle Services“](lcs-setup.md). Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:

- Parengta nauja tuščia „Finance and Operations“ aplinka.
- Parengta naujas tuščias modeliu grįstos programos egzempliorius, kuriame įdiegtas „CRM“ pagrindinis sprendimas.
- DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.
- Objektų žemėlapiai įgalinami tiesioginiui sinchronizavimui.

Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a>Naujas „Finance and Operations“ programos egzempliorius ir esantis modeliu grįstas programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kuri neturi duomenų, egzemplioriaus ir esamo modeliu grįsto egzemplioriaus „Dynamics 365“ programoje, atlikite veiksmus, nurodytus [Dvigubo rašymo nustatymas „Lifecycle Services“](lcs-setup.md). Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:

- Parengta nauja tuščia „Finance and Operations“ aplinka.
- DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.
- Objektų žemėlapiai įgalinami tiesioginiui sinchronizavimui.

Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.

Norėdami sinchronizuoti esamus „Common Data Service“ duomenis su „Finance and Operations“ programa, atlikite šiuos veiksmus.

1. Sukurkite naują įmonę programoje „Finance and Operations“.
2. Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.
3. [Perkraukite](bootstrap-company-data.md) „Common Data Service“ duomenis naudodami trijų raidžių Tarptautinės standartizacijos organizacijos (ISO) įmonės kodą.

Kadangi dvigubo rašymo būsena yra tiesioginio sinchronizavimo režime, duomenys iš „Common Data Service“ automatiškai paleidžiami į „Finance and Operations“ programą.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a>Naujas „Finance and Operations“ programos egzempliorius, kuriame yra demonstraciniai duomenys, ir naujas modeliu grįstas programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje yra demonstraciniai duomenys, egzemplioriaus ir naujo modeliu grįstos „Dynamics 365“ programos egzemplioriaus, atlikite veiksmus, nurodytus ankščiau šioje temoje pateiktame skyriuje [Naujas „Finance and Operations“ programos egzempliorius ir naujas modeliu grįstos programos egzempliorius](#new-new). Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti demonstracinius duomenis su modeliu pagrįsta programa, atlikite šiuos veiksmus.

1. Atidarykite „Finance and Operations“ programą LCS puslapyje, prisijunkite, o tada pereikite prie **Duomenų tvarkymas \> Dvigubas rašymas**.
2. Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a>Naujas „Finance and Operations“ programos egzempliorius, kuriame yra demonstraciniai duomenys, ir esamas modeliu grįstas programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje yra demonstraciniai duomenys, egzemplioriaus ir esamo modeliu grįstos „Dynamics 365“ programos egzemplioriaus, atlikite veiksmus, nurodytus ankščiau šioje temoje pateiktame skyriuje [Naujas „Finance and Operations“ programos egzempliorius ir esamas modeliu grįstos programos egzempliorius](#new-existing). Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti demonstracinius duomenis su modeliu pagrįsta programa, atlikite šiuos veiksmus.

1. Atidarykite „Finance and Operations“ programą LCS puslapyje, prisijunkite, o tada pereikite prie **Duomenų tvarkymas \> Dvigubas rašymas**.
2. Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.

Norėdami sinchronizuoti esamus „Common Data Service“ duomenis su „Finance and Operations“ programa, atlikite šiuos veiksmus.

1. Sukurkite naują įmonę programoje „Finance and Operations“.
2. Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.
3. [Perkraukite](bootstrap-company-data.md) „Common Data Service“ duomenis naudodami trijų raidžių ISO įmonės kodą.

Kadangi dvigubo rašymo būsena yra tiesioginio sinchronizavimo režime, duomenys iš „Common Data Service“ automatiškai paleidžiami į „Finance and Operations“ programą.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a>Esamas „Finance and Operations“ programos egzempliorius ir naujas modeliu grįstas programos egzempliorius

Dvigubo rašymo ryšio nustatymas tarp esamo „Finance and Operations“ programos egzemplioriaus ir naujo arba esamo modeliu grįstos „Dynamics 365“ programos egzemplioriaus vyksta „Finance and Operation“ aplinkoje.

1. Nustatykite ryšį „Finance and Operations“ programoje.
2. Norėdami sinchronizuoti esamus „Common Data Service“ duomenis į „Finance and Operations“ programą, [perkraukite](bootstrap-company-data.md) „Common Data Service“ duomenis naudodami trijų raidžių ISO įmonės kodą.

Kadangi dvigubo rašymo būsena yra tiesioginio sinchronizavimo režime, duomenys iš „Common Data Service“ automatiškai paleidžiami į „Finance and Operations“ programą.
