---
title: Adreso įtraukimas į aptarnavimo užsakymą
description: Šioje temoje aprašoma, kaip įtraukti kliento adresą į aptarnavimo užsakymą.
author: ShylaThompson
manager: AnnBe
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58188be6f82b6587011188379e5370b81f8fd114
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570370"
---
# <a name="add-an-address-to-a-service-order"></a>Adreso įtraukimas į aptarnavimo užsakymą    

[!include [banner](../includes/banner.md)]


Šioje temoje aprašoma, kaip įtraukti kliento adresą į aptarnavimo užsakymą. Kai kuriate aptarnavimo užsakymą, adreso informacija yra perkeliama iš projekto, prie kurio yra pridėtas aptarnavimo užsakymas. Tačiau klientams, tiekėjams, vietoms, sandėliams, aptarnavimo užsakymams ir projektams galite pasirinkti alternatyvią vietą iš adresų, kurie jau yra įtraukti į „Microsoft Dynamics AX“.

Taip pat galite kurti naują adresą. Pagal numatytuosius nustatymus naujas adresas yra perkeliamas į projektą. Tačiau galite nurodyti, kad naujasis adresas būtų taikomas tik šiam aptarnavimo atvejui. Jei tai padarysite, naujasis adresas nebus perkeliamas į projektą.

## <a name="create-a-customer-address-for-a-service-order"></a>Kliento adreso kūrimas aptarnavimo užsakymui

Norėdami įtraukti adresą į aptarnavimo užsakymą, atlikite toliau nurodytus veiksmus.

1.  Spustelėkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.

2.  Atidarykite aptarnavimo užsakymą, kuriam norite sukurti adresą.

3.  Dalyje **Veiksmų sritis**, spustelėkite **Redaguoti**, tada spustelėkite **Antraštės rodinys**.

4.  Dalies **Adresas** „FastTab“ spustelėkite **Pridėti adresą**.

5.  Formoje **Naujas adresas** įveskite unikalų adreso pavadinimą ir užpildykite likusius laukus. 
    

    > [!WARNING]
    > <P>Jei įvesite tą patį pavadinimą kaip esamo adreso, informacija, kurią įvedate likusiuose laukuose, perrašys esamo adreso informaciją.</P>


6.  Spustelėkite **Gerai**, kad nukopijuotumėte naują adresą į aptarnavimo užsakymą.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Alternatyvaus adreso nurodymas aptarnavimo užsakyme

Norėdami įtraukti alternatyvų adresą į aptarnavimo užsakymą, atlikite toliau nurodytus veiksmus.

1.  Spustelėkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.

2.  Atidarykite aptarnavimo užsakymą, kuriame norite įvesti alternatyvų adresą.

3.  Dalyje **Veiksmų sritis**, spustelėkite **Redaguoti**, tada spustelėkite **Antraštės rodinys**.

4.  Dalies **Adresas** „FastTab“ spustelėkite **Kiti adresai**.

5.  Formos **Adreso pasirinkimas** lauke **Įrašo tipas** pasirinkite **Aptarnavimo užsakymai**.

6.  Pasirinkite adresą, tada spustelėkite **Gerai**, kad nukopijuotumėte jį į aptarnavimo užsakymą.


  


