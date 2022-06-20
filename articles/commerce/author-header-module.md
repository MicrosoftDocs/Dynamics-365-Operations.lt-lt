---
title: Antraštės modulis
description: Šiame straipsnyje aprašomi antraštės moduliai ir aprašoma, kaip kurti puslapių antraštes Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7cd53a57c16c180cb7e8958cc3a6bed1fff0512a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876643"
---
# <a name="header-module"></a>Antraštės modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomi antraštės moduliai ir aprašoma, kaip kurti puslapių antraštes Microsoft Dynamics 365 Commerce.

„Dynamics 365 Commerce” puslapio antraštė sukonfigūruota kaip puslapio fragmentas, į kurį įtraukta antraštė, reklaminė juosta ir sutikimo naudoti slapukus moduliai. 

Antraštės modulyje yra svetainės logotipas, saitai į naršymo hierarchiją, saitai į kitus svetainės puslapius, krepšelio piktogramos modulis, pageidavimų sąrašo simbolis, prisijungimo parinktys ir ieškos juosta. Antraštės modulis automatiškai optimizuojamas įrenginiui, kuriame peržiūrima svetainė (kitais žodžiais, stacionariam įrenginiui arba mobiliajam įrenginiui). Pavyzdžiui, mobiliajame įrenginyje naršymo juosta sutraukiama į mygtuką **Meniu** (kuris kartais vadinamas *mėsainio stiliaus meniu*).

Toliau pateiktame paveikslėlyje parodytas pagrindiniame puslapyje esančio antraštės modulio pavyzdys.

![Antraštės modulio pavyzdys.](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Antraštės modulio ypatybės

Antraštės modulis palaiko ypatybes **Logotipo vaizdas**, **Logotipo saitas** ir **Mano paskyros saitai**. 

Ypatybės **Logotipo vaizdas** ir **Logotipo saitas** naudojamos logotipui puslapyje apibrėžti. Daugiau informacijos žr. [Logotipo pridėjimas](add-logo.md). 

Ypatybę **Mano paskyros saitai** galima naudoti norint apibrėžti paskyros puslapius, kurių sparčiuosius saitus svetainės savininkas nori rodyti antraštėje.

## <a name="modules-that-are-available-within-a-header-module"></a>Moduliai, esantys antraštės modulyje

Antraštės modulyje galima naudoti tolesnius modulius.

- **Naršymo meniu** – naršymo meniu vaizduojama kanalo naršymo hierarchija ir kiti statiniai naršymo saitai. Daugiau informacijos žr. [Naršymo meniu modulis](nav-menu-module.md).

- **Ieška** – ieškos modulyje vartotojai gali įvesti ieškos terminus, kad galėtų ieškoti produktų. Numatytojo ieškos puslapio URL ir ieškos užklausos parametrai turi būti pateikti **Svetainės parametrai \> Plėtiniai**. Ieškos modulyje yra ypatybių, kurios leidžia nerodyti ieškos mygtuko arba pažymėti, kaip pageidaujate. Ieškos modulis taip pat palaiko automatinio pasiūlymo parinktis, pavyzdžiui, produktų, raktažodžių ar kategorijų ieškos rezultatus.

- **Krepšelio piktograma** – krepšelio piktogramos modulis vaizduoja krepšelio piktogramą, rodančią krepšelyje esančių prekių skaičių bet kuriuo metu. Daugiau informacijos žr. [Krepšelio piktogramos modulis](cart-icon-module.md).

- **Svetainės išrinkiklis** – svetainės išrinkiklio modulis leidžia vartotojams naršyti įvairiose iš anksto nustatytose rinkų, regionų ir vietovių svetainėse. Daugiau informacijos žr. [Svetainės išrinkiklio modulis](site-selector.md).

- **Parduotuvės išrinkiklis** – parduotuvės išrinkiklio modulį galima įtraukti į antraštės modulio parduotuvės išrinkiklio vietą. Jis leidžia vartotojams naršyti ir rasti netoliese esančias parduotuves. Vartotojai taip pat gali nurodyti pageidaujamą parduotuvę. Ši parduotuvė bus rodoma antraštėje. Kai parduotuvės išrinkiklio modulis įtraukiamas į antraštės modulį, jo ypatybė **Režimas** turi būti nustatyta į **Rasti parduotuves**. Daugiau informacijos žr. [Parduotuvės išrinkiklio modulis](store-selector.md).

> [!NOTE]
> - Krepšelio piktogramos modulio naudojimo antraštės moduliuose palaikymas pasiekiamas kaip 10.0.11 „Dynamics 365 Commerce” versijos leidimas.
> - Svetainės parinkiklio modulio naudojimo antraštės moduliuose palaikymas pasiekiamas kaip 10.0.14 „Dynamics 365 Commerce” versijos leidimas.
> - Parduotuvės parinkiklio modulio naudojimo antraštės moduliuose palaikymas pasiekiamas kaip 10.0.15 „Dynamics 365 Commerce” versijos leidimas.

## <a name="header-module-in-the-adventure-works-theme"></a>Antraštės modulis „Adventure Works” temoje

„Adventure Works” temoje antraštės modulis palaiko **Mobiliojo logotipo** ypatybę. Ši ypatybė leidžia nurodyti mobiliųjų rodinio prievadų logotipą. **Mobiliojo logotipo** ypatybę galima naudoti kaip modulio apibrėžimo plėtinį.

> [!IMPORTANT]
> „Adventure Works” temą galima naudoti kaip 10.0.20 „Dynamics 365 Commerce” versijos leidimą.

## <a name="create-a-header-fragment-for-a-page"></a>Puslapio antraštės fragmento kūrimas

Norėdami sukurti antraštės fragmentą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas** tam, kad sukurtumėte naują fragmentą.
1. Dialogo lange **Pasirinkti fragmentą** pasirinkite konteinerio **modulį**, įveskite fragmento pavadinimą, tada pasirinkite **Gerai**.
1. Pasirinkite lizdą **Numatytasis konteineris**, tada dešinėje esančioje ypatybių srityje nustatykite ypatybės **Plotis** vertę **Užpildyti ekraną**.
1. Numatytame konteinerio **laiko** atminties atminties lape pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite Modulius **Privatumo sutikimas**,**Antraštė** ir **"Akcijos"** ir tada pasirinkite **Gerai**.
1. Modulio **Reklaminė juosta** ypatybių srityje pasirinkite **Įtraukti pranešimą**, tada pasirinkite **Pranešimas**.
1. Dialogo lange **Pranešimas** įtraukite tekstą ir reklaminio turinio saitų, tada pasirinkite **Gerai**.
1. Modulio **Sutikimas dėl slapukų** ypatybių srityje įtraukite ir konfigūruokite tekstą bei saitą su svetainės privatumo puslapiu.
1. Antraštės modulio **naršymo** meniu atminties atminties meniu pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti** modulius pasirinkite naršymo **meniu modulį** ir pasirinkite **Gerai**.
1. Naršymo meniu modulio ypatybių srityje, dalyje **Naršymo meniu šaltinis**, pasirinkite **„Retail Server“**.
1. Naršymo meniu modulio ypatybių srityje, dalyje **Statiniai meniu elementai**, pasirinkite **Įtraukti meniu elementą**, tada pasirinkite **Meniu elementas**. 
1. Dialogo lango **Meniu elementas** dalyje **Meniu elemento tekstas** įveskite „Kontaktas.”
1. Dialogo lango **Meniu elementas** dalyje **Meniu elemento saito paskirtis** pasirinkite **Įtraukti saitą**.
1. Dialogo lange **Saito įtraukimas** pasirinkite svetainės puslapio „Kontaktas” URL, o tada – **Gerai**.  
1. Dialogo lange **Meniu elementas** pasirinkite **Gerai**.
1. Antraštės modulio **ieškos** atminties atminties dalyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti** modulius pasirinkite Ieškos **modulį**, tada pasirinkite **Gerai**.
1. Ieškos modulio ypatybių srityje pagal poreikį sukonfigūruokite ypatybes.
1. Antraštės modulio **krepšelio** piktogramos atminties srityje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite krepšelio **piktogramos** modulį, tada pasirinkite **Gerai**.
1. Krepšelio piktogramos modulio ypatybių srityje pagal poreikį sukonfigūruokite ypatybes. Jei norite, kad krepšelio piktogramoje būtų rodoma krepšelio santrauka (taip pat žinoma kaip mini krepšelis), kai vartotojai užveda žymeklį, pasirinkite **Rodyti mini krepšelį**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

Norėdami padėti užtikrinti, kad antraštė būtų rodoma kiekviename puslapyje, kiekviename sukurtame svetainės puslapio šablone atlikite tolesnius veiksmus.

1. Modulio **Numatytasis puslapis** vietoje **Antraštė** įtraukite jūsų sukurtą poraštės fragmentą.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Krepšelio piktogramos modulis](cart-icon-module.md)

[Reklaminės juostos modulis](add-alert.md)

[Naršymo meniu modulis](nav-menu-module.md) 

[Sutikimas su slapukais](cookie-consent-module.md)

[Poraštės modulis](author-footer-module.md)

[Svetainės išrinkiklio modulis](site-selector.md)

[Parduotuvės išrinkiklio modulis](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
