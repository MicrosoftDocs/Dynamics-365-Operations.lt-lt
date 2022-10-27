---
title: Kuponai
description: Šiame straipsnyje pateikta su kuponu susijusių pajėgumų apžvalga Microsoft Dynamics 365 Commerce.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-30
ms.openlocfilehash: 20427a04a552ddec013daa6576ec64ab7046e95f
ms.sourcegitcommit: 87e75aa6af2c3280316d7d73eafa14a52353a5e4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/21/2022
ms.locfileid: "9709765"
---
# <a name="coupons"></a>Kuponai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikta su kuponu susijusių pajėgumų apžvalga Microsoft Dynamics 365 Commerce.

Kuponai yra kodai ir brūkšniniai kodai, naudojami suteikti nuolaidą. Mažmenininkai paskirsto kuponus galimiems arba esamiems klientams, kad jie galėtų pagerinti prekės ženklo atpažinimą, konvertavimo vairą, išlaikyti savo klientų bazę, padidinti pardavimą ir galiausiai padidinti įplaukas. Kuponai tapo vienu iš populiariausių rinkodaros įrankių ir yra nauja el. komercijos pardavimo norma.

Be Dynamics 365 Commerce to, kuponai yra susieti su nuolaidomis ir laikomi papildomais patikrinti. Kiekvienas kuponas yra susijęs su viena nuolaida, o susieta nuolaida nurodo produktų rinkinį, kuriems galioja kuponas.

Kainų grupės, susietos su nuolaida, apibrėžia tinkamas sąlygas, kurioms galima naudoti kuponą. Šios sąlygos apima klientų grupes ir pardavimo kanalus. Kuponai taip pat suteikia naudojimo **limitą ir** reikalaujamas **kliento ypatybes**, kurias galima naudoti norint konfigūruoti pasirinktinius naudojimo apribojimus.

Kiekvienas kuponas gali turėti keletą kuponų kodų ir kuponų brūkšninių kodų, ir kiekvienas kodas gali turėti savo galiojimo datų diapazoną ir būseną. Jei nustatyta kodo būsena **Neaktyvus**, kodo negalima naudoti bet kuriame kanale.

## <a name="set-up-a-coupon"></a>Nustatyti kuponą

Nustatyti kuponą galite tik nustatę kupono brūkšninį kodą ir dvi kupono numeracijas.

Norėdami nustatyti kuponą "Commerce Headquarters", atlikite šiuos veiksmus.

1. Eikite į " **Retail" ir "Commerce \> Inventor Management" brūkšninius \> kodus ir žymės skaičių \> sekos simbolius**.
1. Norėdami **sukurti** kupono kodo tipo skaičių sekos simbolį **, pasirinkite** Įtraukti. Simbolių **lauke** galite pasirinkti bet kurį nenaudojamą simbolį.
1. Eikite į " **Retail" ir "Commerce \> Inventory" valdymo brūkšninius \> kodus ir etiketes Brūkšninio \> kodo skaičių sekos nustatymas**.
1. Pasirinkite **Nauja,** jei norite sukurti kupono tipo brūkšninio kodo **skaičių juostą**.
1. Eikite į **"Retail" ir "Commerce \> Inventory" valdymo brūkšninius \> kodus ir etiketes \> Brūkšninių kodų nustatymas**.
1. Pasirinkite **Naujas**, norėdami sukurti brūkšninią kodą, kuris naudoja jūsų sukurtą brūkšninio kodo skaičių skaičių juostą.
1. Eiti į **organizacijos administravimo \> numeracijas**.
1. Sukurkite dvi numeracijas:

    1. Viena kupono numerio **nuorodos** seka. Ši seka nurodo unikalų kupono identifikatorių.
    1. Viena kupono kodo **ID nuorodos** seka. Ši seka nurodo unikalų kiekvieno kupono kodo identifikatorių.

    Abiejų numeracijų lauką **Aprėptis** turite nustatyti kaip **Įmonė**. Daugeliu atvejų abu eilės numeriai turi būti generuojami automatiškai.

1. Eikite **į "Commerce" \> parametrus Kainos ir \> nuolaidų kuponai**.
1. Nustatykite **anksčiau sukurto brūkšninio** kodo skaičių sekos lauką Kupono brūkšninis kodas.
1. Eiti į **"Commerce" \> parametrų numeracijas**.
1. Pasirinkite numeracijas, kurias sukūrėte anksčiau kupono numerio ir **kupono** **kodo ID nuorodoms**.

Norėdami nustatyti kuponą, turite sukurti nuolaidą ir kuponą atskirai, **tada** susieti juos pasirinkdami nuolaidą kupono konfigūracijos lauke Nuolaida. Kai kuponas yra susietas su nuolaida, **·** **susietos** nuolaidos laukai Būsena, **Galiojimo** data ir Galiojimo data tampa tik skaitomi, nes vertės nustatomos pagal kupono būseną ir galiojimo laikotarpį. Kai kupono būsena nustatyta kaip **Aktyvus**, susietos nuolaidos būsena automatiškai atnaujinama į **Įjungta**. Taip pat, kai kupono **būsena nustatyta kaip Neaktyvus**, susietos nuolaidos būsena automatiškai atnaujinama į **Išjungta**.

## <a name="use-a-coupon"></a>Naudoti kuponą

Norėdami įtraukti kuponą į pardavimo operaciją "Commerce Point of Sale (POS)", galite naudoti kupono kodą arba kupono juostinį kodą. Norėdami naudoti kupono kodą, pasirinkite operaciją **Įtraukti kupono** kodą, tada įveskite kodą. Norėdami naudoti kupono brūkšninius kodus galite nuskaityti brūkšninius kodus naudodami nuskaitytą įrenginį arba įvesti jį naudodami skaitinę klaviatūrą operacijų **ekrane**.

Mažmenininkai kartais nori, kad kasininkai galėtų klientams suteikti fiksuotos sumos nuolaidas dėl produkto defektų arba dėl produkto defektų, bet jie nenori spausdinti kupono kodų ir juos paskirstyti kasininkams. Šiuo atveju galite nustatyti parinktį Taikyti **be kupono kodo**, kad kuponas būtų **Taip**. EKA kasininkas gali naudoti kupono funkciją Peržiūrėti galimas **nuolaidas** **·**, kad įtrauktų kuponą į operaciją neįvesdami kodo rankiniu būdu. Jei kuponui yra keli kupono kodai, sistema automatiškai pasirenka pirmą aktyvų kodą ir jį taiko operacijai.

Norėdami įtraukti kuponą į skambučių centro pardavimo užsakymą, **·** **skambučių** centro vartotojas turi pasirinkti kuponus pardavimo užsakymo puslapio skirtuke Valdymas.

Norėdami įtraukti kuponą į el. komercijos užsakymą, **pirkėjas gali įvesti kupono kodą pirkimo krepšelio nuolaidos** kodo lauke.

Kai kuponas įtraukiamas į pardavimo užsakymą, kainodaros sistema iškart suaktyvina viso užsakymo perskaičiavimą, neatsižvelgiant į tai, ar įgalintas atidėtas skaičiavimas.

> [!NOTE]
> Commerce 10.0.30 ir ankstesnėje versijoje, kai skambučių centro vartotojai įtraukia kuponą į skambučių centro pardavimo užsakymą, **·** **·** **jie** turi pasirinkti Perskaičiuoti grupės dalyje Skaičiavimas, veiksmų srities skirtuke Pardavimas, kad būtų taikoma su tuo kuponu susijusi nuolaida.

## <a name="coupon-usage-limit"></a>Kupono naudojimo riba

Kuponus galima konfigūruoti, kad juos būtų galima naudoti ribotą naudojimą. Naudojimo limitas gali būti nustatytas klientui, kanalui arba visuotinai. Naudojimo limitas galioja kupono kodui. Pavyzdžiui, vienkartinis kuponas, kuriame yra du kuponų kodai, gali būti naudojamas du kartus, vieną kartą kiekvienam kupono kodui.

Kuponus galima naudoti pardavimo kanaluose. Tačiau skambučių centro atveju, riboto naudojimo kuponus galima taikyti tik tada, kai įgalintas skambučių centro kanalo užsakymo baigimo parametras **Įgalinti**. Jei parametras **Įgalinti užsakymo** baigimą išjungtas, galima taikyti tik neriboto naudojimo kuponus.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
