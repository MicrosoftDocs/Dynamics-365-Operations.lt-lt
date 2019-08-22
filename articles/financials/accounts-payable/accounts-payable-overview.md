---
title: Konfigūruoti Mokėtinas sumas
description: Šiame straipsnyje aprašomi puslapiai, kuriuos naudojate norėdami nustatyti pagrindines ir laisvai pasirenkamas funkcijas programos „Microsoft Dynamics 365 for Finance and Operations“ modulyje Mokėtinos sumos. Jame taip pat aprašomi nustatymo veiksmai, kuriuos turite atlikti prieš pradėdami nustatyti Mokėtinas sumas.
author: abruer
manager: AnnBe
ms.date: 08/08/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8642b27f222ed080539e63b0608a52aefbe64e8
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837475"
---
# <a name="configure-accounts-payable"></a>Konfigūruoti Mokėtinas sumas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomi puslapiai, kuriuos naudojate norėdami nustatyti pagrindines ir laisvai pasirenkamas funkcijas programos „Microsoft Dynamics 365 for Finance and Operations“ modulyje Mokėtinos sumos. Jame taip pat aprašomi nustatymo veiksmai, kuriuos turite atlikti prieš pradėdami nustatyti Mokėtinas sumas.

<a name="prerequisites-for-accounts-payable-setup"></a>Būtinosios Mokėtinų sumų sąrankos sąlygos
----------------------------------------

Prieš nustatydami Mokėtinas sumas, turite atlikti toliau nurodytą sąranką.

-   Didžiojoje knygoje.
    -   Jei planuojate naudoti mokėjimų žurnalus, juos nustatykite.
    -   Jei planuojate vykdyti valiutos kurso koregavimus, puslapyje Valiutos nustatykite valiutų kodus, puslapyje Valiutų kursų tipai nustatykite valiutų kursų tipus, o Valiutų kursų puslapyje nustatykite valiutų kursus.
-   Grynųjų pinigų ir banko valdymo modulyje nustatykite banko sąskaitas, kurias norite naudoti su mokėjimo būdais.

## <a name="setup-pages-for-accounts-payable"></a>Mokėtinų sumų sąrankos puslapiai

Norėdami nustatyti pagrindines kiekvieno juridinio subjekto Mokėtinų sumų funkcijas, naudokite toliau nurodytus puslapius. Puslapiai išvardyti rekomenduojama sąrankos tvarka. Norėdami palengvinti sąrankos procesą, galite kurti šablonus iš pirmųjų sukurtų įrašų. Šablone reikšmės paprastai įvedamos keliuose laukuose, kad būtų atspindimos savybės, kurias organizacija nori pritaikyti tam tikram klientų tipui.
1.  Mokėjimo sąlygų puslapyje apibrėžkite mokėjimo sąlygas, kurias norite priskirti pardavimo užsakymams, pirkimo užsakymams, klientams ir tiekėjams, ir kurios apibrėžia SF terminus. Daugiau informacijos žr. [Nustatyti tiekėjo mokėjimo mokesčius](tasks/define-vendor-payment-fees.md).
2.  Puslapyje Mokėjimo metodai – tiekėjai kurkite ir prižiūrėkite informaciją apie tai, kaip organizacija moka savo tiekėjams.
3.  Tiekėjų grupių puslapyje kurkite ir prižiūrėkite tiekėjų grupes su tokiais pat svarbiais registravimo, sudengimo ir mokėjimo, ataskaitų kūrimo bei prognozavimo parametrais.
4.  Tiekėjų registravimo profilių puslapyje apibrėžkite, kaip tiekėjų operacijos registruojamos į DK.
5.  Mokėtinų sumų parametrų puslapyje nustatykite numatytąsias nuostatas, taikomas, jei nenurodoma konkretesnė nuostata, įvairių funkcijų parametrai ir įvairios Mokėtinų sumų numeracijos.
6.  Formų sąrankos puslapyje apibrėžkite įvairių dokumentų, susijusių su tiekėjais ir kuriuos naudoja organizacija gavimams iš tiekėjų sekti ir mokėjimų tiekėjams nurodyti srauto priežastis, formatą.
7.  Tiekėjų puslapyje kurkite ir prižiūrėkite tiekėjų sąskaitas bei mokesčių institucijas, kurioms jūsų organizacija teikia PVM ataskaitas.

## <a name="optional-setup-pages-for-accounts-payable"></a>Pasirinktiniai mokėtinų sumų sąrankos puslapiai
Be pagrindinių funkcijų, Mokėtinos sumos turi kitų funkcijų, kurias galite nustatyti.

Papildomi sąrankos puslapiai sisteminami pagal funkcijas.

**Strategijos**
-   Tiekėjo SF strategijos puslapyje nustatykite tiekėjo SF strategijas.

**SF gretinimas**

-   SF sumų leistinų nuokrypių puslapyje nustatykite leistinus SF sumų nuokrypius.
-   Puslapyje Gretinimo strategija nustatykite dvišalio ir trišalio gretinimo strategijas.
-   Puslapyje Leistini kainų nuokrypiai nustatykite leistinus vieneto kainų nuokrypius.
-   Leistinų prekių kainų nuokrypių grupių puslapyje nustatykite leistinų prekių kainų nuokrypių grupes.
-   Leistinų tiekėjo kainų nuokrypių grupių puslapyje nustatykite leistinų tiekėjo kainų nuokrypių grupes.
-   Puslapyje Leistini išlaidų nuokrypiai nustatykite leistinus išlaidų nuokrypius.

**Darbo eiga**

-   Mokėtinų sumų darbo eigų puslapyje nustatykite žurnalų patvirtinimo ir pirkimo paraiškų darbo eigų konfigūracijas.

**Priežastys**

-   Tiekėjo priežasčių puslapyje nustatykite priežasčių kodus.

**Mokesčiai**

-   Puslapyje Išlaidų kodas nustatykite išlaidų kodus, naudojamus pirkimo užsakymuose.
-   Puslapyje Tiekėjo išlaidų grupė kurkite ir prižiūrėkite tiekėjų išlaidų grupes.
-   Prekių išlaidų grupių puslapyje kurkite ir prižiūrėkite prekių išlaidų grupes.
-   Automatinių išlaidų puslapyje apibrėžkite išlaidas, kurios yra automatiškai priskiriamos užsakymams.

**Papildomos prekės**

-   Papildomų prekių grupių – tiekėjų puslapyje kurkite ir prižiūrėkite tiekėjų papildomų prekių grupes.
-   Papildomų prekių grupių – atsargų puslapyje kurkite ir prižiūrėkite prekių papildomų prekių grupes.

**Paskirstymas**

-   Pristatymo sąlygų puslapyje kurkite ir prižiūrėkite prekės perdavimo iš pardavėjo pirkėjui sąlygas.
-   Pristatymo būdų puslapyje kurkite ir prižiūrėkite transportavimo būdus, naudojamus pristatant užsakymą iš pardavėjo pirkėjui.
-   Paskirties kodų puslapyje kurkite ir prižiūrėkite pristatymo vietų identifikatorius ir aprašus.

**Formos**

-   Formų pastabų puslapyje sukurkite standartinį tekstą, rodomą įvairiuose puslapiuose.
-   Formų rūšiavimo parametrų puslapyje nustatykite paraiškų, gavimų sąrašų, važtaraščių ir sąskaitų faktūrų rūšiavimo tvarką.
-   Spausdinimo valdymo sąrankos puslapyje nustatykite puslapių originalų ir kopijų spausdinimo valdymo informaciją.

**Mokėjimai**

-   Mokėjimo nuolaidų puslapyje nustatykite ir prižiūrėkite mokėjimo nuolaidų gavimo sąlygas. Mokėjimo nuolaidų kodai susiejami su tiekėjais ir taikomi pirkimo užsakymams.
-   Mokėjimų grafikų puslapyje nustatykite mokėjimų grafikus, kurie naudojami valdant įmokų mokėjimus tiekėjams.
-   Mokėjimo dienų puslapyje apibrėžkite mokėjimo dienas, naudojamas terminams skaičiuoti, ir nurodykite konkrečios savaitės ar mėnesio dienos mokėjimo dienas.
-   Mokėjimo mokesčio puslapyje kurkite ir prižiūrėkite su tiekėjais susietus mokėjimų mokesčius.
-   Mokėjimo instrukcijos puslapyje kurkite ir prižiūrėkite mokėjimų instrukcijas.

**Statistika**

-   Skirstymo pagal terminus laikotarpių apibrėžčių puslapyje nustatykite naudotojo apibrėžtus intervalus, kurie naudojami analizuoti tiekėjų sąskaitų paskirstymui pagal mokėjimo terminus.
-   Verslo šakos puslapyje kurkite verslo šakų (LOB) kodus, priskiriamus tiekėjams.

**Mokesčiai 1099**

-   Puslapyje **1099 laukai** patikrinkite ir atnaujinkite minimalias sumas, apie kurias reikia pranešti JAV mokesčių inspekcijai (IRS) pagal naujausius jos reikalavimus.

## <a name="optional-setup-for-other-modules"></a>**Papildoma kitų modulių sąranka**
**Organizacijos administravimas**

-   Numeracijų puslapyje nustatykite SF numerių numeracijų grupes.
-   Toliau nurodytuose puslapiuose nustatykite adreso informaciją.
    -   Adreso sąranka
    -   NAF kodai
    -   Importuoti pašto indeksus

**DK**

-   Finansinių dimensijų puslapyje nustatykite finansines dimensijas.
-   Toliau nurodytuose puslapiuose nustatykite mokesčių informaciją.
    -   PVM kodai
    -   PVM grupės
    -   Prekės PVM grupės
    -   Sąskaitų grupė
    -   Neapmokestinimo PVM kodai
    -   PVM jurisdikcijos
    -   PVM rinkėjai
    -   PVM sudengimo laikotarpiai

**Grynųjų pinigų ir banko valdymas**

-   Mokėjimų paskirčių kodų puslapyje nustatykite centrinio banko paskirties kodą.





