---
title: Pirkimo paraiškos darbo eiga
description: Darbo eigos proceso metu, pirkimo paraiškos pereina redagavimo procesą, nuo pirminės būsenos Juodraštis iki galutinės būsenos Patvirtinta. Kai pirkimo paraiška pateikiamai peržiūrai, pradedamas darbo eigos procesas. Pirkimo paraišką patvirtinus, pirkimo paraiškos eilutėms galima sugeneruoti pirkimo užsakymą ir pateikti tiekėjui, kad jį įvykdytų.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, WorkflowParticipantExpenToken
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2234
ms.assetid: dad3ba5a-2892-45d2-874a-300896f59b34
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a9dceb3f9e71163dcaf8b8763317110ef019844
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433439"
---
# <a name="purchase-requisition-workflow"></a>Pirkimo paraiškos darbo eiga

[!include [banner](../includes/banner.md)]

Darbo eigos proceso metu, pirkimo paraiškos pereina redagavimo procesą, nuo pirminės būsenos Juodraštis iki galutinės būsenos Patvirtinta. Kai pirkimo paraiška pateikiamai peržiūrai, pradedamas darbo eigos procesas. Pirkimo paraišką patvirtinus, pirkimo paraiškos eilutėms galima sugeneruoti pirkimo užsakymą ir pateikti tiekėjui, kad jį įvykdytų.

Prieš tai, kai pirkimo parašką galima pateikti peržiūrai, reikia sukonfigūruoti darbo eigą. Į darbo eigos procesą bet kokia tvarka gali įeiti vienas ar daugiau peržiūros veiksmų. Darbo eigos procesą taip pat galima sukonfigūruoti taip, kad peržiūros veiksmai būtų praleidžiami ir pirkimo paraiška būtų automatiškai patvirtinta. Galite konfigūruoti darbo eigą, norėdami pirkimo paraišką nukreipti kaip vieną dokumentą, arba atskiras pirkimo paraiškos eilutes galite nukreipti atitinkamiems peržiūrėtojams. Galite sukurti ir tokį scenarijų, kuriuo pirkimo paraiška vieniems peržiūrėtojams nukreipiama kaip vienas dokumentas, o pažymėtos pirkimo paraiškos eilutės nukreipiamos kitiems peržiūrėtojams.  

Jei pirkimo paraiškos eilutės peržiūrimos atskirai, peržiūros procesą reikia atlikti visoms pirkimo paraiškos eilutėms prieš darbo eigos procesui pereinant prie kito veiksmo ir prieš atliekant visą pirkimo paraiškos peržiūros procesą. Kai pabaigtas pirkimo paraiškos ir visų jos eilučių peržiūros procesas, bendroji pirkimo paraiškos būsena atnaujinama į **Patvirtinta**.  

Galite sukonfigūruoti darbo eigą, kad ji atspindėtų jūsų organizacijos pirkimo paraiškų verslo procesą. Konfigūruodami pirkimo paraiškos darbo eigos procesą, atkreipkite dėmesį toliau nurodytus dalykus.

-   Kokias išlaidas reikia peržiūrėti?
-   Kokias išlaidas galima automatiškai patvirtinti?
-   Koks asmuo reikalingas išlaidų paraiškoms peržiūrėti ir patvirtinti? Koks vaidmuo priskirtas šiems vartotojams?
-   Kokio proceso turi būti laikomasi, jei peržiūrėtojas yra nepasiekiamas?

Šiais pavydžiais vaizduojami du būdai, kaip galima konfigūruoti darbo eigą pirkimo paraiškoms.

## <a name="example-1-route-a-purchase-requisition-as-a-single-document-for-review"></a>1 pavyzdys: pirkimo paraišką peržiūrai nukreipkite kaip vieną dokumentą
Šia iliustracija parodoma, kaip pirkimo paraiška gali pereiti per darbo eigos peržiūros procesą kaip vienas dokumentas. Eilutės pirkimo paraiškoje nekreipiamos atskirai. Šiam pavyzdžiui į darbo eigą įeina šie vaidmenys:

-   **Prašytojas** – vartotojas, prašantis prekių ar paslaugų. Prašytojas gali parengti pirkimo paraišką arba jo vardu paraišką gali parengti kitas darbuotojas. Šis darbuotojas yra rengėjas. Rengėjo atsakomybė – valdyti pirkimo paraišką jos peržiūros proceso metu. Tik pirkimo paraiškos rengėjas gali ją modifikuoti.

**Pastaba:** jei darbuotojas nori sukurti pirkimo paraišką kieno nors kito vardu, jam turi būti suteiktos tinkamos teisės. Naudokite puslapį **Pirkimo paraiškos teisė** šioms teisėms nustatyti.

-   **Pirkimo agentas** – vartotojas, atliekantis įsigijimo peržiūrą ir galintis patvirtinti dokumentą.
-   **Prašytojo vadovas** – vartotojas, atliekantis vadybinę peržiūrą ir galintis patvirtinti dokumentą.

![Pirkimo paraiškos darbo eigos peržiūros procesas](./media/purchreqworkflowoverview_submission.gif)  
Šiame pavyzdyje į pirkimo paraiškos darbo eigos procesą įeina šie žingsniai:

1.  Rengėja pirkimo paraišką pateikia peržiūrai.
2.  Pirkimo agentas gauna pranešimą. Pranešime pirkimo agento prašoma patikrinti informaciją pirkimo paraiškoje. Jei trūksta reikiamos informacijos, pirkimo agentas gali ją įtraukti arba grąžinti pirkimo paraišką rengėjui, jog tai padarytų šis. Įvedus visą reikiamą informaciją, pirkimo paraiška gali pereiti prie kito peržiūros proceso veiksmo.
3.  Prašytojo vadovas peržiūri pirkimo paraišką. Jei, pavyzdžiui, pirkimo paraiškos suma viršija prašytojo išlaidų pirkimo paraiškoms limitą, pirkimo paraiška gali būti nukreipiama prašytojo vadovui. Prašytojo vadovas gali patvirtinti arba atmesti pirkimo paraišką arba grąžinti ją rengėjui keisti.

## <a name="example-2-route-the-individual-purchase-requisition-lines-for-review"></a>2 pavyzdys: peržiūrai nukreipkite atskiras pirkimo paraiškos eilutes
Šia iliustracija parodoma, kaip atskiras pirkimo paraiškos eilutes galima nukreipti per darbo eigą. Kiekvienos eilutės procesas paprastai yra toks pats, kaip ir pirkimo paraiškos, peržiūrimo kaip vieno dokumento, procesas. Tačiau iki tol, kai visos pirkimo paraiškos darbo eiga gali būti užbaigta, darbo eigos procesą atskirai turi užbaigti kiekviena eilutė.  

Šiame pavyzdyje darbuotojas rinkodaros kampanijai pateikia paraišką plakatams ir marškinėliams. Plakatų kainą pasidalija rinkodaros skyrius ir pardavimų skyrius. Jei plakatų ar marškinėlių kaina viršija skyriaus vadovams suteiktą pasirašymo limitą, pirkimo paraišką taip pat turi peržiūrėti ir grupės vadovas.  

Šiam pavyzdžiui į darbo eigą įeina šie vaidmenys:

-   **Prašytojas** – vartotojas, prašantis prekių ar paslaugų. Prašytojas gali parengti pirkimo paraišką arba jo vardu paraišką gali parengti kitas darbuotojas. Šis darbuotojas yra rengėjas. Rengėjo atsakomybė – valdyti pirkimo paraišką jos peržiūros proceso metu. Tik pirkimo paraiškos rengėjas gali ją modifikuoti.

**Pastaba:** jei darbuotojas nori sukurti pirkimo paraišką kieno nors kito vardu, jam turi būti suteiktos tinkamos teisės. Naudokite puslapį **Pirkimo paraiškos teisė** šioms teisėms nustatyti.

-   **Pirkimo agentas** – vartotojas, atliekantis įsigijimo peržiūrą ir galintis patvirtinti dokumentą.
-   **Prašytojo vadovas** – vartotojas, atliekantis vadybinę peržiūrą ir galintis patvirtinti dokumentą.
-   **Skyriaus vadovas** – vartotojas, atliekantis išlaidų peržiūrą ir galintis patvirtinti dokumentą.
-   **Grupės vadovas** – vartotojas, atliekantis teisės pasirašyti peržiūrą ir galintis patvirtinti dokumentą.

![Pirkimo paraiškos eilutės darbo eigos peržiūros procesas](./media/purchreqlineworkflowoverview.gif)  
Šiame pavyzdyje į pirkimo paraiškos eilučių darbo eigos procesą įeina šie žingsniai:

1.  Rengėja pirkimo paraišką pateikia peržiūrai. Kiekviena eilutė nukreipiama peržiūrėtojui, kuris darbo eigos proceso metu sukonfigūruojamas ją gauti.
2.  Pirkimo agentas gauna pranešimą. Pranešime pirkimo agento prašoma patikrinti informaciją pirkimo paraiškoje ir pirkimo paraiškos eilutėse. Pirkimo agentui atidarius pirkimo paraišką, rodomos visos eilutės, bet vaizdinis indikatorius nurodo, kurios eilutės buvo išsiųstos pirkimo agentui peržiūrėti. Jei trūksta reikiamos informacijos, pirkimo agentas gali ją įtraukti arba grąžinti pirkimo paraiškos eilutę rengėjui, jog tai padarytų šis. Įvedus visą reikiamą informaciją, pirkimo paraiškos eilutė gali pereiti prie kito peržiūros proceso veiksmo. Pirkimo paraiškos eilutės gali toliau keliauti per peržiūros procesą nepriklausomai viena nuo kitos.
3.  Prašytojo eilučių vadovas peržiūri ir patvirtina pirkimo paraiškos eilutes. Jei, pavyzdžiui, pirkimo paraiškos eilutės suma viršija prašytojo išlaidų pirkimo paraiškų eilutėms limitą, patvirtinimas gali būti nukreipiamas prašytojo vadovui. Vadovas gali patvirtinti arba atmesti vieną ar abi pirkimo paraiškos eilutes.
4.  Rinkodaros skyriaus vadovas peržiūri tiek plakatų, tiek marškinėlių pirkimo paraiškos eilutes. Pardavimo skyriaus vadovas peržiūri tik plakatų pirkimo paraiškos eilutę, nes tik už juos turi sumokėti pardavimo skyrius.
5.  Grupės vadovas peržiūri ir patvirtina marškinėlių pirkimo paraiškos eilutes tik jei grupės vadovo patvirtinimas yra būtinas, nes, pvz., pirkimo paraiškos eilutės suma viršija padalinio vadovo patvirtinimo ribą. Grupės vadovui nereikia patvirtinti plakatų pirkimo paraiškos eilutės.

> [!NOTE]
> Turi būti nustatyta sistemos valiuta, jei pirkimo paraiškos antraštės darbo eigai reikia patvirtinimų, susijusių su pasirašymo limitais.

## <a name="configuring-a-workflow-for-purchase-requisitions"></a>Pirkimo paraiškų darbo eigos konfigūravimas
Norėdami pirkimo paraišką nukreipti peržiūrai, turite sukonfigūruoti pirkimo paraiškų darbo eigos procesus. Jūsų apibrėžtas darbo eigos procesas valdo sąveiką tarp vartotojo, pareikalavusio prekių (prašytojo) ir darbo eigos peržiūrėtojo bei tvirtintojo. Pirkimo paraiškų maršruto planavimas priklauso nuo sąlygų, nurodytų darbo eigos konfigūracijoje. Pvz., šios sąlygos nustato, kada pirkimo paraiška turėtų būti nukreipiama, kokiam vartotojui arba vaidmeniui ji turėtų būti nukreipiama ir kokių veiksmų gali imtis vartotojai.  

Šios temos pavyzdžiuose parodoma, kaip pirkimo paraiška per darbo eigą gali būti nukreipiama kaip vienas dokumentas arba kaip atskiros pirkimo paraiškos eilutės. Taip pat galite sukonfigūruoti pirkimo paraiškų darbo eigą taip, kad ji atspindėtų jūsų organizacijoje apibrėžtą vidinę pirkimo paraiškų kontrolinę peržiūrą.  

Dalyviai arba peržiūrėtojai, kuriems priskirta darbo eigos užduotis, gali būti konkrečios vartotojų grupės nariai, vartotojai, turintys konkretų saugos vaidmenį, vartotojai, kurie yra susieti su pateikėju valdymo hierarchijoje, įvardinti vartotojai arba vartotojai, turintys konkrečių su išlaidomis susijusių atsakomybių.

### <a name="purchase-requisition-expenditure-reviewers"></a>Pirkimo paraiškų išlaidų redaktoriai

Išlaidų peržiūrėtojų konfigūracijos suteikia galimybę dinamiškai nukreipti išlaidas peržiūrėti pagal vartotoją, kuris priskirtas projekto vaidmeniui arba finansinei dimensijai, kur taikomas mokestis. Darbo eigos procesas naudoja nurodytą projekto vaidmenį arba finansinės dimensijos savininką, kad nustatytų, kam nukreipti išlaidas.  

Galite nurodyti vieną arba daugiau išlaidų peržiūrėtojų konfigūracijų ir pasirinkti konfigūraciją kurdami darbo eigą. Taip pat galite sukonfigūruoti išlaidų redaktoriaus reikšmes, taikomas kiekvienam organizacijos juridiniam subjektui. Nurodę išlaidų peržiūrėtojų konfigūracijas, priskirkite konfigūraciją darbo eigos užduočiai.  

Nereikia nustatyti išlaidų peržiūrėtojų konfigūracijų. Kaip peržiūrėtojus galite priskirti konkrečius vartotojus arba vartotojų grupes, kai nurodote darbo eigą. Tačiau jei organizacijos struktūra sudėtinga, išlaidų peržiūrėtojai gali padidinti patvirtinimo proceso efektyvumą. Be to, jei nustatote išlaidų peržiūrėtojus, jums nereikia atnaujinti darbo eigos peržiūrėtojų priskyrimų kiekvieną kartą, kai peržiūrėtojas pakeičia užduoties vaidmenis.  

Išlaidų peržiūrėtojus galite nustatyti puslapyje **Pirkimo paraiškų išlaidų peržiūrėtojai**. Sukurkite išlaidų peržiūrėtojo konfigūraciją ir įveskite reikšmes, taikomas kiekvienam organizacijos juridiniam subjektui. Jei paraiškos yra priskirtos projektui, galite nurodyti vaidmenį, atsakingą už paraiškų peržiūrą: projekto vadovą, projekto kontrolierių arba projekto pardavimo vadybininką. Išlaidos bus nukreipiamos vartotojui, kuris priskirtas tam nurodytam vaidmeniui. Taip pat galite nukreipti išlaidas finansinės dimensijos savininkui, skirtuke **Organizacijų paskirstymas** pažymėdami atitinkamą finansinės dimensijos parinktį.  

Norėdami naudoti vieną iš darbo eigoje nustatytų išlaidų peržiūrėtojų, atitinkamo darbo eigos elemento ypatybėse **Priskyrimas** parinktį **Dalyvio tipas** turite nustatyti į **Išlaidų dalyviai**.

<a name="additional-resources"></a>Papildomi ištekliai
--------

[Vartojimo paraiškos kūrimas](tasks/create-requisition-consumption.md)

[Pirkimo paraiškų verslo procesų darbo eigų nustatymas](https://www.microsoft.com/download/details.aspx?id=101821)

[Paraiškų darbo eigos](procurement-sourcing-workflows.md)

[Pirkimo paraiškos peržiūra](purchase-requisitions-overview.md)



