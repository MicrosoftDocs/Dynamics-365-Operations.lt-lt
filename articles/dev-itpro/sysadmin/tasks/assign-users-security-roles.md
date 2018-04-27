--- 
title: "Vartotojų priskyrimas saugos vaidmenims"
description: "Norint pasiekti „Microsoft Dynamics 365 for Finance and Operations“ vartotojams turi būti priskirti saugos vaidmenys."
author: maertenm
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: da96ec8357ea209fd958e32ab438b13e668735df
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---
# <a name="assign-users-to-security-roles"></a>Vartotojų priskyrimas saugos vaidmenims

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Norint pasiekti „Microsoft Dynamics 365 for Finance and Operations“ vartotojams turi būti priskirti saugos vaidmenys. Šia procedūra paaiškinama, kaip sistemos administratoriai gali automatiškai pagal verslo duomenis priskirti vartotojus. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


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


