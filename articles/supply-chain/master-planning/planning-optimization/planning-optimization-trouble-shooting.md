---
title: „Planning Optimization“ trikčių diagnostika
description: Šiame straipsnyje aprašoma, kaip spręsti problemas, su kuriomis jūs galite susidurti dirbdami naudodami planavimo optimizavimą.
author: t-benebo
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f078fda02a11eb2073738d59b45f81698b707653
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889525"
---
# <a name="troubleshoot-planning-optimization"></a>„Planning Optimization“ trikčių diagnostika 

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip išspręsti bendrąsias problemas, su kuriomis galite susidurti naudodami planavimo optimizavimą.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>„Planning Optimization“ papildinio diegimas nebaigtas

Norint naudoti „Planning Optimization“, reikalinga įgalinta „Lifecycle Services“ (LCS), plačiai pasiekiama 2 ar aukštesnės pakopos aplinka (ne „OneBox” aplinka), turinti „Dynamics 365 Supply Chain Management” 10.0.7 arba naujesnę versiją. Jei papildinį bandysite įdiegti „OneBox“ aplinkoje, diegimas nebus baigtas.

**Pataisymas**: atšaukite diegimą ir naudokite plačiai pasiekiamą 2 ar aukštesnės pakopos aplinką (ne „OneBox“ aplinką).

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>Kai „Planning Optimization“ įgalintas, nepavyksta suplanuoti paketinių užduočių

Kai įgalinate „Planning Optimization“, integruotas bendrojo planavimo mechanizmas yra automatiškai išjungiamas. Bendrojo planavimo paketinių užduočių, kurios buvo sukurtos integruotam „Supply Chain Management“ planavimo mechanizmui, atlikti nepavyks, jei jos suaktyvinamos, kai „Planning Optimization“ yra įgalintas. Galite gauti klaidos pranešimą, pvz., *Ši operacija suaktyvino bendrąjį planavimą, kuris nepalaikomas, kai įgalintas „Planning Optimization“*.

**Pataisymas**: atšaukti visas bendrojo planavimo paketines užduotis, kurios buvo sukurtos integruotam „Supply Chain Management“ planavimo mechanizmui.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>„Planning Optimization“ rezultatai skiriasi nuo ankstesnių rezultatų

„Planning Optimization“ tam tikrose srityse skiriasi nuo integruoto bendrojo planavimo dizaino. Tai gali lemti ir laukimo funkcijos.

**Pataisymas**: vykdyti „Planning Optimization“ tinkamumo analizę, tada analizuoti rezultatus nurodant susijusius dokumentus, kad būtų galima suprasti poveikį. Daugiau informacijos žr. [„Planning Optimization“ tinkamumo analizė](planning-optimization-fit-analysis.md).

## <a name="cant-enable-planning-optimization"></a>Nepavyksta įgalinti „Planning Optimization“

Jei parinkties **Naudoti „Planning Optimization“** reikšmę norite nustatytai kaip **Taip**, **Ryšio būsena** reikšmė turi būti **Prijungta**. Daugiau informacijos žr. [Darbo su „Planning Optimization“ pradžia](get-started.md).

**Pataisa**: įsitikinkite, kad papildinys „Planning Optimization“ buvo įdiegtas sėkmingai.

## <a name="error-message-is-shown-during-ctp"></a>Klaidos pranešimas rodomas CTP metu

Jei galimas pateikti atsargas (CTP) bandysite vykdyti iš pardavimo užsakymo esant įgalintam „Planning Optimization“, gausite tokį klaidos pranešimą: *Ši operacija suaktyvino bendrąjį planavimą, kuris nepalaikomas, kai įgalintas „Planning Optimization“*.

Tai susiję su laukimo funkcija, kuri yra suplanuota kaip gamybos užsakymų palaikymo dalis.

**Pataisa:** venkite CTP skaičiavimų, kai įgalintas „Planning Optimization“, kol bus galima naudoti CTP palaikymą.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo su planavimo optimizavimu pradžia](get-started.md)

[Planavimo optimizavimo tinkamumo analizė](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]