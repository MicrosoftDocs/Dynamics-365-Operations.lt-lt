---
title: Klientų valdymas parduotuvėse
description: Šioje temoje paaiškinama, kaip mažmenininkai gali įgalinti klientų valdymo pajėgumus „Microsoft Dynamics 365 Commerce“ elektroniniame kasos aparate (EKA).
author: josaw1
ms.date: 05/25/2021
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
ms.openlocfilehash: dd17593d84a8bf262712a84b11829f8ec6c49049
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097213"
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

## <a name="sync-customers-and-async-customers"></a>Sinchroniniai ir asinchroniniai klientai

„Commerce“ naudojami du klientų kūrimo būdai: sinchroninis (arba „Sync“) ir asinchroninis (arba "Async"). Numatyta, kad klientai sukuriami sinchroniškai. Kitaip tariant, jie kuriami realiuoju laiku „Commerce“ valdymo srityje. „Sync“ kliento kūrimo režimas naudingas, nes naujų klientų iš karto ieškoma visuose kanaluose. Tačiau yra ir trūkumų. Kadangi ši funkcija generuoja [Commerce Data Exchange: realaus laiko paslaugos](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) skambučius į „Commerce“ valdymo sritį, veiksmingumui tai gali daryti įtakos, jei vienu metu atliekami keli kliento kūrimo skambučiai.

Jei parinktis **Kurti klientą asinchroniniu režimu** nustatyta kaip **Taip** parduotuvės funkcijų profilyje (**Mažmeninė prekyba ir komercija \> Kanalo sąranka \> Interneto parduotuvės sąranka \> Funkcijų profiliai**), realiu laiku atliekami skambučiai nenaudojami klientų įrašams kurti kanalo duomenų bazėje. Sinchroninio kliento kūrimo režimas „Commerce“ valdymo srities efektyvumui įtakos nedaro. Kiekvienam naujam „Async“ kliento įrašui priskiriamas laikinas visuotinis unikalus identifikatorius (GUID) ir naudojamas kaip kliento paskyros ID. Šis GUID nerodomas EKA naudotojams. Vietoje to, kaip kliento paskyros ID šie naudotojai matys **Laukiama sinchronizavimo**. Nors dėl šios konfigūracijos klientai kuriami asinchroniškai, atkreipkite dėmesį, kad klientų įrašų redagavimas visada atliekamas sinchroniškai.

### <a name="convert-async-customers-to-sync-customers"></a>„Async“ klientų konvertavimas į „Sync“ klientus

Kad „Async“ klientus galėtumėte konvertuoti į „Sync“ klientus, pirmiausia turite paleisti P užduotį, kad „Async“ klientus nusiųstumėte į „Commerce“ valdymo sritį. Tada paleiskite užduotį **Klientų ir verslo partnerių sinchronizavimas iš asinchroninio režimo**, kad sukurtumėte klientų paskyrų ID. Galiausiai vykdykite užduotį **1010**, kad sinchronizuotumėte naujų klientų paskyrų ID kanaluose.

### <a name="async-customer-limitations"></a>„Async“ kliento apribojimai

„Async“ kliento funkcijai šiuo metu taikomi šie apribojimai:

- „Async“ kliento įrašų redaguoti negalima, nebent „Commerce“ valdymo srityje buvo sukurtas klientas, o naujo kliento paskyros ID sinchronizuotas atgal į kanalą.
- Priskyrimų negalima susieti su „Async“ klientais. Todėl nauji „Async“ klientai neperima priskyrimų iš numatytojo kliento.
- Lojalumo kortelių negalima išduoti „Async“ klientams, jei naujo kliento paskyros ID nebuvo sinchronizuotas atgal į kanalą.
- Negalima užfiksuoti „Async“ klientų antrinių el. pašto adresų ir telefonų numerių.

### <a name="customer-creation-in-pos-offline-mode"></a>Kliento kūrimas EKA autonominiu režimu

Jei EKA pereina į autonominį režimą, kai įjungtas „Async“ kliento kūrimo režimas, naujų klientų įrašai sukuriami asinchroniškai. Jei EKA veikia autonominiu režimu, kai „Async“ kliento sukūrimo režimas išjungtas, sistema automatiškai perjungia „Async“ kliento kūrimo režimą. Kitaip tariant, kliento įrašus galima kurti asinchroniniu būdu, net jei „Async“ kliento kūrimo režimas išjungtas. Todėl „Commerce“ valdymo srities administratoriai turi sukurti ir suplanuoti pasikartojančią P užduoties paketinę užduotį – **Sinchronizuoti klientus ir verslo partnerius iš asinchroninio režimo** – ir užduotį **1010**, kad „Async“ klientai būtų konvertuojami į „Sync“ klientus „Commerce“ valdymo srityje.

> [!NOTE]
> Jei parinktis **Filtruoti bendrinamas kliento duomenų lenteles** nustatoma kaip **Taip** puslapyje **„Commerce“ kanalo schema** (**Mažmeninės prekybos ir komercijos sąranka \> Valdymo srities sąranka \> „Commerce“ planuoklis \> Kanalo duomenų bazės grupė**), kliento įrašai nesukuriami EKA, veikiant autonominiu režimu. Daugiau informacijos žr. skyriuje [Duomenų pašalinimas veikiant autonominiu režimu](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Papildomi ištekliai

[Kliento atributai](dev-itpro/customer-attributes.md)

[Duomenų pašalinimas veikiant autonominiu režimu](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
