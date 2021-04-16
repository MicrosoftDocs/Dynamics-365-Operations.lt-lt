---
title: Mokesčių skaičiavimo paslauga (peržiūros versija)
description: Šioje temoje paaiškinama bendroji mokesčių skaičiavimo tarnybos apimtis ir funkcijos.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818229"
---
# <a name="tax-calculation-service-preview"></a>Mokesčių skaičiavimo paslauga (peržiūros versija)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Mokesčių skaičiavimo tarnyba yra hyper-scalable multitenant paslauga, kuri leidžia „Global Tax Engine“ automatizuoti ir supaprastinti mokesčių nustatymo ir skaičiavimo procesą. Visiškai konfigūruotinas mokesčių modulis. Elementai, kuriuos galima konfigūruoti, apima (bet tuo neapsiribojama) apmokestinamą duomenų modelį, mokesčio kodą, mokesčių taikomumo matricą ir mokesčių skaičiavimo formulę. Mokesčių sistema veikia pagrindinių paslaugų „Microsoft Azure“ platformoje ir siūlo modernias technologiją bei proporcingai keičiamumą.

Mokesčių skaičiavimo tarnyba integruojama su „Dynamics 365 Finance“ ir „Dynamics 365 Supply Chain Management“. Galiausiai ji taip pat bus „Dynamics 365 Project Operations“ integruota į, ir kitas pirmosios šalies ir trečiosios šalies „Dynamics 365 Commerce“ programas.

Mokesčių skaičiavimo tarnyba yra „Microsoft" mokesčių sistema, kuri siūlo proporcingai keičiamumą. Galite atlikti šias užduotis:

- Konfigūruokite mokesčių skaičiavimo tarnybą per „Regulatory Configuration Service“ (RCS). RCS yra patobulinta elektroninių ataskaitų (ER) dizaino įrankio versija, galima naudoti kaip atskirą paslaugą.
- Konfigūruoti mokesčių matricą, kad automatiškai būtų nustatyti mokesčių kodai ir tarifai.
- Konfigūruoti mokesčių matricą, kad automatiškai būtų nustatytas registracijos numeris.
- Konfigūruokite mokesčių skaičiavimo konstruktorių, kad būtų galima apibrėžti formules ir sąlygas.
- Juridiniuose subjektuose bendrai naudoti mokesčių nustatymo ir skaičiavimo sprendimą.

Norėdami naudoti mokesčių skaičiavimo tarnybą, įdiekite mokesčių skaičiavimo tarnybos priedą iš ciklo tarnybų „Microsoft Dynamics Lifecycle Services“ (LCS) projekto. Tada užbaikite RCS nustatymą ir įjunkite mokesčių skaičiavimo paslaugą „Finance and Supply Chain Management“. Daugiau informacijos žr. [Darbo su mokesčių paslaugų pradžia](https://go.microsoft.com/fwlink/?linkid=2138482).

## <a name="availability"></a>Prieinamumas

Mokesčių skaičiavimo paslauga galima tik sandų saugyklos aplinkose ir pasirinktiems klientams, naudojant viešąją peržiūros programą. Galiausiai ji bus bendrai pasiekiama visiems klientams ir gamybos aplinkoje.

Naujos priemonės ir toliau bus pristatytos mokesčių skaičiavimo paslaugoje. Todėl nepamirškite dažnai patikrinti naujausiais dokumentais, kad sužinotumėte apie palaikomų funkcijų padengimą ir aprėptį.

Mokesčių skaičiavimo paslauga įdiegiama toliau nurodytose „Azure" geografinėse diagramose. Ji taip pat bus įdiegta į daugiau „Azure" geografinių diagramų, atsižvelgiant į kliento poreikius:

- Jungtinės Valstijos
- Europa
- Prancūzija
- Jungtinė Karalystė

> [!NOTE]
> Mokesčių skaičiavimo tarnyba nepalaiko „Dynamics 365" vietinio diegimo. Tai nepalaiko ir ankstesnių versijų, pvz., „Dynamics AX 2012".

## <a name="feature-highlights"></a>Svarbiausi funkcijų aspektai

- Konfigūruoti mokesčių matricą, kad automatiškai būtų nustatyti mokesčių kodai ir tarifai.
- Kelių pridėtinės vertės mokesčio (PVM) registracijos numerių palaikymas
- Perkėlimo užsakymo palaikymas nustatant mokesčius ir skaičiuojant
- Perkėlimo užsakymo palaikymas nustatant keletą PVM registracijos numerių

## <a name="supported-transactions"></a>Palaikomos operacijos

Mokesčių skaičiavimo paslauga gali būti įgalinta juridinio subjekto ir operacijos. Palaikomos toliau nurodytos operacijos:

- Pardavimo procesas

    - Pardavimo pasiūlymas
    - Pardavimo užsakymas
    - Patvirtinimas
    - Išrinkimo dokumentas
    - Važtaraštis
    - Pardavimo sąskaita faktūra
    - Kredito sąskaita
    - Grąžinimo užsakymas
    - Antraštės įvairūs keitimai
    - Įvairių išlaidų eilutė

- Pirkimo procesas

    - Pirkimo užsakymas
    - Patvirtinimas
    - Gavimų sąrašas
    - Gavimo dokumentas
    - Pirkimo SF
    - Antraštės įvairūs keitimai
    - Įvairių išlaidų eilutė
    - Kredito sąskaita
    - Grąžinimo užsakymas
    - Pirkimo paraiška
    - Papildomos pirkimo paraiškos eilutės išlaidos
    - Pasiūlymo patvirtinimas
    - Pasiūlymo patvirtinimo antraštės papildomos išlaidos
    - Pasiūlymo patvirtinimo eilutės papildomos išlaidos

- Atsargų procesas

    - Perlaidos užsakymas - siuntimas
    - Perlaidos užsakymas - gavimas

## <a name="related-resources"></a>Susiję ištekliai

[Darbo su mokesčių paslaugomi pradžia](https://go.microsoft.com/fwlink/?linkid=2138482)

[Kelių PVM registracijų numeris](https://go.microsoft.com/fwlink/?linkid=2153387)

[Mokesčių priemonės perkėlimo užsakymo palaikymas](https://go.microsoft.com/fwlink/?linkid=2153388)

[Kaip sukurti plėtinį mokesčių tarnybose](https://go.microsoft.com/fwlink/?linkid=2138483)
