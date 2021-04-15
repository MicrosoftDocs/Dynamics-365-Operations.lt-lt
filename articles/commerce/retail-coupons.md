---
title: Mažmeninės prekybos pardavimo kuponų nustatymas
description: Šioje temoje apžvelgiami kuponai ir paaiškinama, kaip juos nustatyti.
author: scott-tucker
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 9d8b9977d733c87566249bcb9658b80c4350c17d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792030"
---
# <a name="set-up-coupons-for-retail-sales"></a>Mažmeninės prekybos pardavimo kuponų nustatymas

[!include [banner](includes/banner.md)]

## <a name="overview-of-coupons"></a>Kuponų apžvalga

Kuponai yra kodai ir brūkšniniai kodai, naudojami suteikti nuolaidą. Kiekviename kupone gali būti keli kodai ir kiekvienas kodas gali turėti savo galiojimo datą.

Kiekviename kupone yra viena nuolaida. Su nuolaida susietos kainų grupės apibrėžia klientus, galinčius naudoti kuponą, arba kanalus, kuriuose kuponas galioja.

Iš esmės kuponai suteikia papildomą nuolaidą. Kupone pateikiami reikiami įprasti ir brūkšniniai kodai bei jų datų intervalai. Kupone taip pat pateikiamos pasirenkamos naudojimo ribos ir klientų reikalaujamos ypatybės. Nuolaida nurodo produktus, kuriems galioja kuponas. Nuolaidos kainų grupės nurodo klientus, kanalus ar katalogus, kuriems galioja kuponas.

Norint sukurti kuponą, atskirai sukuriami nuolaida ir kuponas. Tada jie susiejami pasirinkus nuolaidą kupono puslapyje „Commerce“.

> [!NOTE]
> Susiejus kuponą su nuolaida, keli nuolaidos puslapyje „Commerce“ esantys laukai tampa tik skaitomais, nes jie priklauso nuo kupono nustatymų. Šie laukai apima būsenos ir standartinių datų intervalų laukus.

### <a name="limited-use-coupons"></a>Riboto naudojimo kuponai

Kuponus galima sukonfigūruoti kaip riboto naudojimo. Naudojimo limitą galima apibrėžti vienam klientui ar kanalui arba kaip visuotinį limitą. Šis limitas taikomas įprastą ar brūkšninį kodą įvedant ar nuskaitant elektroniniame kasos aparate arba įvedant pardavimo užsakymą.

Limitas taikomas vienam kupono kodui. Pavyzdžiui, vienkartinį kuponą su dviem kodais galima naudoti du kartus: kiekvieną kupono kodą po kartą. Kiekvieną kupono kodą galima nepriklausomai nustatyti kaip aktyvų.

Kuponai gali būti naudojami bet kuriame pardavimo kanale, tačiau, skambučių centro užsakymams, riboto naudojimo kuponus galima naudoti tik tiems skambučių centrų užsakymams, kuriuose įjungtas skambučių centro parametras **Užsakymo užbaigimas**. Jei neįjungta, tai tada ne tik neriboto naudojimo tipo kuponai gali būti naudojami skambučių centro užsakymuose.

> [!NOTE]
> Panaudojus kupono kodą visus galimus kartus, sistemą automatiškai *nepakeičia* kupono kodo būsenos į „Panaudotas“. Tačiau kupono kodas jau panaudotas visus galimus kartus ir negali būti panaudotas dar kartą. Jei rankiniu būdu nustatoma kita kupono kodo būsena, išskyrus **Aktyvus**, tada šio kupono kodo negalima naudoti jokiame kanale.  

## <a name="managing-coupons"></a>Kuponų valdymas

Nuolaidą ir kuponą turite sukurti atskirai. Tada jie susiejami kuponų puslapyje pasirenkant nuolaidą. Kuponą susiejus su nuolaida, keli nuolaidos laukai tampa galimi tik skaityti, nes juos valdo kupono parametrai. Šie laukai apima būsenos ir standartinių datų intervalų laukus.

Iš esmės kuponai dabar suteikia papildomą nuolaidą. Kupone pateikiami įprasti ir brūkšniniai kodai bei jų datų intervalai, naudojimo limitai ir kliento reikalaujama ypatybė. Nuolaida nurodo produktus, kuriems galioja kuponas. Nuolaidos kainų grupės nurodo klientus, kanalus ar katalogus, kuriems galioja kuponas.

## <a name="system-setup-for-coupons"></a>Kuponų sistemos sąranka

Nustatyti kuponą galite tik nustatę kupono brūkšninį kodą ir dvi kupono numeracijas.

1. Puslapyje **Skaičių sekos simboliai** sukurkite naują kupono kodo skaičių sekos simbolį. Galite pasirinkti bet kokį nepanaudotą simbolį.
2. Puslapyje **Brūkšninių kodų skaičių sekų sąranka** sukurkite naują brūkšninio kodo skaičių seką. Lauką **Tipas** nustatykite kaip **Kuponas**.
3. Puslapyje **Brūkšninių kodų sąranka** sukurkite naują brūkšninį kodą, kuris naudoja jūsų ką tik sukurtą brūkšninio kodo skaičių seką.
4. Puslapyje **Numeracijos** sukurkite dvi naujas numeracijas. Viena numeracija skirta kupono kodo ID, o kita – kupono numeriui. Kupono kodo ID yra unikalusis kiekvieno kupono kodo identifikatorius. Kupono numeris yra unikalusis kupono identifikatorius. Kiekviename kupone gali būti keli įprasti ir brūkšniniai kodai, suaktyvinantys kuponą.

    > [!NOTE]
    > Abiejų numeracijų lauką **Aprėptis** turite nustatyti kaip **Įmonė**. Daugeliu atvejų abi numeracijas turėtumėte generuoti automatiškai.

5. Puslapio **„Commerce“ parametrai** skirtuke **Brūkšniniai kodai** pasirinkite brūkšninį kodą, kurį sukūrėte anksčiau.
6. Puslapio **Bendri „Commerce“ parametrai** skirtuke **Skaičių sekos** pasirinkite skaičių sekas, kurias sukūrėte kupono numeriui ir kupono kodo ID.
7. Dabar galite atidaryti puslapį **Kuponai** ir kurti naujus kuponus.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Kas nutinka kuponus atnaujinus iš dalies

Kuponų funkcijos apima kelias atskiras funkcijas. „Commerce“ būstinė (angl. HQ) ir kanalas gali būti iš dalies atnaujinami pagal komponentus. Todėl svarbu suprasti, kas nutinka iš dalies atnaujinus visas kuponų funkcijas.

- **Būstinė yra iš dalies atnaujinama, tačiau „Commerce Scale Unit“ ir EKA nėra atnaujinami.** Atnaujinant būstinę, atnaujinami kuponų ir nuolaidų puslapiai, taip pat atnaujinamas „Commerce“ kainų mechanizmas. Jei atnaujinamas tik vienas iš šių dviejų komponentų, kai kurie „Commerce“ puslapiai neatitiks kainos apskaičiavimo duomenų. Todėl skaičiuojant nuolaidas galima gauti netikėtų rezultatų arba gali įvykti klaidų.
- **Būstinė yra iš dalies atnaujinama, tačiau „Commerce Scale Unit“ ir EKA nėra atnaujinami (N-1).** Kadangi ne visas parduotuves galima atnaujinti tuo pačiu metu, prieš atnaujindami parduotuves rekomenduojame atnaujinti būstinę. Scenarijuje N-1 naujų su kuponais susijusių funkcijų nebus galima naudoti dar neatnaujintose parduotuvėse. Pavyzdžiui, kuponų funkcijos pradeda naudoti „neįtraukimo“ eilutes. Jei naudodami nuolaidą pašalinsite eilutes, jos nebus pritaikytos parduotuvėje, kurioje veikia senesnė versija.
- **Būstinė nėra atnaujinama, tačiau „Commerce Scale Unit“ ir EKA yra atnaujinami (N+1).** Kadangi atnaujintas „Commerce Scale Unit“ kainų mechanizmas gali apskaičiuoti kainą seniems nuolaidų kodams, atnaujinimas tam neturėtų daryti jokios įtakos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]