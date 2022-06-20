---
title: Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. birželio mėn. 11 d.)
description: Šiame straipsnyje aprašomos priemonės, kurios yra naujos arba pakeistos programoje Microsoft Dynamics 365 Human Resources dėl 2020 m. birželio 11 d.
author: andreabichsel
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 78d0adbfea19ce9d77b74cd44dbf19366ae37ff7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852952"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a>Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. birželio mėn. 11 d.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources“ funkcijos. Pakeitimai taikomi 8.1.3316 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo LCS palaikymo numerius informaciniais tikslais.

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a>Kartais dėl supaprastintos darbuotojo formos neveikia antrinės formos uždarymo (X) mygtukai (442369)

Kai nauja **Darbuotojas** forma įjungiama, uždarymo mygtukas ( **X**) retkarčiais neveikia antrinėse formose. Ši problema pasikartodavo. Galėjote uždaryti formą grįžus ir išėjus. Pavyzdžiui, galite pasirinkti meniu elementą kairėje ir grįžti į **Darbuotojas** formą, o tada ją uždaryti. Šios savaitės pataisa išsprendė šią problemą. 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a>Darbuotojo asmeninio kontaktinio asmens objektas neeksportuoja asmeninių kontaktų esant pirminiam ryšio tipui

Šame leidime **Darbuotojo asmeninio kontaktinio asmuo** objektas eksportuoja visus ryšių tipus.

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a>HcmPozicijosDarbuotojoPriskyrimasV2Objektas turėtų būti įtrauktas į „Ceridian” algalapio integravimo paketą pagal numatytuosius nustatymus (448506)

Su šiuo pakeitimu **HcmPozicijaDarbuotojoPriskyrimasV2Objektas** yra įtrauktas į „Ceridian” algalapio integravimo paketą.

## <a name="in-preview"></a>Peržiūros režimu

## <a name="database-logging"></a>Duomenų bazės registravimas

Duomenų bazės registravimo funkcija leidžia nustatyti, kurios lentelės ir laukai turi būti stebimi. Taip pat galite nustatyti įvykius, kurie turi aktyvinti keitimų sekimą. Naudojate duomenų bazės registravimo galimybes, kad laikui bėgant pamatytumėte šiuos pakeitimus. Daugiau informacijos ieškokite [Duomenų bazės registravimo konfigūravimas ir tvarkymas](hr-admin-database-logging.md).

## <a name="human-resources-application-in-teams"></a>„Human Resources“ programa programoje „Teams“

Darbuotojai gali peržiūrėti ir prašyti atostogų programoje „Microsoft Teams“. Jie gali bendrauti su robotu, kad sukurtų atostogų prašymą. Daugiau informacijos žr. [„Human Resources“ programa programoje „Teams“](./hr-admin-teams-leave-app.md). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Duomenų valdymo sistemos (DMF) objektai, skirti išmokų valdymui
 
Išmokų valdymo objektai ir išleidimas. DMF objektai leidžia paprastai importuoti ir eksportuoti duomenis, kad lengviau konfigūruotumėte išmokų valdymą. Išmokų valdymo šablonas taps prieinamu duomenų perkėlimui. Šablonas nuosekliai eksportuoja ir importuoja duomenis išsaugodamas duomenų priklausomumą.

## <a name="buy-and-sell-leave"></a>Atostogų pirkimas ir pardavimas 

Kai kurios organizacijos suteikia išmoką, kuri leidžia darbuotojams pirkti ar parduoti savo atostogas. Šis procesas dažnai valdomas neautomatiniu būdu. Ši funkcija automatizuoja žmogiškųjų išteklių departamento valdymo strategijas ir užklausas. Ji supaprastina atostogų valdymo procesą ir padeda pašalinti klaidas. Daugiau informacijos ieškokite:

- [Atostogų pirkimo ir pardavimo strategijų valdymas](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Atostogų pirkimas ir pardavimas](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Atostogų kaupimas vienai įmonei arba vienam planui

Klientai gali apdoroti vienoje įmonėje sukauptas atostogas, vienkartines atostogas ir neatvykimų planą. Šis gebėjimas suteikia klientams su skirtingais išėjimo į pensiją metais ar atostogomis aiškumo apie kaupimo strategijas. Norėdami sužinoti daugiau, skaitykite [Sukauptos atostogos įmonėje ar atostogų planas](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Priedų pridėjimas prašymams atidėti

Galimybė pridėti priedus prie patvirtintų atostogų prašymų yra itin svarbi dabartinėje COVID-19 situacijoje. Dabar darbuotojai gali pridėti šiuos priedus. Jie taip pat turi daugiau įžvalgų apie atostogų prašymų naujinimų kūrimą. Norėdami sužinoti daugiau, skaitykite [Priedo prie esamo prašymo pridėjimas](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Priežasties kodo pridėjimas į kaupimo sustabdymus 

Į kaupimo sustabdymus įtraukti priežasties kodai.

## <a name="carry-forward-rules"></a>Perkėlimo taisyklės 

Galite nurodyti perkėlimo atostogų tipą, skirtą perkėlimo balansams ir į kurį perkeliami perkeliamų balansų koregavimai. Pavyzdžiui, jei darbuotojas perkelia 10 dienų, toms 10 dienų galite pasirinkti kitą atostogų tipą. Daugiau informacijos žr. [Atostogų ir neatvykimų tipų konfigūravimas](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Atostogų kaupimo sustabdymas konkretiems atostogų tipams

Galite sukurti taisyklę sustabdyti darbuotojų, įvedusių neapmokamų atostogų prašymus, atostogų kaupimą. Neapmokamos atostogos gali būti tipas, tačiau tai neprivaloma. Galite sustabdyti bet kokias atostogas, pagrįstas kitu atostogų tipu.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF objektas pasiekiamas kaupimo sustabdymams 

DMF objektas dabar pasiekiamas kaupimo sustabdymams.

## <a name="coming-soon"></a>Jau greitai

## <a name="new-platform-capabilities"></a>Naujos platformos galimybės 

Jūs galėsite padaryti laukus privalomus naudojant personalizavimą. Norėdami įjungti šią funkciją, įjunkite **Įrašyti rodiniai**.

## <a name="configure-the-name-of-employee-self-service"></a>Darbuotojų savitarnos pavadinimo konfigūravimas

Nauja parinktis bus prieinama „Human Resources” parametruose, kad galėtumėte atnaujinti Darbuotojo savitarnos darbovietės pavadinimą į Savitarną. 

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]