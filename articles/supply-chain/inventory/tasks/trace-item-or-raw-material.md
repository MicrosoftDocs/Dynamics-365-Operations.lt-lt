---
title: "Prekės arba žaliavos sekimas"
description: "Ši procedūra parodo, kaip naudoti prekės sekimą ir identifikuoti, kur prekės arba žaliavos buvo naudojamos arba yra naudojamos."
author: pjacobse
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d7eb282ddf9597385d6660a3fc0ef73f403ab898
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="trace-an-item-or-raw-material"></a>Prekės arba žaliavos sekimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra parodo, kaip naudoti prekės sekimą ir identifikuoti, kur prekės arba žaliavos buvo naudojamos arba yra naudojamos. Naudodami šią procedūrą, galite nustatyti prekę, atsekti jos šaltinį, tada perkelti ją į galutinio produkto gamybą ir pardavimą. Procesą galima naudoti norint ištirti paveiktus klientus, paveiktus pardavimo užsakymus ir kt. Šioje procedūroje naudojami demonstracinių duomenų įmonės USP2.


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a>Sekti prekę atgal, naudojant žinomą paketo numerį
1. Pasirinkite Atsargų valdymas > Užklausos ir ataskaitos > Sekimo dimensijos > Prekės sekimas.
2. Lauke Prekės numeris pasirinkite P9100.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Lauke Į priekį arba atgal pasirinkite 'Atgal'.
5. Lauke Paketo numeris pasirinkite as-12-344-01.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Spustelėkite GERAI.

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a>Identifikuoti prekę, sekti ją į priekį ir atlikti analizę
    * Medžio aukščiausias mazgas nurodo pasirinktos prekės ir paketo turimų atsargų kiekį. Norėdami rasti prekę, kuriai turėtų būti vykdomas sekimas į priekį, turite išplėsti medžio mazgus.   
1. Medyje išplėskite toliau aprašytus mazgus ir pasirinkite paskutinį mazgą.
    * Išplėskite: „P9100 / 1 / 10 / as-12-344-01 ● 2 statinės ● 7,00 gal \P9100 ● Paimta ● Pardavimo užsakymas 000072 ● 2015-12-22  ● -1 statinė ● -4,00 gal ● Vieta=1, Sandėlis=10, Paketo numeris=as-12-344-01 \P9100 ● Gamyba B-000050 ● 2015-12-09● 7 statinės ● 27,00 gal ● Vieta=1,Sandėlis=10,Paketo numeris=as-12-344-01 ● Sudėtiniai produktai: P9101‟ ir pasirinkite tą mazgą.     
2. Medyje išplėskite toliau aprašytą mazgą ir tą mazgą pasirinkite.
    * Pradėdami nuo mazgo, kurį ką tik pasirinkote, išplėskite „M9103 ● Gamybos linija B-000050 ● 2015-12-09  ● -160,00 svar. ● Dydis=70, Spalva=Gerai, Vieta=1, Sandėlis=10, Paketo numeris=App01‟ ir pasirinkite tą mazgą.  
3. Spustelėkite Sekti nuo mazgo.
4. Spustelėkite Pirmyn.
5. Veiksmų srityje spustelėkite Sekimas.
    * Yra kelios sekimo parinktys, pateikiančios informacijos apie klientus, kuriems turėjo įtakos jūsų sekama prekė ir išsiųstus bei neišsiųstus su ta preke susijusius pardavimo užsakymus.   
6. Spustelėkite Klientai.
7. Uždarykite puslapį.
8. Veiksmų srityje spustelėkite Sekimas.
9. Spustelėkite Išsiųsti pardavimo užsakymai.
10. Uždarykite puslapį.

