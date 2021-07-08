---
title: Konvencijos
description: Šioje temoje aprašoma, kaip nustatyti konvencijas, skirtas nustatyti, kaip turėtų būti atlikta išlaidų apskaita Visuotinėje atsargų apskaitoje.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 74d99d3eefdcaaa7f6551668990b702396b32ffc
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273198"
---
# <a name="conventions"></a>Konvencijos

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Konvencija yra strategijų, kurios veikia sistemos elgseną, rinkinio talpykla. Atsižvelgdami į savo verslo reikalavimus, turite apibrėžti konvencijas naudodami įvairias strategijas, kurios nustato, kaip turėtų būti atlikta išlaidų apskaita Visuotinėje atsargų apskaitoje. Galite susieti kiekvieną konvenciją su viena ar daugiau didžiųjų knygų, kad užtikrintumėte didžiosiose knygose taikomų apskaitos strategijų nuoseklumą.

Norėdami nustatyti savo konvencijas, eikite į **Visuotinė atsargų apskaita \> Nustatymas \> Konvencijos**. Kiekvienai konvencijai nustatykite toliau pateiktus laukus:

- **Pavadinimas** – įveskite konvencijos pavadinimą.
- **Aprašas** – įveskite konvencijos aprašą.
- **Savikainos objekto strategija** – pasirinkite savikainos objekto strategiją. Šios strategijos nustato detalumo lygį, kurį sistema taiko atsargų vertei apskaičiuoti ir išlaikyti. Galimos toliau pateiktos iš anksto apibrėžtos parinktys:

    - Produktas
    - Produktas – Vieta
    - Produktas – Vieta – Sandėlis

    Pavyzdžiui, jei pasirenkate *Produktas – Vieta* kiekvienam atsargų perkėlimui (įplaukoms ar išlaidoms), sistema suskaičiuoja ir išlaiko kiekvieno produkto atsargų savikainą vietos lygiu. Todėl atsargų judėjimai žemesniais lygiais, pavyzdžiui, sandėlio lygiu, neturi įtakos atsargų vertei. (Sandėlio lygio perkėlimo pavyzdys yra prekių perkėlimas tarp dviejų sandėlių vienoje vietoje.) Taip pat negalite peržiūrėti atsargų savikainos žemesniu lygiu, pavyzdžiui, sandėlio lygiu.

- **Įvesties matavimo pagrindo strategija** – pasirinkite įvesties matavimo pagrindo strategiją. Šios strategijos nustato išlaidas, kurios turėtų patekti į atsargų sąskaitą, ir išlaidas, kurios turi būti nuskaičiuojamos. Šios pasirinktys yra aktualios prekybos įmonėms:

    - **Įprastas retrospektyvinis** – Visi savikainos komponentų srautai patenka į atsargų sąskaitą.
    - **Standartinis** – Standartinės savikainos patenka į atsargų sąskaitas, o skirtumas tarp taikytų išlaidų ir faktinių išlaidų įskaičiuojamas į nuokrypio sąskaitas. Jei norite sukurti *Standartinę* įvesties matavimo pagrindo strategiją, pirmiausia turite sukurti kainoraštį, kuriame strategija gali ieškoti prekės standartinės savikainos.
    - **Kainoraščiai** – Visuotinė atsargų apskaita palaiko prekių kainų suradimą iš kelių juridinių subjektų. Galite nurodyti kainoraštį, kurį naudos įvesties matavimo pagrindo strategija. Tokiu būdu sistema žinos, kur ieškoti prekės kainos. Atlikite tolesnius veiksmus, jei norite nustatyti kainoraščius:

        1. Lauke **Pavadinimas** įveskite pavadinimą.
        1. Lauke **Aprašas** įveskite aprašą.
        1. **Įkainojimo tipo** lauke pasirinkite įkainojimo tipą (*Standartinė savikaina* arba *Suplanuota savikaina*).
        1. Lauke **Kainos tipas** pasirinkite kainos tipą (*Savikaina*, *Pirkimas* arba *Pardavimo kaina*).
        1. Įtraukite įkainojimo versiją.
        1. Veiksmų srityje pasirinkite **Kaina**, kad patikrintumėte prekių kainas kainoraštyje.

- **Savikainos srauto prielaidos strategija** – Pasirinkite savikainos srauto prielaidos strategiją. Šios strategijos nustato, kaip išlaidos pašalinamos iš atsargų ir pranešamos kaip parduotų prekių savikaina. Galimos toliau pateiktos iš anksto apibrėžtos parinktys:

    - Vidurkis
    - Specialus – Paketas

    > [!NOTE]
    > Visuotinė atsargų apskaita yra nuolatinė atsargų sistema. Todėl sistema seka atsargų vertę po kiekvienos operacijos.

- **Savikainos elemento strategija** – Galite apibrėžti savikainos elemento strategijas ir susieti jas su šiuo lauku. *Savikainos elementas* yra ištekliaus išlaidos, kurias suvartoja įvykis. Galite naudoti savikainos elementus išlaidoms sekti ir skirstyti į kategorijas. Norėdami sukurti savikainos elemento strategijas, įveskite informaciją šiose vietose:

    - **Pavadinimo** lauke
    - **Aprašo** lauke
    - **Savikainos elementų** sąraše
    - **Taisyklių** tinklelyje

    Jei nenorite toliau skaidyti atsargų vertės, turite sukurti savikainos elementų sąrašą, kuriame būtų vienas savikainos elementas. Tada turite sukurti savikainos elemento strategiją, pagal kurią visi atitinkami matavimo tipai (savikainos komponentai) būtų susieti su tuo savikainos elementu.
