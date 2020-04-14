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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172719"
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

## <a name="self-reference-failures-during-initial-synchronization"></a>Nuorodos klaidos pradinio sinchronizavimo metu

Jeigu bet kurie jūsų susiejimų turi savo pačių nuorodų, galite gauti klaidos pranešimą, panašų į šį pavyzdį:

*Tiekėjo V2 klaida: įrašo ID: naujas įrašas, ErrorMessage: nepavyko išspręsti lauko guid: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Peržvalgos vertė nerasta. CN-001. Naudodami šį (šiuos) URL patikrinkite, ar yra nuorodos duomenys: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*

Šio tipo klaida įvyksta atliekant susiejimų, kuriuose yra savo pačių nuorodų, pradinį sinchronizavimą. Ankstesniame pavyzdyje sąskaitos faktūros laukas nurodo tiekėjo objektą.

Jei norite išspręsti šią problemą, galbūt turėsite vykdyti susiejimą du kartus, kol pradinis sinchronizavimas bus atliktas sėkmingai.

