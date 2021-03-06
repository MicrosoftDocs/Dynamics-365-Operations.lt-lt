---
title: „Attract“ išplečiamumas
description: Šioje temoje aprašoma, kaip naudodami „Microsoft Power Platform“ galite išplėsti „Microsoft Dynamics 365 Talent - Attract“.
author: andreabichsel
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ddc6593431585ed79cc15f7ede5daf856f11b959
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527247"
---
# <a name="extensibility-in-attract"></a>„Attract“ išplečiamumas

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

„Microsoft Dynamics 365 Talent“ sukurta kaip „Common Data Service“ papildas ir ją galima išplėsti naudojantis „Microsoft Power Platform“ ir „Common Data Service“ siūlomomis galimybėmis. Todėl sistemą galite konfigūruoti ir pritaikyti asmeniniam poreikiams naudodami „Microsoft Power Apps“ ir „Microsoft Power Automate“. Taip pat naudodamiesi „Microsoft Power BI“ galite gauti papildomų analitinių duomenų apie žmones. Be to, naudojantis naujomis pasirinktinėmis veiklomis, pvz., „Power Apps“ ir interneto turinio („iframe“) veiklomis, samdos procesas gali būti daug lengviau pritaikomas nei bet kada. Naudodamiesi šiomis veiklomis samdos procesą galite pritaikyti pagal savo verslo poreikius ir procesus, taip pat galite būti tikri, kad samdos komanda ir kandidatai turi atitinkamos nuoseklios patirties.

## <a name="extending-option-sets-in-attract"></a>„Attract“ parinkčių rinkinių išplėtimas

**Parinkčių rinkinys** (išrinkimo sąrašas) yra lauko, kurį galima įtraukti į objektą, tipas. Jis apibrėžia parinkčių rinkinį. Kai formoje rodomas parinkčių rinkinys, jis naudoja išplečiamojo sąrašo valdiklį.  „Attract“ yra daug laukų, kurie yra parinkčių rinkiniai.  Pradedame pristatyti galimybę išplėsti parinkčių rinkinius, pradedant nuo laukų Atmetimo priežastis, Įdarbinimo tipas ir Stažo tipas.   Taip pat galite įtraukti lokalizuotas ekrano žymes, skirtas parinktims, kurias norite įtraukti. Daugiau informacijos rasite [Parinkčių rinkinių žymių tinkinimas](https://docs.microsoft.com/powerapps/developer/common-data-service/customize-labels-support-multiple-languages).

> [!NOTE]
> Norint naudoti darbo registravimo „LinkedIn“ funkciją, reikalingi puslapio **Darbo informacija** laukai **Įdarbinimo tipas** ir **Stažo tipas**. Numatytąsias šių laukų reikšmes palaiko „LinkedIn“ ir jos rodomos, kai darbas registruojamas. Todėl, jei registruojate darbus „LinkedIn“ ir modifikuojate esamas tų laukų parinkčių rinkinių reikšmes, darbas bus užregistruotas, bet „LinkedIn“ nerodys pasirinktinių laukų **Įdarbinimo tipas** ir **Stažo tipas** reikšmių.  

Toliau nurodyti veiksmai, kuriuos atlikę galite nurodyti lauko **Atmetimo priežastis** reikšmes, atsižvelgdami į savo įmonę.  

1. Norėdami išplėsti parinkčių rinkinį **Atmetimo priežastis**, atidarykite [„Power Apps“ administravimo svetainę](https://admin.powerapps.com).
2. Jūs būsite paraginti prisijungti prie savo paskyros. Pateikti savo vartotojo ID ir slaptažodžio kredencialus, kuriuos naudodami prisijungiate prie „Dynamics365“ ir (arba) „Office365“, tada spustelėkite **Toliau**.
3. Skirtuke **Aplinkos** pasirinkite aplinką, kurį norite valdyti, ir dukart spustelėkite, kad atidarytumėte skirtuką **Informacija**.
4. Skirtuke **Informacija** pasirinkite **„Dynamics 365“ administravimo centras**.
5. Pasirinkite egzempliorių, kurį norite keisti, ir pasirinkite **Atidaryti**.
6. Pasirinkite **Parametrai**, tada – **Tinkinimai**, tada pasirinkite **Tinkinti sistemą**.
7. Raskite objektą, kurio parinkčių rinkinį norite išplėsti, pasirinkdami parinktį **Objektai** ir išplėsdami grupę. Šiame pavyzdyje tai bus **Prašymo įdarbinti objektas**.
8. Atidarykite lauką, kurio parinkčių rinkinį norite išplėsti, pasirinkdami parinktį **Laukai**. Šiame pavyzdyje tai bus **msdyn_rejectionreason**. Dukart spustelėkite lauką.
9. Lauke **Parinkčių rinkinys** pasirinkite **Redaguoti**.
10. Pasirinkite piktogramą **+**.
11. Įveskite reikšmę lauke **Žymė**.  (Tai turi būti unikali reikšmė – jokių dublikatų).
12. Pasirinkite **Įrašyti**.
13. Puslapio viršuje pasirinkite **Publikuoti**.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Pasinaudokite „Microsoft Power Platform“ 

Kadangi visi duomenys iš „Attract“ laikomi „Common Data Service“, naudodamiesi „Microsoft Power Platform“ įrankiais galite įtraukti unikalius savo verslo poreikius į „Attract“.

### <a name="power-apps"></a>„Power Apps“

Naudojantis „Power Apps“ paprasta kurti prie „Attract“ duomenų prisijungiančias programas, taip pat programas, kurios, naudodamos panašias į „Microsoft Excel“ išraiškas, įtraukia logiką. Naudojant „Power Apps“ sukurtas programas galima paleisti žiniatinklyje, „Apple iOS“ ir „Google Android“ įrenginiuose.

Pavyzdžiui, galite sukurti supaprastintą programą, kuria naudodamiesi darbaviai gali peržiūrėti CV ir priskirti kandidatams atitinkamas „Attract“ nurodytas pareigas – tokiu būdu universiteto karjeros mugės jiems tampa paprastesnės. Arba galite sukurti programą, kuri padėtų įgyvendinti jūsų organizacijos atitikties reikalavimus. Daugiau informacijos apie „Power Apps“ ir apie tai, kaip ja naudojantis kurti programas, ieškokite [Duomenų integravimas į „Common Data Service“](https://docs.microsoft.com/powerapps).

### <a name="microsoft-power-automate"></a>„Microsoft Power Automate“ 

Galite naudoti „Power Automate“, kad sukurtumėte automatines darbo eigas, veikiančias ant „Attract“ duomenų viršaus. Paprasta prijungti prie šimtų populiarių programų ir paslaugų, kadangi nereikia rašyti kodo. Sukurdami eigas, kurios sąveikauja su „Common Data Service“ „Attract“ objektais Pareigos, Kandidatas ir Pareiškimas, galite automatizuoti įvairius veiksmus. Pavyzdžiui, kai kandidatas priima pasiūlymą, galima nusiųsti pranešimą supažindinimo komandai arba apie tai galima paskelbti „Twitter“. Daugiau informacijos apie srautus žr. [„Microsoft Power Automate“ dokumentai](https://docs.microsoft.com/flow/).

### <a name="power-bi"></a>„Power BI‟

Naudodamiesi „Power BI“ galite kurti ir peržiūrėti pasirinktines ataskaitas ir ataskaitų sritis, kad geriau suprastumėte savo „Attract“ duomenis. Daugiau informacijos apie „Power BI“ ir apie tai, kaip sukurti interaktyvias ataskaitas ir ataskaitų sritis, ieškokite [„Power BI“ dokumentacijoje](https://docs.microsoft.com/power-bi/).

### <a name="custom-activities"></a>Pasirinktinės veiklos 

Galite įtraukti pasirinktinių veiklų, pvz., „Power Apps“ programų ir žiniatinklio turinio („iframe“) veiklų (pareigų proceso šablono lygiu arba kuriant naujas pareigas). Naudodamiesi šiomis veiklomis galite pritaikyti samdos procesą ir į „Attract“ įtraukti unikalią savo organizacijos verslo logiką.

#### <a name="power-apps-activity"></a>„Power Apps“ veikla 

Naudodamasis „Power Apps“, pareigų arba pareigų proceso šablono kūrėjas gali įterpti „Power Apps“ programą į samdos eigą. Sukūrę ir išleidę programą, atlikdami veiklos konfigūracijas galite įvesti šios programos ID. Naudodamiesi „Power Apps“ programa, galite skaityti ir rašyti duomenis į „Common Data Service“. Netgi galite susieti programą su eiga. Pavyzdžiui, turite programą, kuria naudodamiesi darbdaviai, vykstant telefoniniam pokalbiui dėl darbo, užpildo formą. Tokiu atveju programą galite susieti su tokia eiga, kurios metu įvertinama, ar pretendentas gali būti perkeliamas į kitą kandidatavimo į pareigas proceso etapą. Šio tipo veiklą gali peržiūrėti tik samdos komandos nariai. Daugiau informacijos apie tai, kaip konfigūruoti „Power Apps“ veiklą, žr. [Įdarbinimo procesų veiklos](./activities-attract.md).

> [!NOTE]
> „Power Apps“ veiklą galima naudoti tik kartu su išsamios įdarbinimo informacijos priedu.

#### <a name="web-content-iframe-activity"></a>Žiniatinklio turinio („iframe“) veikla

Naudodamiesi žiniatinklio turinio („iframe“) veikla galite įterpti vykstant samdos procesui arba kandidato portale sukurtą pasirinktinį žiniatinklio sprendimą. Duomenis skaityti ir rašyti galite tiesiogiai iš „Common Data Service“. Taip pat galite tinkinti sprendimą taip, kad jis suaktyvintų eigas arba naudotųsi „Microsoft Azure“ funkcijomis. Daugiau informacijos apie tai, kaip konfigūruoti žiniatinklio veiklos turinį, žr. [Įdarbinimo procesų veiklos](./activities-attract.md).

> [!NOTE]
> Žiniatinklio turinio veiklą galima naudoti tik kartu su išsamios įdarbinimo informacijos priedu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]