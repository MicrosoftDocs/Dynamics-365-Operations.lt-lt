---
title: „Finance and Operations“ programų ir „Dataverse“ dvigubo rašymo konfigūracijos patvirtinimas
description: Šiame straipsnyje paaiškinama, kaip nustatyti, ar finansų ir operacijų programėlėse ir dalyje sukonfigūruotas dvigubas rašymas Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 7131e6c2c4ca4d9c6bb84ad74bf425faf28bd92c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884465"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>„Finance and Operations“ programų ir „Dataverse“ dvigubo rašymo konfigūracijos patvirtinimas

[!include [banner](../../includes/banner.md)]





Šiame straipsnyje pateikiama trikčių diagnostikos informacija, skirta dvigubo rašymo integravimui tarp finansų ir operacijų programėlių ir Dataverse. Taigi, paaiškinama, kaip galima nustatyti, ar dvigubo rašymo konfigūracija sukonfigūruota finansų ir operacijų programėlėse ir čia Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Patikrinkite, ar dvigubo rašymo programa sukonfigūruota finansų ir operacijų programoje

Norėdami nustatyti, ar klaidos, kurias matote bandydami įrašyti atnaujinimo eilutes, yra gaunamos iš dvigubo rašymo funkcijos, pirma patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota.

+ Jei turite administratoriaus teises finansų ir operacijų programoje, **eikite į Darbo sričių \>** duomenų valdymą ir pasirinkite dvigubo rašymo **išklotinę** programą. Jeigu rodoma susietų aplinkų informacija ir vykdomų eilučių schemų sąrašas, dvigubo rašymo funkcija yra sukonfigūruota.

    ![Tikrinamas finansų ir operacijų programos ryšys, kai turite administratoriaus teises.](media/verify_fin_ops_1.png)

+ Jei neturite administratoriaus teisių, gausite klaidos pranešimą *Nepavyksta įrašyti duomenų į objektą \<entity name\>*. Pateiktame pavyzdyje negalite sukurti kliento eilutės finansų ir operacijų programoje, nes sukonfigūruotas dvigubas rašymas, bet klientų grupės ir mokėjimo sąlygų nuorodos duomenų nėra Dataverse.

    ![Tikrinamas finansų ir operacijų programos ryšys, kai neturite administratoriaus teisių.](media/verify_fin_ops_2.png)

Informacijos, kaip išspręsti problemas, kai kuriate duomenis finansų ir operacijų programėlėse, ieškokite tiesioginio sinchronizavimo [trikčių šalinimas](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Patikrinkite, ar dvigubo rašymo funkcija yra sukonfigūruota „Dataverse“

Jei kurdami duomenis, matote stulpelį **Įmonė** „Dataverse” puslapiuose, dvigubo rašymo funkcija yra sukonfigūruota.

![„Dataverse” ryšio tikrinimas.](media/verify_cds.png)

Informacijos apie tai, kaip spręsti problemas, kai kuriate duomenis „Dataverse”, žr. [Tiesioginio sinchronizavimo trikčių šalinimas](dual-write-troubleshooting-live-sync.md).

Informacijos apie tai, kaip peržiūrėti klaidos informaciją, jei susiduriate su klaidomis, kurdami duomenis „Dataverse”, žr. [Priedo sekimo žurnalo „Dataverse“ įgalinimas ir peržiūra, siekiant peržiūrėti klaidos informaciją](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]