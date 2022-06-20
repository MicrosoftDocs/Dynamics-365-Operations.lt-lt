---
title: Rekomendacijų įtraukimas į operacijų ekraną
description: Šiame straipsnyje aprašoma, kaip įtraukti rekomendacijų kontrolę į operacijos ekraną, nurodytą point of sale (EKA) įrenginyje, naudojant ekrano maketo konstruktorių dalyje Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4748ade8d6693666b58cbded2123d3449d191509
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862077"
---
# <a name="add-recommendations-to-the-transaction-screen"></a>Rekomendacijų įtraukimas į operacijų ekraną

[!include [banner](includes/banner.md)]


Šiame straipsnyje aprašoma, kaip įtraukti rekomendacijų kontrolę į operacijos ekraną, nurodytą point of sale (EKA) įrenginyje, naudojant ekrano maketo konstruktorių dalyje Microsoft Dynamics 365 Commerce. Norėdami gauti daugiau informacijos apie produktų rekomendacijas, perskaitykite [EKA dokumentacijos produktų rekomendacijas.](product.md).


Naudodami „Commerce“ galite rodyti produktų rekomendacijas savo EKA įrenginyje. Norėdami rodyti produktų rekomendacijas, turite valdiklį įtraukti į operacijų ekraną naudodami ekrano maketo dizaino įrankį. 

## <a name="open-layout-designer"></a>Atidarykite maketo dizaino įrankį

1. Pasirinkite **Mažmeninė prekyba ir prekyba** &gt; **Kanalo sąranka** &gt; **EKA sąranka** &gt; **EKA** &gt; **Ekrano maketai**.
2. Naudokite spartųjį filtrą, kad rastumėte ekraną, į kurį norite įtraukti valdiklį. Pvz., filtruokite lauką **Ekrano maketo ID** naudodami reikšmę **F2CP16:9M**.
3. Sąraše raskite ir pasirinkite norimą įrašą. Pvz., pasirinkite **Pavadinimas: F2CP16:9M Ekrano maketo ID: F2CP16:9M**.
4. Spustelėkite dalį **Maketo dizaino įrankis**.
5. Vykdykite paraginimo instrukcijas, kad paleistumėte maketo dizaino įrankį. Kai būsite paraginti įvesti kredencialus, įveskite tuos pačius kredencialus, kuriuos naudojote paleisdami maketo dizaino įrankį iš puslapio **Ekrano maketai**.
6. Prisijungus bus parodytas puslapis, panašus į toliau pateiktą puslapį. Maketas skirsis, atsižvelgiant į jūsų parduotuvėje atliktus tinkinimus.


    [![Maketo dizaineris.](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)

## <a name="choose-a-display-option"></a>Pasirinkite rodomą parinktį

Galima pasirinkti iš dviejų konfigūracijų parinkčių. Pasirinkite geriausiai jūsų parduotuvei tinkančią parinktį ir vadovaukitės likusiomis instrukcijomis, kad baigtumėte valdiklio nustatymą. Toliau nurodytos dvi parinktys.

- Rekomendacijos rodomos visada.
- Skirtukas **Rekomendacijos** rodomas ekrano kairiojoje pusėje esančiame tinklelyje.

### <a name="make-recommendations-always-visible"></a>Nustatymas, kad rekomendacijos būtų visada matomos


1. Sumažinkite operacijų eilučių informacijos srities aukštį, kad ji būtų tokio paties aukščio kaip jos kairėje esanti kliento sritis.


    [![Sumažintas operacijų eilučių informacijos srities aukštis.](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)

2. Iš kairiojo meniu rekomendacijų valdiklį nuvilkite tarp operacijų eilučių informacijos srities ir mygtukyno į operacijų ekrano apatinėje dalyje, centre. Keiskite valdiklio dydį, kad jis tilptų toje erdvėje.

    [![Rekomendacijų valdiklis įtrauktas į maketą.](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)


3. Norėdami įrašyti ir uždaryti maketo dizaino įrankį, spustelėkite **X**.
4. „Commerce“ eikite į **Mažmeninė prekyba ir prekyba** &gt; **Mažmeninės prekybos ir prekybos IT** &gt; **Paskirstymo grafikas**.
5. Išplečiamajame sąraše pasirinkite **1090 registrai**.
6. Spustelėkite **Paleisti dabar**.


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Skirtuko Rekomendacijos įtraukimas į mygtukyną, esantį dešiniojoje ekrano pusėje

1. Dešiniuoju pelės klavišu spustelėkite tuščią erdvę po paskutiniuoju skirtuku mygtukyne, kuris yra kairiojoje puslapio pusėje.

2. Spustelėkite **Pritaikyti**.

    [![Tinkinimas – dialogo langas Skirtukų valdymas.](./media/pic-5.png)](./media/pic-5.png)

3. Spustelėkite **Naujas skirtukas**.
4. Raskite naują skirtuką, kurį ką tik įtraukėte. Gali reikėti slinkti žemyn.
5. Išplečiamajame sąraše **Turinys** pasirinkite **Rekomenduojami produktai**.

    [![Parinkties Rekomenduojami produktai pasirinkimas lauke Turinys.](./media/pic-6.png)](./media/pic-6.png)

6. Lauke **Žyma** įveskite rekomendacijų skirtuko pavadinimą. Pavyzdžiui, įveskite „Rekomenduojami produktai“.
7. Lauke **Vaizdas** pasirinkite vaizdą, kuris bus rodomas skirtuke.
8. Spustelėkite **Gerai**. Naujasis skirtukas atsiranda mygtukyne.
9. Norėdami įrašyti ir uždaryti maketo dizaino įrankį, spustelėkite **X**.
10. „Commerce“ eikite į **Mažmeninė prekyba ir prekyba** &gt; **Mažmeninės prekybos ir prekybos IT** &gt; **Paskirstymo grafikas**.
11. Išplečiamajame sąraše pasirinkite **1090 registrai**.
12. Spustelėkite **Paleisti dabar**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje](enable-adls-environment.md)

[Įjungti produktų rekomendacijas](enable-product-recommendations.md)

[Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md)

[Personalizuotų rekomendacijų atsisakymas](personalization-gdpr.md)

[Įjungti „apsipirkti panašia mada“ rekomendacijas](shop-similar-looks.md)

[Produktų rekomendacijų įtraukimas į EKA](product.md)

[AI-ML rekomendacijų rezultatų koregavimas](modify-product-recommendation-results.md)

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[Rekomendacijų su demonstraciniais duomenimis kūrimas](product-recommendations-demo-data.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]