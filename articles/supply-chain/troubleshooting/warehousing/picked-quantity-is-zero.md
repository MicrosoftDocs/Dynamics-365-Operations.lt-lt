---
title: Negalite patvirtinti siuntos, nes yra nulinis kiekis
description: Negalite patvirtinti siuntos, nes yra nulinis kiekis
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b2f9f8deaca30e318d0393fb1d7911eebf63060ccca83dc6f1de9b04b9e30e11
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712891"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a>Negalite patvirtinti siuntos, nes yra nulinis kiekis

Klaidos kodas: LoadLineWarningUpdatedToZero

## <a name="symptoms"></a>Požymiai

Kai bandote patvirtinti siuntą, sistema rodo šį klaidos pranešimą:

> Prekės %1 ir siuntos %2 krovinio eilutė atnaujinta į nulinį kiekį dėl pristatymo trūkumo sąrankos, leidžiančios nesiųsti jokio šios prekės kiekio.

Todėl negalite patvirtinti krovinio siuntimo.

## <a name="cause"></a>Priežastis

Sistema įvertina, ar paimtas kiekis patenka į numatomus limitus, remdamasi paimtu kiekiu, krovinio eilutės kiekiu ir pristatymo pristatymo procentu. Jei sistema nustato, kad krovinio eilutėje paimtas kiekis yra 0 (nulis), siuntos patvirtinti negalite. Pavyzdžiui, šis išdavimas gali atsirasti, jei darbas buvo atšauktas, o pristatymo eilutėje pristatymo procentinė dalis yra 100 procentų.

## <a name="resolution"></a>Skiriamoji geba

Patikrinkite krovinio eilutes, kad įsitikintumėte, jog pristatymo underdelive procentai ir kiekiai yra sulygiuoti su paimtu darbu.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite pakrovimą, kuriam siuntimo patvirtinti nepavyksta.
1. Krovinio **eilučių** „FastTab" pasirinkite prekės, viršijančios pristatymo pateisavimo procentinę dalį, krovinio eilutę.
1. Koreguokite lauko Pristatymo **Pristatymas ne iki galo** vertę arba **lauką** Kiekis.

> [!TIP]
> Jei išdavimas vis tiek nėra fiksuotas, gali tekti atlikti daugiau susijusių pardavimo užsakymų arba perkėlimo užsakymų paėmimo darbų, kol turimas kiekis nesulygiuotas su kroviniu arba siunta.
