---
title: Finansinių konsolidacijų ir valiutos konvertavimo apžvalga
description: Šiame straipsnyje aprašomos finansinės konsolidacijos ir valiutos konvertavimas į DK.
author: jinniew
ms.date: 10/07/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 56e445dcf471fd20695824d5e47cd15f39c022ce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846863"
---
# <a name="financial-consolidations-and-currency-translation-overview"></a>Finansinių konsolidacijų ir valiutos konvertavimo apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje naudojamas būdas, kaip konsoliduojant Microsoft Dynamics naudojami ir 365 finansai, ir finansinės ataskaitos. Joje aprašomi atvejai, susiję su kelių įmonių ataskaitomis, agregavimu, šalinimu ir segmento palūkanomis. Joje taip pat paaiškinama, kaip elgtis ypatingais atvejais, pvz., kai juridiniai subjektai naudoja skirtingus ataskaitinius laikotarpius arba skirtingus sąskaitų planus.

Šis straipsnis buvo parašytas vartotojams ir funkciniams konsultantams ir laikoma, kad skaitytuvai turi bendrą supratimą apie finansus ir finansines ataskaitas. Pagrindinė sąranka nėra aprašyta.

> [!NOTE]
> Terminas *juridinis subjektas* naudojamas „Finance“, o terminas *įmonė* naudojamas finansinėse ataskaitose. Abu šie terminai naudojami šiame straipsnyje. Tačiau šiame straipsnyje jų prasmės yra tokios pačios.

## <a name="audience"></a>Auditorija
Šis straipsnis skirtas finansų ir apskaitos vartotojams ir programų konsultantams, kurie nori naudoti finansų ir ataskaitų bei finansines ataskaitas, konsoliduoti kelių įmonių ir kelių valiutų duomenis.

## <a name="approach"></a>Metodas
„Finance“ konsolidavimo proceso metu naudoja atskirą juridinį subjektą. Dėl to galima konsoliduoti vieną egzempliorių, tačiau taip pat galima gauti duomenis iš kitų šaltinių. Konsolidavimo procesą reikia vykdyti kiekvieną kartą, kai pirminiuose juridiniuose subjektuose atliekami pakeitimai.

Finansinės ataskaitos gali konsoliduoti kelias įmones ataskaitos generavimo metu. Nors duomenys yra saugomi duomenų srityje versijomis ir juos galima eksportuoti, kiekviena pirminė įmonė yra duomenų savininkas ir konteineris. Ataskaitas galima vykdyti bet kuriuo metu, net kiekvieną minutę (pavyzdžiui). Ji suteikia daug papildomų galimybių, pavyzdžiui, galimybę detalizuoti ir visas įmones ir dimensijas.

Vartotojai gali naudoti konsolidavimą tinkle, finansines ataskaitas arba šių parinkčių derinį. Jų pasirinkimas priklauso nuo jų įmonės poreikių ir jų auditorių nuostatų.

## <a name="consolidations"></a>Konsolidacija
Modulis **Konsolidavimas** apima parinktis, skirtas konsoliduoti kelis juridinius subjektus konsolidavimo proceso metu ir importuoti arba eksportuoti įmonės balansą. Taip pat galite nustatyti pašalinimą ir registruoti pašalinimo žurnalus.

## <a name="benefits-of-using-consolidate-online"></a>Konsolidavimo tinkle privalumai
Klientai, naudojantys modulį **Konsolidavimas** galės pasinaudoti įvairiais privalumais.

- **Duomenų gylis** – galite kurti konsoliduotas ataskaitas, kurios sujungiami faktiniai ir biudžeto duomenys sąskaitos lygiu ir dimensijos lygiu.
- **Dinaminis konsolidavimas** – konsolidacijas galima apdoroti kelis kartus.
- **Audito galimybių** – dimensijos ir sąskaitos tvarkomos analizės ir audito tikslais, o balansai kuriami pagal datą.
- **Valiutos konvertavimas** – galite nustatyti sąskaitų diapazonus ir tarifai, naudojamus konvertuojant iš pirminės įmonės apskaitos valiutos į konsoliduotos įmonės apskaitos valiutą.
- **Pašalinimo apdorojimas konsoliduotoje arba pašalinimo įmonėje** – galite apdoroti ir registruoti pašalinimus vykdydami vieną procesą konsolidavimo metu. Taip pat galite vykdyti pasiūlymą atskirai.

## <a name="supported-consolidation-scenarios"></a>Palaikomi konsolidavimo scenarijai
Toliau pateikti keli konsolidavimo scenarijai, palaikomi konsoliduojant tinkle.

- Vieno lygio konsolidavimas keliuose juridiniuose subjektuose
- Konsolidavimas, apimantis pašalinimus
- Segmento palūkanos (šiuo atveju reikia naudoti neautomatinį skaičiavimą ir įrašą įmonėje.)
- Keli sąskaitų planai keliuose juridiniuose subjektuose
- Skirtingi finansiniai kalendoriai keliuose juridiniuose subjektuose
- Konsolidavimas, apimantis kelias ataskaitų valiutas

## <a name="legal-entity-setup"></a>Juridinio subjekto sąranka
Prieš vykdydami konsolidavimą turite nustatyti juridinį subjektą. Konsolidavimą galite vykdyti tiek kartų, kiek reikia, ir visi duomenys bus konvertuoti iš pirminės įmonės apskaitos valiutos į nurodytą konsolidavimo įmonės valiutą. Todėl, jei naudojant toliau nurodytą organizacijos struktūrą pirmiausia reikia konvertuoti visų Šiaurės Amerikos įmonių duomenis į JAV dolerius (USD), o tada – į eurus (EUR), pirminės įmonės valiutą, reikia turėti bent dvi konsolidavimo įmones.

![Organizacijos struktūra.](./media/organizational-structure.png "Organizacijos struktūra")

Atsižvelgiant į toliau nurodytą organizacijos struktūrą, privalote turėti Šiaurės Amerikos konsolidavimo juridinį subjektą, nes konsolidavimo metu visada konsoliduojama iš pirminės įmonės apskaitos valiutos į konsolidavimo įmonės valiutą. Pateiktame pavyzdyje: jei visos įmonės yra įtrauktos į vieną konsolidavimą, Meksikos filialo duomenys bus konvertuoti iš Meksikos peso (MXN) į EUR, o ne iš MXN į USD ir tada – į EUR.

Kurdami juridinį subjektą galite nurodyti, ar įmonė naudojama konsolidavimo ir pašalinimo procesų metu, ar tik vieno iš šių procesų metu. Tolesnėje iliustracijoje įmonė naudojama abiejuose procesuose. Atkreipkite dėmesį, kad negalite registruoti kasdienių žurnalų konsoliduotoje įmonėje, bet galite juos registruoti pašalinimo įmonėje. Todėl galbūt pageidausite turėti atskirą pašalinimo įmonę.

![Juridinis objektas, kuris naudojamas tiek konsolidavimui, tiek pašalinimui.](./media/sep-elimination-company.png "Juridinis objektas, kuris naudojamas tiek konsolidavimui, tiek pašalinimui")

## <a name="main-accounts-and-consolidation-account-groups"></a>Pagrindinės sąskaitos ir konsolidavimo sąskaitų grupės
Turite pasirinkti, kaip norite konsoliduoti sąskaitų planą. Konsolidavimo proceso metu galite naudoti tris pagrindinės sąskaitos konsolidavimo parinktis.

Pirmoji parinktis yra pirminės įmonės pagrindinės sąskaitos naudojimas. Šiuo atveju bus konsoliduotos visos visų įmonių sąskaitos. Pavyzdžiui, jei įmonės USMF grynųjų pinigų sąskaita yra 100000, o įmonės DEMF grynųjų pinigų sąskaita yra 1100, konsolidavimo įmonėje bus įtrauktos abi sąskaitos. Kiekvienoje sąskaitoje bus nurodyti atitinkami balansai.

Antroji parinktis yra nurodyti numatytąją konsolidavimo sąskaitą puslapyje **Pagrindinė sąskaita**. Sąskaita, tada bus galima susieti su konsolidavimo sąskaita. Ši parinktis gali būti naudinga, kai turite skirtingus sąskaitų planus arba turite susieti planu, kurį nurodo būstinė.

![Numatytoji konsolidavimo sąskaita, nurodyta pagrindinių sąskaitų puslapyje.](./media/main-accounts.png "Numatytoji konsolidavimo sąskaita, nurodyta pagrindinių sąskaitų puslapyje")

Trečioji parinktis – naudoti konsolidavimo sąskaitų grupes. Galite nurodyti tiek konsolidavimo sąskaitų grupių, kaip jums reikia. Tada puslapyje **Papildomos konsolidavimo sąskaitos** tiesiog susiekite sąskaitų plano pagrindinę sąskaitą su sąskaita, kuri turi būti toje grupėje.

![Papildomų konsolidavimo sąskaitų puslapio susiejimas.](./media/additional-consolidation-accounts.png "Papildomų konsolidavimo sąskaitų puslapio susiejimas")

## <a name="consolidating-online"></a>Konsolidavimas tinkle
Norėdami sužinoti, kaip įvesti konsolidavimo informaciją internete, žr. [Internetinis finansinis konsolidavimas](./consolidate-online.md).

## <a name="managing-consolidation-transactions"></a>Konsolidavimo operacijų valdymas
Norėdami peržiūrėti konsolidavimo rezultatus, turite rinktis iš kelių parinkčių.

- Generuokite finansinę ataskaitą pagal konsolidavimo įmonę.
- Peržiūrėkite sąrašo puslapį **Bandomasis balansas** konsolidavimo įmonėje.
- Puslapio **Konsolidavimas** konsolidavimo operacijų sąraše peržiūrėkite pagal datą sukuriamus balansus, skirtus kiekvienai pirminei įmonei ir kiekvienam laikotarpiui.

    ![Konsolidavimo operacijos konsolidavimų puslapyje.](./media/managing-consolidation-transactions.png "Konsolidavimo operacijos konsolidavimų puslapyje")

Norėdami vykdyti konsolidavimą dar kartą, galite tiesiog apdoroti konsolidaciją. Taip pat galite pirmiausia pasirinkti **Pašalinti operacijas** puslapyje **Konsolidavimas**.
Tuo atveju, konsoliduotos sąskaitos balansai nėra tikslūs, šie balansai gali būti koreguojami naudojant **Uždarymo laikotarpio koregavimų** puslapį.

## <a name="consolidate-with-import"></a>Konsoliduoti su importu
Konsolidavimas naudojant importavimo funkciją vykdomas taip, kaip konsolidavimo tinkle funkcija. Kai pasirenkate juridinius subjektus, galite naršyti šaltinio failą, kuriame yra duomenų.

## <a name="export-company-balances"></a>Įmonės balansų eksportavimas
Eksportavimo įmonės balansų funkcija taip pat naudojama taip, kaip konsolidavimo tinkle funkcija. Kai pasirenkate juridinį subjektą, nustatysite išeigos failo kelią.

## <a name="elimination-rules"></a>Pašalinimo taisyklės
Norėdami pašalinti vidinės įmonės operacijas, galite kurti pašalinimo taisyklę. Taip pat galite neautomatiškai pašalinti įrašą įmonėje, kuri nurodyta kaip pašalinimo įmonė. Jei sukursite pašalinimo taisyklę, galėsite rinktis iš dviejų pašalinimo metodo parinkčių: **Grynasis pokytis** ir **Fiksuotas**.

### <a name="set-up-elimination-rules"></a>Nustatyti pašalinimo taisykles
Nustatant pašalinimo taisykles programoje „Finance“, galima sukurti finansinę dimensiją, naudojamą tik šalinimo veiksmams atlikti. Dauguma klientų šią finansinę dimensiją pavadina **Prekybos partneris** arba panašiai. Jei nuspręsite nenaudoti finansinės dimensijos, būtinai turėkite dvi pagrindines sąskaitas, skirtas tik vidinės įmonės operacijoms.

Pašalinimo sąranką galima rasti modulio **Konsolidavimas** srityje **Sąranka**. Įvedę taisyklės aprašą, turite pasirinkti įmonę, kurioje pašalinimo žurnalas bus registruojamas. Tai turi būti įmonė, kurios juridinio subjekto sąrankoje pažymėta parinktis **Naudoti finansinio pašalinimo procese**.

Jei reikia, galite nustatyti pašalinimo taisyklės įsigaliojimo datą ir galiojimo pabaigos datą. Turite nustatyti parinkties **Aktyvus** reikšmę **Taip**, jei norite, kad pašalinimo taisyklę būtų galima naudoti pašalinimo pasiūlymo proceso metu. Pasirinkite žurnalo, kurio žurnalo tipas **Pašalinimas**, pavadinimą.

![Pagrindinės pašalinimo taisyklės ypatybės.](./media/ledger-elimination-rule-journal.png "Pagrindinės pašalinimo taisyklės ypatybės")

Nurodę pagrindines ypatybes, nustatykite pačias apdorojimo taisykles pasirinkdami **Eilutės**. Galimos dvi šalinimo parinktys: grynojo pokyčio sumos pašalinimas arba fiksuotos sumos nustatymas.

Pasirinkite pirmines sąskaitas. Žvaigždutę (\*) galite naudoti kaip universalųjį simbolį. Pavyzdžiui, **1\**_ parenka visas sąskaitas, kurios prasideda _* 1** kaip duomenų šaltinį talpinimui.

Pasirinkę pirmines sąskaitas, naudokite lauką **Sąskaitos specifikacija**, kad nurodytumėte sąskaitą, naudojamą paskirties įmonėje. Pasirinkite **Pirminė**, jei norite naudoti tą pačią pagrindinę sąskaitą, kuri nurodyta pirminėje sąskaitoje. Jei pasirinksite **Nurodyta vartotojo**, turite nurodyti paskirties sąskaitą.

![Didžiosios knygos pašalinimo taisyklės eilutės puslapis.](./media/ledger-elimination-rule-line.png "Didžiosios knygos pašalinimo taisyklės eilutės puslapis")

Laukas **Dimensijos specifikacija** naudojamas taip, kaip laukas **Sąskaitos specifikacija**. Pasirinkite **Pirminė**, jei norite naudoti tas pačias dimensijas paskirties įmonėje ir pirminėje įmonėje. Jei pasirinksite **Nurodyta vartotojo**, turėsite nurodyti paskirties įmonės dimensijas, pasirinkdami **Paskirties dimensijos**. Tada pasirinkite pirmines dimensijas ir finansines dimensijas bei vertes, kurios naudojamos kaip pašalinimo šaltinis.

### <a name="process-elimination-transactions"></a>Apdoroti pašalinimo operacijas
Pašalinimo operacijas galima apdoroti dviem būdais. Operaciją galima apdoroti vykdant konsolidavimo tinkle procesą arba sukuriant pašalinimo žurnalą ir paleidžiant pašalinimo pasiūlymo procesą. Šiame skyriuje apžvelgiama antroji parinktis.

Įmonėje, kuri nurodyta kaip pašalinimo įmonė, modulyje **Konsolidavimas** pasirinkite **Pašalinimo žurnalas**. Pasirinkę žurnalo pavadinimą pasirinkite **Eilutės**. Norėdami paleisti pasiūlymą, pasirinkite **Pasiūlymai** \> **Pašalinimo pasiūlymas**.

Pasirinktie įmonę, kuri yra konsoliduotų duomenų šaltinis, o tada pasirinktie taisyklę, kurią norite apdoroti. Įveskite pradžios ir pabaigos datas, kad nurodytumėte datų intervalą, kuriame ieškoma pašalinimo sumų. Lauke **DK registravimo data** nurodyta data naudojama registruojant žurnalą DK. Pasirinkę **Gerai** galite peržiūrėti sumas ir registruoti žurnalą.

> [!NOTE]
> Pašalinimo žurnale sąskaitos verčių sumos rodomos pradinių jų operacijų valiuta, o ne apskaitos valiuta. Kai pašalinimo žurnale peržiūrite sumas, dėl šios priežasties gali kilti neaiškumų.

Daugiau informacijos ir pavyzdžių žr. [Pašalinimo taisyklės](./elimination-rules.md).

## <a name="currency-revaluation-in-a-consolidation-company"></a>Valiutos kurso pasikeitimas konsoliduotoje įmonėje
Konsoliduojant duomenis iš vienos apskaitos valiutos į kitą, vis tiek reikia vykdyti valiutos kurso pakeitimą, jei pasikeitė valiutų kursai, kad sąskaitos balansai būtų tinkamai perkainoti. Pirmą kartą konsoliduodami duomenis, naudodami skirtuką **Valiutos konvertavimas** pasirinkite pradinius valiutos kursus, kurie bus konvertuojami vykdant konsolidavimo procesą. Įvedę naują valiutos kursą (pavyzdžiui, kitą mėnesį), turite perkainoti sąskaitų balansus. Negautas pelnas arba nuostoliai tada atnaujinami atsižvelgiant į naują valiutos kursą ir datą.

Daugiau informacijos apie valiutos kurso pasikeitimą konsolidavimo įmonėje žr. [Valiutos kurso pasikeitimas konsolidavimo įmonėje](currency-revaluation-consolidation-company.md).

Daugiau informacijos apie tai, kaip vykdomas valiutos kurso pasikeitimas modulyje **Didžioji knyga**, žr. [Užsienio valiutos kurso pasikeitimas DK](./foreign-currency-revaluation-general-ledger.md).

### <a name="additional-information"></a>Papildoma informacija
- Visi registravimo sluoksniai yra konsoliduojami, kai apdorojama konsolidacija.
- Pašalinimo žurnalus galima registruoti tik dabartiniame sluoksnyje.
- Konsoliduojami tik valdymo balansai. Todėl, norėdami matyti pradžios balansus, vis tiek vykdyti metų pabaigos uždarymą konsolidavimo įmonėje.
- Galite registruoti kasdienį žurnalą pašalinimo įmonėje, bet ne konsolidavimo įmonėje.
- Konsolidacijos įmonės balansų koregavimus galima atlikti tik naudojant **Uždarymo laikotarpio koregavimų** puslapį. 

## <a name="benefits-of-using-financial-reporting-for-financial-consolidations-and-currency-translation-or-to-complement-consolidate-online-for-consolidated-reporting"></a>Finansinių ataskaitų privalumai vykdant finansinį konsolidavimą ir valiutos konvertavimą arba privalumai, naudingi vykdant konsolidavimo ataskaitų konsolidavimą tinkle
Klientai gali pasinaudoti finansinių ataskaitų privalumais vykdant finansinį konsolidavimą ir valiutos konvertavimą arba privalumais, naudingais vykdant konsolidavimo ataskaitų konsolidavimą tinkle.

- **Duomenų gylis** – galite kurti konsoliduotas ataskaitas, kurios sujungiami faktiniai ir biudžeto duomenys sąskaitos lygiu ir dimensijos lygiu. „Finance“ šie duomenys apima duomenis iš biudžeto kontrolės ir biudžeto plano.
- **Dinaminis konsolidavimas** – konsolidavimą galima vykdyti bet kuriuo metu ir bet kokiu organizacijos hierarchijos lygiu.
- **Visos audito galimybės** – visa dimensijų, sąskaitų ir operacijų informacija tvarkoma analizės ir audito tikslais. Be to, finansinėse ataskaitose galima visiškai atstatyti detalizuotą pradinės operacijos vaizdą bet kuriame konsoliduojamame juridiniame subjekte.
- **Supaprastintas valiutos konvertavimas** – atlikę minimalią „Finance“ sąranką, galite konvertuoti bet kurią finansinių ataskaitų ataskaitos valiutą į bet kurią nustatytą ataskaitų valiutą. Be to, galite nustatyti neribotą ataskaitų valiutų skaičių.
- **Pašalinimų registravimas šaltinyje** – galite kurti ir spausdinti pašalinimo ataskaitą, kad patvirtintumėte pašalinimo operacijas. Tada galite registruoti bet kokius naujus pašalinimus kaip įprastines vidinės įmonės operacijas. Taip pat pašalinimo juridinį subjektą galite naudoti bet kurioje operacijoje, kurios nenorite taikyti savo juridiniams subjektams.

## <a name="supported-consolidation-scenarios-for-financial-reporting"></a>Palaikomi finansinių ataskaitų konsolidavimo scenarijai

Toliau pateikti keli konsolidavimo scenarijai, palaikomi finansinėse ataskaitose.

- Vieno lygio ir kelių lygių konsolidavimas keliuose juridiniuose subjektuose
- Konsolidavimas naudojant organizacijų struktūras, kurios sukurtos iš juridinių subjektų
- Konsolidavimas, apimantis pašalinimus
- Segmento palūkanos
- Keli sąskaitų planai keliuose juridiniuose subjektuose
- Skirtingi finansiniai kalendoriai keliuose juridiniuose subjektuose
- Konsolidavimas, apimantis kelias ataskaitų valiutas
- Verslo struktūros vienetų konsolidavimas

## <a name="generating-consolidated-financial-statements"></a>Konsoliduotų finansinių ataskaitų generavimas
Informacijos apie scenarijus, kuriais galite generuoti konsoliduotas finansines ataskaitas, žr. [Konsoliduotų finansinių ataskaitų generavimas](./generating-consolidated-financial-statements.md).

## <a name="performance-enhancement-for-large-consolidations"></a>Didelių konsolidacijų našumo patobulinimas

Aplinkos, kur yra daug DK operacijų, gali veikti lėčiau nei optimalios. Norėdami išspręsti šią problemą, galite nustatyti lygiagretų paketų, kurie naudoja vartotojo nustatytą datų skaičių, apdorojimą. Norėdami užtikrinti, kad sprendimas veikia kaip numatyta, įtraukite konsolidavimo plėtinio tašką, kad būtų grąžinamas datų diapazonų konteineris. Pagrindinis diegimas turi turėti vieną konsolidacijos pradžios ir pabaigos datų diapazoną. Bus patikrinti pagrindinio diegimo datų intervalai, siekiant užtikrinti, kad juose nėra tarpų arba persidengimų. Datų diapazonai bus naudojami kiekvienos įmonės lygiagretiems paketų grupavimams kurti.

Galite tinkinti datų diapazonų skaičių, kad jis atitiktų jūsų organizacijos poreikius. Pritaikę datų diapazonų skaičių, galite supaprastinti testą ir sumažinti poveikį esamam kodui, nes nėra paskirstymo logikos. Vieninteliai reikalingi nauji bandymai patvirtinti paketinių užduočių kūrimą, patvirtina dienų sekas ir išbando dienų sekų pogrupį, kad patikrintų, ar partijos gali būti sujungtos paskutinei partijos užduočiai. 

Ši priemonė pagerina konsolidavimo procesą DK, kai procesas vykdomas pakete. Patobulinimas pagerina DK konsolidavimo proceso našumą, išskaidant konsolidaciją į kelias užduotis, kurias galima apdoroti lygiagrečiai. Pagal numatytąjį konsolidavimo veiklos metodą kiekviena užduotis apdoroja aštuonių dienų vertės DK veiklą. Tačiau buvo pridėtas plėtinio taškas, leidžiantis pritaikyti sukurtas skaičių užduotis.

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti **Funkcijos valdymas** darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:

- **Modulis:** Didžioji knyga
- **Funkcijos pavadinimas:** Didelių konsolidacijų našumo patobulinimas

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
