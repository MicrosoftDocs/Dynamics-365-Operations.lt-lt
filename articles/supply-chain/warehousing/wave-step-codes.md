---
title: Bangos veiksmo kodai
description: Šioje temoje pateikiama bangos veiksmo kodų ir jų naudojimo apžvalga.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992362"
---
# <a name="wave-step-codes"></a>Bangos veiksmo kodai

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a>Apie bangos veiksmo kodus

Bangos veiksmo kodai yra kodai, kuriuos vartotojai gali nustatyti ir naudoti konkretiems bangos metodų egzemplioriams susieti su atitinkamu šablonu. Yra papildymo, krovimo į konteinerius, etikečių spausdinimo, krovinio kūrimo ir rūšiavimo šablonų.

Kai bangos veiksmo kodai nenaudojami, vartotojai turi įvesti laisvos formos tekstą, kad galėtų nurodyti konkretų bangos metodo egzemplioriaus šabloną. Laisvos formos tekste dažnai būna klaidų, nes vartotojai turi įsitikinti, kad bangos veiksmo tekstas, kurį jie įtraukia į konkretų bangos veiksmo metodą bangos šablone, tiksliai atitinka tikslinio šablono bangos veiksmo tekstą.

Konkretaus bangos veiksmo tipo bangos veiksmo kodai nustatomi atskirame puslapyje. Kiekvieno bangos veiksmo metodo egzemplioriaus bangos šablone, kuriam būtinas bangos veiksmo kodas, bangos veiksmo kodas turi būti pasirinktas išplečiamajame sąraše. Pasirinkus išplečiamajame meniu, pakeičiamas laisvos formos teksto įrašas ir sumažinamas žmogaus padarytos klaidos pavojus ir poveikis. Sąrankos kodai naudojami norint susieti bangos veiksmo metodą bangos šablone su metodo tiksliniu šablonu.

> [!NOTE]
> Bangos veiksmo kodų funkcijos naudoti neprivaloma, o sunaudojimas vyksta per juridinį subjektą. Todėl, jei konkretus juridinis subjektas naudoja šią funkciją, visų minėto juridinio subjekto esamų bangos veiksmo kodų struktūra atnaujinama.

## <a name="setup-demo"></a>Sąrankos demonstracija 

Norėdami vykdyti šią demonstraciją, turite įdiegti demonstracinius duomenis ir naudoti **USMF** demonstracinių duomenų įmonę.

### <a name="enable-wave-step-codes"></a>Įgalinti bangos veiksmo kodus

Atlikite šiuos veiksmus, norėdami įjungti bangos veiksmo kodų funkciją.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.
2. Skirtuko **Bendra** FastTab **Bangos apdorojimas** nustatykite parinktį **Įjungti bangos veiksmo kodus** į **Taip**.

Visų esamų bangos veiksmo laisvos formos tekstų struktūra atnaujinama. Užbaigus šį naujinimą juridiniame subjekte, parinktis **Įjungti bangos veiksmo kodus** nebebus pasiekiama puslapyje **Sandėlio valdymo parametrai**.

Patvirtinama atliekant naujinimą, todėl, jei atnaujinti nepavyksta, gaunamas klaidos pranešimas. Gali nepavykti atnaujinti dėl toliau pateikiamų nesuderinamumų.

- Yra besidubliuojančių bangos veiksmo laisvos formos tekstų.
- Yra tinkinimų.
- Bangos veiksmo laisvos formos tekstas, susietas su bangos veiksmo metodo egzemplioriumi, neatitinka numatomo šablono tipo.

Pašalinę visus patvirtinimo metu nustatytus nesuderinamumus, galite iš naujo paleisti naujinimo procesą.

Atnaujinus sėkmingai, atsiranda puslapis **Bangos veiksmo kodai** (**Sandėlio valdymas \> Sąranka \> Bangos \> Bangos veiksmo kodai**). Šiame puslapyje pateikiami bangos veiksmo kodai, kurie buvo atnaujinti, kai buvo įjungta bangos veiksmo kodų funkcija.

### <a name="create-new-wave-step-codes"></a>Naujų bangos veiksmo kodų kūrimas

Puslapyje **Bangos veiksmo kodai** galite kurti ir naikinti bangos veiksmo kodus.

Visi nauji bangos veiksmo kodai ir su juo susiję ID turi būti unikalūs visuose bangos veiksmo tipuose ir jie turi būti nurodyti konkrečiame bangos veiksmo tipe.

### <a name="apply-wave-step-codes"></a>Bangos veiksmo kodų taikymas

Nustačius atitinkamus bangos veiksmo kodus, jie gali būti taikomi bangos proceso metodams.

Norėdami taikyti bangos veiksmo kodus, pereikite prie tinkamo tikslinio šablono. Toliau pateikiami tiksliniai šablonai, kuriuos nurodo bangos veiksmo kodai.

- **Papildymo šablonai:** Sandėlio valdymas \> Sąranka \> Papildymas \> Papildymo šablonai
- **Krovinio kūrimo šablonai:** Sandėlio valdymas \> Sąranka \> Krovinys \> Krovinio kūrimo šablonai
- **Rūšiavimo šablonai:** Sandėlio valdymas \> Sąranka \> Pakavimas \> Siuntimo rūšiavimo šablonai
- **Krovimo į konteinerius šablonai:** Sandėlio valdymas \> Sąranka \> Konteineriai \> Konteinerių kūrimo šablonai
- **Etikečių spausdinimo šablonai:** Sandėlio valdymas \>Sąranka \> Dokumento maršruto planavimas \>Bangos etikečių šablonai

Šablonai šiame sąraše taikomi tada, kai jie yra nurodyti bangos proceso metode, kuris pasirinktas bangos šablone. Kai bangos proceso metode esantis bangos veiksmo kodas bangos šablone atitinka bangos veiksmo kodą viename iš šablonų tipų, taikomas šablonas.

### <a name="sample-scenario"></a>Pavyzdinis scenarijus

Ši procedūra padeda užtikrinti, kad jūsų sukurtas papildymo šablonas bus taikomas bangos šablonui.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Bangos \> Bangos veiksmo kodai** ir sukurkite bangos veiksmo kodą tipui **Papildymas**.
2. Eikite į **Sandėlio valdymas \> Sąranka \> Papildymas \> Papildymo šablonai** ir sukurkite papildymo šabloną.
3. Papildymo šablone pasirinkite bangos veiksmo kodą, kurį sukūrėte tipui **Papildymas**.
4. Eikite į **Sandėlio valdymas \>Sąranka \> Bangos \>Bangos šablonai**ir pasirinkite norimą naudoti bangos šabloną.
5. Šablono FastTab **Metodai** pasirinkite metodą **Papildymas**.
6. Lauke **Bangos veiksmo kodas** pasirinkite bangos veiksmo kodą, kurį pasirinkote papildymo šablone.
