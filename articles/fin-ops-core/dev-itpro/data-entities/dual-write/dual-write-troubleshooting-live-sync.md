---
title: Tiesioginio sinchronizavimo trikčių šalinimas
description: Šioje temoje pateikiama trikčių šalinimo informacija, kuri gali padėti išspręsti problemas, susijusias su tiesioginiu sinchronizavimu.
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
ms.openlocfilehash: 1c0dfebb3ef442f67d8489d7aed00305c02cf410
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748902"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Tiesioginio sinchronizavimo trikčių šalinimas

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Dataverse“ programų trikčių šalinimo informacija. Tiksliau sakant, pateikiama informacija, kuri gali padėti išspręsti problemas, susijusias su tiesioginiu sinchronizavimu.

> [!IMPORTANT]
> Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Tiesioginis sinchronizavimas pateikia klaidą „403 draudžiama“, kai kuriate eilutę „Finance and Operations” programoje

Kai „Finance and Operations” programoje kuriate eilutę, galite gauti tokį klaidos pranešimą:

*\[{\\"klaida\\":{\\"kodas\\":\\"0x80072560\\",\\"pranešimas\\":\\"Vartotojas nėra organizacijos narys.\\"}}\], Nuotolinis serveris pateikė klaidą: (403) draudžiama."}}".*

Norėdami išspręsti problemą, atlikite veiksmus, pateiktus skyriuje [Sistemos reikalavimai ir būtinosios sąlygos](requirements-and-prerequisites.md). Norėdami atlikti šiuos veiksmus, dvigubo rašymo programos vartotojai, sukurti „Dataverse”, privalo turėti sistemos administratoriaus vaidmenį. Numatytoji komanda savininkė taip pat turi turėti sistemos administratoriaus vaidmenį.

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Tiesioginis bet kokios lentelės sinchronizavimas nuolat pateikia panašią klaidą, kai kuriate eilutę „Finance and Operations” programoje

**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius

Kaskart bandydami įrašyti lentelės duomenis „Finance and Operations” programoje, galite gauti klaidos pranešimą, panašų į pateiktą toliau:

*Nepavyksta įrašyti duomenų bazės pakeitimų. Darbo vienetas negali įvykdyti operacijos. Nepavyksta įrašyti duomenų į objekto uoms. Įrašyti į UnitOfMeasureEntity nepavyko, nes nepavyko sinchronizuoti klaidos pranešimo su objekto uoms.*

Norėdami išspręsti problemą, turite įsitikinti, kad būtini nuorodos duomenys yra ir „Finance and Operations” programoje, ir „Dataverse”. Pavyzdžiui, jei klientas, kuriame esate „Finance and Operations” programoje, priklauso konkrečiai klientų grupei, įsitikinkite, kad ši klientų grupė yra „Dataverse”.

Jei duomenys yra abiejose programose ir patvirtinote, kad problema nėra susijusi su duomenimis, atlikite šiuos veiksmus:

1. Sustabdykite susijusią lentelę.
2. Prisijunkite prie „Finance and Operations” programos ir įsitikinkite, kad neveikiančios lentelės eilutės yra «DualWriteProjectConfiguration» ir „DualWriteProjectFieldConfiguration” lentelėse. Pavyzdžiui, čia vaizduojama, kaip atrodo užklausa, jei lentelė **Klientai** neveikia.

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. Jei net jums sustabdžius lentelės susiejimą, yra neveikiančios lentelės eilučių, panaikinkite eilutes, susijusias su neveikiančia lentele. Norėdami panaikinti eilutę, lentelėje „DualWriteProjectConfiguration” pasižymėkite stulpelį **„projectname”** ir lentelėje „DualWriteProjectFieldConfiguration” raskite eilutę naudodami projekto pavadinimą.
4. Pradėkite susiejimą su lentele. Patikrinkite, ar sinchronizuojant duomenis nekyla problemų.

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

4. Priskirkite vaidmenį, turintį skaitymo / rašymo teisę, skirtą atitinkamoms lentelėms, tada pasirinkite **Gerai**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Sinchronizavimo problemų aplinkoje, kurioje neseniai buvo pakeista „Dataverse” aplinka, sprendimas

**Reikiamas vaidmuo, norint spręsti problemą:** sistemos administratorius

Kai „Finance and Operations” programoje kuriate duomenis, galite gauti tokį klaidos pranešimą:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Nepavyksta sugeneruoti mokamosios krovos objektui CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Nepavyko sukurti mokamosios krovos, įvyko klaida „Netinkamas URI“: URI yra tuščias."}\],"isErrorCountUpdated":true}*

Čia vaizduojama, kaip atrodo klaida modeliu grįstoje „Dynamics 365” programoje:

*Įvyko netikėta ISV kodo klaida. (ErrorType = ClientError) Netikėta priedo išimtis (vykdyti): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: nepavyko apdoroti objekto sąskaitos – nepavyko užmegzti ryšio, nes šalis, prie kurios buvo jungiamasi, tinkamai neatsakė praėjus tam tikram laiko tarpui, arba užmegztas ryšys nutruko, nes prijungtas pagrindinis kompiuteris neatsakė*

Ši klaida įvyksta, kai „Dataverse” aplinka netinkamai paleidžiama iš naujo tuo pačiu laiku, kai bandote sukurti duomenis „Finance and Operations” programoje.

Norėdami ištaisyti klaidą, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie „Finance and Operations” virtualiosios mašinos (VM), atidarykite SQL serverio valdymo studiją (SSMS) ir ieškokite eilučių lentelėje DUALWRITEPROJECTCONFIGURATIONENTITY, kur **internalentityname** lygu **Klientai V3** ir **externalentityname** lygu **paskyros**. Štai kaip atrodo užklausa.

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

3. Įsitikinkite, kad stulpelyje **externalenvironmentURL** yra tinkamas „Dataverse” arba programos URL. Panaikinkite visas pasikartojančius eilutes, kurios nurodo netinkamą „Dataverse” URL. Panaikinkite atitinkamas eilutes DUALWRITEPROJECTFIELDCONFIGURATION ir DUALWRITEPROJECTCONFIGURATION lentelėse.
4. Sustabdykite susiejimą su lentele, tada paleiskite jį iš naujo


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]