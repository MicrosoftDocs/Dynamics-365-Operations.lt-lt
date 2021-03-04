---
title: Geriausia kvitų importavimo praktika naudojant objektą Bendrasis žurnalas
description: Šioje temoje pateikiama patarimų, kaip į bendrąjį žurnalą importuoti duomenų naudojant objektą Bendrasis žurnalas.
author: rcarlson
manager: AnnBe
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5b36e11bd9ef338334f7ac1b6412edb7754010f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687648"
---
# <a name="best-practices-for-importing-vouchers-by-using-the-general-journal-entity"></a>Geriausia kvitų importavimo praktika naudojant objektą Bendrasis žurnalas

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama patarimų, kaip į bendrąjį žurnalą importuoti duomenų naudojant objektą Bendrasis žurnalas.

Naudodami objektą Bendrasis žurnalas galite importuoti kvitus, kurių sąskaitos ar korespondentinės sąskaitos tipas yra **Didžioji knyga**, **Klientas**, **Tiekėjas** arba **Bankas**. Kvito duomenis galima įvesti vienoje eilutėje naudojant laukus **Sąskaita** ir **Korespondentinė sąskaita** arba keliose eilutėse, kuriose naudojamas tik laukas **Sąskaita**, o kiekvienoje eilutėje laukas **Korespondentinė sąskaita** paliekamas tuščias. Objekte Bendrasis žurnalas nepalaikomi visi sąskaitos tipai. Jeigu reikalingi skirtingi sąskaitų tipų deriniai, geriau naudoti kitus objektus. Pavyzdžiui, naudokite objektą Projekto išlaidų žurnalas projekto operacijai importuoti. Kiekvienas objektas sukurtas tam, kad palaikytų tam tikrus scenarijus. Tai reiškia, kad tų scenarijų objektuose gali būti papildomų laukų. Tačiau skirtingų scenarijų objektuose papildomų laukų gali nebūti.

## <a name="setup"></a>Sąranka
Kol dar neimportavote naudodami objektą Bendrasis žurnalas, patikrinkite toliau nurodytą sąranką.

- **Žurnalo paketo numerio numeracijos nustatymas** – pagal numatytuosius parametrus, kai importuojate naudodami objektą Bendrasis žurnalas, žurnalo paketo numeris naudoja numeraciją, nurodytą DK parametruose. Jei nustatysite žurnalo paketo numerio numeracijos parinktį **Neautomatinis**, numatytasis numeris nebus taikomas. Šis nustatymas nepalaikomas.
- **Finansinių dimensijų konfigūracija** – kiekviena organizacija turi nurodyti finansinių dimensijų tvarką, skirtą operacijoms importuoti naudojant objektus. Formato **DK dimensijų integracija** tvarka nustatoma dalyje **DK** &gt; **Sąskaitų planas** &gt; **Dimensijos** &gt; **Finansinių dimensijų konfigūravimas, kad būtų galima integruoti programas** &gt; **Pasirinkti duomenų objektus**. Importuojamos DK sąskaitos segmentų tvarka turi būti ta tokia pati. Kitaip importavimo metu įvyks klaida.

## <a name="general-journal-entity-setup"></a>Objekto Bendrasis žurnalas nustatymas
Du toliau pateikti duomenų valdymo parametrai nulemia numatytojo žurnalo paketo numerio arba kvito numerio pritaikymo pobūdį.

- **Apdorojimas pagal rinkinį** (duomenų objekte)
- **Automatiškai sugeneruotas** (laukų susiejime)

Tolesniuose skyriuose aprašomas šių parametrų poveikis. Juose taip pat aiškinama, kaip sistema generuoja žurnalų ir kvitų numerių paketų numerius.

### <a name="journal-batch-number"></a>Žurnalo numeris

- Objekto Bendrasis žurnalas nustatymas **Rinkiniu pagrįstas apdorojimas** generuojant žurnalo paketo numerius įtakos neturi.
- Jei laukas **Žurnalo paketo numeris** nustatytas į parinktį **Automatiškai sugeneruotas**, sukuriamas naujas kiekvienos importuojamos eilutės žurnalo paketo numeris. Taip daryti nerekomenduojama. Nustatymą **Automatiškai sugeneruotas** galima rasti importavimo projekto dalie **Peržiūrėti schemą** skirtuke **Susiejimo informacija**.
- Jei laukas **Žurnalo paketo numeris** nėra nustatytas į parinktį **Automatiškai sugeneruotas**, žurnalo paketo numeris, kaip nurodyta toliau.

    - Jei importuoto failo žurnalo paketo numeris atitinka esamą neregistruoto kasdieninio žurnalo numerį, į esamą žurnalą importuojamos visos eilutės, kurių žurnalo paketo numeris atitinka. Eilutės niekada neimportuojamos į užregistruotą žurnalo paketo numerį. Vietoj to sukuriamas naujas numeris.
    - Jei importuoto failo žurnalo paketo numeris neatitinka esamo neregistruoto kasdieninio žurnalo numerio, visos eilutės, kurių žurnalo paketo numeris toks pat, įtraukiamos į naują žurnalą. Pvz., visos eilutės, kurių žurnalo paketo numeris yra 1, importuojamos į naują žurnalą, o visos eilutės, kurių žurnalo paketo numeris yra 2, importuojamos į antrą naują žurnalą. Žurnalo paketo numeris sukuriamas naudojant numeraciją, kuri nurodyta DK parametruose.

### <a name="voucher-number"></a>Kvito numeris

- Kai naudojate objekto Bendrasis žurnalas nustatymą **Rinkiniu pagrįstas apdorojimas**, kvito numeris turi būti nurodytas importuojamame faile. Kiekvienai bendrojo žurnalo operacijai priskiriamas kvito numeris, nurodytas importuojamame faile, net jei kvitas nėra subalansuotas. Jei norite naudoti apdorojimo pagal rinkinį parametrą, tačiau taip pat norite naudoti nustatytą kvitų numerių seką, atkreipkite dėmesį į tolesnius punktus.

    - Norėdami įgalinti šią funkciją, žurnalo pavadinime, kuris naudojamas importavimo operacijoms atlikti, nustatykite parinktį **Numerių paskirstymas registruojant** kaip **Taip**.
    - Kvito numeris vis tiek turi būti nurodytas importuojamame faile. Tačiau šis numeris yra laikinas ir registruojant žurnalą bus perrašytas naudojant kvito numerį. Įsitikinkite, kad visos žurnalo eilutės yra tinkamai sugrupuotos pagal laikiną kvito numerį. Pavyzdžiui, registruojant surandamos trys eilutės, kurių laikinas kvito numeris – 1. Laikinas visų trijų eilučių kvito numeris perrašomas naudojant paskesnį numeracijos numerį. Jei šios trys eilutės nėra subalansuotas įrašas, kvitas nebus registruojamas. Tada, jei rasta eilučių, kurių laikino kvito numeris yra 2, šis numeris yra perrašomas naudojant paskesnį sekos kvito numerį, ir t. t.

- Kai parametro **Apdorojimas pagal rinkinį** nenaudojate, importuojamame faile neturite pateikti kvito numerio. Kvitų numeriai sukuriami importavimo metu pagal žurnalo pavadinimo nustatymą (**Tik vienas kvitas**, **Pagal balansą**, ir t. t.). Pavyzdžiui, jei žurnalo pavadinimo nustatymas yra **Pagal balansą**, pirmai eilutei priskiriamas naujas numatytasis kvito numeris. Tada sistema vertina eilutę, siekdama nustatyti, ar debeto sumos lygios kredito sumoms. Jei eilutėje nurodyta korespondentinė sąskaita, kitai importuojamai eilutei priskiriamas naujas kvito numeris. Jei korespondentinė sąskaita nenurodyta, sistema įvertina, ar debeto sumos lygios kredito sumoms, kai importuojama kiekviena nauja eilutė.
- Jei laukas **Kvito numeris** nustatytas į parinktį **Automatiškai sugeneruotas**, importuoti nepavyks. Lauko **Kvito numeris** nustatymas **Automatiškai sugeneruotas** nepalaikomas.

Pagal numatytuosius parametrus objektas Bendrasis žurnalas naudoja rinkiniu pagrįstą apdorojimą. Įvertinę savo organizacijos verslo poreikius, nustatymą **Rinkiniu pagrįstas apdorojimas** galite pakeisti, darbo srityje **Duomenų valdymas** spustelėdami **Duomenų objektai**. Rinkiniu pagrįstas apdorojimas yra naudojamas importavimo procesui pagreitinti. Jeigu naudojate rinkiniu pagrįsto apdorojimo, importavimo procesas naudojant objektą Bendrasis žurnalas bus lėtesnis.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]