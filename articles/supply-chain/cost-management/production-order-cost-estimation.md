---
title: Gamybos užsakymo savikainos įvertinimas
description: Šiame straipsnyje pateikta informacija apie gamybos savikainos įvertinimą. Gamybos savikainos įvertinime pateiktos numatomo prekės gamybos medžiagų ir pajėgumo suvartojimo išlaidos pagal suplanuotą gamybos užsakymo kiekį.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 59b93b41b74bd3f4cc480c8e60e8c69b25e40e51
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830250"
---
# <a name="production-order-cost-estimation"></a>Gamybos užsakymo savikainos įvertinimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikta informacija apie gamybos savikainos įvertinimą. Gamybos savikainos įvertinime pateiktos numatomo prekės gamybos medžiagų ir pajėgumo suvartojimo išlaidos pagal suplanuotą gamybos užsakymo kiekį. 

Sukūrę gamybos užsakymą, turite įvertinti gamybos išlaidas. Tikslas yra įvertinti prekės ir maršruto suvartojimą gamybos proceso metu, nes šie įvertinimai naudojami kaip tolesnio planavimo ir gamybos procesų pagrindas.

## <a name="production-cost-estimation"></a>Gamybos savikainos įvertinimas
Gamybos išlaidų įvertinimas pagrįstas šia informacija:

-   Gamybos užsakymo kiekis
-   Gamybos komplektavimo specifikacijų (KS) komponentai
-   Gamybos maršruto nukreipimo operacijos
-   Netiesioginės išlaidos, taikomos komponentams ir operacijoms
-   Aktyvių išlaidų duomenys, turimi skaičiavimo dieną

Jei gamybos KS yra fiktyvios eilutės prekė, skaičiavimai atspindi fiktyvius komponentus ir maršruto operacijas. Galite naudoti įvertinimo užduotį, norėdami perskaičiuoti įvertintas išlaidas taip, kad jos atspindėtų atnaujintą informaciją. Pvz., atnaujinta informacija gali būti gamybos užsakymo kiekio, gamybos KS komponentų, gamybos maršruto nukreipimo operacijų, netiesioginių išlaidų, taikomų tiems komponentams ir operacijoms, ar aktyviems išlaidų duomenims, turimiems perskaičiavimo dieną, pokyčiai. Be to, įvertintų savikainų skaičiavimai išlaidų ir antkainio sumos būdu gali pateikti gamybos prekės pardavimo kainą. Papildomai įvertintų išlaidų skaičiavimas gali būti taikomas užsakymams nurodyti, kurie atspindi kitus gamybos užsakymus, susietus su tuo gamybos užsakymu.

## <a name="view-the-estimated-costs"></a>Peržiūrėkite įvertintas išlaidas
Atlikę įvertinimą, rezultatus galite peržiūrėti puslapyje **Kainos skaičiavimas**. Įvertinimo metu apskaičiuojamos šios vertės:

-   **Gamybos išlaidos** – gamybos savikaina yra svarbiausia įvertinimo eilutė. Joje pateikiamos visos gamybos užsakymo išlaidos ir bendra pagamintos prekės pardavimo kaina. Tai yra visų įvertinimo savikainos eilučių suma.
-   **Maršruto arba išteklių išlaidos** – maršruto arba išteklių išlaidos yra gamybos operacijų išlaidos. Jos apima nustatymo laiko, vykdymo laiko savikainą ir pridėtines išlaidas.
-   **Medžiagų išlaidos** – medžiagų išlaidos yra komplektavimo specifikacijų (KS) komponentų, reikiamų prekei pagaminti, išlaidos ir kainos. Šios išlaidos buvo iš anksto nustatytos ir įvestos į sistemą.

## <a name="other-uses-of-cost-estimation"></a>Kita savikainos įvertinimo nauda
Savikainos įvertinime taip pat pateikta ši informacija:

-   reikšmingi kainos pasiūlymai;
-   užsakymo pelningumo įvertinimas;
-   žaliavos suvartojimo įvertinimas;
-   ankstesnių gamybos procesų savikainos informacijos palyginimas;
-   biudžeto ir prognozės informaciją;
-   gamybos apimties, kuri reikalinga tam tikrai savikainai išlaikyti, įvertinimas.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]