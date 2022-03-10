---
title: Išbandykite skalės vienetus paskirstytoje topologijoje
description: Šioje temoje pateikiama informacija apie tai, kaip išbandyti debesies ir krašto skalės vienetus gamybos ir sandėlio valdymo darbo krūviui.
author: perlynne
ms.date: 03/03/2022
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-03-03
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 04fd79f3c582ae9ac51882f73410477efaa35496
ms.sourcegitcommit: b52ff5dfd32580121f74a5f262e5c2495e39d578
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/03/2022
ms.locfileid: "8376259"
---
# <a name="try-out-scale-units-in-a-distributed-hybrid-topology"></a>Išbandykite skalės vienetus paskirstytoje topologijoje

[!include [banner](../includes/banner.md)]

Procesas, išbandant paskirstytą topologiją, yra paprastas. Pirmojo etapo metu turite tikrinti pritaikymus, kad jie veiktų paskirstytoje topologijoje. Galite pasirinkti dvi pasirinktis.

## <a name="option-1-evaluate-customizations-in-development-environments"></a>1 parinktis: programavimo aplinkose įvertinami tinkinimai

Prieš pradedant dirbti su sandbox aplinka, rekomenduojame naršyti skalės vienetus programavimo nustatyme, pvz., vieno langelio aplinkoje (taip pat vadinamoje pakopa 1 aplinka), kad būtų galima patvirtinti procesus, tinkinimus ir sprendimus. Šio etapo metu duomenys ir tinkinimai bus taikomi vieno bloko aplinkoms. Galite naudoti vieną aplinką, kuri gali atlikti ir įmonės centro, ir svarstyklių vieneto vaidmenį. Arba galite turėti dvi programavimo aplinkas, iš kurių viena atlieka centro vaidmenį, o kita – svarstyklių vieneto vaidmenį. Šis nustatymas suteikia geriausią būdą identifikuoti ir išspręsti problemas. Naujausia ankstyvos [prieigos (PEAP) versija](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxURUFWTjQzTzg0UUk5RkJHMDFEMVlSSDFEQy4u) taip pat gali būti naudojama užbaigti šį etapą.

Norėdami diegti ir tvarkyti [aplinkas, turite naudoti vieno langelio programavimo aplinkos skalės](https://github.com/microsoft/SCMScaleUnitDevTools) vieneto diegimo įrankius. Šie įrankiai leidžia konfigūruoti vienetus vienoje arba dviejose vienos dėžės aplinkose. Įrankiai pateikiami kaip dvejetainis paleidimas ir kaip šaltinio kodas GitHub. Studijauooo projektą, kuris apima [etapo naudojimo vadovą](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide), aprašantį, kaip naudoti įrankius. Jei diegiate "Edge [Scale" vienetus pasirinktinę aparatūrą naudodami vietinius verslo duomenis (LBD),](cloud-edge-edge-scale-units-lbd.md) turite vadovautis skirtingu procesu.

## <a name="option-2-acquire-add-ins-and-deploy-in-your-sandbox-environments"></a>2 parinktis: gauti papildinių ir diegti sandų dėžės aplinkose

Norėdami išbandyti paskirstytą topologiją, privalote turėti dvi sandų dėžės aplinkas (2 pakopa), iš kurių vienas turi savo duomenis (įmonės hub), o kitas – svarstyklių vienetui ir turi "tuščius duomenis".

Turite įsigyti bent vieno debesies arba briaunos skalės vieneto papildinių. Tada atitinkami projekto ir aplinkos atžymos bus suteikti ciklo tarnybose (LCS), kad būtų galima įdiegti skalės vieneto aplinkas naudojant svarstyklių [Microsoft Dynamics](https://lcs.dynamics.com/) vienetų tvarkytuvo portalą [.](https://aka.ms/SCMSUM)

Kreipkitės į "Microsoft" palaikymo tarnybą ir kreipkitės į užklausą, kad būtų įgalintos sand. aplinkos.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
