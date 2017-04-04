---
title: "Atributų kūrimas ir valdymas"
description: "Šiame straipsnyje aprašoma atributus Microsoft Dynamics 365 operacijoms. Atributai leidžia apibūdinti produktą ir jo charakteristikas naudojant vartotojo apibrėžiamus laukus."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 26c628e10aaa5f47bc87d7510ca8f41ab3630204
ms.lasthandoff: 03/31/2017


---

# <a name="create-and-manage-attributes"></a>Atributų kūrimas ir valdymas

Šiame straipsnyje aprašoma atributus Microsoft Dynamics 365 operacijoms. Atributai leidžia apibūdinti produktą ir jo charakteristikas naudojant vartotojo apibrėžiamus laukus.

Atributai leidžia apibūdinti produktą ir jo charakteristikas naudojant vartotojo apibrėžiamus laukus. Pavyzdžiui, galite nurodyti produkto atminties dydį ir kietojo disko talpą ir nurodyti, ar produktas atitinka „Energy Star“ reikalavimus. Atributus galima susieti su įvairiais mažmeninės prekybos objektais, pavyzdžiui, produkto kategorijomis ir mažmeninės prekybos kanalais, ir galima nustatyti jį numatytąsias reikšmes. Produktai perima atributus ir tų atributų numatytąsias reikšmes, jei jie yra susieti su produktų kategorijomis arba mažmeninės prekybos kanalais. Numatytųjų reikšmių galima nepaisyti atskiro produkto lygiu, mažmeninės prekybos kanalo lygiu arba mažmeninės prekybos kataloge.

#### <a name="examples"></a>Pavyzdžiai

Kategorija

Atributas

Leistinos reikšmės

Numatytoji reikšmė

TV ir vaizdo įrašai

Rūšis

Bet kuri tinkama reikšmė **Prekės ženklas**

Nėra

TV

Ekrano dydis

**20"**–**80"**

Nėra

Vertikali skiriamoji geba

**480 i**, **720 p**, **1080 i** arba **1080 p**

**1080 p**

Ekrano naujinimo dažnis

**60 hz**, **120 hz** arba **240 hz**

**60 hz**

HDMI įvestys

**0**–**10**

**3**

DVI įvestys

**0**–**10**

**1**

Sudėtinės įvestys

**0**–**10**

**2**

Komponento įvestys

**0**–**10**

**1**

LCD

3D parengta

**Taip** arba **Ne**

**Taip**

3D įgalinta

**Taip** arba **Ne**

**Ne**

Plazminis

Veiklos šablonas nuo

**32**–**110** laipsnių

**32**

Veiklos šablonas iki

**32**–**110** laipsnių

**100**

Projekcinis

Projekcijos vamzdelio garantija

**6**, **12** arba **18** mėnesiai (-ių)

**12**

\#Projekcijos vamzdžių

**1**–**5**

**3**

## <a name="attribute-type"></a>Atributo tipas
  [![atributų nustatytas kopija](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) atributai yra pagrįstos atributų tipų. Atributų tipai nurodo, kokio tipo konkretaus atributo duomenis galima įvesti. Šiuo metu Microsoft Dynamics 365 operacijoms palaiko šių atributų tipų:

-   **Valiuta** – šis atributo tipas palaiko valiutos reikšmes. Jis gali būti apribotas (t. y., gali būti palaikomas reikšmių diapazonas), arba jis gali būti neapibrėžtas.
-   **Data ir laikas** – šis atributo tipas palaiko datos ir laiko reikšmes. Jis gali būti apribotas (t. y., gali būti palaikomas verčių diapazonas), arba jis gali būti neapibrėžtas.
-   **Dešimtainis skaičius** – šis atributo tipas palaiko skaitines reikšmes, kuriose yra dešimtainio skyriklio vietų. Jis taip pat palaiko matavimo vienetus. Jis gali būti apribotas (t. y., gali būti palaikomas reikšmių diapazonas), arba jis gali būti neapibrėžtas.
-   **Sveikasis skaičius** – šis atributo tipas palaiko skaitines reikšmes. Jis taip pat palaiko matavimo vienetus. Jis gali būti apribotas (t. y., gali būti palaikomas verčių diapazonas), arba jis gali būti neapibrėžtas.
-   **Tekstas** – šis atributo tipas palaiko teksto reikšmes. Jis taip pat palaiko iš anksto apibrėžtąjį galimų reikšmių rinkinį (išvardijimą).
-   **Bulio logikos** – Šis atributas tipas palaiko dviejų komponentų vertes (**tiesa**/**klaidinga**).
-   **Nuoroda**.

## <a name="attribute"></a>Atributas
  [![createandmanageattribute-8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png) be pavadinimo, įsimenamas pavadinimas, aprašymas, ir žinyno tekstas, viena ar daugiau iš šių tipų informaciją gali būti užfiksuoti atributą:

-   Numatytoji reikšmė
-   Atributo metaduomenys, pavyzdžiui, metaduomenys, kurie nurodo, ar atributo galima ieškoti, ar galima jį patikslinti arba surūšiuoti

## <a name="attribute-group"></a>Atributų grupė
  [![createandmanageattribute-10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) apibrėžus atributus, jie galima suskirstyti į atributas grupes. Atributų grupėse pateikiami sugrupuoti atskiri atributai, ir jas galima priskirti mažmeninės prekybos kategorijoms arba mažmeninės prekybos kanalams.

## <a name="assigning-attribute-groups-to-retail-categories"></a>Atributų grupių priskyrimas mažmeninės prekybos kategorijoms
  [![createandmanageattribute-12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) vienai ar kelioms atributas grupėms gali būti susijęs su kategorija mazgų mažmeninės prekybos produkto kategorijos hierarchija. Suskirsčius produktus, jie perima atributus, įtrauktus į atributų grupes.

## <a name="assigning-attribute-groups-to-retail-stores"></a>Atributų grupių priskyrimas mažmeninės prekybos parduotuvėms
  [![createandmanageattribute-13-1024 x 576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) vienai ar kelioms atributas grupėms gali būti susijęs su viena ar daugiau mažmeninės prekybos parduotuvėse hierarchijoje mažmeninės prekybos parduotuvėse. Produktais konkrečias mažmeninės prekybos parduotuves, jie perima atributus, įtrauktus į atributų grupes.

## <a name="overriding-attribute-values"></a>Atributo reikšmių nepaisymas
### <a name="at-the-product-level"></a>Produkto lygiu

  [![createandmanageattribute-14-1024 x 576](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) pagal nutylėjimą atributai gali būti svarbesni produkto lygmeniu (t. y. atskirų produktų).

### <a name="in-a-retail-catalog"></a>Mažmeninės prekybos kataloge

  [![createandmanageattribute-2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) pagal nutylėjimą atributai gali būti viršesni už atskirų produktų konkrečius katalogus, kuri yra skirta tikriems mažmeninės prekybos kanalų.

### <a name="at-the-retail-channel-level"></a>Mažmeninės prekybos kanalo lygiu

  [![createandmanageattribute-1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) pagal nutylėjimą atributai gali būti viršesni už atskirų produktų konkrečius katalogus, kuri yra skirta tikriems mažmeninės prekybos kanalų.


