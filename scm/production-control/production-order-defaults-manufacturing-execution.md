---
title: "Gamybos užsakymo nutylėjimą laiko kontrolės"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70073
ms.assetid: 620944ae-3e20-444a-807e-65495f160904
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: b310e799c1ef0756291c5f7ab886531e4caf1945
ms.lasthandoff: 03/31/2017


---

# <a name="production-order-defaults-in-manufacturing-execution"></a>Gamybos užsakymo nutylėjimą laiko kontrolės



Jums reikia atidžiai apsvarstyti visus parametrus ant to **gamybos užsakymą pagal nutylėjimą** puslapyje prieš darbuotojams pradedant padaryti registracijos gamybos užduočių. Jei jūsų įmonė naudoja kelių teritorijų funkcijos, galite nustatyti skirtingas numatytąsias reikšmes gamybos užsakymai kiekvienai svetainei. Integravimo su Gamybos kontrole užsakymo numatytieji nustatymai nustatomi šiuose skirtukuose puslapyje **Gamybos užsakymo numatytoji informacija**:

-   **Bendra** – bendra gamybos užduočių užsakymo numatytoji informacija dalyje Gamybos vykdymas.
-   **Pradėti** – numatytoji užsakymo informacija, kuri naudojama pradėjus gamybos užduotis arba operacijas.
-   **Operacijos** – numatytoji užsakymo informacija, kuri taikomi gamybos užduotims arba operacijoms ir atsiliepimams apie operacijas gamybos proceso metu.
-   **Skelbti baigtu** – numatytoji užsakymo informacija, taikoma tada, kai prekės paskelbtos kaip baigtos atliekant paskutinę gamybos užsakymo operaciją.
-   **Kiekio tikrinimas** – numatytoji užsakymo informacija, skirta tikrinti gamybos užsakymų pradžios ir grįžtamojo ryšio kiekius.

## <a name="types-of-production-jobs"></a>Gamybos užduočių tipai
Skirtuke **Operacijos** pasirinkite gamybos užduočių tipus, kuriuos reikia registruoti puslapyje **Užduoties registracija**. Paprastai darbuotojai atlieka nustatymų užduočių ir apdorojimo užduočių registraciją. Tačiau jeigu taikomas užduočių planavimas, galite pasirinkti kitus užduočių tipus, pvz., transportavimo užduotis, kurias darbuotojai taip pat turi registruoti, kai apdorojamas gamybos užsakymas. **Svarbu:** įsitikinkite, kad pasirinkti visi tinkami užduočių tipai. Kitu atveju užduočių gali nepavykti užregistruoti puslapyje **Užduoties registravimas**. Sulygiuokite savo pasirinkimus su stulpelyje **Užduoties valdymas**, puslapyje **Maršrutų grupės**, atliktais pasirinkimais. Jei **Užduoties valdymas** pasirinktas maršruto grupėje, gamybos užsakymo užduoties tipas bus paskelbtas baigtu. Ši ataskaita pateikiama, kai užduotis paskelbta baigta dalyje Gamybos vykdymas. Kai visi operacijos užduočių tipai, kuriems pasirinktas **Užduoties valdymas**, paskelbti baigtais, dalyje Gamybos vykdymas operacija taip pat bus paskelbta baigta. **Pastaba:** kai kurių užduočių tipų ataskaitas galima pateikti rankiniu būdu gamybos žurnaluose. Tokiu atveju pasirinkite užduoties tipo **Užduoties valdymas**, bet nesirinkite užduoties tipo registruoti skirtuke **Operacijos**, puslapyje **Gamybos užsakymo numatytoji informacija**.

## <a name="bom-consumption-and-picking-list-journals"></a>KS suvartojimo ir išrinkimo dokumentų žurnalai
Medžiagas galima nustatyti taip, kad gamybos metu jos būtų suvartojamos arba automatiškai, arba rankiniu būdu. Automatinį suvartojimą valdo sunaudojimo principas, nustatytas komplektavimo specifikacijos (KS) eilutėse ir nustačius gamybos užsakymo numatytosios informacijos lauką **Automatinis KS suvartojimas**. Automatinį suvartojimą galima nustatyti taip, kad jis vyktų tada, kai gamybos užsakymas yra pradėtas arba paskelbtas baigtu. Kitu atveju, jis gali vykti darbo lygiu, kai užduotis yra pradėta arba baigta.

### <a name="controlling-material-consumption-when-a-production-order-is-started"></a>Medžiagų suvartojimo valdymas, kai gamybos užsakymas pradėtas

Medžiagų suvartojimas gamybos užsakymo pradžioje yra valdomas naudojant lauką **Automatinis KS suvartojimas**, esantį skirtuke **Pradėti**. Galimos šios vertės:

-   **Sunaudojimo principas** – pradėjus gamybos užsakymą, medžiagų kiekis bus sunaudotas pagal sunaudojimo principą, kuris nustatytas KS eilutėse. Tik tos medžiagų eilutės, kuriose sunaudojimo principas nustatytas kaip **Pradėti**, bus naudojamos gamybos pradžioje.
-   **Visada** – visada bus naudojami tie medžiagų kiekiai, kurie yra proporcingi pradžios kiekiams.
-   **Niekada** – medžiagų kiekiai niekada nebus naudojami.

### <a name="controlling-material-consumption-when-a-production-job-is-started-or-completed"></a>Medžiagų sunaudojimo valdymas, kai gamybos užduotis pradėta arba baigta

Medžiagų sunaudojimas gamybos užduoties pradžioje arba pabaigoje yra valdomas naudojant lauką **Automatinis KS suvartojimas**, esantį skirtuke **Operacijos**. Galimos šios vertės:

-   **Sunaudojimo principas** – kai gamybos užduoties medžiagų kiekis pradėtas arba baigtas, medžiagų kiekis bus sunaudotas pagal sunaudojimo principą, kuris nustatytas KS eilutėse. Bus naudojamos tik tos medžiagų eilutės, kuriose sunaudojimo principas nustatytas kaip **Pradėti** arba **Baigti**.
-   **Visada** – visada bus naudojami tie medžiagų kiekiai, kurie yra proporcingi užduoties pradžios kiekiams.
-   **Niekada** – medžiagų kiekiai niekada nebus naudojami.

### <a name="controlling-material-consumption-when-a-production-order-is-reported-as-finished"></a>Medžiagų suvartojimo valdymas, kai gamybos užsakymas paskelbtas baigtu

Medžiagų sunaudojimas gamybos užsakymo proceso Skelbti baigtu metu yra valdomas naudojant lauką **Automatinis KS suvartojimas**, esantį skirtuke **Skelbti baigtu**. Galimos šios vertės:

-   **Sunaudojimo principas** – kai gamybos užsakymas paskelbtas baigtu, medžiagų kiekis bus sunaudotas pagal sunaudojimo principą, kuris nustatytas KS eilutėse. Bus naudojamos tik tos medžiagų eilutės, kuriose sunaudojimo principas nustatytas kaip **Baigti**.
-   **Visada** – visada bus naudojami tie medžiagų kiekiai, kurie yra proporcingi paskelbimo baigtu kiekiams.
-   **Niekada** – medžiagų kiekiai niekada nebus naudojami.



