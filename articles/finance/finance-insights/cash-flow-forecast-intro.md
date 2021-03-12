---
title: Grynųjų pinigų srautų prognozė (peržiūros versija)
description: Šioje temoje aprašoma priemonė Grynųjų pinigų srautų prognozavimas.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 0df58d3571b124acbd1edbc6d6acdd49479c309e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990594"
---
# <a name="cash-flow-forecast-preview"></a>Grynųjų pinigų srautų prognozė (peržiūros versija)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Grynųjų pinigų srautai yra labai svarbūs bet kuriai įmonei. Net pelningos įmonės gali susidurti su nemokumu, jei jos neprižiūri grynųjų pinigų srautų, kurie patenkina neatidėliotinus poreikius. Modulio Finansinės įžvalgos grynųjų pinigų srautų prognozavimo priemonė gali padėti įmonėms efektyviai stebėti ir tvarkyti savo grynųjų pinigų balansus. Ši funkcija naudoja mašininį mokymą, kad padėtų įmonėms prognozuoti grynųjų pinigų srautus tiksliau nei anksčiau. Ji taip pat gali padėti vadovams priimti sprendimus, optimizančius galimybes, susijusias su dabartine grynųjų pinigų padėtimi. 

Daugumai įmonių grynųjų pinigų srautų valdymas ir pinigų srautų prognozavimo vykdymas yra varginantis, pasikartojantis ir neautomatizuotas procesas. Dauguma įmonių naudoja „Microsoft Excel“ sprendimus, kurių sudėtingumo laipsnis skirtingas. Norint tiksliai prognozuoti grynųjų pinigų srautus, kyla tolesnių iššūkių.

- Duomenys nepasiekiami sprendimų priėmėjams, nes jie yra išsibarstę keliose vietose, įskaitant nurodytas toliau. 
  - Apskaitos arba įmonės išteklių planavimo sistema
  - Finansinio planavimo programinė įranga
  - Excel
  - Papildomos programinės įrangos programos 
- Prognozavimas paremtas vidinėmis žiniomis, esančiomis atskirose kiekvieno domeno ar padalinio srityse.
- Grynųjų pinigų srautų prognozavimo tikslumo vertinimas po to, kai finansiniai duomenys jau realizuoti, yra neaišku ir sunkus procesas.
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a>Priemonįs Grynųjų pinigų srautų prognozės informacija
Priemonė Grynųjų pinigų srautų prognozės apima tolesnes funkcijas. 

- Leidžia lengvai integruoti grynųjų pinigų srautų duomenis iš išorinių sistemų į „Dynamics 365 Finance“. Pinigų srautų prognozėms taip pat gali būti naudojama duomenų importavimo-eksportavimo sistema. Ši sistema leidžia lengvai integruoti su „Excel“ „OData“. Taip pat galite sujungti duomenis iš kelių šaltinių, kad sukurtumėte išsamų grynųjų pinigų srautų sprendimą. 

- Įdiegiama sumanios grynųjų pinigų padėties funkcija. Grynųjų pinigų padėtis sukuriama remiantis kliento mokėjimo būdu, siekiant numatyti, kada įmonė gali tikėtis, kad sąskaitoje atsiras grynųjų pinigų. Ji taip pat analizuoja istorinius mokėjimo tiekėjų modelius, kad būtų galima prognozuoti, kada bus apmokamos būsimos SF ir užsakymai. 

- Įdiegiama sumanaus ilgalaikio grynųjų pinigų srautų prognozavimo funkcija, naudojanti laiko serijos prognozavimą per automatinę integraciją su „AI Builder“.

- Suteikia galimybę įrašyti konkrečią grynųjų pinigų srauto padėtį ar prognozes, jas redaguoti, tada lengvai palyginti ir išmatuoti prognozavimo našumą su faktiniais finansiniais rodikliais.

- Suteikia galimybę naudoti sąlyginę analizę, lyginant momentines kopijas. Pavyzdžiui, galite sukurti kelias momentines kopijas, kurios rodo optimistinį, pesimistinį ir realistiškiausią jūsų grynųjų pinigų srauto rodinius, o tada juos palyginti ir peržiūrėti skirtumus.

- Suteikia galimybę peržiūrėti grynųjų pinigų srautų prognozę keliomis valiutomis, visuose juridiniuose subjektuose ir filtruoti bei peržiūrėti grynųjų pinigų srautą, susijusį su tam tikra banko sąskaita. 

- Leidžia filtruoti ir peržiūrėti banko sąskaitas, susijusias su finansinėmis dimensijomis.

Grynųjų pinigų srautų prognozavimo funkcija programoje „Dynamics 365 Finance“ suteiks jūsų organizacijai galimybę transformuoti varginantį, sudėtingą ir pasikartojantį grynųjų pinigų srautų prognozavimą į paprastą, automatizuotą procesą. Automatizuojant labiausiai varginančius grynųjų pinigų srautų prognozavimo aspektus, galima sutelkti dėmesį į svarbių sprendimų priėmimą siekiant norimų verslo rezultatų.

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Grynųjų pinigų srautų prognozavimo dimensijų nustatymas
Naujas skirtukas puslapyje **Grynųjų pinigų srautų prognozavimo sąranka** leidžia kontroliuoti, kokios finansinės dimensijos gali būti naudojamos filtruojant darbo sritį **Grynųjų pinigų srautų prognozavimas**. Šis skirtukas bus rodomas tik tada, kai bus įjungta funkcija Grynųjų pinigų srautų prognozės. 

Skirtuke **Dimensijos** pasirinkite iš dimensijų, kurias naudosite filtruodami, sąrašo ir naudokite rodyklių klavišus, kad perkeltumėte jas į dešinįjį stulpelį. Grynųjų pinigų srautų prognozavimo duomenims filtruoti galima pasirinkti tik dvi dimensijas. 

#### <a name="privacy-notice"></a>Privatumo pranešimas
Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.
