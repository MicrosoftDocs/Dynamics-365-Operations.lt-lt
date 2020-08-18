---
title: Egzemplioriaus šalinimas
description: Šiame straipsnyje pateikiami veiksmai, skirti „Microsoft Dynamics 365 Human Resources“ bandomosios versijos arba gamybos aplinkai pašalinti.
author: andreabichsel
manager: AnnBe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a384801060b2b684f7908daaac2311edd27c773a
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621385"
---
# <a name="remove-an-instance"></a>Egzemplioriaus šalinimas

Šiame straipsnyje pateikiami veiksmai, skirti „Microsoft Dynamics 365 Human Resources“ bandomosios versijos arba gamybos aplinkai pašalinti.

## <a name="remove-a-test-drive-environment"></a>Bandomosios versijos aplinkos šalinimas

„Human Resources“ bandomosios versijos konfigūruojamos taikant 60 dienų galiojimo laiko strategiją. Tačiau bandomųjų versijų savininkai turi galimybę anksčiau laiko užbaigti bandomosios versijos naudojimo laikotarpį atlikę toliau nurodytus veiksmus. 

1. Pereikite į [„Power Apps“ administravimo centrą](https://admin.businessplatform.microsoft.com/).
2. Pasirinkite **Aplinkos**.
3. Pasirinkite bandomosios versijos aplinką, kurios pavadinimas skamba panašiai į šį: TestDrive – alias@domain
4. Pasirinkite **Naikinti** ir patvirtinkite sprendimą. 

Esama bandomosios versijos aplinka bus pašalinta. Šalinimui pasibaigus galite užsiregistruoti naujoje bandomosios versijos aplinkoje. 

## <a name="remove-a-production-environment"></a>Gamybos aplinkos šalinimas

Šiame straipsnyje laikoma, kad įsigijote „Human Resources“ iš debesies sprendimų teikėjo (CSP) arba pagal įmonės architektūros (EA) sutartį. 

Kadangi viena „Human Resources“ aplinka laikoma atskiroje „Power Apps“ aplinkoje, reikėtų atsižvelgti į dvi galimybes. Pirmosios galimybės atveju pašalinama visa „Power Apps“ aplinka, antrosios – tik „Human Resources“ aplinka. Pirmoji galimybė labiau tinka tuo atveju, kai „Power Apps“ aplinką sukuriate tik „Humas Resources“ konfigūravimo tikslais, o diegimą dar tik esate pradėję arba dar neturite jokių sukurtų integravimų. Antroji galimybė tinka tuo atveju, kai turite sukurtą „Power Apps“ aplinką, užpildytą raiškiaisiais duomenimis, kurie naudojami „Power Apps “ ir „Power Automate“.

> [!Important]
> Prieš pašalindami „Power Apps“ aplinką įsitikinkite, kad ji nenaudojama raiškiųjų duomenų integravimams už „Human Resources“ apimties ribų. Be to, atminkite, kad numatytųjų „Power Apps“ aplinkų pašalinti negalima. 

Jei norite pašalinti visą „Power Apps“ aplinką, įskaitant „Human Resources“ bei susijusių programų ir srautų aplinką, atlikite toliau nurodytus veiksmus.

1. Pereikite į [„Power Apps“ administravimo centrą](https://admin.businessplatform.microsoft.com/).
2. Pasirinkite **Aplinkos**.
3. Pasirinkite šalintiną aplinką.
4. Pasirinkite **Naikinti** ir patvirtinkite sprendimą. 
5. Palaukite, kol naikinimas bus baigtas.
6. Prisijunkite prie [„Lifecycle Services“](https://lcs.dynamics.com/Logon/Index) (LCS) naudodami paskyrą, kurią naudojote užsiprenumeruodami „Human Resources“. 
7. Pasirinkite „Human Resources“ projektą, kuriame yra reikiama aplinka. 
8. LCS projekte pasirinkite plytelę **Programos „Human Resources“ valdymas**. 
9. Pasirinkite šalintiną egzempliorių. 
10. Pasirinkite **Pašalinti egzempliorių** ir patvirtinkite savo sprendimą.  

Norėdami „Human Resources“ aplinką pašalinti iš esamos „Power Apps“ aplinkos, atlikite toliau nurodytus veiksmus. Atkreipkite dėmesį, kad į pagalbos tarnybą ir „Human Resources DevOps“ komandą reikia kreiptis laikinai, kol ši funkcija bus įgalinta tiesiogiai LCS.

1. Kreipkitės į palaikymo tarnybą, kad inicijuotumėte pašalinimo užklausą.
2. Palaikymo tarnybos komanda pašalinimo užklausą inicijuos kartu su „Human Resources DevOps“ komanda. 
3. Gavę pranešimą, kad aplinka pašalinta, tęskite toliau.
4. Prisijunkite prie LCS naudodami paskyrą, kurią naudojote prisijungti prie „Human Resources“. 
5. Pasirinkite „Human Resources“ projektą, kuriame yra reikiama aplinka. 
6. LCS projekte pasirinkite plytelę **Programos „Human Resources“ valdymas**. 
7. Pasirinkite egzempliorių, kurį norite pašalinti ir kuris turi būti pažymėtas diegimo būsena **Nepavyko**.
8. Pasirinkite **Pašalinti egzempliorių** ir patvirtinkite savo sprendimą. 

## <a name="recover-a-soft-deleted-environment"></a>Švelniai pašalintos aplinkos atkūrimas

Jei pašalinate „Power Apps“ aplinką, prie kurios yra prijunta žmogiškųjų išteklių aplinka. žmogiškųjų išteklių aplinkos būsena „Lifecycle Services“ bus **Švelniai pašalinta**. Tokiu atveju, naudotojai negalės prisijungti prie žmogiškųjų išteklių.

Aplinkos atkūrimui:

1. Vadovaukitės instrukcijomis [Atkurti „Power Apps“ aplinką](/power-platform/admin/recover-environment.md).

2. Susisiekite su pagalbos skyriumi dėl žmogiškųjų išteklių aplinkos atkūrimo. Norėdami gauti daugiau informacijos, [Gauti pagalbos](hr-admin-troubleshooting-support.md).

> [!Warning]
> „Power Apps“ aplinkos yra saugojamos tik septynias dienas po pašalinimo. Privalote atkurti aplinką per septynių dienų laikotarpį.
