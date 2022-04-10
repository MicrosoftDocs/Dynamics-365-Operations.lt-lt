---
title: Kliento skirstymo pagal terminus duomenų saugykla
description: Šioje temoje aprašomas kliento skirstymo pagal terminus duomenų išorinės saugyklos naudojimo procesas. Galite paleisti kliento skirstymo pagal terminus duomenų saugojimo procesą, kad išvestį būtų galima eksportuoti į išorinę sistemą.
author: JodiChristiansen
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ecd4f5359019e3c4778e21cc4946b9998cd519f
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817464"
---
# <a name="customer-aging-data-storage"></a>Kliento skirstymo pagal terminus duomenų saugykla

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje aprašomas kliento skirstymo pagal terminus duomenų išorinės saugyklos naudojimo procesas. Programoje "Microsoft" Dynamics 365 Finance galite paleisti kliento skirstymo pagal terminus duomenų saugojimo procesą, kad išvestį būtų galima eksportuoti į išorinę sistemą. Paleidus procesą, tos pačios skirstymo pagal terminus ataskaitos parinktys, kurios yra sistemoje, yra prieinamos išorinėse sistemose. Išsami informacija visada įtraukiama į eksportuotus duomenis.

Tais atvejais, kai išvestyje yra daug klientų ir (arba) daug operacijų, gali būti naudinga, kad klientų skirstymo pagal terminus duomenys būtų prieinami išorinei saugojimo sistemai. Jei esamos **klientų skirstymo pagal terminus ataskaitos laikas** sueis, nes joje yra per daug spausdintimų duomenų, ši funkcija pateikia alternatyvų būdą tiems patiems duomenims gauti.

## <a name="enable-the-customer-aging-data-storage-feature"></a>Įgalinti kliento skirstymo pagal terminus duomenų saugojimo funkciją

Kad galėtumėte naudoti šią funkciją, turite ją įgalinti savo sistemoje. Administratoriai gali naudoti funkcijų valdymo parametrus, kad patikrintų funkcijos būseną ir įgalintų ją, jei to reikia. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** Kreditas ir kolekcijos
- **Funkcijos pavadinimas:** Kliento skirstymo pagal terminus duomenų saugykla

## <a name="run-the-customer-aging-data-storage-process"></a>Vykdyti kliento skirstymo pagal terminus duomenų saugojimo procesą

1. Eikite į **Kredito ir mokėjimų priežiūros užklausos ir ataskaitos Kliento klientų skirstymo pagal terminus duomenų \>\>\> saugykla**.
2. Pasirinkite **Nauja**.
3. Lauke **Pavadinimas** įveskite proceso pavadinimą.
4. Nustatykite likusius parametrus, kaip jums reikia.

    > [!NOTE]
    > Operacijos informacija visada įtraukiama, o apdorojimas visada atliekamas paketinėje užduotyje.

5. Pasirinkite **Gerai**.
6. Atnaujinkite **puslapį Kliento skirstymo pagal terminus duomenų saugykla, kad** pamatytumėte paketo **pavadinimo ir paketo vykdymo laiko** **·** reikšmes, kurios rodomos kartu su **apdorojimo būsenos** reikšme. Kai paketinė užduotis baigiama, **laukas Apdorojimo būsena nustatomas kaip** **·** Baigtas, o laukas Skirstymo pagal terminus **eilučių skaičius** nustatytas. Jei paketinė užduotis kartojasi, **laukas Apdorojimo būsena nustatytas kaip Laukiama** **·**.
7. Pasirinkite **·** mygtuką Filtras, esantį šalia **lauko Skirstymo pagal terminus eilučių** skaičius, kad peržiūrėtumėte filtrus, kurie buvo pridėti paketinei užduočiai.

**Kliento skirstymo pagal terminus duomenų saugojimo puslapyje nėra** rezultatų. Tačiau **kliento skirstymo pagal terminus duomenų saugojimo duomenų** objektas leidžia eksportuoti išvestį į bet kurį formatą, kurį palaiko duomenų valdymas.

> [!NOTE]
> Prieš eksportuodami įtraukite filtrą, kad eksportuotus rezultatus apribotumėte iki paskutinio skirstymo pagal terminus. Pavyzdžiui, įtraukite šiuos kriterijus, kad grąžintumėte naujausią paketo vykdymą:
>
> (CustAgingDataStorageSysQueryRangeUtil :: getLatestBatchName())
>
> Arba įtraukite šiuos kriterijus, kad grąžintumėte naujausią dabartinio vartotojo paketinį vykdymą:
>
> (CustAgingDataStorageSysQueryRangeUtil :: getLatestBatchNameForCurrentUser())
