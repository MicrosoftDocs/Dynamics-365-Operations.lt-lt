---
title: Adreso įtraukimas į aptarnavimo užsakymą
description: Šiame straipsnyje aprašoma, kaip į aptarnavimo užsakymą įtraukti kliento adresą.
author: sorenva
ms.date: 06/15/2020
ms.topic: article
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c485c50bab7c2e945aa0f0fc0601008dcebd3328
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015731"
---
# <a name="add-an-address-to-a-service-order"></a>Adreso įtraukimas į aptarnavimo užsakymą

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip į aptarnavimo užsakymą įtraukti kliento adresą. Kai kuriate aptarnavimo užsakymą, adreso informacija yra perkeliama iš projekto, prie kurio yra pridėtas aptarnavimo užsakymas. Tačiau klientams, tiekėjams, vietoms, sandėliams, aptarnavimo užsakymams ir projektams galite pasirinkti alternatyvią vietą iš adresų, kurie jau yra įtraukti į „Microsoft Dynamics AX“.

Taip pat galite kurti naują adresą. Pagal numatytuosius nustatymus naujas adresas yra perkeliamas į projektą. Tačiau galite nurodyti, kad naujasis adresas būtų taikomas tik šiam aptarnavimo atvejui. Jei tai padarysite, naujasis adresas nebus perkeliamas į projektą.

## <a name="create-a-customer-address-for-a-service-order"></a>Kliento adreso kūrimas aptarnavimo užsakymui

Norėdami įtraukti adresą į aptarnavimo užsakymą, atlikite toliau nurodytus veiksmus.

1. Eikite į Aptarnavimo **valdymo aptarnavimo** \> **užsakymai** \> **Aptarnavimo užsakymai**.

1. Atidarykite aptarnavimo užsakymą, kuriam norite sukurti adresą.

1. Atidarykite skirtuką **Antraštė**.

1. Išplėskite **adreso** "FastTab", tada iš **FastTab įrankių juostos** pasirinkite Įtraukti adresą.

1. Naujo adreso **dialogo** lange įveskite unikalų adreso pavadinimą ir užpildykite likusius laukus. 

    > [!WARNING]
    > Jei įvesite tą patį pavadinimą kaip esamo adreso, informacija, kurią įvedate likusiuose laukuose, perrašys esamo adreso informaciją.

1. Pasirinkite **Gerai,** norėdami kopijuoti naują adresą į aptarnavimo užsakymą.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Alternatyvaus adreso nurodymas aptarnavimo užsakyme

Norėdami įtraukti alternatyvų adresą į aptarnavimo užsakymą, atlikite toliau nurodytus veiksmus.

1. Eikite į Aptarnavimo **valdymo aptarnavimo** \> **užsakymai** \> **Aptarnavimo užsakymai**.

1. Atidarykite aptarnavimo užsakymą, kuriame norite įvesti alternatyvų adresą.

1. Atidarykite skirtuką **Antraštė**.

1. Išplėskite **adreso** FastTab, tada FastTab įrankių **juostoje** pasirinkite Kitas adresas.

1. Adreso **pasirinkimo dialogo** lange iš **virš nurašytų** išplečiamojo sąrašo pasirinkite Aptarnavimo užsakymai.

1. Pasirinkite adresą, o tada pasirinkite **Gerai,** norėdami nukopijuoti jį į aptarnavimo užsakymą.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]