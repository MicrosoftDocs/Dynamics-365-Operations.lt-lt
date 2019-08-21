---
title: Finansinis konsolidavimas ir valiutos konvertavimas
description: Šioje temoje aprašomas finansinis konsolidavimas ir valiutos konvertavimas didžiojoje knygoje.
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 8ec6268daa7c7b6c455aad571ef22c083283b5d9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839284"
---
# <a name="financial-consolidations-and-currency-translation"></a>Finansinės konsolidacijos ir valiutos konvertavimas

[!include [banner](../includes/banner.md)]

Šioje temoje apžvelgiamas konsolidavimo metodas, naudojamas „Microsoft Dynamics 365 for Finance and Operations“ ir finansinėse ataskaitose. Joje aprašomi atvejai, susiję su kelių įmonių ataskaitomis, agregavimu, šalinimu ir segmento palūkanomis. Joje taip pat paaiškinama, kaip elgtis ypatingais atvejais, pvz., kai juridiniai subjektai naudoja skirtingus ataskaitinius laikotarpius arba skirtingus sąskaitų planus.

Ši tema skirta vartotojams bei funkciniams konsultantams ir joje manoma, kad skaitytojai yra susipažinę su „Finance and Operations“ ir finansinių ataskaitų pagrindais. Pagrindinė sąranka nėra aprašyta.

> [!NOTE]
> Terminas *juridinis subjektas* naudojamas „Finance and Operations“, o terminas *įmonė* naudojamas finansinėse ataskaitose. Abu šie terminai naudojami šioje temoje. Tačiau šioje temoje jų reikšmės sutampa.

## <a name="audience"></a>Auditorija
Ši tema skirta finansų ir apskaitos programų vartotojams ir konsultantams, kurie nori naudoti „Finance and Reporting“ bei finansines ataskaitas ir konsoliduoti kelių įmonių bei įvairių valiutų duomenis.

## <a name="approach"></a>Metodas
„Finance and Operations“ konsolidavimo proceso metu naudoja atskirą juridinį subjektą. Dėl to galima konsoliduoti vieną egzempliorių, tačiau taip pat galima gauti duomenis iš kitų šaltinių. Konsolidavimo procesą reikia vykdyti kiekvieną kartą, kai pirminiuose juridiniuose subjektuose atliekami pakeitimai.

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

![Organizacijos struktūra](./media/organizational-structure.png "Organizacijos struktūra")

Atsižvelgiant į toliau nurodytą organizacijos struktūrą, privalote turėti Šiaurės Amerikos konsolidavimo juridinį subjektą, nes konsolidavimo metu visada konsoliduojama iš pirminės įmonės apskaitos valiutos į konsolidavimo įmonės valiutą. Pateiktame pavyzdyje: jei visos įmonės yra įtrauktos į vieną konsolidavimą, Meksikos filialo duomenys bus konvertuoti iš Meksikos peso (MXN) į EUR, o ne iš MXN į USD ir tada – į EUR.

Kurdami juridinį subjektą galite nurodyti, ar įmonė naudojama konsolidavimo ir pašalinimo procesų metu, ar tik vieno iš šių procesų metu. Tolesnėje iliustracijoje įmonė naudojama abiejuose procesuose. Atkreipkite dėmesį, kad negalite registruoti kasdienių žurnalų konsoliduotoje įmonėje, bet galite juos registruoti pašalinimo įmonėje. Todėl galbūt pageidausite turėti atskirą pašalinimo įmonę.

![Juridinis subjektas, naudojamas konsolidavimo ir pašalinimo procesuose](./media/sep-elimination-company.png "Juridinis subjektas, naudojamas konsolidavimo ir pašalinimo procesuose")

## <a name="main-accounts-and-consolidation-account-groups"></a>Pagrindinės sąskaitos ir konsolidavimo sąskaitų grupės
Turite pasirinkti, kaip norite konsoliduoti sąskaitų planą. Konsolidavimo proceso metu galite naudoti tris pagrindinės sąskaitos konsolidavimo parinktis.

Pirmoji parinktis yra pirminės įmonės pagrindinės sąskaitos naudojimas. Šiuo atveju bus konsoliduotos visos visų įmonių sąskaitos. Pavyzdžiui, jei įmonės USMF grynųjų pinigų sąskaita yra 100000, o įmonės DEMF grynųjų pinigų sąskaita yra 1100, konsolidavimo įmonėje bus įtrauktos abi sąskaitos. Kiekvienoje sąskaitoje bus nurodyti atitinkami balansai.

Antroji parinktis yra nurodyti numatytąją konsolidavimo sąskaitą puslapyje **Pagrindinė sąskaita**. Sąskaita, tada bus galima susieti su konsolidavimo sąskaita. Ši parinktis gali būti naudinga, kai turite skirtingus sąskaitų planus arba turite susieti planu, kurį nurodo būstinė.

![Numatytoji konsolidavimo sąskaita nurodyta puslapyje Pagrindinė sąskaita](./media/main-accounts.png "Numatytoji konsolidavimo sąskaita nurodyta puslapyje Pagrindinė sąskaita")

Trečioji parinktis – naudoti konsolidavimo sąskaitų grupes. Galite nurodyti tiek konsolidavimo sąskaitų grupių, kaip jums reikia. Tada puslapyje **Papildomos konsolidavimo sąskaitos** tiesiog susiekite sąskaitų plano pagrindinę sąskaitą su sąskaita, kuri turi būti toje grupėje.

![Puslapio Papildomos konsolidavimo sąskaitos susiejimas](./media/additional-consolidation-accounts.png "Puslapio Papildomos konsolidavimo sąskaitos susiejimas")

## <a name="consolidating-online"></a>Konsolidavimas tinkle
Norėdami sužinoti, kaip įvesti konsolidavimo tinkle informaciją, žr. [Konsolidavimas tinkle](./consolidate-online.md).

## <a name="managing-consolidation-transactions"></a>Konsolidavimo operacijų valdymas
Norėdami peržiūrėti konsolidavimo rezultatus, turite rinktis iš kelių parinkčių.

- Generuokite finansinę ataskaitą pagal konsolidavimo įmonę.
- Peržiūrėkite sąrašo puslapį **Bandomasis balansas** konsolidavimo įmonėje.
- Puslapio **Konsolidavimas** konsolidavimo operacijų sąraše peržiūrėkite pagal datą sukuriamus balansus, skirtus kiekvienai pirminei įmonei ir kiekvienam laikotarpiui.

    ![Konsolidavimo operacijos puslapyje Konsolidavimas](./media/managing-consolidation-transactions.png "Konsolidavimo operacijos puslapyje Konsolidavimas")

Norėdami vykdyti konsolidavimą dar kartą, galite tiesiog apdoroti konsolidaciją. Taip pat galite pirmiausia pasirinkti **Pašalinti operacijas** puslapyje **Konsolidavimas**.

## <a name="consolidate-with-import"></a>Konsoliduoti su importu
Konsolidavimas naudojant importavimo funkciją vykdomas taip, kaip konsolidavimo tinkle funkcija. Kai pasirenkate juridinius subjektus, galite naršyti šaltinio failą, kuriame yra duomenų.

## <a name="export-company-balances"></a>Įmonės balansų eksportavimas
Eksportavimo įmonės balansų funkcija taip pat naudojama taip, kaip konsolidavimo tinkle funkcija. Kai pasirenkate juridinį subjektą, nustatysite išeigos failo kelią.

## <a name="elimination-rules"></a>Pašalinimo taisyklės
Norėdami pašalinti vidinės įmonės operacijas, galite kurti pašalinimo taisyklę. Taip pat galite neautomatiškai pašalinti įrašą įmonėje, kuri nurodyta kaip pašalinimo įmonė. Jei sukursite pašalinimo taisyklę, galėsite rinktis iš dviejų pašalinimo metodo parinkčių: **Grynasis pokytis** ir **Fiksuotas**.

### <a name="set-up-elimination-rules"></a>Nustatyti pašalinimo taisykles
Nustatant pašalinimo taisykles programoje „Finance and Operations“, galima sukurti finansinę dimensiją, naudojamą tik šalinimo veiksmams atlikti. Dauguma klientų šią finansinę dimensiją pavadina **Prekybos partneris** arba panašiai. Jei nuspręsite nenaudoti finansinės dimensijos, būtinai turėkite dvi pagrindines sąskaitas, skirtas tik vidinės įmonės operacijoms.

Pašalinimo sąranką galima rasti modulio **Konsolidavimas** srityje **Sąranka**. Įvedę taisyklės aprašą, turite pasirinkti įmonę, kurioje pašalinimo žurnalas bus registruojamas. Tai turi būti įmonė, kurios juridinio subjekto sąrankoje pažymėta parinktis **Naudoti finansinio pašalinimo procese**.

Jei reikia, galite nustatyti pašalinimo taisyklės įsigaliojimo datą ir galiojimo pabaigos datą. Turite nustatyti parinkties **Aktyvus** reikšmę **Taip**, jei norite, kad pašalinimo taisyklę būtų galima naudoti pašalinimo pasiūlymo proceso metu. Pasirinkite žurnalo, kurio žurnalo tipas **Pašalinimas**, pavadinimą.

![Pagrindinės pašalinimo taisyklės ypatybės](./media/ledger-elimination-rule-journal.png "Pagrindinės pašalinimo taisyklės ypatybės")

Nurodę pagrindines ypatybes, nustatykite pačias apdorojimo taisykles pasirinkdami **Eilutės**. Galimos dvi šalinimo parinktys: grynojo pokyčio sumos pašalinimas arba fiksuotos sumos nustatymas.

Pasirinkite pirmines sąskaitas. Žvaigždutę (\*) galite naudoti kaip universalųjį simbolį. Pvz., nurodžius **1\***, kaip paskirstymo duomenų šaltinis būtų pasirinktos visos sąskaitos, kurios prasideda **1**.

Pasirinkę pirmines sąskaitas, naudokite lauką **Sąskaitos specifikacija**, kad nurodytumėte sąskaitą, naudojamą paskirties įmonėje. Pasirinkite **Pirminė**, jei norite naudoti tą pačią pagrindinę sąskaitą, kuri nurodyta pirminėje sąskaitoje. Jei pasirinksite **Nurodyta vartotojo**, turite nurodyti paskirties sąskaitą.

![Puslapis DK pašalinimo taisyklės eilutė](./media/ledger-elimination-rule-line.png "Puslapis DK pašalinimo taisyklės eilutė")

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

## <a name="benefits-of-using-financial-reporting-for-financial-consolidations-and-currency-translation-or-to-complement-consolidate-online-for-consolidated-reporting"></a>Finansinių ataskaitų privalumai vykdant finansinį konsolidavimą ir valiutos konvertavimą arba privalumai, naudingi vykdant konsolidavimo ataskaitų konsolidavimą tinkle
Klientai gali pasinaudoti finansinių ataskaitų privalumais vykdant finansinį konsolidavimą ir valiutos konvertavimą arba privalumais, naudingais vykdant konsolidavimo ataskaitų konsolidavimą tinkle.

- **Duomenų gylis** – galite kurti konsoliduotas ataskaitas, kurios sujungiami faktiniai ir biudžeto duomenys sąskaitos lygiu ir dimensijos lygiu. „Finance and Operations“ šie duomenys apima duomenis iš biudžeto kontrolės ir biudžeto plano.
- **Dinaminis konsolidavimas** – konsolidavimą galima vykdyti bet kuriuo metu ir bet kokiu organizacijos hierarchijos lygiu.
- **Visos audito galimybės** – visa dimensijų, sąskaitų ir operacijų informacija tvarkoma analizės ir audito tikslais. Be to, finansinėse ataskaitose galima visiškai atstatyti detalizuotą pradinės operacijos vaizdą bet kuriame konsoliduojamame juridiniame subjekte.
- **Supaprastintas valiutos konvertavimas** – atlikę minimalią „Finance and Operations“ sąranką, galite konvertuoti bet kurią finansinių ataskaitų ataskaitos valiutą į bet kurią nustatytą ataskaitų valiutą. Be to, galite nustatyti neribotą ataskaitų valiutų skaičių.
- **Pašalinimų registravimas šaltinyje** – galite kurti ir spausdinti pašalinimo ataskaitą, kad patvirtintumėte pašalinimo operacijas. Tada galite registruoti bet kokius naujus pašalinimus kaip įprastines vidinės įmonės operacijas. Taip pat pašalinimo juridinį subjektą galite naudoti bet kurioje operacijoje, kurios nenorite taikyti savo juridiniams subjektams.

## <a name="supported-consolidation-scenarios"></a>Palaikomi konsolidavimo scenarijai
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
