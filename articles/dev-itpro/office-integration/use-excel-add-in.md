---
title: "„Excel“ papildinio naudojimas"
description: "Šioje temoje paaiškinta, kaip programoje „Microsoft Excel“ atidaryti objektų duomenis, tada naudojant „Excel“ skirtą „Microsoft Dynamics Office“ papildinį peržiūrėti, atnaujinti ir redaguoti šiuos duomenis."
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 06fc9f8dda83fddea9ae331bb82c8874b15d76b9
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="use-the-excel-add-in"></a>„Excel“ papildinio naudojimas

[!include[banner](../includes/banner.md)]


Šioje temoje paaiškinta, kaip programoje „Microsoft Excel“ atidaryti objektų duomenis, tada naudojant „Excel“ skirtą „Microsoft Dynamics Office“ papildinį peržiūrėti, atnaujinti ir redaguoti šiuos duomenis. Norėdami atidaryti objekto duomenis, galite paleisti iš „Excel“ arba „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimo.

Kai programoje „Microsoft Excel“ atidarysite objektų duomenis, naudodami „Excel“ skirtą „Microsoft Dynamics Office“ papildinį galėsite greitai ir paprastai peržiūrėti ir redaguoti šiuos duomenis. Norint įdiegti šį papildinį būtina naudoti „Microsoft Excel 2016“. **Pastaba.** Jei „Microsoft Azure Active Directory“ („Azure AD“) nuomotojas bus sukonfigūruotas naudoti „Active Directory“ susiejimo tarnybą (AD FS), būtinai turi būti įdiegtas 2016 m. gegužės mėn. naujinimas – tuomet naudojant „Excel“ papildinį bus galima tinkamai jus prijungti.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-finance-and-operations"></a>Atidaryti objekto duomenis programoje „Excel“ paleidus iš „Dynamics 365 for Finance and Operations“
1.  Programos „Microsoft Dynamics 365 for Finance and Operations“ puslapyje spustelėkite **Atidaryti naudojant „Microsoft Office“**. Jei puslapio šakninis duomenų šaltinis (lentelė) sutaps su bet kurių objektų šakniniu duomenų šaltiniu, puslapyje bus sukuriamos numatytosios parinktys **Atidaryti naudojant „Excel“**. Parinktis **Atidaryti naudojant „Excel“** galima rasti dažnai naudojamuose puslapiuose, pvz., **Visi tiekėjai** ir **Visi klientai**.
2.  Spustelėkite parinktį **Atidaryti naudojant „Excel“** ir atidarykite sukurtą darbaknygę. Šioje darbaknygėje pateikiama su objektu susijusi informacija, aplinkos žymiklis ir „Excel“ papildinio žymiklis.
3.  Programoje „Excel“ spustelėję **Įjungti redagavimą** įjunkite „Excel“ papildinį. „Excel“ papildinys paleidžiamas dešinėje „Excel“ lango pusėje esančioje srityje.
4.  Jei „Excel“ papildinį paleisite pirmą kartą, spustelėkite **Pasitikėti šiuo papildiniu**.
5.  Jei būsite paraginti prisijungti, spustelėkite **Prisijungti**, tada prisijunkite naudodami tuos pačius kredencialus, kuriuos naudojote jungdamiesi prie „Dynamics 365 for Finance and Operations“. „Excel“ papildinys naudos kontekstinę ankstesnio prisijungimo informaciją, gautą iš „Internet Explorer“, ir esant galimybei automatiškai jus prijungs. Todėl viršutiniame dešiniajame „Excel“ papildinio kampe patikrinkite vartotojo vardą.

Naudojant „Excel“ papildinį automatiškai nuskaitomi pasirinkto objekto duomenys. Atminkite, kad darbaknygėje duomenys bus pateikiami tik „Excel“ papildiniui juos nuskaičius.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Kaip paleidus „Excel“ atidaryti objektų duomenis programoje „Excel“
1.  „Excel“ skirtuko **Įterpti** grupėje **Papildiniai** spustelėję **Parduotuvė** atidarykite „Office“ parduotuvę.
2.  „Office“ parduotuvėje ieškokite raktažodžio „Dynamics“ ir spustelėkite **Įtraukti** prie **„Microsoft Dynamics Office“ papildinys** („Excel“ papildinys).
3.  Jei „Excel“ papildinį paleisite pirmą kartą, spustelėję **Pasitikėti šiuo papildiniu** jį įjunkite. „Excel“ papildinys paleidžiamas dešinėje „Excel“ lango pusėje esančioje srityje.
4.  Spustelėję **Įtraukti serverio informaciją** atidarykite sritį **Parinktys**.
5.  Iš „Dynamics 365 for Finance and Operations“ paskirties egzemplioriaus nukopijuokite naršyklės URL, jį įklijuokite į lauką **Serverio URL**, tada panaikinkite visą po pagrindinio kompiuterio pavadinimo esantį tekstą. Gautame URL turi likti tik pagrindinio kompiuterio vardas.
Pavyzdžiui, jei URL yra https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage, panaikinkite viską, išskyrus **https://xxx.dynamics.com**.
6.  Spustelėkite **Gerai**, tada spustelėję **Taip** patvirtinkite pakeitimą. „Excel“ papildinys paleidžiamas iš naujo ir įkeliami metaduomenys. Jau galima naudoti mygtuką **Dizainas**. Jei „Excel“ papildinyje yra mygtukas **Įkelti programėles**, tikriausiai neprisijungėte kaip tinkamas vartotojas. Jei reikia daugiau informacijos, žr. šios temos skyriaus „Trikčių diagnostika“ dalį „Rodomas mygtukas Įkelti programėles“.
7.  Spustelėkite **Dizainas**. Naudojant „Excel“ papildinį gaunami objektų metaduomenys.
8.  Spustelėkite **Įtraukti lentelę**. Pateikiamas objektų sąrašas. Jame objektai nurodomi „Pavadinimas – žyma“ formatu.
9.  Sąraše pasirinkite objektą, pvz., **Klientas – klientai**, tada spustelėkite **Pirmyn**.
10. Norėdami į sąrašą **Pasirinkti laukai** įtraukti sąrašo **Galimi laukai** lauką, spustelėkite lauką, tada spustelėkite **Įtraukti**. Galite ir dukart spustelėti lauką.
11. Įtraukę laukus į sąrašą **Pasirinkti laukai** įsitikinkite, kad žymiklis yra tinkamoje darbalapio vietoje (pavyzdžiui, A1 langelyje), tada spustelėkite **Atlikta**. Tada spustelėję **Atlikta** išeikite iš dizaino įrankio.
12. Spustelėkite **Atnaujinti**, kad būtų nuskaitytas duomenų rinkinys.

## <a name="view-and-update-entity-data-in-excel"></a>Kaip peržiūrėti ir atnaujinti objektų duomenis programoje „Excel“
Kai naudojant „Excel“ papildinį bus nuskaityti ir darbaknygėje pateikti objektų duomenys, bet kada galėsite juos atnaujinti „Excel“ papildinyje spustelėdami **Atnaujinti**.

## <a name="edit-entity-data-in-excel"></a>Kaip redaguoti objektų duomenis programoje „Excel“
Pagal poreikius galite keisti objektų duomenis, tada juos publikuoti „Excel“ papildinyje spustelėdami **Publikuoti**. Norėdami redaguoti įrašą, darbalapyje pasirinkite langelį, tada pakeiskite langelio reikšmę. Norėdami įtraukti naują įrašą, atlikite vieną iš toliau nurodytų veiksmų.

-   Spustelėkite bet kurioje duomenų šaltinio lentelės vietoje, tada „Excel“ papildinyje spustelėkite **Naujas**.
-   Spustelėkite paskutinę duomenų šaltinio lentelės eilutę, tada spauskite klavišą „Tab“, kol žymiklio nebebus paskutiniame šios eilutės stulpelyje ir bus sukurta nauja eilutė.
-   Spustelėkite po pat duomenų šaltinio lentele esančią eilutę ir langelyje pradėkite įvesti duomenis. Kai šiame langelyje nustosite įvesti tekstą ir žymiklį perkelsite į kitą įvesties vietą, lentelė bus išplėsta ir bus įtraukta nauja eilutė.
-   Susiedami antraštės įrašų laukus, spustelėkite vieną iš laukų, o tada „Excel“ papildinyje spustelėkite **Naujas**.

Atkreipkite dėmesį, kad naują įrašą galima kurti tik jei visi pagrindiniai ir privalomi laukai yra susieti darbalapyje arba jei numatytosios vertės buvo įvestos naudojant filtro sąlygą.
Norėdami panaikinti įrašą, atlikite vieną iš toliau nurodytų veiksmų.

-   Dešiniuoju pelės mygtuku spustelėkite eilutės numerį, esantį prie naikintinos darbalapio eilutės, tada spustelėkite **Naikinti**.
-   Dešiniuoju pelės mygtuku spustelėkite naikintiną darbalapio eilutę, tada spustelėkite **Naikinti** &gt; **Lentelės eilutės**.
Jei duomenų šaltiniai buvo įtraukti kaip susiję šaltiniai, antraštė publikuojama prieš eilutes. Jei yra nustatyta priklausomybė tarp kitų duomenų šaltinių, gali tekti pakeisti numatytąją publikavimo tvarką. Norėdami keisti publikavimo tvarką, „Excel“ papildinyje spustelėkite mygtuką **Parinktys** (krumpliaračio simbolis). Tada „FastTab“ **Duomenų jungtis** spustelėkite **Konfigūruoti publikavimo tvarką**.

## <a name="add-or-remove-columns"></a>Įtraukti arba pašalinti stulpelius
Naudodami dizaino įrankį galite koreguoti automatiškai į darbalapį įtraukiamus stulpelius.

1.  Spustelėję mygtuką **Parinktys** (krumpliaračio simbolis) ir pažymėję žymės langelį **Įgalinti dizainą** paleiskite „Excel“ papildinio duomenų šaltinių dizaino įrankį.
2.  „Excel“ papildinyje spustelėkite **Dizainas**. Pateikiami visi duomenų šaltiniai.
3.  Prie duomenų šaltinio spustelėkite mygtuką **Redaguoti** (pieštuko simbolis).
4.  Pagal poreikius pakoreguokite sąrašą **Pasirinkti laukai**.
    -   Norėdami į sąrašą **Pasirinkti laukai** įtraukti sąrašo **Galimi laukai** lauką, spustelėkite lauką, tada spustelėkite **Įtraukti**. Galite ir dukart spustelėti lauką.
    -   Norėdami sąraše **Pasirinkti laukai** pašalinti lauką, spustelėkite šį lauką, tada spustelėkite **Šalinti**. Galite ir dukart spustelėti lauką.
    -   Norėdami keisti laukų tvarką, sąraše **Pasirinkti laukai** spustelėkite lauką, spustelėkite lauką, tada spustelėkite **Aukštyn** arba **Žemyn**.

5. Norėdami pritaikyti duomenų šaltinio keitimus, spustelėkite **Naujinti**. Tada spustelėję **Atlikta** išeikite iš dizaino įrankio. 
6. Jei įtraukėte lauką (stulpelį), spustelėkite **Atnaujinti**, kad būtų nuskaitytas atnaujintas duomenų rinkinys.

## <a name="troubleshooting"></a>Trikčių šalinimas
Kelias triktis galima pašalinti atlikus paprastus veiksmus.

-   **Rodomas mygtukas Įkelti programėles.** Jei prisijungus „Excel“ papildinyje yra mygtukas **Įkelti programėles**, tikriausiai neprisijungėte kaip tinkamas vartotojas. Norėdami išspręsti šią problemą, patikrinkite, ar viršutiniame dešiniajame „Excel“ papildinio kampe pateikiamas teisingas vartotojo vardas. Jei pateikiamas neteisingas vartotojo vardas, jį spustelėkite, atsijunkite, tada prisijunkite iš naujo.
-   **Gaunate pranešimą „Uždrausta“.** Jei „Excel“ papildiniui įkeliant metaduomenis gausite pranešimą „Uždrausta“, paskyrai, kurios duomenis naudojant yra prisijungta prie „Excel“ papildinio, nesuteiktos teisės naudoti paskirties paslaugą, egzempliorių ar duomenų bazę. Norėdami išspręsti šią problemą, patikrinkite, ar viršutiniame dešiniajame „Excel“ papildinio kampe pateikiamas teisingas vartotojo vardas. Jei pateikiamas neteisingas vartotojo vardas, jį spustelėkite, atsijunkite, tada prisijunkite iš naujo.
-   **Programoje „Excel“ pateikiamas tuščias tinklalapis.** Jei per prisijungimo procesą atidaromas tuščias tinklalapis, paskyroje būtinai turi būti naudojama AD FS, tačiau įdiegta nepakankamai nauja papildinį paleidžianti „Excel“ versija ir prisijungimo dialogo langas neįkeliamas. Norėdami pašalinti šią triktį, atnaujinkite naudojamą „Excel“ versiją. Norėdami atnaujinti „Excel“ versiją įmonėje, kurioje naudojamas atidėtų naujinimų kanalas, naudodami [„Office“ diegimo įrankį](https://technet.microsoft.com/library/jj219422.aspx) [pakeiskite atidėtų naujinimų kanalą į dabartinių naujinimų kanalą](https://technet.microsoft.com/library/mt455210.aspx).





