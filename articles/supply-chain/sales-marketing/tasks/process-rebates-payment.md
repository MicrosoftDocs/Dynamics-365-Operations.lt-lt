---
title: Apdoroti mokėjimo grąžinimus
description: Ši procedūra nurodo, kaip konvertuoti patvirtintus ir apdorotus grąžinimus klientams į kredito pažymas.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 617b5d99973e630cca2973227c2e54a63bd1ec4d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263305"
---
# <a name="process-rebates-for-payment"></a>Apdoroti mokėjimo grąžinimus

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip konvertuoti patvirtintus ir apdorotus grąžinimus klientams į kredito pažymas. Šį vadovą galite naudoti demonstracinėje įmonėje USMF. Išankstinė šio vadovo sąlyga – turėti vieną ar daugiau grąžinimo pretenzijų, kurių būsena yra „Žymėti“. Jei naudojate USMF, prieš šį vadovą rekomenduojama įvykdyti „Generuoti ir apdoroti kliento grąžinimus“.


## <a name="convert-rebate-claims-to-credit-note"></a>Konvertuoti grąžinimo pretenzijas į kredito pažymą
1. Eikite į „Visi klientai“.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Veiksmų srityje spustelėkite Rinkti.
5. Spustelėkite „Sudengti operacijas“.
6. Spustelėkite Funkcijos.
7. Spustelėkite „Grąžinimo programa“.
    * Puslapyje „Grąžinimai“ surašytos grąžinimo pretenzijos, kurias apdorojote kliento grąžinimų darbo srityje ir kurių būsena yra „Žymėti“.    
8. Spustelėkite Redaguoti.
    * Lauke „Žymėti“ nustatykite žymes pretenzijose, kurias norite įtraukti į kredito pažymą.   
9. Spustelėkite Funkcijos.
10. Spustelėkite „Sukurti kredito pažymą“.
    * Rodomas pranešimas, kuris jus informuoja, kad žurnalas buvo užregistruotas (tai gautinų sumų suvartojimo žurnalas, kaip nurodyta puslapyje „Gautinų sumų parametrai“). Tai lemia, kad tikrosios atsakomybės (kredito) suma perkeliama į kliento balansą. Tai reiškia, kad kliento sąskaita kredituojama, o grąžinimo kaupimo sąskaita debetuojama.  
11. Uždarykite puslapį.
12. Spustelėkite Atšaukti.
    * Tai atnaujina puslapį, kad matytumėte atnaujinimus.  
13. Veiksmų srityje spustelėkite Rinkti.
14. Spustelėkite „Sudengti operacijas“.
    * Atkreipkite dėmesį, kad į kliento balansą įtraukta operacija su neigiama suma, kuri atitinka bendrą grąžinimo sumą, be sąskaitos faktūros nuorodos.   
15. Spustelėkite Atšaukti.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]