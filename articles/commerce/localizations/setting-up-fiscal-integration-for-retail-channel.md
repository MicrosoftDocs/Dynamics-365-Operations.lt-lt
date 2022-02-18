---
title: Prekybos kanalų fiskalinės integracijos nustatymas
description: Šioje temoje pateikiamos prekybos kanalų fiskalinės integracijos nustatymo gairės.
author: EvgenyPopovMBS
ms.date: 01/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: fd37934e1ebd103d66c5181e0bfb75047f4cb6a3
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076968"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Prekybos kanalų fiskalinės integracijos nustatymas

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šioje temoje pateikiamos prekybos kanalų fiskalinės integracijos nustatymo gairės. Daugiau informacijos apie fiskalinę integraciją žr. [Prekybos kanalų fiskalinės integracijos apžvalga](fiscal-integration-for-retail-channel.md).

## <a name="set-up-commerce-parameters"></a>Nustatykite prekybos parametrus

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

### <a name="upload-configurations-of-fiscal-document-providers"></a>Įkelti fiskalinių dokumentų teikėjų konfigūracijas

Finansinių dokumentų teikėjas generuoja finansinius dokumentus, kuriuose nurodomos prekybos operacijos ir įvykiai, užregistruoti EKA tokiu formatu, koks naudojamas sąveikaujant su finansiniu įrenginiu arba paslauga. Pvz., finansinių dokumentų teikėjas gali generuoti finansinio kvito versiją XML formatu.

Norėdami įkelti fiskalinių dokumentų teikėjų konfigūracijas, atlikite šiuos veiksmus.

1. Prekybos būstinėje eikite į **Fiskalinių dokumentų teikėjai** puslapis (**Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinių dokumentų teikėjai**).
1. Įkelkite XML konfigūraciją kiekvienam įrenginiui ar paslaugai, kurią planuojate naudoti.

> [!TIP]
> Pasirinkdami **Peržiūrėti** galite peržiūrėti visus funkcinius profilius, susijusius su dabartiniu finansinių dokumentų teikėju.

> [!NOTE]
> Duomenų susiejimas laikomas fiskalinio dokumento teikėjo dalis. Norėdami nustatyti skirtingus tos pačios jungties duomenų susiejimus (pvz., nuo būsenos priklausančius reguliatorius), turėtumėte sukurti skirtingus fiskalinių dokumentų teikėjus.

### <a name="upload-configurations-of-fiscal-connectors"></a>Įkelti fiskalinių jungčių konfigūracijas

Fiskalinė jungtis yra atsakinga už ryšį su finansiniu įrenginiu arba paslauga. Pvz., fiskalinė jungtis gali siųsti finansinį kvitą, kurį finansinių dokumentų teikėjas sukūrė XML formatu, fiskaliniam spausdintuvui. Daugiau informacijos apie fiskalinės integracijos komponentus žr [Fiskalinės registracijos procesas ir fiskalinės integracijos pavyzdžiai fiskaliniams įrenginiams ir paslaugoms](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

Norėdami įkelti fiskalinių jungčių konfigūracijas, atlikite šiuos veiksmus.

1. Prekybos būstinėje eikite į **Fiskalinės jungtys** puslapis (**Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinės jungtys**).
1. Įkelkite XML konfigūraciją kiekvienam įrenginiui ar paslaugai, kurią planuojate naudoti mokesčių integravimo tikslais.

> [!TIP]
> Pasirinkdami **Peržiūrėti** galite peržiūrėti visus funkcinius ir techninius profilius, susijusius su dabartine fiskaline jungtimi.

Fiskalinių jungčių ir finansinių dokumentų teikėjų konfigūracijų pavyzdžių žr. [Mažmeninės prekybos SDK fiskalinės integracijos pavyzdžiai](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-commerce-sdk).

### <a name="create-connector-functional-profiles"></a>Sukurkite jungčių funkcinius profilius

Norėdami sukurti jungties funkcinius profilius, atlikite šiuos veiksmus.

1. Prekybos būstinėje eikite į **Jungčių funkciniai profiliai** puslapis (**Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Jungčių funkciniai profiliai**).
1. Kiekvienam fiskalinės jungties ir mokesčių dokumentų teikėjo deriniui, susijusiam su šia fiskaline jungtimi, sukurkite jungties funkcinį profilį atlikdami šiuos veiksmus:

    1. Pasirinkite jungties pavadinimą.
    1. Pasirinkite dokumento teikėją.

#### <a name="change-data-mapping-parameters-in-a-connector-functional-profile"></a>Keiskite duomenų atvaizdavimo parametrus jungties funkciniame profilyje

Funkciniame jungties profilyje galite keisti duomenų susiejimo parametrus. Šioje lentelėje pateikiami keli jungties funkcinio profilio duomenų atvaizdavimo parametrų pavyzdžiai.

| Parametras | Formatuoti | Pavyzdys |
|-----------|--------|---------|
| PVM tarifų parametrai | vertė : VATrate | 1 : 2000, 2 : 1800 |
| PVM kodų susiejimas | VATcode : vertė | vat20 : 1, vat18 : 2 |
| Mokėjimo priemonės tipų susiejimas | TenderType : vertė | Grynieji pinigai : 1, Kortelė : 2 |

Norėdami atkurti numatytuosius parametrus, apibrėžtus fiskalinio dokumento teikėjo konfigūracijoje, pasirinkite **Atnaujinti** ant **Jungčių funkciniai profiliai** puslapį.

> [!NOTE]
> Funkciniai jungčių profiliai nustatomi konkrečioje įmonėje. Jei planuojate naudoti tą patį fiskalinės jungties ir fiskalinių dokumentų teikėjo derinį skirtingoms įmonėms, kiekvienai įmonei turėtumėte sukurti jungties funkcinį profilį.

### <a name="create-connector-technical-profiles"></a>Sukurkite jungčių techninius profilius

Norėdami sukurti jungties techninius profilius, atlikite šiuos veiksmus.

1. Prekybos būstinėje eikite į **Jungčių techniniai profiliai** puslapis (**Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Jungčių techniniai profiliai**).
1. Sukurkite techninį kiekvienos mokesčių jungties profilį atlikdami šiuos veiksmus:

    1. Pasirinkite jungties pavadinimą.
    1. Pasirinkite jungties tipą:

        - Įrenginiams ar paslaugoms, kurie yra prijungti prie aparatinės įrangos stoties arba yra vietiniame tinkle, pasirinkite **Vietinis**.
        - Norėdami gauti išorines paslaugas, pasirinkite **Išorinis**.
        - Vidinėms jungtims „Commerce“ vykdymo metu (CRT), pasirinkite **Vidinis**. 

    1. Pasirinkite jungties vietą:

        - Jei jungtis yra aparatūros stotyje, pasirinkite **Techninės įrangos stotis**.
        - Jei jungtis yra POS registre, pasirinkite **Registruotis**.

Techniniame jungties profilyje pateiktų skirtukų **Įrenginys** ir **Parametrai** nustatymus galima keisti. Norėdami atkurti numatytuosius parametrus, kurie apibrėžti fiskalinės jungties konfigūracijoje, pasirinkite **Naujinti**. Kol bus įkeliama nauja XML konfigūracijos versija, gausite pranešimą, nurodantį, kad dabartinė mokesčių jungtis arba fiskalinio dokumento teikėjas jau naudojamas. Ši procedūra neperrašo neautomatinių pakeitimų, kurie anksčiau buvo atlikti funkciniuose jungčių profiliuose ir techniniuose jungčių profiliuose. Norėdami pritaikyti numatytąjį parametrų rinkinį iš naujos konfigūracijos, pasirinkite **Atnaujinti** arba ant **Jungčių funkciniai profiliai** puslapį arba **Jungčių techniniai profiliai** puslapį.

Jei turite nustatyti konkrečius atskiro POS registro ar parduotuvės parametrus, atlikite šiuos veiksmus.

1. Pasirinkite **Nepaisyti** meniu elementą.
1. Ant **Nepaisyti** puslapį, sukurkite naują įrašą.
1. Pasirinkite parduotuvę arba POS registrą. Galite nepaisyti pasirinkto techninio profilio parametrų atskiram POS registrui arba visiems atskiros parduotuvės POS registrams.
1. Ant **Įrenginys** skirtuką, įveskite pasirinkto POS registro arba parduotuvės parametrus.

### <a name="create-fiscal-connector-groups"></a>Sukurkite fiskalinių jungčių grupes

Fiskalinių jungčių grupė yra su identiškas funkcijas atliekančiomis ir tame pačiame fiskalinės registracijos proceso veiksme naudojamomis fiskalinėmis jungtimis susietų funkcinių profilių subrinkinys. Pavyzdžiui, jei mažmeninėje parduotuvėje galima naudoti kelis fiskalinio spausdintuvo modelius, tų fiskalinių spausdintuvų fiskalinės jungtys gali būti sujungtos į fiskalinių jungčių grupę.

Norėdami sukurti fiskalinių jungčių grupę, atlikite šiuos veiksmus.

1. Eikite į **Fiskalinių jungčių grupė** puslapis (**Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinių jungčių grupės**).
1. Sukurkite naują fiskalinių jungčių grupę.
1. Į jungčių grupę įtraukite funkcinių profilių. Skirtuke **Funkciniai profiliai** pasirinkite **Įtraukti** ir pasirinkite profilio numerį. Kiekviena fiskalinė jungčių grupės jungtis gali turėti tik vieną funkcinį profilį.
1. Jei norite sustabdyti funkcinių profilių naudojimą, nustatykite funkcijos **Išjungti** parinktį **Taip**. Šis pakeitimas taikomas tik dabartinei jungčių grupei. Kitose jungčių grupėse galite ir toliau naudoti tą patį funkcinį profilį.

### <a name="create-a-fiscal-registration-process"></a>Sukurkite fiskalinės registracijos procesą

Fiskalinės registracijos procesas nusakomas registracijos veiksmų seka ir kiekviename veiksme naudojama jungčių grupe.

Norėdami sukurti fiskalinės registracijos procesą, atlikite šiuos veiksmus.

1. Prekybos būstinėje eikite į **Fiskalinės registracijos procesas** puslapis (**Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinės registracijos procesai**).
1. Sukurkite naują įrašą kiekvienam unikaliam fiskalinės registracijos procesui.
1. Pridėkite registracijos veiksmus prie proceso atlikdami šiuos veiksmus:

    1. Pasirinkite **Įtraukti**.
    1. Pasirinkite fiskalinės jungties tipą.
    1. Lauke **Grupės numeris** pasirinkite atitinkamą fiskalinių jungčių grupę.

### <a name="assign-entities-of-the-fiscal-registration-process-to-pos-profiles"></a>Priskirkite fiskalinės registracijos proceso objektus POS profiliams

Norėdami priskirti fiskalinės registracijos proceso objektus POS profiliams, atlikite šiuos veiksmus.

1. Prekybos būstinėje eikite į **POS funkcijų profiliai** puslapis (**Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> POS nustatymas \> POS profiliai \> Funkcionalumo profiliai**). 
1. Priskirkite fiskalinės registracijos procesą POS funkcijų profiliui.
1. Pasirinkite **Redaguoti**, tada skirtuko **Fiskalinės registracijos procesas** lauke **Proceso numeris** pasirinkite procesą.
1. Eikite į **POS techninės įrangos profilis** puslapis (**Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> POS nustatymas \> POS profiliai \> Aparatinės įrangos profiliai**).
1. Priskirkite jungties techninius profilius aparatinės įrangos profiliui. 
1. Pasirinkite **Redaguoti**, o tada, ant **Fiskaliniai periferiniai įrenginiai** skirtuką, pridėkite eilutę. 
1. Viduje konors **Profilio numeris** lauke, pasirinkite jungties techninį profilį.

> [!NOTE]
> Į tą patį aparatūros profilį galite įtraukti kelis techninius profilius. Tačiau aparatūros profilis arba EKA funkcijų profilis turėtų turėti tik vieną sankirtą su bet kuria fiskalinių jungčių grupe.

Fiskalinės registracijos srautą apibrėžia fiskalinės registracijos procesas ir kai kurie fiskalinės integracijos komponentų parametrai:CRT mokesčių dokumentų teikėjo plėtinys ir fiskalinės jungties aparatinės įrangos stoties plėtinys.

- Finansinių dokumentų teikėjas iš anksto nustato įvykių ir operacijų prenumeratą fiskalinėje registracijoje.
- Finansinių dokumentų teikėjas taip pat yra atsakingas už fiskalinių jungčių, naudojamų fiskalinėje registracijoje, nustatymą. Ji sugretina funkcinius jungčių profilius, kurie įtraukti į fiskalinių jungčių grupę, nurodytą esamame fiskalinė registracijos proceso veiksme, su techniniu jungties profiliu, kuris priskirtas aparatūros stoties, su kuria susietas EKA, aparatūros profiliui.
- Finansinių dokumentų teikėjas naudoja duomenų susiejimo parametrus iš finansinių dokumentų teikėjo konfigūracijos, kad transformuotų operacijos / įvykio duomenis, pvz., mokesčius ir mokėjimus, kol generuojamas finansinis dokumentas.
- Kai finansinių dokumentų teikėjas sugeneruoja finansinį dokumentą, fiskalinė jungtis gali siųsti jį nepakeistą į finansinį įrenginį arba išanalizuoti ir transformuoti į įrenginio programos programavimo sąsajos (API) komandų seką, atsižvelgiant į ryšį.

### <a name="validate-the-fiscal-registration-process"></a>Patvirtinkite fiskalinės registracijos procesą

Rekomenduojame patvirtinti fiskalinės registracijos procesą šiais atvejais:

- Atlikote visus naujo registracijos proceso nustatymus. Šie nustatymai apima registracijos procesų priskyrimą POS funkcijų profiliams ir aparatinės įrangos profiliams.
- Pakeitėte esamą fiskalinės registracijos procesą ir dėl šių pakeitimų vykdymo metu gali būti pasirinkta kita fiskalinė jungtis. (Pavyzdžiui, pakeitėte fiskalinės registracijos proceso veiksmo jungčių grupę, įgalinote jungties funkcinį profilį jungčių grupėje arba į jungčių grupę įtraukėte naują jungties funkcinį profilį.)
- Pakeitėte jungčių techninių profilių priskyrimą aparatinės įrangos profiliams.

Norėdami patvirtinti fiskalinės registracijos procesą, atlikite šiuos veiksmus.

1. Prekybos būstinėje eikite į **Fiskalinės registracijos procesas** puslapis (**Mažmeninė prekyba ir prekyba \> Kanalo nustatymas \> Fiskalinė integracija \> Fiskalinės registracijos procesai**).
1. Pasirinkite **Patvirtinti** patvirtinti fiskalinės registracijos procesą.
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

Norėdami nustatyti klaidų tvarkymo nustatymus, atlikite šiuos veiksmus.

1. Puslapyje **Fiskalinės registracijos procesas** (**Mažmeninė prekyba ir prekyba \> Kanalų sąranka \> Fiskalinė integracija \> Fiskalinės registracijos procesai**) galite sukurti toliau nurodytus kiekvieno fiskalinės registracijos proceso veiksmo parametrus.

    - **Leisti praleisti** – šis parametras įjungia parinktį **Praleisti** klaidų tvarkymo dialogo lange.
    - **Leisti pažymėti kaip užregistruotą** – šis parametras įjungia parinktį **Pažymėti kaip užregistruotą** klaidų tvarkymo dialogo lange.
    - **Leisti atidėti** – Šis parametras įgalina **Atidėti** parinktį klaidų tvarkymo dialogo lange.
    - **Tęsti esant klaidai** – jei šis parametras įjungtas, mokesčių registravimo procesą galima tęsti EKA registre, kai operacijos arba įvykio finansinis registravimas nepavyksta. Kitu atveju, norėdamas vykdyti kitos operacijos arba įvykio finansinį registravimą, operatorius turi kartoti nepavykusį finansinį registravimą, nepaisyti jo arba pažymėti operaciją ar įvykį kaip užregistruotą. Daugiau informacijos žr. [Nebūtinas finansinis registravimas](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Jei parametras **Tęsti įvykus klaidai** įjungtas, parametrai **Leisti nepaisyti** ir **Leisti pažymėti kaip užregistruotą** išjungiami automatiškai.

1. The **Praleisti** ir **Pažymėti kaip registruotą** parinktys klaidų apdorojimo dialogo lange reikalauja, kad **Leisti praleisti registraciją arba pažymėti kaip registruotą** leidimas būtų įjungtas. Norėdami įgalinti šį leidimą, eikite į **Leidimų grupės** puslapis (**Mažmeninė prekyba ir prekyba \> Darbuotojai \> Leidimų grupės**) ir nustatykite **Leisti praleisti registraciją arba pažymėti kaip registruotą** galimybė į **Taip**.
1. The **Atidėti** parinktis klaidų tvarkymo dialogo lange reikalauja, kad **Leisti atidėti** leidimas būtų įjungtas. Norėdami įgalinti leidimą, eikite į **Leidimų grupės** puslapis (**Mažmeninė prekyba ir prekyba \> Darbuotojai \> Leidimų grupės**) ir nustatykite **Leisti atidėti** galimybė į **Taip**.
1. The **Praleisti**, **kaip registruotą**, ir **Atidėti** parinktys leidžia operatoriams įvesti papildomos informacijos, kai fiskalinė registracija nepavyksta. Kad ši funkcija būtų prieinama, turėtumėte nurodyti **Praleisti**, **kaip registruotą**, ir **Atidėti** informacijos kodai mokesčių jungčių grupėje. Tada operatoriaus įvesta informacija įrašoma kaip informacijos kodo operacija, susieta su finansine operacija. Daugiau informacijos apie informacijos kodus žr. [Informacijos kodai ir informacijos kodų grupės](../info-codes-retail.md).

    > [!NOTE]
    > **Produkto** paleidiklio funkcija nepalaikoma informacijos koduose, kurie naudojami parinktyse **Praleisti** ir **Pažymėti kaip užregistruotą** fiskalinių jungčių grupėse.

    - Ant **Fiskalinių jungčių grupė** puslapyje, esančiame **Informaciniai kodai** skirtuke pasirinkite informacijos kodus arba informacijos kodų grupes **Praleisti**, **kaip registruotą**, ir **Atidėti** laukai.

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
