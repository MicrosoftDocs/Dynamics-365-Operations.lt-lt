---
title: Atsisakyti asmeniniams poreikiams pritaikytų rekomendacijų
description: Šioje temoje pateikiama informacija, kaip galite leisti klientams atsisakyti asmeniniams poreikiams pritaikytų rekomendacijų, naudojant „Microsoft Dynamics 365 Commerce“.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e88980ef6ad585826762c8be35304aecbcc02ab
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154300"
---
# <a name="opt-out-of-personalized-recommendations"></a>Atsisakyti asmeniniams poreikiams pritaikytų rekomendacijų

[!include [banner](includes/banner.md)]

Šioje temoje pateikiama informacija, kaip galite leisti klientams atsisakyti asmeniniams poreikiams pritaikytų rekomendacijų, naudojant „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūrėti

Kuriant paskyrą, nauji klientai automatiškai gauna asmeniniams poreikiams pritaikytas rekomendacijas. Tačiau „Dynamics 365 Commerce“ siūlo įvairius būdus, kaip mažmenininkams leisti vartotojams atsisakyti gauti šias rekomendacijas ir apriboti jų asmeninių duomenų tvarkymą. Autentifikuoti vartotojai, kurie atsisako gauti asmeniniams poreikiams pritaikytas rekomendacijas, iškart nustos matyti asmeniniams poreikiams pritaikytus sąrašus. Be to, visi asmeniniai duomenys, kurie renkami asmeninių poreikių pritaikymui, bus pašalinti iš asmeniniams poreikiams pritaikytų rekomendacijų modelių.

Norėdami gauti daugiau informacijos apie asmeniniams poreikiams pritaikytas produkto rekomendacijas, žr. [Įgalinti asmeniniams poreikiams pritaikytas rekomendacijas](personalized-recommendations.md).

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a>Būdai, kaip mažmenininkai gali atsisakyti asmeniniams poreikiams pritaikytų rekomendacijų

Mažmenininkai gali atsisakyti asmeniniams poreikiams pritaikytų rekomendacijų trimis būdais.

### <a name="opting-out-on-behalf-of-users"></a>Atsisakymas vartotojų vardu

„Commerce“ operacijų skyriuje, Sąskaitų tvarkymas, mažmenininkai gali atsisakyti vartotojų vardu.

1. Pagrindiniame operacijų skyriaus puslapyje ieškokite **visi klientai**.
1. Ieškokite ir pasirinkite klientą, tada pasirinkite „FastTab“ **Mažmeninė prekyba**.

    ![„FastTab“ mažmeninė prekyba](./media/Disablepersonalizationpart1.png)

1. Būdami **Privatumas**, nustatykite parinktį **Išjungti asmeninius poreikius** į **Taip**.

    ![Privatumo nustatymai](./media/Disablepersonalizationpart2.png)

1. Pasirinkite **Išsaugoti** ir uždarykite puslapį.

### <a name="module-based-opt-out-experience"></a>Moduliais pagrįsta atsisakymo galimybė

Mažmenininkai gali leisti autentifikuotiems vartotojams patiems atsisakyti gauti asmeniniams poreikiams pritaikytas rekomendacijas. Norėdami įgalinti šią atsisakymo galimybę, pridėkite vartotojo atsisakymo modulį prie kliento sąskaitos profilio puslapių.

### <a name="custom-extensions"></a>Pasirinktiniai plėtiniai

Mažmenininkai gali sukurti savo plėtinius, kad galėtų valdyti vartotojų atsisakymo galimybę. Daugiau informacijos rasite [Skambučių mažmeninės prekybos serverio API](e-commerce-extensibility/call-retail-server-apis.md) ir [Internetinio kanalo išplėtimas](e-commerce-extensibility/overview.md).

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a>Autentifikuoto vartotojo vardu gaukite skaitmeninę asmeniniams poreikiams pritaikytų rekomendacijų duomenų kopiją

Klientai gali norėti įsigyti skaitmeninę savo asmeninių duomenų kopiją ir pamatyti jų rekomendacijų rezultatų eksportuotą vaizdą. Jei klientas prašo šios informacijos, mažmenininkas turi sukurti pritaikytą plėtinį, iškviečiantį Mažmeninio serverio programos programavimo sąsają (angl. API), ir visų rezultatų užklausas iš sąrašo **Parinkta jums**, remiantis kliento ID. Tada, kableliais atskyrus vertes (angl. CSV), rezultatus galima eksportuoti ir bendrinti su klientu.

Toliau parodytame pavyzdyje matoma, kaip mažmenininkas gali įvykdyti šią užduotį.

1. Mažmenininkas sukuria pasirinktinį plėtinį, kad vartotojo vardu būtų galima gauti asmeninių rekomendacijų duomenis. Norėdami gauti informacijos apie tai, kaip sukurti modulius, klonuoti esamus modulius, iškviesti Mažmeninės prekybos serverio API ir iškviesti duomenų veiksmus, žr. [Internetinio kanalo išplėtimas](e-commerce-extensibility/overview.md).
2. Pasirinktinis plėtinys iškviečia pagrindinių duomenų veiksmą **gauti rekomendacijas** ir perduoda reikiamą informaciją, remdamasis sąrašo reikalavimais. Sąraše **Parinkta jums** plėtinys duomenų perdavimui turi perduoti teisingą sąrašo pavadinimą ir kliento ID.

    Vienas iš būdų sukurti pasirinktinį plėtinį yra esamo produktų rinkimo modulio, naudojamo grąžinti rekomendacijų rezultatus, klonavimas. Klonuodamas šį esamą modulį, mažmenininkas gali modifikuoti esamą kodą ir pridėti naują mygtuką, kuris eksportuoja rekomendacijų rezultatus į CSV failą. Daugiau informacijos rasite [Klonuoti pradžios rinkinio modulį](e-commerce-extensibility/clone-starter-module.md) ir [Produktų kolekcijos moduliai](product-collection-module-overview.md).

    Norėdami pamatyti visą Mažmeninės prekybos serverio API bibliotekos vaizdą, žr. [Mažmeninės prekybos serverių klientų ir vartotojų API](dev-itpro/retail-server-customer-consumer-api.md).

3. Sukūręs pasirinktinį plėtinį, mažmenininkas gali eksportuoti visų rekomendacijų rezultatų CSV failą, pagrįstą unikaliu autentifikuoto vartotojo kliento ID.
4. Mažmenininkas gali bendrinti eksportuotą CSV failą, kuriame yra visas asmeniniams poreikiams pritaikytų rekomenduojamų produktų sąrašas su autentifikuotu vartotoju.

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[ADLS įgalinimas „Dynamics 365 Commerce” aplinkoje](enable-adls-environment.md)

[Įjungti produktų rekomendacijas](enable-product-recommendations.md)

[Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md)

[Produktų rekomendacijų įtraukimas į EKA](product.md)

[Rekomendacijų įtraukimas į operacijų ekraną](add-recommendations-control-pos-screen.md)

[AI-ML rekomendacijų rezultatų koregavimas](modify-product-recommendation-results.md)

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[Rekomendacijų su demonstraciniais duomenimis kūrimas](product-recommendations-demo-data.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)
