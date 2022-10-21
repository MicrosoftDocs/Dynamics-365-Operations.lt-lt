---
title: Registruoti naudojant išvestines knygas
description: Šiame straipsnyje aprašyta, kaip naudoti išvestines knygas.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0270ad1e66193832fb1139fca4439b36b5ffb84
ms.sourcegitcommit: dca54dd3afc7c94795d89c63050b105df2c48e3f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/15/2022
ms.locfileid: "9682913"
---
# <a name="post-with-derived-books"></a>Registruoti naudojant išvestines knygas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašyta, kaip naudoti išvestines knygas.

Registruojant knygos, kuriai yra priskirtų išvestinių knygų, operacijas, išvestinės knygos operacijos automatiškai užregistruojamos žurnaluose, pirkimo užsakymuose arba laisvos formos SF. Tačiau, jei pagrindinės knygos operacijas ruošiate žurnale Ilgalaikis turtas, išvestinių nusidėvėjimo operacijų sumas galite peržiūrėti ir modifikuoti prieš jas užregistruodami.
-   Tam tikros sąskaitos, pavyzdžiui, PVM ir kliento arba tiekėjo sąskaitos, atnaujinamos tik kartą registruojant pagrindinę knygą. Išvestinės knygos operacijos registruojamos sąskaitose, kurios išvestinei knygai buvo nurodytos puslapyje Ilgalaikio turto registravimo šablonai.
-   Įsigijimas dažnai naudojamas kaip išvestinių knygų operacijų tipas. Naudokite tai, kai knyga ir išvestinė nusidėvėjimo knyga turėtų būti taikomos ilgalaikiam turtui nuo tada, kai ilgalaikis turtas buvo įsigytas.
-   Operacijų tipui taip pat gali būti taikomos kitos vertės. Pavyzdžiui, jei pagrindinė knyga ir išvestinė knyga turi tuos pačius intervalus atsižvelgiant į pardavimą ar likvidavimą, visus ilgalaikio turto operacijos tipus galima nustatyti išvestinėje knygoje.

> [!WARNING]
> Išvestinėje knygoje užregistruotas nusidėvėjimas bus išreikštas ta pačia suma, kokia buvo užregistruota pagrindinėje knygoje. Jei skirtingų knygų nusidėvėjimo metodai yra skirtingi, neturėtumėte generuoti nusidėvėjimo operacijų naudodami išvestinius procesus. 

## <a name="example"></a>Pavyzdys 
Toliau pateikiama informacija apie tai, kaip įsigijimo operacijas nustatyti naudojant išvestinės knygos funkciją.

1.  Kurkite knygas puslapyje Knygos.
    -   Apskaitos knyga: VM 1, dabartinis registravimo sluoksnis
    -   Apskaitos knyga mokesčiams: VM 2, mokesčių registravimo sluoksnis

2.  VM 1 spustelėkite skirtuką Išvestinės knygos. Lauke Knyga pasirinkite VM 2, o lauke Operacijos tipas pasirinkite Įsigijimas.

Tada knygas galima pridėti prie konkretaus ilgalaikio turto. 

Kai ilgalaikio turto įsigijimas užregistruojamas naudojant knygą VM 1, įsigijimas užregistruojamas ne tik vertinimo modelyje VM 1, bet ir išvestinėje knygoje VM 2. Abiejų ilgalaikio turto knygų būsena atnaujinama į Atidaryta.

> [!NOTE]                                                                                                         
> Jei išvestinių knygų nenaudojate, ilgalaikio turto įsigijimą turite registruoti ir knygoje VM 1, ir knygoje VM 2.

Daugiau informacijos ieškokite [Išvestinės knygos](derived-books.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
