---
title: Paskyros valdymo puslapiai ir moduliai
description: Šioje temoje aprašomi „Microsoft Dynamics 365 Commerce“ paskyros valdymo puslapiai ir moduliai.
author: v-chgri
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8787a7b01ecf15752569d2a3a8d7804fe492e63d
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025716"
---
# <a name="account-management-pages-and-modules"></a>Paskyros valdymo puslapiai ir moduliai


[!include [banner](includes/banner.md)]

Šioje temoje aprašomi „Microsoft Dynamics 365 Commerce“ paskyros valdymo puslapiai ir moduliai.

## <a name="overview"></a>Peržiūrėti

Paskyros valdomos keliuose „Dynamics 365 Commerce“ puslapiuose, kuriuose valdoma su vartotoju susijusi informacija. Paskyros valdymo puslapiai apima paskyros valdymo nukreipimo puslapį, vartotojo profilio puslapį, vartotojo adresų puslapį, užsakymų retrospektyvos puslapį, išsamios užsakymų informacijos puslapį, lojalumo puslapį ir pageidavimų sąrašo puslapį.

### <a name="account-management-landing-page"></a>Paskyros valdymo nukreipimo puslapis

Paskyros valdymo nukreipimo puslapyje naudojami tolesni moduliai.

- **Konteineris** – visų paskyros valdymo nukreipimo puslapio modulius reikia patalpinti į konteinerį. 
- **Paskyros pasisveikinimo plytelė** – naudojant šį modulį, paskyros valdymo puslapyje pateikiamas pasisveikinimo pranešimas. Jame yra antraštės ypatybių.
- **Paskyros bendroji plytelė** – šis modulis gali būti naudojamas, norint teikti antraštes ir saitus į paskyrų valdymo puslapius, pavyzdžiui, puslapiai „Užsakymo istorija“ arba „Mano profilis“. Bendrosios plytelės modulį galima naudoti bet kurio puslapio plytelei konfigūruoti. „Fabrikam“ šis modulis naudojamas puslapių „Užsakymo istorija“ ir „Mano profilis“ saitams paskyros valdymo nukreipimo puslapyje.
- **Paskyros pageidavimų sąrašo plytelė** – naudojant šį modulį pateikiama kliento pageidavimų sąraše esančių prekių suvestinė. Pavyzdžiui, jame gali būti nurodyta „Pageidavimų sąraše turite 10 prekių.“ Jame pateikiamos antraštės ir „Peržiūrėti išsamią informaciją“ ypatybės. Saitą „Peržiūrėti išsamią informaciją“ reikia sukonfigūruoti taip, kad jis nukreiptų į pageidavimų sąrašo puslapį. 
- **Paskyros adresų plytelė** – naudojant šį modulį pateikiama vartotojo adresų suvestinė. Pavyzdžiui, jame gali būti nurodyta „Į jūsų paskyrą įtraukti 2 adresai.“ Jame pateikiamos antraštės ir „Peržiūrėti išsamią informaciją“ ypatybės. Saitą „Peržiūrėti išsamią informaciją“ reikia sukonfigūruoti taip, kad jis nukreiptų į vartotojo adresų puslapį.
- **Paskyros lojalumo plytelė** – naudojant šį modulį rodoma informacija apie lojalumo programą ir pateikiamas saitas su šia informacija. Ši plytelė turi dvi būsenas: viena būsena nurodo saitus, skirtus prisijungti prie lojalumo programos, jei vartotojas dar nėra narys. Kita būsena rodo saitus, kad būtų galima peržiūrėti lojalumo informacijos puslapį, kai vartotojas jau yra narys. Ypatybėse yra antraštė, „Prisijungimo“ saitas ir „Peržiūrėti lojalumą“ saitas. Saitą „Peržiūrėti lojalumą“ reikia sukonfigūruoti taip, kad jis nukreiptų į lojalumo puslapį. Saitą „Prisijungti“ reikia sukonfigūruoti taip, kad jis nukreiptų į puslapį, kuriame vartotojai galėtų prisijungti prie lojalumo programos. 

### <a name="order-history-page"></a>Užsakymų retrospektyvos puslapis

Užsakymų retrospektyvos puslapyje naudojant užsakymų retrospektyvos modulį rodomi visi vėliausi vartotojo pateikti užsakymai.

### <a name="order-details-page"></a>Užsakymo informacijos puslapis

Išsamios užsakymų informacijos puslapyje pateikiama išsami informacija apie kiekvieną užsakymą, o jis pasiekiamas užsakymų retrospektyvos puslapyje. Jame naudojamas išsamios užsakymų informacijos modulis, kuriam išsamiai užsakymų informacijai gauti reikalingas pardavimo ID arba operacijos ID.

### <a name="user-profile-page"></a>Vartotojo profilio puslapis

Vartotojo profilio puslapyje rodoma išsami vartotojo paskyros informacija, pvz., vartotojo vardas ir el. pašto adresas. Jis naudoja vartotojo profilio išsamią informaciją ir vartotojo profilio redagavimo modulius. Nors el. pašto adreso pašalinti negalima, jį galima redaguoti. Vartotojo profilio puslapyje taip pat rodomos vartotojo nuostatos, kurias naudodamas vartotojas gali sutikti arba atsisakyti naudoti tam tikras funkcijas, pvz., rekomendacijų sąrašų personalizavimo funkciją. 

### <a name="user-address-page"></a>Vartotojo adresų puslapis

Vartotojo adresų puslapyje rodomas adresų, susietų su vartotojo paskyra, sąrašas. Vartotojas šiuos adresus pateikė užbaigdamas pirkimą arba įtraukė tiesiogiai šiame puslapyje. Puslapyje adresai įtraukiami ir redaguojami, pagrindinis adresas nustatomas, o esami adresai rodomi naudojant vartotojo adresų modulį.

### <a name="wish-list-page"></a>Pageidavimų sąrašo puslapis

Pageidavimų sąrašo puslapyje rodomos prekės, įtrauktos į kliento pageidavimų sąrašą. Jame pageidavimų sąrašo prekės rodomos naudojant pageidavimų sąrašo modulį.

### <a name="loyalty-page"></a>Lojalumo puslapis

Lojalumo puslapyje klientai gali peržiūrėti savo lojalumo išsamią informaciją, jei jie jau yra lojalumo programos nariai. Jie taip pat gali peržiūrėti taškus, kuriuos uždirbo ir panaudojo atlikdami vėliausias operacijas. Puslapis naudoja lojalumo išsamios informacijos modulį, kad parodytų lojalumo išsamią informaciją. 

Norint prisijungti prie lojalumo programos, rinkodaros puslapį galima sukurti naudojant lojalumo prisijungimą ir lojalumo sąlygų modulius. Jei vartotojas nėra lojalumo programos narys, šie moduliai įgalins vartotoją prisijungti.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Užsakymo patvirtinimo modulis](order-confirmation-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)
