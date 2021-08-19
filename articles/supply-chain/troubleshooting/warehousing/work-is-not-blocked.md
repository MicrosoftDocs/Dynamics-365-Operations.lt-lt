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
ms.openlocfilehash: 6b4361682246397732e8326b98b1b86ff878664e54c8c352296b0d7eaff6bbbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719556"
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
