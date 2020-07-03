---
title: „Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje
description: Šioje temoje paaiškinama, kaip įjungti ir tikrinti „Azure Data Lake Storage“ „Dynamics 365 Commerce“ aplinkoje. Tai yra būtina sąlyga norint įgalinti produkto rekomendacijas.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
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
ms.openlocfilehash: 83b829306c2da2d10924e547fd3cac6ae6781db3
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404191"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip įjungti ir tikrinti „Azure Data Lake Storage“ „Dynamics 365 Commerce“ aplinkoje. Tai yra būtina sąlyga norint įgalinti produkto rekomendacijas.

## <a name="overview"></a>Peržiūrėti

Sprendime „Dynamics 365 Commerce“ visų produktų ir operacijų informacija sekama aplinkos objektų saugykloje. Norint, kad šiuos duomenis būtų galima pasiekti naudojant kitas „Dynamics 365“ tarnybas, pvz., duomenų analizę, verslo įžvalgas ir personalizuotas rekomendacijas, reikia sujungti aplinką su klientui priklausančiu „Gen 2“ sprendimu „Azure Data Lake Storage“.

Kadangi „Azure Data Lake Storage“ konfigūruojama aplinkoje, visi reikiami objektų saugyklos duomenys yra dubliuojami, apsaugomi ir valdomi kliento.

Jei produkto rekomendacijos arba personalizuotos rekomendacijos aplinkoje taip pat įgalintos, produkto rekomendacijų dėklui bus suteikta prieiga prie paskirto aplanko, esančio „Azure Data Lake Storage“, kad būtų galima nuskaityti kliento duomenis ir apskaičiuoti jais pagrįstas rekomendacijas.

## <a name="prerequisites"></a>Būtinieji komponentai

Klientai turi sukonfigūruoti „Azure Data Lake Storage“ jiems priklausančioje „Azure“ prenumeratoje. Šioje temoje neaprašomas „Azure“ prenumeratos pirkimas arba saugyklos abonemento, kuriame įgalintas „Azure Data Lake Storage“, nustatymas.

Daugiau informacijos apie „Azure Data Lake Storage“ ieškokite [„Azure Data Lake Storage“ oficialioje „Gen2“ dokumentacijoje](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Konfigūravimo veiksmai

Šiame skyriuje aprašomi konfigūravimo veiksmai, kuriuos reikia atlikti, norint įgalinti „Azure Data Lake Storage“ aplinkoje, susijusioje su produktų rekomendacijomis.
Išsamesnės informacijos apie veiksmus, reikalingus įgalinti „Azure Data Lake Storage“, žr. [Leidimas objektų saugyklą naudoti kaip „Data Lake“](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>„Azure Data Lake Storage“ įgalinimas aplinkoje

1. Prisijunkite prie aplinkos tarnybinio biuro portalo.
1. Ieškokite **Sistemos parametrai** ir pereikite į skirtuką **Duomenų ryšiai**. 
1. Parinktyje **Įjungti „Data Lake“ integraciją** nustatykite **Taip**.
1. Parinktyje **Nuolat naujinti „Data Lake“** nustatykite **Taip**.
1. Paskui įveskite toliau pateikiamą būtiną informaciją.
    1. **Programos ID** // **Programos slapta informacija** // **DNS pavadinimas** – reikalinga, jungiantis prie „KeyVault“, kur saugoma slapta „Azure Data Lake Storage“ informacija.
    1. **Slaptas pavadinimas** – slaptas pavadinimas, saugomas „KeyVault“ ir naudojamas autentifikuojant „Azure Data Lake Storage“.
1. Išsaugokite keitimus puslapio viršutiniame kairiajame kampe.

Toliau pateiktame vaizde parodytas „Azure Data Lake Storage“ konfigūracijos pavyzdys.

![„Azure Data Lake Storage“ konfigūracijos pavyzdys](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>„Azure Data Lake Storage“ ryšio tikrinimas

1. Patikrinkite ryšį su KeyVault, naudodami saitą **Tikrinti „Azure Key Vault“**.
1. Patikrinkite ryšį su „Azure Data Lake Storage“, naudodami saitą **Tikrinti „Azure Storage“**.

> [!NOTE]
> Jei tikrinimo rezultatai neigiami, dar kartą patikrinkite, ar visa pirmiau pateikiama KeyVault informacija yra tinkama, tada bandykite dar kartą.

Kai ryšis patikrinamas sėkmingai, turite įjungti automatinį objektų saugyklos atnaujinimą.

Norėdami įjungti automatinį objektų saugyklos atnaujinimą, atlikite tolesnius veiksmus.

1. Ieškokite **Objektų saugykla**.
1. Kairėje esančiame sąraše pereikite prie įrašo **RetailSales** ir pasirinkite **Redaguoti**.
1. Įsitikinkite, kad parinktyje **Automatinis atnaujinimas įjungtas** nustatyta **Taip**, pasirinkite **Atnaujinti**, tada pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas objektų saugyklos pavyzdys, kai automatinis atnaujinimas įjungtas.

![Objektų saugyklos pavyzdys, kai automatinis atnaujinimas įjungtas](./media/exampleADLSConfig2.png)

Dabar „Azure Data Lake Storage“ sukonfigūruota aplinkoje. 

Jei dar jų neatlikote, atlikite veiksmus, skirtus [įgalinti produkto rekomendacijas ir personalizavimą](enable-product-recommendations.md) aplinkoje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Leidimas objektų saugyklą naudoti kaip „Data Lake“](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[Įjungti produktų rekomendacijas](enable-product-recommendations.md)

[Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md)

[Personalizuotų rekomendacijų atsisakymas](personalization-gdpr.md)

[Produktų rekomendacijų įtraukimas į EKA](product.md)

[Rekomendacijų įtraukimas į operacijų ekraną](add-recommendations-control-pos-screen.md)

[AI-ML rekomendacijų rezultatų koregavimas](modify-product-recommendation-results.md)

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[Rekomendacijų su demonstraciniais duomenimis kūrimas](product-recommendations-demo-data.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)
