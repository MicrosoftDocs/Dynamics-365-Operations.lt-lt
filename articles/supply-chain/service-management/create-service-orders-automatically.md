---
title: Automatinis aptarnavimo užsakymų kūrimas
description: Galite kurti vienos ar kelių aptarnavimo sutarčių aptarnavimo užsakymus.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db9d337166f05f80cfdb9d4b82533117daa871e9
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014726"
---
# <a name="create-service-orders-automatically"></a>Automatinis aptarnavimo užsakymų kūrimas    

[!include [banner](../includes/banner.md)]


Galite kurti vienos ar kelių aptarnavimo sutarčių aptarnavimo užsakymus. Sukūrę aptarnavimo užsakymus, galite juos peržiūrėti formoje **Aptarnavimo užsakymai**.

Kuriami tik aptarnavimo sutarties galiojančio laikotarpio aptarnavimo užsakymai. Jei intervalas, kurį nurodote formoje **Kurti aptarnavimo užsakymus**, yra ankstesnis, nei aptarnavimo sutarties pradžios data, arba vėlesnis, nei aptarnavimo sutarties pabaigos data, kuriami tik tie aptarnavimo užsakymai, kurie apima intervalo dalį, kurią apima aptarnavimo sutarties datos.

Kai aptarnavimo užsakymus kuriate rankiniu arba automatiniu būdu iš aptarnavimo sutarties eilutės, aptarnavimo užsakymas turi būti tame pačiame laiko intervale, kuris nurodytas eilutės pradžios ir pabaigos data, nebent eilutėje nenurodėte pabaigos datos.

## <a name="create-service-orders-automatically-for-a-service-agreement"></a>Aptarnavimo sutarties aptarnavimo užsakymų kūrimas automatiniu būdu

1.  Spustelėkite Aptarnavimo **valdymo sutartys** \> **Aptarnavimo** \> **sutartys**.

2.  Pasirinkite aptarnavimo sutartį.

3.  Spustelėkite skirtuką **Pristatyti**, tada spustelėkite **Suplanuoti aptarnavimo užsakymai**.

4.  Laukuose **Pradžios data** ir **Pabaigos data** nurodykite datas, kad apibrėžtumėte aptarnavimo laikotarpį.

5.  Pažymėkite žymės langelį **Rodyti sistemos pranešimą**, kad būtų rodomas sukurtų aptarnavimo užsakymų sąrašas.

6.  Pasirinkite operacijų tipus laukų grupėje **Įtraukti operacijų tipus**. Operacijų tipai vaizduoja eilutes, sukurtas aptarnavimo sutartyje, o kiekvienas pasirinktas operacijos tipas generuoja kelis aptarnavimo užsakymus, atsižvelgiant į aptarnavimo intervalą, nurodytą aptarnavimo sutarties eilutėje.

7.  Pažymėkite žymės langelį **Ištisinis**, jei norite kurti visus aptarnavimo užsakymus, kurių trūksta nuoseklioje aptarnavimo užsakymų serijoje.

8.  Spustelėkite **Gerai**.

## <a name="create-service-orders-automatically-for-several-service-agreements"></a>Kelių aptarnavimo sutarčių aptarnavimo užsakymų kūrimas automatiniu būdu

1.  Spustelėkite **Aptarnavimo valdymas** \> **Periodinis** \> **Aptarnavimo užsakymai** \> **Kurti aptarnavimo užsakymus**.

2.  Spustelėkite **Pasirinkti**, kad pridėtumėte arba pašalintumėte kriterijus, kurie bus naudojami aptarnavimo užsakymams kurti.

3.  Spustelėkite **Gerai**.

## <a name="see-also"></a>Taip pat žiūrėkite

[Aptarnavimo užsakymai](service-orders.md)

[Automatinis aptarnavimo užsakymų kūrimas](auto-create-service-orders.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]