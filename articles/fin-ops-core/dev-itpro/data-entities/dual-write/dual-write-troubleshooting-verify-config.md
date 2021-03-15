---
title: Dvigubo rašymas konfigūravimo patvirtinimas „Finance and Operations“ programose ir „Dataverse“
description: Šioje temoje paaiškinama, kaip galima nustatyti, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programose ir „Dataverse”.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 361d6555b60e02832c337b6f416b2b3627b6d365
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129312"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Dvigubo rašymas konfigūravimo patvirtinimas „Finance and Operations“ programose ir „Dataverse“

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Šioje temoje pateikiama dvigubo rašymo funkcijos integravimo tarp „Finance and Operations“ ir “Dataverse“ programų trikčių šalinimo informacija. Tiksliau sakant, paaiškinama, kaip galima nustatyti, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programose ir „Dataverse”.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota „Finance and Operations” programoje

Norėdami nustatyti, ar klaidos, kurias matote bandydami įrašyti atnaujinimo eilutes, yra gaunamos iš dvigubo rašymo funkcijos, pirma patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota.

+ Jeigu turite administratoriaus teises „Finance and Operations” programoje, eikite į **Darbo sritys \> Duomenų valdymas** ir pasirinkite plytelę **Dvigubas rašymas**. Jeigu rodoma susietų aplinkų informacija ir vykdomų eilučių schemų sąrašas, dvigubo rašymo funkcija yra sukonfigūruota.

    ![„Finance and Operations” programos ryšio tikrinimas, kai turite administratoriaus teises](media/verify_fin_ops_1.png)

+ Jei neturite administratoriaus teisių, gausite klaidos pranešimą *Nepavyksta įrašyti duomenų į objektą \<entity name\>*. Tolesnėje iliustracijoje pateiktame pavyzdyje parodyta, kad nepavyksta sukurti kliento eilutės „Finance and Operations” programoje, nes dvigubo rašymo funkcija yra sukonfigūruota, bet klientų grupė ir mokėjimo terminų nuorodos duomenų nėra „Dataverse”.

    ![„Finance and Operations” programos ryšio tikrinimas, kai neturite administratoriaus teisių](media/verify_fin_ops_2.png)

Informacijos apie tai, kaip spręsti problemas, kai kuriate duomenis „Finance and Operations” programose, žr. [Tiesioginio sinchronizavimo trikčių šalinimas](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota „Dataverse“

Jei kurdami duomenis, matote stulpelį **Įmonė** „Dataverse” puslapiuose, dvigubo rašymo funkcija yra sukonfigūruota.

![„Dataverse” ryšio tikrinimas](media/verify_cds.png)

Informacijos apie tai, kaip spręsti problemas, kai kuriate duomenis „Dataverse”, žr. [Tiesioginio sinchronizavimo trikčių šalinimas](dual-write-troubleshooting-live-sync.md).

Informacijos apie tai, kaip peržiūrėti klaidos informaciją, jei susiduriate su klaidomis, kurdami duomenis „Dataverse”, žr. [Priedo sekimo žurnalo „Dataverse“ įgalinimas ir peržiūra, siekiant peržiūrėti klaidos informaciją](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]