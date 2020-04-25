---
title: Atsargų skirstymo pagal terminus ataskaita
description: Šioje temoje aprašomos funkcijos, leidžiančios vykdyti atsargų skirstymo pagal terminus ataskaitą ir įgalinti išvestis kaip formą ir diagramą.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 790c8fe3a52bce652227f1cef97eff6496476100
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201627"
---
# <a name="inventory-aging-report"></a>Atsargų skirstymo pagal terminus ataskaita


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

„Microsoft Dynamics 365 Supply Chain Management“ galite vykdyti **Atsargų skirstymas pagal terminus** ataskaitą ir įgalinti išvestį kaip formą ir diagramą. Formoje stulpeliai ir kaupiamieji balansai yra dinamiškai koreguojami atsižvelgiant į sukonfigūruotą maketą. Diagramoje pateikiama vizualinė peržiūra, kuri palaiko filtravimą ir leidžia detalizuoti informaciją. Be to, duomenų subjektas pavadinimu **Atsargų skirstymas pagal terminus ataskaita** leidžia eksportuoti **Atsargų skirstymas pagal terminus** ataskaitą, kad būtų galima naudoti, pavyzdžiui, „Microsoft Excel“ failo arba PDF failo formatą.

Šis **Atsargų skirstymas pagal terminus** ataskaitos vykdymo metodas naudingas tais atvejais, kai išvestyje yra daug eilučių. Pavyzdžiui, išvestyje yra daug eilučių, jei yra 50 000 prekių ir 300 parduotuvių, sukurtų kaip sandėliai, o jūs prašote atsargų skirstymo pagal terminus pagal prekę, teritoriją ir sandėlį.

## <a name="run-an-inventory-aging-report"></a>Atsargų skirstymo pagal terminus ataskaitos vykdymas

1. Eikite į **Išlaidų valdymas \> Užklausos ir ataskaitos \> Atsargų skirstymas pagal terminus**.
1. Pasirinkite **Naujas**.
1. Lauke **Proceso identifikatorius – pavadinimas** įveskite unikalų ataskaitos pavadinimą.
1. Pasirinkite **Identifikavimas – ID** ataskaitą ir filtruokite ją, kaip reikia.

    Ataskaitų vykdymas visada atliekamas paketinėje užduotyje.

1. Po to, kai paketinė užduotis baigiama, išvestis rodoma puslapyje **Atsargų skirstymo pagal terminus saugojimas**.
1. Norėdami peržiūrėti rezultatą kaip formą, kurioje yra tradicinis tinklelio maketas, pasirinkite **peržiūrėti informaciją.** Norėdami peržiūrėti išvestį kaip kaupiamąją diagramą, pasirinkite **Peržiūrėti diagramą**.

    > [!NOTE]
    > Formoje nebus įtrauktos tarpinės sumos, kurios nurodytos ataskaitos makete.

Duomenų objektas**Atsargų skirstymo pagal terminus ataskaita** leidžia eksportuoti **Atsargų skirstymas pagal terminus** ataskaitą taikant filtrą **Proceso identifikatorius – pavadinimas** bet kokiam formatui, kurį palaiko duomenų valdymas.
