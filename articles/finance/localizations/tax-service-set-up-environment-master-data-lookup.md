---
title: Įgalinti mokesčių skaičiavimo konfigūracijos pagrindinių duomenų peržvalgą
description: Šiame straipsnyje paaiškinama, kaip nustatyti ir įgalinti mokesčių skaičiavimo pagrindinių duomenų peržvalgos funkciją.
author: kai-cloud
ms.date: 07/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f9d882340171173e5e503f8b5e3aa856e8544b0
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306210"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Įgalinti mokesčių skaičiavimo konfigūracijos pagrindinių duomenų peržvalgą 

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti ir įgalinti mokesčių skaičiavimo pagrindinių duomenų peržvalgos funkciją. Išplečiamajame sąraše galima pasirinkti vertes mokesčių skaičiavimo konfigūracijoje **laukams**, pvz., Juridiniam subjektui, **Tiekėjo** sąskaitai, **Prekės** kodui ir **Pristatymo terminas**. Šios vertės yra iš susijusios Microsoft Dynamics 365 finansų aplinkos, naudojant duomenų Microsoft Dataverse šaltinį.

> [!NOTE] 
> Mokesčių skaičiavimo pagrindinių duomenų peržvalgos funkcija yra pasirinktinė funkcija. Jei išjungidami mokesčių tarnybos duomenų šaltinių **palaikymo Dataverse** funkciją reguliavimo konfigūracijos tarnyba (RCS), galite praleisti šiuos veiksmus. Tačiau šiuo atveju mokesčių skaičiavimo konfigūracijoje išplečiamasis sąrašas nebus galimas.

Norėdami įjungti išplečiamąjį sąrašą mokesčių skaičiavimo funkcijos versijos konfigūracijoje, atlikite šiuos veiksmus.

1. [Įjunkite Microsoft Power Platform integravimą ir atidarykite Dataverse aplinką.](#enable)
2. [Įdiekite virtualiuosius finansų ir operacijų objektus.](#install)
3. [Registruokite Azure Active Directory (Azure AD) prašymą.](#register)
4. [Suteikite programos teises finansų ir operacijų programėlėse.](#grant)
5. [Sukonfigūruokite virtualiojo objekto duomenų šaltinį.](#configure)
6. [Įgalinkite Dataverse virtualiuosius objektus.](#virtual)
7. [Nustatyti prijungtą mokesčių skaičiavimo programą.](#set-up)
8. [Importuokite ir nustatykite modelio Dataverse susiejimo konfigūraciją.](#import)

## <a name="enable-microsoft-power-platform-integration-and-open-the-dataverse-environment"></a><a name='enable'></a> Įgalinti Microsoft Power Platform integravimą ir aplinkos atidarymą Dataverse

Finansų ir operacijų programėlių integravimas su Microsoft Power Platform Microsoft Dynamics gali būti įgalintas kuriant naują finansų ir operacijų programėlių aplinką vykdymo ciklo tarnybose (LCS). Daugiau informacijos rasite [„Microsoft Power Platform” integravimas – Priedų apžvalga](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Kai baigiate, aplinkos pavadinimas Microsoft Power Platform bus rodomas integravimo **Power Platform** skyriuje.

1. LCS savo finansų ir operacijų aplinkoje integravimo **Power Platform** **skyriuje** raskite ir patykite pastabą apie susietos aplinkos aplinkos pavadinimo vertę.

    [![Aplinkos pavadinimo reikšmė.](./media/tcs-dataverse-master-data-lookup-1.png)](./media/tcs-dataverse-master-data-lookup-1.png)

2. Administravimo centre [Power Platform,](https://admin.powerplatform.microsoft.com/environments) skirtuke **Aplinkos**, pasirinkite aplinką, **kuri** atitinka aplinkos pavadinimo vertę, apie kurią pateikėte pastabą.
3. **Informacijos puslapyje**, raskite **aplinkos** URL Dataverse vertę. Užsirašykite šią vertę, nes jos reikės [7 veiksme. Nustatyti prijungtą mokesčių skaičiavimo programą](#set-up).
4. Įsitikinkite, kad galite atidaryti aplinką Dataverse savo naršyklėje, pasirinkdami **aplinkos URL** vertę.

    [![Dataverse aplinkos puslapis.](./media/tcs-dataverse-master-data-lookup-2.png)](./media/tcs-dataverse-master-data-lookup-2.png)

    > [!NOTE]
    > Aplinkoje Dataverse saugokite aplinką atidarytą naršyklėje. Tai bus reikalinga žingsnyje [5. Sukonfigūruokite virtualiojo objekto duomenų šaltinį](#configure).

Daugiau informacijos ieškokite Enable [the Microsoft Power Platform integration](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

## <a name="install-finance-and-operations-virtual-entities"></a><a name='install'></a> Diegti virtualiuosius finansų ir operacijų objektus

Virtualiųjų Dataverse objektų finansų ir operacijų sprendimas turi būti įdiegtas iš virtualiojo Microsoft AppSource objekto sprendimo.

1. AppSource Raskite virtualų [finansų ir operacijų objektą](https://appsource.microsoft.com/product/dynamics-365/mscrm.finance_and_operations_virtual_entity).
2. Pasirinkite **Gauti dabar**.
3. Lauke Pasirinkti **aplinką įveskite** aplinkos **pavadinimo vertę**, kurią pateikėte kaip ankstesnę pastabą.
4. Pažymėkite žymės langelius, o tada pasirinkite **Diegti**.

Kai diegimas baigtas, galite rasti **finansų**[Power Platform](https://admin.powerplatform.microsoft.com/) ir operacijų virtualiojo objekto programą administravimo centre, **·** \> **dalyje "Resources Dynamics 365" programėlės.**

Norėdami gauti daugiau informacijos, žr. [Virtualiojo objekto sprendimo gimas](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution).

## <a name="register-an-azure-ad-application"></a><a name='register'></a>Azure AD Prašymo registravimas

Turite užregistruoti programą tame Azure AD pačiame nuomininke, kaip ir finansų ir operacijų programėlių, kad jas galėtų iškviesti Dataverse.

1. ["Azure" portale](https://portal.azure.com) eikite į **Azure Active Directory\> programų registracijas**.
2. Pasirinkite **naują registraciją** ir įveskite šią informaciją:

    - **Pavadinimas** – įveskite unikalų pavadinimą.
    - **Sąskaitos tipas** – įveskite bet **kurį Azure AD katalogą** (vieno nuomininko ar kelių nuomininkų).
    - **Nukreipimo URI** – palikite šį lauką tuščią.

3. Pasirinkite **Registruotis**.
4. Pasižymėkite **Programos (kliento) ID** reikšmę, nes jos reikės vėliau.

    [![Azure AD Programos (kliento) ID vertė.](./media/tcs-dataverse-master-data-lookup-3.png)](./media/tcs-dataverse-master-data-lookup-3.png)

5. Sukurti simetrinį programos raktą.
6. Naujoje programoje pasirinkite Sertifikatai **> Paslapymi**.
7. Pasirinkite **Naujas kliento slaptasis raktas**.
8. Įveskite aprašymą, pasirinkite galiojimo pabaigos datą ir pasirinkite **Įrašyti**. Bus sukurtas ir rodomas raktas. Kopijuoti vertę vėlesniam naudojimui.

Daugiau informacijos ieškokite Registruoti [Azure AD prašymą](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#register-the-app-in-the-azure-portal).

## <a name="grant-app-permissions-in-finance-and-operations-apps"></a><a name='grant'></a> Suteikti programos teises finansų ir operacijų programėlėse

Dataverse naudoja programą Azure AD, kurią sukūrėte iškviesti finansų ir operacijų programėles. Todėl programa turi būti pasitikima finansų ir operacijų programėle ir susieta su vartotojo sąskaita, kuri turi atitinkamas teises. Finansų ir operacijų programėlei turite sukurti specialų paslaugų vartotoją, kuris turi teises tik **prie** virtualiojo objekto funkcijų. Šis paslaugų vartotojas neturi turėti kitų teisių. Atlikus šį veiksmą, bet Azure AD kuri programa, kuri turi sukurtos programos slaptą seksą, galės iškviesti finansų ir operacijų programėlių aplinką ir pasiekti virtualiojo objekto funkciją.

1. Savo aplinkoje eikite į sistemos **administravimo** \> **vartotojų** \> **vartotojus**.
2. Pasirinkite **Naujas**, jei norite pridėti naują vartotoją, ir įveskite šią informaciją:

    - **Vartotojo ID** – įveskite **duomenų atvirkštinę reikšmę** ar kitą reikšmę.
    - **Vartotojo vardas** – įvesti **duomenų atvirkštinę integraciją** ar kitą reikšmę.
    - **Teikėjas** – nustatykite šį lauką **kaip NonAAD**.
    - **El** . paštas – **įveskite duomenų atvirkštinę** reikšmę ar kitą reikšmę. (Vertė nebūtinai turi būti galiojanti el. pašto sąskaita.)

3. Priskirkite **Dataverse vartotojui virtualiojo objekto** integravimo programos saugos vaidmenį.
4. Pašalinkite visus kitus vaidmenis, įskaitant **sistemos vartotoją**.
5. Eiti į sistemos **administravimo nustatymo** \> **programas** \> **Azure Active Directory, kurias** norite registruoti.Dataverse 
6. Įtraukite eilutę, tada į kliento **ID** lauką įveskite **programos (kliento) ID** vertę, kurią pateikėte kaip anksčiau pastabą.
7. Lauke **Pavadinimas** įveskite pavadinimą. Pavyzdžiui, įveskite **Dataverse Integravimas**.
8. Lauke Vartotojo **ID** įveskite vartotojo ID, kurį sukūrėte anksčiau.

Norėdami gauti daugiau informacijos, finansų [ir operacijų programėlėse žr. Subsidijos programos teises](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#grant-app-permissions-in-finance-and-operations-apps).

## <a name="configure-the-virtual-entity-data-source"></a><a name='configure'></a>Sukonfigūruokite virtualaus objekto duomenų šaltinį

Turite pateikti finansų ir Dataverse operacijų programos egzempliorių, prie kurių norite prisijungti.

1. Jūsų Dataverse aplinka vis tiek turi būti atidaryta jūsų naršyklėje nuo [1 veiksmo. Įjunkite Microsoft Power Platform integravimą ir atidarykite Dataverse aplinką](#enable). Pasirinkite parametrų mygtuką (pavarų simbolį) viršutinėje dešinėje, tada pasirinkite Išplėstiniai **parametrai**.

    [![Atidaryti išplėstinius aplinkos parametrus Dataverse .](./media/tcs-dataverse-master-data-lookup-4.png)](./media/tcs-dataverse-master-data-lookup-4.png)

2. Nustatymų **išplečiamajame** meniu pasirinkite **Administravimas**.

    [![Administravimo.](./media/tcs-dataverse-master-data-lookup-5.png)](./media/tcs-dataverse-master-data-lookup-5.png)

3. Pasirinkite virtualiojo **objekto duomenų šaltinius**.

    [![Virtualiojo objekto duomenų šaltiniai.](./media/tcs-dataverse-master-data-lookup-6.png)](./media/tcs-dataverse-master-data-lookup-6.png)

4. Pasirinkite duomenų šaltinį, pavadintą **Finansai ir Operacijos**.

    [![Finansų ir operacijų duomenų šaltinis.](./media/tcs-dataverse-master-data-lookup-7.png)](./media/tcs-dataverse-master-data-lookup-7.png)

5. Įveskite šią informaciją iš ankstesnių veiksmų:

    - **Paskirties URL** – įveskite URL, kur galite gauti prieigą prie finansų ir operacijų programėlių.
    - **Autorizavimo URL** – įveskite `https://login.windows.net/`.
    - **Nuomininko ID** – nurodykite savo nuomininką. Ši vertė gali būti jūsų įmonės el. pašto domeno pavadinimas (pvz., contoso.com).
    - **AAD programos ID** – įveskite programos **(kliento) ID** vertę, kuri buvo sukurta anksčiau.
    - **AAD programos slapyme** – įveskite slaptažodį, kuris buvo sugeneruotas anksčiau.
    - **AAD ištekliai** – įveskite **00000015-0000-0000-c000-000000000000**. Ši vertė – tai programa Azure AD, nurodanti finansų ir operacijų programėles. Visada turėtų būti tokia pati vertė.

6. Įrašykite pakeitimus.
7. Uždarykite puslapį, norėdami grįžti į administravimo **puslapį**, kur bus pradėtas [6 veiksmas. Įgalinkite Dataverse virtualiuosius objektus](#virtual).

    [![Uždaromas redaguoti skirtas objektas.](./media/tcs-dataverse-master-data-lookup-8.png)](./media/tcs-dataverse-master-data-lookup-8.png)

Daugiau informacijos rasite virtualiojo [objekto duomenų šaltinio konfigūravimas](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#configure-the-virtual-entity-data-source).

## <a name="enable-dataverse-virtual-entities"></a><a name='virtual'></a> Įgalinti Dataverse virtualiuosius objektus

Kad virtualiieji objektai būtų matomi iš finansų ir operacijų **programėlių**, prieš naudojant mokesčių skaičiavimo konfigūraciją, turi būti nustatyta kaip Taip.

> [!NOTE]
> Šį veiksmą galite praleisti tik vienu spustelėdami 8 veiksmą įjungę su mokesčių apskaičiavimu susijusius [virtualiuosius objektus. Nustatyti prijungtą mokesčių skaičiavimo programą](#import). Tačiau rekomenduojame rankiniu būdu įgalinti bent vieną virtualų objektą, kad nurodytumėte, jog ryšys tarp finansų ir operacijų programėlių yra Dataverse gerai nustatytas.

1. Savo aplinkoje Dataverse, viršutiniame **dešiniajame** kampe, administravimo puslapyje pasirinkite filtro mygtuką (piltuvo simbolį).

    [![Filtro mygtukas.](./media/tcs-dataverse-master-data-lookup-9.png)](./media/tcs-dataverse-master-data-lookup-9.png)

2. Lango Išplėstinė **paieška** lauke Ieškoti **pasirinkite** Galimi finansų **ir operacijų objektai**.
3. Įtraukite šią taisyklę: **Pavadinimas** – **Yra** – **CompanyInfoEntity**. Tada pasirinkite **Rezultatus**.

    [![Išplėstinis ieškos langas.](./media/tcs-dataverse-master-data-lookup-10.png)](./media/tcs-dataverse-master-data-lookup-10.png)

4. Ieškos **rezultatuose pasirinkite CompanyInfoEntity**, pažymėkite žymės **langelį** Matomas, tada pasirinkite **Įrašyti**.

    [![Objekto matomumo nustatymas.](./media/tcs-dataverse-master-data-lookup-11.png)](./media/tcs-dataverse-master-data-lookup-11.png)

5. Pakartokite ankstesnius veiksmus su šiais objektais, kurie nurodyti mokesčių skaičiavimo konfigūracijoje:

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity
    - InventOperationalSitev2Entity
    - TaxExemptCodeEntity
    - InventWarehouseEntity

    > [!NOTE]
    > Tik 5000 Dataverse pirmųjų objekto įrašų galima nuskaityti iš išplečiamojo sąrašo mokesčių skaičiavimo konfigūracija.

Daugiau informacijos žr. skyriuje [Įgalinti Microsoft Dataverse virtualius objektus](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="set-up-the-connected-application-for-tax-calculation"></a><a name='set-up'></a> Nustatyti prijungtą mokesčių skaičiavimo programą

1. Eikite **į Elektroninę** ataskaitą, tada skyriuje Susieti **saitai** pasirinkite Sujungtos **programos**.

    [![Prijungtos programos.](./media/tcs-dataverse-master-data-lookup-12.png)](./media/tcs-dataverse-master-data-lookup-12.png)

2. Pasirinkite **Naujas**, jei norite pridėti įrašą, ir įveskite šią informaciją.

    - Dalyje **Pavadinimas**- įveskite pavadinimą.
    - **Tipas** – pasirinkite **Dataverse**.
    - **Programa** – įveskite Dataverse savo aplinkos **URL** vertę, apie kurią padarėte pastabą [1 veiksme. Įjunkite Microsoft Power Platform integravimą ir atidarykite aplinką Dataverse](#enable).
    - **Nuomininkas** – įveskite savo nuomininką.
    - **Pasirinktinis URL** – įveskite Dataverse URL ir prie jo priduokite **/api/duomenis/v9.1**.

3. Pasirinkite **Tikrinti ryšį**, tada dialogo lange pasirinkite Spustelėkite čia norėdami **prisijungti prie pasirinktos nuotolinės programos**.

    [![Tikrinamas ryšys.](./media/tcs-dataverse-master-data-lookup-13.png)](./media/tcs-dataverse-master-data-lookup-13.png)
4. Įsitikinkite, kad gavote "Sėkmės!" Pranešimas, nurodantis, kad ryšys sėkmingai nustatytas.

    [![Sėkmės pranešimas.](./media/tcs-dataverse-master-data-lookup-14.png)](./media/tcs-dataverse-master-data-lookup-14.png)
    
5. RCS atidarykite funkcijų **valdymo darbo** sritį ir įgalinkite šias funkcijas:

    - Globalizacijos funkcijos
    - Elektroninių ataskaitų „Dataverse” duomenų šaltinių palaikymas
    - Mokesčių tarnybos „Dataverse“ duomenų šaltinių palaikymas

## <a name="import-and-set-up-the-dataverse-model-mapping-configuration"></a><a name='import'></a> Importuoti ir nustatyti modelio susiejimo Dataverse konfigūraciją

"Microsoft" teikia objektų iš finansų ir operacijų programėlių į mokesčių skaičiavimą numatytąsias modelio susiejimo konfigūracijas.

1. RCS eikite į elektroninę **ataskaitą**.
2. Konfigūracijos teikėjų **skyriuje**, "Microsoft **" teikėjo išklotijoje**, pasirinkite **Saugyklos**.

    [![Saugyklas.](./media/tcs-dataverse-master-data-lookup-15.png)](./media/tcs-dataverse-master-data-lookup-15.png)

3. Pasirinkite visuotinės **konfigūracijos saugyklos įrašą**, tada pasirinkite **Atidaryti**.
4. Dalyje **Mokesčių duomenų modelio** \> **mokesčių skaičiavimo duomenų modelis** pasirinkite modelio susiejimo **Dataverse** konfigūraciją.
5. "FastTab **"** versijose pasirinkite versiją, kuri atitinka jūsų finansų ir operacijų programėlių versiją, tada pasirinkite **Importuoti**.

    [![Importuojama modelio susiejimo Dataverse konfigūracija.](./media/tcs-dataverse-master-data-lookup-16.png)](./media/tcs-dataverse-master-data-lookup-16.png)

    > [!IMPORTANT]
    > Modelio **Dataverse susiejimo** konfigūracija veikia tik didžiausiai importuotai versijai. Todėl turėtumėte ne importuoti modelio susiejimo **Dataverse** konfigūracijos versijos, kuri yra didesnė nei mokesčio skaičiavimo konfigūracijos versija, kurią planuojate įdiegti. Pavyzdžiui, jei planuojate įdiegti 40.50.225 konfigūracijos versiją, turėtumėte importuoti tik modelio susiejimo konfigūracijos versiją 40.50.13 **Dataverse**. Neturė turėtumėte importuoti 40.54.14 versijos. Kitu atveju konfigūracijoje bus nesutampa duomenų modelis.

6. Grįžkite **į elektroninę** ataskaitą ir pasirinkite mokesčių **konfigūracijų išklotąją** priemonę.
7. Pasirinkite importuotą **Dataverse modelio susiejimo** konfigūraciją, tada – **Redaguoti**.
8. Nustatykite parinktį **Numatytasis modelių susiejimui** į **Taip**.
9. Lauke **Prijungta programa** pasirinkite prijungtą programą, kurią nustatėte [7 žingsniu. Nustatyti prijungtą mokesčių skaičiavimo programą](#set-up).
10. Nustatykite virtualiosios **lentelės matomumo parinktį** **Taip, norėdami** nustatyti visus su mokesčių apskaičiavimu susijusius virtualiuosius objektus kaip matomus.

Dabar baigėte pagrindinių duomenų peržvalgos funkcijos nustatymą. Dabar mokesčių skaičiavimo **funkcijos nustatyme bus įgalintas išplečiamasis laukų, pvz., Juridinio subjekto,** **·** **Tiekėjo sąskaitos,** **·** **Prekės kodas ir Pristatymo terminas, sąrašas.**

[![Juridinio subjekto išplečiamasis sąrašas.](./media/tcs-dataverse-master-data-lookup-17.png)](./media/tcs-dataverse-master-data-lookup-17.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
