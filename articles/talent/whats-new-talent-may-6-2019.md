---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. gegužės 6 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f06d989ea4e927111729dfbd4bb7700745a16a54
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897516"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-6-2019"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. gegužės 6 d.)

Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

### <a name="select-optional-documents-upon-offer-creation"></a>Sukūrę pasiūlymą pasirinkite pasirinktinius dokumentus

Kai pasirenkate pasiūlymo paketo šabloną, Pritraukti dabar paragins jus pasirinkti taikytinus, pasirinktinius dokumentus iš to paketo šablono. Rengdami pasiūlymą galite pridėti kitų pasirinktinių dokumentų.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Onboard“.

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2282 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo palaikymo numerius „Microsoft Dynamics Lifecycle Services“ (LCS).

### <a name="platform-update-26-for-finance-and-operations"></a>„Finance and Operations“ platformos 26 naujinimas

Papildomos informacijos apie „Finance and Operations“ platformos 26 naujinimą žr. [Peržiūros funkcijos programos „Dynamics 365 Finance and Operations“ platformos 26 naujinime (2019 m. gegužės mėn.)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26). 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service objekto palaikymas pasirinktiniams laukams

Šios savaitės leidime nuo šiol palaikomi šių objektų pasirinktiniai laukai: Išmokos apskaičiavimo dažnis, Išmokos apskaičiavimo koeficientas, Išmokos tipas, Darbo kalendorius, Darbo kalendorius atostogos, Mokėjimo ciklas ir Darbo identifikacijos tipai.

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a>Palikite masinę registraciją, pakeičiant pakopos pagrindą į „Paaukštinimo data“ neatnaujinamas pradinis kaupimo koeficientas (318526)

Kai masiškai registruojate darbuotojus ir pakeičiate jų pakopų pagrindus, pradinis kaupimas atspindi jiems parinktus pakopų pagrindus.

### <a name="workflow-showing-duplicate-place-holders-313636"></a>Darbo eiga, kurioje rodomi pasikartojantys vietos rezervavimo ženklai (313636)

Šio leidimo pakeitimai pašalina vietos rezervavimo ženklų dubliavimą, kai siunčiami darbo eigos pranešimai.

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a>Dimensijų laukai nėra atnaujinami naudojant „Atidaryti naudojant „Excel“ (176261)

Šiame leidime nuo šiol galite naujinti finansinę dimensiją naudodami **Atidaryti naudojant „Excel“** puslapyje **Darbuotojas**. 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a>Darbuotojo adresas, sukurtas „Common Data Service“ nėra sinchronizuojamas su „Talent“ (317555)

Įdiegus šį pakeitimą, adresai, sukurti „Common Data Service“, atnaujinami „Talent: Core HR“.


## <a name="in-preview"></a>Peržiūros režimu

### <a name="new-page-to-validate-position-hierarchy-data"></a>Naujas puslapis, skirtas tikrinti pareigų hierarchijos duomenis

Žmogiškųjų išteklių (HR) skyrius ir administratoriai dabar gali tikrinti visa valdybos hierarchiją, ar joje nėra netyčia importuotų uždarų rekomendacijų. Galite pasiekti naują puslapį dalyje **Organizacijos administravimas > Saitai > Pareigos > Pareigų hierarchijos tikrinimas**.

### <a name="specify-reason-codes-on-leave-types"></a>Nurodykite atostogų tipų priežasties kodus

Organizacijoms gali prireikti papildomos informacijos, susijusios su nedarbo laiko užklausomis. Dabar galite nurodyti nedarbo laiko tipų priežasties kodus ir leisti darbuotojams pasirinkti priežasties kodą savo nedarbo laiko užklausose.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Reikalavimas pateikti priežasties kodus, skirtus tam tikriems nedarbo laiko tipams nedarbo laiko užklausose

Organizacijos gali norėti priežasčių kodus priskirti tam tikriems nedarbo laiko tipams, kai darbuotojai teikia nedarbingumo užklausas. Šis reikalavimas gali būti dėl įmonės strategijos arba reguliavimo reikalavimų. Dabar galite nurodyti, kokių tipų nedarbo laiko priežasties kodus reikia pateikti, ir galite reikalauti darbuotojų pateikti nedarbo laiko tipo priežasties kodą savo nedarbo laiko užklausose.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Nedarbo laiko ir neatvykimo operacijų sąrašo pateikimas personalo skyriui

Galimybė sekti darbuotojų nedarbo laiką ir suprasti, kaip skaičiuojamas nedarbo laikas, ne tik padeda personalo skyriui atsakyti į darbuotojų klausimus, bet ir padeda užtikrinti tikslias darbuotojų nedarbo laiko premijas. Dabar HR suteikta prieiga prie naujo operacijų (subsidijų, kaupimų ir užklausų) rodinio, kad HR darbuotojai galėtų sužinoti likučių priežastis.

## <a name="coming-soon"></a>Jau greitai

### <a name="indicate-instance-type-when-provisioning-talent"></a>Nurodykite egzemplioriaus tipą rengdami „Talent“

Kuriant naują „Talent“ egzempliorių bus galima nurodyti, ar egzemplioriaus tipas yra **Gamyba** ar **Smėlio dėžė**, kad galėtumėte iš anksto patikrinti naujas funkcijas. Visi esami „Talent“ egzemplioriai bus atnaujinti į gamybos egzemplioriaus tipą. Jei norite, kad vienas iš esamų egzempliorių būtų atnaujintas į smėlio dėžės egzemplioriaus tipą, kreipkitės į palaikymo tarnybą, kad ši inicijuotų keitimo užklausą.
