---
title: Konfigūracijos raktai ir duomenų objektai
description: Šiame straipsnyje aprašomas ryšys tarp konfigūracijos raktų ir duomenų objektų.
author: peakerbl
ms.date: 05/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: 25341
ms.assetid: 8e214c95-616b-4ee1-b5a4-fa5ce5147f2c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 8083c8c053197f685985f340281c43f30053d2a5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885268"
---
# <a name="configuration-keys-and-data-entities"></a>Konfigūracijos raktai ir duomenų objektai

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Prieš naudojant duomenų objektus duomenims importuoti ar eksportuoti, rekomenduojame pirmiausia nustatyti konfigūracijos raktų poveikį duomenų objektams, kuriuos planuojate naudoti.

Norėdami daugiau sužinoti apie konfigūracijos raktus, žr. [Licencijų kodų ir konfigūracijos raktų ataskaita](../sysadmin/license-codes-configuration-keys-report.md).

### <a name="configuration-key-assignments"></a>Konfigūracijos raktų priskyrimai
Konfigūracijos raktus galima priskirti vienam arba visiems iš toliau pateiktų artefaktų.

- Duomenų objektai
- Lentelės, naudojamos kaip duomenų šaltiniai
- Lentelės laukai
- Duomenų objektų laukai

Tolesnėje lentelėje apibendrinama, kaip skirtingų artefaktų konfigūracijos raktų reikšmės, kuriomis grindžiamas objektas, pakeičia numatytą objekto veikimą.

| Konfigūracijos rakto parametras duomenų objekte | Konfigūracijos rakto parametras lentelėje | Konfigūracijos rakto parametras lentelės lauke | Konfigūracijos raktas duomenų objekto lauke | Numatytas veikimas |
|-----------------------------------------|------------------------------------|------------------------------------------|----------------------------------------|------------------|
| Uždraustas                                | Neįvertinta                      | Neįvertinta                            | Neįvertinta                          | Jei duomenų objekto konfigūracijos raktas išjungtas, duomenų objektas neveiks. Nesvarbu, ar esamų lentelių ir laukų konfigūracijos raktai yra įjungti, ar išjungti. |
| Įgalinta                                 | Uždraustas                           | Neįvertinta                            | Neįvertinta                          | Jei duomenų objekto konfigūracijos raktas yra įjungtas, duomenų valdymo sistema tikrina kiekvienos esamos lentelės konfigūracijos raktą. Jei lentelės konfigūracijos raktas išjungtas, tos lentelės nebus galima naudoti duomenų objekte. Jei lentelės konfigūracijos raktas yra išjungtas, neįvertinami lentelės ir duomenų objektų konfigūracijos rakto parametrai. Jei pirminės objekto lentelės konfigūracijos raktas yra išjungtas, sistema veiks taip, tarsi objekto konfigūracijos raktas būtų išjungtas. |
| Įgalinta                                 | Įgalinta                            | Uždraustas                                 | Neįvertinta                          | Jei duomenų objekto konfigūracijos raktas yra įjungtas ir įjungti esamų lentelių konfigūracijos raktai, duomenų valdymo sistema tikrins lentelių laukų konfigūracijos raktą. Jei išjungtas kokio nors lauko konfigūracijos raktas, to lauko nebus galima naudoti duomenų objekte, net jei įjungtas atitinkamo duomenų objekto lauko konfigūracijos raktas. |
| Įgalinta                                 | Įgalinta                            | Įgalinta                                  | Uždraustas                               | Jei konfigūracijos raktas įjungtas visuose kituose lygiuose, tačiau neįjungtas objekto lauko konfigūracijos raktas, to lauko nebus galima naudoti duomenų objekte. |

> [!NOTE]
> Jei objekte kaip duomenų šaltinis naudojamas kitas objektas, taikoma tokia pati semantika, kokia pateikta pirmiau.

### <a name="entity-list-refresh"></a>Objektų sąrašo atnaujinimas
Kai atnaujinamas objektų sąrašas, duomenų valdymo sistema kuria konfigūracijos raktų metaduomenis naudoti vykdyklėje. Šie metaduomenys kuriami naudojant pirmiau aprašytą logiką. Primygtinai rekomenduojame prieš duomenų valdymo sistemoje naudojant užduotis ir objektus palaukti, kol bus baigta atnaujinti objektų sąrašą. Jei nepalauksite, konfigūracijos raktų metaduomenys gali būti neatnaujinti ir gali pateikti netikėtų rezultatų. Kai atnaujinamas objektų sąrašas, objektų sąrašų puslapyje rodomas tolesnis pranešimas.

![Objektų sąrašo atnaujinimas.](./media/Entity_refresh_list.png)

### <a name="data-entity-list-page"></a>Duomenų objektų sąrašų puslapis
Darbo srityje Duomenų valdymas esančiame duomenų objektų sąrašų puslapyje rodomi objektų konfigūracijos raktų parametrai. Pradėkite nuo šio puslapio, kad suprastumėte konfigūracijos raktų poveikį duomenų objektui.

Ši informacija rodoma naudojant metaduomenis, sukurtus atnaujinant objektus. Konfigūracijos rakto stulpelyje rodomas su duomenų objektu susieto konfigūracijos rakto pavadinimas. Jei šis stulpelis yra tuščias, tai reiškia, kad su duomenų objektu nesusietas joks konfigūracijos raktas. Konfigūracijos rakto būsenos stulpelyje rodoma konfigūracijos rakto būsena. Jei jame yra žymė, tai reiškia, kad raktas yra įjungtas. Jei jis yra tuščias, tai reiškia, kad raktas išjungtas arba kad nesusietas joks raktas.

![Objektų sąrašų puslapis.](./media/Data_entity_list_page.png)

### <a name="target-fields"></a>Paskirties laukai
Tolesnis veiksmas yra detalizuoti duomenų objektą ir peržiūrėti konfigūracijos raktų poveikį lentelėms bei laukams. Duomenų objekto paskirties laukų formoje rodoma informacija apie susijusių duomenų objekto lentelių ir laukų konfigūracijos raktus bei jų būseną. Jei išjungtas paties duomenų objekto konfigūracijos raktas, rodomas įspėjamasis pranešimas, informuojantis, kad šio objekto paskirties laukų formos lentelių ir laukų nebus galima naudoti visai, nepaisant jų konfigūracijos raktų būsenos.

![Paskirties laukai.](./media/Target_fields_1.png)

### <a name="child-entities"></a>Antriniai objektai 
Tam tikri objektai kaip duomenų šaltinius naudoja kitus objektus arba jie yra sudėtiniai duomenų objektai: informacija apie šių objektų konfigūracijos raktus rodoma formoje Antriniai objektai. Šią formą naudokite panašiai, kaip pirmiau aprašytą objektų sąrašų puslapį. Antrinio objekto paskirties laukų forma taip pat veikia taip, kaip aprašyta pirmiau.

![Paskirties laukai.](./media/Target_fields_2.png)

### <a name="using-data-entities"></a>Duomenų objektų naudojimas
Supratę visą (jei toks yra) konfigūracijos raktų poveikį norimiems naudoti duomenų objektams, dabar duomenų objektus galite naudoti toliau, juos įtraukdami į duomenų projektus. 

### <a name="run-time-validations-for-configuration-keys"></a>Konfigūracijos raktų tikrinimai vykdymo aplinkoje
Naudojant konfigūracijos raktų metaduomenis, sukurtus atnaujinant objektų sąrašus, tolesniais naudojimo atvejais atliekami tikrinimai vykdymo aplinkoje.

- Kai duomenų objektas įtraukiamas į užduotį
- Kai vartotojas objektų sąraše spusteli Tikrinti
- Kai vartotojas į duomenų projektą įkelia duomenų paketą
- Kai vartotojas į duomenų projektą įkelia šabloną
- Kai įkeliamas esamas duomenų projektas
- Kai į duomenų projektą įkeliamas šablonas
- Prieš vykdant eksporto / importo užduotį (paketinę, nepaketinę, pasikartojančią, „OData“)
- Kai vartotojas generuoja susiejimą
- Kai vartotojas susieja lauką susiejimo vartotojo sąsajoje
- Kai vartotojas įtraukia tik „importuojamuosius laukus“

### <a name="managing-configuration-key-changes"></a>Konfigūracijos raktų keitimų valdymas
Kai tik objekto, lentelės ar lauko lygiu atnaujinate objekto konfigūracijos raktus, reikia atnaujinti duomenų valdymo sistemoje esantį objektų sąrašą. Šiuo procesu užtikrinama, kad sistema naudoja naujausius konfigūracijos raktų parametrus. Kol nebus atnaujintas objektų sąrašas, objektų sąrašų puslapyje bus rodomas tolesnis įspėjamasis pranešimas. Atnaujinti konfigūracijos raktų keitimai įsigalios iš karto po to, kai bus atnaujintas objektų sąrašas. Rekomenduojame patikrinti esamus duomenų projektus ir užduotis, kad įsitikintumėte, jog, įsigaliojus konfigūracijos raktų keitimams, jie veikia taip, kaip tikėtasi.

![Paskirties laukai.](./media/Target_fields_3.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
