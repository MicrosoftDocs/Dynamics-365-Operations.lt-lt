---
title: Trikčių šalinimo įvesties sandėlio veiksmai
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su įvesties sandėli veiksmais „Microsoft Dynamics 365 Supply Chain Management“.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6875c3c644b9993a384ba4d8623640536d7307e1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250887"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>Trikčių šalinimo įvesties sandėlio veiksmai

[!include [banner](../includes/banner.md)]

Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su įvesties sandėli veiksmais „Microsoft Dynamics 365 Supply Chain Management“.

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>Gautu tolesnį klaidos pranešimą: „Kokybės užsakymas %1 buvo sukurtas. Klasterio profilio nepavyko rasti, prašome patikrinti konfigūravimą."

### <a name="issue-description"></a>Problemos aprašas

Šis klaidos pranešimas yra susijęs su gavimo procesu, nes kokybės valdymas (QMS) yra įjungtas. Priklausomai nuo konfigūravimų jūsų aplinkoje, papildoma informacija apie perlaidą, sukurianti klaidos pranešimą, gali padėti ištaisyti triktį.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Pirmiausia, peržiūrėkite [klasterio paėmimo](set-up-cluster-picking.md) nustatymus ir įsitikinkite, kad klasterio profiliai yra tinkamai nustatyti. Negalite naudoti prekės mobiliojo įrenginio meniu klasterio paėmimui nebent klasterio profilis yra nustatytas. Priklausomai nuo aplinkos, galbūt jums reikės peržiūrėti taip pat kitas susijusias konfigūracijas.

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>Maišytos licencijos plokštelės gavimas neveikia jokiam suteiktam kodui, išskyrus kredito.

### <a name="issue-description"></a>Problemos aprašas

Kai **Veiksmo** laukelis nustatytam kodui yra nustatytas *Kreditas* ar *Atmestas*, galite naudoti tik [Maišytos licencijos plokštelės gavimas](mixed-license-plate-receiving.md) meniu prekės į proceso sugrąžintas prekes.

### <a name="issue-resolution"></a>Problemos paaiškinimas

„Microsoft“ įvertino šią klaidą ir nustatė jos funkcijos apribojimą. Šiuo metu tik [suteikti kodai](../service-management/set-up-disposition-codes.md), kai **Veiksmo** laukelis yra nustatytas į *Kreditai* ar *Atmestas* yra palaikomi maišytos licencijos plokštelės gavime.

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>Man vykdant naujinimo produkto gavimų periodinę užduotį, nepatvirtinti pirkimo užsakymai yra patvirtinami.

### <a name="issue-description"></a>Problemos aprašas

Man įvykdžius *Naujinimo produkto gavimų* periodinę užduotį, sistema automatiškai patvirtina nepatvirtintus pirkimo užsakymus, kurie turi inventoriaus perlaidos būseną *Registruotą*.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Nauja įvesties apkrovos tvarkymo funkcija, *Per krovinio kiekių gavimą*, ištaiso šią triktį. Norėdami įjungti šią funkciją, eikite į [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ir įjunkite tolesnes funkcijas (tam, kad jos būtų sąraše):

1. Susieti pirkimo užsakymo atsargų operacijas su kroviniu
1. Krovinio kiekio perviršis

Dėl išsamesnės informacijos, žr. [Publikuoti registruotus produktų kiekius pagal pirkimo užsakymus](inbound-load-handling.md#post-registered-quantities).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]