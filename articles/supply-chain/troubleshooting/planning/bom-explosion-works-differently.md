---
title: KS išskleidimas pagal skirtingus galutinai ir įvertintos gamybos užsakymų atvejus
description: Medžiagų važtaraščio sprogimas elgiasi kitaip patvirtintiems gamybos užsakymams ir apskaičiuotiems gamybos užsakymams, kai darbai sukuriami rankiniu būdu
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 94d4b00ea30396923a61b2748cf1aaeedc0af8af
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477089"
---
# <a name="bom-explosion-behaves-differently-for-firmed-and-estimated-production-orders"></a>KS išskleidimas pagal skirtingus galutinai ir įvertintos gamybos užsakymų atvejus

## <a name="symptoms"></a>Požymiai

Patvirtinus gamybos užsakymą, prekės nėra sprogdinamos, kai sprogdinate medžiagų aprašą (BOM). Nepaisant to, jums rankiniu būdu sukuriant darbo užsakymą ir tada apskaičiuojant gamybos užsakymą, prekės yra sprogdinamos.

### <a name="resolution"></a>Sprendimas

Sprogimas, įvykstantis kai gamybos užsakymas yra patvirtinamas, rodys į suplanuotą užsakymą, bet bus nerodoma, jog suplanuotas užsakymas šiuo metu ir šiuo atveju yra patvirtintas. Nepaisant to, ar gamybos užsakymas buvo apskaičiuotas, sprogimas yra paskatinamas iš išleisto gamybos užsakymo, kai nėra jokio suplanuoto užsakymo.
