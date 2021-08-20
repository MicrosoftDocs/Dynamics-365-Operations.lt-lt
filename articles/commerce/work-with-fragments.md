---
title: Darbas su fragmentais
description: Šioje temoje aprašoma, kodėl, kada ir kaip naudoti fragmentus programoje „Microsoft Dynamics 365 Commerce“.
author: phinneyridge
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 35a19f064b63ce476252064253032d35697bd69c84c4c93db1d0349a57527c2a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776199"
---
# <a name="work-with-fragments"></a>Darbas su fragmentais 

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kodėl, kada ir kaip naudoti fragmentus programoje „Microsoft Dynamics 365 Commerce“.

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

![Iliustracija, kurioje rodoma, kaip fragmentai gali būti naudojami bendrai naudojamų modulių konfigūracijų kūrimui centralizuoti visoje elektroninės prekybos svetainėje.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>Fragmento kūrimas

Galite sukurti naują fragmentą arba kaip fragmentą įrašyti esamą modulio konfigūraciją.

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>Esamos modulio konfigūracijos įrašymas kaip fragmento

Norėdami anksčiau sukonfigūruotą modulį konvertuoti į daugkartinio naudojimo fragmentą „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.

1. Atidarykite puslapį arba šabloną, kuriame yra modulis, kurį norite konvertuoti į fragmentą.
1. Struktūros srities kairėje arba tiesiai vizualinėje puslapio daryklėje pasirinkite anksčiau konfigūruotą modulį.
1. Struktūros srityje arba pasirinkto modulio įrankių juostoje vizualinėje puslapio daryklėje pasirinkite daugtaškį (**...**), esantį šalia modulio pavadinimo. 
1. Pasirinkite **Bendrinti kaip fragmentą**. 
1. Dialogo lange **Įrašyti kaip fragmentą** įveskite fragmento pavadinimą.
1. Pasirinkite **Gerai**, kad modulių konfigūraciją įrašytumėte kaip fragmentą, kurį galima įtraukti į kitus puslapius.
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment.](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a>Kurti naują fragmentą

Norėdami sukurti naują fragmentą „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.

1. Kairėje naršymo srityje pasirinkite **Fragmentai**.
1. Pasirinkite **Naujas**. Pasirodys dialogo langas **Naujas fragmentas**, kuriame rodomi visi galimi modulių tipai. Kaip minėta anksčiau, fragmentai gali būti kuriami naudojant bet kokį modulio tipą.
1. Pasirinkite fragmento modulio tipą.

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment.](./media/fragment-nav-menu.png)-->
> [!TIP]
> Pasirinkdami bendrąjį konteinerio modulio tipą, gausite daugiausiai lankstumo, kai vėliau reikės atnaujinti ir konfigūruoti fragmentą.

## <a name="add-remove-or-edit-fragments-on-a-page"></a>Puslapio fragmentų įtraukimas, pašalinimas arba redagavimas

Tolesnėse procedūrose aprašoma, kaip įtraukti fragmentų, juos pašalinti ir redaguoti.

### <a name="add-a-fragment"></a>Fragmento įtraukimas

Norėdami įtraukti fragmentą „Commerce” svetainių daryklės puslapį, atlikite toliau pateiktus veiksmus.

1. Struktūros juostoje kairėje arba tiesiai vizualinėje puslapio daryklėje pasirinkite konteinerį arba vietą, kur būtų galima įtraukti antrinius modulius.
1. Pasirinkite daugtaškį (**...**) šalia talpyklos ar vietos pavadinimo.  Arba, jei naudojate vizualinę puslapio daryklę, pasirinkite pliuso simbolį (**+**).  
1. Pasirinkite **Įtraukti fragmentą**.
    <!-- ![A screen capture of how to add an existing fragment to a slot or container.](./media/add-fragment.png)-->
 
    > [!NOTE]
    > Jei konteineris arba vieta nepalaiko naujų antrinių modulių, parinktis **Įtraukti fragmentą** nepasiekiama.
    
1. Dialogo lange **Pasirinkti fragmentą** ieškokite ir pasirinkite fragmentą, kurį norite įtraukti. Jei sąraše nėra pasiekiamų fragmentų, pirmiausia gali reikėti sukurti fragmentą naudojant pasirinkto konteinerio ar vietos palaikomą modulio tipą.
1. Pasirinkite fragmentą, kurį norite įtraukti į konteinerį arba vietą jūsų puslapyje.
<!--    ![A screen capture of the fragment picker modal window.](./media/fragment-picker.png)-->

> [!NOTE]
> Konteineryje arba vietoje leidžiami moduliai nustatomi puslapio šablone arba pačių modulių aprašuose.

### <a name="remove-a-fragment"></a>Fragmento šalinimas

Norėdami pašalinti fragmentą iš „Commerce” svetainių daryklės puslapio vietos ar konteinerio, atlikite toliau pateiktus veiksmus.

1. Išorinėje kairinėje juostoje pasirinkite elipsę (**...**) šalia šalinamo fragmento pavadinimo ir tuomet pasirinkite šiukšlių dėžės simbolį.  Arba galite pasirinkite fragmentą vizualinėje puslapio daryklėje ir pasirinkti šiukšlių dėžės simbolį fragmento įrankių juostoje.
1. Kai būsite paraginti patvirtinti, kad norite pašalinti fragmentą, pasirinkite **Gerai**.

> [!NOTE]
> Kai pašalinate fragmentą iš puslapio, iš šio puslapio tik pašalinate nuorodą į tą fragmentą. Svetainėje fragmentas **nepanaikinamas**. Norint panaikinti fragmentus iš svetainės, reikia naudoti fragmento inspektoriaus vartotojo sąsają (UI). Panaikinti fragmentus iš svetainės galite tik tuo atveju, jei jie nėra nurodyti jokiuose puslapiuose, šablonuose ar kituose fragmentuose.

### <a name="edit-a-fragment"></a>Fragmento redagavimas

Norint redaguoti fragmentus reikia naudoti fragmentų rengyklės UI. Toks apribojimas yra numatytas. Jis padeda užtikrinti, kad autoriai konkretaus puslapio modulių redagavimo proceso nesupainios su fragmentų, kurie gali būti bendrai naudojami daug puslapių, redagavimo procesu.

Norėdami redaguoti fragmentą „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.

1. Kairėje naršymo srityje pasirinkite **Fragmentai**.
1. Dalyje **Fragmentai** pasirinkite fragmentą, kurį norite redaguoti.
1. Pagal poreikius redaguokite fragmento modulio ypatybes ir struktūrą. Šis procesas panašus į modulių, kurie redaguojami puslapio rengyklės rodinyje, redagavimo procesą.

Fragmentą taip pat galite redaguoti pasirinkę jį puslapyje, šablone arba pirminiame fragmente, o tada dešinėje pusėje esančioje ypatybių srityje pasirinkę **Redaguoti fragmentą**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Šablonų ir maketų apžvalga](templates-layouts-overview.md)

[Darbas su šablonais](work-with-templates.md)

[Darbas su esamais maketais](work-with-layouts.md)

[Darbas su publikavimo grupėmis](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
