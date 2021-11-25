---
title: Nurodymai, kaip nustatyti dvigubą rašymą
description: Šioje temoje aprašomi scenarijai, palaikomi dvigubo rašymo nustatymui.
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 434d1a432cc4b8cfd31198f8f668aef6e04a51fa
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782608"
---
# <a name="guidance-for-dual-write-setup"></a>Nurodymai, kaip nustatyti dvigubą rašymą

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Galite nustatyti dvigubo rašymo ryšį tarp „Finance and Operations“ aplinkos ir „Dataverse“ aplinkos.

+ **„Finance and Operations“ aplinka** suteikia pamatinę platformą **„Finance and Operations“ programoms** (pvz., „Microsoft Dynamics 365 Finance“, „Dynamics 365 Supply Chain Management“, „Dynamics 365 Commerce“ ir „Dynamics 365 Human Resources“).
+ **„Dataverse ”aplinka** suteikia pamatinę platformą **„customer engagement” programoms** („Dynamics 365 Sales“, „Dynamics 365 Customer Service“, „Dynamics 365 column Service“, „Dynamics 365 Marketing“ ir „Dynamics 365 Project Service Automation“).

> [!IMPORTANT]
> Dvigubo rašymo ryšiai palaikomi „Dynamics 365 Finance” modulyje Personalas, tačiau ne „Dynamics 365 Human Resources” programoje.

Nustatymo mechanizmas skiriasi, atsižvelgiant į jūsų prenumeratą ir aplinką.

+ Naudojant naujus „Finance and Operations“ programų egzempliorius, dvigubo rašymo ryšio nustatymas pradedamas „Microsoft Dynamics“ aplinkoje „Lifecycle Services“ (LCS). Jei turite licenciją, skirtą „Microsoft Power Platform“, gausite naują „Dataverse“ aplinką, jei jūsų nuomotojas neturi aplinkos.
+ Esamose egzempliorių „Finance and Operations“ programose dvigubo rašymo ryšio nustatymas pradedamas „Finance and Operations“ aplinkoje.

Prieš pradėdami naudoti dvigubo rašymo funkciją objekte, galite paleisti pradinį sinchronizavimą, norėdami tvarkyti esamus duomenis abiejose „Finance and Operations” ir klientų įtraukimo programų pusėse. Galite praleisti pradinį sinchronizavimą, jei jums nereikia sinchronizuoti dviejų aplinkų duomenų.

Pradinis sinchronizavimas leidžia dvikryptį esamų duomenų kopijavimą iš vienos programos į kitą. Galimi keli nustatymo scenarijai, atsižvelgiant į tai, kokias aplinkas jau turite ir kokio tipo duomenys yra jose.

Palaikomi toliau nurodyti nustatymo scenarijai:

+ [Naujas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius](#new-new)
+ [Naujas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius](#new-existing)
+ [Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir naujas klientų įtraukimo programos egzempliorius](#new-data-new)
+ [Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir esamas klientų įtraukimo programos egzempliorius](#new-data-existing)
+ [Esamas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius](#existing-new)
+ [Esamas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a> Naujas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje nėra duomenų, egzemplioriaus ir naujo klientų įtraukimo programos egzemplioriaus, atlikite veiksmus, nurodytus [Dvigubo rašymo nustatymas „Lifecycle Services“](lcs-setup.md). Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:

- Parengta nauja tuščia „Finance and Operations“ aplinka.
- Parengta naujas tuščias klientų įtraukimo programos egzempliorius, kuriame įdiegtas „CRM“ pagrindinis sprendimas.
- DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.
- Lentelių žemėlapiai įgalinami tiesioginiam sinchronizavimui.

Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a> Naujas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje nėra duomenų, egzemplioriaus ir esamo klientų įtraukimo programos egzemplioriaus, atlikite veiksmus, nurodytus [Dvigubo rašymo nustatymas „Lifecycle Services“](lcs-setup.md). Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:

- Parengta nauja tuščia „Finance and Operations“ aplinka.
- DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.
- Lentelių žemėlapiai įgalinami tiesioginiam sinchronizavimui.

Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.

Norėdami sinchronizuoti esamus „Dataverse“ duomenis su „Finance and Operations“ programa, atlikite šiuos veiksmus.

1. Sukurkite naują įmonę programoje „Finance and Operations“.
2. Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.
3. [Perkraukite](bootstrap-company-data.md) „Dataverse“ duomenis naudodami trijų raidžių Tarptautinės standartizacijos organizacijos (ISO) įmonės kodą.
4. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example) toliau šioje temoje.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a> Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir naujas klientų įtraukimo programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje yra duomenų, egzemplioriaus ir naujo klientų įtraukimo programos egzemplioriaus, atlikite veiksmus, nurodytus ankščiau šioje temoje pateiktame skyriuje [Naujas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius](#new-new). Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti duomenis su klientų įtraukimo programa, atlikite toliau pateiktus veiksmus.

1. Atidarykite „Finance and Operations“ programą LCS puslapyje, prisijunkite, o tada pereikite prie **Duomenų tvarkymas \> Dvigubas rašymas**.
2. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a> Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir esamas klientų įtraukimo programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje yra duomenų, egzemplioriaus ir esamo klientų įtraukimo programos egzemplioriaus, atlikite veiksmus, nurodytus ankščiau šioje temoje pateiktame skyriuje [Naujas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius](#new-existing). Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti duomenis su klientų įtraukimo programa, atlikite toliau pateiktus veiksmus.

1. Atidarykite „Finance and Operations“ programą LCS puslapyje, prisijunkite, o tada pereikite prie **Duomenų tvarkymas \> Dvigubas rašymas**.
2. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Norėdami sinchronizuoti esamus „Dataverse“ duomenis su „Finance and Operations“ programa, atlikite šiuos veiksmus.

1. Sukurkite naują įmonę programoje „Finance and Operations“.
2. Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.
3. [Perkraukite](bootstrap-company-data.md) „Dataverse“ duomenis naudodami trijų raidžių ISO įmonės kodą.
4. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a> Esamas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius

Dvigubo rašymo ryšio nustatymas tarp esamo „Finance and Operations“ programos egzemplioriaus ir naujo klientų įtraukimo programos egzemplioriaus vykdomas „Finance and Operation“ aplinkoje.

1. [Nustatykite ryšį „Finance and Operations“ programoje](enable-dual-write.md).
2. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a> Esamas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius

Dvigubo rašymo ryšio nustatymas tarp esamo „Finance and Operations“ programos egzemplioriaus ir esamo klientų įtraukimo programos egzemplioriaus vykdomas „Finance and Operation“ aplinkoje.

1. [Nustatykite ryšį „Finance and Operations“ programoje](enable-dual-write.md).
2. Norėdami sinchronizuoti esamus „Dataverse“ duomenis į „Finance and Operations“ programą, [perkraukite](bootstrap-company-data.md) „Dataverse“ duomenis naudodami trijų raidžių ISO įmonės kodą.
3. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example).

## <a name="example"></a>Pavyzdys

Pavyzdį rasite [Lentelių Klientai V3 ir Kontaktai schemos įgalinimas](enable-entity-map.md#enable-table-map)

Jei norite naudoti alternatyvų būdą, pagrįstą kiekvieno objekto, kuris turi vykdyti pradinį sinchronizavimą, duomenimis, žr. [Pradinės sinchronizacijos aplinkybės](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]