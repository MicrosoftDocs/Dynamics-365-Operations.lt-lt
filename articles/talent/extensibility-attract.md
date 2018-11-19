---
title: "„Attract“ išplečiamumas"
description: "Šioje temoje aprašoma, kaip naudodami „Microsoft Power Platform“ galite išplėsti programą „Microsoft Dynamics 365 for Talent - Attract“."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 0af60a0aea0f7a5de793631445aaebb37dbb0d74
ms.contentlocale: lt-lt
ms.lasthandoff: 10/22/2018

---

# <a name="extensibility-in-attract"></a>„Attract“ išplečiamumas

[!include[banner](../includes/banner.md)]

„Microsoft Dynamics 365 for Talent“ sukurta kaip programoms skirtos paslaugos „Common Data Service (CDS)“ platformos papildas ir ją galima išplėsti naudojantis „Microsoft Power Platform“ ir programoms skirtos paslaugos „Common Data Service“ siūlomomis galimybėmis. Todėl galite konfigūruoti ir pritaikyti sistemą (naudodamiesi „Microsoft PowerApps“ ir „Microsoft Flow“). Taip pat naudodamiesi „Microsoft Power BI“ galite gauti papildomų analitinių duomenų apie žmones. Be to, naudojantis naujomis pasirinktinėmis veiklomis, pvz., „PowerApps“ ir interneto turinio („iframe“) veiklomis, samdos procesas gali būti daug lengviau pritaikomas nei bet kada. Naudodamiesi šiomis veiklomis samdos procesą galite pritaikyti pagal savo verslo poreikius ir procesus, taip pat galite būti tikri, kad samdos komanda ir kandidatai turi atitinkamos nuoseklios patirties.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Naudojimasis „Microsoft Power Platform“ 

Kadangi visi duomenys iš „Attract“ laikomi programoms skirtoje paslaugoje „Common Data Service“, naudodamiesi „Microsoft Power Platform“ įrankiais galite įtraukti unikalius savo verslo poreikius į „Attract“.

### <a name="powerapps"></a>„PowerApps“

Naudojantis „PowerApps“ paprasta kurti prie „Attract“ duomenų prisijungiančias programas, taip pat programas, kurios, naudodamos išraiškas (pvz., „Microsoft Excel“ išraiškas), įtraukia logiką. Naudojantis „PowerApps“ sukurtas programas galima paleisti žiniatinklyje, „Apple iOS“ ir „Google Android“ įrenginiuose.

Pavyzdžiui, galite sukurti supaprastintą programą, kuria naudodamiesi darbaviai gali peržiūrėti CV ir priskirti kandidatams atitinkamas „Attract“ nurodytas pareigas – tokiu būdu universiteto karjeros mugės jiems tampa paprastesnės. Arba galite sukurti programą, kuri padėtų įgyvendinti jūsų organizacijos atitikties reikalavimus. Daugiau informacijos apie „PowerApps“ ir apie tai, kaip ja naudojantis kurti programas ieškokite [Duomenų integravimas į programoms skirtą „Common Data Service“](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>„Microsoft Flow“ 

Naudodamiesi „Microsoft Flow“ galite sukurti automatinių šalia „Attract“ duomenų veikiančių darbo eigų. Paprasta prijungti prie šimtų populiarių programų ir paslaugų, kadangi nereikia rašyti kodo. Sukurdami eigas, kurios sąveikauja su programoms skirtos „Common Data Service“ „Attract“ objektais Pareigos, Kandidatas ir Pareiškimas, galite automatizuoti įvairius veiksmus. Pavyzdžiui, kai kandidatas priima pasiūlymą, galima nusiųsti pranešimą supažindinimo komandai arba apie tai galima paskelbti „Twitter“. Daugiau informacijos apie eigas ieškokite [„Microsoft Flow“ dokumentacijoje](https://docs.microsoft.com/en-us/flow/).

### <a name="power-bi"></a>„Power BI‟

Naudodamiesi „Power BI“ galite kurti ir peržiūrėti pasirinktines ataskaitas ir ataskaitų sritis, kad geriau suprastumėte savo „Attract“ duomenis. Daugiau informacijos apie „Power BI“ ir apie tai, kaip sukurti interaktyvias ataskaitas ir ataskaitų sritis, ieškokite [„Power BI“ dokumentacijoje](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>Pasirinktinės veiklos 

Galite įtraukti pasirinktinių veiklų, pvz., „PowerApps“ programų ir žiniatinklio turinio („iframe“) veiklų (pareigų proceso šablono lygiu arba kurdami naujas pareigas). Naudodamiesi šiomis veiklomis galite pritaikyti samdos procesą ir į „Attract“ įtraukti unikalią savo organizacijos verslo logiką.

#### <a name="powerapps-activity"></a>„PowerApps“ veikla 

Naudodamasis „PowerApps“ veikla pareigų arba pareigų proceso šablono kūrėjas gali įterpti „PowerApps“ programą į samdos eigą. Sukūrę ir išleidę programą, atlikdami veiklos konfigūracijas galite įvesti šios programos ID. Naudodamiesi „PowerApps“ programa galite skaityti ir rašyti duomenis į programoms skirtą „Common Data Service“. Netgi galite susieti programą su eiga. Pavyzdžiui, turite programą, kuria naudodamiesi darbdaviai, vykstant telefoniniam pokalbiui dėl darbo, užpildo formą. Tokiu atveju programą galite susieti su tokia eiga, kurios metu įvertinama, ar pretendentas gali būti perkeliamas į kitą kandidatavimo į pareigas proceso etapą. Šio tipo veiklą gali peržiūrėti tik samdos komandos nariai. Daugiau informacijos apie tai, kaip sukonfigūruoti „PowerApps“ veiklą, ieškokite skyriuje [„Attract“ veiklos](./activities-attract.md).

> [!NOTE]
> „PowerApps“ veiklą galima naudoti tik kartu su išsamios įdarbinimo informacijos priedu.

#### <a name="web-content-iframe-activity"></a>Žiniatinklio turinio („iframe“) veikla

Naudodamiesi žiniatinklio turinio („iframe“) veikla galite įterpti vykstant samdos procesui arba kandidato portale sukurtą pasirinktinį žiniatinklio sprendimą. Duomenis skaityti ir rašyti galite tiesiogiai iš programoms skirtos „Common Data Service“. Taip pat galite tinkinti sprendimą taip, kad jis suaktyvintų eigas arba naudotųsi „Microsoft Azure“ funkcijomis. Daugiau informacijos apie tai, kaip sukonfigūruoti žiniatinklio turinio veiklą, ieškokite skyriuje [„Attract“ veiklos](./activities-attract.md).

> [!NOTE]
> Žiniatinklio turinio veiklą galima naudoti tik kartu su išsamios įdarbinimo informacijos priedu.

