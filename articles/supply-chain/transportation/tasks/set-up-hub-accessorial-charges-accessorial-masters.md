---
title: Nustatyti tranzito punktų papildomų paslaugų išlaidas ir papildomų paslaugų šablonus
description: Ši procedūra nurodo, kaip sukurti tranzito punkto papildomų paslaugų šabloną ir jį panaudoti tranzito punkto papildomų paslaugų mokesčiui sukurti.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad89afe0a21261c57311c439153b969d837748e4
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434054"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a>Nustatyti tranzito punktų papildomų paslaugų išlaidas ir papildomų paslaugų šablonus

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip sukurti tranzito punkto papildomų paslaugų šabloną ir jį panaudoti tranzito punkto papildomų paslaugų mokesčiui sukurti. Procedūra naudoja USMF duomenų rinkinį. Šį nustatymą paprastai atlieka transportavimo koordinatorius.


## <a name="set-up-a-hub-master"></a>Pagrindinio tranzito punkto nustatymas
1. Pasirinkite Transportavimo valdymas > Nustatymas > Vertinimas > Papildomų paslaugų šablonai.
2. Spustelėkite Naujas.
3. Lauke „Papildomų paslaugų šablonas“ įveskite reikšmę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke „Papildomų paslaugų tipas“ pasirinkite „Tranzito punktas“.
6. Spustelėkite Įrašyti.
7. Uždarykite puslapį.

## <a name="set-up-a-hub-accessorial-charge"></a>Nustatyti tranzito punkto papildomų paslaugų mokestį
1. Pasirinkite Transportavimo valdymas > Nustatymas > Vertinimas > Tranzito punkto papildomų paslaugų mokesčiai.
2. Spustelėkite Naujas.
3. Lauke „Tranzito punkto papildomų paslaugų ID“ įveskite reikšmę.
4. Lauke „Tranzito punktas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Sąraše raskite ir pasirinkite norimą įrašą.
6. Lauke „Tranzito punkto padėtis“ pasirinkite parinktį.
    * Galite sukurti mokestį už paėmimą arba atidavimą. Atsižvelgiant į jūsų pasirinkimą, mokestis bus taikomas atitinkamam transportavimo segmentui jūsų maršrute.  
7. Lauke „Papildomų paslaugų šablonas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pasirinkite šabloną, kurį ką tik sukurėte.  
9. Spustelėkite Įrašyti.
10. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]