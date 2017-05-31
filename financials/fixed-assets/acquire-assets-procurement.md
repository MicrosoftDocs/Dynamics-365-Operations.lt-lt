---
title: "Turto pirkimas įsigyjant"
description: "Šiame straipsnyje aprašyta, kaip nustatyti integravimą tarp ilgalaikio turto ir mokėtinų sumų, kad automatiškai sukurtumėte ilgalaikį turtą iš pirkimo užsakymų ar SF, arba, kad automatiškai registruotumėte ilgalaikio turto įsigijimą ir įsigijimo operacijas."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3481
ms.assetid: d4e73a3f-633b-48b2-b8db-7a4a59a4d7ec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: aa5598ddd0d397314b42c6ac0c1b0d02eb95ebb4
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="acquire-assets-through-procurement"></a>Turto pirkimas įsigyjant

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašyta, kaip nustatyti integravimą tarp ilgalaikio turto ir mokėtinų sumų, kad automatiškai sukurtumėte ilgalaikį turtą iš pirkimo užsakymų ar SF, arba, kad automatiškai registruotumėte ilgalaikio turto įsigijimą ir įsigijimo operacijas.

 Galimi toliau nurodyti Ilgalaikio turto ir Mokėtinų sumų integravimo būdai; tokį patį būdą reikia naudoti visam ilgalaikiam turtui:
-   Jūs neautomatiniu būdu sukuriate ilgalaikį turtą prieš įtraukdami ilgalaikio turto numerį į pirkimo užsakymo arba tiekėjo sąskaitą faktūrą. Kai registruojate tiekėjo sąskaitą faktūrą, automatiškai užregistruojama turto įsigijimo operacija. Tai numatytasis metodas.
-   Jūs neautomatiniu būdu sukuriate ilgalaikį turtą prieš įtraukdami ilgalaikio turto numerį į pirkimo užsakymo arba tiekėjo sąskaitą faktūrą. Kai registruojate tiekėjo sąskaitą faktūrą, turto įsigijimo operacija nėra užregistruojama automatiškai.
-   Ilgalaikis turtas automatiškai sukuriamas, kai užregistruojate produkto gavimo kvitą arba tiekėjo sąskaitą faktūrą, kurios žymės langelis Kurti naują ilgalaikį turtą pažymėtas. Kai registruojate tiekėjo sąskaitą faktūrą, automatiškai užregistruojama turto įsigijimo operacija.
-   Ilgalaikis turtas automatiškai sukuriamas, kai užregistruojate produkto gavimo kvitą arba tiekėjo sąskaitą faktūrą, kurios žymės langelis Kurti naują ilgalaikį turtą pažymėtas. Kai registruojate tiekėjo sąskaitą faktūrą, turto įsigijimo operacija nėra užregistruojama automatiškai.

Jei jums labiau priimtina ilgalaikį turtą kurti rankiniu būdu, pasirinkite vieną iš pirmųjų dviejų metodų ir priskirkite ilgalaikio turto numerį prie pirkimo užsakymo arba tiekėjo sąskaitą faktūrą. Pasirinkite vieną iš paskutiniųjų dviejų metodų, jei jums priimtinas lankstesnis būdas: kartais galite kurti ilgalaikį turtą rankiniu būdu, o kartais galite automatiškai sukurti ilgalaikį turtą pagal ilgalaikio turto eilutės prekės informaciją. 

Nesvarbu, ar kuriate ilgalaikį turtą rankiniu būdu, ar naudojate lankstesnį būdą, turite nuspręsti, ar įsigijimo operaciją galima registruoti tik į ilgalaikį turtą, ar ją galima registruoti registruojant sąskaitą faktūrą. Kai kurios organizacijos pasirenka, kad vartotojai kurtų ilgalaikio turto įsigijimą ir įsigijimo operacijas rankiniu būdu, įvesdami žurnalo įrašus ar pasiūlymus. 

Šioje temoje aprašoma išsami informacija apie kiekvieną metodą.

## <a name="methods-for-manually-creating-fixed-assets"></a> Ilgalaikio turto kūrimo rankiniu būdu metodai
Kai užregistruojate tiekėjo sąskaitą faktūrą, kurios eilutėse įvestas ilgalaikio turto numeris, jei pasirinktis Leisti turto įsigijimą iš pirkimo pasirinkta puslapyje Ilgalaikio turto parametrai, įsigijimas užregistruojamas automatiškai ir turto būsena pasikeičia į Atidaryta. 

Jei įsigijimo negalima užregistruoti, galite rankiniu būdu įvesti įsigijimo operaciją į Ilgalaikį turtą arba, kad sukurtumėte kelias įsigijimo operacijas iš karto, galite tuo pačiu metu naudotis Ilgalaikio turto žurnalu.

> [!NOTE]                                                                                                                              
> Jei Ilgalaikis turtas nustatytas taip, kad apribotų įsigijimo operacijos registravimą konkrečiai vartotojų grupei, privalote būti tos vartotojų grupės narys, kad galėtumėte iš sąskaitos faktūros registruoti įsigijimo operacijas.

## <a name="methods-for-automatically-creating-fixed-assets"></a> Ilgalaikio turto kūrimo automatiniu būdu metodai
Registruojant produkto gavimo dokumentą, kurio eilutei pasirinkta pasirinktis Kurti naują ilgalaikį turtą, sukuriamas naujas ilgalaikis turtas, kurio būsena yra Dar neįgytas. Po to, kai registruojate tiekėjo sąskaitą faktūrą su nauju ilgalaikiu turtu, užregistruojama naujo ilgalaikio turto įsigijimo operacija ir turto būsena pasikeičia į Atidaryta, jei Ilgalaikis turtas nustatytas taip, kad leistų turto įsigijimą iš Mokėtinų sumų ir jūs esate galinčios registruoti įsigijimo operacijas vartotojų grupės narys. 

Jei pirkimo eilutės žymės langelis Naujas ilgalaikis turtas? nebuvo pažymėtas, kai užregistravote produkto gavimo kvitą, bet jis buvo pažymėtas užregistravus tiekėjo sąskaitą faktūrą, sukuriamas naujas ilgalaikis turtas, įgyjamas su būsena Atidaryta, jei Ilgalaikis turtas nustatytas, kad leistų kūrimą ir įgijimą. Kai registruojate tiekėjo sąskaitą faktūrą, papildomas turtas nesukuriamas, jei jis jau buvo sukurtas, kai užregistravote produkto gavimo kvitą.

### <a name="capitalization-threshold"></a>Kapitalizacijos ribinė vertė

Kai naudojate metodą, kuriuo turtas kuriamas ir įgyjamas automatiškai, galite nustatyti sistemą, kad būtų tikrinama, ar ilgalaikio turto pirkimo suma atitinka nurodytą turto nusidėvėjimo kapitalizacijos ribinę vertę. Tokiu atveju pažymima turto knygos parinktis Nusidėvėjimas, kai turtas sukuriamas iš mokėtinų sumų. 

Kapitalizacijos ribinė vertė yra suma valiuta, kuria nustatoma, ar turtai nusidėvėję, kai atitinka nurodytą sumą. Pvz., jei perkate turto ir pirkimo suma yra mažesnė už kapitalizacijos vertę, turtas nepažymimas, kaip galintis nusidėvėti; jei pirkimo suma atitinka arba viršija ribinę vertę, turtas pažymimas, kaip galintis nusidėvėti. 

Galite nustatyti kapitalizacijos ribinę vertę puslapyje Ilgalaikio turto grupės.

## <a name="scenario"></a>Scenarijus
Toliau pateiktame scenarijuje aptariamas visas ilgalaikio turto ir mokėtinų sumų integravimas. Rodomas pavyzdinis nustatymas ir aprašomas įsigijimo pasiūlymų naudojimas. 

Šiame scenarijuje sistema nustatyta taip:

-   Turtas automatiškai kuriamas gavus produktą arba registruojant tiekėjo sąskaitą faktūrą, bet Ilgalaikis turtas nustatomas taip, kad būtų išvengta įsigijimo operacijų registravimo iš Mokėtinų sumų.
-   Ilgalaikio turto gavimo ir Ilgalaikio turto išdavimo sąskaitos tipo sąskaitos nurodytos puslapio Prekių grupės lauke Sąskaitos tipas.
-   Kompiuterių grupės (COMP) kapitalizacijos ribinė vertė yra 1500.
-   Jūsų užduotis yra įvesti naujo nešiojamojo kompiuterio, kurį naudos darbuotojas, pirkimo užsakymą, registruoti pirkimo užsakymą, patikrinti, kad siunčiantis klerkas užregistruotų produkto gavimo kvitą, užregistruoti tiekėjo sąskaitą faktūrą ir patikrinti, kad buhalteris atnaujintų nešiojamojo kompiuterio turto būseną į Atidaryta.

Visų pirma naudokite puslapį Pirkimo užsakymas, kad įvestumėte išsamią informaciją apie nešiojamąjį kompiuterį, kuris kainuoja 1600. Pirkimo užsakymo eilutėse, skirtuke Ilgalaikio turto „FastTab“, pasirinkite pasirinktį Naujas ilgalaikis turtas?, pasirinkite COMP kaip ilgalaikio turto grupę ir įrašykite pirkimo užsakymą. 

Kai nešiojamasis kompiuteris gautas, siunčiantis klerkas įveda ir užregistruoja produkto gavimo kvitą, kad įrašytų nešiojamojo kompiuterio gavimą. Nešiojamojo kompiuterio turtas sukuriamas ir jo būsena yra Dar neįgytas. Suma viršija kapitalizacijos ribinę vertę. Todėl pasirenkama nešiojamojo kompiuterio turto knygų parinktis Nusidėvėjimas. Atliktos toliau pateiktos operacijos.

| Prekės/Paslaugos pavadinimas                               | Paskyra             | Debetas    | Kreditas   |
|-------------------------------------------|---------------------|----------|----------|
| Pirkimas, Produkto gavimo kvito pirkimas        | Gavimai, kuriems neišrašyta sąskaita | 1600,00 |          |
| Pirkimas, Produkto gavimo kvito pirkimo korespondentinė sąskaita | Sukaupti pirkimai   |          | 1600,00 |

Po to registruokite nešiojamojo kompiuterio tiekėjo sąskaitą faktūrą. Nešiojamojo kompiuterio būsena nepasikeičia, nes Ilgalaikis turtas nustatytas taip, kad, užregistravus tiekėjo sąskaitą faktūrą, neleistų registruoti turto įsigijimo operacijos. Registruojant tiekėjo sąskaitą faktūrą buvo pasirinkta pasirinktis Kurti naują ilgalaikį turtą. Todėl buvo naudojama Ilgalaikio turto gavimo sąskaitos kvitas. Sąskaita Ilgalaikio turto išdavimas nebuvo naudojama, nes nebuvo užregistruotas joks įsigijimas; ji bus naudojama vėliau, kai jūsų organizacijos buhalteris užregistruos ilgalaikio turto įsigijimo operaciją naudodamasis įsigijimo pasiūlymais. 

Atliktos toliau pateiktos operacijos.

| Prekės/Paslaugos pavadinimas                               | Paskyra             | Debetas    | Kreditas   |
|-------------------------------------------|---------------------|----------|----------|
| Pirkimas, Produkto gavimo kvito pirkimo korespondentinė sąskaita | Sukaupti pirkimai   | 1600,00 |          |
| Tiekėjo balansas                            | Mokėtinos sumos    |          | 1600,00 |
| Pirkimas, ilgalaikio turto gavimas             | Kompiuterio išlaidos    | 1600,00 |          |
| Pirkimas, Produkto gavimo kvito pirkimas        | Gavimai, kuriems neišrašyta sąskaita |          | 1600,00 |

Galiausiai buhalteris peržiūri visą ilgalaikį turtą, kurio būsena yra Dar neįgytas. Todėl peržiūrimas ir naujas nešiojamojo kompiuterio turtas. Tada buhalteris iš Ilgalaikio turto žurnalo eilučių atidaro puslapį Įsigijimo pasiūlymas ir sukuria visų turtų, turinčių sąskaitą faktūrą, bet kurių būsena yra Dar neįgytas, įsigijimo operacijas. Kai žurnalas užregistruojamas, nešiojamojo kompiuterio turto būsena pakeičiama į Atidaryta. Ilgalaikio turto išdavimo sąskaita kredituojama, o turto įgijimo sąskaita debetuojama. 

Toliau pateikiamos šio scenarijaus variacijos:

-   Jei Ilgalaikis turtas yra nustatytas taip, kad leistų registruoti turto įsigijimo operacijas užregistravus tiekėjo sąskaitą faktūrą, buhalteris neprivalo naudotis Ilgalaikio turto įsigijimo pasiūlymais, nes sukuriama įsigijimo operacija. Be to, užregistravus tiekėjo SF atnaujinamos skirtingos sąskaitos. Vietoj Kompiuterio išlaidų, Ilgalaikio turto gavimo atsargų sąskaita debetuojama ir sukuriamos dvi papildomos operacijos: turto įsigijimo sąskaita debetuojama, o Ilgalaikio turto išdavimo atsargų sąskaita kredituojama.
-   Jei nepasirinkta pasirinktis Kurti naują ilgalaikį turtą užregistravus produkto gavimo kvitą, tuo metu nekuriamas joks turtas. Jei pasirenkate pasirinktį Kurti naują ilgalaikį turtą prieš registruojant tiekėjo sąskaitą faktūrą, turtas sukuriamas ir jo būsena yra Dar neįgytas arba būsena Atidaryta, jei taip pat registruojate įsigijimo operacijas, kai registruojamos tiekėjo sąskaitos faktūros.
-   Jei nešiojamojo kompiuterio kaina yra 1400, o ne 1600, kapitalizacijos ribinė vertė nepasiekta. Todėl turtas sukuriamas ir nusidėvėjimo pasirinktis išvalyta.
-   Jei naudojamas sąskaitos faktūros registras, naudokite puslapį Sąskaitos faktūros patvirtinimo žurnalas po to, kai užregistruojamas sąskaitos faktūros registras, kad nuskaitytumėte kvitą, susiekite pirkimo užsakymą su tiekėjo sąskaita faktūra, pasirinkite pasirinktį Kurti naują ilgalaikį turtą ir užregistruokite tiekėjo sąskaitą faktūrą. Jei esate galinčios kurti įsigijimo operacijas vartotojų grupės narys, įsigijimas sukuriamas ir turto būsena yra Atidaryta.
-   Jei gaunamas tik dalinis kiekis, nesukuriamas joks pirmosios tiekėjo sąskaitos faktūros turto įsigijimas dėl vartotojų grupės apribojimų. Galima užregistruoti antrosios tiekėjo sąskaitos faktūros, kuri užpildo užsakytą kiekį, įsigijimą tik jei pirmosios tiekėjo sąskaitos faktūros įsigijimo operacija buvo jau įvesta ir jūs esate vartotojų grupės, kuriai leidžiama registruoti įsigijimus, narys.


Norėdami daugiau informacijos žr. [Ilgalaikio turto integravimas](fixed-asset-integration.md).




