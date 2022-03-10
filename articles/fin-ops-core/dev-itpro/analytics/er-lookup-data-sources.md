---
title: Peržvalgos duomenų šaltinių konfigūravimas, kad būtų galima naudoti ER programai būdingus parametrus
description: Šioje temoje paaiškinama, kaip galite sukonfigūruoti Elektroninių ataskaitų (ER) formatų Peržvalgos duomenų šaltinius, kad būtų galima naudoti ER programai būdingus parametrus.
author: NickSelin
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: c028b01aa2889a517bee69de46411ada12d6fe25
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343434"
---
# <a name="configure-lookup-data-sources-to-use-er-application-specific-parameters"></a>Peržvalgos duomenų šaltinių konfigūravimas, kad būtų galima naudoti ER programai būdingus parametrus 

[!include[banner](../includes/banner.md)]

[Elektroninių ataskaitų (ER)](general-electronic-reporting.md) programai būdingi parametrai leidžia jums konfigūruoti duomenų filtravimą ER formatu, kad jis būtų pagrįstas abstrakčių taisyklių rinkiniu. Šį taisyklių rinkinį galima sukonfigūruoti taip, kad jis naudotų **Peržvalgos** tipo duomenų šaltinį, prieinamą ER formatu. Gali nurodyti realias, ne tik ER komponentų sistemoje taikomas taisykles, – tai galite daryti naudodami vartotojo sąsają (UI), kuri automatiškai sugeneruojama pagal atitinkamo ER formato **Peržvalgos tipo** duomenų šaltinį ir dabartinius juridinio subjekto duomenis. Galiausiai nurodytas taisykles pasieks ER formato **Peržvalgos** duomenų šaltinis, kai šis ER formatas bus įvykdytas.

> [!NOTE]
> Naudokite redaguojamo ER formato sukonfigūruotus duomenų šaltinius, kad nurodytumėte, kurie programos duomenys yra naudojami realių taisyklių konfigūravimui.

Naudokite [ER Operacijų dizaino įrankį](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base), kad atneštumėte **Peržvalgos** tipo duomenų šaltinį į jūsų ER formatą. Duomenų šaltinis turi būti sukonfigūruotas apibūdinti, kaip atrodo jūsų abstrakčios taisyklės, įskaitant:

   - Tam tikro duomenų tipo, kurio reikšmė pateikta, parametrų rinkinį, skirtą vienai taisyklei nurodyti.
   - Tam tikro duomenų tipo vertės tipą, kurį grąžina viena taisyklė, kai ši taisyklė laikoma pačia tinkamiausia iš visų kitų.

Galite konfigūruoti šiuos **Peržvalgos** duomenų šaltinių tipus, atsižvelgdami į reikšmės, kurią grąžina bet kuri konfigūruota taisyklė, tipą:

   - Naudokite **Duomenų modelio\Peržvalgos** tipą, kai modelio išvardijimo reikšmė turi būti grąžinta.
   - Naudokite **„Dynamics 365” Operacijų\Peržvalgos** tipą, kai programos išvardijimo reikšmė arba programos [išplėstinio duomenų tipo](../extensibility/extensible-edts.md) reikšmė turi būti grąžinta.
   - Naudokite **Formatų išvardijimo\Peržvalgos** tipą, kai formato išvardijimo reikšmė turi būti grąžinta.

Šioje iliustracijoje rodoma, kaip formato išvardijimas gali būti konfigūruojamas pavyzdiniame ER formate.

   ![Formatų išvardijimo kaip sukonfigūruoto peržvalgos duomenų šaltinio pagrindo rodymas.](./media/er-lookup-data-sources-img1.gif)

Šioje iliustracijoje rodomi formato komponentus, kurie buvo sukonfigūruoti pranešti apie skirtingų tipų mokesčius kitoje sugeneruotos ataskaitos dalyje.

   ![Formato skyrių rodymas atskirai pranešti apie skirtingo tipo mokesčius.](./media/er-lookup-data-sources-img2.png)

Šioje iliustracijoje rodoma, kaip ER operacijų dizaino įrankis leidžia **Formatų išvardijimo\Peržvalgos** tipo duomenų šaltinio įtraukimą.  Įtrauktas duomenų šaltinis yra sukonfigūruojamas kaip `List of taxation levels` formatų išvardijimo grąžinama vertė.

   ![Formatų išvardijimo\Peržvalgos tipo ER duomenų šaltinio įtraukimas.](./media/er-lookup-data-sources-img3.gif)

Šioje iliustracijoje rodoma, kaip įtrauktas duomenų šaltinis yra konfigūruojamas naudoti **Modelio** duomenų šaltinio įrašų sąrašo **„Model.Data.Tax”** lauką **Kodas** kaip parametrą, kuris turi būti nurodytas kiekvienai sukonfigūruotai taisyklei.

![Įtraukto Formatų išvardijimo\Peržvalgos tipo duomenų šaltinio parametrų konfigūravimas.](./media/er-lookup-data-sources-img4.gif)

Įtrauktas duomenų šaltinis `Model.Data.Tax` yra sukonfigūruotas nurodyti mokesčių kodą kiekvienai sukonfigūruotai taisyklei, pasiekdamas programos lentelės **„TaxTable”** (Mokesčių lentelė) įrašus.

   ![Formatų išvardijimo\Peržvalgos tipo vienos įmonės peržvalgos duomenų šaltinio peržiūra.](./media/er-lookup-data-sources-img5.gif)

Galite nustatyti pasirinkto ER formato peržvalgos taisykles naudodami vartotojo sąsają, kuri yra automatiškai sulygiuota su sukonfigūruoto duomenų šaltinio struktūra. Šiuo metu ši vartotojo sąsają reikalauja, kad kiekvienai taisyklei nurodytumėte grąžintą reikšmę kaip `List of taxation levels` formato išvardijimo reikšmę, taip pat ir mokesčių kodą kaip parametrą.

   ![Sukonfigūruoto duomenų šaltinio taisyklių nustatymas.](./media/er-lookup-data-sources-img6.gif)

Šioje iliustracijoje rodoma, kaip **Apskaičiuoto lauko** tipo duomenų šaltinį `Model.Data.Summary.LevelByLookup` galima sukonfigūruoti taip, kad pateikiant reikiamus parametrus, būtų iškviečiamas sukonfigūruotas **Peržvalgos** duomenų šaltinis. Kad šis iškvietimas būtų apdorotas vykdymo metu, ER pereina per sukonfigūruotų taisyklių sąrašą nustatyta seka, kad rastų pirmos taisyklės, atitinkančios pateiktas sąlygas, vietą. Šiame pavyzdyje tai yra taisyklė, kurioje yra mokesčio kodas, atitinkantis pateiktą kodą. Todėl surandama tinkamiausia taisyklė ir rastai taisyklei sukonfigūruotą išvardijimo reikšmę grąžina šis duomenų šaltinis.

> [!NOTE]
> Kai nerandama jokia taikoma taisyklė, pateikiama išimtis. Norėdami išvengti šių išimčių, taisyklių sąrašo pabaigoje konfigūruokite papildomas taisykles, kad būtų galima tvarkyti atvejus, kai pateikiama nekonfigūruota reikšmė arba nepateikiama jokia reikšmė. Atitinkamai naudokite parinktis **\*Ne tuščia**\* ir **\*Tuščia**\*.  
>
> ![Duomenų šaltinio įtraukimas konfigūruotam Peržvalgos duomenų šaltiniui iškviesti.](./media/er-lookup-data-sources-img7.png)

Kai redaguojamam peržvalgos duomenų šaltiniui nustatote parinktį **Visos įmonės** į **Taip**, jūs įtraukiate naują reikiamą parametrą **Įmonė** į šio duomenų šaltinio parametrų rinkinį. Parametro **Įmonė** reikšmė turi būti nurodyta vykdymo metu, kai iškviečiamas peržvalgos duomenų šaltinis. Kai įmonės kodas nurodomas vykdymo metu, šiai įmonei sukonfigūruotos taisyklės yra naudojamos labiausiai tinkamai taisyklei rasti ir atitinkama reikšmė yra grąžinama. Šioje iliustracijoje rodoma, kaip galite tai atlikti ir kaip pakeičiamas redaguojamo duomenų šaltinio parametrų rinkinys.

   ![Formatų išvardijimo\Peržvalgos tipo kelių įmonių peržvalgos duomenų šaltinio peržiūra.](./media/er-lookup-data-sources-img8.gif)

> [!NOTE]
> Kiekvieną įmonę pasirinkite atskirai, norėdami konfigūruoti šio redaguojamo ER formato peržvalgos duomenų šaltinio taisyklių rinkinį. Vykdymo metu išmetama išimtis, kai kelių įmonių peržvalga yra iškviečiama naudojant įmonės, kurios peržvalgos nustatymas nebuvo baigtas, kodu.
>
> Užtikrinkite, kad suteikėte teises vartotojui, kuris vykdo ER formatą naudodamas visų įmonių **Peržvalgos** duomenų šaltinį, kad būtų galima pasiekti kiekvienos šio duomenų šaltinio aprėptyje esančios įmonės duomenis. Priešingu atveju vykdymo metu pateikiama išimtis.

Pradedant nuo 10.0.19 versijos, prieinamos **Peržvalgos** duomenų šaltinių išplėstinės galimybės. Kai redaguojamam peržvalgos duomenų šaltiniui nustatote parinktį **Išplėstinis** į **Taip**, sukonfigūruotas peržvalgos duomenų šaltinis yra transformuojamas į susistemintą duomenų šaltinį, kuris siūlo papildomas sukonfigūruoto taisyklių rinkinio analizavimo galimybes. Toliau pateiktoje iliustracijoje vaizduojama ši transformacija.

   ![Formatų išvardijimo\Peržvalgos tipo struktūrinio peržvalgos duomenų šaltinio peržiūra.](./media/er-lookup-data-sources-img9.gif)

- Antrinis elementas **Peržvalga** yra sukurtas kaip funkcija, skirta tinkamiausiai taisyklei rasti iš konfigūruojamų taisyklių rinkinio, atsižvelgiant į pateiktą parametrų rinkinį.
- Antrinis elementas **„IsLookupResultSet”** (Ar peržvalgos rezultatas – rinkinys) yra sukurtas kaip funkcija, skirta priimti pateiktą pagrindinio išvardijimo duomenų šaltinio reikšmę ir grąžinti *Bulio logikos* reikšmę **Teisinga**, kai taisyklių rinkinyje yra bent viena taisyklė, kuriai pateikta išvardijimo reikšmė buvo sukonfigūruota kaip grąžinta reikšmė. Ši funkcija grąžina *Bulio logikos* reikšmę **Klaidinga**, kai nėra sukonfigūruotų taisyklių, skirtų pateiktai išvardijimo reikšmei grąžinti.
- Antrinis elementas **Parametras** yra sukurtas kaip funkcija, grąžinanti sukonfigūruotų taisyklių rinkinį kaip įrašų sąrašo įrašus. Grąžintos reikšmės ir sukonfigūruotų taisyklių parametrų rinkinys yra pateikiami kiekviename grąžintame įraše kaip atitinkamų duomenų tipų laukai:

    - Grąžinta vertė pateikiama kaip **Peržvalgos rezultato** laukas.
    - Sukonfigūruoti parametrai pateikiami kaip laukai, turintys parametrų pavadinimus (šiame pavyzdyje – laukas **Kodas**).

Daugiau informacijos apie tai, kaip konfigūruoti **Peržvalgos** duomenų šaltinį, rasite [ER formatų konfigūravimas, kad būtų galima naudoti juridiniam subjektui būdingus parametrus](er-app-specific-parameters-configure-format.md). Norėdami sužinoti, kaip nustatyti Peržvalgos taisykles, skaitykite [ER formato parametrų nustatymas juridiniam subjektui](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[ER formatų konfigūravimas, kurį atlikus naudojami juridiniam subjektui nurodyti parametrai](er-app-specific-parameters-configure-format.md)

[ER formato parametrų nustatymas kiekvienam juridiniam subjektui](er-app-specific-parameters-set-up.md)
