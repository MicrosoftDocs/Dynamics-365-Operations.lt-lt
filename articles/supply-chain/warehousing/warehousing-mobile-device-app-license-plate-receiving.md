---
title: Su „Warehouse Management“ mobiliųjų įrenginių programėle gaunama numerio lentelė
description: Šiame straipsnyje paaiškinama, kaip nustatyti sandėlio valdymo mobiliąją programą, kad būtų galima naudoti numerio lentelės gavimo procesą norint gauti faktines atsargas.
author: perlynne
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSParameters, WHSRFMenuItem, WHSLicensePlate, WHSPackingStructure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: fe083f16bd47b3f7bdfd366ae4b0fe4a02f49185
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907006"
---
# <a name="license-plate-receiving-via-the-warehouse-management-mobile-app"></a>Su „Warehouse Management“ mobiliųjų įrenginių programėle gaunama numerio lentelė

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti sandėlio valdymo mobiliąją programą, kad ji palaiko numerio lentelės gavimo proceso, norint gauti faktines atsargas, naudojimas.

Šią funkciją galite naudoti norėdami greitai įrašyti gaunamų atsargų gavimą, susijusį su išankstiniu siuntimo pranešimu (ASN). Sistema automatiškai sukuria ASN, kai sandėlio valdymo procesai naudojami perkėlimo užsakymui siųsti. Pirkimo užsakymo procese ASN gali būti įrašytas rankiniu būdu arba automatiškai importuotas naudojant gaunamo ASN duomenų objekto procesą.

ASN duomenys yra susieti su kroviniais ir siuntomis naudojant *pakavimo struktūras*, kurių padėkluose (pirminės numerio lentelės) gali būti saugyklos (įdėtosios numerio lentelės).

> [!NOTE]
> Kad būtų sumažintas atsargų operacijų skaičius, kai naudojamos pakavimo struktūros, kuriose yra įdėtųjų numerio lentelių, sistema įrašo faktines turimas atsargas pirminėje numerio lentelėje. Norėdami suaktyvinti faktinių turimų atsargų perkėlimą iš pirminės numerio lentelės į įdėtąsias numerio lenteles, remiantis pakavimo struktūros duomenimis, mobilusis įrenginys turi pateikti meniu elementą, kuris yra pagrįstas darbo kūrimo procesu *Pakavimas su įdėtosiomis numerių lentelėmis*.

## <a name="warehousing-mobile-device-app-processing"></a>Sandėliavimo mobiliojo įrenginio programėlės apdorojimas

Darbuotojui nuskaičius gaunamą numerio lentelės ID, sistema inicijuoja numerio lentelės gavimo procesą. Remiantis šia informacija, numerio lentelės turinys (duomenys gaunami iš ASN) faktiškai užregistruojamas atvežimo rampos vietoje. Toliau nurodytas srautas priklausys nuo jūsų verslo proceso poreikių.

## <a name="work-policies"></a>Darbo strategijos

Kaip ir (pavyzdžiui) *Pranešti kaip baigta* mobiliojo įrenginio meniu elementų procese, numerio lentelės gavimo procesas palaiko kelias darbo eigas, pagrįstas nustatyta sąranka.

### <a name="work-policies-with-work-creation"></a>Darbo strategijos su darbo kūrimu

Kai registruojate gaunamas prekes naudodami darbo strategiją, kuriančią darbą, sistema sugeneruoja ir išsaugo atidėjimo darbo įrašus kiekvienai registracijai. Jei naudojate *Numerio lentelės gavimas ir atidėjimas* darbo procesą, tada registracija ir atidėjimas yra tvarkomi kaip viena operacija naudojant vieną mobiliojo įrenginio meniu elementą. Jei naudojate *Numerio lentelės gavimas* procesą, gavimo ir atidėjimo procesai yra tvarkomi kaip dvi skirtingos sandėlio operacijos, kurių kiekviena turi savo mobiliojo įrenginio meniu elementą.

### <a name="work-policies-without-work-creation"></a>Darbo strategijos be darbo kūrimo

Galite naudotis numerio lentelės gavimo procesu nesukūrę darbo. Jei apibrėžiate darbo strategijas, turinčias darbo užsakymo tipą, skirtą *Perkėlimo gavimas* ir (arba) *Pirkimų užsakymai* ir naudojatės procesu, skirtu *Numerio lentelės gavimas ir (atidėjimas)*, šie du „Warehousing mobile app” procesai nesukuria darbo. Vietoj to, jie tik užregistruos gaunamas faktines atsargas, esančias numerio lentelėje atvežimo gavimo rampoje.

- *Gaunama numerio lentelė*
- *Numerio lentelės gavimas ir atidėjimas*

> [!NOTE]
> - Skyriuje **Atsargų vietos** turite nustatyti bent vieną darbo strategijos vietą. Negalite nurodyti tos pačios kelių darbo strategijų vietos.
> - **Spausdinti etiketes** parinktis, skirta Sandėliavimo mobiliojo įrenginio meniu elementams, nespausdina numerio lentelės etiketėje be darbo kūrimo.

Jei norite, kad šios funkcijos būtų prieinamos jūsų sistemoje, turite įjungti *Numerio lentelės gavimo patobulinimai* funkciją [funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="receive-inventory-on-a-location-that-doesnt-track-license-plates"></a>Gaukite vietos atsargas, kurioje nesekamos numerio lentelės

Galima naudoti sandėlio vietą, priskirtą vietos profiliui, net jei **Naudoti numerio lentelės sekimas** funkcija nėra įjungta. Todėl, kai gaunate atsargas, galite tiesiogiai užregistruoti turimas atsargas vietoje nekurdami darbo.

## <a name="add-mobile-device-menu-items-for-each-receiving-location-in-a-warehouse"></a>Pridėkite mobiliojo įrenginio meniu elementus kiekvienai gavimo vietai sandėlyje

*Numerio lentelės gavimo patobulinimai* funkcija suteikia galimybę gauti bet kurioje sandėlio vietoje, pridedant konkrečiai vietai būdingos numerio lentelės gavimo (ir atidėjimo) meniu elementus į „Warehousing mobile app”. Anksčiau sistema palaikė tik numatytąją vietą, nurodytą kiekvienam sandėliui. Tačiau, kai ši funkcija įjungta, mobiliojo įrenginio meniu elementai, skirti numerio lentelei (ir atidėjimui), dabar suteikia galimybę **Naudoti numatytuosius duomenis** parinktį, leidžiančią pasirinkti pasirinktiną „į” vietą kiekvienam meniu elementui. (Šią pasirinktį jau buvo galima naudoti kai kuriuose kituose meniu elementų tipuose.)

Jei norite, kad šios funkcijos būtų prieinamos jūsų sistemoje, turite įjungti *Numerio lentelės gavimo patobulinimai* funkciją [funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="show-or-skip-the-receiving-summary-page"></a>Gavimo suvestinės puslapio rodymas arba praleidimas

Galite naudoti funkciją *Kontroliuoti, ar mobiliuosiuose įrenginiuose bus rodomas gavimo suvestinės puslapis*, kad numerio lentelės gavimo proceso metu galėtumėte pasinaudoti papildomu išsamiu sandėlio valdymo mobiliųjų įrenginių programėlės srautu.

Kai ši funkcija įjungta, mobiliojo įrenginio meniu elementai, skirti numerio lentelei gauti arba numerio lentelei gauti ir atidėti, teikia parametrą **Rodyti gavimo suvestinės puslapį**. Šis parametras turi toliau pateiktas parinktis.

- **Rodyti išsamią suvestinę** – numerio lentelės gavimo metu darbuotojai matys papildomą puslapį, kuriame bus rodoma visa ASN informacija.
- **Praleisti suvestinę** – darbuotojai nematys visos ASN informacijos. Sandėlio darbuotojai taip pat negalės nustatyti perdavimo kodo arba pridėti išimtis gavimo proceso metu.

Jei norite naudoti šią funkciją, valdymas *, ar rodyti gaunamą suvestinės puslapį mobiliųjų* įrenginių priemonėje, turi būti įjungtas jūsų sistemoje. Kaip ir tiekimo grandinės valdymo versija 10.0.21 ši funkcija įjungiama pagal numatytąjį nustatymą. Kaip ir tiekimo grandinės valdymas 10.0.25 ši funkcija yra privaloma ir jos išjungti negalima. Jei naudojate senesnę nei 10.0.25 versiją, tada administratoriai gali įjungti arba išjungti šią funkciją ieškodami kontrolės, *·*[ar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) rodyti gavimo suvestinės puslapį mobiliųjų įrenginių funkcija funkcijų valdymo darbo srityje.

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Neleisti perkėlimo užsakyme siunčiamų numerio lentelių naudoti ne paskirties sandėlyje

Numerio lentelės gavimo proceso negalima naudoti, jei ASN yra numerio lentelės ID, kuris jau egzistuoja ir turi faktinių turimų duomenų kitoje sandėlio vietoje, nei sandėlio vietoje, kur vyksta numerio lentelės registracija.

Perkėlimo užsakymo scenarijuose, kuriuose tranzito sandėlis neseka numerio lentelių (todėl taip pat neseka kiekvienos numerio lentelės faktinių turimų atsargų), galite naudoti funkciją *Neleisti perkėlimo užsakyme siunčiamų numerio lentelių naudoti ne paskirties sandėlyje*, kad būtų išvengta faktinių turimų numerio lentelių atnaujinimo tranzito metu. Kad ši funkcija būtų galima, *jūsų* sistemoje turi būti įjungta funkcija Neleisti naudoti perkėlimo užsakymo išsiųstų numerio numerių kituose sandėliuose, nei paskirties sandėlio funkcija. Kaip ir tiekimo grandinės valdymas 10.0.25 ši funkcija yra privaloma ir jos išjungti negalima. Jei naudojate senesnę nei 10.0.25 versiją, [tada administratoriai gali įjungti arba išjungti šią funkciją ieškodami jos funkcijų valdymo darbo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) srityje.

Norėdami valdyti funkciją, kai ji pasiekiama, atlikite toliau pateiktus veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.
1. Skirtuko **Bendra** „FastTab“ konteineryje **Numerio lentelės** nustatykite lauką **Tranzito sandėlio numerio lentelių strategijos** į vieną iš toliau pateiktų verčių.

    - **Leisti pakartotinį nesekamų numerio lentelių naudojimą** – sistema veikia taip pat, kaip veikia, kai nepasiekiama funkcija *Neleisti perkėlimo užsakyme siunčiamų numerio lentelių naudoti ne paskirties sandėlyje*. Ši vertė yra numatytasis parametras, kai pirmą kartą suaktyvinate funkciją.
    - **Vengti pakartotinio nesekamų numerio lentelių naudojimo** – kol perkėlimo užsakymas nebus gautas, paskirties sandėlyje bus leidžiami tik turimi atnaujinimai, susieti su siunčiama numerio lentele.

## <a name="more-information"></a>Daugiau informacijos

Daugiau informacijos apie mobiliojo įrenginio meniu elementus žr. [Mobiliųjų įrenginių nustatymas darbui sandėlyje](configure-mobile-devices-warehouse.md).

Daugiau informacijos apie *Pranešti kaip baigta* gamybos scenarijų rasite [Sandėlio darbo strategijų peržiūroje](warehouse-work-policies.md).

Daugiau informacijos apie gaunamos apkrovos valdymą rasite [Sandėlio pirkimų užsakymų gaunamos apkrovos tvarkymas](inbound-load-handling.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]