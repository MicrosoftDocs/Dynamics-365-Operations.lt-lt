---
title: Naudoti &quot;Excel&quot;
description: "Šioje temoje aiškinama, kaip atidaryti subjekto duomenys programoje Microsoft Excel, ir tada Rodyti, atnaujinti ir redaguoti duomenis naudojant Microsoft Dynamics Office papildinys, skirtas &quot;Excel&quot;. Norėdami atidaryti duomenų subjektas, galite paleisti iš Excel arba Microsoft Dynamics 365 operacijoms."
author: ChrisGarty
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: af7e7288f741b3c519227e2778c4c4311c3a2012
ms.openlocfilehash: 8af663b47117759ed3b2e2ed8eee85ae4df100d1
ms.lasthandoff: 03/31/2017


---

# <a name="use-the-excel-add-in"></a>Naudoti "Excel"

Šioje temoje aiškinama, kaip atidaryti subjekto duomenys programoje Microsoft Excel, ir tada Rodyti, atnaujinti ir redaguoti duomenis naudojant Microsoft Dynamics Office papildinys, skirtas "Excel". Norėdami atidaryti duomenų subjektas, galite paleisti iš Excel arba Microsoft Dynamics 365 operacijoms.

Atidarant objekto duomenis į Microsoft Excel, jūs galite greitai ir lengvai peržiūrėti ir redaguoti duomenis naudojant Microsoft Dynamics Office papildinys, skirtas "Excel". Šis priedas, reikalingas "Microsoft" "Excel" 2016. **Pastaba:** jei savo "Microsoft" Azure Active Directory (Azure AD) nuomininkas yra sukonfigūruotas naudoti Active Directory susiejimo tarnyba (AD FS), turite būti tikri, kad buvo taikomas 2016 m. gegužės atnaujinimas, taip, kad "Excel" papildinys gali teisingai jums prisijungti.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>Atidaryti subjektas duomenis programoje Excel, kai paleidžiate iš Dynamics 365 operacijoms
1.  Microsoft Dynamics "365" operacijų puslapį, spustelėkite **atidaryti Microsoft Office**. Jei šakninis duomenų šaltinis (lentelė) puslapyje yra toks pat kaip Šakninis duomenų šaltinis visiems objektams, **atidaryti naudojant Excel** funkcijos yra generuojami puslapyje. **Atidaryti naudojant Excel** parinktis galima rasti dažnai naudojamas puslapiuose, pvz., **visiems tiekėjams** ir **visiems klientams**.
2.  Spustelėkite į **atidaryti programoje "Excel"** variantas, ir atidarykite darbaknygę, kurioje yra sukurtas. Šioje darbaknygėje yra privalomosios informacijos apie ūkio subjektas, žymiklį į savo aplinką ir rodyklę į "Excel" papildinys.
3.  Programoje "Excel", spustelėkite **redagavimo**, kad į Excel add-in paleisti. "Excel" papildinys veikia srityje "Excel" lango dešinėje pusėje.
4.  Jei naudojate "Excel" papildinys, skirtas pirmą kartą, spustelėkite **pasitikėti šio**.
5.  Jei esate raginami prisijungti, spustelėkite **prisijungti**, ir tada prisijungti naudodami tuos pačius kredencialus, kurį naudojote prisijungti prie Dynamics 365 operacijoms. "Excel" papildinys bus naudoti ankstesnius prisijungimo kontekste "Internet Explorer" ir automatiškai prijungs jus, jei taip. Todėl, patikrinti vartotojo vardą viršutiniame dešiniajame kampe "Excel" pridėti-in.

"Excel" papildinys automatiškai nuskaito duomenų subjektui, kurį pasirinkote. Atkreipkite dėmesį, kad nebus jokių duomenų darbaknygėje tol, kol į Excel add-in skaito jį.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Atidaryti objekto duomenis programoje Excel, kai paleidžiate iš "Excel"
1.  Programoje "Excel", ant į **įterpti** skirtuke, be to **priedai** grupės, spustelėkite **parduotuvėje** atidaryti Office parduotuvės.
2.  Office parduotuvėje, ieškoti pagal raktinį žodį "Dynamics", ir spustelėkite **pridėti** prie to **Microsoft Dynamics Office papildinys** (į Excel add-in).
3.  Jei naudojate "Excel" papildinys, skirtas pirmą kartą, spustelėkite **pasitikėti šios**, kad į Excel add-in paleisti. "Excel" papildinys veikia srityje "Excel" lango dešinėje pusėje.
4.  Spustelėkite **įtraukti serverio informacija** atidaryti, **funkcijos** srityje.
5.  Nukopijuokite į naršyklės URL iš jūsų tikslinės Dynamics 365 operacijų atveju, įklijuokite jį į su **serverio URL** lauko ir tada ištrinti viską po pagrindinio kompiuterio vardą (pvz., ištrinti **/? cmp = usmf & mi = CustTableListPage**). Gautojo URL adresą turėtų turėti tik pagrindinio kompiuterio pavadinimas (pvz., **https://xxx.dynamics.com**).
6.  Spustelėkite **gerai**, ir tada spustelėkite **taip** kad patvirtintumėte keitimą. "Excel" pridėti iš naujo ir įkelia metaduomenų. Į **dizaino** dabar yra mygtukas. Jei "Excel" papildinys, **įkelti programėles** mygtuką, jūs turbūt nesate įėjęs teisingą vartotojo vardą. Norėdami gauti daugiau informacijos, peržiūrėkite "programėlės mygtuką apkrova yra rodomas" šios temos skyriuje "Trikčių diagnostika".
7.  Spustelėkite **dizaino**. "Excel" papildinys nuskaito objekto metaduomenis.
8.  Spustelėkite **pridėti lentelę**. Subjektų sąrašas atrodo. Subjektai yra išvardytos "Vardas – ženklas" formatu.
9.  Pasirinkite ūkio subjektas sąraše, pvz., **klientų - Klientai**, ir tada spustelėkite **kitas**.
10. Pridėti lauką iš to **galimi laukai** sąrašas turi į **pasirinkti laukai** sąrašą, spustelėkite lauką, ir tada spustelėkite **pridėti**. Taip pat galite dukart spustelėkite lauką.
11. Pridėję norimus laukus, **pasirinkti laukai** sąrašą, įsitikinkite, kad kursorius yra į reikiamą vietą darbalapyje (pvz., langelio A1) ir tada spustelėkite **padaryti**. Spustelėkite **padaryti** išeiti iš dizainerio.
12. Spustelėkite **atnaujinti** traukti į duomenų rinkinį.

## <a name="view-and-update-entity-data-in-excel"></a>Peržiūrėkite ir atnaujinkite "Excel" duomenų subjekto
Po to, kai "Excel" papildinys skaito objekto duomenis į darbaknygę, galite atnaujinti duomenis bet kuriuo metu spustelėdami **atnaujinti** "Excel" pridėti-in.

## <a name="edit-entity-data-in-excel"></a>Redaguoti objekto duomenis programoje "Excel"
Galite keisti objekto duomenis, kaip jums reikia ir tada publikuokite jį atgal, paspauskite **skelbti** "Excel" pridėti-in. Norėdami redaguoti įrašą, pasirinkite langelį darbalapyje ir pakeiskite langelio reikšmę. Jei norite pridėti naują įrašą, atlikite vieną iš šių veiksmų:

-   Spustelėkite bet kurioje darbalapio, ir tada spustelėkite **naujas** "Excel" pridėti-in.
-   Spustelėkite paskutinį darbalapio eilutėje, ir tada paspauskite klavišą Tab, kol žymiklis perkeliamas iš tos eilutės, paskutinėje skiltyje ir sukūrė naują eilę.
-   Spustelėkite iš karto po darbalapio eilutėje, o pradėti įvesti duomenis į langelį. Kai įvesties vietą perkeliate iš ląstelių, darbalapio išsiplečia, kad apimtų naują eilutę.

Norėdami panaikinti įrašą, atlikite vieną iš šių veiksmų:

-   Dešiniuoju pelės mygtuku spustelėkite eilutės numeris šalia darbalapio eilutėje Naikinti, o tada spustelėkite **panaikinti**.
-   Dešiniuoju pelės mygtuku spustelėkite darbalapio eilutėje Naikinti, o tada spustelėkite **panaikinti**&gt;**lentelės eilutės**.

## <a name="add-or-remove-columns"></a>Įtraukti arba pašalinti stulpelius
Dizaineris galite koreguoti stulpelių, automatiškai įtraukiami į darbalapį.

1.  Pradžiai duomenų šaltinio dizaineris "Excel" pridėti-in su **funkcijos** mygtuką (įrankių simbolis) ir pasirinkę į **įgalinti dizainas** žymės langelį.
2.  Spustelėkite **projekto** "Excel" pridėti-in. Visi duomenų šaltiniai yra išvardyti.
3.  Šalia duomenų šaltinis, spustelėkite į **redaguoti** mygtukas (pieštuku simbolis).
4.  Koreguoti pateiktame sąraše, **pasirinkti laukai** išvardyti kiek reikės:
    -   Pridėti lauką iš to **galimi laukai** sąrašas turi į **pasirinkti laukai** sąrašą, spustelėkite lauką, ir tada spustelėkite **pridėti**. Taip pat galite dukart spustelėkite lauką.
    -   Norėdami pašalinti lauką iš to **pasirinkti laukai** sąrašą, spustelėkite lauką, ir tada spustelėkite **pašalinti**. Taip pat galite dukart spustelėkite lauką.
    -   Norėdami pakeisti laukų tvarka, spustelėkite lauką, **pasirinkti laukai** sąrašas, ir tada spustelėkite **iki** ar **žemyn**.

5.  Taikyti savo keitimus į duomenų šaltinį, spustelėkite **naujinimas**. Spustelėkite **padaryti** išeiti iš dizainerio. Jei pridėjote lauko (stulpelio), spustelėkite **atnaujinti** traukti į atnaujintą duomenų rinkinį.

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Troubleshooting
Yra keletas klausimų, kurie gali būti išspręsta per keletą paprastų žingsnių.

-   **Programėlės mygtuką apkrova yra rodomas.** Jei "Excel" papildinys, **įkelti programėles** mygtuką po prisijungimo, jūs turbūt nesate įėjęs kaip teisingą vartotojo. Norėdami išspręsti šią problemą, patikrinkite, ar kad teisingą vartotojo vardas rodomas viršutiniame dešiniajame kampe "Excel" pridėti-in. Jei neteisingas vartotojo vardas rodomas, spustelėkite jį, atsijunkite ir vėl prisijunkite.
-   **Gaunate žinutę "Uždraustojo".** Jei gaunate pranešimą "Draudžiama", o "Excel" papildinys yra įkeliami metaduomenys, sąskaitą, kuri yra prisijungęs prie "Excel" papildinys neturi teisės naudotis tikslinių paslaugų, pavyzdžiui, arba duomenų bazės. Norėdami išspręsti šią problemą, patikrinkite, ar kad teisingą vartotojo vardas rodomas viršutiniame dešiniajame kampe "Excel" pridėti-in. Jei neteisingas vartotojo vardas rodomas, spustelėkite jį, atsijunkite ir vėl prisijunkite.
-   **Tuščią tinklalapio rodoma per "Excel".** Jei tuščią tinklalapį atidaro per prisijungimo procesą, sąskaitą reikia AD FS, bet versija "Excel" papildinys veikia ne pakankamai neseniai, įkelti į prisijungimo dialogo lange. Norėdami išspręsti šią problemą, atnaujinti, jūs naudojate "Excel" versiją. Atnaujinti "Excel" versijose, kai esate įmonė, kuri yra atidėtųjų kanalu, naudoti su [Office diegimo įrankis](https://technet.microsoft.com/library/jj219422.aspx) į [perkelti iš atidėtųjų kanalo žiūrimą](https://technet.microsoft.com/library/mt455210.aspx).



