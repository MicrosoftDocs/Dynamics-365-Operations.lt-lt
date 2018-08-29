---
title: "Aparatūros dydžio reikalavimų nustatymas vietinėse aplinkose"
description: "Šioje temoje pateikiami aparatūros dydžio reikalavimai vietinėje aplinkose."
author: kfend
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 269eb1f1c59ef52ce14da11c99fd6d292b9c0b4f
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---

# <a name="hardware-sizing-requirements-for-on-premises-environments"></a>Aparatūros dydžio reikalavimų nustatymas vietinėse aplinkose

[!include [banner](../includes/banner.md)]

Prieš pradėdami vietinės aplinkos aparatūros ir infrastruktūros dydžio nustatymo procesą, susipažinkite su temomis [Sistemos reikalavimai](system-requirements.md) ir [Sąrankos ir diegimo instrukcijos](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md), kad gerai suprastumėte pagrindinę infrastruktūrą. 

  **Pastaba:** atidžiai perskaitykite dalį apie geriausią sistemos sąrankos praktiką, kad užtikrintumėte optimalų našumą. 

Peržiūrėję dokumentus, galite pradėti savo operacijų ir vienu metu dirbančių vartotojų kiekio bei aplinkos dydžio nustatymo pagal vidutinį pagrindinį našumą procesą.

## <a name="factors-that-affect-sizing"></a>Dydį lemiantys veiksniai
Visi tolesniame paveikslėlyje parodyti veiksniai turi įtakos dydžiui. Kuo išsamesnė surinkta informacija, tuo tiksliau galite nustatyti dydį. Nenaudojant papildomų duomenų aparatūros dydis gali būti nustatytas netiksliai. Absoliutus mažiausias reikiamų duomenų kiekis yra didžiausia operacijos eilučių apkrova per valandą. 

[![Aparatūros dydžio nustatymas vietinėse aplinkose](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)

Žvelgiant iš kairės į dešinę, pirmiausias ir svarbiausias veiksnys, reikalingas norint tiksliai įvertinti dydį, yra operacijos šablonas arba operacijos apibūdinimas. Svarbu visada nustatyti didžiausią operacijų kiekį per valandą. Jei yra keli didžiausio kiekio laikotarpiai, šiuos laikotarpius būtina tiksliai apibrėžti. 

Reikia suprasti ne tik jūsų infrastruktūrai poveikį darančią apkrovą, taip pat reikia žinoti papildomą informaciją apie šiuos veiksnius. 

- **Operacijos** – įprastai operacijų apkrova tam tikru dienos / savaitės metu ženkliai padidėja. Tai daugiausia priklauso nuo operacijos tipo. Laiko ir išlaidų įrašai paprastai nurodo didžiausią apkrovą savaitėje, o pardavimo užsakymo įrašai dažnai teikiami masiškai integruojant ir nurodo didžiausią apkrovą dienoje. 

- **Vienu pačiu metu dirbančių vartotojų skaičius** – vienu metu dirbančių vartotojų skaičius yra antras svarbiausias dydžio nustatymo veiksnys. Dydžio negalima patikimai nustatyti naudojant tik vienu metu dirbančių vartotojų skaičių, todėl, jei tai vieninteliai jūsų turimi duomenys, apskaičiuokite apytiksliai ir tada patikslinkite šį skaičių, kai turėsite daugiau duomenų. Tiksli vienu metu dirbančių vartotojų apibrėžtis turi tenkinti toliau nurodytas sąlygas. 
  - Įvardytieji vartotojai nėra vienu metu dirbantys vartotojai.
  - Vienu metu dirbantys vartotojai visada priklauso įvardytųjų vartotojų pogrupiui. 
  - Didžiausia darbo apkrova nurodo didžiausią sutapimą atsižvelgiant į dydį.
 
- Kiekvienas iš vienu metu dirbančių vartotojų turi atitikti visus toliau nurodytus kriterijus. 
  - Prisijungęs. 
  - Skaičiavimo metu dirba su operacijomis / užklausomis. 
  - Seansas nėra laukimo būsenos. 
 
- **Duomenų struktūra** – tai daugiausia yra informacija apie tai, kaip jūsų sistema bus nustatyta ir sukonfigūruota. Pvz., kiek turėsite juridinių subjektų, prekių, KS lygių ir kiek sudėtinga bus jūsų saugos sąranka. Kiekvienas iš šių veiksnių gali turėti nedaug įtakos našumui, todėl šiuos veiksnius galima kompensuoti priimant protingus infrastruktūrinius sprendimus. 

- **Plėtiniai** – tinkinimai gali būti paprasti arba sudėtingi. Tinkinimų skaičius ir sudėtingumo bei naudojimo pobūdis daro įvairų poveikį reikiamos infrastruktūros dydžiui. Jei tinkinimai sudėtingi, patariama atlikti našumo vertinimus ir užtikrinti, kad ne tik tikrinamas jų našumas, bet taip pat geriau suprantami infrastruktūros poreikiai. Tai dar svarbiau, kai plėtiniai nėra koduoti atsižvelgiant į geriausią našumo ir išplečiamumo praktiką. 

- **Ataskaitos ir analizė** – šie veiksniai paprastai apima sudėtingų užklausų vykdymą naudojant įvairias duomenų bazes „Finance and Operations“ duomenų bazių sistemose. Suprasdami ir sumažindami brangių ataskaitų kūrimo dažnį, geriau suprasite jų daromą poveikį. 

- **Trečiųjų šalių sprendimai** – šiems sprendimams, pavyzdžiui, ISV, taikomos tos pačios išvados ir rekomendacijos kaip ir plėtiniams. 

## <a name="sizing-your-finance-and-operations-environment"></a>„Finance and Operations“ aplinkos dydžio nustatymas
Norėdami suprasti dydžio reikalavimus, turite žinoti didžiausią operacijų, kurias reikia apdoroti, kiekį. Didžiausia dalis pagalbinių sistemų, pvz., „Management Reporter“ arba SSRS, šiuo klausimu nėra tokios svarbios. Todėl šiame dokumente daugiausia dėmesio skiriama AOS ir „SQL Server“. 

**Pastaba:** paprastai skaičiavimo pakopos išsiplečia ir jos turėtų būti nustatomos N + 1 būdu, t. y. jei planuojate turėti tris AOS, įtraukite ketvirtą AOS. Duomenų bazės pakopą reikia nustatyti naudojant visada įjungtą ir gerai pasiekiamą sąranką. 


## <a name="sql-server-oltp"></a>SQL Server (OLTP)

### <a name="sizing"></a>Dydis

- 3 000 iki 15 000 operacijų eilučių per valandą duomenų bazės serverio branduolyje.
- Pirminio „SQL Server“ įprastas „AOS į SQL“ branduolio santykis 3:1. Papildomi branduoliai reikalingi atsižvelgiant į pasirinktą didelio pasiekiamo konfigūraciją. 
  - Apdorojant duomenų bazę stipriai apkraunančias operacijas, santykis gali būti sumažintas iki 2:1. 
- Toliau nurodyti veiksniai daro įtaką variantams. 
  - Naudojami parametrų nustatymai. 
  - Plėtinių lygiai. 
  - Papildomų funkcijų, pvz., duomenų bazės žurnalo ir įspėjimų, naudojimas. Detalus duomenų bazės registravimas dar labiau sumažins našumą per valandą branduolyje iki mažiau 3 000 eilučių. 
  - Duomenų struktūros sudėtingumas – paprastas sąskaitų planas, lyginant su išsamiu sąskaitų planu, daro netiesioginę įtaką našumui (kaip pavyzdys). 
  - Operacijos apibūdinimas.
  - Nuo 2 GB iki 4 GB atminties kiekviename branduolyje. 
  - Pagalbinės duomenų bazės duomenų bazės serveryje, pvz., „Management reporter“ ir SSRS duomenų bazės.
  - Laikinoji duomenų bazė = 15 % duomenų bazės dydžio, su tiek failų, kiek yra faktinių procesorių. 
  - SAN dydis ir našumas atsižvelgiant į bendrą vienu metu vykstančių operacijų kiekį / naudojimą. 

### <a name="high-availability"></a>Didelis pasiekiamumas 
Rekomenduojame „SQL Server“ visada naudoti klasterio arba dubliavimo sąrankoje. Antrasis SQL mazgas turi turėti tokį patį skaičių branduolių kaip pirminis mazgas. 

### <a name="active-directory-federation-services-ad-fs"></a>Active Directory Federation Services (AD FS)
Informacijos apie AD FS dydžio nustatymą žr. dalyje [AD FS serverio pajėgumo dokumentai](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).

Planuojant diegimo egzempliorių skaičių galima naudoti [dydžio skaičiuoklę](http://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx).

<a name="aos-online-and-batch"></a>AOS (tinklo ir paketinis)
----------------------

### <a name="sizing"></a>Dydis

- Dydis pagal operacijų kiekį / naudojimą
  - 2 000–6 000 eilučių branduolyje
  - 16 GB atminties viename egzemplioriuje
  - Standartinis paketas – 4–24 branduolių
  - 10–15 „Enterprise“ vartotojų branduolyje
  - 15–25 „Activity“ vartotojų branduolyje
  - 25–50 komandos narių branduolyje
- Paketas
   - 1–4 paketinių gijų branduolyje
   - Dydis pagal paketo lango apibūdinimą
- Atkreipkite dėmesį, kad AOS, „Data Management“ ir Paketas yra tie patys vaidmenys „Service Fabric‟. Turite nustatyti visų šių trijų apkrovų bendrą dydį, o ne jas atskirti, kaip tai daroma „Microsoft Dynamics AX 2012“.
- Čia taikomi tie patys „SQL Server“ įvairovės veiksniai.

### <a name="high-availability"></a>Didelis pasiekiamumas
- Įsitikinkite, kad turite bent 1–2 AOS daugiau, nei, jūsų skaičiavimais, reikia.
- Įsitikinkite, kad turite bent 3–4 virtualiuosius kompiuterius.

## <a name="management-reporter"></a>Management reporter
Daugeliu atvejų turėtų užtekti minimalių rekomenduojamų reikalavimų naudojant du mazgus, nebent naudojama labai daug. Daugiau nei dviejų mazgų reikia tik tuo atveju, jei apkrova yra labai didelė. Keiskite dydį pagal poreikį.

## <a name="sql-server-reporting-services"></a>SQL serverio ataskaitų tarnybos
Naudojant bendrai prieinamą leidimą, galima diegti tik vieną SSRS mazgą. Stebėkite savo SSRS mazgą tikrindami ir didinkite SSRS branduolių skaičių pagal poreikį. Įsitikinkite, kad virtualiajame kompiuteryje, kuris nėra SSRS VM, yra iš anksto sukonfigūruotas antrinis mazgas. Tai svarbu, jei kiltų problema, susijusi su virtualiąja mašina, kurioje numojamas SSRS, arba su virtualiuoju kompiuteriu. Tokiu atveju juos reikėtų pakeisti. 

## <a name="environment-orchestrator"></a>Aplinkos valdymo įrankis
Valdymo įrankio paslauga yra paslauga, kuri valdo jūsų įdiegtį ir su LCS susijusius ryšius. Ši paslauga diegiama kaip pirminė „Service Fabric‟ paslauga ir jai reikalingos bent trys VM. Ši paslauga pateikiama kartu su „Service Fabric‟ valdymo paslaugomis. Dydis turėtų būti nustatomas pagal didžiausią klasterio apkrovą. Daugiau informacijos žr. [„Service Fabric‟ klasterio pajėgumo planavimo klausimai](/azure/service-fabric/service-fabric-cluster-capacity).  


## <a name="virtualization-and-oversubscription"></a>Virtualizavimas ir perviršinis rezervavimas
Kritiškai svarbios tarnybos, pavyzdžiui, AOS, turi būti nuomojamos virtualiuosiuose kompiuteriuose, turinčiuose tam skirtus išteklius – branduolius, atmintį ir diską.   


