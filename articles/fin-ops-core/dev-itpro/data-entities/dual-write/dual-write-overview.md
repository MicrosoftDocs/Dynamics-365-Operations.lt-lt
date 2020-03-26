---
title: Dvigubo rašymo apžvalga
description: Šioje temoje pateikiama dvigubo rašymo apžvalga. Dvigubas rašymas yra infrastruktūra, kuri beveik realiuoju laiku teikia sąveiką tarp „Microsoft Dynamics 365” modeliu pagrįstų programų ir „Finance and Operations” programų.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c4a643d4981364cea5b549118c201ac8a9798e02
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113879"
---
# <a name="dual-write-overview"></a>Dvigubo rašymo apžvalga

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

## <a name="what-is-dual-write"></a>Kas yra dvigubas rašymas?

Dvigubas rašymas yra parengta naudoti infrastruktūra, kuri beveik realiuoju laiku teikia sąveiką tarp „Microsoft Dynamics 365” esančių modeliu pagrįstų programų ir „Finance and Operations” programų. Kai duomenys apie klientus, produktus, žmones ir operacijas siunčiami už programos ribų, visiems organizacijos padaliniams suteikiami įgaliojimai.

Dvigubu rašymu pateikiama glaudžiai susieta, dvikryptė integracija tarp „Finance and Operations” programų ir „Common Data Service”. Bet kokie duomenų keitimai, vykdomi „Finance and Operations” programose, taip pat įrašomi į „Common Data Service”, o bet kokie „Common Data Service” duomenų keitimai yra įrašomi  „Finance and Operations” programose. Šis automatizuotas duomenų srautas suteikia integruotą vartotojo patirtį susietose programose.

![Duomenų ryšys tarp programų](media/dual-write-overview.jpg)

Dvigubo rašymo aspektai yra du – *infrastruktūros* aspektas ir *programos* aspektas.

### <a name="infrastructure"></a>Infrastruktūra

Dvigubo rašymo infrastruktūra yra išplėstinė ir patikima, joje yra šios pagrindinės funkcijos:

+ Sinchroninis ir dvikryptis duomenų srautas tarp programų
+ Sinchronizavimas, kartu su atkūrimo, pristabdymo ir papildymo režimais, siekiant palaikyti sistemą internetiniu ir autonominiu / asinchroniniu režimais.
+ Galimybė sinchronizuoti pradinius duomenis tarp programų
+ Konsoliduotas veiklos rodinys ir duomenų administratorių klaidų žurnalas
+ Galimybė konfigūruoti pasirinktinius įspėjimus ir ribines vertes bei prenumeruoti pranešimus
+ Intuityviosios vartotojo sąsajos (UI) filtravimas ir transformacijos
+ Galimybė nustatyti ir peržiūrėti objekto priklausomybes ir ryšius
+ Ir standartinių, ir tinkintų objektų bei žemėlapių išplėtimas
+ Patikimas programos vykdymo ciklo valdymas
+ Naujo kliento iš anksto parengtos sąrankos funkcijos

### <a name="application"></a>Programos

Dvigubu rašymu sukuriamas susiejimas tarp sąvokų, esančių „Finance and Operations” programose, ir sąvokų, esančių „Dynamics 365” modeliu pagrįstų programų. Ši integracija palaiko šiuos scenarijus:

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
+ Vartotojams skirtas vieno šaltinio valdymas
+ Integruoti mažmeninės prekybos ir rinkodaros kanalai
+ Akcijų ir nuolaidų matomumas
+ Užklausų dėl aptarnavimo funkcijos
+ Racionalizuotos aptarnavimo operacijos

## <a name="top-reasons-to-use-dual-write"></a>Pagrindinės priežastys naudoti dvigubą rašymą

Dvigubu rašymu pateikiama duomenų integracija „Microsoft Dynamics 365” programose. Ši patikima sistema susieja aplinkas ir įgalina skirtingas verslo programas dirbti kartu. Čia pateikiamos pagrindinės priežastys, kodėl reikia naudoti dvigubą rašymą:

+ Dvigubas rašymas suteikia glaudžiai susietą, beveik realiuoju laiku ir dvikryptę integraciją tarp „Finance and Operations” programų ir „Dynamics 365” modeliu pagrįstų programų. Su šiuo integravimu „Microsoft Dynamics 365“ tampa ypač daugialype visiems jūsų verslo sprendimams. Klientai, kurie naudoja „Dynamics 365 Finance” ir „Dynamics 365 Supply Chain Management”, bet kurie naudoja ne „Microsoft” sprendimus kliento ryšių valdymui (CRM), ilgainiui renkasi dažniau „Dynamics 365” dėl jame palaikomo dvigubo rašymo.
+ Duomenys iš klientų, produktų, operacijų, projektų ir internetu sąveikaujančių įrenginių („IoT”) automatiškai siunčiami į „Common Data Service” naudojant dvigubą rašymą. Šis ryšys yra labai naudingas verslo įmonėms, kurios domisi „Microsoft Power Platform” plėtiniais.
+ Dvigubo rašymo infrastruktūra atitinka kodo nereikalavimo / automatizuoto kodavimo principą. Reikia minimalių inžinerinių pastangų, kad būtų galima išplėsti standartinius tarpusavy susietų lentelių žemėlapius ir į juos įterpti pasirinktinius žemėlapius.
+ Dvigubas rašymas palaiko ir internetinį režimą, ir autonominį režimą. „Microsoft” yra vienintelė įmonė, teikianti palaikymą internetiam ir autonominiam režimams.

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a>Kuo vartotojui ir CRM produktų architektams naudingas dvigubas rašymas?

Dvigubas rašymas automatizuoja duomenų srautą tarp „Finance and Operations” programų ir „Common Data Service”. Būsimuose leidimuose sąvokos, esančios „Dynamics 365” modeliu pagrįstose programose, (pvz., klientas, kontaktas, pasiūlymas ir užsakymas) bus pritaikytos vidutinių įmonių ir didesnių nei vidutinės įmonių klientams.

Pirmuoju leidimu didžioji dalis automatizavimo valdoma dvigubo rašymo sprendimų. Būsimuose leidimuose šie sprendimai taps „Common Data Service“ dalimi. Suprasdami būsimų keitimų, kurie bus vykdomi „Common Data Service”, naudą ilgainiui galėsite sutaupyti pastangų. Štai keletas esminių keitimų:

+ „Common Data Service” bus naujų sąvokų, tokių kaip įmonė ir šalis. Šios sąvokos paveiks visas programas, kurios yra sukurtos platformoje „Common Data Service”, pvz., „Dynamics 365 Sales”, „Dynamics 365 Marketing”, „Dynamics 365 Customer Service” ir „Dynamics 365 Field Service”.
+ Veiklos ir pastabos yra suvienodintos ir išplėstos, kad būtų palaikomi ir C1 (sistemos vartotojai), ir C2 (sistemos klientai).
+ Štai keletas būsimų „Common Data Service” keitimų:

    - Dešimtainių duomenų tipas pakeis pinigų duomenų tipą.
    - Datos galiojime bus palaikomi ankstesni, dabartiniai ir būsimi duomenys toje pačioje vietoje.
    - Bus išplėstas valiutos ir valiutos kursų palaikymas, o programos programavimo sąsaja (API) **Valiutos kursas** bus peržiūrėta.
    - Bus palaikomi vienetų konvertavimai.

Norėdami gauti daugiau informacijos apie būsimus keitimus, žr. [Duomenys platformoje „Common Data Service” – 1 ir 2 etapai](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).
