---
title: "Amortizuoti pastovias išlaidas pagamintai prekei"
description: "Gamintojo prekės pastovios išlaidos rodo operacijos nustatymo laikus ir komponentus, turinčius pastovų kiekį arba pastovią nurašymų sumą."
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 1f849e05a6d68cbfb95849ad6e8b34c599716c50
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a>Amortizuoti pastovias išlaidas pagamintai prekei

[!include[banner](../includes/banner.md)]


Gamintojo prekės pastovios išlaidos rodo operacijos nustatymo laikus ir komponentus, turinčius pastovų kiekį arba pastovią nurašymų sumą. 

Įkainojimo partijos dydžio sąvoka naudojama amortizuoti šias pastovias išlaidas pagamintos prekės apskaičiuotose išlaidose. Ši sąvoka turi keletą sinonimų, vienas iš kurių – apskaitos partijos dydis. Amortizuojamų pastovių išlaidų sąvoka taip pat turi keletą sinonimų, vienas iš kurių – proporcinės pastovios išlaidos.
Pagamintos prekės įkainojimo partijos dydžio kiekis naudojamas komplektavimo specifikacijai (KS) skaičiuoti. Kiekis priklauso nuo KS skaičiavimo inicijavimo ir atlikimo, kaip pateikta toliau:
-   Prekės KS skaičiavimo numatytasis skaičiavimo kiekis – prekės standartinis atsargų užsakymo kiekis veikia kaip įkainojimo partijos dydis, tačiau numatytoji reikšmė gali būti didesnis kiekis, kad atspindėtų prekės užsakymo sudėtinį kiekį. Prekės standartinis užsakymo kiekis ir sudėtinis kiekis gali būti nustatomi savo numatytuose užsakymo parametruose arba nuo teritorijos priklausomuose užsakymo parametruose.
-   Nurodytas skaičiavimo kiekis skaičiuojant prekės KS  – nurodytas skaičiavimo kiekis yra prekės įkainojimo partijos dydis. Skaičiavimo kiekis iš pradžių naudoja prekės standartinio užsakymo kiekį, tačiau numatytoji reikšmė gali būti panaikinama rankiniu būdu. Nurodytas skaičiavimo kiekis rodo nurodytos prekės ir pagamintų komponentų, turinčių gamybos KS eilutės tipą, įkainojimo partijos dydį. Tai svarbu, nes laikoma, kad komponentas bus pagamintas tiksliu kiekiu. Kitų pagamintų komponentų, turinčių prekės KS eilutės tipą, įkainojimo partijos dydis parodys jų standartinį užsakymo kiekį.
-   Nurodytas gamybos pagal užsakymą skaičiavimo kiekis skaičiuojant prekės KS − nurodytas skaičiavimo kiekis yra prekės ir jos pagamintų komponentų įkainojimo partijos dydis, kai KS skaičiavimai naudoja gamybos pagal užsakymą išskleidimo režimą. Laikoma, kad pagaminti komponentai bus gaminami tiksliu kiekiu, kaip ir pagamintas komponentas, turintis gamybos KS eilutės tipą.
-   Nustatytas skaičiavimo kiekis skaičiuojant būdingą užsakymui KS − būdingo užsakymui KS skaičiavimas gali būti atliekamas pardavimo užsakymo, pardavimo pasiūlymo arba aptarnavimo užsakymo eilutės elementui. Nurodytas skaičiavimo kiekis naudoja pradinio eilutės elemento kiekį, tačiau numatytojo kiekio galima nepaisyti. Galite pasirinkti, ar būdingas užsakymui KS skaičiavimas naudos gamybos pagal užsakymą, ar daugialygmenį išskleidimo režimą.

Pagamintos prekės amortizuotų pastovių išlaidų apskaičiuota suma laikoma išlaidomis.






