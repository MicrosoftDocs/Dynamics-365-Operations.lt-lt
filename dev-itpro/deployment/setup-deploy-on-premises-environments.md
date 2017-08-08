---
title: "Vietinių aplinkų nustatymas ir diegimas"
description: "Šioje temoje pateikiama informacija apie tai, kaip planuoti, nustatyti ir įdiegti vietinę aplinką."
author: kfend
manager: AnnBe
ms.date: 06/14/2017
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
ms.author: sarvanisathish
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 3e9a2e33d9579769f6808b598f865d75f072c450
ms.openlocfilehash: 7caf033ab2de5afd6a2d88fa2d41631df4542cbe
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---

# <a name="set-up-and-deploy-on-premises-environments"></a>Vietinių aplinkų nustatymas ir diegimas

Šiame dokumente aprašoma, kaip planuoti diegimą, nustatyti infrastruktūrą ir įdiegti „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimą (vietinę versiją).

## <a name="finance-and-operations-components"></a>„Finance and Operations” komponentai

„Finance and Operations“ programą sudaro trys pagrindiniai komponentai.

- Programos objektų serveris (AOS)
- Verslo įžvalgos (BI)
- Finansinės ataskaitos / valdymo ataskaitos priemonė

Šie komponentai priklauso nuo toliau nurodytos sistemos programinės įrangos.

- „Microsoft Windows Server 2016“
- „Microsoft SQL Server 2016 SP1“, turinti toliau nurodytas funkcijas.

    - Įjungta viso teksto turinio ieška.
    - „SQL Server Reporting Services“ (SSRS).
    - „SQL Server Integration Services“ (SSIS).
    
     > [!NOTE]
     > Programa neveiks, jei viso teksto turinio ieška nebus įjungta.

- SQL serverio valdymo studija
- Atskira „Microsoft Azure Service Fabric“
- „Windows PowerShell 5.0“ arba naujesnė versija
- „Active Directory Federation Services“ (AD FS), veikianti „Windows Server 2016“

  Domeno valdiklis turi būti „Windows Server 2012 R2“ arba naujesnės versijos, funkcinis domeno lygis – 2012 R2 arba didesnis

  Daugiau informacijos apie funkcinius domenų lygius žr.: 
  - [Kas yra „Active Directory“ funkciniai lygiai](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
  - [Kas yra „Active Directory“ domenų tarnybų funkciniai lygiai](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)


## <a name="lifecycle-services"></a>„Lifecycle Services‟

„Finance and Operations“ dalys platinamos per „Microsoft Dynamics Lifecycle Services“ (LCS). Prieš diegdami turite įsigyti licencijos raktus naudodami kanalą [„Enterprise“ sutartys](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) ir LCS nustatyti vietinį projektą. Diegimą galima inicijuoti tik per LCS. Daugiau informacijos apie tai, kaip LCS nustatyti vietinius projektus, žr. [Vietinio projekto kūrimas „Lifecycle Services“](../lifecycle-services/lbd-create-lcs-on-prem-project.md).

## <a name="authentication"></a>Autentifikavimas

Vietinė programa veikia su AD FS. Norint palaikyti sąveiką su LCS, taip pat reikia sukonfigūruoti „Azure Active Directory“ („Azure AD“).

## <a name="standalone-service-fabric"></a>Atskira „Service Fabric“

„Finance and Operations“ naudoja atskirą „Service Fabric“. Daugiau informacijos žr. [„Service Fabric“ dokumentai](/azure/service-fabric/).

## <a name="infrastructure"></a>Infrastruktūra

„Finance and Operations“ sukurta veikti itin susietoje architektūroje. Aparatūros konfigūracija apima toliau nurodytus komponentus.

- Atskiras „Service Fabric“ klasteris, pagrįstas „Windows Server 2016“ virtualiosiomis mašinomis (VM)
- „SQL Server“ (palaikomi SQL: „Clustered“ ir „Always-On“)
- Autentifikavimo AD FS
- Serverio pranešimų bloko (SMB) 3 versijos failų bendrinimo saugykla
- Pasirinktinai: „Microsoft Office Server 2017“

Daugiau informacijos žr. dalį [Sistemos reikalavimai](../get-started/system-requirements.md) ir dydžio nustatymo instrukcijas.

### <a name="hardware-layout"></a>Aparatūros maketas

Suplanuokite savo infrastruktūros ir „Service Fabric“ klasterį pagal rekomenduojamą dydį, nurodytą temoje [Aparatūros dydžio nustatymas vietinėse aplinkose](../get-started/hardware-sizing-on-premises-environments.md). Daugiau informacijos apie tai, kaip planuoti „Service Fabric“ klasterį, žr. [„Service Fabric“ atskiro klasterio diegimo planavimas ir ruošimas](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

Tolesnėje lentelėje pateikiamas aparatūros maketo pavyzdys. Visoje šioje temoje šis pavyzdys naudojamas sąrankai pavaizduoti.

> [!NOTE]
> „Service Fabric“ klasterio pirminis mazgas privalo turėti bent tris mazgus. Šiame pavyzdyje **OrchestratorType** apibrėžiamas kaip pirminio mazgo tipas.

| Mašinos paskirtis                                 | Mašinos pavadinimas    | IP adresas    |
|-------------------------------------------------|-----------------|---------------|
| Domeno valdiklis                               | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                                           | DAX7SQLAOADFS1  | 10.179.108.3  |
| Rinkmenos serveris                                     | DAX7SQLAOFILE1  | 10.179.108.4  |
| „SQL Always-On“ klasteris                           | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                                                 | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                                                 | DAX7SQLAOSQLA   | 10.179.108.9  |
| Klientas                                          | SQLAOCLIENT1    | 10.179.108.11 |
| „Service Fabric“ klasteris / AOS 1                    | SQLAOSF1AOS1    | 10.179.108.12 |
| „Service Fabric“ klasteris / AOS 2                    | SQLAOSF1AOS2    | 10.179.108.13 |
| „Service Fabric“ klasteris / AOS 3                    | SQLAOSF1AOS3    | 10.179.108.14 |
| „Service Fabric“ klasteris / 1 valdymo įrankis           | SQLAOSF1ORCH1   | 10.179.108.15 |
| „Service Fabric“ klasteris / 2 valdymo įrankis           | SQLAOSF1ORCH2   | 10.179.108.16 |
| „Service Fabric“ klasteris / 3 valdymo įrankis           | SQLAOSF1ORCH3   | 10.179.108.17 |
| „Service Fabric“ klasteris / „Management Reporter“ mazgas | SQLAOSMR1       | 10.179.108.18 |
| „Service Fabric“ klasteris / SSRS mazgas                | SQLAOSFBIN1     | 10.179.108.10 |

## <a name="setup"></a>Sąranka

### <a name="prerequisites"></a>Būtinieji komponentai

Norint pradėti sąranką, reikia patenkinti toliau nurodytas būtinąsias sąlygas. Šių būtinųjų sąlygų sąranka į šį dokumentą neįtraukti.

- „Active Directory“ domenų tarnybos (AD DS) įdiegiamos ir sukonfigūruojamos jūsų tinkle.
- Įdiegiama AD FS.
- Įdiegiami „SQL Server“, SSRS ir „Management Studio“.

### <a name="overview"></a>Apžvalga

Norint nustatyti „Finance and Operations“ infrastruktūrą, reikia atlikti toliau nurodytus veiksmus.

1. Suplanuoti domeno vardą ir DNS zonas
2. Suplanuoti ir gauti sertifikatus
3. Suplanuoti vartotojus ir tarnybos paskyras
4. Sukurti DNS zonas ir įtraukti A įrašų
5. Prijungti virtualiąsias mašinas prie domeno
6. Į virtualiąsias mašinas įdiegti būtiną programinę įrangą
7. Atsisiųsti sąrankos scenarijus iš LCS
8. Aprašyti savo konfigūraciją
9. Įdiegti sertifikatus
10. Nustatyti atskirą „Service Fabric“ klasterį
11. Sukonfigūruoti nuomininko LCS ryšį
12. Nustatyti failų saugyklą
13. Nustatyti „SQL Server“
14. Sukonfigūruoti duomenų bazes
15. Užšifruoti kredencialus
16. Nustatyti SSRS
17. Sukonfigūruoti AD FS

### <a name="plan-your-domain-name-and-dns-zones"></a>Suplanuoti domeno vardą ir DNS zonas

Diegiant gamybos AOS rekomenduojame naudoti viešai užregistruoto domeno vardą. Tokiu būdu jį galima pasiekti būnant ne tinkle, jei reikia prisijungti iš išorės.

Pavyzdžiui, jei jūsų įmonės domenas yra contoso.com, jūsų „Finance and Operations“ (vietinės versijos) zona gali būti d365ffo.onprem.contoso.com, o pagrindinių kompiuterių vardai gali būti tokie:

- ax.d365ffo.onprem.contoso.com (AOS mašinos)
- sf.d365ffo.onprem.contoso.com („Service Fabric“ klasteris)

### <a name="plan-and-acquire-your-certificates"></a>Suplanuoti ir gauti sertifikatus

Saugiųjų jungčių lygmens (SSL) sertifikatai būtini norint apsaugoti „Service Fabric“ klasterį ir visas įdiegtas programas. Gamybos ir smėlio dėžės darbo krūviai: rekomenduojame įsigyti sertifikatus iš sertifikavimo tarnybos (CA), pavyzdžiui, [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate) arba [GlobalSign](https://www.globalsign.com/en/ssl/). Jei jūsų domene nustatyta [„Active Directory“ sertifikavimo tarnybos](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS), sertifikatus galite kurti per AD CS. Kiekvienas sertifikatas privalo turėti privatųjį raktą, sukurtą raktų mainams atlikti, ir jį turi būti galima eksportuoti į apsikeitimo asmenine informacija (.pfx) failą.

Vartotojo pasirašomus sertifikatus galima naudoti tik tikrinimo tikslais. Dėl patogumo į sąrankos scenarijus įtraukti scenarijai, kurių metu generuojami ir eksportuojami vartotojo pasirašomi sertifikatai. Kaip jau minėta, šiuos sertifikatus galima naudoti tik tikrinimo tikslais.

| Paskirtis                                      | Paaiškinimas | Papildomi reikalavimai |
|----------------------------------------------|-------------|-------------------------|
| „SQL Server SSL“ sertifikatas                   | Šis sertifikatas naudojamas norint užšifruoti duomenis, kurie tinklu perduodami tarp „SQL Server“ ir kliento programos. | <p>Sertifikato domeno vardas turi atitikti „SQL Server“ egzemplioriaus arba nukreipimo priemonės visiškai apibrėžtą domeno vardą (FQDN).</p><p>Pavyzdžiui, jei SQL nukreipimo priemonė nuomojama mašinoje DAX7SQLAOSQLA, sertifikato DNS pavadinimas yra DAX7SQLAOSQLA.onprem.contoso.com.</p> |
| „Service Fabric Server“ sertifikatas            | Šis sertifikatas naudojamas norint apsaugoti „iš mazgo į mazgą“ perduodamą ryšį tarp „Service Fabric“ mazgų. Šis sertifikatas taip pat naudojamas kaip „Server“ sertifikatas, kuris pateikiamas prie klasterio prisijungusiam klientui. | <p>Sertifikato domeno vardas turi atitikti DNS zoną, kurioje nuomojami AOS ir „Service Fabric“.</p><p>Pavyzdžiui, sertifikato domeno pavadinimas gali būti \*.onprem.contoso.com arba \*.contoso.com.</p><p>Jei naudojate pakaitos sertifikatą, pakaitos simbolis taikomas tik vienam lygiui. Padomenį, temos alternatyvų pavadinimą (SAN), reikia pritaikyti sertifikatui, jei jis yra daugiau nei vieno lygio, pvz., \*.contoso.com (ankstesniame pavyzdyje).</p> |
| „Service Fabric Client“ sertifikatas            | Šį sertifikatą naudoja klientai, norėdami peržiūrėti ir tvarkyti „Service Fabric“ klasterį. | |
| Užšifravimo sertifikatas                     | Šis sertifikatas naudojamas norint užšifruoti slaptą informaciją, pvz., „SQL Server“ slaptažodį ir vartotojų paskyrų slaptažodžius. | <p>Su sertifikato raktu būtina naudoti duomenų užšifravimą (10) ir negalima naudoti serverio autentifikavimo arba kliento autentifikavimo.</p><p>Daugiau informacijos žr. [Paslapčių tvarkymas „Service Fabric“ programose](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-secret-management).</p> |
| AOS SSL sertifikatas                          | <p>Šis sertifikatas naudojamas kaip „Server“ sertifikatas, kuris pateikiamas prie AOS svetainės prisijungusiam klientui. Jis taip pat naudojamas norint įjungti „Windows“ ryšio platformos (WCF) / paprastojo objektų prieigos protokolo (SOAP) sertifikatus.</p><p>Čia gali būti naudojamas „Service Fabric Server“ sertifikatas, jei jis yra pakaitos sertifikatas.</p> | <p>Sertifikato domeno vardas turi atitikti DNS zoną, kurioje nuomojami AOS ir „Service Fabric“.</p><p>Pavyzdžiui, sertifikato domeno pavadinimas gali būti \*.d365ffo.onprem.contoso.com, \*.onprem.contoso.com arba \*.contoso.com.</p><p>Jei naudojate pakaitos sertifikatą, pakaitos simbolis taikomas tik vienam lygiui. Padomenį, SAN, reikia pritaikyti sertifikatui, jei jis yra daugiau nei vieno lygio, pvz., \*.contoso.com (ankstesniame pavyzdyje).</p> |
| Seanso autentifikavimo sertifikatas           | Šį sertifikatą naudoja AOS, kad apsaugotų vartotojo seanso informaciją. | Tai taip pat yra **failų bendrinimo** sertifikatas, kuris bus paimamas iš LCS ir naudojamas diegimo metu. |
| Duomenų šifravimo ir duomenų pasirašymo sertifikatas | Šiuos sertifikatus naudoja AOS, kad užšifruotų slaptą informaciją. | |
| Finansinių ataskaitų kliento sertifikatas       | Šis sertifikatas naudojamas norint apsaugoti ryšį, perduodamą tarp finansinių ataskaitų tarnybų ir AOS. | |
| Ataskaitų sertifikatas                        | Šis sertifikatas naudojamas norint apsaugoti ryšį, perduodamą tarp SSRS ir AOS. | |
| Vietinis vietos agento sertifikatas           | <p>Šis sertifikatas naudojamas norint apsaugoti ryšį, perduodamą tarp vietinėje versijoje nuomojamo vietos agento ir LCS.</p><p>Šis sertifikatas vietos agentui suteikia galimybę veikti jūsų „Azure AD“ nuomotojo vardu ir palaikyti ryšį su LCS, kad būtų galima valdyti ir stebėti diegimą.</p> | |

### <a name="plan-your-users-and-service-accounts"></a>Suplanuoti vartotojus ir tarnybos paskyras

Turite sukurti kelias vartotojų arba tarnybos paskyras, kad „Finance and Operations“ (vietinė versija) veiktų. Turite sukurti grupės valdomų tarnybos paskyrų („gMSA“), domeno paskyrų ir SQL paskyrų derinį. Toliau pateikiamoje lentelėje nurodytos vartotojų paskyros, jų paskirtis ir pavadinimų pavyzdžiai, kurie bus naudojami šioje temoje.

| Vartotojo paskyra                                            | Tipas           | Paskirtis | Vartotojo vardas |
|---------------------------------------------------------|----------------|---------|-----------|
| Finansinių ataskaitų programos tarnybos paskyra         | gMSA           |         | Contoso\\svc-FRAS$ |
| Finansinių ataskaitų proceso tarnybos paskyra             | gMSA           |         | Contoso\\svc-FRPS$ |
| Finansinių ataskaitų vieno spustelėjimo dizaino įrankio tarnybos paskyra | gMSA           |         | Contoso\\svc-FRCO$ |
| AOS tarnybos paskyra                                     | gMSA           | Šis vartotojas turi būti sukurtas redagavimui ateityje atlikti. Planuojame, kad būsimuose leidimuose AOS veiks su „gMSA“. Sąrankos metu sukurdami šį vartotoją, padėsite užtikrinti sklandų perėjimą prie „gMSA“. | Contoso\\svc-AXSF$ |
| AOS tarnybos paskyra                                     | Domeno paskyra | AOS naudoja šį vartotoją GA leidime. | Contoso\\AXServiceUser |
| AOS SQL duomenų bazės administratoriaus vartotojas                                   | SQL vartotojas       | „Finance and Operations“ naudoja šį vartotoją, kad autentifikuotų naudodama SQL\*. Būsimuose leidimuose šis vartotojas taip pat bus pakeistas gMSA vartotoju. | AXDBAdmin |
| Vietinio diegimo agento tarnybos paskyra                  | gMSA           | Šią paskyrą naudoja vietos agentas, kad valdytų diegimą įvairiuose mazguose. | Contoso\\Svc-LocalAgent$ |

\* SQL autentifikavimo SQL vartotojo vardas ir slaptažodis yra apsaugoti, nes jie užšifruoti ir saugomi failų bendrinimo vietoje.

### <a name="create-dns-zones-and-add-a-records"></a>Sukurti DNS zonas ir įtraukti A įrašų

DNS yra integruotas į AD DS ir suteikia galimybę tvarkyti, valdyti bei rasti išteklių tinkle. Sukurkite AOS pagrindinio kompiuterio vardo ir „Service Fabric“ klasterio DNS peradresuojamą peržvalgos zoną bei A įrašus. Šiame sąrankos pavyzdyje DNS zonos pavadinimas yra d365ffo.onprem.contoso.com, o A įrašai / pagrindinių kompiuterių vardai yra tokie:

- **ax**.d365ffo.onprem.contoso.com for (AOS mašinos)
- **sf**.d365ffo.onprem.contoso.com („Service Fabric“ klasteris)

#### <a name="add-a-dns-zone"></a>Įtraukti DNS zoną

Norėdami įtraukti DNS zoną, naudokite nurodytą procedūrą.

1. Prisijunkite prie domeno valdiklio mašinos, spustelėkite **Pradėti** ir paleiskite DNS tvarkytuvą, įvesdami **dnsmgmt.msc**.
2. Dešiniuoju pelės mygtuku spustelėkite domeno valdiklio pavadinimą ir tada spustelėkite **Nauja zona** \> **Pirmyn**.
3. Pasirinkite **Pagrindinė zona**.
4. Palikti žymės langelį **Saugoti zoną „Active Directory“ (galima tik jei DNS serveris yra įrašomasis domeno valdiklis)** pažymėtą ir tada spustelėkite **Toliau**.
5. Pasirinkite **Į visus DNS serverius, veikiančius šio domeno valdikliuose: Contoso.com**, tada spustelėkite **Toliau**.
6. Pasirinkite **Peradresuojama peržvalgos zona**, tada spustelėkite **Toliau**.
7. Įveskite sąrankos zonos pavadinimą ir tada spustelėkite **Toliau**. Pavyzdžiui, įveskite **d365ffo.onprem.contoso.com**.
8. Pasirinkite **Neleisti dinaminių naujinimų**, tada spustelėkite **Toliau**.

#### <a name="set-up-an-a-record-for-aos"></a>Nustatyti AOS A įrašą

Naujoje DNS zonoje sukurkite vieną A įrašą pavadinimu **ax.d365ffo.onprem.contoso.com** ir priskirkite **kiekvienam** „Service Fabric“ klasterio mazgui, kurio tipas **AOSNodeType**. Nekurkite kitų tipų mazgų įrašų.

1. Dešiniuoju pelės klavišu spustelėkite naują zoną ir tada spustelėkite **Naujas pagrindinis kompiuteris**.
2. Įveskite „Service Fabric“ mazgo pavadinimą ir IP adresą (pvz., 10.179.108.12), o tada spustelėkite **Įtraukti pagrindinį kompiuterį**.

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>Nustatyti valdymo įrankio A įrašą

Naujoje DNS zonoje sukurkite A įrašą pavadinimu **sf.d365ffo.onprem.contoso.com** ir priskirkite **kiekvienam** „Service Fabric“ klasterio mazgui, kurio tipas **OrchestratorType**. Nekurkite kitų tipų mazgų įrašų.

1. Dešiniuoju pelės klavišu spustelėkite naują zoną ir tada spustelėkite **Naujas pagrindinis kompiuteris**.
2. Įveskite „Service Fabric“ mazgo pavadinimą ir IP adresą (pvz., 10.179.108.15), o tada spustelėkite **Įtraukti pagrindinį kompiuterį**.

#### <a name="join-vms-to-the-domain"></a>Prijungti virtualiąsias mašinas prie domeno

Prijunkite visas virtualiąsias mašinas prie domeno, atlikdami veiksmus, nurodytus temoje [Kaip prijungti „Windows Server 2016“ prie „Active Directory“ domeno](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html). Taip pat galite naudoti „Windows PowerShell“ scenarijų.

```
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
Restart-Computer
```
Kai VM prijungtos prie domeno, į vietinę administratorių grupę įtraukite AOS tarnybos paskyras (Contoso\svc-AXSF$ , Contoso\svc-AXSF$ ). Norėdami sužinoti, kaip tai padaryti, galite peržiūrėti straipsnį [Nario įtraukimas į vietinė grupę](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx).

#### <a name="disable-user-access-control"></a>Išjungti vartotojo prieigos valdymą 

Vykdykite šį scenarijų, kad išjungtumėte vartotojo prieigos valdymą **kiekviename** „Service Fabric“ mazge.
```
$RegPath = "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System"
New-ItemProperty -Path $RegPath -Name "EnableLUA" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "ConsentPromptBehaviorAdmin" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "EnableUIADesktopToggle" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "LocalAccountTokenFilterPolicy" -Value 1 -PropertyType "DWORD" -Force
```
> [!IMPORTANT]
> Sėkmingai įvykdžius scenarijų reikia iš naujo paleisti mazgą.

#### <a name="add-prerequisite-software-to-vms"></a>Į virtualiąsias mašinas įdiegti būtiną programinę įrangą

Tolesnėje lentelėje išvardinta būtina programinė įranga, kurią reikia įdiegti kiekvieno mazgo tipo mašinose.

> [!NOTE]
> Įdiegę komponentus turite iš naujo paleisti kompiuterį.

| Mazgo tipas | Komponentas | Komanda |
|-----------|-----------|---------|
| AOS       | SNAC – ODBC tvarkyklė | Žr. [„Microsoft“ ODBC tvarkyklė 13.1, skirta „SQL Server“ – „Windows“ + „Linux“](https://www.microsoft.com/en-us/download/details.aspx?id=53339). |
| AOS       | „Microsoft .NET Framework“ versija: 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| AOS       | „Microsoft .NET Framework“ versija: 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| AOS       | Interneto informacijos tarnybos (IIS) | `Add-WindowsFeature WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs`<br>`# Windows Process Activation Service`<br>`Add-WindowsFeature Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console` |
| AOS       | „Microsoft SQL Server Management Studio 2016“ | |
| AOS       | „Microsoft Visual C++“ perskirstomieji paketai, skirti „Microsoft Visual Studio 2013“ | Žr. [„Microsoft Visual C++“ perskirstomieji paketai, skirti „Visual Studio 2013“](https://support.microsoft.com/en-us/help/3179560). |
| AOS       | „Microsoft Access“ duomenų bazės modulis, 2010 m. (perskirstomasis) | Žr. [„Microsoft Access“ duomenų bazės modulis, 2010 m. (perskirstomasis)](https://www.microsoft.com/en-us/download/details.aspx?id=13255) |
| BI        | „.NET Framework“ versija: 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| BI        | „.NET Framework“ versija: 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| BI        | „Microsoft SQL Server 2016 SP1“ | |
| BI        | „Management Studio 2016“ | |
| BI        | „SQL Server Reporting Services 2016“ režimu **Vietinis** | |
| MR        | „.NET Framework“ versija: 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| MR        | „.NET Framework“ versija: 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| MR        | „Visual C++“ perskirstomieji paketai, skirti „Visual Studio 2013“ | Žr. [„Microsoft Visual C++“ perskirstomieji paketai, skirti „Visual Studio 2013“](https://support.microsoft.com/en-us/help/3179560). |

#### <a name="download-setup-scripts-from-lcs"></a>Atsisiųsti sąrankos scenarijus iš LCS

Pateikėme keletą scenarijų, kurie padės lengviau atlikti sąranką. Atlikite toliau nurodytus veiksmus, norėdami iš LCS atsisiųsti sąrankos scenarijus.

1. Prisijunkite prie LCS (<https://lcs.dynamics.com/v2>).
2. Ataskaitų srityje spustelėkite plytelę **Bendrai naudojamo turto biblioteka**.
3. Spustelėkite skirtuką **Modelis**.
4. Tinklelyje pasirinkite eilutę **„Dynamics 365 for Operations‟ – vietinio diegimo scenarijai**.
5. Spustelėkite **Versijos** ir atsisiųskite naujausią scenarijų versiją.

### <a name="describe-your-configuration"></a>Aprašyti savo konfigūraciją

Šiame skyriuje pateikiama informacija apie scenarijus, kuriuos turite vykdyti. Scenarijai aptariami ta tvarka, kuria turite juos vykdyti. Norėdami vykdyti scenarijus, užpildykite šablono failą, esantį $(downloadPath)\\ConfigTemplate.xml. Faile ConfigTemplate.xml aprašyti „Service Fabric“ klasteriai, sertifikatai, naudojami jiems sukonfigūruoti, ir sąskaitos, kurioms reikia suteikti prieigą prie atitinkamų sertifikatų. Pateiktame pavyzdyje reikšmės įvedamos į šioje temoje aprašomos infrastruktūros pavyzdį. Šablono failas bus naudojamas kitame skyriuje.

#### <a name="create-the-domain-account-for-a-service-user"></a>Kurti tarnybos vartotojo domeno paskyrą

Vykdykite toliau šią komandą, kad sukurtumėte domeno vartotojo paskyrą, contoso\\AXServiceUser.

```
New-ADUser -Name 'AXServiceUser' `
    -AccountPassword (Read-Host -Prompt 'Specify User Password' -AsSecureString) `
    -PasswordNeverExpires $true -ChangePasswordAtLogon $false `
    -Enabled $true -UserPrincipalName 'AXServiceUser@contoso.com'
```

#### <a name="create-gmsas"></a>Kurti gMSA

1. Pakeiskite katalogą į **$(DownloadPath)** ir vykdykite toliau nurodytą „Windows PowerShell“ komandą.

    > [!NOTE]
    > Vykdant šį scenarijų vartotojai nekuriami. Tačiau atspausdinamos komandos, kurias reikia neautomatiškai vykdyti domeno valdiklio mašinoje.

    ```
    # Generate gMSA account creation script (shows in console):
    .\Get-NewGMSAInDomainScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

2. Nukopijuokite komandos išvestį į „Windows PowerShell“ langą. Būtinai pašalinkite eilutės lūžius ir vykdykite eilutes „Active Directory“ domeno valdiklio mašinoje naudodami didesnes teises (spustelėkite dešinįjį pelės mygtuką ir tada spustelėkite **Paleisti administratoriaus teisėmis**).
3. Vykdykite toliau nurodytą scenarijų „Active Directory“ domeno valdiklio mašinoje ir patikrinkite, ar paskyros sėkmingai sukurtos. Scenarijų būtinai vykdykite po to, kai pakeitėte modelį, kuris atitinka tarnybos paskyrų pavadinimų suteikimo konvenciją.

    ```
    #Use this command to validate the gMSA accounts are added to AD.
    #Ensure to replace the Filter parameter with the pattern used to create your accounts.
    Get-ADServiceAccount -Filter { samAccountName -like "svc-*" }
    ```

4. Kliento mašinoje vykdykite scenarijų Export-AddGMSAsONVMScript.ps1. Šis scenarijus sugeneruoja scenarijus, kurie vykdomi kiekvienoje „Service Fabric“ VM ir įtraukia juos į aplankus, kurie atitinka kiekvieną VM pavadinimą.

    ```
    # Exports a script for installing gMSA on VM nodes into a directory VMs\<VMName>, again feed from XML
    .\Export-AddGMSAsOnVMScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

#### <a name="stop-iis"></a>Sustabdyti IIS

Naudoti nuotolinio darbalaukio protokolą (RDP), kad prisijungtumėte prie kiekvienos „Service Fabric“ VM, ir atlikite vadovo [Pradėti arba sustabdyti žiniatinklio serverį (IIS 7)](https://technet.microsoft.com/en-us/library/cc732317(v=ws.10).aspx) veiksmus. Taip pat galite naudoti toliau nurodytą „Windows PowerShell“ scenarijų, naudodami RDP, kad prisijungtumėte prie kiekvienos „Service Fabric“ VM.

```
$ServiceName = "WAS"
$wasService = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($wasService)
{
    $wasService.DependentServices | Stop-Service -Force -ErrorAction Continue
    $wasService | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}

$ServiceName = 'W3SVC'
$w3svc = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($w3svc)
{
    $w3svc.DependentServices | Stop-Service -Force -ErrorAction Continue
    $w3svc | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}
```
_IIS funkcija turėtų būti įdiegta, bet išjungta, nes produkte yra tam tikrų IIS dll priklausomybių._

### <a name="install-certificates"></a>Įdiegti sertifikatus

1. Jei anksčiau šioje temoje išvardytus sertifikatus gavote tinkamo CA, įveskite .pfx failo vardą ir failo ConfigTemplate.xml sertifikatų nykščio atspaudą. Nustatykite atributą **generateSelfSignedCert** į parinktį **False** ir atributą **eksportuojamas** – į parinktį **False**. Nukopijuokite .pfx failus į aplanką $(DownloadPath)\\InfrastructureScripts\\Certs.
2. Jei naudojate vartotojo pasirašomus sertifikatus (tik tikrinimo tikslais), paleiskite toliau nurodytą scenarijų. Norėdami kurti vartotojo pasirašomus sertifikatus, įsitikinkite, kad faile ConfigTemplate.xml atributas **generateSelfSignedCert** nustatytas į parinktį **True** ir atributas **eksportuojamas** – į parinktį **True**. Scenarijus atnaujins XML sertifikatų nykščio atspaudą.

    ```
    # Create self-signed certs (optionally, use -Display if you only want to see commands):
    # Note: this script is completely driven off ConfigTemplate.xml
    .\New-SelfSignedCertificates.ps1 -InputXml .\ConfigTemplate.xml
    ```

3. Eksportuokite naujus sertifikatus naudodami privatųjį raktą (.pfx failą). Naudoti toliau nurodytą scenarijų, norėdami generuoti ir vykdyti eksportavimo komandas „Windows PowerShell“. .pfx failai bus padėti į aplanką Certs.

    ```
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will reside in a folder named Certs\
    # Feeds from XML, if certs don't have passwords then you are prompted to enter one
    .\Export-PfxFiles.ps1 -InputXml .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Sertifikatai turėjo būti įdiegti ir turi būti šioje vietoje: cert:\\CurrentUser\\My. Taip pat sertifikatai turi būti galima eksportuoti.

    Jei naudojate vartotojo pasirašomus sertifikatus, pereikite prie kito skyriaus. Šios procedūros jums atlikti nereikia.

4. Kai .pfx failus eksportuosite arba nukopijuosite į aplanką $(DownloadPath)\\InfrastructureScripts\\Certs, vykdykite toliau nurodytas komandas, kad generuotumėte scenarijus, kurie bus padėti į VM atitinkančius aplankus.

    ```
    # Exports script for adding ACLs to certs into a directory VMs\<VMName>
    .\Export-CertificateAclsForVMs.ps1 -InputXml .\ConfigTemplate.xml
    
    # Exports Import-PfxFiles.ps1 script for importing PFXs on VM nodes into a directory VMS\<VMname>:
    .\Export-ImportPfxFilesScript.ps1 -InputXml .\ConfigTemplate.xml
    
    .\Export-UnblockStrongNameScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

5. Nukopijuokite scenarijus kiekviename aplanke į VM, kurios atitinka aplanko pavadinimą.
6. Kiekvienoje VM vykdykite scenarijus ta tvarka, kuria jie rodomi.

    ```
    #Run this script only if it exists
    .\Add-GMSAOnVM.ps1
    
    .\Import-PfxFiles.ps1
    
    .\Set-CertificateAcls.ps1
    
    #Run this script only if it exists
    .\Unblock-StrongName.ps1
    ```

### <a name="set-up-a-standalone-service-fabric-cluster"></a>Nustatyti atskirą „Service Fabric“ klasterį

1. Vykdykite toliau nurodytą komandą, kad sugeneruotumėte failą ClusterConfig.json.

    ```
    .\New-SFClusterConfig.ps1 -InputXml .\ConfigTemplate.xml
    ```

    Daugiau informacijos žr. [1B veiksmas: kelių mašinų klasterio kūrimas](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [Atskiro klasterio apsaugojimas „Windows“ naudojant X.509 sertifikatus](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-windows-cluster-x509-security) ir [Atskiro klasterio, veikiančio „Windows Server“, kūrimas](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).

2. Atsisiųskite [„Service Farbic“ atskiro diegimo paketą](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#download-the-service-fabric-standalone-package) į vieną iš savo „Service Farbic“ mazgų. Atsisiuntę ZIP failą atblokuokite jį spustelėdami ZIP failą dešiniuoju pelės klavišu ir tada spustelėdami **Ypatybės**. Dešiniajame apatiniame dialogo lango kampe pasirinkite žymės langelį **Atblokuoti**.
3. Nukopijuokite ZIP failą į vieną iš „Service Fabric“ klasterio mazgų ir jį išskleiskite.
4. Vykdykite toliau nurodytas komandas, kad sukurtumėte įeinančios užkardos taisyklę 443 ir 445 prievaduose visuose mazguose.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "SFInbound443445" -LocalPort 135, 137, 138, 139, 445, 443 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "SFInbound443445"
    ```

5. Vykdykite toliau nurodytas komandas, kad sukurtumėte įeinančios užkardos taisyklę 80 prievade, tik SSRS mazge.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "Reporting80" -LocalPort 80 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "Reporting80"
    ```

6. Nukopijuokite failą ClusterConfig.json į savo atskiros „Service Fabric“ neišskleistą diegimo failo vietą.
7. Atidarykite neišskleisto diegimo failo vietą „Windows PowerShell“ naudodami didesnes teises ir vykdykite toliau nurodytą komandą, kad patikrintumėte ClusterConfig.

    ```
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

8. Jei tikrinimas sėkmingas, vykdydami toliau nurodytą komandą įdiekite klasterį.

    ```
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

9. Sukūrę klasterį atidarykite „Service Fabric“ naršyklę bet kurioje kliento mašinoje, kad patikrintumėte diegimą.

    1. Įdiekite „Service Fabric“ kliento sertifikatą CurrentUser\\My, jei jis dar neįdiegtas.
    2. Pasirinkite **IE parametrai** \> **Suderinamumo režimas** ir išvalykite žymės langelį **Rodyti intraneto svetaines suderinamumo režimu**.
    3. Atidarykite `https://sf.d365ffo.onprem.contoso.com:19080`, kur sf.d365ffo.onprem.contoso.com yra zonoje nurodyto „Service Fabric“ klasterio pagrindinio kompiuterio vardas. Jei DNS vardo vertimas nesukonfigūruotas, naudokite mašinos IP adresą.
    4. Pasirinkite kliento sertifikatą. Rodomas puslapis **„Service Fabric“ naršyklė**.

### <a name="configure-lcs-connectivity-for-the-tenant"></a>Sukonfigūruoti nuomininko LCS ryšį

„Finance and Operations“ diegimas ir priežiūra vykdomi per LCS naudojant vietinį vietos agentą. Norėdami nustatyti ryšį tarp LCS ir „Finance and Operations“ nuomininko, turite sukonfigūruoti sertifikatą, kuris vietos agentui suteikia galimybę veikti jūsų „Azure AD“ nuomotojo vardu (pvz., Contoso.Onmicrosoft.com).

Naudoti vietinio agento sertifikatą, kurį gavote iš CA, arba vartotojo pasirašomą sertifikatą, kurį sukūrėte naudodami scenarijus.

Tik vartotojai, kurių paskyroms priskirtas katalogo vaidmuo Visuotinis administratorius, gali įtraukti sertifikatus ir įgalioti LCS. Pagal numatytuosius parametrus asmuo, kuris jūsų organizacijos vardu prisiregistruoja prie „Microsoft Office 365“, bus katalogo visuotinis administratorius.

> [!NOTE]
> Turite sukonfigūruoti kiekvieno nuomotojo sertifikatą po vieną kartą. Visose vietinėse aplinkose galima naudoti tą patį sertifikatą, norint prisijungti prie LCS.

1. Atsisiųskite ir įdiekite naujausią „Azure PowerShell“ versiją kliento mašinoje. Daugiau informacijos žr. [„Azure PowerShell“ diegimas ir konfigūravimas](https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0).
2. Prisijunkite prie [kliento „Azure“ portalo](https://portal.azure.com) ir įsitikinkite, kad turite katalogo vaidmenį Visuotinis administratorius.
3. Vykdykite toliau nurodytą scenarijų iš $(DownloadPath)\\InfrastructureScripts.

   ```
   .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
   ```

### <a name="set-up-file-storage"></a>Nustatyti failų saugyklą

Turite nustatyti dvi plačiai pasiekiamas SMB 3.0 failų bendrinimo vietas. Informacijos apie tai, kaip įjungti SMB 3.0, žr. [SMB saugos patobulinimai](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1).
Saugaus dialekto derybos negali aptikti arba neleisti SMB versiją pasendinti iš 2.0 arba 3.0 į 1.0. Dėl šios priežasties ir siekiant išnaudoti visas SMB šifravimo galimybes, rekomenduojame išjungti SMB 1.0 serverį

> [!NOTE]
> Siekdami užtikrinti, kad jūsų aplinkoje esantys jūsų duomenys yra apsaugoti, kiekvienoje mašinoje turite įdiegti disko šifravimo programą „BitLocker“. Informacijos apie tai, kaip įjungti „BitLocker“, žr. [„BitLocker“: kaip diegti „Windows Server 2012“ ir naujesnėse versijose](https://docs.microsoft.com/en-us/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server).

- Failų bendrinimo vieta, kurioje saugomi vartotojo dokumentai, įkelti į AOS (pvz., \\\\DAX7SQLAOFILE1\\aos-storage).
- Failų bendrinimo vieta, kurioje saugoma naujausi kūrimo ir konfigūravimo failai, skirti diegimui valdyti (pvz., \\\\DAX7SQLAOFILE1\\agent))

    > [!NOTE]
    > Šis failų bendrinimo vietos kelias turi būti kuo trumpesnis, kad nebūtų viršytas maksimalus failų, kurie bus padėti į bendrinimo vietą, kelio ilgis.

1. Failų bendrinimo mašinoje vykdykite toliau nurodytą komandą.

    ```
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```
#### <a name="set-up-the-dax7sqlaofile1aos-storage-file-share"></a>Nustatyti failų bendrinimo vietą \\\\DAX7SQLAOFILE1\\aos-storage

2. Serverio tvarkytuve pasirinkite **Failų saugyklų tarnybos** \> **Bendrinimo vietos**.
3. Spustelėkite **Užduotys** \> **Nauja bendrinimo vieta**, kad sukurtumėte naują bendrinimo vietą pavadinimu **aos-storage**.
4. Suteikite **keitimo** teises kiekvienai „Service Fabric“ klasterio mašinai, išskyrus **OrchestratorNodeType**.
5. Suteikite **keitimo** teises vartotojo AOS domeno vartotojui (contoso\\AXServiceUser) ir gMSA vartotojui (contoso\\svc AXSF).

#### <a name="set-up-the-dax7sqlaofile1agent-file-share"></a>Nustatyti failų bendrinimo vietą \\\\DAX7SQLAOFILE1\\agent

6. Vėl atidarykite serverio tvarkytuvę, pasirinkite **Failų saugyklų tarnybos** \> **Bendrinimo vietos**.
7. Spustelėkite **Užduotys** \> **Nauja bendrinimo vieta**, kad sukurtumėte naują bendrinimo vietą pavadinimu **agent**.
8. Suteikite **viso turinio valdymo** teises vietinio diegimo agento gMSA vartotojui (contoso\\svc LocalAgent$).

### <a name="set-up-sql-server"></a>Nustatyti „SQL Server“

1. Įdiekite „SQL Server 2016 SP1“, kad jis būtų plačiai pasiekiamas, kaip SQL klasterius, kurie apima saugojimo srities tinklą (SAN), arba „Always-On“ konfigūracijoje.  Patikrinkite, ar **Duomenų bazės modulis, Ataskaitų tarnybos, Viso teksto ieška** ir **Valdymo įrankiai** jau įdiegti.
> [!NOTE]
> Įsitikinkite, kad „SQL Always On“ nustatytas atsižvelgiant į temą [Pradinio duomenų sinchronizavimo puslapio pasirinkimas („Always On“ pasiekiamumo grupių vedliai)](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) ir atitinka [Neautomatinis antrinių duomenų bazių ruošimas](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs)
2. Vykdykite SQL tarnybą kaip domeno vartotojas.
3. Gaukite SSL sertifikatą iš CA, kad sukonfigūruotumėte „Finance and Operations“. Tikrinimo tikslais galite kurti ir naudoti vartotojo pasirašomą sertifikatą.

**Vartotojo pasirašomas sertifikatas, skirtas „Clustered SQL“ egzemplioriui**
   ```
   New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
   ```
**Vartotojo pasirašomas sertifikatas, skirtas „Always-On SQL“ egzemplioriui**
```
#https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

# Create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
# Run script on each node
$computerName = $env:COMPUTERNAME.ToLower() 
$domain = $env:USERDNSDOMAIN.ToLower()
$listenerName = 'dax7sqlaosqla' 
$cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'

```
4. Naudodami sertifikatą atlikite temos [Kaip įjungti SSL šifravimą „SQL Server“ egzemplioriuje naudojant „Microsoft“ valdymo konsolę](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) veiksmus, kad „SQL Server“ sukonfigūruotumėte SSL.
5. Atlikite toliau nurodytus veiksmus su kiekvienu klasterio mazgu. Įsitikinkite, kad keitimus atliekate neaktyviame mazge, o atlikę keitimus jį perimkite.

    1. Importuokite sertifikatą į LocalMachine\\My.
    2. Suteikite sertifikato teises tarnybos paskyrai, kuri naudojama SQL tarnybai paleisti. „Microsoft“ valdymo konsolėje (MMC) dešiniuoju pelės mygtuku spustelėkite sertifikatą (certlm.msc) ir tada spustelėkite **Užduotys** \> **Valdyti asmeninius raktus**.
    3. Įtraukite sertifikato nykščio atspaudą į HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate.
    4. „Microsoft SQL Server“ konfigūracijos tvarkyklėje nustatykite **ForceEncryption** į parinktį **Taip**.

6. Eksportuoti sertifikato viešąjį raktą (.cer failą) ir jį įdiekite kiekvieno „Service Fabric“ mazgo patikimame pagrinde.

### <a name="configure-the-orchestratordata-database"></a>Konfigūruoti duomenų bazę OrchestratorData

1.  Sukurkite tuščią duomenų bazę ir pavadinkite ją **OrchestratorData**. Šią duomenų bazę vietinės versijos vietos agentas naudoja diegimui valdyti.
2.  Suteikite vietos agentui gMSA (svc LocalAgent$) **db\_owner** teises duomenų bazėje.

    1. Medyje išplėskite serverio pavadinimą, išplėskite dalį **Sauga** \> **Prisijungimo informacija** ir tada spustelėkite dešiniuoju pelės mygtuku bei spustelėkite **Nauja prisijungimo informacija**.

        ![Komanda Nauja prisijungimo informacija](./media/OPSetup_01_NewLogin.png)


    2. Ieškokite tarnybos paskyros **svc LocalAgent$**. Spustelėkite **Vietos** ir pasirinkite **Visas katalogas**, tada spustelėkite **Objektų tipai** ir pasirinkite **Tarnybos paskyra**.

        ![Pasirinkite dialogo langą Vartotojas, Tarnybos paskyra arba Grupė](./media/OPSetup_02_SelectUserServiceAccountOrGroupDialogBox.png)

    3. Nustatykite **Priskirti serverio vaidmenį** į parinktį **Viešasis**.
    4. Priskirkite duomenų bazės vaidmens teisę **db\_owner** duomenų bazei OrchestratorData.

### <a name="configure-the-finance-and-operations-database"></a>Konfigūruoti „Finance and Operations” duomenų bazę

1. Prisijunkite prie LCS (<https://lcs.dynamics.com/v2>).
2. Ataskaitų srityje spustelėkite plytelę **Bendrai naudojamo turto biblioteka**.
3. Spustelėkite skirtuką **Modelis** 
4. Tinklelyje spustelėkite eilutę **„Dynamics 365 for Operations“, vietinė versija, „Enterprise“ leidimas – demonstraciniai duomenys**, kad atsisiųstumėte ZIP failą.
5. ZIP faile pateikiami tušti ir demonstraciniai .bak failai. Pagal savo poreikius pasirinkite tinkamą .bak failą. Pavyzdžiui, jei reikia demonstracinių duomenų, atkurkite failą AxBootstrapDB_Demodata.bak. 
6. Atkurkite duomenų bazę AxBootstrapDB_DemoData.bak.
7. Pervardykite duomenų bazę **AXDBRAIN**.
8. Vykdykite toliau nurodytas užklausas atkurtoje duomenų bazėje.

    ```
    ALTER DATABASE AXDBRAIN
    SET READ_COMMITTED_SNAPSHOT ON
    GO
    
    ALTER DATABASE AXDBRAIN
    SET ALLOW_SNAPSHOT_ISOLATION ON
    GO
    ```

4. Atnaujinkite duomenų bazės failus.

    1. Dešiniuoju pelės mygtuku spustelėkite duomenų bazę, tada spustelėkite **Ypatybės**.
    2. Spustelėkite **Failai**, kad pakeistumėte duomenų bazės failo ypatybes.
    3. Lauke **Pradinis dydis (MB)** įveskite reikšmę, kuri yra didesnė nei 5 120.

        ![Duomenų bazės dialogo langas Ypatybės](./media/OPSetup_03_DatabasePropertiesDialogBox.png)

    4. **AXDBBuild\_Data**: nustatykite lauką **Automatinis didinimas/ didėjimas** į **200** megabaitų (MB).
    5. **AXDBBuild\_Log**: nustatykite lauką **Automatinis didinimas/ didėjimas** į **500** MB.

        ![Keisti dialogo langą Automatinis didinimas](./media/OPSetup_04_ChangeAutogrowthDialogBox.png)

5. Sukurkite naują vartotoją, kurio SQL autentifikavimas įjungtas (axdbadmin).
6. Norėdami susieti vartotojus ir duomenų bazės vaidmenis, naudokite toliau pateiktos lentelės informaciją.

    | Vartotojas             | Tipas    | Duomenų bazės vaidmuo |
    |------------------|---------|---------------|
    | svc-AXSF$        | gMSA    | db\_owner     |
    | svc-LocalAgent$  | gMSA    | db\_owner     |
    | svc-FRPS$        | gMSA    | db\_owner     |
    | svc-FRAS$        | gMSA    | db\_owner     |
    | axdbadmin        | SqlUser | db\_owner     |

7. Suteikti vartotojui svc AXSF$ ir SQL vartotojui axdbadmin prieigą prie toliau nurodytų duomenų bazės tempdb vaidmenų.

    - db\_datareader
    - db\_datawriter
    - db\_ddladmin

8. „Management Studio“ vykdykite toliau nurodytas „Transact SQL“ komandas (T-SQL).

    ```
    GRANT VIEW SERVER STATE TO axdbadmin
    GRANT VIEW SERVER STATE TO [contososqlao\svc-AXSF$]
    ```
9. Paleiskite šią komandą:
```
.\Reset-DatabaseUsers.ps1 -DatabaseServer ‘<FQDN of the SQL server>’ -DatabaseName '<AX database name>'
```

### <a name="configure-the-financial-reporting-database"></a>Konfigūruoti finansinių ataskaitų duomenų bazę

1.  Sukurkite tuščią duomenų bazę ir pavadinkite ją **FinancialReporting**.
2.  Norėdami susieti vartotojus ir duomenų bazės vaidmenis, naudokite toliau pateiktos lentelės informaciją.

    | Vartotojas             | Tipas | Duomenų bazės vaidmuo |
    |------------------|------|---------------|
    | svc-LocalAgent$  | gMSA | db\_owner     |
    | svc-FRPS$        | gMSA | db\_owner     |
    | svc-FRAS$        | gMSA | db\_owner     |

### <a name="encrypt-credentials"></a>Užšifruoti kredencialus

1. Bet kurioje kliento mašinoje įdiekite užšifravimo sertifikatą sertifikatų saugykloje LocalMachine\\My.
2. Suteikite dabartiniam vartotojui prieigą prie šio sertifikato privačiojo rakto.
3. Sukurkite failą Credentials.json, kaip parodyta čia.

    ```
    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        }
    }
    ```

    - **AccountPassword** yra užšifruotas domeno vartotojo slaptažodis, skirtas AOS domeno vartotojui (contoso\\axserviceuser).
    - **SqlUser** yra užšifruotas SQL vartotojas (axdbadmin), kuriam suteikta prieiga prie „Finance and Operations“ duomenų bazės (AXDBRAIN), o **SqlPassword** yra užšifruotas SQL slaptažodis.

4. Nukopijuokite .json failą į SMB failų bendrinimo vietą, \\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json.
5. Atnaujinkite failo Credentials.json užšifruotas reikšmes.

    ```
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | clip
    ```

    1. Faile Credentials.json pakeiskite **\<encryptedDomainUserPassword\>** nurodydami užšifruotą domeno slaptažodį.
    2. Pakeiskite **\<encryptedSqlUser\>** nurodydami užšifruotą „Finance and Operations“ SQL vartotoją.
    3. Pakeiskite **\<encryptedSqlPassword\>** nurodydami „Finance and Operations“ SQL slaptažodį.
    
### <a name="set-up-ssrs"></a>Nustatyti SSRS

1.  Prieš pradėdami įsitikinkite, kad įdiegti būtinieji komponentai, išvardyti šios temos pradžioje.
2.  Atlikite temos [„SQL Server Reporting Services“ konfigūravimas vietiniam diegimui atlikti](../analytics/configure-ssrs-on-premises.md) veiksmus.

### <a name="configure-ad-fs"></a>Sukonfigūruoti AD FS

Prieš atlikdami šią procedūrą, „Windows Server 2016“ turite įdiegti AD FS. Informacijos apie tai, kaip diegti AD FS, žr. [„Windows Server 2016“ diegimo vadovas ir „2012 R2 AD FS“ diegimo vadovas](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).

Be numatytosios parengtos naudoti AD FS konfigūracijos, „Finance and Operations“ reikalinga papildoma konfigūracija. Atlikdami tolesnius veiksmus „Windows PowerShell“ veikia mašinoje, kurioje įdiegta AD FS vaidmenų tarnyba. Vartotojo paskyrai reikia priskirti pakankamai teisių, kad ji galėtų administruoti AD FS. Pavyzdžiui, vartotojas privalo turėti domeno administratoriaus paskyrą.

1. Sukonfigūruokite AD FS identifikatorių, kad jis atitiktų AD FS atpažinimo ženklo išdavėją.

    ```
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. Naudodami intraneto autentifikavimo ryšį turėtumėte išjungti „Windows“ integruotąjį autentifikavimą (WIA), nebent AD FS sukonfigūravote veikti įvairiose aplinkose. Daugiau informacijos apie tai, kaip konfigūruoti WIA, kad jį būtų galima naudoti su ADFS, žr. [Konfigūruoti naršykles, kad „Windows“ integruotąjį autentifikavimą (WIA) būtų galima naudoti su AD FS](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).

   ```
   Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
   ```

3. Prisijungiant vartotojo el. pašto adresas turi būti priimtina autentifikavimo įvestis.

   ```
   Add-Type -AssemblyName System.Net
   $fdqn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
   $domainName = $fdqn.Substring($fdqn.IndexOf('.')+1)
   Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
   ```

Tam, kad AD FS pasitikėtų „Finance and Operations“ ir būtų įvykdytas abipusis autentifikavimas, įvairius programų įrašus reikia užregistruoti AD FS, AD FS programų grupėje. Norėdami pagreitinti sąrankos procesą ir sumažinti klaidų skaičių, registruodami galite naudoti toliau nurodytą scenarijų. Nukopijuokite scenarijų Publish-ADFSApplicationGroup.ps1 ir katalogą D365FO-OP į mašiną, kurioje įdiegta AD FS vaidmenų tarnyba. Paleiskite vykdykite scenarijų naudodami vartotojo paskyrą, pvz., administratoriaus paskyrą, kuriai priskirta pakankamai teisių AD FS administruoti. Daugiau informacijos apie tai, kaip naudoti scenarijus, žr. scenarijuje nurodytus dokumentus. Pasižymėkite kliento ID, nurodytus išvestyje, nes atliekant kitą veiksmą jums reikės pateikti šią informaciją LCS.

```
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'ax.d365ffo.onprem.contoso.com'
```

ADFS valdymo konsolė turėtų atitikti toliau pateiktą paveikslėlį. Norėdami atidaryti serverio tvarkytuvą, spustelėkite **Įrankiai** \> **AD FS valdymas** ir tada apatinėje kairiojoje medžio rodinio pusėje spustelėkite **Programų grupės**. Dukart spustelėkite programų grupę, norėdami peržiūrėti daugiau informacijos.

![Programų grupės ypatybės](./media/OPSetup_05_ApplicatioGroupProperties.png)

Galiausiai atlikdami tinkamumo tikrinimą įsitikinkite, kad tipo **AOSNodeType** „Service Fabric“ mazge galite pasiekti AD FS OpenID konfigūracijos URL, žiniatinklio naršyklėje atidarydami `https://<adfs-dns-name>/adfs/.well-known/openid-configuration`. Jei gaunate pranešimą, nurodantį, kad svetainė nėra saugi, į patikimų šakninių sertifikavimo tarnybų saugyklą neįtraukėte savo AD FS SSL sertifikato. Šis veiksmas aprašytas AD FS diegimo vadove. Jei sėkmingai atidarėte URL, grąžinamas „JavaScript Object Notation“ (JSON) failas, kuriame yra jūsų AD FS konfigūracija, ir matysite, kad jūsų AD FS URL yra patikimas.

Atlikus tai infrastruktūros sąranka baigta. Tolesniuose skyriuose aprašoma, kaip atidaryti [LCS](https://lcs.dynamics.com) norint nustatyti jungtį ir įdiegti „Dynamics 365 for Finance and Operations“ aplinką.

## <a name="configure-connector-and-install-on-premises-local-agent"></a>Konfigūruoti jungtį ir diegti vietinės versijos vietos agentą

1. Prisijunkite prie [LCS](https://lcs.dynamics.com/) ir atidarykite vietinės versijos diegimo projektą.
2. Meniu su mėsainio piktograma spustelėkite **Projekto parametrai**.

    ![Komanda Projekto parametrai](./media/OPSetup_06_ProjectSettings.png)

3. Spustelėkite **Vietinės jungtys**.
4. Spustelėkite **Įtraukti**, kad sukurtumėte naują jungtį.
5. Naudodami skirtuką **Sąrankos pagrindinio kompiuterio infrastruktūra** atsisiųskite agento diegimo programą.

    ![Mygtukas Atsisiųsti agento diegimo programą, esantis skirtuke Sąrankos pagrindinio kompiuterio infrastruktūra](./media/OPSetup_07_DownloadAgentInstaller.png)

6. Patikrinkite, ar ZIP failas atblokuotas. Dešiniuoju pelės mygtuku spustelėkite failą, spustelėkite **Ypatybės**, tada pasirinkite **Atblokuoti**.
7. Išskleiskite agento diegimo programą viename iš tipo **OrchestratorType** „Service Fabric“ mazgų.
8. Skirtuke **Konfigūruoti agentą** įveskite konfigūravimo parametrus.
9. Įrašykite konfigūraciją, o tada spustelėkite **Atsisiųsti konfigūracijas**, kad atsisiųstumėte konfigūracijos failą localagent config.json.

    ![Mygtukas Atsisiųsti konfigūracijas, esantis skirtuke Konfigūruoti agentą](./media/OPSetup_08_DownloadConfigurations.png)

10. Nukopijuokite failą localagent config.json į mašiną, kurioje yra agento diegimo programos paketas.
11. Komandinės eilutės lange vykdykite toliau nurodytą komandą ir atidarykite aplanką, kuriame yra agento diegimo programa.

    ```
    LocalAgentCLI.exe Install <path to config.json>
    ```

    > [!NOTE]
    > Šią komandą vykdančiam vartotojui turi būti priskirta **db\_owner** teisė duomenų bazėje OrchestratorData.
    
12. Kai vietos agentas sėkmingai įdiegtas, LCS vėl atidarykite savo vietinę jungtį.
13. Skirtuke **Tikrinti sąranką** spustelėkite mygtuką **Siųsti agentui pranešimą**. Tokiu būdu bus patikrintas LCS ir jūsų vietos agento ryšys. Kai ryšys sėkmingai nustatytas, puslapis atrodys kaip toliau pateikta diagrama.

     ![Tikrinti agentą](./media/ValidateAgent.PNG)

## <a name="deploy-your-dynamics-365-for-finance-and-operations-on-premises-environment"></a>Diegti „Dynamics 365 for Finance and Operations“ (vietinės versijos) aplinką

1. LCS atidarykite vietinį projektą, pasirinkite **Aplinka**, **Smėlio dėžė** ir spustelėkite **Konfigūruoti**
2. Pasirinkite savo **aplinkos topologiją** ir atlikite vedlio veiksmus, kad inicijuotumėte diegimą.
3. Vietos agentas vykdys diegimo užklausą, pradės diegimą ir, viską paruošus, vėl užmegs ryšį su LCS.

