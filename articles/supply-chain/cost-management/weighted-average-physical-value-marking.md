---
title: Svertinis vidurkis su faktine verte ir žymėjimu
description: Svertinis vidurkis yra atsargų modelis, pagrįstas svertinio vidurkio principu, kai išdavimas iš atsargų įvertinamas taikant vidutinę prekių, kurios gautos į atsargas atsargų uždarymo laikotarpiu, vertę, taip pat – visas iš ankstesnio laikotarpio turimas atsargas.
author: AndersGirke
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65501
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c124716b70be837573506a738ef2034397f2bda
ms.sourcegitcommit: addae271ddfc5a8b0721c23337f69916153db4cd
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/21/2022
ms.locfileid: "8330231"
---
# <a name="weighted-average-with-physical-value-and-marking"></a>Svertinis vidurkis su faktine verte ir žymėjimu

[!include [banner](../includes/banner.md)]

Svertinis vidurkis yra atsargų modelis, pagrįstas vidurkiu, kurį naudojant kiekvieno komponento (prekės operacijos) dauginimas pagal koeficientą (savikainą), atspindintį jo svarbą (kiekį). Kitas būdas tai padaryti yra tas, kad svertinis vidurkis yra atsargų modelis, kuris priskiria išdavimo operacijų išlaidas pagal vidutinę visų per laikotarpį gautų atsargų vertę bei visas iš ankstesnio laikotarpio gautas atsargas.

Kai atsargų uždarymą vykdote naudodami svertinio vidurkio atsargų modelį, yra du būdai, kaip galima kurti sudengimą. Paprastai visi gavimų apmokėjimai yra sudengiama prieš virtualų išdavimą, kuriame yra bendras gautas kiekis ir vertė. Šis virtualus išdavimas turi atitinkamą virtualų gavimą, iš kurio sudengiami išdavimai. Tokiu būdu visų išdavimų vidutinės išlaidos būna tokios pačios. Virtualų išdavimą ir gavimą galima matyti kaip virtualųjį perkėlimą, kuris vadinamas svertinio *vidurkio atsargų uždarymo perkėlavimu*. Šis sudengimo metodas vadinamas svertinio vidurkio *suvestinių sudengimų pavadinimu*. Jeigu yra tik vienas gavimas, visi išdavimai gali būti atlikti iš jo, ir nereikės kurti virtualaus perdavimo. Šis sudengimo metodas vadinamas tiesioginiu sudengimo *metodu*. Bet kurios turimos atsargos po atsargų uždarymo vertė apskaičiuojama taikant ankstesnio laikotarpio svertinį vidurkį ir įtraukiama į svertinio vidurkio skaičiavimą kitą laikotarpį.

Galite nepaisyti svertinio vidurkio principo, pažymėdami atsargų operacijas, kad konkrečios prekės gavimas būtų sudengtas su konkrečiu išdavimu. Rekomenduojama periodiškai uždaryti atsargas, kai naudojate svertinio vidurkio atsargų modelį sudengtims kurti ir problemų vertei koreguoti, atsižvelgiant į svertinio vidurkio principą. Kol jūs paleidžiate atsargų uždarymo procesą, išdavimo operacijos yra įvertintos pagal paleidžiamo vidurkio, kai įvyko faktiniai ir finansiniai atnaujinimai. Jei nenaudojate žymėjimo, vykdomasis vidurkis apskaičiuojamas, kai atliekamas faktinis arba finansinis atnaujinimas.

Svertinio vidurkio atsargų įkainojimo būdas apskaičiuojamas naudojant toliau nurodytą formulę.

- Svertinis vidurkis = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q *n* × P *n*\]) ÷ (Q1 + Q2 + Q *n*)

Q = operacijos kiekis  
P = operacijos kaina

Sudengimai yra atsargų uždarymo registravimas, per kurį išdavimai nustatomi pagal pataisytą svertinį vidurkį uždarymo datą. Pateiktame pavyzdyje parodytas svertinio vidurkio naudojimo su penkiomis skirtingomis konfigūracijomis poveikis:

- Svertinio vidurkio tiesioginis sudengimas be **pasirinkties Įtraukti faktinės** vertės
- Svertinio vidurkio suvestinis sudengimas be pasirinkties **Įtraukti fizinę** vertę
- Svertinio vidurkio tiesioginis sudengimas su pasirinktimi **Įtraukti fizinę** vertę
- Svertinio vidurkio suvestinis sudengimas su pasirinktimi **Įtraukti faktines** vertę
- Svertinis vidurkis su žymėjimu

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Svertinio vidurkio tiesioginis sudengimas neįtraukiant faktinės vertės

Tiesioginio sudengimo principas sukuria sudengimą tiesiogiai tarp gavimų ir gavimų, nesukuriant papildomų atsargų operacijų. Sistema naudoja tiesioginį sudengimo principą šiose situacijose:

- Per laikotarpį užregistruotas vienas gavimas ir vienas arba daugiau gavimų.
- Per laikotarpį buvo užregistruoti tik kvitai, o atsargose yra prekių nuo ankstesnio uždarymo.

Šiame pavyzdyje žymės langelis **Įtraukti fizinę** vertę išvalytas išleisto **produkto prekių** modelių grupėje. Toliau pateiktoje iliustracijoje parodytos šios operacijos.

- 1a. Faktinis atsargų gavimas, kai kiekis yra 10 o išlaidos – 10,00 USD už vienetą.
- 1b. Finansinis atsargų gavimas, kai kiekis yra 10 o išlaidos – 10,00 USD už vienetą.
- 2a. Faktinis atsargų gavimas, kai kiekis yra 10 o išlaidos – 20,00 USD už vienetą.
- 3a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 10.00 (finansiškai užregistruotų operacijų svertinis vidurkis).
- 3b. Finansinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 10.00 (finansiškai užregistruotų operacijų svertinis vidurkis).
- 4a. Faktinis atsargų išdavimas, kai kiekis yra 1 o išlaidos USD 10.00 vienetą (finansiškai užregistruotų operacijų svertinis vidurkis).
- 4b. Finansinis atsargų išdavimas, kai kiekis yra 1, vieneto kaina USD 10.00 vienetą (finansiškai užregistruotų operacijų s einamasis vidurkis).
- 5a. Faktinis atsargų išdavimas, kai kiekis yra 1 o išlaidos USD 10.00 vienetą (finansiškai užregistruotų operacijų svertinis vidurkis).
- 6\. Atsargų uždarymas atliktas. Remdamasi svertinio vidurkio metodu sistema naudoja tiesioginio sudengimo metodą, nes tik vienas gavimas finansiškai atnaujinamas tuo laikotarpiu. Šiame pavyzdyje vienas sudengimas sukuriamas tarp 1b ir 3b ir kitas tarp 1b ir 4b. Nėra koreguojama, nes einamasis vidurkis yra toks pat kaip svertinis vidurkis.

Toliau pateiktoje diagramoje parodyta **operacijų serija pasirinkus svertinio vidurkio atsargų modelį ir tiesioginio sudengimo principą be pasirinkties Įtraukti fizinę** vertę.

![Svertinio vidurkio duomenų apims be faktinės vertės įtraukti.](media/weighted-average-direct-settlement-without-include-physical-value.png)

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

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Svertinio vidurkio suvestinis sudengimas be pasirinkties Įtraukti faktinę vertę

Kai per laikotarpį yra keletas gavimų, svertinis vidurkis *naudoja suvestinio sudengimo principą, kai visi uždarymo laikotarpio gavimų suvestinė pateikiami operacijoje, kuri vadinama svertinio vidurkio atsargų uždarymu*. Visi laikotarpio gaviniai bus sudengti su naujai sukurtos atsargų operacijos išdavimu. Visi laikotarpio išduodami bus sudengti su naujos atsargų operacijos gavimu. Jei po atsargų uždarymo lieka turimų atsargų vertė, turimų atsargų vertė įtraukiama į svertinio vidurkio atsargų uždarymo operacijų gavimo operaciją.

Grafike parodytos šios operacijos:

- 1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
- 1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
- 2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
- 2b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 22,00 USD už vienetą.
- 3a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 16.00 (finansiškai užregistruotų operacijų svertinis vidurkis).
- 3b. Finansinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 16.00 (finansiškai užregistruotų operacijų svertinis vidurkis).
- 4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
- 5a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 5b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 6a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 23.00 (finansiškai užregistruotų operacijų svertinis vidurkis).
- 7\. Atsargų uždarymas atliktas.
- 7a. Svertinio vidurkio atsargų uždarymo operacijos finansinis išdavimas sukuriamas, siekiant susumuoti visų atsargų finansinių gavimų sudengimą.
  - 1b operacija sudengiama 1 kiekiui, kurio suma sudengta USD 10.00.
  - 2b operacija sudengiama 1 kiekiui, kurio suma sudengta USD 22.00.
  - 5b operacija sudengiama 1 kiekiui, kurio suma sudengta USD 30.00.
  - Operacija 7a. Sukurtas 3 kiekiui su sudengta USD 62.00. Ši operacija kompensuoja trijų gavimo operacijų, kurios finansiškai atnaujinamos per laikotarpį, sumą.
- 7b. Svertinio vidurkio atsargų uždarymo operacijos finansinis gavimas sukuriamas kaip finansiškai užregistruotų gavimų korespondentinė sąskaita.
  - 3b operacija sudengiama 1 kiekiui, kurio suma sudengta USD 20.67. Ši operacija koreguojama USD 4.67, kad pradinė laikotarpio vertė USD 16.00 20,67, kuri yra finansiškai užregistruotų laikotarpio operacijų svertinis vidurkis.
  - 7b operacija. Sukurtas 1 kiekiui su sudengta suma, USD 20.67 į 3b korespondentinę sąskaitą. Ši operacija koresponduos vienos išdavimo operacijos, kuri finansiškai atnaujinta per laikotarpį, sumą.

Toliau pateiktoje diagramoje parodyta operacijų serija pasirinkus svertinio vidurkio atsargų modelį **ir suvestinio sudengimo principą be pasirinkties Įtraukti fizinę** vertę.

![Svertinio vidurkio SS be faktinės vertės įtraukti.](media/weighted-average-summarized-settlement-without-include-physical-value.png)

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

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Svertinio vidurkio tiesioginis sudengimas su pasirinktimi Įtraukti faktinę vertę

Parametras **Įtraukti fizinę** vertę veikia kitaip, naudojant svertinio vidurkio atsargų modelį, nei ankstesnėse produkto versijose. Kai pasirenkate prekės **pasirinktį** **Įtraukti** fizinę vertę į prekių modelių grupės formą, sistema, skaičiuojant įvertintą išdavimo savikainą arba einamųjų vidurkį, naudos fiziškai atnaujintus gavimus. Išdavimai bus užregistruoti remiantis įvertinta laikotarpio savikaina. Uždarant atsargas finansiškai atnaujinti gavimai bus naudojami tik skaičiuojant svertinį vidurkį.

Grafike parodytos šios operacijos:

- 1a. Faktinis atsargų gavimas, kai kiekis yra 10 o išlaidos – 10,00 USD už vienetą.
- 1b. Finansinis atsargų gavimas, kai kiekis yra 10 o išlaidos – 10,00 USD už vienetą.
- 2a. Faktinis atsargų gavimas, kai kiekis yra 10 o išlaidos – 20,00 USD už vienetą.
- 3a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 15.00 (fiziškai ir finansiškai užregistruotų operacijų svertinė vidurkis).
- 3b. Finansinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 15.00 (faktiškai ir finansiškai užregistruotų operacijų svertinė vidurkis).
- 4a. Faktinis atsargų išdavimas, kai kiekis yra 1, vieneto kaina USD 15.00 vienetą (fiziškai ir finansiškai užregistruotų operacijų sąrangos vidurkis).
- 4b. Finansinis atsargų išdavimas, kai kiekis yra 1, vieneto kaina USD 15.00 vienetą (fiziškai ir finansiškai užregistruotų operacijų sąrangos vidurkis).
- 5a. Faktinis atsargų išdavimas, kai kiekis yra 1, vieneto kaina USD 15.00 vienetą (fiziškai ir finansiškai užregistruotų operacijų sąrangos vidurkis).
- 6\. Atsargų uždarymas atliktas. Remdamasi svertinio vidurkio metodu sistema naudoja tiesioginio sudengimo metodą, nes tik vienas gavimas finansiškai atnaujinamas tuo laikotarpiu. Šiame pavyzdyje vienas sudengimas sukuriamas tarp 1b ir 3b ir kitas tarp 1b ir 4b. Kiekviena operacija 3b ir 4b koreguojama -5,00 USD, kad vertė būtų USD 10.00.

Toliau pateiktoje diagramoje parodyta operacijų serija pasirinkus svertinio vidurkio atsargų modelį **ir tiesioginio sudengimo principą su pasirinktimi Įtraukti fizinę** vertę.

![Svertinio vidurkio duomenų su faktinės vertės įvertimi.](media/weighted-average-direct-settlement-with-include-physical-value.png)

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

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Svertinio vidurkio suvestinis sudengimas su pasirinktimi Įtraukti faktinę vertę

Parametras **Įtraukti fizinę vertę** veikia kitaip, naudojant svertinį vidurkį nei ankstesnėse versijose. Prekių modelių **grupės puslapyje** pažymėkite prekės žymės langelį Įtraukti **fizinę** vertę. Tada sistemoje skaičiuojant įvertintą savikainą arba paleidžiamąjį vidurkį bus naudojami faktiškai atnaujinti gavimai. Išdavimai bus užregistruoti remiantis įvertinta laikotarpio savikaina. Uždarant atsargas finansiškai atnaujinti gavimai bus naudojami tik skaičiuojant svertinį vidurkį. Naudojant svertinio vidurkio atsargų modelį, rekomenduojama kas mėnesį atlikti atsargų uždarymą. Šiame svertinio vidurkio suvestinio sudengimo pavyzdyje atsargų modelis pažymimas siekiant įtraukti faktinę vertę.

Grafike parodytos šios operacijos:

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
- 7\. Atsargų uždarymas atliktas.
- 7a. Svertinio vidurkio atsargų uždarymo operacijos finansinis išdavimas sukuriamas, siekiant susumuoti visų atsargų finansinių gavimų sudengimą.
  - 1b operacija sudengiama 1 kiekiui, kurio suma sudengta USD 10.00.
  - 2b operacija sudengiama 1 kiekiui, kurio suma sudengta USD 22.00.
  - 5b operacija sudengiama 1 kiekiui, kurio suma sudengta USD 30.00.
  - Operacija 7a. Sukurtas 3 kiekiui su sudengta USD 62.00.  
- 7b. Svertinio vidurkio atsargų uždarymo operacijos finansinis gavimas sukuriamas kaip finansiškai uždarytų išdavimo operacijų korespondentinė sąskaita.
  - 3b operacija sudengiama 1 kiekiui, kurio suma sudengta USD 20.67. Ši operacija koreguojama USD 4.67, kad pradinė laikotarpio vertė USD 16.00 20,67, kuri yra finansiškai užregistruotų laikotarpio operacijų svertinis vidurkis.
  - 7b operacija. Sukurtas 1 kiekiui su sudengta suma, USD 20.67 į 3b korespondentinę sąskaitą.

Toliau pateiktoje diagramoje parodyta operacijų serija pasirinkus svertinio vidurkio atsargų modelį **ir suvestinio sudengimo principą be pasirinkties Įtraukti fizinę** vertę.

![Svertinio vidurkio SS su faktinės vertės įtrauktimi.](media/weighted-average-summarized-settlement-with-include-physical-value.png)

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

## <a name="weighted-average-with-marking"></a>Svertinis vidurkis su žymėjimu

Žymėjimas yra procesas, leidžiantis susieti arba pažymėti išdavimo operaciją su gavimo operacija. Žymėjimą galima atlikti prieš arba po operacijos registravimo. Žymėjimą naudokite norėdami patikrinti tikslias uždarymo išlaidas užregistravus operaciją arba atlikus atsargų uždarymą.

Pavyzdžiui, jūsų Klientų aptarnavimo tarnyba priėmė skubų užsakymą iš svarbaus kliento. Kadangi tai yra skubus užsakymas, norėdami susisiekti su kliento pageidavimu, už šią prekę turėsite sumokėti daugiau. Jūs turite įsitikinti, kad šio pardavimo užsakymo sąskaitos faktūros atsargų elemento išlaidos arba parduotų prekių savikaina (PPK) yra pateikiama paraštėje.

Kai pirkimo užsakymas užregistruojamas, gaunama atsargų už 120,00 USD. Pvz., šis pardavimo užsakymo dokumentas pažymėtas prie pirkimo užsakymo prieš užregistruojant važtaraštį ar sąskaitą faktūrą. Tada PPK bus 120,00 USD – prekei nebus taikoma dabartinio slankiojo vidurkio kaina. Jeigu pardavimo užsakymo važtaraštis arba SF užregistruojami prieš žymėjimą, COGS bus užregistruota taikant slankiojo vidurkio savikainą.

Prieš atsargų uždarymą šias dvi operacijas dar galima žymėti kartu.

Gavimo operacija pažymima prie išdavimo operacijos. Tada bus nepaisoma prekės modelių grupėje pasirinkto vertinimo metodo ir sistema sudengs šias operacijas.

Galite pažymėti išdavimo operaciją su gavimu prieš užregistruodami operaciją. Tai galima atlikti iš pardavimo užsakymo eilutės puslapyje **Išsami pardavimo užsakymo informacija**. Atidarytos gavimo operacijos rodomos žymėjimo **puslapyje**.

Galite pažymėti išdavimo operaciją su gavimu užregistravę operaciją. Galite pažymėti išdavimo operaciją atvirai gavimo atsargose esančiai prekei iš registruoto atsargų koregavimo žurnalo.

Grafike parodytos šios operacijos:

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
- 6a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 23.00 (finansiškai užregistruotų operacijų svertinis vidurkis).
- 7\. Atsargų uždarymas atliktas. Remiantis žymėjimo principu, pagal kurį naudojamas svertinio vidurkio metodas, pažymėtos operacijos sudengimos viena su kita. Šiame pavyzdyje 3b sudengiama su 2b, o kurso koregavimas USD 6.00 užregistruojamas 3b, kad vertė būtų USD 22.00. Šiame pavyzdyje jokių papildomų sudengimų atlikti negalima, nes uždarymas sukuria tik finansiškai atnaujintų operacijų sudengimą.

Toliau pateiktoje diagramoje parodyta operacijų serija pasirinkus svertinio vidurkio atsargų modelį su žymėjimu.

![Svertinis vidurkis su žymėjimu.](media/weighted-average-with-marking.png)

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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
