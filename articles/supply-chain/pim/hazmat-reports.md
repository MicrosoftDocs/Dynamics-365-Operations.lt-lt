---
title: Pavojingų medžiagų užklausos ir ataskaitos
description: Šioje temoje paaiškinama kaip dirbti su įvairiomis ataskaitomis, susijusiomis su pavojingomis medžiagomis. Dauguma šių ataskaitų reikalingos tam, kad Jūs atitiktumėte įvairias pavojingų medžiagų nuostatas siuntimo ir saugojimo metu.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 188c339ddf5f5c2488133924e9a0288f218f495c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433629"
---
# <a name="hazardous-materials-inquiries-and-reports"></a>Pavojingų medžiagų užklausos ir ataskaitos

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

„Microsoft Dynamics 365 Supply Chain Management” pateikia įvairias ataskaitas, susijusias su pavojingomis medžiagomis. Dauguma šių ataskaitų reikalingos tam, kad Jūs atitiktumėte įvairias pavojingų medžiagų nuostatas siuntimo ir saugojimo metu.

Visos šios ataskaitos, išskyrus **Daugiamodalinių pavojingų prekių** ataskaitą, naudoja pristatymo režimą, apibrėžtą siuntai rasti nuostatą, kuri turėtų būti naudojama prekių siuntimo teksto spausdinimui. Pristatymo režimas yra susietas su siuntimo vežėju ir vežėjo paslauga. Taigi, turite nustatyti siuntimo vežėją ir vežėjo paslaugą ir susieti juos su pristatymo režimu. Pristatymo režimas yra susijęs su pavojingų medžiagų nuostata.

Ši iliustracija rodo veiksmų seką, kuomet sistema generuoja pavojingų medžiagų ataskaitas.

![Pavojingų medžiagų ataskaitų veiksmų seka](media/hazmat-report-sequence.png "Veiklų seka pavojingų medžiagų ataskaitoms")

## <a name="set-up-hazardous-materials-reporting"></a><a name="set-up"></a>Pavojingų medžiagų ataskaitų nustatymas

Įprastai, jei siunčiate prekes, kuriose yra pavojingų medžiagų, privalote sugeneruoti tam tikras ataskaitas, kad užtikrintumėte saugumą ir atitiktumėte pavojingų medžiagų nuostatas. Ataskaitų nustatymui, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.
2. Atidarykite **Ataskaitų** skirtuką. „FastTab” **Pavojingų medžiagų ataskaitų parametras** nustatykite šiuos laukus.

    | Skyrius | Laukas | Aprašas |
    |---|---|---|
    | Daugiamodalinės pavojingos prekės | Nuostatos kodas | Pasirinkite nuostatą, kuri turi būti naudojama, kai ataskaita **Daugiamodalinės pavojingos prekės** yra generuojama. |
    | Pavojingų medžiagų atsargų limitai | Nuostatos kodas | Pasirinkite nuostatą, kuri turi būti naudojama, kai atsargų limitai yra vertinami. |
    | Prekių vežimas sausumos transportu | CMR grupės produktas | CMR reiškia „kancerogenines, mutagenines ir toksiškas reprodukcijai medžiagas.” Nustatykite šią parinktį kaip **Taip** sukonfigūruoti sistemą atspaudinti tam tikrus perspėjimus ir pranešimus, susijusius su šių medžiagų tvarkymu. |
    | Prekių vežimas sausumos transportu | Pavojingos medžiagos grupės aprašas | Įveskite tam tikrų perspėjimų, susijusių su CMR ir prekių vežimu sausumos transportu, tekstą. Šis tekstas bus įtrauktas į ataskaitą. |
    | Siuntėjų deklaracija | Perspėjimas | Įveskite perspėjamojo pranešimo tekstą, kuris turi būti atspausdintas siuntėjų deklaracijos formoje (pavyzdžiui, „Perspėjimas: Pavojingos prekės, Degios”). |
    | Siuntėjų deklaracija | Poraštės deklaracija | Įveskite pranešimo tekstą, kuris turi būti atspaudintas, siuntimo deklaracijos dokumento pabaigoje. |
    | Pavojingų prekių ataskaitos kalba | Pavojingų prekių vietinės ataskaitos kalba | Pasirinkite numatytąją kalbą pavojingų medžiagų ataskaitoms, siejamoms su vietiniais siuntimais. |
    | Pavojingų prekių ataskaitos kalba | Pavojingų prekių eksporto ataskaitos kalba | Pasirinkite numatytąją kalbą pavojingų medžiagų ataskaitoms, siejamoms su tarptautiniais siuntimais. |

## <a name="hazardous-materials-report"></a>Pavojingų medžiagų ataskaita

Ataskaita **Pavojingos medžiagos** rodo sąrašą visų prekių, kurios buvo nustatytos ir apibrėžtos taip, kad turėtų informaciją apie pavojingas prekes. Galite naudoti šią ataskaitą informacijos, kurią privalote tvarkyti, stebėjimui ir peržiūrėjimui. Ataskaitos puslapis rodo ribotą pavojingų medžiagų sąrankos laukų pasirinkimą. Tačiau galite jį suasmeninti pridėdami papildomus laukus pagal pareikalavimą.

Norėdami peržiūrėti šią ataskaitą, eikite į **Produkto informacijos valdymas \> Užklausos ir ataskaitos \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingos medžiagos**.

## <a name="hazardous-material-stock-limit-report"></a><a name="stock-limit-report"></a>Pavojingų medžiagų atsargų limitų ataskaita

Ataskaita **Pavojingų medžiagų atsargų limitas** leidžia Jums stebėti pavojingų medžiagų atsargų lygius Jūsų sandėlio vietovėse, kad užtikrintumėte, jog atsargos atitinka nustatytus saugius limitus. Šie limitai yra nustatyti pagal limitus, apibrėžtus kiekvienam išleistam produktui.

Norėdami peržiūrėti šią ataskaitą, eikite į **Produkto informacijos valdymas \> Užklausos ir ataskaitos \> Pavojingų medžiagų siuntimo dokumentacija \> Pavojingų medžiagų atsargų limitai**.

Norėdami gauti daugiau informacijos apie tai, kaip nustatyti atsargų limitus išleistam produktui, žr. [Pavojingų produktų atsargų limitų nustatymas](hazmat-items.md#stock-limits).

Nuostata, naudojama atsargų limitams yra apibrėžta **Sandėlio valdymo parametrai** puslapyje. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**, tada skirtuko **Ataskaitos** dalyje **Pavojingų medžiagų atsargų limitas**, nurodykite nuostatos kodą. Daugiau informacijos žr. skyrių [Pavojingų medžiagų ataskaitų nustatymas,](#set-up) pateiktą anksčiau šioje temoje.

## <a name="verified-gross-mass-report"></a>Patvirtintos bendros masės ataskaita

Ataskaita **Patvirtinta bendra masė** leidžia Jums atspaudinti informaciją apie siuntos svorį.

Norėdami sugeneruoti ir atspaudinti šią ataskaitą, eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos** ir atidarykite reikiamą siuntą. Tada veiksmų srities skirtuko **Siuntos** grupėje **Pavojingų medžiagų dokumentas** pasirinkite **Patvirtinta bendra masė**.

## <a name="multimodal-dangerous-goods-report"></a>Daugiamodalinių pavojingų prekių ataskaita

Ataskaita **Daugiamodalinės pavojingos prekės** pateikiama toms siuntoms, kurios turi būti vežamos naudojant kelis transportavimo metodus. Įprastai ji naudojama tuomet, kai siunta pirma yra transportuojama sausuma, o vėliau – jūra.

Norėdami sugeneruoti ir atspaudinti šią ataskaitą, eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos** ir atidarykite reikiamą siuntą. Tada veiksmų srities skirtuko **Siuntos** grupėje **Pavojingų medžiagų dokumentas** pasirinkite **Daugiamodalinės pavojingos prekės**.

Kai generuojate šią ataskaitą, informacija yra išsaugoma, kad galėtumėte ją redaguoti ir (arba) perspausdinti ataskaitą, jeigu tai reikalinga. Norėdami redaguoti sugeneruotą ataskaitą, eikite į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Pavojingų medžiagų siuntimo dokumentacija \> Daugiamodalinės pavojingos medžiagos** ir sąraše raskite reikiamą ataskaitą. Baigę redaguoti turinį pagal reikalavimus, veiksmų srityje pasirinkite **Spausdinti** ataskaitos atspausdinimui.

## <a name="shippers-declaration-report"></a>Siuntėjų deklaracijos ataskaita

Ataskaita **Siuntėjų deklaracija** leidžia atspaudinti informaciją, susijusią su medžiagų, įtrauktų į siuntą, deklaracija.

Norėdami sugeneruoti ir atspaudinti šią ataskaitą, eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos** ir atidarykite reikiamą siuntą. Tada veiksmų srities skirtuko **Siuntos** grupėje **Pavojingų medžiagų dokumentas** pasirinkite **Siuntėjų deklaracija**.

## <a name="carriage-of-merchandise-by-road-report"></a>Prekių vežimo sausumos transportu ataskaita

Ataskaita **Prekių vežimas sausumos transportu** panaši į važtaraštį, tačiau įprastai naudojama sausumos transportavimui Europoje pagal sutartį, susijusią su tarptautinio pavojingų prekių pervežimo sausumos transportu (ADR) nuostatomis. Ši ataskaita naudoja siuntimo spausdinimo tekstą prekei, nebent nustatote **Pavojingos medžiagos grupės aprašas** lauką **Sandėlio valdymo parametrai** puslapyje.

Norėdami sugeneruoti ir atspaudinti šią ataskaitą, eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos** ir atidarykite reikiamą siuntą. Tada veiksmų srities skirtuko **Siuntos** grupėje **Pavojingų medžiagų dokumentas** pasirinkite **Prekių vežimas sausumos transportu**.

Kai generuojate šią ataskaitą, informacija yra išsaugoma, kad galėtumėte ją redaguoti ir (arba) perspausdinti ataskaitą, jeigu tai reikalinga. Norėdami redaguoti sugeneruotą ataskaitą, eikite į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Pavojingų medžiagų siuntimo dokumentacija \> Prekių vežimas sausumos transportu** ir sąraše raskite reikiamą ataskaitą. Baigę redaguoti turinį pagal reikalavimus, veiksmų srityje pasirinkite **Spausdinti** ataskaitos atspausdinimui.

## <a name="shipment-summary-report"></a>Siuntos suvestinės ataskaita

Ataskaita **Siuntos suvestinė** pateikia informaciją, apibendrintą pagal transportavimo kategoriją, susijusią su išleistoms prekėmis.

Norėdami sugeneruoti ir atspaudinti šią ataskaitą, eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos** ir atidarykite reikiamą siuntą. Tada veiksmų srities skirtuko **Siuntos** grupėje **Pavojingų medžiagų dokumentas** pasirinkite **Siuntos suvestinė**.

## <a name="bill-of-lading-report"></a>Važtaraščio ataskaita

Kai pavojingų medžiagų funkcija yra įjungta Jūsų sistemoje, ataskaitoje **važtaraštis** yra **Pavojingos medžiagos** stulpelis, kuriame nurodoma, ar krovinyje yra pavojingų medžiagų. Ši ataskaita, kaip įprastai, yra prieinama **Visi kroviniai** puslapyje.

## <a name="packing-list-report"></a>Pakavimo sąrašo ataskaita

Kai pavojingų medžiagų funkcija yra įjungta Jūsų sistemoje, pakavimo sąrašuose yra papildoma informacija, susijusi su siuntimo spausdinimo tekstu prekei. Ši ataskaita, kaip įprastai, yra prieinama **Visi kroviniai** puslapyje.
