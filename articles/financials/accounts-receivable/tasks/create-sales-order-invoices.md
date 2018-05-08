--- 
title: "Kurti pardavimo užsakymų sąskaitas faktūras"
description: "Šiame užduočių vadove aprašomas pardavimo užsakymo SF išrašymas, įskaitant SF suliejimą ir paketinį vykdymą."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4b72d5b283f9401d358ee68f4650c486ebb2fd7d
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-sales-order-invoices"></a>Kurti pardavimo užsakymų sąskaitas faktūras

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šiame užduočių vadove aprašomas pardavimo užsakymo SF išrašymas, įskaitant SF suliejimą ir paketinį vykdymą. Šioje procedūroje naudojama demonstracinė įmonė USMF.


## <a name="create-an-invoice-from-a-sales-order"></a>Iš pardavimo užsakymo kurti SF
1. Eikite į Gautinos sumos > Užsakymai > Išsiųsti pardavimo užsakymai, kuriems neišrašytos SF.
2. Sąraše pasirinkite pardavimo užsakymą. 
3. Veiksmų srityje spustelėkite Sąskaita faktūra.
4. Spustelėkite Sąskaita faktūra.
    * Atkreipkite dėmesį, kad su šiuo pardavimo užsakymu susieti keli važtaraščiai. Vietoj važtaraščio numerio bus rodomas tik žodis  <multiple>.  
5. Išplėskite skyrių Parametrai.
    * Norint užregistruoti SF, turi būti nustatyta registravimo parinktis Taip. Taip pat galite išjungti registravimą ir tik spausdinti SF. Tačiau tą patį rezultatą galite pasiekti vietoj sąskaitos faktūros sukurdami išankstinę SF.  
    * Ši pasirinktis naudojama su paketinėmis užduotimis. Užklausa vykdoma paleidus paketinę užduotį.    
6. Lauke Spausdinti pasirinkite „Vėliau‟.
7. Pasirinkite funkcijos Spausdinti SF parinktį Taip.
    * Naudojant spausdinimo valdymo funkciją, galima spausdinti kelias SF kopijas ir siųsti SF elektroniniu paštu kaip PDF failą.  
8. Lauke Spausdinti mokesčius pasirinkite „Apibendrinti‟.
9. Lauke Tikrinti kredito limitą pasirinkite „Balansas‟.
10. Spustelėkite Atšaukti.

## <a name="combine-orders-into-a-single-invoice"></a>Sujungti užsakymus į vieną SF
1. Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.
2. Suraskite klientą, kurio atidarytos kelios SF.
3. Pasirinkite atidarytą pirkimo užsakymą.
4. Pasirinkite kitą atidarytą to paties kliento pardavimo užsakymą.
5. Veiksmų srityje spustelėkite Sąskaita faktūra.
6. Spustelėkite Sąskaita faktūra.
7. Išplėskite skyrių Parametrai.
8. Lauke Kiekis pasirinkite Visi.
    * Atkreipkite dėmesį, kad peržiūros dalyje pateikiamos dvi SF. Suliekime jas į vieną SF.  
9. Lauke Suminis atnaujinimas pasirinkite „SF sąskaita‟.
10. Norėdami pardavimo užsakymus sulieti į vieną SF, spustelėkite Išdėstyti.
    * Šie du pardavimo užsakymai dabar sulieti į vieną SF.   
11. Spustelėkite Atšaukti.
12. Spustelėkite Taip.

## <a name="post-invoices-in-a-batch"></a>Registruoti SF pakete
1. Eikite į Gautinos sumos > Sąskaitos faktūros > Paketinis SF išrašymas > Sąskaita faktūra.
2. Spustelėkite Pažymėti.
3. Spustelėkite GERAI.
4. Spustelėkite Paketas.
5. Jei norite įjungti paketinį vykdymą, spustelėkite Taip.
6. Spustelėkite Pasikartojimas.
7. Pasirinkite Dienos
8. Spustelėkite GERAI.
9. Spustelėkite GERAI.
10. Spustelėkite Atšaukti.
11. Spustelėkite Taip.


