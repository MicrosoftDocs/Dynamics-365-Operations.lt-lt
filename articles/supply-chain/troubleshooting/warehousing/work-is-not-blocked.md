---
title: Darbas neužblokuotas
description: Darbas neužblokuotas
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924209"
---
# <a name="work-isnt-blocked"></a>Darbas neužblokuotas

Klaidos kodas: WHSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>Požymiai

Sistema rodo tokį klaidos pranešimą:

> Dirbas su ID %1 nėra užblokuotas.

## <a name="cause"></a>Priežastis

Bangos **parinktis** Užblokuota banga nustatyta kaip *Ne*. Darbo atblokuoti negalima, nes jis šiuo metu nėra užblokuotas.

## <a name="resolution"></a>Skiriamoji geba

 Galima **atblokuoti tik** darbą, kai nustatyta *parinktis* Užblokuota banga kaip Taip.
