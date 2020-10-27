---
title: „Common Data Service“ virtualių objektų konfigūravimas
description: Šioje temoje aprašyta, kaip konfigūruoti „Dynamics 365 Human Resources“ virtualius objektus. Generuokite ir atnaujinkite esamus virtualius objektus, taip pat analizuokite sugeneruotus ir prieinamus objektus.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0848b7556100fba38fcab0aa2a1a109e2e055fc9
ms.sourcegitcommit: b89baab13e530b5b1f079231619c628309a4742d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/05/2020
ms.locfileid: "3959580"
---
# <a name="configure-common-data-service-virtual-entities"></a>„Common Data Service“ virtualių objektų konfigūravimas

[!include [banner](includes/preview-feature.md)]

„Dynamics 365 Human Resources“ yra „Common Data Service“ virtualus duomenų šaltinis. Jis leidžia atlikti visas kūrimo, skaitymo, atnaujinimo ir naikinimo (CRUD) operacijas naudojantis „Common Data Service“ ir „Microsoft Power Platform“. Virtualių objektų duomenys yra saugomi ne „Common Data Service“, bet programos duomenų bazėje. 

Norėdami, kad CRUD operacijas su „Human Resources“ objektais būtų galima atlikti naudojantis „Common Data Service“, turite padaryti, kad objektai „Common Data Service“ būtų prieinami kaip virtualūs objektai. Tai leis jums atlikti CRUD operacijas su „Human Resources“ duomenimis naudojantis „Common Data Service“ ir „Microsoft Power Platform“. Operacijos taip pat palaiko „Human Resources“ visos verslo logikos patvirtinimą, siekiant užtikrinti duomenų vientisumą, kai į objektus rašomi duomenys.

## <a name="available-virtual-entities-for-human-resources"></a>Prieinami „Human Resources“ virtualūs objektai

Visi „Open Data Protocol“ („OData“) objektai, esantys „Human Resources“, yra prieinami kaip virtualūs objektai „Common Data Service“. Jie taip pat yra prieinami „Power Platform“. Dabar galite kurti programas ir patirtis naudodami duomenis tiesiogiai iš „Human Resources“ kartu su visomis CRUD galimybėmis ir nekopijuodami bei nesinchronizuodami duomenų su „Common Data Service“. Norėdami kurti išorines svetaines, kurios leidžia įgyvendinti bendradarbiavimo scenarijus vykdant „Human Resources“ verslo procesus, galite naudoti „Power Apps“ portalus.

Galite peržiūrėti aplinkoje įjungtų virtualių objektų sąrašą ir pradėti dirbti su subjektais [„Power Apps“](https://make.powerapps.com), naudodami sprendimą **Dynamics 365 HR Virtual Entities**.

![„Dynamics 365 HR“ virtualūs objektai, esantys „Power Apps“](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a>Virtualūs objektai ir natūralūs objektai

Virtualūs objektai, skirti „Human Resources“, nėra tokie patys kaip natūralūs „Common Data Service“ objektai, sukurti „Human Resources“. Natūralūs „Human Resources“ objektai generuojami atskirai ir yra tvarkomi „Common Data Service“ „HCM Common“ sprendimo. Dirbant su natūraliais objektais, duomenys saugomi „Common Data Service“ ir turi būti sinchronizuoti su „Human Resources“ programos duomenų baze.

> [!NOTE]
> Natūralių „Common Data Service“ objektų, skirtų „Human Resources“, sąrašą žr. [„Common Data Service“ objektai](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).

## <a name="setup"></a>Sąranka

Atlikite šiuos nustatymo veiksmus, kad įjungtumėte virtualius objektus savo aplinkoje. 

### <a name="register-the-app-in-microsoft-azure"></a>Užregistruokite programą „Microsoft Azure“

Pirmiausia turite užregistruoti programą „Azure“ portale, kad „Microsoft“ tapatumo platforma galėtų teikti autentifikavimo ir autorizavimo paslaugas programai ir vartotojams. Daugiau informacijos apie tai, kaip užregistruoti programas „Azure“, žr. [„Quickstart“: programos registravimas naudojant „Microsoft“ tapatumo platformą](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

1. Atidarykite [„Microsoft Azure“ portalą](https://portal.azure.com).

2. „Azure“ paslaugų sąraše pasirinkite **Programų registracijos**.

3. Pasirinkite **Nauja registracija**.

4. Lauke **Pavadinimas** įveskite apibūdinantį programos pavadinimą. Pavyzdžiui, „**Dynamics 365 Human Resources“ virtualūs objektai**.

5. Lauke **Nukreipimo URI** įveskite „Human Resources“ objekto vardų srities URL.

6. Pasirinkite **Registruotis**.

7. Baigus registraciją, „Azure“ portale rodoma programos registracijos sritis **Apžvalga**, kurioje nurodytas **Programos (kliento) ID**. Pasižymėkite **Programos (kliento) ID**. Šią informaciją turėsite įvesti, kai vykdysite [virtualaus objekto duomenų šaltinio konfigūravimą](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

8. Kairiojoje naršymo srityje pasirinkite **Sertifikatai ir slaptieji raktai**.

9. Puslapio srityje **Kliento slaptieji raktai** pasirinkite **Naujas kliento slaptasis raktas**.

10. Pateikite aprašymą, pasirinkite trukmę ir pasirinkite **Įtraukti**.

11. Pasižymėkite slaptojo rakto vertę. Šią informaciją turėsite įvesti, kai vykdysite [virtualaus objekto duomenų šaltinio konfigūravimą](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).

    > [!IMPORTANT]
    > Šiuo metu būtinai išsisaugokite slaptojo rakto vertę. Palikus šį puslapį, slaptasis raktas daugiau niekada nebus rodomas.

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a>Įdiekite „Dynamics 365 HR Virtual Entity“ programą

Įdiekite „Dynamics 365 HR Virtual Entity“ programą savo „Power Apps“ aplinkoje, kad įdiegtumėte virtualaus objekto sprendimo paketą „Common Data Service“.

1. Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).

2. Sąraše **Aplinkos** pasirinkite „Power Apps“ aplinką, susijusią su „Human Resources“ egzemplioriumi.

3. Puslapio srityje **Ištekliai** pasirinkite **„Dynamics 365“ programos**.

4. Pasirinkite veiksmą **Įdiegti programą**.

5. Pasirinkite **Dynamics 365 HR Virtual Entity**, o tada pasirinkite **Pirmyn**.

6. Peržiūrėkite ir pažymėkite, kad sutinkate su paslaugų teikimo sąlygomis.

7. Pasirinkti **Diegti**.

Diegimas trunka kelias minutes. Baigus, pereikite prie tolesnių veiksmų.

![Įdiekite „Dynamics 365 HR Virtual Entity“ programą iš „Power Platform“ administravimo centro](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a>Sukonfigūruokite virtualaus objekto duomenų šaltinį 

Kitas veiksmas yra sukonfigūruoti virtualaus objekto duomenų šaltinį „Power Apps“ aplinkoje. 

1. Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).

2. Sąraše **Aplinkos** pasirinkite „Power Apps“ aplinką, susijusią su „Human Resources“ egzemplioriumi.

3. Puslapio srityje **Informacija** pasirinkite **Aplinkos URL**.

4. Srityje **Spendimo būklės telkinys** pasirinkite piktogramą **Išplėstinė paieška**, esančią programos viršutiniame dešiniajame kampe.

5. Puslapyje **Išplėstinė paieška**, išskleidžiamajame sąraše **Ieškoti**, pasirinkite „**Finance and Operations“ virtualaus duomenų šaltinio konfigūracijos**.

6. Pasirinkite **Rezultatai**.

7. Pasirinkite įrašą **„Microsoft“ HR duomenų šaltinis**.

8. Įveskite reikiamą duomenų šaltinio konfigūracijos informaciją.

   - **Paskirties URL**: jūsų „Human Resources“ vardų srities URL.
   - **Nuomotojo ID**: „Azure Active Directory“ („Azure AD“) nuomotojo ID.
   - **AAD programos ID**: programos (kliento) ID, sukurtas programai, užregistruotai „Microsoft Azure“ portale. Šią informaciją gavote anksčiau, atlikdami veiksmą [Užregistruokite programą „Microsoft Azure“](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).
   - **AAD programos slaptasis raktas**: kliento slaptasis raktas, sukurtas programai, užregistruotai „Microsoft Azure“ portale. Šią informaciją gavote anksčiau, atlikdami veiksmą [Užregistruokite programą „Microsoft Azure“](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

9. Pasirinkite **Įrašyti ir uždaryti**.

   ![„Microsoft“ HR duomenų šaltinis](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a>Suteikite programos teises „Human Resources“

„Human Resources“ suteikite teises dviem „Azure AD“ programoms:

- Programai, sukurtai jūsų nuomotojui „Microsoft Azure“ portale
- „Dynamics 365 HR Virtual Entity“ programai, įdiegtai „Power Apps“ aplinkoje 

1. „Human Resources“ atidarykite puslapį **„Azure Active Directory“ programos**.

2. Pasirinkite **Nauja**, kad sukurtumėte naują programos įrašą:

    - Lauke **Kliento ID** įveskite programos, kurią užregistravote „Microsoft Azure“ portale, kliento ID.
    - Lauke **Pavadinimas** įveskite programos, kurią užregistravote „Microsoft Azure“ portale, pavadinimą.
    - Lauke **Vartotojo ID** pasirinkite vartotojo, kuriam suteiktos „Human Resources“ ir „Power Apps“ aplinkos administravimo teisės, vartotojo ID.

3. Pasirinkite **Nauja**, kad sukurtumėte antrą programos įrašą:

    - **Kliento ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Pavadinimas**: Dynamics 365 HR Virtual Entity
    - Lauke **Vartotojo ID** pasirinkite vartotojo, kuriam suteiktos „Human Resources“ ir „Power Apps“ aplinkos administravimo teisės, vartotojo ID.

## <a name="generate-virtual-entities"></a>Generuokite virtualius objektus

Baigus nustatymą, galite pasirinkti virtualius objektus, kuriuos norite generuoti ir įjungti savo „Common Data Service“ egzemplioriuje.

1. Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).

2. Sąraše **Aplinkos** pasirinkite „Power Apps“ aplinką, susijusią su „Human Resources“ egzemplioriumi.

3. Puslapio srityje **Informacija** pasirinkite **Aplinkos URL**.

4. Srityje **Spendimo būklės telkinys** pasirinkite piktogramą **Išplėstinė paieška**, esančią puslapio viršutiniame dešiniajame kampe.

5. Puslapyje **Išplėstinė paieška**, išskleidžiamajame sąraše **Ieškoti** pasirinkite **Galimi HR objektai**.

6. Norėdami rasti objektą ar objektus, kuriuos norite įjungti, naudokite filtro pasirinktis.

7. Sąraše pasirinkite objektą.

8. Objekto puslapyje pakeiskite objekto ypatybės **Buvo sugeneruota** reikšmę į **Taip**.

9. Įrašykite ir uždarykite objekto puslapį.

> [!NOTE]
> Naudodami puslapį **Keisti kelis įrašus** galite sugeneruoti kelis virtualius objektus iš karto. Puslapyje pasirinkite kelis įrašus ir juostoje pasirinkite **Redaguoti**. Tada galite pakeisti visų pasirinktų įrašų ypatybę **Buvo sugeneruota**.

![Galimi HR objektai](./media/hr-admin-integration-virtual-entities-available.jpg)

> [!NOTE]
> Tam, kad būtų galima supaprastinti virtualių objektų gamybos procesus būsimose versijose, apdorojimas bus vykdomas „Human Resources“ puslapyje.

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas yra „Common Data Service“?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[Objekto apžvalga](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[Objekto ryšių apžvalga](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[Kurti ir redaguoti virtualius objektus, kuriuose yra duomenų iš išorinio duomenų šaltinio](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Kas yra „Power Apps“ portalai?](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[Programų kūrimo „Power Apps“ apžvalga](https://docs.microsoft.com/powerapps/maker/)
