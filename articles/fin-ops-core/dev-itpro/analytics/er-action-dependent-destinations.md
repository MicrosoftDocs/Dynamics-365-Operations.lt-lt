---
title: Nuo veiksmo priklausomų ER paskirties vietų konfigūravimas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti elektroninių ataskaitų (ER) formato, kuris sukonfigūruotas siunčiamiems dokumentams generuoti, nuo veiksmo priklausomas paskirties vietas.
author: NickSelin
manager: AnnBe
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ea7543fddef085cfd1e92edf0b1dabf6d0aac38a
ms.sourcegitcommit: 5264aaec3723c40a219e4d2867afe1ba9cc5f2a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5153644"
---
# <a name="configure-action-dependent-er-destinations"></a>Nuo veiksmo priklausomų ER paskirties vietų konfigūravimas

[!include [banner](../includes/banner.md)]

Galite konfigūruoti [paskirties vietas](electronic-reporting-destinations.md) kiekvienam [Elektroninių ataskaitų (ER)](general-electronic-reporting.md) [formato](general-electronic-reporting.md#FormatComponentOutbound) [konfigūracijos,](general-electronic-reporting.md#Configuration) naudojamos išvesties dokumento generavimui, išvesties komponentui (aplankui ar failui). Vartotojai, vykdantys šio tipo ER formatą ir turintys atitinkamas prieigos teises, taip pat gali keisti sukonfigūruotus paskirties vietos parametrus vykdymo metu.

„Microsoft Dynamics 365 Finance” **10.0.17 ir vėlesnėse versijose**, ER formatas gali būti vykdomas [parengiant](er-apis-app10-0-17.md) veiksmo kodą, kurį vartotojas atlieka vykdydamas ER formatą. Pavyzdžiui, Spausdinimo valdymo parametrų modulyje **Gautinos sumos** galite pasirinkti ER formatą, generuojantį tam tikrą verslo dokumentą, pavyzdžiui, laisvos formos sąskaitos faktūrą. Tada galėsite pasirinkti **Rodinys** sąskaitai faktūrai peržiūrėti arba **Spausdinti** jos nusiuntimui į spausdintuvą. Jei vartotojo veiksmas yra perduotas vykdomam ER formatui vykdymo metu, galite konfigūruoti skirtingas ER paskirties vietas skirtingiems vartotojo veiksmams. Šioje temoje paaiškinama, kaip konfigūruoti šio tipo ER formato paskirties vietas.

## <a name="make-action-dependent-er-destinations-available"></a>Padarykite nuo veiksmo priklausomas ER paskirties vietas prieinamas

Norėdami konfigūruoti nuo veiksmo priklausomas ER paskirties vietas dabartiniame „Finance” egzemplioriuje ir įgalinti [naują](er-apis-app10-0-17.md) ER API, atidarykite [Funkcijos valdymo](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) darbo sritį ir įjunkite **Konfigūruoti konkrečias ER paskirties vietas, kurios bus naudojamos skirtingiems PM veiksmams** funkciją. Norėdami naudoti ER paskirties vietas [konkrečioms](#reports-list-wave1) ataskaitoms vykdymo metu, įjunkite funkciją **PM ataskaitų, paremtų vartotojų veiksmams būdingomis ER paskirties vietomis, maršruto išvestis (1 banga)**.

## <a name="configure-action-dependent-er-destinations"></a>Nuo veiksmo priklausomų ER paskirties vietų konfigūravimas

Kai įjungiate **Konfigūruoti konkrečias ER paskirties vietas, kurios bus naudojamos skirtingiems PM veiksmams** funkciją, galite konfigūruoti nuo veiksmų priklausomas ER paskirties vietas **Failo paskirties vieta** „FastTab”, esančiame **Elektroninių ataskaitų paskirties vieta** puslapyje. Kiekvienam komponentui galite įtraukti įrašą ir įgalinti konkrečias ER paskirties vietas. Kiekviename įraše turite nurodyti dokumento, kuriam turėtų būti taikomos sukonfigūruotos ER paskirties vietos, tipą. Lauke **Dokumento tipas** pasirinkite vieną iš toliau pateiktų reikšmių:

- Pasirinkite **Elektroninis** taikyti sukonfigūruotoms paskirties vietoms, jei vykdymo metu nepateikiamas vartotojo veiksmo kodas.
- Pasirinkite **Spausdinimo valdymas** taikyti sukonfigūruotoms paskirties vietoms, jei vykdymo metu pateikiamas vartotojo veiksmo kodas.
- Pasirinkite **Bet koks** visada taikyti sukonfigūruotoms paskirties vietoms, nepriklausomai nuo to, ar vykdymo metu pateikiamas vartotojo veiksmo kodas.

Jei pasirenkate **Spausdinimo valdymo** dokumento tipą, turite nurodyti vartotojo veiksmus, kuriems turėtų būti taikomos sukonfigūruotos ER paskirties vietos. Lauke **Spausdinimo valdymo veiksmas** pasirinkite vieną iš šių reikšmių:

- Pasirinkite **Rodyti** taikyti sukonfigūruotoms paskirties vietoms, jei vykdymo metu pateikiamas **Rodyti** vartotojo veiksmas.
- Pasirinkite **Spausdinti** taikyti sukonfigūruotoms paskirties vietoms, jei vykdymo metu pateikiamas **Spausdinti** vartotojo veiksmas.
- Pasirinkite **Siųsti** taikyti sukonfigūruotoms paskirties vietoms, jei vykdymo metu pateikiamas **Siųsti** vartotojo veiksmas.

> [!NOTE]
> Vienam paskirties vietos įrašui galima pasirinkti keletą veiksmų.

Jei pasirenkate **Bet koks** dokumento tipą, **Automatiškai aptikti** yra pasirenkamas automatiškai lauke **Spausdinimo valdymo veiksmas** kaip vartotojo veiksmas ir atsitinka taip:

- Jei vykdymo metu nepateikiamas vartotojo veiksmo kodas, taikomos visos sukonfigūruotos ER paskirties vietos.
- Jei vykdymo metu pateikiamas vartotojo veiksmo kodas, taikoma iš anksto tam veiksmui apibrėžta konkreti ER paskirties vieta, **neatsižvelgiant į tai, ar ji buvo įjungta**:

    - Kai veiksmas **Rodyti** yra pateikiamas vykdymo metu, taikoma ER paskirties vieta **Ekranas**.
    - Kai veiksmas **Siųsti** yra pateikiamas vykdymo metu, taikoma ER paskirties vieta **El. paštas**.
    - Kai veiksmas **Spausdinti** yra pateikiamas vykdymo metu, taikoma ER paskirties vieta **Spausdintuvas**.

Pavyzdžiui, galite naudoti **Laisvos formos sąskaitos faktūros („Excel)”** ER formatą [laisvos formos sąskaitai faktūrai](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/create-free-text-invoice-new) spausdinti, kai ją registruojate. Norėdami nukreipti sugeneruotą dokumentą, turite sukonfigūruoti šio ER formato paskirties vietas. Pavyzdžiui, jums gali prireikti sukonfigūruoti šias ER paskirties vietas tam, kad sugeneruotame dokumente atliktumėte šiuos veiksmus:

- Archyvuoti dokumentą, jei vykdomas ER formatas, tačiau nepateikiamas joks veiksmo kodas (pavyzdžiui, kai dokumentas siunčiamas elektroniniu būdu).
- Peržiūrėti dokumentą žiniatinklio naršyklėje, kai vartotojas atlieka **Rodyti** veiksmą.
- Archyvuoti ir spausdinti dokumentą, kai vartotojas atlieka **Spausdinti** veiksmą.
- Archyvuoti dokumentą ir išsiųskite jį el. paštu kaip siunčiamo el. laiško pranešimo priedą, kai vartotojas atlieka **Siųsti** veiksmą.

Tolesnė iliustracija rodo, kaip galite pasiekti šias konfigūravimo ER paskirties vietas kaip atskirų paskirties vietų įrašų rinkinį, kai kiekvienas įrašas konfigūruojamas kiekvienam vartotojo veiksmui:

![Elektroninių ataskaitų paskirties vietų puslapis, kuriame yra nuo veiksmo priklausomų ER formato paskirties vietų parametrų kai kiekvienas paskirties vietos įrašas konfigūruojamas atskiram vartotojo veiksmui](./media/er-destination-action-dependent-01.png)

Tolesnė iliustracija rodo, kaip galite pasiekti tas pačias alternatyvias konfigūravimo ER paskirties vietas kaip atskirų paskirties vietų įrašų rinkinį, kai kiekvienas įrašas konfigūruojamas kiekvienai paskirties vietai:

![Elektroninių ataskaitų paskirties vietų puslapis, kuriame yra nuo veiksmo priklausomų ER formato paskirties vietų parametrų kai kiekvienas paskirties vietos įrašas konfigūruojamas atskirai paskirties vietai](./media/er-destination-action-dependent-01a.png)

> [!NOTE]
> Jei pateikiamas vykdomo ER formato veiksmo kodas, bet to veiksmo kodui nebuvo sukonfigūruotos jokios paskirties vietos, taikomas [numatytasis](electronic-reporting-destinations.md#default-behavior) paskirties vietos veikimo būdas.

## <a name="change-action-dependent-er-destinations-at-runtime"></a>Pakeiskite nuo veiksmo priklausomas ER paskirties vietas vykdymo metu

Kai vykdomas ER formatas, jei vartotojo veiksmus sukonfigūravo vartotojai, turintis reikiamas [teises](electronic-reporting-destinations.md#security-considerations) pakeisti paskirties vietos konfigūracijos parametrams vykdymo metu, atsiranda dialogo langas, suteikiantis pasirinkimą keisti paskirties vietos konfigūracijos parametrus. Šis dialogo langas yra pasirenkamas ir jo pasirodymas priklauso nuo to, kaip buvo iškviestas ER sistemos vykdomas ER formatas. Jei pasirodo šis dialogo langas, ER paskirties vietos jame bus įgalintos pagal pateiktą vartotojo veiksmą.

Šioje iliustracijoje pateikiamas **Elektroninių ataskaitų formato paskirties vietų** dialogo langas, kuris pasirodo, kai laisvos formos sąskaita faktūra yra [užregistruota](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/create-free-text-invoice-new) ir vykdomas ER formatas **Laisvos formos sąskaita faktūra („Excel”)** šio dokumento generavimui, jei buvo **Spausdintuvo** veiksmas ir ER paskirties vietos buvo sukonfigūruoti šiam formatui, kaip parodyta anksčiau šioje temoje.

![Dialogo langas, kuris suteikia parinktį keisti pradines vykdomo ER formato ER paskirties vietų konfigūracijas](./media/er-destination-action-dependent-02.gif)

> [!NOTE]
> Jei sukonfigūravote vykdomo ER formato paskirties vietas keliems komponentams, atskirai kiekvienam sukonfigūruotam ER formato elementui bus pasiūlyta parinktis.

## <a name="verify-the-provided-user-action"></a>Pateikto vartotojo veiksmo patikrinimas

Galite patikrinti koks vartotojo veiksmas, jei toks yra, pateiktas vykdomam ER formatui, kai atliekate konkretų vartotojo veiksmą. Šis patikrinimas svarbus, kai turite sukonfigūruoti nuo veiksmo priklausomas ER paskirties vietas, tačiau nežinote, koks vartotojo veiksmo kodas, jei toks yra, yra pateiktas. Pavyzdžiui, kai pradedate registruoti laisvos formos sąskaitą faktūrą ir nustatote parinktį **Spausdinti sąskaitą faktūrą** į **Taip** dialogo lange **Registruoti laisvos formos sąskaitą faktūrą** galite nustatyti parinktį **Naudoti spausdinimo valdymo paskirties vietą** į **Taip** arba **Ne**.

Norėdami patikrinti pateiktą vartotojo veiksmo kodą, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
3. Dialogo lange **Vartotojo parametrai** [nustatykite](er-trace-reports-compare-baseline.md#configure-er-parameters-to-use-the-baseline-feature) parinktį **Vykdyti derinimo režimu** į **Taip**.
4. Atlikite vartotojo veiksmą vykdydami ER formatą. Atsiminkite, kad ER vartotojo parametrai yra būdingi įmonei ar vartotojui.
5. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos derinimo žurnalai**.
6. Puslapyje **Konfigūracijos derinimų žurnalas** filtruokite ER vykdymo įrašus jūsų ER formato vykdymo įrašui rasti.
7. Peržiūrėkite žurnalo įrašus, kuriuose turi būti įrašas su pateiktu vartotojo veiksmo kodu, jei buvo pateiktas bet koks ER formato vykdymo veiksmas.

    ![Elektroninių ataskaitų vykdymo žurnalų puslapis, kuriame yra informacija apie vartotojo veiksmo kodą, pateiktą ER formato filtruotam vykdymui](./media/er-destination-action-dependent-03.png)

## <a name=""></a><a name="reports-list-wave1">Verslo dokumentų sąrašas (1 banga)</a>

Šį verslo dokumentų sąrašą valdo funkcija **PM ataskaitų, paremtų vartotojų veiksmams būdingomis ER paskirties vietomis, maršruto išvestis (1 banga)**:

- Kliento sąskaita faktūra (laisvos formos SF)
- Kliento sąskaita faktūra (pardavimo SF)
- Pirkimo užsakymas
- Pirkimo užsakymo pirkimo užklausa
- Pardavimo užsakymo patvirtinimas
- Rinkinių laiško pastaba
- Kliento kodo išrašas
- Delspinigių pažyma
- Tiekėjo mokėjimo pažyma
- Pasiūlymo patvirtinimas

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų (ER) paskirties vietos](electronic-reporting-destinations.md)

[„Application Update 10.0.17“ elektroninės ataskaitų sistemos API pakeitimai](er-apis-app10-0-17.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]