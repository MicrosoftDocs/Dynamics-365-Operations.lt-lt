---
title: Finansų ir operacijų programėlių paslaugos aprašas
description: Šioje temoje pateikiamas finansų ir operacijų programėlių paslaugos aprašymas.
author: tomhig
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: whigginb
ms.search.validFrom: 2021-09-03
ms.openlocfilehash: cd033cfc3df21ddac5572aa70c18db5ffe26f54e
ms.sourcegitcommit: 0abc777986112ea2332f5bf0e815b303b952356c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/29/2022
ms.locfileid: "8656809"
---
# <a name="service-description-for-finance-and-operations-apps"></a>Finansų ir operacijų programėlių paslaugos aprašas

[!include[banner](../includes/banner.md)]

Finansų ir operacijų programos yra įmonės išteklių planavimo (ERP) programinė įranga kaip paslauga (SaaS) siūlymas, kuriam kuriamas ir kuriamas [Microsoft Azure](https://azure.microsoft.com/overview/what-is-azure/). Finansų ir operacijų tarnyba suteikia organizacijoms ERP funkcijas, kurios palaiko savo unikalius reikalavimus ir padeda joms koreguoti, pereidama prie verslo aplinkos keitimo, nereikalaudama, kad jos valdytų infrastruktūrą. Finansų ir operacijų programėles gali sudaryti viena arba daugiau iš šių sprendimų sričių:

- [Dynamics 365 Finance](/dynamics365/finance/)
- [„Dynamics 365 Human Resources“](/dynamics365/human-resources/)
- [„Dynamics 365 Supply Chain Management“](/dynamics365/supply-chain/)
- [„Dynamics 365 Commerce“](/dynamics365/commerce/)
- [„Dynamics 365 Project Operations“](/dynamics365/project-operations/)

Kartu su [verslo sumanumu](/power-bi/fundamentals/power-bi-service-overview), [infrastruktūra](https://azure.microsoft.com/global-infrastructure/), [vykdymu](/azure/service-fabric/service-fabric-overview), ir [duomenų bazės paslaugomis](https://devblogs.microsoft.com/azure-sql/running-1m-databases-on-azure-sql-for-a-large-saas-provider-microsoft-dynamics-365-and-power-platform/), šios programos leidžia organizacijoms vykdyti konkrečią pramonės ir veiklos verslo procesus. Palaikomi savo diegimo partnerio, klientai apibrėžia verslo programos logikos, kuri geriausiai tinka unikaliems verslo procesams, konfigūraciją. Funkcijas ir verslo procesus galima padidinti arba išplėsti naudojant vieną iš šių sprendimų arba jų kombinaciją:

- Sukurta [personalizavimo patirties](personalize-user-experience.md)
- [„Microsoft Power Platform“](../../dev-itpro/power-platform/overview.md) įrankiai
- [Visual Studio](https://visualstudio.microsoft.com)– remiantis finansų [ir operacijų programinės įrangos kūrimo rinkiniu (SDK) ir](../../dev-itpro/dev-tools/developer-home-page.md) automatizavimu [Azure DevOps sukurti automatizavimą](../../dev-itpro/dev-tools/developer-home-page.md#build-automation-using-azure)
- Nepriklausomo programinės įrangos tiekėjo (ISV) sprendimai nuo [„AppSource“](https://appsource.microsoft.com/partners)

Priklausomai nuo reikalavimų, klientai pasirenka būdą, kaip sprendimas. Jie dirba su savo diegimo partneriu, kad nustatytų, vystytų ir išbandykite savo sprendimą, naudodami įrankius ir geriausią [„Microsoft Dynamics“ „Lifecycle Services“ (LCS) pateiktą praktiką](../../dev-itpro/lifecycle-services/lcs.md). Yra keturi įbendrieji scenarijai:

- Standartinės finansų ir operacijų programėlės "už lango" konfigūracijos (nėra plėtinių)
- Finansų ir operacijų programėlių konfigūracija, kurioje yra vienas ar daugiau ISV sprendimų
- Finansų ir operacijų programėlių konfigūracija, kurioje yra vienas arba daugiau klientui skirtų plėtinių
- Finansų ir operacijų programėlių konfigūracija, kurioje yra klientui skirtų plėtinių derinys ir vienas ar daugiau ISV sprendimų

Organizacijos gali suderinti savo verslo augimas, lengvai pridėdami vartotojus ir verslo procesus naudodami paprastą, skaidrų abonemento modelį. Daugiau informacijos apie šiuos pakeitimus žr. [„Dynamics 365“ licencijavimo vadove](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365).

## <a name="operating-model"></a>Veikimo modelis

Finansų ir operacijų programėlių veiklos modelis apibrėžia konkrečius kliento vaidmenis ir atsakomybę, diegimo partnerį ir "Microsoft" viso aptarnavimo ciklo metu. Daugiau informacijos rasite [debesies operacijos ir aptarnavimas](../../dev-itpro/lifecycle-services/cloud-operations-servicing.md).

### <a name="customer-activities"></a>Kliento veiklos

Klientai dirba su savo partneriu [ir "Microsoft FastTrack](/dynamics365/fasttrack/)[" naudodami "Dynamics 365](https://community.dynamics.com/365/dynamics-365-fasttrack/p/dynamics365implementationguide)" diegimo vadovą, [Success by Design](/dynamics365/fasttrack/success-by-design-overview) sistemą ir geriausios praktikos šablonus, [kurie](../../dev-itpro/lifecycle-services/lcs.md) pateikiami vykdymo ciklo tarnybose, kad galėtų įdiegti savo sprendimą. Bendros veiklos apima:

- Vartotojo tapatybė ir saugos valdymas
- Verslo procesų apibrėžimas, vystimas ir veikla
- Apibrėžkite, kurkite, išbandykite ir tęskite plėtinius
- Stebėti ir valdyti ne gamybos diegimus
- Tvarkyti programos naujinimus ir patikrinti plėtinius
- Valdyti ISV sprendimus ir trečiosios šalies integravimą

### <a name="microsoft-responsibilities"></a>„Microsoft“ atsakomybės

"Microsoft" valdo finansų ir operacijų tarnybą, aktyviai stebėjimą ir aptarnavimo klientų sandūras bei gamybos aplinkas "Microsoft SaaS" abonemente. Šis valdymas apima reikiamos sistemos infrastruktūros paskirstymą, kad būtų galima paleisti paslaugą ir aktyviai susisiekti su klientais apie paslaugos būseną. Atsakomybės apima:

**Infrastruktūros valdymas**
- Sauga ir atskyrimas
- Operacinės sistemos ir virtualizavimas
- Serveriai, saugojimas ir bazės
- Duomenų centro galia, pagal, pagal

**Programos platformos valdymas**
- 24/7 programų stebėjimas ir pranešimai
- Diagnostika, platformos naujinimai, pataisos, aptarnavimo atnaujinimai
- Programos nukreipimas, apkrovos balansavimas, svetainės dubliavimas
- Aplinkos parengimas ir valdymas
- Duomenų bazės valdymas, didelis pakankamumas (HA)/nelaimių susigrąžinimas (DB), svarstyklės, operacijos
- Komponuoti diegimą, svarstykles, svarstykles

## <a name="system-configuration"></a>Sistemos konfigūracija

Finansų ir operacijų programėlių svarstyklės pagal operacijų apimtį ir vartotojo krovinį. Kiekvienas kliento diegimas sukuria unikalų sprendimą, kurį sudaro šie elementai:

- **Duomenų struktūra**– unikalus parametrų, kurie kontroliuoja veikimo būdą, organizacijos maketas, pagrindinių duomenų struktūra (pvz., finansinės ir atsargų dimensijos) ir operacijos sekimo detalumas.
- **Plėtinys ir konfigūracija**– plėtinio mechanizmai, naudojantys kodo plėtinius, ISV sprendimus ir unikalias konfigūracijas, kurias sudaro darbo eigos, integracijų ir ataskaitų konfigūracijos.
- **Naudojimo modeliai** – unikalus interneto ir paketinio naudojimo derinys, kartu su galimybe integruotis proceso aukštyn ir proceso metu bei vieningam duomenų srautui ir gebėjimas atskirti, atsižvelgiant į informacijos rodinius, kuriuos klientai naudoja savo verslo procesuose.

„Microsoft" sukonfigūruoja kliento gamybos aplinkas, kurių kiekis yra dydžio, kad būtų galima tvarkyti operacijų tūrius ir vartotojo suumą. „Microsoft" yra atsakinga už šias užduotis:

- Tinkamai paskirstomi gamybos aplinkos ištekliai, remiantis kliento profiliavimo informacija [LCS abonemento įvertinme](../../dev-itpro/lifecycle-services/subscription-estimator.md)
- Nepertraukiamas gamybos aplinkos aptarnavimo prieinamumo stebėjimas ir diagnozavimas
- Sistemos našumo problemų analizavimas ir trikčių šalinimas naudojant finansų ir operacijų programėles

Kad diegimas būtų sukonfigūruotas labai našumui, klientai turi atlikti šias užduotis:

- Pateikti tikslią naudojimo informaciją apie finansų ir operacijų vykdymą [LCS abonemento įvertinme](../../dev-itpro/lifecycle-services/subscription-estimator.md).
- Sukurkite ir išbandykite našumo ir svarstyklių plėtinius.
- Tinkamai išbandykite duomenų konfigūracijas našumui užtikrinti.
- Prieš edami į [darbą įsitikinkite](https://community.dynamics.com/365/b/techtalks/posts/performance-testing-approach-april-30-2018) išplečiamumą ir patikrinkite našumą.

## <a name="onboarding-and-implementation"></a>Diegimas ir implementavimas

Šioje lentelėje pateikiami įprasti įprasti įėjimo ir diegimo įvykiai.

| Prašymas | Numatomas „Microsoft“ veiksmas | Numatomas kliento / diegimo partnerio veiksmas |
|---|---|---|
| Pradinis pasiūlymo pirkimas | LCS projektas sukuriamas įsigius pasiūlymą, remiantis kliento sukeltu įvykiu. | Eikite per įmonės sutarties (EA) ar debesies sprendimų teikėjo (CSP) [prekybos procesą](before-you-buy.md). Partneris sukuria kliento nuomininką, jei taikoma. |
| Pirkimo priedai | Suteikite klientui prieigą prie diegimo metu pasirinkto priedo. | Netaikoma |
| Diegimo planavimas ir analizė | Pateikite atitinkamus LCS įrankius, [pvz., verslo procesų modeliavimo priemonę (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md) ir [sąveiką su „Azure DevOps“](../../dev-itpro/lifecycle-services/synchronize-bpm-vsts.md). | Atlikite projektų planavimą, „Azure DevOps“ nustatykite, baikite sistemos insąskaitų planavimą ir nustatykite administravimo sąskaitas. |

Daugiau informacijos rasite [diegimo projekto insąrangoje](../imp-lifecycle/onboard.md).

## <a name="globalization"></a>Globalizacija

Finansų ir operacijų programėles galima pasiekti iš kelių "Azure" regionų visame pasaulyje. Finansų ir operacijų programėlės suteikia funkcijų, skirtų skirtingoms šalims / regionams ir gimtąsias kalbas palaikyti. Daugiau informacijos rasite [lokalizavimo ir reguliavimo priemonės](../../dev-itpro/lcs-solutions/country-region.md#localization-and-regulatory-features).

### <a name="countryregion-specific-considerations"></a>Konkrečių šalių / regionų svarstymai

- Reguliuojamųjų pramonės ar komercijos organizacijų klientai, kurie verslo veikia su Prancūzijos subjektais, kuriems reikia vietinių duomenų, turėtų [peržiūrėti Prancūzijos finansus ir operacijas](../../dev-itpro/deployment/france-local-deployment.md).
- Klientai, kinijos operacijoms vykdantys operacijas, turi peržiūrėti " [Azure China" "Book](/azure/china/) " [ir "Finance" bei operacijas, kurias operuoja 21 Kliento programos Kinija](../../dev-itpro/deployment/china-local-deployment.md).
- Klientai, kurie turi operacijas Rusijoje, turi peržiūrėti [Rusijos asmeninių duomenų lokalizavimo įstatymą](/business-applications-release-notes/october18/dynamics365-finance-operations/russian-regulations-on-prem#when-will-the-cloud-deployment-option-of-dynamics-365-for-finance-and-operations-be-generally-available-for-russia).

### <a name="general-data-protection-regulation-gdpr"></a>Bendrasis duomenų apsaugos reglamentas (BDAR)

Dėl finansų ir operacijų programėlių "Microsoft" veikia kaip procesorius. Kaip duomenų procesorius, finansai ir operacijos pateikia procesus ir priemones, kurios padeda klientams laikytis GDPR įsipareigojimų kaip duomenų valdiklis. Daugiau informacijos ieškokite [BDAR apžvalga](../../dev-itpro/gdpr/gdpr-guide.md).

## <a name="environment-and-data-management"></a>Aplinkos ir duomenų valdymas

Šiame skyriuje aprašomi įprasti aptarnavimo aplinkos ir duomenų valdymo įvykiai.

### <a name="environment-and-data-management-events-for-production-instances"></a>Gamybos egzempliorių aplinkos ir duomenų valdymo įvykiai

LCS teikia [savitarnos įrankius](../../dev-itpro/deployment/infrastructure-stack.md)ir [duomenų bazės perkėlimo operacijas](../../dev-itpro/database/dbmovement-operations.md), naudojamas atliekant aplinkos ir duomenų valdymo užduotis. Štai keletas pavyzdžių:

**Įvykis:** [gamybos egzemplioriaus prašantis](../imp-lifecycle/prepare-go-live.md#requesting-the-production-environment)

- Užpildykite [„Go-live" kontrolinį](../imp-lifecycle/prepare-go-live.md) sąrašą ir pateikite jį [„Microsoft FastTrack“](/dynamics365/fasttrack/) komandai.
- Prieš [užklausdami gamybos egzempliorių užbaikite LCS](../../dev-itpro/lifecycle-services/subscription-estimator.md) abonemento įvertinimaus.
- Atlikite visas diegimo užduotis, nurodytas [LCS metodologijoje](../../dev-itpro/lifecycle-services/create-methodology.md).

**Įvykis:** [sandų dėžės duomenų bazės kopijavimas į gamybos egzempliorių](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Atlikta dėl einamojo arba faktinio tiesioginio keitimo.

**Įvykis:** [Priežiūros režimas](../../dev-itpro/sysadmin/maintenance-mode.md)

1. Įjunkite priežiūros režimą LCS.
2. Užbaikite reikiamą priežiūrą.
3. Išjunkite priežiūros režimą LCS.

### <a name="environment-and-data-management-events-for-non-production-instances"></a>Ne gamybos egzempliorių aplinkos ir duomenų valdymo įvykiai

LCS teikia [savitarnos tiekimas](../../dev-itpro/deployment/infrastructure-stack.md) ir [duomenų bazės perkėlimo operacijos](../../dev-itpro/database/dbmovement-operations.md), naudojamas atliekant aplinkos ir duomenų valdymo užduotis. Štai keletas pavyzdžių:

**Įvykis:** [naujo smėlio dėžės egzemplioriaus diegimas](../../dev-itpro/deployment/deployenvironment-newinfrastructure.md)

- Įsitikinkite, kad suplanuoti visi būtini egzemplioriai ir kad [buvo](../imp-lifecycle/environment-planning.md) įsigyti taikomi priedų pasiūlymai.
- Vykdykite diegimo LCS procesą.
- Atlikite visas diegimo užduotis, nurodytas LCS patikrų sąrašai.
    
>[!NOTE]
>Programavimo sandbox aplinka yra virtualioji mašina (VM), [diegiama į kliento „Azure" abonementą](../../dev-itpro/dev-tools/access-instances.md) ir valdoma kliento.

**Įvykis:** [Kopijuoti auksinę konfigūracijos duomenų bazę iš smėlio dėžės į gamybą](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Atlikta dėl einamojo arba faktinio tiesioginio keitimo.

**Įvykis:** [gamybos, tam tikrą laiką rezervinės ne gamybos egzemplioriui, atkūrimas](../../dev-itpro/database/database-pitr-prod-sandbox.md)

- Paleiskite [duomenų bazės atnaujinimo](../../dev-itpro/database/database-refresh.md) parinktį LCS.
- Po kopijavimo: panaikinkite arba paskirstykite slaptus duomenis naudodami scenarijus, pakoreguokite nuo aplinkos konkrečias programos konfigūracijas (pvz., integravimo galinius punktus) ir įgalinkite arba įtraukite vartotojus. Įsidėmėkite, kad šie pakeitimai atlikti taikant [duomenų paketą](../../dev-itpro/data-entities/data-entities-data-packages.md#import-a-data-package).

**Įvykis:** [ne gamybos egzemplioriaus duomenų bazės tam tikrą laiką atkūrimas](../../dev-itpro/database/database-point-in-time-restore.md)

- Priimti, kad proceso anuliuoti negalima.
- Į vykdykite į tam tikrą laikotarpį įka grąžinti operaciją LCS.

**Įvykis:** „Tier 2" sandų dėžės duomenų bazės kopijavimas į programavimo sandų dėžę, kad būtų galima trikčių diagnostika ir [derinimas](../../dev-itpro/database/dbmovement-scenario-debugdiag.md)

- Paleiskite duomenų bazės eksportavimo operaciją LCS 2 pakopų smėlio dėžės aplinkoje.
- Importuokite ir atnaujinkite duomenų bazę programavimo aplinkoje.

## <a name="data-backup-and-retention"></a>Duomenų atsarginis kopijavimas ir užlaikymas

SaaS abonemento finansų ir operacijų aplinkos duomenų bazes apsaugo automatinės atsarginės kopijos. Gamybos aplinkoje automatinės atsarginės kopijos išlieka 28 dienas, nebent „Microsoft“ neatidarys keitimų. Sandbox (Tier 2+) aplinkose jos išlaikomos septynias dienas. Gamybos aplinkos keitimų atšaukimą galima atlikti, jei atliekant bet kurį suplanuotą priežiūros atnaujinimą įvyksta triktis.

Norėdami gauti daugiau informacijos apie automatines atsargines kopijas, žr. [automatizuotas atsargines kopijas – „Azure SQL" duomenų bazė ir SQL valdomas egzempliorius](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).

## <a name="service-activity-responsibilities"></a>Aptarnavimo veiklos atsakomybės

Toliau pateikiamoje lentelėje aprašomi įprasti aptarnavimo scenarijai ir veiklos. Taip pat nurodoma, ar „Microsoft", klientas arba ir „Microsoft" ir klientas yra atsakingas už veiklą.

| Veikla | „Microsoft“ atsakomybė | Kliento atsakomybė |
|---|---|---|
| **Pradinių nuomininkų parengimas** | | |
| Naudodami abonemento įvertinimo įrankį galite nustatyti LCS numatytai apkrovai ir prašyti parengti konkrečias aplinkas. | | X |
| Patrūkite visus gamybos egzempliorius ir ne gamybos egzempliorius. | X | |
| Patvirtinti talpintus visus gamybos egzempliorius ir ne gamybos egzempliorius. | | X |
| **Paslaugų naujinimai** | |
| Taikyti tarnybos naujinimus nustatyties ne gamybos ir gamybos egzemplioriams. | X | |
| Rankiniu būdu LCS pritaikykite tarnybos naujinimus sanddėdės egzemplioriams. Nustatykite, sukurkite, išbandykite naujinimą ir atkurkite kodo naujinimo paketą LCS. | | X |
| Prašyti ir planuoti plėtinio naujinimus taip, kad jie būtų taikomi gamybos egzemplioriui. | | X |
| Prieš pradedant taikyti atnaujinimus sukurkite gamybos egzemplioriaus kodą ir duomenų atsarginę kopiją. | X | |
| Įvykus bet kokiems triktims, gamybos egzemplioriaus atšaukite kodą ir duomenų atsarginę kopiją. | X | |
| **Duomenų valdymas (atsarginis kopijavimas, atkūrimas ir atnaujinimas)** | | |
| Sukurti atsarginę duomenų bazės kopiją. | X | |
| Nustatykite aukštą pasiekiamumą ir įvykių susigrąžinimo planą. | X | |
| Stebėti gamybos egzemplioriaus duomenų bazės našumą. | X | |
| Derinti gamybos egzemplioriaus duomenų bazės veikimą. | X | |
| Atlikti gamybos egzemplioriaus duomenų bazės tam tikrą laikotarpį atnaujinimą ne gamybos egzemplioriui. | | X |
| **Infrastruktūros atnaujinimas** | | |
| Suplanuoti įprastus infrastruktūros naujinimus. | X | |
| **Dydžio mastelis (vartotojai, saugykla ir egzemplioriai)** | | |
| Įsigkite papildomų vartotojų ir ne gamybos priedų. | | X |
| Atnaujinkite naudojimo keitimus LCS abonemento įvertinimo įrankyje. | | X |
| Pranešti apie bet kokias svarbias našumo problemas, kurios turi įtakos aptarnavimo naudojimui. | | X |
| Proactively valdyti išteklius, reikalingus taikomai tarnybai. | X | |
| Išnagrinėtos ir trikčių šalinimo incidentai. | X | |
| **Sauga (vartotojo prieiga)** | | |
| Suteikti vartotojui prieigą prie paslaugos. | | X |
| Suteikite LCS projekto prieigą, kad būtų galima valdyti ir valdyti egzempliorius, kurie įdiegti naudojant LCS. | | X |
| **Gamybos egzempliorių stebėjimas** | | |
| Stebėti gamybos egzempliorius 24/7. | X | |
| Aktyviai praneškite klientui apie incidentus, kurie susiję su gamybos egzemplioriumi. | X | |
| **Ne gamybos egzempliorių valdymas ir stebėjimas** | | |
| Tvarkykite ne gamybos egzempliorius naudodami LCS. | | X |
| Stebėti ne gamybos egzempliorius. | | X |

## <a name="service-update-strategy"></a>Paslaugų naujinimų strategija

Atsižvelgiant į programinės įrangos [vykdymo ciklo](../../dev-itpro/migration-upgrade/versions-update-policy.md) strategiją, finansų ir operacijų programėlėse taikoma "Microsoft [" modernaus vykdymo ciklo](../../dev-itpro/migration-upgrade/versions-update-policy.md#modern-lifecycle-policy) strategija, kuri apima nuolat aptarnaujamus ir palaikomus produktus. 

"Microsoft" kasmet išleidžia aštuonis finansinių ir operacijų programėlių paslaugų naujinimus šiais mėnesiais:

- Sausis
- Vasaris
- Balandis
- Gegužės
- Liepos
- Rugpjūčio
- Spalio
- Lapkričio

>[!NOTE]
>Balandžio ir spalio mėnesiai yra pagrindinės funkcijų paleidimo bangos. Klientai gali pristabdyti atskirų paslaugų atnaujinimą iki trijų vienas po kito einančių atnaujinimo ciklų.

Daugiau informacijos peržiūrėkite šiose temose:

- [Vienos versijos paslaugų naujinimų apžvalga](../../dev-itpro/lifecycle-services/oneversion-overview.md)
- [Paslaugų naujinimai per LCS](../../dev-itpro/lifecycle-services/configure-service-updates.md)
- [Paslaugų naujinimai per LCS](../../dev-itpro/lifecycle-services/pause-service-updates.md)
- [Gaukite pranešimus apie paslaugų naujinimus per LCS](../../dev-itpro/lifecycle-services/notifications-service-updates.md)
- [Regresijos tikrinimo įrankiai tarnybos naujinams tikrinti](../../dev-itpro/perf-test/rsat/rsat-overview.md)
- [„Dynamics 365" versija ir paleidimo bangos](https://dynamics.microsoft.com/roadmap/overview/)

## <a name="security-and-administrative-access"></a>Saugos ir administravimo prieiga

Administratoriaus prieiga prie finansų ir operacijų gamybos aplinkos yra griežtai kontroliuojama ir registruojama. Kliento duomenys tvarkomi pagal [„Microsoft Online Services“ sąlygas](https://www.microsoft.com/licensing/terms/productoffering). 

### <a name="customer-administrative-access"></a>Kliento administratoriaus prieiga

Kliento nuomininkų administratorius gali pasiekti gamybos egzempliorius arba ne gamybos egzempliorius, kaip aprašyta šioje lentelėje:

| Aplinkos tipas | Paskirtis | Kliento prieigos lygis |
|---|---|---|
| **Ne gamyba**<br>1 pakopos smėlio dėžutė | Ne gamybos aplinka, kurią klientai diegia programavimo, demonstravimo arba mokymo tikslais. | 1 pakopa su sandbox (taip pat vadinama debesies nuomojama aplinka) yra kliento valdomaS VM, kuris įdiegiamas į kliento „Azure" abonementą iš LCS. Kliento „Azure" abonemente yra VM, todėl klientas turi visiškas administratoriaus prieigą prie aplinkos per nuotolinį darbalaukį. |
| **Ne gamyba**<br>2 (arba naujesnė) smėlio dėžė | Ne gamybos aplinka, kurią klientai diegia vartotojo priėmimo bandymui, integravimo bandymui, mokymas, išdėstymui ar bet kokiam kitam išankstiniam gamybos scenarijui. | 2 ir aukštesnio lygio sanddės diegiamos į finansų ir operacijų SaaS abonementą. Prieiga prie „Azure SQL" duomenų bazių, susietų su ne gamybos [aplinka, suteikiama tik laiku](../../dev-itpro/database/database-just-in-time-jit-access.md). Nuotolinio darbalaukio prieiga negalima. |
| **Gamyba** | Gamybos aplinka įdiegiama, kai projektas [parengtas pradėti vykti](/imp-lifecycle/environment-planning.md#production-system-readiness). | Gamybos aplinkos diegiamos į „SaaS“ abonementą. Visa prieiga – tai naršyklė, paslaugų galiniai punktai arba LCS. |

### <a name="microsoft-administrative-access"></a>„Microsoft“ administratoriaus prieiga

Šioje lentelėje parodyti skirtingi skirtingų „Microsoft“ administratorių prieigos lygiai:

| Administratorius | Kliento duomenys |
|---|---|
| Operacijų atsakymų komanda<br>(Apribota tik raktu personalui) | Prieiga suteikiama per palaikymo bilietą. Prieiga yra audituota ir apribota – iki palaikymo veiklos trukmės. |
| „Microsoft Customer Support Services“ ( CSS) | Tiesioginės prieigos nėra. Klientas gali naudoti ekrano bendrą naudojimą, kad galėtų dirbti su palaikymo darbuotojais, kad būtų derinimo problemos. |
| Inžinerija | Tiesioginės prieigos nėra. Operacijų atsakymo komanda gali naudoti ekrano bendrinimą, kad galėtų dirbti su inžinerija, kad būtų galima derinti problemas. |
| Kiti „Microsoft“ | Nėra prieigos. |

## <a name="monitoring"></a>Stebėjimas

„Microsoft" į turi daug įrankių rinkinio, kad galėtų stebėti ir diagnozuoti klientų gamybos egzempliorius. „Microsoft" stebi klientų gamybos aplinką 24 val. per dieną, 7 dienas per savaitę. Daugiau informacijos ieškokite [Gamybos palaikymas ir stebėjimas](../imp-lifecycle/production-support-monitoring.md).

| „Microsoft“ atsakomybės | Klientų atsakomybė |
|---|---|
| <ul><li>Stebėti tarnybos pasiekiamumą.</li><li>Nuolat stebėti ir gauti įspėjimus dėl kritinių komponentų, pvz., programos objektų serverio (AOS), paketo, duomenų importavimo / eksportavimo sistemos (DIXF), „Commerce" ir „Management Reporter", sveikatos metrikos ir teksto.</li><li>Stebėti, ar nėra našumo, atsiradusio dėl infrastruktūros paslaugų (pvz., „Azure Active Directory“ \[„Azure AD“\] „Azure SQL").</li><li>Jei „Microsoft“ nustato, kad dėl vieno proceso arba paketinės užduoties kyla problemų, šis procesas arba užduotis bus nutraukti bendravimui su klientu.</li></ul> | <ul><li>Stebėti programos konfigūracijų ir plėtinių pakeitimus, kurie gali sukelti funkcinių ir našumo problemų.</li><li>Programos klaidos turi būti diagnozuotos naudojant stebėjimo įrankius. Naudodami šiuos įrankius galite diagnozuoti vartotojo ataskaitoje nurodytus našumo aberacijas.</li><li>Informuokite „Microsoft", jei numatoma įkelti į sistemą viršyto didžiausio naudojimo.</li><li>Jei gamybos egzemplioriuje taikomos paslaugos nėra, klientas gali naudoti LCS ataskaitoje apie [gamybos išlaidas](../../dev-itpro/lifecycle-services/report-production-outage.md).</li></ul> |

Pateikdami palaikymo užklausas internete, naudodami LCS, klientai leidžia „Microsoft" suteikti greitą ir išsamią techninio kompetencijos patirtį našiausiu ir našiausiu būdu. Nors telefono pasirinktis galima, ją galima naudoti tik tada, jei interneto pasirinktis negalima. Daugiau informacijos žr. [Telefono palaikymo parinktys](/power-platform/admin/support-overview.md?toc=/dynamics365/fin-ops-core/dev-itpro/toc.json&bc=/dynamics365/breadcrumb/toc.json#is-there-a-phone-number-i-can-call-to-contact-support).

## <a name="incident-management"></a>Veiksmų valdymas

„Microsoft" atsako į ir pataiso incidentus, remiantis sunkumo lygiais. „Microsoft" incidento sunkumo lygius galima pakeisti pirminio incidento įvertinimo metu ir tampa daugiau informacijos apie poveikį ir aprėptį. Jei incidentas sumažinamas, incidento svarba nekinta.

Daugiau informacijos apie sunkumo lygius ieškokite [šioje sunkumo lentelėje](/power-platform/admin/support-overview#what-is-initial-response-time-and-how-quickly-can-i-expect-to-hear-back-from-someone-after-submitting-my-support-request).

## <a name="business-continuity-through-high-availability-and-disaster-recovery"></a>Verslo tęstinumas per didelio užimtumo ir įvykių susigrąžinimo padarinius 

"Microsoft" užtikrina verslo tęstinumą ir įvykių susigrąžinimą finansų ir operacijų programėlių gamybos egzemplioriams "Azure" regiono atveju – "outage". Daugiau informacijos, įskaitant aptarnavimo susigrąžinimo laiko tikslą (RTO) ir atkūrimo taško tikslą (RPO), žr. verslo [tęstinumą ir įvykių susigrąžinimą](../../dev-itpro/sysadmin/business-continuity-disaster-recovery.md).

- **Didelis pasiekiamumas** – HA funkcija suteikia būdų, kaip išvengti triktį, kurią lemia vieno mazgo gedimas „Azure" duomenų centre. Kiekvienos paslaugos debesies architektūra naudoja „Azure" pasiekiamumo rinkinius apskaičiuoti pakopai, kad išvengtų vieno trikčių taškų įvykių. HA duomenų bazėms pateikiama naudojant [„Azure SQL HA" funkcijas](/azure/azure-sql/database/high-availability-sla).
- **Įvykių sugrąžinimas** – [„Azure“ nelaimių grąžinimo funkcija](/azure/best-practices-availability-paired-regions) apsaugo kiekvieną paslaugą nuo besigrąžinamų įvykių, kurie labai veikia visą „Azure“ duomenų centrą. Štai keletas šių funkcijų:

    - „Azure SQL" aktyvių geografinių išteklių replikavimas, skirtas pirminėms duomenų bazėms (verslo duomenų bazei).
    - „Azure BLOB" saugyklos (kuriame yra dokumentų priedų) perteklinės kopijos kituose „Azure" regionuose.
    - Antrinis „Azure SQL" ir „Azure Azure Blob Storage" kartojimai.

Jei dėl įvykusių įvykių susigrąžinimo naudojamas kliento gamybos egzemplioriui sugrąžinti, „Microsoft" ir klientas pateis prie [incidentų valdymo](service-description.md#incident-management).

„Microsoft“ įvykių susigrąžinimo planai ir procedūros tikrinamos reguliariai atliekant sistemos ir organizacijos valdiklių (SOC) auditus. Šie atitikties auditai patvirtina "Microsoft" DARBO techninio ir procedūrinio proceso, įskaitant "Dynamics 365" finansų ir operacijų programėles, procesą. [SOC atitikties](/compliance/regulatory/offering-soc-2) audito ataskaitos ir visos kitos atitikties ataskaitos yra [„Microsoft" patikimumo centro atitikties pasiūlymų atveju](/compliance/regulatory/offering-home).

## <a name="finance-and-operations-support-offerings"></a>Finansų ir operacijų pasiūlymų palaikymas

Techninis palaikymas prieinamas rinkoje, kurioje siūlomos finansų ir operacijų paslaugos. [Palaikymo patirtis](../../dev-itpro/lifecycle-services/lcs-support.md) pateikiama LCS arba finansų ir operacijų programėlėse. Štai keletas pavyzdžių:

- [Problemų ieška](../../dev-itpro/lifecycle-services/issue-search-lcs.md) LCS
- [Integruotas techninis](../../dev-itpro/lifecycle-services/support-experience.md) palaikymas finansų ir operacijų programėlėse
- [Iš debesies teikiamas palaikymas](../../dev-itpro/lifecycle-services/cloud-powered-support-lcs.md) LCS

"Microsoft" siūlo tris finansų ir operacijų klientų palaikymo planus: Msdn, Professional Direct ir į abonementą įtrauktą palaikymą. Kiekvienam planui skiriasi palaikymo lygis. Toliau pateikiamoje lentelėje pateikiami trijų planų palyginimai.

| Palaikymo funkcija | „Premier“ | Tiesioginė profesionalų pagalba | Abonementas |
|---|---|---|---|
| Neribotas pertraukų / pataisų incidento pateikimas | Taip | Taip | Taip |
| 24/7 prieiga per LCS | Taip | Taip | Taip |
| Incidento atsakymo laikas | Mažiau nei viena valanda | Mažiau nei viena valanda | Kita darbo diena |
| Darbo valandos | Telkiniai įgyjami pagal sutartį. | Ne | Ne |
| Paskirto palaikymo sąskaitos vadovas | Taip | Ne | Ne |
| Paskirto palaikymo inžinierius | Dirbama pagal atskirą sutartį | Ne | Ne |

Daugiau informacijos rasite [Palaikymo apžvalga](/power-platform/admin/support-overview).

### <a name="process-to-engage-support"></a>Procesas, įtraukti palaikymą

Kai incidentai susiję su finansų ir operacijų programėle, klientai per LCS pateikite palaikymo bilietą "Microsoft". CSS tvarko incidentus, remiantis kliento palaikymo planu ir incidento svarba, kaip nurodyta CSS.

### <a name="service-level-agreement"></a>Teikiamų paslaugų sutartis

„Microsoft“ fiksuota 99,9 procento per mėnesį paslaugai. Jei „Microsoft" nepavyksta pasiekti ir išlaikyti taikomos paslaugos lygio, kaip aprašyta aptarnavimo lygio sutartyje (SLA), klientas gali turėti teisę gauti kreditą tam tikrai tos paslaugos mėnesio aptarnavimo mokesčio dalisi. Informacijos apie aptarnavimo kredito iniciavimo procesą ieškokite „Pretenzijos“ skyriuje [Paraiškos](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

## <a name="important-resources"></a>Svarbūs ištekliai

- **[Patikimumo centras](https://www.microsoft.com/trust-center)** – gauti informacijos apie tai, kur saugomi jūsų finansų ir operacijų duomenys, taip pat papildomą informaciją apie privatumą, atitikimą ir saugos procedūras.
- **[Licencijavimo sąlygos ir dokumentai](https://www.microsoftvolumelicensing.com/)** – greitai prieiti prie licencijavimo sąlygų, sąlygų ir papildomos informacijos, susijusios su produktų ir paslaugų, kurios licencijuotos per „Microsoft“ apimties licencijavimo programas, naudojimui.
- **[Licencijavimo sąlygos](https://www.microsoft.com/licensing/product-licensing/)** – šio puslapio ištekliai nurodo programinės įrangos ir interneto paslaugų produktų, kuriuos perkate per „Microsoft“ komercinės licencijos suteikimo programas, sąlygas.
- **[„Microsoft" ciklo strategija](/lifecycle/)** – šiame puslapyje pateikiamos nuoseklios ir numatomos palaikymo per visą produkto naudojimo laiką gairės.
- **[Licencijavimo vadovas](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365)** – norėdami daugiau sužinoti apie „Dynamics 365" licenciją, naudokite šį vadovą.
- **[Klientų palaikymas](https://dynamics.microsoft.com/support/)** – gaukite pramonės šaką tinkantį „Dynamics 365" programėlių palaikymą.
- **[„Dynamics Lifecycle Services"](https://lcs.dynamics.com/)** – valdykite savo programos vykdymo ciklą ir pereisite prie numatymų, pasikartojančių, aukštos kokybės diegimo.
- **["Dynamics 365](https://aka.ms/D365ImplementationGuideFlip)** " diegimo vadovas – "Dynamics 365 Success by Design " diegimo vadovo dokumentų laiko patikrinti principai ir pateikiami prescriptiniai patarimai architektui, kurti, išbandyti ir diegti "Dynamics 365" sprendimus.

## <a name="definitions"></a>Sąvokos

### <a name="azure-region"></a>[„Azure“ regionas](/azure/availability-zones/az-overview#regions)

Geografinis regionas, kuriame yra vienas ar daugiau „Azure" duomenų centrų. Pavyzdžiai yra JAV ir Europa.

### <a name="business-process-modeler-bpm"></a>[Verslo procesų modeliavimo įrankis (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md)

LCS įrankis, kuris padeda atlikti reikiamos įdiegties tinkamos trūkumo analizę, naudojant Amerikos produktyvumo ir kokybės centro (APQC) verslo procesų apibrėžimus, kuriuos palaiko finansų ir operacijų programėlės.

### <a name="cloud-solution-provider"></a>Debesies sprendimo teikėjas

Partneris, kuris yra „Microsoft Cloud Solution Provider" (CSP) programos dalis ir teikia klientams pridėtinės vertės debesies paslaugas, palaikymą, vieną SF ir klientų valdymą svarstyklėmis.

### <a name="customer"></a>Klientas

Verslo objektas, kuris naudoja finansų ir operacijų programėles, ir kuriam nuomininkas atstovauja Office 365.

### <a name="development-environment"></a>Programavimo aplinka

Ne gamybos sandbox aplinka, naudojama plėtinių vystyti. Klientai šią aplinką įdiegia į savo „Azure" abonementą iš LCS. Šią aplinką taip pat galima naudoti demonstravimo, mokymo ar kitoms tikrinimo užduotims atlikti. Jis taip pat žinomas kaip [1 pakopos smėlio dėžė](../imp-lifecycle/environment-planning.md#tier-1-vs-tier-2-and-higher).

### <a name="downtime"></a>Prastova

Bet koks laikotarpis, kai vartotojai negali prisiregistruoti arba gauti prieigos prie savo aktyvaus nuomininko dėl nenaudotos platformos ar aptarnavimo infrastruktūros trikties, kaip nurodo „Microsoft" dėl automatizuoto sveikatos stebėjimo ir sistemos žurnalų. Downtime nėra suplanuoto prasto laiko, prie paslaugos papildomų funkcijų negalima prieiti, dėl jūsų pakeitimų ar laikotarpių, kai viršijamas svarstyklių vieneto pajėgumas.

### <a name="implementation-partner"></a>Diegimo partneris

Partneris, kurį klientas pasirenka, kad pritaikytų, konfigūruo galėtų pritaikyti, vykdyti ir valdyti savo finansų ir operacijų sprendimus.

### <a name="incident"></a>Incidentas

Problema, su kuriomis klientai susiduria, kai jie naudoja finansų ir operacijų tarnybą ir kad jie pateikia bilietą per LCS.

### <a name="microsoft-customer-support-services-css"></a>„Microsoft Customer Support Services“ ( CSS)

"Microsoft" visuotinė palaikymo komanda, skirta finansų ir operacijų programėlių kokybės paslaugai teikti.

### <a name="microsoft-dynamics-lifecycle-services-lcs"></a>Microsoft Dynamics„Lifecycle Services“ (LCS)

Vykdymo ciklo finansų ir operacijų programėlių administravimo portalas nuo bandomojo iki diegimo, iki gamybos valdymo ir palaikymo. Dėl daugiau informacijos, žr. [„Lifecycle Services“ ištekliai](../../dev-itpro/lifecycle-services/lcs.md).

### <a name="non-production-instance"></a>Ne gamybos egzempliorius

Bet kuris iš nurodytų tarnybos egzempliorių, kurį klientas naudoja plėtiniams tikrinti ir kitoms programavimo užduotims atlikti:

- **1 sandbox pakopa** – programuotojo egzempliorius (kliento nuomojamas)
- **Sandbox 2 pakopa** – standartinio priėmimo tikrinimo egzempliorius
- **3–5 pakopų smėlio dėžė** – įtraukti smėlio dėžės

Daugiau informacijos apie 2–5 pakopas ieškokite [Teisingos 2 arba naujesnės aplinkos pakopų pasirinkimas](../imp-lifecycle/environment-planning.md#selecting-the-correct-tier-2-or-higher-environment).

### <a name="production-instance"></a>Gamybos egzempliorius

Finansų ir operacijų aplinka, kurią klientas naudoja savo "tiesioginėms" kasdienės operacijos ir verslo procesams valdyti.

### <a name="sandbox-environment"></a>Smėlio dėžės aplinka

Ne gamybos aplinka, kurią klientas naudoja demonstravimo, mokymo, vartotojo priėmimo tikrinimo, plėtinių tikrinimo ir kitoms tikrinimo užduotims atlikti.

### <a name="service"></a>Aptarnavimas

Visos pagrindinės paslaugos, įtrauktos į finansų ir operacijų programėles.

### <a name="service-level-agreement-sla-for-microsoft-online-services"></a>„Microsoft" interneto paslaugų lygio sutartis (SLA)

SLA taikoma „Microsoft" interneto paslaugoms. Daugiau informacijos rasite faile [Paslaugų lygio sutartys](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

### <a name="service-update"></a>Paslaugos naujinimas

"Microsoft" paslaugų finansų ir operacijų aplinkos nuosekliai, vykdant aptarnavimo naujinimus. Klientai pagal savo verslo poreikius nustato savo aptarnavimo atnaujinimo kalendorių. Norėdami sužinoti daugiau, žr. [Senos versijos paslaugų naujinimai](../../dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="success-by-design"></a>[Success by Design](/dynamics365/fasttrack/success-by-design-overview)

Sistema, kuri sistema sistemiškai rodo vykdymą svarbiais etapais, siekiant užtikrinti Dynamics 365 sprendimo optimalią architektūrą, saugumą, našumą ir vartotojų patirtį.

### <a name="user"></a>Vartotojas

Vienas asmuo, kuris naudoja finansų ir operacijų aplinką ir kuris susijęs su kliento nuomininku.
