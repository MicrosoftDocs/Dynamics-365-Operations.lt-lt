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
ms.openlocfilehash: 37c38ab9cec8ae3c9d4decf8043b43ea2251083e
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739735"
---
# <a name="troubleshoot-planning-optimization"></a>„Planning Optimization“ trikčių diagnostika 

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip išspręsti bendrąsias problemas, su kuriomis galite susidurti naudodami planavimo optimizavimą.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>„Planning Optimization“ papildinio diegimas nebaigtas

Norint naudoti „Planning Optimization“, reikalinga įgalinta „Lifecycle Services“ (LCS), plačiai pasiekiama 2 ar aukštesnės pakopos aplinka (ne „OneBox” aplinka), turinti „Dynamics 365 Supply Chain Management” 10.0.7 arba naujesnę versiją. Jei papildinį bandysite įdiegti „OneBox“ aplinkoje, diegimas nebus baigtas.

**Pataisymas**: atšaukite diegimą ir naudokite plačiai pasiekiamą 2 ar aukštesnės pakopos aplinką (ne „OneBox“ aplinką).

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>Kai „Planning Optimization“ įgalintas, nepavyksta suplanuoti paketinių užduočių

Įgalinus planavimo optimizavimą, automatiškai išjungiamas pasenusias bendrojo planavimo modulis. Bendrojo planavimo paketinės užduotys, kurios buvo sukurtos pasenusiam bendrojo planavimo moduliui, bus nesėkmingos, jei jos bus paleistos įgalinus planavimo optimizavimą. Galite gauti klaidos pranešimą, pvz., *Ši operacija suaktyvino bendrąjį planavimą, kuris nepalaikomas, kai įgalintas „Planning Optimization“*.

**Taisyti**: atšaukite visas bendrojo planavimo paketines užduotis, kurios buvo sukurtos pasenusiam bendrojo planavimo moduliui.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>„Planning Optimization“ rezultatai skiriasi nuo ankstesnių rezultatų

Planavimo optimizavimas skiriasi nuo pasenusio bendrojo planavimo modulio dizaino kai kuriose srityse. Tai gali lemti ir laukimo funkcijos.

**Pataisymas**: vykdyti „Planning Optimization“ tinkamumo analizę, tada analizuoti rezultatus nurodant susijusius dokumentus, kad būtų galima suprasti poveikį. Daugiau informacijos žr. [„Planning Optimization“ tinkamumo analizė](planning-optimization-fit-analysis.md).

## <a name="cant-enable-planning-optimization"></a>Nepavyksta įgalinti „Planning Optimization“

Jei parinkties **Naudoti „Planning Optimization“** reikšmę norite nustatytai kaip **Taip**, **Ryšio būsena** reikšmė turi būti **Prijungta**. Daugiau informacijos žr. [Darbo su „Planning Optimization“ pradžia](get-started.md).

**Pataisa**: įsitikinkite, kad papildinys „Planning Optimization“ buvo įdiegtas sėkmingai.

## <a name="error-message-is-shown-during-ctp"></a>Klaidos pranešimas rodomas CTP metu

Jei galimas pateikti atsargas (CTP) bandysite vykdyti iš pardavimo užsakymo esant įgalintam „Planning Optimization“, gausite tokį klaidos pranešimą: *Ši operacija suaktyvino bendrąjį planavimą, kuris nepalaikomas, kai įgalintas „Planning Optimization“*.

Tai susiję su laukimo funkcija, kuri yra suplanuota kaip gamybos užsakymų palaikymo dalis.

**Pataisa:** venkite CTP skaičiavimų, kai įgalintas „Planning Optimization“, kol bus galima naudoti CTP palaikymą.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Bendrojo planavimo pradžia](get-started.md)
- [Planavimo optimizavimo tinkamumo analizė](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]