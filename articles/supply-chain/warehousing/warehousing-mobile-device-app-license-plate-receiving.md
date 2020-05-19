---
title: Numerio lentelės gavimas naudojant sandėliavimo programą
description: Šioje temoje paaiškinama, kaip nustatyti sandėliavimo programą, kad faktinių atsargų gavimui būtų palaikomas numerio lentelės gavimo proceso naudojimas.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346381"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a>Numerio lentelės gavimas naudojant sandėliavimo programą

Šioje temoje paaiškinama, kaip nustatyti sandėliavimo programą, kad faktinių atsargų gavimui būtų palaikomas numerio lentelės gavimo proceso naudojimas.

Šią funkciją galite naudoti norėdami greitai įrašyti gaunamų atsargų gavimą, susijusį su išankstiniu siuntimo pranešimu (ASN). Sistema automatiškai sukuria ASN, kai sandėlio valdymo procesai naudojami perkėlimo užsakymui siųsti. Pirkimo užsakymo procese ASN gali būti įrašytas rankiniu būdu arba automatiškai importuotas naudojant gaunamo ASN duomenų objekto procesą.

ASN duomenys yra susieti su kroviniais ir siuntomis naudojant *pakavimo struktūras*, kurių padėkluose (pirminės numerio lentelės) gali būti saugyklos (įdėtosios numerio lentelės).

> [!NOTE]
> Kad būtų sumažintas atsargų operacijų skaičius, kai naudojamos pakavimo struktūros, kuriose yra įdėtųjų numerio lentelių, sistema įrašo faktines turimas atsargas pirminėje numerio lentelėje. Norėdami suaktyvinti faktinių turimų atsargų perkėlimą iš pirminės numerio lentelės į įdėtąsias numerio lenteles, remiantis pakavimo struktūros duomenimis, mobilusis įrenginys turi pateikti meniu elementą, kuris yra pagrįstas darbo kūrimo procesu *Pakavimas su įdėtosiomis numerių lentelėmis*.

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a>Gavimo suvestinės puslapio rodymas arba praleidimas

Galite naudoti funkciją *Kontroliuoti, ar mobiliuosiuose įrenginiuose bus rodomas gavimo suvestinės puslapis*, kad numerio lentelės gavimo proceso metu galėtumėte pasinaudoti papildomu išsamiu sandėliavimo programos srautu.

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *sandėlio valdymas*
- **Funkcijos pavadinimas:** *Kontroliuoti, ar mobiliuosiuose įrenginiuose bus rodomas gavimo suvestinės puslapis*

Kai ši funkcija įjungta, mobiliojo įrenginio meniu elementai, skirti numerio lentelei gauti arba numerio lentelei gauti ir atidėti, teikia parametrą **Rodyti gavimo suvestinės puslapį**. Šis parametras turi toliau pateiktas parinktis.

- **Rodyti išsamią suvestinę** – numerio lentelės gavimo metu darbuotojai matys papildomą puslapį, kuriame bus rodoma visa ASN informacija.
- **Praleisti suvestinę** – darbuotojai nematys visos ASN informacijos. Sandėlio darbuotojai taip pat negalės nustatyti perdavimo kodo arba pridėti išimtis gavimo proceso metu.

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Neleisti perkėlimo užsakyme siunčiamų numerio lentelių naudoti ne paskirties sandėlyje

Numerio lentelės gavimo proceso negalima naudoti, jei ASN yra numerio lentelės ID, kuris jau egzistuoja ir turi faktinių turimų duomenų ne sandėlio, kur vyksta numerio lentelės registravimas, vietoje.

Perkėlimo užsakymo scenarijuose, kuriuose tranzito sandėlis neseka numerio lentelių (todėl taip pat neseka kiekvienos numerio lentelės faktinių turimų atsargų), galite naudoti funkciją *Neleisti perkėlimo užsakyme siunčiamų numerio lentelių naudoti ne paskirties sandėlyje*, kad būtų išvengta faktinių turimų numerio lentelių atnaujinimo tranzito metu.

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *sandėlio valdymas*
- **Funkcijos pavadinimas:** *Neleisti perkėlimo užsakyme siunčiamų numerio lentelių naudoti ne paskirties sandėlyje*

Norėdami valdyti funkciją, kai ji pasiekiama, atlikite toliau pateiktus veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.
1. Skirtuko **Bendra** „FastTab“ konteineryje **Numerio lentelės** nustatykite lauką **Tranzito sandėlio numerio lentelių strategijos** į vieną iš toliau pateiktų verčių.

    - **Leisti pakartotinį nesekamų numerio lentelių naudojimą** – sistema veikia taip pat, kaip veikia, kai nepasiekiama funkcija *Neleisti perkėlimo užsakyme siunčiamų numerio lentelių naudoti ne paskirties sandėlyje*. Ši vertė yra numatytasis parametras, kai pirmą kartą suaktyvinate funkciją.
    - **Vengti pakartotinio nesekamų numerio lentelių naudojimo** – kol perkėlimo užsakymas nebus gautas, paskirties sandėlyje bus leidžiami tik turimi atnaujinimai, susieti su siunčiama numerio lentele.

## <a name="more-information"></a>Daugiau informacijos

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

Daugiau informacijos apie mobiliojo įrenginio meniu elementus žr. [Mobiliųjų įrenginių nustatymas darbui sandėlyje](configure-mobile-devices-warehouse.md).
