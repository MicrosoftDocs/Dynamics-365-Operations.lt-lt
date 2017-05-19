---
title: Sistemos reikalavimai
description: "Šioje temoje išvardyti šiai „Microsoft Dynamics 365 for Operations“ versijai taikomi sistemos reikalavimai."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 86053196a3aad6b7b5d7830860e1af347dd969d8
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="system-requirements"></a>Sistemos reikalavimai

[!include[banner](../includes/banner.md)]


Šioje temoje išvardyti šiai „Microsoft Dynamics 365 for Operations“ versijai taikomi sistemos reikalavimai.

<a name="supported-web-browsers"></a>Palaikomos žiniatinklio naršyklės
----------------------

„Microsoft Dynamics 365 for Operations‟ žiniatinklio programa gali veikti bet kurioje iš tolesnių žiniatinklio naršyklių, veikiančių nurodytose operacinėse sistemose.

-   „Microsoft Edge‟ (naujausia viešai pasiekiama versija) sistemoje „Windows 10‟.
-   „Internet Explorer 11‟ sistemose „Windows 10‟, „Windows 8.1‟ arba „Windows 7‟.
-   „Google Chrome‟ (naujausia viešai pasiekiama versija) sistemose „Windows 10‟, „Windows 8.1‟, „Windows 8‟, „Windows 7‟ arba planšetėje „Google Nexus 10‟.
-   „Apple Safari‟ (naujausia viešai pasiekiama versija) sistemoje „Mac OS X 10.10‟ („Yosemite‟), 10.11 („El Capitan‟) arba 10.12 („Sierra‟) arba planšetėje „Apple iPad‟.

Norėdami rasti naujausią kiekvienos žiniatinklio naršyklės leidimą, eikite į programinės įrangos gamintojo svetainę. **Pastabos**

-   Norėdami užfiksuoti vaizdus, sugeneruotus užduočių įrašymo priemonėje ir įtraukti juos į „Microsoft Word“ dokumentus, turite turėti įdiegtą „Chrome“ plėtinį. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   Darbo eigos rengyklė paleidžiama kaip „ClickOnce“ taikomoji programa. Tik „Microsoft Edge“ ir „Internet Explorer“ (palaikomoje „Microsoft Windows“ versijoje) palaiko „ClickOnce“ taikomąsias programas. Darbo eigos rengyklės „ClickOnce“ taikomajai programai reikia 64 bitų suderinamos operacinės sistemos.
-   Finansinėms ataskaitoms skirtas ataskaitų konstruktorius paleidžiama kaip „ClickOnce“ taikomoji programa. Jam reikia 64 bitų suderinamos operacinės sistemos. Jei naudojate „Chrome“, turite įdiegti plėtinį „ClickOnce“, kad galėtumėte atsisiųsti ataskaitų konstruktorių. Jei naudojate „Chrome“ inkognito režimu, įsitikinkite, kad plėtinys „ClickOnce“ nustatytas veikti ir inkognito režimu.
-   Norint peržiūrėti PDF failus, rekomenduojame naudoti modernias naršykles, pvz., „Microsoft Edge“ (naujausią viešai prieinamą versiją) sistemoje „Windows 10“ arba „Google Chrome“ (naujausią viešai prieinamą versiją) sistemoje „Windows 10“, „Windows 8.1“, „Windows 8“ ar „Windows 7“ arba „Google" Nexus 10“ planšetiniame kompiuteryje.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Palaikomos „Retail Cloud POS‟ žiniatinklio naršyklės

„Dynamics 365 for Operations‟ programai skirtas „Retail Cloud POS‟ gali veikti bet kurioje iš tolesnių žiniatinklio naršyklių, veikiančių nurodytose operacinėse sistemose.

-   „Microsoft Edge‟ (naujausia viešai pasiekiama versija) sistemoje „Windows 10‟.
-   „Internet Explorer 11‟ sistemose „Windows 10‟, „Windows 8.1‟ arba „Windows 7‟.
-   „Chrome‟ (naujausia viešai pasiekiama versija) sistemoje „Windows 10‟, „Windows 8.1“ arba „Windows 7“.

## <a name="network-requirements"></a>Tinklo reikalavimai
-   „Dynamics 365 for Operations“ sukurta tinklams, kurių laukimo laikas mažesnis nei 150 milisekundžių (ms). Tai laukimo laikas iš naršyklės kliento iki „Microsoft Azure“ duomenų centro, kuriame yra „Dynamics 365 for Operations“. Rekomenduojame tinklo laukimo laiką patikrinti <http://www.azurespeed.com>.
-   Pralaidumo reikalavimai „Dynamics 365 for Operations“ priklauso nuo jūsų scenarijaus. Labiausiai įprastiems scenarijams reikia didesnio nei 50 kilobitų per sekundę (KB/s) pralaidumo. Tačiau tiems scenarijams, kurių mokamosios krovos reikalavimai aukšti, pvz., darbo sritims arba scenarijams, kurie apima nemažai tinkinimo, rekomenduojamas didesnis pralaidumas.

Apskritai, „Dynamics 365 for Operations“ yra optimizuota internetui. Kreipimosi ciklų iš naršyklės kliento į „Azure“ duomenų centrą skaičius yra labai mažas, o visa mokamoji krova yra suglaudinta. **Įspėjimas:** neskaičiuokite pralaidumo iš kliento vietos reikalavimų, vartotojų skaičių padauginę iš minimalių pralaidumo reikalavimų. Tam tikros vietos naudojimą vienu metu labai sunku apskaičiuoti. Klientams, kurie susirūpinę dėl pralaidumo reikalavimų, naudokite „Dynamics 365 for Operations“ peržiūros versiją.

## <a name="net-framework-requirements"></a>„.NET Framework“ reikalavimai
„Dynamics 365 for Operations“ reikia „.NET Framework“ 4.6.2 versijos visoms vieno paspaudimo taikomosioms programoms, pvz., dokumento maršruto planavimo agentui. Diegimo instrukcijų žr. [„.NET Framework“ diegimas](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Palaikomos „Microsoft Office“ taikomosios programos
-   Kad galėtumėte naudoti „Microsoft Excel“ papildinius, turi būti įdiegta „Windows“ arba „Mac“ skirta „Microsoft Office 2016“. Išsamios informacijos apie versijų reikalavimus žr. [„Office“ integravimo trikčių šalinimas](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Norėdami peržiūrėti dokumentus, sugeneruotus naudojant funkciją Eksportuoti į „Excel“ arba Eksportuoti į „Word“, turi būti įdiegta „Microsoft Office 2007“ arba naujesnė versija.

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
    -   „Windows 7 Professional“, „Enterprise“ ir „Ultimate“ leidimai **Pastaba:** „Windows 7“ palaikoma tik jei „Internet Explorer 11“ sistemoje įdiegta rankiniu būdu.
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

## <a name="requirements-for-development-on-local-vms"></a>Reikalavimai norint kurti vietiniuose virtualiuosiuose įrenginiuose
Išsamesnės informacijos apie reikalavimus norint kurti vietiniuose virtualiuosiuose įrenginiuose (VM) žr. [VM vykdymas vietoje](../dev-tools/access-instances.md).

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Gaukite „Dynamics 365 for Operations“ įvertinimo kopiją](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)




