---
title: Prekybos kanalų fiskalinės integracijos nustatymas
description: Šioje temoje pateikiamos prekybos kanalų fiskalinės integracijos nustatymo gairės.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: e4b0b9f7eb4fb0ffab3237459d85ea92c83dd206
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462171"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Prekybos kanalų fiskalinės integracijos nustatymas

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiamos prekybos kanalų fiskalinės integracijos nustatymo gairės. Daugiau informacijos apie fiskalinę integraciją žr. [Prekybos kanalų fiskalinės integracijos apžvalga](fiscal-integration-for-retail-channel.md).

## <a name="set-up-commerce-parameters"></a>"Commerce" parametrų nustatymas

1. Puslapio **Bendrai naudojami prekybos parametrai** skirtuke **Bendra** nustatykite parinkties **Įjungti fiskalinę integraciją** reikšmę **Taip**.
1. Skirtuke **Numeracijos** nurodykite tolesnių nuorodų numeracijas.

    - Fiskalinio techninio profilio numeris
    - Fiskalinių jungčių grupės numeris
    - Registracijos proceso numeris

1. Puslapyje **Prekybos parametrai** nurodykite fiskalinio funkcinio profilio numeraciją.

    > [!NOTE]
    > Numeracijos nėra būtinos. Visų fiskalinės integracijos objektų numerius galima generuoti naudojant numeraciją arba neautomatiniu būdu.

## <a name="set-up-a-fiscal-registration-process"></a>Fiskalinės registracijos proceso nustatymas

Fiskalinės integracijos nustatymo procesas apima toliau nurodytas užduotis.

- Sukonfigūruoti fiskalines jungtis, kurios nurodo finansinius įrenginius arba paslaugas, naudojamas fiskalinio registravimo tikslais, pvz., fiskaliniai spausdintuvai.
- Sukonfigūruoti dokumentų teikėjus, generuojančius finansinius dokumentus, kuriuos fiskalinės jungtys užregistruos finansiniuose įrenginiuose arba paslaugose.
- Sukonfigūruoti fiskalinės registracijos procesą, kuris apibrėžia fiskalinės registracijos veiksmus ir fiskalines jungtis bei finansinių dokumentų teikėjus, naudojamus kiekviename veiksme.
- Priskirti fiskalinės registracijos procesus elektroninio kasos aparato (EKA) funkcijų profiliams.
- Priskirti jungčių techninius profilius aparatūros profiliams.
- EKA aparatūros ar funkcijų šablonams priskirkite jungties techninius profilius.

### <a name="upload-configurations-of-fiscal-document-providers"></a>Įkelti finansinių dokumentų teikėjų konfigūracijas

Finansinių dokumentų teikėjas generuoja finansinius dokumentus, kuriuose nurodomos prekybos operacijos ir įvykiai, užregistruoti EKA tokiu formatu, koks naudojamas sąveikaujant su finansiniu įrenginiu arba paslauga. Pvz., finansinių dokumentų teikėjas gali generuoti finansinio kvito versiją XML formatu.

Norėdami įkelti finansinių dokumentų teikėjų konfigūracijas, atlikite šiuos veiksmus.

1. Programos "Commerce Headquarters" eikite į puslapį **Iždo dokumentų teikėjai** ("Retail" ir "**Commerce \> Channel" nustatymo " \> Fiscal integration \> Fiscal" dokumentų teikėjai**).
1. Nusiųsti XML konfigūraciją kiekvienam įrenginiui ar paslaugai, kurią planuojate naudoti.

> [!TIP]
> Pasirinkdami **Peržiūrėti** galite peržiūrėti visus funkcinius profilius, susijusius su dabartiniu finansinių dokumentų teikėju.

> [!NOTE]
> Duomenų susiejimas laikomas fiskalinio dokumento teikėjo dalis. Norėdami nustatyti skirtingus tos pačios jungties duomenų susiejimus (pvz., nuo būsenos priklausančius reguliatorius), turėtumėte sukurti skirtingus fiskalinių dokumentų teikėjus.

### <a name="upload-configurations-of-fiscal-connectors"></a>Įkelti finansinių jungčių konfigūracijas

Fiskalinė jungtis yra atsakinga už ryšį su finansiniu įrenginiu arba paslauga. Pvz., fiskalinė jungtis gali siųsti finansinį kvitą, kurį finansinių dokumentų teikėjas sukūrė XML formatu, fiskaliniam spausdintuvui. Daugiau informacijos apie finansinio integravimo komponentus ieškokite finansinio [įrenginių ir paslaugų finansinio integravimo procesas ir finansinio integravimo pavyzdžiai](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

Norėdami įkelti finansinių jungčių konfigūracijas, atlikite šiuos veiksmus.

1. Programos "Commerce Headquarters" eikite į "**Fiscal Connector" puslapį** ("Retail" ir "**Commerce \> Channel" \> nustatymo "Fiscal integration \> Fiscal Connectors").**
1. Nusiųsti KIEKVIENO įrenginio ar paslaugos, kurią planuojate naudoti finansinio integravimo tikslais, XML konfigūraciją.

> [!TIP]
> Pasirinkdami **Peržiūrėti** galite peržiūrėti visus funkcinius ir techninius profilius, susijusius su dabartine fiskaline jungtimi.

Fiskalinių jungčių ir finansinių dokumentų teikėjų konfigūracijų pavyzdžių žr. [Mažmeninės prekybos SDK fiskalinės integracijos pavyzdžiai](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-commerce-sdk).

### <a name="create-connector-functional-profiles"></a>Sukurti jungties funkcinius profilius

Norėdami sukurti jungties funkcinius profilius, atlikite šiuos veiksmus.

1. Programos "Commerce Headquarters" eikite į jungties **funkcinių profilių puslapį** ("Retail" ir "**Commerce \> Channel" \> nustatymo finansinio integravimo \> jungties funkciniai profiliai**).
1. Kiekvienai fiskalinės jungties ir finansinio dokumento teikėjo kombinacijai, susijusiai su šia fiskaline jungtimi, sukurkite jungties funkcinį profilį, atlikite šiuos veiksmus:

    1. Pasirinkite jungties pavadinimą.
    1. Pasirinkite dokumento teikėją.

#### <a name="change-data-mapping-parameters-in-a-connector-functional-profile"></a>Keisti duomenų susiejimo parametrus jungties funkcinėje profilyje

Funkciniame jungties profilyje galite keisti duomenų susiejimo parametrus. Toliau esančioje lentelėje pateikiami kai kurie duomenų susiejimo parametrų pavyzdžiai jungties funkciniame profilyje.

| Parametras | Formatuoti | Pavyzdys |
|-----------|--------|---------|
| PVM tarifų parametrai | vertė : VATrate | 1 : 2000, 2 : 1800 |
| PVM kodų susiejimas | VATcode : vertė | vat20 : 1, vat18 : 2 |
| Mokėjimo priemonės tipų susiejimas | TenderType : vertė | Grynieji pinigai : 1, Kortelė : 2 |

Norėdami atkurti numatytuosius parametrus, kurie apibrėžti finansinio dokumento teikėjo konfigūracijoje, **pasirinkite Naujinti** connector **funkcinių profilių** puslapyje.

> [!NOTE]
> Funkciniai jungčių profiliai nustatomi konkrečioje įmonėje. Jei planuojate skirtingoms įmonėms naudoti tą patį finansinio jungties ir finansinio dokumento teikėjo derinį, turite sukurti kiekvienos įmonės jungties funkcinį profilį.

### <a name="create-connector-technical-profiles"></a>Jungties techninių profilių kūrimas

Norėdami sukurti jungties techninius profilius, atlikite šiuos veiksmus.

1. Programos "Commerce Headquarters" eikite į jungties **techninių profilių puslapį** ("Retail" ir "**Commerce \> Channel" \> nustatymo "Fiscal integration \> Connector" techniniai profiliai**).
1. Sukurkite kiekvienos fiskalinės jungties techninio profilio jungtį, atlikite šiuos veiksmus:

    1. Pasirinkite jungties pavadinimą.
    1. Pasirinkite jungties tipą:

        - Jei norite naudoti įrenginius arba paslaugas, kurie prijungti prie aparatūros stoties arba yra vietiniame tinkle, pasirinkite **Vietinis**.
        - Norėdami naudotis išorinėmis paslaugomis, pasirinkite **Išorinis**.
        - Norėdami su "Commerce runtime" () naudoti vidines jungtis CRT, pasirinkite **Vidinis**. 

    1. Pasirinkite jungties vietą:

        - Jei jungtis yra Aparatūros stotis, pasirinkite Aparatūros **stotis**.
        - Jei jungtis yra EKA kasos aparate, pasirinkite **Registras**.

Techniniame jungties profilyje pateiktų skirtukų **Įrenginys** ir **Parametrai** nustatymus galima keisti. Norėdami atkurti numatytuosius parametrus, kurie apibrėžti fiskalinės jungties konfigūracijoje, pasirinkite **Naujinti**. Kol įkeliama nauja XML konfigūracijos versija, gausite pranešimą, kuriame teigiama, kad dabartinė fiskalinė jungtis arba finansinio dokumento teikėjas jau naudojamas. Ši procedūra neperrašo neautomatinių pakeitimų, kurie anksčiau buvo atlikti funkciniuose jungčių profiliuose ir techniniuose jungčių profiliuose. Norėdami taikyti naujos konfigūracijos numatytąjį parametrų rinkinį, **·** **·** **pasirinkite Naujinti puslapyje Jungties funkciniai profiliai arba Jungties techninių profilių** puslapyje.

Jei turite nustatyti konkrečius atskiro EKA kasos aparato arba parduotuvės parametrus, atlikite šiuos veiksmus.

1. Pasirinkite nepaisymo **meniu** elementą.
1. **Puslapyje Perrašyti sukurkite** naują įrašą.
1. Pasirinkite parduotuvę arba EKA kasos aparatą. Galite nepaisyti pasirinkto atskiro EKA kasos aparato arba visų EKA kasos aparatų atskiroje parduotuvėje pasirinkto techninio profilio parametrų.
1. Skirtuke **Įrenginys** įveskite pasirinkto EKA kasos aparato arba parduotuvės parametrus.

### <a name="create-fiscal-connector-groups"></a>Kurti finansinių jungčių grupes

Fiskalinių jungčių grupė yra su identiškas funkcijas atliekančiomis ir tame pačiame fiskalinės registracijos proceso veiksme naudojamomis fiskalinėmis jungtimis susietų funkcinių profilių subrinkinys. Pavyzdžiui, jei mažmeninėje parduotuvėje galima naudoti kelis fiskalinio spausdintuvo modelius, tų fiskalinių spausdintuvų fiskalinės jungtys gali būti sujungtos į fiskalinių jungčių grupę.

Norėdami sukurti "Fiscal Connector" grupę, atlikite šiuos veiksmus.

1. Eikite į " **Fiscal Connector" grupės puslapį** ("Retail" ir "**Commerce \> Channel" nustatymo " \> Fiscal integration \> Fiscal Connector" grupės**).
1. Sukurkite naują "Fiscal Connector" grupę.
1. Į jungčių grupę įtraukite funkcinių profilių. Skirtuke **Funkciniai profiliai** pasirinkite **Įtraukti** ir pasirinkite profilio numerį. Kiekviena fiskalinė jungčių grupės jungtis gali turėti tik vieną funkcinį profilį.
1. Jei norite sustabdyti funkcinių profilių naudojimą, nustatykite funkcijos **Išjungti** parinktį **Taip**. Šis pakeitimas taikomas tik dabartinei jungčių grupei. Kitose jungčių grupėse galite ir toliau naudoti tą patį funkcinį profilį.

### <a name="create-a-fiscal-registration-process"></a>Sukurti finansinio registravimo procesą

Fiskalinės registracijos procesas nusakomas registracijos veiksmų seka ir kiekviename veiksme naudojama jungčių grupe.

Norėdami sukurti finansinio registravimo procesą, atlikite šiuos veiksmus.

1. Programos "Commerce Headquarters" eikite į puslapį **Finansinio registravimo procesas** ("Retail" ir "**Commerce \> Channel" nustatymo \> finansinio integravimo \> finansinio registravimo procesai**).
1. Sukurkite naują įrašą kiekvienam unikaliam finansinio registravimo procesui.
1. Įtraukite registracijos veiksmus į procesą, atlikite šiuos veiksmus:

    1. Pasirinkite **Įtraukti**.
    1. Pasirinkite fiskalinės jungties tipą.
    1. Lauke **Grupės numeris** pasirinkite atitinkamą fiskalinių jungčių grupę.

### <a name="assign-entities-of-the-fiscal-registration-process-to-pos-profiles"></a>Priskirti finansinio registravimo proceso objektus EKA profiliams

Norėdami priskirti finansinio registravimo proceso objektus EKA profiliams, atlikite šiuos veiksmus.

1. "Commerce Headquarters" eikite į **EKA funkcijų šablonų** puslapį ("Retail" ir "**Commerce \> Channel setup \> POS \> " nustatymo EKA \> šablonų funkcijų profiliai**). 
1. EKA funkcijų šablonui priskirti finansinio registravimo procesą.
1. Pasirinkite **Redaguoti**, tada skirtuko **Fiskalinės registracijos procesas** lauke **Proceso numeris** pasirinkite procesą.
1. Skirtuke **Fiskalinės paslaugos** pasirinkite jungties techninius profilius su jungties vieta **Registras**.
1. Eikite į **EKA aparatūros šablono puslapį** ("Retail" ir "**Commerce \> Channel setup \> POS" nustatymo \> EKA šablonų aparatūros \> profiliai**).
1. Aparatūros šablonui priskirkite jungties techninius šablonus. 
1. Pasirinkite **Redaguoti**, tada skirtuke Finansiniai **išoriniai įrenginiai** pridėkite eilutę. 
1. Lauke Profilio **numeris** pasirinkite jungties techninio profilio.
1. Skirtuke **Finansiniai išoriniai įrenginiai** pasirinkite jungties techninius profilius su jungties vieta Aparatūros **stotis**.

> [!NOTE]
> Į tą patį aparatūros profilį galite įtraukti kelis techninius profilius. Tačiau aparatūros profilis arba EKA funkcijų profilis turėtų turėti tik vieną sankirtą su bet kuria fiskalinių jungčių grupe.

Finansinio registravimo eigą nustato finansinio registravimo procesas ir kai kurie finansinio integravimo komponentų parametrai: CRT finansinio dokumento teikėjo plėtinys ir finansinio jungties "Hardware" stoties plėtinys.

- Finansinių dokumentų teikėjas iš anksto nustato įvykių ir operacijų prenumeratą fiskalinėje registracijoje.
- Finansinių dokumentų teikėjas taip pat yra atsakingas už fiskalinių jungčių, naudojamų fiskalinėje registracijoje, nustatymą. Ji sugretina funkcinius jungčių profilius, kurie įtraukti į fiskalinių jungčių grupę, nurodytą esamame fiskalinė registracijos proceso veiksme, su techniniu jungties profiliu, kuris priskirtas aparatūros stoties, su kuria susietas EKA, aparatūros profiliui.
- Finansinių dokumentų teikėjas naudoja duomenų susiejimo parametrus iš finansinių dokumentų teikėjo konfigūracijos, kad transformuotų operacijos / įvykio duomenis, pvz., mokesčius ir mokėjimus, kol generuojamas finansinis dokumentas.
- Kai finansinių dokumentų teikėjas sugeneruoja finansinį dokumentą, fiskalinė jungtis gali siųsti jį nepakeistą į finansinį įrenginį arba išanalizuoti ir transformuoti į įrenginio programos programavimo sąsajos (API) komandų seką, atsižvelgiant į ryšį.

### <a name="set-up-registers-with-fiscal-registration-restrictions"></a>Nustatyti registrus su finansinio registravimo apribojimais

Galite pasirinkti registrus, kuriuose draudžiama finansų registracija, pvz., tais atvejais, kai turite pateikti tik nefinansinių operacijų, pvz., produktų katalogo ieškos, klientų peržvalgos ar šių įrenginių operacijų juodraščio kūrimo atvejus.

Norėdami nustatyti registrus, kuriuose taikomi finansinio registravimo apribojimai, atlikite šiuos veiksmus.

1. Commerce Headquarters eikite į "Retail" **ir "Commerce \> Channel" nustatymo " \> Fiscal integration \> Fiscal" registravimo procesus**.
1. Pasirinkite reikiamą procesą.
1. Pasirinkite EKA **registrus su finansinio proceso apribojimų skirtuku**.
1. Įtraukite registrus su finansinio proceso apribojimais, pagal poreikį.

### <a name="validate-the-fiscal-registration-process"></a>Tikrinti finansinio registravimo procesą

Rekomenduojama patikrinti finansinio registravimo procesą šiais atvejais:

- Baigėte visus naujo registracijos proceso parametrus. Šie parametrai apima registravimo procesų priskyrimą EKA funkcijų šablonams ir aparatūros šablonams.
- Atlikote esamo finansinio registravimo proceso pakeitimus, todėl šie pakeitimai vykdymo metu gali pasirinkti kitą fiskalinę jungtį. (Pvz., pakeitėte finansinio registravimo proceso veiksmo jungties grupę, įgalinote jungties funkcinį profilį jungties grupėje arba įtraukėte naują jungties funkcinį profilį į jungties grupę.)
- Atlikote jungties techninių profilių priskyrimo aparatūros šablonams pakeitimus.

Norėdami patikrinti finansinio registravimo procesą, atlikite šiuos veiksmus.

1. Programos "Commerce Headquarters" eikite į puslapį **Finansinio registravimo procesas** ("Retail" ir "**Commerce \> Channel" nustatymo \> finansinio integravimo \> finansinio registravimo procesai**).
1. Pasirinkite **Tikrinti,** kad būtų patikrintas finansinio registravimo procesas.
1. Puslapyje **Paskirstymo grafikas** paleiskite **1070** ir **1090** užduotis, kad perkeltumėte duomenis į kanalo duomenų bazę.

## <a name="set-up-fiscal-texts-for-discounts"></a>Nuolaidų finansinio teksto nustatymas

Kai kuriais atvejais specialus tekstas turi būti išspausdintas ant finansinio kvito, jei taikoma nuolaida. Nuolaidų finansinį tekstą galite nustatyti puslapyje **Fiskalinių jungčių grupė** (**Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Fiskalinė integracija \> Fiskalinių jungčių grupė**).

- Jei neautomatinės nuolaidos taikomos EKA, turėtumėte nustatyti finansinį tekstą, taikomą informacijos kodui arba informacijos kodų grupei, nurodytai EKA funkcijų šablono informacijos kode **Produkto nuolaida**.

    1. Puslapyje **Fiskalinių jungčių grupė** pasirinkite **Finansinio kvito tekstas**.
    1. Skirtuke **Informacijos kodai** pasirinkite **Įtraukti** ir pasirinkite informacijos kodą arba informacijos kodų grupę.
    1. Lauke **Informacijos kodo numeris** pasirinkite reikšmę.
    1. Lauke **Antrinio kodo numeris** pasirinkite reikšmę, jei būtinas pasirinkto informacijos kodo antrinis kodas.
    1. Lauke **Finansinio kvito tekstas** nurodykite finansinį tekstą, kuris turi būti spausdinamas ant finansinio kvito.
    1. Nustatykite parinkties **Spausdinti vartotojo įvestį ant finansinio kvito** reikšmę **Taip**, kad perrašytumėte tekstą finansiniame kvite naudodami informaciją, kurią vartotojas pats įveda EKA. Ši pasirinktis taikoma tik informacijos kodams, kurių įvesties tipas yra **Tekstas**.

    > [!NOTE]
    > Galite nurodyti kelių informacijos kodų finansinį tekstą tokiems atvejams, kai naudojami informacijos kodų grupės, susiję informacijos kodai ir suaktyvinti informacijos kodai. Šiuose scenarijuose finansiniame kvite bus finansinis tekstas iš visų informacijos kodų, susietų su operacijos eilute, kurioje pritaikyta nuolaida.

- Jei nuolaida taikoma konkrečiam kanalui, turėtumėte nurodyti nuolaidos ID finansinį tekstą.

    1. Puslapyje **Fiskalinių jungčių grupė** pasirinkite **Finansinio kvito tekstas**.
    1. Skirtuke **Nuolaidos** pasirinkite **Įtraukti** ir pasirinkite nuolaidos ID.
    1. Lauke **Finansinio kvito tekstas** nurodykite finansinį tekstą, kuris turi būti spausdinamas ant finansinio kvito.

    > [!NOTE]
    > Jei kelios nuolaidos taikomos tai pačiai operacijos eilutei, finansiniame kvite bus finansinis tekstas iš visų nuolaidų, kurios susietos su ta operacijos eilute.

## <a name="set-error-handling-settings"></a>Klaidų tvarkymo parametrų nustatymas

Klaidų tvarkymo parinktys, teikiamos fiskalinėje integracijoje, nustatomos fiskalinės registracijos proceso metu. Daugiau informacijos apie fiskalinės integracijos klaidų tvarkymą žr. [Klaidų tvarkymas](fiscal-integration-for-retail-channel.md#error-handling).

Norėdami nustatyti klaidų tvarkymo parametrus, atlikite šiuos veiksmus.

1. Puslapyje **Fiskalinės registracijos procesas** (**Mažmeninė prekyba ir prekyba \> Kanalų sąranka \> Fiskalinė integracija \> Fiskalinės registracijos procesai**) galite sukurti toliau nurodytus kiekvieno fiskalinės registracijos proceso veiksmo parametrus.

    - **Leisti praleisti** – šis parametras įjungia parinktį **Praleisti** klaidų tvarkymo dialogo lange.
    - **Leisti pažymėti kaip užregistruotą** – šis parametras įjungia parinktį **Pažymėti kaip užregistruotą** klaidų tvarkymo dialogo lange.
    - **Leisti atidėti** – šis parametras įgalina **parinktį Atidėti** klaidų tvarkymo dialogo lange.
    - **Tęsti esant klaidai** – jei šis parametras įjungtas, mokesčių registravimo procesą galima tęsti EKA registre, kai operacijos arba įvykio finansinis registravimas nepavyksta. Kitu atveju, norėdamas vykdyti kitos operacijos arba įvykio finansinį registravimą, operatorius turi kartoti nepavykusį finansinį registravimą, nepaisyti jo arba pažymėti operaciją ar įvykį kaip užregistruotą. Daugiau informacijos žr. [Nebūtinas finansinis registravimas](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Jei parametras **Tęsti įvykus klaidai** įjungtas, parametrai **Leisti nepaisyti** ir **Leisti pažymėti kaip užregistruotą** išjungiami automatiškai.

1. Norint **praleisti** ir **pažymėti kaip registruotus** parinktis dialogo lange klaidų tvarkymas, **reikia įgalinti registraciją praleisti arba pažymėti kaip** registruotą teisę. Norėdami įjungti šią teisę, **eikite į teisių grupių puslapį (** Mažmeninės **\> prekybos ir komercijos darbuotojų teisių grupės \>)** **ir nustatykite parinktį Leisti praleisti registravimą arba pažymėkite kaip užregistruotą parinktį kaip** Taip **.**
1. Dialogo **lange Klaidų** tvarkymas pasirinkus Atidėti reikia įgalinti **teisę Leisti** atidėti. Norėdami įjungti teisę, eikite į teisių **grupių** puslapį (**Mažmeninės prekybos \>\> ir komercijos darbuotojų teisių grupės**) **ir nustatykite** parinktį Leisti atidėti kaip **Taip**.
1. Pasirinktys **Praleisti**, Pažymėti **kaip užregistruotos** ir **Atidėti leidžia operatoriams** įvesti papildomą informaciją, kai nepavyksta užregistruoti iždo. Norėdami, kad ši funkcija būtų galima, finansinių **·** **jungčių** grupėje **turite nurodyti žymės langelius Praleisti,** Pažymėti kaip užregistruotus ir Atidėti informacijos kodus. Tada operatoriaus įvesta informacija įrašoma kaip informacijos kodo operacija, susieta su finansine operacija. Daugiau informacijos apie informacijos kodus žr. [Informacijos kodai ir informacijos kodų grupės](../info-codes-retail.md).

    > [!NOTE]
    > **Produkto** paleidiklio funkcija nepalaikoma informacijos koduose, kurie naudojami parinktyse **Praleisti** ir **Pažymėti kaip užregistruotą** fiskalinių jungčių grupėse.

    - Skirtuko Informacijos **kodai puslapyje** **·** **Iždo jungčių grupė pasirinkite informacijos kodus arba informacijos kodų grupes laukuose Praleisti**, **Pažymėti** kaip registruotus **ir Atidėti.**

    > [!NOTE]
    > Vienas finansinis dokumentas ir vienas nefinansinis dokumentas gali būti sugeneruoti bet kuriuo fiskalinės registracijos proceso veiksmu. Finansinio dokumento teikėjo plėtinys nurodo kiekvieno tipo operaciją arba įvykį, susijusį su finansiniais ar nefinansiniais dokumentais. Klaidų tvarkymo priemonė taikoma tik finansiniams dokumentams.
    >
    > - **Finansinis dokumentas** – privalomas dokumentas, kuris turi būti užregistruoti sėkmingai (pavyzdžiui, finansinis kvitas).
    > - **Nefinansinis dokumentas** – papildomas operacijos arba įvykio dokumentas (pvz., dovanų kortelės kvitas).

1. Jei operatorius privalo galėti toliau apdoroti dabartinę operaciją (pvz., kurti arba baigti operaciją) po to, kai įvyksta būsenos tikrinimo klaida, turėtumėte įjungti teisę **Leisti nepaisyti būsenos tikrinimo klaidos** puslapyje **Teisių grupės** (**Mažmeninė prekyba ir prekyba \> Darbuotojai \> Teisių grupės**). Daugiau informacijos apie būsenos tikrinimo procedūrą žr. [Finansinio registravimo būsenos tikrinimas](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Finansinių X / Z ataskaitų iš nustatymas EKA

Norėdami vykdyti finansines X / Z ataskaitas iš EKA, į EKA maketą turėtumėte įtraukti naujų mygtukų.

- Puslapyje **Mygtukynai** vykdykite instrukcijas, nurodytas [EKA operacijų įtraukimas į EKA maketus naudojant mygtukynų dizaino įrankį](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters), kad įdiegtumėte dizaino įrankį ir atnaujintumėte EKA maketą.

    1. Pasirinkite atnaujintiną maketą. 
    1. Įtraukite naują mygtuką ir nustatykite mygtuko **Spausdinti finansinį X** ypatybes.
    1. Įtraukite naują mygtuką ir nustatykite mygtuko **Spausdinti finansinį Z** ypatybes.
    1. Puslapyje **Paskirstymo grafikas** paleiskite **1090** užduotį, kad perkeltumėte pakeitimus į kanalo duomenų bazę.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Rankinio atidėtos finansinio registravimo vykdymo įjungimas

Norėdami įjungti neautomatinį atidėto finansinio registravimo vykdymą, turėtumėte įtraukti naują mygtuką į EKA maketą.

- Puslapyje **Mygtukynai** vykdykite instrukcijas, nurodytas [EKA operacijų įtraukimas į EKA maketus naudojant mygtukynų dizaino įrankį](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters), kad įdiegtumėte dizaino įrankį ir atnaujintumėte EKA maketą.

    1. Pasirinkite atnaujintiną maketą.
    1. Įtraukite naują mygtuką ir nustatykite mygtuko **Baigti finansinio registravimo procesą** ypatybę.
    1. Puslapyje **Paskirstymo grafikas** paleiskite **1090** užduotį, kad perkeltumėte pakeitimus į kanalo duomenų bazę.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
