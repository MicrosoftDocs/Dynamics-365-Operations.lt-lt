---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2021 m. gegužės 20 d.)
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2021 m. gegužės 20 d.
author: marcelbf
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dc7e89fabe1651c858097a6c564b4910a524331f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692757"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-20-2021"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2021 m. gegužės 20 d.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomos naujos, pasikeitusios ar netrukus pasirodysiančios „Dynamics 365 Human Resources“ funkcijos.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2021 m. 1-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.4189 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinamos toliau pateiktos funkcijos.

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Platformos atnaujinimas 10.0.18 (42) | -- | [Finansų ir operacijų programėlių 10.0.18 versijos platformos naujinimai (2021 m. gegužės mėn.)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) |
| Personalo programa, skirta „Microsoft Teams”, dabar palaiko pusės dienos apibrėžimus ir dienos skaidymo galimybę | -- | [Atostogų prašymų valdymas „Teams“](/dynamics365/human-resources/hr-teams-leave-app#create-a-new-request) |

### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šią temą, kad būtų įtraukti klaidų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Problemos numeris | Problema |  Aprašas |
| --- | --- | --- |
| 583776 | Dėl masinės darbuotojų registracijos į atostogų planus, įvyko įrašų dublikatų klaida | Ši klaida buvo ištaisyta naujausiame leidime ir masinės atostogų plano registracijos turėtų būti apdorojamos sėkmingai. |
| 582263 | Vienu metu negalima apdoroti gyvenimo įvykio visiems darbuotojams | Kai **Darbuotojo** laukas paliekamas tuščias apdorojant gyvenimo įvykį, bus apdoroti visi darbuotojai. |
| 558383 | Pirminis gavėjas nepažymėtas kaip 100%, jeigu nepasirinktas numatytasis gavėjas | Klaida buvo ištaisyta ir vartotojui reikia pasirinkti tik pirminį gavėjo perjungiklį.|
| 509404 | Padalinio darbuotojų skaičiaus analizė neatsižvelgia į darbuotojų judėjimą tarp padalinių |Analizė buvo atnaujinta, kad būtų įtraukti darbuotojų perkėlimai tarp padalinių|
| 579420 | Stulpelių įšaldymo tinkleliuose funkcija dar neturi būti pasiekiama | Funkcija **Stulpelių įšaldymas tinkleliuose**, kuri nėra dar nėra galima Personalo programoje, buvo pateikta kaip galima Funkcijų valdyme. Funkcija buvo pašalinta iš funkcijų, kurias galima įgalinti, sąrašo. |

## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie funkcijų įjungimą ir išjungimą žr. [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Pasirinktinių laukų palaikymas išmokų valdyme pagal atitinkamas taisykles | [Pasirinktinio lauko palaikymas tinkamumo apdorojimui](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Tinkamumo taisyklių konfigūravimas](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Išmokų valdymo darbo sritis | [Išmokų valdymo darbo sritis (peržiūra)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Išmokų valdymo darbo sritis](hr-benefits-management-workspace.md) |
| Atostogų ir neatvykimų darbo eigos patirties patobulinimai | [Atostogų ir neatvykimų darbo eigos patirties patobulinimai](https://go.microsoft.com/fwlink/?linkid=2147528) | [Prašyti išleisti iš darbo](hr-employee-self-service-request-time-off.md)|
| Įgalinti supaprastintą algalapio integravimą (algalapio integravimo API) | [Įjunkite supaprastintas integraciją su mokėjimo tiekėjais](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Algalapių integravimo API](hr-admin-integration-payroll-api-introduction.md)|
| Atostogų kaupimo operacijos tikrinimas | - | [Atostogų kaupimo operacijos tikrinimas](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>Jau greitai

| Funkcija | Informacija |
| --- | --- |
|  Įgalinti neatvykimų vadovą valdyti atostogas | [Įgalinti neatvykimų vadovą valdyti atostogas](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2021 m. 1-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2021 m. leidimo 1 bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
