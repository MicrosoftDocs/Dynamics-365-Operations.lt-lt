---
title: Vartotojų priskyrimas saugos vaidmenims
description: Kad būtų galima pasiekti finansų ir operacijų programėles, vartotojai turi būti priskirti saugos vaidmenims.
author: Peakerbl
ms.date: 02/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5e69a79f123daff3f85d0100647615ad818288e
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103875"
---
# <a name="manage-users-and-security-roles"></a>Vartotojų ir saugos vaidmenų valdymas

[!include [banner](../../includes/banner.md)]

Jei norite naudoti ne bendrąsias finansų ir operacijų programėlių galimybes, vartotojai turi būti priskirti saugos vaidmenims. Galite priskirti vartotojus vaidmenims automatiškai, remiantis taisyklėmis ir verslo duomenimis, pašalinti vartotojus iš automatinio vaidmenų priskyrimo arba įtraukti vartotojus į vaidmenis neautomatiniu būdu.

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
Šia procedūra paaiškinama, kaip pašalinti vartotojus iš automatinio vaidmenų priskyrimo.

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

## <a name="manually-remove-users-from-roles"></a>Rankiniu būdu pašalinti vartotojus iš vaidmenų
Vartotojus, kurie neautomatiniu būdu priskirti saugos vaidmenims, administratorius taip pat turi pašalinti neautomatiniu būdu. Šie vartotojai nėra pašalinami iš vaidmenų pagal automatinio vaidmenų priskyrimo taisykles.

1. Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims**.
2. Norėdami pašalinti vieną vartotoją, atlikite šiuos veiksmus:
   1. Medyje pasirinkite vaidmenį. 
   2. Srityje Vartotojai **, priskirti vaidmeniui**, pasirinkite vartotoją, kurį reikia pašalinti.
   3. Pasirinkite **Pašalinti** ir vartotojas pašalintas iš vaidmens.
3. Norėdami pašalinti kelis vartotojus, atlikite šiuos veiksmus:
   1. Medyje pasirinkite vaidmenį. 
   2. Srityje Vartotojai **, priskirti vaidmeniui, pasirinkite** Rankiniu būdu **priskirti / pašalinti vartotojus**.
   3. Priskirti vartotojus **vaidmenų puslapyje arba iš jo** pašalinti vartotojai, kurie nebuvo priskirti vaidmeniui, **·** **priskyrimo režimo stulpelyje** yra Nėra. Pasirinkite vartotojus, kurių vaidmens reikia neįtraukti.
   4. Dalyje **Veiksmų sritis** pasirinkite **Pašalinti iš vaidmens**. Dabar **priskyrimo** režimo stulpelis atnaujintas **į Rankinis**, o vartotojai dabar neįtraukti į vaidmenį.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

