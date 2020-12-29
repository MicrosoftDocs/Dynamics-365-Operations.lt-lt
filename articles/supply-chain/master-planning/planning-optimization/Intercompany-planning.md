---
title: Vidinės įmonės planavimas
description: Šiame skyriuje paaiškintas vidinės įmonės planavimas ir tai, kaip konfigūruoti jos planavimą su „Planning Optimization“ „Microsoft Dynamics 365 Supply Chain Management“.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 25c80ce27498131c6eb92174ab14a592bfa9915a
ms.sourcegitcommit: fe21a3a98dcf6fe4eb9351941493f2c0443d8696
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672198"
---
# <a name="intercompany-planning"></a>Vidinės įmonės planavimas

[!include [banner](../../includes/banner.md)]

Kai kurios organizacijose, logistinės operacijos priklauso nuo kitų juridinių asmenų (įmonių) organizacijos viduje. Šie veiksmai tvarkomi naudojant vidinės įmonės pardavimus ir pirkimus, nes kiekvienas juridnis asmuo yra atskiras sąskaitų grafikas.

Šiame skyriuje paaiškintas vidinės įmonės planavimas ir tai, kaip konfigūruoti jos planavimą su „Planning Optimization“ „Microsoft Dynamics 365 Supply Chain Management“.

Šioje temoje naudojami tolesnės svarbios vidinės įmonės sąvokos:

- **Prieš srovę** – Atitinkama nuoroda firmoje ar tiekimo grandinėje. Jis rodo judėjimą žaliavų tiekėjo kryptimi.
- **Pagal srovę** – Atitinkama nuoroda firmoje ar tiekimo grandinėje. Jis rodo judėjimą kliento kryptimi.
- **Suplanuota vidinės įmonės paklausa** – Suplanuota gaminio įmonėje paklausa pagal suplanuotą paklausą gaminiui iš pagal srovę įmonės.

Pagrindiniame planavime, planavimas vienoje įmonėje gali apimti planavimą vidinės įmonės paklausoje, kuri yra susieta su suplanuotais užsakymais pagal planą kitoje įmonėje. Pajėgumas naudingas, nes jis pateikia pilną planuojamų užsakymų visose įmonėse vaizdą. Jis taip pat užtikrini, kad visi suplanuoti tiekimo užsakymai yra sukurti, bet be poreikio suplanuotus užsakymus patvirtinti vidinės įmonės paklausai.

Jei vykdote pagrindinį planavimą iš pagrindinio plano, kuris apima suplanuotą pagal srovę paklausą, suplanuoti prikimo užsakymai iš susijusių vidinės įmonės pardavėjų bus įtraukti į planą pagal poreikį.

## <a name="required-setup"></a>Būtinas nustatymas

Siekiant naudoti vidinės įmonės planavimą, turite parengti savo sistemą tokiu būdu:

1. Atitinkami produktai turi būti išleisti visose atitinkamose įmonėse. Dėl daugiau informacijos, žr [Konfigūruoti ir naudoti vidinės įmonės prekybą „Dynamics 365 Supply Chain Management“ ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.
1. Pagal srovę paklausa turi būti padengta pirkimo formos tiekėjo, kuris turi vidinės įmonės sąsają su pagal srovės įmonę ir atitinkamą numatytojo inventoriaus matmenis (vietą ir sandėlį) klientui. Dėl daugiau informacijos, žr [Konfigūruoti ir naudoti vidinės įmonės prekybą „Dynamics 365 Supply Chain Management“ ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.
1. Pagrindinis planavimas prieš srovės įmonės turi apimti suplanuotą palei srovės paklausą ir atitinkamą įmonę bei pagrindinis planavimas turi būti nurodytas palei srovės planuose.

## <a name="include-planned-downstream-demand"></a>Įtraukti proceso pabaigoje suplanuotą poreikį

Atlikite šiuos žingsnius tam, kad sukonfigūruotumėte pagrindinį planą taip, kad jis apimtų suplanuotą pagal srovę paklausą.

1. Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**.
1. Pasirinkite ar sukurkite pagrindinį planą.
1. „FastTab“ **Vidinės įmonės planavimas** nustatykite šiuos laukelius:

    - **Įtraukti suplanuotą pagal srovę poreikį** – Nustatykite šią parinktį į *Taip* siekiant įjungti vidinės įmonės planavimą pagrindiniam planui.
    - **Pagal srovę planai** – Jei nustatote **Įtraukti suplanuotą pagal srovę poreikį** parinktį į *Taip*, naudokite įrankių juostą ir tinklelį, kad įtrauktumėte norimus pagrindinius planus iš kitų įmonių.

## <a name="peg-across-companies-by-using-multilevel-pegging"></a>Fiksavimas visose įmonėse naudojant kelių lygių fiksavimą

Kelių lygių fiksavime galite peržiūrėti fiksavimą įmonėse siekiant peržvelgti pradinį paklausos šaltinį, kuris yra padengtas tiekimu.

Norėdami peržiūrėti kelių lygių fiksavimo informaciją, atlikite šiuos žingsnius.

1. Eikite į **Pagrindinis planavimas \> Pagrindinis planavimas \> Suplanuoti užsakymai**.
1. Pasirinkite ar atidarykite suplanuotą užsakymą.
1. Veiksmų juostoje **Rodinys** skirtukas, grupėje **Reikalavimai**, pasirinkite **Kelių lygių fiksavimas**.

### <a name="intercompany-example-that-involves-two-companies"></a>Vidinės įmonės pavyzdys apimantis dvi įmones

Šiame pavyzdyje, suplanuotas gamybos užsakymas yra sukuriamas USMF įmonėje siekiant padengti pardavimo užsakymą DEMF įmonėje. USMF tiesioginis poreikis suplanuotai vidinės įmonės paklausai. Norėdami, kad ši paklausa pasirodytų USMF, pagrindinis planavimas pirmiausia vykdomas DEMF ir tada USMF.

Tolesnis paveikslėlis rodo, kaip šis pavyzdys gali būti rodomas **Kelių lygių fiksavimo** puslapyje suplanuotos gamybos užsakymui.

![Vidinės įmonės pavyzdys apimantis dvi įmones](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a>Vidinės įmonės pavyzdys apimantis tris įmones

Šiame pavyzdyje, suplanuotas pirkimo užsakymas yra sukuriamas USMF įmonėje siekiant padengti pardavimo užsakymą FRRT įmonėje. DEMF ir USM įmonėms, tiesioginė paklausa suplanuotai vidinės įmonės paklausai. Norėdami, kad ši paklausa pasirodytų USMF, pagrindinis planavimas pirmiausia vykdomas FRRT ir tada DEMF, o galiausiai USMF.

Tolesnis paveikslėlis rodo, kaip šis pavyzdys gali būti rodomas **Kelių lygių fiksavimo** puslapyje suplanuotos gamybos užsakymui.

![Vidinės įmonės pavyzdys apimantis tris įmones](media/IntercompanyPlanning2.png)
