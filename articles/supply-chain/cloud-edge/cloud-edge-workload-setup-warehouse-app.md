---
title: mobiliosios programos „Warehouse Management“ konfigūravimas debesiui ir briaunos skalės vienetams
description: Šiame straipsnyje paaiškinama, kaip nustatyti sandėlių valdymo mobiliąsias programėles, skirtas sandėliams, kurie pristatomi debesies arba briaunos svarstyklių vienetais.
author: perlynne
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 86edef2dfa6e9c71c04d50f185148be3a622fea1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865244"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>mobiliosios programos „Warehouse Management“ konfigūravimas debesiui ir briaunos skalės vienetams

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti sandėlio valdymo mobiliąsias programėles, kad jas būtų galima naudoti sandėliuose, kurie pateikiami debesies arba kraštų skalės vienetais.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradedant nustatyti savo mobiliųjų įrenginių ryšį su debesies arba briaunos skalės vienetu, patvirtinkite, kad jie gali prisijungti prie įmonės centro. Norėdami gauti daugiau instrukcijų, [įdiekite ir prijunkite sandėlio valdymo mobiliąją programą](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Papildomas nustatymas paleidus sandėlio valdymo mobiliąją programą naudojant skalės vienetą

Kaip sandėlio [skalės vieneto darbo krūvių diegimo proceso dalis, dauguma duomenų, reikalingų sandėlio valdymo mobiliųjų programų įrenginiams prijungti, automatiškai sinchronizuojami iš įmonės centro į skalės](cloud-edge-landing-page.md#scale-unit-manager-portal) vienetą. Tačiau programos puslapio (**Azure Active Directory Sistemos administravimo sąrankos programos** **) duomenis turite įvesti \>\>Azure Active Directory skalės vieneto diegimo metu.** Be to, gali reikėti atnaujinti vartotojo **ID numatytąją** įmonės vertę arba sukurti naują vartotoją. Vartotojai, susieti su įmone, kuri neegzistuoja skalės vieneto diegime, negalės prisiregistruoti, kai sandėlio valdymo mobilioji programa prijungta prie tos skalės vieneto.

> [!NOTE]
> Programų puslapio duomenys nesinchronizuoti **Azure Active Directory**, todėl turite rankiniu būdu prižiūrėti duomenis, jei norite perkelti sandėlio darbo krūvius į kitą skalės vienetą.

Nepamirškite, kad, kaip kiekvienos sandėlio valdymo mobiliosios programos ryšio nustatymo dalis, nurodytas išteklių URL turi būti skirtas svarstyklių vienetui, Azure Active Directory o ne įmonės centrui.
