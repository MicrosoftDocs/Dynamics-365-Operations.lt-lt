---
title: Vidinės įmonės planavimas
description: Šiame straipsnyje aprašomas vidinės įmonės planavimas ir paaiškinama, kaip konfigūruoti vidinės įmonės planavimą programoje "Microsoft"Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3d1c82aa3810b37b06b9d9157e73588fc1727348
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740038"
---
# <a name="intercompany-planning"></a>Vidinės įmonės planavimas

[!include [banner](../../includes/banner.md)]

Kai kurios organizacijose, logistinės operacijos priklauso nuo kitų juridinių asmenų (įmonių) organizacijos viduje. Šie veiksmai tvarkomi naudojant vidinės įmonės pardavimus ir pirkimus, nes kiekvienas juridinis subjektas yra atskiras sąskaitų planas.

Šiame straipsnyje aprašomas vidinės įmonės planavimas ir paaiškinama, kaip konfigūruoti vidinės įmonės planavimą programoje "Microsoft"Dynamics 365 Supply Chain Management.

Šiame straipsnyje naudojamos šios svarbios vidinės įmonės sąlygos:

- **Prieš srovę** – Atitinkama nuoroda firmoje ar tiekimo grandinėje. Jis rodo judėjimą žaliavų tiekėjo kryptimi.
- **Pagal srovę** – Atitinkama nuoroda firmoje ar tiekimo grandinėje. Jis rodo judėjimą kliento kryptimi.
- **Suplanuota vidinės įmonės paklausa** – Suplanuota gaminio įmonėje paklausa pagal suplanuotą paklausą gaminiui iš pagal srovę įmonės.

Pagrindiniame planavime, planavimas vienoje įmonėje gali apimti planavimą vidinės įmonės paklausoje, kuri yra susieta su suplanuotais užsakymais pagal planą kitoje įmonėje. Pajėgumas naudingas, nes jis pateikia pilną planuojamų užsakymų visose įmonėse vaizdą. Jis taip pat užtikrini, kad visi suplanuoti tiekimo užsakymai yra sukurti, bet be poreikio suplanuotus užsakymus patvirtinti vidinės įmonės paklausai.

Jei vykdote pagrindinį planavimą iš pagrindinio plano, kuris apima suplanuotą pagal srovę paklausą, suplanuoti prikimo užsakymai iš susijusių vidinės įmonės pardavėjų bus įtraukti į planą pagal poreikį.

## <a name="required-setup"></a>Būtinas nustatymas

Siekiant naudoti vidinės įmonės planavimą, turite parengti savo sistemą tokiu būdu:

1. Atitinkami produktai turi būti išleisti visose atitinkamose įmonėse. Daugiau informacijos ieškokite Vidinės įmonės [prekybos konfigūravimas ir naudojimas Dynamics 365 Supply Chain Management](/training/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).
1. Pagal srovę paklausa turi būti padengta pirkimo formos tiekėjo, kuris turi vidinės įmonės sąsają su pagal srovės įmonę ir atitinkamą numatytojo inventoriaus matmenis (vietą ir sandėlį) klientui. Daugiau informacijos ieškokite Vidinės įmonės [prekybos konfigūravimas ir naudojimas Dynamics 365 Supply Chain Management](/training/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).
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

![Vidinės įmonės pavyzdys apimantis dvi įmones.](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a>Vidinės įmonės pavyzdys apimantis tris įmones

Šiame pavyzdyje, suplanuotas pirkimo užsakymas yra sukuriamas USMF įmonėje siekiant padengti pardavimo užsakymą FRRT įmonėje. DEMF ir USM įmonėms, tiesioginė paklausa suplanuotai vidinės įmonės paklausai. Norėdami, kad ši paklausa pasirodytų USMF, pagrindinis planavimas pirmiausia vykdomas FRRT ir tada DEMF, o galiausiai USMF.

Tolesnis paveikslėlis rodo, kaip šis pavyzdys gali būti rodomas **Kelių lygių fiksavimo** puslapyje suplanuotos gamybos užsakymui.

![Vidinės įmonės pavyzdys apimantis tris įmones.](media/IntercompanyPlanning2.png)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
