---
title: Dvigubo rašymo apžvalga
description: Šioje temoje pateikiama dvigubo rašymo apžvalga, kuri suteikia beveik realiojo laiko sąveiką tarp klientų įtraukimo programų ir „Finance and Operations“ programų.
author: RamaKrishnamoorthy
ms.date: 02/06/2020
ms.topic: overview
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f39322a0c2ef50ef2bbeb256c80096e0687c4642
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061339"
---
# <a name="dual-write-overview"></a>Dvigubo rašymo apžvalga

[!include [banner](../../includes/banner.md)]





## <a name="what-is-dual-write"></a>Kas yra dvigubas rašymas?

Dvigubas rašymas yra nebenaudojama infrastruktūra, kuri užtikrina beveik realiojo laiko sąveiką tarp klientų įtraukimo programų ir „Finance and Operations“ programų. Kai duomenys apie klientus, produktus, žmones ir operacijas siunčiami už programos ribų, visiems organizacijos padaliniams suteikiami įgaliojimai.

Dvigubas rašymas suteikia glaudžiai susietą dvikryptį „Finance and Operations“ programų ir Dataverse. Bet koks duomenų pasikeitimas „Finance and Operations“ programose sukelia rašymą į Dataverse ir bet kokie duomenų pasikeitimai Dataverse sukelia rašymą į „Finance and Operations“ programas. Šis automatizuotas duomenų srautas suteikia integruotą vartotojo patirtį susietose programose.

![Duomenų ryšys tarp programų.](media/dual-write-overview.jpg)

Dvigubo rašymo aspektai yra du – *infrastruktūros* aspektas ir *programos* aspektas.

### <a name="infrastructure"></a>Infrastruktūra

Dvigubo rašymo infrastruktūra yra išplėstinė ir patikima, joje yra šios pagrindinės funkcijos:

+ Sinchroninis ir dvikryptis duomenų srautas tarp programų
+ Sinchronizavimas, kartu su atkūrimo, pristabdymo ir papildymo režimais, siekiant palaikyti sistemą internetiniu ir autonominiu / asinchroniniu režimais.
+ Galimybė sinchronizuoti pradinius duomenis tarp programų
+ Jungtinis veiklos rodinys ir duomenų administratorių klaidų žurnalas
+ Galimybė konfigūruoti pasirinktinius įspėjimus ir ribines vertes bei prenumeruoti pranešimus
+ Intuityviosios vartotojo sąsajos (UI) filtravimas ir transformacijos
+ Galimybė nustatyti ir peržiūrėti lentelės priklausomybes ir ryšius
+ Ir standartinių, ir tinkintų lentelių bei žemėlapių išplėtimas
+ Patikimas programos vykdymo ciklo valdymas
+ Naujo kliento iš anksto parengtos sąrankos funkcijos

### <a name="application"></a>Prašymas

Dvigubas rašymas sukuria sąvokų „Finance and Operations“ programose ir sąvokų klientų įtraukimo programose susiejimą. Ši integracija palaiko šiuos scenarijus:

+ Bendrieji integruoto kliento duomenys
+ Prieiga prie kliento lojalumo kortelių ir atlygio taškų
+ Bendrojo produkto bendrosios funkcijos
+ Supratimas apie organizacijos hierarchiją
+ Bendrieji integruoto tiekėjo duomenys
+ Prieiga prie finansinių ir mokesčių nuorodos duomenų
+ Kainos pagal poreikį mechanizmo funkcijos
+ Integruotos potencialių klientų ir grynųjų pinigų funkcijos
+ Galimybė aptarnauti vidaus turtą ir klientų turtą per techninės pagalbos darbo vietoje agentus
+ Integruotos įsigijimo ir apmokėjimo funkcijos
+ Kliento duomenų ir dokumentų integruotos veiklos ir pastabos
+ Galimybė ieškoti turimų atsargų pasiekiamumą ir išsamią informaciją
+ Projekto ir grynųjų pinigų funkcijos
+ Galimybė tvarkyti kelis adresus ir vaidmenis naudojant šalies sąvoką


## <a name="top-reasons-to-use-dual-write"></a>Pagrindinės priežastys naudoti dvigubą rašymą

Dvigubu rašymu pateikiama duomenų integracija „Microsoft Dynamics 365” programose. Ši patikima sistema susieja aplinkas ir įgalina skirtingas verslo programas dirbti kartu. Čia pateikiamos pagrindinės priežastys, kodėl reikia naudoti dvigubą rašymą:

+ Dvigubas rašymas suteikia glaudžiai susietą, beveik realiuoju laiku dvikryptę integraciją tarp „Finance and Operations” ir „Customer Engagement” programų. Su šiuo integravimu „Microsoft Dynamics 365“ tampa ypač daugialype visiems jūsų verslo sprendimams. Klientai, kurie naudoja „Dynamics 365 Finance” ir „Dynamics 365 Supply Chain Management”, bet kurie naudoja ne „Microsoft” sprendimus kliento ryšių valdymui (CRM), ilgainiui renkasi dažniau „Dynamics 365” dėl jame palaikomo dvigubo rašymo.
+ Duomenys iš klientų, produktų, operacijų, projektų ir internetu sąveikaujančių įrenginių („IoT”) automatiškai siunčiami į „Dataverse” naudojant dvigubą rašymą. Šis ryšys yra naudingas verslo įmonėms, kurios domisi „Power Platform” plėtiniais.
+ Dvigubo rašymo infrastruktūra atitinka kodo nereikalavimo / automatizuoto kodavimo principą. Reikia minimalių inžinerinių pastangų, kad būtų galima išplėsti standartinius tarpusavy susietų lentelių žemėlapius ir į juos įterpti pasirinktinius žemėlapius.
+ Dvigubas rašymas palaiko ir internetinį režimą, ir autonominį režimą. „Microsoft” yra vienintelė įmonė, teikianti palaikymą internetiam ir autonominiam režimams.

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>Kuo dvigubas rašymas naudingas klientų įtraukimo programų kūrėjams ir architektams?

Dvigubas rašymas automatizuoja duomenų srautą tarp „Finance and Operations“ ir klientų įtraukimo programų. Dvigubas rašymas susideda iš dviejų „AppSource” sprendimų, įdiegtų „Dataverse”. Sprendimai išplečia „Dataverse” lentelių schemą, priedus ir darbo eigas, kad jie galėtų pritaikyti mastelį prie ERP dydžio. Kad įgyvendinimas būtų sėkmingas, klientų įtraukimo programų kūrėjai ir architektai turi suprasti šiuos pakeitimus ir bendradarbiauti su savo kolegomis kurdami programas „Finance and Operations“.

Norint sukurti lygybę su „Finance and Operations“ programomis, dvigubas rašymas atlieka keletą esminių pakeitimų Dataverse schema. Jei suprantate planą, galite išvengti kai kurių kūrimo ir tobulinimo perdarymo veiksmų ateityje.

+ Įdiegus dvigubo rašymo „AppSource” paketą, „Dataverse” bus naujų sąvokų, tokių kaip įmonė ir šalis. Šios sąvokos padeda kurti programas Dataverse, įskaitant „Dynamics 365 Sales“, „Dynamics 365 Marketing“, „Dynamics 365 Customer Service“ ir Dynamics 365 Field Service, kad galėtumėte sklandžiai bendrauti su „Finance and Operations“ programomis.

+ Veiklos ir pastabos yra suvienodintos ir išplėstos, kad būtų palaikomi ir C1 (sistemos vartotojai), ir C2 (sistemos klientai).

+ Kad neprarastumėte duomenų, kai persiunčiama valiuta tarp „Finance and Operations“ programų ir Dataverse, galėsite išplėsti skaitmenų po kablelio skaičių klientų įtraukimo programų valiutos duomenų tipe. Funkcija automatiškai paverčia esamas eilutes nauja išplėstine būsena metaduomenų sluoksnyje. Šio proceso metu valiutos vertė yra paverčiama dešimtainiais duomenimis, o ne pinigų duomenimis, ir valiutos vertė palaiko 10 skaitmenų po kablelio. Ši funkcija pasirenkama, todėl organizacijoms, kurioms nereikia daugiau nei 4 skaitmenų po kablelio tikslumo, nereikia naudoti funkcijos. Daugiau informacijos žr. [Dvigubo rašymo valiutos duomenų tipo perkėlimas](currrency-decimal-places.md).

+ [Datos galiojimas](../../dev-tools/date-effectivity.md) bus įtrauktas į „Dataverse”. Jame bus palaikomi ankstesni, dabartiniai ir būsimi duomenys toje pačioje lentelėje.

+ Produkto [vienetų konvertavimai](../../../../supply-chain/pim/tasks/manage-unit-measure.md) palaikomi produktuose, pasiūlymuose, užsakymuose ir SF.

Daugiau informacijos apie būsimus keitimus žr. [Kas nauja ar pasikeitė dvigubo rašymo integravime](whats-new-dual-write.md).



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
