---
title: Krepšelio ir pirkimo užbaigimo puslapių apžvalga
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ krepšelio valdymo puslapių apžvalga.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a574494784e9a534307cceff584e047d870dc401
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027944"
---
# <a name="cart-and-checkout-pages-overview"></a>Krepšelio ir pirkimo užbaigimo puslapių apžvalga

[!include [banner](includes/banner.md)]

Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ krepšelio valdymo puslapių apžvalga.

El. prekybos svetainės krepšelio puslapyje pateikiamos visos prekės, kurias klientas įtraukė į krepšelį. Krepšelio puslapis sukurtas naudojant krepšelio modulį. Krepšelio modulis yra konteineris, kuris turi visus modulius, kurių reikia norint rodyti krepšelio elementus. Be to, krepšelio modulyje galima naudoti ir kitus modulius rodyti užsakymo suvestinę ir visus reklaminius kodus, kurie buvo taikomi kliento užsakymui.

El. prekybos svetainės pirkimo užbaigimo puslapyje pateikiamas nuoseklus srautas, kurio klientai laikosi, kad įvestų visą informaciją, reikalingą užsakymui pateikti. Pirkimo užbaigimo modulyje gali būti modulių, tvarkančių siuntimo adresą, siuntimo būdus, atsiskaitymo informaciją, užsakymo suvestinę ir kitą su kliento užsakymais susijusią informaciją.

## <a name="cart-page"></a>Krepšelio puslapis

Krepšelio puslapis naudojamas kaip pirkinių krepšelis ir apima visas prekes, kurios buvo įdėtos į krepšelį.

Toliau pateiktame paveikslėlyje parodytas krepšelio puslapio pavyzdys, kuris buvo sukurtas naudojant modulių biblioteką ir „Fabrikam“ temą.

![Krepšelio puslapio pavyzdys](./media/cart2.PNG)

Pagrindinėje krepšelio puslapio struktūroje pateikiamos visos prekės, kurias klientas įdėjo į krepšelį. Yra pademonstruotos visos taikomos nuolaidos. Šios nuolaidos apima sudėtines nuolaidas. Pavyzdžiui, „Pirkite 3 prekes ir gaukite 10% nuolaidą“ arba „įsigykite buteliuką ir kuprinę ir gaukite 10% nuolaidą.“ Užsakymo suvestinės modulyje rodoma suma, mokėtina pritaikius nuolaidas, su siuntimo išlaidomis, mokesčiais ir t. t. Taip pat yra reklaminio kodo modulis, kuris leidžia klientui taikyti arba pašalinti reklaminius kodus.

Klientas gali apsipirkti anonimiškai arba kaip prisiregistravęs vartotojas. Jei klientas prisiregistravęs, krepšelio elementai išsaugomi tarp seansų. Tokiu būdu klientas gali toliau apsipirkti iš kelių įrenginių.

Iš krepšelio klientas gali pereiti prie pirkimo užbaigimo. Klientas gali pradėti pirkimo užbaigimą kaip svečio vartotojas arba kaip prisiregistravęs vartotojas.

Informacijos apie tai, kaip kurti krepšelio puslapį, žr. [Krepšelio modulio pridėjimas prie puslapio](add-cart-module.md).

## <a name="checkout-page"></a>Pirkimo užbaigimo puslapis

Pirkimo užbaigimo puslapis yra vieta, kurioje klientai įveda informaciją, reikalingą užsakymui pateikti.

Toliau pateiktame paveikslėlyje parodytas pirkimo užbaigimo puslapio pavyzdys, kuris buvo sukurtas naudojant modulių biblioteką.

![Pirkimo užbaigimo puslapio pavyzdys](./media/Checkout.PNG)

Pagrindinė pirkimo užbaigimo puslapio struktūra yra vieta, kur renkama visa užsakymo informacija. Ši informacija apima siuntimo adresą, pristatymo pasirinktis ir informaciją apie mokėjimą. Užbaigti pirkimą atliekamas nuoseklus srautas, nes informacija turi būti įvesta tam tikra apdorota tvarka. Pavyzdžiui, siuntimo adresą reikia įvesti prieš apskaičiuojant siuntimo išlaidas ir patvirtinant mokėjimą.

### <a name="shipping-address"></a>Siuntimo adresas

Siuntimo adresas yra būtinas, jei prekės turi būti išsiųstos. Galima konfigūruoti kiekvienos lokalės siuntimo adresų formatą sprendime „Dynamics 365 Commerce“. Pavyzdžiui, jei prekės bus išsiųstos į Jungtines Amerikos Valstijas, siuntimo adrese turi būti gatvės adresas, valstija ir pašto indeksas. Siuntimo adreso laukams atliekamas tam tikras pagrindinis įvesties patvirtinimas, pvz., tikrinami raidiniai ir skaitmenų simboliai, maksimalus ilgis ir numeriai. Nors pats adreso galiojimas nepatvirtintas, šį tikrinimą galima atlikti naudojant pritaikytas trečiosios šalies tarnybas.

Siuntimo adresas taikomas visoms krepšelio prekėms, kurių parinkta parinktis Siųsti. Jei naudojate pirkimo užbaigimo srautą, kuris pateikiamas modulių bibliotekoje, atskiros krepšelio prekės negali būti išsiųstos į skirtingus adresus. Jei norite, kad ši funkcija būtų galima, ji gali būti įgyvendinta naudojant pirkimo užbaigimo modulių tinkinimą.

Kai pateikiamas siuntimo adresas, bus rodomi siuntimo būdai, galimi „Dynamics 365 Commerce“ internetinėje parduotuvėje. Siuntimo būdus ir adresus, kuriuos jie palaiko, galima sukonfigūruoti „Commerce“.

### <a name="payment"></a>Mokėjimas

Kitas pirkimo užbaigimo srauto veiksmas – mokėjimas. El. prekyboje gali būti naudojami keli mokėjimo būdai, pvz., kredito kortelės, dovanų kortelės ir lojalumo taškai, užsakymams pateikti. Taip pat galima naudoti šių mokėjimo metodų derinį. Atsižvelgiant į naudojamus mokėjimo būdus, gali būti reikalinga papildoma informacija. Pavyzdžiui, atliekant mokėjimą kreditine kortele reikia nurodyti sąskaitų siuntimo adresą. Mokėjimai kredito kortele apdorojami naudojant „Adyen“ mokėjimo jungtį.

#### <a name="loyalty-points"></a>Lojalumo taškai

Atliekant pirkimo užbaigimo seką, klientas, kuris yra lojalumo programos narys ir sukaupęs lojalumo taškų, gali užsakyme išpirkti šiuos lojalumo taškus. Lojalumo taškų modulis rodomas tik tada, kai klientas turi esamą lojalumo narystę. Ne nariams ir svečių vartotojams šis modulis nerodomas.

#### <a name="gift-cards"></a>Dovanų kortelės

Modulių biblioteka leidžia užsakyme vidines dovanų korteles išpirkti. Norint taikyti vidinę dovanų kortelę, klientas turi būti prisijungęs. Siekiant užtikrinti papildomą saugą, rekomenduojame tinkinti eigą, naudojant asmeninį identifikavimo numerį (PIN) vidinėms dovanų kortelėms.

### <a name="signed-in-and-guest-users"></a>Prisijungę ir svečių vartotojai

Klientas gali atlikti pirkimo užbaigimo procesą kaip svečių vartotojas arba kaip prisiregistravęs vartotojas. Jei klientas prisijungia, paskyros informacija, pvz., išsaugoti siuntimo adresai ir įrašyta kredito kortelės informacija, automatiškai nuskaitoma.

### <a name="order-summary"></a>Užsakymo suvestinė

Pirkimo užbaigime pateikiama krepšelio eilutės elementų suvestinė, kad klientas galėtų patvirtinti užsakymą prieš pateikdamas užsakymą. Eilučių elementų negalima redaguoti atliekant pirkimo užbaigimo seką. Tačiau, jei vartotojas nori grįžti ir redaguoti eilutės elementus, bus pateiktas saitas į krepšelį.

Po to, kai klientas pateikia siuntimo ir sąskaitos pateikimo informaciją, užsakymų suvestinė nurodo sumą, mokėtiną po lojalumo taškų, dovanų kortelių ir kitų mokėjimų.

### <a name="order-confirmation-and-email"></a>Užsakymo patvirtinimas ir el. laiškas

Kai klientas pateikia užsakymą, pateikiamas patvirtinimo numeris. Taigi, mokėjimas buvo įgaliotas, bet nebuvo atsiskaityta. Mokėjimu bus atsiskaityta tik tada, kai užsakymas įvykdomas (t. y., kai jis pristatomas arba paimamas).

Sukūrus užsakymą, klientui siunčiamas užsakymo patvirtinimo el. laiškas.

Daugiau informacijos apie tai, kaip kurti pirkimo užbaigimo puslapį, žr. [Pirkimo užbaigimo modulio pridėjimas prie puslapio](add-checkout-module.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Pagrindinio puslapio apžvalga](quick-tour-home-page.md)

[Išsamios informacijos apie produktus puslapių apžvalga](quick-tour-pdp.md)

[Paskyrų tvarkymo puslapių apžvalga](quick-tour-account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
