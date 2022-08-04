---
title: „Dataverse“ virtualiųjų lentelių konfigūravimas
description: Šiame straipsnyje parodyta, kaip konfigūruoti, generuoti, atnaujinti esamas virtualias lenteles ir analizuoti sugeneruotas ir galimas lenteles, skirtas Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 45155dba5063981eb3aeeed4dda1d79a57b7c8af
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067105"
---
# <a name="configure-dataverse-virtual-tables"></a>„Dataverse“ virtualiųjų lentelių konfigūravimas


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



„Dynamics 365 Human Resources“ yra „Microsoft Dataverse“ virtualus duomenų šaltinis. Jis leidžia atlikti visas kūrimo, skaitymo, atnaujinimo ir naikinimo (CRUD) operacijas naudojantis „Dataverse“ ir „Microsoft Power Platform“. Duomenys virtualioms lentelėms nėra laikomi „Dataverse“, bet programos duomenų bazėje.

CRUD operacijas įjungti „Human Resources“ objektuose iš „Dataverse“, turite padaryti objektus prieinamus kaip virtualias lenteles „Dataverse“. Tai leis jums atlikti CRUD operacijas su „Human Resources“ duomenimis naudojantis „Dataverse“ ir „Microsoft Power Platform“. Operacijos taip pat palaiko „Human Resources“ visos verslo logikos patvirtinimą, siekiant užtikrinti duomenų vientisumą, kai į objektus rašomi duomenys.

> [!NOTE]
> „Human Resources“ objektai atitinka „Dataverse“ lenteles. Dėl daugiau informacijos apie „Dataverse“ (anksčiau vadintą „Common Data Service“) ir terminologijos naujinimus, žr. [Kas yra „Microsoft Dataverse“?](/powerapps/maker/data-platform/data-platform-intro)

## <a name="available-virtual-tables-for-human-resources"></a>Prieinamos virtualios lentelės „Human Resources“

Visi atvirų duomenų protokolo (ODat) objektai „Human Resources“ yra prieinami kaip virtualios lentelės „Dataverse“. Jie taip pat yra prieinami „Power Platform“. Dabar galite kurti programas ir patirtis naudodami duomenis tiesiogiai iš „Human Resources“ kartu su visomis CRUD galimybėmis ir nekopijuodami bei nesinchronizuodami duomenų su „Dataverse“. Norėdami kurti išorines svetaines, kurios leidžia įgyvendinti bendradarbiavimo scenarijus vykdant „Human Resources“ verslo procesus, galite naudoti „Power Apps“ portalus.

Galite peržiūrėti virtualių lentelių aplinkoje sąrašą ir pradėti darbą su lentelėmis [„Power Apps“](https://make.powerapps.com), **„Dynamics 365 HR Virtual Tables“** sprendime.

![„Dynamics 365 HR Virtual Tables“ „Power Apps“.](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a>Virtualios lentelės prieš įgimtas lenteles

Virtualios lentelės „Human Resources“ nėra tokios pačios kaip įgimtos „Dataverse“ lentelės sukurtos „Human Resources“. 

Įgimtos lentelės „Human Resources“ yra sukuriamos atskirai ir laikomos HCM bendrame sprendime „Dataverse“. Su įgimtomis lentelėmis, duomenys yra laikomi „Dataverse“ ir juos reikia sinchronizuoti su „Human Resources“ programos duomenų baze.

> [!NOTE]
> Dėl įgimtų lentelių sąrašo „Dataverse“ „Human Resources“, žr. [„Dataverse“ lenteles](./hr-developer-entities.md).

## <a name="setup"></a>Sąranka

Atlikite šiuos žingsnius, kad įjungtumėte virtualias lenteles jūsų aplinkoje.

### <a name="enable-virtual-tables-in-human-resources"></a>Įjungti virtualias lenteles „Human Resources“

Pirmiausia, turite įjungti virtualias lenteles **Funkcijų valdymo** darbo srityje.

1. Programoje „Human Resources“ pasirinkite **Sistemos administravimas**.

2. Pasirinkite plytelę **Funkcijų valdymas**.

3. Rinkitės **Virtualios lentelės palaikymą HR „Dataverse“** ir tada rinkitės **Įjungti**.

Dėl daugiau informacijos apie funkcijų įjungimą ir išjungimą, žr. [Valdyti funkcijas](hr-admin-manage-features.md).

### <a name="register-the-app-in-microsoft-azure"></a>Užregistruokite programą „Microsoft Azure“

Turite registruoti savo žmogiškųjų išteklių elementą „Azure“ portale tam, kad „Microsoft“ tapatybės platforma galėtų pateikti autentifikavimą ir autentifikavimo paslaugas programai ir vartotojams. Daugiau informacijos apie tai, kaip užregistruoti programas „Azure“, žr. [„Quickstart“: programos registravimas naudojant „Microsoft“ tapatumo platformą](/azure/active-directory/develop/quickstart-register-app).

1. Atidarykite [„Microsoft Azure“ portalą](https://portal.azure.com).

2. „Azure“ paslaugų sąraše pasirinkite **Programų registracijos**.

3. Pasirinkite **Nauja registracija**.

4. Lauke **Pavadinimas** įveskite apibūdinantį programos pavadinimą. Pavyzdžiui, **„Dynamics 365 Human Resources“ virtualios lentelės**.

5. Lauke **Nukreipimo URI** įveskite „Human Resources“ objekto vardų srities URL.

6. Pasirinkite **Registruotis**.

7. Baigus registraciją, „Azure“ portale rodoma programos registracijos sritis **Apžvalga**, kurioje nurodytas **Programos (kliento) ID**. Pasižymėkite **Programos (kliento) ID**. Jūs įvesite šią informaciją, kai [Konfigūruosite virtualios lentelės duomenų šaltinį](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

8. Kairiojoje naršymo srityje pasirinkite **Sertifikatai ir slaptieji raktai**.

9. Puslapio srityje **Kliento slaptieji raktai** pasirinkite **Naujas kliento slaptasis raktas**.

10. Pateikite aprašymą, pasirinkite trukmę ir pasirinkite **Įtraukti**.

11. Įrašykite slaptąją reikšmę iš lentelės ypatybės **Reikšmė**. Jūs įvesite šią informaciją, kai [Konfigūruosite virtualios lentelės duomenų šaltinį](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).

    > [!IMPORTANT]
    > Šiuo metu būtinai išsisaugokite slaptojo rakto vertę. Palikus šį puslapį, slaptasis raktas daugiau niekada nebus rodomas.

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a>Įdiekite „Dynamics 365 HR Virtual Tables“ programą

Įdiekite „Dynamics 365 HR Virtual Table“ programą savo „Power Apps“ aplinkoje, kad talpintumėte virtualios lentelės sprendimo paketą į „Dataverse“.

1. „Human Resources“, atverkite **„Microsoft Dataverse“ integravimo** puslapį.

2. Rinkitės **Virtualių lentelių** skirtuką.

3. Pasirinkite **Įdiegti virtualiosios lentelės** programą.

### <a name="configure-the-virtual-table-data-source"></a>Konfigūruokite virtualios lentelės duomenų šaltinį

Kitas žingsnis yra konfigūruoti virtualios lentelės duomenų šaltinį „Power Apps“ aplinkoje.

1. Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com).

2. Sąraše **Aplinkos** pasirinkite „Power Apps“ aplinką, susijusią su „Human Resources“ egzemplioriumi.

3. Puslapio srityje **Informacija** pasirinkite **Aplinkos URL**.

4. Srityje **Spendimo būklės telkinys** pasirinkite piktogramą **Išplėstinė paieška**, esančią programos viršutiniame dešiniajame kampe.

5. Išplėstinės **ieškos** puslapio išplečiamajame **sąraše Ieškoti** pasirinkite Finansų ir **operacijų virtualiųjų duomenų šaltinio konfigūracijos**.

   > [!NOTE]
   > Virtualiosios lentelės programos diegimas iš ankstesnio nustatymo veiksmo gali užtrukti keletą minučių. Jei **finansų ir operacijų virtualiųjų duomenų** šaltinio konfigūracijos sąraše nėra, šiek tiek palaukite ir atnaujinkite sąrašą.

6. Pasirinkite **Rezultatai**.

7. Pasirinkite įrašą **„Microsoft“ HR duomenų šaltinis**.

8. Įveskite būtiną informaciją duomenų šaltinių konfigūravimui:

   - **Paskirties URL**: jūsų „Human Resources“ vardų srities URL. Tikslo URL formatas yra:
     
     https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/

     Pvz.:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >Įsitikinkite, kad įtrauksite "**/**" simbolį URL gale siekiant išvengti klaidos gavimo.

     >[!NOTE]
     >Paskirties URL nurodo „Human Resources“ aplinką, kurią virtualiosios lentelės nurodys kaip duomenų šaltinį. Jei kurdami gamybos aplinkos kopiją sukuriate smėlio dėžės aplinką, atnaujinkite šią vertę į naujos smėlio dėžės aplinkos vardų srities URL. Taip užtikrinsite, kad virtualiosios lentelės bus sujungtos su smėlio dėžės aplinkos duomenimis, o ne toliau nurodys gamybos aplinką.

   - **Nuomotojo ID**: „Azure Active Directory“ („Azure AD“) nuomotojo ID.

   - **AAD programos ID**: programos (kliento) ID, sukurtas programai, užregistruotai „Microsoft Azure“ portale. Šią informaciją gavote anksčiau, atlikdami veiksmą [Užregistruokite programą „Microsoft Azure“](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   - **AAD programos slaptasis raktas**: kliento slaptasis raktas, sukurtas programai, užregistruotai „Microsoft Azure“ portale. Šią informaciją gavote anksčiau, atlikdami veiksmą [Užregistruokite programą „Microsoft Azure“](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).

   ![„Microsoft“ HR duomenų šaltinis.](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. Pasirinkite **Įrašyti ir uždaryti**.

### <a name="grant-app-permissions-in-human-resources"></a>Suteikite programos teises „Human Resources“

„Human Resources“ suteikite teises dviem „Azure AD“ programoms:

- Programai, sukurtai jūsų nuomotojui „Microsoft Azure“ portale
- „Dynamics 365 HR Virtual Table“ programa įdiegta iš „Power Apps“ aplinkos 

1. „Human Resources“ atidarykite puslapį **„Azure Active Directory“ programos**.

2. Pasirinkite **Nauja**, kad sukurtumėte naują programos įrašą:

    - Lauke **Kliento ID** įveskite programos, kurią užregistravote „Microsoft Azure“ portale, kliento ID.
    - Lauke **Pavadinimas** įveskite programos, kurią užregistravote „Microsoft Azure“ portale, pavadinimą.
    - Lauke **Vartotojo ID** pasirinkite vartotojo, kuriam suteiktos „Human Resources“ ir „Power Apps“ aplinkos administravimo teisės, vartotojo ID.

3. Pasirinkite **Nauja**, kad sukurtumėte antrą programos įrašą:

    - **Kliento ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Pavadinimas**: „Dynamics 365 HR Virtual Table“
    - Lauke **Vartotojo ID** pasirinkite vartotojo, kuriam suteiktos „Human Resources“ ir „Power Apps“ aplinkos administravimo teisės, vartotojo ID.

## <a name="generate-virtual-tables"></a>Kurti virtualias lenteles

Kai nustatymas užbaigtas, galite rinktis virtualias lenteles, kurias norite kurti ir įjungti savo „Dataverse“ objekte.

1. „Human Resources“, atverkite **„Microsoft Dataverse“ integravimo** puslapį.

2. Rinkitės **Virtualių lentelių** skirtuką.

> [!NOTE]
> **Įjungti virtualias lenteles** jungiklis bus nustatytas į **Taip** automatiškai, kai visi būtini veiksmai bus užbaigti. Jei perjungiklis nustatytas į **Ne**, peržiūrėkite ankstesniuose šio dokumento skyriuose aprašytus veiksmus, norėdami užtikrinti, kad visi būtinieji nustatymo veiksmai yra baigti.

3. Rinkitės lentelę ar lenteles, kurias norite kurti „Dataverse“.

4. Pasirinkite **Generuoti / atnaujinti**.

![„Dataverse“ integravimas.](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a>Tikrinti lentelės kūrimo būseną

Virtualios lentelės sukurtos „Dataverse“ per nesinchronišką fono procesą. Proceso atnaujinimai rodomi veiksmų centre. Išsami informacija apie procesą, įskaitant klaidos žurnalus, rodoma puslapyje **Proceso automatizavimai**.

1. „Human Resources“ atidarykite puslapį **Proceso automatizavimai**.

2. Pasirinkite skirtuką **Fone vykstantys procesai**.

3. Rinkitės **Virtualios lentelės apklausos nesinchroniško veiksmo fono procesas**.

4. Pasirinkite **Peržiūrėti naujausius rezultatus**.

Išslenkančioje srityje rodomi naujausi proceso vykdymo rezultatai. Galite peržiūrėti proceso žurnalą, įskaitant visas iš „Dataverse” grąžintas klaidas.

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas yra „Dataverse“?](/powerapps/maker/common-data-service/data-platform-intro)<br>
[Lentelės „Dataverse“](/powerapps/maker/common-data-service/entity-overview)<br>
[Lentelės ryšių apžvalga](/powerapps/maker/common-data-service/relationships-overview)<br>
[Kurti ir redaguoti virtualias lenteles, kuriose yra duomenys iš išorės duomenų šaltinio](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Kas yra „Power Apps“ portalai?](/powerapps/maker/portals/overview)<br>
[Programų kūrimo „Power Apps“ apžvalga](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

