---
title: Visuotinės adresų knygelės ir kitų adresų knygelių planas
description: Šioje temoje aprašomos aplinkybės ir sprendimai, kuriuos turite priimti planavimo proceso metu prieš konfigūruodami Išlaidų valdymą.
author: msftbrking
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87b3f6a74c217b0cc7cec784ca6a964ab2caae0c7e9438aee2cc82987a508d63
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771901"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a>Visuotinės adresų knygelės ir kitų adresų knygelių planavimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos aplinkybės ir sprendimai, kuriuos turite priimti planavimo proceso metu prieš nustatydami ir konfigūruodami visuotinę adresų knygelę ir bet kokias papildomas adresų knygeles. Dėl kai kurių sprendimų reikės patvirtinti sprendimus, kurie buvo atlikti kitose produkto srityse, pvz., organizacijos hierarchijoje.

## <a name="global-address-book"></a>Visuotinė adresų knygelė

Prieš pradėdami dirbti su visuotine adresų knygele, turite nustatyti numatytąsias jos reikšmes. Šios numatytosios reikšmės tada naudojamos bet kokioms papildomoms jūsų sukurtoms adresų knygelėms.

**Sprendimai**

- Kokia seka turėtų būti rodomi **Asmens** tipo šalių įrašų vardai ir pavardės? Pavyzdžiui, viena seka yra pavardė, antras vardas, vardas.
- Ar, panaikinus vaidmens įrašą, iš adresų knygelės turėtų būti panaikinti šalių įrašai? Pavyzdžiui, jei panaikinamas kliento įrašas, ar taip pat turėtų būti panaikintas šalies įrašas?
- Ar, kuriant naują įrašą, naudotojams turėtų būti pranešama, jei visuotinėje adresų knygelėje aptinkamas besidubliuojantis įrašas?
- Ar į šalies įrašo informaciją turėtų būti įtrauktas Duomenų universaliosios numeravimo sistemos (DUNS) numeris?
- Jei DUNS numeris įtraukiamas į šalies įrašą, ar turėtų būti tikrinamas numerio unikalumas?
- Kai visuotinėje adresų knygelėje kuriamas šalies įrašas, ar norite nustatyti numatytąjį įrašo tipą, asmens arba organizacijos?
- Kokie naudotojo vaidmenys turėtų turėti prieigą prie šalių įrašų privačios adresų ir kontaktinės informacijos?

## <a name="additional-address-books"></a>Papildomos adresų knygelės

Sukūrę visuotinę adresų knygelę, pagal poreikį galite kurti papildomų adresų knygelių, pvz., atskirą adresų knygelę kiekvienai jūsų organizacijos įmonei ar kiekvienai verslo šakai. Pavyzdžiui, „Fabrikam‟ yra tarptautinė organizacija, kuri turi kelias įmones ir dalyvauja keliose verslo šakose. „Fabrikam‟ planuoja sukurti kiekvienos verslo šakos adresų knygelę. Tų verslo šakų, kurių veikla vykdoma daugiau nei vienoje vietoje, pvz., pneumatinių įrankių verslo, „Fabrikam‟ planuoja sukurti kiekvienos vietos adresų knygelę. Chrisas, „Fabrikam‟ IT vadovas, sukūrė toliau pateiktą reikiamų adresų knygelių sąrašą. Šiame sąraše taip pat aprašomi šalių įrašai, kurie turi būti kiekvienoje adresų knygelėje.

- **Viešojo sektoriaus sutartys (PubSC)** – visų šalių, kurios susijusios su „Fabrikam‟ turimomis viešojo sektoriaus sutartimis, įrašai.
- **Privačiojo sektoriaus sutartys (PriSC)** – visų šalių, kurios susijusios su „Fabrikam‟ turimomis privačiojo sektoriaus sutartimis, įrašai.
- **Elektroniniai įrankiai (ET)** – visų šalių, dalyvaujančių perkant ar parduodant elektroninius įrankius, ar kitaip sąveikaujančių su elektroniniais įrankiais, kuriuos teikia „Fabrikam‟ „Fabrikam-Japan‟ įmonėje, arba kurie jai nuperkami, įrašai.
- **Pneumatiniai įrankiai (PTJPN)** – visų šalių, dalyvaujančių perkant ar parduodant pneumatinius įrankius, ar kitaip sąveikaujančių su pneumatiniais įrankiais, kuriuos teikia „Fabrikam‟ „Fabrikam-Japan‟ įmonėje, arba kurie jai nuperkami, įrašai.
- **Pneumatiniai įrankiai (PTUSA)** – visų šalių, dalyvaujančių perkant ar parduodant pneumatinius įrankius, ar kitaip sąveikaujančių su pneumatiniais įrankiais, kuriuos teikia „Fabrikam‟ „Fabrikam-US‟ įmonėje, arba kurie jai nuperkami, įrašai.

**Sprendimas:**

- Kiek sukursite papildomų adresų knygelių?


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]