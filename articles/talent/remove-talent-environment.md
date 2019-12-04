---
title: „Talent“ aplinkų šalinimas
description: Šioje temoje pateikiami veiksmai, skirti „Microsoft Dynamics 365 Talent“ bandomosios versijos arba gamybos aplinkai pašalinti.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: bbc65a77b7c3df6545dfd7aa2109aba5c4e1b57b
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773040"
---
# <a name="remove-talent-environments"></a>„Talent“ aplinkų šalinimas

[!include [banner](includes/banner.md)]

Šioje temoje pateikiami veiksmai, skirti „Microsoft Dynamics 365 Talent“ bandomosios versijos arba gamybos aplinkai pašalinti.

## <a name="removing-a-test-drive-environment"></a>Bandomosios versijos aplinkos šalinimas

„Talent“ bandomosios versijos konfigūruojamos taikant 60 dienų galiojimo laiko strategiją. Tačiau bandomųjų versijų savininkai turi galimybę anksčiau laiko užbaigti bandomosios versijos naudojimo laikotarpį atlikę toliau nurodytus veiksmus. 

1. Pereikite į [„Power Apps“ administravimo centrą](https://admin.businessplatform.microsoft.com/).
2. Pasirinkite **Aplinkos**.
3. Pasirinkite bandomosios versijos aplinką, kurios pavadinimas skamba panašiai į šį: TestDrive – alias@domain
4. Pasirinkite **Naikinti** ir patvirtinkite sprendimą. 

Esama bandomosios versijos aplinka bus pašalinta. Šalinimui pasibaigus galite užsiregistruoti naujoje bandomosios versijos aplinkoje. 

## <a name="removing-a-production-environment"></a>Gamybos aplinkos šalinimas

Šioje temoje laikoma, kad įsigijote „Talent“ iš debesies sprendimų teikėjo (CSP) arba pagal įmonės architektūros (EA) sutartį. 

Kadangi viena „Talent“ aplinka laikoma atskiroje „Power Apps“ aplinkoje, reikėtų atsižvelgti į dvi galimybes. Pirmosios galimybės atveju pašalinama visa „Power Apps“ aplinka, antrosios – tik „Talent“ aplinka. Pirmoji galimybė labiau tinka tuo atveju, kai „Power Apps“ aplinką sukuriate tik „Talent“ konfigūravimo tikslais, o diegimą dar tik esate pradėję arba dar neturite jokių sukurtų integravimų. Antroji galimybė tinka tuo atveju, kai turite sukurtą „Power Apps“ aplinką, užpildytą raiškiaisiais duomenimis, kurie naudojami „Power Apps “ ir „Power Automate“.

> [!Important]
> Prieš pašalindami „Power Apps“ aplinką įsitikinkite, kad ji nenaudojama raiškiųjų duomenų integravimams už „Talent“ apimties ribų. Be to, atminkite, kad numatytųjų „Power Apps“ aplinkų pašalinti negalima. 

Jei norite pašalinti visą „Power Apps“ aplinką, įskaitant „Talent“ bei susijusių programų ir srautų aplinką, atlikite toliau nurodytus veiksmus.

1. Pereikite į [„Power Apps“ administravimo centrą](https://admin.businessplatform.microsoft.com/).
2. Pasirinkite **Aplinkos**.
3. Pasirinkite šalintiną aplinką.
4. Pasirinkite **Naikinti** ir patvirtinkite sprendimą. 
5. Palaukite, kol naikinimas bus baigtas.
6. Prisijunkite prie [„Lifecycle Services“](https://lcs.dynamics.com/Logon/Index) (LCS) naudodami abonementą, kurį naudojote užsiprenumeruodami „Talent“. 
7. Pasirinkite „Talent“ projektą, kuriame yra reikiama aplinka. 
8. LCS projekte pasirinkite plytelę **Programos „Talent“ valdymas**. 
9. Pasirinkite šalintiną egzempliorių. 
10. Pasirinkite **Pašalinti egzempliorių** ir patvirtinkite savo sprendimą.  

Norėdami „Talent“ aplinką pašalinti iš esamos „Power Apps“ aplinkos, atlikite toliau nurodytus veiksmus. Atkreipkite dėmesį, kad į pagalbos tarnybą ir „Talent DevOps“ komandą reikia kreiptis laikinai, kol ši funkcija bus įgalinta tiesiogiai LCS.

1. Kreipkitės į palaikymo tarnybą, kad inicijuotumėte pašalinimo užklausą.
2. Palaikymo tarnybos komanda pašalinimo užklausą inicijuos kartu su „Talent DevOps“ komanda. 
3. Gavę pranešimą, kad aplinka pašalinta, tęskite toliau.
4.  Prisijunkite prie LCS naudodami abonementą, kurį naudojote užsiprenumeruodami „Talent“. 
5. Pasirinkite „Talent“ projektą, kuriame yra reikiama aplinka. 
6. LCS projekte pasirinkite plytelę **Programos „Talent“ valdymas**. 
7. Pasirinkite egzempliorių, kurį norite pašalinti ir kuris turi būti pažymėtas diegimo būsena **Nepavyko**.
8. Pasirinkite **Pašalinti egzempliorių** ir patvirtinkite savo sprendimą. 

