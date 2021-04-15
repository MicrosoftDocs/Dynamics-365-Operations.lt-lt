---
title: Transportavimo mokesčių derinimo valdymas
description: Šioje temoje aprašomas transportavimo mokesčių derinimo procesas.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d523af235d645bd282af07d6a1f617bca5fba2dc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809091"
---
# <a name="reconcile-freight-in-transportation-management"></a>Transportavimo mokesčių derinimo valdymas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas transportavimo mokesčių derinimo procesas.

Transportavimo mokesčius galima suderinti neautomatiniu arba automatiniu būdu. Norėdami transportavimo mokesčius derinti automatiškai, turite nustatyti pagrindinį auditą ir jame nurodyti kriterijus, pagal kuriuos nustatoma, kurios transportavimo sąskaitos bus derinamos automatiškai.

## <a name="the-freight-reconciliation-process"></a>Transportavimo mokesčių derinimo procesas

Transportavimo tarifus skaičiuoja tarifų mechanizmas, kuris yra susijęs su atitinkamu siuntimo vežėju. Jeigu krovinys yra patvirtintas, sugeneruojama transportavimo sąskaita ir į ją įvedami transportavimo tarifai. Transportavimo tarifai kaip papildomos išlaidos yra paskiriami atitinkamam šaltinio dokumentui (pirkimo užsakymo, pardavimo užsakymo ir (arba) perdavimo užsakymo), atsižvelgiant į sąranką, naudojamą įprastame atsiskaitymo procese. Transportavimo mokesčių derinimo procesas (taip pat vadinamas gretinimo procesu) gali prasidėti iškart, kai iš vežėjo gaunama transportavimo SF. SF galima gauti elektroniniu būdu arba išspausdintą ant popieriaus. Jei SF gauta išspausdinta ant popieriaus, galite generuoti elektroninę SF, transportavimo sąskaitą naudodami kaip šabloną.

[![Transportavimo mokesčio derinimo procesas](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>Neautomatinis derinimas

Jei norite transportavimo mokesčius derinti neautomatiniu būdu, kiekvieną krovinio, kuriam išrašoma SF, SF eilutę turite suderinti su transportavimo sąskaitos eilute arba eilutėmis. Šis derinimas atliekamas puslapyje **Transportavimo sąskaitos ir SF gretinimas**. Jei SF eilutės suma nesutampa su transportavimo sąskaitos suma, turite pasirinkti skirtumo suderinimo priežastį. Jei yra kelios suderinimo priežastys, joms galite padalinti nesuderintą sumą. Suderinimo priežastis lemia, kaip skirtumo sumos registruojamos DK. Kai atskaitomas visos SF sumos suderinimas, jis pateikiamas patvirtinti, o tada žurnalas užregistruojamas. Toliau esančiame paveikslėlyje parodyta, kaip generuoti transportavimo sąskaitą faktūrą ir derinti transportavimo mokesčius.

[![Transportavimo mokesčio derinimo užduotys](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)

## <a name="automatic-reconciliation"></a>Automatinis derinimas

Norėdami derinti automatiškai, turite nurodyti derinimo grafiką ir SF bei siuntimo vežėjus, kuriuos reikia naudoti. SF eilutės ir transportavimo sąskaitos yra derinamos pagal pagrindinio audito sąranką ir transportavimo sąskaitos tipą. Įvykdę automatinį suderinimą, turite sutvarkyti visas SF, kurių sistemai nepavyko suderinti. Tada turite šias SF apdoroti neautomatiniu būdu, kad galėtumėte užregistruoti visas mokėjimo SF.

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a>Transportavimo mokesčių sąskaitų ir sąskaitų faktūrų gretinimas naudojant automatinį arba rankinį derinimą

*Gretinimas* yra transportavimo sąskaitų, atitinkančių kiekvieną transportavimo sąskaitą faktūrą, ieškojimo procesas. Tai galima atlikti sugretinus sąskaitos faktūros eilutes vieną po kito (neautomatinis gretinimas) arba sugretinus visas galimas sąskaitas faktūras iš karto (automatinis gretinimas).

### <a name="auto-matching"></a>Automatinis gretinimas

Kai kelios transportavimo sąskaitos faktūros gretinamos su ta pačia transportavimo sąskaita, automatinio gretinimo procesas vyksta taip:

1. Visos nesugretintos transportavimo sąskaitos faktūros rūšiuojamos pagal sumą, pirmiausia – didžiausią sumą.
1. Transportavimo mokesčių sąskaitos faktūros gretinamos viena po kitos, kol transportavimo sąskaitoje neliks teigiamos sumos.
1. Atsižvelgiant į pagrindinio audito nustatymą ir likusią transportavimo sąskaitų faktūrų sumą, nustatoma likusi suma.

### <a name="manual-matching"></a>Rankinis gretinimas

Bus galima sugretinti visas transportavimo sąskaitas, kurių suma teigiama. Panašiai kaip ir automatiniame gretinime, vartotojas galės sugretinti transportavimo sąskaitas faktūras, turinčias neigiamas sumas, su nevisiškai sugretintomis transportavimo sąskaitomis.

### <a name="example"></a>Pavyzdys

Tarkime, kad turite 1500 sumos transportavimo sąskaitą (FB) ir sukūrėte tris transportavimo sąskaitas faktūras tai transportavimo sąskaitai su viena SF eilute kiekvienai SF su šiais parametrais:

- Pradinė transportavimo sąskaita (FB): Suma 1500
- 1 sąskaita faktūra (Inv1): Suma 1000
- 2 sąskaita faktūra (Inv2): Suma 600
- 3 sąskaita faktūra (Inv3): Suma ‑100

#### <a name="automatic-matching-result"></a>Automatinio gretinimo rezultatas

Automatinis gretinimas bus vykdomas tokia tvarka:

1. Išrūšiuos visas transportavimo sąskaitas faktūras mažėjimo tvarka pagal sumą: Inv1 -> Inv2 -> Inv3.
1. Sugretins Inv1 su FB. Inv1 turi 1000 sugretinta, o FB turi likusią 500 sumą, todėl būsena nustatoma kaip *Iš dalies sugretinta*.
1. Sugretins Inv2 su FB. Inv2 turi 500 sugretinta, o FB turi likusį 0, todėl būsena nustatoma kaip *Pilnai sugretinta*.
1. Kadangi FB dabar yra visiškai sugretinta, Inv3 nebus apdorota.

#### <a name="manual-matching-result"></a>Rankinio gretinimo rezultatas

Neautomatinio gretinimo rezultatai skiriasi atsižvelgiant į gretinimo tvarką, kaip pavaizduota tolesnio pavyzdžio atvejuose.

##### <a name="manual-matching-case-1"></a>Rankinio gretinimo 1 atvejis

Vienas šio pavyzdžio rankinio gretinimo būdas yra elgtis taip:

1. Sugretinti FB su Inv1. FB turi likusią 500 sumą, todėl būsena yra nustatoma kaip *Iš dalies sugretinta*.
1. Sugretins Inv2 su FB. Inv2 turi 500 sugretinta, o FB turi likusį 0, todėl būsena nustatoma kaip *Pilnai sugretinta*.
1. Kai Inv3 gretinsite neautomatiniu būdu, nerasite jokių nesugretintų transportavimo sąskaitų.

Iš esmės šis atvejis yra toks pat, kaip ir automatiniame gretinime

##### <a name="manual-matching-case-2"></a>Rankinio gretinimo 2 atvejis

Kitas šio pavyzdžio rankinio gretinimo būdas yra elgtis taip:

1. Sugretinti Inv3 su FB. Dabar FB turi likusią 1600 sumą, kuri yra tokia pati, kaip iš 1500 atimti neigiamą 100 sumą. Tiek FB, tiek Inv3 sugretintas kiekis yra -100.
1. Sugretinti Inv1 ir Inv 2 su FB vieną po kito. FB yra visiškai sugretinta.

Kaip rodo šis pavyzdys, transportavimo sąskaitos faktūrų su neigiamomis sumomis gretinimą reikia atlikti tik rankiniu būdu. Taip užtikrinsite, kad visada galima sugretinti transportavimo sąskaitas faktūras, turinčias neigiamas sumas, su nevisiškai sugretintomis transportavimo sąskaitomis, kas leidžia valdyti gretinimo seką.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]