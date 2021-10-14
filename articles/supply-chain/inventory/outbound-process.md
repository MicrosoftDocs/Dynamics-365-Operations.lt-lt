---
title: Siuntimo proceso apžvalga
description: Šioje temoje apžvelgiamas modulio Atsargų valdymas siuntimo procesas.
author: yufeihuang
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "274363"
- intro-internal
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 27043828b44cf532d0d8d5091324ba30f3f90cf8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578517"
---
# <a name="outbound-process-overview"></a>Siuntimo proceso apžvalga

[!include [banner](../includes/banner.md)]

Šioje temoje apžvelgiamas modulio Atsargų valdymas siuntimo procesas.

## <a name="output-orders"></a>Išeigos užsakymai

Išeigos užsakymai naudojami pardavimo užsakymų eilutėms ir perkėlimo užsakymų eilutėms susieti su siuntimo paėmimo procesais, naudojančiais išrinkimo dokumentus.

Iš pardavimo užsakymų ar perkėlimo užsakymų generuojant išrinkimo dokumentus, automatiškai sukuriami išeigos užsakymai ir siuntos. Išrinkimo dokumentas yra tiesiogiai susijęs su siunta. Siuntoje galima apdoroti perkėlimo užsakymo siuntą arba pardavimo užsakymo važtaraštį. 

Tolesnėje diagramoje apžvelgiamas siunčiamų užsakymų procesas. 

[![Siunčiamų užsakymų proceso apžvalga.](./media/outbound-order.png)](./media/outbound-order.png)

Galite nustatyti siuntimo taisykles, kad apibrėžtumėte, kaip programa turi apdoroti siuntimo procesą. Naudodami šias taisykles galite valdyti siuntimo procesą. Konkrečiai, naudodami šias taisykles galite valdyti, kuriuo proceso etapu galima siųsti siuntą. Tolesniais parametrais apibrėžiama, kaip tvarkomi siuntimo procesai.

## <a name="picking-route-status-for-sales-and-transfer-orders"></a>Pardavimo ir perkėlimo užsakymų išrinkimo maršruto būsena 

Eikite į **Gautinos sumos** \> **Sąranka** \> **Gautinų sumų parametrai**, tada skirtuko **Naujinimai** lauke **Išrinkimo maršruto būsena** pasirinkite reikšmę.

[![Pardavimo užsakymų laukas Išrinkimo maršruto būsena.](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)

Jei laukas **Išrinkimo maršruto būsena** nustatytas kaip **Baigtas**, išrinkimo procesas įvyksta automatiškai, vykstant išrinkimo dokumentų generavimo procesui. Jei laukas nustatytas kaip **Suaktyvintas**, išrinkimo dokumentų eilutes reikia atnaujinti rankiniu būdu.

Ta pati sąranka taikoma perkėlimo užsakymams. Eikite į **Atsargų valdymas** \> **Sąranka** \> **Atsargų ir sandėlio valdymo parametrai**, tada skirtuko **Transportavimas** lauke **Išrinkimo maršruto būsena** pasirinkite reikšmę.

[![Perkėlimo užsakymų laukas Išrinkimo maršruto būsena.](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)

## <a name="end-output-inventory-orders"></a>Išeigos atsargų užsakymų baigimas

Eikite į **Atsargų valdymas** \> **Sąranka** \> **Atsargų ir sandėlio valdymo parametrai**, tada skirtuke **Bendra** nustatykite parinktį **Baigti išeigos atsargų užsakymą**.

[![Parinktis Baigti išeigos atsargų užsakymą.](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)

Sandėlio darbuotojui sumažinus išrinkimo dokumentų kiekį, iš siuntos bus pašalintas atitinkamas atsargų užsakymo kiekis. Tam tikru laiku atnaujinus išrinkimo dokumentą, apie likusį kiekį pranešama užsakyme, jei parinktis **Baigti išeigos atsargų užsakymą** nustatyta į **Taip**. Jei parinktis **Baigti išeigos atsargų užsakymą** nustatyta į **Ne**, likęs kiekis saugomas kaip atviro išeigos užsakymo kiekis ir turi būti įtrauktas į naują išrinkimo dokumentą kaip **Atviri išeigos užsakymai** funkcijos dalis. 

[![Meniu Funkcijos komanda Atviri išeigos užsakymai.](./media/open-output-order.png)](./media/open-output-order.png)

[![Puslapio Atviri išeigos užsakymai meniu Funkcijos.](./media/open-output-order-function.png)](./media/open-output-order-function.png)

## <a name="reduce-quantity"></a>Mažinti kiekį

Trečiasis parametras, kurį galite naudoti išrinkimo dokumentų generavimo proceso metu, yra parametras **Mažinti kiekį**. Nustačius šį parametrą, jis veikia kartu su parametru **Rezervavimas**, kuris išleidimo į sandėlį metu paleidžia rezervavimo procesą.

[![Parametras Mažinti kiekį.](./media/reduce-quantity.png)](./media/reduce-quantity.png)

## <a name="example-of-an-outbound-process-for-a-sales-order"></a>Pardavimo užsakymo siuntimo proceso pavyzdys

Šiame pavyzdyje naudojamas pardavimo užsakymas su dviem prekėmis. Generuodami išrinkimo dokumentą, pasirenkate parametrą **Mažinti kiekį**. Todėl išleidžiate ir sukuriate tik turimų atsargų paėmimo eilutes. Apie paėmimą reikia pranešti naudojant išrinkimo dokumentų registravimo procesą (**Išrinkimo maršruto būsena** = **Suaktyvintas**).

Generuojant išrinkimo dokumentus rezervuojamos dar nerezervuotos atsargos. Neturimas atsargas galima pašalinti iš pardavimo užsakymo arba išleisti į sandėlį, kad siuntimą būtų galima apdoroti vėliau, kai atsargas bus galima paimti.

[![Išrinkimo dokumento naujinimas.](./media/update-picking-list.png)](./media/update-picking-list.png)

Kai tik paimamos visos puslapio **Išrinkimo dokumento registravimas** paėmimo eilutės, susietoji siunta baigiama. Tada pagal paimtas atsargas galima inicijuoti pardavimo užsakymo važtaraščių procesą.

[![Siunčiamų siuntų naujinimas.](./media/outbound-shipments.png)](./media/outbound-shipments.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]