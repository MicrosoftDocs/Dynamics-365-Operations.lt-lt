--- 
title: "Kurti kliento nurašymo žurnalą"
description: "Šis užduočių vadovas jums parodys, kaip nustatyti nurašymų parametrus ir tada nurašyti operacijas puslapyje Rinkiniai, puslapyje Atidarytos klientų SF ir puslapyje Klientas."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: 19a816f04283ce4f200de7396617313e45e057db
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-write-off-journal-for-a-customer"></a>Kurti kliento nurašymo žurnalą

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šis užduočių vadovas jums parodys, kaip nustatyti nurašymų parametrus ir tada nurašyti operacijas puslapyje Rinkiniai, puslapyje Atidarytos klientų SF ir puslapyje Klientas. Šioje užduotyje naudojama demonstracinė įmonė USMF.


## <a name="set-up-the-write-off-parameters"></a>Nustatyti nurašymo parametrus
1. Pasirinkite Kreditas ir rinkiniai > Sąranka > Gautinų sumų parametrai.
2. Spustelėkite skirtuką Rinkiniai.
3. Išplėskite arba sutraukite dalį Nurašymas.
    * Nurašymo žurnalas yra bendrasis žurnalas, kuriame bus laikomos jūsų sukurtos nurašymo operacijos.  
    * Prie kiekvieno nurašymo galite pridėti priežasties kodą. Nurašydami šios numatytosios nuostatos galite nepaisyti.  
    * Šią parinktį nustatykite į Taip, jei norite atskirti PVM nuo pradinės nurašymo operacijos.  
4. Uždarykite puslapį.
5. Pasirinkite Kreditas ir rinkiniai > Sąranka > Klientų registravimo šablonai.
    * Nurašymo sąskaita bus naudojama kaip išlaidų sąskaita arba rezervo koregavimas bendrajame žurnale   
6. Uždarykite puslapį.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Nurašyti kliento balansą pagal terminus suskirstytų balansų puslapyje
1. Pasirinkite Kreditas ir rinkiniai > Rinkiniai > Pagal terminus suskirstyti balansai.
2. Pažymėkite kliento eilutę, kurią norite nurašyti. Pavyzdžiui, pažymėkite eilutę su Birch Company.
3. Veiksmų srityje spustelėkite Rinkti.
4. Spustelėkite Nurašyti.
5. Spustelėkite GERAI.
6. Uždarykite puslapį.
7. Pasirinkite Didžioji knyga > Žurnalų įrašai > Bendrieji žurnalai.
8. Pasirinkite žurnalo, kuriame yra jūsų nurašymas, paketo numerį.
    * Atšaukti kliento balansui sukuriama viena eilutė. Viena ar kelios eilutės sukuriamos registruoti nurašymui nurašymo sąskaitoje.  
9. Uždarykite puslapį.
10. Uždarykite puslapį.

## <a name="write-off-transactions-from-the-collections-form"></a>Nurašykite operacijas rinkinių formoje.
1. Pasirinkite Kreditas ir rinkiniai > Rinkiniai > Pagal terminus suskirstyti balansai.
2. Pasirinkite kliento su operacijomis, kurias norite nurašyti, pavadinimą. Pavyzdžiui, pasirinkite Cave Wholesales (US-004).
3. Pažymėkite pirmosios operacijos eilutę.
4. Pažymėkite antrosios operacijos eilutę.
5. Spustelėkite Nurašyti.
6. Lauke Priežasties komentaras surinkite „Blogos skolos‟.
7. Spustelėkite GERAI.
8. Uždarykite puslapį.
9. Uždarykite puslapį.
10. Pasirinkite Didžioji knyga > Žurnalų įrašai > Bendrieji žurnalai.
11. Pasirinkite žurnalo, kuriame yra jūsų nurašymas, paketo numerį.
    * Atšaukti kliento balansui sukuriama viena eilutė. Viena ar kelios eilutės sukuriamos registruoti nurašymui nurašymo sąskaitoje.  
12. Uždarykite puslapį.
13. Uždarykite puslapį.

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Nurašyti SF puslapyje Atidarytos klientų SF
1. Pasirinkite Gautinos sumos > Sąskaitos faktūros > Atidarytos klientų SF.
2. Pažymėkite SF eilutę. Pvz., pažymėkite eilutę, skirtą CIV-000667.
3. Veiksmų srityje spustelėkite Sąskaita faktūra.
4. Spustelėkite Nurašyti.
5. Spustelėkite GERAI.
6. Uždarykite puslapį.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Nurašyti kliento balansą kliento puslapyje
1. Pasirinkite Gautinos sumos > Klientai > Visi klientai.
2. Pasirinkti kliento sąskaitą. Pavyzdžiui, pasirinkite US-001 (Contoso Retail San Diego).
3. Veiksmų srityje spustelėkite Rinkti.
4. Spustelėkite Nurašyti.
5. Spustelėkite GERAI.
6. Uždarykite puslapį.


