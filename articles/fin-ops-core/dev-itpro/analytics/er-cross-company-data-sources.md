---
title: Visos įmonės duomenų šaltiniai elektroninėse ataskaitose (ER)
description: Šioje temoje paaiškinta, kaip galima naudoti visos įmonės duomenų šaltinius elektroninėse ataskaitose (ER).
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERModelMappingDesigner, ERFormatMappingLegalEntityFilterTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 1a5c05b65c9022220056947471e95b703d923dc5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680835"
---
# <a name="cross-company-data-sources-in-electronic-reporting-er"></a>Visos įmonės duomenų šaltiniai elektroninėse ataskaitose (ER)

[!include[banner](../includes/banner.md)]

Galite sukurti elektroninių ataskaitų (ER) formatus, norėdami generuoti siunčiamus dokumentus įvairiais formatais. Kai dokumentas sugeneruotas, ER formatas iškviečia duomenų šaltinius, kurie buvo sukonfigūruoti atitinkamame ER modelio susiejime. Norėdami sukonfigūruoti prieigą prie programos lentelių įrašams nuskaityti, galite naudoti ER duomenų šaltinius, kurių tipas yra **Lentelės įrašai**. Kai pasiekiama lentelė yra bendrai naudojama lentelė (t. y., lentelė, kurioje duomenys įrašomi be įmonės identifikatorius), šis duomenų šaltinis pateikia visus įrašus. Kai pasiekiama lentelė yra nuo įmonės priklausanti lentelė (t. y., kai duomenys įrašomi vienoje įmonėje), šis duomenų šaltinis pateikia tik tuos įrašus, kurie buvo įrašyti šiai įmonei (t. y., pagal įmonės kontekstą, pagal kurį vykdomas ER formatas).

Kiekvienas susiejimo modelio duomenų šaltinis, kurio tipas **Lentelės įrašai**, dabar gali būti pažymėtas kaip visos įmonės duomenų šaltinis. Todėl norėdami pasiekti visos įmonės duomenis programos lentelėse, galite naudoti duomenų šaltinius, kurių tipas yra **Lentelės įrašai**.

Jei duomenų šaltinį pažymėsite kaip visos įmonės, taikomas toks veikimo būdas:

- Duomenų šaltinis, kuris nurodo bet kurią bendrai naudojamą lentelę, išskyrus „CompanyInfo“, duomenų šaltinis pateikia visus įrašus, esančius nurodytoje lentelėje. 
- Duomenų šaltinis, kuris nurodo lentelę „CompanyInfo“, net jei lentelė „CompanyInfo“ yra bendrai naudojama, duomenų šaltinis pateikia įrašus, kuriuose yra apibrėžtos srities įmonės identifikatorius.
- Bet kurios nuo įmonės priklausančios lentelės duomenų šaltinis pateikia nurodytos lentelės įrašus, kuriuose yra apibrėžtos srities įmonės identifikatorius.

Sistemos užklausos dialogo lange, kai įjungta parinktis **Prašyti užklausos**, bet kokiame duomenų šaltinyje, kuris pažymėtas kaip visos įmonės, galite rankiniu būdu pasirinkti vieną ar daugiau įmonių, įtrauktinų į skirtuką **Įmonės diapazonas**.

> [!IMPORTANT]
> Kaip ir su kitais filtrais, vykdant ER formatą įmonės filtras išlaikomas kaip paskutinė naudota užklausų vertė. Filtras nekeičiamas automatiškai, jei keičiate visos įmonės duomenų šaltinio vertę. Norėdami naudoti kitą visos įmonės vertę kitam duomenų šaltiniui, panaikinkite atitinkamą konkretų vartotojo pasirinkimą.

Kiekvienam duomenų šaltiniui, kuris pažymėtas kaip visos įmonės, galite pasirinkti norimus įrašus ER išraiškose naudodami funkcijas **FILTRAS** ir **KUR**. Lauką **dataAreaID** taip pat galima naudoti kaip įmonės identifikatorių. Šiuo metu laukas **dataAreaID** yra apribotas pagal šių tipų sąlygas, kai naudojama funkcija **FILTRAS**:

- Palaikomos tik tos sąlygos, kurios turi vieną lauko **dataAreaID** palyginimą.
- Leidžiami tik tie palyginimai, kurie turi išraiškas, nepriklausančias nuo įrašų sąrašo elementų.

Todėl toliau pateiktas įrašas yra tinkamas.

```ER Expression
FILTER (MyTable, MyTable.dataAreaID = $StringUserInputParameter)
While shown below expressions will not pass the validation:
FILTER (MyTable, MyTable.dataAreaID = MyTable2RecordsList.MyField)
FILTER (MyTable, 
    OR(
        MyTable.dataAreaID = $StringUserInputParameter1,
        MyTable.dataAreaID = $StringUserInputParameter2
    )
)
```

Pagal numatytuosius nustatymus aprėptis apima visas dabartinės programos įmones. Tačiau ją galima apriboti. Norėdami apriboti vieno ER formato visos įmonės duomenų prieigos aprėptį, formatui priskirkite konkrečią organizacijos hierarchiją. Kai ER formatui nustatyta hierarchija, pateikiami tik tų juridinių subjektų, kurie pristatyti priskirtoje hierarchijoje, įrašai, net jei formatas iškviečia visos įmonės duomenų šaltinius. Jei ER formatui apibrėžta nebeegzistuojanti hierarchija, taikoma numatytoji aprėptis, o formatas iškviečia visos įmonės duomenų šaltinius. Tokiu atveju, pateikiami visų programos įmonių įrašai.

Atkreipkite dėmesį, kad kai parinktis **Naudoti juodraštį** įjungta vienam ER formatui priskirtai organizacijos hierarchijai, juridiniai subjektai iš šios hierarchijos juodraščio versijos bus naudojami visos įmonės duomenų šaltinių aprėpčiai identifikuoti. Jei juodraščio versijos nėra, tam bus naudojami juridiniai subjektai iš paskutinės publikuotos šios organizacijos hierarchijos versijos.

Atkreipkite dėmesį, kad kai parinktis **Naudoti juodraštį** išjungta vienam ER formatui priskirtai organizacijos hierarchijai, juridiniai subjektai iš šios hierarchijos paskutinės publikuotos versijos bus naudojami visos įmonės duomenų šaltinių aprėpčiai identifikuoti. ER sistemoje dar nepalaikomas organizacijos hierarchijos datos efektyvumas.

Hierarchiją formatui galima priskirti konkrečiame puslapyje, kurį galima pasiekti iš ER darbo srities arba naudojant meniu elementą **Organizacijos administravimas \> Elektroninės ataskaitos \> Juridinio subjekto filtras, skirtas formatams**. Norint patekti į puslapį, vartotojui turi būti suteikta teisė **Tvarkyti juridinio subjekto filtrus, skirtus formatams** (ERMaintainFormatMappingLegalEntityFilters). Pagal hierarchiją juridinių subjektų formato apimties apribojimo taikoma be apribojimų, kurią vartotojas gali nurodyti rankiniu būdu sistemos užklausos dialogo lange. Šių apribojimų sankirta naudojama vykdant formatą.

Norėdami daugiau sužinoti apie šią funkciją, leiskite užduočių vedlį **Nuo įmonės priklausančių lentelių ER prieigos įrašai visos įmonės režimu**, kuris yra 7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677) verslo proceso dalis ir gali būti atsisiųstas iš [„Microsoft“ atsisiuntimo centro](https://go.microsoft.com/fwlink/?linkid=874684). Šis užduočių vedlys padės ER modelio susiejimo ir ER formato konfigūravimo proceso metu pasiekti programos lenteles visos įmonės režimu.

Atsisiųskite šiuos failus norėdami užbaigti užduočių vedlį:

- [ER modelio konfigūracija – CrossCompanyDataAccessModel.xml](https://go.microsoft.com/fwlink/?linkid=874111)
- [ER formato konfigūracija – CrossCompanyDataAccessFormat.xml](https://go.microsoft.com/fwlink/?linkid=874111)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]