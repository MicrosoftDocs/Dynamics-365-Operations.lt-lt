---
title: Svertinio vidurkio data su faktinės vertės įtraukimu ir žymėjimu
description: Svertinio vidurkio data yra atsargų modelis, pagrįstas svertinio vidurkio principu, kai atsargų išdavimai vertinami naudojant vidutinę prekių, gautų į atsargas kiekvieną atskirą atsargų uždarymo laikotarpio dieną, vertę.
author: AndersGirke
ms.date: 03/04/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28991
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3cf2206863d891eceb9c65ff879da3f9f72032b1
ms.sourcegitcommit: fcded93fc6c27768a24a3d3dc5cc35e1b4eff22b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/07/2022
ms.locfileid: "8392006"
---
# <a name="weighted-average-date-with-include-physical-value-and-marking"></a>Svertinio vidurkio data su faktinės vertės įtraukimu ir žymėjimu

[!include [banner](../includes/banner.md)]

*Svertinio vidurkio* data yra atsargų modelis, pagrįstas vidurkiu, kuris apskaičiuojamas padauginant kiekvieną komponentą (prekės operaciją) iš koeficiento (savikainos), kuris atspindi jo svarbą (kiekį) kiekvieną laikotarpio dieną. Kitaip tariant, šis atsargų modelis priskiria išdavimo operacijų išlaidas pagal kiekvienos dienos gautų atsargų ir kiekvienos dienos turimų atsargų vidutinė vertę.

Kai atsargų uždarymas vykdomas naudojant svertinio vidurkio datos atsargų modelį, sudengti galima naudoti du metodus. Paprastai visi gavimų apmokėjimai yra sudengiama prieš virtualų išdavimą, kuriame yra bendras gautas kiekis ir vertė. Šis virtualus išdavimas turi atitinkamą virtualų gavimą, pagal kurį išdavimai yra sudengti. Tokiu būdu visi problemos kiekvieną dieną gauna tą pačią vidutinę kainą. Virtualus išdavimas ir virtualus gavimas gali būti laikomas virtualiu perkėlavimu. Šis virtualus perkėlimas vadinamas svertinio vidurkio *atsargų uždarymo perkėlu*. Dėl to šis sudengimo metodas žinomas kaip svertinio vidurkio *suvestinis sudengimas*. Jei yra tik vienas gavimas, visi gavimų sudengti galima iš jo ir nebus sukurtas virtualusis perkėlimas. Šis sudengimo metodas vadinamas tiesioginiu sudengimo *metodu*. Bet kurios turimos atsargos po atsargų uždarymo vertė apskaičiuojama taikant svertinį vidurkį, pateisėjusį nuo paskutinės ankstesnio laikotarpio dienos, ir įtraukiamos skaičiuojant svertinio vidurkio datą kitame laiko periode.

Galite nepaisyti svertinio vidurkio datos principo, pažymėdami atsargų operacijas, kad konkrečios prekės gavimas būtų sudengtas su konkrečiu išdavimu. Kai naudojate svertinio vidurkio datos atsargų modelį sudengti ir koreguoti išdavimo vertę, naudodami svertinio vidurkio datos principą, reikia periodiškai uždaryti atsargas. Kol uždarysite atsargų uždarymą, išdavimo operacijos bus įvertintos pagal paleidžiamo vidurkio vertę, kai įvyko faktiniai ir finansiniai atnaujinimai. Jei nenaudojate žymėjimo, vykdomasis vidurkis apskaičiuojamas, kai atliekamas faktinis arba finansinis atnaujinimas.

Svertinio vidurkio datos atsargų įkainojimo metodas apskaičiuojamas kiekvieną dieną naudojant šią formulę:

*Išlaidos* = \[ (*Qb*<sub>*·*</sub> × *Pb*<sub>*·*</sub>) + &#x2211;<sub>*n*</sub>(*Qn*<sub>*·*</sub> × *Pn*<sub>*·*</sub>)\] ÷ (*Qb*<sub>*·*</sub> + &#x2211;<sub>*nQn)*</sub>*·*<sub>*·*</sub>

- *Q* = Operacijos kiekis
- *P* = Operacijos kaina

Kitaip tariant, svertinio vidurkio išlaidos yra lygios pradžios kiekiui, gautame už pradžios kainą, pridėjus kiekvieno gavimo kiekio sumą, kuri didesnė už gavimo kainą, visas jos padalintos iš pradžios kiekio ir gavimo kiekių sumos.

Uždarant atsargas, skaičiuojama kiekvieną dieną uždarymo laikotarpiu.

> [!NOTE]
> Daugiau informacijos apie sudengimą ieškokite Atsargų [uždarymas](inventory-close.md).

Toliau pateikti pavyzdžiai rodo svertinio vidurkio datos naudojimo su penkiomis konfigūracijoje poveikį:

- Svetinio vidurkio dienos tiesioginis sudengimas be pasirinkties **Įtraukti faktinę vertę**
- Svetinio vidurkio dienos apibendrintas atsikaitymas, **Įtraukti faktinę vertę** parinktis nenaudojama
- Svetinio vidurkio dienos tiesioginis sudengimas su pasirinktimi **Įtraukti faktinę vertę**
- Svertinio vidurkio dienos suvestinis sudengimas su pasirinktimi **Įtraukti faktinę vertę**
- Svertinio vidurkio diena su žymėjimu

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Svetinio vidurkio dienos tiesioginis sudengimas be pasirinkties Įtraukti faktinę vertę

Tiesioginio sudengimo principas sukuria sudengimą tiesiogiai tarp gavimų ir gavimų, nesukuriant papildomų atsargų operacijų. Sistema naudoja tiesioginį sudengimo principą šiose situacijose:

- Per laikotarpį užregistruotas vienas gavimas ir vienas arba daugiau gavimų.
- Per laikotarpį buvo užregistruoti tik išdavimai, o atsargose yra prekių nuo ankstesnio uždarymo.

Šiame pavyzdyje žymės langelis **Įtraukti fizinę** vertę išvalytas išleisto **produkto prekių** modelių grupės puslapyje. Toliau pateiktoje diagramoje parodytos šios operacijos:

**1 diena**

- 1a. Faktinis atsargų gavimas, kai kiekis yra 10 o išlaidos – 10,00 USD už vienetą.
- 1b. Finansinis atsargų gavimas, kai kiekis yra 10 o išlaidos – 10,00 USD už vienetą.
- 2a. Faktinis atsargų gavimas, kai kiekis yra 10 o išlaidos – 20,00 USD už vienetą.
- 3a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 10.00 (finansiškai užregistruotų operacijų svertinis vidurkis).
- 3b. Finansinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 10.00 (finansiškai užregistruotų operacijų svertinis vidurkis).

**2 diena**

- 4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
- 5a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 5b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 6a. Finansinis atsargų išdavimas, kai kiekis yra 1, vieneto kaina USD 20.00 (finansiškai užregistruotų operacijų svertinis vidurkis).

**3 diena**

- 7\. Atsargų uždarymas atliktas. Remdamasi svertinio vidurkio datos metodu sistema naudoja tiesioginio sudengimo metodą gruodžio 30 d. (12/30), nes tik vienas gavimas finansiškai atnaujintas 12/30. Šiame pavyzdyje sukuriamas vienas sudengimas tarp 1b ir 3b operacijų. Kurso koregavimas USD 10.00 kad operacijos vertė 3b būtų atiduoda iki 20,00. Gruodžio 31 d. (12/31) atliktas joks koregavimas ar sudengimas, nes nėra finansiškai atnaujintų problemų 12/31.

Toliau pateiktoje diagramoje rodoma ši **operacijų serija ir svertinio vidurkio atsargų modelio naudojimo poveikis bei tiesioginio sudengimo principas be pasirinkties Įtraukti fizinę** vertę.

![Svetinio vidurkio datos tiesioginis sudengimas be pasirinkties Įtraukti faktinę vertę.](media/weighted-average-date-direct-settlement-without-include-physical-value.png)

**Diagramos raktas:**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Faktinės operacijos žymimos trumpesniomis pilkomis rodyklėmis.
- Finansinės operacijos rodo ilgesniomis juodomis rodyklėmis.
- Atsargų gaviniai pateikiami vertikaliomis rodyklėmis virš ašies.
- Atsargų problemos vaizduojamos vertikaliomis rodyklėmis po ašimi.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Datos atskiriamos siauromis juoda vertikaliomis eilutėmis. Datos rodomos diagramos apačioje.
- Atsargų uždarymai vaizduojami raudonomis vertikaliomis punktyrine eilutėmis.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Svetinio vidurkio dienos apibendrintas sudengimas be pasirinkties Įtraukti faktinę vertę

Kai per laikotarpį yra keletas gavimų, svertinio vidurkio data naudoja suvestinio sudengimo principą, *kur visi vienos dienos gavimų suvestinė pateikiami operacijoje, kuri vadinama svertinio vidurkio atsargų uždarymu*. Visi tos dienos gaviniai bus sudengti pagal naujai sukurtos atsargų operacijos išdavimą. Visi tos dienos gaviniai bus sudengti pagal naujos atsargų operacijos gavimą. Jei po atsargų uždarymo lieka turimų atsargų vertė, turimų atsargų vertė įtraukiama į svertinio vidurkio atsargų uždarymo operacijų gavimo operaciją.

Toliau pateiktoje diagramoje parodytos šios operacijos:

**1 diena**

- 1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
- 1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
- 2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
- 2b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 22,00 USD už vienetą.
- 3a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 16.00 (finansiškai užregistruotų operacijų svertinis vidurkis).
- 3b. Finansinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 16.00 (finansiškai užregistruotų operacijų svertinis vidurkis).

**2 diena**

- 4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
- 5a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 5b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 6a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 23.00 (finansiškai užregistruotų operacijų svertinis vidurkis).

**3 diena**

- 7\. Atsargų uždarymas atliktas.
- 7a. Svertinio vidurkio atsargų uždarymo operacijos finansinis išdavimas sukuriamas, siekiant susumuoti visų atsargų finansinių gavimų sudengimą.

    - 1b operacija sudengiama 1 kiekiui, kurio sudengta suma USD 10.00.
    - 2b operacija sudengiama 1 kiekiui, kurio sudengta suma USD 22.00.
    - Operacija 7a sukuriama 2 kiekiui, kurio sudengta suma yra USD 32.00. Ši operacija kompensuoja dviejų gavimo operacijų, kurios finansiškai atnaujinamos per laikotarpį, sumą.

- 7b. Svertinio vidurkio atsargų uždarymo operacijos finansinis gavimas sukuriamas kaip finansiškai užregistruotų gavimų korespondentinė sąskaita.

    - 3b operacija sudengiama 1 kiekiui, kurio sudengta suma USD 16.00. Ši operacija nėra koreguojama, nes ji yra finansiškai užregistruotų operacijų svertinis vidurkis gruodžio 1 d. (12/1).
    - 7b operacija sukuriama 2 kiekiui, kurio finansinė suma USD 32.00, ir sudengta USD 16.00 į 3b korespondentinę operaciją. Ši operacija koresponduos vienos išdavimo operacijos, kuri finansiškai atnaujinta per laikotarpį, sumą. Operacija lieka atvira, nes dar yra viena jos dalis.

Toliau pateiktoje diagramoje rodoma ši operacijų serija ir svertinio vidurkio atsargų modelio naudojimo poveikis bei suvestinio sudengimo principas, **tačiau nenaudojant pasirinkties Įtraukti fizinę vertę**.

![Svertinio vidurkio datos suvestinis sudengimas be pasirinkties Įtraukti faktinę vertę.](media/weighted-average-date-summarized-settlement-without-include-physical-value.png)

**Diagramos raktas:**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Faktinės operacijos žymimos trumpesniomis pilkomis rodyklėmis.
- Finansinės operacijos rodo ilgesniomis juodomis rodyklėmis.
- Atsargų gaviniai pateikiami vertikaliomis rodyklėmis virš ašies.
- Atsargų problemos vaizduojamos vertikaliomis rodyklėmis po ašimi.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Datos atskiriamos siauromis juoda vertikaliomis eilutėmis. Datos rodomos diagramos apačioje.
- Atsargų uždarymai vaizduojami raudonomis vertikaliomis punktyrine eilutėmis.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Svetinio vidurkio dienos tiesioginis sudengimas su pasirinktimi Įtraukti faktinę vertę

Dabartinėje produkto versijoje pasirinktis **Įtraukti** fizinę vertę veikia kitaip, nei svertinio vidurkio datos atsargų modelis, nei jis dirbo ankstesnėse versijose. Kai **pasirenkate** **žymės** langelį Įtraukti fizinę vertę prekei prekių modelių grupės puslapyje, sistema naudos fiziškai atnaujintus gavimus, skaičiuodama įvertintą išdavimo savikainą arba einammąjį vidurkį. Išdavimai bus užregistruoti remiantis įvertinta laikotarpio savikaina. Uždarant atsargas finansiškai atnaujinti gavimai bus naudojami tik skaičiuojant svertinį vidurkį.

Toliau pateiktoje diagramoje parodytos šios operacijos:

**1 diena**

- 1a. Faktinis atsargų gavimas, kai kiekis yra 10 o išlaidos – 10,00 USD už vienetą.
- 1b. Finansinis atsargų gavimas, kai kiekis yra 10 o išlaidos – 10,00 USD už vienetą.
- 2a. Faktinis atsargų gavimas, kai kiekis yra 10 o išlaidos – 20,00 USD už vienetą.
- 3a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 15.00 (fiziškai ir finansiškai užregistruotų operacijų svertinė vidurkis).
- 3b. 1 vieneto, kurio savikaina 1, finansinis išdavimas iš atsargų (USD 15.00 faktiškai ir finansiškai užregistruotų operacijų sąrangos vidurkis).

**2 diena**

- 4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
- 5a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 5b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 6a. Faktinis atsargų išdavimas, kai kiekis yra 1, vieneto kaina USD 21.25 vienetą (fiziškai ir finansiškai užregistruotų operacijų sąrangos vidurkis).

**3 diena**

- 7\. Atsargų uždarymas atliktas. Remdamasi svertinio vidurkio datos metodu sistema naudoja tiesioginio sudengimo metodą gruodžio 30 d. (12/30), nes tik vienas gavimas finansiškai atnaujintas 12/30. Šiame pavyzdyje sukuriamas vienas sudengimas tarp 1b ir 3b operacijų. Išdavimas koregavimas atliktas 12/30. Be to, gruodžio 31 d. (12/31) atliktas joks koregavimas ar sudengimas, nes nėra finansiškai atnaujintų problemų 12/31.

Toliau pateiktoje diagramoje rodoma ši operacijų serija ir svertinio vidurkio atsargų modelio naudojimo poveikis bei tiesioginio sudengimo principas su **pasirinktimi Įtraukti fizinę** vertę.

![Svertinio vidurkio tiesioginis sudengimas su faktinės vertės įvertį.](media/weighted-average-date-direct-settlement-with-include-physical-value.png)

**Diagramos raktas:**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Faktinės operacijos žymimos trumpesniomis pilkomis rodyklėmis.
- Finansinės operacijos rodo ilgesniomis juodomis rodyklėmis.
- Atsargų gaviniai pateikiami vertikaliomis rodyklėmis virš ašies.
- Atsargų problemos vaizduojamos vertikaliomis rodyklėmis po ašimi.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Datos atskiriamos siauromis juoda vertikaliomis eilutėmis. Datos rodomos diagramos apačioje.
- Atsargų uždarymai vaizduojami raudonomis vertikaliomis punktyrine eilutėmis.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Svertinio vidurkio dienos suvestinis sudengimas su pasirinktimi Įtraukti faktinę vertę

Dabartinėje produkto versijoje pasirinktis **Įtraukti** fizinę vertę veikia kitaip nei naudojant svertinį vidurkį, nei naudojant ankstesnes versijas. Kai **pasirenkate** **žymės** langelį Įtraukti fizinę vertę prekei prekių modelių grupės puslapyje, sistema, skaičiuodama įvertintą savikainą arba einammąjį vidurkį, naudos fiziškai atnaujintus gavimus. Išdavimai bus užregistruoti remiantis įvertinta laikotarpio savikaina. Uždarant atsargas finansiškai atnaujinti gavimai bus naudojami tik skaičiuojant svertinį vidurkį. Naudojant svertinio vidurkio atsargų modelį, rekomenduojama kas mėnesį atlikti atsargų uždarymą. Šiame svertinio vidurkio datos suvestinio sudengimo pavyzdyje atsargų modelis pažymimas siekiant įtraukti fizinę vertę.

Toliau pateiktoje diagramoje parodytos šios operacijos:

**1 diena**

- 1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
- 1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
- 2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
- 2b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 22,00 USD už vienetą.
- 3a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 16.00 (fiziškai ir finansiškai užregistruotų operacijų sąrangos vidurkis).
- 3b. Finansinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 16.00 (faktiškai ir finansiškai užregistruotų operacijų svertinė vidurkis).

**2 diena**

- 4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
- 5a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 5b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 6a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 23.67 (faktiškai ir finansiškai užregistruotų operacijų svertinė vidurkis).

**3 diena**

- 7\. Atsargų uždarymas atliktas.
- 7a. Svertinio vidurkio atsargų uždarymo operacijos finansinis išdavimas sukuriamas, siekiant susumuoti visų atsargų finansinių gavimų sudengimą.

    - 1b operacija sudengiama 1 kiekiui, kurio sudengta suma USD 10.00.
    - 2b operacija sudengiama 1 kiekiui, kurio sudengta suma USD 22.00.
    - Operacija 7a sukuriama 2 kiekiui, kurio sudengta suma yra USD 32.00. Ši operacija kompensuoja dviejų gavimo operacijų, kurios finansiškai atnaujinamos per laikotarpį, sumą.

- 7b. Svertinio vidurkio atsargų uždarymo operacijos finansinis gavimas sukuriamas kaip finansiškai užregistruotų gavimų korespondentinė sąskaita.

    - 3b operacija sudengiama 1 kiekiui, kurio sudengta suma USD 16.00. Ši operacija nėra koreguojama, nes ji yra finansiškai užregistruotų operacijų svertinis vidurkis gruodžio 1 d. (12/1).
    - 7b operacija sukuriama 2 kiekiui, kurio finansinė suma USD 32.00, ir sudengta USD 16.00 į 3b korespondentinę operaciją. Ši operacija koresponduos vienos išdavimo operacijos, kuri finansiškai atnaujinta per laikotarpį, sumą. Operacija lieka atvira, nes dar yra viena jos dalis.

Toliau pateiktoje diagramoje rodoma ši **operacijų serija ir svertinio vidurkio atsargų modelio naudojimo poveikis bei suvestinio sudengimo principas be pasirinkties Įtraukti fizinę** vertę.

![Svertinio vidurkio suvestinis sudengimas su faktinės vertės įtraukiant.](media/weighted-average-date-summarized-settlement-with-include-physical-value.png)

**Diagramos raktas:**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Faktinės operacijos žymimos trumpesniomis pilkomis rodyklėmis.
- Finansinės operacijos rodo ilgesniomis juodomis rodyklėmis.
- Atsargų gaviniai pateikiami vertikaliomis rodyklėmis virš ašies.
- Atsargų problemos vaizduojamos vertikaliomis rodyklėmis po ašimi.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Datos atskiriamos siauromis juoda vertikaliomis eilutėmis. Datos rodomos diagramos apačioje.
- Atsargų uždarymai vaizduojami raudonomis vertikaliomis punktyrine eilutėmis.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

## <a name="weighted-average-date-when-marking-is-used"></a>Svertinio vidurkio diena su žymėjimu

Žymėjimas yra procesas, leidžiantis susieti arba pažymėti išdavimo operaciją su gavimo operacija. Žymėjimą galima atlikti prieš arba po operacijos registravimo. Žymėjimą galima naudoti norint sužinoti tikslią atsargų kainą registruojant operaciją arba atliekant atsargų uždarymą.

Pavyzdžiui, jūsų Klientų aptarnavimo tarnyba priėmė skubų užsakymą iš svarbaus kliento. Kadangi tai yra skubus užsakymas, už šią prekę turėsite sumokėti daugiau, kad galėtumėte susisiekti su kliento pageidavimu. Turite būti tikri, kad šio pardavimo užsakymo SĄSKAITOS faktūros atsargų prekės kaina arba parduotų prekių savikaina (PPS) yra pateikta paraštėje.

Kai pirkimo užsakymas užregistruojamas, gaunama atsargų už 120,00 USD. Jei pardavimo užsakymo dokumentas pažymėtas prie pirkimo užsakymo prieš užregistruojant važtaraštį arba SF, COGS bus USD 120.00 vietoj dabartinio einamosios prekės vidurkio išlaidų. Jeigu žymėjimas įvyksta po to, kai užregistruojamas pardavimo užsakymo važtaraštis arba SF, COGS bus užregistruota pagal slykamo vidurkio savikainą.

Prieš atsargų uždarymą šias dvi operacijas dar galima žymėti kartu.

Jei gavimo operacija pažymėta išdavimo operacijai, bus nepaisoma prekės modelių grupei pasirinkto vertinimo būdo ir sistema sudengs šias operacijas.

Galite pažymėti išdavimo operaciją su gavimu prieš užregistruodami operaciją. Šį žymėjimą galima atlikti pardavimo užsakymo informacijos puslapyje žymint **pardavimo užsakymo** eilutę. Atidarytos gavimo operacijos rodomos žymėjimo **puslapyje**.

Taip pat galite pažymėti išdavimo operaciją su gavimu užregistravę operaciją. Galite pažymėti išdavimo operaciją atvirai gavimo atsargose esančiai prekei iš registruoto atsargų koregavimo žurnalo.

Toliau pateiktoje diagramoje parodytos šios operacijos:

**1 diena**

- 1a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 10,00 USD už vienetą.
- 1b. 1 vieneto, kurio kaina 10,00 USD, finansinis gavimas į atsargas.
- 2a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 20,00 USD už vienetą.
- 2b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 22,00 USD už vienetą.
- 3a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 16.00 (finansiškai užregistruotų operacijų svertinis vidurkis).
- 3b. Finansinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 16.00 (finansiškai užregistruotų operacijų svertinis vidurkis).
- 3c. 3b operacijos atsargų finansinis išdavimas yra pažymėtas kaip 2b operacijos atsargų finansinis išdavimas.

**2 diena**

- 4a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 25,00 USD už vienetą.
- 5a. Faktinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 5b. Finansinis atsargų gavimas, kai kiekis yra 1 o išlaidos – 30,00 USD už vienetą.
- 6a. Faktinis atsargų išdavimas, kai kiekis yra 1, o vieneto savikaina USD 23.00 (finansiškai užregistruotų operacijų svertinis vidurkis).

**3 diena**

- 7\. Atsargų uždarymas atliktas. Remiantis žymėjimo principu, pagal kurį naudojamas svertinio vidurkio metodas, pažymėtos operacijos sudengimos viena su kita. Šiame pavyzdyje 3b operacija sudengiama su 2b operacija, o operacijų koregavimas USD 6.00 užregistruotas 3b operacijoje, kad vertė būtų USD 22.00. Šiame pavyzdyje jokių papildomų sudengimų atlikti negalima, nes uždarymas sukuria tik finansiškai atnaujintų operacijų sudengimą.

Toliau pateiktoje diagramoje parodyta operacijų serija ir svertinio vidurkio atsargų modelio naudojimo su žymėjimu poveikis.

![Svertinis vidurkis su žymėjimu.](media/weighted-average-date-with-marking.png)

**Diagramos raktas:**

- Atsargų operacijos parodomos vertikaliomis rodyklėmis.
- Faktinės operacijos žymimos trumpesniomis pilkomis rodyklėmis.
- Finansinės operacijos rodo ilgesniomis juodomis rodyklėmis.
- Atsargų gaviniai pateikiami vertikaliomis rodyklėmis virš ašies.
- Atsargų problemos vaizduojamos vertikaliomis rodyklėmis po ašimi.
- Kiekviena nauja gavimo arba išdavimo operacija pažymima nauja žyme.
- Kiekviena vertikali rodyklė yra pažymėta sekos identifikatoriumi, pvz., *1a*. Identifikatoriai rodo atsargų operacijų registracijos laiko juostoje tvarką.
- Datos atskiriamos siauromis juoda vertikaliomis eilutėmis. Datos rodomos diagramos apačioje.
- Atsargų uždarymai vaizduojami raudonomis vertikaliomis punktyrine eilutėmis.
- Iki atsargų uždarymo atlikti sudengimai rodomi raudonomis įstrižomis punktyrinėmis rodyklėmis, einančiomis nuo gavimo prie išdavimo.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
