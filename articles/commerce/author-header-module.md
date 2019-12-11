---
title: Antraštės modulis
description: Šioje temoje aprašomi antraštės moduliai ir tai, kaip juos kurti programoje „Microsoft Dynamics 365 Commerce“.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697280"
---
# <a name="header-module"></a>Antraštės modulis

[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]

Šioje temoje aprašomi antraštės moduliai ir tai, kaip juos kurti programoje „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūrėti

Antraštės modulis yra specialus konteineris, kuriame laikomi visi moduliai, kurie bus rodomi puslapio antraštėje. Pavyzdžiui, jame gali būti svetainės logotipas, saitai su naršymo hierarchija, saitai su kitais svetainės puslapiais ir ieškos juosta.

Antraštės modulis automatiškai optimizuojamas įrenginiui, kuriame peržiūrima svetainė (t. y., stacionariam įrenginiui arba mobiliajam įrenginiui). Pavyzdžiui, mobiliajame įrenginyje naršymo juosta sutraukiama į mygtuką **Meniu** (kuris kartais vadinamas *mėsainio stiliaus meniu*).

## <a name="properties-of-a-header"></a>Antraštės ypatybės

Kaip ir bendrieji konteineriai, antraštės modulis palaiko **antraštės** ir **pločio** ypatybes.

Antraštės modulyje yra kelios vietos. Pavyzdžiui, yra vietos informaciniam pranešimui, naršymo meniu, logotipui, ieškos juostai, krepšelio piktogramai, pageidavimų sąrašo piktogramai ir paskyros informacijai. Kiekviena vieta palaiko konkretų modulių rinkinį.

## <a name="modules-that-are-available-in-a-header-module"></a>Moduliai, esantys antraštės modulyje

Antraštės modulyje galima naudoti tolesnius modulius.

- **Naršymo meniu** – naršymo meniu vaizduojama kanalo naršymo hierarchija ir kiti statiniai naršymo saitai. Kanalo naršymo hierarchiją galima konfigūruoti programoje „Dynamics 365 Retail“. Sukonfigūruoti elementai tada rodomi kaip antraštės naršymo elementai. Be to, galima sukonfigūruoti statinius naršymo saitus ir pateikti santykinius saitus su kitais el. prekybos svetainės puslapiais. Pačią antraštę galima lygiuoti kairėje, dešinėje arba centre.
- **Krepšelio piktograma** – krepšelio piktograma yra speciali piktograma, vaizduojanti krepšelį. Ji rodoma antraštėje ir nurodo krepšelyje esančių prekių skaičių. Prie krepšelio piktogramos turėtų būti saitas su krepšelio puslapiu, kad naudodami piktogramą klientai galėtų būti nukreipiami į krepšelio puslapį.
- **Pageidavimų sąrašo piktograma** – pageidavimų sąrašo piktograma rodoma antraštėje ir nurodo prekių, įtrauktų į kliento pageidavimų sąrašą, skaičių. Prie šios piktogramos turėtų būti saitas su pageidavimų sąrašo puslapiu, kad naudodami piktogramą klientai galėtų būti nukreipiami į pageidavimų sąrašą.
- **Prisijungimo modulis** – antraštėje rodomas prisijungimo modulis. Jį naudodami klientai gali prisijungti prie savo paskyros arba registruotis paskyrai. Jei klientas jau prisijungęs, modulį galima sukonfigūruoti taip, kad jame būtų rodomi saitai su paskyros puslapiu, užsakymų retrospektyvos puslapiu ar kitu puslapiu.
- **Logotipo modulis** – šiame modulyje rodomas logotipas, vaizduojantis pardavėją ir prekės ženklą. Tai yra vaizdas su saitu. Saitas paprastai sukonfigūruotas taip, kad nukreiptų į pagrindinį puslapį, todėl klientai gali greitai grįžti į pagrindinį puslapį iš bet kurio svetainės puslapio.
- **Įspėjimas** – antraštėje rodomas įspėjimas, kurį naudojant rodomas įdėtasis pranešimas, taikomas visiems svetainės puslapiams. Pavyzdžiui, įspėjime gali būti rodomas pranešimas, pvz., „Metinis išpardavimas baigiasi už 2 dienų“.
- **Ieškos juosta** – ieškos juostoje vartotojai gali įvesti ieškos terminus, kad galėtų ieškoti produktų. Modulyje reikia sukonfigūruoti ieškos rezultatų puslapio URL. Galima sukonfigūruoti užklausos eilutės parametrą (numatytoji reikšmė yra **q**). Ieškos juostoje yra automatinio siūlymo vieta, kurioje reikia įtraukti automatinio siūlymo modulį.
- **Automatinis siūlymas** – automatinio siūlymo modulyje rodomi automatiškai pasiūlyti rezultatai. Šie rezultatai gali būti raktažodžiai, produktai ar kategorijos, kur randamas ieškos terminas.

## <a name="create-a-header-module"></a>Kurti antraštės modulį

Norėdami sukurti antraštės modulį, atlikite toliau nurodytus veiksmus.

1. Sukurkite puslapio fragmentą, kuriame yra antraštės modulis.
1. Į antraštės modulio vietas įtraukite modulių.
1. Atnaujinkite kiekvieno modulio parametrus.
1. Puslapio fragmentą įrašykite. 
1. Puslapį įrašykite ir atrakinkite bei publikuokite.

Norėdami padėti užtikrinti, kad antraštė būtų rodoma kiekviename puslapyje, kiekviename sukurtame svetainės puslapio šablone atlikite tolesnius veiksmus.

1. Numatytajame puslapyje į pagrindinės vietos antraštę įtraukite puslapio fragmentą, kuriame yra antraštės modulis.
1. Šabloną įrašykite. 
1. Šabloną įrašykite ir atrakinkite bei publikuokite.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Užsakymo patvirtinimo modulis](order-confirmation-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)
