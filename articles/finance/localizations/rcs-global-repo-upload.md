---
title: Kurkite ER konfigūracijas RCS ir įkelkite jas į bendrąją saugyklą
description: Šioje temoje aiškinama, kaip sukurti elektroninių ataskaitų (ER) konfigūraciją „Microsoft Regulatory Configuration Service“ (RCS) ir nusiųsti ją į bendrąją saugyklą.
author: JaneA07
ms.date: 01/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: eb04362d6d7261af56d2940b085fbc8d43c9d662
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/12/2022
ms.locfileid: "7965094"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>ER konfigūracijų kūrimas „Regulatory Configuration Service“ (RCS) ir įkėlimas į bendrąją saugyklą

[!include [banner](../includes/banner.md)]

Elektroninių ataskaitų (ER) konfigūracijoms kurti galite naudoti „Microsoft Regulatory Configuration Services“ (RCS), o tada publikuoti, kad jas būtų galima naudoti jūsų organizacijoje

Toliau pateiktos procedūros paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų programuotojo vaidmenį turintis vartotojas gali sukurti išvestinę ER konfigūracijos, sukonfigūruotos RCS egzemplioriuje, versiją, o tada nusiųsti išvestinę konfigūraciją į bendrąją saugyklą. 

Kad galėtumėte atlikti šias procedūras, pirmiausia turite įgyvendinti toliau nurodytas būtinąsias sąlygas.

- Turite prieigą prie jūsų organizacijos RCS aplinkos.
- Sukurkite aktyvų konfigūracijos teikėją ir padarykite jį aktyvų. Daugiau informacijos žr. [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Turite užtikrinti, kad jūsų organizacijai būtų galima parengti RCS aplinką. Jei jūsų organizacijai nesusiųstas RCS egzempliorius, tai galite atlikti naudodami šiuos veiksmus:

1. Finansų ir operacijų programoje eikite į organizacijos **administravimo** \> **darbo sričių elektronines** \> **ataskaitas**.
2. Susijusiuose saituose / išoriniuose saituose pasirinkite Reguliavimo tarnybos – Konfigūracija, o tada vykdykite instrukcijas, kad **·** **·** **prisiregistruotumėte** konfigūruoti vieną.

Jei jūsų organizacijai jau buvo sukurta RCS aplinka, norėdami ją pasiekti naudokite puslapio URL ir pasirinkite **prisijungimo** parinktį.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Išvestinės konfigūracijos versijos kūrimas RCS

> [!NOTE]
> Jei tai pirmas kartas, kai naudojote RCS, neturite jokios konfigūracijos, iš kurios jums būtų galima gauti informaciją. Turėsite importuoti konfigūraciją iš visuotinės saugyklos. Daugiau informacijos žr. [ER konfigūracijų atsisiuntimas iš konfigūravimo tarnybos bendrosios saugyklos](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

1. **Prisijunkite prie** RCS ir pasirinkite elektroninių **ataskaitų darbo** sritį.
2. Patikrinkite, ar turite aktyvų konfigūracijos teikėją savo organizacijai, kuri nustatyta kaip aktyvi (žr. būtinuosius komponentus). 
3. Pasirinkite **Ataskaitų konfigūracijos**.
4. Pasirinkite konfigūraciją, iš kurios norite išvesti naują versiją. Ieškai susiaurinti galite naudoti virš medžio esantį filtravimo lauką.
5. Pasirinkite **Kurti konfigūraciją** \> **Kildinti iš pavadinimo**.
6. Įveskite pavadinimą ir aprašymą, tada pasirinkite **Kurti konfigūraciją, kad** sukurtumėte naują išvestinę versiją, kurios būsena Juodraštis.
7. Pasirinkite naujai išvestąją konfigūraciją ir, jei reikia, atlikite papildomus konfigūracijos formato pakeitimus. 
8. Kai jūsų pakeitimai atlikti, turite nustatyti konfigūracijos keitimo būseną **į** **Baigta**, kad būtų galima publikuoti saugykloje. Pasirinkite **Gerai**.

![Nauja konfigūracijos versija RCS.](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Pakeitus konfigūracijos būseną, galite gauti tikrinimo klaidos pranešimą, susijusį su prijungtomis programomis. Norėdami išjungti tikrinimą, veiksmų srities skirtuke **Konfigūracijos** pasirinkite **Vartotojo parametrai** ir nustatykite parinkties **Praleisti tikrinimą konfigūracijos būsenos keitimo ir pritaikymo kitoje vietoje metu** reikšmę kaip **Taip**. 

## <a name="upload-a-configuration-to-the-global-repository"></a>Konfigūracijos nusiuntimas į bendrąją saugyklą

Norėdami su savo organizacija bendrai naudoti naują ar išvestinę konfigūraciją, galite įkelti ją į visuotinę saugyklą, atlikite šiuos veiksmus:

1. Pasirinkite užbaigtą konfigūracijos versiją, tada pasirinkite **Nusiųsti į saugyklą**.
2. Pasirinkite parinktį **Bendroji („Microsoft“)**, tada – **Nusiųsti**.

    ![Nusiuntimo į saugyklą parinktys.](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Patvirtinimo pranešimo lange pasirinkite **Taip**. 
4. Jei reikia, atnaujinkite versijos aprašą ir pasirinkite **Gerai**. Taip pat galite pasirinktinai įkelti versiją į prijungtą programą arba į GIT saugyklą.  

Konfigūracijos būsena atnaujinama į Bendrai **naudojama** ir konfigūracija nusiunčiama į visuotinę saugyklą. Taip pat sukuriama jūsų įkelta konfigūracijos juodraščio versija, kurią galima naudoti, jei reikia atlikti vėlesnius pakeitimus.

Nusiuntę konfigūraciją į visuotinę saugyklą, su ja galite dirbti šiais būdais:

- Importuoti į savo „Dynamics 365“ egzempliorių. Daugiau informacijos žr. [(ER) Konfigūracijų importavimas iš RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Bendrinti su trečiąja šalimi arba su išorine organizacija; žr. [RCS elektroninių ataskaitų (arba) konfigūracijų bendrinimas su išorinėmis organizacijomis](rcs-global-repo-share-configuration.md)

    ![Išvestinė "Intrastat Contoso" konfigūracijos versija visuotinyje saugykloje.](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Konfigūracijos naikinimas iš bendrosios saugyklos
Norėdami panaikinti konfigūraciją, kurią sukūrė jūsų organizacija, atlikite šiuos veiksmus.

1. Darbo srityje **Elektroninės ataskaitos** patvirtinkite, kad jūsų konfigūracijos teikėjo yra **Aktyvus**. Daugiau informacijos žr. [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
2. Prie savo aktyvaus konfigūracijos teikėjo pasirinkite **saugykla**.
3. Pasirinkite **Visuotinį** saugyklos tipą ir tada pasirinkite **Atidaryti**.
4. „FastTab ”skirtuke **Filtras** suraskite konfigūraciją, kurią norite naikinti, naudodami **Filtro** funkciją.
5. „FastTab” **Versija** pasirinkite norimos naikinti konfigūracijos versiją ir pasirinkite **Naikinti**:

    ![Naikinti konfigūraciją iš bendrosios saugyklos.](media/RCS_Delete_from_GlobalRepo.JPG)

6. Patvirtinimo pranešimo lange pasirinkite **Taip**.

    ![Konfigūracijos versijos patvirtinimo pranešimo naikinimas.](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
Konfigūracijos versija panaikinama ir parodomas patvirtinimo pranešimas. 

> [!NOTE]
> Konfigūracijas panaikinti gali tik jas sukūręs konfigūracijos teikėjas. Jei konfigūracija buvo bendrai naudojama su kita organizacija, turėsite atsieti konfigūraciją, prieš ją naikindami.
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
