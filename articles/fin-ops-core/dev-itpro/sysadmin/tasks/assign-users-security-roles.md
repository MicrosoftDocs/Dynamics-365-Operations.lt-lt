---
title: Vartotojų priskyrimas saugos vaidmenims
description: Kad vartotojai galėtų pasiekti „Finance and Operations“ programas, jiems reikia priskirti saugos vaidmenis.
author: Peakerbl
manager: AnnBe
ms.date: 05/06/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f78c24e8c2ffe5418ce119e19b7c0193f01f64b8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679869"
---
# <a name="assign-users-to-security-roles"></a>Vartotojų priskyrimas saugos vaidmenims

[!include [banner](../../includes/banner.md)]

Norėdami „Finance and Operations” programose naudoti bet ką, išskyrus bendrąsias galimybes, vartotojai turi būti priskirti saugos vaidmenims. Galite priskirti vartotojus vaidmenims automatiškai, remiantis taisyklėmis ir verslo duomenimis, pašalinti vartotojus iš automatinio vaidmenų priskyrimo arba įtraukti vartotojus į vaidmenis neautomatiniu būdu.

## <a name="automatically-assign-users-to-roles"></a>Automatinis vartotojų priskyrimas vaidmenims
Šia procedūra paaiškinama, kaip sistemos administratoriai gali automatiškai pagal verslo duomenis priskirti vartotojus vaidmenims. 
1. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims**.
2. Medyje pasirinkite Apskaitos prižiūrėtojas. Pasirinkite vaidmenį, kurio taisyklę norite sukonfigūruoti. Šiame pavyzdyje pasirinkite Apskaitos prižiūrėtojas. 
3. Pasirinkite **Įtraukti taisyklę**, kad atidarytumėte dialogo meniu.
4. Sąraše **Pasirinkti užklausą** raskite ir pasirinkite norimą įrašą. Pasirinkite su šia taisykle naudotiną užklausą.  
5. Sąraše **Narystės taisyklės pavadinimas** spustelėkite saitą pasirinktoje eilutėje.
6. Pasirinkite **Redaguoti užklausą**. Pagal poreikį užklausą redaguokite.  
7. Pasirinkite **Gerai**.
8. Pasirinkite **Automatiškai priskirti vaidmenį**.
9. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Vartotojai > Vartotojai** (geriausia – atskiroje naršyklės kortelėje).
10. Peržiūrėkite vaidmenis, priskirtus skirtingiems vartotojams, kad patvirtintumėte, jog vaidmenų priskyrimo užklausa yra teisinga. Jei reikia, pakoreguokite ir vykdykite iš naujo.

## <a name="exclude-users-from-automatic-role-assignment"></a>Vartotojų šalinimas iš automatinio vaidmenų priskyrimo
1. Uždarykite puslapį.
2. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims**.
3. Medyje pasirinkite Apskaitos prižiūrėtojas. Pasirinkite vaidmenį. Šiam pavyzdžiui pasirinkite Apskaitos prižiūrėtojas.  
4. Meniu **Vaidmeniui priskirti vartotojai** pasirinkite **Rankiniu būdu priskirti / pašalinti vartotojus**.
5. Sąraše **Priskirti vartotojus vaidmeniui arba iš jo pašalinti** pažymėkite pasirinktą eilutę. Pasirinkite vartotoją.  
6. Dalyje **Veiksmų sritis** pasirinkite **Pašalinti iš vaidmens**.
7. Pasirinkite **Pašalinti iš vaidmens**, kad pasirinktus vartotojus pašalintumėte iš vaidmens. Norėdami pašalinti pašalinimus, pasirinkite vartotojus, kurių pašalinimus norite pašalinti, ir spustelėkite **Nustatyti būseną iš naujo**. Kai pašalinate pašalinimą grąžindami vartotojo būseną, vartotojo vaidmuo priskiriamas automatiškai. Tačiau, grąžinus būseną, vartotojas ne iš kato priskiriamas vaidmeniui ar iš vaidmens pašalinamas. Vartotojas vaidmeniui priskiriamas arba iš vaidmens pašalinamas kitą kartą vykdant automatinio vaidmenų priskyrimo taisykles.  

## <a name="manually-assign-users-to-roles"></a>Vartotojų priskyrimas vaidmenims neautomatiniu būdu
Vartotojus, kurie neautomatiniu būdu priskirti saugos vaidmenims, administratorius taip pat turi pašalinti neautomatiniu būdu. Šie vartotojai nėra pašalinami iš vaidmenų pagal automatinio vaidmenų priskyrimo taisykles.

1. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims**.
2. Medyje pasirinkite vaidmenį, tada meniu **Vaidmeniui priskirti vartotojai** pasirinkite **Rankiniu būdu priskirti / pašalinti vartotojus**.
4. Dalyje **Priskirti vartotojus vaidmeniui arba iš jo pašalinti** išvardyti vartotojai, kuriems nebuvo priskirtas vaidmuo, ir laukas **Priskyrimo režimas** nustatytas į **Nėra**. Pasirinkite vieną ar daugiau vartotojų, kuriems reikia priskirti vaidmenį.
5. Dalyje **Veiksmų sritis** pasirinkite **Priskirti vaidmeniui**. Laukas **Priskyrimo režimas** atnaujinamas į **Rankinis**, o vartotojams priskirtas naujas vaidmuo.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]