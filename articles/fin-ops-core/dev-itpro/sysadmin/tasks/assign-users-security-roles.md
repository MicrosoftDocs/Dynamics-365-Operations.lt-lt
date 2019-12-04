---
title: Vartotojų priskyrimas saugos vaidmenims
description: Norint pasiekti „Finance and Operations“ programas, vartotojams turi būti priskirti saugos vaidmenys.
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4f4ef4535de9e371829c2d86d4fdc1400510c7b
ms.sourcegitcommit: 6aa74f66f1abd3a7977050a5339b0b17e62ff053
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/15/2019
ms.locfileid: "2808001"
---
# <a name="assign-users-to-security-roles"></a>Vartotojų priskyrimas saugos vaidmenims

[!include [task guide banner](../../includes/task-guide-banner.md)]

Norėdami naudoti bet ką, išskyrus bendrąsias galimybes, vartotojai turi būti priskirti saugos vaidmenims. Šia procedūra paaiškinama, kaip sistemos administratoriai gali automatiškai pagal verslo duomenis priskirti vartotojus vaidmenims. 

## <a name="automatically-assign-users-to-roles"></a>Automatinis vartotojų priskyrimas vaidmenims
1. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims**.
2. Medyje pasirinkite Apskaitos prižiūrėtojas. Pasirinkite vaidmenį, kurio taisyklę norite sukonfigūruoti. Šiame pavyzdyje pasirinkite Apskaitos prižiūrėtojas. 
3. Spustelėkite **Įtraukti taisyklę**, kad atidarytumėte išplečiamąjį dialogo langą.
4. Sąraše **Pasirinkti užklausą** raskite ir pasirinkite norimą įrašą. Pasirinkite su šia taisykle naudotiną užklausą.  
5. Sąraše **Narystės taisyklės pavadinimas** spustelėkite saitą pasirinktoje eilutėje.
6. Spustelėkite **Redaguoti užklausą**. Pagal poreikį užklausą redaguokite.  
7. Spustelėkite **Gerai**.
8. Spustelėkite **Automatiškai priskirti vaidmenį**.
9. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Vartotojai > Vartotojai** (geriausia – atskiroje naršyklės kortelėje).
10. Peržiūrėkite vaidmenis, priskirtus skirtingiems vartotojams, kad patvirtintumėte, jog vaidmenų priskyrimo užklausa yra teisinga. Jei reikia, pakoreguokite ir vykdykite iš naujo.

## <a name="exclude-users-from-automatic-role-assignment"></a>Vartotojų šalinimas iš automatinio vaidmenų priskyrimo
1. Uždarykite puslapį.
2. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims**.
3. Medyje pasirinkite Apskaitos prižiūrėtojas. Pasirinkite vaidmenį. Šiam pavyzdžiui pasirinkite Apskaitos prižiūrėtojas.  
4. Meniu **Vaidmeniui priskirti vartotojai** pasirinkite **Rankiniu būdu priskirti / pašalinti vartotojus**.
5. Sąraše **Priskirti vartotojus vaidmeniui arba iš jo pašalinti** pažymėkite pasirinktą eilutę. Pasirinkite vartotoją.  
6. Dalyje **Veiksmų sritis** pasirinkite **Pašalinti iš vaidmens**.
    
    Spustelėkite **Pašalinti iš vaidmens**, kad pasirinktus vartotojus pašalintumėte iš vaidmens. Norėdami pašalinti pašalinimus, pasirinkite vartotojus, kurių pašalinimus norite pašalinti, ir spustelėkite **Nustatyti būseną iš naujo**. Kai pašalinate pašalinimą grąžindami vartotojo būseną, vartotojo vaidmuo vėl priskiriamas automatiškai. Tačiau, grąžinus būseną, vartotojas ne iš kato priskiriamas vaidmeniui ar iš vaidmens pašalinamas. Vartotojas vaidmeniui priskiriamas arba iš vaidmens pašalinamas kitą kartą vykdant automatinio vaidmenų priskyrimo taisykles.  
