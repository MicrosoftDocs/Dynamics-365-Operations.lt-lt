---
title: "Įdiegtims debesyje taikomi sistemos reikalavimai"
description: "Šioje temoje išvardyti šiai „Microsoft Dynamics 365 Finance and Operations“ „Enterprise‟ leidimo versijai (įdiegtims debesyje) taikomi sistemos reikalavimai."
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: 7fe11966b27eb0793a47835e05e465d809bf3407
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="system-requirements-for-cloud-deployments"></a>Įdiegtims debesyje taikomi sistemos reikalavimai

[!include[banner](../includes/banner.md)]

Šioje temoje išvardyti šiai „Microsoft Dynamics 365 Finance and Operations“ „Enterprise‟ leidimo versijai (įdiegtims debesyje) taikomi sistemos reikalavimai. Prieš diegdami „Finance and Operations“, kai galėsite, patikrinkite, ar sistema, kurią naudojate, atitinka arba viršija minimalius tinklo, aparatūros ir programinės įrangos reikalavimus.

## <a name="supported-web-browsers"></a>Palaikomos žiniatinklio naršyklės
Žiniatinklio programa gali veikti bet kurioje iš tolesnių žiniatinklio naršyklių, veikiančių nurodytose operacinėse sistemose.

-   „Microsoft Edge‟ (naujausia viešai pasiekiama versija) sistemoje „Windows 10‟.
-   „Internet Explorer 11‟ sistemose „Windows 10‟, „Windows 8.1‟ arba „Windows 7‟.
-   „Google Chrome‟ (naujausia viešai pasiekiama versija) sistemose „Windows 10‟, „Windows 8.1‟, „Windows 8‟, „Windows 7‟ arba planšetėje „Google Nexus 10‟.
-   „Apple Safari‟ (naujausia viešai pasiekiama versija) sistemoje „Mac OS X 10.10‟ („Yosemite‟), 10.11 („El Capitan‟) arba 10.12 („Sierra‟) arba planšetėje „Apple iPad‟.

Norėdami rasti naujausią kiekvienos žiniatinklio naršyklės leidimą, eikite į programinės įrangos gamintojo svetainę. 

> [!NOTE]
> -   Kad užduočių įrašymo priemonė galėtų fiksuoti ekrano nuotraukas ir įtraukti į sugeneruotus „Microsoft Word‟ dokumentus, būtina įdiegti negalutinį „Chrome‟ plėtinį. <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> -   Darbo eigos rengyklė paleidžiama kaip „ClickOnce“ taikomoji programa. Tik „Microsoft Edge“ ir „Internet Explorer“ (palaikomoje „Microsoft Windows“ versijoje) palaiko „ClickOnce“ taikomąsias programas. Darbo eigos rengyklės „ClickOnce“ taikomajai programai reikia 64 bitų suderinamos operacinės sistemos.
> -   Finansinėms ataskaitoms skirtas ataskaitų konstruktorius paleidžiama kaip „ClickOnce“ taikomoji programa. Jam reikia 64 bitų suderinamos operacinės sistemos. Jei naudojate „Chrome“, turite įdiegti plėtinį „ClickOnce“, kad galėtumėte atsisiųsti ataskaitų dizaino įrankio klientą. Jei naudojate „Chrome“ inkognito režimu, įsitikinkite, kad plėtinys „ClickOnce“ nustatytas veikti ir inkognito režimu.
> -   Norint peržiūrėti PDF failus, rekomenduojame naudoti naršykles, pvz., „Microsoft Edge“ (naujausią viešai prieinamą versiją) sistemoje „Windows 10“ arba „Google Chrome“ (naujausią viešai prieinamą versiją) sistemoje „Windows 10“, „Windows 8.1“, „Windows 8“ ar „Windows 7“ arba „Google" Nexus 10“ planšetiniame kompiuteryje.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Palaikomos „Retail Cloud POS‟ žiniatinklio naršyklės

„Retail Cloud POS‟ gali veikti bet kurioje iš tolesnių žiniatinklio naršyklių, veikiančių nurodytose operacinėse sistemose.

-   „Microsoft Edge‟ (naujausia viešai pasiekiama versija) sistemoje „Windows 10‟.
-   „Internet Explorer 11‟ sistemose „Windows 10‟, „Windows 8.1‟ arba „Windows 7‟.
-   „Chrome‟ (naujausia viešai pasiekiama versija) sistemoje „Windows 10‟, „Windows 8.1“ arba „Windows 7“.

## <a name="network-requirements"></a>Tinklo reikalavimai
-   „Finance and Operations“ skirta tinklams, kurių laukimo laikas ne didesnis nei 250–300 milisekundžių (ms). Tai – laukimo laikas iš naršyklės kliento iki „Microsoft Azure“ duomenų centro, kuriame yra „Finance and Operations“. Rekomenduojame tinklo laukimo laiką patikrinti <http://www.azurespeed.com>.
-   „Finance and Operations“ pralaidumo reikalavimai priklauso nuo jūsų scenarijaus. Labiausiai įprastiems scenarijams reikia didesnio nei 50 kilobitų per sekundę (KB/s) pralaidumo. Tačiau tiems scenarijams, kurių mokamosios krovos reikalavimai aukšti, pvz., darbo sritims arba scenarijams, kurie apima nemažai tinkinimo, rekomenduojamas didesnis pralaidumas.

Apskritai „Finance and Operations“ yra optimizuotas internetui. Kreipimosi ciklų iš naršyklės kliento į „Azure“ duomenų centrą skaičius yra labai mažas, o visa mokamoji krova yra suglaudinta. 

> [!WARNING]
> Neskaičiuokite pralaidumo iš kliento vietos reikalavimų, vartotojų skaičių padauginę iš minimalių pralaidumo reikalavimų. Tam tikros vietos naudojimą vienu metu labai sunku apskaičiuoti. Klientams, kurie susirūpinę dėl pralaidumo reikalavimų, rekomenduojama naudoti „Finance and Operations“ peržiūros versiją.

## <a name="net-framework-requirements"></a>„.NET Framework“ reikalavimai
„Finance and Operations“ reikia „Microsoft.NET Framework“ 4.6.2 versijos visoms vieno paspaudimo taikomosioms programoms, pvz., dokumento maršruto planavimo agentui. Diegimo instrukcijų žr. [„.NET Framework“ diegimas](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Palaikomos „Microsoft Office“ taikomosios programos
„Finance and Operations“ įdiegtys debesyje ir vietinės įdiegtys palaiko toliau nurodytas „Microsoft Office“ programas.

-   Kad galėtumėte naudoti „Microsoft Excel“ papildinius, turi būti įdiegta „Windows“ arba „Mac“ skirta „Microsoft Office 2016“. Išsamios informacijos apie versijų reikalavimus žr. [„Office“ integravimo trikčių šalinimas](../../dev-itpro/office-integration/office-integration-troubleshooting.md).
-   Norėdami peržiūrėti dokumentus, sugeneruotus naudojant funkciją Eksportuoti į „Excel“ arba Eksportuoti į „Word“, turi būti įdiegta „Microsoft Office 2007“ arba naujesnė versija.

## <a name="retail-modern-pos-requirements"></a>„Retail Modern POS“ reikalavimai

> [!NOTE]
> Jei „Retail Modern POS“ naudos autonominę duomenų bazę, kompiuteris turi atitikti visus sistemos reikalavimus, skirtus „Microsoft SQL Server“. „Retail Modern POS“ autonominė duomenų bazė veiks „Microsoft SQL Server 2012“ su 3 pakeitimų paketu ar vėlesnėje versijoje, „Microsoft SQL Server 2014“ su 2 pakeitimų paketu ar vėlesnėje versijoje ir „Microsoft SQL Server 2016“. Rekomenduojame visada naudoti naujausią versiją ir įdiegti naujausius pakeitimų paketus.

### <a name="supported-operating-systems"></a>Palaikomos operacinės sistemos

-   „Retail Modern POS“ yra 32 bitų taikomoji programa, bet ji vykdoma ir x86, ir x64 architektūrose.
-   „Retail Modern POS“ palaikoma tik „Windows 10 Pro“, „Enterprise“ ir „Enterprise Long Term Servicing Branch“ (LTSB) leidimai.

### <a name="minimum-system-requirements"></a>Minimalūs sistemos reikalavimai

-   Mažiausia palaikoma skiriamoji geba yra 1280 × 1024.
-   Kompiuteris, kuriame vykdoma „Retail Modern POS“, turi atitikti šiuos reikalavimus:

    -   Jame turi būti mažiausiai dviejų branduolių procesorius, veikiantis ne mažiau kaip 2 gigahercų (GHz) dažniu.
    -   Turi turėti mažiausiai 3 gigabaitus (GB) RAM.
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

-   „Microsoft Dynamics AX‟ jungtis turi dvi atskiras diegimo programas – vieną „Async Server Connector service‟ ir vieną „Real-time service for Dynamics AX 2012 R3‟.
-   Abu komponentai yra 32 bitų programos, tačiau veikia ir x86, ir x64 architektūrose.
-   Abu komponentai palaikomi tolesnėse operacinėse sistemose.

    -   „Windows 7 Professional“, „Enterprise“ ir „Ultimate“ leidimuose
    -   „Windows 8.1“ 1 naujinimas „Professional“, „Enterprise“ ir įdėtieji leidimai
    -   „Windows 10 Pro“, „Enterprise“ ir „Enterprise LTSB“ leidimai
    -   „Microsoft Windows Server 2012 R2“ ir „Microsoft Windows Server 2016“

### <a name="minimum-system-requirements"></a>Minimalūs sistemos reikalavimai
-   2 GB RAM, (rekomenduojama 4 GB RAM).
-   1,6 GHz didžiausia CPU sparta branduolyje (Mažiausiai dviejų branduolių.)
-   Bent 10 GB laisvos vietos (Kanalo duomenų bazei reikia daug vietos.)

## <a name="requirements-for-development-on-local-vms"></a>Reikalavimai norint kurti vietiniuose virtualiuosiuose įrenginiuose
Išsamesnės informacijos apie reikalavimus norint kurti vietiniuose virtualiuosiuose įrenginiuose (VM) žr. [VM vykdymas vietoje](../../dev-itpro/dev-tools/access-instances.md).


## <a name="see-also"></a>Taip pat žiūrėkite

[„Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidimo įvertinimo kopijos gavimas](../../dev-itpro/dev-tools/get-evaluation-copy.md)

