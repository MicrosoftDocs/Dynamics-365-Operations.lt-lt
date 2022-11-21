---
title: Išankstiniai mokėjimai Dynamics 365 Commerce
description: Šiame straipsnyje pateikta išankstinio mokėjimo operacijų apdorojimo apžvalga Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-06-28
ms.openlocfilehash: 8262470f83481ef8840857a52948c0833d8b278e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780205"
---
# <a name="prepayments-in-dynamics-365-commerce"></a>Išankstiniai mokėjimai Dynamics 365 Commerce

[!include[banner](../includes/banner.md)]

Šiame straipsnyje pateikta išankstinio mokėjimo operacijų apdorojimo apžvalga Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce apdoroja šių gautinų sumų arba Commerce naudojamų mokėjimo tipų išankstinio apmokėjimo operacijas:

- **Kliento sąskaitos depozito mokėjimas** – klientas moka įmoką taške (EKA). "Commerce" apdoroja depozito mokėjimą kaip išankstinio mokėjimo operaciją. Kai registruojate operaciją, sukuriamas ir užregistruojamas " **Commerce Headquarters" žurnalo kvito** puslapyje. Mokėjimų **skirtuke automatiškai** pasirenkamas mokėjimų žurnalo **išankstinio** mokėjimo žurnalo kvito žymės langelis. Norėdami gauti daugiau informacijos, įskaitant išankstinio apmokėjimo ir su mokesčiais susijusią informaciją, kuri susijusi su tiksliniu regionu, [žr. globalizavimo išteklius – šaliai/regionui brangų žinyno turinį](/dynamics365/fin-ops-core/dev-itpro/lcs-solutions/country-region?context=%2Fdynamics365%2Fcontext%2Ffinance#countryregion-specific-help-content).
- **Kliento užsakymas, kuriam yra depozitas** – klientas sukuria kliento užsakymą EKA. Klientas gali mokėti užsakymo įmoką, pagrįstas numatytuoju depozito procentu, kuris sukonfigūruotas "Commerce **Headquarters**" puslapyje Klientų užsakymai (**"Commerce" parametrai \> Klientų užsakymai**). "Commerce" apdoroja kliento užsakymo depozito mokėjimą kaip išankstinio mokėjimo operaciją. Kai registruojate operaciją, sukuriamas ir registruojamas žurnalo kvito **puslapyje.** Mokėjimų **skirtuke automatiškai** pasirenkamas mokėjimų žurnalo **išankstinio** mokėjimo žurnalo kvito žymės langelis. Mokėjimas yra sudengtas ir kliento SF automatiškai išduodama, kai užsakymas yra paimtas arba pristatytas.
- **Skambučių centro pardavimo užsakymas** – skambučių centro klientų aptarnavimo atstovas sukuria pardavimo užsakymą kliento vardu, **·** **o** išankstinio mokėjimo atributas mokėjimo fiksavimo metu nustatomas kaip Taip.

"Commerce" atlieka šias užduotis išankstiniam apmokėjimui apdoroti:

- **Apdoroti kliento sąskaitos depozito mokėjimą** – kliento mokėjimo mokėjimas, kuris yra perkeliamas į Commerce, naudojant tarnybą, kuri sinchronizuoja duomenis. "Commerce" sukuria mažmeninės prekybos mokėjimo operaciją mokėjimui. Kai registruojate mažmeninės prekybos operaciją, užregistruojamas grynųjų pinigų žurnalas arba kliento mokėjimo žurnalas. Išankstinio **mokėjimo žurnalo** kvito žymės **langelis, esantis** **"Commerce Headquarters" žurnalo kvitų** puslapio Mokėjimas skirtuke, automatiškai pasirenkamas mokėjimo žurnalui. Išankstinių mokėjimų apdoroti negalima, jei mokėjimo suma yra neigiama.
- **Apdoroti kliento užsakymą arba pardavimo užsakymą**, kuriame yra depozitas – klientas moka reikiamą kliento užsakymo depozitą, Commerce Data Exchange naudodamas: Real-time Service. "Commerce" sukuria kliento mokėjimų žurnalą arba grynųjų pinigų žurnalą, atsižvelgdama į kliento naudojamas mokėjimo būdą. Išankstinio **mokėjimo žurnalo** kvito žymės langelis **, esantis žurnalo** **kvito** puslapio mokėjimų skirtuke, automatiškai pasirenkamas "Commerce Headquarters" žurnalui. Jei daliniams mokėjimams atlikti klientas naudoja kelis mokėjimo metodus, "Commerce" apdoroja kiekvieną dalinį mokėjimą, pagrįstą naudou mokėjimo metodu.

Dėl kredito kortelių ir skaitmeninių reikalavimų, kurie turi kitų kredito kortelių mokėjimo būdų, "Commerce" po sėkmingo autorizavimo siunčia užklausą "perimti". (Lėšos fiksuojamos prieš išrašant pardavimo užsakymo SF.)

Atšaukus kliento užsakymą, grąžinama išankstinio mokėjimo suma ir užregistruojamas įmokos sumos grąžinimo mokėjimo žurnalas. Grąžinimo suma skaičiuojama ir registruojama remiantis mokėjimo metodu, kurį nurodėte užregistravimo grąžinimo mokėjimą. "Commerce" gali taikyti atšaukimo mokestį, remiantis procentiniu dydžiu, kurį nustatėte " **Commerce Parameters"** puslapyje, "Commerce Headquarters".

Jei grąžinsite kliento užsakymą, bus sukurtas grąžinimo užsakymas ir grąžinimo mokėjimo žurnalas. Kai registruojate grąžinimo užsakymą, "Commerce" sukuria kliento mokėjimų žurnalą arba grynųjų pinigų žurnalą, atsižvelgdama į mokėjimo metodą, kurį naudoja klientas pradinėje operacijoje.
