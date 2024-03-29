---
title: Aptarnavimo užsakymo etapai
description: Apibrėždami aptarnavimo užsakymo etapus ir juos priskirdami darbuotojams kontroliuojate aptarnavimo užsakymo eigą, sekdami užduotis, kurias aptarnavimo organizacijoje atlieka įvairūs žmonės.
author: sorenva
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e748afbd159d7a8fca1372676872cc02dd7ea57
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671736"
---
# <a name="service-order-stages"></a>Aptarnavimo užsakymo etapai   

[!include [banner](../includes/banner.md)]


Galite nustatyti aptarnavimo užsakymo etapus, kad nustatytumėte užduotis, kurias būtina atlikti, jų atlikimo tvarką ir už jų atlikimą atsakingus darbuotojus. Apibrėždami aptarnavimo užsakymo etapus ir juos priskirdami darbuotojams, galite kontroliuoti aptarnavimo užsakymo eigą sekdami užduotis, kurias aptarnavimo organizacijoje atlieka įvairūs žmonės. Etapų sekoje turi būti pradinis etapas.

Taip pat galite nurodyti veiksmus, kurie leidžiami kiekviename etape. Pvz., panaikinus visų etapų, išskyrus galutinio etapo, žymės langelio **Registravimas** žymėjimą, nebus registruojami jokie aptarnavimo užsakymai, kol aptarnavimo užsakymai nepereis visų etapų.

## <a name="branching-in-service-order-stages"></a>Skirstymas į aptarnavimo užsakymo etapus

Kai nustatote aptarnavimo etapą, galite sukurti kelis variantus arba šakas, iš kurių galima pasirinkti kitą aptarnavimo etapą. Sukurtas šakas galima pasirinkti baigus pradinį etapą. Pavyzdžiui, nustatėte etapą **Planavimas** kaip pradinį etapą. Sukūrėte du etapus **Vykdoma** ir **Atšaukti**, tada pasirinkote etapą **Planavimas** kaip pirminį šių etapų etapą. Priskyrėte etapą **Planavimas** pardavimo užsakymui. Baigę pardavimo užsakymo planavimo etapą galite pasirinkti etapą **Vykdoma**, jei pardavimo užsakymo galima imtis, arba galite pasirinkti etapą **Atšaukti** etapas, jei pardavimo užsakymas atšauktas.

## <a name="see-also"></a>Taip pat žiūrėkite

[Nustatyti aptarnavimo užsakymų etapus](set-up-service-order-stages.md)

[Aptarnavimo užsakymo etapo keitimas](change-service-order-stage.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]