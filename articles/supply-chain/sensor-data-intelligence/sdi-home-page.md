---
title: Jutiklio duomenų tyrimų pagrindinis puslapis
description: Šiame straipsnyje pateikta Jutiklio duomenų tyrimų apžvalga. Organizacijos gali naudoti šią funkciją, norėdami valdyti verslo procesus "Microsoft Dynamics 365 Supply Chain Management", paremtus objektų interneto ("IT") signalais iš įrenginių ir įrangos gamybos aukšte.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2e4cd8d4d4ffcd10d02fbf26615f12cdd6ccca9e
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/08/2022
ms.locfileid: "9429009"
---
# <a name="sensor-data-intelligence-home-page"></a>Jutiklio duomenų tyrimų pagrindinis puslapis

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

"Jutiklio duomenų įžvalgos", skirtas "Microsoft Dynamics 365 Supply Chain Management ", leidžia organizacijoms valdyti verslo procesus tiekimo grandinės valdymo procesuose, remiantis objektų interneto ("IT") signalais iš įrenginių ir įrangos gamybos aukšte. Tai atnaujinta, pervardyta ĮT tyrimų *funkcijos*, kuri anksčiau buvo galima tiekimo grandinės valdymui, versija.

Jutiklio duomenų įžvalgos leidžia atlikti šias užduotis:

- Surinkti informaciją iš įrenginių ir įrangos, norint atnaujinti priežiūros turto skaitiklio vertes tiekimo grandinės valdymo ir numatymo priežiūros aštrumą.
- Nustatykite sprendimą naudodami paprastą įsk. Microsoft Dynamics vedlį, o ne rankiniu būdu diegiate ir konfigūruojate ciklo tarnybų (LCS) komponentus.
- Įdiekite komponentus savo abonemente, kad būtų galima lanksčiau valdyti "Azure" komponentus.
- Konfigūruokite, svarstykite ir pratęskite sprendimą, kaip verslo logiką, kurią vykdo "Azure" komponentai. Dabar komponentai valdomi jūsų abonemente. Todėl galite pritaikyti juos pagal savo unikalius verslo poreikius.

## <a name="business-scenarios"></a>Verslo scenarijai

"Jutiklio duomenų įžvalgos" leidžia atlikti kelių tipų funkcijas, kurių kiekviena iš jų vaizduojama specialiu *sistemos* scenarijumi. Kiekvienas scenarijus sistemoje teikia specializuotas konfigūravimo pasirinkčių rinkinį, kaip išsamiai pateikiama šioje lentelėje.

| Scenarijus | Aprašymas |
|---|---|
| [Turto prastova](sdi-scenario-asset-downtime.md) | Tiksliai sekite įrenginių turto efektyvumą naudodami jutiklio duomenis įrenginių prastovams sekti. |
| [Turto priežiūra](sdi-scenario-asset-maintenance.md) | Sumažinti priežiūros išlaidas ir pratęsti turto trukmę, pagerinti priežiūros planus, pagrįstus jutiklių rodmenų kritinių įrenginių turto taškų rodmenimis. |
| [Mašinos būsena](sdi-scenario-equipment-downtime.md) | Užtikrinti operacijos efektyvumą naudojant jutiklio rodmenis, siekiant informuoti planuotojas apie įrenginių pašalinę operaciją, ir pateikti parinktis, kurios sumažins galimą uždelsimą. |
| [Produkto kokybė](sdi-scenario-product-quality.md) | Užtikrinkite produktų paketų kokybę, lygindami jutiklio rodmenis faktinėms kiekvieno produkto paketo ypatybei, pvz., konfigūracijai, temperatūrai arba pasirinktinai nustatytai kokybės metrikai. Sistema praneš vartotojams, kai atsiranda nuokrypių. |
| [Gamybos atidėjimai](sdi-scenario-production-delays.md) | Naudokite jutiklio rodmenis, norėdami palyginti faktinį ciklo laiką su suplanuotu ciklo laiku ir įspėti vadovus, kai gamyba nėra suplanuota. Prižiūrėtojai gali būti prižiūrėtojai, jei reikia, norėdami užtikrinti maksimalų operacijų efektyvumą. |

## <a name="architecture"></a>Architektūra

Šioje architektūros diagramoje pateikiama sprendimo ir jo komponentų apžvalga.

![Jutiklio duomenų įžvalgų diagrama.](media/sdi-architecture.png "Jutiklio duomenų įžvalgų diagrama")
