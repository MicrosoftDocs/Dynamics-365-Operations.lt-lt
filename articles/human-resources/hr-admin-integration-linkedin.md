---
title: Integravimas su „LinkedIn Talent Hub“
description: Šiame straipsnyje paaiškinama, kaip nustatyti integravimą tarp Microsoft ir Dynamics 365 Human Resources LinkedIn Talent Hub.
author: jaredha
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df4a0a4dec078392ba835318450f5983a6e95c97
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887754"
---
# <a name="integrate-with-linkedin-talent-hub"></a>Integravimas su „LinkedIn Talent Hub“

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

> [!IMPORTANT]
> Šiame straipsnyje aprašytas Dynamics 365 Human Resources integravimas tarp LinkedIn talentų centro ir jo buvo 2021 m. gruodžio 31 d. Po šios datos integravimo tarnyba nebebus galima. Organizacijos, kurios dar nenaudoja integravimo tarnybos, negalės įdiegti paslaugos prieš išeidami į pensiją.

[„LinkedIn Talent Hub”](https://business.linkedin.com/talent-solutions/talent-hub) yra pretendentų sekimo sistemos (ATS) platforma. Ji leidžia vykdyti darbuotojų iešką bei valdyti ir samdyti darbuotojus vienoje vietoje. Integruodami „Microsoft Dynamics 365 Human Resources” su „LinkedIn Talent Hub” galite lengvai sukurti pretendentų, pasamdytų pareigoms, darbuotojų įrašus „Human Resources”.

## <a name="setup"></a>Sąranka

Sistemos administratorius turi užbaigti sąrankos užduotis, kad būtų galima integruoti su „LinkedIn Talent Hub”. Pirmiausia „Power Apps” aplinkoje turite nustatyti vartotoją ir saugos vaidmenį, kad galėtumėte suteikti „LinkedIn Talent Hub” atitinkamas teises duomenims įrašyti į „Human Resources”.

### <a name="link-your-environment-to-linkedin-talent-hub"></a>Jūsų aplinkos susiejimas su „LinkedIn Talent Hub”

1. Atidarykite [„LinkedIn Talent Hub”](https://business.linkedin.com/talent-solutions/talent-hub).

2. Vartotojo išplečiamajame meniu pasirinkite **Produkto parametrai**.

3. Kairiojoje naršymo srityje, dalyje **Išplėstiniai nustatymai**, pasirinkite **Integravimas**.

4. Pasirinkite „Microsoft Dynamics 365 Human Resources” integravimo parinktį **Įgalioti**.

5. Puslapyje **„Dynamics 365 Human Resources”** pasirinkite aplinką, kurią norite susieti su „LinkedIn Talent Hub”, tada pasirinkite **Susieti**.

    ![„LinkedIn Talent Hub” parengimas.](./media/hr-admin-integration-talent-hub-onboarding.jpg)

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

    ![Rodinys Programos vartotojai.](./media/hr-admin-integration-power-apps-application-users.jpg)

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

### <a name="create-the-table-in-dataverse"></a>Kurti lenteles „Dataverse“

> [!IMPORTANT]
> Integravimas su „LinkedIn Talent Hub“ priklauso nuo virtalių lentelių  Dataverse“ „Human Resources“. Kaip išankstines sąlygas šiam veiksmui nustatymuose, turite konfigūruoti virtualias lenteles. Dėl informacijos apie tai, kaip konfigūruoti virtualias lenteles, žr. [Konfigūruoti „Dataverse“ virtualias lenteles](./hr-admin-integration-common-data-service-virtual-entities.md).

1. „Human Resources“, atverkite **„Dataverse“ integravimo** puslapį.

2. Rinkitės **Virtualių lentelių** skirtuką.

3. Filtruokite objektų sąrašą pagal objektų žymas, norėdami rasti **„LinkedIn” eksportuotas kandidatas**.

4. Pasirinkite objektą ir pasirinkite **Generuoti / atnaujinti**.

## <a name="exporting-candidate-records"></a>Kandidatų įrašų eksportavimas

Užbaigus nustatymus, įdarbintojai ir žmogiškųjų išteklių (HR) darbuotojai gali naudoti **Eksportuoti į HRIS** funkciją „LinkedIn Talent Hub“ siekiant eksportuoti pasamdyto kandidato įrašus iš „LinkedIn Talent Hub“ į „Human Resources“.

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

![Sritis Eksportuoti į HRIS, esanti „LinkedIn Talent Hub”.](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

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

[Konfigūruokite „Dataverse“ virtualias lenteles](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Kas yra „Microsoft Dataverse“?](/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
