---
title: Mažmeninės prekybos pardavimo kuponų nustatymas
description: Šioje temoje apžvelgiami mažmeninės prekybos kuponai ir paaiškinama, kaip juos nustatyti.
author: scott-tucker
manager: AnnBe
ms.date: 05/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: bd3596b6c78c5959ca289c73bcc5785eb770be39
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553558"
---
# <a name="set-up-coupons-for-retail-sales"></a>Mažmeninės prekybos pardavimo kuponų nustatymas

[!include [banner](includes/banner.md)]

## <a name="overview-of-coupons"></a>Kuponų apžvalga

Kuponai yra įprasti ir brūkšniniai kodai, kuriuos naudojant į operacijas įtraukiamos mažmeninės prekybos nuolaidos. Kiekviename kupone gali būti keli kodai ir kiekvienas kodas gali turėti savo galiojimo datą.

Kiekvienas kuponas yra susijęs su viena mažmeninės prekybos nuolaida. Su nuolaida susietos kainų grupės apibrėžia klientus, galinčius naudoti kuponą, arba kanalus, kuriuose kuponas galioja.

Iš esmės kuponai yra papildoma patikra prie mažmeninės prekybos nuolaidų. Kupone pateikiami reikiami įprasti ir brūkšniniai kodai bei jų datų intervalai. Kupone taip pat pateikiamos pasirenkamos naudojimo ribos ir klientų reikalaujamos ypatybės. Nuolaida nurodo produktus, kuriems galioja kuponas. Nuolaidos kainų grupės nurodo klientus, kanalus ar katalogus, kuriems galioja kuponas.

Norint sukurti kuponą, atskirai sukuriami nuolaida ir kuponas. Tada jie susiejami pasirenkant nuolaidą „Microsoft Dynamics 365 for Retail“ kuponų puslapyje.

> [!NOTE]
> Kuponą susiejus su nuolaida, keli „Microsoft Dynamics 365 for Retail“ nuolaidų puslapio laukai tampa galimi tik skaityti, nes juos valdo kupono parametrai. Šie laukai apima būsenos ir standartinių datų intervalų laukus.

### <a name="limited-use-coupons"></a>Riboto naudojimo kuponai

Kuponus galima sukonfigūruoti kaip riboto naudojimo. Naudojimo limitą galima apibrėžti vienam klientui ar kanalui arba kaip visuotinį limitą. Šis limitas taikomas įprastą ar brūkšninį kodą įvedant ar nuskaitant elektroniniame kasos aparate arba įvedant pardavimo užsakymą.

Limitas taikomas vienam kupono kodui. Pavyzdžiui, vienkartinį kuponą su dviem kodais galima naudoti du kartus: kiekvieną kupono kodą po kartą. Kiekvieną kupono kodą galima nepriklausomai nustatyti kaip aktyvų.

> [!NOTE]
> Kupono kodui pasiekus savo naudojimo limitą sistema automatiškai *nepakeičia* kupono kodo būsenos į „Panaudotas“. Tačiau sistema neleidžia toliau naudotis kuponu jam pasiekus naudojimo limitą. Jei neautomatiškai nustatoma kita kupono kodo būsena išskyrus „Aktyvus“, šio kupono kodo negalima naudoti jokiame kanale.

## <a name="managing-coupons"></a>Kuponų valdymas

Nuolaidą ir kuponą turite sukurti atskirai. Tada jie susiejami kuponų puslapyje pasirenkant nuolaidą. Kuponą susiejus su nuolaida, keli nuolaidos laukai tampa galimi tik skaityti, nes juos valdo kupono parametrai. Šie laukai apima būsenos ir standartinių datų intervalų laukus.

Iš esmės kuponai dabar yra papildoma patikra prie mažmeninės prekybos nuolaidų. Kupone pateikiami įprasti ir brūkšniniai kodai bei jų datų intervalai, naudojimo limitai ir kliento reikalaujama ypatybė. Nuolaida nurodo produktus, kuriems galioja kuponas. Nuolaidos kainų grupės nurodo klientus, kanalus ar katalogus, kuriems galioja kuponas.

## <a name="system-setup-for-coupons"></a>Kuponų sistemos sąranka

Nustatyti kuponą galite tik nustatę kupono brūkšninį kodą ir dvi kupono numeracijas.

1. Puslapyje **Skaičių sekos simboliai** sukurkite naują kupono kodo skaičių sekos simbolį. Galite pasirinkti bet kokį nepanaudotą simbolį.
2. Puslapyje **Brūkšninių kodų skaičių sekų sąranka** sukurkite naują brūkšninio kodo skaičių seką. Lauką **Tipas** nustatykite kaip **Kuponas**.
3. Puslapyje **Brūkšninių kodų sąranka** sukurkite naują brūkšninį kodą, kuris naudoja jūsų ką tik sukurtą brūkšninio kodo skaičių seką.
4. Puslapyje **Numeracijos** sukurkite dvi naujas numeracijas. Viena numeracija skirta kupono kodo ID, o kita – kupono numeriui. Kupono kodo ID yra unikalusis kiekvieno kupono kodo identifikatorius. Kupono numeris yra unikalusis kupono identifikatorius. Kiekviename kupone gali būti keli įprasti ir brūkšniniai kodai, suaktyvinantys kuponą.

    > [!NOTE]
    > Abiejų numeracijų lauką **Aprėptis** turite nustatyti kaip **Įmonė**. Daugeliu atvejų abi numeracijas turėtumėte generuoti automatiškai.

5. Puslapio **Mažmeninės prekybos parametrai** skirtuke **Brūkšniniai kodai** pasirinkite savo anksčiau sukurtą brūkšninį kodą.
6. Puslapio **Bendrai naudojami mažmeninės prekybos parametrai** skirtuke **Numeracijos** pasirinkite sukurtas kupono numerio ir kupono kodo ID numeracijas.
7. Dabar galite atidaryti puslapį **Kuponai** ir kurti naujus kuponus.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Kas nutinka kuponus atnaujinus iš dalies

Kuponų funkcijos apima kelias atskiras „Dynamics 365 for Retail“ funkcijas. Galima iš dalies atnaujinti visus „Microsoft Dynamics 365 for Retail Headquarters (HQ)“ ir kanalo komponentus. Todėl svarbu suprasti, kas nutinka iš dalies atnaujinus visas kuponų funkcijas.

- **HQ atnaujinamas iš dalies, tačiau „Retail‟ serveris ir EKA neatnaujinami.** Naujinant HQ atnaujinami kuponų ir nuolaidų puslapiai bei mažmeninės prekybos kainų mechanizmas. Jei atnaujinamas tik vienas iš šių dviejų komponentų, kai kuriuose „Retail“ puslapiuose neatitiks kainų skaičiavimo duomenys. Todėl skaičiuojant nuolaidas galima gauti netikėtų rezultatų arba gali įvykti klaidų.
- **HQ atnaujinamas, tačiau „Retail‟ serveris ir EKA neatnaujinami (N-1).** Kadangi tuo pačiu metu galima atnaujinti ne visas mažmeninės prekybos parduotuves, rekomenduojame prieš naujinant jas atnaujinti HQ. Scenarijuje N-1 naujų su kuponais susijusių funkcijų nebus galima naudoti dar neatnaujintose parduotuvėse. Pavyzdžiui, kuponų funkcijos pradeda naudoti „neįtraukimo“ eilutes. Jei su nuolaida naudosite neįtraukimo eilutes, jos nebus taikomos mažmeninės prekybos parduotuvėje, kurioje veikia ankstesnė versija.
- **HQ neatnaujinamas, tačiau „Retail‟ serveris ir EKA atnaujinami (N+1).** Kadangi atnaujintas „Retail‟ serverio kainų mechanizmas gali naudoti senesnius nuolaidų kodus, šiame scenarijuje naujinimas funkcijoms įtakos turėti neturėtų.
