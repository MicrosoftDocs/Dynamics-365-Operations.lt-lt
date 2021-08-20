---
title: Įsigijimas
description: Šioje temoje aiškinama apie įsigijimą skiltyje Turto valdymas.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderPurchaseListPagePreviewPane, EntAssetWorkOrderPurchaseListPage, EntAssetWorkOrderPurchaseLineAmountInfoPart, EntAssetWorkOrderPurchReqListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2b5e160beb4743db2530b91020f21b686d84237b17cfa7ff7f0cc1da97695d08
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743655"
---
# <a name="procurement"></a>Įsigijimas

[!include [banner](../../includes/banner.md)]

Turto valdyme galite peržvelgti pirkimo paraiškas ir pirkimo užsakymus, susijusius su darbo užsakymais. Taip pat galite sukurti pirkimo užsakymą arba pirkimo paraišką iš darbo užsakymo.

Sąrašo puslapyje **Darbo užsakymo pirkimo paraiška** (**Turto valdymas** > **Bendrieji dalykai** > **Įsigijimas** > **Darbo užsakymo pirkimo paraiška**) rodomas pirkimo paraiškų, susijusių su darbo užsakymais, sąrašas. Šiame puslapyje pasirinkę darbo užsakymo užduotį, norėdami atlikti įvairius veiksmus, galite naudoti mygtukus grupėje **Rodyti**, esančioje veiksmų srities skirtuke **Darbo užsakymo pirkimo paraiška**.

- Norėdami atidaryti susijusią pirkimo paraišką, pasirinkite **Pirkimo paraiška**. 
- Norėdami atidaryti susijusį darbo užsakymą, pasirinkite **Darbo užsakymas**.
- Jei norite apžvelgti, kur naudojama prekė pasirinktoje eilutėje atsižvelgiant į turtą, priežiūros užduoties tipo numatytąsias reikšmes, atsargines dalis ir darbo užsakymus turto valdyme, pasirinkite **Kur naudota prekė**. Daugiau informacijos apie šią apžvalgą žr. [Kur naudota prekė](../controlling-and-reporting/item-where-used.md).

Toliau pateiktame paveikslėlyje parodytas sąrašo puslapio **Darbo užsakymo pirkimo paraiška** pavyzdys.

![1 iliustracija.](media/08-work-orders.png)


Sąrašo puslapyje **Darbo užsakymo pirkimas** (**Turto valdymas** > **Bendrieji dalykai** > **Įsigijimas** > **Darbo užsakymo pirkimas**) rodomas pirkimo užsakymų, susijusių su darbo užsakymais, sąrašas. Šiame puslapyje pasirinkę darbo užsakymo užduotį, norėdami atlikti įvairius veiksmus, galite naudoti mygtukus grupėje **Rodyti**, esančioje veiksmų srities skirtuke **Darbo užsakymo pirkimas**.

- Norėdami atidaryti susijusį pirkimo užsakymą, pasirinkite **Pirkimo užsakymas**. 
- Norėdami atidaryti susijusį darbo užsakymą, pasirinkite **Darbo užsakymas**.
- Jei norite apžvelgti, kur naudojama prekė pasirinktoje eilutėje atsižvelgiant į turtą, priežiūros užduoties tipo numatytąsias reikšmes, atsargines dalis ir darbo užsakymus turto valdyme, pasirinkite **Kur naudota prekė**. Daugiau informacijos apie šią apžvalgą žr. [Kur naudota prekė](../controlling-and-reporting/item-where-used.md).

Toliau pateiktame paveikslėlyje parodytas sąrašo puslapio **Darbo užsakymo pirkimas** pavyzdys.

![2 iliustracija.](media/09-work-orders.png)


Tiek sąrašo puslapyje **Darbo užsakymo pirkimas**, tiek sąrašo puslapyje **Darbo užsakymo pirkimo paraiška** su pristatymo datos valdymu susijęs simbolis rodomas dešinėje kiekvienos eilutės pusėje. Jei šis simbolis yra šauktukas raudoname apskritime, susijęs su pirkimo užsakymu arba pirkimo paraiška pristatymas gali vėluoti.

Pirkimo užsakymo atveju galimai delsai apskaičiuoti naudojama data, susijusi su pirkimo užsakymo eilute. Norėdami peržiūrėti šią datą, puslapyje **Pirkimo užsakymas** pasirinkite pirkimo užsakymo eilutę. Data rodoma lauke **Patvirtinta pristatymo data**, esančiame skirtuke **Sąranka**, kuris yra „FastTab“ **Eilutės informacija**. Jei laukas **Patvirtinta pristatymo data** nenustatytas, skaičiuojant naudojamas laukas **Pristatymo data**, esantis „FastTab“ **Pirkimo užsakymo antraštė**. Viena iš šių datų lyginama su galima data darbo užsakyme arba darbo užsakymo užduotyje šia tvarka:

1. Darbo užsakymo faktinis pradžios laikas  

2. Suplanuota pradžios data susijusioje darbo užsakymo užduotyje 

3. Suplanuota pradžios data darbo užsakyme 

4. Numatoma pradžios data darbo užsakyme 

Dirbant su pirkimo paraiška, galimai delsai apskaičiuoti naudojamas laukas **Pageidaujama data**, esantis „FastTab“ **Pirkimo paraiškos antraštė**, kuris yra puslapyje **Pirkimo paraiškos**. Šiame lauke nurodyta data lyginama su prieinama data darbo užsakyme arba darbo užsakymo užduotyje tokiu pačiu būdu kaip ir pirkimo užsakymo data.


## <a name="create-a-purchase-order-from-a-work-order"></a>Kurkite pirkimo užsakymą iš darbo užsakymo

Sąrašo puslapyje **Visi darbo užsakymai** galite pasirinkti darbo užsakymo užduotį ir sukurti susijusį pirkimo užsakymą arba susijusią pirkimo paraišką. Tokiu būdu užtikrinsite projekto ryšius tarp pirkimo užsakymo arba pirkimo paraiškos ir darbo užsakymo.

1. Pasirinkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Pasirinkite darbo užsakymą, kad sukurtumėte pirkimo užsakymą, o tada pasirinkite **Redaguoti**.

3. „FastTab“ **Darbo užsakymo priežiūros užduotys** pasirinkite darbo užsakymo užduotį, kuriai norite sukurti pirkimo užsakymą.

4. Pasirinkite **Elemento užduotys** > **Pirkimo užsakymas iš darbo užsakymo užduoties**.

5. Sąrašo puslapyje **Projekto pirkimo užsakymai** spustelėkite **Naujas**.

6. Sukurkite pirkimo užsakymą.

>[!NOTE]
>Norėdami sukurti susijusią pirkimo paraišką, atlikite tuos pačius veiksmus. Tačiau atlikdami 4 veiksmą pasirinkite **Elemento užduotys** > **Pirkimo paraiška iš darbo užsakymo užduoties**.


## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Projekto ryšys tarp darbo užsakymo ir pirkimo užsakymo arba pirkimo paraiškos

Pirkimo užsakymo eilutė arba pirkimo paraiškos eilutė yra susijusi su darbo užsakymo užduoties projektu ir susijusio projekto veiklos numeriu. Kai kuriate pirkimo užsakymą arba pirkimo paraišką iš darbo užsakymo užduoties, susijusio projekto veiklos numeris yra privalomas. Jei visos susijusiame darbo užsakyme esančios darbo užsakymo užduotys yra to paties priežiūros užduoties tipo, projekto veiklos numeris automatiškai įterpiamas į pirkimo užsakymą arba pirkimo paraišką. Jei darbo užsakymo užduotys yra skirtingų priežiūros užduoties tipų, projekto veiklos numerį turite rankiniu būdu įvesti į pirkimo užsakymą arba pirkimo paraišką.

Norėdami peržiūrėti arba įvesti veiklos numerį, susijusį su pirkimo užsakymo eilute, sąrašo puslapyje **Darbo užsakymo pirkimas** pasirinkite pirkimo užsakymo įrašą, tada stulpelyje **Pirkimo užsakymas** pasirinkite pirkimo užsakymo saitą. Lauką **Veiklos numeris** galite rasti skirtuke **Projektas**, esančiame „FastTab“ **Eilutės informacija**.

Toliau esančiame paveikslėlyje pateiktas puslapio **Pirkimo užsakymas** pavyzdys pažymėjus **Veiklos numeris**.

![3 iliustracija.](media/10-work-orders.png)

Atitinkamai, norėdami peržiūrėti arba įvesti veiklos numerį, susijusį su darbo užsakymo pirkimo paraiška, sąrašo puslapyje **Darbo užsakymo pirkimo paraiška** pasirinkite pirkimo paraiškos įrašą, tada stulpelyje **Pirkimo paraiška** pasirinkite pirkimo paraiškos saitą. Lauką **Veiklos numeris** galite rasti skirtuke **Projektas**, esančiame „FastTab“ **Eilutės informacija**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]