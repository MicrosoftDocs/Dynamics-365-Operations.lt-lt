---
title: Kas nauja arba pasikeitė „Dynamics 365 Talent” (2019 m. balandžio 9 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 04/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0a4d4de6cf28e24d1265395d6440df85edf71a0d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897861"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-9-2019"></a>Kas nauja arba pasikeitė „Dynamics 365 Talent” (2019 m. balandžio 9 d.)

Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>„Lifecycle Services“ (LCS) integravimas su pranešimu apie problemą
„Attract“ ir „Onboard“ problemos, kurias registruoja galutiniai vartotojai naudodami pranešimo apie problemą funkciją, dabar automatiškai kuria palaikymo problemas kliento LCS projekte. Tada administratoriai gali suskirstyti problemas ir pateikti jas „Microsoft“, kai reikia. Tai atitinka, kaip „Core HR“ apdoroja galutinių vartotojų palaikymo problemas.

### <a name="relevance-search"></a>Tinkamumo ieška
Dabar talentų telkiniuose galite ieškoti visoje kandidatų duomenų bazėje konkrečių įgūdžių, vardų bei pavardžių arba išsilavinimo informacijos. Jums nebereikia nurodyti, kurioje kandidato profilio skiltyje norite ieškoti. „Attract“ ieško visame profilyje ir paryškina visus atitikmenis. „Attract“ taip pat ieško visuose kandidato dokumentuose ir išmaniai rikiuoja ieškos rezultatus. Be to, galite filtruoti rezultatus pagal šaltinį arba pagal tai, ar kandidatas yra sidabro medalio laimėtojas. Daugiau informacijos žr. [Kandidatų profilių ieška ir peržiūra](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-talent-pools#search-and-view-candidate-profiles).

### <a name="prospect-recommendations"></a>Potencialaus kliento rekomendacijos
Suaktyvinus „Attract“ gali padėti pritraukti darbo šaltinių ir teikti išmanias kandidatų rekomendacijas iš jūsų organizacijos kandidatų duomenų bazės. Rekomendacijos apima įgūdžių ir išsilavinimo informaciją, nustatytą ieškant tinkamų kandidatų. Šios rekomendacijos rodomos darbo skirtuke **Kandidatai**, jei jas suaktyvinsite darbo samdos proceso metu. Daugiau informacijos žr. [Kandidatų rekomendacijos](https://docs.microsoft.com/dynamics365/unified-operations/talent/intelligent-recommendations#prospect-recommendations).

### <a name="interviewer-availability-statuses"></a>Kalbintojo pasiekiamumo būsenos
Pokalbio planuotojai greitai galės peržiūrėti kalbintojų būsenas **Ne biure, dirba kitur**, kad būtų galima suplanuoti laiką, kuris labiau tinka kalbintojams.

### <a name="candidate-interview-experience-save-calendar-invites"></a>Kandidatų pokalbio patirtis: kalendoriaus pakvietimų įrašymas
Dabar kandidatai gali atsisiųsti ir įrašyti savo pokalbių įvykius savo asmeniniuose kalendoriuose naudodami .ics failą, pridėtą prie pokalbio suvestinės el. laiško, išsiųsto kandidatui.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>„Lifecycle Services“ (LCS) integravimas su pranešimu apie problemą
„Attract“ ir „Onboard“ problemos, kurias registruoja galutiniai vartotojai naudodami pranešimo apie problemą funkciją, dabar automatiškai kuria palaikymo problemas kliento LCS projekte. Tada administratoriai gali suskirstyti problemas ir pateikti jas „Microsoft“, kai reikia. Tai atitinka, kaip „Core HR“ apdoroja galutinių vartotojų palaikymo problemas.

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai
Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2225 komponavimo versijai.

### <a name="percent-of-basis-variable-plans-load-incorrect-amount"></a>Pagrindo kintamų planų procentas įkelia netinkamą sumą
Šios savaitės leidime pašalinta problema, kuri kildavo įkeliant kintamosios atlyginimo dalies premijas naudojant pagrindo planų procentą.
 
### <a name="date-picker-on-last-day-worked-doesnt-work-correctly"></a>Datos parinkiklis netinkamai parenka paskutinę darbo dieną
Šis pakeitimas išsprendžia problemą: kai vartotojai redaguoja **įdarbinimo pabaigos datą** ir pasirenka datą naudodami kalendoriaus valdiklį, į pasirinkimą įtraukiama diena.

###  <a name="limit-personnel-action-types-by-the-action-taken"></a>Personalo veiksmų tipų ribojimas pagal atliktą veiksmą
Šis pakeitimas apriboja veiksmų tipus, kurie pasirodo atliekant konkrečius veiksmus. Pvz., kai paskelbiama naujų pareigų darbuotojo paieška, pasirinktinų veiksmų sąraše rodomi tik naujų pareigų veiksmai. Anksčiau buvo rodomi nauji ir redagavimo veiksmai. 

### <a name="transferring-an-employee-with-compensation-in-a-second-legal-entity"></a>Darbuotojo su kompensacija perkėlimas į antrą juridinį subjektą
Šiame leidime kompensaciją galima baigti antrame juridiniame subjekte, jei perkėlimas yra visos įmonės perkėlimas.

### <a name="unable-to-select-compensation-for-a-future-employment-during-a-transfer"></a>Perkėlimo metu negalima pasirinkti būsimo įdarbinimo kompensacijos
Perkeldami darbuotoją į naują juridinį subjektą, dabar perkėlimo proceso metu galite nustatyti naujo juridinio subjekto kompensaciją.

### <a name="user-isnt-able-to-assign-compensation-during-position-assignment"></a>Vartotojas negali priskirti kompensacijos pareigų priskyrimo metu
Įtraukiant naują pareigų priskyrimą dabar galima nustatyti pastoviųjų atlyginimo dalių įrašus. 

## <a name="in-preview"></a>Peržiūros režimu

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Leidimas nedarbo laiko tipuose nurodyti priežasčių kodus
Organizacijoms gali prireikti papildomos informacijos, susijusios su nedarbo laiko užklausomis. Dabar galite nurodyti nedarbo laiko tipų priežasties kodus ir leisti darbuotojams pasirinkti priežasties kodą savo nedarbo laiko užklausose.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Reikalavimas pateikti priežasties kodus, skirtus tam tikriems nedarbo laiko tipams nedarbo laiko užklausose
Organizacijos gali norėti priežasčių kodus priskirti tam tikriems nedarbo laiko tipams, kai darbuotojai teikia nedarbo laiko užklausas. Tokia situacija gali susidaryti dėl įmonės strategijos arba reglamentavimo reikalavimų. Dabar galite nurodyti, kokių tipų nedarbo laiko priežasties kodus reikia pateikti, ir galite reikalauti darbuotojų pateikti nedarbo laiko tipo priežasties kodą savo nedarbo laiko užklausose.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Nedarbo laiko ir neatvykimo operacijų sąrašo pateikimas personalo skyriui
Darbuotojų nedarbo laiko sekimas ir supratimas, kaip skaičiuojamas nedarbo laikas, ne tik padeda personalo skyriui atsakyti į darbuotojų klausimus, bet ir užtikrina tikslias darbuotojų nedarbo laiko premijas. Dabar personalo skyriui suteikta prieiga prie naujo operacijų (subsidijų, kaupimų ir užklausų) rodinio, kad būtų galima sužinoti likučių priežastis. 

## <a name="coming-soon"></a>Jau greitai

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Darbuotojų dublikatų patikros vartotojo sąsajoje patobulinimai
Atlikus šį pakeitimą dublikatai aptinkami, kai įvedate laukų pavadinimus, o būsena rodo, kiek dublikatų rasta. Galite pasirinkti pateiktą nuorodą, kad atidarytumėte naują puslapį ir įvertintumėte, ar naudoti aptiktą dublikatą. Dublikatų forma nėra atidaroma automatiškai, kad nebūtų trukdoma įvesti duomenis.

###  <a name="email-support-for-alerts"></a>Įspėjimų el. pašto palaikymas
Įdiegę „Finance and Operations“ platformos 25 naujinimą, vartotojai gali kurti įspėjimo taisykles, pagal kurias įvykus tam tikram įvykiui kontaktams el. paštu bus automatiškai siunčiami pranešimai. 
