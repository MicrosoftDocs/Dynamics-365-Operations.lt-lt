---
title: Žiniatinklio veiklos įvykių rinkimo atsisakymas
description: Šiame straipsnyje paaiškinama, kaip leisti jūsų svetainei atsisakyti interneto veiklos įvykių rinkinio Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: 81343f5033366484140f73fcc313ecd9f35e7d47
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286731"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Žiniatinklio veiklos įvykių rinkimo atsisakymas
[!include [banner](includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip leisti klientams atsisakyti interneto veiklos įvykių rinkinio, naudojant Microsoft Dynamics 365 Commerce.

„Dynamics 365 Commerce“ leidžia svetainių administratoriams analizuoti savo el. prekybos svetainių vartotojų veiklą žiniatinklyje. Tokiu būdu jie gali geriau suprasti, kaip naudojamos jų svetainės, ir gali jas optimizuoti, kad būtų užtikrinta geresnė vartotojų patirtis ir pasiekti verslo tikslai.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>Būdai, kaip administratoriai gali įdiegti atsisakymo funkcijas

Administratoriai atsisakymo funkcijas gali įdiegti trimis būdais.

### <a name="opt-out-on-behalf-of-users"></a>Atsisakymas vartotojų vardu

„Commerce“ pagrindinio komponento (HQ) dalyje Paskyrų tvarkymas administratoriai gali atsisakyti vartotojų vardu.

1. HQ kliento puslapyje **Visi klientai** raskite ir pasirinkite klientą.
1. Kliento informacijos puslapyje, „FastTab“ konteinerio **Mažmeninė prekyba** dalyje **Privatumas** nustatykite parinkties **Nestebėti žiniatinklio veiklos** reikšmę kaip **Taip**.

    ![Privatumo nustatymai.](media/Disablepersonalizationpart2.png)

1. Pasirinkite **Įrašyti** ir uždarykite puslapį.

### <a name="module-based-opt-out-experience"></a>Moduliais pagrįsta atsisakymo galimybė

Administratoriai gali leisti autentifikuotiems vartotojams patiems atsisakyti žiniatinklio veiklos įvykių rinkimo. Norėdami įgalinti šią atsisakymo galimybę, pridėkite vartotojo atsisakymo modulį prie kliento sąskaitos profilio puslapių.

### <a name="custom-extensions"></a>Pasirinktiniai plėtiniai

Administratoriai gali sukurti savo plėtinius, kad galėtų valdyti vartotojų atsisakymo galimybę. Daugiau informacijos rasite [Skambučių mažmeninės prekybos serverio API](e-commerce-extensibility/call-retail-server-apis.md) ir [Internetinio kanalo išplėtimas](e-commerce-extensibility/overview.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
