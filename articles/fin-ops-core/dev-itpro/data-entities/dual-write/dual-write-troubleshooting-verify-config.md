---
title: „Finance and Operations“ programų ir „Dataverse“ dvigubo rašymo konfigūracijos patvirtinimas
description: Šioje temoje paaiškinama, kaip galite nustatyti, ar dvigubas rašymas sukonfigūruotas programose „Finance and Operations“ ir „Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 3fa16a450032464e445ae166f0699fe0dc388071
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062805"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>„Finance and Operations“ programų ir „Dataverse“ dvigubo rašymo konfigūracijos patvirtinimas

[!include [banner](../../includes/banner.md)]





Šioje temoje pateikiama trikčių šalinimo informacija apie dvigubo rašymo integravimą tarp „Finance and Operations“ programų ir Dataverse. Tiksliau, paaiškinama, kaip galite nustatyti, ar dvigubas rašymas sukonfigūruotas programose „Finance and Operations“ ir „Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Patikrinkite, ar programoje „Finance and Operations“ sukonfigūruotas dvigubas rašymas

Norėdami nustatyti, ar klaidos, kurias matote bandydami įrašyti atnaujinimo eilutes, yra gaunamos iš dvigubo rašymo funkcijos, pirma patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota.

+ Jei turite administratoriaus teises programoje „Finance and Operations“, eikite į **Darbo vietos \> Duomenų valdymas** ir pasirinkite **Dvigubas rašymas** plytelė. Jeigu rodoma susietų aplinkų informacija ir vykdomų eilučių schemų sąrašas, dvigubo rašymo funkcija yra sukonfigūruota.

    ![Programos „Finance and Operations“ ryšio patvirtinimas, kai turite administratoriaus teises.](media/verify_fin_ops_1.png)

+ Jei neturite administratoriaus teisių, gausite klaidos pranešimą *Nepavyksta įrašyti duomenų į objektą \<entity name\>*. Toliau pateiktoje iliustracijoje pateiktame pavyzdyje negalite sukurti klientų eilutės programoje „Finance and Operations“, nes sukonfigūruotas dvigubas rašymas, tačiau klientų grupės ir mokėjimo sąlygų nuorodos duomenų nėra Dataverse.

    ![Programos „Finance and Operations“ ryšio patvirtinimas, kai neturite administratoriaus teisių.](media/verify_fin_ops_2.png)

Informacijos apie tai, kaip išspręsti problemas, kai kuriate duomenis „Finance and Operations“ programose, žr [Pašalinkite tiesioginio sinchronizavimo triktis](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota „Dataverse“

Jei kurdami duomenis, matote stulpelį **Įmonė** „Dataverse” puslapiuose, dvigubo rašymo funkcija yra sukonfigūruota.

![„Dataverse” ryšio tikrinimas.](media/verify_cds.png)

Informacijos apie tai, kaip spręsti problemas, kai kuriate duomenis „Dataverse”, žr. [Tiesioginio sinchronizavimo trikčių šalinimas](dual-write-troubleshooting-live-sync.md).

Informacijos apie tai, kaip peržiūrėti klaidos informaciją, jei susiduriate su klaidomis, kurdami duomenis „Dataverse”, žr. [Priedo sekimo žurnalo „Dataverse“ įgalinimas ir peržiūra, siekiant peržiūrėti klaidos informaciją](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]