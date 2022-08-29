---
title: Registruotis ir diegti elektroninių SF išrašymo paslaugą
description: Šiame straipsnyje pateikiama informacija apie tai, kaip registruotis ir įdiegti elektroninių SF išrašymo paslaugą.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 99f484e5ab8821c78fde776a9d3195dade2a09d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283964"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>Registruotis ir diegti elektroninių SF išrašymo paslaugą

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie tai, kaip registruotis ir įdiegti elektroninių SF išrašymo paslaugą. Šiame procese yra keturi veiksmai. Būtina atlikti 1–3 veiksmus, o 4 veiksmas nebūtinas.

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>1 žingsnis: reguliavimo konfigūracijos tarnybos prisijungimas

Reguliavimo konfigūracijos tarnyba (RCS) teikia konfigūravimo ir dizaino patirtį, naudojamą konfigūruojant elektroninių SF išrašymą. Tokie ištekliai kaip aplinkos ir elektroninių SF išrašymo priemonės kuriamos, prižiūrimos ir valdomos RCS. Kai ištekliai parengti, jie paskelbiami elektroninių SF išrašymo paslauga.

Daugiau informacijos apie RCS rasite reguliavimo konfigūracijos [tarnybos (RCS) – globalizavimo funkcijos](rcs-globalization-feature.md).

Norėdami prisiregistruoti prie RCS, eikite į [reguliavimo konfigūracijos tarnybos](https://marketing.configure.global.dynamics.com/) puslapį.

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>2 žingsnis: mikroservices įdiegimas Microsoft Dynamics ciklo tarnybose

Elektroninių SF išrašymo paslauga yra mikroservices rinkinys, kuris yra Microsoft duomenų centruose. Numatyta, kad "Dynamics 365 Finance Dynamics 365 Supply Chain Management " klientai neturi prieigos prie elektroninių SF išrašymo paslaugos. Turite įdiegti ją kaip papildinį ciklo Microsoft Dynamics tarnybose (LCS). Kai įdiegiate priedą, jūsų finansų arba tiekimo grandinės valdymo aplinka užregistruojama programų, prie kurių leidžiama prisijungti prie elektroninių SF išrašymo paslaugos, registre.

Norėdami užbaigti šį veiksmą, [žr. įdiegtį mikroservices ciklo tarnybose](e-invoicing-install-add-in-microservices-lcs.md).

### <a name="step-3-set-up-rcs"></a>3 žingsnis: nustatyti RCS

Turite nustatyti RCS ir elektroninių SF išrašymo tarnybos integravimą. Taip pat turite nustatyti pagrindinius komponentus.

Norėdami atlikti šį veiksmą, žr [. Reguliavimo konfigūracijos tarnybos (RCS) parametrus](e-invoicing-set-up-rcs.md).

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>4 žingsnis: Microsoft Power Platform priedo administratoriaus nuoroda

Kai kuriems scenarijams reikia integravimo Dataverse į veiklos sritį Microsoft Power Platform.

Šiuo metu šis nustatymas privalomas, jei elektroninio SF išrašymo scenarijams naudosite elektroninio SF išrašymo sprendimus. Tačiau saudo Arabijos elektroninių SF išrašymo scenarijų pasirinktis. Norėdami gauti daugiau informacijos, žr. [elektroninių SF išrašymo priemonių pasiekiamumą pagal šalį arba regioną](e-invoicing-country-specific-availability.md).

Norėdami atlikti šį veiksmą, žr [Microsoft Power Platform . priedo administratoriaus nuorodą](e-invoicing-power-platform-plug-in.md).
