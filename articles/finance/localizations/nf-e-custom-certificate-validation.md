---
title: NF-e pasirinktinio sertifikato patvirtinimas
description: Šioje temoje pateikiama informacija apie NF-e pasirinktinio sertifikato suaktyvinimą ir naudojimą.
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8144e16b127bdbe954ef44f52c5ac71689a2036e6085e9a4ccc8bb17f91ae9b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755596"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e pasirinktinio sertifikato patvirtinimas

[!include [banner](../includes/banner.md)]

Pagal **numatytuosius nustatymus serverio** autentifikavimo paskirties ypatybė iš sertifikatų, kuriuos išdavė brazilijos šakninio sertifikato institucija, turi būti įjungta rankiniu būdu. Kai kuriais atvejais automatinio sertifikato atnaujinimo funkcija gali išjungti šią ypatybę, kad ji nebūtų suaktyvinta. Jei taip nutinka, tai turi įtakos TLS ryšiui, kuris tampa nebepatikimas. Tai taip pat turi įtakos galimybei išduoti Brazilijos elektroninį mokesčių dokumento modelį 55 (NF-e) gamybos aplinkoms Minas Žeraiso (MG) ir Paranos (PR) valstijose.

Norėdami įjungti **NF-e pasirinktinio sertifikato tikrinimo pataisą**, eikite į **Funkcijų valdymas**. Ši funkcija leidžia alternatyvų V5 ir V10 sertifikatų patikrinimo sprendimą ir leidžia patikimą ryšį su tinklo paslaugomis, o tai būtina norint užtikrinti saugų NF-e perdavimą ir autorizavimo gavimą iš SEFAZ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
