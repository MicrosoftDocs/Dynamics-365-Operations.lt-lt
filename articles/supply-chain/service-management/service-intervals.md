---
title: Aptarnavimo intervalai
description: Šiame straipsnyje pateikiama apžvalga, kaip dirbti su aptarnavimo intervalais. Aptarnavimo sutarties intervalas nurodo dažnumą, kokiu kuriamos aptarnavimo sutarčių eilučių aptarnavimo užsakymo eilutės, kai automatiškai kuriate aptarnavimo užsakymus.
author: sorenva
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62708258ac3dca9ac03b44efdc96e3bfd643a255
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887231"
---
# <a name="service-intervals"></a>Aptarnavimo intervalai

[!include [banner](../includes/banner.md)]

Aptarnavimo sutarties intervalas nurodo dažnumą, kokiu kuriamos aptarnavimo sutarčių eilučių aptarnavimo užsakymo eilutės, kai automatiškai kuriate aptarnavimo užsakymus.

Kai automatiškai kuriate aptarnavimo užsakymus, aptarnavimo užsakymo eilutės kuriamos pagal intervalą, kurį nurodėte aptarnavimo sutarties eilutėje, nuo sutarties eilutės pradžios datos.

Jei puslapyje **Aptarnavimo sutartys** esančios aptarnavimo sutarties eilutės laukas **Intervalas** yra tuščias, eilutė yra vienkartinis įvykis, ir ji nenaudojama pakartotinai kurti aptarnavimo užsakymams.

## <a name="example"></a>Pavyzdys

Šis pavyzdys iliustruoja, kaip aptarnavimo intervalas paveiks aptarnavimo sutarties eilutes ir aptarnavimo užsakymo eilutes aptarnavimo užsakyme.

### <a name="create-a-service-agreement"></a>Aptarnavimo sutarties kūrimas

Pirma, sukurkite aptarnavimo sutartį ir nustatykite parinkties **Jungti aptarnavimo užsakymus** kriterijų **Pagal aptarnavimo sutartį**.

1. Spustelėkite **Aptarnavimo sutartys**
2. **Veiksmų srityje**, skirtuke **Aptarnavimo sutartis**, grupėje **Nauja** spustelėkite **Aptarnavimo sutartis**, kad sukurtumėte naują aptarnavimo sutartį.
3. Įveskite aprašymą, lauke **Projekto ID** pasirinkite projektą ir įveskite datą lauke **Pradžios data**.
4. Lauke **Jungti aptarnavimo užsakymus** pasirinkite **Pagal aptarnavimo sutartį**.

Dabar sukūrėte tokią aptarnavimo sutartį:

| Projektas      | Pradžios data                                                                         |
|--------------|------------------------------------------------------------------------------------|
| Jūsų projektas | Jūsų nurodyta projekto data. Šiame pavyzdyje naudojama dabartinė data. |

### <a name="create-a-service-agreement-line"></a>Aptarnavimo sutarties eilutės kūrimas

Po to sukurkite aptarnavimo sutarties eilutę, kurios operacijos tipas yra **Valanda**.

Norėdami baigti šią pavyzdžio dalį, puslapyje **Aptarnavimo intervalai** turite sukurti 10 dienų aptarnavimo intervalą. 

1. Pasirinkite ką tik sukurtą aptarnavimo sutartį. 
2. „FastTab“ skirtuke **Eilutės** spustelėkite mygtuką **Pridėti**, kad sukurtumėte naują eilutę apatinėje puslapio **Aptarnavimo sutartys** srityje.
3. Lauke **Operacijos tipas** pasirinkite **Valanda**.
4. Lauke **Darbininkas** pasirinkite darbininką, kuris atliks aptarnavimą.
5. Lauke **Aptarnavimo intervalas** pasirinkite 10 dienų intervalą.

Ką tik sukūrėte tokią aptarnavimo sutarties eilutę su tokia informacija:

| Operacijos tipas | Pradžios data                               | Paslaugos intervalas |
|------------------|------------------------------------------|------------------|
| Valanda             | Dabartinė data.                        | Kas 10 dienų    |
| Darbuotojas           | Darbininkas, atliksiantis aptarnavimą. |                  |

Eilutėje nenurodytas joks laiko langas. 

### <a name="create-planned-service-orders"></a>Suplanuotų aptarnavimo užsakymų kūrimas

Dabar galite kurti suplanuotus aptarnavimo užsakymus ir aptarnavimo užsakymų eilutes kitam mėnesiui.

1. Puslapyje **Aptarnavimo sutartys**, **Veiksmų srityje**, skirtuke **Pristatyti** spustelėkite **Suplanuoti aptarnavimo užsakymai**.
2. Puslapyje **Aptarnavimo užsakymų kūrimas** esančiame lauke **Nuo kada** įveskite dabartinę datą, o lauke **Iki kada** – datą, kuri yra už vieno mėnesio nuo dabartinės datos.
3. Slankiklį **Valanda** nustatykite į padėtį **Taip**. 
4. Spustelėkite **Gerai**.

Aptarnavimo užsakymas nepriskirtas grupei (grupavimą nurodo pasirinktis **Pagal aptarnavimo sutartį** lauke **Jungti aptarnavimo užsakymus**), vienam aptarnavimo užsakymui sukuriama viena aptarnavimo užsakymo eilutė.

### <a name="service-orders-created"></a>Sukurti aptarnavimo užsakymai

Sukurtos trys aptarnavimo užsakymo eilutės patenka į laiko ribas, kurias nurodėte dialogo lange **Aptarnavimo užsakymų kūrimas**. Aptarnavimo užsakymo eilutes galite peržiūrėti puslapyje **Aptarnavimo sutartys** (**Veiksmų sritis** \> skirtukas **Pristatyti** \>mygtukas **Peržiūrėti**).

## <a name="related-articles"></a>Susiję straipsniai

[Aptarnavimo intervalų nustatymas](set-up-service-intervals.md)  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]