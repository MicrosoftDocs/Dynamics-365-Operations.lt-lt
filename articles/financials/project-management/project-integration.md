---
title: „Microsoft Project“ kliento integravimas
description: Planuoti ir tvarkyti projekto grafiką gali būti sudėtinga, todėl projektų vadovai turi naudoti įrankius, padedančius šią užduotį valdyti. Atlikus integravimą su „Microsoft Project“ klientu, galima atidaryti ir valdyti projekto darbo paskirstymo struktūrą.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 04b76b6c097a82e73aba007bff82b58dbbd6eb17
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838348"
---
# <a name="microsoft-project-client-integration"></a>„Microsoft Project“ kliento integravimas

[!include [banner](../includes/banner.md)]

Planuoti ir tvarkyti projekto grafiką gali būti sudėtinga, todėl projektų vadovai turi naudoti įrankius, padedančius šią užduotį valdyti. Atlikus integravimą su „Microsoft Project“ klientu, galima atidaryti ir valdyti projekto darbo paskirstymo struktūrą. Projekto vadovas bet kokius keitimus gali publikuoti atgal į „Finance and Operations“ projekto darbo paskirstymo struktūrą.

> [!NOTE]
> Jei naudojate „Microsoft Dynamics 365 for Finance and Operations“ su 2017 m. liepos mėn. naujinimu, turite įdiegti KB 4054797 ir 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>„Microsoft Project“ kliento papildinio konfigūravimas
Norint įjungti integravimo su „Microsoft Project“ klientu funkciją, vartotojo „Microsoft Project“ kliento programoje reikia įdiegti „Microsoft Dynamics 365“ papildinį. Tai daroma atidarant **darbo sritį Projektų valdymas**.

•   Darbo srities skyriuje **Saitai** > **Sąranka** spustelėkite **Konfigūruoti projekto kliento papildinį**.

•   Paraginti spustelėkite **Atidaryti**, tada – **Paleisti**.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Esamo darbo paskirstymo struktūros juodraščio atidarymas ir redagavimas „Microsoft Project“ kliente
Jei „Finance and Operations“ projektui darbo paskirstymo struktūra jau sukurta ir ji yra juodraščio būsenos, ją galima atidaryti „Microsoft Project“ kliento programoje. Norėdami ją atidaryti puslapyje **Projektas**, skirtuke **Planas** spustelėkite saitą **Atidaryti naudojant „Microsoft Project“**. Šį puslapį taip pat galima atidaryti „Microsoft Project“ kliento programoje, skirtuke **„Microsoft Dynamics 365**“ spustelėjus **Atidaryti**. Sąraše pasirinkite **Juridinis subjektas** ir **Projektas**.

> [!NOTE]
> Jei kaip naršyklę naudojate „Internet Explorer“, turėsite spustelėti **Įrašyti**, kad failą galėtumėte rankiniu būdu atidaryti iš vietos, kurioje jis atsiunčiamas. Arba spustelėkite **Įrašyti ir atidaryti**, kad failą atidarytumėte „Microsoft Project“ kliente. Įrašydami failą, jo nepervardykite.

Prieš failą redaguodami „Microsoft Project“ kliente, jį turite paimti ir užrakinti. Skirtuke **Microsoft Dynamics 365** spustelėkite **Paimti ir užrakinti**. Tai neleis kitiems vartotojams tuo pačiu metu darbo paskirstymo struktūros redaguoti naudojant „Finance and Operations“. Jei, baigę redaguoti darbo paskirstymo struktūrą, norite ją publikuoti, skirtuke **Microsoft Dynamics 365** spustelėkite **Įrašyti ir atrakinti**.

Jei į „Finance and Operations“ projektą jau įtraukta projekto komanda, išteklių sąrašas bus užpildytas komandos nariais. Jei projekto komanda į projektą dar neįtraukta, galite pasirinkti išteklių ir komandą sukurti „Microsoft Project“ kliente – skirtuke **Microsoft Dynamics 365** spustelėkite mygtuką **Ištekliai**. 

Įrašymo ir atrakinimo proceso metu su „Finance and Operations“ vėl bus sinchronizuojami tolesni duomenys.

•   Užduoties pavadinimas

•   Pradžios data

•   Pabaigos data

•   Ankstesnė veikla

•   Išteklių pavadinimai

•   Kategorija

•   Išteklių kategorija

•   Darbo valandos

•   Pastabos

•   Pirmenybė

> [!NOTE]
> Jei į savo „Microsoft Project“ kliento failą įtraukėte kitų stulpelių, jie nebus įrašyti ir, vėl atidarius failą, jie nebus rodomi.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Esamo projekto darbo paskirstymo struktūros kūrimas naudojant „Microsoft Project“ klientą
Jei norite naudodami „Microsoft Project“ klientą sukurti naują darbo paskirstymo struktūrą, atlikite tolesnius veiksmus.


1.  Atidarykite „Microsoft Project“ klientą.

2.  Skirtuke **Microsoft Dynamics 365** spustelėkite **Atidaryti**.

3.  Pasirinkite projekto **juridinį subjektą**.

4.  Pasirinkite **Projektas**.

5.  Skirtuke **Microsoft Dynamics 365** spustelėkite **Paimti ir užrakinti**.

6.  Kai būsite pasirengę ją publikuoti sprendime „Finance and Operations“, skirtuke **Microsoft Dynamics 365** spustelėkite **Įrašyti ir atrakinti**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Esamo projekto esamos darbo paskirstymo struktūros pakeitimas naudojant „Microsoft Project“ klientą
Jei norite naudodami „Microsoft Project“ klientą sukurti naują darbo paskirstymo struktūrą ir pakeisti esamo projekto esamą darbo paskirstymo struktūrą, atlikite tolesnius veiksmus.

1.  Atidarykite „Microsoft Project“ klientą.

2.  „Microsoft Project“ kliente sukurkite grafiką.

3.  Skirtuke **Microsoft Dynamics 365** spustelėkite **Įrašyti keitimus** >  **Pakeisti esamą projektą**.

4.  Pasirinkite projekto **juridinį subjektą**.

5.  Pasirinkite **Projektas**.

6.  Spustelėkite **Gerai**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Naujo projekto kūrimas „Microsoft Project“ kliente


1.  Atidarykite „Microsoft Project“ klientą.

2.  „Microsoft Project“ kliente sukurkite grafiką.

3.  Skirtuke **Microsoft Dynamics 365** spustelėkite **Įrašyti keitimus** > **Įrašyti į naują projektą**.

4.  Pasirinkite projekto **juridinį subjektą**.

5.  Jei reikia, įveskite **Projekto ID**.

6.  Įveskite **Projekto pavadinimą**.

7.  Pasirinkite **Projekto tipą**, **Projektų grupę** ir **Projekto sutarties ID**. Taip pat naują projekto sutartį galite sukurti spustelėdami **Naujas**.

8.  Pasirinkite **kalendorių**, kuris bus naudojamas su ištekliais.

11. Spustelėkite **Gerai**.
