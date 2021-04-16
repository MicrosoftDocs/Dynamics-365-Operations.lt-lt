---
title: Nustatyti perdavimo kodus
description: Šios procedūros tikslas yra nustatyti perdavimo kodą, kuris gali būti naudojamas mobiliajame įrenginyje, vykdant grąžinimo užsakymo gavimo procesą.
author: ShylaThompson
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16458f709788e538d036cc4d3b3239f4ffa3c42e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830935"
---
# <a name="set-up-dispositions-codes"></a>Nustatyti perdavimo kodus

[!include [banner](../../includes/banner.md)]

Šios procedūros tikslas yra nustatyti perdavimo kodą, kuris gali būti naudojamas mobiliajame įrenginyje, vykdant grąžinimo užsakymo gavimo procesą. Perdavimo kodai yra rinkinys taisyklių, kurios gali būti taikomos gaunant prekes. Pvz., kai darbo vartotojas mobiliuoju įrenginiu priima pažeistas prekes, vartotojas turi nuskaityti pažeistų prekių perdavimo kodą. Nuskaičius perdavimo kodą galima nustatyti gautų prekių atsargų būseną, darbo šabloną ir vietos nurodymą. Perdavimo kodo neprivaloma naudoti pirkimo užsakymo gavimo procese ir gamybos užsakymo paskelbimo baigtu procese. Vykdant pardavimo užsakymo grąžinimo gavimo procesą, jei prekės registruotos mobiliuoju įrenginiu, naudoti perdavimo kodą yra privaloma.  Šis vadovas buvo sukurtas naudojant demonstracinių duomenų įmonę USMF. Ši procedūra skirta sandėlio vadovui. 

1. Pasirinkite > Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Perdavimo kodai.
2. Spustelėkite Naujas.
    * Sukurkite naują perdavimo kodą, naudojamą klientų grąžinamoms prekėms.  
3. Lauke „Perdavimo kodas“ įveskite reikšmę.
4. Lauke „Atsargų būsena“ pasirinkite atsargų būseną, kai taikomas atsargų blokavimas.
    * Jei naudojate USMF, pasirinkite „Blokavimas“. Norėdami pakeisti numatytąją užsakymo eilutėse esančią būseną, prie perdavimo kodo galite pridėti atsargų būseną.  
5. Lauke „Darbo šablonas“ įveskite reikšmę.
    * Pasirinktinai: pasirinkite darbo šablono kodą, susijusį su grąžinimo užsakymu. Jei nenurodyta jokia reikšmė, darbo šablonas bus išspręstas naudojant standartines jūsų sistemoje sukonfigūruotas taisykles. Darbo šablono pasirinkimas apribos skaičių procesų, kuriuose galima naudoti šį perdavimo kodą. Pavyzdžiui., jei perdavimo kodas turi darbo šabloną su tipo pirkimo užsakymo darbo užsakymu, jo negalima naudoti, jei norite registruoti klientų grąžinamas prekes.  
6. Lauke „Grąžinti perdavimo kodą“ įveskite reikšmę.
    * Grąžinimo perdavimo kodas nulemia registruotų prekių grąžinimo užsakymo proceso likutį. Šiame pavyzdyje klientas turėtų gauti kredito pažymą. Įtraukite grąžinimo perdavimo kodą, kuriame yra veiksmas „Kreditas“.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]