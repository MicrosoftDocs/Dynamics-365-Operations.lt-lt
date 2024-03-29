---
title: Grąžinimo savikaina ir grąžinamos partijos ID
description: Galite norėti, kad grąžintų produktų savikaina būtų lygi produktų savikainai tuo metu, kai šiuos produktus pardavėte klientui. Tai galite nustatyti naudodami **Grąžinamos partijos ID**.
author: sorenva
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnInventTransIdLookup, ReturnItemNumLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c1d236918eddf3203a544a6b047f8ccac777971
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017250"
---
# <a name="return-cost-price-and-return-lot-id"></a>Grąžinimo savikaina ir grąžinamos partijos ID        

[!include [banner](../includes/banner.md)]



Į atsargas grąžintų produktų savikaina skaičiuojama naudojant dabartinę šių produktų savikainą. Tačiau galite norėti, kad grąžintų produktų savikaina būtų lygi produktų savikainai tuo metu, kai šiuos produktus pardavėte klientui. Tai galite atlikti nustatyti formos **Pardavimo užsakymas** „FastTab“ skirtuko **Eilutės informacija** lauke **Grąžinamos partijos ID** .

Pvz., apsvarstykite toliau pateiktą scenarijų. Klientui nusiunčiate SF. Tada klientas jums grąžina pristatytus produktus. Jūs grąžinate produktus į atsargas. Tokiu atveju, kai kredituojate klientą už grąžintus produktus, šių produktų savikaina apskaičiuojama naudojant dabartinę savikainą. Tačiau, jei naudosite lauką **Grąžinamos partijos ID**, grąžintų produktų savikaina bus apskaičiuojama naudojant savikainą, nurodytą pradinio pardavimo klientui SF.

Jei norite naudoti kitą nei dabartinę kliento grąžintų produktų savikainą, naudokite vieną iš toliau nurodytų būdų.

## <a name="method-1-manually-enter-the-return-cost-price"></a>1 būdas: įveskite grąžinimo savikainą rankiniu būdu

Pagal numatytuosius nustatymus, kai įtraukiate prekes į grąžinimo užsakymą, šios prekės yra grąžinamos į atsargas nurodant dabartinę savikainą. Jei norite nurodyti kitą grąžinimo savikainą, atlikite toliau nurodytus veiksmus.

1.  Spustelėkite **Pardavimas ir rinkodaros pardavimas** \> **grąžina** \> **visus grąžinimo užsakymus**.

2.  Dalies **Veiksmų sritis** grupėje **Naujas** spustelėkite **Grąžinimo užsakymas**.

3.  Formoje **Kurti grąžinimo užsakymą** pasirinkite kliento sąskaitą ir tada spustelėkite **Gerai**.

4.  Formoje **Grąžinimo užsakymas – RMA numeris: %1, %2** pasirinkite prekę ir tada įveskite neigiamą kiekį lauke **Kiekis**.

5.  Spustelėkite „FastTab‟ skirtuką **Eilutės informacija**.

6.  Skirtuko **Bendra** lauke **Grąžinimo savikaina** įveskite vertę. Ši vertė naudojama, kai prekės grąžinamos į atsargas. Jei vertės neįvesite, grąžinant prekes į atsargas bus naudojama dabartinė savikaina.

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a>2 būdas: automatiškas savikainos generavimas pagal kliento SF eilutę

Tai prioritetinis grąžinimo eilučių kūrimo būdas. Norėdami naudoti produktų savikainą, kuri buvo tuo metu, kai šiuos produktus pardavėte klientui, sukurkite grąžinimo užsakymą ir nurodykite grąžintiną pardavimo eilutę.

1.  Spustelėkite **Pardavimas ir rinkodaros pardavimas** \> **grąžina** \> **visus grąžinimo užsakymus**.

2.  Dalies **Veiksmų sritis** grupėje **Naujas** spustelėkite **Grąžinimo užsakymas**.

3.  Formoje **Kurti grąžinimo užsakymą** pasirinkite kliento sąskaitą ir tada spustelėkite **Gerai**.

4.  Formos **Grąžinimo užsakymas – RMA numeris: %1, %2** dalyje **Veiksmų sritis** spustelėkite **Rasti pardavimo užsakymą**.

5.  Formoje **Rasti pardavimo užsakymą** pasirinkite grąžintiną SF eilutę ir tada spustelėkite **Gerai**.
    
    „FastTab“ skirtuko **Eilutės informacija** skirtuko **Bendra** lauke **Grąžinamos partijos ID** rodoma vertė iš pradinio pardavimo eilutės. Be to, lauke **Grąžinimo savikaina** rodoma savikainos vertė iš pradinio pardavimo eilutės.

## <a name="cost-calculation-example"></a>Savikainos skaičiavimo pavyzdys

Kai grąžinimo savikainą nurodote grąžinimo užsakymo eilutės lauke **Grąžinamos partijos ID**, naudojama grąžinimo užsakymo eilutėje nurodyta savikaina. Įjungus atsargų uždarymo arba perskaičiavimo funkciją, pradinio pardavimo eilutėje nurodyta savikaina pakoreguojama. Grąžinimo užsakymo eilutėje nurodyta savikaina automatiškai pakoreguojama, kad atspindėtų tokią pačią vieneto savikainą.

1.  Sukurkite ir išleiskite produktą pavadinimu Testas. Formoje **Išleisto produkto informacija** nurodykite tokią informaciją:
    
    1.  „FastTab“ skirtuko **Tvarkyti savikainą** lauke **Prekių grupė** pasirinkite grupę **Dalys**.
    
    2.  „FastTab“ skirtuko **Bendra** lauke **Prekių modelių grupė** pasirinkite **DEF**.
    
    3.  „FastTab“ skirtuko **Pirkimas** lauke **Kaina** įveskite 10,00 kaip prekės savikainą.
    
    4.  Dalyje **Veiksmų sritis** spustelėkite **Dimensijų grupės**. Lauke **Saugojimo dimensijų grupė** pasirinkite **Tik vieta ir sandėlis**. Lauke **Sekimo dimensijų grupė** pasirinkite **Nėra aktyvių sekimo dimensijų**.

2.  Sukurkite pirkimo užsakymą 10 testinės prekės vienetų po 6,00 už vienetą, tada užregistruokite pirkimo užsakymo SF.
    
    Sukurkite antrą pirkimo užsakymą 10 testinės prekės vienetų po 8,00 už vienetą, tada užregistruokite pirkimo užsakymo SF.

3.  Užregistruokite SF pardavimo užsakymui parduoti penkis testinės prekės vienetus.
    
    Šiuo atveju pardavimo užsakymo eilutė bus įkainota 35,00 (5 vienetai \* 7,00 vidutinė vieneto savikaina).

4.  Sukurkite grąžinimo užsakymą klientui. Formoje **Rasti pardavimo užsakymą** pasirinkite SF eilutę ir tada spustelėkite **Gerai**.

5.  Formoje **Grąžinimo užsakymas – RMA numeris: %1, %2** patikrinkite, ar bandomosios prekės grąžinimo užsakymas yra sugeneruotas. Grąžinimo užsakymo kiekis nustatomas kaip -5,00.
    
    Lauke **Grąžinamos partijos ID** rodomas partijos ID. Šis partijos ID paimamas iš pradinio klientui parduotos prekės pardavimo užsakymo. Lauke **Grąžinimo savikaina** rodoma savikaina iš pradinio pardavimo eilutės.

6.  Užregistruokite grąžintų prekių gavimą.

7.  Užregistruokite grąžintų prekių važtaraštį.

8.  Užregistruokite grąžinimo užsakymo SF. Sąrašo puslapyje **Visi pardavimo užsakymai** pasirinkite pardavimo užsakymą, kurio užsakymo tipas yra **Grąžintas užsakymas**.

9.  Atidarykite formą **Atsargų operacijos**. Patikrinkite, ar grąžinimas įkainotas 7,00 už vienetą, pagal lauke **Grąžinimo savikaina** nurodytą vertę – iš viso lauke **Savikainos suma** turi būti 35,00. Formą **Atsargų operacijos** galite atidaryti iš formos **Grąžinimo užsakymas – RMA numeris: %1, %2**. Tinklelyje **Eilutės** spustelėkite **Atsargos** \> **Operacijos**.

10. Atsargų ir sandėlio valdymo formoje **Uždarymas ir koregavimas** vykdykite procedūrą **3. Uždaryti**.
    
    Šis veiksmas pakoreguos pradinio pardavimo eilutėje nurodytą savikainą, iš -35,00 (5 vienetai \* 7,00) į -30,00 (5 vienetai \* 6,00). Taip yra todėl, kad atsargų modelių grupė naudoja „pirmas ateina, pirmas išeina“ (FIFO) metodą ir 6,00 už vienetą yra FIFO kaina iš pirmojo pirkimo užsakymo. Be to, šis veiksmas pakoreguoja savikainą grąžinimo pardavimo eilutėje, kad ji atitiktų vieneto savikainą pradinio pardavimo eilutėje. Todėl savikaina grąžinimo eilutėje pakoreguojama iš 35,00 į 30,00.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]