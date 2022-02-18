---
title: FIFO su faktine verte ir žymėjimu
description: Pirma gaunama, pirma išduodama (FIFO) yra atsargų modelis, kuriame anksčiau gauti gavimai yra išduodami pirmi. Finansiškai atnaujinti atsargų išdavimai yra sudengiami prieš pirma finansiškai atnaujintus atsargų gavimus, pagrįstus atsargų operacijų finansine data.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5280498a23df26873dda1f380f686796f5e1055f
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092145"
---
# <a name="fifo-with-physical-value-and-marking"></a>FIFO su faktine verte ir žymėjimu

[!include [banner](../includes/banner.md)]


„First in, first out“ (FIFO) yra atsargų valdymo ir vertinimo metodas, kai pirmiausia pagaminamos arba įsigytos atsargos parduodamos, naudojamos arba pašalinamos pirmiausia. „Microsoft“ atsargų uždarymo proceso metu Dynamics 365 Supply Chain Management, sistema sukurs atsiskaitymus, kai pirmasis kvitas bus suderintas su pirmuoju išdavimu ir pan.

Atsiskaitymai ir derinimo principas grindžiami atsargų operacijų finansine data. Preliminarus atsiskaitymų ir patikslinimų įvertinimas gali būti atliktas vykdant atsargų perskaičiavimo procesą.

Galite nepaisyti FIFO principo pažymėdami atsargų operacijas, kad konkrečios prekės kvitas būtų padengtas konkrečia problema. Periodiškas atsargų uždarymas reikalingas, kai naudojate FIFO atsargų modelį, kad sukurtumėte atsiskaitymus ir koreguotų emisijų vertę pagal FIFO principą. Kol vykdote atsargų uždarymo procesą, išdavimo operacijos vertinamos pagal einamąjį vidurkį, kai įvyko fiziniai ir finansiniai atnaujinimai. Jei nenaudojate žymėjimo, einamasis vidurkis apskaičiuojamas, kai atliekamas fizinis arba finansinis atnaujinimas. Šiuose pavyzdžiuose parodytas FIFO su trimis skirtingomis konfigūracijomis naudojimo poveikis:

- FIFO be parinkties **Įtraukti faktinę vertę**
- FIFO su parinktimi **Įtraukti faktinę vertę**
- FIFO su žymėjimu

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO be įtraukiamos faktinės vertės pasirinkties

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
- 7\. Atsargų uždarymas atliktas. Remiantis FIFO metodu, pirmoji finansiškai atnaujinta emisija bus apmokėta pagal pirmąjį finansiškai atnaujintą kvitą ir pan. Šiame pavyzdyje viena gyvenvietė sukuriama tarp 1b ir 3b. –6,00 USD bus pakoreguotas 3b, o galutinė kaina bus USD 10.00.

Nauja veikiančio vidurkio savikaina atitinka finansiškai atnaujintų operacijų vidurkį. Toliau pateiktose iliustracijose parodytas FIFO atsargų modelio poveikis kai kurioms operacijoms, kai parinktis **Įtraukti faktinę vertę** nenaudojama.

![FIFO be parinkties Įtraukti fizinę vertę.](./media/fifo-without-include-physical-value.png)

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Fizinės operacijos pavaizduotos trumpesnėmis šviesiai pilkomis rodyklėmis.
- Finansines operacijas žymi ilgesnės juodos rodyklės.
- Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
- Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Kiekviena data diagramoje atskirta plona juoda vertikalia linija. Data nurodyta diagramos apačioje.
- Atsargų uždarymas pavaizduotas raudona vertikalia punktyrine linija.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO su įtraukiamos faktinės vertės pasirinktimi

Jei **Įtraukite fizinę vertę** pažymėtas elemento žymimasis laukelis **Prekių modelių grupė** puslapyje, sistema naudoja tiek fizines, tiek finansines gavimo operacijas, kad apskaičiuotų einamąją vidutinę savikainą. Kai taikoma, sistema taip pat koreguoja fiziškai atnaujintą išdavimo operaciją. Atsargų uždarymas, naudojant FIFO atsargų modelį, atsiskaito tik su finansiškai atnaujintomis operacijomis. Toliau pateiktoje iliustracijoje parodytos šios operacijos.

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
- 7\. Atsargų uždarymas atliktas. Remiantis FIFO metodu, pirmoji finansiškai atnaujinta emisija bus apmokėta pagal pirmąjį finansiškai atnaujintą kvitą ir pan. Šiame pavyzdyje viena gyvenvietė sukuriama tarp 1b ir 3b. –6,00 USD bus pakoreguotas 3b, o galutinė kaina bus USD 10.00. Be to, 6a operacija bus pakoreguota pagal 2b gavimo operacijos kainą. Sistema nesudengs šių operacijų, nes gavimas bus atnaujintas tik faktiškai, o ne finansiškai. Vietoj to, fizinės emisijos operacijai bus paskelbtas tik -1,67 USD koregavimas, o gautas pakoreguotas mokestis bus USD 22.00.

![FIFO su parinktimi Įtraukti fizinę vertę.](./media/fifo-with-include-physical-value.png)

Atkreipkite dėmesį, kad atsargų uždarymo proceso rezultatas yra toks pat, nepaisant to, ar pasirinkote **Įtraukite fizinę vertę** parinktis ant **Prekių modelių grupė** puslapį. The **Įtraukite fizinę vertę** parinktis turi įtakos tik einamajam vidurkiui.

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Fizinės operacijos pavaizduotos trumpesnėmis šviesiai pilkomis rodyklėmis.
- Finansines operacijas žymi ilgesnės juodos rodyklės.
- Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
- Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Kiekviena data diagramoje atskirta plona juoda vertikalia linija. Data nurodyta diagramos apačioje.
- Atsargų uždarymas pavaizduotas raudona vertikalia punktyrine linija.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="fifo-with-marking"></a>FIFO su žymėjimu

Žymėjimas yra procesas, leidžiantis susieti arba pažymėti išdavimo operaciją su gavimo operacija. Žymėjimą galima atlikti prieš arba po operacijos registravimo. Žymėjimą naudokite norėdami būti tikri dėl tikslios atsargų savikainos užregistravus operaciją arba uždarius atsargas.

Pavyzdžiui, klientų aptarnavimo skyrius priėmė skubų užsakymą iš svarbaus kliento. Kadangi šis užsakymas yra skubus, turite sumokėti daugiau už šią prekę, kad įvykdytumėte kliento prašymą. Turite įsitikinti, kad atsargų prekės savikaina atsispindi pardavimo užsakymo sąskaitos faktūros maržoje arba parduotų prekių savikainoje (COGS). Kai pirkimo užsakymas užregistruojamas, gaunama atsargų už 120,00 USD. Jei pardavimo užsakymo dokumentas yra pažymėtas pirkimo užsakyme prieš užregistruojant važtaraštį arba sąskaitą faktūrą, COGS bus USD 120.00, o ne dabartinė einamoji vidutinė prekės kaina. Jeigu pardavimo užsakymo važtaraštis arba SF užregistruojami prieš žymėjimą, COGS bus užregistruota taikant slankiojo vidurkio savikainą. Prieš atsargų uždarymą šias dvi operacijas dar galima žymėti kartu.

Kai gavimo operacija pažymima išdavimo operacija, prekių modelių grupėje apibrėžto vertinimo metodo nepaisoma, o sistema šias operacijas atsiskaito viena su kita. Galite rankiniu būdu pažymėti operaciją pardavimo užsakymo eilutėje **Pardavimo užsakymo informacija** puslapį pasirinkdami **Inventorius \> Žymėjimas** ant **Pardavimo užsakymų eilutės** FastTab. Galite peržiūrėti atidarytas gavimo operacijas **Žymėjimo** puslapyje. Galite suderinti arba pažymėti išdavimo operaciją su atvira atsargų prekės gavimo operacija iš paskelbto atsargų koregavimo žurnalo. Toliau pateiktoje iliustracijoje parodytos šios operacijos.

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
- 7\. Atsargų uždarymas atliktas. Remiantis žymėjimo principu, kuris naudoja FIFO metodą, pažymėtos operacijos yra atsiskaitomos viena su kita. Šiame pavyzdyje 3b atsiskaitoma su 2b, o USD 6.00 koregavimas paskelbiamas 3b, kad vertė būtų USD 22.00. Šiame pavyzdyje papildomi atsiskaitymai neatliekami, nes uždarymas sukuria atsiskaitymus tik už finansiškai atnaujintas operacijas.

Toliau pateiktoje iliustracijoje parodomas FIFO atsargų modelio poveikis tokioms operacijų sekoms, kai naudojamas išdavimų ir gavimų žymėjimas.

![FIFO su žymėjimu.](./media/fifo-with-marking.png)

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Fizinės operacijos pavaizduotos trumpesnėmis šviesiai pilkomis rodyklėmis.
- Finansines operacijas žymi ilgesnės juodos rodyklės.
- Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
- Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Kiekviena data diagramoje atskirta plona juoda vertikalia linija. Data nurodyta diagramos apačioje.
- Atsargų uždarymas pavaizduotas raudona vertikalia punktyrine linija.
- Atsiskaitymai ir žymėjimai, atlikti uždarant atsargas, vaizduojami raudonomis įstrižomis brūkšninėmis rodyklėmis, kurios pereina nuo kvito iki išdavimo.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
