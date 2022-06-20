---
title: Gaunamų elektroninių dokumentų apdorojimas
description: Šiame straipsnyje pateikta gaunamų elektroninių dokumentų apdorojimo apžvalga.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dec4c16c8ba9f0ba55f30f3944eff172cf9db724
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910014"
---
# <a name="processing-of-incoming-electronic-documents"></a>Gaunamų elektroninių dokumentų apdorojimas

[!include [banner](../includes/banner.md)]

Gaunamus elektroninius dokumentus, pavyzdžiui, tiekėjo elektronines SF, galima importuoti ir apdoroti dviem būdais:

- Failai nuskaitomi iš išorinių kanalų ir perduodami tiesiogiai prie prisijungusių programų. Ten jie papildomai transformuoja ir importuojami į duomenų bazę.
- Failai iš anksto apdoroti elektroninių SF išrašymo paslaugoje ir yra perduoti į jūsų prijungtą programą.

Elektroninių SF išrašymas palaiko du gaunamų dokumentų kanalus: el. paštą ir Microsoft aplankus SharePoint.

Yra Twp nustatymo tipų, kurie nurodo, ar dokumentai iš anksto apdoroti, ar yra tiesiogiai perduoti jūsų susijusiai programai:

- **Duomenų kanalas** – sistema tiesiogiai perduos dokumentą prie prijungtos programos.
- **Duomenų kanalas su apdorojimo** pardavimo galimybes – galite nustatyti papildomus veiksmus, kurie bus paleisti prieš perdant dokumentą prijungtai programai.

Informacijos apie tai, kaip nustatyti scenarijų skirtingiems kanalams gaunamiems elektroniniams dokumentams apdoroti, [ieškokite Konfigūruokite el. pašto kanalą ir konfigūruokite](e-invoicing-configure-email.md) kanalą [SharePoint.](e-invoicing-configure-sharepoint-channel.md)
