---
title: Antraštės modulis
description: Šioje temoje aprašomi antraštės moduliai ir tai, kaip juos kurti puslapio antraštėse „Microsoft Dynamics 365 Commerce“.
author: anupamar
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261449"
---
# <a name="header-module"></a>Antraštės modulis


[!include [banner](includes/banner.md)]

Šioje temoje aprašomi antraštės moduliai ir tai, kaip juos kurti puslapio antraštėse „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūrėti

„Dynamics 365 Commerce“ puslapio antraštę sudaro keli moduliai, pavyzdžiui, antraštė, naršymo meniu, ieška, reklaminė juosta, sutikimo naudoti slapukus moduliai. 

Antraštės modulyje yra svetainės logotipas, saitai į naršymo hierarchiją, saitai į kitus svetainės puslapius, krepšelio simbolis, pageidavimų sąrašo simbolis, prisijungimo parinktys ir ieškos juosta. Antraštės modulis automatiškai optimizuojamas įrenginiui, kuriame peržiūrima svetainė (kitais žodžiais, stacionariam įrenginiui arba mobiliajam įrenginiui). Pavyzdžiui, mobiliajame įrenginyje naršymo juosta sutraukiama į mygtuką **Meniu** (kuris kartais vadinamas *mėsainio stiliaus meniu*).

## <a name="properties-of-a-header-module"></a>Antraštės modulio ypatybės

Antraštės modulis palaiko ypatybes **Logotipo vaizdas**, **Logotipo saitas** ir **Mano paskyros saitai**. 

Ypatybės **Logotipo vaizdas** ir **Logotipo saitas** naudojamos logotipui puslapyje apibrėžti. Daugiau informacijos žr. [Logotipo pridėjimas](add-logo.md). 

Ypatybę **Mano paskyros saitai** galima naudoti norint apibrėžti paskyros puslapius, kurių sparčiuosius saitus svetainės savininkas nori rodyti antraštėje.

## <a name="modules-that-are-available-in-a-header-module"></a>Moduliai, esantys antraštės modulyje

Antraštės modulyje galima naudoti tolesnius modulius.

- **Naršymo meniu** – naršymo meniu vaizduojama kanalo naršymo hierarchija ir kiti statiniai naršymo saitai. Kanalo naršymo hierarchiją galima konfigūruoti programoje „Dynamics 365 Commerce“. Naršymo meniu turi ypatybę **Naršymo šaltinis**, kuri naudojama norint apibrėžti mažmeninės prekybos serverio naršymo meniu elementus ir statinio meniu elementus kaip šaltinį. Jei statinio meniu elementai apibrėžiami kaip šaltinis, svetainėje gali būti pateikiami susiję saitai į kitus puslapius. Sukonfigūruoti elementai tada rodomi kaip antraštės naršymo elementai. 
- **Ieška** – ieškos modulyje vartotojai gali įvesti ieškos terminus, kad galėtų ieškoti produktų. Numatytojo ieškos puslapio URL ir ieškos užklausos parametrai turi būti pateikti **Svetainės parametrai \> Plėtiniai**. Ieškos modulyje yra ypatybių, kurios leidžia nerodyti ieškos mygtuko arba pažymėti, kaip pageidaujate. Ieškos modulis taip pat palaiko automatinio pasiūlymo parinktis, pavyzdžiui, produktų, raktažodžių ar kategorijų ieškos rezultatus.
- **Krepšelio piktograma** – krepšelio piktogramos modulis vaizduoja krepšelio piktogramą, rodančią krepšelyje esančių prekių skaičių bet kuriuo metu. Daugiau informacijos žr. [Krepšelio piktogramos modulis](cart-icon-module.md).

## <a name="create-a-header-module-for-a-page"></a>Puslapio antraštės modulio kūrimas

Norėdami sukurti antraštės modulį, atlikite toliau nurodytus veiksmus.

1. Sukurkite fragmentą pavadinimu **Antraštės fragmentas** ir į jį įtraukite konteinerio modulį.
1. Konteinerio modulio ypatybių srityje nustatykite ypatybę **Plotis** į **Užpildyti konteinerį**.
1. Į konteinerio modulį įtraukite reklaminę juostą ir sutikimo dėl slapukų modulius.
1. Į fragmentą įtraukite kitą konteinerio modulį ir ypatybę **Plotis** nustatykite į **Užpildyti konteinerį**.
1. Į antrą konteinerio modulį įtraukite antraštę.
1. Antraštės modulio atkarpoje **Naršymo meniu** įtraukite naršymo meniu modulį. 
1. Naršymo meniu modulio ypatybių srityje sukonfigūruokite naršymo meniu modulio ypatybes.
1. Į antraštės modulio atkarpą **Ieška** įtraukite ieškos modulį. 
1. Ieškos meniu modulio ypatybių srityje sukonfigūruokite ieškos modulio ypatybes. 
1. Antraštės modulio vietoje **Krepšelio piktograma** įtraukite krepšelio piktogramos modulį. 
1. Krepšelio piktogramos modulio ypatybių srityje sukonfigūruokite krepšelio piktogramos modulio ypatybes. Jei norite, kad būtų rodomas mažasis krepšelis, kai virš jo užvestas pelės žymiklis, nustatykite parinktį **Rodyti mažąjį krepšelį** į **Teisinga**.
1. Įrašykite puslapio fragmentą, baikite redagavimą ir publikuokite. 


Norėdami padėti užtikrinti, kad antraštė būtų rodoma kiekviename puslapyje, kiekviename sukurtame svetainės puslapio šablone atlikite tolesnius veiksmus.

1. Į numatytojo puslapio atkarpą **Pagrindinis** įtraukite antraštės puslapio fragmentą, kuriame yra antraštės modulis.
1. Įrašykite šabloną, baikite redagavimą ir publikuokite.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Krepšelio piktogramos modulis](cart-icon-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Užsakymo patvirtinimo modulis](order-confirmation-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)
