---
title: Trikčių šalinimas pradinio sinchronizavimo metu
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, kurios gali kilti pradinio sinchronizavimo metu.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 030e565ffff561f6c1efbdd0de9928f70c7c46c0
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063063"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Trikčių šalinimas pradinio sinchronizavimo metu

[!include [banner](../../includes/banner.md)]



Šioje temoje pateikiama trikčių šalinimo informacija apie dvigubo rašymo integravimą tarp „Finance and Operations“ programų ir Dataverse. Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, kurios gali kilti pradinio sinchronizavimo metu.

> [!IMPORTANT]
> Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Patikrinkite, ar nėra pradinių sinchronizavimo klaidų programoje „Finance and Operations“.

Įgalinus susiejimo šablonus, schemų būsena turi būti **Vykdoma**. Jei būsena yra **Nevykdoma**, pradinio sinchronizavimo metu įvyko klaidų. Norėdami peržiūrėti klaidas, pasirinkite skirtuką **Pradinio sinchronizavimo informacija** puslapyje **Dvigubas rašymas**.

![Pradinio sinchronizavimo informacijos skirtuko klaida.](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Negalite užbaigti pradinio sinchronizavimo: 400 netinkama užklausa

**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius

Kai bandote vykdyti susiejimą ir pradinį sinchronizavimą, galite gauti tokį klaidos pranešimą:

*(\[Netinkama užklausa\], nuotolinis serveris pateikė klaidą: (400) netinkam užklausa.), AX eksportavimo funkcijoje atsirado klaida.*

Čia pateikiamas viso klaidos pranešimo pavyzdys.

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

Jei šį klaida įvyksta nuolat ir negalite užbaigti pradinio sinchronizavimo, atlikite šiuos veiksmus, kad išspręstumėte problemą.

1. Prisijunkite prie „Finance and Operations“ programėlės virtualios mašinos (VM).
2. Atidarykite „Microsoft“ valdymo konsolę.
3. Eidami į sritį **Paslaugos**, įsitikinkite, kad veikia „Microsoft Dynamics 365” duomenų importavimo / eksportavimo sistemos paslauga. Jeigu ji buvo sustabdyta, paleiskite ją iš naujo, nes ji yra reikalinga pradiniam sinchronizavimui atlikti.

## <a name="initial-synchronization-error-403-forbidden"></a>Pradinio sinchronizavimo klaida: 403 draudžiama

Pradinio sinchronizavimo metu galite gauti tokį klaidos pranešimą:

*\[Draudžiama\], nuotolinis serveris pateikė klaidą: (403 draudžiama), AX eksportavimo funkcija susidūrė su klaida*

Norėdami ištaisyti klaidą, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie programėlės „Finance and Operations“.
2. Puslapyje **„Azure Active Directory” programos** panaikinkite klientą **DtAppID** ir vėl jį pridėkite.

![DtAppID klientas „Azure AD” programų sąraše.](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Nepavykusi auto-nuoroda arba ciklinių nuorodų klaidos pradinio sinchronizavimo metu

Jeigu bet kurie iš jūsų susiejimų turi nuorodų į save ar ciklinių nuorodų, galite gauti klaidos pranešimų. Klaidos skirstomos į toliau pateiktas kategorijas.

- [Klaidos Tiekėjuose V2–to–msdyn_tiekėjai lentelės susiejimas](#error-vendor-map)
- [Klaidos Klientuose V3–to–Paskyros lentelės susiejimas](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>Išspręsti problemas Tiekėjuose V2–to–msdyn_tiekėjai lentelės susiejimas

Gali atsirasti pradinės sinchronizacijos klaidų susiejant **Tiekėjai V2** su **msdyn\_tiekėjai**, jei lentelės turi egzistuojančių eilučių, kai yra verčių **PirminioKontaktinioAsmensId** ir **SąskaitosFaktūrosTiekėjoPaskyrosNumeris** stulpeliuose. Šios klaidos atsiranda, nes **SąskaitosFaktūrosTiekėjoPaskyrosNumeris** yra nuorodos į save stulpelis, o **PirminioKontaktinioAsmensId** yra ciklinė nuoroda tiekėjo susiejime.

Gauti klaidos pranešimai bus šios formos.

*Nepavyko išspręsti lauko GUID: \<field\>. Peržvalga nerasta: \<value\>. Pabandykite šį (-iuos) URL adresą (-us), kad patikrintumėte, ar yra nuorodos duomenys: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Štai keletas pavyzdžių:

- *Nepavyko išspręsti lauko GUID: msdyn\_tiekėjopirminiskontaktinisasmuo.msdyn\_kontaktinioasmensid. Peržvalga nerasta: 000056. Pabandykite šį (-iuos) URL adresą (-us), kad patikrintumėte, ar egzistuoja nuorodos duomenys: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Nepavyko išspręsti lauko GUID: msdyn\_sąskaitosfaktūrostiekėjopaskyrosnumeris.msdyn\_tiekėjopaskyrosnumeris. Peržvalga nerasta: V24-1. Pabandykite šį (-iuos) URL adresą (-us), kad patikrintumėte, ar egzistuoja nuorodos duomenys: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Jei eilutės tiekėjo lentelėje turi verčių **PirminioKontaktinioAsmensId** ir **SąskaitosFaktūrosTiekėjoPaskyrosNumeris** stulpeliuose, vykdykite šiuos žingsnius, kad užbaigtumėte pradinį sinchronizavimą.

1. Programoje „Finance and Operations“ ištrinkite **PrimaryContactPersonId** ir **InvoiceVendorAccountNumber** stulpelius iš atvaizdavimo, tada išsaugokite atvaizdavimą.

    1. Dvigubo rašymo atvaizdavimo puslapyje, skirtame **Pardavėjai V2 (msdyn\_ pardavėjai)**, ant **Lentelių žemėlapiai** skirtuke kairiajame filtre pasirinkite **Finansų ir operacijų programos. Pardavėjai V2**. Dešiniajame filtre pasirinkite **Pardavimai.Tiekėjas**.
    2. Paieškoje įveskite **pirminis kontaktinis asmuo** tam, kad surastumėte **PirminioKontaktinioAsmensId** šaltinio stulpelį.
    3. Pasirinkite **Veiksmai** ir pasirinkite **Naikinti**.

        ![PirminioKontaktinioAsmensId stulpelio naikinimas.](media/vend_selfref3.png)

    4. Pakartokite šiuos veiksmus, kad panaikintumėte **SąskaitosFaktūrosTiekėjoPaskyrosNumeris** stulpelį.

        ![SąskaitosFaktūrosTiekėjoPaskyrosNumerio stulpelio naikinimas.](media/vend-selfref4.png)

    5. Įrašykite savo pakeitimus susiejime.

2. Išjunkite **Tiekėjai V2** lentelės keitimų sekimą.

    1. **Duomenų valdymas** darbo srityje pasirinkite **Duomenų lentelės** plytelę.
    2. Pasirinkite **Tiekėjai V2** lentelę.
    3. Veiksmų srityje pasirinkite **Parinktys**, tada – **Keitimų sekimas**.

        ![Keitimų sekimo parinkties pasirinkimas.](media/selfref_options.png)

    4. Pasirinkite **Išjungti keitimų sekimą**.

        ![Išjungti keitimų sekimą pasirinkimas.](media/selfref_tracking.png)

3. Paleiskite pradinę sinchronizaciją, skirtą **Tiekėjai V2 (msdyn\_tiekėjai)** siejimui. Pradinė sinchronizacija turėtų pavykti sėkmingai be klaidų.
4. Paleiskite pradinę **CDS Kontaktai V2 (kontaktai)** susiejimo sinchronizaciją. Turite sinchronizuoti šį susiejimą, jei norite sinchronizuoti pirminių kontaktų stulpelį tiekėjų lentelėje, nes taip pat turite atlikti kontaktų eilučių sinchronizavimą.
5. Pridėkite **PirminioKontaktinioAsmensId** ir **SąskaitosFaktūrosTiekėjoPaskyrosNumeris** stulpelius vėl į **Tiekėjai V2 (msdyn\_tiekėjai)** susiejimą ir tada jį įrašykite.
6. Vėl paleiskite pradinę sinchronizaciją, skirtą **Tiekėjai V2 (msdyn\_tiekėjai)** susiejimui. Kadangi keitimų sekimas išjungtas, visos eilutės bus sinchronizuotos.
7. Vėl įjunkite **Tiekėjai V2** lentelės keitimų sekimą.

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a>„Klientai V3 į Paskyras lentelės susiejimą” klaidų šalinimas

Gali atsirasti pradinės sinchronizacijos klaidų susiejant **Klientai V3** su **Paskyros**, jei lentelėse yra eilučių, kuriose yra verčių **KontaktinioAsmensID** ir **SąskaitosFaktūrosPaskyra** stulpeliuose. Šios klaidos atsiranda, nes **SąskaitosFaktūrosPaskyra** yra nuorodos į save stulpelis, o **KontaktinioAsmensID** yra ciklinė nuoroda tiekėjo susiejime.

Gauti klaidos pranešimai bus šios formos.

*Nepavyko išspręsti lauko GUID: \<field\>. Peržvalga nerasta: \<value\>. Pabandykite šį (-iuos) URL adresą (-us), kad patikrintumėte, ar yra nuorodos duomenys: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Štai keletas pavyzdžių:

- *Nepavyko išspręsti lauko GUID: pirminiokontaktoid.msdyn\_kontaktinioasmensid. Peržvalga nerasta: 000056. Pabandykite šį (-iuos) URL adresą (-us), kad patikrintumėte, ar egzistuoja nuorodos duomenys: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Nepavyko išspręsti lauko GUID: msdyn\_atsiskaitymopaskyra.paskyrosnumeris. Peržvalga nerasta: 1206-1. Pabandykite šį (-iuos) URL adresą (-us), kad patikrintumėte, ar egzistuoja nuorodos duomenys: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Jei eilutės kliento lentelėje turi verčių **KontaktinioAsmensId** ir **SąskaitosFaktūrosPaskyra** stulpeliuose, atlikite šiuos veiksmus, kad užbaigtumėte pradinį sinchronizavimą. Galite naudoti šį metodą bet kurioms paruoštoms eilutėms, pvz., **Paskyros** ir **Kontaktai**.

1. Programoje „Finance and Operations“ ištrinkite **Kontaktinio asmens ID** ir **InvoiceAccount** stulpeliai iš **Klientai V3 (paskyros)** atvaizdavimą, tada išsaugokite atvaizdą.

    1. Dvigubo rašymo atvaizdavimo puslapyje, skirtame **Klientai V3 (paskyros)**, ant **Lentelių žemėlapiai** skirtuke kairiajame filtre pasirinkite **Finansų ir operacijų programa. Klientai V3**. Dešiniajame filtre pasirinkite **Dataverse.Paskyra**.
    2. Paieškoje įveskite **kontaktinis asmuo**, kad surastumėte **KontaktinioAsmensID** šaltinio stulpelį.
    3. Pasirinkite **Veiksmai** ir pasirinkite **Naikinti**.

        ![„KontaktinioAsmensID” stulpelio naikinimas.](media/cust_selfref3.png)

    4. Pakartokite šiuos veiksmus, kad panaikintumėte **„SąskaitosFaktūrosPaskyra”** stulpelį.

        ![„SąskaitosFaktūrosPaskyros” stulpelio naikinimas.](media/cust_selfref4.png)

    5. Įrašykite savo pakeitimus susiejime.

2. Išjunkite **Klientai V3** lentelės keitimų sekimą.

    1. **Duomenų valdymas** darbo srityje pasirinkite **Duomenų lentelės** plytelę.
    2. Pasirinkite **Klientai V3** lentelę.
    3. Veiksmų srityje pasirinkite **Parinktys**, tada – **Keitimų sekimas**.

        ![Keitimų sekimo parinkties pasirinkimas.](media/selfref_options.png)

    4. Pasirinkite **Išjungti keitimų sekimą**.

        ![Išjungti keitimų sekimą pasirinkimas.](media/selfref_tracking.png)

3. Paleiskite pradinę **Klientai V3 (Paskyros)** susiejimo sinchronizaciją. Pradinė sinchronizacija turėtų pavykti sėkmingai be klaidų.
4. Paleiskite pradinę **CDS Kontaktai V2 (kontaktai)** susiejimo sinchronizaciją.

    > [!NOTE]
    > Yra du tokiu pačiu pavadinimu žemėlapiai. Būtinai pasirinkite žemėlapį, turintį tokį aprašą **Išsami informacija** skirtuke: **Dvigubo rašymo šablonas, skirto FO.CDS Tiekėjo Kontaktai V2 su to CDS.Kontaktai sinchronizacijai atlikti. Reikalingas naujas paketas \[Dynamics365PraplėstaTiekimoGrandinė\].**

5. Pridėkite **„SąskaitosFaktūrosPaskyra”** ir **„KontaktinioAsmensId”** stulpelius vėl į **Klientai V3 (Paskyros)** susiejimą ir tada įrašykite jį. Abu **„SąskaitosFaktūrosPaskyra”** ir **„KontaktinioAsmensId”** stulpeliai dabar įtraukti į tiesioginio sinchronizavimo režimą. Kitame veiksme atliksite šių stulpelių sinchronizavimą.
6. Vėl paleiskite pradinę **Klientai V3 (Paskyros)** susiejimo sinchronizaciją. Kadangi pakeitimų sekimas išjungtas, duomenys už **InvoiceAccount** ir **Kontaktinio asmens ID** bus sinchronizuojamas iš programos „Finance and Operations“ į Dataverse.
7. Norėdami sinchronizuoti duomenis **InvoiceAccount** ir **Kontaktinio asmens ID** iš Dataverse į programą „Finance and Operations“, turite naudoti duomenų integravimo projektą.

    1. Į Power Apps, sukurkite duomenų integravimo projektą tarp **Pardavimai.Sąskaita** ir **Finansų ir operacijų programos. Klientai V3** lenteles. Duomenų kryptis turi būti iš Dataverse į programą „Finance and Operations“. Kadangi **SąskaitosFaktūrosPaskyra** yra naujas atributas dvigubo rašymo funkcijoje, galite praleisti jos pradinę sinchronizaciją. Prireikus daugiau informacijos, žr. [Duomenų integravimas į Dataverse](/power-platform/admin/data-integrator).

        Toliau pateiktame paveikslėlyje parodytas projektas, kuris atnaujina **KlientoPaskyra** ir **KontaktinioAsmensId**.

        ![Duomenų integravimo projektas, skirtas Kliento paskyrai ir KontaktinioAsmensId atnaujinti.](media/cust_selfref6.png)

    2. Pridėkite įmonės kriterijus į filtrą Dataverse pusėje, kad programėlėje „Finance and Operations“ būtų atnaujintos tik filtro kriterijus atitinkančios eilutės. Norėdami pridėti filtrą, pažymėkite filtro mygtuką. Tada **Redaguoti užklausą** dialogo lange galite pridėti filtro užklausą, pavyzdžiui, **\_msdyn\_įmonė\_vertės lyg. '\<guid\>'**.

        > [PASTABA] Jei filtro mygtuko nėra, sukurkite palaikymo kvitą, kad paprašytumėte duomenų integravimo komandos įjungti filtro funkciją jūsų nuomotojui.

        Jei neįvesite filtro užklausos, skirtos **\_msdyn\_įmonės\_vertė**, visos eilutės bus sinchronizuotos.

        ![Filtro užklausos pridėjimas.](media/cust_selfref7.png)

    Pradinė eilučių sinchronizacija baigta.

8. Programoje „Finance and Operations“ vėl įjunkite pakeitimų stebėjimą **Klientai V3** stalo.

## <a name="initial-sync-failures-on-maps-with-more-than-10-lookup-fields"></a>Pradinio sinchronizavimo klaidos schemose su daugiau nei 10 peržvalgos laukų

Galite gauti toliau nurodytą klaidos pranešimą, kai bandote vykdyti pradinio sinchronizavimo klaidas susiejimuose **Klientai V3 – sąskaitos**, **Pardavimo užsakymai** arba bet kurioje schemoje su daugiau kaip 10 peržvalgos laukų.

*CRMExport: paketo vykdymas baigtas. Klaidos aprašas: 5 bandymai gauti duomenis iš https://xxxxx//datasets/yyyyy/tables/accounts/items?$select=accountnumber, address2_city, address2_country, ... (msdyn_company/cdm_companyid eq 'id')&$orderby=accountnumber asc nepavyko.*

Dėl užklausos peržvalgų apribojimo pradinis sinchronizavimas nepavyksta, kai objekto susiejime yra daugiau kaip 10 peržvalgų. Daugiau informacijos žr. [Susijusių lentelės įrašų gavimas naudojant užklausą](/powerapps/developer/common-data-service/webapi/retrieve-related-entities-query).

Norėdami ištaisyti šią problemą, vykdykite toliau nurodytus veiksmus.

1. Pašalinkite pasirinktinius peržvalgos laukus iš dvigubo rašymo objekto schemos, kad peržvalgų būtų 10 ar mažiau.
2. Įrašykite schemą ir atlikite pradinį sinchronizavimą.
3. Kai pirmo veiksmo pradinė sinchronizacija pavyks, pridėkite likusius peržvalgos laukus ir pašalinkite peržvalgos laukus, kuriuos sinchronizavote atlikdami pirmą veiksmą. Įsitikinkite, kad peržvalgos laukų yra 10 ar mažiau. Įrašykite schemą ir vykdykite pradinį sinchronizavimą.
4. Kartokite šiuos veiksmus, kol visi peržvalgos laukai bus sinchronizuoti.
5. Įtraukite visus peržvalgos laukus atgal į schemą, įrašykite schemą ir paleiskite schemą naudodami **Praleisti pradinį sinchronizavimą**.

Šiuo procesu įjungiamas schemos tiesioginis sinchronizavimo režimas.

## <a name="known-issue-during-initial-sync-of-party-postal-addresses-and-party-electronic-addresses"></a>Žinoma klaida, kylanti šalies pašto adresų ir šalies elektroninių adresų pradinio sinchronizavimo metu

Bandydami paleisti šalies pašto adresų ir šalies elektroninių adresų pradinį sinchronizavimą galite gauti toliau pateikiamą klaidos pranešimą.

*Programoje „Dataverse” šalies numerio rasti nepavyko.*

Yra nustatytas diapazonas **DirPartyCDSEntity** „Finance and Operations“ programose, kurios filtruoja tokio tipo šalis **Asmuo** ir **Organizacija**. Todėl susiejimo **CDS šalys – msdyn_parties** pradiniu sinchronizavimu nebus sinchronizuotos kito tipo šalys, įskaitant šalis, kurių tipas **Juridinis objektas** ir **Valdymo vienetas**. Paleidus **CDS šalies pašto adresai (msdyn_partypostaladdresses)** arba **Šalies kontaktai V3 (msdyn_partyelectronicaddresses)** pradinį sinchronizavimą, gali būti pateikta klaida.

Stengiamės pataisyti, kad pašalintume subjekto „Finance and Operations“ partijų tipų diapazoną, kad visų tipų šalys galėtų sinchronizuoti Dataverse sėkmingai.

## <a name="are-there-any-performance-issues-while-running-initial-sync-for-customers-or-contacts-data"></a>Ar vykdant klientų ir kontaktų duomenų pradinį sinchronizavimą kyla našumo problemų?

Jei paleidote **klientų** duomenų pradinį sinchronizavimą ir **klientų** schemos yra vykdomos, o tada paleidžiate **kontaktų** duomenų pradinį sinchronizavimą, gali kilti našumo problemų atliekant įterpimų ir atnaujinimų **kontaktų** adresų lentelėse **LogisticsPostalAddress** ir **LogisticsElectronicAddress**. Tose pačiose iš visų įmonių pasiekiamose pašto adresų ir elektroninių adresų lentelėse sekamos **CustCustomerV3Entity** ir **VendVendorV2Entity**, o dvigubo rašymo funkcija stengiasi sukurti daugiau užklausų, kad duomenys būtų rašomi kitoje pusėje. Jei jau įvykdėte **klientų** pradinį sinchronizavimą, vykdydami **kontaktų** duomenų pradinį sinchronizavimą, sustabdykite atitinkamą schemą. Padarykite tą patį su **tiekėjo** duomenimis. Kai pradinis sinchronizavimas baigtas, galite paleisti visas schemas praleisdami pradinį sinchronizavimą.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
