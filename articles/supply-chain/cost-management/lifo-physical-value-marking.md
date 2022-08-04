---
title: LIFO su faktine verte ir žymėjimu
description: Paskutinis įvestas, pirmasis nurašytas (LIFO) yra atsargų modelis, kuriame vėliausi (naujausi) gavimai yra išduodami pirmiausiai. Išdavimai iš atsargų sudengiami su paskutiniaisiais gavimais į atsargas remiantis atsargų operacijos data.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55021
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1acc103291c5d648ac7e179a598348cd9cc2a93
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135576"
---
# <a name="lifo-with-physical-value-and-marking"></a>LIFO su faktine verte ir žymėjimu

[!include [banner](../includes/banner.md)]

Paskutinis į, pirmas iš (LIFO) yra atsargų valdymo ir vertinimo metodas, kai paskutinės pagamintos ar įsigytos atsargos parduodamos, naudojamos arba likvidinamos pirmos. Microsoft atsargų uždarymo proceso metu Dynamics 365 Supply Chain Management sistema sukurs sudengimą, kuriame paskutinis gavimas yra sugretintas su pirmu išdavimu ir t. t. Sudengimų ir atitikimo principas pagrįstas atsargų operacijų finansine data. Preliminarus sudengimų ir koregavimų vertinimas gali būti atliktas vykdant atsargų perskaičiavimo procesą.

Galite nepaisyti LIFO principo, pažymėdami atsargų operacijas, kad konkretus prekės gavimas būtų sudengtas su konkrečiu išdavimu. Kai, naudodami LIFO atsargų modelį, kuriate sudengimą ir koreguojate problemų vertę, remdate LIFO principą, reikalingas periodinis atsargų uždarymas. Kol jūs paleidžiate atsargų uždarymo procesą, išdavimo operacijos yra įvertintos pagal paleidžiamo vidurkio, kai įvyko faktiniai ir finansiniai atnaujinimai. Jei nenaudojate žymėjimo, vykdomasis vidurkis apskaičiuojamas, kai atliekamas faktinis arba finansinis atnaujinimas.

Šiuose pavyzdžiuose parodytas LIFO su trimis skirtingomis konfigūracijomis naudojimo poveikis:

- LIFO be parinkties **Įtraukti faktinę vertę**
- LIFO su parinktimi **Įtraukti faktinę vertę**
- LIFO su žymėjimu

## <a name="lifo-without-the-include-physical-value-option"></a>LIFO be faktinės vertės įtraukimo pasirinkties

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
- 7\. Atsargų uždarymas atliktas. Remiantis LIFO metodu pirmas finansiškai atnaujintas išdavimas bus sudengtas su paskutiniu finansiškai atnaujintu gavimu ir t. t. Šiame pavyzdyje sukuriamas vienas sudengimas nuo 5b iki 3b. Bus atliktas USD 14.00 3b, o gautos galutinės išlaidos bus USD 30.00.

Toliau pateiktoje iliustracijoje parodytas FIFO atsargų modelio poveikis kai kurioms operacijoms, kai parinktis **Įtraukti faktinę vertę** nenaudojama.

![LIFO be faktinės vertės įtraukties pasirinkties.](./media/lifo-without-including-physical-value.png)

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Faktinės operacijos žymimos trumpesniomis pilkomis rodyklėmis.
- Finansinės operacijos rodo ilgesniomis juodomis rodyklėmis.
- Atsargų gaviniai pateikiami vertikaliomis rodyklėmis virš ašies.
- Atsargų problemos vaizduojamos vertikaliomis rodyklėmis po ašimi.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Kiekviena diagramos data yra atskirta siaura juoda vertikalia linija. Data pažymima diagramos apačioje.
- Atsargų uždarymai vaizduojami raudona vertikalia punktyrine linija.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="lifo-with-the-include-physical-value-option"></a>LIFO su faktinės vertės įtraukimo pasirinktimi

Jei prekių **modelių grupių** puslapyje pažymėtas **žymės** langelis Įtraukti fizinę vertę, sistema naudoja tiek faktines, tiek finansines gavimo operacijas, kad apskaičiuotų einamą vidutinę savikainą. Sistema taip pat, kur reikia, koreguoja faktiškai atnaujinto išdavimo operaciją. Kai žymės **langelis Įtraukti fizinę** vertę išvalytas, atsargų uždarymas, naudojantis LIFO atsargų modelį, atlieka sudengimą tik finansiškai atnaujintoms operacijoms.

Toliau pateiktoje iliustracijoje parodytos šios operacijos.

- 1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
- 1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
- 2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
- 2b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 22,00 USD už vienetą.
- 3a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 16.00 (faktiškai ir finansiškai užregistruotų operacijų svertinė vidurkis).
- 3b. Finansinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 16.00 (faktiškai ir finansiškai užregistruotų operacijų svertinė vidurkis).
- 4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
- 5a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 5b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 6a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 23.67 (faktiškai ir finansiškai užregistruotų operacijų svertinė vidurkis).
- 7\. Atsargų uždarymas atliktas. Remiantis LIFO metodu pirmas finansiškai atnaujintas išdavimas bus sudengtas su paskutiniu finansiškai atnaujintu gavimu ir t. t. Šiame pavyzdyje sukuriamas vienas sudengimas nuo 3b iki 5b. Bus atliktas USD 14.00 3b, o gautos galutinės išlaidos bus USD 30.00. Be to, 6a operacija bus pakoreguota pagal 4a gavimo operacijos išlaidas. Sistema nesudengs šių operacijų, nes gavimas bus atnaujintas tik faktiškai, o ne finansiškai. Todėl faktinio išdavimo USD 1.33 koregavimas bus užregistruotas, o gautos koreguotos išlaidos bus USD 25.00.

Toliau pateiktoje iliustracijoje parodytas LIFO atsargų modelio poveikis kai kurioms operacijoms, kai parinktis **Įtraukti faktinę vertę** naudojama.

![LIFO su faktinės vertės įtraukties pasirinktimi.](./media/lifo-with-included-physical-value.png)

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Faktinės operacijos žymimos trumpesniomis pilkomis rodyklėmis.
- Finansinės operacijos rodo ilgesniomis juodomis rodyklėmis.
- Atsargų gaviniai pateikiami vertikaliomis rodyklėmis virš ašies.
- Atsargų problemos vaizduojamos vertikaliomis rodyklėmis po ašimi.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Kiekviena diagramos data yra atskirta siaura juoda vertikalia linija. Data pažymima diagramos apačioje.
- Atsargų uždarymai vaizduojami raudona vertikalia punktyrine linija.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="lifo-with-marking"></a>LIFO su žymėjimu

Žymėjimas yra procesas, leidžiantis susieti arba pažymėti išdavimo operaciją su gavimo operacija. Žymėjimą galima atlikti prieš arba po operacijos registravimo. Žymėjimą naudokite norėdami būti tikri dėl tikslios atsargų savikainos užregistravus operaciją arba uždarius atsargas. Pavyzdžiui, klientų aptarnavimo skyrius priėmė skubų užsakymą iš svarbaus kliento. Kadangi šis užsakymas yra skubaus užsakymo, jūs turite sumokėti daugiau už prekę, kad būtų patenkintas kliento prašymas.

Turite užtikrinti, kad pardavimo užsakymo SĄSKAITOS faktūros atsargų prekės išlaidos arba parduotų prekių savikaina (PPS) būtų pateikta paraštėje. Kai pirkimo užsakymas užregistruojamas, gaunama atsargų už 120,00 USD. Jeigu šis pardavimo užsakymo dokumentas pažymėtas prie pirkimo užsakymo prieš užregistruojant važtaraštį arba sąskaitą faktūrą, PPK bus 120,00 USD – prekei nebus taikoma dabartinio slankiojo vidurkio kaina. Jeigu pardavimo užsakymo važtaraštis arba SF užregistruojami prieš žymėjimą, COGS bus užregistruota taikant slankiojo vidurkio savikainą.

Prieš atsargų uždarymą šias dvi operacijas dar galima žymėti kartu.

Galite pažymėti išdavimo operaciją su gavimu prieš užregistruodami operaciją. Šį žymėjimą galite atlikti pardavimo užsakymo eilutėje, **·** **\> pardavimo užsakymo informacijos puslapyje, pardavimo užsakymo eilučių "** **FastTab" pasirinkdami Atsargų** žymėjimas. Galite peržiūrėti atidarytas gavimo operacijas **Žymėjimo** puslapyje.

Taip pat galite pažymėti išdavimo operaciją su gavimu užregistravę operaciją. Galite pažymėti išdavimo operaciją atvirai gavimo atsargose esančiai prekei iš registruoto atsargų koregavimo žurnalo.

Toliau pateiktoje iliustracijoje parodytos šios operacijos.

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
- 7\. Atsargų uždarymas atliktas. Remiantis žymėjimo principu, kuris naudoja LIFO metodą, pažymėtos operacijos sudengiamos viena su kita. Šiame pavyzdyje 3b sudengiama su 2b, o kurso koregavimas USD 6.00 užregistruotas 3b, kad vertė būtų USD 22.00. Šiame pavyzdyje papildomi sudengimo nebus atliekami, nes uždarymas sudengs tik finansiškai atnaujintas operacijas.

Nauja slankiojo vidurkio savikaina rodo finansiškai ir fiziškai atnaujintų operacijų vidurkį, 17,50 USD.

Toliau pateiktoje iliustracijoje parodomas LIFO atsargų modelio poveikis tokioms operacijų sekoms, kai naudojamas išdavimų ir gavimų žymėjimas.

![LIFO su žymėjimu.](./media/lifo-with-marking.png)

**Diagramos paaiškinimas**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Faktinės operacijos žymimos trumpesniomis pilkomis rodyklėmis.
- Finansinės operacijos rodo ilgesniomis juodomis rodyklėmis.
- Atsargų gaviniai pateikiami vertikaliomis rodyklėmis virš ašies.
- Atsargų problemos vaizduojamos vertikaliomis rodyklėmis po ašimi.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Kiekviena diagramos data yra atskirta siaura juoda vertikalia linija. Data pažymima diagramos apačioje.
- Atsargų uždarymai vaizduojami raudona vertikalia punktyrine linija.
- Iki atsargų uždarymo atlikti sudengimų ir žymų rodiniai žymimi raudonomis įstrižai einanomis rodyklėmis, kurios eina iš gavimo į išdavimą.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
