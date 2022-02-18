---
title: Sukonfigūruokite saugyklos valdymo programą mobiliesiems debesies ir krašto mastelio vienetams
description: Šioje temoje paaiškinama, kaip nustatyti sandėlių valdymo programas mobiliesiems sandėliams, kuriuos aptarnauja debesies arba krašto masto vienetas.
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
ms.openlocfilehash: 1fa00b40db2f6246029876964dca9d3229567848
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071784"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Sukonfigūruokite saugyklos valdymo programą mobiliesiems debesies ir krašto mastelio vienetams

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti savo sandėlio valdymo programas mobiliesiems, kad jas būtų galima naudoti sandėliuose, kuriuos aptarnauja debesies arba krašto masto vienetas.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami nustatyti mobiliuosius įrenginius, kad jie prisijungtų prie debesies arba krašto masto įrenginio, patvirtinkite, kad jie gali prisijungti prie įmonės centro. Instrukcijas žr [Įdiekite ir prijunkite „Werehouse Management“ mobiliąją programėlę](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Papildoma sąranka, kai paleidžiate Sandėlio valdymo programą mobiliesiems su mastelio vienetu

Kaip dalis [sandėlio masto vieneto darbo krūvių diegimo procesas](cloud-edge-landing-page.md#scale-unit-manager-portal), dauguma duomenų, kurių reikia norint prijungti jūsų sandėlio valdymo mobiliosios programos įrenginius, automatiškai sinchronizuojami iš įmonės centro su mastelio įrenginiu. Tačiau turite įvesti duomenis **Azure Active Directory programos** puslapis (**Sistemos administravimas \> Sąranka \>Azure Active Directory programos**) dėl masto vieneto diegimo. Be to, gali tekti atnaujinti numatytuosius nustatymus **Bendrovė** vartotojo ID vertę arba sukurti naują vartotoją. Naudotojai, susieti su įmone, kuri neegzistuoja svarstyklių įrenginyje, negalės prisijungti, kai prie to mastelio įrenginio bus prijungta Sandėlio valdymo programa mobiliesiems.

> [!NOTE]
> Kadangi duomenys apie **Azure Active Directory programos** puslapis nėra sinchronizuotas, turite rankiniu būdu tvarkyti šiuos duomenis, jei norite perkelti savo sandėlio darbo krūvius į kitą masto vienetą.

Atminkite, kad kaip kiekvienos sandėlio valdymo mobiliosios programos ryšio sąrankos dalis, nurodyta Azure Active Directory išteklių URL turi būti skirtas masto vienetui, o ne įmonės centrui.
