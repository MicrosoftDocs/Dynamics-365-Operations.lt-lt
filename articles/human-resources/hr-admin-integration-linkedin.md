---
title: Integravimas su „LinkedIn Talent Hub“
description: Šioje temoje paaiškinama, kaip nustatyti „Microsoft Dynamics 365 Human Resources” ir „LinkedIn Talent Hub“ integravimą.
author: jaredha
manager: tfehr
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6f70e3a6ccf9770c75334d355db5e9df9ee912dd
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527890"
---
# <a name="integrate-with-linkedin-talent-hub"></a>Integravimas su „LinkedIn Talent Hub“

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[„LinkedIn Talent Hub”](https://business.linkedin.com/talent-solutions/talent-hub) yra pretendentų sekimo sistemos (ATS) platforma. Ji leidžia vykdyti darbuotojų iešką bei valdyti ir samdyti darbuotojus vienoje vietoje. Integruodami „Microsoft Dynamics 365 Human Resources” su „LinkedIn Talent Hub” galite lengvai sukurti pretendentų, pasamdytų pareigoms, darbuotojų įrašus „Human Resources”.

## <a name="setup"></a>Sąranka

Sistemos administratorius turi užbaigti sąrankos užduotis, kad būtų galima integruoti su „LinkedIn Talent Hub”. Pirmiausia „Power Apps” aplinkoje turite nustatyti vartotoją ir saugos vaidmenį, kad galėtumėte suteikti „LinkedIn Talent Hub” atitinkamas teises duomenims įrašyti į „Human Resources”.

### <a name="link-your-environment-to-linkedin-talent-hub"></a>Jūsų aplinkos susiejimas su „LinkedIn Talent Hub”

1. Atidarykite [„LinkedIn Talent Hub”](https://business.linkedin.com/talent-solutions/talent-hub).

2. Vartotojo išplečiamajame meniu pasirinkite **Produkto parametrai**.

3. Kairiojoje naršymo srityje, dalyje **Išplėstiniai nustatymai**, pasirinkite **Integravimas**.

4. Pasirinkite „Microsoft Dynamics 365 Human Resources” integravimo parinktį **Įgalioti**.

5. Puslapyje **„Dynamics 365 Human Resources”** pasirinkite aplinką, kurią norite susieti su „LinkedIn Talent Hub”, tada pasirinkite **Susieti**.

    ![„LinkedIn Talent Hub” parengimas](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > Galite susieti tik su aplinkomis, kuriose jūsų vartotojo abonementas turi administratoriaus prieigą prie „Human Resources” aplinkos ir susijusios „Power Apps” aplinkos. Jei „Human Resources” susiejimo puslapyje nėra pateiktų aplinkų, įsitikinkite, kad turite licencijuotų „Human Resources” aplinkų nuomotojuje ir kad vartotojui, kuriuo prisijungėte prie susiejimo puslapio, suteiktos „Human Resources” aplinkos ir „Power Apps” aplinkos administratoriaus teisės.

### <a name="create-a-power-apps-security-role"></a>„Power Apps” saugos vaidmens kūrimas

1. Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).

2. Sąraše **Aplinkos** pasirinkite aplinką, susietą su „Human Resources” aplinka, su kuria norite susieti jūsų „LinkedIn Talent Hub” egzempliorių.

3. Pasirinkite **Parametrai**.

4. Išplėskite mazgą **Vartotojai ir teisės** ir pasirinkite **Saugos vaidmenys**.

5. Puslapio **Saugos vaidmenys** įrankių juostoje pasirinkite **Naujas vaidmuo**.

6. Skirtuke **Išsami informacija** įveskite vaidmens pavadinimą, pvz., **„LinkedIn Talent Hub” HRIS integravimas**.

7. Skirtuke **Tinkinimas** pasirinkite organizacijos lygio teisę **Skaitymas** toliau pateiktiems objektams.

    - Objektas
    - Laukas
    - Ryšys

8. Įrašykite ir uždarykite saugos vaidmenį.

### <a name="create-a-power-apps-application-user"></a>„Power Apps” programos vartotojo kūrimas

Reikia sukurti „LinkedIn Talent Hub” adapterio programos vartotoją, kad adapteriui būtų suteiktos teisės įrašyti kandidatų įrašus į „Power Apps” aplinką.

1. Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).

2. Sąraše **Aplinkos** pasirinkite aplinką, susietą su „Human Resources” aplinka, su kuria norite susieti jūsų „LinkedIn Talent Hub” egzempliorių.

3. Pasirinkite **Parametrai**.

4. Išplėskite mazgą **Vartotojai ir teisės** ir pasirinkite **Vartotojai**.

5. Pasirinkite **Valdyti „Dynamics 365” vartotojus**.

6. Naudokite išplečiamąjį meniu, esantį virš sąrašo, norėdami pakeisti rodinį iš numatytojo rodinio **Įgalinti vartotojai** į **Programos vartotojai**.

    ![Rodinys Programos vartotojai](./media/hr-admin-integration-power-apps-application-users.jpg)

7. Įrankių juostoje pasirinkite **Naujas**.

8. Puslapyje **Naujas vartotojas** atlikite toliau pateiktus veiksmus.

    1. Pakeiskite lauko **Vartotojo tipas** reikšmę į **Programos vartotojas**.
    2. Nustatykite lauką **Vartotojo vardas** į **„Dynamics365 HR LinkedIn” HRIS integravimas**.
    3. Nustatykite lauką **Programos ID** į **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    4. Įveskite reikšmes laukuose **Vardas**, **Pavardė** ir **Pagrindinis el. pašto adresas**.
    5. Įrankių juostoje pasirinkite **Įrašyti ir uždaryti** (Save \& Close).

### <a name="assign-a-security-role-to-the-new-user"></a>Saugos vaidmens priskyrimas naujam vartotojui

Įrašę ir uždarę naują programos vartotoją, aprašytą ankstesniame skyriuje, būsite grąžinti į puslapį **Vartotojų sąrašas**.

1. Puslapyje **Vartotojų sąrašas** pakeiskite rodinį į **Programos vartotojai**.

2. Pasirinkite programos vartotoją, kurį sukūrėte ankstesniame skyriuje.

3. Įrankių juostoje pasirinkite **Valdyti vaidmenis**.

4. Pasirinkite integracijos saugos vaidmenį, kurį sukūrėte anksčiau.

5. Pasirinkite **Gerai**.

### <a name="add-an-azure-active-directory-app-in-human-resources"></a>„Azure Active Directory” programos įtraukimas į „Human Resources“

1. „Dynamics 365 Human Resources“ atidarykite puslapį **„Azure Active Directory“ programos**.
2. Įtraukite naują įrašą į sąrašą ir nustatykite toliau pateiktus laukus.

    - **Kliento ID**: įveskite **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    - **Pavadinimas**: įveskite „Power Apps” saugos vaidmens, kurį sukūrėte anksčiau, pavadinimą, pvz., **„LinkedIn Talent Hub” HRIS integravimas**.
    - **Vartotojo ID**: pasirinkite vartotoją, kuris turi teises įrašyti duomenis personalo valdyme.

### <a name="create-the-entity-in-common-data-service"></a>Objekto kūrimas „Common Data Service”

> [!IMPORTANT]
> Integravimas su „LinkedIn Talent Hub” priklauso nuo virtualių objektų, esančių „Common Data Service”, skirtoje „Human Resources”. Būtina šio sąrankos veiksmo sąlyga yra sukonfigūruoti virtualius objektus. Informacijos apie tai, kaip konfigūruoti virtualius objektus, žr. [„Common Data Service” virtualių objektų konfigūravimas](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).

1. „Human Resources“ atidarykite puslapį **„Common Data Service“ (CDS) integravimas**.

2. Pasirinkite skirtuką **Virtualūs objektai**.

3. Filtruokite objektų sąrašą pagal objektų žymas, norėdami rasti **„LinkedIn” eksportuotas kandidatas**.

4. Pasirinkite objektą ir pasirinkite **Generuoti / atnaujinti**.

## <a name="exporting-candidate-records"></a>Kandidatų įrašų eksportavimas

Baigus sąranką, darbdaviai ir „Human resources” (HR) specialistai gali naudoti funkciją **Eksportuoti į HRIS**, esančią „LinkedIn Talent Hub”, norėdami eksportuoti pasamdyto kandidato įrašus iš „LinkedIn Talent Hub” į „Human Resources”.

### <a name="export-records-from-linkedin-talent-hub"></a>Įrašų eksportavimas iš „LinkedIn Talent Hub”

Kai kandidatas pereina įdarbinimo procesą ir yra pasamdomas, galima eksportuoti kandidato įrašą iš „LinkedIn Talent Hub“ į „Human Resources”.

1. „LinkedIn Talent Hub” atidarykite projektą, kuriam pasamdėte naują darbuotoją.

2. Pasirinkite kandidato įrašą.

3. Pasirinkite **Keisti etapą** ir pasirinkite **Pasamdytas**.

4. Kandidato daugtaškio meniu (**...**) pasirinkite **Eksportuoti į HRIS**.

5. Srityje **Eksportuoti į HRIS** įveskite informaciją, kurią reikia eksportuoti.

    - Lauke **HRIS teikėjas** pasirinkite **„Microsoft Dynamics 365 Human Resources”**.
    - Lauke **Pradžios data** pasirinkite naujo darbuotojo reikšmę.
    - Lauke **Pareigos** įveskite naujo darbuotojo pareigas.
    - Lauke **Vieta** įveskite vietą, kurioje darbuotojas dirbs.
    - Įveskite arba patvirtinkite darbuotojo el. pašto adresą.

![Sritis Eksportuoti į HRIS, esanti „LinkedIn Talent Hub”](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a>Parengimo užbaigimas „Human Resources”

Kandidatų įrašai, eksportuoti iš „LinkedIn Talent Hub” į „Human Resources”, atsiranda puslapio **Personalo valdymas** dalyje **Samdytini kandidatai**.

1. „Human Resources“ atidarykite puslapį **Personalo valdymas**.

2. Dalyje **Samdytini kandidatai** pasirinkite pasirinkto kandidato parinktį **Samdyti**.

3. Dialogo lange **Samdyti naują darbuotoją** peržiūrėkite įrašą ir įtraukite reikiamos informacijos. Taip pat galite pasirinkti pareigų numerį, kuriam kandidatas buvo pasamdytas.

Įvedę reikiamą informaciją, galite tęsti jūsų standartinius darbuotojų įrašų kūrimo ir darbuotojų parengimo procesus.

Toliau pateikta informacija importuojama ir įtraukiama į naują darbuotojo įrašą.

- Vardas
- Pavardė
- Įdarbinimo pradžios data
- El. pašto adresas
- Telefono numeris

## <a name="see-also"></a>Taip pat žiūrėkite

[„Common Data Service“ virtualių objektų konfigūravimas](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Kas yra „Common Data Service“?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]