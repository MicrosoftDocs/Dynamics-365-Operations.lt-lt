---
title: Tiesioginio sinchronizavimo trikčių šalinimas
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, susijusias su tiesioginiu sinchronizavimu.
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
ms.openlocfilehash: 60839bbd1b3ae642cdd419c7df2388292776a461
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172742"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Tiesioginio sinchronizavimo trikčių šalinimas

[!include [banner](../../includes/banner.md)]



Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų trikčių šalinimo informacija. Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, susijusias su tiesioginiu sinchronizavimu.

> [!IMPORTANT]
> Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>Tiesioginis sinchronizavimas pateikia klaidą „403 draudžiama“, kai kuriate įrašą „Finance and Operations” programoje

Kai „Finance and Operations” programoje kuriate įrašą, galite gauti tokį klaidos pranešimą:

*\[{\\"klaida\\":{\\"kodas\\":\\"0x80072560\\",\\"pranešimas\\":\\"Vartotojas nėra organizacijos narys.\\"}}\], Nuotolinis serveris pateikė klaidą: (403) draudžiama."}}".*

Norėdami išspręsti problemą, atlikite veiksmus, pateiktus skyriuje [Sistemos reikalavimai ir būtinosios sąlygos](requirements-and-prerequisites.md). Norėdami atlikti šiuos veiksmus, dvigubo rašymo programos vartotojai, sukurti „Common Data Service”, privalo turėti sistemos administratoriaus vaidmenį. Numatytoji komanda savininkė taip pat turi turėti sistemos administratoriaus vaidmenį.

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>Tiesioginis bet kokio objekto sinchronizavimas nuolat pateikia panašią klaidą, kai kuriate įrašą „Finance and Operations” programoje

**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius

Kaskart bandydami įrašyti objekto duomenis „Finance and Operations” programoje, galite gauti klaidos pranešimą, panašų į pateiktą toliau:

*Nepavyksta įrašyti duomenų bazės pakeitimų. Darbo vienetas negali įvykdyti operacijos. Nepavyksta įrašyti duomenų į objekto uoms. Įrašyti į UnitOfMeasureEntity nepavyko, nes nepavyko sinchronizuoti klaidos pranešimo su objekto uoms.*

Norėdami išspręsti problemą, turite įsitikinti, kad būtini nuorodos duomenys yra ir „Finance and Operations” programoje, ir „Common Data Service”. Pavyzdžiui, jei klientas, kuriame esate „Finance and Operations” programoje, priklauso konkrečiai klientų grupei, įsitikinkite, kad ši klientų grupė yra „Common Data Service”.

Jei duomenys yra abiejose programose ir patvirtinote, kad problema nėra susijusi su duomenimis, atlikite šiuos veiksmus:

1. Sustabdykite susijusį objektą.
2. Prisijunkite prie „Finance and Operations” programos ir įsitikinkite, kad neveikiančio objekto įrašai yra DualWriteProjectConfiguration ir DualWriteProjectFieldConfiguration lentelėse. Pavyzdžiui, čia vaizduojama, kaip atrodo užklausa, jei objektas **Klientai** neveikia.

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. Jei net jums sustabdžius objekto susiejimą, yra neveikiančio objekto įrašų, panaikinkite įrašus, susijusius su neveikiančiu objektu. Norėdami panaikinti įrašą, lentelėje DualWriteProjectConfiguration pasižymėkite stulpelį **projectname** ir lentelėje DualWriteProjectFieldConfiguration raskite įrašą naudodami projekto pavadinimą.
4. Pradėkite susiejimą su objektu. Patikrinkite, ar sinchronizuojant duomenis nekyla problemų.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Skaitymo arba rašymo teisių klaidų tvarkymas, kuriant duomenis „Finance and Operations” programoje

Kai kuriate duomenis „Finance and Operations” programoje, galite gauti klaidos pranešimą „Netinkama užklausa“, panašų į toliau pateiktą pavyzdį.

![Klaidos pranešimo „Netinkama užklausa“ pavyzdys](media/error_record_id_source.png)

Norėdami išspręsti šią problemą, turite priskirti tinkamą saugos vaidmenį susieto „Dynamics 365 Sales” arba „Dynamics 365 Customer Service” verslo struktūros vieneto komandai, kad įgalintumėte trūkstamą teisę.

1. „Finance and Operations” programoje raskite verslo struktūros vienetą, susietą duomenų integravimo ryšio rinkinyje.

    ![Organizacijos susiejimas](media/mapped_business_unit.png)

2. Prisijunkite prie aplinkos modeliu grįstoje „Dynamics 365” programoje, pereikite į **Parametras \> Sauga** ir raskite susieto verslo struktūros vieneto komandą.

    ![Susieto verslo struktūros vieneto komanda](media/setting_security_page.png)

3. Atidarykite komandos puslapį, kad jį redaguotumėte, tada pasirinkite **Tvarkyti vaidmenis**, kad atidarytumėte dialogo langą **Tvarkyti komandos vaidmenis**.

    ![Vaidmenų tvarkymo mygtukas](media/manage_team_roles.png)

4. Priskirkite vaidmenį, turintį skaitymo / rašymo teisę, skirtą atitinkamiems objektams, tada pasirinkite **Gerai**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a>Sinchronizavimo problemų aplinkoje, kurioje neseniai buvo pakeista „Common Data Service” aplinka, sprendimas

**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius

Kai „Finance and Operations” programoje kuriate duomenis, galite gauti tokį klaidos pranešimą:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Nepavyksta sugeneruoti mokamosios krovos objektui CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Nepavyko sukurti mokamosios krovos, įvyko klaida „Netinkamas URI“: URI yra tuščias."}\],"isErrorCountUpdated":true}*

Čia vaizduojama, kaip atrodo klaida modeliu grįstoje „Dynamics 365” programoje:

*Įvyko netikėta ISV kodo klaida. (ErrorType = ClientError) Netikėta priedo išimtis (vykdyti): Microsoft.Dynamics.Integrator.CrmPlugins.Plugin: System.Exception: nepavyko apdoroti objekto sąskaitos – nepavyko užmegzti ryšio, nes šalis, prie kurios buvo jungiamasi, tinkamai neatsakė praėjus tam tikram laiko tarpui, arba užmegztas ryšys nutruko, nes prijungtas pagrindinis kompiuteris neatsakė*

Ši klaida įvyksta, kai „Common Data Service” aplinka netinkamai paleidžiama iš naujo tuo pačiu laiku, kai bandote sukurti duomenis „Finance and Operations” programoje.

Norėdami ištaisyti klaidą, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie „Finance and Operations” virtualiosios mašinos (VM), atidarykite SQL serverio valdymo studiją (SSMS) ir ieškokite įrašų lentelėje DUALWRITEPROJECTCONFIGURATIONENTITY, kur **internalentityname** lygu **Klientai V3** ir **externalentityname** lygu **paskyros**. Štai kaip atrodo užklausa.

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. Naudokite projekto pavadinimą iš ankstesnės užklausos rezultatų, kad vykdytumėte kitą užklausą.

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. Įsitikinkite, kad stulpelyje **externalenvironmentURL** yra tinkamas „Common Data Service” arba programos URL. Panaikinkite visus pasikartojančius įrašus, kurie nurodo netinkamą „Common Data Service” URL. Panaikinkite atitinkamus įrašus DUALWRITEPROJECTFIELDCONFIGURATION ir DUALWRITEPROJECTCONFIGURATION lentelėse.
4. Sustabdykite susiejimą su objektu, tada paleiskite jį iš naujo