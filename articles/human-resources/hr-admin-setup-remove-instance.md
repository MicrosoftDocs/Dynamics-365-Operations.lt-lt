---
title: Egzemplioriaus šalinimas
description: Šiame straipsnyje aprašomas "Microsoft" bandomojo disko arba gamybos aplinkos pašalinimo procesas Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ce676c93e133cc04ad9c49417ed2ca0d6791e93
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178479"
---
# <a name="remove-an-instance"></a>Egzemplioriaus šalinimas

_**Taikoma:** žmogiškieji ištekliai autonominėje infrastruktūrose_ 

> [!NOTE]
> Nuo 2022 m. liepos mėn. naujų personalo aplinkos negali būti sukurtos atskiras personalo infrastruktūrą ir Microsoft Dynamics naujus ciklo tarnybų (LCS) projektus. Klientai gali įdiegti personalo aplinkas finansų ir operacijų infrastruktūrose. Daugiau informacijos ieškokite Finansų [ir operacijų infrastruktūros personalo parengimas](/hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Finansų ir operacijų programos infrastruktūra palaiko aplinkos panaikinimą. Daugiau informacijos apie aplinkos naikinimą rasite aplinkos [naikinimą](../fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure.md#delete-an-environment).

Šiame straipsnyje paaiškinamas "Microsoft" tikrinimo disko arba gamybos aplinkos pašalinimo procesas Dynamics 365 Human Resources.

## <a name="remove-a-test-drive-environment"></a>Bandomosios versijos aplinkos šalinimas

„Human Resources“ bandomosios versijos konfigūruojamos taikant 60 dienų galiojimo laiko strategiją. Tačiau bandomųjų versijų savininkai turi galimybę anksčiau laiko užbaigti bandomosios versijos naudojimo laikotarpį atlikę toliau nurodytus veiksmus. 

1. Pereikite į [„Power Apps“ administravimo centrą](https://admin.businessplatform.microsoft.com/).
2. Pasirinkite **Aplinkos**.
3. Pasirinkite bandomosios versijos aplinką, kurios pavadinimas skamba panašiai į šį: TestDrive – alias@domain
4. Pasirinkite **Naikinti** ir patvirtinkite sprendimą. 

Esama bandomosios versijos aplinka bus pašalinta. Šalinimui pasibaigus galite užsiregistruoti naujoje bandomosios versijos aplinkoje. 

## <a name="remove-a-production-environment"></a>Gamybos aplinkos šalinimas

Šiame straipsnyje laikoma, kad įsigijote „Human Resources“ iš debesies sprendimų teikėjo (CSP) arba pagal įmonės architektūros (EA) sutartį. 

Kadangi vienoje personalo aplinkoje yra viena personalo Power Apps aplinka, šalinant aplinką reikia atsižvelgti į dvi pasirinktis: 
- **Pašalinkite visą Power Apps aplinką.** Ši pasirinktis yra pageidautina Power Apps, kai aplinka buvo sukurta personalo parengimo tikslu, vykdymas tik pradėtas, arba jūs neturite jokių sukurtų integramų.  
- **Pašalinti tik žmogiškuosius išteklius.** Ši pasirinktis tinkama, kai yra nustatyta Power Apps aplinka, automatiškai įvedama naudojant ir Microsoft Power Apps Power Automate.


> [!Important]
> Prieš šalindami Power Apps aplinką, įsitikinkite, kad ji nebus naudojama integruojant duomenis, nepatenkant į personalo sritį. Be to, atminkite, kad numatytųjų „Power Apps“ aplinkų pašalinti negalima. 

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
7. Pasirinkite norimą pašalinti instanciją, kuri turi būti pažymėta talpinimo **Pašalinta** statusu.
8. Pasirinkite **Pašalinti egzempliorių** ir patvirtinkite savo sprendimą. 

## <a name="recover-a-soft-deleted-environment"></a>Švelniai pašalintos aplinkos atkūrimas

Jei panaikinsite Power Apps aplinką, prie kurios prijungta jūsų personalo aplinka, LCS **personalo aplinkos būsena bus iš dalies panaikinta**. Tokiu atveju, naudotojai negalės prisijungti prie žmogiškųjų išteklių.

Aplinkos atkūrimui:

1. Vadovaukitės instrukcijomis [Atkurti „Power Apps“ aplinką](/power-platform/admin/recover-environment).

2. Susisiekite su pagalbos skyriumi dėl žmogiškųjų išteklių aplinkos atkūrimo. Norėdami gauti daugiau informacijos, [Gauti pagalbos](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

> [!Warning]
> „Power Apps“ aplinkos yra saugojamos tik septynias dienas po pašalinimo. Turite atkurti aplinką per septynių dienų laikotarpį.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
