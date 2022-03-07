---
title: Atsargų žurnalo darbo eigos sąlygos taikomos tik žurnalo, o ne eilutės lygmeniu
description: Atsargų žurnalo darbo eigos sąlygos taikomos tik žurnalo, o ne eilutės lygmeniu.
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
ms.openlocfilehash: 46bdde7f09c639fbefd46162431762b056d521ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477091"
---
# <a name="inventory-journal-workflow-conditions-apply-at-the-journal-level-not-line-level"></a>Atsargų žurnalo darbo eigos sąlygos taikomos tik žurnalo, o ne eilutės lygmeniu

## <a name="symptoms"></a>Požymiai

Ši problema gali kilti jei, pvz., bandysite išlaidų sumai nustatyti atsargų žurnalo darbo eigos sąlygą. Nustatykite sąlygą, kad 1-as veiksmas būtų vykdomas tik tada, kai išlaidų suma yra mažesnė nei 100. Tada nustatykite kitą sąlygą, kad 2-as veiksmas būtų vykdomas tik tada, kai išlaidų suma yra didesnė arba lygi 100. Tada, kai darbo eiga vykdoma, darbo eigos retrospektyvoje rodoma tik viena eilutė, o pirmoji sąlyga visuomet vertinama kaip *true* nepaisant pateiktosios vertės.

## <a name="workaround"></a>Apėjimo būdas

Dabartiniame leidime atsargų žurnalo darbo eigos sąlygos taikomos tik žurnalo, o ne eilutės lygmeniu. Toks veikimo būdas yra numatytas. Rekomenduojame nustatyti sąlygos kriterijus tik žurnalo lygio atributams.
