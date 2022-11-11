---
title: Perkėlimas į „Planning Optimization“ pagrindiniam planavimui
description: Šiame straipsnyje pateikiama informacija apie naują bendrojo planavimo mašinų, planavimo optimizavimą ir perkėlimą iš esamo modulio.
author: t-benebo
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: dbbc58f0dcd833f63e84a73ac68ada60bd0c291d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739957"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a>Perkėlimas į „Planning Optimization“ pagrindiniam planavimui

[!include [banner](../includes/banner.md)]

Sukurtas pagrindinis planavimo variklis nustatytas taip, kad neveiktų (negaliotų). Jį pakeitė „Planning Optimization“ papildinys skirtas „Microsoft Dynamics 365 Supply Chain Management“. Šiame straipsnyje pateikiama informacija apie poveikį naujiems ir esamiems diegimams. Jis apima informaciją apie būtinus veiksmus.

„Planning Optimization“ įjungia pagrindinio planavimo skaičiavimą siekiant, kad jis vyktų ne „Supply Chain Management“ ir jo „Azure SQL“ duomenų bazėje. Nauda susieta su „Planning Optimization“ apima pagerintą naudojimą ir sumažintą poveikį SQL duomenų bazėje pagrindinio planavimo vykdymo metu. Kadangi greito planavimo vykdymai gali būti atlikti net ir biuro darbo valandomis, planuotojai gali nedelsiant reaguoti ir reikalauti ar nustatyti parametrų keitimus.

Daugiau informacijos apie planavimo optimizavimą ieškokite bendrojo planavimo [sistemos architektūroje](master-planning-architecture.md).

## <a name="obsolescence-of-the-existing-master-planning-engine"></a>Esamo pagrindinio planavimo variklio neveikimas

Microsoft šiuo metu veikia, kad pasenęs bendrojo planavimo modulis būtų pasenęs planavimo optimizavimo proceso metu. Šis keitimas veikia visas debesies aplinkas. Patalpos diegimui nėra paveikti. Jei paleisite pasenusią bendrojo planavimo sistemą negeneruodami suplanuotų gamybos užsakymų, 10.0.16 ir vėlesnėje versijoje gausite klaidos pranešimą. Nepaisant to, pagrindinio planavimo vykdymas bus sėkmingai užbaigtas nepaisant klaidos pranešimo.

Daugiau informacijos apie pasenusią bendrojo planavimo sistemą ieškokite pranešimus apie pašalintas [arba pasenusias funkcijas Dynamics 365 Supply Chain Management](../get-started/removed-deprecated-features-scm-updates.md).

## <a name="migration-messages-and-exceptions"></a>Perkėlimas, pranešimai ir išimtys

Esamų aplinkojų, kurios paleidžia pasenusią bendrojo planavimo sistemą negeneruojant suplanuotų gamybos užsakymų, savininkai gaus el. laišką, kuriame pateikiama informacija apie išimčių procesą. Rekomenduojame kartu su partneriu įvertinti ir planuoti perėjimą prie „Planning Optimization“.

Kaip buvo nurodyta, 10.0.16 versijoje ir vėliau, jei paleisite pasenusią bendrojo planavimo sistemą negeneruodami suplanuotų gamybos užsakymų, gausite klaidos pranešimą. Šis klaidos pranešimas apima gaires dėl perkėlimo ir instrukcijas išlygos reikalavimui.

### <a name="new-deployments"></a>Nauji diegimai

Planavimo optimizavimas turi būti laikomas numatytuoju bendrojo planavimo moduliu visiems naujiems diegimams debesyje. Bendrai, „Planning Optimization“ turi būti naudojamas visiems diegimams, kurie nekuria suplanuotų gamybos užsakymų pagrindinio planavimo metu. Jei naujas diegimas priklauso nuo funkcijų, kurias planavimo optimizavimas šiuo metu nepalaiko, galite prašyti išimties, kad galėsite toliau naudoti pasenusią bendrojo planavimo sistemą.

### <a name="existing-deployments"></a>Esantys diegimai

Esantys debesimi grįsti diegimo savininkais priklauso nuo pagrindinio planavimo ir turi planuoti perkelti į „Planning Optimization“. Jei jūsų diegimas priklauso nuo funkcijų, kurias planavimo optimizavimas šiuo metu nepalaiko, galite prašyti išimties, kad vis tiek galite naudoti pasenusią bendrojo planavimo sistemą.

Aplinkoms, kurios šiuo metu naudoja pagrindinius planavimo procesus nuo panaikinimo „Microsoft“ nusiųs el. laišką aplinkos administratoriui. Šis laiškas pateiks informaciją apie veiksmus, kurių reikia perkelti ar reikalauti išlygos.

## <a name="the-exception-process"></a>Išlygos procesas

Galite prašyti išimties, jei turite toliau naudoti pasenusią bendrojo planavimo sistemą, nes jūsų verslo procesai priklauso nuo bent vienos funkcijos, kuri šiuo metu nėra įdiegta planavimo optimizavime. Esamoms sąrašo funkcijoms, žr. [„Planning Optimization“ atitikmens analizė](planning-optimization/planning-optimization-fit-analysis.md).

Šiuo metu planavimo optimizavimo perkėlimo išimtys tinka tik tada, jei jūsų bendrojo planavimo procese nėra gamybos (t. y. suplanuotų gamybos užsakymų, generuojamų bendrojo planavimo), ir jums reikia pasenusio bendrojo planavimo modulio be versijos 10.0.15.

Po to, kai būtinos funkcijos tampa būtinos, „Microsoft“ pateiks pereinamąjį laikotarpį, kol išlyga pasibaigs. Aplinkos administratorius bus informuotas, kai būtinos funkcijos bus prieinamos ir pereinamasis laikotarpis prasidės.

Šioje struktūrinėje schemoje apibendrinama šiame straipsnyje pateikiama informacija, kad galėtumėte greitai rasti, ar norite prašyti išimties. Jeigu jums reikia pateikti išimties užklausą, prašome užpildyti ir pateikti [Optimizavimo planavimo perkėlimo ir išimčių klausimyną](https://go.microsoft.com/fwlink/?linkid=2144962). Produktų grupė yra atsakinga už kiekvienos išimties užklausos vertinimą ir t. t., pateikite savo prašymą tiesiogiai produktų grupei naudodami pateiktą saitą ir nesukurkite palaikymo kvito. Jei jūsų prašymas atmestas, nesukurkite palaikymo kvito, nes "Microsoft Support" negali iš naujo įvertinti ar suteikti išimčių.

![Išimčių struktūrinė schema.](media/exception-diagram.png "Išimčių struktūrinė schema")

> [!NOTE]
> Galite pateikti išimčių užklausas tik tiems nuomotojams, kurie šiuo metu apima arba apims gamybos aplinką, o ne nuomotojams, turintiems tik sandėlio aplinką. Jei jums reikia išjungti „Planning Optimization“ išlygos klaidą infrastruktūrai kaip paslaugoms (IaaS) smėlio dėžės aplinkoje, vykdykite SQL laukimą pateiktą [Smėlio dėžės aplinkose](#faq-sandbox).

## <a name="frequently-asked-questions"></a>Dažniausiai užduodami klausimai

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a>Smėlio dėžės aplinkos

Ar mano sandbox aplinkoje galima naudoti pasenusią bendrojo planavimo sistemą? Ar man reikia išlygos?

**Atsakymas:** paprastai išimtys nėra susijusios su sandbox aplinka, nes planavimo optimizavimo išimties klaida neleidžia sėkmingai paleisti pasenusio bendrojo planavimo modulio. Nepaisant to, jei klaidos pranešimas jus trikdo, galite išjungti jį IaaS (ne „Service Fabric“) smėlio dėžės aplinka vykdoma tolesne užklausa jūsų duomenų bazėje:

```sql
-- Insert or update an enabled flight:
DECLARE @flightName NVARCHAR(100) = 'ReqPlanningOptimizationExceptionToggle';
IF NOT EXISTS (SELECT TOP 1 1 FROM SysFlighting WHERE flightName = @flightName)
    INSERT INTO SYSFLIGHTING(FLIGHTNAME,ENABLED, FLIGHTSERVICEID,PARTITION)
    SELECT @flightName, 1, 12719367,RECID FROM DBO.[PARTITIONS];
ELSE
    UPDATE SysFlighting SET enabled = 1, flightServiceId = 12719367 WHERE flightName = @flightName;
```

### <a name="on-premises-environments"></a>Patalpose esančios aplinkos

Mano aplinka patalpose. Ar man reikia išlygos?

**Atsakymas:** Ne. Išlygos nereikia patalpų aplinkoms. Galite ir toliau naudoti pasenusią bendrojo planavimo sistemą. Jūsų aplinkos administratorius bus informuotas, jei koks nors veiksmas bus būtinas.

### <a name="production-scenarios"></a>Produkto scenarijai

Naudojam suplanuotus gamybos planavimus, bet esu susirūpinęs apie tai, kas nutiks mums atnaujinus iki 10.0.16 versijos. Ar turiu imtis veiksmų?

**Atsakymas:** Nepergyvenkite. Galite ir toliau naudoti pasenusią bendrojo planavimo sistemą versijoje 10.0.16. Nepaisant to, rekomenduojame jums įvertinti, ar perkėlimas į „Planning Optimization“ gali prasidėti su esama funkcija. Taip pat rekomenduojame, kad būtumėte informuoti apie naujas funkcijas.

### <a name="email-from-microsoft"></a>El. laiškas iš „Microsoft“

Mūsų aplinkos administratorius gavo el. laišką iš „Microsoft“. Šiame el. laiške sakoma, kad turime perkelti į „Planning Optimization“ ar reikalauti išlygos. Ar turiu imtis veiksmų?

**Atsakymas:** Taip. Jūsų aplinka bus paveikta nebent seksite nurodymus el. laiške. Galit perkelti „Planning Optimization“ pagal datą nurodytą ar prašyti išlygos naudodami nuorodą į el. laišką. Ši nuoroda atveria klausimyną. Jums užbaigus ir pateikus šį klausimyną, gausite atsakymą el. paštu. Nepaisant to, kad šis procesas yra rankinis, „Microsoft“ bando atsakyti per savaitę po pateikto klausimyno.

### <a name="error-messages"></a>Klaidų pranešimai

Naudoju versiją 10.0.16 ar vėlesnę ir gaunu tolesnį klaidos pranešimą vykdydamas pagrindinį planavimą. Ar pagrindinis planavimas blokuojamas?

> Gaunate šį klaidos pranešimą, nes scenarijams, kuriuos palaiko planavimo optimizavimas, buvo naudojamas pasenusias bendrojo planavimo modulis. Dabar turite perkelti į planavimo optimizavimą, nes įtaisytasis bendrojo planavimo modulis pasenusis. Atminkite, kad šis pagrindinio planavimo vykdymas sėkmingai baigtas.
>
> Jei jūsų perkėlimas labai priklauso nuo laukiančių funkcijų, galima reikalingu toliau naudoti pasenusio bendrojo planavimo modulio išimtį.
>
> Prašome užbaigti tolesnį klausimyną, kad pradėtumėte ir jei būtina užklausos išlygą iš migravimo turi būti perkelta į „Planning Optimization“.

**Atsakymas:** Ne, pagrindinis planavimas neblokuojamas. Jūsų pagrindinis planavimo vykdymas sėkmingai baigtas ir galite naudoti rezultatus įprastu būdu. Nepaisant to, siekiant išvengti šios klaidos pranešimo funkcijos pagrindinio planavimo vykdymo metu, turite perkelti į „Planning Optimization“ nedelsiant arba prašyti išlygos naudodami nuorodą klaidos pranešime.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
