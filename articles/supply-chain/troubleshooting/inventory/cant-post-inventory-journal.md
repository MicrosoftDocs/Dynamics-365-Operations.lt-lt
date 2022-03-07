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
ms.openlocfilehash: 9430068f9c2d92c894817db04143297de6c6aa6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477054"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>Atsargų žurnalo darbo eiga niekada neužbaigiama ir žurnalo negalima sutvarkyti

## <a name="symptoms"></a>Požymiai

Kai pateikiate žurnalo patvirtinimo darbo eigą, darbo eigos apdorojimas nustoja reaguoti ir jūs negalite redaguoti ar apdoroti savo žurnalų.

## <a name="resolution"></a>Sprendimas

Yra kelios priežastys, kodėl gali būti nebaigimas darbo eigos apdorojimas. Patikrinkite, ar yra šios problemos:

- Eikite į **Atsargų valdymas &gt; Sąranka&gt;Atsargų valdymo darbo eigos** ir peržiūrėkite paveiktos darbo eigos konfigūraciją. Daugiau informacijos žr. [Atsargų žurnalo patvirtinimo darbo eigos](/dynamics365/supply-chain/inventory/inventory-journal-workflow.md).
- Gali įvykti darbo eigos išimtis arba klaida. Peržiūrėkite paveiktos darbo eigos darbo elementų retrospektyvą ir sužinokite, ar joje yra programos klaida, nutraukusi darbo eigą.
- Atsargų žurnalą galima atnaujinti arba redaguoti, tik jei jis patvirtintas. Jei atšaukimas aktyvus, galite bandyti atšaukti žurnalą. Darbo eigos paketinės užduoties vykdymas gali būti sustabdytas dėl kelių priežasčių. Kai kurios iš šių priežasčių galėjo kilti dėl darbo eigos sistemos problemos.
