---
title: Transportavimo mokesčių derinimo valdymas
description: Šioje temoje aprašomas transportavimo mokesčių derinimo procesas.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSFBDetailReconcile, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8472094ba532d531b15dc4e9f120646b2c3bbe96
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017304"
---
# <a name="reconcile-freight-in-transportation-management"></a>Transportavimo mokesčių derinimo valdymas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas transportavimo mokesčių derinimo procesas.

Transportavimo mokesčius galima suderinti neautomatiniu arba automatiniu būdu. Norėdami transportavimo mokesčius derinti automatiškai, turite nustatyti pagrindinį auditą ir jame nurodyti kriterijus, pagal kuriuos nustatoma, kurios transportavimo sąskaitos bus derinamos automatiškai.

## <a name="the-freight-reconciliation-process"></a>Transportavimo mokesčių derinimo procesas
Transportavimo tarifus skaičiuoja tarifų mechanizmas, kuris yra susijęs su atitinkamu siuntimo vežėju. Jeigu krovinys yra patvirtintas, sugeneruojama transportavimo sąskaita ir į ją įvedami transportavimo tarifai. Transportavimo tarifai kaip papildomos išlaidos yra paskiriami atitinkamam šaltinio dokumentui (pirkimo užsakymo, pardavimo užsakymo ir (arba) perdavimo užsakymo), atsižvelgiant į sąranką, naudojamą įprastame atsiskaitymo procese. Transportavimo mokesčių derinimo procesas (taip pat vadinamas gretinimo procesu) gali prasidėti iškart, kai iš vežėjo gaunama transportavimo SF. SF galima gauti elektroniniu būdu arba išspausdintą ant popieriaus. Jei SF gauta išspausdinta ant popieriaus, galite generuoti elektroninę SF, transportavimo sąskaitą naudodami kaip šabloną. 

[![Transportavimo mokesčių derinimo procesas](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Neautomatinis derinimas
Jei norite transportavimo mokesčius derinti neautomatiniu būdu, kiekvieną krovinio, kuriam išrašoma SF, SF eilutę turite suderinti su transportavimo sąskaitos eilute arba eilutėmis. Šis derinimas atliekamas puslapyje **Transportavimo sąskaitos ir SF gretinimas**. Jei SF eilutės suma nesutampa su transportavimo sąskaitos suma, turite pasirinkti skirtumo suderinimo priežastį. Jei yra kelios suderinimo priežastys, joms galite padalinti nesuderintą sumą. Suderinimo priežastis lemia, kaip skirtumo sumos registruojamos DK. Kai atskaitomas visos SF sumos suderinimas, jis pateikiamas patvirtinti, o tada žurnalas užregistruojamas. Toliau esančiame paveikslėlyje parodyta, kaip generuoti transportavimo sąskaitą faktūrą ir derinti transportavimo mokesčius. 
[![Transportavimo mokesčių derinimo užduotys](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)
## <a name="automatic-reconciliation"></a>Automatinis derinimas
Norėdami derinti automatiškai, turite nurodyti derinimo grafiką ir SF bei siuntimo vežėjus, kuriuos reikia naudoti. SF eilutės ir transportavimo sąskaitos yra derinamos pagal pagrindinio audito sąranką ir transportavimo sąskaitos tipą. Įvykdę automatinį suderinimą, turite sutvarkyti visas SF, kurių sistemai nepavyko suderinti. Tada turite šias SF apdoroti neautomatiniu būdu, kad galėtumėte užregistruoti visas mokėjimo SF.



