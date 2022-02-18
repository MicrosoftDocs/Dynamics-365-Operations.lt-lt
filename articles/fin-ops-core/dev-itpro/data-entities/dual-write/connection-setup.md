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
ms.openlocfilehash: 6de449b14bcdd82336e3e255bf62ad069d3daaf5
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061609"
---
# <a name="guidance-for-dual-write-setup"></a>Nurodymai, kaip nustatyti dvigubą rašymą

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Galite nustatyti dvigubo rašymo ryšį tarp „Finance and Operations“ aplinkos ir a Dataverse aplinką.

+ A **Finansų ir operacijų aplinka** suteikia pagrindinę platformą **Finansų ir operacijų programėlės** (pavyzdžiui, Microsoft Dynamics 365 Finance,Dynamics 365 Supply Chain Management,Dynamics 365 Commerce, ir Dynamics 365 Human Resources).
+ **„Dataverse ”aplinka** suteikia pamatinę platformą **„customer engagement” programoms** („Dynamics 365 Sales“, „Dynamics 365 Customer Service“, „Dynamics 365 column Service“, „Dynamics 365 Marketing“ ir „Dynamics 365 Project Service Automation“).

> [!IMPORTANT]
> Dvigubo rašymo ryšiai palaikomi „Dynamics 365 Finance” modulyje Personalas, tačiau ne „Dynamics 365 Human Resources” programoje.

Nustatymo mechanizmas skiriasi, atsižvelgiant į jūsų prenumeratą ir aplinką.

+ Naujiems „Finance and Operations“ programų egzemplioriams dvigubo rašymo ryšio sąranka prasideda Microsoft Dynamics Gyvenimo ciklo paslaugos (LCS). Jei turite licenciją, skirtą „Microsoft Power Platform“, gausite naują „Dataverse“ aplinką, jei jūsų nuomotojas neturi aplinkos.
+ Esamų „Finance and Operations“ programų egzempliorių dvigubo rašymo ryšio sąranka pradedama „Finance and Operations“ aplinkoje.

Prieš pradėdami dvigubą objekto rašymą, galite paleisti pradinį sinchronizavimą, kad tvarkytumėte esamus duomenis abiejose pusėse: programose „Finance and Operations“ ir „klientų įtraukimo programose“. Galite praleisti pradinį sinchronizavimą, jei jums nereikia sinchronizuoti dviejų aplinkų duomenų.

Pradinis sinchronizavimas leidžia dvikryptį esamų duomenų kopijavimą iš vienos programos į kitą. Galimi keli nustatymo scenarijai, atsižvelgiant į tai, kokias aplinkas jau turite ir kokio tipo duomenys yra jose.

Palaikomi toliau nurodyti nustatymo scenarijai:

+ [Naujas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius](#new-new)
+ [Naujas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius](#new-existing)
+ [Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir naujas klientų įtraukimo programos egzempliorius](#new-data-new)
+ [Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir esamas klientų įtraukimo programos egzempliorius](#new-data-existing)
+ [Esamas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius](#existing-new)
+ [Esamas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a> Naujas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos egzemplioriaus, kuriame nėra duomenų, ir naujo kliento įtraukimo programos egzemplioriaus, atlikite veiksmus, nurodytus [Dvigubo rašymo sąranka iš Lifecycle Services](lcs-setup.md). Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:

- Numatyta nauja tuščia „Finance and Operations“ aplinka.
- Parengta naujas tuščias klientų įtraukimo programos egzempliorius, kuriame įdiegtas „CRM“ pagrindinis sprendimas.
- DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.
- Lentelių žemėlapiai įgalinami tiesioginiam sinchronizavimui.

Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a> Naujas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos egzemplioriaus, kuriame nėra duomenų, ir esamo kliento įtraukimo programos egzemplioriaus, atlikite veiksmus [Dvigubo rašymo sąranka iš Lifecycle Services](lcs-setup.md). Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:

- Numatyta nauja tuščia „Finance and Operations“ aplinka.
- DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.
- Lentelių žemėlapiai įgalinami tiesioginiam sinchronizavimui.

Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.

Norėdami sinchronizuoti esamą Dataverse duomenis į programą „Finance and Operations“, atlikite šiuos veiksmus.

1. Sukurkite naują įmonę „Finance and Operations“ programėlėje.
2. Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.
3. [Perkraukite](bootstrap-company-data.md) „Dataverse“ duomenis naudodami trijų raidžių Tarptautinės standartizacijos organizacijos (ISO) įmonės kodą.
4. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example) toliau šioje temoje.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a> Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir naujas klientų įtraukimo programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos egzemplioriaus, kuriame yra duomenų, ir naujo kliento įtraukimo programos egzemplioriaus, atlikite veiksmus, pateiktus [Naujas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius](#new-new) skyrių anksčiau šioje temoje. Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti duomenis su klientų įtraukimo programa, atlikite toliau pateiktus veiksmus.

1. Atidarykite programą „Finance and Operations“ iš LCS puslapio, prisijunkite ir eikite į **Duomenų valdymas \> Dvigubas rašymas**.
2. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a> Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir esamas klientų įtraukimo programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos egzemplioriaus, kuriame yra duomenų, ir esamo klientų įtraukimo programos egzemplioriaus, atlikite veiksmus, pateiktus [Naujas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius](#new-existing) skyrių anksčiau šioje temoje. Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti duomenis su klientų įtraukimo programa, atlikite toliau pateiktus veiksmus.

1. Atidarykite programą „Finance and Operations“ iš LCS puslapio, prisijunkite ir eikite į **Duomenų valdymas \> Dvigubas rašymas**.
2. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Norėdami sinchronizuoti esamą Dataverse duomenis į programą „Finance and Operations“, atlikite šiuos veiksmus.

1. Sukurkite naują įmonę „Finance and Operations“ programėlėje.
2. Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.
3. [Perkraukite](bootstrap-company-data.md) „Dataverse“ duomenis naudodami trijų raidžių ISO įmonės kodą.
4. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a> Esamas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius

Dvigubo rašymo ryšys tarp esamo „Finance and Operations“ programos egzemplioriaus ir naujo kliento įtraukimo programos egzemplioriaus nustatomas „Finance and Operation“ aplinkoje.

1. [Nustatykite ryšį naudodami programą „Finance and Operations“.](enable-dual-write.md).
2. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a> Esamas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius

Dvigubo rašymo ryšys tarp esamo „Finance and Operations“ programos egzemplioriaus ir esamo kliento įtraukimo programos egzemplioriaus nustatomas „Finance and Operation“ aplinkoje.

1. [Nustatykite ryšį naudodami programą „Finance and Operations“.](enable-dual-write.md).
2. Norėdami sinchronizuoti esamą Dataverse duomenis į programą „Finance and Operations“,[bootstrap](bootstrap-company-data.md) į Dataverse duomenis naudojant trijų raidžių ISO įmonės kodą.
3. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example).

## <a name="example"></a>Pavyzdys

Pavyzdį rasite [Lentelių Klientai V3 ir Kontaktai schemos įgalinimas](enable-entity-map.md#enable-table-map)

Jei norite naudoti alternatyvų būdą, pagrįstą kiekvieno objekto, kuris turi vykdyti pradinį sinchronizavimą, duomenimis, žr. [Pradinės sinchronizacijos aplinkybės](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]