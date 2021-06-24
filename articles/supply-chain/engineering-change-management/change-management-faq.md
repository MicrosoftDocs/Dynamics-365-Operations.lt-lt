---
title: Inžinerinių pakeitimų valdymo DUK
description: Šioje temoje pateikiami atsakymai į dažniausiai užduodamus klausimus apie inžinerinio keitimo valdymo funkciją.
author: t-benebo
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-25
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9c95c1f2342654ca2bbee57959becc85291eebbc
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187276"
---
# <a name="engineering-change-management-faq"></a>Inžinerinių pakeitimų valdymo DUK

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiami atsakymai į dažniausiai užduodamus klausimus apie inžinerinio keitimo valdymo funkciją.

## <a name="should-i-track-the-version-in-transactions"></a>Ar sekti operacijų versiją?

Kai kuriate inžinerijos keitimo kategoriją, informacijos apie inžinerinio keitimo kategoriją puslapis **pateikia pasirinktį,** pavadintą **Sekti operacijų versiją**. Kas yra šis parametras ir ką darote?

- Jei operacijose nustatote versiją Sekti kaip Taip, dimensijos grupės laukas bus filtruojamas, kad jame būtų rodomos tik dimensijos grupės, kuriose **kuriose** versija *yra* aktyvi **dimensija**.
- Jei nustatote **operacijose sekimo versijos** parinktį į *Ne*, the **dimensijos grupės** laukas bus filtruojamas, kad jame būtų rodomos tik dimensijos grupės, kuriose **versija** nėra aktyvi dimensija.

### <a name="if-you-track-the-version-in-transactions"></a>Jei sekate versiją operacijose

Inžinerijos kategorijoms, kuriose pasirinkote dimensijų grupę, kurioje versija yra aktyvi dimensija, sekate tos kategorijos produktų operacijų versijas. Tuo atveju, inžinerijos produktas bus pagrindinis produktas ir kiekviena jo versija bus produkto variantas, naudojantis versijos matmenis. Kitos dimensijos gali būti naudojamos kartu su versijos dimensija.

Šiuo atveju kiekviena inžinerijos versija bus laikoma visų procesų variantu. Todėl, jei operacijoje turite tam tikrą variantą (tam, kad nustatytumėte, kuris variantas buvo parduotas arba nupirktas), privalote valdyti kiekvienos versijos atsargas, bendrasis planavimas suplanuos kiekvienos versijos atsargas ir t. t. Jei išeisite iš rinkos versiją, rankiniu būdu turite koreguoti jos galiojimo pradžios ir galiojimo pabaigos datas, kad jos atspindėtų pakeitimą. Taip pat turite valdyti savo atsargas, kad įsitikintumėte, jog savo sandėliuose neturite nenaudojamų prekių versijų.

Nors šiai pasirinktii reikia daugiau valdymo pastangų, rekomenduojame, jei reikia aukšto lygio konkrečių versijų, naudojamų kiekvienoje operacijoje.

### <a name="if-you-dont-track-the-version-in-transactions"></a>Jei nesekate versiją operacijose

Inžinerijos kategorijoms, kuriose pasirinkote dimensijų grupę, kurioje versija nėra aktyvi **dimensija**, neseksite **tos** kategorijos produktų operacijų versijas. Šiuo atveju, jei jokios kitos dimensijos nenaudosite, inžinerijos produktas bus skirtingas produktas. Produktas vis tiek bus įdiegtas ir galėsite valdyti informaciją apie konkrečias versijas (pvz., jų KS KS) ir maršrutą, tačiau negalėsite sekti, kuri konkreti versija buvo naudojama kiekvienoje \[operacijoje]. Galiojimo pradžios ir galiojimo pabaigos datos nurodo kiekvienos versijos galiojimą.

Šią pasirinktį lengviau valdyti, nes jei norite pakeisti vieną versiją į kitą, tiesiog turite atlikti reikalingus pakeitimų užsakymo pakeitimus ir tada atnaujinti efektyvias ir efektyvias datas inžinerijos versijoje. Gamybos procesai surinks reikiamą produkto KS ir maršrutą (ir konkrečią jo versiją).

Dauguma organizacijų pasirenka šią pasirinktį, nes pateikia versiją ir keitimų valdymą, bet prie kiekvienos operacijos, atsargų ir bendrojo planavimo metu prideda papildomas versijos sekimo pridėtines išlaidas.

## <a name="which-fields-are-copied-from-the-released-item-template"></a>Kurie laukai nukopijuojami iš išleisto prekės šablono?

Kai inžinerijos įmonė sukuria inžinerijos produktą, šis produktas inžinerijos įmonėje sukuriamas kaip išleistas produktas. Išleistas produktas, sukurtas pagal pasirinktą išleistų *prekių šabloną*. (Išleistas prekės šablonas jau yra išleistas produktas.) Išleistas prekės šablonas taip pat naudojamas, kai produktas išleidžiamas veiklos įmonei. Kiekvienu atveju išleistas prekės šablonas apibrėžia daugumą išleisto produkto laukų verčių ir šios vertės yra iš susijusio **išleisto produkto informacijo** puslapio.

Toliau pateikiamose lentelėse rodomi šių procesų metu nukopijuoti laukai.

| FastTab | Laukai, nukopijuoti kuriant produktą gamybos įmonėje | Laukai, nukopijuoti išleisti į veiklos įmonę |
|---|---|---|
| **Bendroji** | Visi administravimo **skyriaus** laukai | Tie patys laukai, nukopijuoti gamybos įmonei |
| **Pirkimas** | Visi laukai | Visi laukai, išskyrus **vienetą** |
| **Pardavimas** | Visi šių skyrių laukai: **Pardavimo** užsakymas, **Administravimas**, **Apmokestinimas, Kainos atnaujinimas, Bazinė** **pardavimo** **kaina** **Mokesčiai**, **Nuolaidos ir** **Alternatyvus produktas** | Visi tie patys laukai, nukopijuoti gamybos įmonei apart **Vieneto** |
| **Užsienio prekyba** | Visi laukai | Visi laukai |
| **Tvarkyti atsargas** | Visi laukai ir skyriai, *išskyrus* faktines **dimensijas** ir esamo **svorio** | Visi tie patys laukai, nukopijuoti gamybos įmonei apart **Vieneto** |
| **inžinierius** **,** planas, išlaidų **valdymas**, projektų **valdymas**, finansinės dimensijos **ir** **sandėlis** | Visi laukai | Visi laukai, išskyrus **BOM vienetą** |
| **Produkto variantai** | Visi numatytojo **produkto varianto skyriaus** laukai | Tie patys laukai, nukopijuoti gamybos įmonei |

Kartu su laukais, kurie rodomi ankstesnėje lentelėje, visi numatytieji užsakymo parametrai kopijuojami iš išleisto prekės šablono ir tada, kai produktas sukuriamas inžinerijos įmonėje, ir kai jis išleidžiamas į veiklos įmonę. (Norėdami peržiūrėti išleisto prekės šablono numatytuosius užsakymo parametrus, atidarykite reikiamą **Informacijos apie produktą puslapis, tada veiksmų srities skirtuke Tvarkyti atsargas pasirinkite** **Numatytieji** **užsakymo** parametrai.)

## <a name="should-i-create-a-separate-legal-entity-for-engineering-products-or-use-an-existing-legal-entity"></a>Ar reikia sukurti atskirą gamybos produktų juridinį subjektą, ar naudoti esamą juridinį subjektą?

Jūsų verslo reikalavimai apibrėžia, ar reikia sukurti naują inžinerijos produktų juridinį subjektą.

Kurdami atskirą inžinerinę įmonę, inžinerinius duomenis galite laikyti atskirus ir pridėti pakeitimus, reikalingus jūsų vietinėms veiklos įmonėms. Tokiu būdu, galite pasiekti šiuos tikslus:

- Laikyti atskirą objektą, kuriame kuriami ir valdomi inžinerijos produktai.
- Neleiskite inžinerijos produktų rodyti kartu su likusiais išleistais produktais, kol jie nebus paruošti ir išleisti.
- Aiškiai atskiria duomenis, diktuoja inžinerijos ir vietinius duomenis.

Kita vertus, jūs greičiausiai turėtumėte naudoti esamą juridinį subjektą kaip inžinerijos įmonę, jei jums taikomos šios sąlygos:

- Savo sistemoje turite tik vieną juridinį subjektą ir (arba) jums nereikia aiškaus atskyrimo tarp dabar inžinerijos būdu kuriamų produktų.
- Nenorite dubliuoti kai kurių duomenų, pvz., išteklių grupių, išteklių, operacijų ir (galbūt) svetainių.

## <a name="what-is-the-nomenclature-for-engineering-versions-and-variants"></a>Kokia inžinerijos versijų ir variantų klasifikacija?

Inžinerijos produktų ir produktų variantų nomenclatures veikia tokiu būdu:

- Inžinerijos produktui (t. y. išsamusis produktas, jei dimensijos nenaudomos, arba bendrasis produktas, jei naudojama kokia nors dimensija), skaičių taisyklės numeracija nustatoma inžinerijos produktų kategorijoje. Yra pasirinktis naudoti numeraciją, teksto konstantas ir atributų pavadinimus bei vertes.
- Kiekvienam inžinerinio produkto variantui (jei jūsų inžinerijos produktas yra bendrasis produktas, variantai nustatomi inžinerijos produktų kategorijoje, kurioje nurodote dimensijų grupę), kiekvieno varianto numerio taisyklės nomenclature nurodoma dimensijų grupėje. Šiuo atveju galite naudoti bendrojo produkto ID ir dimensijų vertes bei pavadinimus.
