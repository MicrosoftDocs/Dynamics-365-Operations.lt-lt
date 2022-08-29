---
title: QR kodo arba brūkšninio kodo pridėjimas prie operacijų ir kvitų el. laiškų
description: Šiame straipsnyje paaiškinama, kaip įterpti QR kodus ir brūkšninius kodus, reiškiaius užsakymo ID į operacijų ir kvitų el. laiškus Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 2832d1df3893e124759e4719a64341494cea2204
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272050"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a>QR kodo arba brūkšninio kodo pridėjimas prie operacijų ir kvitų el. laiškų

[!include [banner](includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip įterpti QR kodus ir brūkšninius kodus, reiškiaius užsakymo ID į operacijų ir kvitų el. laiškus Microsoft Dynamics 365 Commerce.

QR kodus ir brūkšninius kodus galima lengvai įtraukti į operacijų el. laiškus, kad būtų lengviau paspartinti užsakymų peržvalgos procesą mažmeninės prekybos aplinkoje. Norėdami QR kodus ir brūkšninius kodus įterpti į el. laiškus, naudokite HTML **\<img\>** žymę, kuri reikalauja QR kodo arba brūkšninio kodo vaizdo iš generavimo ir atvaizdavimo paslaugos. „Microsoft“ šios paslaugos neteikia. Tačiau yra daug nemokamų ar nebrangių paslaugų, kurios gali aprūpinti QR kodus arba brūkšninius kodus, kurie dinamiškai generuojami pagal vertę, kuri perduodama užklausos eilutėje.

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a>QR kodo arba brūkšninio kodo pridėjimas prie operacijų el. laiško

Norėdami įterpti QR kodą arba brūkšninį kodą į operacijų el. laišką, kuris siunčiamas kaip el. komercijos pirkimo dalis, atlikite nurodytus veiksmus.

1. Atidarykite operacijų el. laiško šablono šaltinio HTML ir pridėkite HTML žymę, kuri nurodo jūsų **\<img\>** QR kodo ar brūkšninio kodo tarnybą. Toliau pateikiamas pavyzdys.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    Toliau pateiktas ankstesnio pavyzdžio paaiškinimas:

    - **JŪSŲ \_QR \_KODO \_\_BRŪKŠNINIO KODO TARNYBA rodo jūsų \_** QR kodo arba brūkšninio kodo paslaugos domeną.
    - **duomenys** nurodo parametrą, kurį QR kodas arba brūkšninių kodų tarnyba naudoja turiniui, kuris turėtų būti atvaizduotas kaip QR kodas arba brūkšninis kodas, gauti.

        Vertę **%salesid%** reikia priskirti šiam parametrui. Šiame pavyzdyje atkreipkite dėmesį, kad vertė taip pat naudojama kaip alternatyvus vaizdo tekstas.

    - **param1** ir **param2** reiškia papildomus pasirenkamus parametrus.

1. Eikite į **Mažmeninė prekyba ir komercija \> Būstinės sąranka \> Parametrai \> Organizacijos el. laiškų šablonai** ir įkelkite atnaujintą HTML į atitinkamą operacijų el. laiško šabloną.

> [!NOTE]
> Parametrai gali skirtis priklausomai nuo QR kodo ir brūkšninio kodo paslaugų teikėjo. Todėl kreipkitės į savo paslaugų teikėją ir patvirtinkite parametrus, kuriems turite priskirti vertes.

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a>QR kodo arba brūkšninio kodo pridėjimas prie gavimo el. laiško 

Norėdami įterpti QR kodą arba brūkšninį kodą į gavimo el. laišką, kurį galim siųsti atlikus pirkimą elektroniniu kasos aparatu (EKA), atlikite nurodytus veiksmus.

1. Atidarykite gavimo el. laiško šablono šaltinio HTML ir pridėkite HTML **\<img\>** žymę, kuri nurodo jūsų QR kodo ar brūkšninio kodo tarnybą. Toliau pateikiamas pavyzdys.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    Toliau pateiktas ankstesnio pavyzdžio paaiškinimas:

    - **JŪSŲ \_QR \_KODO \_\_BRŪKŠNINIO KODO TARNYBA rodo jūsų \_** QR kodo arba brūkšninio kodo paslaugos domeną.
    - **duomenys** nurodo parametrą, kurį QR kodas arba brūkšninių kodų tarnyba naudoja turiniui, kuris turėtų būti atvaizduotas kaip QR kodas arba brūkšninis kodas, gauti.

        Vertę **%receiptid%** reikia priskirti šiam parametrui. Šiame pavyzdyje atkreipkite dėmesį, kad vertė taip pat naudojama kaip alternatyvus vaizdo tekstas.

    - **param1** ir **param2** reiškia papildomus pasirenkamus parametrus.

1. Eikite į **Mažmeninė prekyba ir komercija \> Būstinės sąranka \> Parametrai \> Organizacijos el. laiškų šablonai** ir įkelkite atnaujintą HTML į el. pašto šabloną, kurio el. pašto ID yra **emailrecpt**.

> [!NOTE]
> Parametrai gali skirtis priklausomai nuo QR kodo ir brūkšninio kodo paslaugų teikėjo. Todėl kreipkitės į savo paslaugų teikėją ir patvirtinkite parametrus, kuriems turite priskirti vertes.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kvitų iš „Modern POS“ (MPOS) siuntimas el. paštu](email-receipts.md)

[El. laiškų šablonų, skirtų operacijų įvykiams, kūrimas](email-templates-transactions.md)
