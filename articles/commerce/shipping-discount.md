---
title: Siuntimo nuolaida
description: Šiame straipsnyje aprašomos siuntimo nuolaidos galimybės Microsoft Dynamics 365 Commerce ir nustatymas, kurio reikia jiems naudoti.
author: ShalabhjainMSFT
ms.date: 08/23/2020
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2019-01-31
ms.openlocfilehash: f19566ce64becea4a53a8479cb5a08579567cda1
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346099"
---
# <a name="shipping-discount"></a>Siuntimo nuolaida

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šiame straipsnyje aprašomos siuntimo nuolaidos galimybės Microsoft Dynamics 365 Commerce ir nustatymas, kurio reikia jiems naudoti.

Laisvas arba su nuolaida siuntimas yra vienas iš faktorių, darančių įtaką klientų pirkimo internetu sprendimams. Kad padidintų savo įplaukas operacijai, daugelis mažmenininkų naudoja nemokamą siuntimo išmoką, kad motyvuos klientus ir padidintų krepšelio dydį.

"Commerce" palaiko siuntimo nuolaidos galimybes, kurios leidžia mažmenininkams konfigūruoti konkretaus siuntimo būdo siuntimo išlaidų nuolaidos procentą, kai bendra operacijos apibrėžtų prekių pardavimo suma atitinka konkrečius kriterijus. Scenarijaus, kuris naudoja siuntimo nuolaidos galimybę, pavyzdys yra "Išlaidos $50 ar daugiau, norint gauti nemokamą per naktį siuntą.

## <a name="prerequisites"></a>Būtinieji komponentai

Siuntimo nuolaidos galimybes palaiko "Commerce'svz." išplėstinės [automatinių išlaidų](/dynamics365/unified-operations/retail/omni-auto-charges) funkcijos. Kad būtų galima dirbti su siuntimo nuolaida, **·** **·** **"Commerce Headquarters" puslapio "Commerce** Headquarters" skirtuke Klientų užsakymai turite įgalinti išplėstinę automatinių išlaidų konfigūraciją. Mažmenininkai gali naudoti išplėstinių automatinių išlaidų funkciją, norėdami nustatyti įvairius išlaidų tipus, pvz., tvarkymo, diegimo ir likvidavimo.

Siuntimo nuolaida taikoma tik gabenimo mokesčiams. Todėl mažmenininkas turi nurodyti, kurios išlaidos yra siuntimo išlaidos. Norėdami nurodyti siuntimo mokesčius "Commerce Headquarters", **\>\>** **·** **eikite į Kanalo nustatymo mokesčių kodą ir nustatykite siuntimo išlaidų parinktį Taip**, jei norite naudoti norimus mokesčius.

![Mokesčio, kaip siuntimo mokesčio, nurodymas.](./media/Specify_shipping_charge.png)

## <a name="configuration"></a>Konfigūracija

Siuntimo nuolaidos galimybės yra pakopinės ir palaiko tik procentinės nuolaidos **skaičiavimo** tipą. Norėdami nustatyti siuntimo nuolaidą "Commerce Headquarters", eikite į siuntos **ribinės nuolaidos kainas \> ir nuolaidas**. Tada galite nurodyti pristatymo būdą, kurį taikoma nuolaida, apibrėžti vieną ar daugiau sumos ribinių verčių ir nustatyti kiekvienos ribinės vertės nuolaidos procentą. Taip pat galite konfigūruoti kategorijų arba produktų sąrašą kaip apibrėžtus prekes. Tokiu būdu tik pardavimo suma su tomis operacijos prekėmis bus skaičiuojama, kai kainos nustatymo variklis įvertins, ar bendra operacijos suma atitinka ribinę vertę.

> [!NOTE]
> Skirtingai nei kitų tipų nuolaidos, siuntimo nuolaida nesukuria nuolaidų eilučių. Vietoj to ji tiesiogiai redaguoja siuntimo išlaidas ir prie mokesčio aprašymo pridės nuolaidos pavadinimą.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
