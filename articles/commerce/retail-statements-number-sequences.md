---
title: Nustatyti mažmeninės prekybos išrašų numeraciją
description: Šiame straipsnyje aprašoma, kaip konfigūruoti numeraciją, kurios reikia mažmeninės prekybos išrašams Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 917d7b7a905a822ca3b1e074055fe0cd4af5555b
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027191"
---
# <a name="set-up-number-sequences-for-retail-statements"></a>Nustatyti mažmeninės prekybos išrašų numeraciją

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip konfigūruoti numeraciją, kurios reikia mažmeninės prekybos išrašams Microsoft Dynamics 365 Commerce.

Du mažmeninės prekybos išrašų tipai naudojami Dynamics 365 Commerce: 

- **Operacijų išrašai** turi būti kuriami ir registruojami labai dažnai. Jos naudojamos registruoti visas nefinansinių operacijų parduotuvėse į būstinę Dynamics 365 Commerce. 
- **Finansinės ataskaitos** yra skirtos kurti ir registruoti vieną kartą per darbo dieną. Jos apima tik uždarytas pamainas iš mažmeninės prekybos parduotuvių, kurios vykdant p užduotį nusiųstos į "Commerce Headquarters".

## <a name="configure-a-number-sequence-for-statement-posting"></a>Konfigūruoti išrašų registravimo numeraciją

Baigę nustatyti parduotuvę "Commerce Headquarters", turite sukonfigūruoti unikalią numeraciją, kuri bus naudojama išrašams kuriant išrašus.

Norėdami konfigūruoti išrašų registravimo "Commerce Headquarters" numeraciją, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimas \> Numeracijos \> Numeracijos**.
1. Norėdami **sukurti \> naują įrašą,** pasirinkite Nauja numeracija.
1. Skirtuke **Identifikavimas** "FastTab" numeracijos **kodo** lauke įveskite numeracijos kodą.
1. **Lauke Numeracijos** pavadinimas įveskite pavadinimą.
1. Aprėpties **parametrų** "FastTab", lauke **Apimtis**, pasirinkite Valdymo **vienetas**.
1. Lauke Valdymo **vienetas** pasirinkite parduotuvę, kurioje bus naudojama numeracija.
1. Segmentų **"** FastTab" apibrėžkite segmentus.
1. Nuorodos "**FastTab**" lauke Sritis nustatykite **kaip** Parduotuvės **parduotuvė**.
1. Nustatykite **nuorodos lauką** **kaip Išrašo** numeris ir pasirinkite **Gerai**.

    ![Identifikavimas, aprėpties parametrai, segmentai ir nuorodos "FastTab" numeracijų puslapyje.](media/retail-statements-num-seq-setup-01.png)

1. Bendrosios FastTab **dalies** Numerių paskirstymas dalyje atnaujinkite laukus Mažiausia ir Didžiausia, kad jie atitiktų raidinio-skaitinio segmento, **kurį** apibrėšite "FastTab" segmentuose **·**,**·** **·** **ilgį**.
1. Našumo "**FastTab**" rekomenduojame nustatyti **parinktį** **Išankstinis paskirstymas kaip Taip**, o numerių **kiekio** lauke – **25**.

    ![Bendrosios ir našumo "FastTab" numeracijų puslapyje.](media/retail-statements-num-seq-setup-02.png)

1. Veiksmų srityje pasirinkite Įrašyti, **kad įrašytumėte** pakeitimus, ir uždarykite puslapį.
