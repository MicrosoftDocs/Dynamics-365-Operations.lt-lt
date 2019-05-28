---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent“ (2019 m. kovo 26 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 03/26/2019
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
ms.search.validFrom: 2019-03-26
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 568a16a17ed3269c7b72f27f0d4b7bbdbd56630e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518677"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-26-2019"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent“ (2019 m. kovo 26 d.)

[!include [banner](includes/banner.md)]

Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 for Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

### <a name="enhancements-to-interview-scheduling"></a>Pokalbio planavimo patobulinimai
Toliau nurodyti pokalbio planavimo patobulinimai.

- Įdarbintojai arba samdos vadovai dabar gali neautomatiškai suaktyvinti priminimą kalbintojui pateikti atsiliepimą. Susietą priminimo el. laiško šabloną taip pat galima konfigūruoti.
- Kai pokalbio suvestinė bendrinama su kandidatu, pokalbio planuotojas gali pasirinkti slėpti kalbintojų vardus bei pavardes ir taip pat pasirinkti slėpti tam tikras pokalbio suvestinės rodinio eilutes.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

### <a name="embedded-images-in-activities"></a>Įdėtieji vaizdai veiklose
Dabar galite įterpti vaizdus tiesiai į veiklas. Be to, galite ne tik kopijuoti ir įklijuoti vaizdus iš žiniatinklio, taip pat galite įkelti vaizdus iš vietinės failų sistemos. Veiklos dydis yra apribotas iki 1 MB. Jei vaizdas yra per didelis, keiskite dydį ir bandykite įkelti dar kartą.

[![Susiejimas](./media/embedimages.png)](./media/embedimages.png)

Šiame leidime įtraukti smulkūs klaidų ištaisymai, skirti „Dynamics 365 Talent: Onboard“

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai
**8.1.2210 versija**

### <a name="custom-field-support-available-for-select-entities-in-common-data-service"></a>Pasirinktinių laukų palaikymas teikiamas tam tikruose „Common Data Service“ objektuose 

Dabar toliau nurodyti „Common Data Service“ objektai palaiko pasirinktinius laukus, sukurtus „Dynamics 365 for Talent“.

- Darbininkas
- Etninė kilmė
- Seniai dirbančiojo būsena
- Kalbos kodas
- Pareigos
- Užduoties tipas
- Užduoties funkcija
- Pozicija
- Pareigų tipas
 
### <a name="employment-history-not-displayed-chronologically"></a>Įdarbinimo retrospektyva nerodoma chronologine tvarka
Atlikus šį pakeitimą, dabar įdarbinimo istorijos puslapyje įdarbinimo įrašai rodomi chronologine tvarka, nepriklausomai nuo įmonės. Taip pat galite naudoti rikiavimo parinktis, kad rikiuotumėte pagal įmonę.

### <a name="fixed-compensation-plans-dont-appear-when-restricting-user-by-company-in-security"></a>Pastoviųjų atlyginimo dalių planai nerodomi, kai saugos parametruose apribojamas vartotojas pagal įmonę.
Dabar šiame leidime pastoviųjų atlyginimo dalių planai rodomi, kai saugos parametruose apribojami vartotojai pagal įmonę. Visų saugos parametrų bus laikomasi, o fiksuoti planai bus rodomi tose įmonėse, kurias pasiekti gali vartotojas. 

### <a name="cant-delete-job-records-using-open-in-excel-option-in-talent"></a>Nepavyksta naikinti darbo įrašų naudojant „Talent“ parinktį Atidaryti naudojant „Excel“
Dabar šiame leidime galite pašalinti darbo įrašus naudodami „Dynamics 365 for Talent“ parinktį **Atidaryti naudojant „Excel“**.

### <a name="upgrade-to-common-data-service"></a>Naujovinimas į „Common Data Service“
Terminas, iki kurio galima naujovinti į „Common Data Service“, sparčiai artėja. Prisijunkite prie „PowerApps“ administravimo centro ir sužinokite, ar jūsų duomenų bazę reikia naujovint. Daugiau informacijos apie galutinius terminus ir reikiamus naujovinimo veiksmus žr. [Naujovinimas į „Common Data Service“](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>Peržiūros režimu

Informacijos apie peržiūros funkcijų įjungimą žr. [Prieiga prie „Talent“ peržiūros funkcijų](./access-preview-feature.md).

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Leidimas nedarbo laiko tipuose nurodyti priežasčių kodus
Organizacijoms gali prireikti papildomos informacijos, susijusios su nedarbo laiko užklausomis. Norėdami gauti šią informaciją, darbuotojai turi įtraukti priežasties kodą į savo nedarbo laiko užklausas. Dabar šiame leidime galite nurodyti priežasties kodus, susietus su tam tikru nedarbo laiko tipu, ir leisti darbuotojams pasirinkti priežasties kodą savo nedarbo laiko užklausose.

### <a name="configure-reason-codes-to-be-required-when-submitting-time-off-for-certain-leave-types"></a>Priežasčių kodų konfigūravimas, kad juos būtų privaloma nurodyti teikiant tam tikrų tipų nedarbo laiko užklausas
Organizacijos gali norėti priežasčių kodus priskirti tam tikriems nedarbo laiko tipams, kai darbuotojai teikia nedarbo laiko užklausas. Tai gali būti privaloma laikantis reglamentavimo reikalavimų organizacijos šalyje / regione arba laikantis įmonės strategijos. Šiame leidime suteikiama galimybė personalo skyriui nurodyti, kokių tipų nedarbo laiko užklausas teikiant reikia nurodyti priežasties kodą. Tai bus vykdoma, kai darbuotojai pateikia nedarbo laiko užklausas, jei reikia nurodyti to tipo nedarbo laiko priežasties kodą.

## <a name="coming-soon"></a>Jau greitai

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Išplėstinės kompensacijos sauga (fiksuota ir kintama)
Daugelyje organizacijų kompensacijų ir išmokų vadovai gali turėti prieigą tik prie konkrečių kompensacijų įrašų. Šie įrašai gali būti skirti vadovams arba regionų darbuotojams. Atlikus šį pakeitimą, personalo skyrius gali valdyti ir tvarkyti kompensacijų planus, skirtus skirtingoms darbuotojų grupėms jūsų organizacijoje. Fiksuotam ir kintamam planams galima priskirti saugos vaidmenis – tokiu būdu nustatysite prieigą prie planų ir darbuotojų duomenų, susijusių su planais, pvz., pajamų arba premijų įrašai. Tik asmenys, kuriems priskirti reikiami vaidmenys, galės apdoroti tų darbuotojų kompensaciją.

###  <a name="email-support-for-alerts"></a>Įspėjimų el. pašto palaikymas
25 platformos naujinį įdiegę vartotojai gali kurti įspėjimo taisykles, kurios automatiškai išsiunčia el. pašto pranešimus kontaktams, kai jas suaktyvina įvykis. 

### <a name="duplicate-employee-checks-user-interface-changes"></a>Darbuotojų dublikatų patikros: vartotojo sąsajos pakeitimai
Atlikus šį pakeitimą dublikatai aptinkami, kai įvedate laukų pavadinimus, o būsena rodo, kiek dublikatų rasta. Galite pasirinkti pateiktą nuorodą, kad atidarytumėte naują puslapį ir įvertintumėte, ar naudoti aptiktą dublikatą. Dublikatų forma nėra atidaroma automatiškai, kad nebūtų trukdoma įvesti duomenis.
