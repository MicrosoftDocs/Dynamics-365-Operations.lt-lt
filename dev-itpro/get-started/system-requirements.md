---
title: Sistemos reikalavimai
description: "Šioje temoje išvardyti šiai „Microsoft Dynamics 365 Finance and Operations“ „Enterprise‟ leidimo versijai (įdiegtims debesyje ir vietinėms įdiegtims) taikomi sistemos reikalavimai."
author: sericks007
manager: AnnBe
ms.date: 07/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 871ba89973f6af341c536f67db056bebb54600b3
ms.contentlocale: lt-lt
ms.lasthandoff: 07/25/2017

---

# <a name="system-requirements"></a>Sistemos reikalavimai

[!include[banner](../includes/banner.md)]


Šioje temoje išvardyti šiai „Microsoft Dynamics 365 Finance and Operations“ „Enterprise‟ leidimo versijai (įdiegtims debesyje ir vietinėms įdiegtims) taikomi sistemos reikalavimai. Prieš diegdami „Finance and Operations“, kai galėsite, patikrinkite, ar sistema, kurią naudojate, atitinka arba viršija minimalius tinklo, aparatūros ir programinės įrangos reikalavimus.


## <a name="supported-microsoft-office-applications"></a>Palaikomos „Microsoft Office“ taikomosios programos
„Finance and Operations“ įdiegtys debesyje ir vietinės įdiegtys palaiko toliau nurodytas „Office“ programas.
-   Kad galėtumėte naudoti „Microsoft Excel“ papildinius, turi būti įdiegta „Windows“ arba „Mac“ skirta „Microsoft Office 2016“. Išsamios informacijos apie versijų reikalavimus žr. [„Office“ integravimo trikčių šalinimas](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Norėdami peržiūrėti dokumentus, sugeneruotus naudojant funkciją Eksportuoti į „Excel“ arba Eksportuoti į „Word“, turi būti įdiegta „Microsoft Office 2007“ arba naujesnė versija.

# <a name="system-requirements-specific-to-cloud-deployments"></a>Įdiegtims debesyje taikomi sistemos reikalavimai
## <a name="network-requirements"></a>Tinklo reikalavimai
-   „Finance and Operations“ skirta tinklams, kurių laukimo laikas ne didesnis nei 250–300 milisekundžių (ms). Tai – laukimo laikas iš naršyklės kliento iki „Microsoft Azure“ duomenų centro, kuriame yra „Finance and Operations“. Rekomenduojame tinklo laukimo laiką patikrinti <http://www.azurespeed.com>.
-   „Finance and Operations“ pralaidumo reikalavimai priklauso nuo jūsų scenarijaus. Labiausiai įprastiems scenarijams reikia didesnio nei 50 kilobitų per sekundę (KB/s) pralaidumo. Tačiau tiems scenarijams, kurių mokamosios krovos reikalavimai aukšti, pvz., darbo sritims arba scenarijams, kurie apima nemažai tinkinimo, rekomenduojamas didesnis pralaidumas.

Apskritai „Finance and Operations“ yra optimizuotas internetui. Kreipimosi ciklų iš naršyklės kliento į „Azure“ duomenų centrą skaičius yra labai mažas, o visa mokamoji krova yra suglaudinta. 

> [!WARNING]
> Neskaičiuokite pralaidumo iš kliento vietos reikalavimų, vartotojų skaičių padauginę iš minimalių pralaidumo reikalavimų. Tam tikros vietos naudojimą vienu metu labai sunku apskaičiuoti. Klientams, kurie susirūpinę dėl pralaidumo reikalavimų, rekomenduojama naudoti „Finance and Operations“ peržiūros versiją.

## <a name="net-framework-requirements"></a>„.NET Framework“ reikalavimai
„Finance and Operations“ reikia „.NET Framework“ 4.6.2 versijos visoms vieno paspaudimo taikomosioms programoms, pvz., dokumento maršruto planavimo agentui. Diegimo instrukcijų žr. [„.NET Framework“ diegimas](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-web-browsers"></a>Palaikomos žiniatinklio naršyklės
Žiniatinklio programa gali veikti bet kurioje iš tolesnių žiniatinklio naršyklių, veikiančių nurodytose operacinėse sistemose.


-   „Microsoft Edge‟ (naujausia viešai pasiekiama versija) sistemoje „Windows 10‟.
-   „Internet Explorer 11‟ sistemose „Windows 10‟, „Windows 8.1‟ arba „Windows 7‟.
-   „Google Chrome‟ (naujausia viešai pasiekiama versija) sistemose „Windows 10‟, „Windows 8.1‟, „Windows 8‟, „Windows 7‟ arba planšetėje „Google Nexus 10‟.
-   „Apple Safari‟ (naujausia viešai pasiekiama versija) sistemoje „Mac OS X 10.10‟ („Yosemite‟), 10.11 („El Capitan‟) arba 10.12 („Sierra‟) arba planšetėje „Apple iPad‟.

Norėdami rasti naujausią kiekvienos žiniatinklio naršyklės leidimą, eikite į programinės įrangos gamintojo svetainę. 

> [!NOTE]
> -   Kad užduočių įrašymo priemonė galėtų fiksuoti ekrano kopijų vaizdus ir kad juos būtų galima įtraukti į sugeneruotus „Microsoft Word‟ dokumentus, turi būti įdiegtas negalutinis „Chrome‟ plėtinys. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   Darbo eigos rengyklė paleidžiama kaip „ClickOnce“ taikomoji programa. Tik „Microsoft Edge“ ir „Internet Explorer“ (palaikomoje „Microsoft Windows“ versijoje) palaiko „ClickOnce“ taikomąsias programas. Darbo eigos rengyklės „ClickOnce“ taikomajai programai reikia 64 bitų suderinamos operacinės sistemos.
> -   Finansinėms ataskaitoms skirtas ataskaitų konstruktorius paleidžiama kaip „ClickOnce“ taikomoji programa. Jam reikia 64 bitų suderinamos operacinės sistemos. Jei naudojate „Chrome“, turite įdiegti plėtinį „ClickOnce“, kad galėtumėte atsisiųsti ataskaitų konstruktoriaus klientą. Jei naudojate „Chrome“ inkognito režimu, įsitikinkite, kad plėtinys „ClickOnce“ nustatytas veikti ir inkognito režimu.
> -   Norint peržiūrėti PDF failus, rekomenduojame naudoti naršykles, pvz., „Microsoft Edge“ (naujausią viešai prieinamą versiją) sistemoje „Windows 10“ arba „Google Chrome“ (naujausią viešai prieinamą versiją) sistemoje „Windows 10“, „Windows 8.1“, „Windows 8“ ar „Windows 7“ arba „Google" Nexus 10“ planšetiniame kompiuteryje.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Palaikomos „Retail Cloud POS‟ žiniatinklio naršyklės

„Retail Cloud POS‟ gali veikti bet kurioje iš tolesnių žiniatinklio naršyklių, veikiančių nurodytose operacinėse sistemose.

-   „Microsoft Edge‟ (naujausia viešai pasiekiama versija) sistemoje „Windows 10‟.
-   „Internet Explorer 11‟ sistemose „Windows 10‟, „Windows 8.1‟ arba „Windows 7‟.
-   „Chrome‟ (naujausia viešai pasiekiama versija) sistemoje „Windows 10‟, „Windows 8.1“ arba „Windows 7“.

## <a name="retail-modern-pos-requirements"></a>„Retail Modern POS“ reikalavimai
### <a name="supported-operating-systems"></a>Palaikomos operacinės sistemos

-   „Retail Modern POS“ yra 32 bitų taikomoji programa, bet ji vykdoma ir x86, ir x64 architektūrose.
-   „Retail Modern POS“ palaikoma tik „Windows 10 Pro“, „Enterprise“ ir „Enterprise Long Term Servicing Branch“ (LTSB) leidimai.

### <a name="minimum-system-requirements"></a>Minimalūs sistemos reikalavimai

-   Mažiausia palaikoma skiriamoji geba yra 1280 × 1024.
-   Kompiuteris, kuriame vykdoma „Retail Modern POS“, turi atitikti šiuos reikalavimus:
    -   Jame turi būti mažiausiai dviejų branduolių procesorius, veikiantis ne mažiau kaip 2 gigahercų (GHz) dažniu.
    -   Turi turėti mažiausiai 3 gigabaitų (GB) RAM.
    -   Būtina interneto prieiga.

## <a name="retail-hardware-station-requirements"></a>„Retail“ aparatūros stoties reikalavimai
### <a name="supported-operating-systems"></a>Palaikomos operacinės sistemos

-   „Retail“ aparatūros stotis yra 32 bitų taikomoji programa, bet ji vykdoma ir x86, ir x64 architektūrose.
-   „Retail“ aparatūros stotį palaiko šios operacinės sistemos:
    -   „Windows 7 Professional“, „Enterprise“ ir „Ultimate“ leidimuose 
    
    > [!NOTE]
    > „Windows 7“ palaikoma tik jei sistemoje neautomatiškai įdiegta „Internet Explorer 11“.

    -   „Windows 8.1“ 1 naujinimas „Professional“, „Enterprise“ ir įdėtieji leidimai
    -   „Windows 10 Pro“, „Enterprise“ ir „Enterprise LTSB“ leidimai

### <a name="minimum-system-requirements"></a>Minimalūs sistemos reikalavimai

Kompiuteris turi atitikti visus sistemos reikalavimus, norint įdiegti ir naudoti šiuos elementus:

-   Interneto informacijos tarnybos (IIS)
-   trečiųjų šalių aparatūrą;

## <a name="retail-store-scale-unit-requirements"></a>„Retail Store Scale Unit“ reikalavimus;
### <a name="supported-operating-systems"></a>palaikomas operacines sistemas.

-   „Retail Store Scale Unit“ yra 32 bitų taikomoji programa, bet vykdoma ir x86, ir x64 architektūrose.
-   „Retail Store Scale Unit“ palaikoma šiose operacinėse sistemose:
    -   „Windows 7 Professional“, „Enterprise“ ir „Ultimate“ leidimuose
    -   „Windows 8.1“ 1 naujinimas „Professional“, „Enterprise“ ir įdėtieji leidimai
    -   „Windows 10 Pro“, „Enterprise“ ir „Enterprise LTSB“ leidimai

### <a name="minimum-system-requirements"></a>Minimalūs sistemos reikalavimai

-   4 GB RAM
-   1,6 GHz didžiausia CPU sparta branduolyje (Mažiausiai dviejų branduolių.)
-   Bent 10 GB laisvos vietos (Kanalo duomenų bazei reikia daug vietos.)

### <a name="recommended-system-requirements"></a>Rekomenduojami sistemos reikalavimai

-   6 GB RAM
-   2,4 GHz i7 (arba atitikmuo) didžiausia CPU sparta branduolyje (Rekomenduojama keturių branduolių.)
-   Bent 10 GB laisvos vietos (Kanalo duomenų bazei reikia daug vietos.)

## <a name="connector-requirements"></a>Jungčių reikalavimai
### <a name="supported-operating-systems"></a>Palaikomos operacinės sistemos

-   „Microsoft Dynamics AX‟ jungtis turi dvi atskiras diegimo programas – **„Async Server Connector service‟** ir **„Real-time service for Dynamics AX 2012 R3‟**.
-   Abu komponentai yra 32 bitų programos, tačiau veikia ir x86, ir x64 architektūrose.
-   Abu komponentai palaikomi tolesnėse operacinėse sistemose.
    -   „Windows 7 Professional“, „Enterprise“ ir „Ultimate“ leidimuose
    -   „Windows 8.1“ 1 naujinimas „Professional“, „Enterprise“ ir įdėtieji leidimai
    -   „Windows 10 Pro“, „Enterprise“ ir „Enterprise LTSB“ leidimai
    -   „Windows Server 2012 R2‟, „Windows Server 2016‟

### <a name="minimum-system-requirements"></a>Minimalūs sistemos reikalavimai

-   Rekomenduojama – 2 GB RAM, 4 GB RAM
-   1,6 GHz didžiausia CPU sparta branduolyje (Mažiausiai dviejų branduolių.)
-   Bent 10 GB laisvos vietos (Kanalo duomenų bazei reikia daug vietos.)

## <a name="requirements-for-development-on-local-vms"></a>Reikalavimai norint kurti vietiniuose virtualiuosiuose įrenginiuose
Išsamesnės informacijos apie reikalavimus norint kurti vietiniuose virtualiuosiuose įrenginiuose (VM) žr. [VM vykdymas vietoje](../dev-tools/access-instances.md).

# <a name="system-requirements-for-on-premises-deployments"></a>Vietinėms įdiegtims taikomi sistemos reikalavimai

## <a name="network-requirements"></a>Tinklo reikalavimai
„Finance and Operations“ (vietinė versija) gali veikti tinkluose, kurie naudoja interneto protokolo 4 versiją („IPv4“) arba interneto protokolo 6 versiją („IPv6“). Planuodami savo sistemą atsižvelkite į tinklo aplinką ir vadovaukitės tolesniais nurodymais.

### <a name="network-response-time"></a>Tinklo atsakymo laikas
Tolesnėje lentelėje pateikiami minimalūs ryšio tarp žiniatinklio naršyklės ir „Application Object Server“ (AOS) nei ryšio tarp AOS ir vietinės sistemos duomenų bazės tinklo reikalavimai.

| Vertė     | Iš interneto naršyklės į AOS | Iš AOS į duomenų bazę                                            |
|-----------|--------------------|------------------------------------------------------------|
| Pralaidumas | 50 KB/s vienam vartotojui   | 100 MB/s                                                   |
| Laukimo laikas   | < 250–300 ms       | < 1 ms (tik LAN). AOS ir duomenų bazė turi būti vienoje vietoje. |

- „Finance and Operations“ (vietinė versija) skirta tinklams, kurių laukimo laikas ne didesnis nei 250–300 milisekundžių (ms). Šis laukimo laikas yra laukimo laikas ryšį perduodant iš naršyklės kliento į duomenų centrą, kuriame nuomojama „Finance and Operations“.
- „Finance and Operations“ (vietinės versijos) pralaidumo reikalavimai priklauso nuo jūsų scenarijaus. Įprastuose scenarijuose būtinas didesnis nei 50 kilobaitų per sekundę (KB/s) pralaidumas tarp naršyklės ir „Finance and Operations“ serverio. Tačiau tuose scenarijuose, kurių mokamosios krovos reikalavimai aukšti, pvz., darbo srityse arba scenarijuose, kurie apima nemažai tinkinimo veiksmų, rekomenduojamas pralaidumas yra didesnis ir jis priklauso naudojimo.
Įdiegtys, kuriose AOS ir „SQL Server“ duomenų bazė yra skirtingose duomenų centruose, nepalaikomos. AOS ir „SQL Server“ duomenų bazė turi būti vienoje vietoje. „Finance and Operations“ optimizuota siekiant sumažinti kreipimosi iš naršyklės į serverį ciklų skaičių. Bet kurio vartotojo veiksmo kreipimosi iš naršyklės kliento į duomenų centrą ciklų skaičius yra nulis arba vienas, o mokamoji krova yra suglaudinta.

> [!WARNING]
> Neskaičiuokite pralaidumo iš kliento vietos reikalavimų, vartotojų skaičių padauginę iš minimalių pralaidumo reikalavimų. Tam tikros vietos naudojimą vienu metu labai sunku apskaičiuoti. „Finance and Operations“ ne gamybos aplinkoje rekomenduojame naudoti realaus modeliavimo funkciją kaip geriausią našumo kriterijų jūsų konkrečiu atveju. 

### <a name="lan-environments"></a>LAN aplinkos
Vietinio tinklo (LAN) aplinkoje „Microsoft Windows Server“ nereikalingas „Microsoft“ nuotolinis darbalaukis, kad būtų galima prisijungti prie „Finance and Operations“. Tačiau tai gali būti reikalinga norint atlikti operacijas VM, kuriose įrašytos serverio įdiegtys.

### <a name="wan-environments"></a>WAN aplinkos
Teritorinio tinklo (WAN) aplinkoje „Windows Server“ nereikalingas nuotolinis darbalaukis, kad būtų galima prisijungti prie „Finance and Operations“.

### <a name="internet-connectivity-requirements"></a>Interneto ryšio reikalavimai
„Finance and Operations“ (vietinei versijai) nereikalingas interneto ryšys iš galutinio vartotojo darbo vietos. Tačiau be interneto ryšio kai kurių funkcijų nebus galima naudoti.

| Naršyklės klientas | Intraneto be interneto ryšio scenarijus yra skirtas vietinėms įdiegtims. Nebus galima naudoti kai kurių funkcijų, kurioms reikalingos debesies paslaugos, pvz., žinyno ir užduočių vedlio bibliotekų LCS. |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Serveris         | AOS arba „Service Fabric“ turi galėti prisijungti susisiekti su LCS. Vietiniam naršykle pagrįstam klientui interneto prieiga nebūtina.                                                                                |
| Telemetrija      | Telemetrijos duomenys gali būti prarasti, jei ryšio pertraukos trunka ilgai. Ryšio su LCS pertraukos neturi įtakos vietinės programos funkcijoms.                                                |
| LCS            | Prisijungimas prie LCS reikalingas atliekant diegimo, kodo diegimo ir aptarnavimo operacijas.                                                                                                                                 |
## <a name="telemetry-data-transfer-to-the-cloud"></a>Telemetrijos duomenų perkėlimas į debesį
Dauguma telemetrijos duomenų saugomi vietoje ir „Microsoft Windows“ juos galima pasiekti naudojant įvykių peržiūros programą. Mažas telemetrijos įvykių pogrupis perkeliamas į „Microsoft“ telemetrijos srautą debesyje diagnostikai atlikti. Kliento duomenų ir galutinio vartotojo identifikavimo duomenų „Microsoft“ siunčiamoje telemetrijoje nėra. VM pavadinimai siunčiami „Microsoft“, siekiant pagerinti aplinkos valdymą ir diagnostiką iš LCS portalo.

## <a name="domain-requirements"></a>Domeno reikalavimai
Diegdami „Finance and Operations“ (vietinę versiją) atsižvelkite į toliau nurodytus domeno reikalavimus.

- Virtualiosios mašinos, kuriose nuomojami „Finance and Operations“ (vietinės versijos) komponentai, turi priklausyti „Active Directory“ domenui. „Active Directory“ domeno tarnybos (AD DS) turi būti sukonfigūruota vietiniu režimu.
- Virtualiosios mašinos, kurios naudoja „Finance and Operations“ (vietinės versijos) komponentus, privalo turėti prieigą prie kitų sukonfigūruotų „Active Directory“ domenų tarnybų. 
- Domeno valdiklis turi veikti „Microsoft Windows Server 2016“.

## <a name="hardware-requirements"></a>Aparatūros reikalavimai
Šiame skyriuje aprašoma aparatūra, reikalinga norint paleisti „Finance and Operations“ (vietinę versiją).
Atsižvelgiant į sistemos konfigūraciją, duomenų struktūrą ir programų bei funkcijas, kurias nuspręsite naudoti, faktiniai aparatūros reikalavimai skirsis. Toliau pateikiami keletas veiksnių, kurie gali turėti įtakos renkantis „Finance and Operations“ (vietinei versijai) tinkamą aparatūrą.

- Operacijos skaičius per valandą.
- Vienu metu dirbančių vartotojų skaičius.

## <a name="minimum-infrastructure-requirements"></a>Minimalūs infrastruktūros reikalavimai
„Finance and Operations“ (vietinė versija) naudoja „Microsoft" Azure Service Fabric“, kad galėtų nuomoti AOS, duomenų valdymo, valdymo ataskaitų priemonės ir aplinkos valdymo įrankio tarnybas. „Microsoft SQL Server“ ataskaitų tarnybos (SSRS) nėra nuomojamos „Service Fabric“ klasteryje.
„SQL Server“ reikia nustatyti plačiai pasiekiamoje HADRON sąrankoje, kurioje yra bent du mazgai, naudotini gamyboje.
Toliau pateikiamame paveikslėlyje parodytas minimalus rekomenduojamas „Service Fabric“ klasterio mazgų skaičius.

[![rekomenduojamas „Service Fabric“ klasterio mazgų skaičius](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Procesoriaus ir RAM reikalavimai
Tolesnėje lentelėje nurodomas procesorių skaičius ir laisvosios kreipties atminties (RAM) kiekis, būtini kiekviename vaidmenyje, kurių reikia šiai įdiegčiai paleisti. Daugiau informacijos skaitykite temoje apie „Service Fabric“ klasterio minimalius rekomenduojamus reikalavimus, [„Service Fabric“ klasterio planavimas ir ruošimas](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Jei tame pačiame kompiuteryje įdiegta kita „Microsoft“ programinė įranga, sistema taip pat turi atitikti tos programinės įrangos aparatūros reikalavimus. Rekomenduojame riboti kitas serverio programas tame pačiame kompiuteryje: AOS iki 1 gigabaito (GB) RAM.

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

**Minimalūs apytiksliai gamybos ir smėlio dėžės įdiegčių dydžio skaičiavimai**\*

| Topologija                                  | Vaidmuo                          | Egzempliorių skaičius |
|-------------------------------------------|-------------------------------|---------------------|
| Gamyba                                | AOS (duomenų valdymas, paketas)  | 3                   |
|                                           | Valdymo ataskaitos priemonė           | 2                   |
|                                           | SQL serverio ataskaitų tarnybos | 1                   |
|                                           | Valdymo įrankis\*\*                | 3                   |
| Smėlio dėžė                                   | AOS, duomenų valdymas, paketas   | 2                   |
|                                           | Valdymo ataskaitos priemonė           | 1                   |
|                                           | SQL serverio ataskaitų tarnybos | 1                   |
|                                           | Valdymo įrankis                  | 3                   |
| *Suvestinės gamybos ir smėlio dėžės topologijos* |                               | 16                  |

\*Šiuos skaičius peržiūri ir tvirtina mūsų klientai, ir , prireikus, juos galima koreguoti atsižvelgiant į jų atsiliepimus.

\*\*Valdymo įrankis sukurtas kaip pirminis mazgo tipas ir taip pat bus naudojamas „Service Fabric“ tarnyboms paleisti.

**Vidinis „SQL Server“ ir AD pradiniai skaičiavimai**

[![Vidinis „SQL Server“ ir AD pradiniai skaičiavimai](./media/system-reqs-on-premises-02.PNG)](./media/system-reqs-on-premises-02.PNG) 

\*„SQL Server“ dydis labai priklauso nuo apkrovos. Daugiau informacijos žr. skyrių [Vietinės aplinkos aparatūros dydis](#Hardware-sizing-for-on-premises-environments).

## <a name="storage"></a>Saugojimas

- **AOS** – „Finance and Operations“ (vietinė versija) bendrai naudos 3.0 serverio pranešimų bloką (SMB) nesusistemintiems duomenims saugoti. Daugiau informacijos žr. [Tiesioginės saugojimo vietos „Windows Server 2016“](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – perspektyvios parinktys.
    - Plačiai pasiekiama netriniojo loginio disko (SSD) sąranka.
    - Saugojimo srities tinklas (SAN) optimizuotas OLTP našumui užtikrinti.
    - Efektyvi tiesioginio prijungimo saugykla (DAS) 
- **SQL ir duomenų valdymo IOPS** – duomenų valdymo ir „SQL Server“ saugykloje turi būti ne mažiau kaip 2000 įvesties / išeigos operacijų per sekundę (IOPS). Gamybos IOPS priklauso nuo daugelio veiksnių. Daugiau informacijos žr. skyrių „Vietinės aplinkos aparatūros dydis“. 
- **Virtualiosios mašinos IOPS** – kiekvienoje virtualiojoje mašinoje turi būti bent 100 rašymo IOPS.

## <a name="virtual-host-requirements"></a>Virtualaus pagrindinio kompiuterio reikalavimai
„Finance and Operations“ (vietinės versijos) aplinkoje nustatydami virtualųjį pagrindinį kompiuterį, vadovaukitės šiais nurodymais: [„Service Fabric“ klasterio planavimas ir ruošimas](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) ir [„Service Fabric“ klasterio aprašymas](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Kiekviename virtualiajame pagrindiniame kompiuteryje turi būti pakankamai branduolių, atsižvelgiant į nustatytą infrastruktūros dydį. Galima naudoti kelias išplėstines konfigūracijas, kai „SQL Server“ patalpintas faktinėje aparatūroje, bet visa kita yra virtualu. Jei „SQL Server“ yra virtualus, disko posistemė turėtų būti greita SAN arba lygiavertė versija. Visais atvejais įsitikinkite, kad pagrindinė virtualiojo pagrindinio kompiuterio sąranka yra plačiai pasiekiama ir perteklinė. Visais atvejais, kai naudojamas virtualizavimas, VM momentinių kopijų fiksuoti nereikia.

## <a name="software-requirements-for-all-server-computers"></a>Visų serverio kompiuterių programinės įrangos reikalavimai
Prieš diegiant „Finance and Operations“ (vietinės versijos) komponentus, kompiuteryje būtina įdiegti toliau nurodytą programinę įrangą.

- „Microsoft .NET Framework 4.5.1“ arba naujesnė versija
- „Service Fabric“ Daugiau informacijos žr. [„Service Fabric“ klasterio planavimas ir ruošimas](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Palaikomos serverio operacinės sistemos
Tolesnėje lentelėje išvardijamos serverio operacinės sistemos, kurias palaiko „Finance and Operations“ komponentai.

| Operacinė sistema                                     | Pastabos                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------|
| „Microsoft Windows Server 2016“ duomenų centras arba standartinė versija | Šie reikalavimai skirti duomenų centrui ir „Service Fabric“ klasteriui, kuris nuomoja AOS. |

## <a name="software-requirements-for-database-servers"></a>Duomenų bazių serverių programinės įrangos reikalavimai

- Palaikomos tik 64 bitų „SQL Server 2016“ versijos.
- Gamybos aplinkoje rekomenduojame įdiegti naujausią jūsų naudojamos „SQL Server“ versijos kaupiamąjį naujinimą (CU).
- „Finance and Operations“ (vietinė versija) palaiko „Unicode“ gretinimą, skiriant didžiąsias ir mažąsias raides, skiriant kirčius, skiriant kana simbolius ir skiriant plotį. Sugretinimas turi atitikti kompiuterio, kuriame veikia AOS egzemplioriai, „Windows“ lokalę. Jei nustatote naują įdiegtį, rekomenduojame pasirinkti „Windows“ sugretinimą, o ne „SQL Server“ sugretinimą. Daugiau informacijos apie tai, kaip pasirinkti „SQL Server“ duomenų bazės sugretinimą, žr. [„SQL Server“ dokumentai](/sql/sql-server/sql-server-technical-documentation).
Tolesnėje lentelėje išvardijamos „SQL Server“ versijos, kurias palaiko „Finance and Operations“ duomenų bazės. Daugiau informacijos, žr. minimalius [„SQL Server“](https://www.microsoft.com/en-us/sql-server/sql-server-2016) aparatūros reikalavimus.

| Poreikis                                                      | Pastabos                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| „Microsoft SQL Server 2016“ „Standard“ leidimas arba „Enterprise“ leidimas | Informacijos apie „SQL Server 2016“ aparatūros reikalavimus žr. [„SQL Server 2016“ diegimo aparatūros ir programinės įrangos reikalavimai](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-client-computers"></a>Kliento kompiuterių programinės įrangos reikalavimai
„Finance and Operations“ žiniatinklio programą galima paleisti bet kuriame įrenginyje naudojant su HTML5.0 reikalavimus atitinkančią žiniatinklio naršyklę. Konkretūs įrenginio / naršyklės deriniai, kuriuos „Microsoft“ patvirtino:

- „Microsoft Edge‟ (naujausia viešai pasiekiama versija) sistemoje „Windows 10‟.
- „Internet Explorer 11‟ sistemose „Windows 10‟, „Windows 8.1‟ arba „Windows 7‟.
- „Google Chrome‟ (naujausia viešai pasiekiama versija) sistemose „Windows 10‟, „Windows 8.1‟, „Windows 8‟, „Windows 7‟ arba planšetėje „Google Nexus 10‟.
- „Apple Safari‟ (naujausia viešai pasiekiama versija) sistemoje „Mac OS X 10.10‟ („Yosemite‟), 10.11 („El Capitan‟) arba 10.12 („Sierra‟) arba planšetėje „Apple iPad‟.

## <a name="software-requirements-for-active-directory-federation-services"></a>„Active Directory“ susiejimo tarnybų programinės įrangos reikalavimai 
„Active Directory Federation Services“ (AD FS), veikianti „Windows Server 2016“

Domeno valdiklis turi būti „Windows Server 2012 R2“ arba naujesnės versijos, funkcinis domeno lygis – 2012 R2 arba didesnis

Daugiau informacijos apie funkcinius domenų lygius žr.: 
- [Kas yra „Active Directory“ funkciniai lygiai](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Kas yra „Active Directory“ domenų tarnybų funkciniai lygiai](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>„Retail“ komponentų aparatūros ir programinės įrangos reikalavimai
„Finance and Operations“ (vietinė versija) šiuo metu neapima „Retail“ komponentų.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[„Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidimo įvertinimo kopijos gavimas](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

