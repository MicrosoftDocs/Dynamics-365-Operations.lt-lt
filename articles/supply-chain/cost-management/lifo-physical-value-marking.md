---
title: LIFO su faktine verte ir žymėjimu
description: Paskutinis įvestas, pirmasis nurašytas (LIFO) yra atsargų modelis, kuriame vėliausi (naujausi) gavimai yra išduodami pirmiausiai. Išdavimai iš atsargų sudengiami su paskutiniaisiais gavimais į atsargas remiantis atsargų operacijos data.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55021
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd57d58aa91aa87b1c2feff52a568296fc18ed9b
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092169"
---
# <a name="lifo-with-physical-value-and-marking"></a>LIFO su faktine verte ir žymėjimu

[!include [banner](../includes/banner.md)]

Paskutinis, pirmas išeina (LIFO) yra atsargų valdymo ir vertinimo metodas, kai paskutinės pagamintos arba įsigytos atsargos parduodamos, naudojamos arba pašalinamos pirmiausia. „Microsoft“ atsargų uždarymo proceso metu Dynamics 365 Supply Chain Management, sistema sukurs atsiskaitymus, kai paskutinis kvitas bus suderintas su pirmuoju išdavimu ir pan. Atsiskaitymai ir derinimo principas grindžiami atsargų operacijų finansine data. Preliminarus atsiskaitymų ir patikslinimų įvertinimas gali būti atliktas vykdant atsargų perskaičiavimo procesą.

Galite nepaisyti LIFO principo pažymėdami atsargų operacijas, kad konkrečios prekės kvitas būtų padengtas konkrečia problema. Periodiškas atsargų uždarymas reikalingas, kai naudojate LIFO atsargų modelį, kad sukurtumėte atsiskaitymus ir koreguotų emisijų vertę pagal LIFO principą. Kol vykdote atsargų uždarymo procesą, išdavimo operacijos vertinamos pagal einamąjį vidurkį, kai įvyko fiziniai ir finansiniai atnaujinimai. Jei nenaudojate žymėjimo, einamasis vidurkis apskaičiuojamas, kai atliekamas fizinis arba finansinis atnaujinimas.

Šiuose pavyzdžiuose parodytas LIFO su trimis skirtingomis konfigūracijomis naudojimo poveikis:

- LIFO be parinkties **Įtraukti faktinę vertę**
- LIFO su parinktimi **Įtraukti faktinę vertę**
- LIFO su žymėjimu

## <a name="lifo-without-the-include-physical-value-option"></a>LIFO be faktinės vertės įtraukimo pasirinkties

Šiame pavyzdyje **Įtraukite fizinę vertę** Išleisto produkto prekių modelių grupės žymimasis laukelis išvalytas. Toliau pateiktoje iliustracijoje parodytos šios operacijos.

- 1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
- 1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
- 2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
- 2b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 22,00 USD už vienetą.
- 3a. Atsargų fizinė problema 1 kiekiui už USD 16.00 savikainą (einamoji finansiškai paskelbtų operacijų vidurkis).
- 3b. Atsargų finansinė problema 1 kiekiui už USD 16.00 savikainą (einamoji finansiškai paskelbtų operacijų vidurkis).
- 4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
- 5a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 5b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 6a. Atsargų fizinė problema 1 kiekiui už USD 23.00 savikainą (skaičiuojamas finansiškai paskelbtų operacijų vidurkis)
- 7\. Atsargų uždarymas atliktas. Remiantis LIFO metodu, pirmoji finansiškai atnaujinta problema bus apmokėta pagal paskutinį finansiškai atnaujintą kvitą ir pan. Šiame pavyzdyje tarp 5b ir 3b sukuriama viena gyvenvietė. USD 14.00 koregavimas bus atliktas į 3b, o galutinė kaina bus USD 30.00.

Toliau pateiktoje iliustracijoje parodytas FIFO atsargų modelio poveikis kai kurioms operacijoms, kai parinktis **Įtraukti faktinę vertę** nenaudojama.

![LIFO be parinkties Įtraukti fizinę vertę.](./media/lifo-without-including-physical-value.png)

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Fizinės operacijos pavaizduotos trumpesnėmis šviesiai pilkomis rodyklėmis.
- Finansines operacijas žymi ilgesnės juodos rodyklės.
- Kvitai į atsargas yra pavaizduoti vertikaliomis rodyklėmis virš ašies.
- Problemos, kurios nėra atsargų, pavaizduotos vertikaliomis rodyklėmis žemiau ašies.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Kiekviena data diagramoje atskirta plona juoda vertikalia linija. Data nurodyta diagramos apačioje.
- Atsargų uždarymas pavaizduotas raudona vertikalia punktyrine linija.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="lifo-with-the-include-physical-value-option"></a>LIFO su faktinės vertės įtraukimo pasirinktimi

Jei **Įtraukite fizinę vertę** pažymėtas elemento žymimasis laukelis **Prekių modelių grupės** puslapyje, sistema naudoja tiek fizines, tiek finansines gavimo operacijas, kad apskaičiuotų einamąją vidutinę savikainą. Kai taikoma, sistema taip pat koreguoja fiziškai atnaujintą išdavimo operaciją. Kai **Įtraukite fizinę vertę** žymimasis laukelis išvalytas, atsargų uždarymas, kuris naudoja LIFO atsargų modelį, atsiskaito tik už finansiškai atnaujintas operacijas.

Toliau pateiktoje iliustracijoje parodytos šios operacijos.

- 1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
- 1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
- 2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
- 2b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 22,00 USD už vienetą.
- 3a. Atsargų fizinė problema 1 kiekiui už USD 16.00 savikainą (einamoji fiziškai ir finansiškai paskelbtų operacijų vidurkis).
- 3b. Atsargų finansinė problema 1 kiekiui už USD 16.00 savikainą (fiziškai ir finansiškai paskelbtų operacijų einamojo vidurkio).
- 4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
- 5a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 5b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 6a. Atsargų fizinė problema 1 kiekiui už USD 23.67 savikainą (skaičiuojamas fiziškai ir finansiškai paskelbtų operacijų vidurkis).
- 7\. Atsargų uždarymas atliktas. Remiantis LIFO metodu, pirmoji finansiškai atnaujinta problema bus apmokėta pagal paskutinį finansiškai atnaujintą kvitą ir pan. Šiame pavyzdyje viena gyvenvietė sukuriama tarp 3b ir 5b. USD 14.00 koregavimas bus atliktas į 3b, o galutinė kaina bus USD 30.00. Be to, 6a operacija bus pakoreguota pagal gavimo operacijos kainą 4a. Sistema nesudengs šių operacijų, nes gavimas bus atnaujintas tik faktiškai, o ne finansiškai. Vietoj to, fizinės emisijos operacijai bus paskelbtas tik USD 1.33 koregavimas, o gauta pakoreguota kaina bus USD 25.00.

Toliau pateiktoje iliustracijoje parodytas LIFO atsargų modelio poveikis kai kurioms operacijoms, kai parinktis **Įtraukti faktinę vertę** naudojama.

![LIFO su parinktimi Įtraukti fizinę vertę.](./media/lifo-with-included-physical-value.png)

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Fizinės operacijos pavaizduotos trumpesnėmis šviesiai pilkomis rodyklėmis.
- Finansines operacijas žymi ilgesnės juodos rodyklės.
- Kvitai į atsargas yra pavaizduoti vertikaliomis rodyklėmis virš ašies.
- Problemos, kurios nėra atsargų, pavaizduotos vertikaliomis rodyklėmis žemiau ašies.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Kiekviena data diagramoje atskirta plona juoda vertikalia linija. Data pažymėta diagramos apačioje.
- Atsargų uždarymas pavaizduotas raudona vertikalia punktyrine linija.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="lifo-with-marking"></a>LIFO su žymėjimu

Žymėjimas yra procesas, leidžiantis susieti arba pažymėti išdavimo operaciją su gavimo operacija. Žymėjimą galima atlikti prieš arba po operacijos registravimo. Žymėjimą naudokite norėdami būti tikri dėl tikslios atsargų savikainos užregistravus operaciją arba uždarius atsargas. Pavyzdžiui, klientų aptarnavimo skyrius priėmė skubų užsakymą iš svarbaus kliento. Kadangi šis užsakymas yra skubus, turite sumokėti daugiau už prekę, kad įvykdytumėte kliento prašymą.

Turite įsitikinti, kad atsargų prekės savikaina atsispindi pardavimo užsakymo sąskaitos faktūros maržoje arba parduotų prekių savikainoje (COGS). Kai pirkimo užsakymas užregistruojamas, gaunama atsargų už 120,00 USD. Jeigu šis pardavimo užsakymo dokumentas pažymėtas prie pirkimo užsakymo prieš užregistruojant važtaraštį arba sąskaitą faktūrą, PPK bus 120,00 USD – prekei nebus taikoma dabartinio slankiojo vidurkio kaina. Jeigu pardavimo užsakymo važtaraštis arba SF užregistruojami prieš žymėjimą, COGS bus užregistruota taikant slankiojo vidurkio savikainą.

Prieš atsargų uždarymą šias dvi operacijas dar galima žymėti kartu.

Galite pažymėti išdavimo operaciją su gavimu prieš užregistruodami operaciją. Šį žymėjimą galite atlikti pardavimo užsakymo eilutėje **Pardavimo užsakymo informacija** puslapį pasirinkdami **Inventorius \> Žymėjimas** ant **Pardavimo užsakymų eilutės** FastTab. Galite peržiūrėti atidarytas gavimo operacijas **Žymėjimo** puslapyje.

Taip pat galite pažymėti išdavimo operaciją su gavimu užregistravę operaciją. Galite pažymėti išdavimo operaciją atvirai gavimo atsargose esančiai prekei iš registruoto atsargų koregavimo žurnalo.

Toliau pateiktoje iliustracijoje parodytos šios operacijos.

- 1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
- 1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
- 2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
- 2b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 22,00 USD už vienetą.
- 3a. Atsargų fizinė problema 1 kiekiui už USD 16.00 savikainą (einamoji finansiškai paskelbtų operacijų vidurkis).
- 3b. Atsargų finansinė problema 1 kiekiui už USD 16.00 savikainą (einamoji finansiškai paskelbtų operacijų vidurkis).
- 3c. 3b atsargų finansinė emisija pažymėta kaip 2b atsargų finansinė emisija.
- 4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
- 5a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 5b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 6a. Atsargų fizinė problema 1 kiekiui už USD 23.00 savikainą (skaičiuojamas finansiškai paskelbtų operacijų vidurkis)
- 7\. Atsargų uždarymas atliktas. Remiantis žymėjimo principu, kuris naudoja LIFO metodą, pažymėtos operacijos atsiskaitomos viena su kita. Šiame pavyzdyje 3b atsiskaitoma su 2b, o USD 6.00 koregavimas paskelbiamas 3b, kad vertė būtų USD 22.00. Šiame pavyzdyje papildomi atsiskaitymai neatliekami, nes uždarymas sukuria atsiskaitymus tik už finansiškai atnaujintas operacijas.

Nauja slankiojo vidurkio savikaina rodo finansiškai ir fiziškai atnaujintų operacijų vidurkį, 27,50 USD.

Toliau pateiktoje iliustracijoje parodomas LIFO atsargų modelio poveikis tokioms operacijų sekoms, kai naudojamas išdavimų ir gavimų žymėjimas.

![LIFO su žymėjimu.](./media/lifo-with-marking.png)

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Fizinės operacijos pavaizduotos trumpesnėmis šviesiai pilkomis rodyklėmis.
- Finansines operacijas žymi ilgesnės juodos rodyklės.
- Kvitai į atsargas yra pavaizduoti vertikaliomis rodyklėmis virš ašies.
- Problemos, kurios nėra atsargų, pavaizduotos vertikaliomis rodyklėmis žemiau ašies.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Kiekviena data diagramoje atskirta plona juoda vertikalia linija. Data nurodyta diagramos apačioje.
- Atsargų uždarymas pavaizduotas raudona vertikalia punktyrine linija.
- Atsiskaitymai ir žymėjimai, atlikti uždarant atsargas, vaizduojami raudonomis įstrižomis brūkšninėmis rodyklėmis, kurios pereina nuo kvito iki išdavimo.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
