---
title: Produktų rekomendacijos EKA
description: Šioje temoje aprašomos produktų rekomendacijų naudojimas elektroniniame kasos aparate (EKA).
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: c78fc1f2f1bb08d01828a8b71ad5d3c16ad31b86
ms.sourcegitcommit: 5b53bdafa5cb9a1279576bfece0452a50383b122
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/01/2019
ms.locfileid: "2278390"
---
# <a name="product-recommendations-on-pos"></a>Produktų rekomendacijos EKA

[!include [banner](includes/banner.md)]

Iš esmės produktų rekomendacijos yra pokyčius lemianti verslo programa, kuri apima visas mažmeninės prekybos erdves, kad sukurtų turtingą, įtraukiančią ir pritaikytą produktų atradimo patirtį. Norėdami įdiegti šią funkciją EKA, atlikite veiksmus, atliktinus norint [įtraukti rekomendacijas į EKA įrenginius.](add-recommendations-control-pos-screen.md) 

Daugiau informacijos apie produktų rekomendacijų funkcijas rasite [produkto rekomendacijų apžvalgoje.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Scenarijai

Produktų rekomendacijas galima naudoti taikant toliau nurodytus EKA scenarijus. Juos rasite naudodami „Cloud POS“ arba „Modern POS“ (MPOS).

1. Puslapyje **Produkto informacija**:

    - • Jeigu parduotuvės atstovas puslapyje **Produkto informacija** apsilanko skirtinguose kanaluose žiūrėdamas į ankstesnes operacijas, rekomendacijų tarnyba siūlo papildomų prekių, kurios gali būti perkamos kartu.

    [![Rekomendacijos puslapyje Produkto informacija](./media/proddetails.png)](./media/proddetails.png)

2. Puslapyje **Operacija**:

    - • Rekomendacijų variklis pasiūlo prekes, pagrįstas visu krepšelio prekių, kurios dažnai perkamos kartu, sąrašu.

    > [!NOTE]
    > Norėdamas, kad rekomendacijos būtų rodomos puslapyje **Operacija**, pardavėjas turi atnaujinti „Dynamics 365 for Retail“ ekrano išdėstymą. Valdiklis **Rekomendacijos** turi būti perkeltas į puslapį **Operacija**.

    [![Rekomendacijos puslapyje Operacijos](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-dynamics-365-retail-to-enable-pos-recommendations"></a>Sukonfigūruokite „Dynamics 365 Retail“, kad būtų leidžiamos EKA rekomendacijos

Norėdami nustatyti produktų rekomendacijas, atlikite toliau pateikiamus veiksmus.

1. Užtikrinkite, kad jūsų tarnyba buvo atnaujinta į **10.0.6 komponavimo versiją.**
2. Sekite instrukcijas, kaip [įgalinti produktų rekomendacijas](../commerce/enable-product-recommendations.md) jūsų verslui.
3. Nebūtina: norėdami, kad rekomendacijos būtų rodomos operacijos ekrane, eikite į dalį **Ekrano išdėstymas**, pasirinkite savo ekrano išdėstymą, paleiskite **ekrano išdėstymo kūrimo priemonę**, o po to kur reikia perkelkite **rekomendacijų** valdiklį.
4. Eikite į **Mažmeninės prekybos parametrai**, pasirinkite **Mašininis mokymas**, dalyje **Įjungti EKA rekomendacijas** pasirinkite **Taip**.
5. Norėdami pamatyti rekomendacijas naudodami EKA, paleiskite visuotinės konfigūracijos užduotį **1110**. Norėdami, kad būtų rodomi EKA ekrano išdėstymo kūrimo priemonei atlikti pakeitimai, paleiskite kanalo konfigūracijos užduotį **1070**.



## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Trikčių šalinimas, kai funkcija Produktų rekomendacijos jau įjungta

- Eikite į **Mažmeninės prekybos parametrai** \> **Rekomendacijų sąrašai** \> **Išjungti produktų rekomendacijas** ir paleiskite **visuotinės konfigūracijos užduotį \[9999\]**. 
- Jei, naudodami **ekrano maketo dizaino įrankį**, į savo operacijų ekraną įtraukėte **rekomendacijų valdiklį**, jį taip pat pašalinkite.
- Jei turite papildomų klausimų, norėdami gauti daugiau informacijos peržiūrėkite [rekomendacijų DUK](../commerce/faq-recommendations.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Pridėti rekomendacijų valdiklį prie operacijos puslapio, esančio EKA įrenginyje](add-recommendations-control-pos-screen.md)
[Produktų rekomendacijų apžvalga](../commerce/product-recommendations.md)
[Įgalinti produkto rekomendacijas](../commerce/enable-product-recommendations.md) 
