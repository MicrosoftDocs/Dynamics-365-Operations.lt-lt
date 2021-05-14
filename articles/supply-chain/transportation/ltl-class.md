---
title: Mažiau nei sunkvežimio (LTL) krovinių klasės
description: Šioje temoje paaiškinama, kas yra mažiau nei sunkvežimio krovinio (LTL) klasės ir aprašoma, kaip jas nustatyti programoje „Microsoft Dynamics 365 Supply Chain Management“.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941815"
---
# <a name="less-than-truckload-ltl-classes"></a>Mažiau nei sunkvežimio (LTL) krovinių klasės

[!include [banner](../includes/banner.md)]

Mažiau nei sunkvežimio krovinio (LTL) klasė yra krovinio siuntimo klasė, naudojama prekėms, kurios gali būti siunčiamos, klasifikuoti. Paprastai kiekvienas produkto ar prekės tipas turi „National Motor Freight Classification“ (NMFC) kodą, kuris atitinka specialų LTL siuntų transportavimo klasės numerį. LTL transportavimo klasės nurodo prekių kategorijas, o NMFC kodai yra susiję su konkrečiomis prekėmis kiekvienoje iš 18 transportavimo klasių.

Ši funkcija jums leidžia jums naudoti jūsų sistemą siekiant atlikti tolesnes užduotis:

- Nustatykite jūsų įmonėje naudojamas LTL transportavimo klases.
- Kiekvienai LTL klasei priskirkite NMFC kodą **NMFC kodų** puslapyje. Daugiau informacijos ieškokite [„National Motor Freight Classificatio“ (NMFC) ](nmfc-codes.md) kodais.
- Kiekvienam produktui produktų puslapyje priskirkite NMFC kodą (ir su juo susijęs LTL) **kodas**.
- Tiksliai įvertinti kiekvieno produkto, prie kurių priskirtas NMFC kodas, LTL klasę.
- Nustatyti pakavimo reikalavimus kiekvienai LTL klasei, tikrinant tarptautinius LTL standartus. Taip užtikrinate, kad jūsų produktai bus gerai apsaugoti ir saugiai išsiųsti.
- Gauti tikslius siuntimo įvertinimus, remiantis kiekvieno produkto LTL transportavimo klase.

Šioje temoje aprašoma, kaip sukurti LTL klases, naudojant „Microsoft Dynamics 365 Supply Chain Management“.

## <a name="create-an-ltl-class"></a>LTL klasės kūrimas

Norėdami sukurti LTL klasę, atlikite toliau nurodytus veiksmus.

1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Eikite į **Sandėlio valdymas \> Nustatymas \> Atsargos \> LTL klasės**.
    - Eikite į **Gabenimo valdymas \> Nustatymai \> Gabenimo standartai \> LTL klasės**.

2. Veiksmų srityje pasirinkite **Nauja** tam, kad sukurtumėte LTL klasę. Tada nustatykite toliau nurodytus laukus.

    - **LTL klasė – įveskite prekės tipo vidinį įmonės LTL klasės** identifikatorių (ID). Daugelis įmonių naudoja tarptautinius standartą. Tokiu atveju šio lauko vertė atitiks lauko Klasė **vertę**. Tačiau, jei jūsų įmonė naudoja savo standartą, įveskite kodą, kuris atitinka tą standartą.
    - **Pavadinimas** – įveskite aprašomąjį pavadinimą, kuris padės jums ir kitiems vartotojams pasirinkti teisingą kiekvieno NMFC kodo LTL klasę.
    - **Klasė** – įveskite prekės tipo tarptautinės standartinės LTL klasės ID. Čia įvedamas kodas turi atitikti oficialų standartą.

## <a name="example-set-up-ltl-classes"></a>Pavyzdys: LTL klasių rinkinys

Toliau pateikiamas pavyzdys rodo, kaip nustatyti dvi skirtingas LTL klases, kurias galima naudoti su skirtingais produktų tipais.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Atsargos \> LTL klasės**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **LTL klasė:** *92,5*
    - **Pavadinimas:** *kompiuteriai, stebėjimas, programos*
    - **Klasė:** *92,5*

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **LTL klasė:** *125*
    - **Pavadinimas:** *mažas plėtinys*
    - **Klasė:** *125*

1. Veiksmų srityje pasirinkite **Įrašyti**.

## <a name="additional-resources"></a>Papildomi ištekliai

- [„National Motor Freight Classification“ (NMFC) kodai](nmfc-codes.md)
- [Važtaraščio kūrimas](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
