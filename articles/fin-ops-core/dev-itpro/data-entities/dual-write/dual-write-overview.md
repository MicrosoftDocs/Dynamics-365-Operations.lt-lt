---
title: Dvigubo rašymo apžvalga
description: Šiame straipsnyje pateikiama dvigubo rašymo peržiūra, kuri leidžia realiuoju laiku bendrauti tarp klientų įsipareigojimo programėlių ir finansų ir operacijų programėlių.
author: RamaKrishnamoorthy
ms.date: 02/06/2020
ms.topic: overview
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2ef4fb1a51bd92db440841eb2a9d9ebcce0e1b1d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872946"
---
# <a name="dual-write-overview"></a>Dvigubo rašymo apžvalga

[!include [banner](../../includes/banner.md)]





## <a name="what-is-dual-write"></a>Kas yra dvigubas rašymas?

Dvigubo rašymo sistema yra ne "box" infrastruktūra, kuri leidžia realiuoju laiku užtikrinti klientų įsipareigojimo programėlių ir finansų ir operacijų programėlių sąveiką. Kai duomenys apie klientus, produktus, žmones ir operacijas siunčiami už programos ribų, visiems organizacijos padaliniams suteikiami įgaliojimai.

Dvigubo rašymo sistema užtikrina daugiakryptį finansų ir operacijų programėlių ir dviejų krypčių integravimą Dataverse. Dėl bet kokių duomenų keitimo finansų ir operacijų programėlių Dataverse Dataverse rašoma ir visi duomenų keitimo priežastis kuria finansų ir operacijų programėles. Šis automatizuotas duomenų srautas suteikia integruotą vartotojo patirtį susietose programose.

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

Dvigubo rašymo atveju sukuriamas finansų ir operacijų programėlių sąvokų ir klientų įsipareigojimo programėlių sąvokų susiejimas. Ši integracija palaiko šiuos scenarijus:

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

+ Dvigubas rašymas suteikia glaudžiai susietą, beveik realiuoju laiku dvikryptę integraciją tarp „Finance and Operations” ir „Customer Engagement” programų. Su šiuo integravimu „Microsoft Dynamics 365“ tampa ypač daugialype visiems jūsų verslo sprendimams. Klientai, naudojantys "Dynamics 365" Dynamics 365 Supply Chain Management finansus ir, bet naudojantys ne "Microsoft" sprendimus ryšių su klientais valdymui (CRM), perkeliami į "Dynamics 365" dėl dvigubo rašymo palaikymo.
+ Duomenys iš klientų, produktų, operacijų, projektų ir internetu sąveikaujančių įrenginių („IoT”) automatiškai siunčiami į „Dataverse” naudojant dvigubą rašymą. Šis ryšys yra naudingas verslo įmonėms, kurios domisi „Power Platform” plėtiniais.
+ Dvigubo rašymo infrastruktūra atitinka kodo nereikalavimo / automatizuoto kodavimo principą. Reikia minimalių inžinerinių pastangų, kad būtų galima išplėsti standartinius tarpusavy susietų lentelių žemėlapius ir į juos įterpti pasirinktinius žemėlapius.
+ Dvigubas rašymas palaiko ir internetinį režimą, ir autonominį režimą. „Microsoft” yra vienintelė įmonė, teikianti palaikymą internetiam ir autonominiam režimams.

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>Kuo dvigubas rašymas naudingas klientų įtraukimo programų kūrėjams ir architektams?

Dvigubo rašymo metu automatizuojami duomenų srautai tarp finansų ir operacijų programėlių ir klientų įsipareigojimo programėlių. Dvigubas rašymas susideda iš dviejų „AppSource” sprendimų, įdiegtų „Dataverse”. Sprendimai išplečia „Dataverse” lentelių schemą, priedus ir darbo eigas, kad jie galėtų pritaikyti mastelį prie ERP dydžio. Sėkmingai įdiegtos programos programuotojai ir architektai turi suprasti šiuos pakeitimus ir bendradarbiauti su finansų ir operacijų programėle.

Norėdami sukurti lygumą su finansų ir operacijų programomis, dvigubo rašymo metu schemoje labai pasikeičia Dataverse. Jei suprantate planą, galite išvengti kai kurių kūrimo ir tobulinimo perdarymo veiksmų ateityje.

+ Įdiegus dvigubo rašymo „AppSource” paketą, „Dataverse” bus naujų sąvokų, tokių kaip įmonė ir šalis. Šios koncepcijos Dataverse padeda programoms, įtaisytoms "Dynamics 365 Sales", "Dynamics 365 Marketing", "Dynamics 365" klientų aptarnavimo tarnyba, Dynamics 365 Field Service ir sklandžiai sąveikauti su finansų ir operacijų programomis.

+ Veiklos ir pastabos yra suvienodintos ir išplėstos, kad būtų palaikomi ir C1 (sistemos vartotojai), ir C2 (sistemos klientai).

+ Norėdami išvengti duomenų praradimo Dataverse perduodant valiutą tarp finansų ir operacijų programėlių ir "The", galėsite išplėsti klientų įsipareigojimo programėlių valiutos duomenų tipo dešimtainių dalių vietų skaičių. Funkcija automatiškai paverčia esamas eilutes nauja išplėstine būsena metaduomenų sluoksnyje. Šio proceso metu valiutos vertė yra paverčiama dešimtainiais duomenimis, o ne pinigų duomenimis, ir valiutos vertė palaiko 10 skaitmenų po kablelio. Ši funkcija pasirenkama, todėl organizacijoms, kurioms nereikia daugiau nei 4 skaitmenų po kablelio tikslumo, nereikia naudoti funkcijos. Daugiau informacijos žr. [Dvigubo rašymo valiutos duomenų tipo perkėlimas](currrency-decimal-places.md).

+ [Datos galiojimas](../../dev-tools/date-effectivity.md) bus įtrauktas į „Dataverse”. Jame bus palaikomi ankstesni, dabartiniai ir būsimi duomenys toje pačioje lentelėje.

+ Produkto [vienetų konvertavimai](../../../../supply-chain/pim/tasks/manage-unit-measure.md) palaikomi produktuose, pasiūlymuose, užsakymuose ir SF.

Daugiau informacijos apie būsimus keitimus žr. [Kas nauja ar pasikeitė dvigubo rašymo integravime](whats-new-dual-write.md).



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
