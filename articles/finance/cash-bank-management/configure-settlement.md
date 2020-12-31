---
title: Sudengimo konfigūravimas
description: Tai, kaip ir kada operacijos sudengiamos, gali būti sudėtinga, todėl labai svarbu, kad suprastumėte ir tinkamai nustatytumėte parametrus, kad jie atitiktų jūsų verslo poreikius. Šioje temoje aprašyti parametrai, kurie naudojami mokėtinoms sumoms ir gautinoms sumoms sudengti.
author: kweekley
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 094b8876b3b10b6dcbc0ce399a1a9915271459ed
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446132"
---
# <a name="configure-settlement"></a>Sudengimo konfigūravimas

[!include [banner](../includes/banner.md)]

Tai, kaip ir kada operacijos sudengiamos, gali būti sudėtinga, todėl labai svarbu, kad suprastumėte ir tinkamai nustatytumėte parametrus, kad jie atitiktų jūsų verslo poreikius. Šioje temoje aprašyti parametrai, kurie naudojami mokėtinoms sumoms ir gautinoms sumoms sudengti. 

Šie parametrai lemia, kaip „Microsoft Dynamics 365 Finance“ apdoroja sudengimus. Sudengimas yra procesas, kurio metu SF sudengiama su mokėjimu arba kredito pažyma. Šie parametrai yra srityje **Sudengimas** puslapiuose **Gautinų sumų parametrai** ir **Mokėtinų sumų parametrai**.

- **Automatinis sudengimas** – nustatykite šios parinkties reikšmę **Taip**, jei operacija turi būti sudengta automatiškai su kitomis atidarytomis operacijomis, kai ji registruojama. Jei šiai parinkčiai nustatyta reikšmė **Ne**, vartotojai gali rankiniu būdu sudengti operacijas, kai jie įveda mokėjimus arba vėliau, naudodami puslapį **Sudengti operacijas**.
- **Mokėjimo nuolaidos administravimas** – nurodykite, kaip [tvarkoma mokėjimo nuolaida, kai SF yra permokėta](cash-discount-handling-overpayments.md). Įvykus permokėjimui, mokėjimo nuolaida gali būti sumažinta, ji gali būti laikoma skirtumu arba ji gali likti tiekėjo ar kliento sąskaitoje.
  -   **Nespecifinis** – mokėjimo nuolaidos suma sumažinama permokėta suma. Šis veiksmas visada naudojamas, neatsižvelgiant, ar permokėjimo suma didesnė ar mažesnė už lauke **Didžiausias permokėjimas arba neprimokėjimas** įvestą sumą.
  -   **Specifinis** – permokėjimo suma yra užregistruojama į mokėjimo nuolaidų skirtumų DK sąskaitą arba lieka kaip balansas kliento ar tiekėjo sąskaitoje. Atliekamą specifinį veiksmą lemia, ar permokėjimo suma yra tarp 0,00 ir lauke **Didžiausias permokėjimas arba neprimokėjimas** įvestos sumos, ar permokėjimo suma yra didesnė už lauko **Didžiausias permokėjimas arba neprimokėjimas** sumą.
- **Didžiausias skirtumas centais** – įveskite didžiausią leidžiamą sudengtų operacijų skirtumą centais. Jei skirtumas centais yra lygus arba mažesnis už šiame lauke nurodytą skirtumą, skirtumasužregistruojamas skirtumo centais DK sąskaitoje, kuri yra nurodyta puslapyje **Automatinių operacijų sąskaitos**.
- **Didžiausias permokėjimas arba neprimokėjimas** – įveskite priimtą permokėjimo ar neprimokėjimo sumą. Norėdami apskaičiuoti permokėjimo ar neprimokėjimo mokestį, puslapyje **DK parametrai** spustelėkite **PVM** ir pasirinkite parinktį **PVM permokėjimas arba neprimokėjimas**.
  -   Jei skaičiuojant permokėjimą arba neprimokėjimą atsiranda centų skirtumas, kuris yra mažesnis nei skirtumas, nurodytas lauke **Didžiausias skirtumas centais**, centų skirtumo suma yra užregistruojama centų skirtumo sąskaitoje.
  -   Jei skaičiuojant permokėjimą arba neprimokėjimą atsiranda skirtumas, kuris yra didesnis nei skirtumas, nurodytas lauke **Didžiausias skirtumas centais**, skirtumo suma yra užregistruojama skirtumo sąskaitoje, kuri pasirenkama registravimo tipui **Kliento mokėjimo nuolaida** arba **Tiekėjo mokėjimo nuolaida** puslapyje **Automatinių operacijų sąskaitos**.
- **Skaičiuoti dalinių mokėjimų nuolaidas** – nustatykite šiai parinkčiai reikšmę **Taip**, kad būtų automatiškai apskaičiuojamos dalinių mokėjimų nuolaidos.
  -   Šios parinkties poveikis priklauso nuo lauko **Naudoti mokėjimo nuolaidą** reikšmės puslapyje **Sudengti operacijas**. Jei šiai parinkčiai nustatyta reikšmė **Taip**, nuolaida paimama, kai laukui **Naudoti mokėjimo nuolaidą** nustatyta reikšmė **Įprasta**. Kai laukui **Naudoti mokėjimo nuolaidą** nustatyta reikšmė **Visada**, mokėjimo nuolaida paimama visada, nepriklausomai nuo šio lauko nustatymo. Kai laukui **Naudoti mokėjimo nuolaidą** nustatyta reikšmė **Niekada**, mokėjimo nuolaida niekada neimama, nepriklausomai nuo šio lauko nustatymo.
  -   Jei šiai parinkčiai nustatyta reikšmė **Taip** ir vartotojas pakeičia lauko **Sudengtina suma** reikšmę puslapyje **Sudengti operacijas**, nuolaida apskaičiuojama automatiškai ir rodoma kaip numatytasis lauko **Taikytinos mokėjimo nuolaidos suma** įrašas.
  -   Jei šiai parinkčiai nustatyta reikšmė **Ne** ir vartotojas pakeičia lauko **Sudengtina suma** reikšmę puslapyje **Sudengti operacijas**, numatytasis lauko **Taikytinos mokėjimo nuolaidos suma** įrašas yra **0** (nulis).
- **Skaičiuoti kredito pažymų mokėjimo nuolaidas** – nustatykite šiai parinkčiai reikšmę **Taip**, kad automatiškai apskaičiuotumėte kredito pažymų mokėjimo nuolaidą. Naudojant modulį „Gautinos sumos“, kredito pažymos operacija yra neigiama operacija, kurios reikšmė nurodyta lauke **SF** puslapyje **Laisvos formos SF** arba grąžinimą puslapyje **Pardavimo užsakymas**.
  - Šios parinkties poveikis priklauso nuo lauko <strong>Naudoti mokėjimo nuolaidą</strong> reikšmės puslapyje <strong>Sudengti operacijas</strong>. Jei šiai parinkčiai nustatyta reikšmė <strong>Taip</strong>, nuolaida paimama, kai laukui *<strong><em>Naudoti mokėjimo nuolaidą</em></strong>* nustatyta reikšmė <strong>Įprasta</strong>. Kai laukui *<strong><em>Naudoti mokėjimo nuolaidą</em></strong>* nustatyta reikšmė <strong>Visada</strong>, mokėjimo nuolaida paimama visada, nepriklausomai nuo šio lauko parametro. Kai laukui *<strong><em>Naudoti mokėjimo nuolaidą</em></strong>* nustatyta reikšmė <strong>Niekada</strong>, mokėjimo nuolaida niekada neimama, nepriklausomai nuo šio lauko parametro.
  - Jei šiai parinkčiai nustatyta reikšmė **Taip**, o puslapyje **Sudengti operacijas** pažymėta kredito pažyma, nuolaida apskaičiuojama automatiškai ir yra rodoma kaip numatytasis lauko **Taikytinos mokėjimo nuolaidos suma** įrašas.
  - Jei šiai parinkčiai nustatyta reikšmė **Ne**, o puslapyje **Sudengti operacijas** pažymėta kredito pažyma, numatytasis lauko **Taikytinos mokėjimo nuolaidos suma** įrašas yra **0** (nulis).

- **Nuolaidos korespondentinės sąskaitos (tik AP)** – apibrėžkite numatytąją mokėjimo nuolaidos DK sąskaitą, kuri turi būti naudojama mokėjimo nuolaidų apskaitos įrašui.
  -   **Naudoti pagrindinę sąskaitą, skirtą tiekėjo nuolaidoms** – mokėjimo nuolaida užregistruojama į pagrindinę sąskaitą, kuri apibrėžta puslapyje **Mokėjimo nuolaidos nustatymas**.
  -   **Sąskaitos SF eilutėse** – mokėjimo nuolaida užregistruojama į DK sąskaitas, nurodytas originalioje sąskaitoje faktūroje.
- **Pažymėti eilutes laisvos formos SF ir delspinigių pažymose (tik AR)** – nustatykite šiai parinkčiai reikšmę **Taip**, kad įgalintumėte mygtuką **Pažymėti SF eilutes** puslapiuose **Įvesti kliento mokėjimus**, **Mokėjimo žurnalo kvitas** ir **Sudengti operacijas**. Šis mygtukas leidžia vartotojams pažymėti atskiras eilutes sudengimui.
- **Nustatyti sudengimo prioritetą (tik AR)** – nustatykite šiai parinkčiai reikšmę **Taip**, kad įgalintumėte mygtuką **Žymėti pagal prioritetą** puslapiuose **Įvesti kliento mokėjimus** ir **Sudengti operacijas**. Šis mygtukas vartotojams suteikia galimybę priskirti iš anksto nustatytą operacijų sudengimo tvarką.  Pritaikius operacijai sudengimo tvarką, šią tvarką ir mokėjimo paskirstymą galima modifikuoti prieš registruojant.
- **Naudoti prioritetą automatiniams sudengimams atlikti** – nustatykite šios parinkties reikšmę **Taip**, kad taikytumėte nustatytą prioritetinę tvarką, kai operacijos sudengiamos automatiškai. Šis laukas galimas tik tada, jei parinktims **Nustatyti sudengimo prioritetą** ir **Automatinis sudengimas** nustatyta reikšmė **Taip**.

## <a name="fixed-dimensions-on-accounts-receivableaccounts-payable-main-accounts"></a>Fiksuotos dimensijos gautinos / mokėtinos sumos pagrindinėse sąskaitose

Kai gautinų / mokėtinų sumų pagrindinėje sąskaitoje naudojamos fiksuotos dimensijos, sudengimo procesas užregistruos du papildomus apskaitos įrašus ir dvi papildomas tiekėjo operacijas. Sudengimo funkcija palygins gautinų / mokėtinų sumų DK sąskaitą, nurodytą SF, su mokėjimu.  Kartu su apmokėjimu įvykdžius ir sudengimą, kas paprastai ir yra daroma, mokėjimo apskaitos įrašas didžiojoje knygoje nebus užregistruotas tol, kol taip pat nebus atliktas atsiskaitymo procesas. Dėl apdorojimo įvykių tvarkos sudengimo funkcija negali nustatyti faktinių gautinų / mokėtinų sumų mokėjimo apskaitos įrašo DK sąskaitoje. Sudengimo funkcija atkuria būsimą mokėjimo DK sąskaitą. Kai gautinų / mokėtinų sumų pagrindinėje sąskaitoje naudojama fiksuota dimensija, tai tampa problema.

Kad būtų atkurta DK sąskaita, kaip nurodyta mokėjimų žurnale iš registravimo šablono gaunama gautinų / mokėtinų sumų pagrindinė sąskaita, o iš tiekėjo mokėjimo operacijos įrašo – finansinės dimensijos. Fiksuotos dimensijos mokėjimų žurnaluose nenumatomos, o vietoj to pritaikomos pagrindinėje sąskaitoje kaip paskutinis registravimo proceso veiksmas. Dėl to fiksuotos dimensijos reikšmė galimai nebus įtraukta į tiekėjo operaciją, nebent ji bus numatyta kitame šaltinyje, pvz., tiekėjo. Atkurtoje sąskaitoje nebus įtraukta fiksuotoji dimensija. Sudengimo apdorojimo funkcija nustatys, kad turi būti sukurtas reguliavimo įrašas, nes SF, užregistruotoje su fiksuotos dimensijos reikšme ir atkurto mokėjimo sąskaita, jis sukurtas nebuvo.  Sudengimo funkcijai toliau registruojant reguliavimo įrašą, atliekamas paskutinis registravimo veiksmas, skirtas taikytinai fiksuotai dimensijai. Prie reguliavimo įrašo pridėjus fiksuotą dimensiją, ji užregistruojama su debetu ir kreditu toje pačioje DK sąskaitoje. Naudojant sudengimo funkciją, apskaitos įrašo atšaukti negalima.

Norint išvengti papildomų apskaitos įrašų, debeto ir kredito toje pačioje DK sąskaitoje, priklausomai nuo verslo poreikių reikėtų atsižvelgti į toliau pateiktus sprendimo būdus. 

-   Organizacijos dažnai naudoja fiksuotas dimensijas, kad nereikalingą finansinę dimensiją užpildytų nuliais. Tai paprastai daroma su balanso sąskaitomis, pvz., gautinomis / mokėtinomis sumomis. Sąskaitos struktūrą galima panaudoti tam, kad finansinės dimensijos, kurios paprastai užpildomos nuliais, nebūtų sekamos.  Iš balanso sąskaitų galite pašalinti finansinę dimensiją, kad nereikėtų naudoti fiksuotų dimensijų.
-   Jei jūsų organizacija reikalauja, kad gautinų / mokėtinų sumų pagrindinėje sąskaitoje būtų nurodytos fiksuotos dimensijos, raskite būdą, kaip mokėjime nustatyti numatytąją fiksuotą dimensiją, kad fiksuotos dimensijos reikšmė būtų saugoma tiekėjo mokėjimo operacijos srityje. Tokiu būdu sistema atkurs gautinas / mokėtinas sumas pagrindinėje sąskaitoje, įtraukdama fiksuotas dimensijos reikšmes. Fiksuotos dimensijos reikšmę kaip numatytąją galima apibrėžti tiekėjų arba mokėjimų žurnalo pavadinimo srityje.
