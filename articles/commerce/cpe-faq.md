---
title: DUK apie „Dynamics 365 Commerce” vertinimo aplinką
description: Šiame straipsnyje pateikiami atsakymai į dažnai užduodamus klausimus apie vertinimo Microsoft Dynamics 365 Commerce aplinką.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 94717c1b9ff4ec05ee9734e1471a137cef55edfe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861945"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>DUK apie „Dynamics 365 Commerce” vertinimo aplinką

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikiami atsakymai į dažnai užduodamus klausimus apie vertinimo Microsoft Dynamics 365 Commerce aplinką.

## <a name="can-we-use-the-commerce-evaluation-environment-as-an-e-commerce-storefront-for-customers-that-currently-implement-retail"></a>Ar galime naudoti komercijos vertinimo aplinką kaip „e-Commerce“ parduotuvę savo klientams, kurie jau įgyvendino „Retail“?

Nr. Komercijos vertinimo aplinka yra skirta tik vertinimui. Jei reikia aplinkos klientui, kuris yra įsidiegęs „Retail“, kreipkitės į „Microsoft“.

## <a name="can-the-commerce-evaluation-environment-be-used-to-provision-the-e-commerce-features-on-top-of-an-existing-applicationenvironment-that-implements-retail"></a>Ar gali komercijos vertinimo aplinka būti naudojama „e-Commerce“ savybių parengimui esančioje aplinkoje ar programose, kurios įgyvendino „Retail“?

Ne (dažniausiai). Komercijos vertinimo komponentai yra prieinami tik aplinkose, kurios atitinka konfigūravimus, nustatytus būtinosiose sąlygose ir parengimo gide. Taip pat, reikalaujama demo duomenų pagrindo versija nebus prieinama aplinkose, kurios turi pirmąją versiją, ankstesnę nei 10.0.8. 

## <a name="what-costs-are-involved-in-deploying-the-commerce-evaluation-environment-on-microsoft-azure-via-microsoft-dynamics-lifecycle-services-lcs"></a>Kiek kainuoja įdiegti komercijos vertinimo aplinką „Microsoft Azure“ paslaugoje, naudojant „Microsoft Dynamics Lifecycle Services“ (LCS)?

Tradicinė "Dynamics 365" finansų /Dynamics 365 Supply Chain Management Dynamics 365 Commerce būstinės parodomoji aplinka (virtualioji \[mašina VM\]) bus laikoma jūsų "Azure" abonemente. Norėdami įvertinti šiuos kaštus, galite naudoti [„Azure“ kainų skaičiuotuvą](https://azure.microsoft.com/pricing/calculator/).

Kiti komponentai, tokie kaip „Commerce Scale Unit“, komercijos vietos kūrimo įrankis ir jūsų „e-Commerce“ vieta bus prieinama kaip programinės įrangos paslaugos (SaaS) ir patalpinti „Microsoft“.

## <a name="which-azure-geographies-are-currently-supported-for-the-commerce-evaluation-environment"></a>Kokios „Azure“ geografinės sritys šiuo metu palaikomos komercijos vertinimo aplinkoje?

Komercijos vertinimo aplinka gali būt patalpinta tik Šiaurės Amerikos regione.

## <a name="is-there-a-downloadable-virtual-hard-disk-vhd-that-has-the-complete-onebox-virtual-machine-vm-option"></a>Ar galima atsisiųsti virtualųjį standųjį diską (VHD), kuriame yra visavertės „OneBox“ virtualiosios mašinos (VM) parinktis?

„Dynamics 365 Commerce“ ir „Commerce Scale Unit“ yra visa programinė įranga, kaip paslaugų (Saas) ir turi būti patalpinta debesyje.

## <a name="how-long-can-the-commerce-evaluation-environment-be-used"></a>Kiek laiko galima naudoti komercijos vertinimo aplinką?

Komercijos vertinimo aplinka turi 30 dienų laiko limitą nuo dienos, kai SaaS komponentai, tokie kaip „Commerce Scale Unit“, komercijos vietos kūrimo įrankis ir jūsų „e-Commerce“ vieta yra suteikta.

## <a name="can-i-extend-the-time-limit-for-my-commerce-evaluation-environment"></a>Ar galiu pratęsti komercijos vertinimo aplinkos laikotarpį?

Laikotarpio pratęsimas yra išimtis iš taisyklės ir vertinamas kiekvienu atskiru atveju skirtingai. Turėtumėte susisiekite su „Microsoft“ partnerio pagalbos centru.

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365 Commerce“ vertinimo aplinkos peržiūra](cpe-overview.md)

[Parenkite „Dynamics 365 Commerce“ vertinimo aplinką](provisioning-guide.md)

[Sukonfigūruokite „Dynamics 365 Commerce“ vertinimo aplinką](cpe-post-provisioning.md)

[Sukonfigūruokite „BOPIS“ „Dynamics 365 Commerce“ vertinamoje aplinkoje](cpe-bopis.md)

[Konfigūruokite pasirinktas savybes „Dynamics 365 Commerce“ vertinamoje aplinkoje](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
