---
title: Papildomos knygos perkėlimas į Didžiąją knygą
description: Šiame straipsnyje aprašomos galimybės, susijusios su papildomos knygos perkėlimo procesu DK.
author: RyanCCarlson2
ms.date: 12/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 6d9b40409089e2050dc28c21040069107b766aa0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871252"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Papildomos knygos perkėlimas į Didžiąją knygą

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomos galimybės, susijusios su papildomos knygos žurnalo įrašų paketų perkėlimo taisyklėmis.

Versijoje 8.1 buvo atlikti pakeitimai, kad būtų leidžiama perkelti taisykles, pagal kurias nebenaudojama parinktis **Sinchroninis**. Daugiau informacijos ieškokite Pašalintos [arba pasenusios finansų ir operacijų funkcijos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Galimos toliau nurodytos papildomos knygos paketų perkėlimo parinktys:

- **Asinchroninis** – papildomos knygos apskaitos įrašų perkėlimas į didžiąją knygą bus suplanuotas nedelsiant. Didžiosios knygos kvitas bus įrašytas iš karto, kai tik ištekliai bus galimi apdoroti šią užklausą serveryje.
- **Suplanuotas paketas** – papildomos knygos apskaitos įrašai, kuriuos reikia perkelti, įtraukiami į apdorojimo eilę Didžiojoje knygoje. Įrašai eilėje bus apdoroti ta tvarka, kuria jie bus gauti. Kiekvienas didžiosios knygos kvitas atnaujins paskyras numatytu laiku, jei bus galimi ištekliai šios paketinės užduoties apdorojimui serveryje.

10.0.8 versijoje buvo atlikti patobulinimai, siekiant padidinti parinkties **Asinchroninis** efektyvumą. Ši funkcija aktyvinama funkcijos pavadinimu **Papildomos knygos perkėlimas į didžiosios knygos našumo optimizavimą**.

Asinchroninio papildomos knygos paketų perkėlimo funkcijos padeda pagerinti duomenų perkėlimą iš papildomos knygos į didžiąją knygą. Sugrupavus mažesnių operacijų rinkinius ir perkėlus operacijas į grupes, funkcionalumas apdoroja operacijas efektyviau. Sugrupavus operacijas, paketo serverio ištekliai naudojami efektyviau.

Asinchroninis papildomos knygos paketų perkėlimas reikalauja, kad paketinio apdorojimo serveris būtų nustatytas, tinklo ir darbo, nes paketinės užduotys yra sukuriamos tam, kad paketinio apdorojimo serveryje būtų nedelsiant užduotys. Kai papildomos knygos **perkėlimas** į DK našumo optimizavimo funkciją įgalintas, **turi būti įjungta proceso automatizavimo** **sistemos** paketinė užduotis, pavadinta Proceso automatizavimo apklausų sistemos užduotis. Norėdami gauti daugiau informacijos, [žr. Apdorojimo automatizavimas](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

Efektyvumo pokytis paketo lygiu naudoja vieną pasikartojančią paketinę užduotį visiems sistemos juridiniams subjektams. Apdorojimo metu sukuriama nauja paketinė užduotis siekiant apdoroti reikalingus įrašus, kurie nebuvo perkelti. Daugiau parametrų galima kontroliuoti sistemos administravimo **Proceso automatizavimo** puslapyje. Šiame puslapyje galite modifikuoti fono procesą, keisti dažnį ir nurodyti miego režimo laikotarpį.

Daugiau informacijos apie automatinio nustatymo procesą rasite [Proceso automatizavimas](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
