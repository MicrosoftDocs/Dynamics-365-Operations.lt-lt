---
title: Kurkite ER konfigūracijas RCS ir įkelkite jas į bendrąją saugyklą
description: Šioje temoje aiškinama, kaip sukurti elektroninių ataskaitų (ER) konfigūraciją „Microsoft Regulatory Configuration Service“ (RCS) ir nusiųsti ją į bendrąją saugyklą.
author: JaneA07
manager: AnnBe
ms.date: 05/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 0e194a8b777f984412d81e315f92ab4bb8a3b0c9
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371259"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>ER konfigūracijų kūrimas „Regulatory Configuration Service“ (RCS) ir įkėlimas į bendrąją saugyklą

[!include [banner](../includes/banner.md)]

Elektroninių ataskaitų (ER) konfigūracijoms kurti galite naudoti „Microsoft Regulatory Configuration Services“ (RCS), o tada publikuoti, kad jas būtų galima naudoti jūsų organizacijoje

Toliau pateiktos procedūros paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų programuotojo vaidmenį turintis vartotojas gali sukurti išvestinę ER konfigūracijos, sukonfigūruotos RCS egzemplioriuje, versiją, o tada nusiųsti išvestinę konfigūraciją į bendrąją saugyklą. 

Kad galėtumėte atlikti šias procedūras, pirmiausia turite įgyvendinti toliau nurodytas būtinąsias sąlygas.

- Pasiekti RCS egzempliorių.
- Sikurti aktyvų konfigūracijos teikėją. Daugiau informacijos žr. [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Taip pat turite įsitikinti, kad RCS aplinka yra parengta jūsų įmonei.

1. Programoje „Finance and Operations“ eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Jei jūsų įmonei RCS aplinka neparengta, pasirinkite **„Regulatory Services“ – išorinė konfigūracija** ir vykdykite instrukcijas, kad ją parengtumėte.

Jei RCS aplinka jūsų įmonei jau parengta, pasiekite ją naudodami puslapio URL ir pasirinkdami prisijungimo parinktį.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>Išvestinės konfigūracijos versijos kūrimas RCS

1. Darbo srityje **Elektroninės ataskaitos** patvirtinkite, kad turite aktyvų savo organizacijos konfigūracijos teikėją. 
2. Pasirinkite **Ataskaitų konfigūracijos**.
3. Pasirinkite konfigūraciją, iš kurios norite išvesti naują versiją. Ieškai susiaurinti galite naudoti virš medžio esantį filtravimo lauką.
4. Pasirinkite **Kurti konfigūraciją** \> **Kildinti iš pavadinimo**.
5. Įveskite pavadinimą ir aprašą, tada pasirinkite **Kurti konfigūraciją**, kad sukurtumėte naują išvestinę versiją.
6. Pasirinkite naujai išvestą konfigūraciją, įtraukite versijos aprašą, tada pasirinkite **Gerai**. Konfigūracijos būsena pakeičiama į **Baigta**.

![Nauja konfigūracijos versija RCS](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Pakeitus konfigūracijos būseną, galite gauti tikrinimo klaidos pranešimą, susijusį su prijungtomis programomis. Norėdami išjungti tikrinimą, veiksmų srities skirtuke **Konfigūracijos** pasirinkite **Vartotojo parametrai** ir nustatykite parinkties **Praleisti tikrinimą konfigūracijos būsenos keitimo ir pritaikymo kitoje vietoje metu** reikšmę kaip **Taip**. 

## <a name="upload-a-configuration-to-the-global-repository"></a>Konfigūracijos nusiuntimas į bendrąją saugyklą

Norėdami bendrinti naują arba išvestinę konfigūraciją su savo organizacija, galite nusiųsti ją į bendrąją saugyklą.

1. Pasirinkite užbaigtą konfigūracijos versiją, tada pasirinkite **Nusiųsti į saugyklą**.
2. Pasirinkite parinktį **Bendroji („Microsoft“)**, tada – **Nusiųsti**.

    ![Nusiuntimo į saugyklą parinktys](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Patvirtinimo pranešimo lange pasirinkite **Taip**. 
4. Jei reikia, atnaujinkite versijos aprašą ir pasirinkite **Gerai**. 

Konfigūracijos būsena atnaujinama į **Bendrinama**, o konfigūracija nusiunčiama į bendrąją saugyklą. Čia ją galite naudoti toliau nurodytais būdais.

- Importuoti į savo „Dynamics 365“ egzempliorių. Daugiau informacijos žr. [(ER) Konfigūracijų importavimas iš RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Bendrinti su trečiąja šalimi arba su išorine organizacija; žr. [RCS elektroninių ataskaitų (arba) konfigūracijų bendrinimas su išorinėmis organizacijomis](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)

![Išvestinė „Intrastat Contoso“ konfigūracijos versija bendrojoje saugykloje](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Config_upload_GlobalRepo.JPG)
