---
title: Kliento skirstymo pagal terminus duomenų saugykla
description: Šiame straipsnyje aprašomas procesas, kaip naudoti išorinę klientų skirstymo pagal terminus duomenų saugyklą. Galite vykdyti klientų skirstymo pagal terminus duomenų saugojimo procesą, kad išeigą būtų galima eksportuoti į išorinę sistemą.
author: JodiChristiansen
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7a66485cc9a538f5c3999009b6dbe295d7a5b9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894148"
---
# <a name="customer-aging-data-storage"></a>Kliento skirstymo pagal terminus duomenų saugykla

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomas procesas, kaip naudoti išorinę klientų skirstymo pagal terminus duomenų saugyklą. Microsoft Dynamics 365 finansuose galite vykdyti klientų skirstymo pagal terminus duomenų saugojimo procesą, **kad** išeigą būtų galima eksportuoti į išorinę sistemą. Kai vykdote procesą, tos pačios skirstymo pagal terminus ataskaitos pasirinktys, galimos sistemoje, yra galimos išorinėms sistemoms. Išsami informacija visada įtraukiama į eksportuotus duomenis.

Gali padėti klientų skirstymo pagal terminus duomenis padaryti prieinamus išorinėje sistemoje saugykloje, kai išeigos operacijų yra daug klientų ir (arba) yra daug operacijų. Jei esamos klientų **skirstymo pagal terminus** ataskaitos laikas jau sueis, nes jame yra per daug duomenų spausdinti, ši funkcija suteikia alternatyvų būdą gauti tuos pačius duomenis.

## <a name="enable-the-customer-aging-data-storage-feature"></a>Įjungti klientų skirstymo pagal terminus duomenų saugojimo funkciją

Šią funkciją galėsite naudoti tik tada, kai ją įgalinsite savo sistemoje. Administratoriai gali naudoti funkcijų valdymo parametrus, norėdami patikrinti funkcijos būseną ir įgalinti ją, jei to reikalaujama. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** kreditas ir rinkiniai
- **Funkcijos pavadinimas: klientų** skirstymo pagal terminus duomenų saugojimas

## <a name="run-the-customer-aging-data-storage-process"></a>Vykdyti klientų skirstymo pagal terminus duomenų saugojimo procesą

1. Eikite į **Kredito ir mokėjimų priežiūros užklausas \> ir ataskaitas Klientų \> skirstymo pagal \> terminus duomenų saugojimą**.
2. Pasirinkite **Nauja**.
3. **Lauke Pavadinimas** įveskite proceso pavadinimą.
4. Nustatykite likusius parametrus taip, kaip jums reikia.

    > [!NOTE]
    > Operacijos informacija visada įtraukiama, o apdorojimas visada atliekamas paketinėje užduotyje.

5. Pasirinkite **Gerai**.
6. Atnaujinkite **klientų skirstymo pagal terminus duomenų saugojimo** **·** **puslapį**, kad pamatytumėte paketo pavadinimą ir paketo vykdymo laiko vertes, rodomas kartu su apdorojimo **būsenos** verte. Kai paketinė užduotis baigiama, apdorojimo **būsenos** laukas nustatomas į **Baigta** ir nustatytas **skirstymo pagal terminus eilučių** skaičius. Jei paketinė užduotis pasikartojanti, apdorojimo **būsenos** laukas nustatomas kaip **Laukiama**.
7. Pasirinkite mygtuką **Filtras**, esantį šalia skirstymo pagal **terminus eilučių skaičiaus lauko**, norėdami peržiūrėti filtrus, pridėtus prie paketinės užduoties.

Klientų **skirstymo pagal terminus duomenų** saugojimo puslapis neapima rezultatų. Tačiau klientų skirstymo **pagal terminus duomenų saugyklos duomenų** objektas leidžia eksportuoti išeigą į bet kokį formatą, kurį palaiko duomenų valdymas.

> [!NOTE]
> Prieš eksportuojant pridėti filtrą, kad būtų galima apriboti eksportuotus rezultatus iki naujausio skirstymo pagal terminus. Pavyzdžiui, pridėkite šiuos kriterijus, kad būtų pateiktas vėliausias paketinis paleidimas:
>
> (CustAgingDataStorageSysQueryRangeUtil:: getLatestBatchName())
>
> Arba pridėkite šiuos kriterijus, kad būtų galima grąžinti naujausią dabartinio vartotojo paketinį vykdymo paketą:
>
> (CustAgingDataStorageSysQueryRangeUtil:: getLatestBatchNameForCurrentUser())
