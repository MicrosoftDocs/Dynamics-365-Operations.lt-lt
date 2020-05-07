---
title: Projekto subsidijos
description: Šioje temoje aiškinama, kaip kurti arba keisti subsidiją.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f4f7d347dab9f02fc474656e2f4cfba8e374480d
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282840"
---
# <a name="project-grants"></a>Projekto subsidijos

[!include [banner](../includes/banner.md)]

Subsidija yra piniginė dovana, skirta konkrečiam tikslui arba projektui. Paprastai subsidijos išleidimui taikomi apribojimai. Modulyje Projektų valdymas ir apskaita galite įvesti ir stebėti subsidijas ir nurodyti jų ryšius su projektais bei projektų sutartimis. Pvz., galite atlikti toliau nurodytas užduotis.

- Susiekite subsidijas su projektais ir lėšų skyrimo šaltiniais naudodami saitus su puslapiais **Projektas** ir **Projekto sutarties informacija**.
- Įveskite ir stebėkite subsidijos keitimus, kai jos būsena keičiama iš vienos į kitą.
- Įveskite ir stebėkite išlaidas, pageidaujamas sumas ir gautas sumas.
- Sukurkite bendrąsias subsidijas ir su jomis susiekite papildomas subsidijas.

Galite sukurti subsidiją įvesdami visą išsamią informaciją į naują įrašą arba galite nukopijuoti išsamią informaciją iš esamos subsidijos ir tada atnaujinti ją.

## <a name="create-a-new-grant"></a>Kurti naują subsidiją

1. Eikite į **Projektų valdymas ir apskaita** \> **Subsidijos** \> **Subsidijos**.
2. Pasirinkite **Naujas** \> **Subsidija**.
3. Subsidijos informacijos puslapyje, „FastTab” **Bendra**, lauke **Subsidijos ID**, įveskite raidinį-skaitinį subsidijos identifikatorių.
4. Lauke **Subsidijos pavadinimas** įveskite subsidijos pavadinimą.
5. Lauke **Aprašas** įtraukite informacijos apie naują subsidiją.

    Daugelis kitų puslapyje esančių laukų yra pasirenkamieji ir galite įvesti tiek informacijos, kiek norite.

    Toliau pateiktame sąraše aprašoma informacija, kuri nurodoma kiekvieno subsidijos informacijos puslapio „FastTab”.

    - **Bendra** – įveskite subsidijos pavadinimą, būseną, aprašą, tikslą ir sumą.
    - **Kontaktinė informacija** – įveskite išsamią informaciją apie darbuotojus, padalinį, kuriame tvarkoma subsidija, ir apie subsidijos klientą arba organizacijos subsidijos šaltinį. Taip pat galite nustatyti, ar organizacija yra pereinamasis objektas, kuris gauna subsidiją ir tada perduoda ją kitam gavėjui. Spustelėkite **Įtraukti**, kad įtrauktumėte organizacijos, kuri skiria subsidiją, kontaktinę informaciją, pvz., telefono numerius ir el. pašto adresus.
    - **Datos ir galutiniai terminai** – įveskite datas, kurios yra susijusios su subsidija ir subsidijos prašymu. Pavyzdžiai apima prašymo terminą, pateikimo datą ir datą, kada subsidija patvirtinta arba atmesta.
    - **Susiję projektai ir projektų sutartys** – šiame „FastTab” galite įvesti informaciją tik tada, jei laukas **Subsidijos būsena**, esantis „FastTab” **Bendra**, nustatytas į **Aktyvi** arba **Suteikta**. Norėdami užbaigti susijusią užduotį, pasirinkite iš toliau pateiktų parinkčių.

        - **Įtraukti lėšų skyrimo šaltinį** – įtraukite naują subsidijos lėšų skyrimo šaltinį. Galite įvesti visą išsamią informaciją dabar arba galite naudoti numatytąją informaciją ir atnaujinti ją vėliau.
        - **Įtraukti projekto sutartį** – įtraukite arba atnaujinkite projekto sutarties informaciją.
        - **Įtraukti projektą** – įtraukite arba atnaujinkite išsamią projekto informaciją.

    - **Nustatymas** – įveskite išsamią informaciją apie atitinkančias lėšas, jei to reikalaujama. Daugelyje organizacijų, kurios skiria subsidijas, reikalaujama, kad gavėjai išleistų konkrečią sumą savo pinigų arba išteklių, atitinkančių sumą, kuri skirta subsidijoje. Lauke **Vietinis projekto arba sekimo ID** galite įvesti identifikatorių, kuris skiriasi nuo projekto identifikatoriaus.

        > [!NOTE]
        > Jei dalis subsidijos bus skirta kitai organizacijai, nustatykite parinktį **Papildomas cedentas** į **Taip**. Galite nurodyti, ar subsidijos, kurios skiriamos Jungtinėse Valstijose, bus skirtos pagal valstijos arba federalinį įgaliojimą.

    - **Lėšų išmokėjimo informacija** – įtraukite arba atnaujinkite informaciją apie tai, kaip dažnai subsidijos lėšos bus išimtos, kaip dažnai už jas bus išrašomos sąskaitos arba kaip dažnai jos bus leidžiamos.

## <a name="create-a-new-grant-from-a-copy"></a>Naujos subsidijos kūrimas pagal kopiją

1. Eikite į **Projektų valdymas ir apskaita** \> **Subsidijos** \> **Subsidijos**.
2. Pasirinkite **Naujas** \> **Subsidija pagal kopiją**.
3. Įveskite iš raidžių ir skaitmenų sudarytą naujosios subsidijos identifikatorių ir pavadinimą, tada pasirinkite **Gerai**.
4. Subsidijos informacijos puslapyje peržiūrėkite nukopijuotos subsidijos informaciją ir atlikite reikalingus pakeitimus. Dauguma puslapio laukų yra pasirinktiniai.

## <a name="view-or-modify-grant-details"></a>Subsidijos informacijos peržiūra arba modifikavimas

1. Eikite į **Projektų valdymas ir apskaita** \> **Subsidijos** \> **Subsidijos**.
2. Pasirinkite subsidiją, kurią norite modifikuoti.
3. Veiksmų srities skirtuke **Subsidija**, grupėje **Prižiūrėti** pasirinkite **Redaguoti**.
4. Peržiūrėkite subsidijos informaciją ir atlikite reikalingus pakeitimus.
