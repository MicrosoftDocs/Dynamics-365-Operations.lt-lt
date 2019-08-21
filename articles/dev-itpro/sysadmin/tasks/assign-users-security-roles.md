---
title: Vartotojų priskyrimas saugos vaidmenims
description: Kad vartotojai galėtų pasiekti Microsoft Dynamics 365 for Finance and Operations redakciją įmonėms, jiems reikia priskirti saugos vaidmenis.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c0afd0f5754e59307a82af9c9700b36c31edcc4
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851364"
---
# <a name="assign-users-to-security-roles"></a>Vartotojų priskyrimas saugos vaidmenims

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kad vartotojai galėtų pasiekti Microsoft Dynamics 365 for Finance and Operations redakciją įmonėms, jiems reikia priskirti saugos vaidmenis. Šia procedūra paaiškinama, kaip sistemos administratoriai gali automatiškai pagal verslo duomenis priskirti vartotojus. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="automatically-assign-users-to-roles"></a>Automatinis vartotojų priskyrimas vaidmenims
1. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims**.
2. Medyje pasirinkite Apskaitos prižiūrėtojas. Pasirinkite vaidmenį, kurio taisyklę norite sukonfigūruoti. Šiame pavyzdyje pasirinkite Apskaitos prižiūrėtojas. 
3. Spustelėkite **Įtraukti taisyklę**, kad atidarytumėte išplečiamąjį dialogo langą.
4. Sąraše **Pasirinkti užklausą** raskite ir pasirinkite norimą įrašą. Pasirinkite su šia taisykle naudotiną užklausą.  
5. Sąraše **Narystės taisyklės pavadinimas** spustelėkite saitą pasirinktoje eilutėje.
6. Spustelėkite **Redaguoti užklausą**. Pagal poreikį užklausą redaguokite.  
7. Spustelėkite **Gerai**.

## <a name="exclude-users-from-automatic-role-assignment"></a>Vartotojų šalinimas iš automatinio vaidmenų priskyrimo
1. Uždarykite puslapį.
2. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims**.
3. Medyje pasirinkite Apskaitos prižiūrėtojas. Pasirinkite vaidmenį. Šiam pavyzdžiui pasirinkite Apskaitos prižiūrėtojas.  
4. Meniu **Vaidmeniui priskirti vartotojai** pasirinkite **Rankiniu būdu priskirti / pašalinti vartotojus**.
5. Sąraše **Priskirti vartotojus vaidmeniui arba iš jo pašalinti** pažymėkite pasirinktą eilutę. Pasirinkite vartotoją.  
6. Dalyje **Veiksmų sritis** pasirinkite **Pašalinti iš vaidmens**.
    
    Spustelėkite **Pašalinti iš vaidmens**, kad pasirinktus vartotojus pašalintumėte iš vaidmens. Norėdami pašalinti pašalinimus, pasirinkite vartotojus, kurių pašalinimus norite pašalinti, ir spustelėkite **Nustatyti būseną iš naujo**. Kai pašalinate pašalinimą grąžindami vartotojo būseną, vartotojo vaidmuo vėl priskiriamas automatiškai. Tačiau, grąžinus būseną, vartotojas ne iš kato priskiriamas vaidmeniui ar iš vaidmens pašalinamas. Vartotojas vaidmeniui priskiriamas arba iš vaidmens pašalinamas kitą kartą vykdant automatinio vaidmenų priskyrimo taisykles.  
