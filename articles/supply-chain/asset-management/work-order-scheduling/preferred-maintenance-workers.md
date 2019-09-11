---
title: Nustatyti pageidaujamus priežiūros darbuotojus
description: Šioje temoje aiškinama, kaip nustatyti pageidaujamus priežiūros darbuotojus skiltyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887416"
---
# <a name="preferred-maintenance-workers"></a>Pageidaujami priežiūros darbuotojai

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Planuodami darbo užsakymus galite nustatyti priežiūros darbuotojų pasirinkimo atlikti darbo užsakymą pirmumą. Ši funkcija yra nebūtina, tačiau ji gali būti naudinga sprendžiant dėl labiausiai kvalifikuoto priežiūros darbuotojo užduočiai atlikti, atsižvelgiant į darbuotojo įgūdžius ir kompetencijas. Taigi, planuojant darbo užsakymą sąranka **Pageidaujami priežiūros darbuotojai** yra naudojama sprendžiant dėl konkretaus priežiūros darbuotojo ar darbo grupės skyrimo atlikti darbo užsakymą. Tik tie priežiūros darbuotojai, kurie yra pasiekiami planuojamo užsakymo metu, pateks į grafiką. Jei planuojant užsakymą pageidaujamo priežiūros darbuotojo sąranka atitiks darbo užsakymą, bet priežiūros darbuotojas paskirtas atlikti kitus darbus, darbo užsakymas bus paskirtas kitam pasiekiamam priežiūros darbuotojui.

Prieš pradedant nustatyti pageidaujamus priežiūros darbuotojus, pirmiausia turite nustatyti priežiūros darbuotojus ir darbo grupes, kurios yra pasiekiamos atrankai. Norėdami sužinoti, kaip nustatyti priežiūros darbuotojus ir darbo grupes žr. aprašą [Priežiūros darbuotojai ir darbo grupės](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-preferred-workers"></a>Pageidaujamų priežiūros darbuotojų sąranka

Pageidaujamas priežiūros darbuotojas ar darbo grupė gali būti susijusi konkrečiai su

- prekyba  
- priežiūros užduoties tipo variantu  
- priežiūros užduoties tipu  
- priežiūros užduoties tipo kategorija  
- turtas  
- turto tipu  

arba šių atrankos kriterijų deriniu. Kuo daugiau atrankos kriterijų sukursite tam pačiam įrašui, tuo konkretesnė bus sąranka.

1. Spustelėkite **Turto valdymas** > **Sąranka** > **Darbuotojai** > **Pageidaujami priežiūros darbuotojai**.

2. Spustelėję **Naujas** sukurkite naują įrašą.

3. Pradėkite sukurdami „numatytąją“ priežiūros darbuotojų arba darbo grupių sąranką, kurios laukuose nėra nustatyti atrankos kriterijai, kaip nurodyta viršutiniame ženklelių sąraše. Tokiu būdu jūs atrinksite tik naudodamiesi lauku **Pageidaujama priežiūros darbo grupė** arba lauku **Pageidaujamas priežiūros darbuotojas**. Toliau paveikslėlyje galite matyti pavyzdį pirmajame įraše, kuriame „Užklausos“ pasirinktos kaip pageidaujama priežiūros darbo grupė.

>[!NOTE]
>Numatytoji sąranka bus naudojama planuojant darbo užsakymą tokiu atveju, kai skiriant darbo užsakymą jokia kita, išsamesnė, kombinacija neatitinka darbo užsakymo turinio.

4. Kartokite 2 žingsnį, kad sukurtumėte naują įrašą. Nustatykite reikiamus atrankos kriterijus priklausomai nuo išsamumo lygio pageidaujamam darbuotojui ar darbo grupei. *Pavyzdys:* toliau paveikslėlyje, šeštame įraše, priežiūros darbuotojas Šonas Ričardsonas pasirenkamas kaip pageidaujamas darbuotojas. Jis bus automatiškai atrinktas planuojant darbo užsakymą, kuriame pateikiamas turtas CH-BP1-03-02, o priežiūros užduoties tipas – „Patalpų įvertinimas“, jei jis bus pasiekiamas grafike nustatytu laiku.

>[!NOTE]
>Įprastai, kai pageidaujamas priežiūros darbuotojas pasirenkamas sudarant darbo užsakymo grafiką, Turto valdyme peržiūrimi visi įrašai **Pageidaujami priežiūros darbuotojai** dėl galimų atitikimų, visada pirmiausiai atsižvelgiama į sudėtingiausią derinį. Jei nerandama atitikimų, naudojami „numatytieji“ įrašai su atrankos kriterijais, nurodytais lauke **Pageidaujama priežiūros darbo grupė** ar lauke **Pageidaujamas priežiūros darbuotojas**.


![1 pav.](media/02-work-order-scheduling.png)

Taip pat galite nustatyti atsakingus priežiūros darbuotojus, kurie gali būti atrinkti, kai sukuriama priežiūros užklausa arba darbo užsakymas. Jeigu reikia, galite keisti atrankos kriterijus skiltyse **Visi darbo užsakymai** ir **Visos priežiūros užklausos**. Daugiau informacijos žr. [Atsakingi priežiūros darbuotojai](../setup-for-maintenance-requests/responsible-workers.md).

Kuriant darbo užsakymo grafiką skaičiuojami įvairūs įverčiai, siekiant nustatyti, kuriam darbuotojui turi būti paskirta atlikti užduotis, susijusias su darbo užsakymu (tokie įverčiai yra nustatomi nuorodoje **Turto valdymo parametrai** > **Darbo užsakymų planavimas**). Jei du ar daugiau pageidaujami priežiūros darbuotojai ar atsakingi priežiūros darbuotojai įvertinami taip pat, planuojant darbo užsakymą, vienas darbuotojas yra pasirenkamas atsitiktine tvarka. Kitaip, darbuotojas, surinkęs didžiausią įvertį, visada bus paskirtas atlikti darbo užsakymą.

