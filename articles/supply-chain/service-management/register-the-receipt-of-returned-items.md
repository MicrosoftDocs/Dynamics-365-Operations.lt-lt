---
title: Grąžintų prekių gavimo registravimas
description: Galite užregistruoti grąžintų prekių gavimą naudodami gavimų apžvalgos formą arba registracijos formą.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8e1da5fee9607bf9f38c90d3db891ffa212ab01f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219298"
---
# <a name="register-the-receipt-of-returned-items"></a>Grąžintų prekių gavimo registravimas 

[!include [banner](../includes/banner.md)]


Grąžintų prekių gavimą galima registruoti dviem būdais. Pirmasis būdas yra sandėlio gavimo procesas, kuris naudoja formą **Gavimų apžvalga**. Antrasis naudoja formą **Registracija**.

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a>Grąžintų prekių gavimo registravimas naudojant formą Gavimų apžvalga

Galite naudoti formą **Gavimų apžvalga**, jei norite identifikuoti grąžinimo siuntą pagal jos grąžinamų medžiagų autorizavimo (RMA) numerį. Jei žurnalo pavadinimas nurodytas skirtuke **Nustatymas** ir yra žurnalo eilutės, kurios atitinka eilutes, pažymėtas formoje **Gavimų apžvalga**, nauja žurnalo antraštė yra sukuriama spustelėjus **Pradėti gavimo žurnalą**.

1.  Spustelėkite **Atsargų valdymas** \> **Laikotarpio** \> **Gavimų apžvalga**.

2.  Lauke **Nustatymo pavadinimas** pasirinkite **Grąžinimo užsakymas**, tada spustelėkite **Naujinti**.
    

    > [!TIP]
    > <P>Galite naudoti laukus <STRONG>Diapazonas</STRONG> norėdami susiaurinti paieškos rezultatus. Galite įrašyti ar pasirinkti RMA numerį lauke <STRONG>RMA numeris</STRONG>, jei norite tikslaus rezultato. Norėdami apibrėžti ir įrašyti rinkinį filtrų, kurie nustatys, kurie įeinantys gavimai bus rodomi, spustelėkite skirtuką <STRONG>Nustatymas</STRONG>. Galimi filtrai yra tipai, sandėliai ir rampos.</P>

    

    > [!WARNING]
    > <P>Grąžinimo užsakymų negalima maišyti su kitais gavimų tipais formoje <STRONG>Gavimų apžvalga</STRONG>. Todėl, nuoroda visada bus pardavimo užsakymas, bet pardavimo užsakymo ID nebus nurodyti žurnalo antraštėje.</P>



3.  Tinklelyje **Gavimai** raskite eilutę, atitinkančią grąžinamą prekę ir tada pasirinkite žymės langelį, esantį stulpelyje **Pasirinkti įtraukti į gavimą**.

4.  Jei norite pašalinti tam tikras eilutes iš grąžinimo gavimo, pavyzdžiui, prekes iš pradinio užsakymo, kurios nebuvo įtrauktos į grąžinimo siuntą, išvalykite susijusius žymės langelius **Pasirinkti įtraukti į gavimą** lentelėje **Eilutės**, esančioje apatinėje formos dalyje.

5.  Spustelėkite mygtuką **Pradėti gavimo žurnalą** norėdami sukurti gavimo žurnalą.
    

    > [!NOTE]
    > <P>Galite pasirinkti kelis grąžinimo užsakymus ir juos visus įtraukti į vieną gavimo procesą. Kiekviena grąžinimo užsakymo eilutė bus nukopijuotą į atitinkamą prekių gavimo žurnalo eilutę.</P>

    

    > [!NOTE]
    > <P>Taip pat galite rankiniu būdu sukurti gavimo žurnalą naudodami formą <STRONG>Prekių gavimo žurnalas</STRONG>. 



6.  Spustelėkite **Atsargų valdymas** \> **Žurnalai** \> **Prekių gavimas** \> **Prekių gavimas**.

7.  Pasirinkite gavimo žurnalą, kurį ką tik sukūrėte, ir tada spustelėkite **Eilutės**, kad atidarytumėte formą **Žurnalo eilutės, vietos**.

8.  Skirtuke **Bendra** pakoreguokite skaičių lauke **Kiekis** (jei reikia), tada priskirkite perdavimo kodą lauke **Perdavimo kodas**.
    
    Taip pat galite pasirinkti ir žymės langelį **Sulaikymo valdymas**, kad grąžinamos prekės būtų siunčiamos naudojant tikrinimo procesą pagal sulaikymo užsakymą.
    

    > [!NOTE]
    > <P>Jei siunčiate grąžinamas prekes per karantiną, jūs negalite nurodyti perdavimo kodo.</P>



9.  Spustelėkite mygtuką **Tikrinti**.

10. Jei nėra klaidų tikrinimo procese, spustelėkite **Registruoti**.

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a>Grąžintų prekių gavimo registravimas naudojant formą Registracija

Vietoje formos **Gavimų apžvalga**, galite naudoti formą **Registracija**, kad užregistruotumėte grąžinamų prekių gavimą.

1.  Spustelėkite **Pardavimas ir rinkodara** \> **Bendra** \> **Grąžinimo užsakymai** \> **Visi grąžinimo užsakymai**. Sukurkite naują grąžinimo užsakymą arba atidarykite grąžinimo užsakymą iš sąrašo. „FastTab“ skirtuke **Eilutės** pasirinkite grąžinimo užsakymo eilutę. Spustelėkite **Naujinti eilutę**, tada spustelėkite **Registracija**.

2.  Priskirkite perdavimo kodą lauke **Perdavimo kodas**, tada spustelėkite **Gerai**.
    

    > [!NOTE]
    > <P>Neįmanoma išsiųsti prekės patikrinti kaip sulaikymo užsakymo, naudojant formą <STRONG>Registracija</STRONG>.</P>



3.  Tinklelyje **Operacijos** pasirinkite operaciją, kuri turi būti registruojama.

4.  Tinklelyje **Registruoti dabar** spustelėkite **Įtraukti**. Kartokite du ankstesnius veiksmus, kol visos grąžinamos prekės bus rodomos tinklelyje **Registruoti dabar**.

5.  Spustelėkite **Registruoti viską**.

## <a name="see-also"></a>Taip pat žiūrėkite

[Gavimų peržiūra (forma)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]