---
title: Trikčių šalinimas pradinio sinchronizavimo metu
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, kurios gali kilti pradinio sinchronizavimo metu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410086"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Trikčių šalinimas pradinio sinchronizavimo metu

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų trikčių šalinimo informacija. Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, kurios gali kilti pradinio sinchronizavimo metu.

> [!IMPORTANT]
> Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Patikrinkite, ar nėra pradinio sinchronizavimo klaidų „Finance and Operations” programoje

Įgalinus susiejimo šablonus, schemų būsena turi būti **Vykdoma**. Jei būsena yra **Nevykdoma**, pradinio sinchronizavimo metu įvyko klaidų. Norėdami peržiūrėti klaidas, pasirinkite skirtuką **Pradinio sinchronizavimo informacija** puslapyje **Dvigubas rašymas**.

![Pradinio sinchronizavimo informacijos skirtukas](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Negalite užbaigti pradinio sinchronizavimo: 400 netinkama užklausa

**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius

Kai bandote vykdyti susiejimą ir pradinį sinchronizavimą, galite gauti tokį klaidos pranešimą:

*Nuotolinis serveris pateikė klaidą: (400 netinkama užklausa), AX eksportavimo funkcija susidūrė su klaida*

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

![„Azure AD” programų sąrašas](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Nuorodų į save arba ciklinių nuorodų klaidos pradinio sinchronizavimo metu

Jeigu bet kurie iš jūsų susiejimų turi nuorodų į save ar ciklinių nuorodų, galite gauti klaidos pranešimų. Klaidos skirstomos į toliau pateiktas kategorijas.

- [Objektų „Tiekėjai V2“ ir „msdyn_vendors“ susiejimas](#error-vendor-map)
- [Objektų „Klientai V3“ ir „Paskyros“ susiejimas](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>Objektų „Tiekėjai V2ׅ“ ir „msdyn_vendors“ susiejimo klaidos šalinimas

Atlikdami **Tiekėjai V2** susiejimą su **msdyn_vendors** gali kilti toliau pateiktų pradinio sinchronizavimo klaidų, jei objektai turi esamų įrašų su vertėmis laukuose **PrimaryContactPersonId** ir **InvoiceVendorAccountNumber**. Taip yra todėl, kad susiejant tiekėją **InvoiceVendorAccountNumber** yra nuorodos į save laukas, o **PrimaryContactPersonId** yra ciklinė nuoroda.

*Nepavyko išspręsti lauko guid: <field>. Peržvalga nerasta: <value>. Naudodami šį (šiuos) URL patikrinkite, ar yra nuorodos duomenys: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

Štai keletas pavyzdžių:

- *Nepavyko išspręsti lauko guid: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Peržvalga nerasta: 000056. Naudodami šį (šiuos) URL patikrinkite, ar yra nuorodos duomenys: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Nepavyko išspręsti lauko guid: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Peržvalga nerasta: V24-1. Naudodami šį (šiuos) URL patikrinkite, ar yra nuorodos duomenys: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*

Jei jūs tiekėjo objekte turite įrašų su vertėmis šiuose laukuose, vadovaukitės tolesniame skyriuje pateiktais veiksmais, kad sėkmingai atliktumėte pradinį sinchronizavimą.

1. Finance and Operations programoje panaikinkite laukus **PrimaryContactPersonId** ir **InvoiceVendorAccountNumber** iš susiejimo ir įrašykite pakeitimus.

    1. Pereikite į **Tiekėjai V2 (msdyn_vendors)** dvigubo rašymo susiejimo puslapį ir pasirinkite skirtuką **Objektų susiejimai**. Kairiajame filtre pasirinkite **Finance and Operations programos.Tiekėjai V2**. Dešiniajame filtre pasirinkite **Pardavimai.Tiekėjas**.

    2. Paieškoje įveskite **primarycontactperson**, kad surastumėte šaltinio lauką **PrimaryContactPersonId**.
    
    3. Spustelėkite mygtuką **Veiksmai** ir pasirinkite **Naikinti**.
    
        ![nuoroda į save ar ciklinė nuoroda 3](media/vend_selfref3.png)
    
    4. Pakartokite veiksmus, kad panaikintumėte lauką **InvoiceVendorAccountNumber**.
    
        ![nuoroda į save ar ciklinė nuoroda 4](media/vend-selfref4.png)
    
    5. Įrašykite susiejimo pakeitimus.

2. Išjunkite objekto **Tiekėjai V2** keitimų sekimą.

    1. Eikite į **Duomenų valdymas \> Duomenų objektai**.
    
    2. Pasirinkite objektą **Tiekėjai V2**.
    
    3. Meniu juostoje spustelėkite **Parinktys**, tada – **Keisti sekimą**.
    
        ![nuoroda į save ar ciklinė nuoroda 5](media/selfref_options.png)
    
    4. Spustelėkite **Išjungti keitimų sekimą**.
    
        ![nuoroda į save ar ciklinė nuoroda 6](media/selfref_tracking.png)

3. Paleiskite pradinį **Tiekėjai V2 (msdyn_vendors)** susiejimo sinchronizavimą. Pradinis sinchronizavimas turėtų būtį įvykdytas sėkmingai ir be klaidų.

4. Paleiskite pradinį **CDS Kontaktai V2 (kontaktai)** susiejimo sinchronizavimą. Turite sinchronizuoti šį susiejimą, jei norite sinchronizuoti tiekėjų objekto pagrindinio kontakto lauką, nes kontaktų įrašams taip pat turi būti atliekamas pradinis sinchronizavimas.

5. Įtraukite laukus **PrimaryContactPersonId** ir **InvoiceVendorAccountNumber** atgal į **Tiekėjai V2 (msdyn_vendors)** susiejimą ir įrašykite jį.

6. Dar kartą paleiskite pradinį **Tiekėjai V2 (msdyn_vendors)** susiejimo sinchronizavimą. Visi įrašai bus sinchronizuoti, nes keitimų sekimas yra išjungtas.

7. Įjunkite objekto **Tiekėjai V2** keitimų sekimą.

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a>Objektų „Klientai V3“ ir „Paskyros“ susiejimo klaidų šalinimas

Atlikdami **Klientai V3** susiejimą su **Paskyros** gali kilti toliau pateiktų pradinio sinchronizavimo klaidų, jei objektai turi įrašų su vertėmis laukuose **ContactPersonID** ir **InvoiceAccount**. Taip yra todėl, kad susiejant tiekėją **InvoiceAccount** yra nuorodos į save laukas, o **ContactPersonID** yra ciklinė nuoroda.

*Nepavyko išspręsti lauko guid: <field>. Peržvalga nerasta: <value>. Naudodami šį (šiuos) URL patikrinkite, ar yra nuorodos duomenys: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

- *Nepavyko išspręsti lauko guid: primarycontactid.msdyn_contactpersonid. Peržvalga nerasta: 000056. Naudodami šį (šiuos) URL patikrinkite, ar yra nuorodos duomenys: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Nepavyko išspręsti lauko guid: msdyn_billingaccount.accountnumber. Peržvalga nerasta: 1206-1. Naudodami šį (šiuos) URL patikrinkite, ar yra nuorodos duomenys: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account$filter=accountnumber eq '1206-1'*

Jei jūs kliento objekte turite įrašų su vertėmis šiuose laukuose, vadovaukitės tolesniame skyriuje pateiktais veiksmais, kad sėkmingai atliktumėte pradinį sinchronizavimą. Galite naudoti šį metodą bet kuriems iš karto pasiekiamiems objektams, pvz., „Paskyros“ ir „Kontaktai“.

1. „Finance and Operations“ programoje panaikinkite laukus **ContactPersonID** ir **InvoiceAccount** iš **Klientai V3 (paskyros)** susiejimo ir įrašykite pakeitimus.

    1. Eikite į **Klientai V3 (paskyros)** dvigubo rašymo susiejimo puslapį ir pasirinkite skirtuką **Objektų susiejimai**. Kairiajame filtre pasirinkite **Finance and Operations programa.Tiekėjai V3**. Dešiniajame filtre pasirinkite **Common Data Service.Paskyra**.

    2. Paieškoje įveskite **contactperson**, kad surastumėte šaltinio lauką **ContactPersonID**.
    
    3. Spustelėkite mygtuką **Veiksmai** ir pasirinkite **Naikinti**.
    
        ![nuoroda į save ar ciklinė nuoroda 3](media/cust_selfref3.png)
    
    4. Pakartokite, kad panaikintumėte lauką **InvoiceAccount**.
    
        ![nuoroda į save ar ciklinė nuoroda](media/cust_selfref4.png)
    
    5. Įrašykite susiejimo pakeitimus.

2. Išjunkite objekto **Klientai V3** keitimų sekimą.

    1. Eikite į **Duomenų valdymas \> Duomenų objektai**.
    
    2. Pasirinkite objektą **Klientai V3**.
    
    3. Meniu juostoje spustelėkite **Parinktys**, tada – **Keisti sekimą**.
    
        ![nuoroda į save ar ciklinė nuoroda 5](media/selfref_options.png)
    
    4. Spustelėkite **Išjungti keitimų sekimą**.
    
        ![nuoroda į save ar ciklinė nuoroda 6](media/selfref_tracking.png)

3. Paleiskite pradinį **Klientai V3 (Paskyros)** susiejimo sinchronizavimą. Pradinis sinchronizavimas turėtų būtį įvykdytas sėkmingai ir be klaidų.

4. Paleiskite pradinį **CDS Kontaktai V2 (kontaktai)** susiejimo sinchronizavimą. Yra 2 schemos su tuo pačiu pavadinimu. Pasirinkite tą, kurios aprašymas yra **Dvigubo rašymo šablonas, skirtas sinchronizuoti FO.CDS Tiekėjo kontaktai V2 su CDS.Kontaktai. Reikalingas naujas paketas \[Dynamics365SupplyChainExtended\] .** schemos skirtuke **Išsami informacija**.

5. Įtraukite laukus **InvoiceAccount** ir **ContactPersonId** atgal į **Klientai V3 (Paskyros)** susiejimą ir įrašykite jį. Dabar laukai **InvoiceAccount** ir **ContactPersonId** vėl įtraukti į tiesioginio sinchronizavimo režimą. Kitame veiksme užbaigiate pradinį šių laukų sinchronizavimą.

6. Vėl paleiskite pradinį **Klientai V3 (Paskyros)** susiejimo sinchronizavimą. Kadangi keitimų sekimas yra išjungtas, paleidus sinchronizavimą bus sinchronizuoti **InvoiceAccount** ir **ContactPersonId** duomenys iš „Finance and Operations“ programos į „Common Data Service“.

7. Norėdami sinchronizuoti **InvoiceAccount** ir **ContactPersonId** duomenis iš „Common Data Service“ į „Finance and Operations“, naudokite duomenų integravimo projektą.

    1. „Power Apps“ sukurkite duomenų integravimo projektą tarp **Pardavimai.Paskyra** ir **Finance and Operations programos.Klientai V3** objektų. Duomenų kryptis turi būti iš „Common Data Service“ į „Finance and Operations“ programą.  Kadangi **InvoiceAccount** yra naujas atributas dvigubo rašymo funkcijoje, rekomenduojama praleisti pradinį šio atributo sinchronizavimą. Prireikus daugiau informacijos, žr. [Duomenų integravimas į Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).

        Toliau pateiktame paveikslėlyje parodytas projektas, kuris atnaujina **CustomerAccount** ir **ContactPersonId**.

        ![nuoroda į save ar ciklinė nuoroda](media/cust_selfref6.png)

    2. Įtraukite įmonės kriterijus į „Common Data Service“ filtrą, nes programoje „Finance and Operations“ bus atnaujinti tik tie įrašai, kurie atitinka filtro kriterijus. Norėdami įtraukti filtrą, spustelėkite filtro piktogramą. Dialogo lange **Redaguoti užklausą** galite įtraukti filtro užklausą, pvz., **_msdyn_company_value eq '\<guid\>'**. Jei filtro piktogramos nėra, sukurkite palaikymo kvitą, kad paprašytumėte duomenų integravimo komandos įjungti filtro funkciją jūsų nuomotojui. Jei neįvesite **_msdyn_company_value** filtro užklausos, visi įrašai bus sinchronizuoti.

        ![nuoroda į save ar ciklinė nuoroda](media/cust_selfref7.png)

        Tai yra pradinio įrašų sinchronizavimo pabaiga.

8. Įjunkite objekto **Klientai V3** keitimų sekimą „Finance and Operations“ programoje.

