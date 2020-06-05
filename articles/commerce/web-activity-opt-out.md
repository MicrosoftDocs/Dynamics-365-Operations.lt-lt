---
title: Žiniatinklio veiklos įvykių rinkimo atsisakymas
description: Šioje temoje aiškinama, kaip galite leisti savo svetainės lankytojams atsisakyti žiniatinklio veiklos įvykių rinkimo naudojant „Microsoft Dynamics 365 Commerce“.
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4b0e48307527a8fea729d8dfdcdbc6337be0faf1
ms.sourcegitcommit: 8058db089b8768076ff1250be77d42a6e2b3f570
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378997"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Žiniatinklio veiklos įvykių rinkimo atsisakymas
[!include [banner](includes/banner.md)]

Šioje temoje aiškinama informacija, kaip galite leisti klientams atsisakyti žiniatinklio veiklos įvykių rinkimo naudojant „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūra

„Dynamics 365 Commerce“ leidžia svetainių administratoriams analizuoti savo el. prekybos svetainių vartotojų veiklą žiniatinklyje. Tokiu būdu jie gali geriau suprasti, kaip naudojamos jų svetainės, ir gali jas optimizuoti, kad būtų užtikrinta geresnė vartotojų patirtis ir pasiekti verslo tikslai.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>Būdai, kaip administratoriai gali įdiegti atsisakymo funkcijas

Administratoriai atsisakymo funkcijas gali įdiegti trimis būdais.

### <a name="opt-out-on-behalf-of-users"></a>Atsisakymas vartotojų vardu

„Commerce“ pagrindinio komponento (HQ) dalyje Paskyrų tvarkymas administratoriai gali atsisakyti vartotojų vardu.

1. HQ kliento puslapyje **Visi klientai** raskite ir pasirinkite klientą.
1. Kliento informacijos puslapyje, „FastTab“ konteinerio **Mažmeninė prekyba** dalyje **Privatumas** nustatykite parinkties **Nestebėti žiniatinklio veiklos** reikšmę kaip **Taip**.

    ![Privatumo nustatymai](media/Disablepersonalizationpart2.png)

1. Pasirinkite **Įrašyti** ir uždarykite puslapį.

### <a name="module-based-opt-out-experience"></a>Moduliais pagrįsta atsisakymo galimybė

Administratoriai gali leisti autentifikuotiems vartotojams patiems atsisakyti žiniatinklio veiklos įvykių rinkimo. Norėdami įgalinti šią atsisakymo galimybę, pridėkite vartotojo atsisakymo modulį prie kliento sąskaitos profilio puslapių.

### <a name="custom-extensions"></a>Pasirinktiniai plėtiniai

Administratoriai gali sukurti savo plėtinius, kad galėtų valdyti vartotojų atsisakymo galimybę. Daugiau informacijos rasite [Skambučių mažmeninės prekybos serverio API](e-commerce-extensibility/call-retail-server-apis.md) ir [Internetinio kanalo išplėtimas](e-commerce-extensibility/overview.md).
