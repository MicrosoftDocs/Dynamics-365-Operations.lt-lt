---
title: "Apibrėžti mažmeninės prekybos komunikacijas („Commerce Data Exchange‟)"
description: "Šiame straipsnyje pateikiama „Commerce Data Exchange“ ir jos komponentų apžvalga. Jame paaiškinama kiekvieno komponento atliekama dalis perkeliant duomenis tarp „Microsoft Dynamics 365 for Operations“ ir mažmeninės prekybos kanalų."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: ba1bb54a29250a2bb59622ee4391b64ac455af33
ms.contentlocale: lt-lt
ms.lasthandoff: 04/26/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Apibrėžti mažmeninės prekybos komunikacijas („Commerce Data Exchange‟)

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikiama „Commerce Data Exchange“ ir jos komponentų apžvalga. Jame paaiškinama kiekvieno komponento atliekama dalis perkeliant duomenis tarp „Microsoft Dynamics 365 for Operations“ ir mažmeninės prekybos kanalų.

<a name="overview"></a>Apžvalga
--------

„Commerce Data Exchange‟ yra sistema, kuri perkelia duomenis tarp „Dynamics 365 for Operations‟ ir mažmeninės prekybos kanalų, pvz., interneto parduotuvių ar fizinių parduotuvių. Duomenų bazė, kurioje saugomi mažmeninės prekybos kanalo duomenys, skiriasi nuo „Dynamics 365 for Operations‟ duomenų bazės. Kanalų duomenų bazėje saugomi tik tie duomenys, kurių reikia vykdant mažmeninės prekybos operacijas. Bendrieji duomenys konfigūruojami programoje „Dynamics 365 for Operations‟ ir platinami kanalams. Operacijų duomenys kuriami elektroninio kasos aparato (EKA) sistemoje ar interneto parduotuvėje, o tada įkeliami į „Dynamics 365 for Operations‟. Duomenų paskirstymas yra asinchroninis. Kitaip tariant, duomenų rinkimo ir pakavimo šaltinyje procesas vyksta atskirai nuo duomenų gavimo ir taikymo paskirties vietoje proceso. Kai kuriais scenarijais, pvz., peržvelgiant kainą ir atsargas, duomenis reikia gauti realiu laiku. Siekiant palaikyti šiuos scenarijus, „Commerce Data Exchange‟ modulyje taip pat yra paslauga, kuri leidžia realiu laiku komunikuoti tarp „Dynamics 365 for Operations‟ ir kanalo. 

[![updated-retail-graphic](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>„Async“ paslauga
„Microsoft SQL Server‟ keitimų sekimas „Dynamics 365 for Operations‟ duomenų bazėje naudojamas nustatyti duomenų pakeitimams, kuriuos reikia siųsti kanalams. Pagal paskirstymo grafiką „Dynamics 365 for Operations‟ tuos duomenis supakuoja ir įrašo į pagrindinę saugyklą („Azure‟ didelių dvejetainių objektų saugyklą). Atskiras paketinis procesas „Commerce Data Exchange: Async‟ kliento biblioteką naudoja šiam duomenų paketui įterpti į kanalo duomenų bazę. 

[![„Async“ paslauga](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Duomenų apsikeitimo valdymas

Duomenų apsikeitimo valdymo užduotys yra mechanizmas, skirtas duomenims į vietas ir iš jų paskirstyti. Užduotis sudaro antrinės užduotys, kurios nurodo lenteles ir lentelių laukus, kuriuose yra skirstytini duomenys. Programoje „Dynamics 365 for Operations‟ pateikiamos iš anksto apibrėžtos duomenų apsikeitimo valdymo užduotys ir antrinės užduotys, atitinkančios daugumos organizacijų dubliavimo reikalavimus. Kuriami tolesni iš anksto apibrėžtų užduočių tipai.

-   **Atsisiuntimo užduotys** – atsisiuntimo užduotys duomenis, kurie pasikeitė nuo „Dynamics 365 for Operations‟, siunčia kanalų duomenų bazėms. Įrašų modifikacijos sekamos naudojant „SQL Server‟ keitimų sekimą.
-   **Įkėlimo užduotys (P užduotys)** – įkėlimo užduotys pardavimo operacijas iš kanalo perkelia į „Dynamics 365 for Operations‟ duomenų bazę. P užduotys duomenis įkelia palaipsniui. Kai vykdoma P užduotis, „Async‟ kliento biblioteka dublikatų skaitiklyje tikrina, ar nėra įrašų, kurie jau gauti iš vietos. Įrašas įkeliamas tik tada, jei jo dublikatų skaitiklis yra didesnis už didžiausią rastą reikšmę. P užduotys neatnaujina anksčiau įkeltų duomenų.

Paskirstymo grafikas naudojamas vykdyti duomenų perdavimui – rankiniu būdu arba planuojant paketinę užduotį programoje „Dynamics 365 for Operations‟. Paskirstymo grafike gali būti viena ar kelios kanalo duomenų grupės ir viena ar kelios duomenų apsikeitimo valdymo užduotys.

## <a name="realtime-service"></a>Realtime Service
„Commerce Data Exchange: Real-time Service“ yra integruotoji tarnyba, leidžianti realiu laiku palaikyti ryšį tarp „Dynamics 365 for Operations‟ ir mažmeninės prekybos kanalų. „Real-time Service‟ leidžia atskiriems POS kompiuteriams ir interneto parduotuvėms realiu laiku gauti konkrečius duomenis iš „Dynamics 365 for Operations‟. Nors daugumą pagrindinių operacijų galima atlikti vietinėje kanalo duomenų bazėje, tolesniais scenarijais reikia tiesioginės prieigos prie duomenų, kurie yra saugomi programoje „Dynamics 365 for Operations‟.

-   Dovanų kortelių išdavimas ir panaudojimas.
-   Lojalumo taškų panaudojimas.
-   Kredito pažymų išdavimas ir panaudojimas.
-   Klientų įrašų kūrimas ir naujinimas.
-   Pardavimo užsakymų kūrimas, naujinimas ir atlikimas.
-   Atsargų gavimas pagal pirkimo užsakymą ar perkėlimo užsakymą.
-   Atsargų skaičiavimas.
-   Pardavimo operacijų gavimas parduotuvėse ir grąžinimo operacijų atlikimas.

[![Real-time Service](./media/rts.png)](./media/rts.png) 

Sukuriamas iš anksto apibrėžtas „Real-time Service‟ profilis.




