---
title: LIFO su faktine verte ir žymėjimu
description: Paskutinis įvestas, pirmasis nurašytas (LIFO) yra atsargų modelis, kuriame vėliausi (naujausi) gavimai yra išduodami pirmiausiai. Išdavimai iš atsargų sudengiami su paskutiniaisiais gavimais į atsargas remiantis atsargų operacijos data.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 55021
ms.assetid: 49c492b0-b018-44e0-928f-9671e54eee20
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c6f59f5bb0d19c32e07b15141c12066948b7a6f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433647"
---
# <a name="lifo-with-physical-value-and-marking"></a>LIFO su faktine verte ir žymėjimu

[!include [banner](../includes/banner.md)]

Paskutinis įvestas, pirmasis nurašytas (LIFO) yra atsargų modelis, kuriame vėliausi (naujausi) gavimai yra išduodami pirmiausiai. Išdavimai iš atsargų sudengiami su paskutiniaisiais gavimais į atsargas remiantis atsargų operacijos data. 

Naudojant atsargų modelį Paskutinis į, pirmas iš (LIFO) paskutiniai (naujausi) gavimai išduodami pirmiausia. Išdavimai iš atsargų sudengiami su paskutiniaisiais gavimais į atsargas remiantis atsargų operacijos data. Naudojant LIFO nereikia naudoti LIFO taisyklės. Užuot ją naudoję, galite pažymėti atsargų operacijas tam, kad tam tikros prekės išdavimas būtų sudengiamas su tam tikru gavimu. Naudojant LIFO atsargų modelį, rekomenduojama reguliariai atlikti atsargų uždarymą. 

Šiuose pavyzdžiuose parodytas LIFO su trimis skirtingomis konfigūracijomis naudojimo poveikis:

-   LIFO be parinkties **Įtraukti faktinę vertę**
-   LIFO su parinktimi **Įtraukti faktinę vertę**
-   LIFO su žymėjimu

## <a name="lifo-without-the-include-physical-value-option"></a>LIFO be faktinės vertės įtraukimo pasirinkties
Šiame pavyzdyje prekių modelio grupė nėra pažymėta, kad būtų įtraukta faktinė vertė. Toliau pateiktoje iliustracijoje parodytos šios operacijos.

-   1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
-   1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
-   2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
-   2b. 1 vieneto, kurio kaina 20,00 USD, finansinis gavimas į atsargas.
-   3a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
-   4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
-   4b. 1 vieneto, kurio kaina 30,00 USD, finansinis gavimas į atsargas.
-   5a. Atsargų faktinis išdavimas, kai kiekis – 1, vieneto savikaina – 20,00 USD (finansiškai atnaujintų operacijų slankusis vidurkis).
-   5b. Atsargų finansinis išdavimas, kai kiekis – 1, kiekvieno savikaina – 20,00 USD (finansiškai atnaujintų operacijų slankusis vidurkis).
-   6. Atsargų uždarymas atliktas. Remiantis LIFO metodu paskutinis finansiškai atnaujintas išdavimas bus sudengtas su paskutiniu finansiškai atnaujintu gavimu. Išdavimo operacijoje bus atliktas 10,00 USD dydžio koregavimas.

Naudojama nauja vidutinė savikaina atspindi finansiškai atnaujintų operacijų vidurkį – 15,00 USD. Toliau pateiktoje iliustracijoje parodytas LIFO atsargų modelio poveikis kai kurioms operacijoms, kai parinktis **Įtraukti faktinę vertę** nenaudojama. 

![LIFO be faktinės vertės įtraukimo](./media/lifowithoutincludephysicalvalue.gif) 

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
- Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
- Virš (arba po) kiekviena vertikalia rodykle atsargų operacijos vertė nustatyta formatu Kiekis@Prekės kaina.
- Atsargų operacijos vertė skliaustuose rodo, kad atsargų operacija atsargose užregistruota fiziškai.
- Atsargų operacijos vertė, kuri nėra skliaustuose, rodo, kad atsargų operacija atsargose užregistruota finansiškai.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Atsargų uždarymai rodomi raudona vertikalia punktyrine linija ir žyme *Atsargų uždarymas*.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="lifo-with-the-include-physical-value-option"></a>LIFO su faktinės vertės įtraukimo pasirinktimi
Jei pažymėtas prekės, esančios puslapyje **Prekių modelių grupės**, žymės langelis **Įtraukti faktinę vertę**, sistema naudoja tiek faktines, tiek finansines gavimo operacijas einamajai vidutinei savikainai apskaičiuoti. Sistema taip pat kur reikia atlieka finansiškai atnaujintos išdavimo operacijos koregavimus. Išvalius žymės langelį **Įtraukti faktinę vertę**, atsargų uždarymas taikant LIFO atsargų modelį atliks tik finansiškai atnaujintų operacijų sudengimus. 

Toliau pateiktoje iliustracijoje parodytos šios operacijos.

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
-   7. Atsargų uždarymas atliktas. Remiantis LIFO metodu paskutinė išdavimo operacija bus pakoreguota arba sudengta su paskutiniu atnaujintu gavimu.

Operacija 6a bus pakoreguota pagal gavimo operaciją 4b. Sistema nesudengs šių operacijų, nes gavimas bus atnaujintas tik faktiškai, o ne finansiškai. Todėl faktinio išdavimo operacijoje bus užregistruotas tik 8,75 USD sumos koregavimas. Operacija 5b bus pakoreguota pagal faktinio gavimo operaciją 3a. Sistema nesudengs šių operacijų, nes jos abi nebus finansiškai atnaujintos. Todėl šioje išdavimo operacijoje bus vykdomas tik –3,75 USD sumos koregavimas. Nauja slankiojo vidurkio savikaina rodo finansiškai ir fiziškai atnaujintų operacijų vidurkį, 20,00 USD. 

Toliau pateiktoje iliustracijoje parodytas LIFO atsargų modelio poveikis kai kurioms operacijoms, kai parinktis **Įtraukti faktinę vertę** naudojama. 

![LIFO su faktinės vertės įtraukimu](./media/lifowithincludephysicalvalue.gif) 

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
- Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
- Virš (arba po) kiekviena vertikalia rodykle atsargų operacijos vertė nustatyta formatu Kiekis@Prekės kaina.
- Atsargų operacijos vertė skliaustuose rodo, kad atsargų operacija atsargose užregistruota fiziškai.
- Atsargų operacijos vertė, kuri nėra skliaustuose, rodo, kad atsargų operacija atsargose užregistruota finansiškai.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Atsargų uždarymai rodomi raudona vertikalia punktyrine linija ir žyme *Atsargų uždarymas*.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="lifo-with-marking"></a>LIFO su žymėjimu
Žymėjimas yra procesas, leidžiantis susieti arba pažymėti išdavimo operaciją su gavimo operacija. Žymėjimą galima atlikti prieš arba po operacijos registravimo. Žymėjimą naudokite norėdami būti tikri dėl tikslios atsargų savikainos užregistravus operaciją arba uždarius atsargas. Pavyzdžiui, klientų aptarnavimo skyrius priėmė skubų užsakymą iš svarbaus kliento. Kadangi tai skubus užsakymas, norėdami patenkinti kliento pageidavimus, už šią prekę turite mokėti daugiau. 

Turite įsitikinti, kad šios pardavimo užsakymo sąskaitos faktūros atsargų prekės savikaina atsispindi maržoje arba parduotų prekių savikainoje (PPK). Kai pirkimo užsakymas užregistruojamas, gaunama atsargų už 120,00 USD. Jeigu šis pardavimo užsakymo dokumentas pažymėtas prie pirkimo užsakymo prieš užregistruojant važtaraštį arba sąskaitą faktūrą, PPK bus 120,00 USD – prekei nebus taikoma dabartinio slankiojo vidurkio kaina. Jeigu pardavimo užsakymo važtaraštis arba SF užregistruojami prieš žymėjimą, COGS bus užregistruota taikant slankiojo vidurkio savikainą. 

Prieš atsargų uždarymą šias dvi operacijas dar galima žymėti kartu. 

Galite pažymėti išdavimo operaciją prie gavimo prieš registruodami operaciją. Tai galima atlikti iš pardavimo užsakymo eilutės puslapyje **Išsami pardavimo užsakymo informacija**. Galite peržiūrėti atidarytas gavimo operacijas puslapyje **Žymėjimas**. 

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
-   7. Atsargų uždarymas atliktas. Kadangi finansiškai atnaujinta FIFO operacija yra pažymėta su esamu gavimu, šios operacijos sudengiamos viena pagal kitą, ir joks koregavimas neatliekamas.

Nauja slankiojo vidurkio savikaina rodo finansiškai ir fiziškai atnaujintų operacijų vidurkį, 27,50 USD. 

Toliau pateiktoje iliustracijoje parodomas LIFO atsargų modelio poveikis tokioms operacijų sekoms, kai naudojamas išdavimų ir gavimų žymėjimas. 

![LIFO su žymėjimu](./media/lifowithmarking.gif) 

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
- Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
- Virš (arba po) kiekviena vertikalia rodykle atsargų operacijos vertė nustatyta formatu Kiekis@Prekės kaina.
- Atsargų operacijos vertė skliaustuose rodo, kad atsargų operacija atsargose užregistruota fiziškai.
- Atsargų operacijos vertė, kuri nėra skliaustuose, rodo, kad atsargų operacija atsargose užregistruota finansiškai.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Atsargų uždarymai rodomi raudona vertikalia punktyrine linija ir žyme *Atsargų uždarymas*.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]