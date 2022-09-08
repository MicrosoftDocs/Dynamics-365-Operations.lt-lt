---
title: Rankiniu būdu tvarkyti pardavimo ir perkėlimo eilutės paėmimo išimtis
description: Šiame straipsnyje aprašoma, kaip administratoriai gali paimti (arba atsisakyti paėmimo) atsargų operacijas, kad ištaisytų problemas, kurias sukėlė sugadinti pardavimo ir perkėlimo užsakymo duomenys.
author: perlynne
ms.date: 08/19/2022
ms.topic: article
ms.search.form: WHSManualSalesLinePicking, WHSManualInventTransferLinePicking, InventTransPick, WHSLoadLineManualCorrection, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d2f89a7109060e69aca6a06eadaedc017728bbae
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404430"
---
# <a name="manually-handle-sales-and-transfer-line-picking-exceptions"></a>Rankiniu būdu tvarkyti pardavimo ir perkėlimo eilutės paėmimo išimtis

[!include [banner](../includes/banner.md)]

Rankinis pardavimo ir perkėlimo eilučių paėmimo išimčių tvarkymas leidžia administratoriams išspręsti problemas, kurias sukėlė sugadinti pardavimo ir perkėlimo užsakymo duomenys. Tai leidžia patikimiems vartotojams rankiniu būdu paimti (arba atsisakyti paėmimo) atsargų operacijas, susijusias su pardavimo ir perkėlimo užsakymo eilutėmis, kai sandėlio procesai jau vyksta.

Čia aprašyta funkcija turi būti naudojama tik tais atvejais, kai sistema negali baigti sandėlio procesų apdorojimo, suspausti įprastu būdu. Pagal numatytuosius nustatymus, jį naudoti leidžiama tik vartotojams, kurie turi sistemos administratoriaus vaidmenį. Tačiau galite suteikti prieigą prie jos rankiniu būdu *priskirdami teisę Išrinkti pardavimo* eilutes kitiems vaidmenims, jeigu to reikalaujate.

## <a name="turn-on-this-feature-for-your-system"></a>Šios funkcijos įjungimas sistemoje

Kad naudodami šiame straipsnyje aprašytas priemones, jas galėsite įjungti savo sistemoje. Administratoriai gali naudoti funkcijų [valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami patikrinti funkcijų būseną ir įjungti jas. **Priemonių valdymo darbo** srityje priemonės išvardytos naudojant šiuos pavadinimus:

- *Administratoriaus arba panašių patikimų vartotojų pardavimo eilutės išrinkimo rankiniu būdu paslauga*<br>(Kaip ir tiekimo grandinės valdymo versija 10.0.25, ši funkcija yra privaloma ir jos išjungti negalima.)
- *Administratoriaus arba panašių patikimų vartotojų perkėlimo eilutės išrinkimo rankiniu būdu paslauga*

## <a name="correct-transactions-related-to-sales-or-transfer-order-lines"></a>Taisyti operacijas, susijusias su pardavimo arba perkėlimo užsakymo eilutėmis

Norėdami ištaisyti operacijas, susijusias su pardavimo ar perkėlimo užsakymo eilutėmis, naudokite šią procedūrą.

1. Atlikite vieną iš šių veiksmų, atsižvelgdami į užsakymo tipą, kurį turite pataisyti:

    - Norėdami pataisyti su pardavimo užsakymu susijusią operaciją, eikite į sandėlio valdymo **\> periodines užduotis \> Išvalykite pardavimo \> užsakymo eilutę rankiniu būdu**.
    - Norėdami ištaisyti operaciją, susijusią su perkėlimo užsakymu, eikite į sandėlio valdymo **\> periodines užduotis Išvalykite \> paėmimo \> perkėlimo eilutes rankiniu būdu**.

1. **Puslapyje Išrinkti** **pardavimo** eilutes rankiniu būdu arba Paėmimo perkėlimo eilutėse rankiniu būdu naudokite tinklelio viršuje filtrų eilutes, kurių ieškote, ir viršutiniame tinklelyje pasirinkite tikslinę užsakymo eilutę.
1. Norėdami gauti **daugiau informacijos apie pasirinktą eilutę**, naudokite apatinės dalies skirtukus Atsargų operacijos, **·** **·** **Krovinio** eilutės, Darbo eilutės ir Konteinerio eilutės. Šiuose skirtukuose pateikiama informacija pateikia pagrindinę susijusių sandėlio procesų ir jų būsenų apžvalgą.
1. Veiksmų srityje pasirinkite Paimti **, kad** atidarytumėte pasirinktą užsakymo eilutę atsargų **operacijų** paėmimo puslapyje. Galite atlikti šį žingsnį net ir užsakymo eilutėms, kurios jau išleistos į sandėlį. (Paprastai į sandėlį išleistų užsakymo eilučių atidaryti negalima **Išrinkimo** puslapis.)

    > [!NOTE]
    > Atidaryę paėmimo puslapį galite gauti įvairius **perspėjimus**. Atlikti bet kurį veiksmą, kurį rekomenduoja šie įspėjimai. Pavyzdžiui, galite gauti įspėjimą apie užsakymo eilutes, kurios susietos su sandėlio darbu. Tokiu atveju, prieš koreguojant rankiniu [būdu](cancel-warehouse-work.md), svarbu bandyti atšaukti darbą naudojant standartines darbo atšaukimo funkcijas.

1. Pasirinkite eilutę operacijų **tinklelyje**, tada operacijų įrankių juostoje **pasirinkite Įtraukti** paėmimo **eilutę**.
1. Pasirinkta eilutė perkeliama į paėmimo **eilučių tinklelį**. Nustatykite atitinkamas visų stulpelių, kurių trūksta reikiamos informacijos, vertes. (Pvz., nurodykite vietą ir numerio lentelę, iš kurios prekė turėtų būti paimta / iš jos paimta.)
1. Pasirinkite **Patvirtinti viską paėmimo** eilučių **įrankių juostoje**.

## <a name="correct-load-line-quantities"></a>Taisyti krovinio eilutės kiekius

Norėdami ištaisyti krovinio eilutės kiekį, naudokite nurodytą procedūrą.

1. Atlikite vieną iš šių veiksmų, atsižvelgdami į užsakymo tipą, kurį turite pataisyti:

    - Norėdami pataisyti su pardavimo užsakymu susijusią operaciją, eikite į sandėlio valdymo **\> periodines užduotis \> Išvalykite pardavimo \> užsakymo eilutę rankiniu būdu**.
    - Norėdami ištaisyti operaciją, susijusią su perkėlimo užsakymu, eikite į sandėlio valdymo **\> periodines užduotis Išvalykite \> paėmimo \> perkėlimo eilutes rankiniu būdu**.

1. **Puslapyje Išrinkti** **pardavimo** eilutes rankiniu būdu arba Paėmimo perkėlimo eilutėse rankiniu būdu naudokite tinklelio viršuje filtrų eilutes, kurių ieškote, ir viršutiniame tinklelyje pasirinkite tikslinę užsakymo eilutę.
1. Apatinės **dalies skirtuke** Krovinio eilutės pasirinkite Taisyti krovinio **eilutes rankiniu būdu** įrankių juostoje.
1. Puslapyje Taisyti **krovinio eilutes** rankiniu būdu atsargų **operacijų tinklelyje** peržiūrėkite atsargų operacijas, susijusias su pasirinkta krovinio eilute.
1. Viršutiniame tinklelyje tinkamai ištaisykite krovinio eilutės kiekius toliau nurodytose stulpeliuose:

    - **Sukurto darbo kiekis**
    - **Paimtas kiekis**
    - **Planuotas prekių skirstymo kiekis**

    Sistema patvirtins visus jūsų atliktus šių stulpelių pakeitimus.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
