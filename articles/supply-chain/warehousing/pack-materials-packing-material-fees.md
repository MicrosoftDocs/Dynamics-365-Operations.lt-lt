---
title: "Pakavimo medžiagos ir mokesčiai"
description: "Pakavimo medžiagų mokesčiai atliekų perdirbimo įmonei mokami tam tikrais intervalais. Už kiekvieną pakuotės sudedamosios dalies svorio vienetą mokama tam tikra suma. Pakavimo medžiagų mokesčiai skaičiuojami ir pateikiami ataskaitose, tačiau DK operacijos neregistruojamos, nes šie mokesčiai nelaikomi valstybei mokamais mokesčiais."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b131cdfa2f0e3b6a8f116464323d49eaa4584634
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="packing-materials-and-fees"></a>Pakavimo medžiagos ir mokesčiai

[!include[banner](../includes/banner.md)]


Pakavimo medžiagų mokesčiai atliekų perdirbimo įmonei mokami tam tikrais intervalais. Už kiekvieną pakuotės sudedamosios dalies svorio vienetą mokama tam tikra suma. Pakavimo medžiagų mokesčiai skaičiuojami ir pateikiami ataskaitose, tačiau DK operacijos neregistruojamos, nes šie mokesčiai nelaikomi valstybei mokamais mokesčiais.

Skaičiuojami pardavimo užsakymo eilučių ir pirkimo užsakymų eilučių pakavimo medžiagų svoriai ir mokesčiai.

Prekei, prekių pakavimo grupei ar visoms prekėms galite apibrėžti vieną ar kelis pakavimo vienetus. Pakavimo vienetą sudaro pakavimo medžiagos, jų svoriai ir prekių, įeinančių į pakavimo vienetą, skaičius. Pakavimo medžiagos kodas priskiriamas kiekvienam apibrėžtam pakavimo medžiagos tipui. Pagal pakavimo medžiagos kodą galite nurodyti nurodyto laikotarpio kainą. Pagal šią informaciją skaičiuojamas pakavimo medžiagos mokestis.

| **Pastaba.**                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Net jei jūsų įmonė nemoka pakavimo medžiagų mokesčių, galite šią funkciją naudoti pakavimo medžiagų svorių statistikai skaičiuoti. |

## <a name="setup-requirements-for-packing-material-fees"></a>Nustatyti reikalavimus pakavimo medžiagų mokesčiams
Prieš skaičiuodami pakavimo medžiagų svorius ar pakavimo medžiagų mokesčius, arba ir viena, ir kita, turite sukurti toliau nurodytus pagrindinius duomenis.

-   Pakavimo grupės – sukurkite pakavimo grupes, kurias priskirsite prekėms.
-   Pakavimo medžiagų kodai – sukurkite kiekvieno apibrėžto pakavimo medžiagos tipo pakavimo medžiagų kodus.
-   Pakavimo vienetai – nurodykite prekės, pakavimo grupės arba visų prekių pakavimo vienetą. Kiekvienam pakavimo vienetui apibrėžkite, kurias pakavimo medžiagos įtraukti, priskirkite svorius ir Pakavimo vieneto koeficiento lauke iš atsargų vieneto įveskite konvertavimo koeficientą.
-   Pakavimo medžiagų mokesčiai – nurodykite vieno pakavimo medžiagų kodo pakavimo medžiagų mokesčius. Nurodykite kiekvieno medžiagų tipo galiojimo laikotarpį, kiekvienos medžiagos kainą, valiutą ir vienetą.

## <a name="packing-units-on-sales-order-lines"></a>Pakavimo vienetai pardavimo užsakymo eilutėse
Kai kuriate pardavimo užsakymo eilutę, sistema tikrina, ar nurodyti prekės pakavimo vienetai. Jei pakavimo vienetai nurodyti, sistema pardavimo užsakymo eilutę atnaujina įrašydama nurodytą pakavimo vienetą ir pakavimo vienetų kiekį. Pakavimo vienetų kiekis gaunamas užsakytą kiekį padalinus iš pasirinkto pakavimo vieneto prekių skaičiaus. Jei pakavimo vienetas nenurodytas, pardavimo užsakymo eilutėje pakavimo vienetą ir pakavimo vieneto kiekį galima įrašyti rankiniu būdu. Keisti pakavimo vienetą ir pakavimo vienetų kiekį taip pat galite registruodami pardavimo užsakymo eilutę. Tai aktualu, jei pardavimo užsakymo eilutė pristatyta arba jai SF išrašyta tik iš dalies. Kai pardavimo užsakymui išrašote SF, sukuriamos pakavimo medžiagų operacijos. Pakavimo medžiagų operacijose yra pardavimo eilutės pakavimo medžiagų svoriai. Modifikuoti operacijas taip galite joms išrašę SF, o tada kurti naujas operacijas.

## <a name="packing-units-on-purchase-order-lines"></a>Pakavimo vienetai pirkimo užsakymo eilutėse
Pirkimo užsakymo eilutės pakavimo medžiagų operacijų sistema nesukuria. Pirkimo užsakymo, kuriam išrašyta SF, eilučių operacijos kuriamos rankiniu būdu, **Pakavimo medžiagų operacijų** puslapyje.

## <a name="set-up-customer-packaging-material-fee-license-numbers"></a>Klientų pakavimo medžiagų mokesčio licencijos numerio nustatymas
Jei pakavimo medžiagų mokesčius moka klientai, puslapyje **Klientai** nurodykite klientų pakavimo medžiagų mokesčio licencijų numerius. Kai klientui priskiriamas licencijos numeris, išrašius pardavimo užsakymų SF pakavimo medžiagų mokesčiai skaičiuojami automatiškai. Išrašius SF, atžymimas puslapio **Pakavimo medžiagų operacijos** žymės langelis **Skaičiuoti mokestį**, nes jums nereikia skaičiuoti ir spausdinti ataskaitos. Galite ant SF spausdinti pakavimo medžiagų svorius, ir informuoti klientus, kad mokesčius mokės jie. 

Jei pakavimo medžiagų mokesčius moka jūsų įmonė, kliento licencijos numerio nurodyti nereikia. Išrašius SF, **Pakavimo medžiagų operacijų** puslapyje pažymimas žymės langelis **Skaičiuoti mokestį**. Tai nurodo, kad mokesčiai skaičiuojami kuriant ataskaitą. Galite ant SF spausdinti svorius ir nurodyti, kad mokesčius moka įmonė.

## <a name="print-packaging-material-weights-on-invoices"></a>Pakavimo medžiagų svorio spausdinimas ant SF
Galite ant SF spausdinti pakavimo medžiagų svorius ir nurodyti, kas mokės pakavimo medžiagų mokesčius. Svoriai sumuojami pagal pakavimo kodą.
 





