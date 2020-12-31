---
title: Tiekėjo mokėjimų darbo sritis
description: Šioje temoje pateikiama informacijos apie tiekėjų mokėjimo darbo sritį. Tiekėjų mokėjimo darbo srityje rodoma informacija, susijusi su tiekėjų mokėjimo apdorojimu.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymentWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 39a9ba54ba26db5904c2cd519be9f83bbc68c037
ms.sourcegitcommit: 30c541426cf2037b768e3556e1b170a64991f64a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/17/2020
ms.locfileid: "4446165"
---
# <a name="vendor-payments-workspace"></a>Tiekėjo mokėjimų darbo sritis

[!include [banner](../includes/banner.md)]

**Tiekėjų mokėjimo** darbo srityje rodoma informacija, susijusi su tiekėjų mokėjimo apdorojimu. Šioje darbo srityje yra rodinys **Mano darbas** ir puslapis **Analizė**. **Mano darbo** rodinyje rodomos suvestinės plytelės, tiekėjų operacijų tinkleliai ir susijusi tiekėjų informacija. Puslapyje **Analizė** naudojantis „Microsoft Power BI“ galimybėmis parodomi su tiekėjų mokėjimais susiję vaizdiniai elementai.

## <a name="setup-needed-to-view-power-bi-content"></a>Norint peržiūrėti „Power BI“ turinį reikia atlikti sąranką

Norint, kad duomenys būtų rodomi „Power BI“ srities **Tiekėjo mokėjimai** vaizdiniuose elementuose, reikia atlikti tolesnę sąranką.
1. Eikite į **Sistemos administravimas > Sąranka > Sistemos parametrai** ir nustatykite **Sistemos valiuta** ir **Sistemos valiutos kursas**.
2. Eikite į **Didžioji knyga > Kalendoriai > Fiskaliniai kalendoriai** tam, kad patvirtintumėte fiskalinio kalendoriaus datas priskirtas aktyviam laikotarpiui.
3. Norėdami nustatyti parinktis **Apskaitos valiuta** ir **Valiutos kurso tipas** eikite į **Didžioji knyga > sąranka >DK**. 
4. Nustatykite valiutų keitimo kursus tarp perlaidų valiutų ir apskaitos valiutos bei apskaitos valiutos ir sistemos valiutos. Norėdami tai padaryti, eikite į **Didžioji knyga > Valiutos > Valiutų kursai**.
5. Norėdami atnaujinti agreguotą matavimo vienetą **VendPaymentBIMeasureV2** eikite į **Sistemos administravimas > Sąranka > Objektų saugykla**.

## <a name="my-work-view"></a>Mano darbo rodinys

### <a name="summary-tiles"></a>Suvestinės išklotinės

Plytelės skyriuje **Suvestinė** suteikia mokėjimo informacijos būsenos apžvalgą. Galite matyti dar neužregistruotus mokėjimo žurnalus, vėluojančias SF, visus tiekėjus ir sulaikytus tiekėjus. Skyriuje **Suvestinė** galite sukurti naują mokėjimų apdorojimą.

Skyriuje **Suvestinė** pateikiama įmonės, prie kurios esate prisijungę, informacija.

### <a name="vendor-transactions-grids"></a>Tiekėjų operacijų tinkleliai

Skyriuje **Tiekėjų operacijos** yra tinkleliai, kuriose rodomos vėluojančios SF ir neatlikti mokėjimai. Tinklelyje **Vėluojančios SF** galite peržiūrėti pasirinktos SF sudengimo retrospektyvą. Tinklelyje **Mokėjimai nesudengti** galite peržiūrėti pasirinktos SF sudengimo retrospektyvą ir sudengti SF.

Centralizuotų mokėjimų tarnautojai gali naudoti filtrą, kuris pasirodo kiekvieno tinklelio viršuje, kad būtų galima pasirinkti įmonę. Tada tinklelis atfiltruojamas taip, kad būtų rodomos tik įmonės, kurios apibrėžtos centralizuotų mokėjimų organizacijos hierarchijoje, kurią centralizuotų mokėjimų tarnautojas turi teisę peržiūrėti.

Skyriaus **Tiekėjų operacijos** skirtuke **Rasti operacijas** galite ieškoti tiekėjo operacijos.

### <a name="related-information"></a>Susijusi informacija

Galite peržiūrėti **Tiekėjų skirstymo pagal terminus** ataskaitą ir **Mokėjimų suvestinės pagal datą** ataskaitą naudodami darbo srities skyriaus **Susijusi informacija** saitus.

## <a name="analytics-page"></a>Analizės puslapis

Puslapyje **Analizė** pateikiamos svarbios metrikos, pvz., vėluojančios tiekėjo SF ir tiekėjo SF, kurios vėluos ateityje. Šiame puslapyje yra devyni ataskaitos puslapiai. Viename puslapyje pateikiama apžvalga, o kituose aštuoniuose puslapiuose pateikiama informacija apie mokėtinų sumų mokėjimo metriką.

Toliau pateikiamoje lentelėje nurodyti kiekviename ataskaitos puslapyje pateikiami vaizdai.


|            Ataskaitų puslapis            |                                                                                                                                                                                Vizualizacija                                                                                                                                                                                |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Tiekėjo mokėjimų peržiūra      | <ul><li>SF, kurių terminas praėjęs</li><li>Šiandien apmokėtinos SF</li><li>Pritaikytos nuolaidos ir prarastos nuolaidos</li><li>Ateities SF pagal mokėjimo nuolaidos datą</li><li>Ateities SF pagal terminą</li><li>Pavėluotai apmokėtos SF ir laiku apmokėtos SF</li><li>Mokėjimo darbo srauto priskyrimas</li><li>Tiekėjo ir kliento balansas</li><li>Atidaryti SF su sulaikytu mokėjimu</li></ul> |
|         SF, kurių terminas praėjęs         |                                                                                             <ul><li>SF, kurių terminas praėjęs</li><li>Vėluojančių SF informacija</li><li>Visos atviros SF</li><li>Vėluojančios SF pagal tiekėjų grupę</li><li>Vėluojančios SF pagal įmonę</li></ul>                                                                                              |
|        Šiandien apmokėtinos SF         |                                                                                                         <ul><li>Šiandien apmokėtinos SF</li><li>Šiandien apmokėtinų SF informacija</li><li>Šiandien apmokėtinos SF pagal įmonę</li><li>Šiandien apmokėtinos SF pagal tiekėjų grupę</li></ul>                                                                                                          |
| Pritaikytos nuolaidos ir prarastos nuolaidos |                                                                             <ul><li>Pritaikytos nuolaidos ir prarastos nuolaidos</li><li>Pritaikytų nuolaidų ir prarastų nuolaidų informacija</li><li>Pritaikytos nuolaidos ir prarastos nuolaidos pagal įmonę</li><li>Pritaikytos nuolaidos ir prarastos nuolaidos pagal tiekėjų grupę</li></ul>                                                                              |
|      Ateityje apmokėtinos SF       |                                                 <ul><li>Ateityje apmokėtinos SF</li><li>Ateityje apmokėtinų SF informacija</li><li>Ateityje apmokėtinos SF pagal įmonę</li><li>Ateityje apmokėtinos SF pagal tiekėjų grupę</li><li>Ateities SF pagal mokėjimo nuolaidos datą</li><li>Ateities SF pagal terminą</li></ul>                                                  |
|        Vėlai apmokėtos SF         |                                                         <ul><li>SF, apmokėtos praėjus terminui</li><li>SF, apmokėtų praėjus terminui, informacija</li><li>SF, apmokėtos praėjus terminui pagal įmonę</li><li>SF, apmokėtos praėjus terminui pagal tiekėjų grupę</li><li>Pavėluotai apmokėtos SF ir laiku apmokėtos SF</li></ul>                                                          |
|         Mokėjimo darbo eiga          |                                                                                <ul><li>Tiekėjo mokėjimo darbo eigos egzemplioriai</li><li>Tiekėjo mokėjimo darbo eigos egzemplioriai pagal tvirtintoją</li><li>Tiekėjo mokėjimo darbo eigos egzemplioriai pagal įmonę</li><li>Vidutinis darbo eigos dienų skaičius pagal tvirtintoją</li></ul>                                                                                |
|    Tiekėjo ir kliento balansas     |                                                                                                                   <ul><li>Tiekėjo ir kliento balansas</li><li>Tiekėjo ir kliento balansas pagal įmonę</li><li>Tiekėjo ir kliento balanso informacija</li></ul>                                                                                                                    |
|    SF su sulaikytu mokėjimu     |                                                                                         <ul><li>SF su sulaikytu mokėjimu</li><li>SF su sulaikytu mokėjimu informacija</li><li>SF su sulaikytu mokėjimu pagal įmonę</li><li>SF su sulaikytu mokėjimu pagal tiekėjų grupę</li></ul>                                                                                          |

