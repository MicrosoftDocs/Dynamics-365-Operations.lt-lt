---
title: Elektroninių SF išrašymo nustatymas
description: Šioje temoje pateikta apžvalga apie elektroninių SF išrašymo nustatymo ir konfigūravimo procesą.
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
ms.openlocfilehash: 8138c63e9eff1d2ca934f9d4467e4e3b73dae941
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371936"
---
# <a name="electronic-invoicing-setup"></a>Elektroninių SF išrašymo nustatymas

[!include [banner](../includes/banner.md)]

Šioje temoje apžvelgiamas elektroninių SF išrašymo nustatymo ir konfigūravimo procesas. Nustatymo veiksmus turite atlikti nurodyta tvarka. Jei veiksmas privalomas, bet jį praleisite, funkcija veikia netinkamai, o atliekant vėlesnius veiksmus arba naudojant funkciją įvyks keletas trikčių. 

Prieš pradėdami įsitikinkite, kad visi pagrindiniai komponentai nustatyti teisingai, ar esate prisiregistravę prie reguliavimo konfigūracijos tarnybos (RCS) ir turite RCS egzempliorių bei ar įdiegtas jūsų "Microsoft Dynamics 365 Finance " arba aplinkos elektroninių SF išrašymo Dynamics 365 Supply Chain Management priedas. Norėdami gauti daugiau informacijos, žr. Elektroninių [SF išrašymo prisiregistravimo ir diegimo metu](e-invoicing-install-add-in-microservices-lcs.md).

Tada nustatykite "Azure" išteklius, kurių elektroninio SF išrašymo atveju reikia atlikti darbą. Norėdami gauti daugiau informacijos, žr. ["Azure" išteklių nustatymas elektroninių SF išrašymo metu](e-invoicing-set-up-azure-resources.md).

Sukonfigūrę pagrindinius komponentus, kartu su RCS nustatykite pagrindinius loginius elektroninių SF išrašymo komponentus. Pirmiausia nurodykite aptarnavimo aplinkos, kurias išlaikysite, skaičių. Tokiu būdu apibrėžiate loginius duomenis ir konfigūracijos skaidymo duomenis, norėdami užtikrinti, kad turite ribą tarp programavimo arba tikrinimo aplinkos ir gamybos aplinkos. Norint jūsų programavimo procesą nustatyti lanksčiu būdu, gali reikėti kelių atskirų programavimo ir tikrinimo aplinkos. Be paslaugų aplinkos nustatymo, nustatykite saitą į savo verslo programas, pvz., finansų arba tiekimo grandinės valdymą, tiesiogiai iš RCS, norėdami nustatyti parametrus, kurie reikalingi tinkamai operacijai naudojant elektroninį SF išrašymą. Daugiau informacijos apie aplinkas žr. tarnybos [aplinkose](e-invoicing-service-environments.md).

Nustatę viską, galite sukurti savo globalizavimo priemones, kurios apibrėžia skirtingus elektroninių dokumentų apdorojimo ir duomenų transformavimo arba dokumentų importavimo iš visuotinės saugyklos scenarijus. Daugiau informacijos apie tai, kaip dirbti su globalizavimo funkcijomis, ieškokite Darbas [su globalizavimo funkcijomis](e-invoicing-working-globalization-features.md).

Informacijos apie apdorojimo pardavimo galimybių veiksmus, kurie sudaro procesą, kurį kursite globalizavimo funkcijose, **ieškokite [COMPLETE!: Document processing actions]**.

Jeigu jūsų scenarijams reikalingas integravimas su el. paštu arba gaunamų elektroninių dokumentų apdorojimui, informacijos apie tai, SharePoint [kaip nustatyti ir naudoti šiuos kanalus](e-invoicing-process-incoming-electronic-documents.md), žr. gaunamų elektroninių dokumentų apdorojimą.
