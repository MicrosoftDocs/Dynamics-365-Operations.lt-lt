--- 
title: "Kurti gamybos užsakymą"
description: "Šioje procedūroje nurodoma, kaip kurti gamybos užsakymą."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ac2ee418082aa6579424fc9480478587b7c22c6d
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-production-order"></a>Kurti gamybos užsakymą

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje nurodoma, kaip kurti gamybos užsakymą. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Tai yra pirmoji procedūra iš septynių, kurioje paaiškinamas gamybos užsakymo ciklas.


## <a name="create-a-production-order"></a>Kurti gamybos užsakymą
1. Pasirinkite Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai.
2. Spustelėkite Naujas gamybos užsakymas.
3. Lauke „Prekės numeris“ įveskite „D0001“.
4. Lauke Pristatymas įveskite datą.
    * Pristatymo data nurodo, kada turėtų baigtis gamybos užsakymas, kad būtų pristatyta laiku. Šią datą galima naudoti planavimo procese. Pavyzdžiui, užsakymą galite planuoti atgal nuo pristatymo datos.  
5. Nustatykite kiekį – 20.
    * Pastaba: KS skaičiaus lauke automatiškai rodomas visų aktyvių dabartinės prekės KS skaičius, tačiau gamybos užsakymo KS galite keisti iš patvirtintų KS versijų sąrašo pasirinkdami aktyvią KS.    Lauke Maršrutų skaičius automatiškai rodomas visų aktyvių dabartinės prekės maršrutų skaičius, tačiau gamybos užsakymo maršrutą galite keisti iš patvirtintų maršrutų versijų sąrašo pasirinkdami aktyvų maršrutą.  
6. Spustelėkite Kurti.

## <a name="validate-the-production-order"></a>Tikrinti gamybos užsakymą
1. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Spustelėkite gamybos užsakymo numerio, kurį ką tik sukūrėte, saitą. Bus atidarytas užsakymo informacijos puslapis.  
2. Spustelėkite Redaguoti.
3. Lauke Pristatymas įveskite datą.
    * Pavyzdžiui, galite keisti gamybos užsakymo pristatymo datą.  
4. Spustelėkite Įrašyti.
5. Uždarykite puslapį.

## <a name="update-the-bom"></a>Naujinti KS
1. Veiksmų srityje spustelėkite Gamybos užsakymas.
2. Spustelėkite KS.
    * Atidarykite KS puslapį, kad patikrintumėte KS duomenis, nukopijuotus iš numatytųjų duomenų kuriant gamybos užsakymą. Atliekant šią procedūrą, reikia atnaujinti KS kiekį.  
3. Spustelėkite Redaguoti.
4. Lauke Kiekis įveskite skaičių.
    * Kiekio KS eilutėje keitimas turi įtakos gamybos užsakymo medžiagų suvartojimo išlaidų įvertinimui.  
5. Spustelėkite Įrašyti.
6. Uždarykite puslapį.

## <a name="update-the-production-route"></a>Naujinti gamybos maršrutą
1. Veiksmų srityje spustelėkite Gamybos užsakymas.
2. Spustelėkite Maršrutas.
    * Atidarykite puslapį Maršrutas, kad patikrintumėte gamybos maršruto duomenis, nukopijuotus iš numatytųjų duomenų kuriant užsakymą. Atliekant šią procedūrą, reikia atnaujinti vienos iš gamybos maršruto operacijų kiekį.  
3. Sąraše raskite ir pasirinkite norimą įrašą.
4. Spustelėkite Redaguoti.
5. Proceso kiekis. įveskite skaičių.
    * Vykdymo laiko keitimas turi įtakos gamybos užsakymo apskaičiuotam maršruto suvartojimui ir išlaidoms.  
6. Spustelėkite Įrašyti.
7. Uždarykite puslapį.


