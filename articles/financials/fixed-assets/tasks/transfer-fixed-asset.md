---
title: Perkelti ilgalaikį turtą
description: Šis užduočių vadovas ilgalaikio turto knygos finansinę informaciją iš vieno finansinių dimensijų rinkinio perkels į naują finansinių dimensijų rinkinį.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 167591cf160916f256e2d10f122eca312ba07639
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839742"
---
# <a name="transfer-a-fixed-asset"></a>Perkelti ilgalaikį turtą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šis užduočių vadovas ilgalaikio turto knygos finansinę informaciją iš vieno finansinių dimensijų rinkinio perkels į naują finansinių dimensijų rinkinį.  Jis naudoja vaidmenį Buhalteris ir USMF juridinio subjekto demonstracinius duomenis.

1. Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Ilgalaikis turtas > Ilgalaikis turtas**.
2. Sąraše raskite ir pasirinkite perkeltiną ilgalaikį turtą.
3. Veiksmų srityje spustelėkite **Ilgalaikis turtas**.
4. Spustelėkite **Transfer fixed assets**.
5. Lauke **Transfer date** įveskite datą.
6. Įveskite perkėlimą apibūdinančių komentarų.
    
    Šiame sąraše rodomos visos ilgalaikio turto knygos.  
7. Pažymėkite knygas, kurias norite perkelti į naują finansinių dimensijų rinkinį.
    * Šiame sąraše rodomos pasirinktos knygos esamos finansinių dimensijų reikšmės.  
    * Pasirinkite, kurią pasirinktos ilgalaikio turto knygos finansinę dimensiją norite atnaujinti.  
8. Lauke **Financial dimension** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Tinkamai nustatykite kitas finansinių dimensijų reikšmes.  
    * Įvykus perkėlimui, pasikeičia visos finansinių dimensijų reikšmės, nesvarbu, ar reikšmė buvo įvesta, ar palikta tuščia. Pavyzdžiui, jei įvedėte VersloVienetas reikšmę, o finansines dimensijas IšlaidųCentras ir Skyrius palikote tuščias. Jei jūsų sąskaitos struktūra leidžia reikšmes IšlaidųCentras ir Skyrius palikti tuščias, po perkėlimo kiekviena VersloVienetas vertinimo modelio reikšmė būtų nauja, o reikšmės IšlaidųCentras ir Skyrius – tuščios.  
9. Spustelėkite **Update**.
    * Prieš baigdami perkėlimą, turite galimybę pakeitimus peržiūrėti.  
    * Prieš perkeldami ilgalaikio turto knygas, peržiūrėkite rezultatus.  
10. Spustelėkite **Transfer**.

