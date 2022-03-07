---
title: Kurti pardavimo užsakymų sąskaitas faktūras
description: Šiame užduočių vadove aprašomas pardavimo užsakymo SF išrašymas, įskaitant SF suliejimą ir paketinį vykdymą.
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a6556838a2843f961e1538947a6eda090b94894ed4df8476ea60abeda8056b6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771829"
---
# <a name="create-sales-order-invoices"></a>Kurti pardavimo užsakymų sąskaitas faktūras

[!include [banner](../../includes/banner.md)]

Šiame užduočių vadove aprašomas pardavimo užsakymo SF išrašymas, įskaitant SF suliejimą ir paketinį vykdymą. Šioje procedūroje naudojama demonstracinė įmonė USMF.


## <a name="create-an-invoice-from-a-sales-order"></a>Iš pardavimo užsakymo kurti SF
1. Eikite į **Naršymo sritis > Moduliai >Gautinos sumos > Užsakymai > Išsiųsti pardavimo užsakymai, kuriems neišrašytos SF**.
2. Sąraše pasirinkite pardavimo užsakymą. 
3. **Veiksmų srityje** spustelėkite **Sąskaita faktūra > Generuoti > Sąskaita faktūra**. Atkreipkite dėmesį, kad su šiuo pardavimo užsakymu susieti keli važtaraščiai. Vietoj važtaraščio numerio bus rodomas tik žodis  <multiple>.  
4. Išplėskite skyrių **Parametrai**.
    - Norint užregistruoti SF, turi būti nustatyta registravimo parinktis Taip. Taip pat galite išjungti registravimą ir tik spausdinti SF. Tačiau tą patį rezultatą galite pasiekti vietoj sąskaitos faktūros sukurdami išankstinę SF.  
    - Ši pasirinktis naudojama su paketinėmis užduotimis. Užklausa vykdoma paleidus paketinę užduotį.
5. Lauke **Spausdinti** pasirinkite „Vėliau”.
6. Pasirinkite funkcijos **Spausdinti SF** parinktį **Taip**. Naudojant spausdinimo valdymo funkciją, galima spausdinti kelias SF kopijas ir siųsti SF elektroniniu paštu kaip PDF failą.  
7. Lauke **Spausdinti mokesčius** pasirinkite „Apibendrinti”.
8. Lauke **Tikrinti kredito limitą** pasirinkite „Balansas”.
9. Spustelėkite **Atšaukti**.

## <a name="combine-orders-into-a-single-invoice"></a>Sujungti užsakymus į vieną SF
1. Eikite į **Valdymo skiltį > Moduliai > Gautinos sumos > Užsakymai > Visi pardavimo užsakymai**.
2. Suraskite klientą, kurio atidarytos kelios SF.
3. Pasirinkite kelis atvirus pardavimo užsakymus iš to paties kliento.
4. **Veiksmų srityje** spustelėkite **Sąskaita faktūra > Generuoti > Sąskaita faktūra**.
5. Išplėskite skyrių **Parametrai**.
6. Lauke **Kiekis** pasirinkite „Visi‟. Atkreipkite dėmesį, kad peržiūros dalyje pateikiamos dvi SF. Suliekime jas į vieną SF.  
7. Lauke **Suminis atnaujinimas** pasirinkite „SF sąskaita”.
8. Norėdami pardavimo užsakymus sulieti į vieną SF, spustelėkite **Išdėstyti**. Šie du pardavimo užsakymai dabar sulieti į vieną SF.   
9. Spustelėkite **Atšaukti**.
10. Spustelėkite **Taip**.

## <a name="post-invoices-in-a-batch"></a>Registruoti SF pakete
1. Eikite į **Naršymo sritis > Moduliai > Gautinos sumos > Sąskaitos faktūros > Paketinis SF išrašymas > Sąskaita faktūra**.
2. Spustelėkite **Pažymėti**.
3. Spustelėkite **Gerai**.
4. Spustelėkite **Paketas**.
5. Lange **Paketinis vykdymas**, pasirinkite **Taip**.
6. Spustelėkite **Pasikartojimas**.
7. Pasirinkite **Dienos**.
8. Spustelėkite **Gerai**.
9. Spustelėkite **Gerai**.
10. Spustelėkite **Atšaukti**.
11. Spustelėkite **Taip**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]