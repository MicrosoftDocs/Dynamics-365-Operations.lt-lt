---
title: ADLS įgalinimas „Dynamics 365 Commerce“ aplinkoje
description: Šioje temoje paaiškinama, kaip įjungti ir tikrinti „Azure Data Lake Storage“ (ADLS) „Dynamics 365 Commerce“ aplinkoje. Tai yra būtina sąlyga norint įgalinti produkto rekomendacijas.
author: bebeale
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 068eb522bd44e02dd31d3337a051691a956637fc
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025266"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a>ADLS įgalinimas „Dynamics 365 Commerce“ aplinkoje

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip įjungti ir tikrinti „Azure Data Lake Storage“ (ADLS) „Dynamics 365 Commerce“ aplinkoje. Tai yra būtina sąlyga norint įgalinti produkto rekomendacijas.

## <a name="overview"></a>Peržiūrėti

Sprendime „Dynamics 365 Commerce“ visų produktų ir operacijų informacija sekama aplinkos objektų saugykloje. Norint, kad šiuos duomenis būtų galima pasiekti naudojant kitas „Dynamics 365“ tarnybas, pvz., duomenų analizę, verslo įžvalgas ir personalizuotas rekomendacijas, reikia sujungti aplinką su klientui priklausančiu sprendimu „Azure Data Lake Storage“ „Gen 2“ (ADLS).

Kadangi ADLS konfigūruojamas aplinkoje, visi reikiami objektų saugyklos duomenys yra dubliuojami, apsaugomi ir valdomi kliento.

Jei produkto rekomendacijos arba personalizuotos rekomendacijos aplinkoje taip pat įgalintos, produkto rekomendacijų dėklui bus suteikta prieiga prie paskirto aplanko, esančio ADLS, kad būtų galima nuskaityti kliento duomenis ir apskaičiuoti jais pagrįstas rekomendacijas.

## <a name="prerequisites"></a>Būtinieji komponentai

Klientai turi sukonfigūruoti ADLS jiems priklausančioje „Azure“ prenumeratoje. Šioje temoje neaprašomas „Azure“ prenumeratos pirkimas arba saugyklos abonemento, kuriame įgalintas ADLS, nustatymas.

Daugiau informacijos apie ADLS ieškokite [Oficialioje ADLS dokumentacijoje](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Konfigūravimo veiksmai

Šiame skyriuje aprašomi konfigūravimo veiksmai, kuriuos reikia atlikti, norint įgalinti ADLS aplinkoje.

### <a name="enable-adls-in-the-environment"></a>ADLS įgalinimas aplinkoje

1. Prisijunkite prie aplinkos tarnybinio biuro portalo.
1. Ieškokite **Sistemos parametrai** ir pereikite į skirtuką **Duomenų ryšiai**. 
1. Parinktyje **Įjungti „Data Lake“ integraciją** nustatykite **Taip**.
1. Parinktyje **Nuolat naujinti „Data Lake“** nustatykite **Taip**.
1. Paskui įveskite toliau pateikiamą būtiną informaciją.
    1. **Programos ID** // **Programos slapta informacija** // **DNS pavadinimas** – reikalinga, jungiantis prie KeyVault, kur saugoma slapta ADLS informacija.
    1. **Slaptas pavadinimas** – slaptas pavadinimas, saugomas KeyVault ir naudojamas autentifikuojant ADLS.
1. Išsaugokite keitimus puslapio viršutiniame kairiajame kampe.

Toliau pateiktame vaizde parodytas ADLS konfigūracijos pavyzdys.

![ADLS konfigūracijos pavyzdys](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a>ADLS ryšio tikrinimas

1. Patikrinkite ryšį su KeyVault, naudodami saitą **Tikrinti „Azure Key Vault“**.
1. Patikrinkite ryšį su ADLS, naudodami saitą **Tikrinti „Azure Storage“**.

> [!NOTE]
> Jei tikrinimo rezultatai neigiami, dar kartą patikrinkite, ar visa pirmiau pateikiama KeyVault informacija yra tinkama, tada bandykite dar kartą.

Kai ryšis patikrinamas sėkmingai, turite įjungti automatinį objektų saugyklos atnaujinimą.

Norėdami įjungti automatinį objektų saugyklos atnaujinimą, atlikite tolesnius veiksmus.

1. Ieškokite **Objektų saugykla**.
1. Kairėje esančiame sąraše pereikite prie įrašo **RetailSales** ir pasirinkite **Redaguoti**.
1. Įsitikinkite, kad parinktyje **Automatinis atnaujinimas įjungtas** nustatyta **Taip**, pasirinkite **Atnaujinti**, tada pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas objektų saugyklos pavyzdys, kai automatinis atnaujinimas įjungtas.

![Objektų saugyklos pavyzdys, kai automatinis atnaujinimas įjungtas](./media/exampleADLSConfig2.png)

Dabar ADLS aplinkoje sukonfigūruotas. 

Jei dar jų neatlikote, atlikite veiksmus, skirtus [įgalinti produkto rekomendacijas ir personalizavimą](enable-product-recommendations.md) aplinkoje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[Įjungti produktų rekomendacijas](enable-product-recommendations.md)

[ĮProduktų rekomendacijų sąrašų įtraukimas į puslapius](add-reco-list-to-page.md)

[Rekomendacijų valdiklio įtraukimas į EKA įrenginių operacijų ekraną](../retail/add-recommendations-control-pos-screen.md?toc=/dynamics365/commerce/toc.json)


