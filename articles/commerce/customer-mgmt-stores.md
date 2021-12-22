---
title: Klientų valdymas parduotuvėse
description: Šioje temoje paaiškinama, kaip mažmenininkai gali įgalinti klientų valdymo pajėgumus „Microsoft Dynamics 365 Commerce“ elektroniniame kasos aparate (EKA).
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 29e45419f712e25092b473e34144ac1146e4ed9b
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913631"
---
# <a name="customer-management-in-stores"></a>Klientų valdymas parduotuvėse

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip mažmenininkai gali įgalinti klientų valdymo pajėgumus „Microsoft Dynamics 365 Commerce“ elektroniniame kasos aparate (EKA).

Svarbu, kad parduotuvės susiejimai galėtų kurti ir redaguoti klientų įrašus EKA. Tokiu būdu jie gali užfiksuoti visus kliento informacijos naujinimus, pvz., el. pašto adresą, telefono numerį ir adresą. Ši informacija yra naudinga proceso pabaigos sistemose, pvz., rinkodaros, nes šių sistemų efektyvumas priklauso nuo jų klientų duomenų tikslumo.

Pardavimo susiejimai gali iššaukti klientų kūrimo darbo eigą iš EKA įėjimo taškų. Jie gali paspausti mygtuką, atvaizduotą operacijai **Kliento pridėjimas** arba programėlės juostoje paieškos rezultatų puslapyje jie gali pasirinkti **Kurti klientą**. Abiem atvejais pasirodo dialogo langas **Naujas klientas**, kuriame pardavimų susiejimai gali įvesti reikiamus kliento duomenis, pvz., kliento vardą ir pavardę, el. pašto adresą, telefono numerį, adresą ir visą su įmone susijusią papildomą informaciją. Šią papildomą informaciją galima užfiksuoti naudojant su kliento susietus kliento atributus. Daugiau informacijos apie kliento atributus žr. skyriuje [Kliento atributai](dev-itpro/customer-attributes.md).

Pardavimų susiejimai taip pat gali užfiksuoti antrinius el. pašto adresus ir telefono numerius. Be to, jie gali užfiksuoti kliento pasirinkimus dėl rinkodaros informacijos gavimo šiais antriniais el. pašto adresais ar telefono numeriai. Kad įjungtų šią galimybę, mažmenininkai turi įjungti funkciją **Šiuose kontaktuose užfiksuoti kelis el. pašto adresus ir telefono numerius bei sutikimą dėl rinkodaros**, esančią darbo srityje **Funkcijų valdymas**, kurią galima rasti „Commerce“ valdymo srityje (**Sistemos administravimas \> Darbo sritys \> Funkcijų valdymas**).

## <a name="default-customer-properties"></a>Numatytosios kliento savybės

Mažmenininkai puslapį **Visos parduotuvės**, esantį „Commerce“ valdymo srityje (**Mažmeninė prekyba ir komercija \> Kanalai \> Parduotuvės**), kad su numatytąjį klientą susietų su kiekviena parduotuve. Tada „Commerce“ visiems naujiems sukurtiems kliento įrašams kopijuoja savybes, kurios apibrėžiamos numatytajam klientui. Pavyzdžiui, dialogo lange **Kurti klientą** rodomos savybės, kurios perimamos iš numatytojo kliento, kuris yra siejamas su parduotuve. Šios savybės – tai **kliento tipas**, **kliento grupė**, **kvito parinktis**, **kvito el. paštas**, **valiuta** ir **kalba**. Visi **priskyrimai** (klientų grupavimai) taip pat perduodami iš numatytojo kliento. Tačiau **finansinės dimensijos** yra perimamos iš tos klientų grupės, kuri yra susieta su numatytuoju klientu, o ne iš paties numatytojo kliento.

> [!NOTE]
> **Kvito el. pašto** vertė nukopijuojama iš numatytojo kliento tik tada, jei kvito el. pašto ID nėra pateikiama naujai sukurtiems klientams. Tai reiškia, kad jei numatytajam klientui yra kvito el. pašto ID, tada visi klientai, sukurti iš el. prekybos svetainės, gaus tą patį kvito el. pašto ID, nes nėra vartotojo sąsajos, kad būtų galima fiksuoti kvito el. pašto ID iš kliento. Rekomenduojame palikti **kvito el. pašto** lauką tuščią numatytam parduotuvės klientui ir naudoti jį tik tada, jei turite verslo procesą, kuris priklauso nuo esamo kvito el. pašto adreso. 

Pardavimų susiejimai gali perimti kelis kliento adresus. Kliento vardas ir pavardė bei telefono numeris perimami iš kontaktinės informacijos, siejamos su kiekvienu adresu. Kliento įrašo „FastTab“ skirtukas **Adresai** apima laukelį **Tikslas**, kurį pardavimų susiejimai gali redaguoti. Jei kliento tipas yra **Asmuo**, numatytoji vertė yra **Namai**. Jei kliento tipas yra **Organizacija**, numatytoji reikšmė yra **Įmonė**. Kitos šio laukelio palaikomos vertės: **Namai**, **Biuras** ir **Pašto dėžutė**. Adreso laukelis **Šalis** perimamas iš pagrindinio adreso, kuris nurodomas puslapyje **Valdymo vienetas**, esančiame „Commerce“ valdymo srityje pasirinkus **Organizacijos administravimas \> Organizacijos \> Valdymo vienetai**.



## <a name="additional-resources"></a>Papildomi ištekliai

[Asinchroninis kliento kūrimo režimas](async-customer-mode.md)

[Asinchroninių klientų konvertavimas į sinchronus klientus](convert-async-to-sync.md)

[Kliento atributai](dev-itpro/customer-attributes.md)

[Duomenų pašalinimas veikiant autonominiu režimu](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
