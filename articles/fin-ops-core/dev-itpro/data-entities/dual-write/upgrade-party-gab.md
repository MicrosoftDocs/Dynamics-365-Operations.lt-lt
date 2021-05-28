---
title: Naujinimas į šalies ir visuotinės adresų knygelės modelius
description: Šioje temoje aprašoma, kaip atnaujinti dvigubo rašymo į šalies ir visuotinės adresų knygelės modelius duomenis.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 95472a00d34ba939ac89b4e2484f34d50bee3088
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018317"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Naujinimas į šalies ir visuotinės adresų knygelės modelius

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[„Azure” duomenų gamyklos šablonas](https://aka.ms/dual-write-gab-adf) padeda jums atnaujinti esamus **Paskyros**, **Kontakto** ir **Tiekėjo** lentelės duomenis dvigubame rašyme į šalies ir visuotinės adresų knygelės modelius. Šablonas suderina duomenis iš „Finance and Operations” ir „Customer Engagement” programų. Proceso pabaigoje bus sukurti laukai **Šalis** ir **Kontaktai**, skirti **Šalies** įrašams, ir tie laukai bus susieti su **Paskyros**, **Kontakto** ir **Tiekėjo** įrašais „Customer Engagement” programose. Sugeneruojamas .csv failas (`FONewParty.csv`), kad „Finance and Operations” programoje būtų galima kurti naujus **Šalies** įrašus. Šioje temoje pateikiamos instrukcijos, kaip naudoti Duomenų gamyklos šabloną ir atnaujinti savo duomenis.

Jei neturite jokių tinkinimų, galite naudoti šabloną tokį, koks jis yra. Jei laukams **Paskyra**, **Kontaktas** ir **Tiekėjas** turite tinkinimus, tada turite modifikuoti šabloną pagal šias instrukcijas.

> [!Note]
> Šablonas padeda atnaujinti tik **Šalies** duomenis. Būsimame leidime bus įtraukti pašto ir elektroniniai adresai.

## <a name="prerequisites"></a>Būtinieji komponentai

Reikalingi šie būtinieji komponentai:

+ [„Azure” prenumerata](https://portal.azure.com/)
+ [Prieiga prie šablono](https://aka.ms/dual-write-gab-adf)
+ Jūs – dvigubo rašymo klientas.

## <a name="prepare-for-the-upgrade"></a>Parengimas atnaujinimui

+ **Visiškai sinchronizuota**: Abi aplinkos yra visiškai sinchronizuotoje būsenoje laukams **Paskyra (Klientas)**, **Kontaktas** ir **Tiekėjas**.
+ **Integravimo raktai**: lentelės **Paskyra (Klientas)**, **Kontaktas** ir **Tiekėjas** „Customer Engagement” programose naudoja integravimo raktus, kurie yra visiškai parengti naudoti. Jeigu tinkinote integravimo raktus, turite tinkinti ir šabloną.
+ **Šalies numeris**: Visi laukų **Paskyra (Klientas)**, **Kontaktas** ir **Tiekėjas** įrašai, kurie bus išplėtoti, turi **Šalies** numerį. Įrašų, neturinčių **Šalies** numerio, bus nepaisoma. Jeigu norite išplėtoti šiuos įrašus, prieš pradėdami plėtojimo procesą, į juos įtraukite **Šalies** numerį.
+ **Sistemos triktis**: Plėtojimo proceso metu turėsite atjungti „Finance and Operations” ir „Customer Engagement” aplinkas.
+ **Momentinė kopija**: Pasidarykite „Finance and Operations” ir „Customer Engagement” programų momentines kopijas. Naudokite momentines kopijas ankstesnės būsenos atkūrimui, jei to reikia.

## <a name="deployment"></a>Visuotinis diegimas

1. Atsisiųskite šabloną iš [„Dynamics-365-FastTrack-Implementation-Assets”](https://aka.ms/dual-write-gab-adf).

2. Prisijunkite prie [„Microsoft Azure”](https://portal.azure.com/).

3. Sukurkite [išteklių grupę](/azure/azure-resource-manager/management/manage-resource-groups-portal).

4. Sukurkite [saugyklos paskyrą](/azure/storage/common/storage-account-create?tabs=azure-portal) jūsų sukurtoje išteklių grupėje.

5. Sukurkite [duomenų gamyklą](/azure/data-factory/quickstart-create-data-factory-portal) aukščiau jūsų sukurtoje išteklių grupėje.

6. Atidarykite duomenų gamyklą ir pasirinkite **Kurti & Stebėti** plytelę.

7. Skirtuke **Valdyti** pasirinkite **ARM šablonas**.

8. Pasirinkite **Importuoti ARM šabloną**, kad importuotumėte **Šalies** šabloną.

9. Importuokite šabloną į duomenų gamyklą. Įveskite šias reikšmes laukams **Projekto informacija** ir **Egzemplioriaus informacija**.

    Laukas | Reikšmė
    ---|---
    Prenumerata | „Azure” prenumerata
    Išteklių grupė | Pateikite tuos pačius išteklius, kuriuose sukurta saugyklos paskyra.
    Regionas | Nurodykite regioną.
    Gamyklos pavadinimas | Nurodykite gamyklos pavadinimą.
    Su FO susietas „Service_service” pagrindinis raktas | Nurodykite programos raktą.
    „Azure Blob Storage_connection String” | „Azure“ didelių dvejetainių objektų saugyklos ryšio eilutė.
    Su „Dynamics CRM” susietas „Service_password” | Vartotojo paskyros, kurią nurodėte kaip vartotojo vardą, slaptažodis.
    Su FO susietas „Service_properties_type” „Properties_url”  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    Su FO susietas „Service_properties_type” „Properties_tenant” | Nurodykite nuomotojo informaciją (domeno vardą ar nuomotojo ID), pagal kurią egzistuoja jūsų programa.
    Su FO susietas „Service_properties_type” „Properties_aad Resource Id” | `https://sampledynamics.sandboxoperationsdynamics.com`
    Su FO susietas „Service_properties_type” „Properties_service Principal Id” | Nurodykite programos kliento ID.
    Su „Dynamics CRM” susietas „Service_properties_type” „Properties_username” | Vartotojo vardas, skirtas prisijungti prie „Dynamics”.

    Daugiau informacijos rasite [Rankiniu būdu pakelkite „Resource Manager” šabloną į aukštesnį lygį kiekvienai aplinkai](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Susietos paslaugos ypatybės](/azure/data-factory/connector-dynamics-ax#linked-service-properties) ir [Duomenų kopijavimas naudojant „Azure” duomenų gamyklą](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Atlikę diegimą, patikrinkite duomenų rinkinius, duomenų srautą ir susietą duomenų gamyklos paslaugą.

   ![Duomenų rinkiniai, duomenų srautas ir susieta paslauga](media/data-factory-validate.png)

11. Pereikite prie **Valdyti**. Dalyje **Ryšiai** pasirinkite **Susieta paslauga**. Pasirinkite **„DynamicsCrmLinkedService”**. Formoje **Redaguoti susietą paslaugą („Dynamics CRM”)** įveskite šias reikšmes:

    Laukas | Reikšmė
    ---|---
    Pavadinimas | „DynamicsCrmLinkedService”
    Aprašas | Susietos paslaugos, skirtos prisijungti prie CRM egzemplioriaus, kad būtų galima iškviesti objektų duomenis
    Prisijungti per integracijos vykdymą | „AutoResolvelntegrationRuntime”
    Diegimo tipas | Internete
    Paslaugos Uri | `https://<organization-name>.crm[x].dynamics.com`
    Autentifikavimo tipas | „Office365”
    Vartotojo vardas |
    Slaptažodis arba „Azure” raktų saugykla | Slaptažodis
    Slaptažodis |

## <a name="run-the-template"></a>Šablono vykdymas

1. Sustabdykite **Paskyros**, **Kontakto** ir **Tiekėjo** dvigubą rašymą naudodami „Finance and Operations” programą.

    + Klientai V3(paskyros)
    + Klientai V3(kontaktai)
    + „CDS” kontaktai V2(kontaktai)
    + „CDS” kontaktai V2(kontaktai)
    + Tiekėjas V2 („msdyn_vendor”)

2. Užtikrinkite, kad susiejimai yra pašalinti iš „Dataverse” lentelės `msdy_dualwriteruntimeconfig`.

3. Įdiekite [Dvigubo rašymo į Šalies ir Visuotinę adresų knygelė sprendimus](https://aka.ms/dual-write-gab) iš „AppSource”.

4. Jei šiose „Finance and Operations” programos lentelėse yra duomenų, tada joms paleiskite **Pradinį sinchronizavimą**.

    + Pasisveikinimai
    + Asmeninių savybių tipai
    + Baigiamoji mandagumo frazė
    + Kontaktinio asmens pareigos
    + Sprendimų priėmimo vaidmenys
    + Lojalumo lygiai

5. „Customer Engagement” programoje uždrauskite šiuos papildinių veiksmus.

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

6. „Customer Engagement” programoje uždrauskite šias darbo eigas:

    + Tiekėjų kūrimas lentelėje Klientai
    + Tiekėjų kūrimas lentelėje Klientai
    + Tiekėjų kūrimas asmens tipo lentelėje Kontaktai
    + Tiekėjų kūrimas tipo Asmuo lentelėje Tiekėjai
    + Tiekėjų naujinimas lentelėje Klientai
    + Tiekėjų naujinimas lentelėje Tiekėjai
    + Tiekėjų naujinimas tipo Asmuo lentelėje Kontaktai
    + Tiekėjų naujinimas tipo Asmuo lentelėje Tiekėjai

7. Duomenų gamykloje vykdykite šabloną pasirinkdami **Paleisti dabar**, kaip parodyta šiame paveikslėlyje. Šis procesas gali užtrukti keletą valandų, priklausomai nuo duomenų tūrio.

    ![Paleidiklio vykdymas](media/data-factory-trigger.png)

    > [!NOTE]
    > Jei laukams **Paskyra**, **Kontaktas** ir **Tiekėjas** turite tinkinimus, tada turite modifikuoti šabloną.

8. Importuokite naujus **Šalies** įrašus „Finance and Operations” programoje.

    + Atsisiųskite `FONewParty.csv` failą iš „Azure“ didelių dvejetainių objektų saugyklos. Kelias yra `partybootstrapping/output/FONewParty.csv`.
    + Konvertuokite failą `FONewParty.csv` į „Excel” failą ir tada importuokite „Excel” failą į „Finance and Operations” programą.  Jei csv importavimas jums tinka, galite csv failą importuoti tiesiogiai. Importavimas gali užtrukti kelias valandas, priklausomai nuo duomenų tūrio. Daugiau informacijos rasite [Duomenų importavimo ir eksportavimo užduočių apžvalga](../data-import-export-job.md).

    ![„Dataverse” šalies įrašų importavimas](media/data-factory-import-party.png)

9. „Customer Engagement” programose įgalinkite šiuos papildinių veiksmus:

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

10. „Customer Engagement” suaktyvinkite šias darbo eigas, jei išjungėte jas ankstesniais veiksmais:

    + Tiekėjų kūrimas lentelėje Klientai
    + Tiekėjų kūrimas lentelėje Klientai
    + Tiekėjų kūrimas asmens tipo lentelėje Kontaktai
    + Tiekėjų kūrimas tipo Asmuo lentelėje Tiekėjai
    + Tiekėjų naujinimas lentelėje Klientai
    + Tiekėjų naujinimas lentelėje Tiekėjai
    + Tiekėjų naujinimas tipo Asmuo lentelėje Kontaktai
    + Tiekėjų naujinimas tipo Asmuo lentelėje Tiekėjai

11. Vykdykite su **Šalimi** susijusias schemas, kaip nurodyta [Šalies ir visuotinėje adresų knygelėje](party-gab.md).

## <a name="troubleshooting"></a>Trikčių diagnostika

1. Jei procesas nepavyksta, iš naujo paleiskite duomenų gamyklą, pradedant nuo nesėkmingos veiklos.
2. Kai kuriuos duomenų gamyklos sugeneruotus failus galite naudoti duomenų tikrinimo tikslais.
3. Duomenų gamykla veikia pagal kableliais atskirtus csv failus. Jeigu kuri nors lauko vertė turi kablelius, tai gali trukdyti rezultatams. Jums reikia pašalinti kablelius.
4. Skirtuke **Stebėjimas** pateikiama informacija apie visus veiksmus ir apdorotus duomenis. Pasirinkite konkretų veiksmą jo suderinimui.

    ![Stebėjimo skirtukas](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Sužinokite daugiau apie šabloną

Šablono komentarus galite rasti [„readme.md”](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) faile.