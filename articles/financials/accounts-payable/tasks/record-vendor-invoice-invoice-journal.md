---
title: Įrašyti tiekėjo SF į SF žurnalą
description: Šis užduočių vadovas parodys, kaip įrašyti tiekėjo SF, kurios nėra susietos su pirkimo užsakymais.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97dd03a96389ab22e441acd0af1ad35852570be4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837017"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Įrašyti tiekėjo SF į SF žurnalą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šis užduočių vadovas parodys, kaip įrašyti tiekėjo SF, kurios nėra susietos su pirkimo užsakymais. Šio tipo SF pavyzdžiai yra tiekimo ar paslaugų išlaidos.  Šiame įraše naudojama demonstracinė įmonė USMF.

1. Eikite į **Naršymo sritis > Moduliai > Mokėtinos sumos > Darbo sritys > Tiekėjo SF įrašas**.
2. **Action pane** spustelėkite **New invoice journal**.
3. Spustelėkite **Naujas**.
4. Lauke **Name**įveskite žurnalo pavadinimą arba spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Lauke **Description field**surinkite reikšmę.
6. **Action pane**spustelėkite **Lines**. Lauke **Date**įveskite registravimo datą, kuri atnaujins DK.  
7. Lauke **Account** nurodykite **Vendor account**.
8. Lauke **Invoice** įveskite SF numerį.
9. Lauke **Description field**surinkite reikšmę.
10. Lauke **Credit** įveskite skaičių.
11. Lauke **Offset account** įveskite sąskaitos numerį arba spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą
    * Pagal numatytąsias nuostatas bus naudojama tokia pati **Sales tax group**, kaip ir tiekėjo sąskaitoje.  
    * Pagal numatytąsias nuostatas bus naudojama tokia pati grupė **Item sales tax group**, kaip ir pagrindinėje sąskaitoje, nurodytoje lauke **Offset account**.  
    * **Due date** bus apskaičiuotas remiantis mokėjimo sąlygomis.  
    * Pagal numatytąsias nuostatas bus naudojama tokia pati **Cash discount** kaip ir tiekėjo sąskaitoje.  
12. Spustelėkite **Registruoti.**
13. Uždarykite puslapį.

