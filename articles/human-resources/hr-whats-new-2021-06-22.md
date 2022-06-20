---
title: Kas nauja ar pasikeitė „Dynamics 365 Human Resources” 2021 m. birželio 22 d
description: Šiame straipsnyje aprašomos priemonės, kurios yra naujos arba pakeistos programoje Microsoft Dynamics 365 Human Resources, 2021 m. birželio 22 d.
author: marcelbf
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aacb605374d99a3c0bad3438c89e33a04a4d7faf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897783"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-22-2021"></a>Kas nauja ar pasikeitė „Dynamics 365 Human Resources” 2021 m. birželio 22 d

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomos priemonės, kurios yra naujos, pakeistos arba tuoj pat Dynamics 365 Human Resources.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2021 m. 1-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.4258 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinamos toliau pateiktos funkcijos.

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Informuokite vartotojų apie darbuotojus be įdarbinimo funkciją – kai įjungta patobulinta, o funkcija **Rodyti visus darbuotojus be įdarbinimo** išjungta funkcijų valdyme, reklaminė juosta bus rodoma darbuotojų be įdarbinimo formoje. Reklaminė juosta nukreips vartotoją įjungti **Rodyti visus darbuotojus be įdarbinimo** funkciją. | Netaikoma| [Neįdarbinti darbininkai](/dynamics365/human-resources/hr-personnel-workers-without-employment)|
| Pasirinktinių laukų palaikymas Išmokų valdymo tinkamumo taisyklėms | [Pasirinktinio lauko palaikymas tinkamumo apdorojimui](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Tinkamumo taisyklių konfigūravimas](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Atostogų kaupimo operacijos tikrinimas | Netaikoma | [Atostogų kaupimo operacijos tikrinimas](hr-leave-and-absence-accrue.md)|
| Atostogų ir neatvykimų darbo eigos patirties patobulinimai | [Atostogų ir neatvykimų darbo eigos patirties patobulinimai](https://go.microsoft.com/fwlink/?linkid=2147528) | [Prašyti išleisti iš darbo](hr-employee-self-service-request-time-off.md)|

### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šį straipsnį, kad būtų įtrauktos pataisos, kurios buvo sukurtas po to, kai buvo publikuotas šis straipsnis.

| Problemos numeris | Problema |  Aprašymas |
| --- | --- | --- |
| 583052 | Vartotojas, gaunantis atsiliepimą, gali redaguoti gautą atsiliepimą | Kai atsiliepimą gaunantis darbuotojas efektyvumo žurnale pasirenka **Įtraukti išorinę nuorodą**, forma tampa redaguotina, taip leisdama darbuotojui redaguoti gautą efektyvumo atsiliepimą. |
| 522281 | Darbuotojų skaičiaus pasirinkimas kompensavimo struktūros plytelėse Kompensacijų valdyme lemia neteisingus rezultatus| Detalizuojant kompensacijų planus iš kompensacijų darbo srities, dabar rodomas teisingas darbuotojų skaičius. |
| 580683 | Vartotojai su priskirtais Darbuotojo ir Vadovo vaidmenimis negali pridėti pastabų arba naujinti Efektyvumo žurnalo | Vartotojai su priskirtais Darbuotojo ir Vadovo vaidmenimis negali pridėti pastabų arba naujinti Efektyvumo žurnalo. Vartotojas gauna klaidą: „Negalima sukurti įrašo Efektyvumo žurnalo įraše (HcmPerfJournal)”. „Saugos strategijos teisė atmesta.” |
| 583077 | Darbuotojo gimimo data įmonės atostogų ir neatvykimų kalendoriuje rodo neteisingą datą | Vartotojai galės peržiūrėti teisingą darbuotojų gimimo datą įmonės atostogų ir neatvykimų kalendoriuje. |
| 586996 | Dėl visos įmonės atostogų rodinio funkcijos balansai yra tušti, kai prieiga yra apribota iki vienos įmonės | Vartotojai gali tinkamai peržiūrėti darbuotojo būsimų atostogų balansus, kai įgalintas visos įmonės atostogų rodinys. |
| 581014 | Įgalinus visos įmonės atostogų ir neatvykimo rodinį, įvyko klaida peržiūrint būsimus balansus | Klaidos buvo ištaisytos, kai vartotojai peržiūri būsimų atostogų balansus su įgalintu visos įmonės atostogų rodiniu. |
| 509404 | Padalinio darbuotojų skaičiaus analizė neatsižvelgia į darbuotojų perkėlimą tarp departamentų. | kai darbuotojas persikelia iš vieno padalinio į kitą, padalinio darbuotojų skaičiaus duomenys neatspindi seno padalinio, iš kurio perkeliamas darbuotojas, jei pareigų informacija baigia galioti tais metais. |
| 584851 | Išmokos kredito proporcingo paskirstymo taisyklė „Jokio” niekada nepateikia kredito |Nukrypimo kredito proporcingo paskirstymo taisyklė „Jokio” lėmė, kad darbuotojai gauna nulinį išmokų laikotarpio kreditą, neatsižvelgiant į tai, kada jie buvo pasamdyti. Tai buvo išspręsta taip, kad darbuotojas gautų visus nukrypimo kreditus, jei buvo pasamdytas prieš prasidedant išmokų laikotarpiui, o jei buvo pasamdytas jau prasidėjus laikotarpiui – jokio kredito. |
| 584897 | Pareigos „Naudoti pagrindines išorines funkcijas” dublikato kūrimo rezultatas yra klaida | Bandant sukurti pareigos „Naudoti pagrindines išorines funkcijas” pareigą, vartotojas gavo klaidą „Nepavyko rasti objekto su identifikatoriumi UserDefinedAppHostDialogView.” |
| 575692 | Atostogų ir neatvykimų kaupimas negalimas laukiantiems darbuotojams | Atostogų ir neatvykimų kaupimą galima vykdyti būsimuose samdiniuose, kai **Supaprastintas darbuotojo įrašas** yra įgalintas. |
| 580110 | Įmonės įtraukimas į algalapio integravimą iš naujo nustato integravimą, kad būtų naudojami visi objektai, net jei nustatyta pasirinktis neatnaujinti projekto | Jei klientas pašalino objektus arba pakeitė duomenų projektą algalapio integravimui ir turi nustatytą parinktį išvengti automatinio projekto atnaujinimo, naujos įmonę įtraukimas prie integravimo nepaiso parametro ir atnaujina projektą.  |
| 584518 |Užregistruoti išmokų apdorojimo efektyvumo problemą | Ši klaida adresavo efektyvumo problemas, susijusias su senstelėjusiu išmokų registracijos procesu. |

## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie funkcijų įjungimą ir išjungimą žr. [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Išmokų valdymo darbo sritis | [Išmokų valdymo darbo sritis (peržiūra)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Išmokų valdymo darbo sritis](hr-benefits-management-workspace.md) |
| Įgalinti supaprastintą algalapio integravimą (algalapio integravimo API) | [Įjunkite supaprastintas integraciją su mokėjimo tiekėjais](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Algalapių integravimo API](hr-admin-integration-payroll-api-introduction.md)|


## <a name="coming-soon"></a>Jau greitai

| Funkcija | Informacija |
| --- | --- |
| Platformos atnaujinimas 10.0.19 (43) | Platformos atnaujinimas 10.0.19 yra suplanuotas pasirodyti su nauju leidimu 2021 m. birželio 28 d. Daugiau informacijos rasite finansų ir [operacijų programėlių 10.0.19 versijos (2021 m. birželio mėn.) platformos naujinimus](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19). |
|  Tarnybos metų rodymo perjungiklis | Ši funkcija suteikia parinktį naudoti skirtingas datas, kad būtų galima apskaičiuoti tarnybos metus, rodomus **Supaprastinto darbuotojo įrašo** ir **Žmonių** formose.  Tai bus galima „Human Resources” parametruose. |
|  Įgalinti neatvykimų vadovą valdyti atostogas | [Įgalinti neatvykimų vadovą valdyti atostogas](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |
|  Įgaliojimo priedai konkretiems atostogų tipams | Ši funkcija leidžia administratoriams įgalioti pridėti priedus pateikiant konkrečių atostogų tipų atostogų užklausas. |
|  Konfigūruoti atostogų vienetus kiekvienam atostogų tipui | Ši funkcija leidžia administratoriams konfigūruoti atostogų vienetus (valandas arba dienas) kiekvienam atostogų tipui.  |
| Įgalinkite darbuotojus būtų pažymėtiems kaip pasiruošusius apmokėjimui | [Įgalinkite darbuotojus būtų pažymėtiems kaip pasiruošusius apmokėjimui](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) |

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2021 m. 1-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2021 m. leidimo 1 bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
