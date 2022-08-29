---
title: NF-e pasirinktinio sertifikato patvirtinimas
description: Šiame straipsnyje pateikiama informacija apie NF-e pasirinktinio sertifikato įgalinimas ir naudojimas.
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f78fdbd133aecaf9dbf8abe0006abd6deb1b1b15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288551"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e pasirinktinio sertifikato patvirtinimas

[!include [banner](../includes/banner.md)]

Pagal **numatytuosius nustatymus serverio** autentifikavimo paskirties ypatybė iš sertifikatų, kuriuos išdavė brazilijos šakninio sertifikato institucija, turi būti įjungta rankiniu būdu. Kai kuriais atvejais automatinio sertifikato atnaujinimo funkcija gali išjungti šią ypatybę, kad ji nebūtų suaktyvinta. Jei taip nutinka, tai turi įtakos TLS ryšiui, kuris tampa nebepatikimas. Tai taip pat turi įtakos galimybei išduoti Brazilijos elektroninį mokesčių dokumento modelį 55 (NF-e) gamybos aplinkoms Minas Žeraiso (MG) ir Paranos (PR) valstijose.

Norėdami įjungti **NF-e pasirinktinio sertifikato tikrinimo pataisą**, eikite į **Funkcijų valdymas**. Ši funkcija leidžia alternatyvų V5 ir V10 sertifikatų patikrinimo sprendimą ir leidžia patikimą ryšį su tinklo paslaugomis, o tai būtina norint užtikrinti saugų NF-e perdavimą ir autorizavimo gavimą iš SEFAZ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
