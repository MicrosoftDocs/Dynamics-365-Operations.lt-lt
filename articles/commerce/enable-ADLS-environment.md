---
title: „Azure Data Lake Storage“ įjungimas „Dynamics 365 Commerce“ aplinkoje
description: Šioje temoje pateikiamos instrukcijos, kaip „Azure Data Lake Storage“ Gen 2 sprendimą „Dynamics 365 Commerce“ prie aplinkos objektų saugyklos. Tai yra būtinas žingsnis prieš įgalinant produkto rekomendacijas.
author: bebeale
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c96c29a4d9639b02e6a60ad938b7e06f7d500c68
ms.sourcegitcommit: 98061a5d096ff4b9078d1849e2ce6dd7116408d1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2021
ms.locfileid: "7466297"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>„Azure Data Lake Storage“ įjungimas „Dynamics 365 Commerce“ aplinkoje

[!include [banner](includes/banner.md)]

Šioje temoje pateikiamos instrukcijos, kaip „Azure Data Lake Storage“ Gen 2 sprendimą „Dynamics 365 Commerce“ prie aplinkos objektų saugyklos. Tai yra būtinas žingsnis prieš įgalinant produkto rekomendacijas.

Sprendimas – duomenys, reikalingi apskaičiuoti rekomendacijas, produktus ir „Dynamics 365 Commerce“ operacijas, sujungiami aplinkos objektų saugykloje. Norint, kad šiuos duomenis būtų galima pasiekti naudojant kitas „Dynamics 365“ tarnybas, pvz., duomenų analizę, verslo įžvalgas ir personalizuotas rekomendacijas, reikia sujungti aplinką su klientui priklausančiu „Gen 2“ sprendimu „Azure Data Lake Storage“.

Atlikus aukščiau aprašytus veiksmus visi kliento duomenys aplinkos objektų saugykloje automatiškai atspindėti kliento „Azure Data Lake Storage“ Gen 2 sprendimą. Kai rekomendacijų priemonės įgalintos per Funkcijų valdymo darbo sritį, kuri yra „Commerce Headquarters", rekomendacijų dėklui bus suteikta prieiga prie to paties „Azure Data Lake Storage“ Gen2 sprendimo.

Viso proceso metu klientų duomenys lieka apsaugoti ir jiems valdomi.

## <a name="prerequisites"></a>Būtinieji komponentai

Aplinkos „Dynamics 365 Commerce“ objektų saugykla turi būti prijungta prie „Azure“ „Data Lake“ „Gen Storage Gen2" sąskaitos ir prie kitų paslaugų.

Daugiau informacijos apie „Azure Data Lake Storage“ Gen2 ir kaip nustatyti ieškokite [„Azure Data Lake Storage“ oficialioje „Gen2“ dokumentacijoje](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Konfigūravimo veiksmai

Šiame skyriuje aprašomi konfigūravimo veiksmai, kuriuos reikia atlikti, norint įgalinti „Azure Data Lake Storage“ Gen2 aplinkoje, susijusioje su produktų rekomendacijomis.
Išsamesnės informacijos apie veiksmus, reikalingus įgalinti „Azure Data Lake Storage“ Gen2, žr. [Leidimas objektų saugyklą naudoti kaip „Data Lake“](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>„Azure Data Lake Storage“ įgalinimas aplinkoje

1. Prisijunkite prie aplinkos tarnybinio biuro portalo.
1. Ieškokite **Sistemos parametrai** ir pereikite į skirtuką **Duomenų ryšiai**. 
1. Parinktyje **Įjungti „Data Lake“ integraciją** nustatykite **Taip**.
1. Paskui įveskite toliau pateikiamą būtiną informaciją.
    1. **Programos ID** // **Programos slapta informacija** // **DNS pavadinimas** – reikalinga, jungiantis prie „KeyVault“, kur saugoma slapta „Azure Data Lake Storage“ informacija.
    1. **Slaptas pavadinimas** – slaptas pavadinimas, saugomas „KeyVault“ ir naudojamas autentifikuojant „Azure Data Lake Storage“.
1. Išsaugokite keitimus puslapio viršutiniame kairiajame kampe.

Toliau pateiktame vaizde parodytas „Azure Data Lake Storage“ konfigūracijos pavyzdys.

![„Azure Data Lake Storage“ konfigūracijos pavyzdys.](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>„Azure Data Lake Storage“ ryšio tikrinimas

1. Patikrinkite ryšį su KeyVault, naudodami saitą **Tikrinti „Azure Key Vault“**.
1. Patikrinkite ryšį su „Azure Data Lake Storage“, naudodami saitą **Tikrinti „Azure Storage“**.

> [!NOTE]
> Jei tikrinimo rezultatai nepavyksta, patikrinkite, ar visa pirmiau pateikiama KeyVault informacija yra tinkama, tada bandykite dar kartą.

Kai ryšis patikrinamas sėkmingai, turite įjungti automatinį objektų saugyklos atnaujinimą.

Norėdami įjungti automatinį objektų saugyklos atnaujinimą, atlikite tolesnius veiksmus.

1. Ieškokite **Objektų saugykla**.
1. Kairėje esančiame sąraše pereikite prie įrašo **RetailSales** ir pasirinkite **Redaguoti**.
1. Įsitikinkite, kad parinktyje **Automatinis atnaujinimas įjungtas** nustatyta **Taip**, pasirinkite **Atnaujinti**, tada pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas objektų saugyklos pavyzdys, kai automatinis atnaujinimas įjungtas.

![Objektų saugyklos pavyzdys, kai automatinis atnaujinimas įjungtas.](./media/exampleADLSConfig2.png)

Dabar „Azure Data Lake Storage“ sukonfigūruota aplinkoje. 

Jei dar jų neatlikote, atlikite veiksmus, skirtus [įgalinti produkto rekomendacijas ir personalizavimą](enable-product-recommendations.md) aplinkoje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Leidimas objektų saugyklą naudoti kaip „Data Lake“](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[Įjungti produktų rekomendacijas](enable-product-recommendations.md)

[Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md)

[Personalizuotų rekomendacijų atsisakymas](personalization-gdpr.md)

[Įjungti „apsipirkti panašia mada“ rekomendacijas](shop-similar-looks.md)

[Produktų rekomendacijų įtraukimas į EKA](product.md)

[Rekomendacijų įtraukimas į operacijų ekraną](add-recommendations-control-pos-screen.md)

[AI-ML rekomendacijų rezultatų koregavimas](modify-product-recommendation-results.md)

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[Rekomendacijų su demonstraciniais duomenimis kūrimas](product-recommendations-demo-data.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
