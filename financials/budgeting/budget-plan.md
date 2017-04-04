---
title: "Biudžeto planavimas"
description: "Šioje laboratorijoje tikslas teikti vadovaujasi vaizdas Microsoft Dynamics 365 veiklos funkcijų naujinimus biudžeto planavimo srityje. Šios laboratorijos tikslas yra iliustruoti greitą biudžeto planavimo modulio konfigūracijos pavyzdį ir pademonstruoti, kaip atlikti biudžeto planavimą naudojant šią konfigūraciją.  Šioje laboratorijoje bus orientuota konkrečiai į šios verslo procesus arba užduotis – sukurti organizacijos hierarchiją biudžeto planavimas ir sukonfigūruoti vartotojo saugą - apibrėžti biudžeto planavimo scenarijai, biudžeto planą kolonos, maketai ir Excel šablonai - sukurti ir aktyvinti-biudžeto planavimo procesą - kurti biudžeto planą dokumento faktinių duomenų DK traukimas naudojant asignavimus koreguoti biudžeto plano dokumento duomenis - redagavimo biudžeto planą dokumento duomenų programoje &quot;Excel&quot;"
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 81b44aa7af3a05ebc28963f406fab98bfbbb340d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning"></a>Biudžeto planavimas

Šioje laboratorijoje tikslas teikti vadovaujasi vaizdas Microsoft Dynamics 365 veiklos funkcijų naujinimus biudžeto planavimo srityje. Šios laboratorijos tikslas yra iliustruoti greitą biudžeto planavimo modulio konfigūracijos pavyzdį ir pademonstruoti, kaip atlikti biudžeto planavimą naudojant šią konfigūraciją.  Šioje laboratorijoje bus orientuota konkrečiai į šios verslo procesus arba užduotis – sukurti organizacijos hierarchiją biudžeto planavimas ir sukonfigūruoti vartotojo saugą - apibrėžti biudžeto planavimo scenarijai, biudžeto planą kolonos, maketai ir Excel šablonai - sukurti ir aktyvinti-biudžeto planavimo procesą - kurti biudžeto planą dokumento faktinių duomenų DK traukimas naudojant asignavimus koreguoti biudžeto plano dokumento duomenis - redagavimo biudžeto planą dokumento duomenų programoje "Excel" 

<a name="prerequisites"></a>Būtinieji komponentai 
------------------

Šiame pavyzdyje, jums reikia gauti Dynamics 365 operacijų aplinkoje su Contoso demonstraciniams duomenims, ir naudojama kaip administratorius egzemplioriuje. Nenaudokite į privatų naršyklės režimu šioje laboratorijoje - išsiregistravimas iš kitos paskyros naršyklėje, jei reikia ir prisijungti su Dynamics 365 operacijų administratoriaus kredencialų. Įėjus į Dynamics 365 operacijoms, jūs **turi** patikrinti "Įsiminti mane" langelį. Taip sukuriamas nuolatinis slapukas, kurio dabar reikia „Excel“ programai. Jei galite prisijungti prie Dynamics 365 operacijoms naudojate naršyklę, išskyrus IE, tada jūs būsite paraginti prisijungti per "Excel" programą. Spustelėjus „Prisijungti“ „Excel“ programoje, atsidarys IE iššokantysis langas – prisijungdami **PRIVALOTE** patikrinti, ar pažymėtas žymės langelis „Likti prisijungus“. Jei „Excel“ programoje spustelėjus „Prisijungti“ nepanašu, kad kas nors būtų įvykę, reikėtų išvalyti IE slapukų talpyklą.

## <a name="scenario-overview"></a>**Scenario overview**
Julija dirba finansų vadove „Contoso Entertainment Systems“ įmonėje Vokietijoje (DEMF). Artėjant FY2016, ji turi sudaryti kitų metų įmonės biudžetą. Biudžeto sudarymas atrodo taip:

1.  Julija naudoja ankstesnių metų faktines sumas kaip atskaitos tašką kuriant biudžetą.
2.  Atsižvelgdama į ankstesnių metų faktines sumas, ji kuria kitų metų 12 mėnesių įvertinimus
3.  Julija peržiūri biudžetą su CFO. Tai padariusi, ji atlieka būtinus biudžeto plano koregavimus ir užbaigia biudžeto rengimą.

Biudžeto planavimo schemą konfigūracijos scenarijus atrodys taip:

![Screenshot1](./media/screenshot1-300x152.png)

Julija naudoja šių "Excel" šablonas rengti biudžeto:

[![](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>1 užduotis: konfigūracija
=========================

## <a name="task-1-create-organizational-hierarchy"></a>**1 užduotis: Sukurti organizacijos hierarchiją**
Visas biudžeto sudarymo procesas vyksta finansų padalinyje, todėl Julija turi sukurti labai paprastą organizacinę hierarchiją – sudarytą tik iš finansų padalinio. 1.1. Eikite į organizacijos hierarchijos (organizacijos administracijos &gt;organizacijos &gt;organizacijos hierarchijos) ir spustelėkite Naujas mygtuką

![Screenshot3](./media/screenshot3.png) 

1.2. Organizacijos hierarchiją vardą ir spustelėkite mygtuką priskirti tikslas

[![Screenshot4](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. Pasirinkite biudžeto planavimo tikslas, spustelėkite mygtuką Pridėti ir priskirti naujai sukurtos organizacijos hierarchiją: 

[![Screenshot5](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Kartokite minėtus veiksmus saugumo organizacijos paskirčiai. Kai baigsite, uždarykite formą.

[![Screenshot6](./media/screenshot6.png)](./media/screenshot6.png)

1.5. Formoje „Organizacinės hierarchijos“ spustelėkite mygtuką „Peržiūrėti“. Spustelėkite „Redaguoti“ hierarchijos dizaino įrankyje ir sukurkite hierarchiją spustelėdami mygtuką „Įterpti“.

[![Screenshot7](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Biudžeto sudarymo hierarchijoje pasirinkite finansų padalinį. 

[![Screenshot8](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Kai baigsite, spustelėkite mygtuką „Publikuoti“ ir „Uždaryti“. Pasirinkite 1/1/2015 kaip hierarchijos publikavimo įsigaliojimo datą.

[![Screenshot9](./media/screenshot9.png)](./media/screenshot9.png)

## <a name="task-2-configure-user-security"></a>2 užduotis: sukonfigūruokite vartotojo saugą
Biudžeto planavimas naudoja specialias saugos strategijas, kad sukonfigūruotų prieigą prie biudžeto planų duomenų. Julija turi suteikti prieigą prie finansų biudžeto planų sau pačiai. 2.1. Perjungti į DEMF juridinio asmens atžvilgiu: [![Screenshot10](./media/screenshot10.png)](./media/screenshot10.png) 2.2. Pereiti prie biudžetinės sandaros &gt;nustatymo &gt;biudžeto planavimas &gt;biudžeto planavimo konfigūracijos. Parametrų skirtuke, nustatyti saugumo modelio reikšmę pagal saugumo organizacijoms [![Screenshot11](./media/screenshot11.png)](./media/screenshot11.png) 2.3. Eikite į sistemos administravimo &gt;vartotojai &gt;vartotojams. Suteikti vartotojui administratoriui (Julia Funderburk) biudžeto vadovo vaidmenį. [![Screenshot12](./media/screenshot12.png)](./media/screenshot12.png) 2.4. Pasirinkite vartotojo vaidmenį ir spustelėkite priskirti organizacijos [![Screenshot13](./media/screenshot13.png)](./media/screenshot13.png)2.5. Pasirinkite „Suteikti prieigą tik tam tikroms organizacijoms“. Pasirinkite organizacinę hierarchiją, sukurtą pirmuoju veiksmu. Pasirinkite finansų mazgas ir spustelėkite suteikti vaikams klavišu ***svarbu!*** *– Įsitikinkite, ar esate DEMF juridinio asmens atžvilgiu atlikdama šią užduotį, kaip juridiniam vienetui taikoma organizacinių saugumo*[![Screenshot14](./media/screenshot14.png)](./media/screenshot14.png)

## <a name="task-3-create-scenarios"></a>3 užduotis: sukurkite scenarijus
3.1. Pereiti prie biudžetinės sandaros&gt;nustatymo &gt;biudžeto planavimas &gt;biudžeto planavimo konfigūracijos. Puslapyje „Scenarijai“ atkreipkite dėmesį į scenarijus, kuriuos naudosime toliau šiame laboratoriniame darbe: ankstesnių metų faktinės ir planuojamos sumos. *Pastaba: jei norite, galite sukurti naujus scenarijus šiai užduočiai ir naudoti juos.* [![Screenshot15](./media/screenshot15.png)](./media/screenshot15.png)*Pastaba: Julia nenaudoja oficialaus patvirtinimo procesas dėl biudžeto sudarymo, mes praleisti darbo eigą, etapus ir darbo eigos etapais įdiegti šioje laboratorijoje ir panaudos esamą nustatymą Auto-patvirtinti darbo eigos. Žr šio darbo eigos konfigūracijai.*

## <a name="task-4-create-budget-plan-columns"></a>4 užduotis: sukurkite biudžeto plano stulpelius
Biudžeto plano stulpeliai būna piniginiai arba kiekiniai ir jie gali būti naudojami biudžeto plano dokumento makete. Mūsų pavyzdyje turime sukurti ankstesnių metų faktinių sumų stulpelį ir 12 stulpelių, atstovaujančių kiekvieną biudžetinių metų mėnesį. Stulpelius galima sukurti tiesiog spustelėjus mygtuką „Pridėti“ ir užpildant reikšmes arba su duomenų objekto pagalba. Šiame laboratoriniame darbe naudosime duomenų objektą, kad užpildytume reikšmes. 4.1. Į biudžetinės&gt;nustatymo &gt;biudžeto planavimas &gt;biudžeto planavimo konfigūracijos atidaryti stulpelių puslapį. Spustelėkite Office mygtuką viršutiniame dešiniajame kampe formos ir pasirinkti stulpelius (nefiltruotas) [![Screenshot16](./media/screenshot16.png)](./media/screenshot16.png) 4.2. Sistema atidarys „Excel“ darbaknygę, kuri bus naudojama reikšmėms užpildyti. Jei būsite paraginti, spustelėkite Įjungti redagavimą ir pasitikėti šia programa [![Screenshot18](./media/screenshot18.png)](./media/screenshot18.png)[![Screenshot17](./media/screenshot17.png)](./media/screenshot17.png) 4.3. Mes turime daugiau stulpelių, įveskite reikšmes. Spustelėkite dešiniojoje srityje įtraukti stulpelius į grotelių dizainas: [![Screenshot19](./media/screenshot19.png)](./media/screenshot19.png) 4.4. Spustelėkite mygtuką šalia PlanColumns Norėdami pamatyti galimus stulpelius norite įtraukti į tinklelį pieštuku šiek tiek [![Screenshot20](./media/screenshot20.png)](./media/screenshot20.png) 4.5. Dukart spustelėkite ant kiekvieno lauko įtraukti juos į pasirinktus laukus ir spustelėkite atnaujinti [![Screenshot21](./media/screenshot21.png)](./media/screenshot21.png) 4.6. „Excel“ lentelėje pridėkite visus stulpelius, kuriuos reikia sukurti. Naudokite „AutoFill“ funkciją programoje „Excel“, kad greitai pridėtumėte eilutes. Įsitikinkite, kad linijos yra įtraukta kaip dalis stalo (naudojant vertikalią slinkties, jūs galėsite pamatyti stulpelių antraštes ant grotelių) [![Screenshot22](./media/screenshot22.png)](./media/screenshot22.png) 4,7. Grįžti į Dynamics 365 operacijoms ir atnaujinkite puslapį. Paskelbta reikšmės bus rodomos Dynamics 365 operacijoms. [![Screenshot23](./media/screenshot23.png)](./media/screenshot23.png)

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>5 užduotis: sukurkite biudžeto plano dokumento maketus ir šablonus
Maketas apibrėžia, kaip atrodys biudžeto plano dokumento eilučių tinklelis, kai vartotojas atidarys biudžeto plano dokumentą. Taip pat galima perjungti biudžeto plano dokumento maketą ir pamatyti tuos pačius duomenis iš skirtingų kampų. Dabar, kai ji turi stulpeliusč kurie bus naudojami su mūsų biudžeto plano dokumentu, Julija turi sukurti biudžeto plano dokumento maketą, kuris būtų panašus į „Excel“ lentelę, kuri! ji naudoja biudžeto duomenims sukurti (žr. šio laboratorinio darbo skyrių „Scenarijaus apžvalga“) 5.1. Į biudžetinės&gt;nustatymo &gt;biudžeto planavimas &gt;biudžeto planavimo konfigūracijos atidaryti maketai puslapį. Sukurkite naują maketą mėnesiniam biudžeto įrašui:

-   Pasirinkite MA+BU dimensiją, nustatytą taip, kad į maketą įtrauktų pagrindines sąskaitas ir verslo vienetus.
-   Surašykite visus biudžeto plano stulpelius, kurie buvo sukurti ankstesniu veiksmu, skyriuje „Elementai“. Padarykite visas faktines ankstesnių metų sumas redaguojamas.
-   Spustelėkite mygtuką „Aprašymai“, kad pasirinktumėte, kurios finansinės dimensijos turi rodyti aprašymus tinklelyje.

[![Screenshot24](./media/screenshot24.png)](./media/screenshot24.png) pagal biudžeto plano maketo apibrėžimus, mes galime sukurti "Excel" šablonas, naudotinas kaip alternatyviu būdu redaguoti biudžeto duomenis. „Excel“ šablonas turi atitikti biudžeto plano maketo aprašą, todėl, sugeneravę „Excel“ šabloną, negalėsite redaguoti biudžeto plano maketo – dėl šios priežasties ši užduotis turėtų būti atliekama apibrėžus visus maketo komponentus. 5.2. Išdėstymas sukurtas pagal 5.1 punkte. žingsnis, spustelėkite mygtuką šablonas &gt;kurti. Patvirtinkite perspėjimo pranešimą. Norėdami peržiūrėti šabloną, spustelėkite Šablonas &gt;nuomone. *Pastaba: Įsitikinkite, kad pasirinkti "Įrašyti kaip" ir pasirinkite vietą, kur šablonas turi būti laikomas siekiant jį redaguoti. Jei vartotojas pasirinks "Open" dialogo langą neįrašę, pakeitimai, padaryti, kad failas liks ne uždarius failą.* [![Screenshot25](./media/screenshot25.png)](./media/screenshot25.png) 5.3. &lt;Šis žingsnis nėra privalomas&gt; modifikuoti "Excel" šablonas, kad ji atrodytų daugiau vartotojui draugiškas – įtraukti visas formules, antraštės laukų formatavimo ir t. t. Įrašyti keitimus ir įkelti failą į biudžeto planą maketas spustelėkite maketo &gt;įkelti [![Screenshot26](./media/screenshot26.png)](./media/screenshot26.png)

## <a name="task-6-create-a-budget-planning-process"></a>6 užduotis: sukurkite biudžeto planavimo procesą
Julija turi sukurti ir aktyvinti naują biudžeto planavimo procesą, apimantį visus aukščiau minėtus nustatymus, kad galėtų pradėti vesti biudžeto planus. Biudžeto planavimo procesas apibrėžia, kokios biudžeto sudarymo organizacijos, darbo eiga, maketai ir šablonai bus naudojami kuriant biudžeto planus. 6.1. Pereiti prie biudžetinės sandaros &gt;nustatymo &gt;biudžeto planavimas &gt;biudžeto planavimo procesą ir sukurti naują įrašą.

-   Biudžeto planavimo procesas – DEMF biudžeto sudarymas 2016
-   Biudžeto ciklas – 2016
-   Didžioji knyga – DEMF
-   Numatytoji sąskaitos struktūra – gamybos P&L
-   Organizacijos hierarchija – pasirinkite hierarchiją, sukūrtą laboratorinio darbo pradžioje
-   Biudžeto planavimo darbo eiga – priskirkite automatiškai – patvirtinkite darbo eigą finansų padaliniui
-   Biudžeto planavimo etapo taisyklėse ir šablonuose, kiekvienam darbo eigos biudžeto planavimo etapui nustatykite, ar leidžiama pridėti eilučių ir jas modifikuoti, ir koks turėtų būti numatytasis maketas

*Pastaba: galite sukurti papildomus dokumento maketus ir juos priskirti biudžeto planavimo darbo eigos etapui spustelėję mygtuką Alternatyvūs maketai.* [![Screenshot27](./media/screenshot27.png)](./media/screenshot27.png) 6.2. Pasirinkite veiksmų &gt;aktyvinti Norėdami suaktyvinti šią biudžeto planavimo eigos [![Screenshot28](./media/screenshot28.png)](./media/screenshot28.png)

<a name="exercise-2-process-simulation"></a>2 užduotis: proceso modeliavimas
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>7 užduotis: sugeneruokite biudžeto plano pirminius duomenis iš DK
7.1. Pereiti prie biudžetinės sandaros &gt;periodinės &gt;generuoti biudžeto planą iš Didžiosios knygos. Užpildykite periodinio proceso parametrus ir spustelėkite mygtuką „Generuoti“. [![Screenshot29](./media/screenshot29.png)](./media/screenshot29.png) 7.2. Pereiti prie biudžetinės sandaros &gt;biudžeto planus, rasti biudžeto planą sukūrė generuoti procesui. [![Screenshot30](./media/screenshot30.png)](./media/screenshot30.png) 7,3. Atidarykite dokumento informaciją spustelėję ant dokumento numerio hipersaito. Biudžeto planas pateikiamas kaip sukurta per šioje laboratorijoje makete apibrėžta [![Screenshot31](./media/screenshot31.png)](./media/screenshot31.png)

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>8 užduotis: sukurkite einamųjų metų biudžetą, remiantis ankstesnių metų faktinėmis sumomis
Biudžeto plane galima naudoti paskirstymo metodus, kad būtų lengva kopijuoti informaciją apie biudžeto planus iš vieno scenarijaus į kitą / paskirstyti juos per laikotarpius / paskirstyti dimensijoms. Naudosime paskirstymus, kad sukurtume einamųjų metų biudžetą pagal ankstesnių metų faktines sumas. 8.1. Pasirinkti visas eilutes į biudžeto planą dokumento tinklelis ir spustelėkite mygtuką skirstyti biudžeto [![Screenshot32](./media/screenshot32.png)](./media/screenshot32.png) 8,2. Pasirinkite paskirstymo metodo, laikotarpio raktą, šaltinio ir paskirties scenarijus ir spustelėkite paskirstyti 

[![Screenshot33](./media/screenshot33.png)](./media/screenshot33.png)

Praėjusiais metais faktinės sumos bus nukopijuota į einamųjų metų biudžetą ir juos paskirstyti per laikotarpius, naudojant pardavimų kreivės laikotarpio raktą. 

[![Screenshot34](./media/screenshot34.png)](./media/screenshot34.png)

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>9 užduotis: koreguokite biudžeto plano dokumentą naudodami „Excel“ ir užbaikite dokumentą
9.1. Spustelėkite mygtuką atidaryti dokumento turinys programoje "Excel" darbalapį

[![Screenshot35](./media/screenshot35.png)](./media/screenshot35.png)

9.2. Kai atsidarys „Excel“ darbaknygė, koreguokite biudžeto plano dokumento skaičius ir spustelėkite mygtuką „Publikuoti“.

[![Screenshot36](./media/screenshot36.png)](./media/screenshot36.png)

9.3. Grįžti į biudžeto planą dokumento Dynamics 365 operacijoms. Spustelėkite darbo eigos &gt;pateikti Auto patvirtinti dokumentą

[![Screenshot37](./media/screenshot37.png)](./media/screenshot37.png) 

Kai baigia darbo eigos, biudžeto planą dokumentu scenos pasikeičia į patvirtintą. [![Screenshot38](./media/screenshot38.png)](./media/screenshot38.png)

<a name="appendix"></a>Priedas
========

### <a name="auto-approve-workflow-configuration"></a>Darbo eigos konfigūracijos automatinis patvirtinimas

A. Biudžeto &gt;nustatymo &gt;biudžeto planavimas &gt;sudaromo biudžeto darbo eigos sukurti naują darbo eigos šablono biudžeto planavimo darbo eigų naudojimu:

[![Screenshot39](./media/screenshot39.png)](./media/screenshot39.png)

Šią darbo eigą bus pateikta tik viena užduotis – etapas pereinamojo laikotarpio biudžeto planas 

[![Screenshot40](./media/screenshot40.png)](./media/screenshot40.png) 

Išsaugoti ir suaktyvinti darbo eigos. 

B. Pereiti prie biudžetinės sandaros &gt;nustatymo &gt;biudžeto planavimas &gt;biudžeto planavimo konfigūracijos. Etapais skirtuke kurti 2 etapai – pradinio ir pateikė 

[![Screenshot41](./media/screenshot41.png)](./media/screenshot41.png)

C. Pereiti prie biudžetinės sandaros &gt;nustatymo &gt;biudžeto planavimas &gt;biudžeto planavimo konfigūracijos. Darbo eigos etapus skirtuke susieti darbo eiga Auto-patvirtinti sukūrėte atlikdami su etapais, pirminį ir pateikė 

[![Screenshot42](./media/screenshot42.png)](./media/screenshot42.png)  


