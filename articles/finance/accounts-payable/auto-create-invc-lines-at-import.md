---
title: Generuoti SF eilutes importuojant tiekėjo SF
description: Šiame straipsnyje aprašomos funkcijos, naudojamos automatiškai generuojant SF eilutes tiekėjo SF, kai importuotos SF.
author: sunfzam
ms.date: 09/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 5cb2c1234de03e9777921c18e4cbb81eec7feef9
ms.sourcegitcommit: 9c637bcf4e2eb8f711290a861492f038feaf1568
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/09/2022
ms.locfileid: "9462280"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Generuoti SF eilutes importuojant tiekėjo SF

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šiame straipsnyje aprašomos funkcijos, naudojamos automatiškai generuojant SF eilutes tiekėjo SF, kai importuotos SF.

Kartais tiekėjo SF yra ribotos informacijos, tokios kaip gavėjo informacija ir tarpinės sumos. Tačiau jose nėra informacijos apie eilutės prekes. Importuojant SF, SF eilutės bus generuojamos automatiškai, remiantis informacija apie atitinkamą pirkimo užsakymą.

Norėdami įgalinti automatinį SF eilučių kūrimą, atlikite šiuos veiksmus.

1.  Pasirinkite **Mokėtinos sumos \> Sąranka \> Mokėtinų sumų parametrai**.
2.  Skirtuko **Tiekėjo SF automatizavimas dalyje** kūrimas **Automatinis importuotų SF eilučių** nustatykite **Automatinis importuotų SF eilučių** pasirinktį į **Taip**. 
4.  Lauke Pasirinkti **numatytąjį kiekį, naudojamą kuriant automatinio SF eilutes**, pasirinkite kiekį, kuris turėtų būti naudojamas SF eilutėms automatiškai generuoti:

    - **Užsakytas kiekis** – eilutės bus sugeneruotos iš pirkimo užsakymo eilučių. Tai – numatytojo parametro vertė.
    - **Produkto gavimo kvitų** kiekis – pirkimo užsakymo numeris bus naudojamas norint rasti atitinkamus gavimo kvitus. Tada ji naudos produkto gavimo kvitų kiekius SF eilutėms generuoti.

## <a name="data-entity-changes"></a>Duomenų objektų keitimai

Siekiant palaikyti šiame straipsnyje aprašytas funkcijas, patobulintas **tiekėjo SF antraštės** duomenų objektas. Įtraukti trys laukai:

- **HeaderOnlyImport** – šį lauką reikia nustatyti kaip **Taip,** kad būtų generuojamos SF antraščių eilutės.
- **PurchIdRange** – pirkimo užsakymų numerių sąrašas. SF numeriai gali būti diapazonas, pvz. **, PO0001. PO0009** (kur du taškai atskiria diapazono pradžia ir pabaigą) arba atskiros vertės, pvz., **PO0001, PO0003, PO0006**. Visi pirkimo užsakymai turi priklausyti tai pačiai tiekėjo sąskaitai SF antraštėje. Kitu atveju gausite tokį klaidos pranešimą: „Nepavyko sugeneruoti SF eilučių. Pirkimo užsakymų tiekėjų sąskaitos skiriasi.“
- **PackingslipRange** – gavimo dokumentų numerių sąrašas. Tiekėjo SF eilutės gali būti sukurtos iš produkto gavimo kvitų. Tačiau produkto gavimo kvitų numeriai paprastai neįtraukiami į tiekėjo SF. Šiame lauke įveskite produkto gavimo kvitų numerius tik tada, jei galite aiškiai nustatyti, kuriems gavimo sąrašams naudojate konkrečias SF. Sąskaitos eilutės gali būti kuriamos pagal produkto kvitus. Jei šis laukas naudojamas, nepaisoma **·** **automatinio** SF eilučių kūrimo lauko Pasirinkti numatytąjį kiekį parametrų puslapyje Mokėtinų sumų parametrai. 

**Apribojimas**: Jei įvedate kelis produkto gavimo kvitų numerius, bus sukurtos kelios laukiančios tiekėjo SF su tuo pačiu SF numeriu. Prieš toliau apdorodami SF turite jas konsoliduoti neautomatiniu būdu. Būsimuose leidimuose planuojame automatiškai konsoliduoti SF, todėl apribojimas bus pašalintas.

Visi produkto kvitai turi priklausyti tai pačiai tiekėjo sąskaitai SF antraštėje.

## <a name="result"></a>Rezultatas

Jei eilutės sėkmingai sugeneruotos, tiekėjo SF automatizavimo retrospektyvoje registruojamas šis pranešimas: "Automatiškai kurti SF eilutes: pavyko".

Jei eilutės nesugeneruoja, užregistruojamas šis klaidos pranešimas: "Automatiškai sukurti SF eilutes: nepavyko".
