---
title: Produktų rekomendacijų įtraukimas į EKA
description: Šioje temoje aprašomos produktų rekomendacijų naudojimas elektroniniame kasos aparate (EKA).
author: bebeale
manager: AnnBe
ms.date: 03/19/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2ad50a83b85de49b0016549f0baec2328f1608f5
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154208"
---
# <a name="add-product-recommendations-on-pos"></a>Produktų rekomendacijų įtraukimas į EKA

[!include [banner](includes/banner.md)]

Produktų rekomendacijos yra transformuojanti verslo programa, apimanti visas prekybos sritis ir sukurianti įdomią, patrauklią ir pritaikytą produktų atradimo patirtį. Norėdami įdiegti šią funkciją EKA, atlikite veiksmus, atliktinus norint [įtraukti rekomendacijas į EKA įrenginius.](add-recommendations-control-pos-screen.md) 

Daugiau informacijos apie produktų rekomendacijų funkcijas rasite [produkto rekomendacijų apžvalgoje.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Scenarijai

Produktų rekomendacijas galima naudoti taikant toliau nurodytus EKA scenarijus. Juos rasite naudodami „Cloud POS“ arba „Modern POS“ (MPOS).

1. Puslapyje **Produkto informacija**:

    - Jeigu parduotuvės atstovas puslapyje **Produkto informacija** apsilanko skirtinguose kanaluose žiūrėdamas į ankstesnes operacijas, rekomendacijų tarnyba siūlo papildomų prekių, kurios gali būti perkamos kartu.

    [![Rekomendacijos puslapyje Produkto informacija](./media/proddetails.png)](./media/proddetails.png)

2. Puslapyje **Operacija**:

    - Rekomendacijų variklis pasiūlo prekes, pagrįstas visu krepšelio prekių, kurios dažnai perkamos kartu, sąrašu.

    > [!NOTE]
    > Norėdamas, kad rekomendacijos būtų rodomos puslapyje **Operacija**, pardavėjas turi atnaujinti „Dynamics 365 Commerce“ ekrano išdėstymą. Valdiklis **Rekomendacijos** turi būti perkeltas į puslapį **Operacija**.

    [![Rekomendacijos puslapyje Operacijos](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Konfigūruokite „Commerce“, kad įgalintumėte EKA rekomendacijas

Norėdami nustatyti produktų rekomendacijas, atlikite toliau pateikiamus veiksmus.

1. Užtikrinkite, kad jūsų tarnyba buvo atnaujinta į **10.0.6 komponavimo versiją.**
2. Sekite instrukcijas, kaip [įgalinti produktų rekomendacijas](../commerce/enable-product-recommendations.md) jūsų verslui.
3. Nebūtina: norėdami, kad rekomendacijos būtų rodomos operacijos ekrane, eikite į dalį **Ekrano išdėstymas**, pasirinkite savo ekrano išdėstymą, paleiskite **ekrano išdėstymo kūrimo priemonę**, o po to kur reikia perkelkite **rekomendacijų** valdiklį.
4. Eikite į **„Commerce“ parametrai**, pasirinkite **Mašininis mokymas** ir skyriuje **Įgalinti EKA rekomendacijas** pasirinkite **Taip**.
5. Norėdami pamatyti rekomendacijas naudodami EKA, paleiskite visuotinės konfigūracijos užduotį **1110**. Norėdami, kad būtų rodomi EKA ekrano išdėstymo kūrimo priemonei atlikti pakeitimai, paleiskite kanalo konfigūracijos užduotį **1070**.

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Trikčių šalinimas, kai funkcija Produktų rekomendacijos jau įjungta

- Eikite į **„Commerce“ parametrai** \> **Rekomendacijų sąrašai** \> **Išjungti produkto rekomendacijas** ir paleiskite **Bendra konfigūracijos užduotis\[9999\]**. 
- Jei, naudodami **ekrano maketo dizaino įrankį**, į savo operacijų ekraną įtraukėte **rekomendacijų valdiklį**, jį taip pat pašalinkite.
- Jei turite papildomų klausimų, norėdami gauti daugiau informacijos peržiūrėkite [Produkto rekomendacijų DUK](../commerce/faq-recommendations.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[ADLS įgalinimas „Dynamics 365 Commerce” aplinkoje](enable-adls-environment.md)

[Įjungti produktų rekomendacijas](enable-product-recommendations.md)

[Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md)

[Personalizuotų rekomendacijų atsisakymas](personalization-gdpr.md)

[Rekomendacijų įtraukimas į operacijų ekraną](add-recommendations-control-pos-screen.md)

[AI-ML rekomendacijų rezultatų koregavimas](modify-product-recommendation-results.md)

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[Rekomendacijų su demonstraciniais duomenimis kūrimas](product-recommendations-demo-data.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)
