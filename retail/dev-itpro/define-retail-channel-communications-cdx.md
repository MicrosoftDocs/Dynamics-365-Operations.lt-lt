---
title: "Apibrėžti mažmeninės prekybos komunikacijas („Commerce Data Exchange‟)"
description: "Šiame straipsnyje pateikiama „Commerce Data Exchange“ ir jos komponentų apžvalga. Ji paaiškina, kad kiekvienas komponentas atlieka duomenų perdavimą tarp Microsoft Dynamics 365 operacijoms ir mažmeninės prekybos kanalų."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 29938d962db42a521dd8dc03b8e45e0e34410e4d
ms.openlocfilehash: d3b36ec2a3f859215d93dd7ebf1f1ecfb2731c59
ms.lasthandoff: 03/31/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Apibrėžti mažmeninės prekybos komunikacijas („Commerce Data Exchange‟)

Šiame straipsnyje pateikiama „Commerce Data Exchange“ ir jos komponentų apžvalga. Ji paaiškina, kad kiekvienas komponentas atlieka duomenų perdavimą tarp Microsoft Dynamics 365 operacijoms ir mažmeninės prekybos kanalų.

<a name="overview"></a>Apžvalga
--------

Prekybos duomenų mainai yra sistema, kuri perduoda duomenis tarp Dynamics 365 operacijoms ir mažmeninės prekybos kanalais, pvz., elektronines parduotuves ar plytų ir skiedinio parduotuvės. Duomenų bazę, kurioje įrašomi duomenys, skirti mažmeninės prekybos kanalas yra atskirtas nuo Dynamics 365 operacijos duomenų bazės. Kanalų duomenų bazėje saugomi tik tie duomenys, kurių reikia vykdant mažmeninės prekybos operacijas. Pagrindiniai duomenys yra sukonfigūruotas Dynamics 365 operacijoms ir platinama kanalai. Sandorių duomenų sukuriamas pardavimo (PV) sistemos taškas arba internete laikyti, ir tada įkelti į Dynamics 365 operacijoms. Duomenų paskirstymas yra asinchroninis. Kitaip tariant, duomenų rinkimo ir pakavimo šaltinyje procesas vyksta atskirai nuo duomenų gavimo ir taikymo paskirties vietoje proceso. Kai kuriais scenarijais, pvz., peržvelgiant kainą ir atsargas, duomenis reikia gauti realiu laiku. Remti šiuos scenarijus, komercijos keitimosi duomenimis taip pat yra paslauga, kuri leidžia realaus laiko komunikacijos tarp Dynamics 365 operacijoms ir kanalą. 

[![Atnaujinta mažmeninė grafika](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>„Async“ paslauga
Microsoft SQL serverio pakeitimų sekimą "Dynamics 365" duomenų bazės operacijų naudojama nustatyti duomenų pakeitimus, kurie turi būti siunčiami į kanalus. Remiantis paskirstymo grafikas, Dynamics 365 operacijų duomenų paketai ir išsaugo jį į centrinės saugyklos (Azure blob saugyklų). Atskiras paketinis procesas „Commerce Data Exchange: Async‟ kliento biblioteką naudoja šiam duomenų paketui įterpti į kanalo duomenų bazę. 

[![Async Service](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Duomenų apsikeitimo valdymas

Duomenų apsikeitimo valdymo užduotys yra mechanizmas, skirtas duomenims į vietas ir iš jų paskirstyti. Užduotis sudaro antrinės užduotys, kurios nurodo lenteles ir lentelių laukus, kuriuose yra skirstytini duomenys. Dinamika 365 operacijos apima iš anksto apibrėžtų duomenų apsikeitimo valdymo užduotys ir antrinės užduotys replikacijos reikalavimus dauguma organizacijų. Kuriami tolesni iš anksto apibrėžtų užduočių tipai.

-   **Atsisiųsti darbo vietų** – Parsisiųsti darbo vietų siųsti duomenis, kurie pasikeitė Dynamics 365 operacijoms kanalo duomenų bazėmis. Įrašų modifikacijos sekamos naudojant „SQL Server‟ keitimų sekimą.
-   **Įkelti darbo vietos (darbo vietos P)** – įkelti darbai traukti pardavimo sandoriai iš kanalo į Dynamics "365" operacijų duomenų bazės. P užduotys duomenis įkelia palaipsniui. Kai vykdoma P užduotis, „Async‟ kliento biblioteka dublikatų skaitiklyje tikrina, ar nėra įrašų, kurie jau gauti iš vietos. Įrašas įkeliamas tik tada, jei jo dublikatų skaitiklis yra didesnis už didžiausią rastą reikšmę. P užduotys neatnaujina anksčiau įkeltų duomenų.

Pasiskirstymo grafikas yra naudojamų duomenų perdavimą, rankiniu būdu arba suplanuoti paketinės užduoties Dynamics 365 operacijoms. Paskirstymo grafike gali būti viena ar kelios kanalo duomenų grupės ir viena ar kelios duomenų apsikeitimo valdymo užduotys.

## <a name="realtime-service"></a>Realiu laiku paslauga
Prekybos duomenų mainai: Realiu laiku paslauga yra integruota paslauga, kuri suteikia realaus laiko bendravimo Dynamics 365 operacijoms ir mažmeninės prekybos kanalų. Realiu laiku paslauga, kuri leidžia atskirus POS kompiuteriai ir internetinių parduotuvių nuskaityti konkrečius duomenis Dynamics 365 operacijas realiuoju laiku. Nors dauguma pagrindinių operacijų gali būti atliekamas vietinių kanalų duomenų bazėje, toliau nurodytais atvejais reikalaujama tiesiogiai naudotis duomenimis, kuris saugomas Dynamics 365 operacijoms:

-   Dovanų kortelių išdavimas ir panaudojimas.
-   Lojalumo taškų panaudojimas.
-   Kredito pažymų išdavimas ir panaudojimas.
-   Klientų įrašų kūrimas ir naujinimas.
-   Pardavimo užsakymų kūrimas, naujinimas ir atlikimas.
-   Atsargų gavimas pagal pirkimo užsakymą ar perkėlimo užsakymą.
-   Atsargų skaičiavimas.
-   Pardavimo operacijų gavimas parduotuvėse ir grąžinimo operacijų atlikimas.

[![Real-time Service](./media/rts.png)](./media/rts.png) 

Iš anksto realiu laiku paslaugų profilis sukuriamas.


