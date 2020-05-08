---
title: Poraštės modulis
description: Šioje temoje aprašomi poraštės moduliai ir tai, kaip juos kurti programoje „Dynamics 365 Commerce“.
author: anupamar
manager: annbe
ms.date: 04/14/2020
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 51f8d26d6223dcd1f6961058cd9d772a67c69670
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269641"
---
# <a name="footer-module"></a>Poraštės modulis  


[!include [banner](includes/banner.md)]

Šioje temoje aprašomi poraštės moduliai ir tai, kaip juos kurti programoje „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūrėti

Poraštės modulis yra specialus konteineris, kuriame laikomi moduliai, rodomi puslapio poraštėje. Pavyzdžiui, jame gali būti saitų su įvairiais svetainės puslapiais, pvz., puslapiais **Susisiekite su mumis** ir **Parduotuvės strategijos**.

## <a name="footer-module-properties"></a>Poraštės modulių ypatybės 

Kaip ir dauguma konteinerių, poraštės modulis palaiko antraštės ir pločio ypatybes. Jis taip pat palaiko kelių poraštės kategorijos modulių įtraukimo galimybę. Kiekvienas įtrauktas poraštės kategorijos modulis poraštės modulyje vaizduojamas kaip stulpelis.

## <a name="modules-available-in-a-footer-module"></a>Poraštės modulyje esantys moduliai

**Poraštės elementai** – poraštės elementų modulyje gali būti antraštė, vaizdas ir saitas. Antraštė gali būti naudojama atskirai arba kartu su vaizdu ir saitu. Kiekvieną poraštės saitą galima sukonfigūruoti taip, kad jame būtų tik tekstas (pavyzdžiui, saitai „Susisiekite su mumis“ ir „Privatumas“), arba kad jame būtų ir tekstas, ir vaizdas (pavyzdžiui, socialinės medijos saitai).

**Grįžti į viršų** – grįžimo į viršų modulis suteikia saitą greitai pereiti į puslapio viršų. Būtina paskirties vieta. Numatytoji paskirties vietos reikšmė yra #, kuri vartotoją perkelia į puslapio viršų.

## <a name="author-a-footer-module"></a>Poraštės modulio kūrimas

1. Naršymo srityje pasirinkite **Fragmentai** ir **Naujas puslapio fragmentas**.
1. Dialogo lange **Naujas puslapio fragmentas** pasirinkite poraštės modulį, įveskite puslapio fragmento pavadinimą ir pasirinkite **Gerai**.
1. Kairėje esančiame struktūros medyje pasirinkite prie poraštės modulio esantį daugtaškio mygtuką (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Modulio įtraukimas** pasirinkite poraštės kategorijos modulį ir **Gerai**.
1. Struktūros medyje pasirinkite prie poraštės kategorijos modulio esantį daugtaškio mygtuką, tada – **Įtraukti modulį**.
1. Dialogo lange **Modulio įtraukimas** pasirinkite poraštės elemento modulį ir **Gerai**.
1. Struktūros medyje pasirinkite poraštės elemento modulį. Tada dešinėje esančioje ypatybių srityje pagal poreikį sukonfigūruokite antraštę, saitą ir saito tekstą bei vaizdą.
1. Norėdami įtraukti daugiau poraštės elementų, pakartokite 5–7 veiksmus.
1. Norėdami į poraštę įtraukti saitą „grįžti į viršų“, pasirinkite prie poraštės kategorijos modulio esantį daugtaškio mygtuką, tada – **Įtraukti modulį**.
1. Dialogo lange **Modulio įtraukimas** pasirinkite grįžimo į viršų modulį ir **Gerai**.
1. Struktūros medyje pasirinkite grįžimo į viršų modulį. Tada dešinėje esančioje ypatybių srityje pagal poreikį sukonfigūruokite grįžimo į viršų modulį.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapio fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

Kiekviename sukurtame svetainės puslapio šablone atlikite tolesnius veiksmus.

1. Numatytojo puslapio vietos **Pagrindinis** poraštės modulyje įtraukite sukurtą poraštės fragmentą.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

Puslapio fragmentą įtraukdami į puslapio šablonus, padedate užtikrinti, kad poraštė bus vaizduojama kiekviename puslapyje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Užsakymo patvirtinimo modulis](order-confirmation-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)
