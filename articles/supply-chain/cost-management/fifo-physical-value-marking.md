---
title: FIFO su faktine verte ir žymėjimu
description: Pirma gaunama, pirma išduodama (FIFO) yra atsargų modelis, kuriame anksčiau gauti gavimai yra išduodami pirmi. Finansiškai atnaujinti atsargų išdavimai yra sudengiami prieš pirma finansiškai atnaujintus atsargų gavimus, pagrįstus atsargų operacijų finansine data.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 663dce9f871e96fec7017616732428c49b1224a0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676249"
---
# <a name="fifo-with-physical-value-and-marking"></a>FIFO su faktine verte ir žymėjimu

[!include [banner](../includes/banner.md)]


Pirmas į, pirmas iš (FIFO) yra atsargų valdymo ir vertinimo metodas, kai atsargos, kurios gaminamos ar įgyjamos pirma, yra parduodamos, naudojamos ar likvidinamos pirmos. Microsoft atsargų uždarymo proceso metu Dynamics 365 Supply Chain Management sistema sukurs sudengimą, kuriame pirmas gavimas yra sugretintas su pirmu išdavimu ir t. t.

Sudengimų ir atitikimo principas pagrįstas atsargų operacijų finansine data. Preliminarus sudengimų ir koregavimų vertinimas gali būti atliktas vykdant atsargų perskaičiavimo procesą.

Galite nepaisyti FIFO principo, pažymėdami atsargų operacijas, kad konkretus prekės gavimas būtų sudengtas su konkrečiu išdavimu. Kai naudojate FIFO atsargų modelį sudengti ir pakoreguoti išduodamą vertę pagal FIFO principą, reikalingas periodinis atsargų uždarymas. Kol jūs paleidžiate atsargų uždarymo procesą, išdavimo operacijos yra įvertintos pagal paleidžiamo vidurkio, kai įvyko faktiniai ir finansiniai atnaujinimai. Jei nenaudojate žymėjimo, vykdomasis vidurkis apskaičiuojamas, kai atliekamas faktinis arba finansinis atnaujinimas. Šiuose pavyzdžiuose parodytas FIFO su trimis skirtingomis konfigūracijomis naudojimo poveikis:

- FIFO be parinkties **Įtraukti faktinę vertę**
- FIFO su parinktimi **Įtraukti faktinę vertę**
- FIFO su žymėjimu

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO be įtraukiamos faktinės vertės pasirinkties

Šiame pavyzdyje žymės langelis **Įtraukti fizinę** vertę išvalytas išleisto produkto prekių modelių grupėje. Toliau pateiktoje iliustracijoje parodytos šios operacijos.

- 1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
- 1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
- 2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
- 2b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 22,00 USD už vienetą.
- 3a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 16.00 (finansiškai užregistruotų operacijų svertinis vidurkis).
- 3b. Finansinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 16.00 (finansiškai užregistruotų operacijų svertinis vidurkis).
- 4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
- 5a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 5b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 6a. 1 vieneto, kurio savikaina 1, atsargų faktinis išdavimas USD 23.00 (finansiškai užregistruotų operacijų svertinis vidurkis)
- 7\. Atsargų uždarymas atliktas. Pagrįstas FIFO metodu, pirmas finansiškai atnaujintas išdavimas bus sudengtas su pirmu finansiškai atnaujintu gavimu ir t. t. Šiame pavyzdyje sukuriamas vienas sudengimas nuo 1b iki 3b. Bus atliktas 3b –6,00 USD vertės koregavimas, o gautas galutines išlaidas USD 10.00.

Nauja veikiančio vidurkio savikaina atitinka finansiškai atnaujintų operacijų vidurkį. Toliau pateiktose iliustracijose parodytas FIFO atsargų modelio poveikis kai kurioms operacijoms, kai parinktis **Įtraukti faktinę vertę** nenaudojama.

![FIFO be faktinės vertės įtraukties pasirinkties.](./media/fifo-without-include-physical-value.png)

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Faktinės operacijos žymimos trumpesniomis pilkomis rodyklėmis.
- Finansinės operacijos rodo ilgesniomis juodomis rodyklėmis.
- Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
- Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Kiekviena diagramos data yra atskirta siaura juoda vertikalia linija. Data pažymima diagramos apačioje.
- Atsargų uždarymai vaizduojami raudona vertikalia punktyrine linija.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO su įtraukiamos faktinės vertės pasirinktimi

Jei prekių **modelių grupės** puslapyje pažymėtas **žymės** langelis Įtraukti fizinę vertę, sistema naudoja tiek faktines, tiek finansines gavimo operacijas, kad apskaičiuotų einamą vidutinę savikainą. Sistema taip pat, kur reikia, koreguoja faktiškai atnaujinto išdavimo operaciją. Atsargų uždarymas, naudojantis FIFO atsargų modelį, atlieka sudengimą tik su finansiškai atnaujintomis operacijomis. Toliau pateiktoje iliustracijoje parodytos šios operacijos.

- 1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
- 1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
- 2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
- 2b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 22,00 USD už vienetą.
- 3a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 16.00 (fiziškai ir finansiškai užregistruotų operacijų sąrangos vidurkis).
- 3b. Finansinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 16.00 (faktiškai ir finansiškai užregistruotų operacijų svertinė vidurkis).
- 4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
- 5a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 5b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 6a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 23.67 (faktiškai ir finansiškai užregistruotų operacijų svertinė vidurkis).
- 7\. Atsargų uždarymas atliktas. Pagrįstas FIFO metodu, pirmas finansiškai atnaujintas išdavimas bus sudengtas su pirmu finansiškai atnaujintu gavimu ir t. t. Šiame pavyzdyje sukuriamas vienas sudengimas nuo 1b iki 3b. Bus atliktas 3b –6,00 USD vertės koregavimas, o gautas galutines išlaidas USD 10.00. Be to, 6a operacija bus pakoreguota pagal gavimo operacijos išlaidas 2b. Sistema nesudengs šių operacijų, nes gavimas bus atnaujintas tik faktiškai, o ne finansiškai. Todėl faktinio išdavimo operacijoje bus užregistruotas tik -1,67 USD koregavimas, o gauta pakoreguota savikaina bus USD 22.00.

![FIFO su faktinės vertės įtraukties pasirinktimi.](./media/fifo-with-include-physical-value.png)

Atkreipkite dėmesį, kad atsargų uždarymo proceso rezultatas yra toks pats, nepaisant to, **·** **ar prekių modelių grupės puslapyje pasirenkate pasirinktį Įtraukti fizinę** vertę. Pasirinktis **Įtraukti fizinę vertę** veikia tik einamoji vidurkis.

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Faktinės operacijos žymimos trumpesniomis pilkomis rodyklėmis.
- Finansinės operacijos rodo ilgesniomis juodomis rodyklėmis.
- Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
- Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Kiekviena diagramos data yra atskirta siaura juoda vertikalia linija. Data pažymima diagramos apačioje.
- Atsargų uždarymai vaizduojami raudona vertikalia punktyrine linija.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="fifo-with-marking"></a>FIFO su žymėjimu

Žymėjimas yra procesas, leidžiantis susieti arba pažymėti išdavimo operaciją su gavimo operacija. Žymėjimą galima atlikti prieš arba po operacijos registravimo. Žymėjimą naudokite norėdami būti tikri dėl tikslios atsargų savikainos užregistravus operaciją arba uždarius atsargas.

Pavyzdžiui, klientų aptarnavimo skyrius priėmė skubų užsakymą iš svarbaus kliento. Kadangi šis užsakymas yra skubus užsakymas, norėdami įvykdyti kliento prašymą, už šią prekę turite mokėti daugiau. Turite užtikrinti, kad pardavimo užsakymo SĄSKAITOS faktūros atsargų prekės išlaidos arba parduotų prekių savikaina (PPS) būtų pateikta paraštėje. Kai pirkimo užsakymas užregistruojamas, gaunama atsargų už 120,00 USD. Jei pardavimo užsakymo dokumentas pažymėtas prie pirkimo užsakymo prieš užregistruojant važtaraštį arba SF, COGS bus USD 120.00 ne dabartinio einamoji vidutinė prekės savikaina. Jeigu pardavimo užsakymo važtaraštis arba SF užregistruojami prieš žymėjimą, COGS bus užregistruota taikant slankiojo vidurkio savikainą. Prieš atsargų uždarymą šias dvi operacijas dar galima žymėti kartu.

Kai gavimo operacija pažymima išdavimo operacijai, nepaisoma prekių modelių grupėje nustatyto vertinimo būdo, ir sistema sudengia šias operacijas. Galite rankiniu būdu pažymėti operaciją prieš **pardavimo** **\>** **užsakymo eilutę pardavimo užsakymo informacijos puslapyje pardavimo užsakymo žymėjimo puslapyje pardavimo užsakymo eilutėse "FastTab" pasirinkdami** Atsargų žymėjimas. Galite peržiūrėti atidarytas gavimo operacijas **Žymėjimo** puslapyje. Galite sugretinti arba pažymėti išdavimo operaciją su atvira atsargų prekės gavimo operacija iš užregistruoto atsargų koregavimo žurnalo. Toliau pateiktoje iliustracijoje parodytos šios operacijos.

- 1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
- 1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
- 2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
- 2b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 22,00 USD už vienetą.
- 3a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 16.00 (finansiškai užregistruotų operacijų svertinis vidurkis).
- 3b. Finansinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 16.00 (finansiškai užregistruotų operacijų svertinis vidurkis).
- 3c. 3b atsargų finansinis išdavimas yra pažymėtas kaip 2b atsargų finansinis išdavimas.
- 4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
- 5a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 5b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 6a. 1 vieneto, kurio savikaina 1, atsargų faktinis išdavimas USD 23.00 (finansiškai užregistruotų operacijų svertinis vidurkis)
- 7\. Atsargų uždarymas atliktas. Remiantis žymėjimo principu, kuris naudoja FIFO metodą, pažymėtos operacijos sudengimos viena su kita. Šiame pavyzdyje 3b sudengiama su 2b, o kurso koregavimas USD 6.00 užregistruotas 3b, kad vertė būtų USD 22.00. Šiame pavyzdyje papildomi sudengimo nebus atliekami, nes uždarymas sudengs tik finansiškai atnaujintas operacijas.

Toliau pateiktoje iliustracijoje parodomas FIFO atsargų modelio poveikis tokioms operacijų sekoms, kai naudojamas išdavimų ir gavimų žymėjimas.

![FIFO su žymėjimu.](./media/fifo-with-marking.png)

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Faktinės operacijos žymimos trumpesniomis pilkomis rodyklėmis.
- Finansinės operacijos rodo ilgesniomis juodomis rodyklėmis.
- Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
- Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Kiekviena diagramos data yra atskirta siaura juoda vertikalia linija. Data pažymima diagramos apačioje.
- Atsargų uždarymai vaizduojami raudona vertikalia punktyrine linija.
- Iki atsargų uždarymo atlikti sudengimų ir žymų rodiniai žymimi raudonomis įstrižai einanomis rodyklėmis, kurios eina iš gavimo į išdavimą.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
