---
title: Nurodymai, kaip nustatyti dvigubą rašymą
description: Šioje temoje aprašomi scenarijai, palaikomi dvigubo rašymo nustatymui.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088511"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a>Nurodymai, kaip nustatyti dvigubą rašymą

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Galite nustatyti dvigubo rašymo ryšį tarp „Finance and Operations“ aplinkos ir „Common Data Service“ aplinkos.

+ **„Finance and Operations” aplinka** suteikia esamą platformą **„Finance and Operations” programoms** (pavyzdžiui, „Microsoft Dynamics 365 Finance”, „Dynamics 365 Supply Chain Management” ir „Dynamics 365 Retail”).
+ **„Common Data Service“ aplinka** suteikia pamatinę platformą **klientų įtraukimo programoms** („Dynamics 365 Sales“, „Dynamics 365 Customer Service“, „Dynamics 365 Field Service“, „Dynamics 365 Marketing“ ir „Dynamics 365 Project Service Automation“).

>[!IMPORTANT]
>Dvigubo rašymo ryšiai palaikomi „Finance and Operations” žmogiškuosiuose ištekliuose, tačiau ne „Dynamics 365 Human Resources” programoje.

Nustatymo mechanizmas skiriasi, atsižvelgiant į jūsų prenumeratą ir aplinką.

+ Naudojant naujus „Finance and Operations“ programų egzempliorius, dvigubo rašymo ryšio nustatymas pradedamas „Microsoft Dynamics“ aplinkoje „Lifecycle Services“ (LCS). Jei turite licenciją, skirtą „Power Platform“, gausite naują „Common Data Service“ aplinką, jei jūsų nuomotojas neturi aplinkos.
+ Esamose egzempliorių „Finance and Operations“ programose dvigubo rašymo ryšio nustatymas pradedamas „Finance and Operations“ aplinkoje.

Prieš pradėdami naudoti dvigubo rašymo funkciją objekte, galite paleisti pradinį sinchronizavimą, norėdami tvarkyti esamus duomenis abiejose „Finance and Operations” ir klientų įtraukimo programų pusėse. Galite praleisti pradinį sinchronizavimą, jei jums nereikia sinchronizuoti dviejų aplinkų duomenų.

Pradinis sinchronizavimas leidžia dvikryptį esamų duomenų kopijavimą iš vienos programos į kitą. Galimi keli skirtingi nustatymo scenarijai, atsižvelgiant į tai, kokias aplinkas jau turite ir kokio tipo duomenys yra aplinkose.

Palaikomi toliau nurodyti nustatymo scenarijai:

+ [Naujas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius](#new-new)
+ [Naujas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius](#new-existing)
+ [Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir naujas klientų įtraukimo programos egzempliorius](#new-data-new)
+ [Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir esamas klientų įtraukimo programos egzempliorius](#new-data-existing)
+ [Esamas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius](#existing-new)
+ [Esamas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Naujas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje nėra duomenų, egzemplioriaus ir naujo klientų įtraukimo programos egzemplioriaus, atlikite veiksmus, nurodytus [Dvigubo rašymo nustatymas „Lifecycle Services“](lcs-setup.md). Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:

- Parengta nauja tuščia „Finance and Operations“ aplinka.
- Parengta naujas tuščias klientų įtraukimo programos egzempliorius, kuriame įdiegtas „CRM“ pagrindinis sprendimas.
- DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.
- Objektų žemėlapiai įgalinami tiesioginiui sinchronizavimui.

Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Naujas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje nėra duomenų, egzemplioriaus ir esamo klientų įtraukimo programos egzemplioriaus, atlikite veiksmus, nurodytus [Dvigubo rašymo nustatymas „Lifecycle Services“](lcs-setup.md). Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:

- Parengta nauja tuščia „Finance and Operations“ aplinka.
- DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.
- Objektų žemėlapiai įgalinami tiesioginiui sinchronizavimui.

Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.

Norėdami sinchronizuoti esamus „Common Data Service“ duomenis su „Finance and Operations“ programa, atlikite šiuos veiksmus.

1. Sukurkite naują įmonę programoje „Finance and Operations“.
2. Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.
3. [Perkraukite](bootstrap-company-data.md) „Common Data Service“ duomenis naudodami trijų raidžių Tarptautinės standartizacijos organizacijos (ISO) įmonės kodą.
4. Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.

Pavyzdį ir alternatyvų būdą rasite [Pavyzdys](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir naujas klientų įtraukimo programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje yra duomenų, egzemplioriaus ir naujo klientų įtraukimo programos egzemplioriaus, atlikite veiksmus, nurodytus ankščiau šioje temoje pateiktame skyriuje [Naujas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius](#new-new). Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti duomenis su klientų įtraukimo programa, atlikite toliau pateiktus veiksmus.

1. Atidarykite „Finance and Operations“ programą LCS puslapyje, prisijunkite, o tada pereikite prie **Duomenų tvarkymas \> Dvigubas rašymas**.
2. Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.

Pavyzdį ir alternatyvų būdą rasite [Pavyzdys](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir esamas klientų įtraukimo programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje yra duomenų, egzemplioriaus ir esamo klientų įtraukimo programos egzemplioriaus, atlikite veiksmus, nurodytus ankščiau šioje temoje pateiktame skyriuje [Naujas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius](#new-existing). Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti duomenis su klientų įtraukimo programa, atlikite toliau pateiktus veiksmus.

1. Atidarykite „Finance and Operations“ programą LCS puslapyje, prisijunkite, o tada pereikite prie **Duomenų tvarkymas \> Dvigubas rašymas**.
2. Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.

Norėdami sinchronizuoti esamus „Common Data Service“ duomenis su „Finance and Operations“ programa, atlikite šiuos veiksmus.

1. Sukurkite naują įmonę programoje „Finance and Operations“.
2. Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.
3. [Perkraukite](bootstrap-company-data.md) „Common Data Service“ duomenis naudodami trijų raidžių ISO įmonės kodą.
4. Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.

Pavyzdį ir alternatyvų būdą rasite [Pavyzdys](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Esamas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius

Dvigubo rašymo ryšio nustatymas tarp esamo „Finance and Operations“ programos egzemplioriaus ir naujo klientų įtraukimo programos egzemplioriaus vykdomas „Finance and Operation“ aplinkoje.

1. [Nustatykite ryšį „Finance and Operations“ programoje](enable-dual-write.md).
2. Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.

Pavyzdį ir alternatyvų būdą rasite [Pavyzdys](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Esamas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius

Dvigubo rašymo ryšio nustatymas tarp esamo „Finance and Operations“ programos egzemplioriaus ir esamo klientų įtraukimo programos egzemplioriaus vykdomas „Finance and Operation“ aplinkoje.

1. Nustatykite ryšį „Finance and Operations“ programoje.
2. Norėdami sinchronizuoti esamus „Common Data Service“ duomenis į „Finance and Operations“ programą, [perkraukite](bootstrap-company-data.md) „Common Data Service“ duomenis naudodami trijų raidžių ISO įmonės kodą.
3. Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.

Pavyzdį ir alternatyvų būdą rasite [Pavyzdys](#example).

## <a name="example"></a>Pavyzdys

Pavyzdį rasite [Objektų Klientai V3 ir Kontaktai schemos įgalinimas](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)

Jei norite naudoti alternatyvų būdą, pagrįstą kiekvieno objekto, kuris turi vykdyti pradinį sinchronizavimą, duomenimis, žr. [Pradinės sinchronizacijos aplinkybės](initial-sync-guidance.md).
