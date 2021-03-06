---
title: Trikčių šalinimas pradinio sinchronizavimo metu
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, kurios gali kilti pradinio sinchronizavimo metu.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 709a3c332bb6d086910b257fee9cdec8d2bc81a2
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941060"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Trikčių šalinimas pradinio sinchronizavimo metu

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Dataverse“ programų trikčių šalinimo informacija. Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, kurios gali kilti pradinio sinchronizavimo metu.

> [!IMPORTANT]
> Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Patikrinkite, ar nėra pradinio sinchronizavimo klaidų „Finance and Operations” programoje

Įgalinus susiejimo šablonus, schemų būsena turi būti **Vykdoma**. Jei būsena yra **Nevykdoma**, pradinio sinchronizavimo metu įvyko klaidų. Norėdami peržiūrėti klaidas, pasirinkite skirtuką **Pradinio sinchronizavimo informacija** puslapyje **Dvigubas rašymas**.

![Pradinio sinchronizavimo informacijos skirtuko klaida](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Negalite užbaigti pradinio sinchronizavimo: 400 netinkama užklausa

**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius

Kai bandote vykdyti susiejimą ir pradinį sinchronizavimą, galite gauti tokį klaidos pranešimą:

*(\[Netinkama užklausa\], nuotolinis serveris grąžino klaidą: (400) netinkam užklausa.), AX eksportavimo funkcijoje atsirado klaida*

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

1. Prisijunkite prie „Finance and Operations” programos virtualiosios mašinos.
2. Atidarykite „Microsoft“ valdymo konsolę.
3. Eidami į sritį **Paslaugos**, įsitikinkite, kad veikia „Microsoft Dynamics 365” duomenų importavimo / eksportavimo sistemos paslauga. Jeigu ji buvo sustabdyta, paleiskite ją iš naujo, nes ji yra reikalinga pradiniam sinchronizavimui atlikti.

## <a name="initial-synchronization-error-403-forbidden"></a>Pradinio sinchronizavimo klaida: 403 draudžiama

Pradinio sinchronizavimo metu galite gauti tokį klaidos pranešimą:

*\[Draudžiama\], nuotolinis serveris pateikė klaidą: (403 draudžiama), AX eksportavimo funkcija susidūrė su klaida*

Norėdami ištaisyti klaidą, atlikite toliau nurodytus veiksmus.

1. Prisijungimas prie „Finance and Operations” programos.
2. Puslapyje **„Azure Active Directory” programos** panaikinkite klientą **DtAppID** ir vėl jį pridėkite.

![DtAppID klientas „Azure AD” programų sąraše](media/aad_applications.png)

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

1. „Finance and Operations” programoje panaikinkite **PirminioKontaktinioAsmensId** ir **SąskaitosFaktūrosTiekėjoPaskyrosNumeris** stulpelius iš susiejimo ir tada jį įrašykite.

    1. Dvigubo rašymo susiejimo puslapyje **Tiekėjai V2 (msdyn\_tiekėjai)**, **Lentelės susiejimai** skirtuke, kairiajame filtre pasirinkite **„Finance and Operations” programos.Tiekėjai V2**. Dešiniajame filtre pasirinkite **Pardavimai.Tiekėjas**.
    2. Paieškoje įveskite **pirminis kontaktinis asmuo** tam, kad surastumėte **PirminioKontaktinioAsmensId** šaltinio stulpelį.
    3. Pasirinkite **Veiksmai** ir pasirinkite **Naikinti**.

        ![PirminioKontaktinioAsmensId stulpelio naikinimas](media/vend_selfref3.png)

    4. Pakartokite šiuos veiksmus, kad panaikintumėte **SąskaitosFaktūrosTiekėjoPaskyrosNumeris** stulpelį.

        ![SąskaitosFaktūrosTiekėjoPaskyrosNumerio stulpelio naikinimas](media/vend-selfref4.png)

    5. Įrašykite savo pakeitimus susiejime.

2. Išjunkite **Tiekėjai V2** lentelės keitimų sekimą.

    1. **Duomenų valdymas** darbo srityje pasirinkite **Duomenų lentelės** plytelę.
    2. Pasirinkite **Tiekėjai V2** lentelę.
    3. Veiksmų srityje pasirinkite **Parinktys**, tada – **Keitimų sekimas**.

        ![Keitimų sekimo parinkties pasirinkimas](media/selfref_options.png)

    4. Pasirinkite **Išjungti keitimų sekimą**.

        ![Išjungti keitimų sekimą pasirinkimas](media/selfref_tracking.png)

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

1. „Finance and Operations“ programoje panaikinkite laukus **KontaktinioAsmensID** ir **SąskaitosFaktūrosPaskyra** stulpelius iš **Klientai V3 (paskyros)** susiejimo ir tada jį įrašykite.

    1. Dvigubo rašymo susiejimo puslapyje, skirtame **Klientai V3 (paskyros)** **Lentelių susiejimai** skirtuke kairiajame filtre pasirinkite **Finance and Operations programa.Klientai V3**. Dešiniajame filtre pasirinkite **Dataverse.Paskyra**.
    2. Paieškoje įveskite **kontaktinis asmuo**, kad surastumėte **KontaktinioAsmensID** šaltinio stulpelį.
    3. Pasirinkite **Veiksmai** ir pasirinkite **Naikinti**.

        ![„KontaktinioAsmensID” stulpelio naikinimas](media/cust_selfref3.png)

    4. Pakartokite šiuos veiksmus, kad panaikintumėte **„SąskaitosFaktūrosPaskyra”** stulpelį.

        ![„SąskaitosFaktūrosPaskyros” stulpelio naikinimas](media/cust_selfref4.png)

    5. Įrašykite savo pakeitimus susiejime.

2. Išjunkite **Klientai V3** lentelės keitimų sekimą.

    1. **Duomenų valdymas** darbo srityje pasirinkite **Duomenų lentelės** plytelę.
    2. Pasirinkite **Klientai V3** lentelę.
    3. Veiksmų srityje pasirinkite **Parinktys**, tada – **Keitimų sekimas**.

        ![Keitimų sekimo parinkties pasirinkimas](media/selfref_options.png)

    4. Pasirinkite **Išjungti keitimų sekimą**.

        ![Išjungti keitimų sekimą pasirinkimas](media/selfref_tracking.png)

3. Paleiskite pradinę **Klientai V3 (Paskyros)** susiejimo sinchronizaciją. Pradinė sinchronizacija turėtų pavykti sėkmingai be klaidų.
4. Paleiskite pradinę **CDS Kontaktai V2 (kontaktai)** susiejimo sinchronizaciją.

    > [!NOTE]
    > Yra du tokiu pačiu pavadinimu žemėlapiai. Būtinai pasirinkite žemėlapį, turintį tokį aprašą **Išsami informacija** skirtuke: **Dvigubo rašymo šablonas, skirto FO.CDS Tiekėjo Kontaktai V2 su to CDS.Kontaktai sinchronizacijai atlikti. Reikalingas naujas paketas \[Dynamics365PraplėstaTiekimoGrandinė\].**

5. Pridėkite **„SąskaitosFaktūrosPaskyra”** ir **„KontaktinioAsmensId”** stulpelius vėl į **Klientai V3 (Paskyros)** susiejimą ir tada įrašykite jį. Abu **„SąskaitosFaktūrosPaskyra”** ir **„KontaktinioAsmensId”** stulpeliai dabar įtraukti į tiesioginio sinchronizavimo režimą. Kitame veiksme atliksite šių stulpelių sinchronizavimą.
6. Vėl paleiskite pradinę **Klientai V3 (Paskyros)** susiejimo sinchronizaciją. Kadangi keitimų sekimas yra išjungtas, **SąskaitosFaktūrosPaskyra** ir **KontaktinioAsmensId** duomenys iš „Finance and Operations“ programos į „Dataverse“ bus sinchronizuoti.
7. Norėdami sinchronizuoti **SąskaitosFaktūrosPaskyra** ir **KontaktinioAsmensId** duomenis iš „Dataverse“ į „Finance and Operations“ programą, turite naudoti duomenų integravimo projektą.

    1. „Power Apps“ sukurkite duomenų integravimo projektą tarp **Pardavimai.Paskyra** ir **Finance and Operations programos.Klientai V3** lentelių. Duomenų kryptis turi būti iš „Dataverse“ į „Finance and Operations“ programą. Kadangi **SąskaitosFaktūrosPaskyra** yra naujas atributas dvigubo rašymo funkcijoje, galite praleisti jos pradinę sinchronizaciją. Prireikus daugiau informacijos, žr. [Duomenų integravimas į Dataverse](/power-platform/admin/data-integrator).

        Toliau pateiktame paveikslėlyje parodytas projektas, kuris atnaujina **KlientoPaskyra** ir **KontaktinioAsmensId**.

        ![Duomenų integravimo projektas, skirtas Kliento paskyrai ir KontaktinioAsmensId atnaujinti](media/cust_selfref6.png)

    2. Pridėkite įmonės kriterijus į filtrą, esantį „Dataverse“, kad tik eilutės, atitinkančios filtro kriterijus, būtų atnaujintos „Finance and Operations“ programoje. Norėdami pridėti filtrą, pažymėkite filtro mygtuką. Tada **Redaguoti užklausą** dialogo lange galite pridėti filtro užklausą, pavyzdžiui, **\_msdyn\_įmonė\_vertės lyg. '\<guid\>'**. 

        > [PASTABA] Jei filtro mygtuko nėra, sukurkite palaikymo kvitą, kad paprašytumėte duomenų integravimo komandos įjungti filtro funkciją jūsų nuomotojui.

        Jei neįvesite filtro užklausos, skirtos **\_msdyn\_įmonės\_vertė**, visos eilutės bus sinchronizuotos.

        ![Filtro užklausos pridėjimas](media/cust_selfref7.png)

    Pradinė eilučių sinchronizacija baigta.

8. „Finance and Operations” programoje vėl įjunkite **Klientai V3** lentelės keitimų sekimą.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]