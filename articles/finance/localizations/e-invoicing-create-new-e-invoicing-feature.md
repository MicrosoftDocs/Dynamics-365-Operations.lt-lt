---
title: Kurti SF išrašymo priemonių funkcijas
description: Šioje temoje paaiškinama, kaip sukurti naują elektroninių SF išrašymo priemonę, kai jūsų šalyje arba regione, kuris nėra langelyje, nėra konfigūruotinos funkcijos.
author: gionoder
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffef49c78fd0564db7a2329580ad33a9ccc633c8ac74557e625d1cfb29931576
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744940"
---
# <a name="create-a-new-electronic-invoicing-feature"></a>Kurti SF išrašymo priemonių funkcijas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip sukurti naują elektroninių SF išrašymo priemonę, kai jūsų šalyje arba regione, kuris nėra langelyje, nėra konfigūruotinos funkcijos.

Norėdami sukurti elektroninių SF funkciją, atlikite šias užduotis:

1. Sukurkite naują failo formato konfigūraciją naudodami pateiktą SF modelio konfigūraciją ir išnaudodami esamą norimos sukurti priemonės SF konvertavimą.
2. Įtraukite failo formato konfigūracijas į elektroninių SF funkcijos konfigūracijas.
3. Kurti elekroninių SF funkcijos nustatymus.
4. Užbaikite naują elektroninių SF išrašymo priemonę ir publikuokite ją savo organizacijos visuotinoje saugykloje.
5. Naujos Elektroninių SF išrašymo funkcijos talpinimas į aptarnavimo aplinką.

## <a name="create-new-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Kurti naujas failo formato konfigūracijas, išvestas iš esamo SF modelio

Šioje procedūroje sukursite rinkmenos formato konfigūracijas, reikalingas naujai jūsų sukurtai elektroninių SF išrašymo funkcijai. Galite sukurti elektroninės SF failo formato konfigūraciją ir bet kokias kitas rinkmenos formato konfigūracijas, kurių gali prireikti jūsų naujai elektroninių SF išrašymo funkcijai.

Prieš pradėdami šią procedūrą, prisiregistruokite prie „Regulatory Configuration Service“ (RCS) sąskaitos.

1. „Microsoft Dynamics 365 Finance“, kuri yra **Elektroninių ataskaitų** darbo srityje rinkitės **Saugyklos** skirtas **„Microsoft“** konfigūracijos tiekėjui.
2. Pasirinkite **Visuotinis** ir pasirinkite **Atidaryti** , tada kairiojoje srityje pasirinkite **SF modelio** konfigūraciją.

    > [!IMPORTANT]
    > Brazilijoje pasirinkite **iždo dokumentų** modelio konfigūraciją.

3. Skirtuke **Konfigūracijos** pasirinkite **Importavimas**.
4. Uždarykite puslapį.
5. Uždarykite puslapį.
6. Pasirinkite **Ataskaitų konfigūracijų** išklotinį numerį, tada pasirinkite importuotą SF modelį.
7. Pasirinkite **Kurti konfigūraciją** tada pasirinkite **Formatas pagal SF konteksto modelį**.
8. Įveskite paketo pavadinimą ir formato konfigūracijos aprašymą.
9. Lauke **Formato tipas** pasirinkite failo plėtinio tipą.
10. Rinkitės **Kurti konfigūracijas** ir tada rinkitės savo sukurtą formato konfigūraciją.
11. Pasirinkite **konstruktorių** ir naudodami formato kūrimo įrankį konfigūruokite rinkmenos maketą, kad jis atitiktų rinkmenos formato specifikacijas.
12. Uždarykite puslapį.
13. Elemente **Versijos** rinkitės **Keisti būseną** \> **Užbaigta**.
14. Pasirinkite **Keisti būseną**\> **Bendrai** naudoti, kad būtų publikuojate formato konfigūraciją visuotiniame saugykloje.

Nauja failo formato konfigūracija turi būti bendrai naudojama „Microsoft" domene, kad konfigūraciją galėtų suvartoti elektroninių SF išrašymo tarnyba.

1. Pasirinkite formato konfigūraciją, su kurią dirbate. Konfigūracijos būsena turi būti **Bendrai** naudojama.
2. Skirtuke **Versijos** pasirinkite **Išplėstinis bendrinimas** \> **visuotinė saugykla**.
3. Skirtuke **Bendrinama su** pasirinkite **Organizacija**.
4. Į **lauką** Parametrai įveskite **Microsoft.com** siekiant bendrinti „Microsoft" domeną bendrai naudoja formato konfigūraciją.
5. Pasirinkite **Gerai**.

## <a name="create-the-new-electronic-invoicing-feature"></a>Kurti SF išrašymo priemonių funkcijas

1. RCS pasirinkus dalį **Visuotinės funkcijos**, esančią darbo srityje **Funkcijos**, pasirinkite plytelę **Elektroninių SF priedas**.
2. Pasirinkite **Įtraukti** ir tada pasirinkite **Nauja funkcija**.
3. Įveskite elektroninės SF funkcijos pavadinimą ir aprašą.
4. Pasirinkite **Sukurti funkciją**.

## <a name="add-electronic-invoicing-feature-configurations"></a>Elektroninių SF išrašymo priedo funkcijos konfigūracijų įtraukimas

1. Rinkitės jūsų sukurtą elektroninės sąskaitos funkciją, su kuria dirbate.
2. Skirtuke **Konfigūracijos** pasirinkite **Įtraukti**.
3. Tinklelyje **Konfigūracijos** naršykite ir pasirinkite failo formato konfigūracijas, kurių Jūsų SF funkcijai reikia siekiant sukurti SF failą.
4. Pasirinkite **Gerai**.

## <a name="add-electronic-invoicing-feature-setups"></a>Elektroninių SF išrašymo priedo funkcijos nustatymų įtraukimas

1. Skirtuke **Nustatymai** pasirinkite **Įtraukti** tada pasirinkite **Pasirinktinis nustatymas**.
2. Įveskite funkcijos nustatymų pavadinimą ir aprašymą.
3. Lauke **Nustatymo tipas** pasirinkite **Apdorojimo vamzdyno** galimybės.
4. Pasirinkite **Kurti**.
5. Pasirinkite nustatymą, su kuriuo dirbate ir tada – **Redaguoti**.
6. Pardavimo **galimybių apdorojimo** skirtuke pasirinkite **Naujas** norėdami įtraukti pardavimo galimybių veiksmą. Dėl daugiau informacijos apie vamzdynus, žr. [Veiksmai](e-invoicing-configuration-rcs.md#actions).
7. Skirtuke **Taikymo galimybės** rinkitės **Naujas** norėdami įtraukti taikymo taisyklės sąlygas. Daugiau informacijos apie taikymo taisykles žr. [Taisyklių taikymas](e-invoicing-configuration-rcs.md#applicability-rules).
8. Skirtuke **Kintamieji** pasirinkite **Naujas** jei reikia pridėti kintamųjų.
9. Pasirinkite **Įrašyti**, o tada **pasirinkite** Tikrinti, kad būtų patikrintas konfigūracijos vientisumas.
10. Uždarykite puslapį.

## <a name="deploy-the-electronic-invoicing-feature-to-the-service-environment"></a>Naujos Elektroninių SF išrašymo funkcijos talpinimas į aptarnavimo aplinką

Informacijos, kaip atlikti šią užduotį, ieškokite [Elektroninių SF išrašymo funkcijos diegimas aptarnavimo aplinkoje](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="deploy-the-electronic-invoicing-feature-to-a-connected-application"></a>Elektroninių SF išrašymo funkcijos talpinimas į susietą programą

Informacijos, kaip atlikti šią užduotį, ieškokite Konfigūruoti programos nustatymą ir [Diegti elektroninių SF išrašymo](e-invoicing-get-started.md#configure-the-application-setup) funkciją prie [prijungtos programos](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application).
