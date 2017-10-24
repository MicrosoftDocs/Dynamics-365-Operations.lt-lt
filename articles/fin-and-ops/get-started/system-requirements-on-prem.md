---
title: "Vietinėms įdiegtims taikomi sistemos reikalavimai"
description: "Šioje temoje išvardyti šiai „Microsoft Dynamics 365 Finance and Operations“ „Enterprise‟ leidimo versijai (vietinėms įdiegtims) taikomi sistemos reikalavimai."
author: kfend
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 25a6f326c57e84d6a7c356ac5407be7ed3095f83
ms.openlocfilehash: 5edc6f0b2240e9dd2d3b72a13f35e96f016aa013
ms.contentlocale: lt-lt
ms.lasthandoff: 10/04/2017

---

# <a name="system-requirements-for-on-premises-deployments"></a>Vietinėms įdiegtims taikomi sistemos reikalavimai

[!include[banner](../includes/banner.md)]

Šioje temoje išvardyti šiai „Microsoft Dynamics 365 Finance and Operations“ „Enterprise‟ leidimo versijai (vietinėms įdiegtims) taikomi sistemos reikalavimai. Prieš diegdami „Finance and Operations“, kai galėsite, patikrinkite, ar sistema, kurią naudojate, atitinka arba viršija minimalius tinklo, aparatūros ir programinės įrangos reikalavimus.

## <a name="network-requirements"></a>Tinklo reikalavimai
„Microsoft Dynamics 365 for Finance and Operations“ „Enterprise“ leidimas (vietinė versija) gali veikti tinkluose, kurie naudoja interneto protokolo versija 4 (IPv4) arba interneto protokolo 6 versija (IPv6). Planuodami savo sistemą atsižvelkite į tinklo aplinką ir vadovaukitės tolesniais nurodymais.

### <a name="network-response-time"></a>Tinklo atsakymo laikas
Tolesnėje lentelėje pateikiami minimalūs ryšio tarp žiniatinklio naršyklės ir „Application Object Server“ (AOS) nei ryšio tarp AOS ir vietinės sistemos duomenų bazės tinklo reikalavimai.

| Vertė     | Iš interneto naršyklės į AOS                      | Iš AOS į duomenų bazę |
|-----------|-----------------------------------------|------------------------------------------------------------------------------------------|
| Pralaidumas | 50 kilobaitų per sekundę (KB/s) vienam vartotojui | 100 MB per sekundę (MB/s) |
| Laukimo laikas   | Mažiau negu 250-300 milisekundžių (ms)     | Mažiau nei 1 ms (tik vietiniame tinkle [LAN]). AOS ir duomenų bazė turi būti vienoje vietoje. |

- „Finance and Operations“ (vietinė versija) skirta tinklams, kurių laukimo laikas ne didesnis nei 250–300 milisekundžių (ms). Šis laukimo laikas yra laukimo laikas ryšį perduodant iš naršyklės kliento į duomenų centrą, kuriame nuomojama „Finance and Operations“.
- „Finance and Operations“ (vietinės versijos) pralaidumo reikalavimai priklauso nuo jūsų scenarijaus. Įprastuose scenarijuose būtinas didesnis nei 50 kilobaitų per sekundę (KB/s) pralaidumas tarp naršyklės ir „Finance and Operations“ serverio. Tačiau tiems scenarijams, kurių mokamosios krovos reikalavimai aukšti, pvz., darbo sritims arba scenarijams, kurie apima nemažai tinkinimo, rekomenduojamas didesnis pralaidumas. Konkretus srauto dydis priklauso nuo naudojimo.

Įdiegtys, kuriose AOS ir „Microsoft SQL Server“ duomenų bazė yra skirtinguose duomenų centruose, nepalaikomos. AOS ir „SQL Server“ duomenų bazė turi būti vienoje vietoje. 

„Finance and Operations“ optimizuota siekiant sumažinti kreipimosi iš naršyklės į serverį ciklų skaičių. Bet kurio vartotojo veiksmo kreipimosi iš naršyklės kliento į duomenų centrą ciklų skaičius yra nulis arba vienas, o mokamoji krova yra suglaudinta.

> [!WARNING]
> Neskaičiuokite pralaidumo iš kliento vietos reikalavimų, vartotojų skaičių padauginę iš minimalių pralaidumo reikalavimų. Tam tikros vietos naudojimą vienu metu labai sunku apskaičiuoti. „Finance and Operations“ ne gamybos aplinkoje rekomenduojame naudoti realaus modeliavimo funkciją kaip geriausią našumo kriterijų jūsų konkrečiu atveju. 

### <a name="lan-environments"></a>LAN aplinkos
LAN aplinkoje „Microsoft Windows Server“ nereikalingas „Microsoft“ nuotolinis darbalaukis, kad būtų galima prisijungti prie „Finance and Operations“. Tačiau nuotolinis darbalaukis gali būti reikalingas norint atlikti operacijas virtualiuosiuose įrenginiuose (VM), kuriuose įrašytos serverio įdiegtys.

### <a name="wan-environments"></a>WAN aplinkos
Teritorinio tinklo (WAN) aplinkoje „Windows Server“ nereikalingas nuotolinis darbalaukis, kad būtų galima prisijungti prie „Finance and Operations“.

### <a name="internet-connectivity-requirements"></a>Interneto ryšio reikalavimai
„Finance and Operations“ (vietinei versijai) nereikalingas interneto ryšys iš vartotojo darbo vietos. Tačiau be interneto ryšio kai kurių funkcijų nebus galima naudoti.

|                    |   |
|--------------------|---|
| **Naršyklės klientas** | Intraneto be interneto ryšio scenarijus yra skirtas vietinėms įdiegtims. Nebus galima naudoti kai kurių funkcijų, kurioms reikalingos debesies paslaugos, pvz., žinyno ir užduočių vedlio bibliotekų „Microsoft Dynamics Lifecycle Services“ LCS. |
| **Serveriui**         | AOS arba „Microsoft Azure Service Fabric“ turi galėti prisijungti susisiekti su LCS. Vietiniam naršykle pagrįstam klientui interneto prieiga nebūtina. |
| **Telemetrija**      | Telemetrijos duomenys gali būti prarasti, jei ryšio pertraukos trunka ilgai. Ryšio su LCS pertraukos neturi įtakos vietinės programos funkcijoms. |
| **LCS**            | Prisijungimas prie LCS reikalingas atliekant diegimo, kodo diegimo ir aptarnavimo operacijas. |

## <a name="telemetry-data-transfer-to-the-cloud"></a>Telemetrijos duomenų perkėlimas į debesį
Dauguma telemetrijos duomenų saugomi vietoje ir „Microsoft Windows“ juos galima pasiekti naudojant įvykių peržiūros programą. Mažas telemetrijos įvykių pogrupis perkeliamas į „Microsoft“ telemetrijos srautą debesyje diagnostikai atlikti. Kliento duomenų ir vartotojo identifikavimo duomenų „Microsoft“ siunčiamuose telemetrijos duomenyse nėra. VM pavadinimai siunčiami „Microsoft“, siekiant pagerinti aplinkos valdymą ir diagnostiką iš LCS portalo.

## <a name="domain-requirements"></a>Domeno reikalavimai
Diegdami „Finance and Operations“ (vietinę versiją) atsižvelkite į toliau nurodytus domeno reikalavimus.

- Virtualiosios mašinos, kuriose nuomojami „Finance and Operations“ (vietinės versijos) komponentai, turi priklausyti „Active Directory“ domenui. „Active Directory“ domeno tarnybos (AD DS) turi būti sukonfigūruota vietiniu režimu.
- VM, kuriose veikia „Finance and Operations“ (vietinės versijos) komponentai, privalo turėti prieigą prie viena kitos. Ši prieiga konfigūruojama AD DS. 
- Domeno valdiklis turi būti „Microsoft Windows Server 2012 R2“ arba naujesnės versijos, funkcinis domeno lygis – 2012 R2 arba didesnis

## <a name="hardware-requirements"></a>Aparatūros reikalavimai
Šiame skyriuje aprašoma aparatūra, reikalinga norint paleisti „Finance and Operations“ (vietinę versiją).

Faktiniai aparatūros reikalavimai priklauso nuo sistemos konfigūracijos, duomenų struktūros ir programų bei funkcijų, kurias nuspręsite naudoti. Toliau pateikiami keletas veiksnių, kurie gali turėti įtakos renkantis „Finance and Operations“ (vietinei versijai) tinkamą aparatūrą.

- Operacijų skaičius per valandą
- Vienu metu dirbančių vartotojų skaičius

## <a name="minimum-infrastructure-requirements"></a>Minimalūs infrastruktūros reikalavimai
„Finance and Operations“ (vietinė versija) naudoja „Service Fabric“, kad galėtų nuomoti AOS, duomenų valdymo, valdymo ataskaitų priemonės ir aplinkos valdymo įrankio tarnybas. 

„SQL Server“ turi būti naudojama plačiai pasiekiama HADRON sąranka, kurioje yra bent du mazgai, naudotini gamyboje.

Toliau pateikiamame paveikslėlyje parodytas minimalus rekomenduojamas „Service Fabric“ klasterio mazgų skaičius.

[![Rekomenduojamas „Service Fabric“ klasterio mazgų skaičius](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Procesoriaus ir RAM reikalavimai
Tolesnėse lentelėse nurodomas procesorių skaičius ir laisvosios kreipties atminties (RAM) kiekis, būtini kiekviename vaidmenyje, kurių reikia šiai įdiegčiai paleisti. Daugiau informacijos skaitykite temoje apie „Service Fabric“ klasterio minimalius rekomenduojamus reikalavimus, [„Service Fabric“ klasterio planavimas ir ruošimas](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Jei tame pačiame kompiuteryje įdiegta kita „Microsoft“ programinė įranga, sistema taip pat turi atitikti tos programinės įrangos aparatūros reikalavimus. Jeigu tame pačiame kompiuteryje kaip AOS įdiegtos kitos serverio programos, rekomenduojame riboti kitas serverio programas iki 1 gigabaito (GB) RAM.

**Dydis pagal vaidmenį ir topologijos tipą**

| Topologija   | Vaidmuo (mazgo tipas)              | Rekomenduojami procesoriaus branduoliai | Rekomenduojama atmintis (GB) |
|------------|-------------------------------|-----------------------------|-------------------------|
| Gamyba | AOS, duomenų valdymas, paketas   | 8                           | 24                      |
|            | Valdymo ataskaitos priemonė           | 4                           | 16                      |
|            | SQL serverio ataskaitų tarnybos | 4                           | 16                      |
|            | Valdymo įrankis                  | 4                           | 16                      |
| Smėlio dėžė    | AOS, duomenų valdymas, paketas   | 4                           | 24                      |
|            | Valdymo ataskaitos priemonė           | 4                           | 16                      |
|            | SQL serverio ataskaitų tarnybos | 4                           | 16                      |
|            | Valdymo įrankis                  | 4                           | 16                      |

**Minimalūs apytiksliai gamybos ir smėlio dėžės įdiegčių dydžio skaičiavimai\***

| Topologija                                        | Vaidmuo                          | Egzempliorių skaičius |
|-------------------------------------------------|-------------------------------|---------------------|
| Gamyba                                      | AOS (duomenų valdymas, paketas)  | 3                   |
|                                                 | Valdymo ataskaitos priemonė           | 2                   |
|                                                 | SQL serverio ataskaitų tarnybos | 1                   |
|                                                 | Valdymo įrankis\*\*              | 3                   |
| Smėlio dėžė                                         | AOS, duomenų valdymas, paketas   | 2                   |
|                                                 | Valdymo ataskaitos priemonė           | 1                   |
|                                                 | SQL serverio ataskaitų tarnybos | 1                   |
|                                                 | Valdymo įrankis                  | 3                   |
| *Gamybos ir smėlio dėžės topologijos suvestinė* |                               | *16*                |

\* Šioje lentelėje skaičiai patvirtinti mūsų peržiūros klientų ir gali būti koreguojami atsižvelgiant į klientų atsiliepimus.

\*\* Valdymo įrankis sukurtas kaip pirminis mazgo tipas ir taip pat bus naudojamas „Service Fabric“ tarnyboms paleisti.

**Vidinio „SQL Server“ ir AD DS pradiniai skaičiavimai**

<table>
<thead>
<tr>
<th></th>
<th>Vaidmuo</th>
<th>VM / egzemplioriai</th>
<th>Branduoliai</th>
<th>Bendras branduolių skaičius</th>
<th>Atminties vienam egzemplioriui (GB)</th>
<th>Bendras atminties kiekis (GB)</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><strong>Bendra infrastruktūra</strong></td>
<td>SQL Server*</td>
<td>2</td>
<td>8</td>
<td>16</td>
<td>32</td>
<td>64</td>
</tr>
<tr>
<td>Failų serveris / saugojimo srities tinklas / patogiai prasiekiama saugykla</td>
<td colspan="5"><p>Vidinė saugykla turi būti pagrįsta netriniaisiais loginiais diskais (SSD), vykdymo laiko saugyklos srities tinkle (SAN).</p>
<p>Dydis ir įvesties / išvesties operacijų per sekundę (IOPS) pralaida priklauso nuo darbo krūvio dydžio.</p></td>
</tr>
<tr>
<td>„Active Directory“</td>
<td>3</td>
<td>4</td>
<td>12</td>
<td>16</td>
<td>48</td>
</tr>
<tr>
<td><em>Bendros infrastruktūros suvestinė</em></td>
<td></td>
<td><em>5</em></td>
<td></td>
<td><em>28</em></td>
<td></td>
<td><em>112</em></td>
</tr>
</tbody>
</table>

\*„SQL Server“ dydis labai priklauso nuo apkrovos. Daugiau informacijos žr. [Vietinės aplinkos aparatūros dydis](hardware-sizing-on-premises-environments.md).

## <a name="storage"></a>Saugojimas

- **AOS** – „Finance and Operations“ (vietinė versija) bendrai naudos 3.0 serverio pranešimų bloką (SMB) nesusistemintiems duomenims saugoti. Daugiau informacijos žr. [Tiesioginės saugojimo vietos „Windows Server 2016“](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – galimos toliau nurodytos pasirinktys:

    - Patogiai pasiekiama SSD sąranka
    - SAN, kuri optimizuota tinklo operacijų apdorojimo (OLTP) našumui
    - Efektyvi tiesioginio prijungimo saugykla (DAS) 

- **„SQL Server“ ir duomenų valdymo IOPS** – duomenų valdymo ir „SQL Server“ saugykloje turi būti ne mažiau kaip 2000 IOPS. Gamybos IOPS priklauso nuo daugelio veiksnių. Daugiau informacijos žr. [Vietinės aplinkos aparatūros dydis](hardware-sizing-on-premises-environments.md).
- **VM IOPS** – kiekviena VM turi turėti ne mažiau 100 rašymo IOPS.

## <a name="virtual-host-requirements"></a>Virtualaus pagrindinio kompiuterio reikalavimai
„Finance and Operations“ (vietinės versijos) aplinkoje nustatydami virtualųjį pagrindinį kompiuterį, vadovaukitės nurodymais: [„Service Fabric“ klasterio planavimas ir ruošimas](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) ir [„Service Fabric“ klasterio aprašymas](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Kiekviename virtualiajame pagrindiniame kompiuteryje turi būti pakankamai branduolių, atsižvelgiant į nustatytą infrastruktūros dydį. Galima naudoti kelias išplėstines konfigūracijas, kai „SQL Server“ patalpintas faktinėje aparatūroje, bet visa kita yra virtualu. Jei „SQL Server“ yra virtualus, disko posistemė turėtų būti greita SAN arba lygiavertė versija. Visais atvejais įsitikinkite, kad pagrindinė virtualiojo pagrindinio kompiuterio sąranka yra plačiai pasiekiama ir perteklinė. Visais atvejais, kai naudojamas virtualizavimas, VM momentinių kopijų fiksuoti nereikia.

## <a name="software-requirements-for-all-server-computers"></a>Visų serverio kompiuterių programinės įrangos reikalavimai
Prieš diegiant „Finance and Operations“ (vietinės versijos) komponentus, kompiuteryje būtina įdiegti toliau nurodytą programinę įrangą.

- „Microsoft .NET Framework“ versija 4.5.1 ar vėlesnė
- „Service Fabric‟

Daugiau informacijos žr. [„Service Fabric“ klasterio planavimas ir ruošimas](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Palaikomos serverio operacinės sistemos
Tolesnėje lentelėje išvardijamos serverio operacinės sistemos, kurias palaiko „Finance and Operations“ komponentai.

| Operacinė sistema                                     | Pastabos |
|------------------------------------------------------|-------|
| „Microsoft Windows Server 2016“ duomenų centras arba standartinė versija | Šie reikalavimai skirti duomenų centrui ir „Service Fabric“ klasteriui, kuris nuomoja AOS. |

## <a name="software-requirements-for-database-servers"></a>Duomenų bazių serverių programinės įrangos reikalavimai

- Palaikomos tik 64 bitų „SQL Server 2016“ versijos.
- Gamybos aplinkoje rekomenduojame įdiegti naujausią jūsų naudojamos „SQL Server“ versijos kaupiamąjį naujinimą (CU).
- „Finance and Operations“ (vietinė versija) palaiko „Unicode“ gretinimą, skiriant didžiąsias ir mažąsias raides, skiriant kirčius, skiriant kana simbolius ir skiriant plotį. Sugretinimas turi atitikti kompiuterio, kuriame veikia AOS egzemplioriai, „Windows“ lokalę. Jei nustatote naują įdiegtį, rekomenduojame pasirinkti „Windows“ sugretinimą, o ne „SQL Server“ sugretinimą. Daugiau informacijos apie tai, kaip pasirinkti „SQL Server“ duomenų bazės sugretinimą, žr. [„SQL Server“ dokumentai](/sql/sql-server/sql-server-technical-documentation).

Tolesnėje lentelėje išvardijamos „SQL Server“ versijos, kurias palaiko „Finance and Operations“ duomenų bazės. Daugiau informacijos, žr. minimalius [„SQL Server“](https://www.microsoft.com/en-us/sql-server/sql-server-2016) aparatūros reikalavimus.

| Poreikis                                                      | Pastabos |
|------------------------------------------------------------------|-------|
| „Microsoft SQL Server 2016“ „Standard“ leidimas arba „Enterprise“ leidimas | Informacijos apie „SQL Server 2016“ aparatūros reikalavimus žr. [„SQL Server 2016“ diegimo aparatūros ir programinės įrangos reikalavimai](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-application-object-server-aos"></a>Programos objektų serveriui (AOS) taikomi programinės įrangos reikalavimai 
- „SQL Server Integration Services“ (SSIS)

## <a name="software-requirements-for-reporting-server-bi"></a>Ataskaitų serveriui (BI) taikomi programinės įrangos reikalavimai
- „SQL Server Reporting Services“ (SSRS)

## <a name="software-requirements-for-client-computers"></a>Kliento kompiuterių programinės įrangos reikalavimai
„Finance and Operations“ žiniatinklio programą galima paleisti bet kuriame įrenginyje, kuriame naudojama HTML 5.0 reikalavimus atitinkančią žiniatinklio naršyklę. Toliau pateikti konkretūs įrenginio / naršyklės deriniai, kuriuos „Microsoft“ patvirtino:

- „Microsoft Edge‟ (naujausia viešai pasiekiama versija) sistemoje „Windows 10‟.
- „Internet Explorer 11‟ sistemose „Windows 10‟, „Windows 8.1‟ arba „Windows 7‟.
- „Google Chrome‟ (naujausia viešai pasiekiama versija) sistemose „Windows 10‟, „Windows 8.1‟, „Windows 8‟, „Windows 7‟ arba planšetėje „Google Nexus 10‟.
- „Apple Safari‟ (naujausia viešai pasiekiama versija) sistemoje „Mac OS X 10.10‟ („Yosemite‟), 10.11 („El Capitan‟) arba 10.12 („Sierra‟) arba planšetėje „Apple iPad‟.

## <a name="software-requirements-for-active-directory-federation-services"></a>„Active Directory“ susiejimo tarnybų programinės įrangos reikalavimai 
Būtinos „Active Directory Federation Services“ (AD FS), veikiančios „Windows Server 2016“

Domeno valdiklis turi būti „Windows Server 2012 R2“ arba naujesnės versijos, funkcinis domeno lygis – 2012 R2 arba didesnis Daugiau informacijos apie funkcinius domenų lygius žr. tolesniuose puslapiuose:

- [Kas yra „Active Directory“ funkciniai lygiai](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Kas yra „Active Directory“ domenų tarnybų funkciniai lygiai](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)

## <a name="supported-microsoft-office-applications"></a>Palaikomos „Microsoft Office“ taikomosios programos
„Finance and Operations“ įdiegtys debesyje ir vietinės įdiegtys palaiko toliau nurodytas „Microsoft Office“ programas.

-   Kad galėtumėte naudoti „Microsoft Excel“ ir „Microsoft Word“ papildinius, turi būti įdiegta „Windows“ arba „Mac“ skirta „Microsoft Office 2016“. Išsamios informacijos apie versijų reikalavimus žr. [„Office“ integravimo trikčių šalinimas](../../dev-itpro/office-integration/office-integration-troubleshooting.md).
-   Norėdami peržiūrėti dokumentus, sugeneruotus naudojant funkciją Eksportuoti į „Excel“ arba Eksportuoti į „Word“, turi būti įdiegta „Microsoft Office 2007“ arba naujesnė versija.
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>„Retail“ komponentų aparatūros ir programinės įrangos reikalavimai
Šiuo metu „Finance and Operations“ (vietinė versija) neapima „Retail“ komponentų.

