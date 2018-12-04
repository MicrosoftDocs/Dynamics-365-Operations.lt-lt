--- 
title: "Vartotojų priskyrimas saugos vaidmenims"
description: "Norėdami pasiekti „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimą, vartotojams turi būti priskirti saugos vaidmenys."
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 551048af26f46d334c562d1968963aed262a5e03
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="assign-users-to-security-roles"></a>Vartotojų priskyrimas saugos vaidmenims

[!include [task guide banner](../../includes/task-guide-banner.md)]

Norėdami pasiekti „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimą, vartotojams turi būti priskirti saugos vaidmenys. Šia procedūra paaiškinama, kaip sistemos administratoriai gali automatiškai pagal verslo duomenis priskirti vartotojus. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="automatically-assign-users-to-roles"></a>Automatinis vartotojų priskyrimas vaidmenims
1. Eikite į Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims.
2. Medyje pasirinkite Apskaitos prižiūrėtojas.
    * Pasirinkite vaidmenį, kurio taisyklę norite sukonfigūruoti. Šiame pavyzdyje pasirinkite Apskaitos prižiūrėtojas.  
3. Spustelėkite Įtraukti taisyklę, kad atidarytumėte išplečiamąjį dialogo langą.
4. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite su šia taisykle naudotiną užklausą.  
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Spustelėkite Redaguoti užklausą.
    * Pagal poreikį užklausą redaguokite.  
7. Spustelėkite GERAI.

## <a name="exclude-users-from-automatic-role-assignment"></a>Vartotojų šalinimas iš automatinio vaidmenų priskyrimo
1. Uždarykite puslapį.
2. Eikite į Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims.
3. Medyje pasirinkite Apskaitos prižiūrėtojas.
    * Pasirinkite vaidmenį. Šiam pavyzdžiui pasirinkite Apskaitos prižiūrėtojas.  
4. Spustelėkite Rankiniu būdu priskirti / pašalinti vartotojus.
5. Sąraše pažymėkite pasirinktą eilutę.
    * Pasirinkite vartotoją.  
6. Spustelėkite Pašalinti iš vaidmens.
    * Spustelėkite Pašalinti iš vaidmens, kad pasirinktus vartotojus pašalintumėte iš vaidmens. Norėdami pašalinti pašalinimus, pasirinkite vartotojus, kurių pašalinimus norite pašalinti ir spustelėkite Grąžinti būseną. Kai pašalinate pašalinimą grąžindami vartotojo būseną, vartotojo vaidmuo vėl priskiriamas automatiškai. Tačiau, grąžinus būseną, vartotojas ne iš kato priskiriamas vaidmeniui ar iš vaidmens pašalinamas. Vartotojas vaidmeniui priskiriamas arba iš vaidmens pašalinamas kitą kartą vykdant automatinio vaidmenų priskyrimo taisykles.  


