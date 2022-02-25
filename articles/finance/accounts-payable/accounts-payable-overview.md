---
title: Mokėtinos sumos sąskaitos faktūros apžvalgos konfigūravimas
description: Šioje temoje aprašomi puslapiai, kuriuos naudojate norėdami nustatyti pagrindines ir pasirinktines mokėtinų sumų funkcijas. Jame taip pat aprašomi nustatymo veiksmai, kuriuos turite atlikti prieš pradėdami nustatyti Mokėtinas sumas.
author: abruer
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "24671"
- intro-internal
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6cbc800d7ae4d566fddb111b7ee9d67234e3cf8c
ms.sourcegitcommit: 43d0555c17a0643c9e5ba3bc2da3ce5f80754642
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/18/2022
ms.locfileid: "8325999"
---
# <a name="configure-accounts-payable-overview"></a>Mokėtinos sumos sąskaitos faktūros apžvalgos konfigūravimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomi puslapiai, kuriuos naudojate norėdami nustatyti pagrindines ir laisvai pasirenkamas funkcijas modulyje Mokėtinos sumos. Jame taip pat aprašomi nustatymo veiksmai, kuriuos turite atlikti prieš pradėdami nustatyti Mokėtinas sumas.

## <a name="prerequisites-for-accounts-payable-setup"></a>Būtinosios Mokėtinų sumų sąrankos sąlygos

Prieš nustatydami Mokėtinas sumas, turite atlikti toliau nurodytą sąranką.

-   Didžiojoje knygoje.
    -   Jei planuojate naudoti mokėjimų žurnalus, juos nustatykite.
    -   Jei planuojate vykdyti valiutos kurso koregavimus, **nustatykite** valiutų kodus puslapyje Valiutos, **·** **nustatykite** valiutos kurso tipus puslapyje Valiutų kursų tipai ir nustatykite valiutų kursus valiutų kursų puslapyje.
-   Grynųjų pinigų ir banko valdymo modulyje nustatykite banko sąskaitas, kurias norite naudoti su mokėjimo būdais.

## <a name="setup-pages-for-accounts-payable"></a>Mokėtinų sumų sąrankos puslapiai

Norėdami nustatyti pagrindines kiekvieno juridinio subjekto Mokėtinų sumų funkcijas, naudokite toliau nurodytus puslapius. Puslapiai išvardyti rekomenduojama sąrankos tvarka. Norėdami palengvinti sąrankos procesą, galite kurti šablonus iš pirmųjų sukurtų įrašų. Šablone reikšmės paprastai įvedamos keliuose laukuose, kad būtų atspindimos savybės, kurias organizacija nori pritaikyti tam tikram klientų tipui.
1.  Mokėjimo sąlygų **puslapyje,** apibrėžkite mokėjimo sąlygas, kurias priskiriate pardavimo užsakymams, pirkimo užsakymams, klientams ir tiekėjams ir kurios nurodo SF terminus. Daugiau informacijos žr. [Nustatyti tiekėjo mokėjimo mokesčius](tasks/define-vendor-payment-fees.md).
2.  Mokėjimo metodų **puslapyje – tiekėjai kurkite** ir prižiūrėkite informaciją apie tai, kaip organizacija moka savo tiekėjams.
3.  Tiekėjų grupių **puslapyje** kurkite ir prižiūrėkite tiekėjų grupes, kurioms svarbūs registravimo, sudengimo ir mokėjimo, ataskaitų ir prognozavimo parametrai.
4.  Puslapyje Tiekėjo **registravimo šablonas nurodykite**, kaip tiekėjo operacijos registruojamos DK.
5.  Mokėtinų **sumų parametrų** puslapyje nustatykite numatytuosius parametrus, taikymą, jei nenurodytas specifinis parametras, įvairių funkcijų parametrus ir įvairias mokėtinų sumų numeracijas.
6.  Formos nustatymo **puslapyje** nustatykite įvairių dokumentų, susijusių su tiekėjais, formatą, kurį organizacija naudoja, kad sekų gavimų iš tiekėjų informaciją ir įveda mokėjimų tiekėjams srauto priežastis.
7.  Puslapyje Tiekėjai **kurkite** ir prižiūrėkite tiekėjų sąskaitas, taip pat mokesčių inspekcijas, į kurias jūsų organizacija praneša apie PVM.

## <a name="optional-setup-pages-for-accounts-payable"></a>Pasirinktiniai mokėtinų sumų sąrankos puslapiai
Be pagrindinių funkcijų, Mokėtinos sumos turi kitų funkcijų, kurias galite nustatyti.

Papildomi sąrankos puslapiai sisteminami pagal funkcijas.

**Strategijos**
-   **Tiekėjo SF strategijos puslapyje** nustatykite tiekėjo SF strategijas.

**SF gretinimas**

-   Leistino **SF sumų nuokrypio puslapyje** nustatykite SF sumų leistinus nuokrypius.
-   Atitikimo **strategijos puslapyje** nustatykite dviejų ir tri dalių atitikimo strategijas.
-   Leistino **kainų nuokrypio puslapyje** nustatykite vieneto kainų nuokrypius.
-   Leistino **prekių kainų nuokrypio grupių** puslapyje nustatykite prekių kainų nuokrypių grupes.
-   Leistino **tiekėjo kainų nuokrypio grupių** puslapyje nustatykite tiekėjo kainų nuokrypių grupes.
-   Leistino **išlaidų nuokrypio puslapyje** nustatykite leistinus išlaidų nuokrypius.

**Darbo eiga**

-   Mokėtinų **sumų darbo eigos puslapyje** nustatykite žurnalų patvirtinimo ir pirkimo paraiškų darbo eigos konfigūracijas.

**Priežastys**

-   **Tiekėjų priežasčių puslapyje** nustatykite priežasčių kodus.

**Mokesčiai**

-   **Išlaidų kodų** puslapyje nustatykite išlaidų, naudojamų pirkimo užsakymuose, kodus.
-   Puslapyje Tiekėjų **mokesčių grupė** kurkite ir prižiūrėkite tiekėjų išlaidų grupes.
-   Prekių išlaidų **grupių puslapyje** kurkite ir prižiūrėkite prekių išlaidų grupes.
-   Automatinių **išlaidų puslapyje** nurodykite išlaidas, kurios automatiškai priskiriamos užsakymams.

**Papildomos prekės**

-   **Puslapyje Papildomų prekių grupės – Tiekėjas** kurkite ir prižiūrėkite tiekėjų papildomų prekių grupes.
-   **Puslapyje Papildomų prekių grupės – Atsargos** kurkite ir prižiūrėkite prekių papildomų prekių grupes.

**Paskirstymas**

-   **Pristatymo sąlygų puslapyje** kurkite ir prižiūrėkite prekės perdavimo iš pardavėjo pirkėjui sąlygas.
-   Pristatymo būdų **puslapyje** kurkite ir prižiūrėkite transportavimo būdus, kurie naudojami, kai užsakymas iš pardavėjo pristatomas pirkėjui.
-   Paskirties kodų **puslapyje** kurkite ir prižiūrėkite pristatymo vietų identifikatorius ir aprašymus.

**Formos**

-   Formos pastabų **puslapyje sukurkite** standartinį tekstą, kuris bus rodomas įvairiuose puslapiuose.
-   **Formos rūšiavimo parametrų** puslapyje nustatykite paraiškų, gavimo sąrašų, važtaraščių ir SF rūšiavimo tvarką.
-   Spausdinimo **valdymo nustatymo puslapyje** nustatykite puslapių originalų ir kopijų spausdinimo valdymo informaciją.

**Mokėjimai**

-   **Mokėjimo nuolaidų puslapyje** nustatykite ir tvarkykite mokėjimo nuolaidų gavimo sąlygas. Mokėjimo nuolaidų kodai susiejami su tiekėjais ir taikomi pirkimo užsakymams.
-   **Mokėjimo grafikų puslapyje** nustatykite mokėjimo grafikus, kurie naudojami įmokų mokėjimams tiekėjams valdyti.
-   **Mokėjimo dienų puslapyje** nurodykite mokėjimo dienas, naudojamas terminui apskaičiuoti, ir nurodykite konkrečios savaitės arba mėnesio dienos mokėjimo dienas.
-   Mokėjimo mokesčio **puslapyje** kurkite ir prižiūrėkite su tiekėjais susietus mokėjimo mokesčius.
-   Mokėjimo instrukcijos **puslapyje sukurkite** ir prižiūrėkite mokėjimo instrukcijas.

**Statistika**

-   Skirstymo pagal **terminus laikotarpio apibrėžimų puslapyje nustatykite vartotojo nustatytus intervalus, naudojamus tiekėjų sąskaitų paskirstymui pagal mokėjimo terminus** analizuoti.
-   **Verslo eilutės puslapyje sukurkite** verslo eilutės (LOB) kodus, priskirtus tiekėjams.

**Mokesčiai 1099**

-   Puslapyje **1099 laukai** patikrinkite ir atnaujinkite minimalias sumas, apie kurias reikia pranešti JAV mokesčių inspekcijai (IRS) pagal naujausius jos reikalavimus.

## <a name="optional-setup-for-other-modules"></a>**Papildoma kitų modulių sąranka**
**Organizacijos administravimas**

-   **Numeracijų puslapyje** nustatykite SF numerių numeracijos grupes.
-   Toliau nurodytuose puslapiuose nustatykite adreso informaciją.
    -   **Adreso sąranka**
    -   **NAF kodai**
    -   **Importuoti pašto indeksus**

**DK**

-   Puslapyje Finansinės **dimensijos** nustatykite finansines dimensijas.
-   Toliau nurodytuose puslapiuose nustatykite mokesčių informaciją.
    -   **PVM kodai**
    -   **PVM grupės**
    -   **Prekės PVM grupės**
    -   **Sąskaitų grupė**
    -   **Neapmokestinimo PVM kodai**
    -   **PVM jurisdikcijos**
    -   **PVM rinkėjai**
    -   **PVM sudengimo laikotarpiai**

**Grynųjų pinigų ir banko valdymas**

-   **Mokėjimo paskirties kodų** puslapyje nustatykite centrinio banko **paskirties kodą**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
