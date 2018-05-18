---
title: "Būtinos standartinių išlaidų konvertavimo sąlygos"
description: "Šioje temoje aptariama užduotis, kurią reikia atlikti prieš vykdant standartinių išlaidų konvertavimą."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 50891
ms.assetid: 73af66cf-c924-45be-837a-a648dbd05a31
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 65844bd78363dc6638b16b3fd4ca163a3fde6a23
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="prerequisites-for-a-standard-cost-conversion"></a>Būtinos standartinių išlaidų konvertavimo sąlygos

[!include [banner](../includes/banner.md)]

Šioje temoje aptariama užduotis, kurią reikia atlikti prieš vykdant standartinių išlaidų konvertavimą. 

Prieš atlikdami standartinių išlaidų konvertavimą, atlikite šiuos veiksmus:

1.  Nustatykite standartinių išlaidų **prekių modelių grupę**. Naudokite puslapį Prekių modelio grupės, kad sukurtumėte prekių modelio grupę, kurioje naudojamas standartinių išlaidų atsargų modelis. Nustatydami standartinių išlaidų konvertavimą, priskiriate šią prekių modelių grupę konvertuojamoms prekėms.
2.  Kiekvienai prekei priskirkite **išlaidų grupę**.
    -   Išlaidų grupė, priskirta nupirktai prekei, gali veikti kaip pagrindas priskiriant DK sąskaitas, susijusias su standartinėmis išlaidomis. Tai apima DK sąskaitų priskyrimą pirkimo kainų nuokrypiams. Gamybos aplinkoje nupirktiems komponentams priskirta išlaidų grupė taip pat suteikia išlaidų segmentavimą apskaičiuotose pagamintos prekės išlaidose.
    -   Pagamintai prekei priskirta išlaidų grupė gali veikti kaip pagrindas priskiriant DK sąskaitas, susijusias su standartinėmis išlaidomis, pvz., DK sąskaitų priskyrimas gamybos nuokrypiams.

3.  Pagamintai prekei, kurios išlaidos yra pastovios, priskirkite **standartinį užsakymo kiekį**. Pagamintos prekės standartinis užsakymo kiekis veikia kaip amortizavimo, arba skirstymo, pastoviųjų išlaidų apskaitos partijos dydis. Tai apima nukreipimo operacijų nustatymo laiką arba pastovų komponentų kiekį komplektavimo specifikacijoje (KS).
4.  Priskirti **DK sąskaitas**, susijusias su standartinėmis išlaidomis, ypač su perkainojimo nuokrypiu. Naudokite puslapį **Registravimas** (**Atsargų valdymas** &gt; **Sąranka**), kad priskirtumėte DK sąskaitas, susijusias su standartinėmis išlaidomis. Standartinių išlaidų konvertavimo procesui reikia bent priskirti sąskaitą visų prekių ir visų išlaidų grupių perkainojimo nuokrypiui. Naudokite puslapį **Sąskaitų planas**, norėdami apibrėžti DK sąskaitas, kurių reikės standartinėms išlaidoms. Naudokite puslapį **Operacijų deriniai** norėdami įgalioti išlaidų santykius (lentelėms, grupėms ir viskam) prieš nustatydami prekių registravimo taisykles.
5.  Nustatykite atsargų parametrus, kurie yra susiję su standartinėmis išlaidomis. Naudokite puslapyje **Atsargų ir sandėlio valdymo parametrai** esantį skirtuką **Numeracija** norėdami priskirti numeraciją perkainojimo kvitams. Perkainojimo kvitas generuojamas tada, kai dėl standartinių išlaidų konvertavimo įvyksta prekės atsargų vertės pokytis. Naudokite puslapį **Atsargų ir sandėlio valdymo parametrai** norėdami nustatyti išlaidų valdymo parametrus (skirtuke **Atsargų apskaita**), kad nustatytumėte du parametrus, kurie yra susiję su standartinėmis išlaidomis.
    -   Lauke **Išlaidų paskirstymas** pasirinkite Ne arba Antrinė DK. Antrinės DK pasirinkimas vadinamas aktyviu išlaidų paskirstymu. Aktyvus išlaidų paskirstymas yra labai svarbus skaičiavimui, išlaikymui ir išlaidų grupės segmentavimo peržiūrai visoje standartinių išlaidų komponentų kelių lygių produkto struktūroje. Kai išlaidų paskirstymas yra aktyvus, galite paskelbti ir analizuoti toliau nurodytus elementus vieno lygio, kelių lygių ar visu formatu:
        1.  Atsargos
        2.  Nebaigta gamyba (NG)
        3.  Parduotų prekių savikaina (PPS) pagal išlaidų grupę

        Aktyvus išlaidų paskirstymas reiškia, kad, suaktyvinus pagamintos prekės išlaidas, rezultatas bus saugomas išlaidų grupių segmentavime prekės išlaidų įraše. Jei lauke **Išlaidų paskirstymas** neįvesite vertės, išlaidų grupės segmentavimas nebus išsaugotas standartinių išlaidų komponentams. Vadinasi, pagamintų prekių standartinės išlaidos bus apskaičiuotos ir liks vienintelė suma be išlaidų grupių segmentavimo o pagamintų komponentų išlaidų įnašai bus sujungti į vieną sumą.
    -   Naudokite lauką **Nuokrypiai nuo standarto** norėdami pasirinkti susumuotą grupę ar grupę pagal išlaidas. Pasirinkus grupę pagal išlaidas galima identifikuoti pirkimo kainų nuokrypius ir gamybos nuokrypius pagal išlaidų grupę. Tai taip pat leidžia identifikuoti keturis gamybos nuokrypių tipus (partijos dydis, kiekis, kaina ir pakaitalų nuokrypiai). Pasirinkę susumuotą grupę negalėsite identifikuoti nuokrypių pagal išlaidų grupę ir negalėsite identifikuoti keturių gamybos nuokrypių tipų. Galėsite tik peržiūrėti susumuotus gamybos nuokrypius. Standartinė nuokrypių strategija yra nepriklausoma nuo išlaidų paskirstymo strategijos. Tai reiškia, galite nepasirinkti jokios išlaidų paskirstymo strategijos ir pasirinkti išlaidų grupės nuokrypius taip, kad gamybos nuokrypiai pagal išlaidų grupę vis tiek bus užfiksuoti.






