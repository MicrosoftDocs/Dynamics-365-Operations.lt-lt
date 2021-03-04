---
title: Trikties šalinimo išvesties sandėlio operacijos
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti dirbdami su išvesties sandėlio operacijomis „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 56bd91d8a6fe895317021d806e180df3a2db302b
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645458"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a>Trikties šalinimo išvesties sandėlio operacijos

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti dirbdami su išvesties sandėlio operacijomis „Microsoft Dynamics 365 Supply Chain Management“.

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a>Gaunu tolesnį klaidos pranešimą: „Pardavimo užsakymo nepavyko išleisti"

### <a name="issue-description"></a>Problemos aprašas

Ši problema gali įvykti dėl kelių priežasčių. Pavyzdžiui, užsakymą sustabdė kredito valdyba ir jokių siuntimų negalima sukurti kol patvirtinimo pašto adresas yra įvestas pardavimo eilutėms susietoms su pardavimo užsakymu. Kitu atveju, užsakymas yra sustabdytas ir turi būti įvertintas prieš tai, kai jis bus išleistas į sandėlį. Šis sulaikymas gali būti konkretus užsakymui arba būti kliento paskyroje.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Įtraukite ar naujinkite adresą pardavimo užsakyme ir užsakymo eilutėse ir tuomet paleiskite užsakymą į sandėlį. Užsakymai gali būti išleisti į sandėlį tik jei jie turi galiojantį pristatymo adresą (adreso formato nustatymuose **Organizacijos adminstracijos** modulyje).

Tirkite sustabdytą užsakymą ir adreso problemas. Tuomet pašalinkite sustabdytą užsakymą ar klientą ir išleiskite užsakymą į sandėlį.

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a>Gaunu tolesnį pranešimą: „Siuntimas 1% apkrovai buvo patvirtintas." Nepaisant, nėra jokių publikuotų eilučių.

### <a name="issue-description"></a>Problemos aprašas

Krovinio siuntimas buvo patvirtintas, bet neįvyko jokio tolesnio publikavimo.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Siuntimo patvirtinimas neveikia publikavimo. Jis tik naujina siuntimą ir krovinio būseną. Publikavimas turi vykti kaip atskiras procesas.

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a>Gaunu tolesnį klaidos pranešimą: „Tiesioginis pristatymas negali apdoroti sandėlio 1%, nes jam įjungtas sandėlio valdymas. Prašome nurodyti kitą sandelį, kuris nėra įjungtas sandėlio valdymui."

### <a name="issue-description"></a>Problemos aprašas

Prekė yra įtraukta į pardavimo eilutę tiesioginiam pristatymui iš sandėlio, kuris yra įjungtas sandėlio valdyme (WMS). Gausite šį klaidos pranešimą, kai pardavimo eilutės bus naujinta. 

### <a name="issue-resolution"></a>Problemos paaiškinimas

„Microsoft“ įvertino šią klaidą ir nustatė jos funkcijos apribojimą. Šiuo metu, WMS nepalaiko tiesioginio pristatymo. Dėl to, norėdami naudoti tiesioginį pristatymą, turite pasirinkti ne WMS prekę ir sandėlį.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]