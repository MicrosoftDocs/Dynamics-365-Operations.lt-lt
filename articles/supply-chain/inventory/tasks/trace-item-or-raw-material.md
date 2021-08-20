---
title: Prekės arba žaliavos sekimas
description: Ši procedūra parodo, kaip naudoti prekės sekimą ir identifikuoti, kur prekės arba žaliavos buvo naudojamos arba yra naudojamos.
author: sherry-zheng
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 01e945b94017dd95a43e0f089902ffd3ea1298ef230f84d9198031b30e323ef9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781931"
---
# <a name="trace-an-item-or-raw-material"></a>Prekės arba žaliavos sekimas

[!include [banner](../../includes/banner.md)]

Ši procedūra parodo, kaip naudoti prekės sekimą ir identifikuoti, kur prekės arba žaliavos buvo naudojamos arba yra naudojamos. Naudodami šią procedūrą, galite nustatyti prekę, atsekti jos šaltinį, tada perkelti ją į galutinio produkto gamybą ir pardavimą. Procesą galima naudoti norint ištirti paveiktus klientus, paveiktus pardavimo užsakymus ir kt. Šioje procedūroje naudojami demonstracinių duomenų įmonės USP2.


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a>Sekti prekę atgal, naudojant žinomą paketo numerį
1. **Naršymo srityje** eikite į **Moduliai > Atsargų valdymas > Sąranka > Užklausos ir ataskaitos > Sekimo dimensijos > Prekės sekimas**.
2. Lauke **Prekės numeris** pasirinkite P9100.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Lauke **Pirmyn arba atgal** pasirinkite Atgal.
5. Lauke **Paketo numeris** pasirinkite kaip-12-344-01.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Spustelėkite **Gerai**.

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a>Identifikuoti prekę, sekti ją į priekį ir atlikti analizę

Medžio aukščiausias mazgas nurodo pasirinktos prekės ir paketo turimų atsargų kiekį. Norėdami rasti prekę, kuriai turėtų būti vykdomas sekimas į priekį, turite išplėsti medžio mazgus.   
1. Medyje išplėskite toliau aprašytus mazgus ir pasirinkite paskutinį mazgą.
    
    Išplėskite: „P9100 / 1 / 10 / as-12-344-01 ● 2 statinės ● 7,00 gal \P9100 ● Paimta ● Pardavimo užsakymas 000072 ● 2015-12-22 ● -1 statinė ● -4,00 gal ● Vieta=1, Sandėlis=10, Paketo numeris=as-12-344-01 \P9100 ● Gamyba B-000050 ● 2015-12-09● 7 statinės ● 27,00 gal ● Vieta=1,Sandėlis=10,Paketo numeris=as-12-344-01 ● Sudėtiniai produktai: P9101‟ ir pasirinkite tą mazgą.     
2. Medyje išplėskite toliau aprašytą mazgą ir tą mazgą pasirinkite.
    
    Pradėkite nuo ką tik pasirinkto mazgo, išplėskite „M9103“ ● Gamybos linija B-000050 ● 2015-09-12 ● -160,00 lb ● Dydis = 70, Spalva = Gerai, Vieta = 1, Sandėlis = 10, Paketo numeris = „App01“ ir pasirinkite tą mazgą.  
3. Spustelėkite **Sekti nuo mazgo**.
4. Spustelėkite **Pirmyn**.
5. **Veiksmų srityje** spustelėkite **Sekimas**.
    
    Yra keletas sekimo parinkčių, teikiančių informaciją apie klientus, kuriuos paveikė jūsų sekama prekė, ir su prekėmis susijusius užsakymus, kurie buvo ir nebuvo išsiųsti.   
6. Spustelėkite **Klientai**.
7. Uždarykite puslapį.
8. **Veiksmų srityje** spustelėkite **Sekimas**.
9. Spustelėkite **Išsiųsti pardavimo užsakymai**.
10. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]