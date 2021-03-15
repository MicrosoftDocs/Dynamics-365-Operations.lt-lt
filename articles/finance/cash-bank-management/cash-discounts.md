---
title: Mokėjimo nuolaidos
description: Mokėjimo nuolaidos yra nustatomos ir bendrai naudojamos dalyse Mokėtinos sumos ir Gautinos sumos.  Galimą mokėjimo nuolaidą galima nurodyti kliento SF arba tiekėjo SF; ji bus pritaikyta, jei sąskaita faktūra bus apmokėta mokėjimo nuolaidos laikotarpiu.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: roschlom
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d4f6d5bdf4f2fdc4529d9f51515ed2ac4b5b3b5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985317"
---
# <a name="cash-discounts"></a>Mokėjimo nuolaidos

[!include [banner](../includes/banner.md)]

Mokėjimo nuolaidos yra nustatomos ir bendrai naudojamos dalyse Mokėtinos sumos ir Gautinos sumos.  Galimą mokėjimo nuolaidą galima nurodyti kliento SF arba tiekėjo SF; ji bus pritaikyta, jei sąskaita faktūra bus apmokėta mokėjimo nuolaidos laikotarpiu. 

## <a name="cash-discounts"></a>Mokėjimo nuolaidos

Tiek klientų, tiek tiekėjų mokėjimo nuolaidas galima kurti Mokėjimo nuolaidų puslapyje. Taip pat naudodami Kito nuolaidos kodo lauką galite apibrėžti mokėjimo nuolaidų seką, kuri pradedama taikyti baigiant galioti ankstesnėms mokėjimo nuolaidų datoms. Daugiau informacijos rasite toliau šioje temoje, „Pavyzdys: mokėjimo nuolaidų seka‟. Jei SF, kredito operacija (mokėjimas arba kredito pažyma), arba jos abi įvedamos valiuta, kuri skiriasi nuo juridinio subjekto apskaitos valiutos, mokėjimo nuolaida apskaičiuojama naudojant mokėjimo arba kredito pažymos dienos valiutos kursą. Jei SF ir kredito dokumentas įvedami skirtinguose juridiniuose subjektuose, ir jei skiriasi juridinių subjektų apskaitos valiutos, kredito dokumento dienos valiutos kursas paimamas iš SF juridinio subjekto. Daugiau informacijos rasite toliau šioje temoje, „Pavyzdys: mokėjimo nuolaidų valiutos kursai‟.

## <a name="defaulting-order-of-cash-discount-main-account"></a>Numatytasis mokėjimo nuolaidos pagrindinės sąskaitos užsakymo apdorojimas

Jei, norint gauti mokėjimo nuolaidą, SF sudengiama laiku, mokėjimo nuolaida automatiškai registruojama mokėjimo nuolaidos pagrindinėje sąskaitoje pagal toliau nurodytą numatytąjį prioritetą.
1.  Pagrindinė sąskaita, nurodyta lauke Alternatyvi mokėjimo nuolaidos sąskaita, esančiame klientų puslapyje Sudengti atidarytas operacijas arba tiekėjų puslapyje Sudengti atidarytas operacijas.
2.  Pagrindinė sąskaita, nurodyta DK registravimo grupės, priskirtos SF PVM grupei, lauke Kliento mokėjimo nuolaida arba lauke Tiekėjo mokėjimo nuolaida. DK registravimo grupes nustatykite DK registravimo grupių puslapyje ir jas priskirkite PVM kodams PVM kodų puslapyje.
3.  Mokėjimo nuolaidos kodo, esančio sudengtoje SF, pagrindinė registravimo sąskaita Mokėjimo nuolaidų puslapio lauke Pagrindinė sąskaita, skirta kliento nuolaidoms arba lauke Pagrindinė sąskaita, skirta tiekėjo nuolaidoms.
4.  Pagrindinė mokėjimo nuolaidų sąskaita, kaip apibrėžta Automatinių operacijų sąskaitų puslapyje.

## <a name="example-series-of-cash-discounts"></a> Pavyzdys: mokėjimo nuolaidų seka
Nustatykite tris mokėjimo nuolaidos kodus:
-   Kodas 5D10% – 10 proc. mokėjimo nuolaida, jei suma sumokama per 5 dienas.
-   Kodas 10D5% – 5 proc. mokėjimo nuolaida, jei suma sumokama per 10 dienų.
-   Kodas 14D2% – 2 proc. mokėjimo nuolaida, jei suma sumokama per 14 dienų.

Lauke Kitas nuolaidos kodas:
-   Kodui 5D10% pasirinkite 10D5%.
-   Kodui 10D5% pasirinkite 14D2%.
-   Pasirinkę kodą 14D2%, lauką Naujas nuolaidos kodas palikite tuščią.

Mokėjimo datai esant vėlesnei už ankstesnę SF mokėjimo nuolaidos datą, viena po kitos taikomos šios trys mokėjimo nuolaidos. Apmokėjus SF, suteikiama tik viena mokėjimo nuolaida – pagal tai, kuri mokėjimo nuolaidų sekos data patenkinama.

## <a name="example-exchange-rates-for-cash-discounts"></a> Pavyzdys: mokėjimo nuolaidų valiutų kursai
Jūsų juridinio subjekto apskaitos valiuta yra EUR, o toliau pateikti valiutų kursai nurodyti USD.
-   Vasario 1 d. = 110.
-   Kovo 1 d. = 80.

1000 USD SF su 20D2% mokėjimo nuolaidos sąlygomis užregistruojama vasario 15 d. SF apskaitos valiutos suma yra 1100 EUR. 980 USD mokėjimas su SF sudengiamas kovo 1 d. Mokėjimo nuolaidos suma yra 20 USD. Mokėjimo apskaitos valiutos suma yra 784 EUR. Mokėjimo nuolaidos apskaitos valiutos suma apskaičiuojama naudojant kovo 1 d. valiutos kursą: 20 \* 80 / 100 = 16 EUR.

> [!NOTE]
> Jei apskaičiuotos grynųjų pinigų nuolaidos dalinių mokėjimų parinkčiai yra pasirenkami Paskyrų gaunamusoe parametruose ar Paskyrų mokėtinų parametrų puslapiuose, naudojamas kiekvieno mokėjimo dieną galiojantis keitimo kursas. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]