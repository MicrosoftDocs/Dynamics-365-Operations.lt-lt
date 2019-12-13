---
title: Paskyros valdymo puslapiai ir moduliai
description: Šioje temoje aprašomi „Microsoft Dynamics 365 Commerce“ paskyros valdymo puslapiai ir moduliai.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 3986505a7e0e8d33d5b8ff2c06f493335731a8d9
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785390"
---
# <a name="account-management-pages-and-modules"></a>Paskyros valdymo puslapiai ir moduliai

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašomi „Microsoft Dynamics 365 Commerce“ paskyros valdymo puslapiai ir moduliai.

## <a name="overview"></a>Peržiūrėti

Paskyros valdomos keliuose „Dynamics 365 Commerce“ puslapiuose, kuriuose valdoma su vartotoju susijusi informacija. Paskyros valdymo puslapiai apima paskyros valdymo nukreipimo puslapį, vartotojo profilio puslapį, vartotojo adresų puslapį, užsakymų retrospektyvos puslapį, išsamios užsakymų informacijos puslapį, lojalumo puslapį ir pageidavimų sąrašo puslapį.

### <a name="account-management-landing-page"></a>Paskyros valdymo nukreipimo puslapis

Paskyros valdymo nukreipimo puslapyje naudojami tolesni moduliai.

- **Turinio išdėstymas** – šis modulis yra konteinerio modulis, kuriame laikomi visi paskyros valdymo nukreipimo puslapio moduliai.
- **Paskyros pasisveikinimo elementas** – naudojant šį modulį, paskyros valdymo puslapyje pateikiamas pasisveikinimo pranešimas. Jame pateikiamos antraštės ir plytelių dydžio ypatybės. Ypatybė **Plytelių dydis** apibrėžia turinio išdėstymo modulio plotį. Reikšmių intervalas yra nuo **1** iki **12** – **12** reiškia visą turinio išdėstymo konteinerio plotį.
- **Paskyros užsakymų pateikimo elementas** – naudojant šį modulį pateikiama vartotojo paskyros pateiktų užsakymų skaičiaus suvestinė. Jame pateikiamos antraštės, plytelių dydžio ir saito „peržiūrėti išsamią informaciją“ ypatybės. Saitą „peržiūrėti išsamią informaciją“ reikia sukonfigūruoti taip, kad jis nukreiptų į užsakymų retrospektyvos puslapį.
- **Paskyros profilio išdėstymo elementas** – naudojant šį modulį pateikiama vartotojo profilio suvestinė. Jame pateikiamos antraštės, plytelių dydžio ir saito „peržiūrėti išsamią informaciją“ ypatybės. Saitą „peržiūrėti išsamią informaciją“ reikia sukonfigūruoti taip, kad jis nukreiptų į vartotojo profilio puslapį.
- **Paskyros pageidavimų sąrašo elementas** – naudojant šį modulį pateikiama kliento pageidavimų sąraše esančių prekių suvestinė. Pavyzdžiui, jame gali būti nurodyta „Pageidavimų sąraše turite 10 prekių.“ Jame pateikiamos antraštės, plytelių dydžio ir saito „peržiūrėti išsamią informaciją“ ypatybės. Saitą „peržiūrėti išsamią informaciją“ reikia sukonfigūruoti taip, kad jis nukreiptų į pageidavimų sąrašo puslapį.
- **Paskyros adresų elementas** – naudojant šį modulį pateikiama vartotojo adresų suvestinė. Pavyzdžiui, jame gali būti nurodyta „Į jūsų paskyrą įtraukti 2 adresai.“ Jame pateikiamos antraštės, plytelių dydžio ir saito „peržiūrėti išsamią informaciją“ ypatybės. Saitą „peržiūrėti išsamią informaciją“ reikia sukonfigūruoti taip, kad jis nukreiptų į vartotojo adresų puslapį.
- **Paskyros lojalumo elementas** – naudojant šį modulį rodoma informacija apie lojalumo programą ir pateikiamas saitas su šia informacija. Jame pateikiamos antraštės, plytelių dydžio, saito „peržiūrėti išsamią informaciją“ ir saito „tapkite nariu“ ypatybės. Saitą „peržiūrėti išsamią informaciją“ reikia sukonfigūruoti taip, kad jis nukreiptų į lojalumo puslapį. Saitą „tapkite nariu“ reikia sukonfigūruoti taip, kad jis nukreiptų į puslapį, kuriame vartotojai galėtų prisijungti prie lojalumo programos.

### <a name="order-history-page"></a>Užsakymų retrospektyvos puslapis

Užsakymų retrospektyvos puslapyje naudojant užsakymų retrospektyvos modulį rodomi visi vėliausi vartotojo pateikti užsakymai.

### <a name="order-details-page"></a>Užsakymo informacijos puslapis

Išsamios užsakymų informacijos puslapyje pateikiama išsami informacija apie kiekvieną užsakymą, o jis pasiekiamas užsakymų retrospektyvos puslapyje. Jame naudojamas išsamios užsakymų informacijos modulis, kuriam išsamiai užsakymų informacijai gauti reikalingas pardavimo ID arba operacijos ID.

### <a name="user-profile-page"></a>Vartotojo profilio puslapis

Vartotojo profilio puslapyje rodoma išsami vartotojo paskyros informacija, pvz., vartotojo vardas ir el. pašto adresas. Jame naudojamas vartotojo profilio modulis. Nors el. pašto adreso pašalinti negalima, jį galima redaguoti.

### <a name="user-address-page"></a>Vartotojo adresų puslapis

Vartotojo adresų puslapyje rodomas adresų, susietų su vartotojo paskyra, sąrašas. Vartotojas šiuos adresus pateikė užbaigdamas pirkimą arba įtraukė tiesiogiai šiame puslapyje. Puslapyje adresai įtraukiami ir redaguojami, pagrindinis adresas nustatomas, o esami adresai rodomi naudojant vartotojo adresų modulį.

### <a name="wish-list-page"></a>Pageidavimų sąrašo puslapis

Pageidavimų sąrašo puslapyje rodomos prekės, įtrauktos į kliento pageidavimų sąrašą. Jame pageidavimų sąrašo prekės rodomos naudojant pageidavimų sąrašo modulį.

### <a name="loyalty-page"></a>Lojalumo puslapis

Lojalumo puslapyje klientai gali prisijungti prie lojalumo programos arba, jei jie jau yra lojalumo programos nariai, peržiūrėti asmeninę išsamią programos informaciją. Jie taip pat gali peržiūrėti taškus, kuriuos uždirbo ir panaudojo atlikdami vėliausias operacijas.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Užsakymo patvirtinimo modulis](order-confirmation-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)
