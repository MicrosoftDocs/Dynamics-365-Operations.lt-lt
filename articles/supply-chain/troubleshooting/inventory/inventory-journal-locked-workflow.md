---
title: Jūsų atsargų žurnalas užrakintas ir darbo eigos paketinė užduotis neveikia
description: Vienas iš jūsų atsargų žurnalų užrakintas dėl tam tikros operacijos ir jis nėra atrakintas
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
ms.openlocfilehash: 8b21ec2e2b3b8546dcb138422c5540053392c179
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477065"
---
# <a name="your-inventory-journal-is-locked-and-the-workflow-batch-job-doesnt-work"></a>Jūsų atsargų žurnalas užrakintas ir darbo eigos paketinė užduotis neveikia

## <a name="symptoms"></a>Požymiai

Vienas iš jūsų atsargų žurnalų užrakintas dėl tam tikros operacijos ir jis nėra atrakintas. Pavyzdžiui, jei registruojant įvyksta nežinoma klaida (tai yra sistemos užrakto operacija), žurnalo būsena gali išlikti sistemos užrakinta. Šiuo atveju darbo eigos darbo elementų apdorojimo programa parodys klaidą, kol tikrins užraktą.

## <a name="resolution"></a>Sprendimas

Prisijunkite prie „Supply Chain Management” „SQL Server” programos ir patikrinkite, ar **InventJournalTable.SystemBlocked** yra nustatyta *1*. Jei taip, įsitikinkite, kad žurnalo būsena nebūtų užrakinta, tada iš naujo nustatykite **InventJournalTable.SystemBlocked** *0*.
