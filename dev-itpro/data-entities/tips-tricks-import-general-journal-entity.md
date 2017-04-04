---
title: "Geriausios praktikos importavimas naudojant bendrąjį žurnalą subjektas kvitus"
description: "Šioje temoje pateikta patarimų duomenų importavimo į bendrąjį žurnalą naudojant bendrojo žurnalo subjektas."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 81a52acd1d9baa12fcfe9d848441901894fa5682
ms.lasthandoff: 03/31/2017


---

# <a name="best-practices-for-importing-vouchers-using-the-general-journal-entity"></a>Geriausios praktikos importavimas naudojant bendrąjį žurnalą subjektas kvitus

Šioje temoje pateikta patarimų duomenų importavimo į bendrąjį žurnalą naudojant bendrojo žurnalo subjektas.  

Galite naudoti bendrąjį žurnalą subjektas importuoti kvitus, kurie turi sąskaitą arba kompensuoti abonemento tipą, **knygos, pirkėjas, tiekėjas ar banko**. Kvitas gali būti pateikiami vienoje eilutėje, naudojant tiek **į** lauko ir **korespondentinė sąskaita** lauko, arba kaip kelių eilučių kvito, tik jeigu į **į** laukas naudojamas (ir **korespondentinė sąskaita** yra tuščias kiekvienoje eilutėje). Bendrojo žurnalo subjektas nepalaiko kiekvieno sąskaitos tipo. Jeigu reikalingi skirtingi sąskaitų tipų deriniai, geriau naudoti kitus objektus. Pavyzdžiui, Norėdami importuoti projekto operacijos, naudoti projekto išlaidų žurnalo subjektas. Kiekvienas subjektas yra sukurta palaikyti konkrečių scenarijų, kuris reiškia papildomus laukus galima subjektai scenarijuose, o ne subjektai skirtingų scenarijų.

## <a name="setup"></a>Sąranka
Prieš importuodami iš bendrojo žurnalo asmuo, patvirtinti tokį nustatymą:

-   **Numeracijos nustatymo už žurnalo paketo numeris** - pagal numatytuosius nustatymus, kai importuojate naudojant bendrąjį žurnalą subjektui, žurnalo paketo numeris naudoja numeraciją, kuri yra nurodyta DK parametrai. Jei nustatysite žurnalo paketo numerio numeracijos parinktį **Neautomatinis**, numatytasis numeris nebus taikomas. Šis nustatymas nepalaikomas.
-   **Finansinės dimensijos konfigūracija** -kiekviena organizacija turi apibrėžti finansinės dimensijos kai organizacijos importuoti operacijas. Tokia tvarka yra nustatyta į **knygos matmenys integracijos** formatas, ne **DK**&gt;**sąskaitų**&gt;**matmenys**&gt;**finansinės dimensijos konfigūracija, apimanti taikomąsias programas**&gt;**pasirinkite duomenų subjektų**. Importuojamos DK sąskaitos segmentų tvarka turi būti ta tokia pati. Kitaip importavimo metu įvyks klaida.

## <a name="general-journal-entity-setup"></a>Objekto Bendrasis žurnalas nustatymas
Dviejų parametrų srityje duomenų valdymo poveikio, kaip taikoma Numatytoji žurnalo paketo numeris ir kvito numeris:

-   **Tvarkymo pagrindu sukurti** (ant duomenų subjektas)
-   **Automatiškai sugeneruotas** (ant lauko atvaizdavimas)

Tolesniuose skyriuose apibūdinama, kaip šie parametrai veikia, ir paaiškinama, kaip generuojami žurnalo paketo numeriai ir kvitų numeriai.

### <a name="journal-batch-number"></a>Žurnalų paketo numeris

-   Objekto Bendrasis žurnalas nustatymas **Rinkiniu pagrįstas apdorojimas** generuojant žurnalo paketo numerius įtakos neturi.
-   Jei laukas **Žurnalo paketo numeris** nustatytas į parinktį **Automatiškai sugeneruotas**, sukuriamas naujas kiekvienos importuojamos eilutės žurnalo paketo numeris. Taip daryti nerekomenduojama. Nustatymą **Automatiškai sugeneruotas** galima rasti importavimo projekto dalie **Peržiūrėti schemą** skirtuke **Susiejimo informacija**.
-   Jei laukas **Žurnalo paketo numeris** nėra nustatytas į parinktį **Automatiškai sugeneruotas**, žurnalo paketo numeris, kaip nurodyta toliau.
    -   Jei žurnalo paketo numeris, kuris yra nurodytas lentelėse importuotame faile atitinka esamą, neužregistruotas kasdieninio žurnalo Microsoft Dynamics 365 operacijoms, visos linijos, kurios turi atitikimo žurnalo paketo numeris yra importuojami į esamą žurnalą. Eilutės niekada neimportuojamos į užregistruotą žurnalo paketo numerį. Vietoj to sukuriamas naujas numeris.
    -   Jei žurnalo paketo numeris, kuris yra nurodytas lentelėse importuotame faile neatitinka esamų, neužregistruotas kasdieninio žurnalo Dynamics 365 operacijoms, visoms eilutėms, kurios pažymėtos paties žurnalo paketo numeris yra sugrupuoti pagal naują žurnalą. Pvz., visos eilutės, kurių žurnalo paketo numeris yra 1, importuojamos į naują žurnalą, o visos eilutės, kurių žurnalo paketo numeris yra 2, importuojamos į antrą naują žurnalą. Žurnalo paketo numeris sukuriamas naudojant numeraciją, kuri nurodyta DK parametruose.

### <a name="voucher-number"></a>Kvito numeris

-   Kai naudojate objekto Bendrasis žurnalas nustatymą **Rinkiniu pagrįstas apdorojimas**, kvito numeris turi būti nurodytas importuojamame faile. Kiekvienai bendrojo žurnalo operacijai priskiriamas kvito numeris, nurodytas importuojamame faile, net jei kvitas nėra subalansuotas. Jei norite naudoti pagrindu sukurti perdirbimo, bet jūs taip pat norite naudoti numeraciją, kuri nustatyta kvitų numerius Dynamics 365 operacijoms, karštosios pataisos pateikė 2016 m. vasario išleidimo. Karštosios pataisos numeris yra 3170316 ir ją galima atsisiųsti iš „Lifecycle services“ (LCS). Daugiau informacijos žr. [Karštųjų pataisų atsisiuntimas iš „Lifecycle services“](..\migration-upgrade\download-hotfix-lcs.md).
    -   Norėdami įgalinti šią funkciją, žurnalo pavadinimas, kuris naudojamas importo dinamika 365 operacijoms, nustatykite **numeris paskirstymas registruojant** į **taip**.
    -   Kvito numeris vis tiek turi būti nurodytas importuojamame faile. Tačiau šis skaičius yra laikinas ir perrašoma Dynamics 365 operacijų kvito numerio, kai žurnalas užregistruojamas. Įsitikinkite, kad visos žurnalo eilutės yra tinkamai sugrupuotos pagal laikiną kvito numerį. Pvz., registruojant, trimis linijomis randama, kad turi laikiną kvito numeris 1. Laikinas kvito numeris visų trijų linijų perrašoma kitą numerį numerių seką. Jei šios trys eilutės nėra subalansuotas įrašas, kvitas nėra registruojamas. Tada, jei rasta eilučių, kurių laikino kvito numeris yra 2, šis numeris yra perrašomas naudojant paskesnį numeracijos kvito numerį, ir t. t.

<!-- -->

-   Kai nenaudojate, **pagrindu sukurti perdirbimo** aplinkoje, jums nereikia nurodyti kvito numerį importuotame faile. Kvitų numeriai sukuriami importavimo metu pagal žurnalo pavadinimo nustatymą (**Tik vienas kvitas**, **Pagal balansą**, ir t. t.). Pavyzdžiui, jei žurnalo pavadinimo nustatymas yra **Pagal balansą**, pirmai eilutei priskiriamas naujas numatytasis kvito numeris. Tada sistema vertina eilutę, siekdama nustatyti, ar debeto sumos lygios kredito sumoms. Jei eilutėje nurodyta korespondentinė sąskaita, kitai importuojamai eilutei priskiriamas naujas kvito numeris. Jei korespondentinė sąskaita nenurodyta, sistema įvertina, ar debeto sumos lygios kredito sumoms, kai importuojama kiekviena nauja eilutė.
-   Jei laukas **Kvito numeris** nustatytas į parinktį **Automatiškai sugeneruotas**, importuoti nepavyks. Lauko **Kvito numeris** nustatymas **Automatiškai sugeneruotas** nepalaikomas.

Pagal numatytuosius parametrus objektas Bendrasis žurnalas naudoja rinkiniu pagrįstą apdorojimą. Įvertinę savo organizacijos verslo poreikius, nustatymą **Rinkiniu pagrįstas apdorojimas** galite pakeisti, darbo srityje **Duomenų valdymas** spustelėdami **Duomenų objektai**. Rinkiniu pagrįstas apdorojimas yra naudojamas importavimo procesui pagreitinti. Jeigu naudojate rinkiniu pagrįsto apdorojimo, importavimo procesas naudojant objektą Bendrasis žurnalas bus lėtesnis.


