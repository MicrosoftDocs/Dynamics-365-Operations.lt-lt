---
title: Atsargų skirstymo pagal terminus ataskaitos saugykla
description: Šiame straipsnyje aprašomos funkcijos, kurios leidžia vykdyti atsargų skirstymo pagal terminus ataskaitą ir padaryti išvestį galima kaip formą ir diagramą.
author: JennySong-SH
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1d810ec90c85f2f7758ec01ef4b24611e026cc80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875574"
---
# <a name="inventory-aging-report-storage"></a>Atsargų skirstymo pagal terminus ataskaitos saugykla

[!include [banner](../includes/banner.md)]

„Microsoft Dynamics 365 Supply Chain Management“ galite vykdyti **Atsargų skirstymo pagal terminus ataskaitos saugykla** ataskaitą ir įgalinti išvestį kaip formą ir diagramą. Formoje stulpeliai ir kaupiamieji balansai yra dinamiškai koreguojami atsižvelgiant į sukonfigūruotą maketą. Diagramoje pateikiama vizualinė peržiūra, kuri palaiko filtravimą ir leidžia detalizuoti informaciją. Be to, duomenų subjektas pavadinimu **Atsargų skirstymas pagal terminus ataskaita** leidžia eksportuoti **Atsargų skirstymo pagal terminus ataskaitos saugykla** ataskaitą, kad būtų galima naudoti, pavyzdžiui, „Microsoft Excel“ failo arba PDF failo formatą.

Šis **Atsargų skirstymo pagal terminus ataskaitos saugykla** ataskaitos vykdymo metodas naudingas tais atvejais, kai išvestyje yra daug eilučių. Pavyzdžiui, išvestyje yra daug eilučių, jei yra 50 000 prekių ir 300 parduotuvių, sukurtų kaip sandėliai, o jūs prašote atsargų skirstymo pagal terminus pagal prekę, teritoriją ir sandėlį.

## <a name="enable-the-inventory-value-storage-report-feature"></a>Atsargų vertės saugyklos ataskaitos funkcijos įjungimas

Kad galėtumėte naudoti šią funkciją, turite ją įjungti savo sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įgalinti ją, jei reikia. Čia funkcija yra nurodyta kaip:

- **Modulis** – kaštų valdymas
- **Funkcijos pavadinimas** – Atsargų skirstymo pagal terminus ataskaitos saugykla

## <a name="run-an-inventory-aging-report-storage"></a>Atsargų skirstymo pagal terminus ataskaitos saugyklos vykdymas

1. Eikite į **Išlaidų valdymas \> Užklausos ir ataskaitos \> Atsargų skirstymas pagal terminus**.
1. Pasirinkite **Naujas**.
1. Lauke **Proceso identifikatorius – pavadinimas** įveskite unikalų ataskaitos pavadinimą.
1. Pasirinkite **Identifikavimas – ID** ataskaitą ir filtruokite ją, kaip reikia.

    Ataskaitų vykdymas visada atliekamas paketinėje užduotyje.

1. Po to, kai paketinė užduotis baigiama, išvestis rodoma puslapyje **Atsargų skirstymo pagal terminus saugojimas**.
1. Norėdami peržiūrėti rezultatą kaip formą, kurioje yra tradicinis tinklelio maketas, pasirinkite **peržiūrėti informaciją.** Norėdami peržiūrėti išvestį kaip kaupiamąją diagramą, pasirinkite **Peržiūrėti diagramą**.

    > [!NOTE]
    > Formoje nebus įtrauktos tarpinės sumos, kurios nurodytos ataskaitos makete.

Duomenų objektas **Atsargų skirstymo pagal terminus ataskaita** leidžia eksportuoti **Atsargų skirstymo pagal terminus ataskaitos saugykla** ataskaitą taikant filtrą **Proceso identifikatorius – pavadinimas** bet kokiam formatui, kurį palaiko duomenų valdymas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]