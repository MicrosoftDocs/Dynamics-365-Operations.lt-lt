---
title: Kaip nustatyti balansavimo finansines dimensijas?
description: Šioje temoje aprašomos pasirinktys, kaip nustatyti ir naudoti balansavimo finansinės dimensijos funkciją.
author: kweekley
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-08-17
ms.dyn365.ops.version: 10.0.210
ms.openlocfilehash: cb3033a615200a358c1b28b0991bae4b84470ae0
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/06/2022
ms.locfileid: "8720117"
---
# <a name="how-do-i-set-up-balancing-financial-dimensions"></a>Kaip nustatyti balansavimo finansines dimensijas?

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos pasirinktys, kaip nustatyti ir naudoti balansavimo finansinės dimensijos funkciją.

## <a name="symptom"></a>Požymis

Yra dvi balansavimo finansinių dimensijų nustatymo pasirinktys. Pirmoji parinktis yra naudoti **Balansuoti finansinės dimensijos** laukelį **DK** nustatymų puslapį (**DK \> DK nustatymai \> DK**). Antroji parinktis yra naudoti **Būtina balansuoti dimensija** laukelis puslapyje **Finansinė dimensija** (**DK > Sąskaitų grafikas \> Dimensijas \> Finansinės dimensijos**). Šioje temoje paaiškinamas skirtumas tarp šių dviejų pasirinkčių.

## <a name="resolution"></a>Sprendimas

Organizacijos paprastai balansavimo dimensijas naudoja balansui, balansui finansinės dimensijos lygiu, generuoti. Įgalinus bet kurią priemonę, užregistruotos, nesubalansuotos dimensijos nebus subalansuotos. Prieš įjungdami bet kurią priemonę, pirmiausia turite rankiniu būdu įvesti koregavimo įrašus, kad balanso balansas būtų su balansu.

Šios dvi galimybės nėra tarpusavyje nesuderinamos. Parinktis, kurią naudoja jūsų organizacija, turi būti pagrįsta jūsų verslo reikalavimais. Dažnai susiduriame su klientais, kurie DK nustatyme ir finansinės dimensijos nustatyme apibrėžia balansavimo dimensiją, ir kai kuriuos ar visus reikiamus papildomus nustatymus. Tačiau jų vis tiek negalima registruoti dėl finansinių dimensijų lygio disbalanso.

Toliau pateikiamame skyriuje aprašomos dvi pasirinktys ir paaiškinama, kaip jas nustatyti.

### <a name="ledger--balancing-financial-dimension"></a>DK – Balansavimo finansinė dimensija

Balansavimo dimensija **DK** nustatymo puslapyje naudojama norint įgalinti vienetų apskaitą. Atlikite šiuos veiksmus, kad įjungtumėte funkcijas.

1. Nustatykite, kuri finansinė dimensija bus balansavimo dimensija.

    - Naudodami šią funkciją kaip balansavimo dimensiją galite pasirinkti tik vieną finansinę dimensiją.
    - DK nustatymo puslapyje dimensijos dar **DK** nepasirinko.
    - Įsitikinkite, kad pasirinktos finansinės dimensijos balansas jau subalansuotas.

2. Atnaujinti balansavimo finansinės dimensijos sąskaitos struktūrą.

    - Finansinės dimensijos balansavimas turi būti įtrauktas į visas sąskaitos struktūras, kurios priskirtos DK.
    - Finansinė dimensija neturi leisti tuščių vietų sąskaitos struktūroje. Šis apribojimas užtikrina, kad kiekviename DK užregistruotame apskaitos įraše yra finansinės dimensijos vertė. Naudojant balansavimo dimensijas, tuščia dimensija yra netinkama.

3. Puslapyje **Sąskaitų automatinės operacijos** puslapyje (**DK \> Publikavimo nustatymai \> Sąskaitos automatinėms perlaidoms**), nustatykite tarpinė skola ir kredito pagrindinės sąskaitos.
4. Nustatymų puslapyje **DK** (**DK \> DK nustatymai \> DK**), laukelyje **Balansavimo finansinės dimensijos** rinkitės finansinę dimensiją, kurią naudosite balansuoti.

Jei pasirinkta finansinė dimensija nesubalansuojama, kai įvedamos ir registruojamos operacijos, sistema automatiškai įtrauks debeto arba kredito įrašus, reikalingus apskaitos įrašui subalansuoti registruojant. Visų vienetų operacijos debeto ir kredito DK sąskaitos rodomos registruotuose DK kvituose. Tačiau jie nebus rodomi žurnaluose arba šaltinio dokumentuose, kurių apskaitos įrašai buvo užregistruoti.

### <a name="financial-dimensions--require-the-dimension-to-be-balanced"></a>Finansinės dimensijos – reikia, kad dimensija būtų subalansuota

Nors balansavimo dimensiją finansinių dimensijų puslapyje paprastai naudoja viešojo sektoriaus įmonės, funkcija nėra susieta su jokio **viešojo sektoriaus** konfigūracijos raktu. Kadangi sistemoje nėra apribojimo, galite naudoti šią funkciją net jeigu jūsų organizacija nėra viešojo sektoriaus subjektas.

Ši funkcija paprastai naudojama viešojo sektoriaus klientų bazėje, kadangi joje reikalaujama, kad registravimo aprašai būtų naudojami, norint automatiškai subalansuoti kiekvieną operaciją. Ji naudoja tarpinių vienetų debeto ir kredito sąskaitas, kurios nustatytos automatinių operacijų puslapyje nustatytose sąskaitose, kad būtų **automatiškai subalansuoti apskaitos** įrašai. Jei pritaikius registravimo aprašus apskaitos įrašas nesubalansuotas dimensijos lygyje, operacija nebus užregistruota, net jei yra nustatytos tarpinių vienetų debeto ir kredito sąskaitos.

Dažnai susiduriame su klientais, kurie dk nustatyme ir finansinės dimensijos nustatyme apibrėžia balansavimo dimensiją. Šiuo atveju sistema naudoja finansinių dimensijų funkcijas. Balansavimo dimensijų nustatymas finansinės dimensijos lygiu, registruojant, yra svarbesnis. Registravimas nepavyks, jei registravimo aprašas nesukuria subalansuotų apskaitos įrašų finansinės dimensijos lygiu.

Norėdami įjungti balansavimo dimensijos naudojimą finansinės dimensijos lygiu, atlikite šiuos veiksmus.

1. Nustatykite, kuri finansinė dimensija bus balansavimo dimensija.

    - Kaip balansavimo dimensiją galite nustatyti daugiau nei vieną finansinę dimensiją.
    - Dar nenustatę finansinių dimensijų, kurių bus reikalaujama norint subalansuoti operaciją **finansinių dimensijų** puslapyje.

2. Nurodykite kiekvieno jūsų organizacijos naudojamus žurnalo ar šaltinio dokumento tipo registravimo aprašus. Publikavimo sąvokos sunaudoja DK sąskaitas iš nepublikuoto žurnalo ar ištekliaus dokumenti kaip „atitikties kriterijai“. Tada registravimo aprašas grąžina „sugeneruotus įrašus", kurie tampa apskaitos įrašu. Jei registravimo aprašas nustatytas teisingai, sugeneruotas įrašas apima gretės kriterijų DK sąskaitas ir papildomas sąskaitas, kad būtų galima subalansuoti apskaitos įrašą dimensijos lygiu. Daugiau informacijos ieškokite [Registravimo aprašų pavyzdžiai](posting-definitions.md). 
   
   Registravimo aprašai nepalaikomi kiekviename operacijos tipe. Pavyzdžiui, registravimo aprašų negalima nurodyti jokiai operacijai, įvestai per bendrąjį žurnalą arba ilgalaikio turto žurnalą. Jei žurnalo arba šaltinio dokumento registravimo aprašo nurodyti negalima, operacija turi būti subalansuoti rankiniu būdu pagal finansinės dimensijos vertę. Pavyzdžiui, jei atliktas bendrojo žurnalo įrašas, o padalinio dimensija yra balansavimo dimensija, turite užtikrinti, kad kiekviena padalinio vertė būtų balansinė.  Jei kiekvienos padalinio vertės dimensija nesubalansuojama, kvitas nebus registruotis, kol nebus ištaisytas disbalansas, rankiniu būdu į kvitą įtraukiant tarpinių vienetų debetą arba kreditą. 

    > [!IMPORTANT]
    > Jei perviršinis operacijų skaičius turi būti subalansuotas rankiniu būdu, jūs neturėdami **naudoti** balansavimo dimensijos funkcijos **puslapyje Finansinės** dimensijos. Vietoje to, naudokite balansavimo dimensijos funkciją **DK** nustatymo puslapyje.

3. Nustačius registravimo aprašus, finansinės dimensijos gali būti pažymėtos kaip reikalingos balansuoti.

Kai įvedate ir registruojate operacijas, registravimo aprašai iškvie rodomi registruojant, kad būtų nustatyti apskaitos įrašai. Jei finansinės dimensijos yra subalansuotos, patikrinimas įvyksta nustačius apskaitos įrašus. Jei finansinių dimensijų nesubalansuotas, operacija nebus registruojama, o jūs gausite pranešimą, kuriame teigiama, kad debetai nėra lygūs konkrečios dimensijos kreditams.
