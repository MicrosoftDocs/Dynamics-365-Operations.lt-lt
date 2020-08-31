---
title: Kuruojamų rekomendacijų kūrimas rankiniu būdu
description: Šioje temoje paaiškinama, kaip prekybininkai gali rankiniu būdu kurti ir tvarkyti produktų sąrašus, skirtus „Microsoft Dynamics 365 Commerce“ klientams.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9826785700dcc1a35e6199b7aeff4e06b6d9da39
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665062"
---
# <a name="manually-create-curated-recommendations"></a>Kuruojamų rekomendacijų kūrimas rankiniu būdu

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip prekybininkai gali rankiniu būdu kurti ir tvarkyti produktų rekomendacijų sąrašus, skirtus „Microsoft Dynamics 365 Commerce“ klientams.

Kuruojami sąrašai yra atskiro turinio, kurį sukūrė ir kuruoja žmonės, rinkiniai.  

## <a name="create-a-new-list"></a>Naujo sąrašo sukūrimas

Norėdami sukurti kuruojamą produktų rekomendacijų sąrašą, atlikite tolesnius veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba &gt; Produktų rekomendacijos &gt; Rekomendacijų sąrašai**.
1. Pasirinkite **Naujas**.
1. Lauke **Sąrašo ID** įveskite reikšmę.
1. Lauke **Sąrašo pavadinimas** įveskite reikšmę.
    - **Sąrašo pavadinimas** bus rodomas modulio **Produktų rinkinys** kuruojamų sąrašų skyriuje.
1. Norėdami į sąrašą įtraukti produktų, pasirinkite **įtraukti produktų**.
1. Norėdami pakeisti sąrašo produktų tvarką, įveskite reikšmę stulpelyje **Rodymo tvarka**.
    - Jei du produktai turi tokią pačią rodymo tvarkos reikšmę, tada galutinė tų dviejų rezultatų tvarka gali skirtis nuo esančios įmonės padalinyje.
1. Pasirinkite **Įrašyti**, kad įrašytumėte sąrašą.

## <a name="example-list"></a>Sąrašo pavyzdys

![Kuruojamo sąrašo pavyzdys įmonės padalinyje](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje](enable-adls-environment.md)

[Įjungti produktų rekomendacijas](enable-product-recommendations.md)

[Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md)

[Personalizuotų rekomendacijų atsisakymas](personalization-gdpr.md)

[Įjungti „apsipirkti panašia mada“ rekomendacijas](shop-similar-looks.md)

[Produktų rekomendacijų įtraukimas į EKA](product.md)

[Rekomendacijų įtraukimas į operacijų ekraną](add-recommendations-control-pos-screen.md)

[AI-ML rekomendacijų rezultatų koregavimas](modify-product-recommendation-results.md)

[Rekomendacijų su demonstraciniais duomenimis kūrimas](product-recommendations-demo-data.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)
