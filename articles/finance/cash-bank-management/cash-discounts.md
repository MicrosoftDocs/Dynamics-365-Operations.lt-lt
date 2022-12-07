---
title: Mokėjimo nuolaidos
description: Mokėjimo nuolaidos yra nustatomos ir bendrai naudojamos dalyse Mokėtinos sumos ir Gautinos sumos.  Galimą mokėjimo nuolaidą galima nurodyti kliento SF arba tiekėjo SF; ji bus pritaikyta, jei sąskaita faktūra bus apmokėta mokėjimo nuolaidos laikotarpiu.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: kfend
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b75637bfb38c13591223ff11be36d958b3972d4f
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804142"
---
# <a name="cash-discounts"></a>Mokėjimo nuolaidos

[!include [banner](../includes/banner.md)]

Mokėjimo nuolaidos yra nustatomos ir bendrai naudojamos dalyse Mokėtinos sumos ir Gautinos sumos. Galimą mokėjimo nuolaidą galima nurodyti kliento SF arba tiekėjo SF; ji bus pritaikyta, jei sąskaita faktūra bus apmokėta mokėjimo nuolaidos laikotarpiu. 

## <a name="cash-discounts"></a>Mokėjimo nuolaidos

Mokėjimo nuolaidas klientams ir tiekėjams galima sukurti mokėjimo **nuolaidų** puslapyje. Taip pat, naudodami lauką Pirmyn **nuolaidos** kodas, galite nustatyti mokėjimo nuolaidų serijas, kurios pavyksta viena po kitos, nes ankstesnės mokėjimo nuolaidos datos baigs galioti. Daugiau informacijos rasite toliau šiame straipsnyje skyriuje "Pavyzdys: Mokėjimo nuolaidų serija". Jei SF, kredito operacija (mokėjimas arba kredito pažyma), arba jos abi įvedamos valiuta, kuri skiriasi nuo juridinio subjekto apskaitos valiutos, mokėjimo nuolaida apskaičiuojama naudojant mokėjimo arba kredito pažymos dienos valiutos kursą. Jei SF ir kredito dokumentas įvedami skirtinguose juridiniuose subjektuose, ir jei skiriasi juridinių subjektų apskaitos valiutos, kredito dokumento dienos valiutos kursas paimamas iš SF juridinio subjekto. Daugiau informacijos rasite toliau šiame straipsnyje skyriuje "Pavyzdys: Mokėjimo nuolaidų valiutos kursai".

## <a name="defaulting-order-of-cash-discount-main-account"></a>Numatytasis mokėjimo nuolaidos pagrindinės sąskaitos užsakymo apdorojimas

Jei, norint gauti mokėjimo nuolaidą, SF sudengiama laiku, mokėjimo nuolaida automatiškai registruojama mokėjimo nuolaidos pagrindinėje sąskaitoje pagal toliau nurodytą numatytąjį prioritetą.
1.  Pagrindinė sąskaita, nurodyta lauke Alternatyvi **mokėjimo nuolaidos sąskaita, kliento**  **atvirų** operacijų sudengimo puslapyje arba tiekėjo atvirų operacijų **sudengimo** puslapyje.
2.  Pagrindinė sąskaita, nurodyta **DK registravimo**  **grupės**, priskirtos SF PVM kodui, lauke Kliento mokėjimo nuolaida arba Tiekėjo mokėjimo nuolaida. Nustatykite DK registravimo grupes DK **registravimo grupių puslapyje** ir priskirkite jas PVM kodams **PVM kodų** puslapyje.
3.  Mokėjimo nuolaidų **puslapio**  **·**  **·**, esančio kliento nuolaidų pagrindinės sąskaitos lauke arba mokėjimo nuolaidos kodo pagrindinės sąskaitos lauke pagrindinė sąskaita, skirta mokėjimo nuolaidos kodui, kuris yra sudengtame SF, pagrindinė sąskaita.
4.  Pagrindinė mokėjimo nuolaidų sąskaita, kaip nurodyta automatinių **operacijų sąskaitų puslapyje** .

## <a name="example-series-of-cash-discounts"></a> Pavyzdys: mokėjimo nuolaidų seka
Nustatykite tris mokėjimo nuolaidos kodus:
-   Kodas 5D10% – 10 proc. mokėjimo nuolaida, jei suma sumokama per 5 dienas.
-   Kodas 10D5% – 5 proc. mokėjimo nuolaida, jei suma sumokama per 10 dienų.
-   Kodas 14D2% – 2 proc. mokėjimo nuolaida, jei suma sumokama per 14 dienų.

Lauke Kita **nuolaidos kodas** :
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
>  **Jei parinktis Skaičiuoti dalinių mokėjimų mokėjimo nuolaidas pasirinkta gautinų sumų parametrų arba mokėtinų sumų parametrų puslapiuose, naudojamas valiutos kursas**  **·**  **·**, kuris galiotų kiekvieno dalinio mokėjimo dieną. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
