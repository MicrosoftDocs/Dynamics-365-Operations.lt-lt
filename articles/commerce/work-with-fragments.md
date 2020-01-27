---
title: Darbas su fragmentais
description: Šioje temoje aprašoma, kodėl, kada ir kaip naudoti fragmentus programoje „Microsoft Dynamics 365 Commerce“.
author: v-chgri
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 32482538b2913e6585257bcf7a1cbe780d3cdd30
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914705"
---
# <a name="work-with-fragments"></a>Darbas su fragmentais 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kodėl, kada ir kaip naudoti fragmentus programoje „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūrėti

Fragmentai leidžia centralizuotai kurti modulių konfigūracijas, kurias reikia pakartotinai naudoti jūsų svetainėje. Pavyzdžiui, antraštės, poraštės ir reklamos juostos dažnai sukonfigūruojamos kaip fragmentai, nes jos yra bendrai naudojamos daug puslapių. Fragmentus galima laikyti miniatiūriniais tinklalapiais, kuriuos galima įtraukti į kitus svetainės puslapius. Fragmentai turi savo ciklą. Kitaip tariant, jie kuriami, nurodomi, atnaujinami ir naikinami kaip nepriklausomi kūrimo įrankių objektai.

Sukonfigūruotus fragmentus galima naudoti ten, kur svetainės struktūroje galima naudoti modulius. Fragmentai gali būti nurodomi puslapiuose, maketuose, šablonuose ir kituose fragmentuose.

> [!NOTE]
> Fragmentai gali būti įdedami kituose fragmentuose iki septynių lygių gylio.

Pavyzdžiui, jei norite reklamuoti sezoninį įvykį daugelyje savo svetainės puslapių, galite naudoti fragmentą. Pirmas naujo fragmento kūrimo veiksmas – modulio tipo, nuo kurio norite pradėti, pasirinkimas. Pavyzdžiui, galite kurti fragmentą naudodami pagrindinės reklamos juostos modulį.

> [!NOTE]
> Fragmentus galima kurti naudojant bet kokį modulio tipą.

Tada pagrindinės reklamos juostos fragmentą galite konfigūruoti su konkrečiu reklaminiu turiniu. Jei reikia, taip pat galite jį lokalizuoti. Tada naujas atskiras pagrindinės reklamos juostos fragmentas gali būti naudojamas visoje svetainėje kaip iš anksto sukonfigūruotas modulis. Jį galite lengvai įtraukti į šablonus, konkrečius puslapius ar kitus fragmentus, kuriuose yra pagrindinės reklamos juostos modulių.

Visos vietos, į kurias įtrauktas fragmentas, yra nuorodos jūsų sukurtą centrinį pagrindinės reklamos juostos fragmentą. Jeigu publikuosite fragmento keitimus, tie pakeitimai bus iš karto rodomi visose vietose, kuriose fragmentas yra nurodytas svetainėje. Todėl fragmentai – galingas ir veiksmingas būdas pakartotinai naudoti ir centralizuotai valdyti modulių konfigūracijas svetainėje. Veiksmingai juos naudodami galite smarkiai padidinti lankstumą ir padėti sumažinti išlaidas, susijusias su svetainės turinio valdymu.

Toliau pateiktame paveikslėlyje rodoma, kaip fragmentai gali būti naudojami bendrai naudojamų modulių konfigūracijų kūrimui centralizuoti visoje el. prekybos svetainėje.

![Iliustracija, kurioje rodoma, kaip fragmentai gali būti naudojami bendrai naudojamų modulių konfigūracijų kūrimui centralizuoti visoje el. prekybos svetainėje](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>Fragmento kūrimas

Galite sukurti naują fragmentą arba kaip fragmentą įrašyti esamą modulio konfigūraciją.

### <a name="create-a-new-fragment"></a>Naujo fragmento kūrimas

Norėdami sukurti naują fragmentą, atlikite toliau nurodytus veiksmus.

1. Kairėje naršymo srityje pasirinkite **Fragmentai**.
1. Pasirinkite **Naujas puslapio fragmentas**. Pasirodys dialogo langas, kuriame rodomi visi galimi modulių tipai. Kaip minėta anksčiau, fragmentai gali būti kuriami naudojant bet kokį modulio tipą.
1. Pasirinkite fragmento modulio tipą, tada pasirinkite **Gerai**.

    > [!TIP]
    > Pasirinkdami bendrąjį konteinerio modulio tipą, gausite daugiausiai lankstumo, kai vėliau reikės atnaujinti ir konfigūruoti fragmentą.

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>Esamos modulio konfigūracijos įrašymas kaip fragmento

Norėdami anksčiau sukonfigūruotą modulį konvertuoti į daugkartinio naudojimo fragmentą, atlikite šiuos veiksmus.

1. Atidarykite puslapį arba šabloną, kuriame yra modulis, kurį norite konvertuoti į fragmentą.
1. Struktūros srityje kairėje šalia modulio pavadinimo pasirinkite daugtaškio mygtuką (**...**), tada pasirinkite **Įrašyti kaip fragmentą**. Atsiranda dialogo langas.
1. Įveskite fragmento pavadinimą ir metaduomenis.
1. Pasirinkite **Gerai**, kad modulių konfigūraciją įrašytumėte kaip fragmentą, kurį galima įtraukti į kitus puslapius.

## <a name="add-remove-or-edit-fragments-on-a-page"></a>Puslapio fragmentų įtraukimas, pašalinimas arba redagavimas

Tolesnėse procedūrose aprašoma, kaip įtraukti fragmentų, juos pašalinti ir redaguoti.

### <a name="add-a-fragment"></a>Fragmento įtraukimas

Norėdami į puslapį įtraukti fragmentą, atlikite toliau nurodytus veiksmus.

1. Struktūros srityje kairėje pasirinkite konteinerį arba vietą, į kuriuos galima įtraukti antrinių modulių.
1. Šalia konteinerio arba vietos pavadinimo pasirinkite daugtaškio mygtuką, tada pasirinkite **Įtraukti fragmentą**. Atsiranda dialogo langas.

    > [!NOTE]
    > Jei konteineris arba vieta nepalaiko naujų antrinių modulių, parinktis **Įtraukti fragmentą** nepasiekiama.

1. Dialogo lange raskite ir pasirinkite fragmentą, kurį norite įtraukti. Jei sąraše nėra pasiekiamų fragmentų, pirmiausia gali reikėti sukurti fragmentą naudojant pasirinkto konteinerio ar vietos palaikomą modulio tipą.
1. Pasirinkite **Gerai**, kad pasirinktą fragmentą įtrauktumėte į pasirinktą konteinerį arba vietą jūsų puslapyje.

> [!NOTE]
> Konteineryje arba vietoje leidžiami moduliai nustatomi puslapio šablone arba pačių modulių aprašuose.

### <a name="remove-a-fragment"></a>Fragmento šalinimas

Norėdami fragmentą pašalinti iš vietos arba konteinerio puslapyje, atlikite šiuos veiksmus.

1. Struktūros srityje kairėje šalia fragmento, kurį norite pašalinti, pavadinimo pasirinkite daugtaškio mygtuką, tada pasirinkite šiukšliadėžės mygtuką.
1. Kai būsite paraginti patvirtinti, kad norite pašalinti fragmentą, pasirinkite **Gerai**.

> [!NOTE]
> Kai pašalinate fragmentą iš puslapio, iš šio puslapio tik pašalinate nuorodą į tą fragmentą. Svetainėje fragmentas **nepanaikinamas**. Norint panaikinti fragmentus iš svetainės, reikia naudoti fragmento inspektoriaus vartotojo sąsają (UI). Panaikinti fragmentus iš svetainės galite tik tuo atveju, jei jie nėra nurodyti jokiuose puslapiuose, šablonuose ar kituose fragmentuose.

### <a name="edit-a-fragment"></a>Fragmento redagavimas

Norint redaguoti fragmentus reikia naudoti fragmentų rengyklės UI. Toks apribojimas yra numatytas. Jis padeda užtikrinti, kad autoriai konkretaus puslapio modulių redagavimo proceso nesupainios su fragmentų, kurie gali būti bendrai naudojami daug puslapių, redagavimo procesu.

Norėdami redaguoti fragmentą, atlikite toliau nurodytus veiksmus.

1. Kairėje naršymo srityje pasirinkite **Fragmentai**.
1. Dalyje **Fragmentai** pasirinkite fragmentą, kurį norite redaguoti.
1. Pagal poreikius redaguokite fragmento modulio ypatybes ir struktūrą. Šis procesas panašus į modulių, kurie redaguojami puslapio rengyklės rodinyje, redagavimo procesą.

Fragmentą taip pat galite redaguoti pasirinkę jį puslapyje, šablone arba pirminiame fragmente, o tada dešinėje pusėje esančioje ypatybių srityje pasirinkę **Redaguoti fragmentą**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Šablonų ir maketų apžvalga](templates-layouts-overview.md)

[Darbas su šablonais](work-with-templates.md)

[Darbas su esamais maketais](work-with-layouts.md)

[Darbas su publikavimo grupėmis](publish-groups.md)
