---
title: Naujinimas į šalies ir visuotinės adresų knygelės modelius
description: Šioje temoje aprašoma, kaip atnaujinti dvigubo rašymo į šalies ir visuotinės adresų knygelės modelius duomenis.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 579a7d19ee7196d3242c78bd9915df24ec479c31
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060490"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Naujinimas į šalies ir visuotinės adresų knygelės modelį

[!include [banner](../../includes/banner.md)]



The [Microsoft Azure Data Factory šablonai](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) padėti atnaujinti šiuos esamus dvigubo rašymo duomenis į šalies ir visuotinės adresų knygos modelį: duomenys **sąskaita**, **·**, ir **Pardavėjas** lenteles ir pašto bei elektroninius adresus.

Pateikiami šie trys „Data Factory“ šablonai. Jie padeda suderinti duomenis iš „Finance and Operations“ ir iš klientų įtraukimo programų.

- **[Vakarėlio šablonas](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (Naujovinkite duomenis į dvigubo rašymo Party-GAB schema/arm_template.json)** – Šis šablonas padeda atnaujinti **Vakarėlis** ir **kontaktas** duomenis, kurie yra susieti su **sąskaita**, **·**, ir **Pardavėjas** duomenis.
- **[Vakarėlio pašto adreso šablonas](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) (Naujovinkite duomenis į dvigubo rašymo partijos-GAB schemą / naujovinkite į partijos pašto adresą – GAB/arm_template.json)** – Šis šablonas padeda atnaujinti pašto adresus, kurie yra susieti su **sąskaita**, **·**, ir **Pardavėjas** duomenis.
- **[Vakarėlio elektroninio adreso šablonas](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) (Naujovinkite duomenis į dvigubo rašymo partijos-GAB schemą / naujovinkite į šalies elektroninį adresą – GAB/arm_template.json)** – Šis šablonas padeda atnaujinti elektroninius adresus, kurie yra susieti su **sąskaita**, **·**, ir **Pardavėjas** duomenis.

Proceso pabaigoje sugeneruojami šie kableliais atskirtų reikšmių (.csv) failai.

| Failo vardas | Paskirtis |
|---|---|
| FONewParty.csv | Šis failas padeda sukurti naują **Vakarėlis** įrašai „Finance and Operations“ programoje. |
| ImportFONewPostalAddressLocation.csv | Šis failas padeda sukurti naują **Pašto adresas Vieta** įrašus programėlėje „Finance and Operations“. |
| ImportFONewPartyPostalAddress.csv | Šis failas padeda sukurti naują **Vakarėlio pašto adresas** įrašus programėlėje „Finance and Operations“. |
| ImportFONewPostalAddress.csv | Šis failas padeda sukurti naują **Pašto adresas** įrašus programėlėje „Finance and Operations“. |
| ImportFONewElectronicAddress.csv | Šis failas padeda sukurti naują **Elektroninis adresas** įrašus programėlėje „Finance and Operations“. |

Šioje temoje paaiškinama, kaip naudoti „Data Factory“ šablonus ir atnaujinti duomenis. Jei neturite tinkinimų, galite naudoti tokius šablonus, kokie jie yra. Tačiau, jei turite tinkinimų **sąskaita**, **·**, ir **Pardavėjas** duomenis, turite keisti šablonus, kaip aprašyta šioje temoje.

> [!IMPORTANT]
> Partijos pašto adreso ir partijos elektroninio adreso šablonams paleisti yra specialios instrukcijos. Pirmiausia turite paleisti Šalies šabloną, tada Šalies pašto adreso šabloną ir tada Šalies elektroninio adreso šabloną. Kiekvienas šablonas skirtas importuoti į atskirą duomenų gamyklą.

## <a name="prerequisites"></a>Būtinieji komponentai

Kad galėtumėte naujovinti į partijos ir visuotinės adresų knygos modelį, turi būti įvykdytos šios būtinosios sąlygos:

+ Jūs privalote turėti [Azure prenumerata](https://portal.azure.com/).
+ Turite turėti prieigą prie [šablonus](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
+ Privalote būti dvigubo rašymo klientas.

## <a name="prepare-for-the-upgrade"></a>Parengimas atnaujinimui

Atnaujinti reikia tokio pasiruošimo:

+ **Pilnas sinchronizavimas:** Tiek finansų ir operacijų aplinka, tiek klientų įtraukimo aplinka yra visiškai sinchronizuotos **Paskyra (klientas)**, **·**, ir **Pardavėjas** lenteles.
+ **Integravimo raktai:** The **Paskyra (klientas)**, **·**, ir **Pardavėjas** Klientų įtraukimo programų lentelėse naudojami jau paruošti integravimo raktai. Jeigu tinkinote integravimo raktus, turite tinkinti ir šabloną.
+ **Vakarėlio numeris:** Visi **Paskyra (klientas)**, **·**, ir **Pardavėjas** įrašai, kurie bus atnaujinti, turi partijos numerį. Įrašai, neturintys partijos numerio, bus ignoruojami. Jei norite atnaujinti tuos įrašus, prieš pradėdami naujinimo procesą pridėkite prie jų šalies numerį.
+ **Sistemos gedimas:** Atnaujinimo proceso metu turėsite atjungti tiek finansų ir operacijų aplinką, tiek klientų įtraukimo aplinką.
+ **Momentinė nuotrauka:** Padarykite „Finance and Operations“ ir klientų įtraukimo programų momentinę nuotrauką. Tada galite naudoti momentines nuotraukas, kad atkurtumėte ankstesnę būseną, jei reikia.

## <a name="deployment"></a>Visuotinis diegimas

1. Atsisiųskite šablonus iš [„Dynamics-365-FastTrack-Implementation-Assets“](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
2. Prisijunkite prie [„Azure“ portalo](https://portal.azure.com/).
3. Sukurkite [išteklių grupę](/azure/azure-resource-manager/management/manage-resource-groups-portal).
4. Sukurkite [saugyklos paskyrą](/azure/storage/common/storage-account-create?tabs=azure-portal) jūsų sukurtoje išteklių grupėje.
5. Sukurti [duomenų gamykla](/azure/data-factory/quickstart-create-data-factory-portal) sukurtoje išteklių grupėje.
6. Atidarykite duomenų gamyklą ir pasirinkite **Autorius ir stebėtojas** plytelė.
7. Skirtuke **Valdyti** pasirinkite **ARM šablonas**.
8. Pasirinkite **Importuoti ARM šabloną** importuoti **Vakarėlis** šabloną.
9. Importuokite šabloną į duomenų gamyklą. Įveskite šias reikšmes laukams **Projekto informacija** ir **Egzemplioriaus informacija**.

    | Laukas | Reikšmė |
    |---|---|
    | Abonementas | Azure prenumerata |
    | Išteklių grupė | Pateikite tuos pačius išteklius, pagal kuriuos sukurta saugyklos paskyra. |
    | Regionas | Regionas |
    | Gamyklos pavadinimas | Gamyklos pavadinimas |
    | Su FO susietas „Service_service” pagrindinis raktas | Programos raktas |
    | „Azure Blob Storage_connection String” | „Azure Blob“ saugyklos ryšio eilutė |
    | Su „Dynamics CRM” susietas „Service_password” | Vartotojo abonemento, kurį nurodėte kaip vartotojo vardą, slaptažodis |
    | Su FO susietas „Service_properties_type” „Properties_url” | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | Su FO susietas „Service_properties_type” „Properties_tenant” | Informacija (domeno vardas arba nuomininko ID) apie nuomininką, kuriam priklauso jūsų programa |
    | Su FO susietas „Service_properties_type” „Properties_aad Resource Id” | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | Su FO susietas „Service_properties_type” „Properties_service Principal Id” | Programos kliento ID |
    | Su „Dynamics CRM” susietas „Service_properties_type” „Properties_username” | Vartotojo vardas, naudojamas prisijungiant prie „Dynamics 365“. |

    Daugiau informacijos ieškokite šiose temose:

    - [„Resource Manager” šablono skatinimas rankiniu būdu kiekvienai aplinkai](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Susietosios tarnybos ypatybės](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Duomenų kopijavimas naudojant „Azure Data Factory”](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Atlikę diegimą, patikrinkite duomenų rinkinius, duomenų srautą ir susietą duomenų gamyklos paslaugą.

    ![Duomenų rinkiniai, duomenų srautas ir susieta paslauga.](media/data-factory-validate.png)

11. Eiti į **Tvarkyti**. Dalyje **Ryšiai** pasirinkite **Susieta paslauga**. Tada pasirinkite **DynamicsCrmLinkedService**. Viduje konors **Redaguoti susietą paslaugą (Dynamics CRM)** dialogo lange įveskite šias reikšmes.

    | Laukas | Reikšmė |
    |---|---|
    | Pavadinimas | „DynamicsCrmLinkedService” |
    | Aprašas | Susietos paslaugos, skirtos prisijungti prie CRM egzemplioriaus, kad būtų galima iškviesti objektų duomenis |
    | Prisijungti per integracijos vykdymą | „AutoResolvelntegrationRuntime” |
    | Diegimo tipas | Internete |
    | Paslaugos Uri | `https://<organization-name>.crm[x].dynamics.com` |
    | Autentifikavimo tipas | „Office365” |
    | Vartotojo vardas | |
    | Slaptažodis arba „Azure” raktų saugykla | Slaptažodis |
    | Slaptažodis | |

## <a name="prepare-to-run-the-data-factory-templates"></a>Pasiruoškite paleisti Data Factory šablonus

Šiame skyriuje aprašoma sąranka, kurios reikia prieš paleidžiant šalies pašto adreso ir šalies elektroninio adreso duomenų gamyklos šablonus.

### <a name="setup-to-run-the-party-postal-address-template"></a>Nustatykite, kad paleistumėte vakarėlio pašto adreso šabloną

1. Prisijunkite prie klientų įtraukimo programų ir eikite į **Nustatymai** \> **Personalizavimo nustatymai**. Tada, ant **Generolas** skirtuke, sukonfigūruokite laiko juostos nustatymą sistemos administratoriaus paskyrai. Laiko juosta turi būti suderintu pasauliniu laiku (UTC), kad būtų atnaujintos „Finance and Operations“ programos pašto adresų „galioja nuo“ ir „galioja iki“ datos.

    ![Sistemos administratoriaus paskyros laiko juostos nustatymas.](media/ADF-1.png)

2. „Data Factory“ svetainėje **Tvarkyti** skirtukas, apačioje **Pasauliniai parametrai**, sukurkite šį visuotinį parametrą.

    | Skaičius | Pavadinimas | Tipas | Reikšmė |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | eilutė | Šis parametras prie naujai sukurtų pašto adresų prideda serijos numerį kaip priešdėlį. Būtinai pateikite eilutę, kuri neprieštarauja pašto adresams „Finance and Operations“ ir klientų įtraukimo programose. Pavyzdžiui, naudoti **ADF-PAD-**. |

    ![Pasaulinis parametras PostalAddressIdPrefix, sukurtas skirtuke Tvarkyti.](media/ADF-2.png)

3. Kai baigsite, pasirinkite **Paskelbti viską**.

    ![Mygtukas Paskelbti viską.](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>Nustatykite, kad paleistumėte vakarėlio elektroninio adreso šabloną

1. „Data Factory“ svetainėje **Tvarkyti** skirtukas, apačioje **Pasauliniai parametrai**, sukurkite šiuos visuotinius parametrus.

    | Skaičius | Pavadinimas | Tipas | Reikšmė |
    |---|---|---|---|
    | 1 | IsFOSource | bool | Šis parametras nustato, kurie pirminiai sistemos adresai turi būti pakeisti konfliktų atveju. Jei vertė yra **tiesa**, pirminiai adresai „Finance and Operations“ programose pakeis pirminius adresus klientų įtraukimo programose. Jei vertė yra **klaidinga**, pirminiai adresai klientų įtraukimo programose pakeis pirminius adresus programose „Finance and Operations“. |
    | 2 | ElectronicAddressIdPrefix | eilutė | Šis parametras prie naujai sukurtų elektroninių adresų prideda serijos numerį kaip priešdėlį. Būtinai pateikite eilutę, kuri neprieštarauja elektroniniams adresams „Finance and Operations“ ir klientų įtraukimo programose. Pavyzdžiui, naudoti **ADF-EAD-**. |

    ![„IsFOSource“ ir „ElectronicAddressIdPrefix“ bendrieji parametrai, sukurti skirtuke „Tvarkyti“.](media/ADF-4.png)

2. Kai baigsite, pasirinkite **Paskelbti viską**.

## <a name="run-the-templates"></a>Paleiskite šablonus

1. Sustabdykite šiuos veiksmus **sąskaita**, **·**, ir **Pardavėjas** dvigubo rašymo žemėlapiai, kuriuose naudojama programa „Finance and Operations“:

    + Klientai V3(paskyros)
    + Klientai V3(kontaktai)
    + „CDS” kontaktai V2(kontaktai)
    + „CDS” kontaktai V2(kontaktai)
    + Tiekėjas V2 („msdyn_vendor”)

2. Įsitikinkite, kad žemėlapiai pašalinti iš **msdy_dualwriteruntimeconfig** stalo viduje Dataverse.
3. Įdiekite [Dvigubo rašymo į Šalies ir Visuotinę adresų knygelė sprendimus](https://aka.ms/dual-write-gab) iš „AppSource”.
4. Programoje „Finance and Operations“ paleiskite **Pradinis sinchronizavimas** toliau nurodytoms lentelėms, jei jose yra duomenų:

    + Pasisveikinimai
    + Asmeninių savybių tipai
    + Baigiamoji mandagumo frazė
    + Kontaktinio asmens pareigos
    + Sprendimų priėmimo vaidmenys
    + Lojalumo lygiai

5. Klientų įtraukimo programoje išjunkite šiuos papildinio veiksmus:

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

    + Kliento adresas

        + Kurti

            + Microsoft.Dynamics.GABEextended.Plugins.CreatePartyAddress: Kliento adreso kūrimas

        + Naujinti

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: kliento adreso atnaujinimas

        + Panaikinti

            + Microsoft.Dynamics.GABEextended.Plugins.DeleteCustomerAddress: kliento adreso ištrynimas

    + msdyn_partypostaladdress

        + Kurti

            + Microsoft.Dynamics.GABEextended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress kūrimas
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdress kūrimas

        + Naujinti

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress atnaujinimas
            + Microsoft.Dynamics.GABEextended.Plugins.PartyPostalAddress: msdyn_partypostaladdress atnaujinimas

    + msdyn_pašto adresas

        + Kurti

            + Microsoft.Dynamics.GABEextended.Plugins.PostalAddress: msdyn_postaladdress kūrimas
            + Microsoft.Dynamics.GABEextended.Plugins.PostalAddressPostCreate: msdyn_postaladdress kūrimas
            + Microsoft.Dynamics.GABEextended.Plugins.UpdateCustomerAddress: msdyn_postaladdress kūrimas

        + Naujinti

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: msdyn_postaladdress atnaujinimas
            + Microsoft.Dynamics.GABEextended.Plugins.UpdateCustomerAddress: msdyn_postaladdress atnaujinimas

    + msdyn_partyelectronicaddress

        + Kurti

            + Microsoft.Dynamics.GABEextended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress kūrimas

        + Naujinti

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress atnaujinimas

        + Panaikinti

            + Microsoft.Dynamics.GABEextended.Plugins.DeletePartyElectronicAddressSync: ištrinkite msdyn_partyelectronicaddress

6. „Customer Engagement” programoje uždrauskite šias darbo eigas:

    + Tiekėjų kūrimas lentelėje Klientai
    + Tiekėjų kūrimas lentelėje Klientai
    + Tiekėjų kūrimas asmens tipo lentelėje Kontaktai
    + Tiekėjų kūrimas tipo Asmuo lentelėje Tiekėjai
    + Tiekėjų naujinimas lentelėje Klientai
    + Tiekėjų naujinimas lentelėje Tiekėjai
    + Tiekėjų naujinimas tipo Asmuo lentelėje Kontaktai
    + Tiekėjų naujinimas tipo Asmuo lentelėje Tiekėjai

7. Duomenų gamykloje paleiskite šabloną pasirinkdami **Suaktyvinkite dabar** kaip parodyta toliau pateiktoje iliustracijoje. Šis procesas gali užtrukti kelias valandas, atsižvelgiant į duomenų kiekį.

    ![Šablono paleidimas.](media/data-factory-trigger.png)

    > [!NOTE]
    > Jei turite tinkinimų **sąskaita**, **·**, ir **Pardavėjas**, turite pakeisti šabloną.

8. Importuokite naują **Vakarėlis** įrašus į „Finance and Operations“ programėlę.

    1. Atsisiųskite **FONewParty.csv** failą iš Azure Blob saugyklos. Kelias yra **partybootstrapping/output/FONewParty.csv**.
    2. Konvertuoti **FONewParty.csv** failą į „Excel“ failą ir importuoti „Excel“ failą į programą „Finance and Operations“. Arba, jei CSV importavimas jums tinka, galite importuoti .csv failą tiesiogiai. Šis veiksmas gali užtrukti kelias valandas, atsižvelgiant į duomenų kiekį. Daugiau informacijos rasite [Duomenų importavimo ir eksportavimo užduočių apžvalga](../data-import-export-job.md).

    ![Importuojant Dataverse Vakarėlio įrašai.](media/data-factory-import-party.png)

9. Duomenų gamykloje vieną po kito paleiskite Šalies pašto adreso ir Šalies elektroninio adreso šablonus.

    + Šalies pašto adreso šablonas iškelia visus pašto adreso įrašus klientų įtraukimo programoje ir susieja juos su atitinkamais **sąskaita**, **·**, ir **Pardavėjas** įrašų. Taip pat sukuriami trys .csv failai: ImportFONewPostalAddressLocation.csv, ImportFONewPartyPostalAddress.csv ir ImportFONewPostalAddress.csv.
    + Šalies elektroninio adreso šablonas įtraukia visus elektroninius adresus klientų įtraukimo programėlėje ir susieja juos su atitinkamais **sąskaita**, **·**, ir **Pardavėjas** įrašų. Taip pat sukuriamas vienas .csv failas: ImportFONewElectronicAddress.csv.

    ![Šalies pašto adreso ir partijos elektroninio adreso šablonų paleidimas.](media/ADF-7.png)

10. Norėdami atnaujinti programą „Finance and Operations“ naudodami šiuos duomenis, turite konvertuoti .csv failus į „Excel“ darbaknygę ir [importuokite jį į programą „Finance and Operations“.](/data-entities/data-import-export-job). Arba, jei CSV importavimas jums tinka, galite importuoti .csv failus tiesiogiai. Šis veiksmas gali užtrukti kelias valandas, atsižvelgiant į garsumą.

    ![Sėkmingas importas.](media/ADF-8.png)

11. Klientų įtraukimo programoje įgalinkite šiuos papildinio veiksmus:

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

            + Microsoft.Dynamics.GABEextended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress kūrimas
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: msdyn_partypostaladdress kūrimas

        + Naujinti

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: msdyn_partypostaladdress atnaujinimas
            + Microsoft.Dynamics.GABEextended.Plugins.PartyPostalAddress: msdyn_partypostaladdress atnaujinimas

    + msdyn_pašto adresas

        + Kurti

            + Microsoft.Dynamics.GABEextended.Plugins.PostalAddress: msdyn_postaladdress kūrimas
            + Microsoft.Dynamics.GABEextended.Plugins.PostalAddressPostCreate: msdyn_postaladdress kūrimas
            + Microsoft.Dynamics.GABEextended.Plugins.UpdateCustomerAddress: msdyn_postaladdress kūrimas

        + Naujinti

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: msdyn_postaladdress atnaujinimas
            + Microsoft.Dynamics.GABEextended.Plugins.UpdateCustomerAddress: msdyn_postaladdress atnaujinimas
 
    + msdyn_partyelectronicaddress

        + Kurti

            + Microsoft.Dynamics.GABEextended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress kūrimas

        + Naujinti

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: msdyn_partyelectronicaddress atnaujinimas

        + Panaikinti

            + Microsoft.Dynamics.GABEextended.Plugins.DeletePartyElectronicAddressSync: ištrinkite msdyn_partyelectronicaddress

12. Klientų įtraukimo programoje suaktyvinkite šias darbo eigas, jei jas anksčiau išaktyvinote:

    + Tiekėjų kūrimas lentelėje Klientai
    + Tiekėjų kūrimas lentelėje Klientai
    + Tiekėjų kūrimas asmens tipo lentelėje Kontaktai
    + Tiekėjų kūrimas tipo Asmuo lentelėje Tiekėjai
    + Tiekėjų naujinimas lentelėje Klientai
    + Tiekėjų naujinimas lentelėje Tiekėjai
    + Tiekėjų naujinimas tipo Asmuo lentelėje Kontaktai
    + Tiekėjų naujinimas tipo Asmuo lentelėje Tiekėjai

13. Paleiskite **Vakarėlis** su įrašais susijusių žemėlapių, kaip aprašyta [Vakarėlių ir pasaulinė adresų knyga](party-gab.md).

## <a name="explanation-of-the-data-factory-templates"></a>„Data Factory“ šablonų paaiškinimas

Šiame skyriuje pateikiami kiekvieno Data Factory šablono veiksmai.

### <a name="steps-in-the-party-template"></a>Veiksmai vakarėlio šablone

1. 1–6 veiksmais nustatomos įmonės, kuriose įgalintas dvigubas rašymas, ir sukuriama joms filtro sąlyga.
2. Atliekant 7–1–7–9 veiksmus, gaunami duomenys iš programos „Finance and Operations“ ir iš klientų įtraukimo programos ir pateikiami naujinimo etapai.
3. Atlikdami 8–9 veiksmus palyginkite partijos numerį **sąskaita**, **·**, ir **Pardavėjas** įrašai tarp programos „Finance and Operations“ ir klientų įtraukimo programos. Visi įrašai, neturintys partijos numerio, praleidžiami.
4. 10 veiksmas sugeneruoja du .csv failai šalies įrašams, kurie turi būti sukurti klientų įtraukimo programoje ir programoje „Finance and Operations“.

    - **FOCDSParty.csv** – Šiame faile yra visi abiejų sistemų šalių įrašai, neatsižvelgiant į tai, ar įmonėje įgalintas dvigubas rašymas.
    - **FONewParty.csv** – Šiame faile yra partijos įrašų poaibis Dataverse žino (pavyzdžiui, sąskaitos apie **Prospektas** tipas).

5. 11 veiksme sukuriamos šalys klientų įtraukimo programoje.
6. 12 veiksmas nuskaito pasaulinius unikalius šalių identifikatorius (GUID) iš klientų įtraukimo programos ir suskirsto juos taip, kad juos būtų galima susieti su **sąskaita**, **·**, ir **Pardavėjas** įrašus tolesniuose etapuose.
7. 13 veiksmas susieja su **sąskaita**, **·**, ir **Pardavėjas** įrašai su partijų GUID.
8. 14-1–14-3 veiksmai atnaujinkite **sąskaita**, **·**, ir **Pardavėjas** įrašai klientų įtraukimo programoje su šalių GUID.
9. Paruoškite 15-1–15-3 veiksmus **Susisiekite su vakarėliu** įrašai už **sąskaita**, **·**, ir **Pardavėjas** įrašų.
10. 16-1–16-7 veiksmais atrenkami referenciniai duomenys, pvz., sveikinimai ir asmeninių simbolių tipai, ir susiejami su **Susisiekite su vakarėliu** įrašų.
11. 17 veiksmas sujungia **Susisiekite su vakarėliu** įrašai už **sąskaita**, **·**, ir **Pardavėjas** įrašų.
12. 18 veiksmas importuoja **Susisiekite su vakarėliu** įrašus į klientų įtraukimo programėlę.

### <a name="steps-in-the-party-postal-address-template"></a>Veiksmai partijos pašto adreso šablone

1. Atliekant 1–1–1–10 veiksmus, gaunami duomenys iš programos „Finance and Operations“ ir iš klientų įtraukimo programos ir surenkami naujinimo duomenys.
2. 2 veiksmas panaikina pašto adreso duomenų normalizavimą programoje „Finance and Operations“, sujungiant pašto adresą ir šalies pašto adresą.
3. 3 veiksmas pašalina ir sujungia paskyros, kontaktinio ir pardavėjo adreso duomenis iš klientų įtraukimo programos.
4. 4 veiksme sukuriami .csv failai, skirti programai „Finance and Operations“, kad būtų sukurti nauji adreso duomenys, pagrįsti paskyros, kontaktų ir tiekėjo adresais.
5. 5-1 veiksme sukuriami .csv failai klientų įtraukimo programai, kad būtų sukurti visi adreso duomenys, remiantis programa „Finance and Operations“ ir klientų įtraukimo programa.
6. 5-2 veiksmas konvertuoja .csv failus į Finance and Operations importavimo formatą, kad būtų galima importuoti rankiniu būdu.

    - ImportFONewPostalAddressLocation.csv
    - ImportFONewPartyPostalAddress.csv
    - ImportFONewPostalAddress.csv

7. 6 veiksmas importuoja pašto adresų rinkimo duomenis į klientų įtraukimo programą.
8. 7 veiksmas nuskaito pašto adresų rinkimo duomenis iš klientų įtraukimo programos.
9. 8 veiksmas sukuria kliento adreso duomenis ir susieja pašto adresų rinkimo ID.
10. 9-1–9-2 veiksmai: susietų šalių ir pašto adresų rinkimo ID su pašto adresais ir šalies pašto adresais.
11. 10-1–10-3 veiksmai importuokite klientų adresus, pašto adresus ir šalies pašto adresus į klientų įtraukimo programą.

### <a name="steps-in-the-party-electronic-address-template"></a>Veiksmai partijos elektroninio adreso šablone

1. Atliekant 1–1–1–5 veiksmus, gaunami duomenys iš programos „Finance and Operations“ ir iš klientų įtraukimo programos ir suskirstyti tie duomenys naujinimui.
2. 2 veiksme sujungiami elektroniniai adresai klientų įtraukimo programoje iš paskyros, kontaktinio ir tiekėjo subjektų.
3. 3 veiksmas sujungia pirminius elektroninius adreso duomenis iš klientų įtraukimo programos ir programos „Finance and Operations“.
4. 4 veiksmas sukuria .csv failus.

    - Kurkite naujus elektroninius adresų duomenis, skirtus programai „Finance and Operations“, atsižvelgdami į paskyros, kontaktų ir tiekėjo adresus.
    - Sukurkite naujus elektroninius klientų įtraukimo programėlės adreso duomenis pagal elektroninį adresą, paskyrą, kontaktinius ir tiekėjo adresus programėlėje „Finance and Operations“.

5. 5-1 veiksmas importuoja elektroninius adresus į klientų įtraukimo programą.
6. 5-2 veiksme sukuriami .csv failai, skirti atnaujinti pirminius paskyrų ir kontaktų adresus klientų įtraukimo programoje.
7. 6–1–6–2 veiksmai importuokite paskyras ir kontaktinius pirminius adresus į klientų įtraukimo programą.

## <a name="troubleshooting"></a>Trikčių šalinimas

1. Jei procesas nepavyksta, iš naujo paleiskite duomenų gamyklą. Pradėkite nuo nesėkmingos veiklos.
2. Kai kurie failai, kuriuos sugeneruoja duomenų gamykla, gali būti naudojami duomenims tikrinti.
3. Duomenų gamykla veikia pagal .csv failus. Todėl, jei į bet kurią lauko reikšmę įtraukiamas kablelis, tai gali trukdyti rezultatams. Turite pašalinti visus kablelius iš lauko verčių.
4. The **Stebėjimas** skirtuke pateikiama informacija apie visus veiksmus ir duomenis, kurie buvo apdoroti. Pasirinkite konkretų veiksmą jo suderinimui.

    ![Stebėjimo skirtukas.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Sužinokite daugiau apie šabloną

Norėdami gauti daugiau informacijos apie šabloną, žr [„Azure Data Factory“ šablono „readme“ komentarai](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).
