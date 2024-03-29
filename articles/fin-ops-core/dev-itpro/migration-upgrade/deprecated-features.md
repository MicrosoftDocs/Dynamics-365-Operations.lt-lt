---
title: Pašalintos arba nebenaudojamos funkcijos ankstesniuose leidimuose
description: Šiame straipsnyje aprašomos priemonės, kurios buvo pašalintos arba suplanuotos pašalinti iš Dynamics 365 for Finance and Operations ir ankstesniuose leidimuose.
author: sericks007
ms.date: 02/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea9355b040c6431f5ddcccc4aaa0de73e21ad299
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124565"
---
# <a name="removed-or-deprecated-features-in-previous-releases"></a>Pašalintos arba nebenaudojamos funkcijos ankstesniuose leidimuose

[!include [banner](../includes/banner.md)]



> [!IMPORTANT]
> Šis straipsnis nebenaujinamas. Norėdami matyti dabartinį funkcijų, kurios buvo pašalintos arba pasenusios iš finansų ir operacijų programėlių, sąrašą, ieškokite turinio "Pašalintos arba pasenusios funkcijos"**,** kuris susijęs su jūsų naudojama programa.

Šiame straipsnyje aprašomos priemonės, kurios buvo pašalintos arba pasenusios Dynamics 365 for Finance and Operations iš ir ankstesnių to produkto leidimų.

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Šis sąrašas skirtas suteikti jums informacijos apie pašalintas ir nebenaudojamas funkcijas, kad galėtumėte geriau planuoti savo darbą. 

Išsami informacija apie finansų ir operacijų programėlių objektus pateikta techninės [nuorodos ataskaitose](/dynamics/s-e/global/axtechrefrep_61). Galite palyginti skirtingas šių ataskaitų versijas ir sužinoti apie objektus, kurie buvo pakeisti ar pašalinti kiekvienoje finansų ir operacijų programėlių versijoje.

## <a name="finance-1007-with-platform-update-31"></a>„Finance“ 10.0.7 su „Platform update 31“

### <a name="chinese-voucher-types-without-account-groups-selection"></a>Kinijos kvitų tipai be sąskaitų grupių pasirinkimo
|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Pakeista į funkciją su sąskaitų grupių pasirinkimu. |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Programos |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nebenaudojama: nuo 2020 m. gruodžio 1 d. planuojame nebepalaikyti Kinijos kvitų tipų nustatymų be sąskaitų grupių pasirinkimo. Daugiau informacijos apie naujai sukurtas funkcijas žr. „Kas naujo 10.0.7 versijoje“ |

## <a name="finance-and-operations-1006-with-platform-update-30"></a>„Finance and Operations 10.0.6“ su „Platform update 30”


### <a name="dimensionhashgethashstr-_message"></a>DimensionHash.getHash(str _message)

|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | „Windows“ nebenaudoja SHA1, kaip dokumentuota [„Windows“ sprendimas dėl SHA1 sertifikatų](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx).  |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Programos |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nebenaudojamas: Nuo 2020 m. balandžio 1 d. kūrėjai turėtų naudoti API platformą esančią klasėje **„HasFunction“**. |

### <a name="hashcomputesha1hashstring-message"></a>Hash.ComputeSHA1Hash(string message)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | „Windows“ nebenaudoja SHA1, kaip dokumentuota [„Windows“ sprendimas dėl SHA1 sertifikatų](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx).  |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Platforma |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nebenaudojamas: Nuo 2020 m. balandžio 1 d. kūrėjai turėtų naudoti API platformą, esančią klasėje **„HasFunction“**. |


### <a name="formdatetimecontrolsetutcstring"></a>FormDateTimeControl.setUtcString()

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mes panaikiname metodą **setUtcString()**, nes galimas geresnis pakeitimo metodas. |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Platforma |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nebenaudojama: iki 2020 m. spalio 1 d. planuojame nebepalaikyti metodo **setUtcString()**. Kūrėjai turėtų naudoti metodą **setUtcDateTime()**. |

### <a name="blocklist-report-it--feature-reference-it-00001"></a>Blocklist ataskaita (IT) – priemonės nuorodos IT-00001

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | Nėra teisiškai reikalaujama. |
| **Pakeitė kita funkcija?**   | Ne |
| **Paveiktos produkto sritys**         | Italijos lokalizavimas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nebenaudojama: iki 2020 m. spalio 1 d. planuojame nebepalaikyti šios ataskaitos. |

### <a name="domestic-tax-report--feature-reference-it-00003"></a>Vietinių mokesčių ataskaita – funkcijos nuoroda IT-00003

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Nerekomendavimo / pašalinimo priežastis** | Nėra teisiškai reikalaujama. |
| **Pakeitė kita funkcija?**   | Ne |
| **Paveiktos produkto sritys**         | Italijos lokalizavimas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nebenaudojama: iki 2020 m. spalio 1 d. planuojame nebepalaikyti **vietinių mokesčių ataskaitos – funkcijos nuoroda IT-00003**. |

## <a name="october-2019-deprecation-announcement"></a>2019 m. spalio pranešimas apie netinkamumą

### <a name="flowchart-diagrams-in-business-process-modeler"></a>Struktūrinės schemos diagramos verslo procesų modeliavimo įrankyje

<table>
<tbody>
<tr>
<td><strong>Nebenaudojimo / pašalinimo priežastis</strong></td>
<td>Verslo procesų modeliavimo įrankio (BPM) struktūrinių schemų komponentas tampa nebenaudojamas, nes dėl senstelėjusio dizaino sumažėjo naudojimas.</td>
</tr>
<tr>
<td><strong>Pakeitė kita funkcija?</strong></td>
<td>Ne</td>
</tr>
<tr>
<td><strong>Paveiktos sritys</strong></td>
<td>Verslo procesų modeliavimo įrankis</td>
</tr>
<tr>
<td><strong>Būsena</strong></td>
<td>Nebenaudojama: tikimasi, kad BPM struktūrinės schemos diagramų komponentas bus pašalintas 2020 m. Toliau nurodytos funkcijos bus nepasiekiamos.
<ul>
<li>Visas struktūrines schemas bus galima tik skaityti. Jų redaguoti bus negalima. Formų ypatybės, susietos su struktūrinės schemos veiklomis, bus taip pat nepasiekiamos. Šios struktūrinės schemos apima ir numatytąsias struktūrines schemas, kurios yra automatiškai generuojamos, ir pritaikytas struktūrines schemas, modifikuojamas pagal minėtas numatytąsias struktūrines schemas.</li>
<li>Proceso veiksmus galite tik skaityti ir negalima jų redaguoti.</li>     
<li>Senstelėjusi tinkamumo / trūkumų analizės funkcija nebus pasiekiama. Todėl trūkumų sąrašas nebus automatiškai sukuriamas ir jo nebus galima eksportuoti.
<p><strong>Pastaba.</strong> Ši funkcija anksčiau tapo nebenaudojama ir ją pakeitė „Microsoft Azure DevOps“ integracijos.</p>
</li>
<li>Struktūrinių schemų versijų retrospektyva nebus pasiekiama.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="finance-and-operations-1005-with-platform-update-29"></a>„Finance and Operations 10.0.5“ su „Platform update 29”

### <a name="us-payroll-tax-updates"></a>JAV algalapių mokesčių atnaujinimai

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mes šaliname JAV algalapių mokesčių atnaujinimus dėl mažo naudojimo ir patobulintos funkcijos, kuri dabar siūloma per strateginę integraciją.  |
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Payroll |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nebenaudojama: iki 2024 m. liepos 31 d. planuojame daugiau nebeteikti mokesčių atnaujinimų JAV algalapių klientams. Funkcija išliks produkte, tačiau patobulinimai daugiau nebeatnaujins šios funkcijos ir bet kokie produkto defektai bus vertinami kiekvienu konkrečiu atveju. |

>[!NOTE]
> Tai nurodo pradinės 2021 m. spalio 1 d. nutraukimo datos pakeitimą. Norėdami gauti daugiau informacijos žr. [„Mokesčių atnaujinimai šalinami iš JAV algalapių funkcijos“ temoje Microsoft Dynamics 365 for Finance and Operations](https://aka.ms/financepayrollfaq).


### <a name="data-management-staging-clean-up"></a>Duomenų valdymo išdėstymo valymas
|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Neatitinka pagrindinių reikalavimų, kurių reikia planuojant periodinį valymą. |
| **Pakeitė kita funkcija?**   | Taip, užduočių retrospektyvos valymo funkcija yra įtraukiama, kad holistiškai atitiktų scenarijus. |
| **Paveiktos produkto sritys**         | Duomenų valdymas |
| **Visuotinio diegimo parinktis**              | Visos  |
| **Būsena**                         | Nebenaudojama. Tikslinis funkcijos pašalinimo laikotarpis – 2020 m. gruodžio mėn. |

## <a name="finance-and-operations-1004-with-platform-update-28"></a>„Finance and Operations 10.0.4“ su „Platform update 28”

### <a name="france-fec-accounting-data-export-in-xml"></a>Prancūzija: FEC apskaitos duomenų eksportavimas XML formatu

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | **Prancūzijos FEC audito failas**, kuris pakeistas TXT formatu, pasiekiamas pasirinkus **Didžioji knyga** \> **Periodinės užduotys** \> **Duomenų eksportavimas**.
| **Pakeitė kita funkcija?**   | Taip |
| **Paveiktos produkto sritys**         | Didžioji knyga |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nebenaudojama. Tikslinis funkcijos pašalinimo laikotarpis – 2020 m. liepos mėn. |


### <a name="legacy-navigation-bar"></a>Senesnių funkcijų naršymo juosta

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Antraštės lygiavimas su kitais „Dynamics“ ir „Office“ produktais. Norėdami daugiau informacijos žr. [Atnaujinta naršymo juosta, sulygiuota su „Office“ antrašte](/business-applications-release-notes/April19/dynamics365-finance-operations/updatednavbar).
| **Pakeitė kita funkcija?**   | Į 24 ir vėlesnius platformos naujinius įtraukta perkurta naršymo juosta, kurioje pateikta ieškos funkcija. |
| **Paveiktos produkto sritys**         | Žiniatinklio klientas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nebenaudojama: nuo 2020 m. balandžio mėn. senstelėjusios naršymo juostos nebebus galima naudoti. Iki tol klientai gali perjungti į senstelėjusią naršymo juostą naudodami puslapį **Kliento našumo parinktys**. |


## <a name="finance-and-operations-1002-with-platform-update-26"></a>„Finance and Operations 10.0.2“ su „Platform update 26”


### <a name="legacy-default-action-behavior"></a>Senesnis numatytųjų veiksmų veikimas

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Dėl senesnio tinklelių numatytųjų veiksmų veikimo numatytasis veiksmo saitas personalizuojant pertvarkius tinklelio stulpelius atsiranda nenumatytame stulpelyje. Tai ištaiso naujoji „priklijuojamųjų“ numatytųjų veiksmų funkcija. Norėdami gauti daugiau informacijos, žr. [„Priklijuojamieji“ numatytieji veiksmai tinkleliuose](/business-applications-release-notes/October18/dynamics365-finance-operations/sticky-default-action). |
| **Pakeitė kita funkcija?**   | Nuo „Platform Update 21“ buvo įdiegta „priklijuojamųjų” numatytųjų veiksmų funkcija. Šią funkciją galima įjungti puslapyje **Kliento našumo parinktys**. |
| **Paveiktos produkto sritys**         | Tinkleliai žiniatinklio kliente |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nerekomenduojama. Nuo 2020 m. balandžio mėn. numatytasis veikimo būdas bus „priklijuojamieji“ numatytieji veiksmai ir nebus mechanizmo grąžinti senesnio veikimo būdo. |

### <a name="legacy-is-one-of-filtering-experience"></a>Senesnė filtravimo patirtis „vienas iš“

|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Naujinime „Platform Update 22“ filtravimo patirtis „vienas iš“ buvo pertvarkyta; planuojama, kad ilgainiui ji bus vienintelė tokia filtravimo patirtis. |
| **Pakeitė kita funkcija?**   | Nuo „Platform Update 22“ puslapyje **Kliento našumo parinktys** galima naudoti patobulintą filtravimo patirtį „vienas iš“. Norėdami gauti daugiau informacijos, žr. [Optimizuota filtravimo patirtis „vienas iš“](/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering). |
| **Paveiktos produkto sritys**         | Žiniatinklio klientas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nerekomenduojama. Nuo 2020 m. balandžio mėn. numatytasis veikimo būdas bus patobulinta patirtis „vienas iš“ ir nebus mechanizmo grąžinti senesnio veikimo būdo. |

### <a name="parameter-to-enable-sales-orders-with-multiple-project-contract-funding-sources"></a>Parametras, kuriuo įjungiami pardavimo užsakymai su keliais projekto sutarties lėšų skyrimo šaltiniais
Projektinių pardavimo užsakymų, kuriuose projekto sutartis turi kelis lėšų skyrimo šaltinius, palaikymas įjungiamas puslapio **Projektų valdymo parametrai** parametru **Leisti projekto su keliais lėšų skyrimo šaltiniais pardavimo užsakymus**. Pagal numatytuosius parametrus šis parametras nėra įjungtas. 

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Parametrą pašalinus, ši funkcija visada bus įjungta. |
| **Pakeitė kita funkcija?**   | Ne. Projektinių pardavimo užsakymų su keliais lėšų skyrimo šaltiniais palaikymo funkcija visada bus įjungta.   |
| **Paveiktos produkto sritys**         |Parametras **Leisti projekto su keliais lėšų skyrimo šaltiniais pardavimo užsakymus** bus pašalintas. Pašalinus parametrą bus modifikuoti šie metodai: klasės **ProjStatusType** metodas **ctrlSalesOrderTable**, lauko **ProjId** metodas **validate** ir formos **SalescreateOrder** metodas **run**. Pašalinus parametrą, šie metodai bus nerekomenduojami: **IsSalesOrderAllowedForMultipleFundingSources** lentelės faile **ProjTable**, lentelės failo **ProjTable** metodas **IsAllowSalesOrdersForMultipleFundingSourcesParamEnabled**, formos **ProjParameters** ir failų **ProjParameterEntity** duomenų laukas **AllowSalesOrdersForMultipleFundingSources**, lentelės failo **ProjTable** privatusis metodas **IsAssociatedToMultipleFundingSourcesContract**. |
| **Visuotinio diegimo parinktis**              | Visos  |
| **Būsena**                         | Planuojama, kad šie metodai nebebus rekomenduojami nuo 2020 m. balandžio mėn. leidimų bangos. |

### <a name="legacy-workflow-reports-for-tracking-and-instance-status"></a>Senesnės sekimo ir egzempliorių būsenos darbo eigų ataskaitos

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Senesnės sekimo ir egzempliorių būsenos darbo eigų ataskaitos neberekomenduojamos, nes jos nebenurodomos naršant. Ataskaitos vadinasi WorkflowWorkflowInstanceByStatusReport ir WorkflowWorkflowTrackingReport. |
| **Pakeitė kita funkcija?**   | Vietoj jų galima naudoti darbo eigos retrospektyvos formą. |
| **Paveiktos produkto sritys**         | Žiniatinklio klientas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nerekomenduojama: tikslinis funkcijos pašalinimo laikotarpis – 2020 m. balandžio mėn. |

## <a name="finance-and-operations-1001-with-platform-update-25"></a>„Finance and Operations 10.0.1“ su „Platform update 25”

### <a name="deprecated-apis-and-potential-breaking-changes"></a>Nebenaudojami API ir gedimus galintys sukelti pakeitimai


#### <a name="deriving-from-internal-classes-is-deprecated"></a>Išvedimas iš vidinių klasių nebenaudojamas

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Iki „Platform Update 25“ buvo galima sukurti klasę arba lentelę, kuri išvedama iš vidinės klasės / lentelės, apibrėžtos kitame pakete / modulyje. Tai nėra saugi kodavimo praktika. Nuo „Platform Update 25” kompiliatorius rodys įspėjimą. |
| **Pakeitė kita funkcija?**   | Naujinime „Platform Update 26“ kompiliatoriaus įspėjimas bus pakeistas į klaidą. Paleidimo metu šis pakeitimas yra suderinamas su ankstesnėmis sistemomis, o tai reiškia, kad „Platform Update 25“ ar naujesnį naujinimą galima įdiegti bet kurioje smėlio dėžėje arba gamybos aplinkoje – pasirinktinio kodo keisti nereikia. Šis pakeitimas taikomas tik programavimo ir kompiliavimo laikui.|
| **Paveiktos produkto sritys**         | „Visual Studio“ kūrimo įrankiai |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nerekomenduojama. Naujinime „Platform Update 26“ įspėjimas bus pakeistas į kompiliavimo klaidą. |

#### <a name="overriding-internal-methods-is-deprecated"></a>Vidinių metodų perrašymas nebenaudojamas

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Iki „Platform Update 25“ buvo galima vidinį metodą perrašyti išvestoje klasėje, kuri apibrėžta kitame pakete / modulyje. Tai nėra saugi kodavimo praktika. Nuo „Platform Update 25” kompiliatorius rodys įspėjimą. |
| **Pakeitė kita funkcija?**   | Naujinime „Platform Update 26“ šis įspėjimas bus pakeistas į kompiliavimo klaidą. Paleidimo metu šis pakeitimas yra suderinamas su ankstesnėmis sistemomis, o tai reiškia, kad „Platform Update 25“ ar naujesnį naujinimą galima įdiegti bet kurioje smėlio dėžėje arba gamybos aplinkoje – pasirinktinio kodo keisti nereikia. Šis pakeitimas taikomas tik programavimo ir kompiliavimo laikui. |
| **Paveiktos produkto sritys**         | „Visual Studio“ kūrimo įrankiai |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nerekomenduojama. Naujinime „Platform Update 26“ įspėjimas bus pakeistas į kompiliavimo klaidą. |

## <a name="finance-and-operations-1000-with-platform-update-24"></a>„Finance and Operations 10.0.0“ su „Platform update 24”

### <a name="renaming-released-products"></a>Išleistų produktų pervardijimas 
| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Kai naudojate funkciją **Pervadinti pirminį raktą**, kad pakeistumėte išleisto produkto „ItemId“, atnaujinamos tik tiesioginės išorinio rakto nuorodos. Visos kitos išleisto produkto nuorodos, pvz., iš gamybos užsakymų, išlaikys seną „ItemId“. Dėl to duomenys gali būti nenuoseklūs, o tai ilgainiui gali blokuoti verslo procesus. |
| **Pakeitė kita funkcija?**   | Ne. |
| **Paveiktos produkto sritys**         | Produkto informacijos valdymas |
| **Visuotinio diegimo parinktis**              | Visos  |
| **Būsena**                         | Pašalinta iš „Finance and Operations 10.0.0“ su „Platform update 24”.|


## <a name="finance-and-operations-813-with-platform-update-23"></a>„Finance and Operations 8.1.3“ su „Platform update 23”

### <a name="sql-server-reporting-services-reportviewer-control"></a>„SQL Server Reporting Services“ valdiklis ReportViewer
Klientai gali naudoti veiksmą **Eksportuoti**, pateiktą įdėtajame „SQL Server Reporting Services“ (SSRS) valdiklyje ReportViewer, kad atsisiųstų dokumentų, kuriuos sugeneravo „Finance and Operations“ programos. Ši HTML pagrįsta ataskaitos pateiktis vartotojams siūlo nesunumeruotą dokumento peržiūrą.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | HTML pagrįsta nesunumeruota peržiūros sąsaja **neužtikrina** tikslumo lyginant su faktiniais dokumentais, kuriuos galiausiai sugeneruoja „Finance and Operations“. Naudodami PDF kaip standartinį verslo dokumentų formatą ir kurdami programų ataskaitas vartotojai gali išnaudoti šiuolaikiškas peržiūros galimybes ir būti našesni. |
| **Pakeitė kita funkcija?**   | Žvelgiant į ateitį, PDF dokumentai bus numatytasis „Finance and Operations“ generuojamų ataskaitų formatas.   |
| **Paveiktos produkto sritys**         | Šis pakeitimas **netaikomas** klientų scenarijuose, kai ataskaitos paskirstomos elektroniniu būdu arba siunčiamos tiesiogiai į spausdintuvus.    |
| **Visuotinio diegimo parinktis**              | Visos  |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. Automatinės programų ataskaitų peržiūros naudojant įdėtąją PDF peržiūros programą funkciją planuojama įtraukti į 2019 m. gegužės mėn. „Platform Update“. |

### <a name="client-kpi-controls"></a>Kliento KPI valdikliai
Įdėtuosius pagrindinius efektyvumo indikatorius (KPI) sistemoje „Visual Studio“ gali modeliuoti kūrėjas ir toliau tinkinti galutinis vartotojas.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Vietinius kliento valdiklius, naudojamus KPI apibrėžti, klientai naudoja retai, ir kūrėjai turi įtraukti sekamą metriką. |
| **Pakeitė kita funkcija?**   | PowerBI.com paslauga pristato aukštos klasės įrankius, skirtus nustatyti ir valdyti KPI, remiantis duomenimis iš išorinių šaltinių.  Būsimame leidime planuojame suteikti galimybę įdėti sprendimus, nuomojamus PowerBI.com, į programos darbo sritis.   |
| **Paveiktos produkto sritys**         | Šis naujinimas neleis kūrėjams įtraukti naujų KPI valdiklių į „Visual Studio“ dizaino įrankį.    |
| **Visuotinio diegimo parinktis**              | Visos  |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |

### <a name="deprecated-apis-and-future-breaking-changes"></a>Nebenaudojami API ir būsimi gedimus sukeliantys pakeitimai

#### <a name="field-groups-containing-invalid-field-references"></a>Laukų grupės, kuriose pateiktos netinkamos laukų nuorodos

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Lentelės metaduomenų aprašuose gali būti laukų grupių, kuriose yra netinkamų laukų nuorodų. Įdiegus gali kiti leidimo laiko gedimų finansinėse ataskaitose ir „SQL Server Reporting Services“ (SSRS). Šiuo metu ši problema klasifikuojama kaip *kompiliatoriaus įspėjimas*, o ne *klaida*, o tai reiškia, kad diegiamo paketo kūrimą ir diegimą galima tęsti neištaisius problemos. Kaip išspręsti šią problemą<br><br>1. Pašalinkite netinkamą lauko nuorodą iš lentelės lauko grupės aprašo.<br><br>2. Perkompiliuokite.<br><br>3. Įsitikinkite, kad pašalinti visi įspėjimai arba klaidos. |
| **Pakeitė kita funkcija?**   | Ateityje šis įspėjimas bus pakeistas į kompiliavimo klaidą. |
| **Paveiktos produkto sritys**         | „Visual Studio“ kūrimo įrankiai |
| **Visuotinio diegimo parinktis**              | Visi / Viskas |
| **Būsena**                         | Pasenusi: įspėjimas yra finansų ir operacijų programėlių 10.0.11 versijos platformos naujinimų kompiliavimo klaida. |

#### <a name="complete-list"></a>Visas sąrašas
Norėdami pasiekti visą nebenaudojamų API sąrašą, žr. [Metodų ir metaduomenų elementų nebenaudojimas](deprecation-deletion-apis.md).

## <a name="finance-and-operations-81-with-platform-update-20"></a>„Finance and Operations 8.1“ su „Platform update 20”

### <a name="batch-transfer-rules-for-subledger-journal-account-entries"></a>Papildomos knygos žurnalo sąskaitų įrašų paketo perkėlimo taisyklės
DK parametruose sinchroninio perkėlimo režimas nebenaudojamas.  Šis režimas pakeičiamas nesinchroniniu ir skirtu tik suplanuotam paketui, o šios parinktys jau naudojamos perkeliant. Norėdami gauti papildomos informacijos, žr. tinklaraštį [Didžiosios knygos parametrai – paketų perkėlimo taisyklės](https://community.dynamics.com/365/financeandoperations/b/financials/archive/2019/03/15/general-ledger-parameters-batch-transfer-rules).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Sinchroninę parinktį pašalinsime, kadangi ji gali turėti įtakos sistemos efektyvumui. |
| **Pakeitė kita funkcija?**   | Vietoje sinchroninės parinkties naudojamos nasinchroninė ir suplanuoto paketo parinktys.   |
| **Paveiktos produkto sritys**         | DK, mokėtinos sumos, gautinos sumos, įsigijimas, išlaidos    |
| **Visuotinio diegimo parinktis**              | Visos  |
| **Būsena**                         | Nebenaudojama: tikslinis funkcijos pašalinimo laikotarpis yra 10.0 versija.|

### <a name="electronic-reporting-for-russia"></a>Rusijos elektroninės ataskaitos
Funkcija, skirta konfigūruoti deklaracijų .txt ir .xml failų formatus. 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Pakeista elektroninėmis ataskaitomis. |
| **Pakeitė kita funkcija?**   | Taip. |
| **Paveiktos produkto sritys**         | Didžioji knyga |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Pašalinta iš „Finance and Operations 8.1“ su „Platform update 20”. |

### <a name="financial-reports-generator-for-russia"></a>Rusijos finansinių ataskaitų generatorius
Įrankis, skirtas apskaitos ir mokesčių ataskaitų duomenų rinkiniui nustatyti ir duomenims į XLS ir DOC ataskaitų šablonus eksportuoti. Funkcinės dalys: duomenų eksportavimas į XLS ir DOC ataskaitų šablonus, užklausos, fiksuotieji rekvizitai pašalinami. 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Pašalintos dalys pakeičiamos elektroninėmis ataskaitomis. |
| **Pakeitė kita funkcija?**   | Taip. Finansinių ataskaitų sąrankos vartotojo sąsaja turėtų būti naudojama norint nustatyti DK sąskaitų ir mokesčių registrų duomenų rinkimo taisykles. Duomenų eksportavimo į įvairių tipų failus, fiksuotųjų rekvizitų ir į užklausas panašių duomenų rinkimo taisyklės turėtų būti konfigūruojamos elektroninėse ataskaitose. |
| **Paveiktos produkto sritys**         | Didžioji knyga. |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Pašalinta iš „Finance and Operations 8.1“ su „Platform update 20”. |

### <a name="integration-with-external-providers-for-sending-electronic-reporting-through-communication-channels-for-russia"></a>Integravimas su išoriniais tiekėjais siekiant elektronines ataskaitas siųsti Rusijos ryšio kanalais
Eksportuojant funkciją aplanke sukurti elektroniniai deklaracijų failai, kad vėliau juos būtų galima išsiųsti oficialiems elektroninių ataskaitų teikėjams, taip pat importuoti būseną.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Pakeista konfigūruojama elektroninių pranešimų funkcija. |
| **Pakeitė kita funkcija?**   | Taip.  |
| **Paveiktos produkto sritys**         | Didžioji knyga, mokestis |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Pašalinta iš „Finance and Operations 8.1“ su „Platform update 20”. |


### <a name="profit-tax-register-wizard"></a>Pelno mokesčio registro vedlys
Funkcija, skirta naujiems pelno mokesčio registrų šablonams kurti. Ši funkcija sukuria naujų registrų X++ objektus, kurie vėliau kuriami kaip šablonai su įtraukta atitinkama skaičiavimo logika.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Funkcija nesuderinama su „Finance and Operations“ išplėtimo modeliu. |
| **Pakeitė kita funkcija?**   | Ne |
| **Paveiktos produkto sritys**         | Mokesčiai |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Pašalinta iš „Finance and Operations 8.1“ su „Platform update 20”. |

### <a name="payroll-and-human-resources-for-russia"></a>Rusijos atlyginimų ir personalo valdymas
Rusijos šaliai skirtas modulis, skirtas darbuotojų administravimo informacijai valdyti, darbuotojų tabelio informacijai, atlyginimų apskaitai ir mokėjimo išrašų sukūrimui. 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo / pašalinimo priežastis** | Algalapis neįtrauktas į „Dynamics 365“ visuotinį strateginį židinį. Partneriai ir ISV – tai geriausia vieta, kad būtų galima teikti algalapio funkcijas, atitinkančias vietinius nuostatus ir mokesčių atnaujinimus.|
| **Pakeitė kita funkcija?**   | Ne|
| **Paveiktos produkto sritys**         | Rusijos atlyginimų ir personalo išteklių valdymas |
| **Visuotinio diegimo parinktis**              | Visos |
| **Būsena**                         | Nebenaudojama: tikslinis funkcijos pašalinimo laikotarpis yra 10.0 versija ir ateities naujinimai. |

## <a name="finance-and-operations-80-with-platform-update-15"></a>„Finance and Operations 8.0“ su „Platform update 15”
Iš šio leidimo nebuvo pašalintos jokios funkcijos ir visos jos yra tebenaudojamos. 15 platformos naujinimas yra kaupiamasis ir jame pateikiamos naujos arba pakeistos 13 platformos naujinimo, 14 platformos naujinimo ir 15 platformos naujinimo funkcijos.

## <a name="finance-and-operations-enterprise-edition-73-with-platform-update-12"></a>„Finance and Operations, Enterprise edition 7.3“ su „Platform update 12”

### <a name="personalized-product-recommendations"></a>Personalizuotų produktų rekomendacijos 
Nuo 2018 m. vasario 15 d. mažmenininkai nebegalės rodyti personalizuotų produktų rekomendacijų elektroninio kasos aparato (EKA) įrenginyje. Išsamesnės informacijos žr. [Produktų rekomendacijų apžvalga](../../../commerce/product-recommendations.md).  

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Pašalinsime dabartinę produktų rekomendavimo paslaugos versiją ir šią funkciją pertvarkysime, suteikdami jai geresnį algoritmą ir naujesnes į mažmeninę prekybą orientuotas galimybes.  |
| **Pakeitė kita funkcija?**   | Ne Tačiau po 2018 m. pavasario planuojame šią funkciją sugrąžinti su nauja rekomendacijų paslauga.   |
| **Paveiktos produkto sritys**         | Personalizuotos produktų rekomendacijos EKA.                                                    |
| **Visuotinio diegimo parinktis**              | Visos                                                                                      |
| **Būsena**                         |Pašalinta nuo 2018 m. vasario 15 d. Tai turės įtakos klientams, naudojantiems „Dynamics 365 for Operations 1611“ ir vėlesnes versijas.  |

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a>Elektroninių ataskaitų (ER) funkcijų sąrašo išplėtimas
Pasirinktinių funkcijų įtraukti norint naudoti ER išraiškos daryklė (daugiau informacijos žr. [Elektroninių ataskaitų (ER) funkcijų sąrašo išplėtimas](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)) nebegalima. Pasikeitus ER API, API, skirti įtaisytąsias funkcijas iš ER išraiškos daryklės iškviesti, tapo vidiniais ir jų nebegalima išplėsti.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Kodo antspaudavimo iniciatyva  |
| **Pakeitė kita funkcija?**   | Nėra. Kai reikalinga nauja įtaisytoji funkcija, naują išplėtimo užklausą reikia skirti ER sistemos komandai.<br><br>Kol ER komanda kuria pageidaujamą funkciją, šią problemą galima laikinai išspręsti – reikalingą logiką galima suprogramuoti kaip pasirinktinės programos klasės metodą. Šį metodą galima pasiekti ER išraiškoje kaip įtraukto ER duomenų šaltinio, kurio tipas **Programa \ klasė**, ypatybę, nurodančią tą pasirinktinę programos klasę.  |
| **Paveiktos produkto sritys**         | Elektroninių ataskaitų sistema                                                      |
| **Visuotinio diegimo parinktis**              | Visos                                                                                      |
| **Būsena**                         | Pašalinta iš „Finance and Operations, Enterprise edition 7.3‟.    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a>Atsargos pagal prekių grupę ir atsargos pagal atsargų dimensijų skirstymo pagal terminus ataskaitas

Šios dvi ataskaitos nebepalaikomos „Finance and Operations“. Vietoje to galima naudoti ataskaitą **Atsargų skirstymas pagal terminus**, norint pagerinti vartotojų patirtį.

| &nbsp;  | &nbsp; |
|--------------|-----------------------|
| **Nebenaudojimo priežastis**       | Besidubliuojančios funkcijos  |
| **Pakeitė kita funkcija?** | Taip. Abi ataskaitas pakeitė ataskaita **Atsargų skirstymas pagal terminus**.     |
| **Paveiktos produkto sritys**       | Atsargų valdymas, išlaidų valdymas        |
| **Visuotinio diegimo parinktis**        | Visos|
| **Būsena**                       | Nebenaudojama: abiejų ataskaitų meniu elementai buvo pašalinti iš 7.3 versijos. Tačiau į produktą vis dar įtrauktas ataskaitų kodas. Kodą planuojama pašalinti iš būsimo leidimo. |

### <a name="power-bi-content-packs-available-on-appsource"></a>„Power BI“ turinio paketai, prieinami „AppSource“
Turinio paketai **Išlaidų valdymas**, **Finansinė veikla** ir **Retail Channel Performance**, prieinami svetainėje [Microsoft AppSource](https://appsource.microsoft.com), yra nebenaudojami dėl „Microsoft Power BI“ produkto naujinių. Sistemos administravimo formos, naudojamos šiems turinio paketams PowerBI.com diegti, taip pat yra nebenaudojami „Finance and Operations“.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nerekomendavimo/pašalinimo priežastis** | „Microsoft Power BI“ produkto naujiniai. |
| **Pakeitė kita funkcija?**   | Turinio paketai **Išlaidų valdymas**, **Finansinė veikla** ir **Retail Channel Performance**, prieinami svetainėje [AppSource](https://appsource.microsoft.com), keičiami analizės programomis, kurios suteikia galimybę integruoti sprendimą duomenų bazės lygiu. Daugiau informacijos apie analizės programas žr. [Įdėtosios „Power BI“ darbo sritys](../../dev-itpro/analytics/embed-power-bi-workspaces.md).    |
| **Paveiktos produkto sritys**         | Išlaidų valdymas, „Finance“ ir „Retail“                                                                                               |
| **Visuotinio diegimo parinktis**              | Tik debesyje (integravimas su PowerBI.com nepalaikomas vietinėse įdiegtyse.)                                                                                                            |
| **Būsena**                         | Nebenaudojama: tikslinis funkcijos pašalinimo laikotarpis – 2018 m. antrasis ketvirtis.    |

### <a name="standard-ui-in-data-management-workspace"></a>Standartinė duomenų valdymo darbo srities vartotojo sąsaja

Standartinė duomenų valdymo vartotojo sąsaja yra senesnė vartotojo sąsaja, kuri yra numatytoji vartotojo sąsaja, vartotojams rodoma, kai jie apsilanko duomenų valdymo darbo srityje.

| &nbsp;  | &nbsp; |
|------------------|-------------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Investuojame į naujas vartotojo patirtis naujoje vartotojo sąsajoje.             |
| **Pakeitė kita funkcija?**   | Naujoji vartotojo sąsaja, vadinama *Patobulinti rodiniai*, keičia senąją vartotojo sąsają.            |
| **Paveiktos produkto sritys**         | Duomenų valdymo darbo sritis                                                     |
| **Visuotinio diegimo parinktis**              | Visos                                                                           |
| **Būsena**                         | Nebenaudojama: tikslinis funkcijos pašalinimo laikotarpis – 2018 m. antrasis ketvirtis. |

### <a name="excise-sales-tax-service-tax-for-india"></a>Akcizas, PVM, paslaugų mokestis (Indija)

Šie mokesčiai įtraukti į Indijos GST.

|  &nbsp;                                           |      &nbsp;                                                                   |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Pašalinimo arba nebenaudojimo priežastis**       | Šie mokesčiai įtraukti į Indijos GST.                          |
| **Pakeitė kita funkcija?**            | Indijos GST                                                              |
| **Paveiktos produkto sritys**                  | Mokesčiai                                                                     |
| **Visuotinio diegimo parinktis**                       | Visi moduliai                                                   |
| **Būsena**                                  | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |    

### <a name="file-validation-utility-fvu-for-india"></a>Failo tikrinimo priemonė (FVU), Indija

|              &nbsp;                               |      &nbsp;                                                                   |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Pašalinimo arba nebenaudojimo priežastis**       | Naudojo mažai klientų                                                  |
| **Pakeitė kita funkcija?**            | Ne                                                                      |
| **Paveiktos produkto sritys**                  | Indijos išskaitomas mokestis                                                  |
| **Visuotinio diegimo parinktis**                       | Visi moduliai                                                                    |
| **Būsena**                                  | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.   |        

### <a name="tdstcs-certificate-for-india"></a>Indijos TDS / TKS sertifikatas

Vartotojai gali tai atsisiųsti iš vyriausybės portalo.

|             &nbsp;                                |    &nbsp;                                                                     |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Pašalinimo arba nebenaudojimo priežastis**       | Naudojo mažai klientų                                                  |
| **Pakeitė kita funkcija?**            | Ne                                                                      |
| **Paveiktos produkto sritys**                  | Indijos išskaitomas mokestis                                                  |
| **Visuotinio diegimo parinktis**                       | Visi moduliai                                                                   |
| **Būsena**                                  | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a>Indijos eksportavimo / importavimo (EXIM) paskatinimo schema


|              &nbsp;                               |        &nbsp;                                                                 |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Pašalinimo arba nebenaudojimo priežastis**       | Naudojo mažai klientų                                                  |
| **Pakeitė kita funkcija?**            | Ne                                                                      |
| **Paveiktos produkto sritys**                  | Importuoti ir eksportuoti                                                       |
| **Visuotinio diegimo parinktis**                       | Visi moduliai                                                                    |
| **Būsena**                                  | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.  |    


## <a name="dynamics-365-for-retail-72"></a>„Dynamics 365 for Retail 7.2“

### <a name="personalized-product-recommendations"></a>Personalizuotų produktų rekomendacijos 
Nuo 2018 m. vasario 15 d. mažmenininkai nebegalės rodyti personalizuotų produktų rekomendacijų elektroninio kasos aparato (EKA) įrenginyje. Išsamesnės informacijos žr. [Produktų rekomendacijų apžvalga](../../../commerce/product-recommendations.md).  

|  &nbsp; |  &nbsp;|
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Pašalinsime dabartinę produktų rekomendavimo paslaugos versiją ir šią funkciją pertvarkysime, suteikdami jai geresnį algoritmą ir naujesnes į mažmeninę prekybą orientuotas galimybes.  |
| **Pakeitė kita funkcija?**   | Ne Tačiau po 2018 m. pavasario planuojame šią funkciją sugrąžinti su nauja rekomendacijų paslauga.   |
| **Paveiktos produkto sritys**         | Personalizuotos produktų rekomendacijos EKA.                                                    |
| **Visuotinio diegimo parinktis**              | Visos                                                                                      |
| **Būsena**                         |Pašalinta nuo 2018 m. vasario 15 d. Tai turės įtakos klientams, naudojantiems „Dynamics 365 for Retail 7.2“ ir vėlesnes versijas. |


## <a name="finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>„Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.) su „Platform update 8”

### <a name="currency-conversion-for-accounting-and-reporting-currencies"></a>Valiutos konvertavimas, skirtas apskaitos ir ataskaitų valiutoms

Valiutos konvertavimas, skirtas apskaitai ir ataskaitų valiutoms, buvo įdiegtas įvedus eurą.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Ribotas funkcijos Kopijuoti juridinį subjektą naudojimas ir įtraukimas kaip pakaitalas.      |
| **Pakeitė kita funkcija?**   | Ne, bet funkcijos Kopijuoti juridinį subjektą ir Konfigūracijos buvo įtrauktos tam, kad būtų lengviau perkelti į įmonę, kuri pakeitė pagrindinius reikalavimus. |
| **Paveiktos produkto sritys**         | Finansų valdymas     |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.   |


### <a name="warehouse-mobile-devices-portal"></a>Sandėlio mobiliųjų įrenginių portalas

Sandėlio mobiliųjų įrenginių portalas (WMDP) buvo atskiras komponentas, kuris buvo skirtas vietiniam savarankiškam diegimui. Šis komponentas nebepalaikomas „Finance and Operations“. Vietinė vartotojo patirtį pagerinanti programa pakeitė WMDP funkcijas.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Besidubliuojančios funkcijos.       |
| **Pakeitė kita funkcija?**   | Taip. Šią funkciją pakeitė „Finance and Operations“ – versija „Warehousing“. Norėdami gauti daugiau informacijos apie sąranką ir būtinąsias sąlygas, žr. [Sandėliavimo programos diegimo ir konfigūravimo apžvalga](../../../supply-chain/warehousing/install-configure-warehousing-app.md). |
| **Paveiktos produkto sritys**         | Sandėlio valdymas, transportavimo valdymas     |
| **Visuotinio diegimo parinktis**              | Sandėlio mobiliųjų įrenginių portalas (WMDP) buvo atskiras komponentas, kuris buvo skirtas vietiniam savarankiškam diegimui.               |
| **Būsena**                         | Nebenaudojama: tikslinis funkcijos pašalinimo laikotarpis – 2019 m. 4 ketvirtis.   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Pažangaus banko derinimo ir rankinio gretinimo taisyklė

Gretinimo taisyklė buvo naudojama norint pasirinkti ir pažymėti banko dokumentą rankiniu būdu gretinant dokumentus suderinimo darbalapyje.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Ribotas naudojimas.                                                                         |
| **Pakeitė kita funkcija?**   | Ne. Stulpelio filtravimo galimybės turėtų būti naudojamos norint surasti suderinimui skirtus dokumentus. |
| **Paveiktos produkto sritys**         | Grynųjų pinigų ir banko valdymas                                                               |
| **Visuotinio diegimo parinktis**              | Visos                                                                                    |
| **Būsena**                         | Pašalinta 2017 m. liepos mėn.                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a>„Dynamics 365 for Operations 1611“ su „Platform Update 3“

### <a name="aeb-payment-formats-for-spain"></a>AEB mokėjimo formatai, skirti Ispanijai

Consejo Superior Bancario mokėjimo formatai buvo naudojami siunčiant kliento ir tiekėjo mokėjimų pavedimo failus į banką. Šių formatų turinį nustatė Asociación Española de Banca. Ji apima Cuaderno 19, 32, 58, 34.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mokėjimo formatai nebenaudojami.                                  |
| **Pakeitė kita funkcija?**   | Taip, ISO20022 kredito pervedimo ir tiesioginio debeto mokėjimo formatai, skirti Ispanijai |
| **Paveiktos produkto sritys**         | Mokėtinos sumos, gautinos sumos                                    |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.           |

### <a name="bank-payments-transfer-for-lithuania"></a>Banko mokėjimų perkėlimas, skirtas Lietuvai

Banko mokėjimų pervedimai buvo generuojami ir spausdinami naudojant Lietuvos mokėjimo pervedimo (LT) eksportavimo formatą. Lietuvos rinkoje 2005 m. pradėta naudoti LITAS, suvienodinta elektroninės bankininkystės sistema.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mokėjimo formatai nebenaudojami.                        |
| **Pakeitė kita funkcija?**   | Taip, ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Lietuvai     |
| **Paveiktos produkto sritys**         | Mokėtinos sumos                                               |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>BBS „Direkte Remittering“ mokėjimo formatai, skirti Norvegijai

BBS „Direkte Remittering“ mokėjimo formatai apima kliento mokėjimų rinkinio eksportavimą (tiesioginis debetas) ir grąžinimo pranešimo importavimą.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mokėjimo formatai nebenaudojami.  |
| **Pakeitė kita funkcija?**   | „AvtaleGiro“ kliento mokėjimų formatą, skirtą Norvegijai, galima naudoti norint generuoti tiesioginio debeto pranešimus. Grąžinimo pranešimo importavimo funkciją bus galima naudoti būsimuose leidimuose. |
| **Paveiktos produkto sritys**         | Mokėtinos sumos, gautinos sumos   |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a>Sąskaitų plano įrankis, skirtas Ispanijai

Šis įrankis naudojama, kai sąskaitų plane, skirtame Ispanijai, reikia atlikti didelių keitimų. Vartotojai gali importuoti naują sąskaitų planą, naudodami „Microsoft Excel“ arba teksto formatu, ir taip pat gali importuoti finansines ataskaitas.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Ribotas naudojimas                                                  |
| **Pakeitė kita funkcija?**   | Ne                                                             |
| **Paveiktos produkto sritys**         | DK                                                 |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |

### <a name="dom80-payment-format-for-belgium"></a>„Dom80“ mokėjimo formatas, skirtas Belgijai

Senesnės versijos Belgijos mokėjimų rinkinio mokėjimo formatas (tiesioginis debetas).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mokėjimo formatas nebenaudojamas.                          |
| **Pakeitė kita funkcija?**   | Taip, ISO 20022 tiesioginio debeto mokėjimo formatas, skirtas Belgijai         |
| **Paveiktos produkto sritys**         | Gautinos sumos                                            |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA / EZAG mokėjimo formatai, skirti Šveicarijai

ATM / EZAG formatai yra integruoti į ESR sistemą, nes jie turi nuorodos numerius. Nuorodos numeriai nėra būtini, todėl naudojant šiuos formatus galima apdoroti bet kurį tiekėjo mokėjimą. Šiuos formatus naudoja įmonės, turinčios ne „Postfinance“ esančias banko sąskaitas.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mokėjimo formatai nebenaudojami.                        |
| **Pakeitė kita funkcija?**   | Taip, ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Šveicarijai   |
| **Paveiktos produkto sritys**         | Mokėtinos sumos                                               |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>EDIFACT-DIRDEB tiesioginio debeto mokėjimo formatas, skirtas Austrijai

EDIFACT-DIRDEB mokėjimų rinkinio mokėjimo formatas (tiesioginis debetas).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mokėjimo formatas nebenaudojamas.                          |
| **Pakeitė kita funkcija?**   | Taip, ISO 20022 tiesioginio debeto mokėjimo formatas, skirtas Austrijai         |
| **Paveiktos produkto sritys**         | Gautinos sumos                                            |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |

### <a name="edivat-for-belgium"></a>EDIVAT, skirtas Belgijai

EDIVAT yra pasenęs Belgijos elektroninių deklaracijų teikimo saugiu paštu standartas. „Dynamics AX 2012“ lieka tik skaitymo sprendimas, kad būtų galima prieiga prie retrospektyvos duomenų.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Funkcija nebenaudojama.                           |
| **Pakeitė kita funkcija?**   | Ne                                                             |
| **Paveiktos produkto sritys**         | DK                                                 |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>„eGiro“ EDIFACT CREMUL mokėjimo importavimo formatas, skirtas Norvegijai

„eGiro“ yra pagrįstas tarptautiniu JT standartu EDIFACT CREMUL (pakartotinis kredito pažymų pranešimas), kuris naudojamas automatiškai registruojant kliento mokėjimus. „Dynamics AX“ „eGiro“ naudojamas kaip kliento mokėjimo importavimo formatas.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mokėjimo formatas nebenaudojamas.                                                     |
| **Pakeitė kita funkcija?**   | Taip, ISO20022 CAMT.054 pranešimų importavimas. |
| **Paveiktos produkto sritys**         | Gautinos sumos                                                                       |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.                            |

### <a name="external-inventory-for-poland"></a>Išorinės atsargos, skirtos Lenkijai

Įrodymas, kad iš tiekėjo paimtos parduotinos prekės be pirkimo. Prekės, tvarkomos išorinėse atsargose, neturi įtakos standartinėms atsargoms ir gali būti parduotos bei automatiškai nupirktos. Šiuo procesu sukuriami tikri atsargų perkėlimai.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Pakeitė kita funkcija                                    |
| **Pakeitė kita funkcija?**   | Taip, pagrindinė gaunamos konsignacijos funkcija                |
| **Paveiktos produkto sritys**         | Mokėtinos sumos, atsargų valdymas                         |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |

### <a name="financial-reports-generator-for-eastern-europe"></a>Finansinių ataskaitų generatorius, skirtas Rytų Europai

Įrankis yra skirtas apskaitos ir mokesčių ataskaitų duomenų rinkiniui nustatyti ir duomenims į XLS ir DOC ataskaitų šablonus eksportuoti.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Ribotas naudojimas                                                                            |
| **Pakeitė kita funkcija?**   | Ne. Būsimuose leidimuose įrankį pakeis elektroninių ataskaitų konfigūracijos. |
| **Paveiktos produkto sritys**         | DK                                                                           |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Kliento mokėjimo operacijų importavimas, skirtas Suomijai

Galite pasirinkti Suomijos mokėjimų importavimo formatą, kurį naudojant kliento mokėjimo operacijos importuojamos iš išorinio banko pateikto failo.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mokėjimo formatas nebenaudojamas.                                                     |
| **Pakeitė kita funkcija?**   | Taip, ISO20022 CAMT.054 pranešimų importavimas. |
| **Paveiktos produkto sritys**         | Gautinos sumos                                                                       |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Mokėjimo operacijų importavimas į DK žurnalą, skirtas Suomijai

Suomijai būdingas formatas naudojamas apskaitos operacijoms į DK importuoti.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mokėjimo formatas nebenaudojamas.                                                     |
| **Pakeitė kita funkcija?**   | Taip, ISO20022 CAMT.053 banko išrašo importavimas naudojant pažangų banko suderinimą. |
| **Paveiktos produkto sritys**         | Gautinos sumos                                                                       |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Sinchronizuotas integravimas su „Isabel“ (CIS), skirtas Belgijai

„Isabel“ yra elektroninės bankininkystės sistema Europoje ir de facto standartinė sistema Belgijoje.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Integravimas su „Isabel“ klientu nebepalaikomas.   |
| **Pakeitė kita funkcija?**   | Ne. Mokėjimo formatai nebenaudojami, juos pakeitė ISO20022 kredito pervedimo mokėjimo formatas, skirtas Belgijai. |
| **Paveiktos produkto sritys**         | Mokėtinos sumos     |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Sąskaitų plano ir apskaitos taisyklių modifikavimai, skirti Ispanijai

Ši funkcija naudojama Ispanijos sąskaitų plano ir apskaitos taisyklių keitimams atlikti. Ji sąskaitas susieja ir padeda seną sąskaitų planą paversti nauju sąskaitų planu bei palygina ankstesnius finansinius metus su naujais finansiniais metais, net jei jie buvo užregistruotu kituose sąskaitos numeriuose.

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Ribotas naudojimas                                                  |
| **Pakeitė kita funkcija?**   | Ne                                                             |
| **Paveiktos produkto sritys**         | DK                                                 |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |

### <a name="pagamento-fornittori-vendor-payment-format"></a>„Pagamento Fornittori“ tiekėjo mokėjimo formatas

Senesnės versijos Italijos kredito perkėlimų mokėjimo formatas.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mokėjimo formatas nebenaudojamas.                          |
| **Pakeitė kita funkcija?**   | Taip, ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Italijai         |
| **Paveiktos produkto sritys**         | Mokėtinos sumos                                               |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |

### <a name="payment-export-formats-for-estonia"></a>Mokėjimų eksportavimo formatai, skirti Estijai

„Telehansa“ ir „Teleservice“ formatai naudojami banko mokėjimams eksportuoti.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mokėjimo formatai nebenaudojami.                        |
| **Pakeitė kita funkcija?**   | Taip, ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Estijai       |
| **Paveiktos produkto sritys**         | Mokėtinos sumos                                               |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |

### <a name="payment-file-archive-for-norway"></a>Mokėjimo failo archyvas, skirtas Norvegijai

Generuojant mokėjimo failus, failų archyvas automatiškai suarchyvuoja visus sukurtus failus, įskaitant net anksčiau rašytus ar skaitytis failus.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Pakeitė kita funkcija                                        |
| **Pakeitė kita funkcija?**   | Taip, suarchyvuotos elektroninių ataskaitų užduotys                            |
| **Paveiktos produkto sritys**         | Mokėtinos sumos, gautinos sumos, organizacijos administravimas |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.     |

### <a name="payment-import-formats-for-estonia"></a>Mokėjimų importavimo formatai, skirti Estijai

„Telehansa“ ir „TeleTeenus“ formatai naudojami banko mokėjimams importuoti.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mokėjimo formatai nebenaudojami.                                                    |
| **Pakeitė kita funkcija?**   | Taip, ISO20022 CAMT.054 banko pranešimų importavimas. |
| **Paveiktos produkto sritys**         | Gautinos sumos                                                                        |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.                             |

### <a name="payroll-information-in-human-resources"></a>Algalapio informacija Žmogiškuosiuose ištekliuose

Žmogiškųjų išteklių Algalapio informacija

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Šią funkciją pakeitė pagrindiniai puslapiai Algalapis ir Žmogiškieji ištekliai.  |
| **Pakeitė kita funkcija?**   | **Išmokų**, **Pajamų** ir kiti susiję puslapiai, kurie anksčiau buvo JAV algalapyje, perkonfigūruoti ir dabar yra pagrindinės Žmogiškųjų išteklių konfigūracijos dalis, siekiant padėti teikti palaikymą išoriniam algalapių apdorojimui. Ši funkcija pasiekiama naudojant konfigūracijos raktą **1 žmogiškieji ištekliai** \> **Algalapis**. |
| **Paveiktos produkto sritys**         | Žmogiškieji ištekliai, Algalapis   |
| **Būsena**                         | Pašalinta iš „Dynamics 365 for Operations“ 1611 versijos.    |

### <a name="performance-management-goal-workflow"></a>Efektyvumo valdymo tikslų darbo eiga

Efektyvumo valdymas apima tikslų valdymą ir integravimą su efektyvumo apžvalgomis.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Efektyvumo valdymas buvo atnaujintas ir tikslo puslapių skaičius buvo sumažintas siekiant supaprastinti procesą.                 |
| **Pakeitė kita funkcija?**   | Ne. Tikslus gali vadovai mato naudodami portalą Vadovų savitarna ir vadovas gali juos keisti bei peržiūrėti. |
| **Paveiktos produkto sritys**         | Žmogiškojo kapitalo valdymas       |
| **Būsena**                         | Pašalinta iš „Dynamics 365 for Operations“ 1611 versijos.    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>„Postgirot“ ir „Postgirot Utland“ mokėjimo formatai, skirti Švedijai

„Postgirot“ ir „Postgirot Utland“ mokėjimo formatai, skirti Švedijai.

|&nbsp;   |&nbsp;  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mokėjimo formatai nebenaudojami.                        |
| **Pakeitė kita funkcija?**   | Taip, ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Švedijai        |
| **Paveiktos produkto sritys**         | Mokėtinos sumos                                               |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |

### <a name="radio-frequency-identifier"></a>Radijo dažnio identifikatorius

Radijo dažnio identifikavimas (RFID) yra duomenų surinkimo technologija, naudojanti elektronines žymes identifikavimo duomenims saugoti ir tiesioginio matymo skaitytuvą jiems gauti.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Naudojo mažai klientų ir ribotas funkcijų rinkinys.   |
| **Pakeitė kita funkcija?**   | Ne                                              |
| **Paveiktos produkto sritys**         | Atsargų valdymas                            |
| **Būsena**                         | Pašalinta iš „Dynamics 365 for Operations 1611“. |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Valstybinių SF numeravimo ataskaita, skirta Latvijai

Pagal Latvijos įstatymus galioja konkrečios pardavimo SF numeravimo taisyklės. Ši funkcija suteikia galimybę pardavimo SF priskirti konkrečius numerius pagal vartotoją arba vartotojų grupę. Tada galima generuoti ataskaitą arba XML failą. Taip pat galite spausdinti naudojamų SF numerių ataskaitą.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Valstybinių SF numeravimo tvarkyti nebereikia. Anksčiau naudota SF numerių ataskaita nebereikalinga. |
| **Pakeitė kita funkcija?**   | Ne       |
| **Paveiktos produkto sritys**         | Gautinos sumos    |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Lietuvos įmonės vadovo ir vyriausiojo buhalterio vardų nustatymas

Įmonės vadovo ir vyriausiojo buhalterio vardus galima nurodyti įmonės informacijoje ir naudoti skirtinguose vietos ataskaitų spaudiniuose.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Pakeitė kita funkcija                                     |
| **Pakeitė kita funkcija?**   | Taip, tarnautojų nustatymo funkciją galima naudoti tais pačiais tikslais.   |
| **Paveiktos produkto sritys**         | Mokėtinos sumos, Gautinos sumos, Grynųjų pinigų ir banko valdymas |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.  |

### <a name="shipping-carrier-interface"></a>Vežėjo sąsaja

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Besidubliuojančios funkcijos   |
| **Pakeitė kita funkcija?**   | Iš dalies pakeitė transportavimo valdymas |
| **Paveiktos produkto sritys**         | Pardavimas ir rinkodara, Atsargų valdymas  |
| **Būsena**                         | Pašalinta iš „Dynamics 365 for Operations“ 1611 versijos.  |

### <a name="telepay-payment-formats-for-norway"></a>„Telepay“ mokėjimo formatai, skirti Norvegijai

„Telepay“ mokėjimo formatai apima tiekėjo mokėjimo eksportavimą (kredito pervedimas) ir kliento mokėjimo surinkimą (tiesioginis debetas).

|&nbsp;   |&nbsp;  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mokėjimo formatai nebenaudojami.                                                        |
| **Pakeitė kita funkcija?**   | Taip, ISO20022 kreditų perkėlimo formatas ir „AvtaleGiro” kliento mokėjimo formatas, skirtas Norvegijai, taip pat pain.002 ir camt.054 banko pranešimų grąžinamų failų importavimas. |
| **Paveiktos produkto sritys**         | Mokėtinos sumos, gautinos sumos                                                          |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.                                 |

### <a name="vendor-payment-export-formats-for-finland"></a>Tiekėjo mokėjimo eksportavimo formatai, skirti Suomijai

Suomijai skirti du mokėjimų eksportavimo formatai. LM02 (FI) naudojamas vietiniams mokėjimams, o LUM2 (FI) naudojamas užsienio mokėjimams.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mokėjimo formatai nebenaudojami.                        |
| **Pakeitė kita funkcija?**   | Taip, ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Suomijai       |
| **Paveiktos produkto sritys**         | Mokėtinos sumos                                               |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |

### <a name="warehouse-management-ii"></a>II sandėlio valdymas

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Sandėlio valdymo II sprendimas (WMS II), kuris buvo prieinamas modulyje **Atsargų valdymas**, dubliuoja funkcijas, kurios yra modulyje **Sandėlio valdymas**, kuris buvo išleistas programoje „Dynamics AX 2012 R3“.                                                                         |
| **Pakeitė kita funkcija?**   | Modulis **Sandėlio valdymas**, kuris buvo išleistas programoje „AX 2012 R3“, „Dynamics AX 2012 R3 CU8“ ir „Dynamics AX 2012 R3 CU9“, pakeičia II sandėlio valdymo funkcijas. Naujasis modulis turi daugiau išplėstinių funkcijų ir lankstesnių sandėlio valdymo procesų nei tie, kurie buvo II sandėlio valdyme. |
| **Paveiktos produkto sritys**         | Atsargų valdymas, Pardavimas ir rinkodara, Įsigijimas ir šaltinio parinkimas   |
| **Būsena**                         | Pašalinta iš „Dynamics 365 for Operations“ 1611 versijos.    |

### <a name="worker-reminders-in-human-resources"></a>Darbuotojų priminimai Žmogiškuosiuose ištekliuose

Žmogiškųjų išteklių Algalapio informacija

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mažai naudojama                                                           |
| **Pakeitė kita funkcija?**   | Ne                                                                  |
| **Paveiktos produkto sritys**         | Personalas                                                     |
| **Būsena**                         | Pašalinta iš „Dynamics 365 for Operations“ 1611 versijos |

### <a name="workflow-for-creating-goals"></a>Tikslų kūrimo darbo eiga

Darbo eiga, skirta darbuotojų tikslų kūrimui valdyti, yra viena iš kelių darbo eigų, kurias buvo galima naudoti norint geriau koordinuoti efektyvumo valdymo procesą.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | „Finance and Operations“ efektyvumo valdymas buvo visiškai perkurtas.     |
| **Pakeitė kita funkcija?**   | Perkurta efektyvumo valdymo funkcija suteikia galimybę geriau kontroliuoti tikslų turinį, matavimus, naudojamus eigai sekti, ir patvirtinamųjų dokumentų pridėjimą. Tikslai gali būti saugomi kaip šablonai ir naudojami pakartotinai. Naudodami šią funkciją galite greičiau nustatyti papildomus darbuotojų tikslus. |
| **Paveiktos produkto sritys**         | Žmogiškojo kapitalo valdymas                 |
| **Būsena**                         | Pašalinta iš „Dynamics 365 for Operations“ 1611 versijos. |

## <a name="dynamics-ax-70"></a>Dynamics AX 7.0 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Galimybė atšaukti tiekėjo SF pakeitimus

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Našumo padidinimas        |
| **Pakeitė kita funkcija?**   | Ne                             |
| **Paveiktos produkto sritys**         | Mokėtinos sumos               |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“. |

### <a name="aif-axd-and-axbc-integrations"></a>AIF, AxD ir AxBC integracijos

Programos integravimo sistemoje (AIF) duomenimis su išorinėmis sistemomis galima keistis naudojant verslo logiką, rodomą kaip paslaugas. Dynamics AX apima paslaugas, kurios remiasi dokumentais ir .NET Business Connector (AxBC). Dokumentas sukuriamas naudojant XML. XML yra antraštės informacija, kuri pridedama sukurti *pranešimui*, kuris gali būti perkeliamas į „Dynamics AX“ arba iš jos. Dokumentų pavyzdžiai apima pardavimo užsakymus ir pirkimo užsakymus. Tačiau dokumentas gali atstoti beveik visus objektus, pvz., klientą. Paslaugos, paremtos dokumentais, naudoja **Axd \<Document\>** klases.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | AIF ir AxDs architektūros dydžio negalima keisti pagal debesies tarnybą. Atliekant masinį importą, buvo našumo problemų.                                        |
| **Pakeitė kita funkcija?**   | Šią funkciją pakeitė Duomenų importavimo / eksportavimo sistema, kuri palaiko pasikartojantį masinį importavimą / eksportavimą. Su AxBC rekomenduojame naudoti faktines lenteles. |
| **Paveiktos produkto sritys**         | AxD, AxBC ir AIF   |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.   |

### <a name="billing-code-rate-scripts"></a>Atsiskaitymo kodų tarifų scenarijai

Atsiskaitymo scenarijai buvo naudojami atsiskaitymo kodų atsiskaitymo tarifams apskaičiuoti. Šiems scenarijams reikėjo pasirinktinio kodo „C Sharp“ arba „Visual Basic“ programavimo kalba. Dabartinėje „Dynamics AX“ versijoje **atsiskaitymo kodų tarifų scenarijai** nėra palaikomi.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Pasirinktinių „C Sharp“ arba „Visual Basic“ scenarijų palaikymas į „Dynamics AX 7.0“ nebuvo įtrauktas. |
| **Pakeitė kita funkcija?**   | Ne                                                                                      |
| **Paveiktos produkto sritys**         | Viešasis sektorius. Gautinos sumos                                    |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.                                                          |

### <a name="boms-without-bom-versions"></a>KS be KS versijų

Kai **KS versijų** konfigūracijos raktas buvo išjungtas, komplektavimo specifikacijų (KS) versijos buvo paslėptos visose formose, ir sistema tarp išleistų produktų ir KS priverstinai taikė ryšį 1:1. Dabartinėje „Dynamics AX“ versijoje konfigūracijos rakto **KS versijos** išjungti negalima.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Naudojant konfigūracijos raktą KS versijoms kontroliuoti, dydžio keisti debesies aplinkoje negalima. |
| **Pakeitė kita funkcija?**   | Ne                                                                                      |
| **Paveiktos produkto sritys**         | Produktų informacijos valdymas, Atsargų valdymas                                    |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.                                                          |

### <a name="brazilian-bordero"></a>Brazilijos „Bordero“

Konkretus mokėjimo būdas, skirtas Brazilijos įmonėms

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Brazilijos „Bordero“ mokėjimo būdo lokalizavimas nebepalaikomas |
| **Pakeitė kita funkcija?**   | Ne   |
| **Paveiktos produkto sritys**         | Mokėtinos sumos   |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |

### <a name="brazilian-sintegra-statement"></a>Brazilijos „Sintegra“ išrašas

ICMS mokesčio federalinių mokesčių ataskaita

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Šis išrašas kai kuriose Brazilijos apskrityse nebetaikomas. |
| **Pakeitė kita funkcija?**   | Ne. Vartotojai gali naudoti įrankį Bendrosios elektroninės ataskaitos, norėdami konfigūruoti išrašą, jei to reikalaujama konkrečiose situacijose. |
| **Paveiktos produkto sritys**         | Finansų knygos    |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brazilijos SCAN atsakomųjų priemonių režimas, skirtas NF-e

(SCAN) atsakomųjų priemonių režimas naudojamas norint generuoti, eksportuoti ir importuoti „Nota Fiscal eletrônica“ (NF-e) būseną, kai „Secretaria da Fazenda“ (SEFAZ) režimo naudoti negalima.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Šis atsakomųjų priemonių metodas nebetaikomas nė vienoje Brazilijos apskrityje |
| **Pakeitė kita funkcija?**   | Ne                                                                          |
| **Paveiktos produkto sritys**         | Gautinos sumos                                                         |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.              |

### <a name="business-analyzer"></a>Veiklos analizatorius

Ši mobilioji programa naudotojams leidžia peržiūrėti pagrindinę verslo metriką.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Šią funkciją pakeitė kita funkcija.   |
| **Pakeitė kita funkcija?**   | „Microsoft Power BI“ turinio pakete Stebėti finansinį našumą bus įtraukta pagrindinė finansų metrika, kuri anksčiau buvo prieinama programoje „Business Analyzer“. |
| **Paveiktos produkto sritys**         | DK      |
| **Būsena**                         | Nebenaudojama: „Business Analyzer“ nebenaudojama.    |

### <a name="business-statistics"></a>Verslo statistika

Verslo statistikos užklausų, galinčių padėti analizuoti organizacijos efektyvumą, sąranka

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Senesnės verslo įžvalgų (BI) versijos, mažas klientų naudojimas ir ribotas funkcijų rinkinys |
| **Pakeitė kita funkcija?**   | Nauji dabartinės „Dynamics AX“ versijos BI sprendimai                                      |
| **Paveiktos produkto sritys**         | Įsigijimas ir šaltinio parinkimas, Mokėtinos sumos, Pardavimas ir rinkodara, Gautinos sumos         |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Keisti dokumento datos funkciją SF patvirtinimo žurnale

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mažai naudojama                                                               |
| **Pakeitė kita funkcija?**   | Taip. Užregistruotos tiekėjo operacijos dokumento datą galima keisti. |
| **Paveiktos produkto sritys**         | Mokėtinos sumos                                                        |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a>Nyderlandų mokėjimo formatas ClieOp03

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Formatas Nyderlanduose nebetaikomas, nes jį pakeitė (SEPA) funkcija. |
| **Pakeitė kita funkcija?**   | SEPA mokėjimų eksportas  |
| **Paveiktos produkto sritys**         | Visi moduliai     |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.   |

### <a name="compliance-center"></a>Atitikties centras

Atitikties centras buvo įmonės portalo svetainė, skirta valdyti atitikties iniciatyvų, susijusių su Sarbanes-Oxley įstatymu, dokumentų reikalavimams.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Naudojo mažai klientų. „Microsoft SharePoint“ apima tuos pačius pajėgumus, kurie buvo prieinami atitikties centre. |
| **Pakeitė kita funkcija?**   | Ne   |
| **Paveiktos produkto sritys**         | Atitikties ir vidiniai valdikliai  |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.    |

### <a name="connector-for-microsoft-dynamics"></a>„Microsoft Dynamics“ jungtis

Šis įrankis buvo naudojamas integruoti pagrindiniams duomenims iš „Microsoft Dynamics CRM“ į „Dynamics ERP“ programas.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Šią funkciją pakeitė kita funkcija. |
| **Pakeitė kita funkcija?**   | „Dataverse“                                      |
| **Paveiktos produkto sritys**         | „Dynamics“ jungtis                         |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Turimas konteinerių vienetas ir kelios dimensijos

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Besidubliuojančios funkcijos |
| **Pakeitė kita funkcija?**   | Taip. Nuo „AX 2012“ šią funkciją pakeitė konsoliduotųjų paketinius užsakymų funkcijų rinkinys. Šis funkcijų rinkinys apima konsoliduotąjį turimų objektų rodinį. |
| **Paveiktos produkto sritys**         | Produktų informacijos valdymas, Gamybos kontrolė, Atsargų valdymas, Pardavimas ir rinkodara  |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“. |

### <a name="cue-group-metadata"></a>Eilių grupės metaduomenys

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Eilių grupės buvo naudojamos rodyti vienai ar kelioms Eilėms „FactBox‟ srityje. Naudojimas buvo ribotas, taip pat buvo našumo klausimų, kadangi pirminės formos įrašo pakeitimas lėmė vieną Eilės užklausą Eilių grupėje. |
| **Pakeitė kita funkcija?**   | Ne      |
| **Paveiktos produkto sritys**         | Visi moduliai    |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.  |

### <a name="cue-metadata"></a>Eilių metaduomenys

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Eilių metaduomenys buvo apriboti skaičių ar sumos informacija.    |
| **Pakeitė kita funkcija?**   | Plytelių metaduomenys buvo įdiegti siekiant suteikti daugiau modeliavimo lankstumo. Pavyzdžiui, galite modeliuoti dabartinius skaičiavimus, naršymą ir pagrindinius našumo indikatorius (KPI). Skaičiavimo plytelių metaduomenys tiesiogiai pakeičia Eilių metaduomenis. |
| **Paveiktos produkto sritys**         | Visi moduliai           |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“      |

### <a name="danish-check-format"></a>Daniška čekio forma

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Danijos čekio formato maketo palaikymas nutrauktas, o ataskaita pašalinta iš DK lokalizacijos. |
| **Pakeitė kita funkcija?**   | Ne    |
| **Paveiktos produkto sritys**         | Visi moduliai    |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.  |

### <a name="data-partitions"></a>Duomenų skaidiniai

Naudojant duomenų skaidinius duomenys logiškai suskaidomi „Dynamics AX“ duomenų bazėje.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Duomenų skaidiniai pristatyti „Dynamics AX 2012 R2“, kad būtų galima duomenis atskirti. Įprastu scenarijumi įmonė turi dukterinių įmonių ir vienos dukterinės įmonės duomenų kita dukterinė įmonė neturėtų matyti, nors abi dukterinės įmonės valdomos to paties IT skyriaus. Tačiau visoje programoje buvo reikalingi papildomi scenarijai ir pridėtinės valdymo išlaidos, siekiant sukurti naujus skaidinius ir užpildyti juos duomenimis bei sukurti skaidinio duomenų atsarginę kopiją. Debesyje teikiama prieiga prie paslauginės platformos duomenų bazės tarnybų („Microsoft Azure“ SQL duomenų bazės), todėl tai yra daug efektyvesnis būdas duomenų bazę naudoti kaip atskirtą konteinerį negu atskyrimą atlikti programoje. Nesvarbu, ar duomenų skaidymas reikalingas filialams, keliems nuomininkams, ar tiesiog dėl masto, manome, kad scenarijus galima tvarkyti geriau naudojant kelis „Finance and Operations“ egzempliorius. |
| **Pakeitė kita funkcija?**   | Klientai, naudojantys duomenų skaidinius, turi naudoti kelis „Finance and Operations“ egzempliorius, jei duomenų bazės lygių atskyrimas yra didelė problema.    |
| **Paveiktos produkto sritys**         | Visi moduliai  |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.  |


### <a name="database-and-file-share-storage-for-attachments"></a>Duomenų bazės ir bendrai naudojamo failo saugykla, skirta priedams

„Dynamics AX 2012“ leidžiamas priedų saugyklos duomenų bazėje ir bendrai naudojamuose failuose kiekis. Abejos parinktys nebepalaikomos.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Bendrai naudojamų failų saugykla nebepalaikoma, nes aplinkos diegimo debesyje įrankis nesusijungia su vietiniais bendrai naudojamais failais. Duomenų bazė nebenaudojama „Azure“ didelių dvejetainių objektų saugyklos naudai. „Azure“ didelių dvejetainių objektų saugykla yra tokia pati kaip ir duomenų bazės saugykla, nes dokumentus galima pasiekti tik per „Finance and Operations“ kliento formas. Tai tarnauja kaip papildomas pranašumas teikiant saugyklą, neturinčią neigiamo poveikio duomenų bazės efektyvumui. Didelių dvejetainių objektų saugykla yra numatytoji dokumentų valdymo mechanizmo saugykla ir veikia nedelsiant. |
| **Pakeitė kita funkcija?**   | Duomenų bazė nebenaudojama „Azure“ didelių dvejetainių objektų saugyklos naudai.   |
| **Paveiktos produkto sritys**         | Visi moduliai  |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.   |

### <a name="delimitation"></a>Apribojimas

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Funkcijomis nesinaudota. |
| **Pakeitė kita funkcija?**   | Ne                                     |
| **Paveiktos produkto sritys**         | Laikas ir buvimas darbe                    |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.         |

### <a name="desktop-client"></a>Darbalaukio klientas

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | „Dynamics AX“ kliento patirtis perkurta, siekiant pagerinti naudojimą keliose platformose ir įrenginiuose.                      |
| **Pakeitė kita funkcija?**   | Naujasis žiniatinklio klientas paremtas darbalaukio formos metaduomenimis ir programavimo modeliu, kurie modifikuoti siekiant suteikti turiningą žiniatinklio platformą. |
| **Paveiktos produkto sritys**         | Visi moduliai  |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.   |

### <a name="direct-database-connection"></a>Tiesioginis duomenų bazės ryšys

Programoje „Dynamics AX 2012 R3“ „Retail Modern POS“ gali tiesiogiai prisijungti prie kanalo duomenų bazės panašiai kaip įmonės EKA. Tai yra papildomas ryšio metodas, teikiamas kartu su standartiniu „Retail Modern POS“ ryšio per „Retail Server“ metodu.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Tiesioginiam duomenų bazės ryšiui reikia žemesnio lygio saugos protokolų ir jis daugiausia buvo naudojamas siekiant aukščiausio lygio efektyvumo. Dėl „Dynamics 365 Finance and Operations‟ įdiegtų efektyvumo ir saugos patobulinimų dabar ši funkcija sukelia daugiau problemų, negu išsprendžia. |
| **Pakeitė kita funkcija?**   | Ne. Dabar palaikomas tik standartinis „Retail Server“ ryšys.  |
| **Paveiktos produkto sritys**         | Kanalo duomenų bazė / „Retail Modern POS“   |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.  |

### <a name="dutch-swift-mt940"></a>Nyderlandų SWIFT MT940

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Vietoj lokalizuotų funkcijų dabar naudojamos bendrosios funkcijos.                    |
| **Pakeitė kita funkcija?**   | Taip, šią funkciją pakeitė funkcija Išplėstinis banko suderinimas. |
| **Paveiktos produkto sritys**         | Visi moduliai                                                                              |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.                           |

### <a name="ebilanz-xbrl-for-germany"></a>„eBilanz‟ (Vokietijos XBRL)

Ši funkcija teikė išplėstinės verslo ataskaitų kalbos (XBRL) išeigą, kuri skirta konkrečiai Vokietijos „eBilanz‟ taksonomijai.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Naudojo mažai klientų  |
| **Pakeitė kita funkcija?**   | Ši funkcija nėra pakeista kita funkcija, o Vokietijos rinkai prieinami keli specializuoti XBRL paketai, kurie teikia XBRL funkcijas. |
| **Paveiktos produkto sritys**         | „Management Reporter“      |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.  |

### <a name="enterprise-portal-client"></a>Įmonės portalo klientas

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Suteikta viena kliento platforma.  |
| **Pakeitė kita funkcija?**   | Naujasis žiniatinklio klientas paremtas darbalaukio formos metaduomenimis ir programavimo modeliu, kurie modifikuoti siekiant suteikti turiningą žiniatinklio platformą. |
| **Paveiktos produkto sritys**         | Visi moduliai  |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.   |

### <a name="environmental-sustainability"></a>Aplinkos tvarumas

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Naudojo mažai klientų ir ribotas funkcijų rinkinys  |
| **Pakeitė kita funkcija?**   | Ne              |
| **Paveiktos produkto sritys**         | Atitikties ir vidiniai valdikliai, Mokėtinos sumos  |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“. |

### <a name="form-activex-and-managed-host-controls"></a>Forma „ActiveX‟ ir Tvarkomo pagrindinio kompiuterio valdikliai

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | „ActiveX‟ ir Tvarkomo pagrindinio kompiuterio valdikliai paremti pasenusiu darbalaukio klientu. |
| **Pakeitė kita funkcija?**   | Išplečiamoji valdymo sistema palaiko naujų valdiklių, paremtų HTML, CSS ir „JavaScript“, kūrimą ir yra aukščiausios klasės valdiklis „Microsoft Visual Studio“ įrankių aplinkoje. |
| **Paveiktos produkto sritys**         | Visi moduliai     |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.       |

### <a name="generate-prenotes-by-using-a-batch"></a>Generuoti išankstinius pranešimus naudojant paketą

Išankstinių pranešimų generavimo negalima atlikti naudojant paketą, bet jį vis dar gali atlikti naudotojas.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Nėra jokios formos, kurioje išliktų ir būtų rodomas gautas išankstinis pranešimas, kai jis generuojamas naudojant paketą. |
| **Pakeitė kita funkcija?**   | Išankstiniai pranešimai vis dar gali būti generuojami, ir naudotojas gali kontroliuoti vietą, kur failas įrašomas.   |
| **Paveiktos produkto sritys**         | Mokėtinos sumos, Gautinos sumos, Grynųjų pinigų ir banko valdymas  |
| **Būsena**                         | Pašalinta iš „AX 7.0“.    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Vokietijos DTAUS mokėjimo eksportas ir sąskaitos išrašo importas (bendrosios sumos ir operacijos)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Formatas Vokietijoje nebetaikomas, nes jį pakeitė bendros mokėjimų eurais erdvės (SEPA) funkcija.                    |
| **Pakeitė kita funkcija?**   | Taip, šią funkciją pakeitė SEPA mokėjimo eksportavimo ir išplėstinio banko suderinimo funkcija, skirta importuoti sąskaitų išrašams. |
| **Paveiktos produkto sritys**         | Visi moduliai  |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |

### <a name="german-dtazv-payment-format-in-domestic-currency"></a>Vokietijos DTAZV mokėjimo formatas nacionaline valiuta

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Formatas Vokietijoje nebetaikomas, nes jį pakeitė (SEPA) funkcija. |
| **Pakeitė kita funkcija?**   | SEPA mokėjimų eksportas    |
| **Paveiktos produkto sritys**         | Mokėtinos sumos   |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.    |

### <a name="german-mt940-import"></a>Vokietijos MT940 importas

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Vietoj lokalizuotų funkcijų dabar naudojamos bendrosios funkcijos.                    |
| **Pakeitė kita funkcija?**   | Taip, šią funkciją pakeitė funkcija Išplėstinis banko suderinimas. |
| **Paveiktos produkto sritys**         | Visi moduliai                                                                              |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.                           |

### <a name="german-xml-eu-sales-list"></a>Vokietijos XML ES pardavimo sąrašas

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | XML formatas, skirtas Vokietijos ES pardavimo sąrašo ataskaitoms, nebepalaikomas. Galima naudoti tik ELMA5 teksto failo formatą, ES pardavimo sąrašo ataskaitai pateikti Vokietijos mokesčių inspekcijai. |
| **Pakeitė kita funkcija?**   | Ne         |
| **Paveiktos produkto sritys**         | Mokesčiai        |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.   |

### <a name="gl-ssrs-reports"></a>DK SSRS ataskaitos

Ataskaitos, kurios apima šiuos meniu elementus, pašalintos: **Bandomojo balanso suvestinė**, **Išsamus bandomasis balansas**, **Sąskaitų planas**, **Audito sekimas**, **Balansai** ir **Balansų sąrašas**.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Finansines „Microsoft SQL Server“ serverio ataskaitų tarnybų (SSRS) ataskaitas pakeitė „Management Reporter“ galimybės ir numatytosios ataskaitos. |
| **Pakeitė kita funkcija?**   | „Management Reporter“ (dabartinėje „Dynamics AX“ versijoje pažymėta **Finansinės ataskaitos**)    |
| **Paveiktos produkto sritys**         | Didžioji knyga   |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.   |

### <a name="infopart-and-formpart-metadata"></a>„InfoPart‟ ir „FormPart‟ metaduomenys

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | „InfoPart‟ ir „FormPart‟ metaduomenys įgalino „FactBox‟ kūrimą dviem skirtingiems klientams. |
| **Pakeitė kita funkcija?**   | „InfoPart‟ metaduomenys, kurie buvo supaprastinta formos apibrėžtis, konvertuojami į formą naudojant naujinimo įrankius. „FormPart‟ metaduomenis, kurie nurodė į formą, pakeičia labiau tiesioginė nuoroda, kuri sukurta naudojant naujinimo įrankius. |
| **Paveiktos produkto sritys**         | Visi moduliai    |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.        |

### <a name="main-account-list-page"></a>Pagrindinės sąskaitos sąrašo puslapis

Juridinio subjekto sąskaitų ir susijusios balanso informacijos sąrašas

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Balanso informacija pagal sąskaitą ir dimensiją prieinama **Bandomojo balanso** sąrašo puslapyje.  |
| **Pakeitė kita funkcija?**   | **Pagrindinėse sąskaitose** yra tas pats sąskaitų sąrašas, kuris buvo **Pagrindinės sąskaitos** sąrašo puslapyje. **Pagrindinių sąskaitų** tinklelio rodinyje taip pat rodomas dar mažesnis, tinklelio vaizdas. |
| **Paveiktos produkto sritys**         | Didžioji knyga      |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malaizijos ir Singapūro bankų grynųjų pinigų srauto ataskaita

Ši funkcija naudotojui leidžia spausdinti pinigų srauto ataskaitą, kurioje rodomos pasirinktų banko sąskaitų operacijos ir išsami pinigų įplaukų bei išmokų informacija tam tikru laikotarpiu.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Tą pačią informaciją galima gauti iš Užklausos apie banko operaciją. |
| **Pakeitė kita funkcija?**   | Užklausa apie banko operaciją                                            |
| **Paveiktos produkto sritys**         | Grynųjų pinigų ir banko valdymas                                                |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta.          |

### <a name="mexican-cfd-electronic-invoice"></a>Meksikos CFD elektroninė SF

Ši funkcija leido generuoti Meksikos elektronines SF naudojant „Comprobante Fiscal Digital‟ (CFD) metodą, kai įmonė pasirašo SF reikalaudama susijusio autorizavimo iš vyriausybės. Ši funkcija taip pat pateikia mėnesio ataskaitą, kurioje įtrauktos visos elektroninės SF, išduotos tuo laikotarpiu.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Šis metodas nebetaikomas. Elektroninių sąskaitų faktūrų generavimas naudojant CFD metodą nebenaudojamas, nes mokesčių institucijos jį pakeitė Comprobante Fiscal Digital a través de Internet (CFDI) metodu, kuriuo pasirašymas perduodamas trečiosios šalies teikėjui (PAC). Mėnesio ataskaita pašalinta, o užklausos parinktis naudotojams leidžia paklausti apie praeities operacijas. |
| **Pakeitė kita funkcija?**   | Ne    |
| **Paveiktos produkto sritys**         | Gautinos sumos, Projektas   |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |

### <a name="mexico-realized-and-unrealized-vat"></a>Meksikos sumokėtas ir nesumokėtas PVM

„Dynamics AX 2012“ nesumokėtą pridėtinės vertės mokestį (PVM) valdė naudodama tik Meksikai skirtas nesumokėto mokesčio funkcijas.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Besidubliuojančios funkcijos  |
| **Pakeitė kita funkcija?**   | Taip, šią funkciją pakeitė standartinė sąlyginio PVM funkcija, kurią teikia „Core‟. |
| **Paveiktos produkto sritys**         | Mokesčiai   |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data nenustatyta. |

### <a name="microsoft-outlook-integration"></a>„Microsoft Outlook“ integravimas


| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Šią funkciją pakeitė „Microsoft Exchange Server“ integracija. |
| **Pakeitė kita funkcija?**   | Taip                                                                            |
| **Paveiktos produkto sritys**         | „Sales and marketing“                                                            |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Privatus atsargų ir sandėlio valdymo žurnalų blokavimas

Atsargų ir sandėlio žurnalai nebepalaiko galimybės pasirinkto naudotojo žurnalą pažymėti kaip privatų. Palaikomas tik naudotojų grupių privačių žurnalų blokavimo procesas ir blokavimas redaguojant.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Funkcijomis nesinaudota. |
| **Pakeitė kita funkcija?**   | Ne                                     |
| **Paveiktos produkto sritys**         | Atsargų valdymas                   |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.         |

### <a name="product-builder"></a>Produkto generatorius

Produkto generatorius buvo naudojamas dinamiškai konfigūruoti prekėms iš pardavimo užsakymo, pirkimo užsakymo, gamybos užsakymo, pardavimo pasiūlymo, projekto pasiūlymo ar prekės reikalavimo. Pagal produkto modelį, turintį modeliavimo kintamųjų, naudotojas galėdavo pasirinkti reikšmes, kurios atitikdavo kliento reikalavimus ir gauti unikalų produkto variantą, turintį KS ir maršrutą.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Produkto generatorius X++ kodą rodydavo galutiniams naudotojams ir dabartinėje „Dynamics AX“ versijoje nėra palaikomas. Jis pašalintas siekiant išvengti besidubliuojančių priežiūros darbų sutampančiose, keičiamo dydio kodų bazėse.  |
| **Pakeitė kita funkcija?**   | Taip. Konfigūravimas pagal apribojimus buvo pristatytas ir įtrauktas į „Dynamics AX 2012“, kai jau buvo paskelbta, kad produkto generatorius būsimose versijose nebebus naudojamas. Konfigūravimo pagal apribojimus technologija pasirenkama bendruosiuose produktuose, siekiant įjungti konfigūraciją. Norėdami sužinoti daugiau, žr. [Produkto konfigūracijos modelio apžvalga](../../../supply-chain/pim/build-product-configuration-model.md). |
| **Paveiktos produkto sritys**         | Produktų informacijos valdymas, Pardavimas ir rinkodara  |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.      |

### <a name="production-floor-app"></a>Gamybos vietos programa
Tai programa, skirta planšetiniams įrenginiams, kuriuose veikia „Windows 8.1 RT“ ir „Windows 8.1 Pro“.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Pakeitus žiniatinklio klientą, panašias funkcijas galima teikti naudojant vietinę „Dynamics AX 7.0“ kliento programą. Užduoties kortelės įrenginyje pateikiama gamybos vietos vartotojo sąsaja, kuri optimizuota lietimui, o jos išvaizda pritaikyta prie planšetinių kompiuterių. |
| **Pakeitė kita funkcija?**   | Taip. Užduoties kortelės įrenginys, kuris yra „Dynamics AX 7.0“ vietinė dalis.                                                                           |
| **Paveiktos produkto sritys**         | Gamybos kontrolė                                                |
| **Būsena**                         | Nebenaudojama: šios funkcijos pašalinimo data iš „Microsoft“ parduotuvės dar nenustatyta.                                                |


### <a name="rename-product-dimension"></a>Pervardyti produkto dimensiją

Ši funkcija leidžia pakeisti vienos iš trijų standartinių produktų dimensijų (dydžio, spalvos arba stiliaus) pavadinimą į tokį, kuris geriau tinka jūsų verslo poreikiams. Pervardijimas apėmė visas etiketes, kuriose buvo naudojamas produkto dimensijos pavadinimas.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Dabartinė „Dynamics AX“ versija nepalaiko etikečių keitimo vykdymo metu. |
| **Pakeitė kita funkcija?**   | Ne                                                                            |
| **Paveiktos produkto sritys**         | Produkto informacijos valdymas                                                |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.                                                |

### <a name="retail-server-connectivity-using-http"></a>„Retail Server“ ryšys naudojant HTTP

Programoje „Dynamics AX 2012 R3“ „Retail Server“ galėjo veikti naudojant HTTP ryšį (nesaugų). Tai buvo papildomas metodas, teikiamas kartu su standartiniu ryšiu naudojant HTTPS.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Dėl naujų saugos reikalavimuų dabar palaikomas tik saugus ryšys naudojant TLS 1.2 (arba naujesnę versiją, jei yra). Savitarnos diegimo programa automatiškai sukonfigūruos kompiuterį šiam ryšiui užmegzti. |
| **Pakeitė kita funkcija?**   | Ne. Dabar palaikomas tik standartinis HTTPS ryšys. |
| **Paveiktos produkto sritys**         | Parduotuvės serveris  |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“. |

### <a name="role-center-pages"></a>Vaidmenų centrų puslapiai

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Vaidmenų centrų puslapiai buvo sukurti pasenusioje įmonės portalo platformoje, kurią dabartinėje „Dynamics AX“ versijoje pakeitė naujoji žiniatinklio kliento programa. |
| **Pakeitė kita funkcija?**   | Naujasis Darbo srities formos modelis naudotojams pateikia į procesą orientuotą dizainą, kuris suteikia lengvą prieigą prie dažniausiai naudojamų užduočių tame procese.                       |
| **Paveiktos produkto sritys**         | Visi moduliai    |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“   |

### <a name="sales-tax-jurisdictions"></a>PVM jurisdikcijos

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Naudojo mažai klientų ir ribotas funkcijų rinkinys |
| **Pakeitė kita funkcija?**   | Ne                                           |
| **Paveiktos produkto sritys**         | JAV PVM                                 |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.               |

### <a name="sites-services"></a>„Sites Services“

„Sites Services“ leidžia kurti svetaines, išplečiančias jūsų verslo procesus į internetą be IT palaikymo.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | „Microsoft Azure“ infrastruktūra, kurią naudoja „Dynamics AX“, turi naujų galimybių, kurias galima naudoti vietoje jų (pvz., „Azure“ svetainės). |
| **Pakeitė kita funkcija?**   | Ne   |
| **Paveiktos produkto sritys**         | Personalo įdarbinimas, atvejų valdymas, pasiūlymų patvirtinimas, tiekėjų registracija, galimybių ir kampanijų bendradarbiavimo darbo sritys  |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.    |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS poreikio prognozės strategija

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Naujoje debesies architektūroje funkcijos dizainas nepalaikomas. |
| **Pakeitė kita funkcija?**   | „Azure“ mašininio mokymo poreikio prognozės strategija                           |
| **Paveiktos produkto sritys**         | Bendrasis planavimas                                                              |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Tiekėjo SF telkinys be registravimo informacijos

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mažai naudotasi. Ši funkcija buvo pakeista SF žurnalu, kuriame yra darbo eigos funkcija. |
| **Pakeitė kita funkcija?**   | SF žurnalo darbo eigos galimybės.     |
| **Paveiktos produkto sritys**         | Mokėtinos sumos |
| **Būsena**                         | Pašalinta iš „Dynamics AX 7.0“.    |


### <a name="virtual-company-accounts"></a>Virtualios įmonės

Virtualių įmonių funkcija programoje „Dynamics AX“ nebepalaikoma. Virtualių įmonių funkcija naudotojams leidžia nustatyti lenteles, kurias gali bendrai naudoti įmonių grupė. Funkcijos aprašo žr.: [Įmonių sąskaitos ir Virtualių įmonių sąskaitos](../../fin-ops/get-started/ax4-content-retired.md). Funkcija veikia grupuodama lenteles į rinkinius, kurie yra priskiriami virtualioms įmonėms, kurios yra esamų „tikrų‟ įmonių grupės. Užklausos kuriamos taip, kad visos įmonės virtualioje įmonėje galėtų prieiti prie lentelių duomenų, susietų lentelių rinkiniuose.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | - Prieš lentelėse saugant duomenis, reikia nustatyti virtualias įmones. Virtualias įmones pertvarkyti į esamą diegimą yra labai sunku.<br><br>- Kadangi dabartinėje „Dynamics AX“ versijoje buvo tiek daug duomenų normalizavimo, pasidarė sudėtinga sužinoti, ką įtraukti į lentelių rinkinius. Pvz., sunku žinoti, kurias lenteles bendrai naudoti. Taip pat reikia pridėti visas lenteles, į kurias nurodoma iš lentelių, esančių virtualioje įmonėje. Dėl lentelių normalizavimo net paprasti bendrieji duomenys, paskirstyti daugybėje lentelių, turi būti virtualios įmonės dalis. Bet kokia čia padaryta klaida sukels funkcinių problemų.<br><br>- Kai lentelė yra virtualios įmonės dalis, ji praranda informaciją apie duomenų šaltinį, ir įrašoma tik virtuali įmonė.   |
| **Pakeitė kita funkcija?** | Kad lentelės būtų pasiekiamos iš visų įmonių, gali būti naudojamos visuotinės lentelės. Šiuo metu nėra pakeitimo. |   
| **Paveiktos produkto sritys**       | Visi moduliai |   
| **Būsena**                       | Pašalinta iš „Dynamics AX 7.0“.   |   

### <a name="windows-8-tablet-app"></a>„Windows 8“ planšetinių kompiuterių programėlė

„Windows 8“ planšetinių kompiuterių programėlė turėdavo išlaidų pateikimo ir patvirtinimo funkciją.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | „Finance and Operations” suderinama su planšetiniais kompiuteriais. Planšetinių kompiuterių programėlės nebereikia.    |
| **Pakeitė kita funkcija?**   | Ne.          |
| **Paveiktos produkto sritys**         | Išlaidų valdymas   |
| **Būsena**                         | Pašalinta: šią funkciją galima naudoti tik „Dynamics AX 2012“ R3. |

### <a name="workplanner"></a>Darbo planuotuvas

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Nebenaudojimo / pašalinimo priežastis** | Mažai naudojama |
| **Pakeitė kita funkcija?**   | Ne, bet puslapis **Šablono ryšys**, kuris atidaromas iš puslapio **Šablonų grupės**, palaiko tą patį verslo scenarijų kaip ir pasenęs puslapis **Darbo planuotuvas**. |
| **Paveiktos produkto sritys**         | Laikas ir buvimas darbe     |
| **Būsena**                         | Kodas bevyvo pašalintas. Tačiau forma JmgWorkPlanner nebuvo perkelta.    |

### <a name="x-financial-statements"></a>X++ finansinės ataskaitos

| &nbsp;  | &nbsp; |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <strong>Nebenaudojimo / pašalinimo priežastis</strong> |                         Šią funkciją pakeitė kita funkcija.                         |
|  <strong>Pakeitė kita funkcija?</strong>  | „Management Reporter“ (dabartinėje „Dynamics AX“ versijoje pažymėta <strong>Finansinės ataskaitos</strong>) |
|     <strong>Paveiktos produkto sritys</strong>     |                                              Didžioji knyga                                              |
|             <strong>Būsena</strong>             |                                      Pašalinta iš „Dynamics AX 2012“                                      |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

