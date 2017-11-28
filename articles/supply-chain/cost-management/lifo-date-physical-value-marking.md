---
title: "LIFO data su faktine verte ir žymėjimu"
description: "Paskutinė įvesta, pirma nurašyta data (LIFO data) yra atsargų modelis, pagrįstas LIFO principu. Išdavimai iš atsargų sudengiami su paskutiniaisiais gavimais į atsargas remiantis atsargų operacijos data. Naudojant LIFO data, jei prieš išduodant prekes jos nėra gautos, išdavimas nustatomas pagal bet kurį gavimą, įvykstantį po prekės išdavimo datos. Tą pačią dieną galima sudengti keletą išdavimų paskutinio išduoto, paskutinio gauto tvarka."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 51592
ms.assetid: d9f13274-3268-444f-85c8-b686fd39286d
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0b94d3f23c929c45a67894bd08706144c9226491
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="lifo-date-with-physical-value-and-marking"></a>LIFO data su faktine verte ir žymėjimu

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Paskutinė įvesta, pirma nurašyta data (LIFO data) yra atsargų modelis, pagrįstas LIFO principu. Išdavimai iš atsargų sudengiami su paskutiniaisiais gavimais į atsargas remiantis atsargų operacijos data. Naudojant LIFO data, jei prieš išduodant prekes jos nėra gautos, išdavimas nustatomas pagal bet kurį gavimą, įvykstantį po prekės išdavimo datos. Tą pačią dieną galima sudengti keletą išdavimų paskutinio išduoto, paskutinio gauto tvarka. 

Naudodami atsargų modelį Paskutinė įvesta, pirma nurašyta data (LIFO data) atsargų modelį, jei nėra gavimo prieš išdavimą, išdavimas sudengiamas pagal bet kurį gavimą, įvykusį po išdavimo datos. Tą pačią darą galima sudengti keletą išdavimų paskutinio išduoto, paskutinio gauto tvarka. Naudojant LIFO datą nereikia naudoti LIFO datos taisyklės. Užuot ją naudoję, galite pažymėti atsargų operacijas tam, kad tam tikros prekės gavimas būtų sudengiamas su tam tikru išdavimu. 

Naudojant LIFO datos atsargų modelį, rekomenduojama reguliariai atlikti atsargų uždarymą. 

Šiuose pavyzdžiuose parodytas LIFO datos su trimis skirtingomis konfigūracijomis naudojimo poveikis:

-   LIFO duomenys be **faktinės vertės įtraukimo** pasirinkties
-   LIFO duomenys su**faktinės vertės įtraukimo** pasirinktimi
-   LIFO duomenys su žymėjimu

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO duomenys be faktinės vertės įtraukimo pasirinkties
Šiame pavyzdyje prekių modelio grupė nėra pažymėta, kad būtų įtraukta faktinė vertė. Toliau pateiktoje iliustracijoje parodytos šios operacijos.

-   1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
-   1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
-   2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
-   2b. 1 vieneto, kurio kaina 20,00 USD, finansinis gavimas į atsargas.
-   3a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
-   4a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina 15,00 USD (finansiškai atnaujintų operacijų slankusis vidurkis).
-   4a. Finansinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina 15,00 USD (finansiškai atnaujintų operacijų slankusis vidurkis).
-   5a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
-   5b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
-   6. Atsargų uždarymas atliktas. Remiantis LIFO datos metodu paskutinis finansiškai atnaujintas išdavimas bus pagal datą sudengtas su paskutiniu finansiškai atnaujintu gavimu. Išdavimo operacijoje bus atliktas 5,00 USD dydžio koregavimas. Šios operacijos bus sudengtos viena pagal kitą.

Naudojama nauja vidutinė savikaina atspindi finansiškai atnaujintų operacijų vidurkį – 15,00 USD. 

Toliau pateiktoje iliustracijoje parodytas LIFO datos atsargų modelio poveikis, kai parinktis **Įtraukti faktinę vertę** nenaudojama. ![LIFO duomenys su faktinės vertės įtraukimu](./media/lifodatewithoutincludephysicalvalue.gif) 

**Diagramos paaiškinimas**

-   Atsargų operacijos parodomos vertikaliomis rodyklėmis.
-   Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
-   Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
-   Virš (arba po) kiekviena vertikalia rodykle atsargų operacijos vertė nustatyta formatu „Quantity@Unitprice“.
-   Atsargų operacijos vertė skliaustuose rodo, kad atsargų operacija atsargose užregistruota fiziškai.
-   Atsargų operacijos vertė, kuri nėra skliaustuose, rodo, kad atsargų operacija atsargose užregistruota finansiškai.
-   Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
-   Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
-   Atsargų uždarymai rodomi raudona vertikalia punktyrine linija ir žyme *Atsargų uždarymas*.
-   Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO duomenys su faktinės vertės įtraukimo pasirinktimi
Puslapyje **Prekių modelių grupės** galite pažymėti žymės langelį **Įtraukti faktinę vertę**. Šiuo atveju sistema naudoja tiek faktines, tiek finansines gavimo operacijas, siekdama suskaičiuoti slankiojo vidurkio savikainą. Sistema taip pat kur reikia atlieka finansiškai atnaujintos išdavimo operacijos koregavimus. Išvalius žymės langelį **Įtraukti faktinę vertę**, atsargų uždarymas taikant LIFO datos atsargų modelį atliks tik finansiškai atnaujintų operacijų sudengimus. 

Šiame pavyzdyje prekių modelio grupė pažymėta, kad būtų įtraukta faktinė vertė. 

Toliau pateiktoje iliustracijoje parodytos šios operacijos.

-   1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
-   1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
-   2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
-   2b. 1 vieneto, kurio kaina 20,00 USD, finansinis gavimas į atsargas.
-   3a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
-   4a. Atsargų faktinis išdavimas, kai kiekis – 1, vieneto savikaina – 18,33 USD (finansiškai atnaujintų operacijų slankusis vidurkis).
-   4b. Finansinis atsargų išdavimas, kai kiekis yra 1, vieneto savikaina 18,33 USD (finansiškai atnaujintų operacijų slankusis vidurkis).
-   5a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
-   5b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
-   6. Atsargų uždarymas atliktas. Remiantis LIFO datos metodu paskutinis atnaujintas išdavimas bus pagal datą pakoreguotas arba sudengtas pagal paskutinį atnaujintą gavimą. Šios operacijos nebus sudengiamos viena su kita, nes finansinio gavimo operacija pakoreguojama pagal faktiškai atnaujintą operaciją. Todėl šioje išdavimo operacijoje bus vykdomas tik 6,67 USD dydžio koregavimas.

Naudojama nauja vidutinė savikaina atspindi finansiškai atnaujintų operacijų vidurkį – 20,00 USD. 

Toliau pateiktoje iliustracijoje parodytas LIFO atsargų modelio poveikis, kai parinktis **Įtraukti faktinę vertę** naudojama. ![LIFO duomenys su faktinės vertės įtraukimu](./media/lifodatewithincludephysicalvalue.gif) 

**Diagramos paaiškinimas**

-   Atsargų operacijos parodomos vertikaliomis rodyklėmis.
-   Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
-   Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
-   Virš (arba po) kiekviena vertikalia rodykle atsargų operacijos vertė nustatyta formatu „Quantity@Unitprice“.
-   Atsargų operacijos vertė skliaustuose rodo, kad atsargų operacija atsargose užregistruota fiziškai.
-   Atsargų operacijos vertė, kuri nėra skliaustuose, rodo, kad atsargų operacija atsargose užregistruota finansiškai.
-   Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
-   Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
-   Atsargų uždarymai rodomi raudona vertikalia punktyrine linija ir žyme *Atsargų uždarymas*.
-   Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="lifo-date-with-marking"></a>LIFO duomenys su žymėjimu
Žymėjimas yra procesas, leidžiantis susieti arba pažymėti išdavimo operaciją su gavimo operacija. Žymėjimą galima atlikti prieš arba po operacijos registravimo. Žymėjimą naudokite norėdami būti tikri dėl tikslios atsargų savikainos užregistravus operaciją arba uždarius atsargas. 

Pavyzdžiui, klientų aptarnavimo skyrius priėmė skubų užsakymą iš svarbaus kliento. Kadangi šis užsakymas yra skubus, norėdami patenkinti kliento pageidavimus, už šią prekę turėsite mokėti daugiau. Turite įsitikinti, kad šios pardavimo užsakymo sąskaitos faktūros atsargų prekės savikaina atsispindi maržoje arba parduotų prekių savikainoje (PPK). 

Kai pirkimo užsakymas užregistruojamas, gaunama atsargų už 120,00 USD. Jeigu šis pardavimo užsakymo dokumentas pažymėtas prie pirkimo užsakymo prieš užregistruojant važtaraštį arba sąskaitą faktūrą, PPK bus 120,00 USD – prekei nebus taikoma dabartinio slankiojo vidurkio kaina. Jeigu pardavimo užsakymo važtaraštis arba SF užregistruojami prieš žymėjimą, COGS bus užregistruota taikant slankiojo vidurkio savikainą. 

Prieš atsargų uždarymą šias dvi operacijas dar galima žymėti kartu. 

Pavyzdžiui, gavimo operacija pažymima prie išdavimo operacijos. Šiuo atveju nepaisoma prekės modelių grupėje nustatyto vertinimo būdo ir sistema sudengia šias operacijas vieną su kita. 

Galite pažymėti išdavimo operaciją su gavimu prieš užregistruodami operaciją. Tai galima atlikti iš pardavimo užsakymo eilutės puslapyje **Išsami pardavimo užsakymo informacija**. Galite peržiūrėti atidarytas gavimo operacijas puslapyje **Žymėjimas**. 

Taip pat galite pažymėti išdavimo operaciją su gavimu užregistravę operaciją. Galite pažymėti išdavimo operaciją atvirai gavimo atsargose esančiai prekei iš registruoto atsargų koregavimo žurnalo. 

Toliau pateiktoje iliustracijoje parodytos šios operacijos.

-   1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
-   1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
-   2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
-   2b. 1 vieneto, kurio kaina 20,00 USD, finansinis gavimas į atsargas.
-   3a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
-   4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
-   4b. 1 vieneto, kurio kaina 30,00 USD, finansinis gavimas į atsargas.
-   5a. Fizinis 1 vieneto, kurio savikaina 21,25 USD, atsargų išdavimas (finansiškai ir fiziškai atnaujintų operacijų slankusis vidurkis).
-   5b. Prieš užregistruojant operaciją, 1 vieneto atsargų finansinis išdavimas yra pažymimas 2b atsargų gavime. Šios užregistruotos operacijos savikaina yra 20,00 USD už vienetą.
-   6a. 1 vieneto, kurio savikaina 21,25 USD, fizinis išdavimas iš atsargų.
-   7. Atsargų uždarymas atliktas. Kadangi finansiškai atnaujinta Pirma gaunama, pirma išduodama (FIFO) operacija yra pažymima esamame gavime, šios operacijos yra sudengiamos viena su kita ir jokios korekcijos neatliekamos.

Nauja slankiojo vidurkio savikaina rodo finansiškai ir fiziškai atnaujintų operacijų vidurkį – 27,50 USD. 

Toliau pateiktoje iliustracijoje parodytas LIFO atsargų modelio poveikis, naudojant žymėjimą tarp gavimų ir išdavimų. ![LIFO duomenys su žymėjimu](./media/lifodatewithmarking.gif) 

**Diagramos paaiškinimas**

-   Atsargų operacijos parodomos vertikaliomis rodyklėmis.
-   Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
-   Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
-   Virš (arba po) kiekviena vertikalia rodykle atsargų operacijos vertė nustatyta formatu „Quantity@Unitprice“.
-   Atsargų operacijos vertė skliaustuose rodo, kad atsargų operacija atsargose užregistruota fiziškai.
-   Atsargų operacijos vertė, kuri nėra skliaustuose, rodo, kad atsargų operacija atsargose užregistruota finansiškai.
-   Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
-   Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
-   Atsargų uždarymai rodomi raudona vertikalia punktyrine linija ir žyme *Atsargų uždarymas*.
-   Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.





