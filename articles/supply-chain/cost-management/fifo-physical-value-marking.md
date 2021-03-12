---
title: FIFO su faktine verte ir žymėjimu
description: Pirma gaunama, pirma išduodama (FIFO) yra atsargų modelis, kuriame anksčiau gauti gavimai yra išduodami pirmi. Finansiškai atnaujinti atsargų išdavimai yra sudengiami prieš pirma finansiškai atnaujintus atsargų gavimus, pagrįstus atsargų operacijų finansine data.
author: AndersGirke
manager: tfehr
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.assetid: dc0e2855-83a0-41a7-a398-3c7852597d1a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b6b5e7b654b5732290489c0dbcb13d1cc441e9c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5002053"
---
# <a name="fifo-with-physical-value-and-marking"></a>FIFO su faktine verte ir žymėjimu

[!include [banner](../includes/banner.md)]

Pirma gaunama, pirma išduodama (FIFO) yra atsargų modelis, kuriame anksčiau gauti gavimai yra išduodami pirmi. Finansiškai atnaujinti atsargų išdavimai yra sudengiami prieš pirma finansiškai atnaujintus atsargų gavimus, pagrįstus atsargų operacijų finansine data. 

Naudojant FIFO nereikia naudoti FIFO taisyklės. Užuot ją naudoję, galite pažymėti atsargų operacijas tam, kad tam tikros prekės gavimas būtų sudengiamas su tam tikru išdavimu. Naudojant FIFO atsargų modelį, rekomenduojama reguliariai atlikti atsargų uždarymą. Šiuose pavyzdžiuose parodytas FIFO su trimis skirtingomis konfigūracijomis naudojimo poveikis:

-   FIFO be parinkties **Įtraukti faktinę vertę**
-   FIFO su parinktimi **Įtraukti faktinę vertę**
-   FIFO su žymėjimu

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO be įtraukiamos faktinės vertės pasirinkties
Šiame pavyzdyje prekių modelio grupė nėra pažymėta, kad būtų įtraukta faktinė vertė. Toliau pateiktoje iliustracijoje parodytos šios operacijos.

-   1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
-   1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
-   2a. Faktinis atsargų gavimas, kai kiekis yra 2 o išlaidos – 10,00 USD už vienetą.
-   2b. 2 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
-   3a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
-   4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
-   4b. 1 vieneto, kurio kaina 30,00 USD, finansinis gavimas į atsargas.
-   5a. Atsargų faktinis išdavimas, kai kiekis – 1, vieneto savikaina – 20,00 USD (finansiškai atnaujintų operacijų slankusis vidurkis).
-   5b. Atsargų finansinis išdavimas, kai kiekis – 1, kiekvieno savikaina – 15,00 USD (finansiškai atnaujintų operacijų slankusis vidurkis).
-   6. Atsargų uždarymas atliktas. Pagal FIFO metodą, pirmas finansiškai atnaujintas išdavimas sudengiamas pagal pirmą finansiškai atnaujintą gavimą. Išdavimo operacija bus pakoreguota –5,00 USD.

Nauja veikiančio vidurkio savikaina atitinka finansiškai atnaujintų operacijų vidurkį. Toliau pateiktose iliustracijose parodytas FIFO atsargų modelio poveikis kai kurioms operacijoms, kai parinktis **Įtraukti faktinę vertę** nenaudojama. 

![LIFO be faktinės vertės įtraukimo](./media/fifowithoutincludephysicalvalue.gif) 

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
- Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
- Virš (arba po) kiekviena vertikalia rodykle atsargų operacijos vertė nustatyta formatu „Kiekis@Prekėskaina“.
- Atsargų operacijos vertė skliaustuose rodo, kad atsargų operacija atsargose užregistruota fiziškai.
- Atsargų operacijos vertė, kuri nėra skliaustuose, rodo, kad atsargų operacija atsargose užregistruota finansiškai.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Atsargų uždarymai rodomi raudona vertikalia punktyrine linija ir žyme *Atsargų uždarymas*.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO su įtraukiamos faktinės vertės pasirinktimi
Jei pažymėtas prekės, esančios puslapyje **Prekių modelių grupė**, žymės langelis **Įtraukti faktinę vertę**, sistema naudoja tiek faktines, tiek finansines gavimo operacijas einamajai vidutinei savikainai apskaičiuoti. Sistema taip pat kur reikia atlieka finansiškai atnaujintos išdavimo operacijos koregavimus. Išvalius žymės langelį **Įtraukti faktinę vertę**, atsargų uždarymas taikant FIFO atsargų modelį atliks tik finansiškai atnaujintų operacijų sudengimus. Toliau pateiktoje iliustracijoje parodytos šios operacijos.

-   1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
-   1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
-   2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
-   2b. 1 vieneto, kurio kaina 20,00 USD, finansinis gavimas į atsargas.
-   3a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
-   4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
-   4b. 1 vieneto, kurio kaina 30,00 USD, finansinis gavimas į atsargas.
-   5a. Fizinis 1 vieneto, kurio savikaina 21,25 USD, atsargų išdavimas (finansiškai ir fiziškai atnaujintų operacijų slankusis vidurkis).
-   5b. Finansinis atsargų išdavimas: 1 vienetas, kurio savikaina 21,25 USD (finansiškai ir faktiškai atnaujintų operacijų slankusis vidurkis).
-   6a. 1 vieneto, kurio savikaina 21,25 USD, fizinis išdavimas iš atsargų.
-   7. Atsargų uždarymas atliktas. Pagal FIFO metodą, pirma finansinė išdavimo operacija bus koreguojama arba sudengiama pagal pirmą atnaujintą gavimą, kuris gali būti finansinis arba faktinis.

5b operacija bus sudengiama pagal 1b gavimo operaciją. Ši išdavimo operacija bus pakoreguota –11,25 USD . Nauja slankiojo vidurkio savikaina rodo finansiškai ir fiziškai atnaujintų operacijų vidurkį, 27,50 USD. Toliau pateiktoje iliustracijoje parodytas FIFO atsargų modelio poveikis kai kurioms operacijoms, kai parinktis **Įtraukti faktinę vertę** naudojama. 

![FIFO su faktinės vertės įtraukimu](./media/fifowithincludephysicalvalue.gif) 

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
- Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
- Virš (arba po) kiekviena vertikalia rodykle atsargų operacijos vertė nustatyta formatu „Kiekis@Prekėskaina“.
- Atsargų operacijos vertė skliaustuose rodo, kad atsargų operacija atsargose užregistruota fiziškai.
- Atsargų operacijos vertė, kuri nėra skliaustuose, rodo, kad atsargų operacija atsargose užregistruota finansiškai.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Atsargų uždarymai rodomi raudona vertikalia punktyrine linija ir žyme *Atsargų uždarymas*.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="fifo-with-marking"></a>FIFO su žymėjimu
Žymėjimas yra procesas, leidžiantis susieti arba pažymėti išdavimo operaciją su gavimo operacija. Žymėjimą galima atlikti prieš arba po operacijos registravimo. Žymėjimą naudokite norėdami būti tikri dėl tikslios atsargų savikainos užregistravus operaciją arba uždarius atsargas. Pavyzdžiui, klientų aptarnavimo skyrius priėmė skubų užsakymą iš svarbaus kliento. Kadangi tai skubus užsakymas, norėdami patenkinti kliento pageidavimus, už šią prekę turite mokėti daugiau. Turite įsitikinti, kad šios pardavimo užsakymo sąskaitos faktūros atsargų prekės savikaina atsispindi maržoje arba parduotų prekių savikainoje (PPK). Kai pirkimo užsakymas užregistruojamas, gaunama atsargų už 120,00 USD. Jeigu šis pardavimo užsakymo dokumentas pažymėtas prie pirkimo užsakymo prieš užregistruojant važtaraštį arba sąskaitą faktūrą, PPK bus 120,00 USD – prekei nebus taikoma dabartinio slankiojo vidurkio kaina. Jeigu pardavimo užsakymo važtaraštis arba SF užregistruojami prieš žymėjimą, COGS bus užregistruota taikant slankiojo vidurkio savikainą. Prieš atsargų uždarymą šias dvi operacijas dar galima žymėti kartu. Kai gavimo operacija sutampa su išdavimo operacija, nepaisoma prekės modelių grupėje nustatyto vertinimo būdo ir sistema sudengia šias operacijas. Galite pažymėti išdavimo operaciją su gavimu prieš užregistruodami operaciją. Tai galima atlikti iš pardavimo užsakymo eilutės puslapyje **Išsami pardavimo užsakymo informacija**. Galite peržiūrėti atidarytas gavimo operacijas puslapyje **Žymėjimas**. Taip pat galite pažymėti išdavimo operaciją su gavimu užregistravę operaciją. Galite pažymėti išdavimo operaciją atvirai gavimo atsargose esančiai prekei iš registruoto atsargų koregavimo žurnalo. Toliau pateiktoje iliustracijoje parodytos šios operacijos.

-   1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
-   1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
-   2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
-   2b. 1 vieneto, kurio kaina 20,00 USD, finansinis gavimas į atsargas.
-   3a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
-   4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
-   4b. 1 vieneto, kurio kaina 30,00 USD, finansinis gavimas į atsargas.
-   5a. Fizinis 1 vieneto, kurio savikaina 21,25 USD, atsargų išdavimas (finansiškai ir fiziškai atnaujintų operacijų slankusis vidurkis).
-   5b. Prieš užregistruojant operaciją, 1 vieneto atsargų finansinis išdavimas yra pažymimas 2b atsargų gavime. Ši operacija registruojama 20,00 USD savikaina kiekvienam.
-   6a. 1 vieneto, kurio savikaina 21,25 USD, fizinis išdavimas iš atsargų.
-   7. Atsargų uždarymas atliktas. Kadangi finansiškai atnaujinta FIFO operacija yra pažymėta su esamu gavimu, šios operacijos sudengiamos viena pagal kitą, ir joks koregavimas neatliekamas.

Nauja slankiojo vidurkio savikaina rodo finansiškai ir fiziškai atnaujintų operacijų vidurkį, 27,50 USD. Toliau pateiktoje iliustracijoje parodomas FIFO atsargų modelio poveikis tokioms operacijų sekoms, kai naudojamas išdavimų ir gavimų žymėjimas. 

![FIFO su žymėjimu](./media/fifowithmarking.gif) 

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
- Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
- Virš (arba po) kiekviena vertikalia rodykle atsargų operacijos vertė nustatyta formatu „Kiekis@Prekėskaina“.
- Atsargų operacijos vertė skliaustuose rodo, kad atsargų operacija atsargose užregistruota fiziškai.
- Atsargų operacijos vertė, kuri nėra skliaustuose, rodo, kad atsargų operacija atsargose užregistruota finansiškai.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Atsargų uždarymai rodomi raudona vertikalia punktyrine linija ir žyme *Atsargų uždarymas*.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.




