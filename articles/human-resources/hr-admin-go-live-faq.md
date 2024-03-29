---
title: DUK apie įgyvendinimo pradžią
description: Šiame straipsnyje pateikiami dažnai užduodami klausimai apie tai, kaip vykti į diegimo Dynamics 365 Human Resources projektą.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dfb2434b0d0573f2edab228fcca77ee653d751a5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853109"
---
# <a name="go-live-faq"></a>DUK apie įgyvendinimo pradžią 


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Šiame straipsnyje pateikiami dažnai užduodami klausimai apie tai, kaip vykti į diegimo Dynamics 365 Human Resources projektą. 

## <a name="when-can-i-configure-and-request-my-production-environment"></a>Kada galiu konfigūruoti ir pateikti užklausą dėl mano gamybos aplinkos? 

Paprastai gamybos aplinka įdiegiama, jei ji atitinka toliau pateiktus kriterijus.

- Visi tinkinimai yra užkoduoti ir baigti.
- Vartotojo priėmimo testavimas (UAT) baigtas.
- Klientas atsijungė nuo sprendimo.
- Nėra įgyvendinimo blokavimo problemų. 

Kai kvalifikuoti klientai yra šiame etape, „Microsoft FastTrack” komanda bendradarbiauja su projekto komanda, kad atliktų įgyvendinimo įvertinimą. 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a>Kokios būtinosios gamybos aplinkos diegimo sąlygos? 

Norėdami gauti būtinųjų sąlygų sąrašą, žr.  [Rengimasis įgyvendinimo pradžiai](hr-admin-go-live-prepare.md). 

## <a name="what-is-a-go-live-assessment"></a>Kas yra įgyvendinimo įvertinimas?  

Įgyvendinimo įvertinimas yra  [„Microsoft FastTrack” programos](/dynamics365/fasttrack/) dalis. Šios peržiūros metu sprendimų architektas įvertina, ar įgyvendinimo projektas parengtas sėkmingam pritaikymui ir įgyvendinimui. Ši peržiūra yra privaloma kiekvienam įgyvendinimo projektui, kad galima būtų pateikti įgyvendinimo gamybos aplinkoje užklausą. 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a>Mūsų smėlio dėžės aplinkos diegiamos centrinės JAV duomenų centre. Norime, kad mūsų gamybos aplinkos būtų diegiamos Vakarų JAV duomenų centre. Ar mano gamybos konfigūracijoje galiu pasirinkti Vakarų JAV kaip duomenų centrą? 

LCS nedraudžia pasirinkti kito duomenų centro, kai diegiate „Human Resources” aplinką, tačiau primygtinai rekomenduojame nesirinkti kito duomenų centro.  

Jei norite, kad jūsų gamybos aplinka būtų Vakarų JAV duomenų centre, pirmiausia turite iš naujo įdiegti jūsų smėlio dėžės aplinkas į Vakarų JAV duomenų centrą, patikrinti jas ir išsiregistruoti. 

Informacijos apie teisingo duomenų centro pasirinkimą žr. [Tinklo reikalavimai](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements). 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a>Kokio lygio prieigą prie „Azure“ išteklių turiu mano „Human Resources” aplinkose?  

Prieiga prie „Human Resources” aplinkų yra ribota. Neturite prieigos prie virtualiosios mašinos (VM) arba „Microsoft“ informacinių interneto paslaugų (IIS). Taip pat neturite prieigos prie duomenų bazės per „Microsoft SQL Server” valdymo studiją. 

Nors negalite tiesiogiai pasiekti „Azure” išteklių ar „Dynamics 365 Human Resources” aplinkos, yra papildomų funkcijų, kurias galite naudoti norėdami pasiekti jūsų duomenis.

- „Azure SQL” duomenų bazę galite įdiegti savo „Azure” nuomotojuje ir naudoti savo duomenų bazės naudojimo (BYOD) funkciją duomenims sinchronizuoti. Daugiau informacijos žr. [Savo duomenų bazės naudojimas (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).

- Galite naudoti „Dataverse” integravimą, norėdami sinchronizuoti pasirinktus objektus su „Dataverse” duomenų baze. Dėl daugiau informacijos, žr. [„Dataverse“ lentelės](hr-developer-entities.md). 

## <a name="how-often-is-my-production-database-backed-up"></a>Kaip dažnai sukuriamos mano gamybos duomenų bazės atsarginės kopijos? 

Duomenų bazių atsarginės kopijos kuriamos automatiškai toliau pateiktu dažnumu.

| Atsarginės kopijos tipas | Dažnumas |
| --- | --- |
| Visos duomenų bazės atsarginė kopija | Savaitinis |
| Diferencinės duomenų bazės atsarginė kopija | Kas 12-24 val. |
| Operacijų žurnalo atsarginė kopija | Kas 5-10 min. |

„Microsoft“ saugo pakankamai atsarginių kopijų taško laike atkūrimui (PITR) per paskutiniąsias 14 dienų. 

Daugiau informacijos žr.  [Sužinokite apie automatiškai sukurtas SQL duomenų bazės atsargines kopijas](/azure/azure-sql/database/automated-backups-overview?tabs=single-database). 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>Ar galiu pateikti užklausą dėl mano gamybos duomenų bazės atsarginės kopijos? 

Nr. Tačiau galite pateikti duomenų bazės atnaujinimo paslaugos užklausą, kad nukopijuotumėte jūsų gamybos aplinką į jūsų smėlio dėžės aplinką. „Azure SQL” duomenų bazę galite įdiegti savo „Azure” nuomotojuje ir naudoti BYOD funkciją duomenims iš jūsų gamybos aplinkos sinchronizuoti. Daugiau informacijos žr. [Savo duomenų bazės naudojimas (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md). 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a>Kaip galiu perkelti mano smėlio dėžės aplinką į gamybos aplinką, norėdamas atlikti įgyvendinimą? 

Kadangi kopijavimo funkcija nepasiekiama perkeliant jūsų aplinką iš smėlio dėžės į gamybos aplinką, turite naudoti duomenų paketus, kad perkeltumėte duomenis į jūsų gamybos aplinką.  

Viso projekto metu rekomenduojame išlaikyti aiškų objektų, sukonfigūruotų jūsų smėlio dėžėje, sąrašą. Tada patikrinkite visų duomenų paketų, kurių reikia įgyvendinimui, pritaikymą ir perkėlimą. Kai esate pasiruošę įgyvendinimui, turite rankiniu būdu perkelti visus duomenų paketus į gamybos aplinką. 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>Ką daryti, jei mano gamybos aplinka neveikia? 

Norėdami pranešti apie gamybos sutrikimus, vykdykite procesą, aprašytą  [Pranešimas apie gamybos sutrikimus](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md). 

 ## <a name="see-also"></a>Taip pat žiūrėkite

 [Rengimasis įgyvendinimo pradžiai](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
