---
title: Generuoti SF eilutes importuojant tiekėjo SF
description: Šioje temoje aprašomos funkcijos, naudojamos automatiškai generuojant SF eilutes tiekėjo SF, kai importuojamos SF.
author: sunfzam
ms.date: 09/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 87dec3c142ae296975ab98432421be4548085c80
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647901"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Generuoti SF eilutes importuojant tiekėjo SF

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje aprašomos funkcijos, naudojamos automatiškai generuojant SF eilutes tiekėjo SF, kai importuojamos SF.

Kartais tiekėjo SF yra ribotos informacijos, tokios kaip gavėjo informacija ir tarpinės sumos. Tačiau jose nėra informacijos apie eilutės prekes. Kai importuojate SF, sistema gali automatiškai generuoti SF eilutes, remdamasi informacija apie atitinkamą pirkimo užsakymą.

Norėdami įgalinti automatinį SF eilučių kūrimą, atlikite šiuos veiksmus.

1.  Pasirinkite **Mokėtinos sumos \> Sąranka \> Mokėtinų sumų parametrai**.
2.  Skirtuko **Tiekėjo SF automatizavimas dalyje** kūrimas **Automatinis importuotų SF eilučių** nustatykite **Automatinis importuotų SF eilučių** pasirinktį į **Taip**. 
4.  Lauke **Pasirinkti numatytąjį kiekį, kad būtų galima kurti SF eilutes automatiškai** pasirinkite kiekį, kurį sistema turėtų naudoti SF eilutėms automatiškai generuoti:

    - **Užsakytas kiekis** – sistema sugeneruos eilutes iš pirkimo užsakymo eilučių. Tai – numatytojo parametro vertė.
    - **Produkto gavimo kvitų kiekis** – sistema naudos pirkimo užsakymų numerius, siekdama rasti susijusius produkto gavimo kvitus. Tada ji naudos produkto gavimo kvitų kiekius SF eilutėms generuoti.

## <a name="data-entity-changes"></a>Duomenų objektų keitimai

Siekiant palaikyti šioje temoje aprašytas funkcijas, tiekėjo **SF antraštės duomenų objektas** išplėstas. Įtraukti trys laukai:

- **HeaderOnlyImport** – šis laukas turi būti nustatytas kaip **Taip**, kad sistema galėtų sugeneruoti SF antraščių eilutes.
- **PurchIdRange** – pirkimo užsakymų numerių sąrašas. SF numeriai gali būti diapazonas, pvz., **INV0001. INV0009** (kur du taškai atskiria diapazono pradžia ir pabaigą) arba atskiros vertės, pavyzdžiui **INV0001, INV0003, INV0006**. Visi pirkimo užsakymai turi priklausyti tai pačiai tiekėjo sąskaitai SF antraštėje. Kitu atveju gausite tokį klaidos pranešimą: „Nepavyko sugeneruoti SF eilučių. Pirkimo užsakymų tiekėjų sąskaitos skiriasi.“
- **PackingslipRange** – gavimo dokumentų numerių sąrašas. Tiekėjo SF eilutės gali būti sukurtos iš produkto gavimo kvitų. Tačiau produkto gavimo kvitų numeriai paprastai neįtraukiami į tiekėjo SF. Šiame lauke įveskite produkto gavimo kvitų numerius tik tada, jei galite aiškiai nustatyti, kuriems gavimo sąrašams naudojate konkrečias SF. Sąskaitos eilutės gali būti kuriamos pagal produkto kvitus. Ir jei šis laukas naudojamas, nepaisoma automatinio **SF eilučių kūrimo lauko, esančio mokėtinų sumų parametrų** puslapyje **Pasirinkti numatytąj kiekį** puslapyje. 

**Apribojimas**: Jei įvedate kelis produkto gavimo kvitų numerius, bus sukurtos kelios laukiančios tiekėjo SF su tuo pačiu SF numeriu. Prieš toliau apdorodami SF turite jas konsoliduoti neautomatiniu būdu. Būsimuose leidimuose planuojame įgalinti sistemą automatiškai konsoliduoti SF, todėl apribojimas bus pašalintas.

Visi produkto kvitai turi priklausyti tai pačiai tiekėjo sąskaitai SF antraštėje.

## <a name="result"></a>Rezultatas

Jei sistema sėkmingai sugeneruoja eilutes, tiekėjo SF automatizavimo retrospektyvoje registruojamas šis pranešimas: „Automatiškai kurti SF eilutes: pavyko."

Jei sistemai nepavyko sugeneruoti eilučių, bus užregistruotas šis klaidos pranešimas: „Automatiškai sukurti SF eilučių: nepavyko."
