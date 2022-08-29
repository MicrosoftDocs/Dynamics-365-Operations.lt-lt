---
title: Warehouse Management mobiliųjų įrenginių programėlės skatinamų laukų konfigūravimo žingsniai
description: Šiame straipsnyje aprašoma, kaip skatina ir išryškina konkrečią informaciją apie bet kuriuos sandėlio valdymo mobiliosios programos užduočių eigos žingsnius.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 3451b1aec525cd0738af558b183f8676d20294a0
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336072"
---
# <a name="configure-promoted-fields-for-steps-in-the-warehouse-management-mobile-app"></a>Warehouse Management mobiliųjų įrenginių programėlės skatinamų laukų konfigūravimo žingsniai

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Šiame straipsnyje aprašytos funkcijos taikomos tik naujai sandėlio valdymo mobiliąją programai. Jie neturi įtakos senai sandėlio programai, kuri dabar pasenusi.

Šiame straipsnyje aprašoma, kaip skatina ir išryškina konkrečią informaciją apie bet kuriuos sandėlio valdymo mobiliosios programos užduočių eigos žingsnius. Ši galimybė gali padėti darbuotojams sutelkti dėmesį į svarbiausius laukus, kai jie dirba sraute. Kiekviename kiekvieno proceso etape administratoriai gali pasirinkti, kuriuos laukus skatinate ir kuriuos laukus žymėti.

## <a name="enable-promoted-fields-in-your-system"></a>Įjunkite skatinamuosius laukus savo sistemoje

Jei paleisite tiekimo grandinės valdymo versiją 10.0.28 ar ankstesne, prieš nustatę skatinamą lauką, turite atlikti toliau nurodytą procedūrą, kad įgalintumėte reikiamas funkcijas ir sugeneruotumėte būtinus laukų pavadinimus sandėlio valdymo mobiliųjų įrenginių programoje. Jei paleisite tiekimo grandinės valdymo 10.0.29 arba vėlesnę versiją, šios funkcijos yra privalomos ir negali būti išjungtas, todėl galite praleisti šią procedūrą.

1. Eikite į **Sistemos administravimas \> Darbo sritys \> Funkcijų valdymas**. (Žr. [Funkcijų valdymo apžvalga](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), skirta daugiau informacijos apie šį puslapį.)
1. Įsitikinkite, kad *sandėlio programos veiksmo* instrukcijų funkcija jūsų sistemai įjungta. Ši funkcija yra būtina *Warehouse Management programos skatinamų laukų* sąlyga. Kaip tiekimo grandinės valdymo versija 10.0.29, ji yra privaloma ir negali būti išjungta. Daugiau informacijos apie *Warehouse programos veiksmų instrukcijų* funkciją žr. [Warehouse Management mobiliosios programos veiksmų pavadinimų ir instrukcijų pritaikymas](mobile-app-titles-instructions.md).
1. Įsitikinkite, kad *sandėlio programos skatinami* laukų funkcija jūsų sistemai įjungta. Tai šiame straipsnyje aprašyta funkcija. Kaip tiekimo grandinės valdymo versija 10.0.29, ji yra privaloma ir negali būti išjungta.
1. Warehouse Management mobiliojoje programėlėje atnaujinkite laukų pavadinimus eidami į **Warehouse Management \> Sąranka \> Mobilus įrenginys \> Warehouse programėlė** ir pasirinkite **Kurti numatytąjį nustatymą**. Pakartokite šį veiksmą su kiekvienu juridiniu subjektu (įmone), kuriame naudojate sandėlio valdymo mobiliąją programą. Daugiau informacijos rasite [Sandėlio valdymo mobiliųjų įrenginių programėlės laukų konfigūravimas](configure-app-field-names-priorities-warehouse.md).

## <a name="configure-promoted-fields-from-a-menu-specific-override"></a>Konfigūruokite skatinamus laukus iš meniu specifinio keitimo

Naudokite toliau nurodytą procedūrą, kad nustatytumėte skatinamus laukus.

1. Sukurkite meniu specifinį atnaujinimą, skirtą atitinkamo meniu ir atlikite veiksmus, kaip aprašyta [Warehouse Management mobiliosios programos veiksmų pavadinimų ir instrukcijų pritaikymas](mobile-app-titles-instructions.md).
1. Raskite veiksmo **Veiksmo ID** ir **Menu prekės pavadinimas** vertės, kurias norite redaguoti ir tada pasirinkite vertę **Veiksmo ID** stulpelyje.
1. Pasirodžiusiame puslapyje **Pasirinkti skatinamus laukus** FastTab skirtuke pasirinkite **Pasirinkti laukus** įrankių juostoje.
1. Dialogo lange **Skatinami laukai** pasirinkite laukus, kuriuos norite skatinti. Taip pat galite pažymėti iki dviejų pasirinktų laukų. Paryškinti laukai Warehouse Management mobiliųjų įrenginių programoje bus rodomi paryškinti. Kai pasirenkate laukus, apsvarstykite faktą, kad kai kurie ekranai gali būti pakankamai dideli, kad būtų rodomi tik vienas ar du pagrindiniai skatinami laukai. Pvz., kuriame parodyta, kaip naudoti šiuos parametrus, žr. scenarijų toliau šiame straipsnyje.

    > [!NOTE]
    > **Galimų laukų** sąrašas ribojamas iki laukų, kurie gali būti rodomi meniu elementui. Tačiau kiti faktoriai (pvz., prekės sudėtis) lemia, ar laukas iš tikrųjų rodomas Warehouse Management mobilioje programoje. Jei sukonfigūravote skatinamus laukus, Warehouse Management mobiliosios programos pagrindiniame puslapyje bus rodomi tik pasirinkti laukai. Tačiau darbuotojai vis dar gali peržiūrėti likusius laukus pasispaudę ant informacijos puslapio.

1. Pasirinkite **Gerai** savo nustatymų pritaikymui. Jūsų pasirinkti laukai dabar pateikti **Pasirinkti skatinamus laukus** "FastTab" skirtuke.

## <a name="example-scenario"></a>Pavyzdinis scenarijus

### <a name="enable-sample-data"></a>Duomenų pavyzdžių įgalinimas

Norėdami naudoti nurodytus pavyzdinius įrašus ir reikšmes, norėdami dirbti naudodami šį scenarijų, turite naudoti sistemą, kurioje įdiegti standartiniai [demonstraciniai](../../fin-ops-core/fin-ops/get-started/demo-data.md) duomenys. Prieš pradėdami turite pasirinkti juridinį subjektą **USMF**.

### <a name="configure-sales-picking-with-promoted-steps-on-the-license-plate-step"></a>Konfigūruokite pardavimų pasirinkimą naudojant skatinamus veiksmus licencijos lentelės veiksme.

Šios procedūros metu sukonfigūruosite skatinamus ir paryškintus laukus **Pardavimo pasirinkimo** meniu elemento licencijos lentelės veiksme.

1. Eikite į **Warehouse management  \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio veiksmai**.
1. Raskite veiksmo ID, kuris vadinamas *LicensePlateId* ir pasirinkite jį.
1. Veiksmų srityje pasirinkite **Įtraukti veiksmo konfigūraciją**.
1. Iššokančiame dialogo lange naudokite **Meniu elemento** lauką, kad rastumėte ir pasirinktumėte *Pardavimų pasirinkimą*.
1. Pasirinkite **Gerai**.
1. Rodomas ką tik sukurto pakeistos informacijos puslapis. Puslapyje **Pasirinkti skatinamus laukus** FastTab skirtuke pasirinkite **Pasirinkti laukus** įrankių juostoje.
1. Dialogo lange **Skatinami laukai** galite pasirinkti laukus, kuriuos norite skatinti ir skatinti. Sąraše **Galimi laukai** raskite ir pasirinkite šiuos laukus bei naudokite mygtukus perkelkite juos į **Pasirinktų laukų** sąrašą:

    - Vieta
    - Prekė
    - Produkto pavadinimas
    - Atsargų būsena

1. Naudokite rodyklių aukštyn ir žemyn mygtukus norėdami tinkinti laukų tvarką **Pasirinkti laukai** sąraše. Warehouse Management mobilioje programoje laukai bus rodomi tokia tvarka, kaip nustatėte čia.
1. Pasirinkite lauką **Vieta**, o tada pasirinkite **Paryškinti**.
1. Pasirinkite **Gerai** kad išsaugotumėte konfigūraciją.

### <a name="view-the-promoted-fields-in-the-warehouse-management-mobile-app"></a>Warehouse Management mobiliųjų įrenginių programėlėje peržiūrėkite skatinamus laukus.

Šioje procedūroje atidarysite Warehouse Management mobiliąją programą ir galėsite peržiūrėti laukus, kuriuos skatinate ir išryškinote ankstesnėje procedūroje.

1. Microsoft Dynamics 365 Supply Chain Management sukurkite pardavimo užsakymą, kuriame reikės atlikti pasirinkimo veiksmą, kad būtų paimta iš vietos, kuri yra sekama pagal licencijos lentelę. Tada išleiskite pardavimo užsakymą į sandėlį. Pasižymėkite rodomo darbo ID, kuris yra generuojamas.
1. Atidarykite Warehouse Management mobiliųjų įrenginių programėlę ir prisiregistruokite sandėlyje 24. (Standartiniuose demonstraciniuose duomenyse prisijunkite kaip vartotojo ID naudodami *24*, o kaip slaptažodį – *1*.)
1. Pasirinkite **Išsiuntimo** meniu ir tada pasirinkite **Pardavimo pasirinkimas** meniu elementą.
1. Norėdami įvesti darbo ID, kuris buvo sugeneruotas 1 veiksmu, vadovaukitės ekrane pateikiamomis duomenų įvedimo instrukcijomis.
1. Žingsnyje, kuriame yra tekstas **Nuskaityti licencijos lentelę** turėtumėte matyti keitimus, atliktus informacijos puslapyje. Laukai rodomi tokia tvarka, kurią nustatėte skatinamius laukus, o laukas **Vieta** rodomas paryškintu šriftu.
