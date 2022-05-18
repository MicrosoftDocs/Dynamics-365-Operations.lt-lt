---
title: Įsigijimo katalogų apžvalga
description: Šiame straipsnyje aukštu lygiu aprašoma, kaip pirkimo specialistai gali nustatyti ir tvarkyti įsigijimo katalogus. Įsigijimo katalogais apibrėžiamos prekės ir paslaugos, kurias įmonės darbuotojai gali užsakyti naudoti viduje.
author: GalynaFedorova
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, CatDisplayProductRelationAdd
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2214"
- intro-internal
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd267cbbe7767faab538cacad26636ff1f37a551
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672016"
---
# <a name="procurement-catalogs-overview"></a>Įsigijimo katalogų apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aukštu lygiu aprašoma, kaip pirkimo specialistai gali nustatyti ir tvarkyti įsigijimo katalogus. Įsigijimo katalogais apibrėžiamos prekės ir paslaugos, kurias įmonės darbuotojai gali užsakyti naudoti viduje.

Pirkimo specialistai gali kurti ir tvarkyti prekių ir paslaugų, kurias galima nusipirkti ir naudoti organizacijos viduje, katalogus. Nustačius katalogus, įmonės darbuotojai gali kurti pirkimo paraiškas ir jas naudodami užsakyti. Katalogus galima naudoti pirkimo strategijoms taikyti, kad darbuotojai galėtų užsakyti tik tas prekes ir paslaugas, kurias galima atsižvelgiant į jų pirkimo juridinį subjektą. Kai kuriate įsigijimo katalogą, galite atlikti toliau nurodytas užduotis.

-   Prieš kurdami katalogą sukonfigūruokite savo įsigijimo kategorijų hierarchiją.
-   Nustatykite, kuriuos produktus jūsų darbuotojai gali užsakyti. Konkrečius produktus galite rodyti arba slėpti katalogo mazge arba galite rodyti arba slėpti visus produktus mazge.
-   Nustatykite, kiek įsigijimo katalogų jums reikia. Prieiga prie įsigijimo katalogo priklauso nuo katalogo strategijos taisyklės, kurią sukonfigūruojate juridiniam subjektui ir valdymo vienetui, kuriam priskiriamas darbuotojas.

Keli faktoriai nustato, kuriuos produktus darbuotojai gali užsakyti ir kurias įsigijimo kategorijas jie gali naudoti kurdami pirkimo paraiškas.

-   Pirkimo strategijos kategorijos prieigos strategijos taisyklė nustato, kurias įsigijimo kategorijas galima naudoti pirkimo paraiškoje. Jei taisyklė nenurodyta, galima naudoti visas įsigijimo kategorijas.
-   Darbuotojai gali produktą užsakyti tik jei jis yra aktyviame jūsų organizacijos įsigijimo kataloge ir aktyviame mazge bei nėra paslėptas. Produktas taip pat turi būti kategorijoje, prie kurios konkretus darbuotojas turi prieigą, atsižvelgiant į kategorijos prieigos strategijos taisyklę.
-   Katalogo strategijos taisyklė nurodo naudojamą katalogą. Jei katalogo strategijos taisyklė nenurodyta, tik kategorijos prieigos taisyklė nustato produktus, kuriuos darbuotojas gali užsakyti paraiškoje.

## <a name="prerequisites"></a>Būtinieji komponentai
Pateiktoje lentelėje aprašomos užduotys, kurios turi būti užbaigtos, kad pirkimo specialistas galėtų sukurti įsigijimo katalogą.

| Užduotis                                                | Vaidmuo               | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Įsigijimo kategorijų hierarchijos nustatymas.            | Pirkimo vadovas | Įsigijimo kategorijų hierarchijos suklasifikuoja prekes arba operacijas, kad būtų galima teikti ataskaitas ir analizuoti. Naudodamos įsigijimo kategorijų hierarchiją įmonės gali strategiškai valdyti kategorijas, produktus, tiekėjus ir kitus įsigijimo veiksnius iš centrinės vietos. Viena įsigijimo kategorijų hierarchija nustatoma visai organizacijai. Katalogas yra pagrįstas įsigijimo kategorijų hierarchija: hierarchijos kategorijos tampa katalogo mazgais. Į jūsų katalogą įtraukti tiekėjai ir produktai. |
| Tiekėjų ir produktų įtraukimas į įsigijimo kategorijas. | Pirkimo vadovas | Kai sukuriama jūsų organizacijos įsigijimo kategorijų hierarchija, kiekvieną įsigijimo kategoriją galima susieti su konkrečiais tiekėjais, produktais ir kt. Šie susiejimai yra automatiškai nukopijuojami į katalogą.                                                                                                                                                                                                                                                                                           |

## <a name="setting-up-a-catalog"></a>Katalogo nustatymas
Kai įvykdytos būtinosios sąlygos, galite nustatyti katalogus. Galite kurti vieną katalogą, kurį naudos visa jūsų organizacija, arba kelis katalogus, kuriuos naudos įvairūs jūsų organizacijos padaliniai. Jei sukuriate vieną visos organizacijos katalogą, prieiga prie katalogo priklauso nuo jūsų pirkimo strategijos taisyklių.  

Katalogas apibrėžia, kuriuos produktus galima užsakyti kuriant pirkimo paraiškas, bet jūs galite naudoti kategorijos prieigos strategijos taisykles papildomiems apribojimams taikyti. Kadangi katalogo mazgai yra įsigijimo kategorijos, juos galima sulaikyti naudojant kategorijos prieigos strategijos taisyklę. Šiuo atveju šios kategorijos produktų darbuotojai negali naudoti paraiškose. Kategorijos prieigos strategijos taisykles galite nustatyti puslapyje **Pirkimo strategijos**. Pateiktoje lentelėje aprašomos užduotys, kurios turi būti atliktos norint nustatyti katalogą.

| Užduotis                                                   | Vaidmuo             | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Naujo katalogo kūrimas.                                  | Pirkimo agentas | Kai kuriate katalogą, galite nurodyti jo pavadinimą ir aprašą. Taip pat galite nustatyti, ar katalogas bus naujinamas neautomatiškai, ar automatiškai, ir nurodyti katalogo savininką.                                                                                                                                      |
| Kontroliuokite, ar produktus kataloge galima naudoti. | Pirkimo agentas | Kadangi produktai yra nustatomi pagal įsigijimo kategorijas, visi jie rodomi atitinkamuose katalogo mazguose. Galite kontroliuoti, ar visi mazgo produktai bus paslėpti arba rodomi, kai katalogas naudojamas pirkimo paraiškoje. Taip pat galite kontroliuoti, ar atskiri mazgo produktai bus paslėpti arba rodomi. |
| Katalogo publikavimas.                                   | Pirkimo agentas | Norėdami, kad darbuotojai galėtų katalogą naudoti paraiškoje, turite nurodyti katalogo strategijos taisyklę, nustatyti katalogo būseną į **Aktyvus** ir jį publikuoti. Galite išjungti katalogus, kurių nenorite leisti vartotojams naudoti.                                              |

Naujinimai publikuojami automatiškai arba neautomatiškai, atsižvelgiant į katalogo parinktį, kurią pasirinkote puslapio **Katalogai** lauke **Numatytasis naujinimo tipas**. Galima naudoti toliau nurodytus numatytuosius katalogų naujinimo tipus.

-   **Dinaminis** – katalogas atnaujinamas automatiškai, kai tik jis pakeičiamas.
-   **Statinis** – katalogus reikia naujinti neautomatiškai.
-   **Abu** – jei į katalogą įtrauktos produktų kategorijos, kurių numatytasis naujinimo tipas yra **Statinis**, atnaujinus šias kategorijas reikia neautomatiškai atnaujinti ir katalogą. Jei į katalogą įtrauktos produktų kategorijos, kurių numatytasis naujinimo tipas yra **Dinaminis**, jis atnaujinamas automatiškai, kai tik yra pakeičiamas.


## <a name="additional-resources"></a>Papildomi ištekliai

[Įsigijimo kategorijų hierarchijos nustatymas](tasks/set-up-procurement-category-hierarchy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]