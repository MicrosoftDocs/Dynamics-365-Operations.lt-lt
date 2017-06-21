---
title: "Svertinis vidurkis su faktine verte ir žymėjimu"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 65501
ms.assetid: 25041ff0-bafe-484d-a94a-e1772ad43204
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: cdbca6d9c71c901a1f4e7a8e5a2f9be1d3efb355
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="weighted-average-with-physical-value-and-marking"></a>Svertinis vidurkis su faktine verte ir žymėjimu

[!include[banner](../includes/banner.md)]




Kai vykdote atsargų uždarymą visi gavimai sudengiami prieš virtualų išdavimą, kuriame yra bendras gautas kiekis ir vertė. Šis virtualus išdavimas turi atitinkamą virtualų gavimą, iš kurio sudengiami išdavimai. Tokiu būdu visų išdavimų vidutinės išlaidos būna tokios pačios. Virtualus išdavimas ir gavimas gali būti suprantami kaip virtualus perdavimas, vadinamas svertinio vidurkio atsargų uždarymu.

Jeigu yra tik vienas gavimas, visi išdavimai gali būti atlikti iš jo, ir nereikės kurti virtualaus perdavimo. 

Naudodami svertinį vidurkį, galite žymėti atsargų operacijas, kad konkretus prekės gavimas būtų sudengtas su konkrečiu išdavimu, užuot naudoję svertinio vidurkio taisyklę. 

Naudojant svertinio vidurkio atsargų modelį, rekomenduojama kas mėnesį atlikti atsargų uždarymą. 

Svertinio vidurkio atsargų įkainojimo būdas apskaičiuojamas naudojant toliau nurodytą formulę.
-   Svertinis vidurkis = (Q1\*P1 + Q2\*P2 + Qn\*Pn) / (Q1 + Q2 + Qn)

Atsargų operacijos, paliekančios atsargų išdavimus. Tai apima pardavimo užsakymus, atsargų žurnalus ir gamybos užsakymus, esančius įvertintos savikainos registravimo datą. Ši įvertinta savikaina taip pat nurodoma kaip slankusis vidurkis. Uždarant atsargas sistemoje bus išanalizuotos ankstesnių laikotarpių ir dabartinio laikotarpio atsargų operacijos ir bus nustatoma, kuris iš toliau nurodytų uždarymo principų turėtų būti naudojamas.
-   Tiesioginis sudengimas
-   Suvestinis sudengimas

Sudengimai yra atsargų uždarymo registravimas, per kurį išdavimai nustatomi pagal pataisytą svertinį vidurkį uždarymo datą. Pateiktame pavyzdyje parodytas svertinio vidurkio naudojimo su penkiomis skirtingomis konfigūracijomis poveikis:
-   Svertinio vidurkio tiesioginis sudengimas be pasirinkties Įtraukti faktinę vertę
-   Svertinio vidurkio suvestinis sudengimas be pasirinkties Įtraukti faktinę vertę
-   Svertinio vidurkio tiesioginis sudengimas su pasirinktimi Įtraukti faktinę vertę
-   Svertinio vidurkio suvestinis sudengimas su pasirinktimi Įtraukti faktinę vertę
-   Svertinis vidurkis su žymėjimu

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Svertinio vidurkio tiesioginis sudengimas neįtraukiant faktinės vertės
Taikomas tas pats tiesioginio sudengimo principas, naudojamas su svertiniu vidurkiu ankstesnėse versijose. Sistema sudengs tiesiogiai tarp gavimų ir išdavimų. Sistemoje šis tiesioginio sudengimo principas naudojamas esant šioms konkrečioms situacijoms.
-   Per laikotarpį užregistruotas vienas gavimas ir vienas arba keletas išdavimų
-   Per laikotarpį buvo užregistruoti tik išdavimai, o atsargose yra prekių nuo ankstesnio uždarymo

Tolesniuose skyriuose pateiktame scenarijuje užregistruotas finansiškai atnaujintas gavimas ir išdavimas. Uždarant atsargas sistemoje gavimas bus tiesiogiai sudengiamas su išdavimu ir nereikės koreguoti išdavimo savikainos. Grafike parodytos šios operacijos.
-   1a. Faktinis atsargų gavimas atnaujintas 5 vienetais, vieneto kaina 10,00 USD
-   1b. Atsargų finansinis gavimas atnaujintas 5 vienetais, vieneto kaina 10,00 USD
-   2a. Faktinis atsargų išdavimas atnaujintas 2 vienetais, vieneto kaina 10,00 USD
-   2b. Finansinis atsargų išdavimas atnaujintas 2 vienetais, vieneto kaina 10,00 USD
-   3. Atsargų uždarymas atliekamas taikant tiesioginio sudengimo būdą, kad būtų sudengtas finansinis atsargų gavimas su finansiniu atsargų išdavimu.

Toliau pateiktoje diagramoje parodytas šių operacijų serijos poveikis, pasirinkus svertinio vidurkio atsargų modelį ir tiesioginio sudengimo principą be pasirinkties Įtraukti faktinę vertę. 

![Svertinio vidurkio tiesioginis sudengimas be faktinės vertės įtraukimo](./media/weightedaveragedirectsettlementwithoutincludephysicalvalue.gif) 

**Diagramos paaiškinimas**
-   Atsargų operacijos parodomos vertikaliomis rodyklėmis.
-   Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
-   Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
-   Virš (arba po) kiekviena vertikalia rodykle atsargų operacijos vertė nustatyta formatu „Quantity@Unitprice“.
-   Atsargų operacijos vertė skliausteliuose rodo, kad atsargų operacija atsargose užregistruota fiziškai.
-   Atsargų operacijos vertė be skliaustelių rodo, kad atsargų operacija atsargose užregistruota finansiškai.
-   Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
-   Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje seką.
-   Atsargų uždarymai rodomi raudona vertikalia punktyrine linija ir žyme Atsargų uždarymas.
-   Iki atsargų uždarymo atlikti sudengimai rodomi punktyrinėmis raudonomis rodyklėmis, einančiomis įstrižai nuo gavimo prie išdavimo.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Svertinio vidurkio suvestinis sudengimas be pasirinkties Įtraukti faktinę vertę
Su svertiniu vidurkiu naudojamas sudengimo principas, kuriuo remiantis visi uždarymo laikotarpio gavimai yra sumuojami operacijoje, kuri vadinasi Svertinio vidurkio atsargų uždarymas. Visi laikotarpio gavimai bus sudengiami su naujai sukurtos atsargų perkėlimo operacijos išdavimu. Visi laikotarpio išdavimai bus sudengiami su naujai sukurtos atsargų perkėlimo operacijos gavimu. Jeigu po atsargų uždarymo turimas atsargų kiekis yra teigiamas, tos turimos atsargos ir atsargų vertė susumuojamos naujoje atsargų perdavimo operacijoje (gavimas). Jeigu po atsargų uždarymo turimas atsargų kiekis yra neigiamas, turimos atsargos ir atsargų vertė yra iki galo nesudengtų atskirų išdavimų suma. Toliau pateiktame scenarijuje užregistruota keletas finansiškai atnaujintų gavimų ir vienas išdavimas. 

Uždarant atsargas sistemoje bus sugeneruojama ir užregistruojama apibendrinta atsargų perkėlimo operacija, o laikotarpio gavimai bus sudengiami su apibendrinta atsargų perkėlimo išdavimo operacija. Visi užregistruoti laikotarpio išdavimai bus sudengti su suvestine atsargų perkėlimo gavimo operacija. Apskaičiuotas svertinis vidurkis yra 15,00 USD. Išdavimas iš pradžių užregistruotas su įvertinta 14,67 USD savikaina. Todėl neigiamas 0,33 USD koregavimas bus sukurtas ir užregistruotas išdavime. Kaip ir atsargų uždarymo datą turimos atsargos yra 3 vienetai, kurių vertė 45,00 USD. 

Tolesniame grafike parodytos šios operacijos:
-   1a. Atsargų fizinis gavimas atnaujintas 2 vienetais, kiekvieno vieneto kaina 11,00 USD.
-   1b. Atsargų finansinis gavimas atnaujintas 2 vienetais, kiekvieno vieneto kaina 14,00 USD.
-   2a. Atsargų fizinis gavimas atnaujintas 1 vienetais, kiekvieno vieneto kaina 12,00 USD.
-   2b. Atsargų finansinis gavimas atnaujintas 1 vienetu, vieneto kaina 16,00 USD.
-   3a. Atsargų faktinis išdavimas atnaujintas 1 vienetu, vieneto kaina 14,67 USD (slankusis vidurkis).
-   3b. Atsargų finansinis išdavimas atnaujintas 1 vienetu, vieneto kaina 14,67 USD (slankusis vidurkis).
-   4a. Atsargų fizinis gavimas atnaujintas 1 vienetais, kiekvieno vieneto kaina 14,00 USD.
-   4b. Atsargų finansinis gavimas atnaujintas 1 vienetu, vieneto kaina 16,00 USD.
-   5. Atsargų uždarymas atliktas.
-   6a. „Slankiojo vidurkio atsargų uždarymo operacija“ finansinis išdavimas sukuriamas, siekiant susumuoti visų atsargų finansinių gavimų sudengimus.
-   6b. „Svertinio vidurkio atsargų uždarymo operacija“ finansinis gavimas, sukurtas kaip 5a korespondentinė sąskaita.

Toliau pateiktoje diagramoje parodytas šių operacijų serijos poveikis, pasirinkus svertinio vidurkio atsargų modelį ir apibendrinto sudengimo principą be pasirinkties Įtraukti faktinę vertę. 

![Svertinio vidurkio apibendrintas sudengimas su faktinės vertės įtraukimu    ](./media/weightedaveragesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Diagramos paaiškinimas**
-   Atsargų operacijos parodomos vertikaliomis rodyklėmis.
-   Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
-   Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
-   Virš (arba po) kiekviena vertikalia rodykle atsargų operacijos vertė nustatyta formatu „Quantity@Unitprice“.
-   Atsargų operacijos vertė skliausteliuose rodo, kad atsargų operacija atsargose užregistruota fiziškai.
-   Atsargų operacijos vertė be skliaustelių rodo, kad atsargų operacija atsargose užregistruota finansiškai.
-   Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
-   Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje seką.
-   Atsargų uždarymai rodomi raudona vertikalia punktyrine linija ir žyme Atsargų uždarymas.
-   Iki atsargų uždarymo atlikti sudengimai rodomi punktyrinėmis raudonomis rodyklėmis, einančiomis įstrižai nuo gavimo prie išdavimo.
-   Raudonos rodyklės rodo gavimo operacijas, sudengtas su sistemos sukurta išdavimo operacija.
-   Žalia rodyklė rodo korespondentinę sistemos sukurtą gavimo operaciją, su kuria sudengta iš pradžių užregistruota išdavimo operacija

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Svertinio vidurkio tiesioginis sudengimas su pasirinktimi Įtraukti faktinę vertę
Parametras Įtraukti faktinę vertę svertinio vidurkio atsargų modeliui taikomas kitaip nei ankstesnėse produkto versijose. Formoje Prekių modelių grupė pažymėkite langelį Įtraukti faktinę vertę. Tada sistemoje skaičiuojant įvertintą savikainą arba paleidžiamąjį vidurkį bus naudojami faktiškai atnaujinti gavimai. Išdavimai bus užregistruoti remiantis įvertinta laikotarpio savikaina. Uždarant atsargas finansiškai atnaujinti gavimai bus naudojami tik skaičiuojant svertinį vidurkį. Naudojant svertinio vidurkio atsargų modelį, rekomenduojama kas mėnesį atlikti atsargų uždarymą. Šiame svertinio vidurkio tiesioginio sudengimo pavyzdyje prekių modelių grupė pažymėta įtraukti faktinę vertę. 

Tolesniame grafike parodytos šios operacijos:
-   1a. Atsargų fizinis gavimas atnaujintas 1 vienetais, kiekvieno vieneto kaina 11,00 USD.
-   1b. Atsargų finansinis gavimas atnaujintas 1 vienetais, kiekvieno vieneto kaina 10,00 USD.
-   2a. Atsargų fizinis gavimas atnaujintas 1 vienetais, kiekvieno vieneto kaina 15,00 USD.
-   3a. Atsargų faktinis išdavimas atnaujintas 1 vienetu, vieneto kaina 12,50 USD (slankiojo vidurkio kaina, nes atsižvelgiama į faktinio gavimo vertę).
-   3b. Atsargų finansinis išdavimas atnaujintas 1 vienetu, vieneto kaina 12,50 USD (slankiojo vidurkio kaina, nes atsižvelgiama į faktinę gavimo vertę).
-   4. Atsargų uždarymas atliktas. Uždarant atsargas sistemoje bus nepaisoma visų tik faktiškai atnaujintų atsargų operacijų. Bus taikomas tiesioginio sudengimo principas, nes yra tik vienas finansinis gavimas. Bus užregistruotas atsargų finansinio išdavimo operacijos 2,50 USD koregavimas atsargų uždarymo datą. Uždarius atsargas, turimos atsargos bus 1 vienetas, kurio slankiojo vidurkio savikaina 15,00 USD.

Toliau pateiktoje diagramoje parodytas šių operacijų serijos poveikis, pasirinkus svertinio vidurkio atsargų modelį ir tiesioginio sudengimo principą su pasirinktimi Įtraukti faktinę vertę. 

![Svertinio vidurkio tiesioginis sudengimas su faktinės vertės įtraukimu](./media/weightedaveragedirectsettlementwithincludephysicalvalue.gif) 

**Diagramos paaiškinimas**
-   Atsargų operacijos parodomos vertikaliomis rodyklėmis.
-   Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
-   Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
-   Virš (arba po) kiekviena vertikalia rodykle atsargų operacijos vertė nustatyta formatu „Quantity@Unitprice“.
-   Atsargų operacijos vertė skliausteliuose rodo, kad atsargų operacija atsargose užregistruota fiziškai.
-   Atsargų operacijos vertė be skliaustelių rodo, kad atsargų operacija atsargose užregistruota finansiškai.
-   Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
-   Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje seką.
-   Atsargų uždarymai rodomi raudona vertikalia punktyrine linija ir žyme Atsargų uždarymas.
-   Iki atsargų uždarymo atlikti sudengimai rodomi punktyrinėmis raudonomis rodyklėmis, einančiomis įstrižai nuo gavimo prie išdavimo.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Svertinio vidurkio suvestinis sudengimas su pasirinktimi Įtraukti faktinę vertę
Parametras Įtraukti faktinę vertę svertiniam vidurkiui taikomas kitaip nei ankstesnėse versijose. Puslapyje Prekių modelių grupė pažymėkite langelį Įtraukti faktinę vertę. Tada sistemoje skaičiuojant įvertintą savikainą arba paleidžiamąjį vidurkį bus naudojami faktiškai atnaujinti gavimai. Išdavimai bus užregistruoti remiantis įvertinta laikotarpio savikaina. Uždarant atsargas finansiškai atnaujinti gavimai bus naudojami tik skaičiuojant svertinį vidurkį. Naudojant svertinio vidurkio atsargų modelį, rekomenduojama kas mėnesį atlikti atsargų uždarymą. Šiame svertinio vidurkio suvestinio sudengimo pavyzdyje atsargų modelis pažymimas siekiant įtraukti faktinę vertę. 

Tolesniame grafike parodytos šios operacijos:
-   1a. Atsargų fizinis gavimas atnaujintas 2 vienetais, kiekvieno vieneto kaina 11,00 USD.
-   1b. Atsargų finansinis gavimas atnaujintas 2 vienetais, kiekvieno vieneto kaina 14,00 USD.
-   2. Atsargų fizinis gavimas atnaujintas 1 vienetais, kiekvieno vieneto kaina 10,00 USD.
-   3a. Atsargų fizinis gavimas atnaujintas 1 vienetais, kiekvieno vieneto kaina 12,00 USD.
-   3b. Atsargų finansinis gavimas atnaujintas 1 vienetu, vieneto kaina 16,00 USD.
-   4a. Atsargų faktinis išdavimas atnaujintas 1 vienetu, vieneto kaina 13,50 USD (slankiojo vidurkio kaina, nes atsižvelgiama į faktinio gavimo vertę).
-   4b. Atsargų finansinis išdavimas atnaujintas 1 vienetu, vieneto kaina 13,50 USD (slankiojo vidurkio kaina, nes atsižvelgiama į faktinio gavimo vertę).
-   5a. Atsargų fizinis gavimas atnaujintas 1 vienetais, kiekvieno vieneto kaina 14,00 USD.
-   5b. Atsargų finansinis gavimas atnaujintas 1 vienetu, vieneto kaina 16,00 USD.
-   6. Atsargų uždarymas atliktas. Uždarant atsargas sistemoje bus nepaisoma visų tik faktiškai atnaujintų atsargų operacijų. Bus naudojamas suvestinio sudengimo principas, nes yra tik vienas finansinis gavimas. Bus užregistruotas atsargų finansinio išdavimo operacijos 1,50 USD koregavimas atsargų uždarymo datą. Uždarius atsargas, turimos atsargos bus 3 vienetai, kurių slankiojo vidurkio savikaina 15,00 USD.
-   7a. „Slankiojo vidurkio atsargų uždarymo operacija“ finansinis išdavimas sukuriamas, siekiant susumuoti visų atsargų finansinių gavimų sudengimus.
-   7b. „Svertinio vidurkio atsargų uždarymo operacija“ finansinis gavimas sukuriamas kaip 5a korespondentinė sąskaita.

Toliau pateiktoje diagramoje parodytas šių operacijų serijos poveikis, pasirinkus svertinio vidurkio atsargų modelį ir apibendrinto sudengimo principą be pasirinkties Įtraukti faktinę vertę. 

![Svertinio vidurkio apibendrintas sudengimas su faktinės vertės įtraukimu](./media/weightedaveragesummarizedsettlementwithincludephysicalvalue.gif) 

**Diagramos paaiškinimas**
-   Atsargų operacijos parodomos vertikaliomis rodyklėmis.
-   Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
-   Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
-   Virš (arba po) kiekviena vertikalia rodykle atsargų operacijos vertė nustatyta formatu „Quantity@Unitprice“.
-   Atsargų operacijos vertė skliausteliuose rodo, kad atsargų operacija atsargose užregistruota fiziškai.
-   Atsargų operacijos vertė be skliaustelių rodo, kad atsargų operacija atsargose užregistruota finansiškai.
-   Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
-   Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., 1a. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje seką.
-   Atsargų uždarymai rodomi raudona vertikalia punktyrine linija ir žyme Atsargų uždarymas.
-   Iki atsargų uždarymo atlikti sudengimai rodomi punktyrinėmis raudonomis rodyklėmis, einančiomis įstrižai nuo gavimo prie išdavimo.
-   Raudonos rodyklės rodo gavimo operacijas, sudengtas su sistemos sukurta išdavimo operacija.
-   Žalia rodyklė rodo korespondentinę sistemos sukurtą gavimo operaciją, su kuria sudengta iš pradžių užregistruota išdavimo operacija

## <a name="weighted-average-with-marking"></a>Svertinis vidurkis su žymėjimu
Žymėjimas yra procesas, leidžiantis susieti arba pažymėti išdavimo operaciją su gavimo operacija. Žymėjimą galima atlikti prieš arba po operacijos registravimo. Žymėjimą naudokite norėdami patikrinti tikslias uždarymo išlaidas užregistravus operaciją arba atlikus atsargų uždarymą. 

Pavyzdžiui, jūsų Klientų aptarnavimo tarnyba priėmė skubų užsakymą iš svarbaus kliento. Kadangi tai skubus užsakymas, norėdami patenkinti kliento pageidavimus, už šią prekę turėsite mokėti daugiau. Jūs turite įsitikinti, kad šio pardavimo užsakymo sąskaitos faktūros atsargų elemento išlaidos arba parduotų prekių savikaina (PPK) yra pateikiama paraštėje. 

Kai pirkimo užsakymas užregistruojamas, gaunama atsargų už 120,00 USD. Pvz., šis pardavimo užsakymo dokumentas pažymėtas prie pirkimo užsakymo prieš užregistruojant važtaraštį ar sąskaitą faktūrą. Tada PPK bus 120,00 USD – prekei nebus taikoma dabartinio slankiojo vidurkio kaina. Jeigu pardavimo užsakymo važtaraštis arba SF užregistruojami prieš žymėjimą, COGS bus užregistruota taikant slankiojo vidurkio savikainą. 

Prieš atsargų uždarymą šias dvi operacijas dar galima žymėti kartu. 

Gavimo operacija pažymima prie išdavimo operacijos. Tada bus nepaisoma prekės modelių grupėje pasirinkto vertinimo būdo ir sistemoje šios operacijos bus sudengiamos tarpusavyje. 

Galite pažymėti išdavimo operaciją su gavimu prieš užregistruodami operaciją. galite tai atlikti puslapio Pardavimo užsakymas pardavimo užsakymo eilutėje. Atidarytas gavimo operacijas galima peržiūrėti puslapyje Žymėjimas. 

Galite pažymėti išdavimo operaciją su gavimu užregistravę operaciją. Galite suderinti arba pažymėti inventorizuojamos prekės atidarytos gavimo operacijos išdavimo operaciją užregistruotų atsargų koregavimų žurnale. 

Tolesniame grafike parodytos šios operacijos:
-   1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
-   1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
-   2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
-   2b. 1 vieneto, kurio kaina 20,00 USD, finansinis gavimas į atsargas.
-   3a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
-   4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
-   4b. 1 vieneto, kurio kaina 30,00 USD, finansinis gavimas į atsargas.
-   5a. 1 vieneto, kurio savikaina 21,25 USD, faktinis išdavimas iš atsargų (finansiškai ir faktiškai atnaujintų operacijų slankusis vidurkis).
-   5b. 1 vieneto atsargų finansinis išdavimas prieš registruojant operaciją yra žymimas prie atsargų gavimo 2b. Ši operacija yra registruojama taikant 20,00 USD savikainą.
-   6a. 1 vieneto, kurio savikaina 21,25 USD, fizinis išdavimas iš atsargų.
-   7 Atsargų uždarymas įvykdytas. Kadangi finansiškai atnaujinta operacija yra pažymima prie esamo gavimo, šios operacijos yra sudengiamos viena su kita nekoreguojant.

Nauja slankiojo vidurkio savikaina rodo finansiškai ir fiziškai atnaujintų operacijų vidurkį – 27,50 USD. 

Pateiktoje diagramoje parodyta operacijų serija, kai pasirenkamas svertinio vidurkio atsargų modelis su žymėjimu. 

![Svertinis vidurkis su žymėjimu](./media/weightedaveragewithmarking.gif) 

**Diagramos paaiškinimas**
-   Atsargų operacijos parodomos vertikaliomis rodyklėmis.
-   Atsargų gavimai parodomi vertikaliomis rodyklėmis virš laiko juostos.
-   Atsargų išdavimai parodomi vertikaliomis rodyklėmis po laiko juosta.
-   Virš (arba po) kiekviena vertikalia rodykle atsargų operacijos vertė nustatyta formatu „Quantity@Unitprice“.
-   Atsargų operacijos vertė skliausteliuose rodo, kad atsargų operacija atsargose užregistruota fiziškai.
-   Atsargų operacijos vertė be skliaustelių rodo, kad atsargų operacija atsargose užregistruota finansiškai.
-   Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
-   Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje seką.
-   Atsargų uždarymai rodomi raudona vertikalia punktyrine linija ir žyme Atsargų uždarymas.
-   Iki atsargų uždarymo atlikti sudengimai rodomi punktyrinėmis raudonomis rodyklėmis, einančiomis įstrižai nuo gavimo prie išdavimo.






