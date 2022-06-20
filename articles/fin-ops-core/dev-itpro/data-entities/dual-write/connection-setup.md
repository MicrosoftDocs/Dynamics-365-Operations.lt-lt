---
title: Nurodymai, kaip nustatyti dvigubą rašymą
description: Šiame straipsnyje aprašomi scenarijai, kurie palaikomi dvigubo rašymo nustatymui.
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: a0d1b4e1f093874a8fd37cf7aadb331cd1e7adc4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873155"
---
# <a name="guidance-for-dual-write-setup"></a>Nurodymai, kaip nustatyti dvigubą rašymą

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Galite nustatyti dvigubo rašymo ryšį tarp finansų ir operacijų aplinkos ir Dataverse aplinkos.

+ Finansų **ir operacijų aplinka suteikia** pagrindinę finansų **ir** operacijų programėlių platformą (pvz., Microsoft Dynamics "365" finansai Dynamics 365 Supply Chain Management ir Dynamics 365 Commerce).Dynamics 365 Human Resources
+ **„Dataverse ”aplinka** suteikia pamatinę platformą **„customer engagement” programoms** („Dynamics 365 Sales“, „Dynamics 365 Customer Service“, „Dynamics 365 column Service“, „Dynamics 365 Marketing“ ir „Dynamics 365 Project Service Automation“).

> [!IMPORTANT]
> Personalo modulis, skirtas "Dynamics 365 Finance", palaiko dvigubo rašymo ryšius Dynamics 365 Human Resources, bet programa neįrašo.

Nustatymo mechanizmas skiriasi, atsižvelgiant į jūsų prenumeratą ir aplinką.

+ Naujiems finansų ir operacijų programėlių egzemplioriams pradedamas dvigubo rašymo ryšio Microsoft Dynamics nustatymas vykdymo ciklo tarnybose (LCS). Jei turite licenciją, skirtą „Microsoft Power Platform“, gausite naują „Dataverse“ aplinką, jei jūsų nuomotojas neturi aplinkos.
+ Esamų egzempliorių finansų ir operacijų programėlių dvigubo rašymo ryšio nustatymas pradedamas finansų ir operacijų aplinkoje.

Prieš pradėdami dvigubo rašymo objektą, galite vykdyti pradinį sinchronizavimą, kad apdorotumėte esamus duomenis abiejose pusėse: finansų ir operacijų programėles ir klientų įsipareigojimo programėles. Galite praleisti pradinį sinchronizavimą, jei jums nereikia sinchronizuoti dviejų aplinkų duomenų.

Pradinis sinchronizavimas leidžia dvikryptį esamų duomenų kopijavimą iš vienos programos į kitą. Galimi keli nustatymo scenarijai, atsižvelgiant į tai, kokias aplinkas jau turite ir kokio tipo duomenys yra jose.

Palaikomi toliau nurodyti nustatymo scenarijai:

+ [Naujas finansų ir operacijų programos egzempliorius ir naujas klientų įsipareigojimų programos egzempliorius](#new-new)
+ [Naujas finansų ir operacijų programos egzempliorius ir esamas klientų įsipareigojimų programos egzempliorius](#new-existing)
+ [Naujas finansų ir operacijų programos egzempliorius, kuriame yra duomenų ir naujas klientų įsipareigojimų programos egzempliorius](#new-data-new)
+ [Naujas finansų ir operacijų programos egzempliorius, kuriame yra duomenų ir esamo klientų įsipareigojimo programos egzemplioriaus](#new-data-existing)
+ [Esamas finansų ir operacijų programos egzempliorius ir naujas klientų įsipareigojimų programos egzempliorius](#existing-new)
+ [Esamas finansų ir operacijų programos egzempliorius ir esamas klientų įsipareigojimų programos egzempliorius](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a> Naujas finansų ir operacijų programos egzempliorius ir naujas klientų įsipareigojimų programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo finansų ir operacijų programos egzemplioriaus, kuriame nėra duomenų, ir naujo klientų įsipareigojimo programos egzemplioriaus, [atlikite dvigubo rašymo nustatymo veiksmus iš vykdymo ciklo tarnybų](lcs-setup.md). Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:

- Su nuostata nauja, tuščia finansų ir operacijų aplinka.
- Parengta naujas tuščias klientų įtraukimo programos egzempliorius, kuriame įdiegtas „CRM“ pagrindinis sprendimas.
- DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.
- Lentelių žemėlapiai įgalinami tiesioginiam sinchronizavimui.

Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a> Naujas finansų ir operacijų programos egzempliorius ir esamas klientų įsipareigojimų programos egzempliorius

Norėdami nustatyti dvigubo rašymo ryšį tarp naujo finansų ir operacijų programos egzemplioriaus, kuriame nėra duomenų, ir esamo klientų įsipareigojimo programos egzemplioriaus, [atlikite dvigubo rašymo nustatymo veiksmus iš vykdymo ciklo tarnybų](lcs-setup.md). Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:

- Su nuostata nauja, tuščia finansų ir operacijų aplinka.
- DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.
- Lentelių žemėlapiai įgalinami tiesioginiam sinchronizavimui.

Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.

Norėdami sinchronizuoti esamus duomenis Dataverse su finansų ir operacijų programa, atlikite šiuos veiksmus.

1. Sukurkite naują įmonę finansų ir operacijų programoje.
2. Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.
3. [Perkraukite](bootstrap-company-data.md) „Dataverse“ duomenis naudodami trijų raidžių Tarptautinės standartizacijos organizacijos (ISO) įmonės kodą.
4. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Pavyzdžio ir alternatyvaus metodo saitų ieškokite toliau [šiame straipsnyje skyriuje](#example) Pavyzdys.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a> Naujas finansų ir operacijų programos egzempliorius, kuriame yra duomenų ir naujas klientų įsipareigojimų programos egzempliorius

Norėdami [nustatyti dvigubo rašymo ryšį tarp naujo finansų ir operacijų programos egzemplioriaus, kuriame yra duomenų ir naujo klientų įsipareigojimo programos egzemplioriaus, atlikite veiksmus,](#new-new) nurodytus naujoje finansų ir operacijų programos egzemplioriuje ir anksčiau šiame straipsnyje naujame klientų įsipareigojimo programos skyriuje. Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti duomenis su klientų įtraukimo programa, atlikite toliau pateiktus veiksmus.

1. Atidarykite finansų ir operacijų programą iš LCS puslapio, prisiregistruokite ir eikite į duomenų valdymo **dvigubo \> rašymo parinktį**.
2. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a> Naujas finansų ir operacijų programos egzempliorius, kuriame yra duomenų ir esamo klientų įsipareigojimo programos egzemplioriaus

Norėdami [nustatyti dvigubo rašymo ryšį tarp naujo finansų ir operacijų programos egzemplioriaus, kuriame yra duomenų ir esamo klientų įsipareigojimo programos egzemplioriaus, atlikite veiksmus, nurodytus naujoje finansų ir operacijų programos egzemplioriuje ir esamame klientų įsipareigojimo programos skyriuje,](#new-existing) kuris nurodytas anksčiau šiame straipsnyje. Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti duomenis su klientų įtraukimo programa, atlikite toliau pateiktus veiksmus.

1. Atidarykite finansų ir operacijų programą iš LCS puslapio, prisiregistruokite ir eikite į duomenų valdymo **dvigubo \> rašymo parinktį**.
2. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Norėdami sinchronizuoti esamus duomenis Dataverse su finansų ir operacijų programa, atlikite šiuos veiksmus.

1. Sukurkite naują įmonę finansų ir operacijų programoje.
2. Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.
3. [Perkraukite](bootstrap-company-data.md) „Dataverse“ duomenis naudodami trijų raidžių ISO įmonės kodą.
4. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a> Esamas finansų ir operacijų programos egzempliorius ir naujas klientų įsipareigojimų programos egzempliorius

Dvigubo rašymo ryšio tarp esamo finansų ir operacijų programos egzemplioriaus ir naujo kliento įsipareigojimo programos egzemplioriaus nustatymas vyksta finansų ir operacijų aplinkoje.

1. [Nustatykite ryšį iš finansų ir operacijų programos](enable-dual-write.md).
2. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a> Esamas finansų ir operacijų programos egzempliorius ir esamas klientų įsipareigojimų programos egzempliorius

Dvigubo rašymo ryšio tarp esamo finansų ir operacijų programos egzemplioriaus ir esamo kliento įsipareigojimo programos egzemplioriaus nustatymas vyksta finansų ir operacijų aplinkoje.

1. [Nustatykite ryšį iš finansų ir operacijų programos](enable-dual-write.md).
2. Norėdami sinchronizuoti esamus duomenis Dataverse su finansų ir operacijų programa, [vykdykite](bootstrap-company-data.md)Dataverse duomenų kainą naudodami trijų raidžių ISO įmonės kodą.
3. Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.

Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example).

## <a name="example"></a>Pavyzdys

Pavyzdį rasite [Lentelių Klientai V3 ir Kontaktai schemos įgalinimas](enable-entity-map.md#enable-table-map)

Jei norite naudoti alternatyvų būdą, pagrįstą kiekvieno objekto, kuris turi vykdyti pradinį sinchronizavimą, duomenimis, žr. [Pradinės sinchronizacijos aplinkybės](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]