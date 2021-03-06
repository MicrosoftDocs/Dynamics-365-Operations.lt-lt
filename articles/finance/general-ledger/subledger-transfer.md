---
title: Papildomos knygos perkėlimas į didžiąją knygą
description: Šioje temoje aprašomos „Microsoft Dynamics 365 Finance” teikiamos galimybės, susijusios su papildomos knygos perkėlimo procesu didžiojoje knygoje.
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1efdf095e379b73d553ca3525abbeee8ca35bcbb
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897509"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Papildomos knygos perkėlimas į didžiąją knygą

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos „Microsoft Dynamics 365 Finance” teikiamos galimybės, susijusios su papildomos knygos žurnalo įrašų paketų perkėlimo taisyklėmis.

Versijoje 8.1 buvo atlikti pakeitimai, kad būtų leidžiama perkelti taisykles, pagal kurias nebenaudojama parinktis **Sinchroninis**. Norėdami gauti daugiau informacijos, žr. [Pašalintos arba nerekomenduojamos „Finance and Operations” funkcijos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Galimos toliau nurodytos papildomos knygos paketų perkėlimo parinktys. 

 - Asinchroninė – pasirinkus šią parinktį, nedelsiant bus suplanuotas papildomos knygos apskaitos įrašų perkėlimas didžiąją knygą. Didžiosios knygos kvitas bus įrašytas iš karto, kai tik ištekliai galės laisvai apdoroti šią užklausą serveryje. 

- Planuojamas paketas – pasirinkus šią parinktį, bus įtraukti papildomos knygos apskaitos įrašai, persiunčiami į didžiosios knygos apdorojimo darbo grupę, kur įrašai bus apdorojami ta tvarka, kuria buvo gauti. Didžiosios knygos kvitas bus įrašytas numatytu laiku, jei ištekliai galės laisvai apdoroti šią paketinę užduotį serveryje. 
 
10.0.8 versijoje buvo atlikti patobulinimai, siekiant padidinti parinkties Asinchroninis efektyvumą. Ši funkcija aktyvinama funkcijos pavadinimu **Papildomos knygos perkėlimas į didžiosios knygos našumo optimizavimą**. 
 
Ši funkcija pagerina duomenų perkėlimą iš papildomos knygos į didžiąją knygą. Tai leidžia vykdyti procesą efektyviau, sugrupuojant kartu mažesnes perkeltinas operacijas. Tai leidžia efektyviau naudoti paketinio apdorojimo serverį. Norint naudoti šią funkciją, reikia nustatyti, kad paketinio apdorojimo serveris būtų nustatytas, tinkle ir veiktų, kad veiktų asinchroninio perkėlimo parinktis. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]