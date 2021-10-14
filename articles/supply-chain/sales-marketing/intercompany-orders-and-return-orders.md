---
title: Vidinės įmonės užsakymai ir grąžinimo užsakymai
description: Šioje temoje paaiškinami vidinės įmonės užsakymai ir grąžinimo užsakymai
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 103225595e82bdedec6d97e5ebe5b61498377065
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548432"
---
# <a name="intercompany-orders-and-return-orders"></a>Vidinės įmonės užsakymai ir grąžinimo užsakymai

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip kurti ir atnaujinti vidinės įmonės pirkimo, pardavimo užsakymus, pirkimo ir pardavimo sutartis.

## <a name="about-intercompany-orders"></a>Apie vidinės įmonės užsakymus

Jums sukūrus vidinės įmonės pardavimo užsakymą, „Microsoft Dynamics 365 Supply Chain Management“ automatiškai sukuria atitinkamą pirkimo užsakymą. Panašiu būdu vidinės įmonės pirkimo užsakymo sukūrimas iššaukia automatinį atitinkamo vidinės įmonės pardavimo užsakymo sukūrimą.

Tai taikoma dvipusiams užsakymams (operacijoms tarp dviejų susijusių įmonių) ir daugumai tripusių įmonių (kai vidinės įmonės operacija sukuriama su pardavimo užsakymu, skirtu išoriniam klientui).

## <a name="intercompany-order-example"></a>Vidinės įmonės užsakymo pavyzdys

Jūs turite dvi susijusias įmones. Įmonė A yra pardavimo dukterinė įmonė, o įmonė B – paskirstymo filialas. Vidinės įmonės pardavimo ir pirkimo užsakymai automatiškai kuriami naudojant šiuos scenarijus:

- Įmonei A sukūrus pardavimo užsakymą, o tiekėju esant įmonei B, vidinės įmonės pardavimo užsakymas automatiškai sukuriamas įmonėje B. Dvipusio užsakymo grandinė sudaryta iš pirkimo užsakymo įmonėje A ir vidinės įmonės pardavimo užsakymo įmonėje B.
- Įmonei B sukūrus pardavimo užsakymą, o klientui esant įmonei A, vidinės įmonės pirkimo užsakymas automatiškai sukuriamas įmonėje A. Dvipusio užsakymo grandinė sudaryta iš pardavimo užsakymo įmonėje B ir vidinės įmonės pirkimo užsakymo įmonėje A.
- Įmonei A pirmąkart sukūrus pardavimo užsakymą, skirtą išoriniam klientui, įmonėje A gali būti automatiškai sukurtas pirkimo užsakymas. Tai savo ruožtu iššauks automatinį vidinės įmonės pardavimo užsakymo sukūrimą įmonėje B. Tripusio užsakymo grandinė sudaryta iš pardavimo ir pirkimo užsakymo įmonėje A ir vidinės įmonės pardavimo užsakymo įmonėje B.

## <a name="about-intercompany-return-orders"></a>Apie vidinės įmonės grąžinimo užsakymus

Vidinės įmonės prekes galite grąžinti kaip ir įprastas. Tačiau grąžinant vidinės įmonės prekes grąžinimo užsakymas iš išorinio kliento sukuria vidinės įmonės pirkimo užsakymą. Tai savo ruožtu lemia automatinį vidinės įmonės grąžinamo pardavimo užsakymo sukūrimą. Taip pat galite grąžinti vidinės įmonės prekę be išorinio kliento grąžinimo užsakymo.

Vidinės įmonės grąžinimo užsakymai, panašiai, kaip ir įprasti grąžinimo užsakymai, inicijuojami puslapyje **Kurti grąžinim užsakymą**.

Naudojant „Microsoft Dynamics 365 Supply Chain Management“, vidinės įmonės pardavimo ir pirkimo sutartys automatiškai atnaujinamos, kad būtų rodoma grąžinta prekė. Prekės pardavimo arba pirkimo sutarties įsipareigojimas automatiškai koreguojamas, kad būtų rodomas tinkamas kiekis arba suma grąžinant prekę.

## <a name="intercompany-return-order-example"></a>Vidinės įmonės grąžinimo užsakymo pavyzdys

Įmonė A sukuria pirkimo užsakymą, susietą su vidinės įmonės prekės pirkimo sutartimi. Įmonėje B automatiškai sukuriamas vidinės įmonės pardavimo užsakymas, susietas su atitinkama pardavimo sutartimi. Pirkimo ir pardavimo sutartys yra susijusios su vidinės įmonės sutartimis.

Įmonė A grąžina vidinės įmonės prekę įmonei B. Įmonė B sukuria prekės grąžinimo užsakymą ir prekės pirkimo grąžinimo užsakymas automatiškai sukuriamas įmonėje A. Pirkimo sutarties ir pardavimo sutarties įsipareigojimai, susieti su pradiniais užsakymais, automatiškai koreguojami, kad po pasikeitimo būtų rodomas tinkamas kiekis arba suma.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
