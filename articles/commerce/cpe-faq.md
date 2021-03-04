---
title: „Dynamics 365 Commerce“ vertinimo aplinkos DUK
description: Šioje temoje pateikiami atsakymai į dažniausiai užduodamus klausimus apie „Microsoft Dynamics 365 Commerce“ vertinimo aplinką.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 637714e28b9f8f4aa66e251e709d8f78bff2739d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414245"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>„Dynamics 365 Commerce“ vertinimo aplinkos DUK

[!include [banner](includes/banner.md)]

Šioje temoje pateikiami atsakymai į dažniausiai užduodamus klausimus apie „Microsoft Dynamics 365 Commerce“ vertinimo aplinką.

**Ar galime naudoti komercijos vertinimo aplinką kaip „e-Commerce“ parduotuvę savo klientams, kurie jau įgyvendino „Retail“?**

Nr. Komercijos vertinimo aplinka yra skirta tik vertinimui. Jei reikia aplinkos klientui, kuris yra įsidiegęs „Retail“, kreipkitės į „Microsoft“.

**Ar gali komercijos vertinimo aplinka būti naudojama „e-Commerce“ savybių parengimui esančioje aplinkoje ar programose, kurios įgyvendino „Retail“?**

Ne (dažniausiai). Komercijos vertinimo komponentai yra prieinami tik aplinkose, kurios atitinka konfigūravimus, nustatytus būtinosiose sąlygose ir parengimo gide. Taip pat, reikalaujama demo duomenų pagrindo versija nebus prieinama aplinkose, kurios turi pirmąją versiją, ankstesnę nei 10.0.8. 

**Kiek kainuoja patalpinti komercijos vertinimo aplinką „Microsoft Azure“ per „Microsoft Dynamics Lifecycle Services“ (LCS)?**

Įprasta „Dynamics 365 Finance“/„Dynamics 365 Supply Chain Management“/„Dynamics 365 Commerce“ būstinės demo aplinka (virtuali mašina \[VM\]) bus patalpinta jūsų „Azure“ prenumeratoje. Norėdami įvertinti šiuos kaštus, galite naudoti [„Azure“ kainų skaičiuotuvą](https://azure.microsoft.com/pricing/calculator/).

Kiti komponentai, tokie kaip „Commerce Scale Unit“, komercijos vietos kūrimo įrankis ir jūsų „e-Commerce“ vieta bus prieinama kaip programinės įrangos paslaugos (SaaS) ir patalpinti „Microsoft“.

**Kokios „Azure“ geografinės sritys šiuo metu palikomos komercijos vertinimo aplinkoje?**

Komercijos vertinimo aplinka gali būt patalpinta tik Šiaurės Amerikos regione.

**Ar galima atsisiųsti virtualųjį standųjį diską (VHD), kuriame yra visavertės „OneBox“ virtualiosios mašinos (VM) parinktis?**

„Dynamics 365 Commerce“ ir „Commerce Scale Unit“ yra visa programinė įranga, kaip paslaugų (Saas) ir turi būti patalpinta debesyje.

**Kiek laiko galima naudoti komercijos vertinimo aplinką?**

Komercijos vertinimo aplinka turi 30 dienų laiko limitą nuo dienos, kai SaaS komponentai, tokie kaip „Commerce Scale Unit“, komercijos vietos kūrimo įrankis ir jūsų „e-Commerce“ vieta yra suteikta.

**Ar galiu pratęsti komercijos vertinimo aplinkos laikotarpį?**

Laikotarpio pratęsimas yra išimtis iš taisyklės ir vertinamas kiekvienu atskiru atveju skirtingai. Turėtumėte susisiekite su „Microsoft“ partnerio pagalbos centru.

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365 Commerce“ vertinimo aplinkos peržiūra](cpe-overview.md)

[Parenkite „Dynamics 365 Commerce“ vertinimo aplinką](provisioning-guide.md)

[Sukonfigūruokite „Dynamics 365 Commerce“ vertinimo aplinką](cpe-post-provisioning.md)

[Sukonfigūruokite „BOPIS“ „Dynamics 365 Commerce“ vertinamoje aplinkoje](cpe-bopis.md)

[Konfigūruokite pasirinktas savybes „Dynamics 365 Commerce“ vertinamoje aplinkoje](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]