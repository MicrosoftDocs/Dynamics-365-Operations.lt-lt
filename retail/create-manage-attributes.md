---
title: "Atributų kūrimas ir valdymas"
description: "Šiame straipsnyje aprašyti „Microsoft Dynamics 365 for Retail“ atributai. Atributai leidžia apibūdinti produktą ir jo charakteristikas naudojant vartotojo apibrėžiamus laukus."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 4493c2f9e9e9dfe990f3b1670d3cd35e3bbaa38d
ms.contentlocale: lt-lt
ms.lasthandoff: 06/20/2017



---

# <a name="create-and-manage-attributes"></a>Atributų kūrimas ir valdymas

[!include[banner](includes/banner.md)]


Šiame straipsnyje aprašyti „Microsoft Dynamics 365 for Retail“ atributai. Atributai leidžia apibūdinti produktą ir jo charakteristikas naudojant vartotojo apibrėžiamus laukus.

Atributai leidžia apibūdinti produktą ir jo charakteristikas naudojant vartotojo apibrėžiamus laukus. Pavyzdžiui, galite nurodyti produkto atminties dydį ir kietojo disko talpą ir nurodyti, ar produktas atitinka „Energy Star“ reikalavimus. Atributus galima susieti su įvairiais mažmeninės prekybos objektais, pavyzdžiui, produkto kategorijomis ir mažmeninės prekybos kanalais, ir galima nustatyti jį numatytąsias reikšmes. Produktai perima atributus ir tų atributų numatytąsias reikšmes, jei jie yra susieti su produktų kategorijomis arba mažmeninės prekybos kanalais. Numatytųjų reikšmių galima nepaisyti atskiro produkto lygiu, mažmeninės prekybos kanalo lygiu arba mažmeninės prekybos kataloge.

#### <a name="examples"></a>Pavyzdžiai

| Kategorija   | Atributas                | Leistinos reikšmės          | Numatytoji vertė |
|------------|--------------------------|-----------------------------|---------------|
| TV ir vaizdo įrašai | Rūšis                    | Bet kuri tinkama reikšmė Prekės ženklas       | Joks          |
| TV         | Ekrano dydis              | 20–80 col.                     | Joks          |
| TV         | Vertikali skiriamoji geba      | 480 i, 720 p, 1080 i arba 1080 p | 1080 p         |
| TV         | Ekrano naujinimo dažnis      | 60 hz, 120 hz arba 240 hz       | 60 hz          |
| TV         | HDMI įvestys              | 0–10                        | 3             |
| TV         | DVI įvestys               | 0–10                        | 1             |
| TV         | Sudėtinės įvestys         | 0–10                        | 2             |
| TV         | Komponento įvestys         | 0–10                        | 1             |
| LCD        | 3D parengta                 | Taip arba Ne                   | Taip           |
| LCD        | 3D įgalinta               | Taip arba Ne                   | Nr.            |
| Plazminis     | Veiklos šablonas nuo      | 32–110 laipsnių              | 32            |
| Plazminis     | Veiklos šablonas iki        | 32–110 laipsnių              | 100           |
| Projekcinis | Projekcijos vamzdelio garantija | 6, 12 arba 18 mėnesiai (-ių)         | 12            |
| Projekcinis | Projekcijos vamzdelių skaičius    | 1–5                         | 3             |


## <a name="attribute-type"></a>Atributo tipas
  [![attributes-fixed-copy](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) 
  
Atributai pagrįsti atributų tipais. Atributų tipai nurodo, kokio tipo konkretaus atributo duomenis galima įvesti. Šiuo metu „Microsoft Dynamics 365 for Retail“ palaiko šiuos atributų tipus.

-   **Valiuta** – šis atributo tipas palaiko valiutos reikšmes. Jis gali būti apribotas (t. y., gali būti palaikomas reikšmių diapazonas), arba jis gali būti neapibrėžtas.
-   **Data ir laikas** – šis atributo tipas palaiko datos ir laiko reikšmes. Jis gali būti apribotas (t. y., gali būti palaikomas verčių diapazonas), arba jis gali būti neapibrėžtas.
-   **Dešimtainis skaičius** – šis atributo tipas palaiko skaitines reikšmes, kuriose yra dešimtainio skyriklio vietų. Jis taip pat palaiko matavimo vienetus. Jis gali būti apribotas (t. y., gali būti palaikomas reikšmių diapazonas), arba jis gali būti neapibrėžtas.
-   **Sveikasis skaičius** – šis atributo tipas palaiko skaitines reikšmes. Jis taip pat palaiko matavimo vienetus. Jis gali būti apribotas (t. y., gali būti palaikomas verčių diapazonas), arba jis gali būti neapibrėžtas.
-   **Tekstas** – šis atributo tipas palaiko teksto reikšmes. Jis taip pat palaiko iš anksto apibrėžtąjį galimų reikšmių rinkinį (išvardijimą).
-   **Bulio logika** – šis atributo tipas palaiko dvejetaines reikšmes (**teisinga** / **klaidinga**).
-   **Nuoroda**.

## <a name="attribute"></a>Atributas
  [![createandmanageattribute-8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png) Be pavadinimo, patogaus pavadinimo, aprašo ir žinyno teksto, galima įrašyti vieną ar daugiau iš šių atributo informacijos tipų.

-   Numatytoji reikšmė
-   Atributo metaduomenys, pavyzdžiui, metaduomenys, kurie nurodo, ar atributo galima ieškoti, ar galima jį patikslinti arba surūšiuoti

## <a name="attribute-group"></a>Atributų grupė
  [![createandmanageattribute-10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) Apibrėžus atributus, juos galima sugrupuoti į atributų grupes. Atributų grupėse pateikiami sugrupuoti atskiri atributai, ir jas galima priskirti mažmeninės prekybos kategorijoms arba mažmeninės prekybos kanalams.

## <a name="assigning-attribute-groups-to-retail-categories"></a>Atributų grupių priskyrimas mažmeninės prekybos kategorijoms
  [![createandmanageattribute-12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) Vieną ar kelias atributų grupes galima susieti su mažmeninės prekybos produktų kategorijų hierarchijos kategorijų mazgais. Suskirsčius produktus, jie perima atributus, įtrauktus į atributų grupes.

## <a name="assigning-attribute-groups-to-retail-stores"></a>Atributų grupių priskyrimas mažmeninės prekybos parduotuvėms
  [![createandmanageattribute-13-1024x576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) Vieną ar kelias atributų grupes galima susieti su viena ar keliomis mažmeninės prekybos parduotuvių hierarchijos mažmeninės prekybos parduotuvėmis. Produktais konkrečias mažmeninės prekybos parduotuves, jie perima atributus, įtrauktus į atributų grupes.

## <a name="overriding-attribute-values"></a>Atributo reikšmių nepaisymas
### <a name="at-the-product-level"></a>Produkto lygiu

  [![createandmanageattribute-14-1024x576](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) Atributų numatytųjų reikšmių galima nepaisyti produkto lygiu (t. y. atskirų produktų).

### <a name="in-a-retail-catalog"></a>Mažmeninės prekybos kataloge

  [![createandmanageattribute-2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) Galima nepaisyti konkrečių katalogų, skirtų konkretiems mažmeninės prekybos kanalams, atskirų produktų atributų numatytųjų reikšmių.

### <a name="at-the-retail-channel-level"></a>Mažmeninės prekybos kanalo lygiu

  [![createandmanageattribute-1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) Galima nepaisyti konkrečių katalogų, skirtų konkretiems mažmeninės prekybos kanalams, atskirų produktų atributų numatytųjų reikšmių.




