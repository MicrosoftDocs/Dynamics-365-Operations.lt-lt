---
title: Produktų rekomendacijų įtraukimas į EKA
description: Šiame straipsnyje aprašoma, kaip naudoti produkto rekomendacijas point of sale (EKA) įrenginyje.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 170e2bf18aefc79a796620818c7100ff8e6e689a
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460062"
---
# <a name="add-product-recommendations-on-pos"></a>Produktų rekomendacijų įtraukimas į EKA

[!include [banner](includes/banner.md)]

Produktų rekomendacijos yra transformuojanti verslo programa, apimanti visas prekybos sritis ir sukurianti įdomią, patrauklią ir pritaikytą produktų atradimo patirtį. Norėdami įdiegti šią funkciją EKA, atlikite veiksmus, atliktinus norint [įtraukti rekomendacijas į EKA įrenginius.](add-recommendations-control-pos-screen.md) 

Daugiau informacijos apie produktų rekomendacijų funkcijas rasite [produkto rekomendacijų apžvalgoje.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Scenarijai

Produktų rekomendacijas galima naudoti taikant toliau nurodytus EKA scenarijus. Juos rasite naudodami „Cloud POS“ arba „Modern POS“ (MPOS).

1. Puslapyje **Produkto informacija**:

    - Jei parduotuvė susieja apsilankymus **produkto** informacijos puslapyje, kai jie ieško ankstesnių operacijų skirtinguose kanaluose, rekomendacijų tarnyba siūlo papildomas prekes, kurios tikriausiai bus nupirktos kartu. Priklausomai nuo papildomų paslaugos priedų, mažmenininkai, be pritaikytų rekomendacijų vartotojams, **·** **kurie** turi ankstesnę pirkimo retrospektyvą, gali rodyti rekomendacijas apie panašią parduotuvės išvaizdą ir parduotuvės panašias produkto aprašymo rekomendacijas.

    [![Rekomendacijos puslapyje Produkto informacija.](./media/proddetails.png)](./media/proddetails.png)

2. Puslapyje **Operacija**:

    - Rekomendacijų variklis pasiūlo prekes, pagrįstas visu krepšelio prekių, kurios dažnai perkamos kartu, sąrašu.

    > [!NOTE]
    > Norėdamas, kad rekomendacijos būtų rodomos puslapyje **Operacija**, pardavėjas turi atnaujinti „Dynamics 365 Commerce“ ekrano išdėstymą. Valdiklis **Rekomendacijos** turi būti perkeltas į puslapį **Operacija**.

    [![Rekomendacijos puslapyje Operacijos.](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Konfigūruokite „Commerce“, kad įgalintumėte EKA rekomendacijas 

Norėdami nustatyti produkto rekomendacijas, patvirtinkite, kad baigėte "Commerce" produktų rekomendacijų parengimo procesą, atlikite veiksmus, nurodytus produkto [rekomendacijose įgalinti](../commerce/enable-product-recommendations.md). Pagal numatytuosius nustatymus, rekomendacijos **rodomos** **ir** produkto informacijos puslapyje, ir kliento informacijos puslapyje po to, kai užbaigsite atidėjimo veiksmus ir duomenys bus sėkmingai parinkti. 

## <a name="add-recommendations-to-the-transaction-screen"></a>Rekomendacijų įtraukimas į operacijų ekraną

1. Norėdami pridėti rekomendacijas į operacijų ekraną, atlikite veiksmus, aprašytus [prie operacijos ekrano pridėti rekomendacijas](add-recommendations-control-pos-screen.md).
1. Norėdami atsižvelgti į EKA ekrano maketo dizaino įrankio pakeitimus, **paleiskite kanalo konfigūravimo 1070** užduotį "Commerce Headquarters".

> [!NOTE] 
> Jei norite įgalinti EKA rekomendacijas naudodami RecoMock kableliais atskirtų verčių (CSV) failą, prieš konfigūruokite maketo tvarkytuvą, turite įdiegti CSV Microsoft Dynamics failą į ciklo tarnybų (LCS) turto biblioteką. Jei naudojate RecoMock CSV failą, jums nereikia įgalinti rekomendacijų. CSV failas galimas tik demonstraciniu tikslu. Rekomenduojama klientams arba sprendimų architektams, norintiems pateikti parodomųjų sąrašų išvaizdą nepirkant papildomų atsargų saugojimo vieneto (SKU).

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje](enable-adls-environment.md)

[Įjungti produktų rekomendacijas](enable-product-recommendations.md)

[Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md)

[Personalizuotų rekomendacijų atsisakymas](personalization-gdpr.md)

[Įjungti „apsipirkti panašia mada“ rekomendacijas](shop-similar-looks.md)

[Rekomendacijų įtraukimas į operacijų ekraną](add-recommendations-control-pos-screen.md)

[AI-ML rekomendacijų rezultatų koregavimas](modify-product-recommendation-results.md)

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[Rekomendacijų su demonstraciniais duomenimis kūrimas](product-recommendations-demo-data.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
