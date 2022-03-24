---
title: Naujinimas į šalies ir visuotinės adresų knygelės modelius
description: Šioje temoje aprašoma, kaip atnaujinti dvigubo rašymo į šalies ir visuotinės adresų knygelės modelius duomenis.
author: RamaKrishnamoorthy
ms.date: 03/10/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 95d272d9076f1ab25230e4efa98e321bdd618062
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407800"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Naujinimas į šalies ir visuotinės adresų knygelės modelį

[!include [banner](../../includes/banner.md)]



Duomenų [Microsoft Azure gamyklos šablonai padeda atnaujinti šiuos esamus duomenis dvigubo rašymo į šalį ir visuotinės adresų knygelės modelį:](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema)**duomenys sąskaitos,** **·** **kontakto ir tiekėjo lentelėse, taip pat pašto ir elektroniniuose adresuose.**

Pateikiami trys duomenų gamyklos šablonai: Jos padeda suderinti duomenis iš finansų ir operacijų programėlių ir klientų įsipareigojimo programėlių.

- **[Šalies šablonas](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (duomenų atnaujinimas į dvigubo rašymo šalies-GAB schemą/arm_template.json)** – **·** **·** **šis** šablonas padeda atnaujinti šalies ir kontakto duomenis, susijusius su sąskaitos, **·** **kontakto ir tiekėjo** duomenimis.
- **[Šalies pašto](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) adreso šablonas (atnaujinti duomenis į dvigubo rašymo šalies-GAB schemą/atnaujinti į šalies pašto adresą – GAB/arm_template.json)** – **šis šablonas padeda atnaujinti pašto adresus, susietus su sąskaitos**, **·** **kontakto** ir tiekėjo duomenimis.
- **[Įrašo elektroninio](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) adreso šablonas (Atnaujinti duomenis į dvigubo rašymo šalies-GAB schemą/Atnaujinti į šalies elektroninį adresą - GAB/arm_template.json)** – **šis šablonas padeda atnaujinti elektroninius adresus, susietus su sąskaitos**,**·** **kontakto** ir tiekėjo duomenimis.

Proceso pabaigoje sugeneruojami šie kableliais atskirtų verčių (.csv) failai.

| Failo vardas | Paskirtis |
|---|---|
| FONewParty.csv | Šis failas padės sukurti naujus **įrašus** finansų ir operacijų programoje. |
| ImportFONewPostalAddressLocation.csv | Šis failas padės sukurti naujus **pašto adreso vietos** įrašus finansų ir operacijų programoje. |
| ImportFONewPartyPostalAddress.csv | Šis failas padės sukurti naujus **šalies pašto adreso** įrašus finansų ir operacijų programoje. |
| ImportFONewPostalAddress.csv | Šis failas padės sukurti naujus **pašto adreso** įrašus finansų ir operacijų programoje. |
| ImportFONewElectronicAddress.csv | Šis failas padės sukurti naujus elektroninio **adreso** įrašus finansų ir operacijų programoje. |

Šioje temoje paaiškinama, kaip naudoti duomenų gamyklos šablonus ir atnaujinti savo duomenis. Jei neturite jokių pritaikymų, galite naudoti šablonus. Tačiau jei turite pritaikyti abonemento, **kontakto** **ir tiekėjo duomenis**, **turite** modifikuoti šablonus, kaip aprašyta šioje temoje.

> [!IMPORTANT]
> Yra specialių instrukcijų, kaip paleisti šalies pašto adresą ir šalies elektroninio adreso šablonus. Pirmiausia turite paleisti šalies šabloną, tada šalies pašto adreso šabloną, tada šalies elektroninio adreso šabloną. Kiekvienas šablonas sukurtas importuoti atskiroje duomenų gamyklose.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš atnaujinant šalies ir visuotinės adresų knygelės modelį, būtina įdiegti šiuos būtinuosius komponentus:

+ Turite turėti "Azure" [abonementą](https://portal.azure.com/).
+ Turite turėti prieigą prie [šablonų](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
+ Privalote būti dvigubo rašymo klientas.

## <a name="prepare-for-the-upgrade"></a>Parengimas atnaujinimui

Atnaujinimui atlikti reikia šio pasirengimo:

+ **Visiškas sinchronizavimas:** **ir finansų,** ir operacijų aplinkos, ir klientų įsipareigojimo aplinkos būsena yra visiškai sinchronizuojama sąskaitoje (klientas), **·** **kontakte ir tiekėjų lentelėse**.
+ **Integravimo raktai:** sąskaita **(klientas),** **kontaktas** ir tiekėjas, **esantis** klientų įsipareigojimo programėlių lentelėse, naudoja ne "box" integravimo raktus. Jeigu tinkinote integravimo raktus, turite tinkinti ir šabloną.
+ **Įrašo numeris:** visuose **abonemente (klientas),** **kontakte** ir **tiekėjo** įrašuose, kurie bus atnaujinti, yra įrašo numeris. Įrašų, kurie neturi įrašo numerio, bus nepaisoma. Jei norite atnaujinti šiuos įrašus, prieš pradėdami atnaujinimo procesą, įtraukite į juos šalies numerį.
+ **Sistemos išlaidos:** naujinimo proceso metu atsijungus nuo finansų ir operacijų aplinkos ir kliento įsipareigojimo aplinkos.
+ **Momentinė kopija:** momentinę finansų ir operacijų programėlių ir klientų įsipareigojimo programėlių kopiją. Tada, norėdami atkurti ankstesnę būseną, jei reikia, galite naudoti momentines kopijas.

## <a name="deployment"></a>Visuotinis diegimas

1. Atsisiųskite šablonus [iš "Dynamics-365-FastTrack-Implementation-Assets"](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
2. Prisijunkite prie [„Azure“ portalo](https://portal.azure.com/).
3. Sukurkite [išteklių grupę](/azure/azure-resource-manager/management/manage-resource-groups-portal).
4. Sukurkite [saugyklos paskyrą](/azure/storage/common/storage-account-create?tabs=azure-portal) jūsų sukurtoje išteklių grupėje.
5. Sukurti duomenų [gamyklos išteklių](/azure/data-factory/quickstart-create-data-factory-portal) grupėje, kurią sukūrėte.
6. Atidarykite duomenų gamyklos ir pasirinkite Autorius **& Monitorius išklotinę** kainą.
7. Skirtuke **Valdyti** pasirinkite **ARM šablonas**.
8. Norėdami **importuoti šalies šabloną,** pasirinkite importuoti **PREKIŲ grupės** šabloną.
9. Importuokite šabloną į duomenų gamyklą. Įveskite šias reikšmes laukams **Projekto informacija** ir **Egzemplioriaus informacija**.

    | Laukas | Reikšmė |
    |---|---|
    | Abonementas | "Azure" abonementas |
    | Išteklių grupė | Pateikite tuos pačius išteklius, pagal kuriuos sukurta saugojimo sąskaita. |
    | Regionas | Regionas |
    | Gamyklos pavadinimas | Gamyklos pavadinimas |
    | Su FO susietas „Service_service” pagrindinis raktas | Prašymo raktas |
    | „Azure Blob Storage_connection String” | "Azure" BLOB saugyklos ryšio eilutė |
    | Su „Dynamics CRM” susietas „Service_password” | Vartotojo abonemento, kurį nurodote kaip vartotojo vardą, slaptažodis |
    | Su FO susietas „Service_properties_type” „Properties_url” | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | Su FO susietas „Service_properties_type” „Properties_tenant” | Informacija (domeno pavadinimas ar nuomininko ID) apie nuomininką, kuriame yra jūsų programa |
    | Su FO susietas „Service_properties_type” „Properties_aad Resource Id” | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | Su FO susietas „Service_properties_type” „Properties_service Principal Id” | Programos kliento ID |
    | Su „Dynamics CRM” susietas „Service_properties_type” „Properties_username” | Vartotojo vardas, naudojamas jungiantis prie "Dynamics 365" |

    Daugiau informacijos ieškokite šiose temose:

    - [„Resource Manager” šablono skatinimas rankiniu būdu kiekvienai aplinkai](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Susietosios tarnybos ypatybės](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Duomenų kopijavimas naudojant „Azure Data Factory”](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Atlikę diegimą, patikrinkite duomenų rinkinius, duomenų srautą ir susietą duomenų gamyklos paslaugą.

    ![Duomenų rinkiniai, duomenų srautas ir susieta paslauga.](media/data-factory-validate.png)

11. Eiti į **Valdyti**. Dalyje **Ryšiai** pasirinkite **Susieta paslauga**. Tada pasirinkite **DynamicsCrmLinkedService**. Dialogo lange **Redaguoti susietą paslaugą (Dynamics CRM)** įveskite šias vertes.

    | Laukas | Reikšmė |
    |---|---|
    | Pavadinimas / vardas ir (arba) pavardė | „DynamicsCrmLinkedService” |
    | Aprašas | Susietos paslaugos, skirtos prisijungti prie CRM egzemplioriaus, kad būtų galima iškviesti objektų duomenis |
    | Prisijungti per integracijos vykdymą | „AutoResolvelntegrationRuntime” |
    | Diegimo tipas | Internete |
    | Paslaugos Uri | `https://<organization-name>.crm[x].dynamics.com` |
    | Autentifikavimo tipas | „Office365” |
    | Vartotojo vardas | |
    | Slaptažodis arba „Azure” raktų saugykla | Slaptažodis |
    | Slaptažodis | |

## <a name="prepare-to-run-the-data-factory-templates"></a>Duomenų gamyklos šablonų paruošimas

Šiame skyriuje aprašomas nustatymas, reikalingas prieš jums paleidus šalies pašto adresą ir šalies elektroninio adreso duomenų gamyklos šablonus.

### <a name="setup-to-run-the-party-postal-address-template"></a>Šalies pašto adreso šablono vykdymo nustatymas

1. Prisiregistruokite prie klientų įsipareigojimo programėlių ir eikite į **Parametrų** \> **personalizavimo parametrus.** Tada skirtuke **Bendra sukonfigūruokite** sistemos administratoriaus abonemento laiko juostos nustatymus. Laiko juosta turi būti universaliuoju laiku (UTC), kad būtų galima atnaujinti pašto adresų iš finansų ir operacijų programėlių "galioja nuo" ir "galioja iki" datas.

    ![Sistemos administratoriaus abonemento laiko juostos parametras.](media/ADF-1.png)

2. Duomenų gamyklos skirtuke Valdyti **, visuotiniuose** parametruose **, sukurkite** šiuos visuotinius parametrus.

    | Skaičius | Pavadinimas / vardas ir (arba) pavardė | Tipas | Reikšmė |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | eilutė | Šis parametras prie naujai sukurtų pašto adresų kaip prefikso pridėti serijos numerį. Būtinai pateikite eilutę, kuri nesuderinamumą su pašto adresais finansų ir operacijų programėlių ir klientų įsipareigojimo programėlių. Pavyzdžiui, naudokite **ADF-PAD-**. |

    ![Globalus parametras PostalAddressIdPrefix sukurtas skirtuke Tvarkyti.](media/ADF-2.png)

3. Baigę pasirinkite Publikuoti **viską**.

    ![Publikuoti visą mygtuką.](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>Šalies elektroninio adreso šablono vykdymo nustatymas

1. Duomenų gamyklos skirtuke **Valdyti**, visuotiniuose **parametruose**, sukurkite šiuos visuotinius parametrus.

    | Skaičius | Pavadinimas / vardas ir (arba) pavardė | Tipas | Reikšmė |
    |---|---|---|---|
    | 1 | IsFOSource | "bo bo" | Šis parametras nustato, kurie pirminiai sistemos adresai pakeičiami konfliktų atveju. Jei vertė teisinga **, pirminiai** finansų ir operacijų programėlių adresai pakeis pirminius adresus klientų įsipareigojimo programėlėse. Jei vertė klaidinga **, pagrindiniai** klientų įsipareigojimo programėlių adresai pakeis pirminius adresus finansų ir operacijų programėlėse. |
    | 2 | ElectronicAddressIdPrefix | eilutė | Šis parametras prie naujai sukurtų elektroninių adresų kaip prefikso pridėti serijos numerį. Pateikite eilutę, kuri nesuderinamumą su elektroniniais adresais finansų ir operacijų programėlėse ir klientų įsipareigojimo programėlėse. Pavyzdžiui, naudokite **ADF-EAD-**. |

    ![IsFOSource ir ElectronicAddressIdPrefix visuotiniai parametrai, sukurti skirtuke Valdymas.](media/ADF-4.png)

2. Baigę pasirinkite Publikuoti **viską**.

## <a name="run-the-templates"></a>Šablonų paleidimas

1. Sustabdykite šias **šalies**, sąskaitos **·**, kontakto **ir** tiekėjo dvigubo **rašymo** schemas, kuriose naudojama finansų ir operacijų programėlių:

    + CDS šalys (msdyn_parties) 
    + Klientai V3(paskyros)
    + Klientai V3(kontaktai)
    + „CDS” kontaktai V2(kontaktai)
    + „CDS” kontaktai V2(kontaktai)
    + Tiekėjas V2 („msdyn_vendor”)
    + Kontaktai V2 (msdyn_contactforparties)
    + CDS įrašo pašto adreso vietos (msdyn_partypostaladdresses)
    + CDS pašto adreso retrospektyva V2 (msdyn_postaladdresses)
    + CDS įrašo pašto adreso vietos (msdyn_postaladdresscollections)
    + Šalies kontaktų V3 (msdyn_partyelectronicaddresses)

2. Įsitikinkite, kad schemos pašalintos iš msdy_dualwriteruntimeconfig **lentelės** Dataverse.
3. Įdiekite [Dvigubo rašymo į Šalies ir Visuotinę adresų knygelė sprendimus](https://aka.ms/dual-write-gab) iš „AppSource”.
4. Finansų ir operacijų programoje paleiskite šių lentelių **pradinį sinchronizavimą**, jei jose yra duomenų:

    + Pasisveikinimai
    + Asmeninių savybių tipai
    + Baigiamoji mandagumo frazė
    + Kontaktinio asmens pareigos
    + Sprendimų priėmimo vaidmenys
    + Lojalumo lygiai

5. Klientų įsipareigojimo programoje išjunkite šiuos priedo veiksmus:

    + Paskyros atnaujinimas

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Paskyros atnaujinimas
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Paskyros atnaujinimas

    + Kontakto atnaujinimas

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Kontakto atnaujinimas
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Kontakto atnaujinimas

    + msdyn_party Atnaujinimas

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party atnaujinimas

    + msdyn_vendor Atnaujinimas

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor atnaujinimas

    + Klientųaddress

        + Kurti

            + Microsoft.Dynamics.GABExtended.Vzs.CreatePartyAddress: klientųaddress kūrimas

        + Naujinti

            + Microsoft.Dynamics.GABExtended.Vzs.CreatePartyAddress: klientųaddress atnaujinimas

        + Panaikinti

            + Microsoft.Dynamics.GABExtended.Vzs.DeleteCustomerAddress: customeraddress naikinimas

    + msdyn_partypostaladdress

        + Kurti

            + Microsoft.Dynamics.GABExtended.Vzs.CreateCustomerAddress: sukurti msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Vzs.PartyPostalAddress: sukurti msdyn_partypostaladdress

        + Naujinti

            + Microsoft.Dynamics.GABExtended.Vzs.CreateCustomerAddress: atnaujinti msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Vzs.PartyPostalAddress: atnaujinti msdyn_partypostaladdress

    + msdyn_postaladdress

        + Kurti

            + Microsoft.Dynamics.GABExtended.Vzs.PostalAddress: sukurti msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Vzs.PostalAddressPostCreate: sukurti msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Vzs.UpdateCustomerAddress: sukurti msdyn_postaladdress

        + Naujinti

            + Microsoft.Dynamics.GABExtended.Vzs.PostalAddressUpdate: atnaujinti msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Vzs.UpdateCustomerAddress: atnaujinti msdyn_postaladdress

    + msdyn_partyelectronicaddress

        + Kurti

            + Microsoft.Dynamics.GABExtended.Vzs.PartyElectronicAddressSync: sukurti msdyn_partyelectronicaddress

        + Naujinti

            + Microsoft.Dynamics.GABExtended.Vzs.PartyElectronicAddressSync: atnaujinti msdyn_partyelectronicaddress

        + Panaikinti

            + Microsoft.Dynamics.GABExtended.Vzs.DeletePartyElectronicAddressSync: naikinti msdyn_partyelectronicaddress

6. „Customer Engagement” programoje uždrauskite šias darbo eigas:

    + Tiekėjų kūrimas lentelėje Klientai
    + Tiekėjų kūrimas lentelėje Klientai
    + Tiekėjų kūrimas asmens tipo lentelėje Kontaktai
    + Tiekėjų kūrimas tipo Asmuo lentelėje Tiekėjai
    + Tiekėjų naujinimas lentelėje Klientai
    + Tiekėjų naujinimas lentelėje Tiekėjai
    + Tiekėjų naujinimas tipo Asmuo lentelėje Kontaktai
    + Tiekėjų naujinimas tipo Asmuo lentelėje Tiekėjai

7. Duomenų gamyklos paleiskite šabloną pasirinkdami Paleidiklio dabar **,** kaip parodyta toliau pateiktame pavyzdyje. Atsižvelgiant į duomenų tūrį, šis procesas gali užtrukti keletą valandų.

    ![Šablono naudojimas.](media/data-factory-trigger.png)

    > [!NOTE]
    > Jei yra pritaikymų **sąskaitai**, kontaktui **ir** tiekėjui **·**, turite modifikuoti šabloną.

8. Importuokite naujus **įrašus** į finansų ir operacijų programą.

    1. Atsisiųskite **FONewParty.csv failą** iš "Azure BLOB" saugyklos. Maršrutas yra **partybootstrapping/output/FONewParty.csv**.
    2. Konvertuokite **FONewParty.csv failą** į Excel failą ir importuokite Excel failą į finansų ir operacijų programą. Taip pat, jei CSV importavimas jums reikalingas, galite importuoti .csv failą tiesiogiai. Atsižvelgiant į duomenų tūrį, šis veiksmas gali užtrukti kelias valandas. Daugiau informacijos rasite [Duomenų importavimo ir eksportavimo užduočių apžvalga](../data-import-export-job.md).

    ![Dataverse Importuojami šalies įrašai.](media/data-factory-import-party.png)

9. Duomenų gamyklos paleiskite šalies pašto adresą ir šalies elektroninio adreso šablonus, vieną po kito.

    + Įrašo pašto adreso šablonas įterpa visus pašto adreso įrašus **klientų** įsipareigojimo programoje ir susieja juos su atitinkamais sąskaitos, kontakto **ir** tiekėjo **įrašais**. Taip pat generuojami trys .csv failai: ImportFONewPostalAddressLocation.csv, ImportFONewPartyPostalAddress.csv ir ImportFONewPostalAddress.csv.
    + Įrašo elektroninio adreso šablonas įterpa visus elektroninius adresus **klientų** įsipareigojimo programoje ir susieja juos su atitinkamais sąskaitos, kontakto **ir** tiekėjo **įrašais**. Taip pat sugeneruoja vieną .csv failą: ImportFONewElectronicAddress.csv.

    ![Šalies pašto adreso ir šalies elektroninio adreso šablonų paleistis.](media/ADF-7.png)

10. Norėdami atnaujinti finansų ir operacijų programą naudodami šiuos duomenis, turite konvertuoti .csv failus į Excel [darbaknygę ir importuoti juos į finansų ir operacijų programą](/data-entities/data-import-export-job). Taip pat, jei CSV importavimas veikia jums, galite importuoti .csv failus tiesiogiai. Atsižvelgiant į tūrį, šis veiksmas gali užtrukti kelias valandas.

    ![Sėkmingas importavimas.](media/ADF-8.png)

11. Klientų įsipareigojimo programoje įjunkite šiuos priedo veiksmus:

    + Paskyros atnaujinimas

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Paskyros atnaujinimas
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Paskyros atnaujinimas

    + Kontakto atnaujinimas

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Kontakto atnaujinimas
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Kontakto atnaujinimas

    + msdyn_party Atnaujinimas

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party atnaujinimas

    + msdyn_vendor Atnaujinimas

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor atnaujinimas

    + msdyn_partypostaladdress

        + Kurti

            + Microsoft.Dynamics.GABExtended.Vzs.CreateCustomerAddress: sukurti msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Vzs.PartyPostalAddress: sukurti msdyn_partypostaladdress

        + Naujinti

            + Microsoft.Dynamics.GABExtended.Vzs.CreateCustomerAddress: atnaujinti msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Vzs.PartyPostalAddress: atnaujinti msdyn_partypostaladdress

    + msdyn_postaladdress

        + Kurti

            + Microsoft.Dynamics.GABExtended.Vzs.PostalAddress: sukurti msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Vzs.PostalAddressPostCreate: sukurti msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Vzs.UpdateCustomerAddress: sukurti msdyn_postaladdress

        + Naujinti

            + Microsoft.Dynamics.GABExtended.Vzs.PostalAddressUpdate: atnaujinti msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Vzs.UpdateCustomerAddress: atnaujinti msdyn_postaladdress
 
    + msdyn_partyelectronicaddress

        + Kurti

            + Microsoft.Dynamics.GABExtended.Vzs.PartyElectronicAddressSync: sukurti msdyn_partyelectronicaddress

        + Naujinti

            + Microsoft.Dynamics.GABExtended.Vzs.PartyElectronicAddressSync: atnaujinti msdyn_partyelectronicaddress

        + Panaikinti

            + Microsoft.Dynamics.GABExtended.Vzs.DeletePartyElectronicAddressSync: naikinti msdyn_partyelectronicaddress

12. Klientų įdarbinimo programoje suaktyvinkite šias darbo eigas, jei anksčiau jas išjungėte:

    + Tiekėjų kūrimas lentelėje Klientai
    + Tiekėjų kūrimas lentelėje Klientai
    + Tiekėjų kūrimas asmens tipo lentelėje Kontaktai
    + Tiekėjų kūrimas tipo Asmuo lentelėje Tiekėjai
    + Tiekėjų naujinimas lentelėje Klientai
    + Tiekėjų naujinimas lentelėje Tiekėjai
    + Tiekėjų naujinimas tipo Asmuo lentelėje Kontaktai
    + Tiekėjų naujinimas tipo Asmuo lentelėje Tiekėjai

13. Vykdykite **šalies įrašą** – susijusias schemas, kaip aprašyta Šalies ir [visuotinoje adresų knygelėje](party-gab.md).

## <a name="explanation-of-the-data-factory-templates"></a>Duomenų gamyklos šablonų paaiškinimas

Šiame skyriuje rasite kiekvieno duomenų gamyklos šablono veiksmus.

### <a name="steps-in-the-party-template"></a>Veiksmai šalies šablone

1. 1–6 žingsnius nustatykite įmones, kurios yra įgalintos dvigubo rašymo funkcijai, ir sukuria joms filtro sąlygą.
2. 7–1–7–9 žingsniai nuskaito duomenis iš finansų ir operacijų programos bei klientų įsipareigojimo programos ir iš to etapo, kurį norite atnaujinti.
3. 8–9 veiksmais palyginkite **sąskaitos**, **·** **kontakto** ir tiekėjo įrašų tarp finansų ir operacijų programos ir kliento įsipareigojimų programos šalies numerį. Praleisti visi įrašai, kurie neturi įrašo numerio.
4. 10 veiksmas sugeneruoja du įrašų .csv failus, kurie turi būti sukurti kliento įsipareigojimo programoje ir finansų ir operacijų programoje.

    - **PSTDSParty.csv** – šiame faile yra visi abiejų sistemų šalies įrašai, nepaisant to, ar įmonė įgalinta dvigubo rašymo funkcijai.
    - **FONewParty.csv** – šiame faile yra žinomų įrašų (pvz., potencialaus kliento tipo sąskaitų Dataverse) submeniu **·**.

5. 11 veiksmu sukuriamos klientų įsipareigojimo programos šalys.
6. 12 veiksmas nuskaito visuotinai unikalius šalių identifikatorius (GUID) **iš** klientų įsipareigojimų programos ir etapų, kad vėliau jie būtų susieti su Sąskaita, **·** **Kontaktu** ir Tiekėjo įrašais.
7. 13 veiksmas susieja sąskaitos **, kontakto** **ir** tiekėjo įrašus **su** šalies GUID.
8. 14–1–14–3 **veiksmais** atnaujinkite klientų įsipareigojimų programos sąskaitos, **·** **kontakto** ir tiekėjo įrašus su šalies GUID.
9. 15–1–15–3 **veiksmais kontaktas paruoškite įrašus** **sąskaitai**, kontaktui **ir** tiekėjui.**·**
10. 16–1–16–7 veiksmus nuskaityti nuorodos duomenis, pvz., pasveikinimus ir asmeninius simbolių tipus, **ir susieti juos su šalių įrašų kontaktu**.
11. 17 veiksmas sulieja **įrašo kontaktą sąskaitos**, kontakto **·** **ir** tiekėjo **įrašams**.
12. 18 veiksmu importuoja **šalių įrašų kontaktą** į klientų aptarnavimo programą.

### <a name="steps-in-the-party-postal-address-template"></a>Šalies pašto adreso šablone atlikti veiksmai

1. 1–1–10 veiksmai nuskaito duomenis iš finansų ir operacijų programos ir klientų įsipareigojimo programos bei iš to etapo, kurį reikia atnaujinti.
2. 2 veiksmas normalizuoja pašto adreso duomenis finansų ir operacijų programoje, sujungdamas pašto adresą ir šalies pašto adresą.
3. 3 veiksmas: dublikatai ir sulietų sąskaitų, kontaktų ir tiekėjų adresų duomenys iš klientų įdarbinimo programos.
4. 4 veiksmu sukuriami finansų ir operacijų programos .csv failai, skirti naujiems adreso duomenims pagal sąskaitą, kontaktą ir tiekėjo adresus kurti.
5. 5–1 veiksmu sukuriami .csv failai, skirti klientų įsipareigojimo programai, kad būtų sukurti visi adreso duomenys, remiantis finansų ir operacijų programa ir klientų įsipareigojimų programa.
6. 5–2 veiksmus .csv failai konvertuojami į neautomatinį importavimo finansų ir operacijų importavimo formatą.

    - ImportFONewPostalAddressLocation.csv
    - ImportFONewPartyPostalAddress.csv
    - ImportFONewPostalAddress.csv

7. 6 veiksmu importuojami pašto adresų rinkinio duomenys į klientų įsipareigojimo programą.
8. 7 veiksmai nuskaito pašto adresų rinkinio duomenis iš klientų įdarbinimo programos.
9. 8 žingsniu sukuriami kliento adreso duomenys ir susiejamas pašto adreso rinkinio ID.
10. 9–1–9–2 žingsniai susieja šalies ir pašto adresų rinkinio ID su pašto adresais ir šalių pašto adresais.
11. 10–1–10–3 importo klientų adresai, pašto adresai ir šalių pašto adresai klientų įsipareigojimo programoje.

### <a name="steps-in-the-party-electronic-address-template"></a>Veiksmai šalies elektroninio adreso šablone

1. 1–1–5 veiksmais nuskaitomi duomenys iš finansų ir operacijų programos ir klientų įsipareigojimo programos bei duomenų, kuriuos reikia atnaujinti, etapas.
2. 2 veiksmas konsoliduoja elektroninius adresus klientų įsipareigojimo programoje iš sąskaitos, kontakto ir tiekėjų objektų.
3. 3 veiksmu suliejami pagrindiniai elektroninio adreso duomenys iš klientų įsipareigojimo programos ir finansų ir operacijų programos.
4. 4 žingsniu sukuriami .csv failai.

    - Kurkite naujus finansų ir operacijų programos elektroninio adreso duomenis pagal sąskaitą, kontaktą ir tiekėjo adresus.
    - Kurkite naujus klientų įsipareigojimo programos elektroninio adreso duomenis, paremtus elektroninio adreso, sąskaitos, kontakto ir tiekėjo adresais finansų ir operacijų programoje.

5. 5–1 veiksmu importuojami elektroniniai adresai į klientų įsipareigojimo programą.
6. 5–2 veiksmu sukuriami .csv failai, skirti klientų įdarbinimo programoje atnaujinti pirminius sąskaitų ir kontaktų adresus.
7. 6–1–6–2 veiksmų importavimo sąskaitos ir pagrindiniai kontakto adresai klientų įsipareigojimo programoje.

## <a name="troubleshooting"></a>Trikčių šalinimas

1. Jei procesas nepavyksta, iš naujo paleiskite duomenų gamyklos duomenis. Pradėti nuo trikties veiklos.
2. Kai kurie failai, kuriuos sugeneravo duomenų gamyklos, gali būti naudojami duomenų tikrinimas.
3. Duomenų gamyklos parametrai paleidžiami remiantis .csv failais. Todėl jei kablelis įtraukiamas į bet kurią lauko vertę, jis gali pereiti prie rezultatų. Turite pašalinti visas lauko reikšmių kablelius.
4. Skirtuke **Stebėjimas** pateikiama informacija apie visus apdorotus veiksmus ir duomenis. Pasirinkite konkretų veiksmą jo suderinimui.

    ![Stebėjimo skirtukas.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Sužinokite daugiau apie šabloną

Norėdami gauti daugiau informacijos apie šabloną, žr. " [Azure" duomenų gamyklos šablono "Readme" komentarus](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).
