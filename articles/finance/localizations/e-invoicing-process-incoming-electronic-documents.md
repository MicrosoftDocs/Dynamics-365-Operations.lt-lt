---
title: Gaunamų elektroninių dokumentų apdorojimas
description: Šioje temoje pateikta gaunamų elektroninių dokumentų apdorojimo apžvalga.
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
ms.openlocfilehash: 9701367e1ba1f9dbd1e53deb863c10af4213a359
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371913"
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
