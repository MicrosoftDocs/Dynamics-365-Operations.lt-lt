---
title: Proceso vadovo sistema
description: Šioje temoje pateikiama informacija apie programuotojų, kurie išplečia mūsų sandėlio mobiliųjų procesų X++, apdorojimo vadovo sistemą.
author: Mirzaab
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 6882c979ad9b37eb4f95a04259b6ac0f0a0edcdc
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902051"
---
# <a name="process-guide-framework"></a>Proceso vadovo sistema

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie programuotojų, kurie išplečia mūsų sandėlio mobiliųjų procesų X++, apdorojimo vadovo sistemą. Sandėlio mobiliųjų procesų procesas gali būti extensible, nes procesai suskirstomi į smulkius žingsnius. Kiekvieno žingsnio verslo logika ir vartotojo sąsajos kūrimas išskleistas atskirose klasėse, tai leidžia extensibility.

## <a name="overview-of-the-existing-design"></a>Esamo dizaino peržiūra

Sandėlio mobiliųjų vykdymo srautai veikia vieno pasirinktinio tarnybos galinio punkto metu. Užklausa pateikiama iš mobiliosios programos XML formato eilute, kurioje pateikiami vartotojo sąsajos metaduomenys ir vartotojo įvestos vertės.

Kai užklausa gauta, pirmasis veiksmas yra šio XML išdėstymo išplėtimas laipsniu. **WHSMobileAppServiceXMLTranslator** klasė konvertuoja XML į konteinerį, kuriame yra kontrolės informacija ir seanso informacija.

Po to konteinerio informacija naudojama nustatyti, su kuriuo sandėlio procesu vartotojas dirba ar kada pradėti (atstovauja **WHSWorkExecuteMode** išvardijimas), ir atitinkamai sukurti išvestinę **WHSWorkExecuteDisplay** klasę. Iškviestas **displayform()** metodas, kuris tada atlikite šiuos veiksmus:

-   Apdoroja vartotojo duomenis (perduotas **WHSRFControlData** klasei, bet kai kurie procesai įdiegia specifinę logiką perrašant **processControl()** metodą).

-   Vykdo verslo logiką.

-   Padidina veiksmą.

-   Kuriamas konteineris, nurodantis naują vartotojo sąsają (paprastai **kuriama... ()** metodas).

Tada konteineris grąžinamas vertėjui, kuris tada eilutėmis išduoja XML ir siunčia jį atgal kaip atsakymą į mobilųjį įrenginį.

Toliau pateiktoje sekos diagramoje parodyta vykdymo srauto apžvalga. Atkreipkite dėmesį, kad diagrama yra daugiau schemos peržiūros ir nėra faktinio kodo 1:1 atvaizdo.

![Schematinė proceso apžvalga.](media/schematic-overview.png) 

### <a name="reason-for-the-redesign"></a>Problemos naujas planavimas

Aukščiau pateiktas dizainas suteikia labai paprastą struktūrą kūrimo procesams, naudojamiems mobiliojo įrenginio srautuose. Tačiau, kaip yra pirmiau, **displayform()** metodai perims kelias atsakomybes. Jis perduoda juos kitiems metodams ir klasėms, tačiau jei nėra konkrečios klasės atsakomybės, jis atliekamas nesuderinamu būdu tarp klasių. Taip pat, kai kurie iš palaikomų scenarijų nuosekliai plečiasi, kai kurios iš šių klasių gali tapti gana sudėtingas. Norint padaryti daug išsamesnę, kai kurios klasės/metodai yra perrašomos ir pakartotinai naudojami keliuose režimuose. Rezultatas – ypač ilgas metodas, kurio sudėtingumas yra didelis. Dėl jų praeityje kyla priežiūros problemų. Šių metodų klaidos buvo rizikos ir regresijos prone.
Pavyzdžiui, **processWorkLine()** metodas klasėje **WhsWorkExecuteDisplay** nurodytas iš kelių procesų (iš esmės, bet kurioje vietoje, kur vykdomas darbas).

Kad šios extensible, viena iš pasirinkčių būtų išskaidyti metodus **displayForm** į mažesnius metodus ir pristatyti išplėtimo taškus. Tačiau dėl scenarijaus matricos būtų taip, kad partneriai galėtų įrašyti plėtinius ir patvirtinti pagal regresiją. Ne tik dėl pirmiau minimo susistemuoto atsakomybės paskirstymo trūkumo kodas ilgai tęsis nenuspėjamais būdais, o dėl to, kad statant kokybės plėtinius vis tiek didėja.

Todėl perprojektavimas yra efektyvumo pasirinktis, siekiant aiškiai nustatyti klases, kurios turi nepriklausomą atsakomybę. Klasė turi turėti vieną atsakomybę, vieną pakeitimo priežastį ir vieną priežastį, dėl kurios reikia išplėsti.

## <a name="design-overview"></a>Dizaino peržiūra

Perprojektuotame sistemoje pagrindinė strategija rodo du principus: padalinti vykdymo srautą į atskirus komponentus, kurie turi gerai apibrėžtas atsakomybes ir turėti gerai nustatytus plėtinio taškus kiekviename iš komponentų.

Naujos sistemos pavadinimas yra „ProcessGuide“. Taip yra todėl, kad šių klasių tikslas yra padėti vartotojui pereiti į verslo procesą (priešingai nei raiškiosios kliento programos, kuri yra forma pagrįsta patirtis, kai vartotojas turi daugiau lankstumo bendraujant su duomenimis arba tvarka, kuria jie atlieka užduotis).

> [!NOTE]
> Neįmanoma neįmanoma išsamiai yra preliminari „WHS" prefikso praleidimas. Nors mobilieji procesai iš pradžių buvo įvesti sandėliavimui, vėliau jie turi peržengiantis ribas, kurios palaiko įvairius gamybos ir atsargų valdymo procesus. Todėl sandėlio nuoroda buvo pašalinta iš sistemos pavadinimo.

Norint identifikuoti komponentus, pirmiausia reikia peržiūrėti gamybos pradžios procesą (**WhsWorkExecuteDisplayProdStart** klasę). Pateiktas schematinis procesas.

![Schematinio proceso vaizdas.](media/production-start-process-schematic.png)

Reikia toliau nurodytų komponentų ieškant kontrolinio srauto:

-   Kontrolierius, pereięs per visą verslo procesą.
-   Veiksmas, atsakingas už proceso žingsnio vykdymą.
-   Duomenų procesorius, skirtas duomenims apdoroti žingsnyje.
-   Puslapių generatorius, atsakingas už žingsnio vartotojo sąsajos kūrimą.
-   Naršymo agentas, atsakingas už žingsnių perėjimą.
-   Klasė, atsakinga už verslo proceso vykdymo procesą.

Anksčiau pateiktoje proceso struktūrinėje diagramoje, jei pradėsite 1 žingsnį ir pradėsite apdoroti ankstesnio veiksmo duomenis, ir tada sujungsite su UI kūrimas, duomenys toliau bus apdorojami kitame žingsnyje. Taip bus pristatyta nuosekli veiksmų versija, todėl naujas aukšto lygio schematinis atrodys taip:

![Aukšto lygio schemos proceso vaizdas.](media/high-level-schematic.png)

Toliau pateikiami pagrindiniai perprojektavimo proceso komponentai:

-   **ProcessGuideController** – ši klasė suderina bendrą verslo proceso vykdymą. Ji apibrėžia etapus, kurie sudaro žingsnį ir naršymo agentą, kuris vėliau sudaro proceso vykdymą, taip pat valymo logiką, kad būtų galima atšaukti arba išeiti iš proceso.

-   **ProcessGuideStep** – ši klasė nurodo vieną verslo proceso veiksmą. Šioje klasėje yra fabrikų, kurie sukurti puslapio generatorių, veiksmus ir duomenų procesorius bei atsakingi už jų iškvietimą tinkama seka, apibrėžimas.

-   **ProcessGuideNavigationAgent** – ši klasė yra atsakinga už žingsnių naršymą. Kai veiksmas baigiamas, naršymo agentas yra atsakingas už kito žingsnio apibrėžimą ir išlaiko visus parametrus, kuriuos ankstesniam veiksmui gali reikėti perduoti prie kito.

-   **ProcessGuidePageBuilder** – ši klasė atsakinga už vartotojo sąsajos inicijavę.

-   **ProcessGuideAction** – ši klasė nurodo veiksmą, rodomą kaip vartotojo mygtukas.

-   **ProcessGuideDataProcessor** – ši klasė atsakinga už vartotojo įvestų duomenų į lauką apdorojimą.

## <a name="execution-flow"></a>Vykdymo eiga

Vykdymo srauto pradžios taškas nekinta. Taigi, užklausa vis dar patenka į tuos pačius galinius punktus, tada XML eilutėmis išdėsojama į konteinerį. Tada šis konteineris perduotas į **getNextFormState()**.

Yra trys svarbios klasės, apie kurių pastabą:

-  **ProcessGuideSessionState** – čia pateikiama seanso būsenos informacija – režimas, perdavimas, valdiklis ir vykdomas veiksmas, ir taip toliau.

-  **ProcessGuidePage** – tai yra primygtinai tipo vartotojo sąsajos metaduomenų pateiktis.

-  **ProcessGuideRequest**– tai apima du kaip nariai ir tai yra primygtinai tipo užklausos, gautos iš mobiliojo įrenginio, vaizdas.

Šios klasės sukuriamos naudojant konteinerio informaciją (ir būsenos, ir vartotojo įvestus kontrolės duomenis). Tai leidžia saugiai naudoti tipą vertėms pasiekti ir valdyti. Lyginant su pasikartojančia konteinerio prieiga proceso metu, tai suteikia naudos ir iš skaitymo, ir našumo.

Seanso būsenos informacija naudojama teisingai **ProcessGuideController** klasei sukurti. Kartą momentinis metodas **createResponse()** klasėje **ProcessGuideController** iškviečiamas. Šis metodas yra įvesties taškas į proceso vadovą, o po vykdymo grįžtant prie atsakymo (vaizduojamo **ProcessGuideResponse** klasėje). Tada atsakymas konvertuojamas atgal į konteinerį ir atisiunčiamas atgal į senstelėjusią logiką, kuri tada nusiunčia jį į XML ir siunčia atsakymą atgal į mobilųjį įrenginį.

Po to kontrolieriui reikia rasti kitą vykdyti žingsnį. Jei tai naujo proceso pradžia, valdiklis iškies **initialStep()** kad gautumėte pirmąjį proceso veiksmą. Po to **execute()** jis iškviestų metodą **ProcessGuideStep**. Tokiu būdu būtų kuriama **ProcessGuidePageBuilder** klasė ir iškviesta **buildPage()**, kuri grąžintų **ProcessGuidePage** objektu, kuris yra virtualus vartotojo sąsajos vaizdas, kuris turi būti pateikiamas vartotojui. Tada veiksmas nusiųs rezultatą atgal į valdiklį, kuris įrašytų dabartinės seanso būseną ir grąžintų rezultatą atgal į **getNextFormState()** klasės **ProcessGuideResponse** formoje. Tada atsakymas konvertuojamas atgal į konteinerį, o vėliau eilutėmis į XML ir išsiunčia atsakymą į mobilųjį įrenginį.

Toliau pateiktoje sekos diagramoje paaiškinamas šis valdymo srautas. Įsidėmėkite, kad tai dažniausiai naudojamas kontrolės srautas, supaprastinto dizaino paaiškinimas.

![Supaprastintos kontrolės srautas.](media/control-flow.png)

Kai vartotojas atlieka veiksmą mobiliajame įrenginyje, spustelėdamas mygtuką (arba nuskaitęs vertę, kuri paprastai suaktyvina numatytąjį veiksmą) – užklausa pristatoma **createResponse()** metodą **ProcessGuideController** per tą patį maršrutą. Šis laikas, tačiau valdiklis iš seanso būsenos informacijos žino, kuriame etape yra vartotojas. Todėl ji inkcijaoja atitinkamą **ProcessGuideStep** klasę ir iškviečiamas vykdymo metodas. **ProcessGuideStep** savo ruožtu perskaito vartotojo iškviečiamą veiksmo pavadinimą ir paleidžia atitinkamą **ProcessGuideAction** klasę ir iškviečia **execute()**.

Klasė **ProcessGuideAction** yra atsakinga už konkretaus veiksmo įdėjimo procesą, tačiau yra dvi nepaisomos išimtys.

Pirmasis yra **ProcessGuideOKAction** klasė. Šis veiksmas leidžia suprasti, kad vartotojas nori patvirtinti ir pereiti į priekį proceso metu. Atsižvelgiant į tai, šis metodas iš tikrųjų atlieka perskambinti ProcessGuideStep klasėje, tai reiškia, kad veiksmas iškviečiamas **processData()** esanti **ProcessGuideDataProcessor**. Tai apdoroja vartotojo įvestus duomenis, tada atnaujina veiksmo būseną ir siunčia rezultatą atgal valdikliui. Atsižvelgiant į procesoriaus rezultatus, veiksmas iškviečiamas puslapio generatorių, kad būtų kuriama atitinkama vartotojo sąsaja, arba nustatoma veiksmo būsena kaip baigta. Tai atsispindi viršutinėje diagramos dalyje, žemiau pateiktoje sekų diagramoje.

Kita išimtis yra atšaukimo veiksmas, įdiegtas **ProcessGuideCancelResetProcessAction** ir **ProcessGuideCancelExitProcessAction** klasėse. Šie veiksmai reiškia tikslą atšaukti procesą ir grįžti į proceso pradžios procesą arba visiškai išeiti iš proceso. Panašus į veiksmą **Gerai** šie veiksmai taip pat atlieka žingsnio perskambinimą, kuris rodo tikslą **ProcessGuideController**. Tada valdiklis atlieka reikiamą būsenų kintamųjų valymą ir arba perkelia kontrolę į pradinį proceso veiksmą, arba visiškai nutraukia procesą.

Atlikus veiksmą, jei nustatyta žingsnio būsena **Baigta** valdiklis inicijaus **ProcessGuideNavigationAgent** kuris grąžina kito veiksmo pavadinimą. Valdiklis tuomet atlieka šį veiksmą ir iškviečiamas **execute()** metodas ir ciklas tęsiamas. Dažniausiai naujas veiksmas iškviečiamas atitinkamą **ProcessGuidePageBuilder** kad būtų kuriama kito ekrano vartotojo sąsaja, kuri bus pateikiama vartotojui, o paskui siunčiama atgal. Šis srautas rodomas apatinėj pusėje, žemiau pateiktoje sekų diagramoje.

![Sekos diagramą.](media/sequence-diagram.png)

## <a name="building-a-new-process-using-the-processguide-framework"></a>Naujo proceso kūrimas naudojant ProcessGuide sistemą

Geriausias būdas paaiškinti kontrolės eigą yra naudojant pavyzdį, kuris yra programoje – gamybos pradžios procesą.

## <a name="overview-of-the-production-start-process"></a>Gamybos proceso pradžios apžvalga

Pradėkite suprasdami proceso srautą. Pirmuoju veiksmu vartotojas raginamas įvesti gamybos užsakymo ID.

![Raginti įvesti gamybos ID.](media/production-id-prompt.png)

Kai vartotojas įveda gamybos užsakymo ID, užsakymo numeris patikrinamas. Kai kurie paleisti patikrinimas yra pagrįsti tuo, ar užsakymas yra tame pačiame sandėlyje kaip ir vartotojas prisijungęs, bei užsakymo būsena. Jei patikrinimas nesėkmingas, vartotojui rodomas klaidos pranešimas. Jei patikrinimas sėkmingas, vartotojui rodoma gamybos užsakymo ir prekės informacija.

Vartotojas gali arba atšaukti, kad grįžtų prie proceso pradžios, arba spustelėti **Gerai**, kad patvirtintumėte. Pastarąjį atveju gamybos užsakymo būsena yra **Pradėta** atitinkami žurnalai užregistruojami, valdiklis pereina prie pirmo veiksmo, o vartotojui rodomas pranešimas „Darbas baigtas".


## <a name="creating-the-controller"></a>Valdiklio kūrimas

Pirmas žingsnis kuriant verslo procesą sukuria valdiklio klasę, išplečiant iš **ProcessGuideController** abstrakčios klasės, kuri įdiegia numatytuosius valdiklio elgseną. Naujas klasės pavadinimas yra **ProdProcessGuideProductionStartController** ir kartu su **WHSWorkExecuteMode** verte **StartProdOrder**. Naudojama ta pati **SysExtension** momentinė programa, kuri buvo naudojama **WHSWorkExecuteDisplay** klasėse, kuri padeda sukurti valdiklio momentinę užklausą, kai vartotojas vykdo šio režimo meniu elementą.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
public class ProdProcessGuideProductionStartController extends ProcessGuideController
```

> [!NOTE]
> Klasės pavadinimų šablonas yra **\<FunctionalArea\>ProcessGuide \<Businessprocessname\>Valdiklis**. Tai šablonas, naudojamas valdiklių klasėms ir išplečiant jį kitoms klasėms.


## <a name="building-the-first-step"></a>Pirmojo žingsnio kūrimas

Tada apibrėžkite pirmą veiksmą, kurį sukuriate klasę **ProdProcessGuidePromptProductionIdStep** kuri išplečia iš **ProcessGuideStep**.

Klasės inkseravimo užduotis perduota žingsnių gamyklai, kurią iškviečiama **ProcessGuideController** bazinė klasė. Numatytasis gamyklos diegimas inicijauoja veiksmą, paremtą pavadinimu. Todėl, norėdami sukurti **ProdProcessGuidePromptProductionIdStep** kaip pirmą kontrolieriaus veiksmą, turite atlikti du dalykus:

-   **ProdProcessGuidePromptProductionIdStep** klasė konvertuojama naudojant atributą **ProcessGuideStepName**.

    ```xpp
    [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))] public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
    ```

-   Valdiklio klasėje, norėdami grąžinti veiksmo pavadinimą, įdiegti abstraktų metodą **initialStepName()**.

    ```xpp
    protected final ProcessGuideStepName initialStepName()
    {
        return classStr(ProdProcessGuidePromptProductionIdStep);
    }
    ````   
    
> [!NOTE]
> Atributo **ProcessGuideStepName** vertė nebūtinai turi tiksliai atitikti klasės pavadinimą, kaip parodyta anksčiau. Tačiau naudojant šią klasę, naudojant šią klasę, suteikiamas uniformumas ir sauga pagal tipą. Rekomenduojama naudoti šią vardų suteikimo konvenciją.
>
> Šis **ProcessGuideStepName** žingsnis pagrįstas momentinis veiksmas įdiegtas **ProcessGuideStepDefaultFactory** klasėje. Retais atvejais, norėdami turėti skirtingą veiksmo momentavimo strategiją, turite atlikti šiuos veiksmus:
> -   Sukurkite naują gamyklos klasę, perimtą iš **ProcessGuidStepAbstractFactory**.
> -   Pasirinktinai sukurkite naują parametrų klasę, kuri pridės sąsają **ProcessGuideIStepCreationParameters** kurioje būtų parametrai, kurių prireiks gamyklos.
> -   Savo kontrolieriaus klasėje, norėdami grąžinti anksčiau nurodytą gamyklos ir parametrus, nepaisoma **stepFactory()** ir **stepCreationParameters()** metodų.

Kitas žingsnis yra įdiegti **ProdProcessGuidePromptProductionIdStep** klasės funkcijas. Turite įdiegti vartotojo sąsajos kūrimo logiką, apdoroti vartotojo įvestus duomenis ir nustatyti, kada veiksmas bus baigtas.

### <a name="building-the-user-interface-for-the-first-step"></a>Kuriama pirmojo veiksmo vartotojo sąsaja

Vartotojo sąsaja kuriama naudojant klasę, perimtą iš aabstrakčios klasės **ProcessGuidePageBuilder**. Šiame veiksme pavadinkite klasę, kad ji rodytų tai, kas tai daro – **ProdProcessGuidePromptProductionIdPageBuilder**.

Klasės inicijacijų mechanizmas panašus į tai, kaip veiksmas buvo sukurtas iš valdiklio. 

-   **ProdProcessGuidePromptProductionIdPageBuilder** klasė konvertuojama naudojant atributą **ProcessGuidePageBuilderName**.

    ```xpp
    [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))] public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
    ```

-   Klasėje **ProdProcessGuidePromptProductionIdStep** norėdami grąžinti šį pavadinimą pristatę abstrakčią metodą **pageBuilderName()**.

    ```xpp
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
    }
    ```    

> [!TIP]
> Panašus į žingsnių gamyklos, taip pat yra abstrakti gamyklos šablonas, įdiegtas puslapių generatoriaus gamyklos. Todėl retais atvejais, norėdami turėti skirtingą veiksmo momentavimo strategiją, turite atlikti šiuos veiksmus:
> - Sukurkite naują gamyklos klasę, perimtą iš **ProcessGuidePageBuilderAbstractFactory**.
> - Pasirinktinai sukurkite naują parametrų klasę, kuri pridės sąsają **ProcessGuideIPageBuilderCreationParameters** kurioje būtų parametrai, kurių prireiks gamyklos.
> - Savo kontrolieriaus klasėje, norėdami grąžinti anksčiau nurodytą gamyklos ir parametrus, nepaisoma **pageBuilderFactory()** ir **pageBuilderCreationParameters()** metodų.

Norint įdiegti vartotojo sąsają, reikia turėti puslapį su vienu teksto lauku, kad būtų galima įvesti gamybos užsakymo ID, plius mygtuką **Gerai** ir mygtuką **Atšaukti**. Mygtukas **Atšaukti** turi išeiti iš proceso.

Norėdami tai įgyvendinti, turite nepaisyti dviejų metodų klasėje **ProdProcessGuidePromptProductionIdPageBuilder**:

-   Norėdami pridėti teksto lauką, naudokite **addDataControls()** metodą.

    ```xpp
    protected final void addDataControls(ProcessGuidePage _page)
    {
        _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
    }
    ```   

-   Naudokite metodą **addActionControls()** norėdami pridėti mygtukus **Gerai** ir **Atšaukti**.

    ```xpp
    protected final void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelExitProcess));
    }
    ``` 

Taip įtraukiate duomenų valdiklius, po jų – mygtukus. Tačiau jei norite sukurti ekraną su tarpinių duomenų valdikliais ir mygtukais, vietoj jo galite nepaisyti **addControls()** metodo, kad jis būtų lankstesnis.

Papildomas scenarijus, į kuriuos reikia atsižvelgti, yra tai, kaip atkurti puslapį, kai tikrinimo triktis, pavyzdžiui, jei vartotojas įveda neteisingą gamybos užsakymo ID. The **ProcessGuidePageBuilder** bazinė klasė vykdo numatytąją elgseną, kuri atkuriama vartotojo sąsają, išvalo nuskaitytą vertę ir įtraukia klaidos valdiklį su klaidos valdymo klaidos pranešimu. Kadangi tai numatytasis veikimo būdas, kurį norite naudoti, klaidų tvarkymui nereikia pridėti jokio kodo.

> [!TIP]
> Jei norite taikyti pasirinktinį UI veikimo būdą esant klaidoms, galite nepaisyti vieno ar daugiau **metodų rebuildFromRequestPage()**, **isErrorState()** ir **reuseRequestPageOnError()**.

### <a name="processing-the-user-entered-data-in-the-first-step"></a>Vartotojo įvestų duomenų apdorojimas pirmuoju žingsniu

Duomenys apdorojami klasėje **ProcessGuideDataProcessorDefault** kuri savo ruožtu iškviečiama senstelėjusią **WhsRfControlData** klasę. Nereikia atlikti jokių numatytosios veikimo būdo pakeitimų, o **WhsRfControlData** jau turi logiką, kuria galima **ProdId** lauką, todėl jums nereikia rašyti jokios logikos, reikalingos tai tvarkyti. Jei reikia tikrinimo logikos plėtinių, nagrinėkime galimybę naudoti **WhsControl** pagrįstą plėtinio mechanizmą.

### <a name="determine-if-the-first-step-is-complete"></a>Nustatyti, ar pirmasis veiksmas baigtas

Kai patikrinimas sėkmingas, laikas pažymėti veiksmą kaip užbaigtą. Tai atliekama bazinėje klasėje, tačiau norint nustatyti žingsnio užbaigimą, reikia įdiegti sąlygą. Šis nepaisomas metodas tai daro.

```xpp
protected final boolean isComplete()
{
    WhsrfPassthrough pass = controller.parmSessionState().parmPass();
    ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);
        return (prodId != '');
}
```   

### <a name="step-two-view-order-details-and-confirm"></a>Antras veiksmas: peržiūrėti užsakymo informaciją ir patvirtinti

Antruoju proceso žingsniu vartotojas rodomas ekranas, turintį išsamią informaciją apie užsakymą. Vartotojas gali spustelėti mygtuką **Gerai** ad patvirtintų gamybos užsakymo pradžiai, arba spustelėti **Atšaukti** kad grįžtų prie proceso pradžios. Pavyzdžiui, pavadinkite veiksmą **ProdProcessGuideConfirmProductionOrderStep** ir puslapio generatoriaus klasę **ProdProcessGuideConfirmProductionOrderPageBuilder**.

Klasė ProdProcessGuideConfirmProductionOrderStep atrodo taip.

```xpp
[ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
{
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
     }
}
```     

Kadangi čia vartotojas neįves jokių verčių, jums nereikia nepaisyti **isComplete()** metodo. Veiksmas baigtas, kai vartotojas spusteli **Gerai**.

Puslapių generatoriaus klasė nepaiso **addDataControls()** metodo, kad būtų galima pridėti tris žymes. Pirmojoje žymėje rodomas gamybos užsakymo ID, antrame – prekės informacija (pvz., prekės ID, dimensijos ar aprašymas), o trečiasis – kiekio ir matavimo vieneto.

**addActionControls()** nepaisoma, kad būtų įtraukti 2 mygtukai **Gerai** ir **Atšaukti** procesui atšaukti ir grįžti atgal į proceso pradžios mygtuką.

```xpp
/// <summary>
/// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
/// and then confirm.
/// </summary>
[ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
{
    protected void addDataControls(ProcessGuidePage _page)
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;
        
        _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
        _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
        _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

        if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
        {
            _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
        }
    }

    protected void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelResetProcess));
    }
```

> [!NOTE]
> Naudodami programą Explorer, šioje temoje galite rasti tą patį X++ metodų šaltinio kodą. Filtruokite klasės pavadinimą, dešiniuoju pelės klavišu spustelėkite klasės pavadinimą ir pasirinkite **Peržiūrėti kodą**.

### <a name="step-3-start-the-production-order"></a>3 veiksmas: Gamybos užsakymo pradėjimas

Trečiasis žingsnis yra vykdyti gamybos užsakymo pradžios verslo logiką. Šis žingsnis šiek tiek skiriasi nuo ankstesnių veiksmų, nes šis veiksmas neturi vartotojo sąsajos. Šis veiksmas vykdomas tyliuoju būdu, kai ankstesniame veiksme vartotojas spusteli **Gerai**.

**ProcessGuideStepWithoutPrompt** abstrakti klasė įdiegia numatytąjį tokių veiksmų elgseną. Todėl dabartinis veiksmas turi išplėsti **ProcessGuideStepWithoutPrompt** klasę ir nepaisyti **doExecute()** metodo.

Šiame kodo pavyzdyje parodyta klasė ir **doExecute()** metodo diegimas. Būdas tiesiog nuskaito užsakymo ID ir vartotojo ID iš seanso būsenos ir iškviečiamas būdas pradėti šį gamybos užsakymą.

```xpp
/// <summary>
/// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
/// </summary>
[ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
{
    protected final void doExecute()
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        WhsWorkExecute workExecute = WhsWorkExecute::construct();
        workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

        this.addProcessCompletionMessage();

        super();
    }

}
```

Išimties atveju sistemos išimčių apdorojimo logika užtikrina, kad procesas bus atmestas atgal prie ankstesnio veiksmo.

> [!NOTE]
> Iškviečiamas **addProcessCompletionMessage()** įtraukia pranešimą „Darbas baigtas" prie naršymo parametrų. Kitas veiksmas (darant prielaidą, kad jis turi vartotojo sąsają) parodys šį pranešimą. Pagrindinės klasės apdoros šią logiką ir joks konkretus kodas neturi būti pridėtas prie proceso klasių, kad būtų pasiektas toks veikimo būdas.


### <a name="building-the-navigation-through-the-steps"></a>Naršymo kūrimas naudojant žingsnius

**ProcessGuideController** bazinė klasė inicijavo klasę **ProcessGuideNavigationAgentDefault** kuri remiasi iš anksto nustatyta naršymo maršrutu, kuris yra paprastas šaltinio ir paskirties veiksmų schema. Gamybos pradžios scenarijaus atveju, nes nėra sąlyginio šakų, šis diegimas užtenka. Todėl, norint nustatyti naršymo maršrutą, reikia tik nepaisyti metodo **initializeNavigationRoute()**.

```xpp
    protected ProcessGuideNavigationRoute initializeNavigationRoute()
    {
        ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
        navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

        return navigationRoute;
    }
```

Yra procesų, kuriuose bus sąlyginis filialas (remiantis vartotojo veiksmais ar kitomis sąlygomis). Tokie procesai turi atlikti šiuos veiksmus:

-   Įdiegti konkrečius naršymo agentus, paveldėtus iš klasės **ProcessGuideNavigationAgent**.

-   Įdiegti konkretaus naršymo agentų gamyklos paveldėtą iš klasės **ProcessGuideNavigationAgentAbstractFactory** kurioje yra logika, skirta tinkamam naršymo agentui, pagrįstam dabartiniu veiksmu, seanso būsena, vartotojo veiksmu ar kita logika, sukurti.

-   Pasirinktinai nepaisyti kontrolieriaus klasės **navigationAgentCreationParameters()** kad tinkami parametrai būtų perduoti.

-   Nepaisyti kontrolieriaus **navigationAgentFactory()** kad būtų galima kurti anksčiau sukurtą naršymo agentų gamyklos paiešką.

### <a name="action-classes"></a>Veiksmo klasės

Veiksmų klasės nurodo vartotojo veiksmus, todėl šiame pavyzdyje naudojamas veiksmas **Gerai**, kad parodytų, kaip šie veiksmai kuriami.

```xpp
[ProcessGuideActionName(#ActionOK)]
public class ProcessGuideOKAction extends ProcessGuideAction
{
    public final str label()
    {
        return "@SYS5473";
     }
     protected final void doExecute()
     {
        step.executeOKAction();
      }
}
```    

Klasė turi įdiegti 2 abstrakčius metodus:

-   **label()** kuri grąžina žymę, kuri bus rodoma mygtuko valdiklyje, susietame su šiuo veiksmu.

-   **doExecute()** kuris atlieka veiksmą. Kaip buvo nurodyta anksčiau, mygtukas **Gerai** tiesiog atlieka veiksmą perskambinti. Tačiau kiti veiksmai čia gali turėti sudėtingesnę logiką.

Veiksmai sukurti naudojant **SysExtension** sistemą, pagrįstą atributu **ProcessGuideActionName**. Panašus į puslapių generatoriaus inicijas, žingsnio klasė vykdo numatytąją veiksmų gamyklos veiklą ir jos galima nepaisyti. Puslapių generatorius įtraukia mygtuko valdiklį.

```xpp
_page.addButton(step.createAction(#ActionOK), true);
```

Tai atliekant klausiama, kaip sukurti perduotam pavadinimui veiksmų klasę ir prie mygtuko pridėti veiksmą.

### <a name="summary"></a>Suvestinė

Norėdami apibendrinti viską, kas paaiškinta šioje temoje, čia pateikiama išsamesnė procesui reikalingų kodų suvestinė:

1.  **ProdProcessGuideProductionStartController**

    1.  Nepaisyti **initialStepName()** kad būtų rodomas pirmojo veiksmo pavadinimas.
    2.  Nepaisyti **initializeNavigationRoute()** kad būtų galima kurti naršymo schemą.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideProductionStartController</c> class is the controller class for the production order start process guide.
        /// </summary>
        [WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
        public class ProdProcessGuideProductionStartController extends ProcessGuideController
        {
            protected ProcessGuideStepName initialStepName()
            {
                return classStr(ProdProcessGuidePromptProductionIdStep);
            }

            protected ProcessGuideNavigationRoute initializeNavigationRoute()
            {
                ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
                navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

                return navigationRoute;
            }

        }
        ```

2.  **ProdProcessGuidePromptProductionIdStep**

    1.  Nepaisyti **isComplete()** norint nurodyti, kada veiksmas laikomas baigtu.
    2.  **pageBuilderName()** nepaisymo, jei norite nurodyti naudoti naudojamą puslapio generatorių.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdStep</c> represents a step that 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))]
        public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
        {
            protected boolean isComplete()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);

                return (prodId != '');
            }

            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuidePromptProductionIdPageBuilder**

    1.  Nepaisykite **addDataControls()** tam, kad įtrauktumėte **Prod ID** teksto lauką.
    2.  Nepaisykite **addActionControls()** norėdami pridėti mygtukus **Gerai** ir **Atšaukti**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdPageBuilder</c> class builds a page 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))]
        public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelExitProcess));
            }

        }
        ```

4.  **ProdProcessGuideConfirmProductionOrderStep**

    1.  **pageBuilderName()** nepaisymo, jei norite nurodyti naudoti naudojamą puslapio generatorių.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderStep</c> class represents the step for viewing production order
        /// details and confirming the same.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
        public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
        {    
            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuideConfirmProductionOrderPageBuilder**

    1.  Nepaisyti **addDataControls()** jei norite įtraukti užsakymo, prekės ir kiekio informacijos žymes.

    2.  Nepaisykite **addActionControls()** norėdami pridėti mygtukus **Gerai** ir **Atšaukti**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
        /// and then confirm.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
        public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;

                _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
                _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
                _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

                if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
                {
                    _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
                }
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelResetProcess));
            }

        ```

        > [!NOTE]
        > Metodas **generateItemInfoForProdId()** kuris naudojamas prekių informacijos etiketėms generuoti, į šią temą neįtraukiamas. Šis metodas pateikia užklausas kelioms lentelėms, kad būtų galima gauti prekės ID, aprašymą ir dimensijas. Jei norite geriau suprasti **generateItemInfoForProdId()** žiūrėkite šaltinio kodą.

4.  **ProdProcessGuideStartProductionOrderStep**

    1.  Nepaisyti **doExecute()** kad būtų galima vykdyti gamybos pradžios procesą ir įtraukti proceso užbaigimo pranešimą.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
        public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
        {
            protected final void doExecute()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                WhsWorkExecute workExecute = WhsWorkExecute::construct();
                workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

                this.addProcessCompletionMessage();

                super();
            }

        }
        ```

> [!NOTE]
> Atsidėmėkite, kad į sistemą buvo perkelta daug bendrųjų šablonų (vartotojo sąsajos atnaujinimas dėl klaidos, proceso užbaigimo pranešimo, **Gerai** ir **Atšaukti** elgesį) todėl programos programuotojas įrašomas įrašant parametrų kodą, kuris yra ir tarpinis, ir todėl rizikuoja nenuoseklus veikimas procesuose. Jei scenarijus turi krypti nuo bendro maršruto, programos programuotojas teikia pasirinktį perrašyti tinkamus metodus, bet tai yra apgalvotas nuokrypis, kuris yra ir aiškus, ir sekamas.


### <a name="extending-a-business-process"></a>Verslo proceso plėtimas

Ši tema išryškino, kaip kurti naują procesą naudojant **ProcessGuide** sistemą. Šiame galutiniame skyriuje rasite keletą pavyzdžių, kaip šis verslo procesas gali būti išplėstas.

### <a name="add-a-step-in-a-flow-using-processguidenavigationagentdefault"></a>Įtraukti srauto veiksmą (naudojant ProcessGuideNavigationAgentDefault)

Kur išplėsti:

-   Proceso **ProcessGuideController** klasės antrinis procesas.

Kaip išplėsti:

-   Plėskite **initializeNavigationRoute()** metodą ir iškvieskite kontrolės klasę **addFollowingStep()** klasėje **ProcessGuideNavigationRoute**.

### <a name="add-a-step-in-a-flow-using-custom-navigation-agent"></a>Įtraukti srauto veiksmą (naudojant tinkintą naršymoa agentą)

Kur išplėsti:

-   **ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent** antrinis procesas.

Kaip išplėsti:

-   Sukurkite naują **ProcessGuideNavigationAgent** vienoje klasėje, kuri pateikia norimą veiksmo pavadinimą.

-   Sukurkite naują klasę, išvedusią iš **ProcessGuideNavigationAgentFactory** kuri sąlygiškai grąžina anksčiau sukurtą naršymo agentą.

-   Išplėsti metodą **navigationAgentFactory()** kad būtų galima kurti anksčiau sukurtą klasę grąžinti į gamyklos paiešką.

### <a name="add-a-new-control-in-the-ui-of-an-existing-step"></a>Įtraukti naują valdiklį į esamo veiksmo UI 

Kur išplėsti:

-   **ProdProcessGuidePageBuilder** antrinis veiksmas.

Kaip išplėsti:

-   Išplėskite **addDataControls()** metodą ir įtraukite papildomą valdiklį.

### <a name="complete-overhaul-of-the-user-interface-in-an-existing-step"></a>Baigti vartotojo sąsajos perpildą esamame veiksme

Kur išplėsti:

-   **ProdProcessGuideStep** antrinis puslapis.

Kaip išplėsti:

-   Sukurkite naują **ProdProcessGuidePageBuilder** klasės vienoje klasėje ir įdiegiate norimą vartotojo sąsają.

-   Pratęskite metodą **pageBuildeName()** veiksmų klasėje, kad būtų galima grąžinti anksčiau sukurtai klasei **ProcessGuidePageBuilderNameAttribute**.

### <a name="alter-logic-when-a-step-is-considered-complete"></a>Pakeisti logiką, kai veiksmas laikomas baigtu

Kur išplėsti:

-   **ProdProcessGuideStep** antrinis puslapis.

Kaip išplėsti:

-   Norėdami sukurti papildomą logiką, pratęskite **isComplete()** metodą.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]