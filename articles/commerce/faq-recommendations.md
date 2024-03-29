---
title: DUK apie produktų rekomendacijas
description: Šiame straipsnyje pateikiama informacija apie procesus ir įrankius, kuriuos galite naudoti trikčių šalinimui, susijusiam su produkto rekomendacijas ar jų rezultatais.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 77a5532ab1ae3b630bb335aa7cff6dc747184994
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900452"
---
# <a name="product-recommendations-faq"></a>DUK apie produktų rekomendacijas


[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie procesus ir įrankius, kuriuos galite naudoti trikčių šalinimui, susijusiam su [produkto rekomendacijas](product-recommendations.md) ar jų rezultatais.

## <a name="best-practices"></a>Geriausia praktika
Labai svarbu naudoti bendrųjų produktų ir variantų koncepciją. Pagrįstu variantų grupavimu su pirminiais bendraisiais produktais galima sąrašų algoritmais ir tarnyba kurti geresnius modelius. Be to, tarnyba gali naudoti tik vieną produkto egzempliorių, užuot naudojusi visus glaudžiai susijusius sąrašo variantus. Kai visi artimai susiję variantai yra įtraukti į sąrašą, gali atsirasti klaidingi arba pasikartojantys rezultatai.

## <a name="why-are-products-missing-from-my-recommendation-lists"></a>Kodėl mano rekomendacijų sąrašuose trūksta produktų?

Paprastai, jei produkto rekomendacijų sąraše trūksta prekės, gali kilti produkto konfigūracijos problema. Pavyzdžiui, gali būti netinkama produkto pradžios data arba pabaigos data, dimensija gali būti netinkamai sukonfigūruota arba produktas gali būti neatitikti kanalo asortimento ir pan.

Jei nėra rekomendacijų sąrašo, kuris yra paremtas dirbtinio intelekto mašininiu mokymu (AI-ML), elemento, jis gali neatitikti rekomendacijų sąrašo kriterijų arba, jam nepakanka pirkimo operacijų, kad būtų rodomas rekomendacijų sąraše.

Rekomenduojame patikrinkite, ar atlikti šie veiksmai:
1. **Įsitikinkite, ar produkto rekomendacijos buvo įjungtos BŪSTINĖJE.** Daugiau informacijos apie tai, kaip įgalinti šią paslaugą, ieškokite [Produkto rekomendacijų įgalinimas](enable-product-recommendations.md).
1. **Įsitikinkite, kad yra nustatytos pagrindinės produkto ypatybės.** Pavyzdžiui, produktų asortimentai turi būti nustatyti taip, kad **įtrauktų**.
1. **Dėl naujai atrinktų produktų procesas gali užtrukti iki 3 valandų, kol produktas pradės būti rodomas naujame sąraše.**
1. **Jei produktas vis dar nerodomas sąrašuose Populiaru, Perkamiausi, Žmonėms taip pat patiko ar Dažnai kartu perkama, tada šiam produktui nepakanka operacijų.** Tokiu atveju galite palaukti, kol atsiras daugiau operacijų, naujinti numatytuosius rekomendacijų sąrašo parametrus arba naudoti rankinį įsikišimą, kad galėtumėte modifikuoti rekomenduojamų produktų sąrašo rezultatus. Daugiau informacijos apie rekomendacijų parametrus žr. [AI-ML pagrįstų produktų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).
1. **Įsitikinkite, kad produktas atitinka rekomendacijų sąrašo kriterijus**. Daugiau informacijos apie produktų rekomendacijų parametrus žr. [AI-ML pagrįstų produktų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a>Kaip išvengti prastų rekomendavimo rezultatų generavimo?

Rekomendacijų sąrašams reikalingas didelis operacijų kiekis, kad būtų gaunami rezultatai. Todėl svarbu, kad vartotojai pateiktų visus retrospektyvius operacijų duomenis.

Be to, produktai, kurie neturi operacijų ar kelių operacijų, paprastai nėra tarp **Žmonėms taip pat patiko** ar **Dažnai kartu perkama** rezultatų, tad nėra rodomi rekomendacijų sąrašuose **Populiaru** ir **Perkamiausi**. Ši situacija dažnai gali kilti dėl labai naujų produktų arba senų produktų, kurių pirkimų skaičius yra mažas. Populiarioms naujos prekėms ši problema greitai išnyksta.

Rekomenduojame atlikti šiuos veiksmus:
1. **Įsitikinkite, kad produktas atitinka to rekomendacijų sąrašo kriterijus**. Daugiau informacijos apie produktų rekomendacijų parametrus žr. AI-ML pagrįstų produktų rekomendacijų rezultatų modifikavimas.
1. **Jei produktas yra naujas, apsvarstykite galimybę modifikuoti rekomendacijų sąrašą, kol produktas turės daugiau operacijų.** Daugiau informacijos apie tai, kaip modifikuoti rekomendacijų sąrašo rezultatus, žr. [AI-ML pagrįstų produktų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).


- **Įsitikinkite, kad produktas atitinka to rekomendacijų sąrašo kriterijus**. Daugiau informacijos apie produktų rekomendacijų parametrus žr. [AI-ML pagrįstų produktų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).
- **Jei produktas yra naujas, apsvarstykite galimybę modifikuoti rekomendacijų sąrašą, kol produktas turės daugiau operacijų.** Daugiau informacijos apie tai, kaip modifikuoti rekomendacijų sąrašo rezultatus, žr. [AI-ML pagrįstų produktų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a>Ar galiu pašalinti produktą, bet jį vis dar matys parduotuvėje?

Galite pakoreguoti sąrašus, kurie yra algoritmiškai sugeneruoti, jei atsiranda verslo poreikis. Tačiau, jei produktas pašalinamas iš rekomendacijų sąrašo, produktas bus aptinkamas parduotuvėje. Daugiau informacijos apie tai, kaip modifikuoti produktų rekomendacijų rezultatus, žr. [AI-ML pagrįstų produktų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).

Jei turite užblokuoti prekę, kuri bus aptikta parduotuvėje, turite pakeisti reikšmę **prekių asortimentai** į **Neįtraukti**.

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a>Kaip pridėti sąrašą prie el. prekybos puslapio?

Norėdami gauti informacijos apie tai, kaip įtraukti produkto rekomendacijų puslapius į savo el. prekybos svetainę, žr. [Produktų rekomendacijų sąrašų įtraukimas į puslapius](./product-recommendations.md).

## <a name="how-do-i-enable-recommendations-on-pos"></a>Kaip įjungti EKA rekomendacijas?

Įjungus produkto rekomendacijas, prie valdiklio EKA ekrano reikės pridėti rekomendacijų skydelį. Daugiau informacijos rasite [Rekomendacijų valdiklio įtraukimas į EKA įrenginių operacijų ekraną](add-recommendations-control-pos-screen.md).

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

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[Rekomendacijų su demonstraciniais duomenimis kūrimas](product-recommendations-demo-data.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]