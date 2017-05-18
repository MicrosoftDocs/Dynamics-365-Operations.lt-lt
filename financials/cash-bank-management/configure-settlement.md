---
title: "Sudengimo konfigūravimas"
description: "Tai, kaip ir kada operacijos sudengiamos, gali būti sudėtinga, todėl labai svarbu, kad suprastumėte ir tinkamai nustatytumėte parametrus, kad jie atitiktų jūsų verslo poreikius. Šiame straipsnyje aprašyti parametrai, kurie naudojami Mokėtinoms sumoms ir Gautinoms sumoms sudengti."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: dd10b2ebe1871f5845b1f245e259c8647a4408c1
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="configure-settlement"></a>Sudengimo konfigūravimas

[!include[banner](../includes/banner.md)]


Tai, kaip ir kada operacijos sudengiamos, gali būti sudėtinga, todėl labai svarbu, kad suprastumėte ir tinkamai nustatytumėte parametrus, kad jie atitiktų jūsų verslo poreikius. Šiame straipsnyje aprašyti parametrai, kurie naudojami Mokėtinoms sumoms ir Gautinoms sumoms sudengti. 

Šie parametrai lemia, kaip „Microsoft Dynamics 365 for Operations“ apdoroja sudengimus. Sudengimas yra procesas, kurio metu SF sudengiama su mokėjimu arba kredito pažyma. Šie parametrai yra srityje **Sudengimas** puslapiuose **Gautinų sumų parametrai** ir **Mokėtinų sumų parametrai**.

-   **Automatinis sudengimas** – nustatykite šios parinkties reikšmę **Taip**, jei operacija turi būti sudengta automatiškai su kitomis atidarytomis operacijomis, kai ji registruojama. Jei šiai parinkčiai nustatyta reikšmė **Ne**, vartotojai gali rankiniu būdu sudengti operacijas, kai jie įveda mokėjimus arba vėliau, naudodami puslapį **Sudengti operacijas**.
-   **Mokėjimo nuolaidos administravimas** – nurodykite, kaip [tvarkoma mokėjimo nuolaida, kai SF yra permokėta](cash-discount-handling-overpayments.md). Įvykus permokėjimui, mokėjimo nuolaida gali būti sumažinta, ji gali būti laikoma skirtumu arba ji gali likti tiekėjo ar kliento sąskaitoje.
    -   **Nespecifinis** – mokėjimo nuolaidos suma sumažinama permokėta suma. Šis veiksmas visada naudojamas, neatsižvelgiant, ar permokėjimo suma didesnė ar mažesnė už lauke **Didžiausias permokėjimas arba neprimokėjimas** įvestą sumą.
    -   **Specifinis** – permokėjimo suma yra užregistruojama į mokėjimo nuolaidų skirtumų DK sąskaitą arba lieka kaip balansas kliento ar tiekėjo sąskaitoje. Atliekamą specifinį veiksmą lemia, ar permokėjimo suma yra tarp 0,00 ir lauke **Didžiausias permokėjimas arba neprimokėjimas** įvestos sumos, ar permokėjimo suma yra didesnė už lauko **Didžiausias permokėjimas arba neprimokėjimas** sumą.
-   **Didžiausias skirtumas centais** – įveskite didžiausią leidžiamą sudengtų operacijų skirtumą centais. Jei skirtumas centais yra lygus arba mažesnis už šiame lauke nurodytą skirtumą, skirtumasužregistruojamas skirtumo centais DK sąskaitoje, kuri yra nurodyta puslapyje **Automatinių operacijų sąskaitos**.
-   **Didžiausias permokėjimas arba neprimokėjimas** – įveskite priimtą permokėjimo ar neprimokėjimo sumą. Norėdami apskaičiuoti permokėjimo ar neprimokėjimo mokestį, puslapyje **DK parametrai** spustelėkite **PVM** ir pasirinkite parinktį **PVM permokėjimas arba neprimokėjimas**.
    -   Jei skaičiuojant permokėjimą arba neprimokėjimą atsiranda centų skirtumas, kuris yra mažesnis nei skirtumas, nurodytas lauke **Didžiausias skirtumas centais**, centų skirtumo suma yra užregistruojama centų skirtumo sąskaitoje.
    -   Jei skaičiuojant permokėjimą arba neprimokėjimą atsiranda skirtumas, kuris yra didesnis nei skirtumas, nurodytas lauke **Didžiausias skirtumas centais**, skirtumo suma yra užregistruojama skirtumo sąskaitoje, kuri pasirenkama registravimo tipui **Kliento mokėjimo nuolaida** arba **Tiekėjo mokėjimo nuolaida** puslapyje **Automatinių operacijų sąskaitos**.
-   **Skaičiuoti dalinių mokėjimų nuolaidas** – nustatykite šiai parinkčiai reikšmę **Taip**, kad būtų automatiškai apskaičiuojamos dalinių mokėjimų nuolaidos.
    -   Toks šios parinkties poveikis priklauso nuo lauko **Naudoti mokėjimo nuolaidą** reikšmės puslapyje **Sudengti operacijas**. Jei šiai parinkčiai nustatyta reikšmė **Taip**, nuolaida paimama, kai laukui **Naudoti mokėjimo nuolaidą** nustatyta reikšmė **Įprasta**. Kai laukui **Naudoti mokėjimo nuolaidą** nustatyta reikšmė **Visada**, mokėjimo nuolaida paimama visada, nepriklausomai nuo šio lauko nustatymo. Kai laukui **Naudoti mokėjimo nuolaidą** nustatyta reikšmė **Niekada**, mokėjimo nuolaida niekada neimama, nepriklausomai nuo šio lauko nustatymo.
    -   Jei šiai parinkčiai nustatyta reikšmė **Taip** ir vartotojas pakeičia lauko **Sudengtina suma** reikšmę puslapyje **Sudengti operacijas**, nuolaida apskaičiuojama automatiškai ir rodoma kaip numatytasis lauko **Taikytinos mokėjimo nuolaidos suma** įrašas.
    -   Jei šiai parinkčiai nustatyta reikšmė **Ne**ir vartotojas pakeičia lauko **Sudengtina suma** reikšmę puslapyje **Sudengti operacijas**, numatytasis lauko **Taikytinos mokėjimo nuolaidos suma** įrašas yra **0** (nulis).
-   **Skaičiuoti kredito pažymų mokėjimo nuolaidas** – nustatykite šiai parinkčiai reikšmę **Taip**, kad automatiškai apskaičiuotumėte kredito pažymų mokėjimo nuolaidą. Naudojant modulį „Gautinos sumos“, kredito pažymos operacija yra neigiama operacija, kurios reikšmė nurodyta lauke **SF** puslapyje **Laisvos formos SF** arba grąžinimą puslapyje **Pardavimo užsakymas**.
    -   Šios parinkties poveikis priklauso nuo lauko **Naudoti mokėjimo nuolaidą** reikšmės puslapyje **Sudengti operacijas**. Jei šiai parinkčiai nustatyta reikšmė **Taip**, nuolaida paimama, kai laukui ****Naudoti mokėjimo nuolaidą**** nustatyta reikšmė **Įprasta**. Kai laukui ****Naudoti mokėjimo nuolaidą**** nustatyta reikšmė **Visada**, mokėjimo nuolaida paimama visada, nepriklausomai nuo šio lauko nustatymo. Kai laukui ****Naudoti mokėjimo nuolaidą**** nustatyta reikšmė **Niekada**, mokėjimo nuolaida niekada neimama, nepriklausomai nuo šio lauko nustatymo.
    -   Jei šiai parinkčiai nustatyta reikšmė **Taip**, o puslapyje **Sudengti operacijas** pažymėta kredito pažyma, nuolaida apskaičiuojama automatiškai ir yra rodoma kaip numatytasis lauko **Taikytinos mokėjimo nuolaidos suma** įrašas.
    -   Jei šiai parinkčiai nustatyta reikšmė **Ne**, o puslapyje **Sudengti operacijas** pažymėta kredito pažyma, numatytasis lauko **Taikytinos mokėjimo nuolaidos suma** įrašas yra **0** (nulis).
-   **Nuolaidos korespondentinės sąskaitos (tik AP)** – apibrėžkite numatytąją mokėjimo nuolaidos DK sąskaitą, kuri turi būti naudojama mokėjimo nuolaidų apskaitos įrašui.
    -   **Naudoti pagrindinę sąskaitą, skirtą tiekėjo nuolaidoms** – mokėjimo nuolaida užregistruojama į pagrindinę sąskaitą, kuri apibrėžta puslapyje **Mokėjimo nuolaidos nustatymas**.
    -   **Sąskaitos SF eilutėse** – mokėjimo nuolaida užregistruojama į DK sąskaitas, nurodytas originalioje sąskaitoje faktūroje.
-   **Pažymėti eilutes laisvos formos SF ir delspinigių pažymose (tik AR)** – nustatykite šiai parinkčiai reikšmę **Taip**, kad įgalintumėte mygtuką **Pažymėti SF eilutes** puslapiuose **Įvesti kliento mokėjimus**, **Mokėjimo žurnalo kvitas** ir **Sudengti operacijas**. Šis mygtukas leidžia vartotojams pažymėti atskiras eilutes sudengimui.
-   **Nustatyti sudengimo prioritetą (tik AR)** – nustatykite šiai parinkčiai reikšmę **Taip**, kad įgalintumėte mygtuką **Žymėti pagal prioritetą** puslapiuose **Įvesti kliento mokėjimus** ir **Sudengti operacijas**. Šis mygtukas vartotojams suteikia galimybę priskirti iš anksto nustatytą operacijų sudengimo tvarką.  Pritaikius operacijai sudengimo tvarką, šią tvarką ir mokėjimo paskirstymą galima modifikuoti prieš registruojant.
-   **Naudoti prioritetą automatiniams sudengimams atlikti** – nustatykite šios parinkties reikšmę **Taip**, kad taikytumėte nustatytą prioritetinę tvarką, kai operacijos sudengiamos automatiškai. Šis laukas galimas tik tada, jei parinktims **Nustatyti sudengimo prioritetą** ir **Automatinis sudengimas** nustatyta reikšmė **Taip**.





