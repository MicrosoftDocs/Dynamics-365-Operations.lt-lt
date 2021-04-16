---
title: Prekybos kanalų fiskalinės integracijos nustatymas
description: Šioje temoje pateikiamos prekybos kanalų fiskalinės integracijos nustatymo gairės.
author: josaw
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: bc87972b1cd2e04d31a3d48132cd1de42353698d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801922"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Prekybos kanalų fiskalinės integracijos nustatymas

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Įžanga

Šioje temoje pateikiamos prekybos kanalų fiskalinės integracijos nustatymo gairės. Daugiau informacijos apie fiskalinę integraciją žr. [Prekybos kanalų fiskalinės integracijos apžvalga](fiscal-integration-for-retail-channel.md).

Fiskalinės integracijos nustatymo procesas apima toliau nurodytas užduotis.

1. Sukonfigūruoti fiskalines jungtis, kurios nurodo finansinius įrenginius arba paslaugas, naudojamas fiskalinio registravimo tikslais, pvz., fiskaliniai spausdintuvai.
2. Sukonfigūruoti dokumentų teikėjus, generuojančius finansinius dokumentus, kuriuos fiskalinės jungtys užregistruos finansiniuose įrenginiuose arba paslaugose.
3. Sukonfigūruoti fiskalinės registracijos procesą, kuris apibrėžia fiskalinės registracijos veiksmus ir fiskalines jungtis bei finansinių dokumentų teikėjus, naudojamus kiekviename veiksme.
4. Priskirti fiskalinės registracijos procesus elektroninio kasos aparato (EKA) funkcijų profiliams.
5. Priskirti jungčių techninius profilius aparatūros profiliams.

## <a name="set-up-a-fiscal-registration-process"></a>Fiskalinės registracijos proceso nustatymas

Prieš naudodamiesi fiskalinės integracijos funkcija, turėtumėte sukonfigūruoti toliau išvardytus parametrus.

1. Atnaujinti prekybos parametrus.

    1. Puslapio **Bendrai naudojami prekybos parametrai** skirtuke **Bendra** nustatykite parinkties **Įjungti fiskalinę integraciją** reikšmę **Taip**. Skirtuke **Numeracijos** nurodykite tolesnių nuorodų numeracijas.

        - Fiskalinio techninio profilio numeris
        - Fiskalinių jungčių grupės numeris
        - Registracijos proceso numeris

    2. Puslapyje **Prekybos parametrai** nurodykite fiskalinio funkcinio profilio numeraciją.

    > [!NOTE]
    > Numeracijos nėra būtinos. Visų fiskalinės integracijos objektų numerius galima generuoti naudojant numeraciją arba neautomatiniu būdu.

2. Įkelkite fiskalinių jungčių ir finansinių dokumentų teikėjų konfigūracijas.

    Finansinių dokumentų teikėjas generuoja finansinius dokumentus, kuriuose nurodomos prekybos operacijos ir įvykiai, užregistruoti EKA tokiu formatu, koks naudojamas sąveikaujant su finansiniu įrenginiu arba paslauga. Pvz., finansinių dokumentų teikėjas gali generuoti finansinio kvito versiją XML formatu.

    Fiskalinė jungtis yra atsakinga už ryšį su finansiniu įrenginiu arba paslauga. Pvz., fiskalinė jungtis gali siųsti finansinį kvitą, kurį finansinių dokumentų teikėjas sukūrė XML formatu, fiskaliniam spausdintuvui. Daugiau informacijos apie fiskalinės integracijos komponentus žr. [Finansinių įrenginių fiskalinės integracijos procesas ir fiskalinės integracijos pavyzdžiai](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

    1. Puslapyje **Fiskalinės jungtys** (**Mažmeninė prekyba ir prekyba \> Kanalų sąranka \> Fiskalinė integracija \> Fiskalinės jungtys**) nusiųskite kiekvieno įrenginio arba paslaugos, kuria planuojate naudotis fiskalinės integracijos tikslais, XML konfigūraciją.

        > [!TIP]
        > Pasirinkdami **Peržiūrėti** galite peržiūrėti visus funkcinius ir techninius profilius, susijusius su dabartine fiskaline jungtimi.

    2. Puslapyje **Finansinių dokumentų teikėjai** (**Mažmeninė prekyba ir prekyba \> Kanalų sąranka \> Fiskalinė integracija \> Finansinių dokumentų teikėjai**) nusiųskite kiekvieno įrenginio arba paslaugos, kuria planuojate naudotis fiskalinės integracijos tikslais, XML konfigūraciją.

        > [!TIP]
        > Pasirinkdami **Peržiūrėti** galite peržiūrėti visus funkcinius profilius, susijusius su dabartiniu finansinių dokumentų teikėju.

    Fiskalinių jungčių ir finansinių dokumentų teikėjų konfigūracijų pavyzdžių žr. [Mažmeninės prekybos SDK fiskalinės integracijos pavyzdžiai](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-retail-sdk).

    > [!NOTE]
    > Duomenų susiejimas laikomas fiskalinio dokumento teikėjo dalis. Norėdami nustatyti skirtingus tos pačios jungties duomenų susiejimus (pvz., nuo būsenos priklausančius reguliatorius), turėtumėte sukurti skirtingus fiskalinių dokumentų teikėjus.

3. Sukurkite jungčių funkcinius profilius ir jungčių techninius profilius.

    1. Puslapyje **Funkciniai jungčių profiliai** (**Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Fiskalinė integracija \> Funkciniai jungčių profiliai**), sukurkite funkcinį kiekvieno fiskalinės jungties ir finansinių dokumentų teikėjo, susijusio su šia fiskaline jungtimi, derinio profilį.

        1. Pasirinkite jungties pavadinimą.
        2. Pasirinkite dokumento teikėją.

        Funkciniame jungties profilyje galite keisti duomenų susiejimo parametrus. Norėdami atkurti numatytuosius parametrus, kurie apibrėžti finansinių dokumentų teikėjo konfigūracijoje, pasirinkite **Naujinti**.

        **Pavyzdžiai**

        |   | Formatas | Pavyzdys |
        |---|--------|---------|
        | **PVM tarifų parametrai** | vertė : VATrate | 1 : 2000, 2 : 1800 |
        | **PVM kodų susiejimas** | VATcode : vertė | vat20 : 1, vat18 : 2 |
        | **Mokėjimo priemonės tipų susiejimas** | TenderType : vertė | Grynieji pinigai : 1, Kortelė : 2 |

        > [!NOTE]
        > Funkciniai jungčių profiliai nustatomi konkrečioje įmonėje. Jei planuojate naudoti tokį patį fiskalinės jungties ir finansinių dokumentų teikėjo derinį skirtingose įmonėse, sukurkite funkcinį jungties profilį kiekvienoje įmonėje.

    2. Puslapyje **Techniniai jungčių profiliai** (**Mažmeninė prekyba ir prekyba \> Kanalų sąranka \> Fiskalinė integracija \> Techniniai jungčių profiliai**) sukurkite techninį kiekvienos fiskalinės jungties profilį.

        1. Pasirinkite jungties pavadinimą.
        2. Pasirinkite jungties tipą. Įrenginiuose, kurie prijungti prie aparatūros stoties, pasirinkite **Vietos**.

            > [!NOTE]
            > Šiuo metu palaikomos tik vietos jungtys.

        Techniniame jungties profilyje pateiktų skirtukų **Įrenginys** ir **Parametrai** nustatymus galima keisti. Norėdami atkurti numatytuosius parametrus, kurie apibrėžti fiskalinės jungties konfigūracijoje, pasirinkite **Naujinti**. Kol įkeliama nauja XML konfigūracijos versija, gausite pranešimą, nurodantį, kad dabartinė fiskalinė jungtis arba finansinių dokumentų teikėjas jau yra naudojamas. Ši procedūra neperrašo neautomatinių pakeitimų, kurie anksčiau buvo atlikti funkciniuose jungčių profiliuose ir techniniuose jungčių profiliuose. Norėdami taikyti numatytąjį naujos konfigūracijos parametrų rinkinį, puslapyje **Funkciniai jungčių profiliai** arba puslapyje **Techniniai jungčių profiliai** pasirinkite **Naujinti**.

4. Sukurkite fiskalinių jungčių grupes.

    Fiskalinių jungčių grupė yra su identiškas funkcijas atliekančiomis ir tame pačiame fiskalinės registracijos proceso veiksme naudojamomis fiskalinėmis jungtimis susietų funkcinių profilių subrinkinys. Pavyzdžiui, jei mažmeninėje parduotuvėje galima naudoti kelis fiskalinio spausdintuvo modelius, tų fiskalinių spausdintuvų fiskalinės jungtys gali būti sujungtos į fiskalinių jungčių grupę.

    1. Puslapyje **Fiskalinių jungčių grupė** (**Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Fiskalinė integracija \> Fiskalinių jungčių grupė**) sukurkite naują fiskalinių jungčių grupę.
    2. Į jungčių grupę įtraukite funkcinių profilių. Skirtuke **Funkciniai profiliai** pasirinkite **Įtraukti** ir pasirinkite profilio numerį. Kiekviena fiskalinė jungčių grupės jungtis gali turėti tik vieną funkcinį profilį.
    3. Jei norite sustabdyti funkcinių profilių naudojimą, nustatykite funkcijos **Išjungti** parinktį **Taip**. Šis pakeitimas taikomas tik dabartinei jungčių grupei. Kitose jungčių grupėse galite ir toliau naudoti tą patį funkcinį profilį.

5. Sukurkite fiskalinės registracijos procesą.

    Fiskalinės registracijos procesas nusakomas registracijos veiksmų seka ir kiekviename veiksme naudojama jungčių grupe.

    1. Puslapyje **Fiskalinės registracijos procesas** (**Mažmeninė prekyba ir prekyba \> Kanalų sąranka \> Fiskalinė integracija \> Fiskalinės registracijos procesai**) sukurkite naują kiekvieno unikalaus fiskalinės registracijos proceso įrašą.
    2. Į procesą įtraukite registracijos veiksmus.

        1. Pasirinkite **Įtraukti**.
        2. Pasirinkite fiskalinės jungties tipą.
        3. Lauke **Grupės numeris** pasirinkite atitinkamą fiskalinių jungčių grupę.

6. Priskirkite fiskalinės registracijos proceso objektus EKA profiliams.

    1. Puslapyje **EKA funkcijų profiliai** (**Mažmeninė prekyba ir prekyba \> Kanalų sąranka \> EKA sąranka \> EKA profiliai \> Funkcijų profiliai**) priskirkite fiskalinės registracijos procesą EKA funkcijų profiliui. Pasirinkite **Redaguoti**, tada skirtuko **Fiskalinės registracijos procesas** lauke **Proceso numeris** pasirinkite procesą.
    2. Puslapyje **EKA aparatūros profilis** (**Mažmeninė prekyba ir prekyba \> Kanalų sąranka \> EKA sąranka \> EKA profiliai \> Funkcijų profiliai**) priskirkite techninius jungčių profilius aparatūros profiliui. Pasirinkite **Redaguoti**, įtraukite eilutę į skirtuką **Finansiniai periferiniai įrenginiai**, tada lauke **Profilio numeris** pasirinkite techninį jungties profilį.

    > [!NOTE]
    > Į tą patį aparatūros profilį galite įtraukti kelis techninius profilius. Tačiau aparatūros profilis arba EKA funkcijų profilis turėtų turėti tik vieną sankirtą su bet kuria fiskalinių jungčių grupe.

    Fiskalinės registracijos eigą nustato fiskalinės registracijos procesas ir kai kurie fiskalinės integracijos komponentų parametrai: „Commerce Runtime“ plėtinys, skirtas finansinių dokumentų teikėjui, ir aparatūros stoties plėtinys, skirtas fiskalinei jungčiai.

    - Finansinių dokumentų teikėjas iš anksto nustato įvykių ir operacijų prenumeratą fiskalinėje registracijoje.
    - Finansinių dokumentų teikėjas taip pat yra atsakingas už fiskalinių jungčių, naudojamų fiskalinėje registracijoje, nustatymą. Ji sugretina funkcinius jungčių profilius, kurie įtraukti į fiskalinių jungčių grupę, nurodytą esamame fiskalinė registracijos proceso veiksme, su techniniu jungties profiliu, kuris priskirtas aparatūros stoties, su kuria susietas EKA, aparatūros profiliui.
    - Finansinių dokumentų teikėjas naudoja duomenų susiejimo parametrus iš finansinių dokumentų teikėjo konfigūracijos, kad transformuotų operacijos / įvykio duomenis, pvz., mokesčius ir mokėjimus, kol generuojamas finansinis dokumentas.
    - Kai finansinių dokumentų teikėjas sugeneruoja finansinį dokumentą, fiskalinė jungtis gali siųsti jį nepakeistą į finansinį įrenginį arba išanalizuoti ir transformuoti į įrenginio programos programavimo sąsajos (API) komandų seką, atsižvelgiant į ryšį.

7. Puslapyje **Fiskalinės registracijos procesas** (**Mažmeninė prekyba ir prekyba \> Kanalų sąranka \> Fiskalinė integracija \> Fiskalinės registracijos procesai**) pasirinkite **Tikrinti**, kad patikrintumėte fiskalinės registracijos procesą.

    Rekomenduojame atlikti šio tipo tikrinimą toliau nurodytais atvejais.

    - Naujam registracijos procesui užbaigus atlikti visus nustatymus, įskaitant registracijos procesų priskyrimą EKA funkcijų profiliams ir aparatūros profiliams.
    - Atlikus esamo fiskalinės registracijos proceso pakeitimus, tie pakeitimai gali sukelti skirtingų fiskalinių jungčių pasirinkimą vykdymo metu (pvz., pakeitus fiskalinės registracijos proceso veiksmo jungčių grupę, įjungus funkcinį jungčių profilį jungčių grupėje arba įtraukus naują funkcinį jungties profilį į jungčių grupę).
    - Atlikę techninių jungčių profilių priskyrimo aparatūros šablonams pakeitimus.

8. Puslapyje **Paskirstymo grafikas** paleiskite **1070** ir **1090** užduotis, kad perkeltumėte duomenis į kanalo duomenų bazę.

## <a name="set-up-fiscal-texts-for-discounts"></a>Nuolaidų finansinio teksto nustatymas

Kai kuriais atvejais specialus tekstas turi būti išspausdintas ant finansinio kvito, jei taikoma nuolaida. Nuolaidų finansinį tekstą galite nustatyti puslapyje **Fiskalinių jungčių grupė** (**Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Fiskalinė integracija \> Fiskalinių jungčių grupė**).

- Jei neautomatinės nuolaidos taikomos EKA, turėtumėte nustatyti finansinį tekstą, taikomą informacijos kodui arba informacijos kodų grupei, nurodytai EKA funkcijų šablono informacijos kode **Produkto nuolaida**.

    1. Puslapyje **Fiskalinių jungčių grupė** pasirinkite **Finansinio kvito tekstas**.
    2. Skirtuke **Informacijos kodai** pasirinkite **Įtraukti** ir pasirinkite informacijos kodą arba informacijos kodų grupę.
    3. Lauke **Informacijos kodo numeris** pasirinkite reikšmę.
    4. Lauke **Antrinio kodo numeris** pasirinkite reikšmę, jei būtinas pasirinkto informacijos kodo antrinis kodas.
    5. Lauke **Finansinio kvito tekstas** nurodykite finansinį tekstą, kuris turi būti spausdinamas ant finansinio kvito.
    6. Nustatykite parinkties **Spausdinti vartotojo įvestį ant finansinio kvito** reikšmę **Taip**, kad perrašytumėte tekstą finansiniame kvite naudodami informaciją, kurią vartotojas pats įveda EKA. Ši pasirinktis taikoma tik informacijos kodams, kurių įvesties tipas yra **Tekstas**.

    > [!NOTE]
    > Galite nurodyti kelių informacijos kodų finansinį tekstą tokiems atvejams, kai naudojami informacijos kodų grupės, susiję informacijos kodai ir suaktyvinti informacijos kodai. Šiuose scenarijuose finansiniame kvite bus finansinis tekstas iš visų informacijos kodų, susietų su operacijos eilute, kurioje pritaikyta nuolaida.

- Jei nuolaida taikoma konkrečiam kanalui, turėtumėte nurodyti nuolaidos ID finansinį tekstą.

    1. Puslapyje **Fiskalinių jungčių grupė** pasirinkite **Finansinio kvito tekstas**.
    2. Skirtuke **Nuolaidos** pasirinkite **Įtraukti** ir pasirinkite nuolaidos ID.
    3. Lauke **Finansinio kvito tekstas** nurodykite finansinį tekstą, kuris turi būti spausdinamas ant finansinio kvito.

    > [!NOTE]
    > Jei kelios nuolaidos taikomos tai pačiai operacijos eilutei, finansiniame kvite bus finansinis tekstas iš visų nuolaidų, kurios susietos su ta operacijos eilute.

## <a name="set-error-handling-settings"></a>Klaidų tvarkymo parametrų nustatymas

Klaidų tvarkymo parinktys, teikiamos fiskalinėje integracijoje, nustatomos fiskalinės registracijos proceso metu. Daugiau informacijos apie fiskalinės integracijos klaidų tvarkymą žr. [Klaidų tvarkymas](fiscal-integration-for-retail-channel.md#error-handling).

1. Puslapyje **Fiskalinės registracijos procesas** (**Mažmeninė prekyba ir prekyba \> Kanalų sąranka \> Fiskalinė integracija \> Fiskalinės registracijos procesai**) galite sukurti toliau nurodytus kiekvieno fiskalinės registracijos proceso veiksmo parametrus.

    - **Leisti praleisti** – šis parametras įjungia parinktį **Praleisti** klaidų tvarkymo dialogo lange.
    - **Leisti pažymėti kaip užregistruotą** – šis parametras įjungia parinktį **Pažymėti kaip užregistruotą** klaidų tvarkymo dialogo lange.
    - **Tęsti esant klaidai** – jei šis parametras įjungtas, mokesčių registravimo procesą galima tęsti EKA registre, kai operacijos arba įvykio finansinis registravimas nepavyksta. Kitu atveju, norėdamas vykdyti kitos operacijos arba įvykio finansinį registravimą, operatorius turi kartoti nepavykusį finansinį registravimą, nepaisyti jo arba pažymėti operaciją ar įvykį kaip užregistruotą. Daugiau informacijos žr. [Nebūtinas finansinis registravimas](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Jei parametras **Tęsti įvykus klaidai** įjungtas, parametrai **Leisti nepaisyti** ir **Leisti pažymėti kaip užregistruotą** išjungiami automatiškai.

2. Norint naudoti parinktis **Nepaisyti** ir **Pažymėti kaip užregistruotą** klaidų tvarkymo dialogo lange, reikia teisės **Leisti nepaisyti registravimo arba pažymėti kaip užregistruotą**. Todėl puslapyje **Teisių grupės** (**Mažmeninė prekyba ir prekyba \> Darbuotojai \> Teisių grupės**) įjunkite teisę **Leisti nepaisyti registravimo arba pažymėti kaip užregistruotą**.
3. Parinktys **Praleisti** ir **Pažymėti kaip užregistruotą** operatoriams suteikia galimybę įvesti papildomą informaciją, kai fiskalinė registracija. Jei norite, kad ši funkcija būtų teikiama, turite nurodyti parinkčių **Praleisti** ir **Pažymėti kaip užregistruotą** informacijos kodus fiskalinių jungčių grupėje. Tada operatoriaus įvesta informacija įrašoma kaip informacijos kodo operacija, susieta su finansine operacija. Daugiau informacijos apie informacijos kodus žr. [Informacijos kodai ir informacijos kodų grupės](../info-codes-retail.md).

    > [!NOTE]
    > **Produkto** paleidiklio funkcija nepalaikoma informacijos koduose, kurie naudojami parinktyse **Praleisti** ir **Pažymėti kaip užregistruotą** fiskalinių jungčių grupėse.

    - Puslapio **Fiskalinių jungčių grupės** skirtuke **Informacijos kodai** pasirinkite informacijos kodus arba informacijos kodų grupes laukuose **Praleisti** ir **Pažymėti kaip užregistruotą**.

    > [!NOTE]
    > Vienas finansinis dokumentas ir vienas nefinansinis dokumentas gali būti sugeneruoti bet kuriuo fiskalinės registracijos proceso veiksmu. Finansinio dokumento teikėjo plėtinys nurodo kiekvieno tipo operaciją arba įvykį, susijusį su finansiniais ar nefinansiniais dokumentais. Klaidų tvarkymo priemonė taikoma tik finansiniams dokumentams.
    >
    > - **Finansinis dokumentas** – privalomas dokumentas, kuris turi būti užregistruoti sėkmingai (pavyzdžiui, finansinis kvitas).
    > - **Nefinansinis dokumentas** – papildomas operacijos arba įvykio dokumentas (pvz., dovanų kortelės kvitas).

4. Jei operatorius privalo galėti toliau apdoroti dabartinę operaciją (pvz., kurti arba baigti operaciją) po to, kai įvyksta būsenos tikrinimo klaida, turėtumėte įjungti teisę **Leisti nepaisyti būsenos tikrinimo klaidos** puslapyje **Teisių grupės** (**Mažmeninė prekyba ir prekyba \> Darbuotojai \> Teisių grupės**). Daugiau informacijos apie būsenos tikrinimo procedūrą žr. [Finansinio registravimo būsenos tikrinimas](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Finansinių X / Z ataskaitų iš nustatymas EKA

Norėdami vykdyti finansines X / Z ataskaitas iš EKA, į EKA maketą turėtumėte įtraukti naujų mygtukų.

- Puslapyje **Mygtukynai** vykdykite instrukcijas, nurodytas [EKA operacijų įtraukimas į EKA maketus naudojant mygtukynų dizaino įrankį](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters), kad įdiegtumėte dizaino įrankį ir atnaujintumėte EKA maketą.

    1. Pasirinkite atnaujintiną maketą. 
    2. Įtraukite naują mygtuką ir nustatykite mygtuko **Spausdinti finansinį X** ypatybes.
    3. Įtraukite naują mygtuką ir nustatykite mygtuko **Spausdinti finansinį Z** ypatybes.
    4. Puslapyje **Paskirstymo grafikas** paleiskite **1090** užduotį, kad perkeltumėte pakeitimus į kanalo duomenų bazę.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Rankinio atidėtos finansinio registravimo vykdymo įjungimas

Norėdami įjungti neautomatinį atidėto finansinio registravimo vykdymą, turėtumėte įtraukti naują mygtuką į EKA maketą.

- Puslapyje **Mygtukynai** vykdykite instrukcijas, nurodytas [EKA operacijų įtraukimas į EKA maketus naudojant mygtukynų dizaino įrankį](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters), kad įdiegtumėte dizaino įrankį ir atnaujintumėte EKA maketą.

    1. Pasirinkite atnaujintiną maketą.
    2. Įtraukite naują mygtuką ir nustatykite mygtuko **Baigti finansinio registravimo procesą** ypatybę.
    3. Puslapyje **Paskirstymo grafikas** paleiskite **1090** užduotį, kad perkeltumėte pakeitimus į kanalo duomenų bazę.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]