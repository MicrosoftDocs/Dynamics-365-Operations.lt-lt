---
title: Nustatyti pageidaujamus priežiūros darbuotojus
description: Šioje temoje aiškinama, kaip nustatyti pageidaujamus priežiūros darbuotojus skiltyje Turto valdymas.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 511d875baed029df9083da36baf6c48ca4b7abf866ae569038b554bf594473c8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734432"
---
# <a name="set-up-preferred-maintenance-workers"></a>Nustatyti pageidaujamus priežiūros darbuotojus

[!include [banner](../../includes/banner.md)]

 

Planuodami darbo užsakymus galite nustatyti priežiūros darbuotojų ar darbuotojų grupių pasirinkimo atlikti darbo užsakymą pirmumą. Ši funkcija yra nebūtina, tačiau ji gali būti naudinga sprendžiant dėl labiausiai kvalifikuoto priežiūros darbuotojo užduočiai atlikti, atsižvelgiant į darbuotojo įgūdžius ir kompetencijas. Tik tie priežiūros darbuotojai, kurie yra pasiekiami planuojamo užsakymo metu, pateks į grafiką. Jei planuojant užsakymą pageidaujamo priežiūros darbuotojo sąranka atitiks darbo užsakymą, bet priežiūros darbuotojas paskirtas atlikti kitus darbus, darbo užsakymas bus paskirtas kitam pasiekiamam priežiūros darbuotojui.

Kad galėtumėte nustatyti pageidaujamus priežiūros darbuotojus, pirmiausia turite nustatyti priežiūros darbuotojus ir darbuotojų grupes. Norėdami sužinoti, kaip nustatyti priežiūros darbuotojus ir darbo grupes, žr. [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-preferred-workers"></a>Pageidaujamų priežiūros darbuotojų sąranka

Pageidaujamas priežiūros darbuotojas ar darbuotojų grupė gali būti susijusi konkrečiai su vienu ar daugiau toliau nurodytu aspektu.

- prekyba  
- priežiūros užduoties tipo variantu  
- priežiūros užduoties tipu  
- priežiūros užduoties tipo kategorija  
- turtas  
- turto tipu  

Kuo daugiau atrankos kriterijų sukursite tam pačiam įrašui, tuo konkretesnė bus sąranka.

1. Spustelėkite **Turto valdymas** > **Sąranka** > **Darbuotojai** > **Pageidaujami priežiūros darbuotojai**.

2. Spustelėję **Naujas** sukurkite naują įrašą.

3. Pirmiausia sukurkite „numatytąjį” priežiūros darbuotoją ar darbuotojų grupę. Tokiu būdu jūs atrinksite tik naudodamiesi lauku **Pageidaujama priežiūros darbo grupė** arba lauku **Pageidaujamas priežiūros darbuotojas**. Toliau ekrano kopijoje galite matyti pavyzdį pirmajame įraše, kuriame „Užklausos“ pasirinktos kaip **Pageidaujama priežiūros darbuotojų grupė**.

    [!NOTE] Numatytoji konfigūracija bus naudojama darbo užsakymų planavimo metu, jei nebus rasta jokia kita, konkrečiau darbo užsakymo turinį atitinkanti kombinacija.

4. Kartokite 2 žingsnį, kad sukurtumėte naują įrašą. Nustatykite reikiamus atrankos kriterijus priklausomai nuo išsamumo lygio pageidaujamam darbuotojui ar darbo grupei. 

    *Pavyzdys:* toliau ekrano kopijoje, šeštame įraše, priežiūros darbuotojas Šonas Ričardsonas pasirenkamas kaip pageidaujamas darbuotojas. Jis bus automatiškai atrinktas planuojant darbo užsakymą, kuriame pateikiamas turtas CH-BP1-03-02, o priežiūros užduoties tipas – „Patalpų įvertinimas“, jei jis bus pasiekiamas grafike nustatytu laiku.

    [!NOTE] Įprastai, kai pageidaujamas priežiūros darbuotojas pasirenkamas sudarant darbo užsakymo grafiką, Turto valdyme peržiūrimi visi įrašai **Pageidaujami priežiūros darbuotojai** dėl galimų atitikimų, visada pirmiausiai atsižvelgiama į sudėtingiausią derinį. Jei nerandama atitikimų, naudojami „numatytieji“ įrašai su atrankos kriterijais, nurodytais lauke **Pageidaujama priežiūros darbo grupė** ar lauke **Pageidaujamas priežiūros darbuotojas**.

![1 iliustracija.](media/02-work-order-scheduling.png)

Taip pat galite nustatyti *atsakingus* priežiūros darbuotojus, kurie gali būti atrinkti, kai sukuriama priežiūros užklausa arba darbo užsakymas. Jeigu reikia, galite keisti atrankos kriterijus skiltyse **Visi darbo užsakymai** ir **Visos priežiūros užklausos**. Daugiau informacijos žr. [Atsakingi priežiūros darbuotojai](../setup-for-maintenance-requests/responsible-workers.md).

Kuriant darbo užsakymo grafiką skaičiuojami įvairūs įverčiai, siekiant nustatyti, kuriam darbuotojui turi būti paskirta atlikti užduotis, susijusias su darbo užsakymu (tokie įverčiai yra nustatomi nuorodoje **Turto valdymo parametrai** > **Darbo užsakymų planavimas**). Jei du ar daugiau pageidaujami priežiūros darbuotojai ar atsakingi priežiūros darbuotojai įvertinami taip pat, planuojant darbo užsakymą, vienas darbuotojas yra pasirenkamas atsitiktine tvarka. Kitaip, darbuotojas, surinkęs didžiausią įvertį, visada bus paskirtas atlikti darbo užsakymą.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]