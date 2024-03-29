---
title: Įrašyti tiekėjo SF į SF žurnalą
description: Šis užduočių vadovas parodys, kaip įrašyti tiekėjo SF, kurios nėra susietos su pirkimo užsakymais.
author: abruer
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27d0e81ca37c9a59adc3acce3610fd17fd954a8b
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716670"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Įrašyti tiekėjo SF į SF žurnalą

[!include [banner](../../includes/banner.md)]

Šis užduočių vadovas parodys, kaip įrašyti tiekėjo SF, kurios nėra susietos su pirkimo užsakymais. Šio tipo SF pavyzdžiai yra tiekimo ar paslaugų išlaidos.  Šiame įraše naudojama demonstracinė įmonė USMF.

1. Eikite į **Naršymo sritis > Moduliai > Mokėtinos sumos > Darbo sritys > Tiekėjo SF įrašas**.
2. **Veiksmų srityje** spustelėkite **Naujas SF žurnalas**.
3. Spustelėkite **Naujas**.
4. Lauke **Pavadinimas** įveskite žurnalo pavadinimą arba spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Lauke **Aprašymas įveskite** surinkite reikšmę.
6. **Veiksmų srityje** spustelėkite **Eilutės**. Lauke **Data** įveskite registravimo datą, kuri atnaujins DK.  
7. Lauke **Sąskaita** turi būti nurodyta **Tiekėjo sąskaita**.
8. Lauke **Sąskaita faktūra** įveskite SF numerį.
9. Lauke **Aprašymas įveskite** surinkite reikšmę.
10. Lauke **Kreditas** įveskite skaičių.
11. Lauke **Korespondentinė sąskaita** įveskite sąskaitos numerį arba spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą
    * Pagal numatytąsias nuostatas bus naudojama tokia pati **PVM grupė**, kaip ir tiekėjo sąskaitoje.  
    * Pagal numatytąsias nuostatas bus naudojama tokia pati **Prekės PVM grupė**, kaip ir pagrindinėje sąskaitoje, nurodytoje lauke **Korespondentinė sąskaita**.  
    * **Terminas** bus apskaičiuotas remiantis mokėjimo sąlygomis.  
    * Pagal numatytąsias nuostatas bus naudojama tokia pati **Mokėjimo nuolaida** kaip ir tiekėjo sąskaitoje.
12. Jei įjungėte tiekėjo SF žurnalo darbo eigą, spustelėkite **Darbo eiga > Pateikti**.
    * Patvirtinus jūsų pateikimą, data bus pakeista į pirmą artimiausio atviro laikotarpio dieną, jei operacijos registravimo data patenka į sulaikytą arba uždarytą DK registravimo laikotarpį.
12. Spustelėkite **Registruoti.**
13. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
