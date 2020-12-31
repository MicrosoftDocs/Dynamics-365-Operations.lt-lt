---
title: ER formato parametrų nustatymas kiekvienam juridiniui subjektui
description: Šioje temoje paaiškinama, kaip galite nustatyti modulio Elektroninės ataskaitos (ER) formato parametrus kiekvienam juridiniam subjektui.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: b51a7ae8587a3cbb65efc4af574929efcbc8fbf8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681477"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a>ER formato parametrų nustatymas kiekvienam juridiniui subjektui

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a>Būtinieji komponentai

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, aprašytus temoje [Kaip sukonfigūruoti, kad būtų naudojami ER formatų parametrai, nurodyti kiekvienam juridiniam subjektui](er-app-specific-parameters-configure-format.md).

Norėdami atlikti šioje temoje pateiktus pavyzdžius, turite turėti prieigą prie „Microsoft Dynamics 365 Finance“ („Finance“) ir vieną iš tolesnių vaidmenų.

- Elektroninės ataskaitos kūrėjas
- Elektroninės ataskaitos funkcijų konsultantas
- Sistemos administratorius

## <a name="import-er-configurations"></a>Importuokite ER konfigūracijas

1.  Prisijunkite prie savo aplinkos.
2.  Numatytoje ataskaitų srityje pasirinkite **Elektroninės ataskaitos**.
3.  Pasirinkite **Ataskaitų konfigūracijos**.
4.  Į dabartinį „Finance“ egzempliorių importuokite konfigūracijas, kurias eksportavote iš „Regulatory Configuration Service“ (RCS) atlikdami veiksmus, aprašytus temoje [Kaip sukonfigūruoti, kad būtų naudojami ER formatų parametrai, nurodyti kiekvienam juridiniam subjektui](er-app-specific-parameters-configure-format.md). Šiuos veiksmus atlikite su kiekviena modulio Elektroninės ataskaitos (ER) konfigūracija šia tvarka: duomenų modelis, modelio susiejimas ir formatai.

    1. Pasirinkite **Keistis \> Įkelti iš XML failo**.
    2. Paspaudę **Naršyti** pasirinkite reikiamos ER konfigūracijos failą XML formatu.
    3. Pasirinkite **Gerai**.
    
    Toliau pateiktoje iliustracijoje pateikiamos konfigūracijos, kurias reikia turėti atlikus veiksmus.

    ![ER konfigūracijų puslapis](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a>DEMF įmonės parametrų nustatymas

Naudodami ER sistemą, ER formato parametrus galite nustatyti konkrečiai programai.

1.  Pasirinkite juridinį subjektą **DEMF**.
2.  Konfigūracijų medyje pasirinkite formatą **Mokymo, kaip peržvelgti LE duomenis, formatas**.
3.  Veiksmų srities skirtuko **Konfigūracijos** grupėje **Konkrečių programų parametrai** pasirinkite **Sąranka**.

    ![ER konkrečių programų parametrų puslapis](./media/GER-AppSpecParms-LookupForm.PNG)
    
    Puslapyje **Konkrečių programų parametrai** galite konfigūruoti formato **Mokymo, kaip peržvelgti LE duomenis, formatas** duomenų šaltinio **Išrinkiklis** taisykles.
    
    Jei baziniame ER formate bus keli tipo **Peržvalga** duomenų šaltiniai, pradėti konfigūruoti norimo duomenų šaltinio taisyklių rinkinį galėsite tik norimą duomenų šaltinį pasirinkę „FastTab“ elemente **Peržvalgos**.
    
    Kiekviename duomenų šaltinyje galite konfigūruoti atskiras kiekvienos pasirinkto ER formato versijos taisykles.
    
    Visas taisyklių rinkinys, skirtas visiems peržvalgos duomenų šaltiniams, kurie yra pasiekiami pasirinktoje bazinio ER formato versijoje, sudaro ER formato konkrečių programų parametrus.

4.  Pasirinkite ER formato versiją **1.1.1**.
5.  „FastTab“ elemente **Sąlygos** pasirinkite **Įtraukti**.
6.  Naujo įrašo lauke **Kodas** pasirinkite išplečiamąją rodyklę, kad atidarytumėte peržvalgą.

    Peržvalgoje pateikiamas pasirenkamų mokesčių kodų sąrašas. Šį sąrašą pateikia duomenų šaltinis **Model.Data.Tax**, sukonfigūruotas baziniame ER formate. Kadangi šiame duomenų šaltinyje yra laukas **Pavadinimas**, peržvalgoje rodomas kiekvieno mokesčio kodo pavadinimas.

    ![ER konkrečių programų parametrų puslapis](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  Pasirinkite mokesčio kodą **VAT19**.
8.  Naujo įrašo lauke **Peržvalgos rezultatas** pasirinkite išplečiamąją rodyklę, kad atidarytumėte peržvalgą. Peržvalgoje pateikiamas pasirenkamų formatų išvardijimo TaxationLevel reikšmių sąrašas.

    Atkreipkite dėmesį, kad, jei kaip pageidajama vartotojo, kuriuo esate prisijungę, kalba pasirinkta vokiečių k., peržvalgos reikšmių žymos bus vokiečių k. (jei jos išverstos baziniame ER formate). Be to, jei peržvalgos duomenų šaltinio žyma išversta, ji skirtuke **Peržvalgos** bus rodoma vartotojo pageidaujama kalba.

    ![ER konkrečių programų parametrų puslapis](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  Pasirinkite reikšmę **Įprastas apmokestinimas**.

    Įtraukdami šį įrašą, apibrėžiate tokią taisyklę: kai reikalaujamas peržvalgos duomenų šaltinis **Išrinkiklis** ir kaip argumentas perduodamas mokesčio kodas **VAT19**, kaip reikalaujamas apmokestinimo lygis bus pateiktas **Įprastas apmokestinimas**.

10. Pasirinkite **Įtraukti** ir atlikite tolesnius veiksmus.

    1. Lauke **Kodas** pasirinkite mokesčio kodą **InVAT19**.
    2. Lauke **Peržvalgos rezultatas** pasirinkite reikšmę **Įprastas apmokestinimas**.
    
11. Dar kartą pasirinkite **Įtraukti** ir atlikite tolesnius veiksmus.

    1. Lauke **Kodas** pasirinkite mokesčio kodą **VAT7**.
    2. Lauke **Peržvalgos rezultatas** pasirinkite reikšmę **Sumažintas apmokestinimas**.
    
12. Dar kartą pasirinkite **Įtraukti** ir atlikite tolesnius veiksmus.

    1. Lauke **Kodas** pasirinkite mokesčio kodą **InVAT7**.
    2. Lauke **Peržvalgos rezultatas** pasirinkite reikšmę **Sumažintas apmokestinimas**.
    
13. Dar kartą pasirinkite **Įtraukti** ir atlikite tolesnius veiksmus.

    1. Lauke **Kodas** pasirinkite mokesčio kodą **THIRD**.
    2. Lauke **Peržvalgos rezultatas** pasirinkite reikšmę **Apmokestinimo nėra**.
    
14. Dar kartą pasirinkite **Įtraukti** ir atlikite tolesnius veiksmus.

    1. Lauke **Kodas** pasirinkite mokesčio kodą **InVAT0**.
    2. Lauke **Peržvalgos rezultatas** pasirinkite reikšmę **Apmokestinimo nėra**.
    
15. Dar kartą pasirinkite **Įtraukti** ir atlikite tolesnius veiksmus.

    1. Lauke **Kodas** pasirinkite parinktį **\*Ne tuščia\***.
    2. Lauke **Peržvalgos rezultatas** pasirinkite reikšmę **Kita**.
    
    Įtraukdami šį pastarąjį įrašą, apibrėžiate tokią taisyklę: kai mokesčio kodas, perduodamas kaip argumentas, netenkina nė vienos iš ankstesnių taisyklių, peržvalgos duomenų šaltinis kaip reikalaujamą apmokestinimo lygį pateiks **Kita**.

    ![ER konkrečių programų parametrų puslapis](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. Lauke **Būsena** pasirinkite **Baigta**.

    Paleidus ER formato versiją, kurios būsena yra **Baigta** arba **Bendrai naudojama**, šio taisyklių rinkinio būsena turi būti **Baigta**. Kitu atveju, formatui bandant įkelti duomenis iš šio taisyklių rinkinio, tuo pačiu metu paleidus peržvalgos duomenų šaltinį **Išrinkiklis**, bazinio ER formato vykdymas bus pertrauktas.
    
    Paleidus ER formato versiją, kurios būsena yra **Juodraštis**, bazinis ER formatas gali pasiekti šį taisyklių rinkinį – nesvarbu, kokia jo būsena.
    
17. Pasirinkite **Įrašyti**.
18. Puslapį **Konkrečių programų parametrai** uždarykite.

## <a name="run-the-er-format-in-the-demf-company"></a>ER formato vykdymas DEMF įmonėje

1.  Konfigūracijų medyje pasirinkite formatą **Mokymo, kaip peržvelgti LE duomenis, formatas**.
2.  Veiksmų srityje pasirinkite **Vykdyti**.
3.  Pasirodžiusiame dialogo lange pasirinkite **Gerai**.
4.  Atsisiųskite sugeneruotą išrašą ir jį išsaugokite vietiniame įrenginyje.

    Atkreipkite dėmesį, kad sugeneruotame išraše mokesčio kodo **InVAT7** suvestinė perkelta į lygį **Sumažintas**, o mokesčių kodų **VAT19** ir **InVA19** suvestinės perkeltos į lygį **Įprastas**. Tokį veikimo būdą nustato nuo juridinio subjekto priklausomų taisyklių rinkinio konfigūracija.
    
5.  Nueikite į **Mokestis \> Netiesioginiai mokesčiai \> PVM \> PVM kodai**.
6.  Pasirinkite mokesčio kodą **InVAT7**.
7.  Veiksmų srities skirtuko **PVM kodas** grupėje **Užklausos** pasirinkę **Registruotas PVM**, galite peržiūrėti informaciją apie mokesčio reikšmę ir taikomą kiekvieno mokesčio kodo tarifą.

    ![Registruoto PVM puslapis](./media/GER-AppSpecParms-Statement.PNG)

8.  Puslapį Registruotas PVM uždarykite.

## <a name="set-up-parameters-for-the-usmf-company"></a>USMF įmonės parametrų nustatymas

1.  Pasirinkite juridinį subjektą **USMF**.
2.  Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.
3.  Konfigūracijų medyje išplėskite elementą **Parametrizuotų iškvietų mokymo modelis**, tada – elementą **Parametrizuotų iškvietų mokymo formatas** ir pasirinkite formatą **Mokymo, kaip peržvelgti LE duomenis, formatas**.
4.  Veiksmų srities skirtuko **Konfigūracijos** grupėje **Konkrečių programų parametrai** pasirinkite **Sąranka**.
5.  Pasirinkite pasirinkto ER formato versiją **1.1.1**.
6.  „FastTab“ elemente **Sąlygos** pasirinkite **Įtraukti**.
7.  Naujo įrašo lauke **Kodas** pasirinkite išplečiamąją rodyklę, kad atidarytumėte peržvalgą.

    Dabar peržvalgoje pateikiamas pasirenkamų **USMF** įmonės mokesčių kodų sąrašas.

    ![ER konkrečių programų parametrų puslapis](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  Pasirinkite mokesčio kodą **EXEMPT**.
9.  Naujo įrašo lauke **Peržvalgos rezultatas** pasirinkite reikšmę **Apmokestinimo nėra**.
10. Dar kartą pasirinkite **Įtraukti**.
11. Naujo įrašo lauke **Kodas** pasirinkite parinktį **\*Ne tuščia\***.
12. Naujo įrašo lauke **Peržvalgos rezultatas** pasirinkite reikšmę **Įprastas apmokestinimas**.
13. Lauke **Būsena** pasirinkite **Baigta**.
14. Pasirinkite **Įrašyti**.

    ![ER konkrečių programų parametrų puslapis](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. Puslapį **Konkrečių programų parametrai** uždarykite.

## <a name="run-the-er-format-in-the-usmf-company"></a>ER formato vykdymas USMF įmonėje

1.  Konfigūracijų medyje pasirinkite formatą **Mokymo, kaip peržvelgti LE duomenis, formatas**.
2.  Veiksmų srityje pasirinkite **Vykdyti**.
3.  Pasirodžiusiame dialogo lange pasirinkite **Gerai**.
4.  Atsisiųskite sugeneruotą išrašą ir jį išsaugokite vietiniame įrenginyje.

    Atkreipkite dėmesį, kad sugeneruotame išraše tą patį ER formatą dar kartą panaudojote kitam juridiniam subjektui, tačiau ER formato nepakoregavę.

## <a name="reuse-legal-entitydependent-parameters"></a>Pakartotinis nuo juridinio subjekto priklausomų parametrų naudojimas

### <a name="export-parameters"></a>Eksportavimo parametrai

1.  Eikite į **Organizacijos administravimas \> Darbo sritys \> Elektroninės ataskaitos**.
2.  Pasirinkite **Ataskaitų konfigūracijos**.
3.  Konfigūracijų medyje pasirinkite formatą **Mokymo, kaip peržvelgti LE duomenis, formatas**.
4.  Veiksmų srities skirtuko **Konfigūracijos** grupėje **Konkrečių programų parametrai** pasirinkite **Sąranka**.
5.  Pasirinkite ER formato versiją **1.1.1**.
6.  Veiksmų srityje pasirinkite **Eksportuoti**.
7.  Atsisiųskite sugeneruotą failą ir jį išsaugokite vietiniame įrenginyje.

    Sukonfigūruotas konkrečių programų parametrų rinkinys dabar eksportuotas kaip XML failas.

### <a name="import-parameters"></a>Parametrų importavimas

1.  Pasirinkite ER formato versiją **1.1.2**.
2.  Veiksmų srityje pasirinkite **Importuoti**.
3.  Pasirinkite **Taip**, kad patvirtintumėte, jog norite perrašyti esamus šios formato versijos konkrečių programų parametrus.
4.  Pasirinkę **Naršyti** raskite failą, kuriame yra eksportuoti versijos **1.1.1** konkrečių programų parametrai.
5.  Pasirinkite **Gerai**.

    ER formato **1.1.2** versijoje dabar yra tie patys konkrečių programų parametrai, kuriuos iš pradžių sukonfigūravote **1.1.1** versijoje.
    
    Atkreipkite dėmesį, kad ER formato konkrečių programų parametrai priklauso nuo juridinio subjekto. Norėdami vienam juridiniam subjektui sukonfigūruotus konkrečių programų parametrus pakartotinai naudoti kitam juridiniam subjektui, turite juos eksportuoti būdami prisijungę prie pirmojo juridinio subjekto ir importuoti prisijungę prie kito juridinio subjekto.

    Šį metodą taip pat galite naudoti norėdami su ER formatu susijusius konkrečių programų parametrus, kurie iš pradžių buvo sukonfigūruoti viename „Finance“ egzemplioriuje, perkelti į kitą „Finance“ egzempliorių.

    Turėkite omenyje, kad, jei konkrečių programų parametrus sukonfigūruosite vienai ER formato versijai ir į dabartinį „Finance“ egzempliorių importuosite naujesnę to paties formato versiją, esami konkrečių programų parametrai importuoti versijai nebus taikomi.
    
    Taip pat žinokite, kad, kai pasirenkate importuotiną failą, jo konkrečių programų parametrų struktūra palyginama su atitinkamo tipo **Peržvalga** duomenų šaltinio, esančio pasirinktame importuoti ER formate, struktūra. Importavimas atliekamas, kai kiekvieno konkrečios programos parametro struktūra sutampa su atitinkamo duomenų šaltinio, esančio importuoti pasirinktame ER formate, struktūra. Jei struktūros nesutampa, gaunate įspėjamąjį pranešimą, kuriame nurodoma, kad importuoti negalima. Jei importavimą atliksite priverstinai, esami pasirinkto ER formato konkrečių programų parametrai bus išvalyti ir juos turėsite nustatyti nuo pradžių.

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a>Ryšys tarp konkrečių programų parametrų ir ER formato

Ryšį tarp ER formato ir jo konkrečių programų parametrų nustato ER formato nuo egzempliorius nepriklausomas unikalus identifikavimo kodas. Todėl, ER formatą pašalinus iš „Finance“, sukonfigūruoti to ER formato konkrečių programų parametrai išsaugomi dabartiniame „Finance“ egzemplioriuje. Juos galima pasiekti, kai bazinis ER formatas vėl importuojamas į šį „Finance“ egzempliorių.

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a>Prieiga prie konkrečių programų parametrų naudojant ER sistemą

Ankstesniame pavyzdyje ER formato konkrečių programų parametrus pasiekėte naudodami ER sistemą. Naudojant šį metodą, negalima apriboti prieigos prie ER formato konkrečių programų parametrų. Jei turite taikyti tokius apribojimus, atlikite tolesnius veiksmus. 

1.  Dar kartą panaudokite meniu elementą **ERSolutionAppSpecificParametersDesigner** arba įdiekite savo meniu elementą **ERSolutionAppSpecificParametersDesigner**.

    ![„Visual Studio“ puslapis](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  Atlikite vieną iš toliau nurodytų veiksmų.

    1.  Sukurkite naują meniu elemento mygtuką ir jį susiekite su atitinkamu lentelės **ERSolutionTable** įrašu, jo ypatybę **Duomenų šaltinis** nustatydami kaip **ERSolutionTable**.
    
        ![„Visual Studio“ puslapis](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  Sukurkite paprastą mygtuką ir perrašykite jo metodą **Spustelėta**, kaip parodyta tolesniame pavyzdyje.
    
        Naudodami šį metodą, galite nurodyti unikalų sprendimo ID (apibrėžtą reikšme **GUID**), kad būtų leidžiama pasiekti tik konkretaus ER formato ir iš jo išvestų kopijų konkrečių programų parametrus.
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)

[Kaip sukonfigūruoti, kad būtų naudojami ER formatų parametrai, nurodyti kiekvienam juridiniam subjektui](er-app-specific-parameters-configure-format.md)
