---
title: Elektroninių SF išrašymo nustatymas
description: Šiame straipsnyje pateikta proceso, kaip nustatyti ir konfigūruoti elektroninių SF išrašymą, apžvalga.
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
ms.openlocfilehash: 8e2aa89119530a0ba00a8561d94006285d67a71b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883125"
---
# <a name="electronic-invoicing-setup"></a>Elektroninių SF išrašymo nustatymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama proceso, kaip nustatyti ir konfigūruoti elektroninį SF išrašymą, apžvalga. Nustatymo veiksmus turite atlikti nurodyta tvarka. Jei veiksmas privalomas, bet jį praleisite, funkcija veikia netinkamai, o atliekant vėlesnius veiksmus arba naudojant funkciją įvyks keletas trikčių. 

Prieš pradėdami įsitikinkite, kad visi pagrindiniai komponentai nustatyti teisingai, ar esate prisiregistravę prie reguliavimo konfigūracijos tarnybos (RCS) ir turite RCS egzempliorių ir Microsoft Dynamics ar įdiegtas elektroninių SF išrašymo priedas, skirtas jūsų 365 Dynamics 365 Supply Chain Management finansams arba aplinkai. Norėdami gauti daugiau informacijos, žr. Elektroninių [SF išrašymo prisiregistravimo ir diegimo metu](e-invoicing-install-add-in-microservices-lcs.md).

Tada nustatykite "Azure" išteklius, kurių elektroninio SF išrašymo atveju reikia atlikti darbą. Norėdami gauti daugiau informacijos, žr. ["Azure" išteklių nustatymas elektroninių SF išrašymo metu](e-invoicing-set-up-azure-resources.md).

Sukonfigūrę pagrindinius komponentus, kartu su RCS nustatykite pagrindinius loginius elektroninių SF išrašymo komponentus. Pirmiausia nurodykite aptarnavimo aplinkos, kurias išlaikysite, skaičių. Tokiu būdu apibrėžiate loginius duomenis ir konfigūracijos skaidymo duomenis, norėdami užtikrinti, kad turite ribą tarp programavimo arba tikrinimo aplinkos ir gamybos aplinkos. Norint jūsų programavimo procesą nustatyti lanksčiu būdu, gali reikėti kelių atskirų programavimo ir tikrinimo aplinkos. Be paslaugų aplinkos nustatymo, nustatykite saitą į savo verslo programas, pvz., finansų arba tiekimo grandinės valdymą, tiesiogiai iš RCS, norėdami nustatyti parametrus, kurie reikalingi tinkamai operacijai naudojant elektroninį SF išrašymą. Daugiau informacijos apie aplinkas žr. tarnybos [aplinkose](e-invoicing-service-environments.md).

Nustatę viską, galite sukurti savo globalizavimo priemones, kurios apibrėžia skirtingus elektroninių dokumentų apdorojimo ir duomenų transformavimo arba dokumentų importavimo iš visuotinės saugyklos scenarijus. Daugiau informacijos apie tai, kaip dirbti su globalizavimo funkcijomis, ieškokite Darbas [su globalizavimo funkcijomis](e-invoicing-working-globalization-features.md).

Jeigu jūsų scenarijams reikalingas integravimas su el. paštu arba gaunamų elektroninių dokumentų apdorojimui, informacijos apie tai, SharePoint [kaip nustatyti ir naudoti šiuos kanalus](e-invoicing-process-incoming-electronic-documents.md), žr. gaunamų elektroninių dokumentų apdorojimą.
