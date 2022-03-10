---
title: LIFO data su faktine verte ir žymėjimu
description: Paskutinė į, pirma iš data (LIFO data) yra atsargų modelis, pagrįstas LIFO principu. Išdavimai iš atsargų sudengiami su paskutiniaisiais gavimais į atsargas remiantis atsargų operacijos data. Naudojant LIFO datą, jei nėra gavimo prieš išdavimą, išdavimas sudengimas su bet kuriuo gavimu, kuris įvyksta po išdavimo dienos. Tą pačią dieną galima sudengti keletą išdavimų paskutinio išduoto, paskutinio gauto tvarka.
author: AndersGirke
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51592
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6f5f447724ace473bece3007a96c4b56e90a908
ms.sourcegitcommit: addae271ddfc5a8b0721c23337f69916153db4cd
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/21/2022
ms.locfileid: "8330281"
---
# <a name="lifo-date-with-physical-value-and-marking"></a>LIFO data su faktine verte ir žymėjimu

[!include [banner](../includes/banner.md)]

"Paskutinė į, pirma iš" data (LIFO data) yra atsargų valdymo ir vertinimo metodas, kai atsargos, kurios buvo pagamintos ar įsigytos paskutinė, yra parduodamos, naudojamos arba likvidinamos pirmos. Microsoft atsargų uždarymo Dynamics 365 Supply Chain Management proceso metu sistema sukurs sudengimų, kuriuose paskutinis gavimas yra sugretintas su pirmuoju kiekvienos duotos datos išdavimu, prasidedant seniausia pirma data ir t. t. Kai naudojate atsargų modelį "paskutinė į, pirma nuskaityta data" (LIFO data), jei nėra gavimo prieš išdavimą, išdavimas sudengiama su bet kuriuo gavimu, kuris įvyksta po išdavimo datos. Sudengimų ir atitikimo principas pagrįstas atsargų operacijų finansine data. Kai tą pačią dieną yra keletas išdavimų, jie sudengti paskutinio išdavimo, paskutinio gavimo tvarka. Preliminarus sudengimų ir koregavimų vertinimas gali būti atliktas vykdant atsargų perskaičiavimo procesą.

Pažymėdami atsargų operacijas, kad konkretus prekės gavimas būtų sudengtas su tam tikro išdavimo atveju, galite nepaisyti LIFO datos principo. Kai naudodami LIFO datos atsargų modelį kuriate sudengimą ir koreguojate išdavimo vertę, atsižvelgiant į LIFO principą, reikalingas periodinis atsargų uždarymas. Kol jūs paleidžiate atsargų uždarymo procesą, išdavimo operacijos yra įvertintos pagal paleidžiamo vidurkio, kai įvyko faktiniai ir finansiniai atnaujinimai. Jei nenaudojate žymėjimo, vykdomasis vidurkis apskaičiuojamas, kai atliekamas faktinis arba finansinis atnaujinimas.

Naudojant LIFO datos atsargų modelį, rekomenduojama reguliariai atlikti atsargų uždarymą.

Toliau pateikti pavyzdžiai rodo, kaip veikia LIFO data trimis konfigūracijoje:

- LIFO data be faktinės **vertės įtraukimo pasirinkties**
- LIFO data su faktinės **vertės įtraukimo pasirinktimi**
- LIFO data su žymėjimu

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO data be faktinės vertės įtraukimo pasirinkties

Šiame pavyzdyje prekių modelio grupė nėra pažymėta, kad būtų įtraukta faktinė vertė. Toliau pateiktoje iliustracijoje parodytos šios operacijos.

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
- 7\. Atsargų uždarymas atliktas. Remiantis LIFO datos metodu pirmas finansiškai atnaujintas išdavimas bus sudengtas su paskutiniu finansiškai atnaujintu gavimu, prasideda galiu pirmąją dieną ir t. t. Šiame pavyzdyje sukuriamas vienas sudengimas nuo 3b iki 2b. Bus atliktas USD 6.00 3b, o gautos galutinės išlaidos bus USD 22.00.

Toliau esanti iliustracija rodo LIFO datos atsargų modelio poveikį, **kai nėra naudojamos pasirinkties** Įtraukti fizinę vertę.

![LIFO data be faktinės vertės įtraukimo pasirinkties.](media/lifo-date-without-include-physical-value.png)

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

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO data su faktinės vertės įtraukimo pasirinktimi

Jei prekių **modelių grupių** puslapyje pažymėtas **žymės** langelis Įtraukti fizinę vertę, sistema naudoja tiek faktines, tiek finansines gavimo operacijas, kad apskaičiuotų einamą vidutinę savikainą. Sistema taip pat, kur reikia, koreguoja faktiškai atnaujinto išdavimo operaciją. Išvalius **žymės** langelį Įtraukti fizinę vertę, atsargų uždarymas, naudojantis LIFO datos atsargų modelį, sudengia tik finansiškai atnaujintas operacijas.

Šiame pavyzdyje prekių modelio grupė pažymėta, kad būtų įtraukta faktinė vertė. 

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
- 7\. Atsargų uždarymas atliktas. Remiantis LIFO datos metodu pirmas finansiškai atnaujintas išdavimas bus sudengtas su paskutiniu finansiškai atnaujintu kiekvienos pradžios datos gavimu ir t. t. Šiame pavyzdyje sukuriamas vienas sudengimas nuo 2b iki 3b. Bus atliktas USD 6.00 3b, o gautos galutinės išlaidos bus USD 22.00. Be to, 6a operacija bus pakoreguota pagal gavimo operacijos išlaidas 5b. Sistema nesudengs šių operacijų, nes gavimas atnaujinamas faktiškai, bet ne finansiškai. Todėl faktinio išdavimo USD 6.33 koregavimas bus užregistruotas, o gautos koreguotos išlaidos bus USD 30.00.

Toliau pateiktoje iliustracijoje parodytas LIFO atsargų modelio poveikis, kai parinktis **Įtraukti faktinę vertę** naudojama.

![LIFO data su faktinės vertės įtraukimo pasirinktimi.](media/lifo-date-with-include-physical-value.png)

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

## <a name="lifo-date-with-marking"></a>LIFO data su žymėjimu

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
- 3c. 3b atsargų finansinis išdavimas yra pažymėtas kaip 1b atsargų finansinis išdavimas.
- 4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
- 5a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 5b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 6a. 1 vieneto, kurio savikaina 1, atsargų faktinis išdavimas USD 23.00 (finansiškai užregistruotų operacijų svertinis vidurkis)
- 7\. Atsargų uždarymas atliktas. Remiantis žymėjimo principu, kuris naudoja LIFO datos metodą, pažymėtos operacijos sudengiamos viena su kita. Šiame pavyzdyje 3b sudengiama su 1b, o -6,00 USD koregavimas registruojamas 3b, kad vertė būtų USD 10.00. Šiame pavyzdyje papildomi sudengimo nebus atliekami, nes uždarymas sudengs tik finansiškai atnaujintas operacijas.

Toliau esanti iliustracija rodo LIFO datos atsargų modelio poveikį, kai naudojamas išdavimų ir gavimų žymėjimas. 

![LIFO data su žymėjimu.](media/lifo-date-with-marking.png)

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
