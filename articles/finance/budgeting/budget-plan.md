---
title: Biudžeto planavimas
description: Šios laboratorijos tikslas yra pateikti valdomą „Microsoft Dynamics 365 Finance“ funkcijos naujinimų peržiūrą srityje Biudžeto planavimas. Šios laboratorijos tikslas yra iliustruoti greitą biudžeto planavimo modulio konfigūracijos pavyzdį ir pademonstruoti, kaip atlikti biudžeto planavimą naudojant šią konfigūraciją.
author: ShylaThompson
manager: AnnBe
ms.date: 06/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9558013236a728e0fb9691f4edd719fe58d5457
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772150"
---
# <a name="budget-planning"></a>Biudžeto planavimas

[!include [banner](../includes/banner.md)]

Šios laboratorijos tikslas yra pateikti valdomą „Microsoft Dynamics 365 Finance“ funkcijos naujinimų peržiūrą srityje Biudžeto planavimas. Šios laboratorijos tikslas yra iliustruoti greitą biudžeto planavimo modulio konfigūracijos pavyzdį ir pademonstruoti, kaip atlikti biudžeto planavimą naudojant šią konfigūraciją.  Šis laboratorinis darbas ypatingą dėmesį skirs tokiems verslo procesams ar užduotims:
- Sukuriama organizacijos biudžeto planavimo hierarchija ir sukonfigūruojama vartotojo sauga
- Apibrėžiami biudžeto plano scenarijai, biudžeto plano stulpeliai, išdėstymai ir „Excel“ šablonai
- Sukuriamas ir suaktyvinamas biudžeto planavimo procesas
- Sukuriamas biudžeto plano dokumentas paimant faktines sumas iš DK
- Naudojami paskirstymai biudžeto plano dokumento duomenims koreguoti
- Biudžeto plano dokumento duomenys redaguojami programoje „Excel“ 

<a name="prerequisites"></a>Būtinieji komponentai 
------------------

Šioje mokymo programoje jums reikės prieigos prie „Microsoft Dynamics 365 Finance“ aplinkos naudojant „Contoso“ demonstracinius duomenis ir turėti administratoriaus teises naudojant egzempliorių. Šiame laboratoriniame darbe nenaudokite privataus naršyklės režimo – jei reikia, atsijunkite nuo bet kokių kitų sąskaitų naršyklėje, ir prisijunkite naudodami administratoriaus kredencialus. Prisijungdami **PRIVALOTE** pažymėti žymės langelį Likti prisijungus. Taip sukuriamas nuolatinis slapukas, kurio dabar reikia „Excel“ programai. Jei prisijungsite prie programos naudodami kitą naršyklę nei IE, tada jus paragins prisijungti per „Excel“ programą. Spustelėjus „Prisijungti“ „Excel“ programoje, atsidarys IE iššokantysis langas – prisijungdami **PRIVALOTE** patikrinti, ar pažymėtas žymės langelis „Likti prisijungus“. Jei „Excel“ programoje spustelėjus „Prisijungti“ nepanašu, kad kas nors būtų įvykę, reikėtų išvalyti IE slapukų talpyklą.

## <a name="scenario-overview"></a>**Scenarijaus apžvalga**
Julija dirba finansų vadove „Contoso Entertainment Systems“ įmonėje Vokietijoje (DEMF). Artėjant FY2016, ji turi sudaryti kitų metų įmonės biudžetą. Biudžeto sudarymas atrodo taip:

1.  Julija naudoja ankstesnių metų faktines sumas kaip atskaitos tašką kuriant biudžetą.
2.  Atsižvelgdama į ankstesnių metų faktines sumas, ji kuria kitų metų 12 mėnesių įvertinimus
3.  Julija peržiūri biudžetą su CFO. Tai padariusi, ji atlieka būtinus biudžeto plano koregavimus ir užbaigia biudžeto rengimą.

Šio scenarijaus biudžeto planavimo konfigūracijos schema atrodo taip:

![Biudžeto planavimo konfigūracijos schema](./media/screenshot1-300x152.png)

Julija rengia biudžetą naudodama šį „Excel“ šabloną.

[![„Excel“ šablonas](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

## <a name="exercise-1-configuration"></a>1 užduotis: konfigūracija

### <a name="task-1-create-organizational-hierarchy"></a>**1 užduotis: sukurkite organizacijos hierarchiją**
Visas biudžeto sudarymo procesas vyksta finansų padalinyje, todėl Julija turi sukurti labai paprastą organizacinę hierarchiją – sudarytą tik iš finansų padalinio. 

1.1. Pasirinkite „Organizacijos hierarchijos“ („Organizacijos administravimas“ &gt; „Organizacijos“ &gt; „Organizacijos hierarchijos“) ir paspauskite mygtuką „Naujas“.

![Organizacijų hierarchijos](./media/screenshot3.png) 

1.2. Įveskite organizacinės hierarchijos pavadinimą ir langelyje „Pavadinimas“ spustelėkite mygtuką „Priskirti paskirtį“.

1.3. Pasirinkite biudžeto planavimo paskirtį, spustelėkite mygtuką „Įtraukti“ ir priskirkite naujai sukurtą organizacinę hierarchiją. 

[![Priskirti paskirtį](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Kartokite minėtus veiksmus saugumo organizacijos paskirčiai. Kai baigsite, uždarykite formą.

1.5. Formoje „Organizacinės hierarchijos“ spustelėkite mygtuką „Peržiūrėti“. Spustelėkite „Redaguoti“ hierarchijos dizaino įrankyje ir sukurkite hierarchiją spustelėdami „Įterpti“.

[![Įterpti](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Biudžeto sudarymo hierarchijoje pasirinkite finansų padalinį. 

[![Finansai](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Kai baigsite, spustelėkite „Publikuoti“ ir „Uždaryti“. Pasirinkite 1/1/2015 kaip hierarchijos publikavimo įsigaliojimo datą.

[![Įsigaliojimo data](./media/screenshot9.png)](./media/screenshot9.png)

### <a name="task-2-configure-user-security"></a>2 užduotis: sukonfigūruokite vartotojo saugą
Biudžeto planavimas naudoja specialias saugos strategijas, kad sukonfigūruotų prieigą prie biudžeto planų duomenų. Julija turi suteikti prieigą prie finansų biudžeto planų sau pačiai. 

2.1. Pereikite prie DEMF juridinio subjekto konteksto. 


2.2. Pasirinkite Biudžeto sudarymas &gt; Sąranka &gt; Biudžeto planavimas &gt; Biudžeto planavimo konfigūracija. Skirtuke „Parametrai“ nustatykite saugos modelio reikšmę į „Remiantis saugos organizacijomis“. 

[![Parametrai](./media/screenshot11.png)](./media/screenshot11.png) 

2.3. Pasirinkite Sistemos administravimas &gt; Vartotojai &gt; Vartotojai. Suteikti vartotojui administratoriui (Julia Funderburk) biudžeto vadovo vaidmenį. 

[![Biudžeto vadybininkas](./media/screenshot12.png)](./media/screenshot12.png) 

2.4. Pasirinkite vartotojo vaidmenį ir spustelėkite „Priskirti organizacijas“. 

[![Priskirti organizacijas](./media/screenshot13.png)](./media/screenshot13.png)

2.5. Pasirinkite „Suteikti prieigą tik tam tikroms organizacijoms“. Pasirinkite organizacinę hierarchiją, sukurtą pirmuoju veiksmu. Pasirinkite finansų mazgą ir spustelėkite „Suteikti su antriniais elementais“. 

***Svarbu!*** *– Įsitikinkite, kad jūs esate DEMF juridinio subjekto kontekste, kai atliekate šią užduotį, nes organizacijos sauga taikoma pagal juridinį subjektą* 

### <a name="task-3-create-scenarios"></a>3 užduotis: sukurkite scenarijus
3.1. Pasirinkite Biudžeto sudarymas &gt; Sąranka &gt; Biudžeto planavimas &gt; Biudžeto planavimo konfigūracija. Puslapyje „Scenarijai“ atkreipkite dėmesį į scenarijus, kuriuos naudosime toliau šiame laboratoriniame darbe: ankstesnių metų faktinės ir planuojamos sumos. 

*Pastaba: jei norite, galite sukurti naujus scenarijus šiai užduočiai ir naudoti juos.* 

[![Nauji scenarijai](./media/screenshot15.png)](./media/screenshot15.png) 

*Pastaba: Julija nenaudoja formalaus biudžeto sudarymo patvirtinimo proceso, todėl šiame laboratoriniame darbe mes praleisime darbo eigas, etapus ir darbo eigos etapų nustatymą ir naudosime esamą automatinio patvirtinimo darbo eigos nustatymą. Žr. priedą prie šios darbo eigos konfigūracijos.*

### <a name="task-4-create-budget-plan-columns"></a>4 užduotis: sukurkite biudžeto plano stulpelius
Biudžeto plano stulpeliai būna piniginiai arba kiekiniai ir jie gali būti naudojami biudžeto plano dokumento makete. Mūsų pavyzdyje turime sukurti ankstesnių metų faktinių sumų stulpelį ir 12 stulpelių, atstovaujančių kiekvieną biudžetinių metų mėnesį. Stulpelius galima sukurti tiesiog spustelėjus mygtuką „Pridėti“ ir užpildant reikšmes arba su duomenų objekto pagalba. Šiame laboratoriniame darbe naudosime duomenų objektą, kad užpildytume reikšmes. 

4.1. Spustelėję Biudžeto sudarymas&gt;Sąranka &gt; Biudžeto planavimas &gt; Biudžeto planavimo konfigūracija, atidarykite puslapį „Stulpeliai“. Spustelėkite mygtuką „Office“, esantį viršutiniame dešiniajame formos kampe, ir pasirinkite „Stulpeliai“ (nefiltruoti). 

[![Stulpeliai nefiltruoti](./media/screenshot16.png)](./media/screenshot16.png) 

4.2. Sistema atidarys „Excel“ darbaknygę, kuri bus naudojama reikšmėms užpildyti. Jei būsite paraginti, spustelėkite „Įjungti redagavimą“ ir „Pasitikėti šia programa“. 

4.3. Mums reikės daugiau stulpelių, kad įvestumėme reikšmes. Dešinėje srityje spustelėkite „Dizainas“, kad pridėtumėte stulpelių į tinklelį. 

[![Dizainas](./media/screenshot19.png)](./media/screenshot19.png) 

4.4. Spustelėkite mažą pieštuko mygtuką šalia dalies „PlanColumns“, kad pamatytumėte, kokius stulpelius galima įtraukti į tinklelį. 

[![Redaguoti](./media/screenshot20.png)](./media/screenshot20.png) 

4.5. Dukart spustelėkite kiekvieną galimą lauką, kad įtrauktumėte juos į pasirinktus laukus, ir spustelėkite „Naujinti“. 

4.6. „Excel“ lentelėje pridėkite visus stulpelius, kuriuos reikia sukurti. Naudokite „AutoFill“ funkciją programoje „Excel“, kad greitai pridėtumėte eilutes. Įsitikinkite, ar eilutės įtraukiamos į lentelę (naudodami vertikalią slinktį, turėtumėte matyti stulpelių antraštes tinklelio viršuje). 

4.7. Grįžkite į programą ir atnaujinkite puslapį. Publikuotos reikšmės bus rodomos. 

[![Atnaujinti](./media/screenshot23.png)](./media/screenshot23.png)

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>5 užduotis: sukurkite biudžeto plano dokumento maketus ir šablonus
Maketas apibrėžia, kaip atrodys biudžeto plano dokumento eilučių tinklelis, kai vartotojas atidarys biudžeto plano dokumentą. Taip pat galima perjungti biudžeto plano dokumento maketą ir pamatyti tuos pačius duomenis iš skirtingų kampų. Dabar, kai ji turi stulpelius, kurie bus naudojami su mūsų biudžeto plano dokumentu, Julija turi sukurti biudžeto plano dokumento maketą, kuris būtų panašus į „Excel“ lentelę, kuri ji naudoja biudžeto duomenims sukurti (žr. šio laboratorinio darbo skyrių „Scenarijaus apžvalga“) 

5.1. Spustelėję Biudžeto sudarymas &gt; Sąranka &gt; Biudžeto planavimas &gt; Biudžeto planavimo konfigūracija, atidarykite puslapį „Maketai“. Sukurkite naują maketą mėnesiniam biudžeto įrašui:

-   Pasirinkite MA+BU dimensiją, nustatytą taip, kad į maketą įtrauktų pagrindines sąskaitas ir verslo vienetus.
-   Surašykite visus biudžeto plano stulpelius, kurie buvo sukurti ankstesniu veiksmu, skyriuje „Elementai“. Padarykite visas faktines ankstesnių metų sumas redaguojamas.
-   Spustelėkite mygtuką „Aprašymai“, kad pasirinktumėte, kurios finansinės dimensijos turi rodyti aprašymus tinklelyje.

[![Aprašymai](./media/screenshot24.png)](./media/screenshot24.png) 

Pagal biudžeto plano maketo aprašą, galime sukurti „Excel“ šabloną, kuris bus naudojamas kaip alternatyvus būdas biudžeto duomenims redaguoti. „Excel“ šablonas turi atitikti biudžeto plano maketo aprašą, todėl, sugeneravę „Excel“ šabloną, negalėsite redaguoti biudžeto plano maketo – dėl šios priežasties ši užduotis turėtų būti atliekama apibrėžus visus maketo komponentus. 

5.2. 5.1. veiksmu sukurtam maketui spustelėkite mygtuką Šablonas &gt; Generuoti. Patvirtinkite perspėjimo pranešimą. Norėdami peržiūrėti šabloną, spustelėkite Šablonas &gt; Peržiūrėti. 

*Pastaba: įsitikinkite, kad pasirinkote „Išsaugoti kaip“ ir pasirinkite vietą, kur šablonas turėtų būti saugomas, kad būtų galima jį redaguoti. Jei vartotojas dialoge pasirenka Atidaryti ir neįrašo, failo pakeitimai jį uždarius neišliks.* 
[![Šablono rodinys](./media/screenshot25.png)](./media/screenshot25.png) 

5.3. &lt;Pasirinktinis veiksmas&gt; Modifikuokite „Excel“ šabloną, kad jis būtų patogesnis – įtraukite bendrų sumų formules, antraščių laukus, formatavimą ir t. t. Įrašykite pakeitimus ir įkelkite failą į biudžeto plano maketą spustelėdami&gt; „Maketas“. 


### <a name="task-6-create-a-budget-planning-process"></a>6 užduotis: sukurkite biudžeto planavimo procesą
Julija turi sukurti ir aktyvinti naują biudžeto planavimo procesą, apimantį visus aukščiau minėtus nustatymus, kad galėtų pradėti vesti biudžeto planus. Biudžeto planavimo procesas apibrėžia, kokios biudžeto sudarymo organizacijos, darbo eiga, maketai ir šablonai bus naudojami kuriant biudžeto planus. 

6.1. Pasirinkite Biudžeto sudarymas &gt; Sąranka &gt; Biudžeto planavimas &gt; Biudžeto planavimo procesas, ir sukurkite naują įrašą.

-   Biudžeto planavimo procesas – DEMF biudžeto sudarymas 2016
-   Biudžeto ciklas – 2016
-   Didžioji knyga – DEMF
-   Numatytoji sąskaitos struktūra – gamybos P&L
-   Organizacijos hierarchija – pasirinkite hierarchiją, sukūrtą laboratorinio darbo pradžioje
-   Biudžeto planavimo darbo eiga – priskirkite automatiškai – patvirtinkite darbo eigą finansų padaliniui
-   Biudžeto planavimo etapo taisyklėse ir šablonuose, kiekvienam darbo eigos biudžeto planavimo etapui nustatykite, ar leidžiama pridėti eilučių ir jas modifikuoti, ir koks turėtų būti numatytasis maketas

*Pastaba: galite sukurti papildomus dokumento maketus ir juos priskirti biudžeto planavimo darbo eigos etapui spustelėję mygtuką Alternatyvūs maketai.* 

[![Alternatyvūs maketai](./media/screenshot27.png)](./media/screenshot27.png) 

6.2. Pasirinkite Veiksmai &gt; Aktyvinti, kad suaktyvintumėte šią biudžeto planavimo darbo eigą. 

[![Aktyvinti](./media/screenshot28.png)](./media/screenshot28.png)

## <a name="exercise-2-process-simulation"></a>2 užduotis: proceso modeliavimas

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>7 užduotis: sugeneruokite biudžeto plano pirminius duomenis iš DK
7.1. Pasirinkite Biudžeto sudarymas &gt; Laikotarpio &gt; Generuoti biudžeto planą iš didžiosios knygos. Užpildykite periodinio proceso parametrus ir spustelėkite mygtuką „Generuoti“. 

7.2. Pasirinkite Biudžeto sudarymas &gt; Biudžeto planai ir raskite generavimo proceso sukurtą biudžeto planą. 

[![Biudžeto planas](./media/screenshot30.png)](./media/screenshot30.png) 

7.3. Atidarykite dokumento informaciją spustelėję ant dokumento numerio hipersaito. Biudžeto planas rodomas pagal šiame laboratoriniame darbe sukurto maketo nustatymus. 

[![Rodyti biudžeto planą](./media/screenshot31.png)](./media/screenshot31.png)

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>8 užduotis: sukurkite einamųjų metų biudžetą, remiantis ankstesnių metų faktinėmis sumomis
Biudžeto plane galima naudoti paskirstymo metodus, kad būtų lengva kopijuoti informaciją apie biudžeto planus iš vieno scenarijaus į kitą / paskirstyti juos per laikotarpius / paskirstyti dimensijoms. Naudosime paskirstymus, kad sukurtume einamųjų metų biudžetą pagal ankstesnių metų faktines sumas. 

8.1. Pasirinkite visas eilutes biudžeto plano dokumento tinklelyje ir spustelėkite mygtuką „Paskirstyti biudžetą“. 

[![Visos eilutės](./media/screenshot32.png)](./media/screenshot32.png) 

8.2. Pasirinkite paskirstymo metodą, laikotarpio raktą, šaltinio bei paskirties scenarijus ir spustelėkite „Paskirstyti“. 

[![Paskirstyti](./media/screenshot33.png)](./media/screenshot33.png)

Ankstesnių metų faktinės sumos bus nukopijuotos į einamųjų metų biudžetą ir paskirstytos laikotarpiams, naudojant pardavimo kreivės laikotarpio raktą. 

[![Pardavimo kreivė](./media/screenshot34.png)](./media/screenshot34.png)

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>9 užduotis: koreguokite biudžeto plano dokumentą naudodami „Excel“ ir užbaikite dokumentą
9.1. Spustelėkite mygtuką „Darbalapis“, kad atidarytumėte dokumento turinį programoje „Excel“.

9.2. Kai atsidarys „Excel“ darbaknygė, koreguokite biudžeto plano dokumento skaičius ir spustelėkite mygtuką „Publikuoti“.

9.3. Grįžkite į biudžeto plano dokumentą. Spustelėkite Darbo eiga &gt; Pateikti, kad automatiškai patvirtintumėte dokumentą.

[![Automatiškai patvirtinti](./media/screenshot37.png)](./media/screenshot37.png) 

Kai darbo eiga bus baigta, biudžeto plano dokumento etapas pasikeis į „Patvirtintas“. [![Aprobuota](./media/screenshot38.png)](./media/screenshot38.png)

## <a name="appendix"></a>Priedas

### <a name="auto-approve-workflow-configuration"></a>Darbo eigos konfigūracijos automatinis patvirtinimas

A. Biudžeto sudarymas &gt; Sąranka &gt; Biudžeto planavimas &gt; Biudžeto sudarymo darbo eigos. Kurkite naują darbo eigą naudodami šabloną „Biudžeto planavimo darbo eigos“:

[![Sukurti naują darbo eigą](./media/screenshot39.png)](./media/screenshot39.png)

Ši darbo eiga apims tik vieną užduotį – biudžeto plano etapo perkėlimą. 

[![Biudžeto plano etapo perkėlimas](./media/screenshot40.png)](./media/screenshot40.png) 

Įrašykite ir suaktyvinkite darbo eigą. 

B. Pasirinkite Biudžeto sudarymas &gt; Sąranka &gt; Biudžeto planavimas &gt; Biudžeto planavimo konfigūracija. Skirtuke „Etapai“ sukurkite 2 etapus – pradinį ir pateikimo. 

[![Pradinis ir pateikimo](./media/screenshot41.png)](./media/screenshot41.png)

C. Pasirinkite Biudžeto sudarymas &gt; Sąranka &gt; Biudžeto planavimas &gt; Biudžeto planavimo konfigūracija. Skirtuke „Darbo eigos etapai“ susiekite A veiksmu automatiškai patvirtintą darbo eigą su pradiniu ir pateikimo etapais.

[![Biudžeto sudarymas ir biudžeto planavimas](./media/screenshot42.png)](./media/screenshot42.png)  



