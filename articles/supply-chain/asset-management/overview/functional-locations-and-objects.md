---
title: Funkcinės vietos ir ištekliai
description: Šiame straipsnyje aprašomos turto valdymo funkcinės vietos ir turtas. Turto valdymas yra išplėstinis modulis, skirtas turtui ir priežiūros užduotims valdyti programoje „Dynamics 365 Supply Chain Management“.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 274e80136ee303af9d0fe5fd04095f575a345d19
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875661"
---
# <a name="functional-locations-and-assets"></a>Funkcinės vietos ir ištekliai

[!include [banner](../../includes/banner.md)]

 

Šiame straipsnyje aprašomos turto valdymo funkcinės vietos ir turtas. Turto valdymas yra išplėstinis modulis, skirtas turtui ir priežiūros užduotims valdyti programoje „Dynamics 365 Supply Chain Management“.

## <a name="overview"></a>Apžvalga

Turto valdymas sklandžiai integruojamas su keletu kitų „Finance and Operations“ programų modulių. Toliau pateikiamoje iliustracijoje pavaizduotos sąsajos su kitais moduliais.

![Diagrama, rodanti, kaip turto valdymas siejasi su kitais moduliais.](media/01-overview-image.png)

Turto valdymas leidžia efektyviai valdyti ir atlikti visas užduotis, susijusias su daugelio tipų įrangos valdymu ir aptarnavimu jūsų įmonėje. Ši įranga apima mašinas, gamybos įrangą ir transporto priemones. Modulyje Turto valdymas taip pat palaikomi sprendimai daugelyje pramonės šakų.

Toliau esančioje iliustracijoje pateikiama modulio Turto valdymas pagrindinių funkcijų apžvalga.

![Diagrama, rodanti pagrindines turto valdymo funkcijas.](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>Funkcinės vietos ir ištekliai

Funkcinės vietos naudojamos vietose esančiam turtui valdyti. Šis valdymas apima turto išlaidų sekimą funkcinėse vietose. Funkcinių vietų struktūra yra hierarchinė, o vietose gali būti antrinių vietų. Funkcinių vietų struktūra yra statinė. Kitaip tariant, negalima keisti vietų buvimo vietų. Turtas gali būti įdiegtas funkcinėse vietose ir, jei reikia, vėliau gali būti įdiegtas kitose funkcinėse vietose.

Turto išlaidos visada priklauso nuo turto vietos. Kitaip tariant, jei įdiegiate turtą naujoje funkcinėje vietoje, turtas automatiškai naudoja finansines dimensijas, susijusias su nauja funkcine vieta. Todėl turto išlaidos visada yra susijusios su funkcine vieta, kurioje turtas šiuo metu yra įdiegtas. Toks automatinis finansinių dimensijų tvarkymas padeda užtikrinti visišką išlaidų sekimą, kai jūsų įmonė kontroliuoja projektus ir teikia ataskaitas apie funkcines vietas.

Funkcinių vietų hierarchijos kūrimo būdas priklauso nuo jūsų įmonės reikalavimų dėl vidinės įrangos priežiūros arba klientų įrangos aptarnavimo. Toliau pateikiamame paveikslėlyje pavaizduotas geografinėmis vietovėmis pagrįstų funkcinių vietų pavyzdys.

![Diagrama, rodanti geografinėmis vietovėmis pagrįstas funkcines vietas.](media/03-overview-image.png)

Toliau pateikiamame paveikslėlyje pavaizduotas klientais pagrįstų funkcinių vietų pavyzdys.

![Diagrama, rodanti klientais pagrįstas funkcines vietas.](media/04-overview-image.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]