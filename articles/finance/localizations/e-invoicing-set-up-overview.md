---
title: Elektroninių sąskaitų faktūrų išrašymo sąranka
description: Šioje temoje apžvelgiamas elektroninių SF nustatymo ir konfigūravimo procesas.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 42e617e26e7658fae9ee54cb8a4dee45314fddaa
ms.sourcegitcommit: 5f7177b9ab192b5a6554bfc2f285f7cf0b046264
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661698"
---
# <a name="electronic-invoicing-setup"></a>Elektroninių sąskaitų faktūrų išrašymo sąranka

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama elektroninių SF nustatymo ir konfigūravimo proceso apžvalga. Turite atlikti nustatymo veiksmus čia nurodyta tvarka. Jei veiksmas yra privalomas, bet praleidžiate jį, funkcija neveiks tinkamai, o vėlesnių veiksmų metu arba naudojant funkciją atsiras daug gedimų. 

Prieš pradėdami įsitikinkite, kad visi pagrindiniai komponentai nustatyti teisingai, kad prisiregistravote naudoti reguliavimo konfigūravimo tarnybą (RCS) ir turite RCS egzempliorių, ir kad elektroninis SF išrašymo priedas yra įdiegtas jūsų Microsoft Dynamics "365 Finance" arba Dynamics 365 Supply Chain Management aplinkai. Daugiau informacijos ieškokite [Prisiregistruokite ir įdiekite Elektroninę SF išrašymą](e-invoicing-install-add-in-microservices-lcs.md).

Tada nustatykite "Azure" išteklius, kurių darbui atlikti reikia elektroniniam SF išrašymui. Daugiau informacijos ieškokite [Set up Azure resources for Electronic INSIGNING](e-invoicing-set-up-azure-resources.md).

Konfigūravus pagrindinius komponentus, dirbkite su RCS, kad nustatytumėte pagrindinius loginius elektroninių SĄSKAITŲ faktūrų išrašymo komponentus. Pirma, apibrėžkite aptarnavimo aplinkų, kurias išlaikysite, skaičių. Tokiu būdu apibrėžiate loginius duomenis ir konfigūracijos skaidymą, kad įsitikintumėte, jog turite ribą tarp kūrimo ar bandymo aplinkos ir gamybos aplinkų. Jei norite lanksčiai nustatyti kūrimo procesą, gali prireikti kelių atskirų kūrimo ir bandymų aplinkų. Be aptarnavimo aplinkų apibrėžimo, nustatykite nuorodą į savo verslo programas, pvz., "Finance" arba "Supply Chain Management", tiesiogiai iš RCS, kad nustatytumėte parametrus, reikalingus tinkamam veikimui naudojant elektronines SF. Daugiau informacijos apie aplinkas ieškokite [Service environments](e-invoicing-service-environments.md).

Kai viskas bus nustatyta, galite sukurti savo globalizacijos funkcijas, kurios apibrėžia skirtingus elektroninių dokumentų apdorojimo ir duomenų transformavimo scenarijus arba dokumentų importavimą iš visuotinės saugyklos. Daugiau informacijos apie tai, kaip dirbti su globalizacijos funkcijomis, ieškokite [Work with Globalization features](e-invoicing-working-globalization-features.md).

Jei jūsų scenarijus reikia integruoti su el. paštu arba SharePoint apdoroti gaunamus elektroninius dokumentus, informacijos apie tai, kaip nustatyti ir naudoti tuos kanalus, ieškokite [Gaunamų elektroninių dokumentų](e-invoicing-process-incoming-electronic-documents.md) apdorojimas.
