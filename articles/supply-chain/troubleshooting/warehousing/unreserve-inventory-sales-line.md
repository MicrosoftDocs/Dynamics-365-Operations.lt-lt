---
title: Negalima rezervuoti atsargų pardavimo užsakymo eilutėje
description: Jei atidarytas darbas su pardavimo eilute ir bandote nereservuoti atsargų eilutėje, gausite klaidą. Užpildykite arba panaikinkite darbą, kad atlaisvintų rezervavimą.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1a042065dc4cd637aff58e55cf16179b7022f6ca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477101"
---
# <a name="cant-unreserve-inventory-on-a-sales-order-line"></a>Negalima rezervuoti atsargų pardavimo užsakymo eilutėje

## <a name="symptoms"></a>Požymiai

Jei atidarytas darbas su pardavimo užsakymo eilute ir bandote nereservuoti atsargų eilutėje, gausite klaidą su tokiu pranešimu:

> Rezervacijų šalinti negalima, nes sukurtas šiomis rezervacijomis grindžiamas darbas.

## <a name="resolution"></a>Sprendimas

Nustatykite, ar atviro pakavimo grupės darbas yra skirtas siekiant perkelti prekę iš pakavimo stoties į kitą stotį (tokią kaip *Baydoor*). Peržiūrėkite įrašus **Darbo sukūrimo istorijos žurnale** ir **Išsamios darbo informacijos** puslapiuose siekiant nustatyti, kas fiziškai rezervuoja inventorių ir tada užbaikite bei panaikinkite darbą siekiant atlaisvinti rezervaciją.
