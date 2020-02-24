---
title: Perkelkite užsakymus iš kitos parduotuvės naudodami mokesčių siuntimo funkciją.
description: Šioje temoje aprašoma mokesčių siuntimo funkcija.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 0bbebcc7b2ab89bf2f5db7294acfca1d8a5ad96e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023380"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>Perkelkite užsakymus iš kitos parduotuvės naudodami mokesčių siuntimo funkciją.

[!include [banner](includes/banner.md)]

Naudojant mokesčių siuntimo funkciją programoje „Commerce“ kliento užsakymus galima pateikti vienoje parduotuvėje, o išsiųsti iš kitos.

Elektroninio kasos aparato (EKA) kliente esantys kliento užsakymai palaiko keletą įvykdymo parinkčių. Toliau nurodyta keletas įvykdymo parinkčių pavyzdžių.

- Paėmimas iš tos pačios parduotuvės kitą dieną.
- Paėmimas iš kitos parduotuvės tą pačią dieną.
- Siuntimas iš numatytojo siuntimo sandėlio, priskirto parduotuvei, ir pristatymas nurodžius konkrečią datą.

Taikant mokesčio siuntimo funkciją naudojamos toliau nurodytos EKA operacijos: Siųsti visus produktus ir Siųsti pasirinktus produktus. Tai parduotuvės klerkui leidžia pasirinkti vietą iš kurios siųsti ir kurioje užsakymas arba užsakymo eilutė gali būti įvykdyta. Pagal numatytuosius nustatymus vieta iš kurios siunčiama yra su parduotuve susietas siuntimo sandėlis. Tačiau parduotuvės klerkas gali pakeisti šią vietą ir pasirinkti bet kurią parduotuvei priskirtoje lokatorių grupėje apibrėžtą parduotuvę.

Tokia pati galimybė suteikiama pasirenkant ir gavėjo adresus.

Siuntimo metodai, kurios galima naudoti norint įvykdyti užsakymo eilutę, yra pagrįsti produktų pristatymo ir adresų leistinų režimų konfigūracija. Kadangi tinkamų pristatymo režimų taisyklės tvarkomos tik „Headquarters“ (HQ), EKA klientas kreipiasi realiuoju laiku ir randa tinkamus siuntimo eilutės pristatymo režimus.
