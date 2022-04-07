---
title: Atsargų žurnalo darbo eiga niekada neužbaigiama ir žurnalo negalima sutvarkyti
description: Kai pateikiate žurnalo patvirtinimo darbo eigą, darbo eigos apdorojimas nustoja reaguoti ir jūs negalite redaguoti ar apdoroti savo žurnalų.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 5e8168a20a1fa4f52d28129eebb9931b31157ced
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/26/2022
ms.locfileid: "8488973"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>Atsargų žurnalo darbo eiga niekada neužbaigiama ir žurnalo negalima sutvarkyti

## <a name="symptoms"></a>Požymiai

Kai pateikiate žurnalo patvirtinimo darbo eigą, darbo eigos apdorojimas nustoja reaguoti ir jūs negalite redaguoti ar apdoroti savo žurnalų.

## <a name="resolution"></a>Sprendimas

Yra kelios priežastys, kodėl gali būti nebaigimas darbo eigos apdorojimas. Patikrinkite, ar yra šios problemos:

- Eikite į **Atsargų valdymas &gt; Sąranka&gt;Atsargų valdymo darbo eigos** ir peržiūrėkite paveiktos darbo eigos konfigūraciją. Daugiau informacijos žr. [Atsargų žurnalo patvirtinimo darbo eigos](../../inventory/inventory-journal-workflow.md).
- Gali įvykti darbo eigos išimtis arba klaida. Peržiūrėkite paveiktos darbo eigos darbo elementų retrospektyvą ir sužinokite, ar joje yra programos klaida, nutraukusi darbo eigą.
- Atsargų žurnalą galima atnaujinti arba redaguoti, tik jei jis patvirtintas. Jei atšaukimas aktyvus, galite bandyti atšaukti žurnalą. Darbo eigos paketinės užduoties vykdymas gali būti sustabdytas dėl kelių priežasčių. Kai kurios iš šių priežasčių galėjo kilti dėl darbo eigos sistemos problemos.
