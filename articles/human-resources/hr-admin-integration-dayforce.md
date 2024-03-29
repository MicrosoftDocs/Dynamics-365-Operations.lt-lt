---
title: Integravimo su „Dayforce“ konfigūravimas
description: Šiame straipsnyje aprašomi būtini konfigūracijos žingsniai, reikalingi integravimui tarp Microsoft Dynamics 365 Human Resources ir Ceriforce Dayforce.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5a5d296dd4c1b09065fc47673dd540d8c122c482
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896140"
---
# <a name="configure-integration-with-dayforce"></a>Integravimo su „Dayforce“ konfigūravimas


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Integravimas tarp „Microsoft Dynamics 365 Human Resources“ ir „Ceridian Dayforce“ paremtas keliais konfigūravimo veiksmais, aprašytais šiame straipsnyje. Prieš mokėjimo vykdymo apdorojimą turite sukonfigūruoti integravimą tiek „Human Resources“, tiek „Dayforce“.

Kai naudojate paslaugas, pvz., „Dayforce“ kad atliktumėte mokėjimų vykdymus, turite įjungti integravimą į „Human Resources“. Integravimui reikalingi konkretūs duomenys iš „Human Resources“. Todėl turite patvirtinti, kad duomenys, susieti su „Dayforce“, yra sukonfigūruojami „Human Resources“ taip, kad integravimas būtų palaikomas. Integravimui naudojamos šios plačios duomenų kategorijos:

- Personalo duomenys
- Atlyginimo dalies duomenys
- Algalapio duomenys, pvz., mokėjimo ciklai, mokėjimo laikotarpiai ir pajamų kodai
- Darbuotojo duomenys

Šiame straipsnyje aprašomi veiksmai, kuriuos turite atlikti, kad įgalintumėte integravimą, ir paaiškinami integravimo duomenų tipai ir konfigūracijos informacija.

## <a name="enable-the-integration"></a>Integravimo įjungimas

Pirmiausia programoje „Human Resources“ turite įjungti integravimą ir įvesti konfigūravimo informaciją, kad prisijungtumėte prie „Dayforce“. Jei norite, kad Microsoft Dynamics didžiosios knygos operacija, kuri gaminama, būtų importuojama į "365 Finance", Microsoft Azure taip pat turite nustatyti saugojimo sąskaitą ir įvesti "Azure" saugyklos ryšio eilutę finansuose.

Norėdami įjungti integravimą į „Human Resources“, atlikite šiuos veiksmus.

1. Puslapyje **Sistemos administravimas** pasirinkite **Integravimo konfigūracija**.
2. Įveskite saugų failų perdavimo protokolo (FTP) galinį punktą ir saugų FTP aplanko kelią.
3. Įveskite vardą ir slaptažodį to vartotojo, kuris turės prieigą prie saugaus FTP galinio punkto ir aplanko kelio.
4. Tinkamai išbandykite ryšį ir nustatykite parinktį **Įjungti algalapių integravimą** į **Taip**.

Kai integravimas įjungiamas, sukuriamas duomenų eksportavimo paketas bei failai ir nustatomas dažnumas. Galite pakeisti šį dažnumą pagal poreikį.

Daugiau informacijos apie „Azure“ saugyklos paskyras ir „Azure Storage“ jungimosi eilutes rasite šiose „Azure“ temose:

- [Apie „Azure“ saugyklos paskyras](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [„Azure Storage“ jungimosi eilučių konfigūravimas](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a>Techninė informacija apie algalapių integravimo įjungimą

Įjungus algalapių integravimą gaunami du pagrindiniai rezultatai:

- Sukuriamas duomenų eksportavimo projektas pavadinimu Atlyginimų integravimo eksportavimas. Šiame projekte yra objektai ir laukai, kurie būtini norint užtikrinti algalapių integravimą. Norėdami analizuoti projektą, eikite į **Sistemos administravimas**, pasirinkite plytelę **Duomenų valdymas**, tada projektų sąraše atidarykite duomenų projektą.
- Ši paketinė užduotis vykdo duomenų eksportavimo projektą, užšifruoja gautą duomenų paketą ir perduoda duomenų paketo failą į SFTP galinį punktą, sukonfigūruotą ekrane **Integravimo konfigūracija**.

> [!NOTE]
> Duomenų paketas, perduotas į SFTP galinį punktą, užšifruojamas naudojant unikalų pakuotės raktą. Raktas laikomas „Azure Key Vault“, kurį gali pasiekti tik „Ceridian“. Neįmanoma iššifruoti ir išanalizuoti duomenų paketo turinio. Jei reikia analizuoti duomenų paketo turinį, reikės rankiniu būdu eksportuoti duomenų projektą Atlyginimų integravimo eksportavimas, jį atsisiųsti ir tada atsidaryti. Eksportuojant rankiniu būdu nebus taikomas šifravimas ir paketas nebus perduodamas.

## <a name="configure-your-data"></a>Jūsų duomenų konfigūravimas 

Kad apdorotumėte algalapį, turite sukonfigūruoti personalo duomenis „Human Resources“. Turite nustatyti organizacijos duomenis, pvz., užduotis ir pareigas, taip pat išmokų ir atlyginimo dalies informaciją. Čia pateikiama įdarbinimo, mokėjimų ir atskaitymų informacija, būtina tam, kad būtų galima sugeneruoti darbuotojo mokėjimą.

### <a name="human-resource-data"></a>Personalo duomenys

#### <a name="benefits"></a>Išmokos 

Personalas pateikia įrankius, kuriuos galima naudoti norint nustatyti ir tvarkyti organizacijos darbuotojams siūlomas arba apdorojamas išmokas, atskaitymus ir darbininkų atlyginimų dalies planus.

Kurdami išmokas turėkite omenyje, kad toliau pateikiami duomenys ir konfigūracijos naudojami „Dayforce“.

##### <a name="benefit-plans"></a>Išmokų planai

- Planas (būtina)
- Tipas (būtina)
- Poveikis algalapiui (būtina)
- Susigrąžinti skolas
- Atskaitymo metodas
- Atskaitymo pirmumas
- Apribojimo laikotarpis
- Limito suma

##### <a name="benefits"></a>Išmokos

- Planas (būtina)
- Tipas (būtina)
- Parinktis (būtina)
- Išmokos ID (būtina)
- Dažnumas
- Pagrindas
- Suma arba tarifas
- Pajamų kodas

##### <a name="supported-frequencies"></a>Palaikomi dažnumai 

- Savaitinis
- Už dvi savaites
- Kas pusę mėnesio
- Mėnesinis

##### <a name="supported-bases"></a>Palaikomos bazės 

- Fiksuota suma
- Pajamų procentinė dalis
- Produktyvios valandos

„Dayforce“ sukuria šiuos atskaitymus pagal poveikį atlyginimui, šis poveikis apibrėžiamas išmokų plane.

| Pasirinkimas programoje „Human Resources“        | Rezultatas „Dayforce“                            |
|----------------------------|-----------------------------------------------|
| Jokia                       | Nesukuriama jokio atskaitymo.                      |
| Tik atskaitymas             | Sukuriamas darbuotojo atskaitymas.             |
| Tik įnašas          | Sukuriamas darbdavio atskaitymas.             |
| Atskaitymas ir įnašas | Sukuriami darbuotojo ir darbdavio atskaitymai. |

Daugiau informacijos apie tai, kaip nustatyti ir tvarkyti išlaidų programą, rasite šiose temose:

- [Pristatyti darbuotojų išmokų programą](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [Kurti naują išmoką](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [Apibrėžti išmokų tinkamumo taisykles ir strategijas](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [Užregistruoti ir pašalinti išmokas darbuotojams](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a>Atlyginimo dalis 

Atlyginimų dalies valdymas naudojamas kontroliuoti pagrindinio užmokesčio ir premijų pristatymui. Darbuotojo fiksuotas pagrindinis užmokestis ir nuopelnų padidėjimai kontroliuojami naudojant pastoviosios atlyginimo dalies dalies planus. Skatinamųjų išmokų, pvz., priedų, apdovanojimų už našumą, akcijų pasirinkimo sandorių, subsidijų bei vienkartinių premijų mokėjimas valdomas naudojant kintamosios atlyginimo dalies dalies planus.

„Dayforce“ naudojama atlyginimo dalies informacija, kad būtų apskaičiuotas darbuotojo valandinis ar metinis tarifas. Būtini pastoviosios atlyginimo dalies planai ir užmokesčio tarifo konvertavimas. Darbuotojai turi būti susieti su pastoviosios atlyginimo dalies planu.

Daugiau informacijos apie kompensacijų planus rasite šios temose:

- [Pastoviosios atlyginimo dalies planų kūrimas](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [Kintamosios atlyginimo dalies planų kūrimas](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [Kurti atlyginimų / kompensavimo struktūrą ir planus](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [Kompensavimo apdorojimas](/dynamics365/unified-operations/talent/process-compensation)
- [Kompensavimo proceso nustatymas ir rezultatų skaičiavimas](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [Darbuotojo įtraukimas į fiksuoto atlyginimo dalies planą](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [Darbuotojo įtraukimas į kintamosios atlyginimo dalies planą](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a>Darbai 

Užduotis yra užduočių ir pareigų, kurias asmeniui reikia įvykdyti, rinkinys. Daugiau informacijos ieškokite šiose temose:

- [Užduoties komponentų nustatymas](/dynamics365/unified-operations/talent/create-job)
- [Apibrėžti naujas užduotis](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a>Pareigybės

Pareigos yra atskiros užduoties egzemplioriaus. Pavyzdžiui, pareigos „Pardavimo vadybininkas (rytų regionas)“ yra vienos iš pareigų, susietų su užduotimi „Pardavimo vadovas“. Pareigos egzistuoja padalinyje. Su kiekvienomis pareigomis galima susieti tik vieną darbuotoją.

Nustatydami pareigas, atkreipkite dėmesį į šiuos duomenis ir konfigūravimą:

- Pareigos (būtina)
- Aprašas (būtina)
- Užduotis (būtina)
- Padalinys (būtina)
- Pareigų tipas (būtina)
- Viso etato ekvivalentas
- Įprastos darbo valandos per metus (būtina)
- Apmokama juridinio subjekto (būtina)
- Mokėjimo ciklas (būtina)
- Numatytosios finansinės dimensijos – išlaidų centras (būtina)
- Darbininko priskyrimas – darbininkas, priskyrimo pradžia, priskyrimo pabaiga, priežasties kodas

Jei tame pačiame padalinyje su tuo pačiu darbu susiejamos kelios pareigos, „Dayforce“ jos yra konsoliduojamos į vienas pareigas.

Daugiau informacijos ieškokite šiose temose:

- [Darbo jėgos organizavimas naudojant padalinius, darbo vietas ir pareigas](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [Pareigų nustatymas](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a>Padaliniai

Padalinys yra valdymo vienetas, nurodantis organizacijos kategoriją arba funkcinę sritį. Padalinys yra atsakingas už tam tikrą organizacijos sritį, pvz., pardavimą, apskaitą arba personalą. Padalinius galite naudoti norėdami pranešti apie funkcines sritis. Padaliniai gali turėti pelno ir nuostolio atsakomybę.

Daugiau informacijos ieškokite šiose temose:

- [Padalinio kūrimas ir priskyrimas padalinių hierarchijai](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [Apibrėžti naujus padalinius](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a>Mokėjimo ciklai ir mokėjimo laikotarpiai

Mokėjimo ciklas lemia algalapio pateikimo dažnumą ir konkrečias dienas, kuriomis sumokama darbininkams. Pavyzdžiui, mokėjimo ciklas gali būti mėnesinis ir darbuotojams gali būti sumokėta paskutinę mėnesio dieną. Mokėjimo ciklas taip pat gali būti savaitinis, o darbuotojams gali būti sumokama kitą antradienį po mokėjimo laikotarpio pabaigos. Mokėjimo ciklai priskiriami pareigoms tam, kad būtų galima valdyti, kada sumokama tas pareigas einantiems darbininkams.

Sukūrę mokėjimo ciklus, galite generuoti kiekvieno ciklo mokėjimo laikotarpius. Į kiekvieną mokėjimo laikotarpį įeina numatytoji mokėjimo data, paremta jūsų pateikta informacija. Tačiau galite pakeisti numatytąją mokėjimo datą mokėjimo laikotarpyje, kad leistumėte išimtis, pvz., tuo atveju, jei mokėjimo data sutampa su švente.

„Dayforce“ naudojama ši informacija:

- Mokėjimo ciklas (būtina)
- Mokėjimo ciklo dažnumas (būtina)
- Laikotarpio pradžios data (būtina pirmajam mokėjimo laikotarpiui)
- Numatytoji mokėjimo data (būtina pirmajam mokėjimo laikotarpiui)

Ši informacija yra integruota į „Dayforce“ kaip mokėjimo grupės ir skiriasi priklausomai nuo šalies ar regiono kiekvienam mokėjimo ciklui. Prieš integravimą reikia sugeneruoti bent vieną mokėjimo laikotarpį. „Dayforce“ sugeneruoja mokėjimo grupių kalendorius ir mokėjimo datas pagal pirmojo laikotarpio pradžios datą ir numatytojo mokėjimo datą, nustatytą „Human Resources“.

#### <a name="earning-codes"></a>Pajamų kodai

Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas. Kodams būdingi įvairūs parametrai, susiję su pajamomis, pvz., apskaitos taisyklės, mokesčių įstatymai, ataskaitų kūrimo reikalavimai ir bendrųjų sumų pajėgumas.

„Dayforce“ naudojama ši informacija:

- Pajamų kodas (būtina)
- aprašymas
- Matavimo vienetas
- Produktyvus

### <a name="worker-data"></a>Darbininko duomenys

Įrašai apie jūsų turimus darbininkų tipus yra svarbūs jūsų personalo ir algalapių sistemoms. Informacija, kurią įvedate, gali būti naudojama darbininkų ir asmeninei informacijai sekti.

Galite tvarkyti šią darbininkų informaciją:

- **Pagrindinė** – tvarkykite pagrindinę darbininko informaciją, pvz., kontaktinę informaciją, demografinę informaciją, identifikacijos informaciją, šeimos informaciją, santykį su karine tarnyba, informaciją apie gyvenimą ne tėvynėje ir asmeninius kontaktus bei kontaktinius asmenis nelaimės atveju.
- **Įdarbinimas** – tvarkykite informaciją apie darbininko įdarbinimą, pvz., priklausymą įmonei ar organizacijai, priskyrimą pareigoms, pradžios ir pabaigos datas, tinkamumą dirbti, darbo režimą, pensiją, atostogas ir informaciją apie perkėlimą.
- **Atostogos ir nebuvimas** – tvarkykite informaciją apie darbininko nebuvimą, pvz., darbo kalendorius, nebuvimo operacijas ir nebuvimo nustatymą.
- **Atlyginimo dalis ir algalapis** – tvarkykite informaciją apie darbininko atlyginimo dalies planus ir algalapio informaciją, pvz., plano registraciją, apdovanojimus, našumą, komisinius, mokesčių informaciją, išėjimą į pensiją ir atskaitymus iš atlyginimų.

Įvesdami darbininko informaciją turėkite omenyje, kad toliau pateikiami duomenys ir konfigūracijos naudojami „Dayforce“.

#### <a name="general-information"></a>Bendroji informacija

- Darbuotojo numeris (būtina)
- Vardas (būtinas)
- Pavardė (būtinai)
- Antras vardas
- Paaukštinimo data
- Žinoma kaip

#### <a name="personal-information"></a>Asmeninė informacija

- Šeiminė padėtis (būtina)
- Gimimo data (būtina)
- Lytis (būtina)
- Asmuo su negalia
- Pilietybės šalies regionas (tik Meksikai)

#### <a name="address-information"></a>Adresas

- Pagrindinis (būtina)
- Šalis / regionas (būtina)
- Pašto kodas (būtina)
- Gatvės numeris (būtina) (tik Meksikai)
- Pastatų kompleksas (tik Meksikai)
- Miestas (būtina)
- Valstija (būtina)
- Apygarda (būtina)

#### <a name="contact-information"></a>Kontaktinė informacija 

- Pirminis (būtina)
- Kontakto numeris (būtina)
- Išplėtimas

#### <a name="payroll-information-and-earning-codes"></a>Algalapio informacija ir pajamų kodai

Darbuotojams gali būti priskirtos tam tikros pajamos, išmokamos tam tikru dažnumu, darbuotojai gali turėti pageidaujamą mokėjimo būdą. Toliau pateikiami laukeliai naudojami „Dayforce“, kad būtų užtikrinta, jog naudojamos tos parinktys ir nustatymai.

##### <a name="earning-codes"></a>Pajamų kodai

- Pareigos (būtina)
- Pajamų kodas (būtina)
- Dažnumas (būtina)
- Suma (būtina)

##### <a name="payroll-information"></a>Algalapių informacija

- Mokėjimo būdas
- Ekonominė sritis (būtina)
- Darbuotojų išmokų ID
- Asmens kodas (būtina)
- Karo tarnybos numeris
- Pamainos ID (būtina)
- Mokesčių numeris (būtina)
- Sąjungos ID (būtina)
- Darbo dienos ID (būtina)
- Darbo leidimo numeris

> [!NOTE]
> Meksikoje palaikomi šie mokėjimo būdai – **Grynieji**, **Čekis** (įmonės fizinis čekis) ir **Elektroninis mokėjimas**. Jei konkretus mokėjimo būdas nenurodytas, kaip numatytasis būdas naudojamas **Čekis**.

#### <a name="employment-details"></a>Įdarbinimo informacija

Detali įdarbinimo retrospektyva naudojama kaip pagrindinis informacijos šaltinis, kuriuo remiantis „Dayforce“ gaunamos darbuotojo samdos, atleidimo ir pakartotinės samdos būsenos. „Dayforce“ palaiko tik vieną įdarbinimo įrašą vienu metu.

- Įdarbinimo pradžios data (būtina)
- Įdarbinimo pabaigos data
- Pradžios data
- Patikslinta darbo pradžios data
- Atleidimo data (būtina po atleidimo)
- Atleidimo priežastis (būtina po atleidimo)

Darbuotojo pagrindinės datos gaunamos naudojant toliau pateikiamą informaciją.

| Personalas                | „Dayforce“                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| Naujausia samdos data | Dabartinio nenutraukto įdarbinimo retrospektyvos įrašo įdarbinimo pradžia                                 |
| Atleidimo data      | Dabartinio nenutraukto įdarbinimo retrospektyvos įrašo atleidimo data                                 |
| Pradžios data            | Dabartinio neaktyvios įdarbinimo retrospektyvos įrašo koreguota pradžios data, pradžios data ar įdarbinimo pradžia |
| Pradinio įdarbinimo data    | Anksčiausio įdarbinimo retrospektyvos įrašo įdarbinimo pradžia                                               |

#### <a name="compensation"></a>Atlyginimo dalis

Pastoviosios atlyginimo dalies planas turi būti susietas su kiekvieno darbuotojo pagrindinėmis pareigomis įdarbinimo laikotarpio metu. Šis laikotarpis prasideda nuo tos datos, kai darbuotojas pasamdomas (ar įdarbinimo pradžios datos), ir tęsiasi iki atleidimo.

- Įsigaliojimo data (būtina)
- Galiojimo pabaigos data
- Užmokesčio tarifas (būtina)
- Užmokesčio tarifo konvertavimas (būtina)
- Metinis atitikmuo (būtina)
- Valandinis atitikmuo (būtina)

Jei pagal valandas apmokamas darbuotojas eina kelias pareigas, pagrindinių pareigų pastovioji atlyginimo dalis importuojama į „Dayforce“ kaip darbuotojo lygmens bazinis tarifas / alga. Nepagrindinių pareigų valandinis tarifas išsaugomas atitinkamose pareigose „Dayforce“.

Jei etatinis darbuotojas eina kelias pareigas, iš visų aktyvių pareigų išvedamas suvestinis valandinis tarifas bei metinė alga ir jie naudojami kaip darbuotojo lygmens bazinis tarifas / alga.

#### <a name="identification-numbers"></a>Identifikavimo numeriai

##### <a name="social-security-identifier"></a>Socialinio draudimo identifikatorius 

Kiekvienas darbuotojas turi turėti vieną pirminį identifikatorių. Šis identifikatorius turi būti **SSN** identifikacijos tipo. „Dayforce“ jis automatiškai išvedamas kaip darbuotojo socialinio draudimo identifikatorius, kuris yra būtinas samdai.

- Pirminis (būtina)
- Identifikacijos tipas = "SSN"
- Išdavimo data
- Galiojimo data

Darbuotojai gali deklaruoti kelis **SSN** identifikacijos tipo identifikacijos numerius. Tačiau tik įrašas, pažymėtas kaip **Pirminis**, yra integruojamas į „Dayforce“, nepriklausomai nuo to, ar numeris yra aktyvus ar negaliojantis.

#### <a name="bank-accounts-and-disbursements"></a>Banko sąskaitos ir išmokos

Jei darbuotojas pasirinko, kad pinigai jam būtų pervesti pavedimu į jo banko sąskaitą, būtina įvesti galiojančią banko sąskaitos informaciją.

| Personalas                         | „Dayforce“                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| Banko sąskaitos numeris (būtina) |                                                                                                             |
| SWIFT kodas (būtina)          | **Banko ID** laukelis naudojamas, apdorojant algalapį Meksikoje.                                                             |
| Filialo numeris (būtina)       |                                                                                                             |
| Banko sąskaitos tipas (būtina)   | **Sąskaitos tipo** laukelis naudojamas apdorojant algalapį Meksikoje. Į palaikomas vertes įeina **Tikrinimas** ir **Algalapis**. |

> [!NOTE]
> Darbuotojai, pasirinkę apmokėjimą pavedimu į banko sąskaitą, turi pateikti nuorodą į likučio sąskaitą, esančią juridiniame subjekte, kurio pirminis adresas yra Meksikoje ir kuris yra susietas su galiojančia banko sąskaita Meksikos banke. Visos kitos nelikutinės sąskaitos yra ignoruojamos.

#### <a name="address-information"></a>Adresas

Kiekvienas darbuotojas turi turėti vieną pirminę vietą. „Dayforce“ ši vieta naudojama darbuotojo pagrindinei gyvenamajai vietai nustatyti mokesčių tikslais.

- Pirminis (būtina)
- Šalis / regionas (būtina)
- Pašto kodas (būtina)
- Gatvė (būtina)
- Gatvės numeris (būtina)
- Pastatų kompleksas
- Miestas (būtina)
- Valstija (būtina)
- Apygarda (būtina)

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a>Duomenų konfigūravimas norint generuoti algalapius JAV ir Kanadoje

Jei generuojate užmokesčius darbuotojams JAV ir Kanadoje, reikia sukonfigūruoti šiuos elementus:

- Su pareigomis būtina nurodyti padalinius.
- Išlaidų centrai turi būti nustatyti kaip finansinės dimensijos ir būti pirmas elementas numatytoje finansinės dimensijos eilutėje.

> [!NOTE] 
> Galite sukonfigūruoti „Human Resources“, kad prie pareigų būtų nurodytas padalinys. Norėdami tai atlikti, eikite į **Bendrinamos personalo pareigos > Pareigos > Prie pareigų reikalauti padalinių**. Rekomenduojame integruojant šį parametrą taikyti.

### <a name="job-types"></a>Pareigų rūšys

Užduočių tipai naudojami sugrupuoti panašioms užduotims į kategorijas. Užduočių tipai būtini tam, kad algalapiai būtų apdoroti JAV ir Kanadoje. Kai kurie užduočių tipų pavyzdžiai: visa darbo diena ar ne visa darbo diena arba atlyginimas ir valandinis užmokestis. Užduočių tipai yra susieti su „Dayforce“ kaip mokėjimo tipai, nurodantys, ar darbuotojas gauna valandinį ar fiksuotą užmokestį.

Šie užduočių tipai ir aprašai yra būtini.

| Darbo vietos tipas   | aprašymas |
|------------|-------------|
| Valandinis     | Valandinis      |
| Fiksuotas atlyginimas   | Fiksuotas atlyginimas    |

### <a name="position-types"></a>Pareigų tipai 

Pareigų tipus naudojate tam, kad apibrėžtumėte, ar pareigoms skirta visa darbo diena, ne visa darbo diena ar kad esama dar kito varianto. Pareigų tipai yra susieti su „Dayforce“ kaip mokėjimo klasės, nurodančios, ar darbuotojas dirba visą ar ne visą darbo dieną.

Šie pareigų tipai ir aprašai yra būtini.

| Pareigų tipas   | aprašymas        |
|-----------------|--------------------|
| Visą darbo dieną       | Darbuotojas, dirbantis visą darbo dieną |
| Ne visą darbo dieną       | Darbuotojas, dirbantis ne visą darbo dieną |

### <a name="reason-codes"></a>Priežasčių kodai

Priežasčių kodai pateikia informaciją apie darbuotojo būseną. Priežasčių kodai yra susieti su „Dayforce“ kaip būsenos priežastys, nurodančios darbuotojo pareigų ar įdarbinimo būsenos pokyčių priežastį.

Šie priežasčių kodai ir aprašai yra būtini.

| Tikslinės paskirties šifras    | aprašymas      | Taikomi scenarijai |
|----------------|------------------|----------------------|
| RESIGNATION    | Atsistatydinimas      | Atleisti darbininką     |
| TERMINATION    | Atleidimas      | Atleisti darbininką     |
| RETIREMENT     | Išėjimas į pensiją       | Atleisti darbininką     |
| KITA          | Kitos priežastys    | Atleisti darbininką     |
| DEATH          | Mirtis            | Atleisti darbininką     |
| LEAVEOFABSENCE | Laisvadienis | Atleisti darbininką     |
| CONTRACTEND    | Sutarties pabaiga  | Atleisti darbininką     |
| SALARYCHANGE   | Atlyginimo pasikeitimas | Atlyginimo dalis         |

### <a name="marital-status"></a>Šeiminė padėtis

Šeiminės padėties vertės yra susietos su „Dayforce“ ir išverčiamos, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.

Toliau pateikiamoje lentelėje parodoma, kaip šeiminės padėties vertės yra susietos su „Dayforce“.

| Personalas                 | „Dayforce“             |
|------------------------|----------------------|
| Vedęs/ištekėjusi                | Vedęs/ištekėjusi              |
| Nevedęs / neištekėjusi                 | Nevedęs / neištekėjusi               |
| Našlys (-ė)                | Našlys (-ė)              |
| Išsiskyręs (-usi)               | Išsiskyręs (-usi)             |
| Registruota partnerystė | Civilinė partnerystė |
| Nėra                   | Nėra                 |
| Sugyventiniai             | Sugyventiniai           |

### <a name="gender"></a>Giminė

Paskirtoji lytis yra susieta su „Dayforce“ ir išverčiama, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.

Toliau pateikiamoje lentelėje parodoma, kaip paskirtoji lytis yra susieta su „Dayforce“.

| Personalas       | „Dayforce“        |
|--------------|-----------------|
| Vyras         | Vyras            |
| Moteris       | Moteris          |
| Konkrečiai nenurodyta | *Nepalaikoma* |

### <a name="earning-codes"></a>Pajamų kodai

Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas. Kodai apibrėžia kelis parametrus, susijusius su pajamomis, pvz., apskaitos taisykles, mokesčių įstatymus, ataskaitų kūrimo reikalavimus ir bendrųjų sumų pajėgumą. Jei naudojamas nepalaikomas dažnumas, skaičiavimams naudojamas iš anksto numatytasis dažnumas **Kiekvienas mokėjimas**.

#### <a name="supported-frequencies"></a>Palaikomi dažnumai

- Visos
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Adresai

Konkrečios šalies ar regiono, valstijos ir apygardos (savivaldybės) kodų identifikacijai reikalingi tam tikri formatai, kuriuos gali atpažinti „Dayforce“ ir šalyje / regione veikiantys teikėjai. Nors miestų formatas yra kintamas, kiekvienas miestas turi būti susietas su valstija.

| Personalas          | „Dayforce“              |
|-----------------|-----------------------|
| Šalis/regionas  | Šalies kodas          |
| Pašto kodas | Pašto indeksas           |
| Apskritis           | Valstijos kodas            |
| Miestas            | Miestas                  |
| Apygarda          | Apygarda (savivaldybė) |
| Gatvė          | 1 adreso eilutė        |

### <a name="tax-regions"></a>Mokesčių regionai

Mokesčių regionai naudojami apibrėžti tinkamam mokesčiui, kuris turėtų būti taikomas generuojant algalapį. Mokesčių regionai yra susieti su „Dayforce“ vietų adresais. Numatytasis mokesčių regionas turi būti susietas su darbininko aktyviomis pareigomis. 

- Mokesčių regionas (būtina)
- Šalis / regionas (būtina)
- Valstija (būtina)
- Apygarda 
- Miestas (būtina)

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a>Duomenų konfigūravimas sugeneruoti algalapiui Meksikoje

Jei generuojate mokėjimus darbuotojams Meksikoje, reikia sukonfigūruoti šiuos elementus:

- Su pareigomis būtina nurodyti padalinius.
- Išlaidų centrai turi būti nustatyti kaip finansinės dimensijos ir būti pirmas elementas numatytoje finansinės dimensijos eilutėje.

### <a name="job-types"></a>Užduočių tipai

Užduočių tipai naudojami sugrupuoti panašioms užduotims į kategorijas. Užduočių tipai yra būtini, kad algalapis būtų apdorotas Meksikoje. Kai kurie užduočių tipų pavyzdžiai: visa darbo diena ar ne visa darbo diena arba atlyginimas ir valandinis užmokestis. Užduočių tipai yra susieti su „Dayforce“ kaip mokėjimo tipai, nurodantys, ar darbuotojas gauna valandinį ar fiksuotą užmokestį.

Šie užduočių tipai ir aprašai yra būtini.

| Darbo vietos tipas   | aprašymas |
|------------|-------------|
| Valandinis     | MX valandinis   |
| Fiksuotas atlyginimas   | MX fiksuotas atlyginimas |

### <a name="position-types"></a>Pareigų tipai 

Pareigų tipus naudojate tam, kad apibrėžtumėte, ar pareigoms skirta visa darbo diena, ne visa darbo diena ar kad esama dar kito varianto. Pareigų tipai yra susieti su „Dayforce“ kaip mokėjimo klasės, nurodančios, ar darbuotojas dirba visą ar ne visą darbo dieną.

Šie pareigų tipai ir aprašai yra būtini.

| Pareigų tipas   | aprašymas        |
|-----------------|--------------------|
| Visą darbo dieną       | Darbuotojas, dirbantis visą darbo dieną |
| Ne visą darbo dieną       | Darbuotojas, dirbantis ne visą darbo dieną |

### <a name="reason-codes"></a>Priežasčių kodai

Priežasčių kodai pateikia informaciją apie darbuotojo būseną. Priežasčių kodai yra susieti su „Dayforce“ kaip būsenos priežastys, nurodančios darbuotojo pareigų ar įdarbinimo būsenos pokyčių priežastį.

Šie priežasčių kodai ir aprašai yra būtini.

| Tikslinės paskirties šifras            | aprašymas                    | Taikomi scenarijai |
|------------------------|--------------------------------|----------------------|
| DEPARTUREBEFOREPAYMENT | Išvykimas prieš pirmą algalapį | Atleisti darbininką     |
| RESIGNATION            | Atsistatydinimas                    | Atleisti darbininką     |
| PENSION                | Pensija                        | Atleisti darbininką     |
| TERMINATION            | Atleidimas                    | Atleisti darbininką     |
| RETIREMENT             | Išėjimas į pensiją                     | Atleisti darbininką     |
| ABSENTEE               | Nesantysis                       | Atleisti darbininką     |
| KITA                  | Kitos priežastys                  | Atleisti darbininką     |
| CLOSURE                | Įmonės uždarymas               | Atleisti darbininką     |
| DEATH                  | Mirtis                          | Atleisti darbininką     |
| LEAVEOFABSENCE         | Laisvadienis               | Atleisti darbininką     |
| CONTRACTEND            | Sutarties pabaiga                | Atleisti darbininką     |
| SALARYCHANGE           | Atlyginimo keitimas               | Atlyginimo dalis         |

### <a name="terms-of-employment"></a>Įdarbinimo sąlygos

Įdarbinimo sąlygos naudojamos įdarbinimo sąlygų kategorijoms kurti. Sąlygos yra susietos su „Dayforce“ kaip įdarbinimo indikatorių vertės.

Šios įdarbinimo sąlygos ir aprašai yra būtini.

| Įdarbinimo sąlygos   | aprašymas |
|-----------------------|-------------|
| Reguliarus               | Reguliarus     |
| Tiesioginis                | Tiesioginis      |
| Stažuotė            | Stažuotė  |
| Nuolatinis             | Nuolatinis   |

### <a name="marital-status"></a>Šeiminė padėtis

Šeiminės padėties vertės yra susietos su „Dayforce“ ir išverčiamos, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.

Toliau pateikiamoje lentelėje parodoma, kaip šeiminės padėties vertės yra susietos su „Dayforce“.

| Personalas                 | „Dayforce“                  |
|------------------------|---------------------------|
| Vedęs/ištekėjusi                | Vedęs/ištekėjusi                   |
| Nevedęs / neištekėjusi                 | Nevedęs / neištekėjusi                    |
| Našlys (-ė)                | Našlys (-ė)                   |
| Išsiskyręs (-usi)               | Išsiskyręs (-usi)                  |
| Registruota partnerystė | Civilinė partnerystė      |
| Nėra                   | *Nepalaikoma Meksikoje* |
| Sugyventiniai             | *Nepalaikoma Meksikoje* |

### <a name="gender"></a>Giminė

Paskirtoji lytis yra susieta su „Dayforce“ ir išverčiama, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.

Toliau pateikiamoje lentelėje parodoma, kaip paskirtoji lytis yra susieta su „Dayforce“.

| Personalas       | „Dayforce“                  |
|--------------|---------------------------|
| Vyras         | Vyras                      |
| Moteris       | Moteris                    |
| Konkrečiai nenurodyta | *Nepalaikoma Meksikoje* |

### <a name="payment-method"></a>Mokėjimo būdas

Mokėjimo būdai leidžia darbuotojui ir įmonei apibrėžti darbuotojų apmokėjimą. Mokėjimo būdai yra susieti su „Dayforce“ ir išverčiami, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.

Toliau pateikiamoje lentelėje parodoma, kaip mokėjimo būdai yra susieti su „Dayforce“.

| Personalas             | „Dayforce“                  |
|--------------------|---------------------------|
| Grynieji pinigai               | Grynieji pinigai                      |
| Elektroninis mokėjimas | Perkelti                  |
| Tikrinti              | Čekis                    |
| Banko čekis         | *Nepalaikoma Meksikoje* |
| Kiti              | *Nepalaikoma Meksikoje* |

### <a name="bank-account-type"></a>Banko sąskaitos tipas

Banko sąskaitų tipai naudojami elektroniniams mokėjimams į darbuotojų sąskaitas vykdyti. Banko sąskaitų tipai yra susieti su „Dayforce“ kaip pavedimų sąskaitos informacija. Banko sąskaitų tipai yra išverčiami, priklausomai nuo aplinkybių, į priimtas vertes po integravimo.

| Personalas            | „Dayforce“                  |
|-------------------|---------------------------|
| Čekių sąskaita  | Čekių sąskaita           |
| Algalapių sąskaita   | Algalapių sąskaita            |
| Taupomoji sąskaita   | *Nepalaikoma Meksikoje* |
| „BankGirot“ sąskaita | *Nepalaikoma Meksikoje* |
| „PlusGirot“ sąskaita | *Nepalaikoma Meksikoje* |

### <a name="earning-codes"></a>Pajamų kodai

Naudojant pajamų kodus unikaliai identifikuojamas kiekvienas darbininkų gaunamų pajamų tipas. Kodai apibrėžia kelis parametrus, susijusius su pajamomis, pvz., apskaitos taisykles, mokesčių įstatymus, ataskaitų kūrimo reikalavimus ir bendrųjų sumų pajėgumą. Jei naudojamas nepalaikomas dažnumas, skaičiavimams naudojamas iš anksto numatytasis dažnumas **Kiekvienas mokėjimas**.

#### <a name="supported-frequencies"></a>Palaikomi dažnumai

- Visos
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Adresai

Konkrečios šalies ar regiono, valstijos ir apygardos (savivaldybės) kodų identifikacijai reikalingi tam tikri formatai, kuriuos gali atpažinti „Dayforce“ ir šalyje / regione veikiantys teikėjai. Nors miestų formatas yra kintamas, kiekvienas miestas turi būti susietas su valstija.

| Personalas              | „Dayforce“              |
|---------------------|-----------------------|
| Šalis/regionas      | Šalies kodas          |
| Pašto kodas     | Pašto indeksas           |
| Apskritis               | Valstijos kodas            |
| Miestas                | Miestas                  |
| Apygarda              | Apygarda (savivaldybė) |
| Gatvė              | 1 adreso eilutė        |
| Gatvė, namo nr.       | 2 adreso eilutė        |
| Pastatų kompleksas | 5 adreso eilutė        |

### <a name="passport-number"></a>Paso numeris

Darbuotojai gali paskelbti paso informaciją. Ši informacija yra **Paso** identifikacijos tipo pobūdžio ir yra integruota į „Dayforce“ kaip dalis darbuotojo informacijos, susijusios su Meksika.

- Identifikacijos tipas = "Pasas"
- Išdavimo data
- Galiojimo data

Darbuotojai gali paskelbti kelis **Paso** identifikacijos tipo identifikacijos numerius. Tačiau į „Dayforce“ integruojamas tik dabartinis aktyvus paso įrašas. Jei nebegalioja visi paso įrašai, į „Dayforce“ integruojamas pasas, kuris buvo išduotas vėliausiai.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
