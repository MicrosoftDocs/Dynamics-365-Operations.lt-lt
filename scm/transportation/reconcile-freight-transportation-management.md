---
title: "Transportavimo mokesčių derinimo valdymas"
description: "Šiame straipsnyje aprašomas transportavimo mokesčių derinimo procesas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 59c5dd4574aed1bc97fc945c999016be1c399f71
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="reconcile-freight-in-transportation-management"></a>Transportavimo mokesčių derinimo valdymas

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašomas transportavimo mokesčių derinimo procesas.

Transportavimo mokesčius galima suderinti neautomatiniu arba automatiniu būdu. Norėdami transportavimo mokesčius derinti automatiškai, turite nustatyti pagrindinį auditą ir jame nurodyti kriterijus, pagal kuriuos nustatoma, kurios transportavimo sąskaitos bus derinamos automatiškai.

## <a name="the-freight-reconciliation-process"></a>Transportavimo mokesčių derinimo procesas
Transportavimo tarifus skaičiuoja tarifų mechanizmas, kuris yra susijęs su atitinkamu siuntimo vežėju. Jeigu krovinys yra patvirtintas, sugeneruojama transportavimo sąskaita ir į ją įvedami transportavimo tarifai. Transportavimo tarifai kaip papildomos išlaidos yra paskiriami atitinkamam šaltinio dokumentui (pirkimo užsakymo, pardavimo užsakymo ir (arba) perdavimo užsakymo), atsižvelgiant į sąranką, naudojamą įprastame atsiskaitymo procese. Transportavimo mokesčių derinimo procesas (taip pat vadinamas gretinimo procesu) gali prasidėti iškart, kai iš vežėjo gaunama transportavimo SF. SF galima gauti elektroniniu būdu arba išspausdintą ant popieriaus. Jei SF gauta išspausdinta ant popieriaus, galite generuoti elektroninę SF, transportavimo sąskaitą naudodami kaip šabloną. 

[![Transportavimo mokesčių derinimo procesas](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Neautomatinis derinimas
Jei norite transportavimo mokesčius derinti neautomatiniu būdu, kiekvieną krovinio, kuriam išrašoma SF, SF eilutę turite suderinti su transportavimo sąskaitos eilute arba eilutėmis. Šis derinimas atliekamas puslapyje **Transportavimo sąskaitos ir SF gretinimas**. Jei SF eilutės suma nesutampa su transportavimo sąskaitos suma, turite pasirinkti skirtumo suderinimo priežastį. Jei yra kelios suderinimo priežastys, joms galite padalinti nesuderintą sumą. Suderinimo priežastis lemia, kaip skirtumo sumos registruojamos DK. Kai atskaitomas visos SF sumos suderinimas, jis pateikiamas patvirtinti, o tada žurnalas užregistruojamas. Toliau pateiktoje iliustracijoje parodyta, kaip generuoti transportavimo SF ir atlikti transportavimo mokesčių derinimą programoje „Microsoft Dynamics 365 for Operations“. 
[![Transportavimo mokesčių derinimo užduotys programoje „Dynamics AX“](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)
## <a name="automatic-reconciliation"></a>Automatinis derinimas
Norėdami derinti automatiškai, turite nurodyti derinimo grafiką ir SF bei siuntimo vežėjus, kuriuos reikia naudoti. SF eilutės ir transportavimo sąskaitos yra derinamos pagal pagrindinio audito sąranką ir transportavimo sąskaitos tipą. Įvykdę automatinį suderinimą, turite sutvarkyti visas SF, kurių sistemai nepavyko suderinti. Tada turite šias SF apdoroti neautomatiniu būdu, kad galėtumėte užregistruoti visas mokėjimo SF.




