---
title: Projekto įvertinimų šalinimas
description: Šioje temoje pateikiama informacija apie projekto įvertinimų šalinimą po to, kai jis užbaigiamas.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410246"
---
# <a name="eliminate-a-project-estimate"></a>Projekto įvertinimų šalinimas

[!include [banner](../includes/banner.md)]

Projekto įvertinimai yra darbo, kuris apskaičiuotas ir suplanuotas projektui, finansinis rodinys. Norėdami dirbti su projekto įvertinimais, turite pridėti projektą prie vertinamo projekto. Vertinamas projektas visada pagrįstas esamu projektu, tačiau keli projektai gali nurodyti vieną vertinamą projektą. Prie vertinamų projektų galima pridėti tik fiksuotos kainos ir investicijų projektus, o šie projektai turi priklausyti tai pačiai projektų grupei kaip vertinamas projektas.

Norint pašalinti vertinamą projektą, jis turi būti užbaigtas. Toliau pateikti veiksmai paaiškina, kaip pašalinti įvertinimą.

1. Eikite į **Projektų valdymas ir apskaita** > **Visi projektai** ir atidarykite projektą. 
2. Skirtuke **Valdymas** pasirinkite **Įvertinimai**, o puslapyje **Įvertinimas** pasirinkite **Pašalinti**.
3. Puslapyje **Įvertinimo šalinimas**, skirtuke **Bendra**, nustatykite toliau išvardytas parinktis.

   - **Laikotarpio kodas** – pasirinkite laikotarpio kodą, kad galėtumėte pasirinkti atitinkamus vertinamus projektus. 
   - **Įvertinimo data** – pasirinkite atitinkamą įvertinimo šalinimo datą.
   - **Pašalinti su NG įspėjimais** – įjunkite šią pasirinktį, kad būtų rodomas pranešimas, kai pašalinamas su nebaigta gamyba (NG) susijęs įvertinimas. Kai ši parinktis neįjungta, šalinimas negali tęstis, jei yra neįvertintų operacijų. 
   > [!NOTE]
   > Ši pasirinktis galima tik tada, kai šalinimas taikomas vertinamam projektui. Ji negalima, jei naudojate periodinius registravimus. Šis parametras veikia kartu su parametrais, esančiais skirtuke **Įvertinimas**, puslapyje **Projekto parametrai**, laukų grupėje **Leisti pašalinti, kai yra neįvertintų operacijų**.
   - **Nustatyti užbaigimo etapą** – įjunkite šią pasirinktį norėdami nustatyti vertinamo projekto etapą į **Baigtas** po to, kai atliekate šalinimą.
   - **Spausdinti įvertinimų sąrašą** – pasirinkite informaciją, kuri bus įtraukta spausdinant įvertinimų sąrašą.
   - **Rodyti sistemos pranešimą** – įjunkite šią pasirinktį, kad būtų rodomas sistemos pranešimas.
   - **Registravimo data** – pasirinkite įvertinimo didžiosios knygos registravimo datą.

4.  Pasirinkite **Gerai**.
5. Užbaigus šalinimo procesą, pašalintas vertinimas projektas rodomas su neigiama verte. 

Jei neketinote šalinti įvertinimo, galite pasirinkti pašalintą įvertinimą ir spustelėti **Atšaukti šalinimą**.   
