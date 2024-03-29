---
title: Bendrojo planavimo nustatymo vedlys (yra vaizdo įrašas)
description: Šiame straipsnyje aprašoma, kaip paleisti bendrojo planavimo nustatymo vedlį, norint nustatyti bendrąjį planavimą.
author: t-benebo
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: a53dfd02ac2f42fd680eb71509dbd41214160f19
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066025"
---
# <a name="master-planning-setup-wizard"></a>Bendrojo planavimo sąrankos vedlys

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiamas bendrojo planavimo nustatymo **vedlio vadovas**. Jame paaiškinta, kaip apskaičiuojami parametrų pasiūlymai, taip pat pateikiami pavyzdžiai, parodantys, kaip skirtingos įmonės nustato bendrąjį planavimą pagal savo verslo poreikius.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3YnSB]

Bendrojo [planavimo nustatymo vedlys vaizdo įraše Dynamics 365 Supply Chain Management](https://youtu.be/c-e6n-8rZb4) (parodyta viršuje) yra įtrauktas į finansų [ir operacijų,](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) kurios galimos šiandien, sąrašą YouTube.


## <a name="specific-requirements-of-your-company"></a>Konkretūs jūsų įmonės reikalavimai

Pirmajame vedlio puslapyje klausiama apie konkrečius jūsų įmonės reikalavimus. Jūsų atsakymai į šiuos klausimus neturi būti tikslūs, tačiau turėtumėte pateikti apytikslį prekių ir planuojamų užsakymų skaičių, kuris bus skiriamas juridiniam subjektui. Jūsų atsakymai naudojami konfigūruojant juridiniam subjektui taikomus parametrus, o ne tik nustatant pasirinktą bendrąjį planą. Tolesniuose skyriuose aprašyti apskaičiuojami parametrai ir naudojamos formulės.

### <a name="number-of-threads"></a>Gijų skaičius

- **Jei įmonė gamina bet kokį skaičių elementų:** gijų skaičius = suplanuotų užsakymų skaičius ÷ 1 000
- **Jei įmonė negamina jokių elementų:** gijų skaičius = suplanuotų elementų skaičius ÷ 1 000

Jei apskaičiuotas gijų skaičius viršija 75 proc. turimų gijų skaičiaus, jis apribojamas 75 proc. kiekvieno kliento gijų skaičiaus. (Galimų gijų skaičius bus nustatytas kiekvienam pirkėjui.)

Daugiau informacijos žr. [Gijų skaičius](/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads).

### <a name="bundle-size"></a>Grupavimo dydis

Paketo dydis bus nustatytas į **1**. Ši reikšmė dažnai yra geriausia reikšmė, nes ji padeda padidinti bendrojo planavimo našumą.

Daugiau informacijos žr. [Pagalbinės priemonės užduočių skaičius užduočių pakete](/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle).

### <a name="firming-bundle-size"></a>Tvirtinamo paketo dydis

- **Jei gaminate kurį nors iš elementų:** tvirtinamo paketo dydis bus nustatytas į didesnę iš šių dviejų reikšmių: **10** ir paketo skaičiavimas
- **Jei negaminate jokių elementų:** tvirtinamo paketo dydis bus nustatytas į didesnę iš šių dviejų reikšmių: **50** ir paketo skaičiavimas

Paketo skaičiavimas = (suplanuotų užsakymų skaičius × (tvirtinimo laiko riba ÷ aprėpties laiko riba) ÷ gijų skaičius) ÷ 10

### <a name="cache-size"></a>Talpyklos dydis

Podėlio dydis bus nustatytas į **Maks.**. Ši reikšmė dažnai yra geriausia reikšmė, nes ji padeda padidinti bendrojo planavimo našumą.

Daugiau informacijos žr. [Laiko priskyrimas užduotims užduočių paketuose](/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle).

### <a name="manufacturing-setup"></a>Gamybos nustatymas

Jei gaminate prekes, vėliau bus rodomas vedlio puslapis **Gamybos nustatymai**.

## <a name="scope-of-the-current-plan"></a>Dabartinio plano aprėptis

Vedlio puslapyje **Dabartinio plano aprėptis** atsakote į klausimus, susijusius su tuo, kaip toli atsižvelgiama į būsimus reikalavimus ir skaičiuojamas bendrasis planas. Kiekvienu klausimu klausiama, ar norite naudoti funkciją ir kaip pageidaujate ją sukonfigūruoti.

Pvz., peržiūrint prognozės plano funkcija, vedlys klausia, „Ar norite naudoti prognozės planą bendrajam planui, kad siekiant įgyvendinti suplanuotą poreikį būtų siūlomi suplanuoti užsakymai?“

Galimos toliau nurodytos parinktys.

- **Ne** – bendrasis planavimas nesiūlys suplanuotų užsakymų, kad įgyvendintų prognozę. Skirtuke **Laiko ribos** puslapyje **Bendrieji planai** (**Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**), vedlys nustatys parinktį **Prognozės planas (laiko riba)** į **Taip**, tada nustatys dienų skaičių į **0** (nulį). Šis nustatymas pakeis laiko ribas, nurodytas aprėpties grupėje. Dienų skaičius nustatytas į **0** (nulį), todėl funkcija nebus naudojama.
- **Taip, kaip nurodyta šiame bendrajame plane** – tampa pasiekiamas laukas, kuriame galima įvesti skaičių dienų, kurias bendrasis planavimas pasiūlys suplanuotiems užsakymams siekiant įgyvendinti prognozuojamą paklausą. Vedlys nustatys parinktį **Prognozės planas (laiko riba)** į **Taip**, tada nustatys dienų skaičių į dienų skaičių, įvestą lauke **Prognozės planas** puslapio **Bendrieji planai** skirtuke **Laiko ribos**. Ši sąranka perrašys reikšmes, nustatytas aprėpties grupėse.
- **Taip, kaip apibrėžta aprėptyje** – vedlys nustatys parinktį **Prognozės planas (laiko riba)** į **Ne**. Aprėpties grupėje nurodytos laiko ribos bus naudojamos nurodyti, kiek laiko bus planuojama prognozė.

Likusiems klausimams šiame puslapyje ir jų atsakymams taikoma ta pati schema:

- **Ne** – parinktis **Prognozės planas (laiko ribos)** bus nustatyta į **Taip**, o dienų skaičius bus nustatytas į **0** (nulį).
- **Taip, kaip apibrėžta bendrajame plane** – parinktis **Prognozės planas (laiko riba)** bus nustatyta į **Taip**. Jūsų įvestas dienų skaičius bus naudojamas ir perrašys reikšmes, nustatytas aprėpties grupėse.
- **Taip, kaip apibrėžta aprėpties grupėje** – parinktis **Prognozės planas (laiko riba)** bus nustatyta į **Ne**.

Daugiau informacijos žr. [Užduočių planavimas](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="scheduling-options"></a>Planavimo parinktys

Puslapis **Planavimo parinktys** rodomas tik atsakius **Taip** į klausimą „Ar gaminate kurį nors iš planuojamų elementų?“ klausimas pirmame vedlio puslapyje spustelėkite.

Jūsų atsakymas į pirmąjį klausimą šiame puslapyje („Ar reikia planuoti operacijas, suskirstytas į atskiras užduotis?“) apibrėžia planavimo metodą skirtuko **Bendra** puslapyje **Bendrieji planai**.

- **Taip** – bus naudojamas užduočių planavimas.
- **Ne** – bus naudojamas operacijų planavimas.

Daugiau informacijos žr. [Operacijų planavimas](/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling) ir [Užduočių planavimas](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="updates-of-demand-and-supply"></a>Poreikio ir tiekimo atnaujinimai

Klausimai puslapyje **Paklausos ir pasiūlos naujinimai** susiję su tvirtinimais, veiksmų pranešimais ir vėlavimais.

Bendrojo planavimo nustatymas bus atnaujintas atsižvelgiant į jūsų atsakymus naudojant tą pačią schemą, kuri aprašyta ankstesniame skyriuje:

- **Ne** – parinktis **Laiko riba** puslapyje **Bendrieji planai** bus nustatyta į **Taip**, o dienų skaičius bus nustatytas į **0** (nulį).
- **Taip, kaip apibrėžta bendrajame plane** – parinktis **Laiko riba** bus nustatyta į **Taip**. Jūsų įvestas dienų skaičius bus naudojamas ir perrašys reikšmes, nustatytas aprėpties grupėse.
- **Taip, kaip apibrėžta aprėpties grupėje** – parinktis **Laiko riba** bus nustatyta į **Ne**.

Apskaičiuotiems atidėjimams jūsų atsakymai į klausimus vedlyje atnaujins atitinkamus parametrus puslapio **Bendrieji planai** skirtuke **Apskaičiuoti atidėjimai**.

## <a name="summary-of-your-changes"></a>Jūsų keitimų suvestinė

Paskutiniame vedlio puslapyje rodomi pakeitimai, kurie rekomenduojami pagal jūsų atsakymus. Rodoma reikšmė jūsų nustatyme (**Dabartinis nustatymas**) ir reikšmę, kurią rekomenduoja vedlys (**Nauja konfigūracija**).

Taip pat galite modifikuoti parametrus naujoje konfigūracijoje. Parametrai yra suskirstyti į parametrus, kurie taikomi jūsų juridiniam subjektui, ir parametrus, kurie taikomi tik jūsų pasirinkto bendrojo plano parametrams. Norėdami peržiūrėti visus nustatymo parametrus, kuriuos galima keisti naudojant vedlį, puslapio apačioje pasirinkite **Rodyti visus parametrus**. Tada galite keisti parametrus.

Galiausiai, pasirinkus **Baigti** bus taikoma nauja konfigūracija. Jei pasirinksite **Atšaukti**, jokie keitimai netaikomi.

## <a name="examples"></a>Pavyzdžiai

Šiame skyriuje aprašomas dviejų fiktyvių įmonių nustatymas, kad būtų galima parodyti, kaip nustatymai gali pasikeisti atsižvelgiant į kiekvienos įmonės poreikius.

### <a name="example-1-contoso-manufacturer"></a>1 pavyzdys: „Contoso Manufacturer“

„Contoso Manufacturer“ yra garsiakalbius gaminanti įmonė. Ji iš įvairių tiekėjų perka įvairias žaliavas ir komponentus, kurie naudojami garsiakalbių gamybai. Toliau pateikta kai kuri tiekimo ir gamybos informacija:

- Galutiniai elementai, kuriuos gamina įmonė, pasižymi KS struktūra.
- Visi galutiniai elementai ir komponentai planuojami pagal bendrąjį planavimą. Rankinis planavimas neatliekamas.
- Kiekvieno galutinio elemento gamybai apibrėžiamas operacijų maršrutas.
- Galutiniai elementai gaminami gamykloje. Joje yra apibrėžtas skaičius frezavimo ir gręžimo staklių, kurios naudojamos komponentams apdoroti. Šios mašinos apdoroja įvairius komponentus.
- Yra daug tiekėjų. Vidutinis elementų gamybos laikas yra viena savaitė. Elementų grupei iš to paties tiekėjo skirtas septynių savaičių vykdymo laikas.

Vedlyje „Contoso Manufacturer“ įvedamos šios reikšmės:

- **Aprėptis:**

    - **Klausimas:** „Ar norite nurodyti savo planavimo aprėpties dienų skaičių?“
    - **Atsakymas:** „Taip, kaip apibrėžta aprėpties grupėse“.

    Elementų gamybos laikas labai skiriasi, todėl „Contoso“ neprivalo planuoti visų būtinų to paties laikotarpio elementų. Sukuriamos elementų aprėpties grupės. Elementai, kurių gamybos laikas panašus, priskiriami tai pačiai aprėpties grupei. Kiekvienos aprėpties grupės (t. y. aprėpties laiko ribos) planavimo aprėptis yra maždaug gamybos laikas ir vienos savaitės marža. Tokiu atveju bendrasis planavimas užtikrina, kad elementai planuojami iš anksto pagal jų gamybos laiką.

    Todėl šiame pavyzdyje bus sukurtos dvi aprėpties grupės. Viena aprėpties grupė turės dviejų savaičių aprėpties laiko ribą, o kita – aštuonių savaičių aprėpties laiko ribą.

    Jeigu kaip atsakymas pasirenkama **Taip, kaip nurodyta šiame bendrajame plane**, įvedamas dienų skaičius turėtų viršyti ilgiausią visų elementų gamybos laiką. Kadangi daug elementų nėra būtina planuoti iš anksto, daug suplanuotų užsakymų bus apskaičiuojami, tačiau niekada nenaudojami. Todėl padidės bendrojo planavimo vykdymo laikas.

- **Planavimas:**

    - **Klausimas:** „Ar reikia planuoti operacijas, suskirstytas į atskiras užduotis?“
    - **Atsakymas:** „Taip“.

    „Contoso Manufacturing“ privalo planuoti atskiras užduotis, kurios bus atliekamos ceche. Todėl bus naudojamas užduočių planavimas.

- **Pajėgumas:**

    - **Klausimas:** „Ar norite planuoti naudodami išteklių pajėgumą?"
    - **Atsakymas:** „Taip, kaip apibrėžta šiame bendrajame plane.“ Įvedama **10 dienų**.

    Frezavimo ir gręžimo staklių skaičius yra ribotas. Planuojant gamybą būtina atsižvelgti į šį apribojimą ir laiku organizuoti užduotis atsižvelgiant į išteklių pajėgumą. Kitaip tariant, suplanuotos užduotys bus iš naujo planuojamos atsižvelgiant į išteklių apribojimus. Planavimo metu, be nustatyto laikotarpio, bus naudojamas gamybos laikas. (Suplanuoti gamybos užsakymai gali persidengti.) Elementų gamybos laikas yra septynios dienos, todėl bus atsižvelgiama į 10 dienų bendrojo planavimo išteklių pajėgumą.

- **Seka:**

    - **Klausimas:** „Ar norite nustatyti suplanuotų užsakymų seką naudodami produkto sekos reikšmes?“
    - **Atsakymas:** „Taip, kaip apibrėžta aprėpties grupėse“.

    Kiekvieno galutinio elemento gamybai apibrėžiamas maršrutas. Todėl atliekant bendrąjį planavimą užsakymai bus planuojami laiku atsižvelgiant į apibrėžtus maršrutus.

- **Išskleidimas:**

    - **Klausimas:** „Ar norite planuoti užsakymus visiems KS elementams (planas, skirtas pirminiams ir visiems antriniams elementams)?“
    - **Atsakymas:** „Taip, kaip apibrėžta aprėpties grupėse“.

    Būtina planuoti visus gamybai naudojamus elementus. Elementai pasižymi labai skirtingais gamybos laikais, todėl bendrasis planavimas bus efektyvesnis naudojant aprėpties grupes. Vėlgi, galima įvesti vienos savaitės maržą, o išskleidimą atlikti tokiam pačiam laikotarpiui, kaip aprėptis.

### <a name="example-2-contoso-retailer"></a>2 pavyzdys: „Contoso Retailer“

„Contoso Retailer“ yra platinimo įmonė, veikianti mados pramonės srityje. Ji naudoja bendrąjį planavimą, kad apskaičiuotų, kada turėtų būti pateikiami pirkimo užsakymai, atsižvelgiant į prognozuojamus pardavimus. Štai keletas įmonės ypatybių:

- „Contoso Retailer“ pardavimams prognozuoti naudoja poreikio prognozę. Pirkimo užsakymai bus planuojami atsižvelgiant į prognozę.
- Parduotuvės papildymui naudoja rekvizitus.
- Visų elementų vykdymo laikas iš pagrindinio sandėlio į kiekvieną parduotuvę yra maždaug dvi savaitės.

Vedlyje „Contoso Retailer“ įvedamos šios reikšmės:

- **Poreikio prognozė:**

    - **Klausimas:** „Ar norite naudoti prognozės planą bendrojo planavimo metu, kad suplanuoti užsakymai būtų siūlomi atsižvelgiant į prognozuojamą paklausą?”
    - **Atsakymas:** „Taip, kaip apibrėžta šiame bendrajame plane.“

    „Contoso“ įtraukė poreikio prognozę, kad galėtų prognozuoti pardavimus. Todėl bendrasis planavimas turi rekomenduoti suplanuotus užsakymus, kad įvykdytų prognozę.

- **Tvirtinimas:**

    - **Klausimas:** „Ar norite, kad bendrasis planavimas automatiškai patvirtintų suplanuotus užsakymus į užsakymo dokumentus, pvz., gamybos ar pirkimo užsakymus?“
    - **Atsakymas:** „Taip, kaip apibrėžta šiame bendrajame plane.“ Įdedama **1 diena**.

    „Contoso Retailer“ sukurs pirkimo užsakymus tiesiogiai iš suplanuotų pirkimo užsakymų, todėl būtų patogu, jeigu suplanuoti pirkimo užsakymai būtų automatiškai patvirtinami. Kiekvieną dieną įmonė vykdo bendrąjį planavimą, todėl vienos dienos tvirtinimo laiko riba automatiškai patvirtins visus užsakymus, būtinus kitai dienai.

- **Patvirtintos paraiškos:**

    - **Klausimas:** „Ar norite įtraukti poreikį iš patvirtintų paraiškų, kad būtų papildytos mažmeninės prekybos parduotuvės?“
    - **Atsakymas:** „Taip, kaip apibrėžta šiame bendrajame plane.“ Įdedama **1 diena**.

    „Contoso“ naudoja patvirtintas savo parduotuvių paraiškas, kad sukurtų planuojamus pirkimo užsakymus ir papildytų tas parduotuves. Bendrasis planavimas vykdomas kiekvieną dieną, todėl paraiškos iš paskutinės dienos bus įtrauktos į planavimą.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
