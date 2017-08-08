---
title: "Medžiagų vartojimo registravimas naudojant mobilųjį įrenginį"
description: "Šioje temoje aprašoma darbo eiga, kurią naudojant galima kišeniniu įrenginiu registruoti žaliavų sunaudojimą gamybos metu."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b4c0d14340e96b2e7916ea73e25e62ae5c33ce49
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---

# <a name="register-material-consumption-using-a-mobile-device"></a>Medžiagų vartojimo registravimas naudojant mobilųjį įrenginį
Šioje temoje aprašoma darbo eiga, kurią naudojant galima kišeniniu įrenginiu registruoti žaliavų sunaudojimą gamybos metu.

<a name="introduction"></a>Įžanga
------------

Ši darbo eiga aktuali, jei griežtai reikalaujama atsekti medžiagas. Tokiais atvejais norint užtikrinti medžiagų atsekamumą reikia nurodyti tikslų sunaudojimo laiką ir kiekį. Šį procesą galima laikyti priešingu išankstinio ar atgalinio sunaudojimo operacijoms, kai nesutampa registracijos laikas ir laikas, kada medžiagos faktiškai naudojamos. Tai paaiškina, kodėl automatinio sunaudojimo strategijos negalima naudoti su kai kuriomis medžiagomis, kurias reikalaujama atsekti. Pažvelkime į paprastą scenarijų, paaiškinantį, kaip nustatyti darbo eigą, kad kišeniniu įrenginiu būtų galima registruoti žaliavų sunaudojimą gamybos metu. [![](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a>Išsami scenarijaus informacija

Nepertraukiamo gamybos proceso (5) metu sunaudojama paketiniu būdu kontroliuojama žaliava RM-100. Medžiaga turima vietoje Bulk-001 (1) (numerio lentelė – PL-1), kurioje yra du paketai (B1 ir B2), kuriuose yra po 100 svarų medžiagos kiekio. Pateikiamas ir apdorojamas RM-100 sandėlio darbas (2), o medžiaga iš Bulk-001 paimama į gamybos įvesties vietą PIL-01 (3), kuri apibrėžta kaip kontroliuojama ne pagal numerio lentelę. Mašinos operatorius pasveria medžiagą iš gamybos įvesties vietos (3) ir svorį bei paketo numerį užregistruoja kaip sunaudotus (4). Dalis medžiagos apibrėžtais laiko intervalais rankiniu būdu iš gamybos įvesties vietos dedama į gamybos procesą. Mašinos operatoriui dedant medžiagą, ji pasveriama ant svarstyklių ir užregistruojamas paketo numeris.

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a>Darbo eigos nustatymas, kad sunaudojimą būtų galima registruoti kišeniniu įrenginiu
Sukurkite baigtos prekės produktą FG-100 su komplektavimo specifikacija, kurioje yra paketiniu būdu kontroliuojama žaliava RM-100. Į vietą Bulk-001 (numerio lentelė – PL-1) įtraukite du RM-100 paketus (B1 ir B2), kurių kiekis – 100. Komplektavimo specifikacijos RM-100 eilutėje sunaudojimo principas nustatomas kaip **Rankinis**. Gamybos įvesties vietą nustatykite kaip PIL-01. Tai padaryti galite šią vietą pasirinkdami kaip numatytąją 51 sandėlio gamybos įvesties vietą.

1.  Sukurkite naują mobiliojo įrenginio meniu elementą: 

-    **Meniu elemento pavadinimas** – Registruoti medžiagų sunaudojimą. 
-    **Pavadinimas** – Registruoti medžiagų sunaudojimą. 
-    **Režimas** – Netiesioginis. 
-    **Veiklos kodas** – Registruoti medžiagų sunaudojimą.

2.  Meniu elementą įtraukite į mobiliojo įrenginio meniu **Gamyba**.
3.  Sukurkite baigto produkto gamybos užsakymą: 

-    **Prekės numeris** – FG-100 
-    **Teritorija** – 5 
-    **Sandėlis** – 51 
-    **Kiekis** – 150

Gamybos užsakymas **įvertinamas** bei **pateikiamas** ir sukuriamas sandėlio darbas.

4.  Atlikite darbą naudodami kišeniniam įrenginiui skirtą žaliavų paėmimo darbo eigą.

Taip medžiaga iš buferinės vietos bus perkelta į gamybos įvesties vietą PIL-01. Baigus darbą medžiagos būsena yra **Paimta gamybos įvesties vietoje**. Apdorojus darbą būsena gali būti **Paimta** arba **Rezervuota faktiškai**. Tai konfigūruojama naudojant parametrą **išdavimo būsena pateikus sandėlio formoje**.

5.  Kliente arba kišeniniame įrenginyje naudodami meniu elementą **Gamybos pradžia** pradėkite gamybos užsakymą.

Kai gamybos užsakymas pradėtas, naudodami kišeniniam įrenginiui skirtą darbo eigą galite registruoti medžiagų sunaudojimą. Pradėkime registruodami paketo B1 25 svarų sunaudojimą.

6.  Kišeninio įrenginio meniu pasirinkite elementą **Registruoti medžiagų** **sunaudojimą** ir įveskite tolesnę informaciją. 

-    Gamybos užsakymo numeris. 
-    Vietą, kurioje medžiaga bus sunaudota, šiuo atveju – PIL-01. 
-    Prekės numerį RM-100. 
-    Paketo numerį B1. 
-    Kiekį – 25.

7.  Pasirinkite **Gerai**.

Atkreipkite dėmesį, kad ekrane atsiranda pranešimas „Sukurta žurnalo eilutė‟. Gamybos užsakyme yra atviras tipo **Gamybos išrinkimo dokumentas** žurnalas, kurio prekės numeris – RM-100, o paketo numeris – B1. 

Dabar galite pasirinkti tęsti registraciją, pavyzdžiui, paketo nr. B2, ir kiekvieną kartą pasirinkus **Gerai** į atvirą žurnalą įtraukiama nauja žurnalo eilutė. 

Baigę registraciją pasirinkite **Atlikta** – žurnalas užregistruojamas, o darbo eiga baigiama.

### <a name="additional-comments"></a>Papildomi komentarai 

-   Jei vartotojas atšaukia darbo eigą, kai sukurta žurnalo eilutė, žurnalas yra neužregistruotos būsenos, tačiau, jei vartotojas vėliau šią darbo eigą naudos su tuo pačiu gamybos užsakymu, eilutės bus įtrauktos į atvirą, o ne į naują žurnalą.
-   Naujoje darbo eigoje taip pat galima registruoti serijos numerius.
-   Galima registruoti tik pasirinkto gamybos užsakymo arba paketinio užsakymo komplektavimo specifikacijoje ar formulėje nustatytą prekės numerį.
-   Medžiagos galima sunaudoti daugiau nei numatyta. Pavyzdžiui, jei numatoma sunaudoti 100 svarų medžiagos, jos galima sunaudoti daugiau, pavyzdžiui, 105 svarus.



