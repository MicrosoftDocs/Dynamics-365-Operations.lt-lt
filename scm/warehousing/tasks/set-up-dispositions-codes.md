--- 
title: Nustatyti perdavimo kodus
description: "Šios procedūros tikslas yra nustatyti perdavimo kodą, kuris gali būti naudojamas mobiliajame įrenginyje, vykdant grąžinimo užsakymo gavimo procesą."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: cefa614ed68d6f6f72b31b3b55fba77f0f02e889
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-dispositions-codes"></a>Nustatyti perdavimo kodus

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šios procedūros tikslas yra nustatyti perdavimo kodą, kuris gali būti naudojamas mobiliajame įrenginyje, vykdant grąžinimo užsakymo gavimo procesą. Perdavimo kodai yra rinkinys taisyklių, kurios gali būti taikomos gaunant prekes. Pvz., kai darbo vartotojas mobiliuoju įrenginiu priima pažeistas prekes, vartotojas turi nuskaityti pažeistų prekių perdavimo kodą. Nuskaičius perdavimo kodą galima nustatyti gautų prekių atsargų būseną, darbo šabloną ir vietos nurodymą. Perdavimo kodo neprivaloma naudoti pirkimo užsakymo gavimo procese ir gamybos užsakymo paskelbimo baigtu procese. Vykdant pardavimo užsakymo grąžinimo gavimo procesą, jei prekės registruotos mobiliuoju įrenginiu, naudoti perdavimo kodą yra privaloma.  Šis vadovas buvo sukurtas naudojant demonstracinių duomenų įmonę USMF. Ši procedūra skirta sandėlio vadovui. 

1. Pasirinkite > Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Perdavimo kodai.
2. Spustelėkite Naujas.
    * Sukurkite naują perdavimo kodą, naudojamą klientų grąžinamoms prekėms.  
3. Lauke „Perdavimo kodas“ įveskite reikšmę.
4. Lauke „Atsargų būsena“ pasirinkite atsargų būseną, kai taikomas atsargų blokavimas.
    * Jei naudojate USMF, pasirinkite „Blokavimas“. Į perdavimo kodą galima įtraukti atsargų būseną, kad būtų perrašyta užsakymo eilutėse esanti numatytoji būsena.  
5. Lauke „Darbo šablonas“ įveskite reikšmę.
    * Pasirinktinai: pasirinkite darbo šablono kodą, susijusį su grąžinimo užsakymu. Jei nenurodyta jokia reikšmė, darbo šablonas bus išspręstas naudojant standartines jūsų sistemoje sukonfigūruotas taisykles. Darbo šablono pasirinkimas apribos skaičių procesų, kuriuose galima naudoti šį perdavimo kodą. Pvz., jei perdavimo kodas turi darbo šabloną su pirkimo užsakymo tipo darbo užsakymu, juo nebus galima registruoti prekių, kurias grąžina klientai.  
6. Lauke „Grąžinti perdavimo kodą“ įveskite reikšmę.
    * Grąžinimo perdavimo kodas nulemia registruotų prekių grąžinimo užsakymo proceso likutį. Šiame pavyzdyje klientas turėtų gauti kredito pažymą. Įtraukite grąžinimo perdavimo kodą, kuriame yra veiksmas „Kreditas“.  


