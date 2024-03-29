---
title: Kurti kliento nurašymo žurnalą
description: Šis užduočių vadovas jums parodys, kaip nustatyti nurašymų parametrus ir tada nurašyti operacijas puslapyje Rinkiniai, puslapyje Atidarytos klientų SF ir puslapyje Klientas.
author: ShivamPandey-msft
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21aaeda413e767fed1815423b0262127c6692bb6
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775305"
---
# <a name="create-a-write-off-journal-for-a-customer"></a>Kurti kliento nurašymo žurnalą

[!include [banner](../../includes/banner.md)]

Šis užduočių vadovas jums parodys, kaip nustatyti nurašymų parametrus ir tada nurašyti operacijas puslapyje Rinkiniai, puslapyje Atidarytos klientų SF ir puslapyje Klientas. Šioje užduotyje naudojama demonstracinė įmonė USMF.


## <a name="set-up-the-write-off-parameters"></a>Nustatyti nurašymo parametrus
1. Eikite į **Naršymo sritis > Moduliai> Kreditas ir mokėjimų priežiūra > Sąranka > Gautinos sumos parametrai**.
2. Spustelėkite skirtuką **Mokėjimų priežiūra**.
3. Išplėskite arba sutraukite dalį **Nurašyti**.
    - **Nurašymo žurnalas** yra bendrasis žurnalas, kuriame saugomos jūsų sukurtos nurašytos operacijos.  
    - Prie kiekvieno nurašymo galite pridėti priežasties kodą. Nurašydami šios numatytosios nuostatos galite nepaisyti.  
    - Nustatykite **Atskirti pardavimo mokestį** kaip Taip, jei norite atskirti pardavimo mokestį nuo nurašomos originalios operacijos.  
4. Uždarykite puslapį.
5. Pasirinkite **Kreditas ir mokėjimų priežiūra > Sąranka > Klientų registravimo šablonai**. Nurašyta sąskaita bus naudojama kaip išlaidų sąskaita arba rezervo reguliavimas bendrajame žurnale.
6. Uždarykite puslapį.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Nurašyti kliento balansą pagal terminus suskirstytų balansų puslapyje
1. Pasirinkite **Kreditas ir mokėjimai > Mokėjimų peržiūra > Suskirstyti pagal terminus balansai**.
2. Pažymėkite kliento eilutę, kurią norite nurašyti. Pavyzdžiui, pažymėkite eilutę su Birch Company.
3. **Veiksmų sritis** spustelėkite **Surinkti**.
4. Spustelėkite **Nurašyti**.
5. Spustelėkite **Gerai**.
6. Uždarykite puslapį.
7. Eikite į **Naršymo sritis > Moduliai > Bendroji didžioji knyga > Žurnalo įrašai > Bendrieji žurnalai**.
8. Pasirinkite žurnalo, kuriame yra jūsų nurašymas, paketo numerį. Atšaukti kliento balansui sukuriama viena eilutė. Viena ar kelios eilutės sukuriamos registruoti nurašymui nurašymo sąskaitoje.  
9. Uždarykite puslapį.


## <a name="write-off-transactions-from-the-collections-page"></a>Nurašyti operacijas iš mokėjimų priežiūros puslapio
1. Pasirinkite **Kreditas ir mokėjimai > Mokėjimų peržiūra > Suskirstyti pagal terminus balansai**.
2. Pasirinkite kliento su operacijomis, kurias norite nurašyti, pavadinimą. Pavyzdžiui, pasirinkite Cave Wholesales (US-004).
3. Pažymėkite pirmosios operacijos eilutę.
4. Pažymėkite antrosios operacijos eilutę.
5. Spustelėkite **Nurašyti**.
6. Lauke **Priežasties komentaras** įveskite „Blogosios skolos“.
7. Spustelėkite **Gerai**.
8. Uždarykite puslapį.
9. Uždarykite puslapį.
10. Eikite į **Didžio knyga > Žurnalo įrašai > Bendrieji žurnalai**.
11. Pasirinkite žurnalo, kuriame yra jūsų nurašymas, paketo numerį. Atšaukti kliento balansui sukuriama viena eilutė. Viena ar kelios eilutės sukuriamos registruoti nurašymui nurašymo sąskaitoje.  
12. Uždarykite puslapį.


## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Nurašyti SF puslapyje Atidarytos klientų SF
1. Eikite į **Naršymo sritis > Moduliai > Gautinos sumos > Sąskaitos faktūros > Atidarytos kliento sąskaitos faktūros**.
2. Pažymėkite SF eilutę. Pvz., pažymėkite eilutę, skirtą CIV-000667.
3. **Veiksmų sritis** spustelėkite **Sąskaita faktūra**.
4. Spustelėkite **Nurašyti**.
5. Spustelėkite **Gerai**.
6. Uždarykite puslapį.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Nurašyti kliento balansą kliento puslapyje
1. Eikite į **Gautinos sumos > Klientai > Visi klientai**.
2. Pasirinkti kliento sąskaitą. Pavyzdžiui, pasirinkite US-001 (Contoso Retail San Diego).
3. **Veiksmų sritis** spustelėkite **Surinkti**.
4. Spustelėkite **Nurašyti**.
5. Spustelėkite **Gerai**.
6. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
