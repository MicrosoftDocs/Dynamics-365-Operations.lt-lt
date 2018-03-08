---
title: "Produktų ieška ir klientų ieška naudojant EKA"
description: "Šioje temoje apžvelgiama, kaip patobulinta „Dynamics 365 for Retail“ produktų ir klientų ieškos funkcija."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 08/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 5f6f9a02b20549a75941d367c1b46e3439360078
ms.contentlocale: lt-lt
ms.lasthandoff: 01/19/2018

---

# <a name="overview-of-product-and-customer-search-in-point-of-sale"></a>Produktų ir klientų ieškos elektroniniame kasos aparate apžvalga

[!include[banner](includes/banner.md)]

Į modernųjį elektroninį kasos aparatą (MEKA) ir debesies elektroninį kasos aparatą (DEKA) įtraukta lengvai naudojama funkcija, parduotuvės darbuotojams leidžianti greitai ieškoti produktų ir klientų. MEKA ir DEKA viršuje visada yra ieškos juosta, kad darbuotojai galėtų greitai rasti produktus ir klientus.

Darbuotojai produktų gali ieškoti asortimentuose ir kataloguose, susietuose su dabartine parduotuve, bei asortimentuose ir kataloguose, susietuose su bet kuria kita įmonės parduotuve. Todėl kasininkai gali parduoti ir grąžinti į parduotuvės asortimentą neįtrauktus produktus. Panašiai darbuotojai gali ieškoti klientų, susietų su dabartine parduotuve arba bet kuria kita įmonės parduotuve. Be to, darbuotojai gali ieškoti klientų, susietų su kita pirminės organizacijos įmone.

## <a name="product-search"></a>Produktų paieška 

Pagal numatytuosius parametrus produktų ieškoma parduotuvės asortimente. Šis ieškos tipas vadinamas *vietine produktų ieška*. Tačiau darbuotojai gali lengvai pereiti į bet kokį su dabartine parduotuve susietą katalogą arba jie gali ieškoti kitoje parduotuvėje. Šis ieškos tipas vadinamas *nuotoline produktų ieška*. Norėdami pakeisti katalogą, pasirinkite kairėje puslapio pusėje esantį mygtuką **Kategorijos**. Pasirodžiusios srities viršuje pasirinkite mygtuką **Keisti katalogą**, tada pasirinkite vieną iš galimų katalogų, kad jį galėtumėte naršyti. Sistema pasirinktame kataloge ieškos produktų.

Puslapyje **Keisti katalogą** darbuotojai gali lengvai pasirinkti bet kurią parduotuvę arba produktų jie gali ieškoti visose parduotuvėse.

![Katalogo keitimas](./media/Changecatalog.png "Katalogo keitimas")
 
Atliekant vietinę produktų iešką, ieškoma tolesnėse produktų ypatybėse.

- Produkto numeris
- Produkto pavadinimas
- aprašymas
- Dimensijos
- Brūkšninis kodas
- Ieškos pavadinimas

### <a name="enhancements-to-local-product-searches"></a>Vietinių produktų ieškų patobulinimai

Vietinių produktų ieškų veikimas dabar patogesnis vartotojui. Atlikti tolesni patobulinimai.

- Į ieškos juostą įtraukti produktų ir klientų išplečiamieji meniu, kad darbuotojai prieš atlikdami iešką galėtų pasirinkti **Produktas** arba **Klientas**. Pagal numatytuosius parametrus pasirinkta **Produktas**, kaip parodyta tolesnėje iliustracijoje.
- Atlikdami ieškas su keliais raktažodžiais (t. y., atlikdami ieškas, kuriose naudojami ieškos terminai), mažmenininkai gali sukonfigūruoti, ar į ieškos rezultatus reikia įtraukti rezultatus, atitinkančius bet kurį ieškos terminą, ar tik tuos rezultatus, kurie atitinka visus ieškos terminus. Šis parametras pasiekiamas naujoje EKA funkcijų profilio grupėje pavadinimu **Produktų ieška**. Numatytasis parametras yra **Atitinka bet kurį ieškos terminą**. Šis parametras taip pat yra rekomenduojamas parametras. Kai naudojamas parametras **Atitinka bet kurį ieškos terminą**, kaip rezultatai pateikiami visi produktai, visiškai ar iš dalies atitinkantys vieną ar kelis ieškos terminus, o rezultatuose didėjimo tvarka surikiuojami produktai su daugiausiai raktažodžių atitikčių (visiškų arba dalinių).

    Naudojant parametrą **Atitinka visus ieškos terminus**, pateikiami tik tie produktai, kurie atitinka visus ieškos terminus (visiškai arba iš dalies). Šis parametras naudingas, kai produktų pavadinimai yra ilgi ir darbuotojai ieškos rezultatuose nori matyti tik ribotą produktų skaičių. Tačiau šio tipo ieška turi du tolesnius apribojimus.

    - Ieška atliekama atskirose produktų ypatybėse. Pavyzdžiui, pateikiami tik tie produktai, kurių bent vienoje ypatybėje yra visi ieškomi raktažodžiai.
    - Dimensijose neieškoma.

- Mažmenininkai dabar produktų iešką gali sukonfigūruoti taip, kad, vartotojams vedant produktų pavadinimus, būtų rodomi ieškos pasiūlymai. Naujas šios funkcijos parametras pasiekiamas EKA funkcijų profilio grupėje pavadinimu **Produktų ieška**. Parametro pavadinimas yra **Vedant tekstą rodyti ieškos pasiūlymus**. Ši funkcija darbuotojams gali padėti greitai rasti ieškomą produktą, nes jiems nereikia rankiniu būdu įvesti viso pavadinimo.
- Produktų ieškos algoritmas ieškomų terminų dabar taip pat ieško produkto ypatybėje **Ieškos pavadinimas**.

![Produktų pasiūlymai](./media/Productsuggestions.png "Produktų pasiūlymai")

## <a name="customer-search"></a>Kliento ieška

Naudojant klientų iešką, įvairiais tikslais ieškoma klientų. Pavyzdžiui, kasininkai gali norėti peržiūrėti kliento pageidavimų sąrašą ar pirkimo istoriją, arba klientą įtraukti į operaciją. Jei ieškoma naudojant kelis raktažodžius, klientų ieškos algoritmas pateikia visus klientus, kurie atitinka bet kurį iš ieškomų raktažodžių. Tačiau daugiausia raktažodžių atitinkantys klientai rodomi rezultatų viršuje. Toks veikimo būdas yra analogiškas kitų ieškos mechanizmų rezultatų rodymo būdui. Pirmiausia jie rodo rezultatus, atitinkančius daugiausia ieškomų terminų, o tada – rezultatus, ieškos raktažodžius atitinkančius iš dalies. Toks veikimo būdas kasininkams padeda situacijose, kai ieškodami jie naudoja kelis raktažodžius, tačiau viename iš jų yra rašybos klaida.

Pagal numatytuosius parametrus klientų ieškoma su parduotuve susietose klientų adresų knygelėse. Šis ieškos tipas vadinamas *vietine klientų ieška*. Tačiau darbuotojai klientų taip pat gali ieškoti visuotinai. Kitaip tariant, jie gali ieškoti visose įmonės parduotuvėse ir visuose kituose juridiniuose subjektuose. Šis ieškos tipas vadinamas *nuotoline klientų ieška*.

Norėdami ieškoti visuotinai, darbuotojai gali pasirinkti puslapio apačioje esantį mygtuką **Filtruoti rezultatus**, o tada pasirinkti parinktį **Ieškoti visose parduotuvėse**, kaip parodyta tolesnėje iliustracijoje. Tokiu atveju pateikiami ne tik klientai. Taip pat pateikiamos visų tipų šalys, priklausančios bet kuriai būstinės adresų knygelei. Šios šalys – tai darbininkai, tiekėjai, kontaktai ir konkurentai.

> [!NOTE]
> Kad nuotolinė klientų ieška pateiktų rezultatų, reikia įvesti mažiausiai keturis simbolius.

Atliekant nuotolinę klientų iešką, kitų juridinių subjektų klientų ID nerodomi, nes dabartinėje įmonėje tų šalių klientų ID nėra sukurta. Tačiau, jei darbuotojas atidaro kliento informacijos puslapį, sistema automatiškai sugeneruoja šalies kliento ID ir su klientu susieja parduotuvės klientų adresų knygeles. Todėl klientas bus matomas vėliau atliekamose vietinėse parduotuvių ieškose.

![Visuotinė klientų ieška](./media/Globalcustomersearch.png "Visuotinė klientų ieška")

### <a name="enhancements-to-local-customer-searches"></a>Vietinių klientų ieškų patobulinimai

Atlikdami vietines klientų ieškas darbuotojai klientus gali greitai surasti pagal telefono numerį. Darbuotojams nereikia įvesti jokių specialių simbolių, įtrauktų į kliento telefono numerį, pvz., tarpų, brūkšnelių ar skliaustelių. Nors kasininkai telefonų numerius gali saugoti bet kokiu formatu (pavyzdžiui, jie gali įtraukti skliaustelių, brūkšnelių, simbolių ir t. t.), klientų jie gali ieškoti įvesdami telefono numerio dalį. Jei, įvesdamas telefono numerį, kasininkas įtraukė specialių simbolių, kiti kasininkai klientą gali rasti įvesdami po specialių simbolių rodomus skaitmenis. Pavyzdžiui, jei kliento telefono numeris buvo įvestas kaip **123-456-7890**, kasininkas kliento gali ieškoti įvesdamas **123**, **456**, **7890** arba **1234567890**, arba įvesdamas pirmuosius keletą telefono numerio skaitmenų.

