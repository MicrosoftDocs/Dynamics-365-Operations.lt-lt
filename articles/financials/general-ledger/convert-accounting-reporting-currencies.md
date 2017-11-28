---
title: "Apskaitos arba ataskaitų valiutos konvertavimas"
description: "Norėdama pakeisti apskaitos arba ataskaitų valiutą, įmonė turi du pasirinkimus."
author: aprilolson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 78223
ms.assetid: 31c56f9a-9c64-40a2-90e3-1969a760614b
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ad840f4ed2cf27615e699a13fcd8be7f3c2cd5c8
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="convert-accounting-or-reporting-currencies"></a>Apskaitos arba ataskaitų valiutos konvertavimas

[!include[banner](../includes/banner.md)]


Norėdama pakeisti apskaitos arba ataskaitų valiutą, įmonė turi du pasirinkimus. Pirmuoju būdu galima kurti naują įmonę ir pradėti naują veiklą. Antruoju būdu galima vykdyti apskaitos ir ataskaitų valiutos konvertavimo procesą. Tai labai ilgai trunkantis procesas, kurio metu pakeičiamos visos sistemos operacijos. Prieš vykdant procesą taip pat reikia atlikti kelis sąrankos veiksmus.

## <a name="preparing-the-legal-entity-for-currency-conversion"></a>Juridinio subjekto parengimas valiutos konvertavimui
Norėdami konvertuoti juridinio subjekto valiutą, pirmiausia turite sugrąžinti visas klientų ir tiekėjų sąskaitų užsienio valiutos kurso pasikeitimo sumas ir uždaryti ankstesnius finansinius metus. Taip pat turite parengti duomenų bazę konvertavimui, tada atlikti reikiamus juridinio subjekto sąskaitos, kurioje konvertuojama valiuta, pakeitimus. Konvertavę valiutą turite atlikti kelias papildomas procedūras. Turite suderinti konvertuotų sumų apvalinimo skirtumus, perskaičiuoti verslo statistiką, įtraukti DK operacijas į žurnalą, apriboti prieigą prie konvertavimo įrankio ir perkainoti kliento ir tiekėjo sąskaitų užsienio valiutos sumas.

## <a name="setting-up-accounts-for-automatic-transactions"></a>Automatinių operacijų sąskaitų nustatymas
Valiutos konvertavimo proceso metu pelnas ar nuostoliai arba centų skirtumas yra užregistruojamas sąskaitose, nurodytose puslapyje **Automatinių operacijų sąskaitos**. Prieš vykdant konvertavimo procesą pagrindines sąskaitas reikia priskirti toliau nurodytų tipų operacijoms.

-   Apskaitos valiutos konvertavimo pelnas
-   Apskaitos valiutos konvertavimo nuostoliai
-   Skirtumas centais apskaitos valiuta
-   Skirtumas centais ataskaitų valiuta
-   Metų laikotarpio rezultatas

## <a name="posting-rounding-differences-and-sum-recalculations"></a>Apvalinimo skirtumų registravimas sumų perskaičiavimas
Toliau pateikta informacija, kur gali susidaryti apvalinimo skirtumų.

-   Jei prekių kainos buvo konvertuotos į 0 (nulį), sugeneruojama ataskaita, kurioje rodomas produkto numeris, modulio tipas, kaina prieš konvertavimą ir vienetas.
-   Apvalinimo skirtumai tarp PVM ir didžiosios knygos registruojami bendrajame žurnale.
-   Perskaičiuojamos užsienio valiutos kurso pasikeitimo sumos ir kliento bei tiekėjo operacijų sumos.
-   Sukuriami kiekvienos kliento ir tiekėjo operacijos apvalinimo skirtumų kliento ir tiekėjo sudengimo įrašai.
-   Klientų ir tiekėjų apvalinimo skirtumai registruojami bendrajame žurnale.
-   Perskaičiuojamos uždarytų atsargų operacijų sudengtos išlaidų sumos ir išlaidų koregavimo sumos.
-   Dalyje Atsargų valdymas esantys apvalinimo skirtumai užregistruojami bendrajame žurnale.
-   Perskaičiuojamos turimos atsargos.
-   Perskaičiuojamos didžiosios knygos žurnalų bendrosios sumos.
-   Perskaičiuojami didžiosios knygos uždarymo lapai.
-   Perskaičiuojami didžiosios knygos balansai.
-   Didžiojoje knygoje esantys apvalinimo skirtumai užregistruojami bendrajame žurnale.
-   Perskaičiuojamos didžiosios knygos atidarymo operacijos.
-   Apskaičiuojama galutinė didžiosios knygos balansų suma.

Jei konvertuojate į naują DK apskaitos valiutą ir perskaičiuojant bendrąsias sumas arba registruojant apvalinimo skirtumus įvyko klaida, turite uždaryti puslapį **DK apskaitos valiutos konvertavimas**. Tada bus perskaičiuotos bendrosios sumos ir užregistruoti apvalinimo skirtumai.

## <a name="processing-the-currency-conversion"></a>Valiutos konvertavimo apdorojimas
Kai pradedate valiutos konvertavimo procesą, visi vartotojai turi būti atsijungę nuo sistemos. Turite nustatyti naują DK arba ataskaitų valiutą ir valiutų kursus. Kai spustelite **Gerai**, procesas pradedamas vykdyti ir sistemoje atnaujinamos visos operacijos. Valiutos konvertavimas yra labai ilgas procesas. Kai jis bus baigtas, pamatysite, kad apskaitos arba ataskaitų valiuta bus atnaujinta puslapyje **DK**.

## <a name="completing-the-currency-conversion"></a>Valiutos konvertavimo baigimas
Po valiutos konvertavimo turi būti iš naujo sugeneruotos visos suderinimo ataskaitos, kad nekiltų abejonių, ar visos konvertuotos sumos yra teisingos.

-   Jei konvertavus DK apskaitos valiutą atsirado apvalinimo skirtumų, jie nėra registruojami naudojant kvitą, kuriame atsirado apvalinimo skirtumas. Skirtumai užregistruojami naudojant nurodytą konvertavimo registravimo kvitą. Po konvertavimo visose ataskaitose, kurios tikrinamos pagal kvitą ir datą, bus įtraukti šie apvalinimo skirtumai. Tai yra teisinga ir to galima nepaisyti.
-   Jei kliento ir tiekėjo suderinimo ataskaitose skirtumo suma rodoma kaip bendra eilučių suma, o prieš konvertavimą skirtumo sumos nebuvo, šią skirtumo sumą reikia registruoti. Sąskaita yra klientų ir tiekėjų suminė sąskaita. Korespondentinė sąskaita yra konvertavimo nuostolio arba konvertavimo pelno DK sąskaita.

Kai visi DK operacijų žurnalai panaikinti, DK operacijas galima įtraukti į žurnalą. Spustelėkite **DK** &gt; **Laikotarpio** &gt; **Žurnalai** &gt; **Įtraukimas į žurnalą**. Užsienio valiutos sumas galima perkainoti atlikus valiutos konvertavimą, jei perkainojimas būtinas. Užsienio valiutos sumas galima perkainoti, perkainojimo lauke **Metodas** pasirinkus **Standartinis**.

Daugiau informacijos žr. [Į žurnalą įtraukti užregistruotus žurnalo įrašus](tasks/journalize-posted-journal-entries.md).


