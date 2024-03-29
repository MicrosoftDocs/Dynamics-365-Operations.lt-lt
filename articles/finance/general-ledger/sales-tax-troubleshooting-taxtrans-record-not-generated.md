---
title: TaxTrans įrašas nesugeneruojamas
description: Šiame straipsnyje pateikiama trikčių diagnostikos informacija, kuri gali padėti, kai TaxTrans įrašas nesugeneruojamas.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 402b1200e96ec8130034a03447ca071477544a88
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846718"
---
# <a name="taxtrans-record-isnt-generated"></a>TaxTrans įrašas nesugeneruojamas

[!include [banner](../includes/banner.md)]

Jei pasirenkate operacijos užregistruotą PVM, bet užregistruoto PVM puslapyje nėra mokesčio eilučių arba trūksta mokesčio eilutės, „TaxTrans“ įrašas **galėjo** **būti** **nesugeneruotas**.

[![Užregistruotas PVM puslapis, kuriame nėra eilučių elementų.](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)

Norėdami išspręsti šią problemą, atlikite tolesniuose skyriuose nurodytus veiksmus.

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a>Pvm tikrinimas prieš užregistruojant operaciją

1. Prieš registruodami operaciją, SF **registravimo** puslapyje pasirinkite **PVM, norėdami patikrinti** skaičiavimą.

    [![PVM mygtukas SF registravimo puslapyje.](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)

2. Laikinų **PVM operacijų puslapyje** peržiūrėkite skaičiavimo rezultatą. Jei mokestis nėra skaičiuojamas, [žr. mokestis nesuskaičiuotas arba mokesčio suma yra](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md) nulis.

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a>Rasti TaxTrans įrašą visuose užregistruotuose PVM

1. Eikite į **Mokestis** \> **Užklausos ir ataskaitos** \> **ataskaitos** > **Registruotas PVM**.
2. Kvito **stulpelio** antraštėje pasirinkite filtro simbolį, kad rastumėte **TaxTrans** įrašą.
3. Jei radote PVM įrašus, kurių ieškote, patikrinkite datą. Jei data skiriasi nuo žurnalo antraštės datos, sukurkite „Microsoft“ aptarnavimo papildomos pagalbos užklausą.

    [![Registruoto PVM puslapis.](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)

## <a name="debug-to-check-details"></a>Derinti norint patikrinti informaciją

1. Norėdami gauti informacijos, kaip suderinti ir nustatyti, ar **TmpTaxWorkTrans ir TaxUncommitted sugeneruota teisingai, žr.** **TaxTrans** [lauko](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md) vertę.
2. Jei TaxTmpWorkTrans arba TaxUncommitted sugeneruotas teisingai, pridėkite stabdos **tašką** **TaxPost** **SaveAndPost::() ir** **Mokesčių ::saveAndPost,** **kad** būtų suderinti TaxTrans įterpimo priežastis.

    [![Kode įtraukti stabdos taškai.](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)

    [![Pridėtų stabdos taškų rezultatai.](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)

## <a name="determine-whether-customization-exists"></a>Nustatyti, ar yra tinkinimas

Jei atlikote veiksmus ankstesniuose skyriuose, bet neradote problemos, nustatykite, ar yra tinkinimas. Jei tinkinimo nėra, sukurkite „Microsoft" aptarnavimo užklausą, kad ji būtų tolimesnė.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
