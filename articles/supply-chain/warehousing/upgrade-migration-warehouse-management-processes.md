---
title: "Produktų ir sandėlio valdymo perkėlimas iš AX 2012 į „Finance and Operations“"
description: "Šioje temoje apžvelgiamos produktų ir sandėlio valdymo perkėlimo parinktys."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 9f618e61cd1cfb7e2abbbc0c9a00b5a06792b4bc
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="migrate-products-and-warehouse-management-from-ax-2012-to-finance-and-operations"></a>Produktų ir sandėlio valdymo perkėlimas iš AX 2012 į „Finance and Operations“

Šioje temoje pateikiama produkto ir sandėlio valdymo perkėlimo parinkčių apžvalga programoje „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidime.

<a name="introduction"></a>Įžanga
------------

Naujinant „Finance and Operations“ produktai blokuojami, jeigu jie susiję su saugojimo dimensijų grupe, turinčia parametrų, kurie neatitinka „Finance and Operations“ saugojimo dimensijų grupės parametrų reikalavimų. Tačiau atnaujinę galite naudoti perkėlimo parinkčių rinkinį procese **Keisti prekių saugojimo dimensijų grupę** norėdami atblokuoti produktus, kurie buvo užblokuoti naujinant. Tada galite apdoroti tų produktų operacijas. Kai kurios jūsų prekės jau gali būti susietos su saugojimo dimensijų grupėmis kur Teritorijos, Sandėlio ir Vietos atsargų dimensijos yra aktyvios ir faktiškai sekamos. Tokiu atveju galite naudoti procesą **Keisti prekių saugojimo dimensijų grupę**, kad tas prekes būtų galima naudoti sandėlio valdymo procesuose. Ši funkcija yra naudinga, jei sandėlio valdymo funkcijas norite naudoti esamoms prekėms.

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a>Naujinimas į „Finance and Operations“, kai naudojama AX 2012 R3 WMSII
„Finance and Operations“ nebepalaiko senstelėjusio **WMSII** modulio iš „Microsoft Dynamics AX 2012“. Vietoj to galite naudoti naują **Sandėlio valdymo** modulį. Ankstesnėse versijose vietos ir padėklo ID atsargų dimensijas buvo galima pasirinkti finansinėms atsargoms. Tačiau atnaujinus padėklo ID atsargų dimensija nebegali būti įjungta finansinėms atsargoms. Visi produktai, susiję su saugojimo dimensijų grupe, kuri naudoja padėklo ID atsargų dimensiją, bus užblokuoti ir nebus apdorojami.

### <a name="enabling-items-in-finance-and-operations"></a>Prekių įgalinimas naudojant „Finance and Operations“

Naudojant „Finance and Operations“ prekės, kurios bus naudojamos sandėlio valdymo procesuose, turi būti susietos su saugojimo dimensijų grupe, kur pasirinktas parametras **Naudoti sandėlio valdymo procesus**. Pasirinkus šį parametrą taps aktyvios teritorijos, sandėlio, atsargų būsenos, vietos ir numerio lentelės atsargų dimensijos. Galite pakeisti į šio tipo saugojimo dimensijų grupę tik prekėms, kurios jau susietos su saugojimo dimensijų grupėmis, kur aktyvi vietos atsargų dimensija.

### <a name="items-that-are-blocked-for-inventory-updates"></a>Prekės, kurios blokuojamos atsargų naujinimuose

Norėdami peržiūrėti išleistus produktus, kurie buvo užblokuoti naujinant ir negali būti apdoroti, spustelėkite **Atsargų valdymas** &gt; **Sąranka** &gt; **Atsargos** &gt; **Prekės, užblokuotos naujinant atsargas**.

### <a name="reapplying-blocked-products"></a>Užblokuotų produktų pakartotinis pritaikymas

Norėdami atblokuoti produktus, kurie buvo užblokuoti naujinant, turite pasirinkti naują produktų saugojimo dimensijų grupę. Atminkite, kad galite pakeisti saugojimo dimensijų grupę, net jei yra atvirų atsargų operacijų. Norėdami naudoti prekes, kurios buvo užblokuotos naujinant, turite dvi parinktis:

-   Pakeisti prekės saugojimo dimensijų grupę į saugojimo dimensijų grupę, kuri naudoja tik teritorijos, sandėlio ir vietos atsargų dimensijas. Dėl šio pakeitimo padėklo ID atsargų dimensija nebenaudojama.
-   Pakeiskite prekės saugojimo dimensijų grupę į saugojimo dimensijų grupę, kuri naudoja sandėlio valdymo procesus. Dėl šio pakeitimo dabar naudojama numerio lentelės atsargų dimensija.

### <a name="migration-processes"></a>Perkėlimo procesai

Naudojant „Finance and Operations“ prekių sekimas yra sandėlio valdymo procesų dalis. Šiuose procesuose visi sandėliai ir jų vietos turi būti susieti su vietos šablonu. Teoriškai, jei norite naudoti sandėlio valdymo procesus, turi būti tvarkomi du procesai:

-   Esami sandėliai turi būti įgalinti naudoti sandėlio valdymo procesus.
-   Esami išleisti produktai turi būti susieti su nauja saugojimo dimensijų grupe, naudojančia sandėlio valdymo procesus.

Jei šaltinio saugojimo dimensijų grupės naudoja padėklo ID atsargų dimensiją, turimų atsargų vietos, kurios naudoja padėklo ID atsargų dimensiją, turi būti susietos su vietos šablonu, kur pasirinktas parametras **Naudoti numerio lentelės sekimą**. Jei esami sandėliai neturi būti įgalinti naudoti sandėlio valdymo procesų, galite pakeisti turimų atsargų saugojimo dimensijų grupes į grupes, kurios tvarko tik teritorijos, sandėlio ir vietos atsargų dimensijas.

### <a name="using-the-warehouse-management-processes"></a>Sandėlio valdymo procesų naudojimas

Prieš naudojant išleistus produktus modulyje **Sandėlio valdymas** produktai turi naudoti saugojimo dimensijų grupę, kurioje pasirinktas parametras **Naudoti sandėlio valdymo procesus**.

#### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Įgalinti sandėlius naudoti sandėlio valdymo procesus

1.  Sukurkite bent vieną naują vietos šabloną.
2.  Spustelėkite **Sandėlio valdymas** &gt; **Sąranka** &gt; **Įgalinti sandėlio valdymo procesus** &gt; **Įgalinti sandėlio nustatymus**.
3.  Puslapyje **Įgalinti sandėlio nustatymus** įtraukite sandėlius, kurie turėtų būti įgalinti. Šį veiksmą galite atlikti tiesiog puslapyje arba naudodami „Microsoft Office“ integraciją.
4.  Priskirkite vietos šabloną visoms vietoms. Šį veiksmą galite lengvai atlikti „Microsoft Office“ integraciją tiesiog naudodami puslapyje. Galite eksportuoti ir importuoti duomenis arba naudoti duomenų objekto apdorojimą dalyje [Duomenų valdymas](../../dev-itpro/data-entities/data-entities.md).
5.  Patikrinkite pakeitimus. Tikrinimo proceso metu bus atliekami įvairūs duomenų vientisumo tikrinimai. Vykdant didesnį naujinimo procesą, iškylančios problemos gali būti pakoreguotos diegiant šaltinį. Šiuo atveju reikės papildomo duomenų naujinimo.
6.  Apdorokite pakeitimus.

#### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Pakeiskite prekių saugojimo dimensijų grupę, kad ji naudotų sandėlio valdymo procesus

1.  Sukurkite naują **Atsargų būsenos** vertę ir priskirkite ją kaip **Numatytosios atsargų būsenos ID** vertę **Sandėlio valdymo parametruose**.
2.  Sukurkite naują saugojimo dimensijų grupę, kur pasirinktas parametras **Naudoti sandėlio valdymo procesus**.
3.  Puslapyje **Rezervavimo hierarchija** nustatykite naują rezervavimo hierarchiją pagal prekės saugojimo ir sekimo dimensijų grupes.
4.  Sukurkite vieną ar daugiau vienetų sekų grupių, kuriose yra tokių pačių vienetų, naudojamų prekių atsargų vienetams.
5.  Spustelėkite **Sandėlio valdymas** &gt; **Nustatymas** &gt; **Įgalinti sandėlio valdymo procesus** &gt; **Pakeisti prekių saugojimo dimensijų grupę**.
6.  Puslapyje **Pakeisti prekių saugojimo dimensijų grupę** įtraukite prekių numerius, saugojimo dimensijų grupes ir vienetų sekų grupes. Šį veiksmą galite atlikti tiesiog puslapyje, naudodami „Microsoft Office“ integraciją arba duomenų objekto procesą dalyje [Duomenų valdymas](../../dev-itpro/data-entities/data-entities.md).
7.  Patikrinkite pakeitimus. Tikrinimo proceso metu bus atliekami įvairūs duomenų vientisumo tikrinimai. Vykdant didesnį naujinimo procesą, iškylančios problemos gali būti pakoreguotos diegiant šaltinį. Šiuo atveju reikės papildomo duomenų naujinimo.
8.  Apdorokite pakeitimus. Visų atsargų dimensijų atnaujinimas gali šiek tiek užtrukti. Galite stebėti eigą naudodami paketines užduotis.



