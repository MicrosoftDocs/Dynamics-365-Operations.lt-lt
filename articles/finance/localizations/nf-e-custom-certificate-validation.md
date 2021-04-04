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
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3efa05f49748f6bbff680f322a77cec24da46c0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240584"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e pasirinktinio sertifikato patvirtinimas

[!include [banner](../includes/banner.md)]

Įjungus NF-e pasirinktinio sertifikato tikrinimo funkciją, pasirinktinis patvirtinimas leidžia palaikyti ryšį su žiniatinklio tarnybomis. Šis ryšys reikalingas norint perduoti NF-e ir vykdyti SEFAZ autorizavimą.

Sertifikato V5 ypatybę **Serverio autentifikavimo paskirtis** suteikia Brazilijos šakninio sertifikato institucija. Esant numatytiesiems parametrams, ši ypatybė yra išjungta ir turi būti įjungta rankiniu būdu. Kai kuriais atvejais automatinio sertifikato atnaujinimo funkcija gali išjungti šią ypatybę, kad ji nebūtų suaktyvinta. Jei taip nutinka, tai turi įtakos TLS ryšiui, kuris tampa nebepatikimas. Tai taip pat turi įtakos galimybei išduoti NF-e gamybos aplinkoms Minas Žeraiso (MG) ir Paranos (PR) valstijose.

Šis naujinimas leidžia naudoti alternatyvų sprendimą sertifikato patvirtinimui, o tai reiškia galimybę užmegzti saugų ryšį.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]