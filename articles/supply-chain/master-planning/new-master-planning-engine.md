---
title: Perkėlimas į „Planning Optimization“ pagrindiniam planavimui
description: Šioje temoje aprašyta informacija apie naują pagrindinio planavimo variklį „Planning Optimization“ ir apie perkėlimą iš esančio variklio.
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9590213ef73f7623aff10d4c8ee3efbea0e7984b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823462"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a>Perkėlimas į „Planning Optimization“ pagrindiniam planavimui

[!include [banner](../includes/banner.md)]

Sukurtas pagrindinis planavimo variklis nustatytas taip, kad neveiktų (negaliotų). Jį pakeitė „Planning Optimization“ papildinys skirtas „Microsoft Dynamics 365 Supply Chain Management“. Šioje temoje pateikta informacija apie naujo ir esančių diegimų poveikį. Jis apima informaciją apie būtinus veiksmus.

„Planning Optimization“ įjungia pagrindinio planavimo skaičiavimą siekiant, kad jis vyktų ne „Supply Chain Management“ ir jo „Azure SQL“ duomenų bazėje. Nauda susieta su „Planning Optimization“ apima pagerintą naudojimą ir sumažintą poveikį SQL duomenų bazėje pagrindinio planavimo vykdymo metu. Kadangi greito planavimo vykdymai gali būti atlikti net ir biuro darbo valandomis, planuotojai gali nedelsiant reaguoti ir reikalauti ar nustatyti parametrų keitimus.

Daugiau informacijos apie „Planning Optimization“ rasite [„Planning Optimization“ apžvalga](planning-optimization/planning-optimization-overview.md).

## <a name="obsolescence-of-the-existing-master-planning-engine"></a>Esamo pagrindinio planavimo variklio neveikimas

„Microsoft“ bando sukurti įtaisytąjį pagrindinį variklį, neveikiantį „Planning Optimization“ naudai. Šis keitimas veikia visas debesies aplinkas. Patalpos diegimui nėra paveikti. Versijoje 10.0.16 ir vėlesnėje gausite klaidos pranešimą, kai vykdysite sukurtą pagrindinį planavimą nekurdami suplanuotų gamybos užsakymų. Nepaisant to, pagrindinio planavimo vykdymas bus sėkmingai užbaigtas nepaisant klaidos pranešimo.

Dėl daugiau informacijos apie negaliojantį sukurtą planavimo variklį, žr. [Pašalintos ar negaliojančios funkcijos „Dynamics 365 Supply Chain Management“](../get-started/removed-deprecated-features-scm-updates.md).

## <a name="migration-messages-and-exceptions"></a>Perkėlimas, pranešimai ir išimtys

Esančių aplinkų, kurios vykdo įtaisytąjį bendrojo planavimo mechanizmą, nekurdamos suplanuotos gamybos užsakymų, svininkas gaus el. laišką, kuriame pateikta išsami informacija apie proceso išlygą. Rekomenduojame kartu su partneriu įvertinti ir planuoti perėjimą prie „Planning Optimization“.

Kaip buvo minėta, versijoje 10.0.16 ir vėlesnėje versijoje gausite klaidos pranešimą, kai vykdysite sukurtą pagrindinį planavimą nekurdami suplanuotų gamybos užsakymų. Šis klaidos pranešimas apima gaires dėl perkėlimo ir instrukcijas išlygos reikalavimui.

### <a name="new-deployments"></a>Nauji diegimai

„Planning Optimization“ turi būti laikomas numatytuoju pagrindinio planavimo variklius visiems diegimams debesyje. Bendrai, „Planning Optimization“ turi būti naudojamas visiems diegimams, kurie nekuria suplanuotų gamybos užsakymų pagrindinio planavimo metu. Jei naujas diegimas priklauso nuo funkcijų, kurios „Planning Optimization“ šiuo metu nepalaikomos, galite reikalauti išimties taip, kad tęstumėte naudoti sukurtą pagrindinį planavimo variklį.

### <a name="existing-deployments"></a>Esantys diegimai

Esantys debesimi grįsti diegimo savininkais priklauso nuo pagrindinio planavimo ir turi planuoti perkelti į „Planning Optimization“. Jei jūsų diegimas priklauso nuo funkcijų, kurios „Planning Optimization“ šiuo metu nepalaikomos, galite reikalauti išimties taip, kad tęstumėte naudoti sukurtą pagrindinį planavimo variklį.

Aplinkoms, kurios šiuo metu naudoja pagrindinius planavimo procesus nuo panaikinimo „Microsoft“ nusiųs el. laišką aplinkos administratoriui. Šis laiškas pateiks informaciją apie veiksmus, kurių reikia perkelti ar reikalauti išlygos.

## <a name="the-exception-process"></a>Išlygos procesas

Galite prašyti išlygos, jei turite tęsti naudoti sukurtus pagrindinį planavimo variklį, nes jūsų verslo procesai priklauso stipriai nuo paskutinės funkcijos, kuri šiuo metu nėra įkelta į „Planning Optimization“. Esamoms sąrašo funkcijoms, žr. [„Planning Optimization“ atitikmens analizė](planning-optimization/planning-optimization-fit-analysis.md).

Šiuo metu, išlygos „Planning Optimization“ perkėlimui yra tik būtinos, jei jūsų pagrindinis planavimo procesas neapima gamybos (tai yra, suplanuotos gamybos užsakymų, kuriuos sukūrė pagrindinis planavimas) ir jums reikia sukurtų pagrindinio planavimo variklio versijų vėlesnių nei 10.0.15.

Po to, kai būtinos funkcijos tampa būtinos, „Microsoft“ pateiks pereinamąjį laikotarpį, kol išlyga pasibaigs. Aplinkos administratorius bus informuotas, kai būtinos funkcijos bus prieinamos ir pereinamasis laikotarpis prasidės.

> [!NOTE]
> Galite tik reikalauti išlygos gamybos aplinkoms, o ne smėlio dėžės aplinkoms. Jei jums reikia išjungti „Planning Optimization“ išlygos klaidą infrastruktūrai kaip paslaugoms (IaaS) smėlio dėžės aplinkoje, vykdykite SQL laukimą pateiktą [Smėlio dėžės aplinkose](#faq-sandbox).

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a>Smėlio dėžės aplinkos

Ar galiu naudoti sukurtą pagrindinė planavimą savo smėlio dėžėje? Ar man reikia išlygos?

**Atsakymas:** Išlygos nėra įprastai svarbios smėlio dėžės aplinkoms, dėl to, kad „Planning Optimization“ išlygos klaida neapsaugo inkorporuoto pagrindinio planavimo variklio nuo sėkmingo veikimo. Nepaisant to, jei klaidos pranešimas jus trikdo, galite išjungti jį IaaS (ne „Service Fabric“) smėlio dėžės aplinka vykdoma tolesne užklausa jūsų duomenų bazėje:

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

**Atsakymas:** Ne. Išlygos nereikia patalpų aplinkoms. Galite tęsti naudoti inkorporuotą pagrindinį planavimą. Jūsų aplinkos administratorius bus informuotas, jei koks nors veiksmas bus būtinas.

### <a name="production-scenarios"></a>Produkto scenarijai

Naudojam suplanuotus gamybos planavimus, bet esu susirūpinęs apie tai, kas nutiks mums atnaujinus iki 10.0.16 versijos. Ar turiu imtis veiksmų?

**Atsakymas:** Nepergyvenkite. Galite tęsti naudoti inkorporuotą pagrindinį planavimą iki 10.0.16 versijos. Nepaisant to, rekomenduojame jums įvertinti, ar perkėlimas į „Planning Optimization“ gali prasidėti su esama funkcija. Taip pat rekomenduojame, kad būtumėte informuoti apie naujas funkcijas.

### <a name="email-from-microsoft"></a>El. laiškas iš „Microsoft“

Mūsų aplinkos administratorius gavo el. laišką iš „Microsoft“. Šiame el. laiške sakoma, kad turime perkelti į „Planning Optimization“ ar reikalauti išlygos. Ar turiu imtis veiksmų?

**Atsakymas:** Taip. Jūsų aplinka bus paveikta nebent seksite nurodymus el. laiške. Galit perkelti „Planning Optimization“ pagal datą nurodytą ar prašyti išlygos naudodami nuorodą į el. laišką. Ši nuoroda atveria klausimyną. Jums užbaigus ir pateikus šį klausimyną, gausite atsakymą el. paštu. Nepaisant to, kad šis procesas yra rankinis, „Microsoft“ bando atsakyti per savaitę po pateikto klausimyno.

### <a name="error-messages"></a>Klaidų pranešimai

Naudoju versiją 10.0.16 ar vėlesnę ir gaunu tolesnį klaidos pranešimą vykdydamas pagrindinį planavimą. Ar pagrindinis planavimas blokuojamas?

> Gaunate tolesnį klaidos pranešimą, nes sukurtas pagrindinis planavimo variklis buvo naudojamas scenarijų metu, kuriuos palaikė „Planning Optimization“. Turite perkelti į „Planning Optimization“ dabar, nes esamas sukurtas pagrindinis planavimas nebegalios. Atminkite, kad šis pagrindinio planavimo vykdymas sėkmingai baigtas.
>
> Jei perkėlimas turi stiprius priklausinius nuo esamų funkcijų, išlyga, kuria bus tęsiamas sukurtų pagrindinio planavimo variklio naudojimas gali būti prašomas.
>
> Prašome užbaigti tolesnį klausimyną, kad pradėtumėte ir jei būtina užklausos išlygą iš migravimo turi būti perkelta į „Planning Optimization“.

**Atsakymas:** Ne, pagrindinis planavimas neblokuojamas. Jūsų pagrindinis planavimo vykdymas sėkmingai baigtas ir galite naudoti rezultatus įprastu būdu. Nepaisant to, siekiant išvengti šios klaidos pranešimo funkcijos pagrindinio planavimo vykdymo metu, turite perkelti į „Planning Optimization“ nedelsiant arba prašyti išlygos naudodami nuorodą klaidos pranešime.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]