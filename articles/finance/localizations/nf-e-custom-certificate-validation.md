---
title: NF-e pasirinktinio sertifikato patvirtinimas
description: Šioje temoje pateikiama informacija apie NF-e pasirinktinio sertifikato suaktyvinimą ir naudojimą.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 26ffed1f49d9087ca767aab1b8cac41b099f73cb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445927"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e pasirinktinio sertifikato patvirtinimas

[!include [banner](../includes/banner.md)]

Įjungus NF-e pasirinktinio sertifikato tikrinimo funkciją, pasirinktinis patvirtinimas leidžia palaikyti ryšį su žiniatinklio tarnybomis. Šis ryšys reikalingas norint perduoti NF-e ir vykdyti SEFAZ autorizavimą.

Sertifikato V5 ypatybę **Serverio autentifikavimo paskirtis** suteikia Brazilijos šakninio sertifikato institucija. Esant numatytiesiems parametrams, ši ypatybė yra išjungta ir turi būti įjungta rankiniu būdu. Kai kuriais atvejais automatinio sertifikato atnaujinimo funkcija gali išjungti šią ypatybę, kad ji nebūtų suaktyvinta. Jei taip nutinka, tai turi įtakos TLS ryšiui, kuris tampa nebepatikimas. Tai taip pat turi įtakos galimybei išduoti NF-e gamybos aplinkoms Minas Žeraiso (MG) ir Paranos (PR) valstijose.

Šis naujinimas leidžia naudoti alternatyvų sprendimą sertifikato patvirtinimui, o tai reiškia galimybę užmegzti saugų ryšį.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]