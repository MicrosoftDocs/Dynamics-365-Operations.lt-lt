---
title: Atnaujinti sandėlio valdymą iš „Microsoft Dynamics AX 2012“ į Tiekimo grandinės valdymą
description: Šioje temoje apžvelgiamos produktų ir sandėlio valdymo perkėlimo parinktys.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45d9809d4bbf1b5a68c3f799ce5d51f9709d276b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970286"
---
# <a name="upgrade-warehouse-management-from-microsoft-dynamics-ax-2012-to-supply-chain-management"></a>Atnaujinti sandėlio valdymą iš „Microsoft Dynamics AX 2012“ į Tiekimo grandinės valdymą 


[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama proceso naujinimo iš „Microsoft Dynamics AX 2012 R3“ su WMSII moduliu į Tiekimo grandinės valdymą apžvalga.

Tiekimo grandinės valdymas nebepalaiko senstelėjusio **WMSII** modulio iš „Microsoft Dynamics AX 2012“. Vietoj to galite naudoti modulį **Sandėlio valdymas**. WMSII modulyje galima pasirinkti finansų atsargų vietos ir padėklo ID atsargų dimensijas, tačiau padėklo ID atsargų dimensijos negalima naudoti Tiekimo grandinės valdymo finansų atsargoms.

Naujinant nustatomi, pažymimi kaip užblokuoti ir naujinimo metu neapdorojami visi su saugojimo dimensijos grupe, kurioje naudojamos padėklo ID atsargos, susieti produktai.

## <a name="upgrading-to-supply-chain-management-when-ax-2012-r3-wmsii-is-used"></a>Atnaujinama į Tiekimo grandinės valdymą, kai naudojama AX 2012 R3 WMSII
Atnaujinę galite naudoti parinkčių rinkinį formoje **Keisti prekių saugojimo dimensijų grupę**, kad atblokuotumėte produktus, kurie buvo užblokuoti naujinant, tada apdoroti šių produktų operacijas.

### <a name="enabling-items-in-supply-chain-management"></a>Tiekimo grandinės valdymo elementų įgalinimas 
Šis keitimas reikalingas, nes prekių sekimas Tiekimo grandinės valdyme yra sandėlio valdymo procesų dalis. Šiuose procesuose visi sandėliai ir jų vietos turi būti susieti su vietos šablonu. Jei norite naudoti sandėlio valdymo procesus, turite atlikti toliau nurodytas konfigūracijas.
-   Esami sandėliai turi būti įgalinti naudoti sandėlio valdymo procesus 
-   Esami išleisti produktai turi būti susieti su saugojimo dimensijų grupe, naudojančia sandėlio valdymo procesus 

Jei šaltinio saugojimo dimensijų grupės naudoja padėklo ID atsargų dimensiją, turimų atsargų vietos, kurios naudoja padėklo ID atsargų dimensiją, turi būti susietos su vietos šablonu, kuriame pasirinktas parametras **Naudoti numerio lentelės sekimą**. Jei esami sandėliai neturi būti įgalinti naudoti sandėlio valdymo procesų, galite pakeisti turimų atsargų saugojimo dimensijų grupes į grupes, kurios tvarko tik teritorijos, sandėlio ir vietos atsargų dimensijas. 

> [!NOTE] 
>  Elementų saugojimo dimensijų grupę galite pakeisti net jei yra atvirų atsargų operacijų.

## <a name="find-products-that-were-blocked-because-of-pallet-id"></a>Raskite produktus, užblokuotus dėl padėklo ID
Norėdami peržiūrėti išleistus produktus, kurie buvo užblokuoti naujinant ir negali būti apdoroti, spustelėkite **Atsargų valdymas** &gt; **Sąranka** &gt; **Atsargos** &gt; **Prekės, užblokuotos naujinant atsargas**.

## <a name="change-storage-dimension-group-for-blocked-products"></a>Pakeiskite užblokuotų produktų saugojimo dimensijų grupę 
 
Kad elementą būtų galima naudoti kaip sandėlio valdymo proceso dalį, jis turi būti susietas su saugojimo dimensijos grupe, kurioje yra aktyvi vietos atsargų dimensija ir pasirinktas parametras **Naudoti sandėlio valdymo procesus**. Pasirinkus šį parametrą taps aktyvios teritorijos, sandėlio, atsargų būsenos, vietos ir numerio lentelės atsargų dimensijos.

Norėdami atblokuoti produktus, kurie buvo užblokuoti naujinant, turite pasirinkti naują produktų saugojimo dimensijų grupę. Atminkite, kad galite pakeisti saugojimo dimensijų grupę, net jei yra atvirų atsargų operacijų. Norėdami naudoti prekes, kurios buvo užblokuotos naujinant, turite dvi parinktis:

-   Pakeisti prekės saugojimo dimensijų grupę į saugojimo dimensijų grupę, kuri naudoja tik teritorijos, sandėlio ir vietos atsargų dimensijas. Dėl šio pakeitimo padėklo ID atsargų dimensija nebenaudojama.
-   Pakeiskite prekės saugojimo dimensijų grupę į saugojimo dimensijų grupę, kuri naudoja sandėlio valdymo procesus. Dėl šio pakeitimo dabar naudojama numerio lentelės atsargų dimensija.

## <a name="configure-warehouse-management-processes"></a>Sukonfigūruokite sandėlio valdymo procesus
Prieš naudojant išleistus produktus modulyje **Sandėlio valdymas** produktai turi naudoti saugojimo dimensijų grupę, kurioje pasirinktas parametras **Naudoti sandėlio valdymo procesus**.

### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Įgalinti sandėlius naudoti sandėlio valdymo procesus

1.  Sukurkite bent vieną naują vietos šabloną.
2.  Spustelėkite **Sandėlio valdymas** &gt; **Sąranka** &gt; **Įgalinti sandėlio valdymo procesus** &gt; **Įgalinti sandėlio nustatymus**.
3.  Puslapyje **Įgalinti sandėlio nustatymus** įtraukite sandėlius, kurie turėtų būti įgalinti. Šį veiksmą galite atlikti tiesiog puslapyje arba naudodami „Microsoft Office“ integraciją.
4.  Priskirkite vietos šabloną visoms vietoms. Šį veiksmą galite lengvai atlikti „Microsoft Office“ integraciją tiesiog naudodami puslapyje. Galite eksportuoti ir importuoti duomenis arba naudoti duomenų objekto apdorojimą dalyje [Duomenų valdymas](../../dev-itpro/data-entities/data-entities.md).
5.  Patikrinkite pakeitimus. Tikrinimo proceso metu bus atliekami įvairūs duomenų vientisumo tikrinimai. Vykdant didesnį naujinimo procesą, iškylančios problemos gali būti pakoreguotos diegiant šaltinį. Šiuo atveju reikės papildomo duomenų naujinimo.
6.  Apdorokite pakeitimus.

### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Pakeiskite prekių saugojimo dimensijų grupę, kad ji naudotų sandėlio valdymo procesus

1.  Sukurkite naują **Atsargų būsenos** vertę ir priskirkite ją kaip **Numatytosios atsargų būsenos ID** vertę **Sandėlio valdymo parametruose**.
2.  Sukurkite naują saugojimo dimensijų grupę, kur pasirinktas parametras **Naudoti sandėlio valdymo procesus**.
3.  Puslapyje **Rezervavimo hierarchija** nustatykite naują rezervavimo hierarchiją pagal prekės saugojimo ir sekimo dimensijų grupes.
4.  Sukurkite vieną ar daugiau vienetų sekų grupių, kuriose yra tokių pačių vienetų, naudojamų prekių atsargų vienetams.
5.  Spustelėkite **Sandėlio valdymas** &gt; **Nustatymas** &gt; **Įgalinti sandėlio valdymo procesus** &gt; **Pakeisti prekių saugojimo dimensijų grupę**.
6.  Puslapyje **Pakeisti prekių saugojimo dimensijų grupę** įtraukite prekių numerius, saugojimo dimensijų grupes ir vienetų sekų grupes. Šį veiksmą galite atlikti tiesiog puslapyje, naudodami „Microsoft Office“ integraciją arba duomenų objekto procesą dalyje [Duomenų valdymas](../../dev-itpro/data-entities/data-entities.md).
7.  Patikrinkite pakeitimus. Tikrinimo proceso metu bus atliekami įvairūs duomenų vientisumo tikrinimai. Vykdant didesnį naujinimo procesą, iškylančios problemos gali būti pakoreguotos diegiant šaltinį. Šiuo atveju reikės papildomo duomenų naujinimo.
8.  Apdorokite pakeitimus. Visų atsargų dimensijų atnaujinimas gali šiek tiek užtrukti. Galite stebėti eigą naudodami paketines užduotis.
