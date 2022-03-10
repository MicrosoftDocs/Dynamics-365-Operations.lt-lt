---
title: Registruotis ir diegti elektroninių SF išrašymo paslaugą
description: Šioje temoje pateikiama informacija apie tai, kaip registruotis ir įdiegti elektroninių SF išrašymo paslaugą.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4ab16652e4a50dd71a5d0b2b49b4dd79e327f7a8
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371931"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>Registruotis ir diegti elektroninių SF išrašymo paslaugą

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie tai, kaip registruotis ir įdiegti elektroninių SF išrašymo paslaugą. Šiame procese yra keturi veiksmai. Būtina atlikti 1–3 veiksmus, o 4 veiksmas nebūtinas.

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>1 žingsnis: reguliavimo konfigūracijos tarnybos prisijungimas

Reguliavimo konfigūracijos tarnyba (RCS) teikia konfigūravimo ir dizaino patirtį, naudojamą konfigūruojant elektroninių SF išrašymą. Tokie ištekliai kaip aplinkos ir elektroninių SF išrašymo priemonės kuriamos, prižiūrimos ir valdomos RCS. Kai ištekliai parengti, jie paskelbiami elektroninių SF išrašymo paslauga.

Daugiau informacijos apie RCS rasite reguliavimo konfigūracijos [tarnybos (RCS) – globalizavimo funkcijos](rcs-globalization-feature.md).

Norėdami prisiregistruoti prie RCS, eikite į [reguliavimo konfigūracijos tarnybos](https://marketing.configure.global.dynamics.com/) puslapį.

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>2 žingsnis: mikroservices įdiegimas Microsoft Dynamics ciklo tarnybose

Elektroninių SF išrašymo paslauga yra mikroservices rinkinys, kuris yra Microsoft duomenų centruose. Numatyta, kad klientai ir Dynamics 365 Finance Dynamics 365 Supply Chain Management neturi prieigos prie elektroninių SF išrašymo paslaugos. Turite įdiegti ją kaip papildinį ciklo Microsoft Dynamics tarnybose (LCS). Kai įdiegiate priedą, jūsų finansų arba tiekimo grandinės valdymo aplinka užregistruojama programų, prie kurių leidžiama prisijungti prie elektroninių SF išrašymo paslaugos, registre.

Norėdami užbaigti šį veiksmą, [žr. įdiegtį mikroservices ciklo tarnybose](e-invoicing-install-add-in-microservices-lcs.md).

### <a name="step-3-set-up-rcs"></a>3 žingsnis: nustatyti RCS

Turite nustatyti RCS ir elektroninių SF išrašymo tarnybos integravimą. Taip pat turite nustatyti pagrindinius komponentus.

Norėdami atlikti šį veiksmą, žr [. Reguliavimo konfigūracijos tarnybos (RCS) parametrus](e-invoicing-set-up-rcs.md).

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>4 žingsnis: Microsoft Power Platform priedo administratoriaus nuoroda

Kai kuriems scenarijams reikia integravimo Dataverse į veiklos sritį Microsoft Power Platform.

Šiuo metu šis nustatymas privalomas, jei elektroninio SF išrašymo scenarijams naudosite elektroninio SF išrašymo sprendimus. Tačiau saudo Arabijos elektroninių SF išrašymo scenarijų pasirinktis. Norėdami gauti daugiau informacijos, žr. [elektroninių SF išrašymo priemonių pasiekiamumą pagal šalį arba regioną](e-invoicing-country-specific-availability.md).

Norėdami atlikti šį veiksmą, žr [Microsoft Power Platform . priedo administratoriaus nuorodą](e-invoicing-power-platform-plug-in.md).
