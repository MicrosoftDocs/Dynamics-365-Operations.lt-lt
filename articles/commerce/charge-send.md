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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: d8c2288a18398f71a75dad6e51d51ba4b09561e6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997680"
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
