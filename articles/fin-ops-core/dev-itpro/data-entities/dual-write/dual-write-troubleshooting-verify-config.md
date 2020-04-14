---
title: Patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programose ir „Common Data Service”
description: Šioje temoje paaiškinama, kaip galima nustatyti, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programose ir „Common Data Service”.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f2ba2564ad3e8e444e27fcc0c586ddf252afabd
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172650"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a>Patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programose ir „Common Data Service”

[!include [banner](../../includes/banner.md)]



Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Common Data Service“ programų trikčių šalinimo informacija. Tiksliau sakant, paaiškinama, kaip galima nustatyti, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programose ir „Common Data Service”.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programoje

Norėdami nustatyti, ar klaidos, kurias matote bandydami įrašyti atnaujinimo įrašus, yra gaunamos iš dvigubo rašymo funkcijos, pirma patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota.

+ Jeigu turite administratoriaus teises „Finance and Operations” programoje, eikite į **Darbo sritys \> Duomenų valdymas** ir pasirinkite plytelę **Dvigubas rašymas**. Jeigu rodoma susietų aplinkų informacija ir vykdomų objektų schemų sąrašas, dvigubo rašymo funkcija yra sukonfigūruota.

    ![„Finance and Operations” programos ryšio tikrinimas, kai turite administratoriaus teises](media/verify_fin_ops_1.png)

+ Jei neturite administratoriaus teisių, gausite klaidos pranešimą *Nepavyksta įrašyti duomenų į objektą \<objekto pavadinimas\>*. Tolesnėje iliustracijoje pateiktame pavyzdyje parodyta, kad nepavyksta sukurti kliento įrašo „Finance and Operations” programoje, nes dvigubo rašymo funkcija yra sukonfigūruota, bet klientų grupė ir mokėjimo terminų nuorodos duomenų nėra „Common Data Service”.

    ![„Finance and Operations” programos ryšio tikrinimas, kai neturite administratoriaus teisių](media/verify_fin_ops_2.png)

Informacijos apie tai, kaip spręsti problemas, kai kuriate duomenis „Finance and Operations” programose, žr. [Tiesioginio sinchronizavimo trikčių šalinimas](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a>Patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota „Common Data Service“

Jei kurdami duomenis, matote lauką **Įmonė** „Common Data Service” puslapiuose, dvigubo rašymo funkcija yra sukonfigūruota.

![„Common Data Service” ryšio tikrinimas](media/verify_cds.png)

Informacijos apie tai, kaip spręsti problemas, kai kuriate duomenis „Common Data Service”, žr. [Tiesioginio sinchronizavimo trikčių šalinimas](dual-write-troubleshooting-live-sync.md).

Informacijos apie tai, kaip peržiūrėti klaidos informaciją, jei susiduriate su klaidomis, kurdami duomenis „Common Data Service”, žr. [Priedo sekimo žurnalo „Common Data Service“ įgalinimas ir peržiūra, siekiant peržiūrėti klaidos informaciją](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).
