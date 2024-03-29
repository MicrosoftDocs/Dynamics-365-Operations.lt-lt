---
title: Pardavimo užsakymų sąskaitų faktūrų kūrimas
description: Šiame straipsnyje aprašoma, kaip išrašyti pardavimo užsakymo SF, įskaitant SF suliejimą ir paketinį apdorojimą.
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ff76eac54da6621d999d9b629fac920ba8de294
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778390"
---
# <a name="create-sales-order-invoices"></a>Pardavimo užsakymų sąskaitų faktūrų kūrimas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip išrašyti pardavimo užsakymo SF, įskaitant SF suliejimą ir paketinį apdorojimą. Šioje procedūroje naudojama demonstracinė įmonė USMF.


## <a name="create-an-invoice-from-a-sales-order"></a>Iš pardavimo užsakymo kurti SF
1. Eikite į **Naršymo sritis > Moduliai >Gautinos sumos > Užsakymai > Išsiųsti pardavimo užsakymai, kuriems neišrašytos SF**.
2. Sąraše pasirinkite pardavimo užsakymą. 
3. **Veiksmų srityje** spustelėkite **Sąskaita faktūra > Generuoti > Sąskaita faktūra**. Atkreipkite dėmesį, kad su šiuo pardavimo užsakymu susieti keli važtaraščiai. Vietoj važtaraščio numerio bus rodomas tik žodis *keletas*.  
4. Išplėskite skyrių **Parametrai**.
    - Norint registruoti SF, registravimas **turi** būti nustatytas kaip Taip. Taip pat galite išjungti registravimą ir tik spausdinti SF. Tačiau tą patį rezultatą galite pasiekti vietoj sąskaitos faktūros sukurdami išankstinę SF.  
    - Ši pasirinktis naudojama su paketinėmis užduotimis. Užklausa vykdoma paleidus paketinę užduotį.
5. **Lauke Spausdinti** pasirinkite **Po**.
6. Pasirinkite funkcijos **Spausdinti SF** parinktį **Taip**. Spausdinimo valdymas gali spausdinti kelias SF kopijas ir taip pat siųsti SF el. paštu kaip PDF failą.  
7. **Lauke Spausdinimo mokesčiai** pasirinkite **Apibendrinta**.
8. Lauke Tikrinti **kredito limitą** pasirinkite **Balansas**.
9. Spustelėkite **Atšaukti**.

## <a name="combine-orders-into-a-single-invoice"></a>Sujungti užsakymus į vieną SF
1. Eikite į **Valdymo skiltį > Moduliai > Gautinos sumos > Užsakymai > Visi pardavimo užsakymai**.
2. Suraskite klientą, kurio atidarytos kelios SF.
3. Pasirinkite kelis atvirus pardavimo užsakymus iš to paties kliento.
4. **Veiksmų srityje** spustelėkite **Sąskaita faktūra > Generuoti > Sąskaita faktūra**.
5. Išplėskite skyrių **Parametrai**.
6. Lauke **Kiekis** pasirinkite **Visi**. Atkreipkite dėmesį, kad peržiūros dalyje pateikiamos dvi SF. Suliekime jas į vieną SF.  
7. Lauke Suminį **atnaujinimą** pasirinkite SF **sąskaita**.
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
