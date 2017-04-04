---
title: "Kaina kontroliuoti mobiliojo darbo srities Microsoft Dynamics &quot;365&quot; veiksmų programos"
description: "Su išlaidomis kontroliuoti mobiliojo ryšio darbo sritį, išlaidų centrų vadovų galite pamatyti išlaidų centras bet kada ir bet kur."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 53 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 84740472-494f-444c-9b74-f83b7342fd25
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 8136efb1d2669c39fcc0f80b60e80ecae983d5d8
ms.lasthandoff: 03/31/2017


---

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Kaina kontroliuoti mobiliojo darbo srities Microsoft Dynamics "365" veiksmų programos

Su išlaidomis kontroliuoti mobiliojo ryšio darbo sritį, išlaidų centrų vadovų galite pamatyti išlaidų centras bet kada ir bet kur. 

<a name="prerequisites"></a>Būtinieji komponentai
-------------

| Būtinoji sąlyga                                                         | aprašymas                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Skaityti apie Microsoft Dynamics 365 operacijų mobiliųjų platformų | [Dinamika 365 operacijų mobiliųjų platformų](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dinamika 365 operacijoms                                          | Įsitikinkite, kad naudojate aplinkoje, kuri yra Microsoft Dynamics 365 operacijų versija 1611 ir "Microsoft Dynamics" operacijų platformos naujinimas 3 (2016 m lapkričio mėn.). |
| Karštosios pataisos KB 3215650                                                    | Įdiekite karštąją pataisą norite įgalinti darbo sritys, kurios yra teikiamos Microsoft Dynamics 365 operacijoms.                                                                       |
| Mobiliojo įrenginio, turinčio Dynamics 365 dėl operacijų taikomąją programą | Atsisiųskite Dynamics 365 operacijų App iš mobiliųjų programėlių parduotuvėje.                                                                                                      |

## <a name="introduction"></a>Įžanga
Kontroliuoti mobiliojo darbo srities išlaidas siūlo momentinių atsižvelgiant, dabartinę veiklą ir išlaidų centrai lyginant faktines išlaidas nuo biudžete numatytoms išlaidoms. Jūs galite išgręžti iki atskirų išlaidų elementų būsenas.

### <a name="example"></a>Pavyzdys

Darbuotojas gauna kvietimą į tarptautinę konferenciją. Organizacijos turės padengti visas kelionės išlaidas. Darbuotojas prašo jo ėdžiose, jei jis gali dalyvauti konferencijoje. Vadybininkas greitai atidaro išlaidas kontroliuoti mobiliojo darbo srities į savo mobilųjį telefoną pamatyti, ar jis nebuvo biudžeto darbuotojo dalyvauti konferencijoje.

### <a name="data-security"></a>Duomenų sauga

Išlaidas kontroliuoti darbo srities duomenys yra užpatentuotas vartotojo kredencialus. Išlaidų centro vadovui leidžiama tik pamatyti duomenis savo išlaidų centrą. Prieigos lygio saugumo funkcijas sąnaudų apskaitos modulis. Kaina buhalterių apibrėžti kontroliuoti mobiliojo darbo srities konfigūravimas kaštų apskaitos modulio kaina. Paskelbus darbo srities Microsoft Dynamics 365 veiklos programą, tai galima Dynamics "365" mobiliesiems operacijas. Tai užtikrina, kad visi išlaidų centro vadovai organizacijoje pažvelgti į duomenis tuo pačiu formatu.

### <a name="actions-views-and-links"></a>Veiksmus, vaizdai ir nuorodos

Išlaidas kontroliuoti mobiliojo darbo srities Dynamics "365" veiksmų programos numato tokius veiksmus, vaizdai ir nuorodos:

-   Veiksmai 
    -   Pasirinkite **konfigūracijos** paimti maketą.
    -   Pasirinkite **išlaidų objektus** pasirinkti išlaidų centrai, kurią norite filtruoti duomenis. **Pastaba:** sąrašas pateikiamas pagal kaštų apskaitos modulio suteikta teisė susipažinti.

<!-- -->

-   Atsižvelgiant į tai, kas pasirinkta pagal **veiklos** ir kas yra sukonfigūruotas kaštų apskaitos modulio, galite peržiūrėti šią informaciją kortelės. Atkreipkite dėmesį, kad suma rodoma to paties formato: tikrasis, biudžetas, nuokrypis ir dispersija %. 
    -   Realių ir įvertintųjų biudžeto (ataskaitinio laikotarpio)
    -   Realių ir įvertintųjų pataisytas biudžetas (ataskaitinio laikotarpio)
    -   Realių ir įvertintųjų biudžeto (praėjusį laikotarpį)
    -   Realių ir įvertintųjų pataisytas biudžetas (praėjusį laikotarpį)
    -   Realių ir įvertintųjų biudžeto (metai iki datos)
    -   Realių ir įvertintųjų pataisytas biudžetas (metai iki datos)

<!-- -->

-   Saitai
    -   Ataskaitinio laikotarpio informacija.
    -   Ankstesnio laikotarpio duomenys.
    -   Detalių metų iki datos.

Pasirinkus vieną iš pateiktų nuorodų, yra rodomas kortelės už sąnaudų dalis. Kortelės suma yra rodomas tokiu formatu: tikrasis, biudžetas, biudžetas dispersija, biudžeto nuokrypis %, pataisytas biudžetas, pataisytas biudžetas dispersija ir pataisytas biudžetas nuokrypis %.  [![išlaidų kontrolė](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Darbo pradžia
Atlikite šiuos veiksmus Norėdami pradėti naudotis išlaidų kontrolės Mobilioji programėlė mobiliajame įrenginyje.

1.  Jūsų mobiliųjų įrenginių programėlę parduotuvėje, atsisiųskite ir įdiekite Microsoft Dynamics 365 veiklos programą.
2.  Paleiskite programėlę į savo įrenginį.
3.  Įveskite savo dinamika 365 URL.
4.  Įveskite prisijungti prie kompanijos. Pavyzdžiui, įveskite **USMF**.
5.  Pirmą kartą, kai prisijungsite, bus rodomas raginimas įvesti vartotojo vardą ir slaptažodį savo Microsoft Dynamics "365" veiklos sąskaita. Įvesti savo kredencialus. Po to, kai prisijungsite, matote laisvų darbo srities jūsų įmonė.

Norėdami peržiūrėti savo mobiliesiems darbo sričių, pirmiausia turi publikuoti norimą darbo srities dinamika 365 operacijų programos.

1.  Paleisti Dynamics 365 operacijoms.
2.  Eikite į **sistemos administravimo**&gt;**nustatymo**&gt;**sistemos parametrai**.
3.  Pasirinkite **tvarkyti mobiliųjų įrenginių programėlę**.
4.  Pasirinkite darbo sritį ** kaina kontroliuoti ** skelbti apie mobiliųjų platformų.
5.  Pasirinkite **skelbti darbo srities**.
6.  Atnaujinkite įrenginio paskelbtų darbo sritis.

## <a name="view-the-performance-of-your-cost-center"></a>Rodyti savo išlaidų centro veiklos
1.  Mobiliajame įrenginyje, pasirinkite pagal **išlaidų kontrolės** darbo srities.
2.  Pasirinkite **išlaidų objekto kontroliuoti**.
3.  Spustelėkite **veiklos**.
4.  Spustelėkite **pasirinkite konfigūracijos** pasirinkti išlaidų kontrolės išdėstymą.
5.  Spustelėkite **atlikti**.
6.  Spustelėkite **veiklos**.
7.  Spustelėkite **sąnaudų objektą** pasirinkti išlaidų centrai, prie kurių jums suteikta prieigos.
8.  Spustelėkite **atlikti**.
9.  Rodyti bendrą našumą jūsų išlaidų centrą.
10. Spustelėkite **detalių ataskaitinio laikotarpio**.
11. Rodyti atskirų išlaidų elementų veikimui.
12. Taip pat galite ieškoti konkrečių išlaidų elementai.



