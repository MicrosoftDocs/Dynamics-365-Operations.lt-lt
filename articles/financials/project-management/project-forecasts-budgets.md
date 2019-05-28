---
title: Projektų prognozės ir biudžetai
description: „Microsoft Dynamics 365 for Finance and Operations“ pateikiamos projekto prognozės ir biudžetai, skirti projektams tvarkyti ir kontroliuoti.
author: KimANelson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 530a2717427c540d80509c4862e6fb8ea7c5694a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556534"
---
# <a name="project-forecasts-and-budgets"></a>Projektų prognozės ir biudžetai

[!include [banner](../includes/banner.md)]

„Microsoft Dynamics 365 for Finance and Operations“ pateikiami du projektų tvarkymo ir kontroliavimo būdai: projektų prognozės ir projektų biudžetai. 

Projektų prognozavimą naudokite, jei jūsų organizacija turi veiklos perspektyvą ir jei ji pagrindinį dėmesį skiria įplaukoms ir išlaidoms, gaunamoms iš konkrečių operacijų. Projektų biudžeto sudarymą naudokite, jei jūsų organizacija daugiau dėmesio skiria finansinėms sumoms. 

Tiek projektų prognozės, tiek projektų biudžetai išlaikyti numatomoms operacijų sumoms naudoja prognozių modelius. 

Kiekvienas metodas turi savų privalumų. Prieš savo organizacijai parinkdami metodą, turėtumėte atsižvelkite į toliau nurodytus dalykus.

|                           |                                          |                                                    |
|---------------------------|------------------------------------------|----------------------------------------------------|
|                           | **Projektų prognozavimas**                  | **Projektų biudžetų sudarymas**                              |
| **Laikotarpių paskirstymas**     | Negalima tiesiogiai paskirstyti operacijų ataskaitiniam laikotarpiui. Vietoj to, prognozė ir prognozės kontrolė paremtos projekto trukme. Kadangi prognozės paremtos konkrečia data, laikotarpį turite numatyti iš datos. | Operacijas galite paskirstyti visam projektui arba ataskaitiniam laikotarpiui. Jei paskirstote laikotarpiui, nepanaudotas sumas galite perkelti į kitą ataskaitinį laikotarpį. |
| **Operacijų peržiūra**  | Peržiūrėti operacijas galite prognozių formose, kuriose galite matyti visos įmonės ir visų projektų prognozes, nepaisant hierarchijos. Norėdami dėmesį sutelkti į konkretų projektą, turite filtruoti duomenis.                                       | Galite peržiūrėti vienos projekto hierarchijos biudžeto operacijas. Todėl galite peržiūrėti pirminio projekto arba jo subprojektų operacijų informaciją.                 |
| **Operacijų kintamieji** | Įvesdami prognozių operacijas, galite naudoti kiekvieną esamą faktinės operacijos atributą. Taip galima prognozę padaryti išsamesnę. Pavyzdžiui, galite įvesti kiekių, darbuotojų, prekių ar eilučių ypatybių informaciją.         | Įvesdami biudžeto informaciją, naudoti galite tik sumas, kategorijas ir veiklas.                    |
| **Sauga**              | Prognozavimas paremtas operacijomis, kurias įvedate prognozių formose, ir nėra jokio jo procesų kontrolės mechanizmo. Bet kuris darbuotojas, turintis prognozės formos teises, gali be patvirtinimo tikslinti informaciją.                                        | Sudarant biudžetą naudojama darbo eigų sistema, todėl galima valdyti pakeitimus ir leidžiama saugoti tikslinimų istoriją.         |
| **Įrašų tipai**           | Prognozių operacijų įrašai paremti vienetų skaičiumi ir savikaina bei pardavimo vieneto kainomis.  | Biudžeto informacija paremta sumomis, kurios padalytos į išlaidas ir įplaukas.                                          |
| **Prognozių modeliai**       | Kadangi kiekviena prognozė turi būti susieta su modeliu, galite kurti kelis prognozių modelius ir nustatyti submodelius.           | Sudarant projektų biudžetus, ribojami prognozių modeliai, kurie naudojami sudarant biudžetą. Naudojant mažiau prognozių modelių, gali padidėti projekcijų nuoseklumas.                           |
| **Išlaidų perviršiai**         | Operacijas, kurios lems išlaidų perviršį, įvesti galima tik leisti arba neleisti.   | Projektų biudžeto sudarymas naudotojams suteikia papildomų kontrolės parinkčių. Galite leisti įspėjimus ir perviršius.                    |
| **Kontrolė**               | Prognozių kontrolė atliekama naudojant prognozių mažinimą. Be jokio audito sekimo faktinės sumos atimamos iš prognozių operacijų balansų. Dėl to gali būti sunkiau atsekti, kur įvyko faktinės operacijos.                   | Vykdant projektų biudžeto kontrolę, faktinės sumos atimamos iš likusio biudžeto sumų. Taip galima aiškiau vykdyti audito sekimą.                                   |

## <a name="project-forecasts"></a>Projekto prognozė
Naudojant projekto prognozavimą, prognozės formose galima įvesti kiekvieno operacijos tipo prognozės operacijas. Prognozės operacijai galima naudoti kiekvieną atributą, kurį galima naudoti faktinei operacijai – pvz., eilutės pelningumą, eilutės atributus, darbuotojus arba aprašus. Taip pat galima planuoti, po kiek laiko, patyrus išlaidų, klientui išrašomos SF. 

Projekto prognozės operacijos grindžiamos vienetais ir sumomis. 

Kiekvieną projekto prognozę turite susieti su prognozės modeliu. Įvedant prognozės operaciją, automatiškai pasiūlomas prognozės modelis. Prognozės modelis veikia kaip prognozių operacijų talpykla. 

Prognozių modelius modeliui galite priskirti kaip submodelius. Taip prognozuoti galima pagal regioną, laikotarpį ar skyrių. Prognozių operacijas galima kopijuoti į modelį, kad būtų sukurtas naujas modelis, taip pat galite operacijas perkelti į didžiąją knygą. Dėl tiesioginio ryšio tarp prognozės ir modelio, kiekvienas prognozės modelis sudaro atskirą projekto biudžetą. 

Kaip projektų valdymo mechanizmas, prognozės modeliuose gali būti naudojamas prognozės mažinimas. Vykdant prognozių mažinimą, faktinės operacijos mažina prognozių operacijų balansus. Prognozės mažinimas taikomas aukščiausiam projektui hierarchijoje, todėl jis teikia tik ribotą prognozės pokyčių rodinį. Pavyzdžiui, jei darbuotojas susietas su subprojektu, darbuotojo faktinės operacijos registruojamos pagrindiniame projekte. Todėl gali būti sunku sekti pakeitimus, nes negalite lengvai nustatyti, dėl kurios operacijos kuriame subprojekte sumažėjo prognozės suma. Todėl naudinga sukurti prognozės modelio kopiją, kuri bus naudojama atliekant prognozių mažinimą. Tada galite naudoti ataskaitas ir peržiūrėti, kas iš pradžių buvo prognozuota. 

Projektų prognozes galite tikslinti, kopijuoti, naikinti ar perkelti į DK biudžetą. Tačiau nėra jokios procesų kontrolės. Bet kuris darbuotojas, turintis prognozės formos prieigos teises, gali atlikti tikslinimus be peržiūros.

-   **Tikslinti** – galite tikslinti prognozės operaciją tose pačiose formose, kuriose įvesti pradiniai įrašai.
-   **Kopijuoti arba naikinti** – kopijuojant prognozių operacijas, operacijų eilutės kopijuojamos iš vieno prognozės modelio į kitą. Naikinat prognozes, naikinamos prognozės modelio operacijos. Norėdami apriboti prognozių operacijas, kurios kopijuojamos ar naikinamos, pasirinkite konkrečius operacijų tipus ir datas. Taip galima kopijuoti ar naikinti tik konkrečias prognozės dalis.
-   **Perkelti** – perkeliant projekto prognozę į DK biudžetą, į jį perkeliamos prognozės modelio operacijos. Galima perrašyti bet kurią anksčiau perkeltą operaciją, esančią DK biudžete, į kurį perkeliate savo projekto prognozę.

## <a name="project-budgets"></a>Projektų biudžetai
Projektų biudžeto sudarymas yra paprastesnis metodas nei prognozavimas, nors jis integruojasi su prognozių modeliais. Jį naudojant, pradinei biudžeto informacijai ir tikslinimams įvesti naudojama viena forma, ir galima naudoti projekcijas, paremtas tik suma, kategorija ar veikla. 

Sudarant projekto biudžetą, visi pradiniai biudžetai ir tikslinimai turi būti siunčiami į projekto darbo eigą patvirtinti. Darbo eigos jums suteikia didesnę proceso kontrolę ir sukuria keitimų istorijos įrašą. 

Projekto biudžeto sudarymas primena DK biudžeto sudarymą, tik yra greitesnis ir lengviau nustatomas. Daugelio projektų DK biudžeto sudarymo parinkčių, pvz., numeracijų ar valiutos, nereikia nustatyti atskirai.

Projektų biudžetai automatiškai susiejami su dviem prognozių modeliais – vienas skirtas pradiniam biudžetui, o kitas – likusiam biudžetui. Todėl ataskaitose, kurios paremtos prognozių modeliais, galima naudoti biudžeto duomenis. Fiksuojant projekto biudžetą, sistema prognozių operacijas kuria pagal susietus modelius, kurie naudojami ataskaitų ir kontrolės tikslais.

## <a name="forecast-models"></a>Prognozių modeliai
Prognozių modeliai turi vieno sluoksnio hierarchiją. Tai reiškia, kad viena projekto prognozė turi būti susieta su vienu prognozės modeliu.

Jei naudojate projekto prognozavimą, modelius galite identifikuoti kaip submodelius. Po to galite sukurti prognozes pagal skyriu, laikotarpį arba regioną. Pvz., prognozės modelį galite sukurti metams ir tada kurti Šiaurės Rytų, Pietryčių, Šiaurės Vakarų ir Pietvakarių regionų prognozių, kurias pateikia regionų vadovai, submodelius. Pateikiamose ataskaitose pasirinkę skirtingas parinktis, informaciją galite peržiūrėti pagal bendrą prognozę arba pagal submodelį.



