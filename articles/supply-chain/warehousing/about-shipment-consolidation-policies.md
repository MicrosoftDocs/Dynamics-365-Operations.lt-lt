---
title: Siuntos konsolidacijos strategijos
description: Šioje temoje pateikiama funkcijų, suteikiančių lanksčią siuntos konsolidacijos strategijų konfigūraciją, apžvalga.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationError, WHSShipConsolidationSetShipment, WHSShipConsolidationPolicySelect, WHSShipPlanningListPage, TMSCarrierGroup, WHSShipConsolidationTemplate, WHSShipConsolidationTemplateApply, WHSShipConsolidationTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: b39bcf316d7779765b588d75d8057da285b47de2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831463"
---
# <a name="shipment-consolidation-policies"></a>Siuntos konsolidacijos strategijos

Siuntos konsolidacijos procesas, naudojantis siuntos konsolidacijos strategijas, sudaro galimybę automatizuotai siuntos konsolidacijai automatizuoto ir rankinio paleidimo į sandėlį metu. Automatizuota konsolidacija, kuri buvo prieinama iki šios funkcijos įvedimo, turėjo užprogramuotų laukų ir buvo pagrįsta lauku **Konsoliduoti siuntą išleidžiant ją į sandėlį**, nustatytu sandėliui.

Siuntos konsolidacijos strategijos naudojamos tolesnėms funkcijoms.

- Automatizuota paleidimo į sandėlį paketinė užduotis
- Komanda **Išleisti į sandėlį** pardavimo arba perkėlimo užsakyme
- Paskirtas puslapis **Išleisti į sandėlį**
- Komanda **Išleisti į sandėlį** puslapyje **Krovinio planavimo darbo sritis**
- Neautomatinė siuntų konsolidacija puslapiuose **Konsoliduoti siuntas** ir **Siuntų konsolidacijos darbo sritis**

Prieš įvedant siuntos konsolidacijos strategijas, konsolidacijos funkcija egzistavo kaip parametras sandėlio lygiu. Visi visų vieno sandėlio klientų užsakymai buvo laikomi taip, tarsi jiems būtų taikomi tokie patys konsolidacijos reikalavimai. Siuntos konsolidacijos strategijos įtraukia scenarijų, kuriuose skirtingoms organizacijoms taikomi skirtingi siuntos konsolidacijos reikalavimai, palaikymą.

Užklausos naudojamos norint nustatyti taikomą siuntos konsolidacijos strategiją, o tada redaguojamas laukų rinkinys nurodo, kaip krovinio eilutės sugrupuojamos siuntos lygiu. (Šis šablonas panašus į šabloną, pagal kurį veikia bangos šablonai.) Be to, į kiekvieną strategiją įtraukta parinktis **Konsoliduoti su esamomis siuntomis**. Įjungus šią parinktį, procedūra *Išleisti į sandėlį* randa siuntas konsolidavimui ieškodama esamose siuntose, sukurtose pagal tą pačią konsolidacijos strategiją. Tokiu atveju sistema pasirinks esamą siuntą arba krovinį, o ne kurs naują. Tačiau sistema vykdys konsolidaciją tik su esamomis siuntomis, kurių būsena yra *Atvira*; siuntos, kurios priklauso bangos išleidimui ir kurių būsena yra *Išleista* arba aukštesnė, nebus laikomos konsolidacijos tikslais.

Kai siuntos konsolidacijos strategijos prieinamos, parametras **Konsoliduoti siuntą išleidžiant ją į sandėlį**, kuris anksčiau buvo pasiekiamas nustatymo puslapyje **Sandėliai**, paslepiamas. Kad būtų lengviau pereiti prie naujos siuntos konsolidacijos funkcijos, funkcija puslapyje **Siuntos konsolidacijos strategijos** sukuria numatytąją strategiją, kuri automatiškai įtraukia seną esamų sandėlių parametrą. Sukūrus numatytąją strategiją, į parametrą **Konsoliduoti siuntą išleidžiant ją į sandėlį** nustatymo puslapyje **Sandėliai** nebebus atsižvelgiama.

Galite naudoti puslapį **Išleisti į sandėlį**, kad galėtumėte neautomatiniu būdu perrašyti taikomą konsolidacijos strategiją taip pat, kaip perrašomos įvykdymo strategijos.

Norėdami kurti siunčiamus krovinius, pagrįstus pardavimo arba perkėlimo užsakymo eilutėmis, prieš atliekant išleidimą į sandėlį, galite naudoti komandą **Išleidimas \> Išleidimas į sandėlį** puslapyje **Krovinio planavimo darbo sritis**. Šie kroviniai naudoja tą pačią konsolidacijos logiką, įvestą kartu su siuntos konsolidacijos strategijomis.

Galite naudoti puslapį **Siuntos konsolidacijos darbo sritis**, norėdami konsoliduoti dar nepatvirtintas, bet jau išleistas į sandėlį, esamas siuntas. Ši funkcija palaiko scenarijus, kuriuose automatizuotas paleidimo procesas, turintis savo siuntos konsolidaciją, vykdomas kelis kartus per dieną, bet galimos papildomos konsolidacijos rankiniu būdu nustatomos prieš išsiunčiant siuntą vežėjams patvirtinimo proceso metu. Ši funkcija leidžia konsoliduoti siunčiamas siuntas, sukurtas pagal pardavimo ar perkėlimo užsakymo eilutes, bet kuriuo metu po siuntų išleidimo į sandėlį, bet prieš jų patvirtinimą.

Puslapis **Siuntos konsolidacijos darbo sritis** naudojamas taip, kaip krovinio kūrimo darbo sritis, kurioje vienu metu galima įvertinti kelias siuntas ir priskirti nekonsoliduotąjį užsakymą konkrečiai siuntai. Galite taikyti siuntos konsolidacijos šablonus, kad galėtumėte įvertinti siūlomas konsolidacijas kelis kartus ir jas patvirtinti. Kai kurios taisyklės yra taikomos siekiant išvengti neteisėtos konsolidacijos ir įspėti apie galimas klaidas.

## <a name="overview-of-new-functionality"></a>Naujų funkcijų apžvalga

Šiame skyriuje aprašomi puslapiai, komandos ir funkcijos, kurie keičiami arba įtraukiami, kai įjungiate ir naudojate funkciją *Siuntos konsolidacijos strategijos*.

### <a name="shipment-consolidation-policies-page"></a>Puslapis Siuntos konsolidacijos strategijos

Strategijos skiriamos pagal darbo užsakymo tipą. Tipas **Pardavimo užsakymai** nurodo _pardavimo užsakymų_ siuntas, o tipas **Perkėlimo užsakymai** nurodo _perkėlimo išdavimo_ siuntas.

Kiekvienoje siuntos konsolidacijos strategijoje yra užklausa, apibrėžianti, kada strategija taikoma, ir sekos numeris, nurodantis vykdymo tvarką. Konsolidacija taikoma kiekvienam unikaliam pažymėtų laukų deriniui. Pateiktas papildomas parametras naudojamas konsoliduoti su esamomis (atidarytomis) siuntomis. Strategijos vertinamos ir taikomos kiekvieną kartą, kai sukuriama nauja siunta (prieš bangos apdorojimą).

Jei strategijoje trūksta privalomų laukų arba yra draudžiamų laukų, strategija pažymima kaip netinkama dalyje **Pasirinkta**. Privalomų ir draudžiamų laukų sąrašai yra užprogramuoti ir gali būti išplėsti.

Tolesnis sąrašas nurodo privalomus laukus. Kadangi siuntos visada išskaidomos pagal šiuos laukus, negalima grupuoti kelių siuntų, turinčių skirtingas šių laukų reikšmes.

- Pardavimo užsakymams:

    - **Sąskaitos numeris:** _WHSShipmentTable.AccountNum_
    - **Pristatymo gavėjas:** _WHSShipmentTable.DeliveryName_
    - **Pašto adresas (RecId):** _WHSShipmentTable.DeliveryPostalAddress_
    - **Sandėlis:** _WHSShipmentTable.InventLocationId_

- Perkėlimo užsakymams:

    - **Iš sandėlio:** _InventTransferTable.InventLocationIdFrom_
    - **Į sandėlį:** _InventTransferTable.InventLocationIdTo_

Tolesni laukai negalimi visuose dokumentų tipuose. Šie laukai nematomi vartotojo sąsajoje (UI) ir jų negalima naudoti konsolidavimui.

- **Siuntos ID:** _WHSShipmentTable.ShipmentId_
- **Būsena:** _WHSShipmentTable.ShipmentStatus_
- **Siuntos konsolidacijos strategija:** _WHSShipmentTable.ShipConsolidationPolicyName_
- **Darbo operacijos tipas:** _WHSShipmentTable.WorkTransType_
- **Bangos ID:** _WHSShipmentTable.WaveId_
- **Krovinio ID:** _WHSShipmentTable.LoadId_
- **Siuntos ID:** _WHSLoadLine.ShipmentId_
- **Krovinio ID:** _WHSLoadLine.LoadId_

Pagal numatytuosius nustatymus, kai kuriate strategiją, privalomų laukų rinkinys naudojamas kaip konsolidacijos laukai. Tačiau sąrašą galima modifikuoti naudojant rodyklės kairėn ir rodyklės dešinėn mygtukus. (Procesas panašus į būdų pasirinkimo procesą bangos šablonuose.)

Reikšmės, kurias vartotojai pasirenka šiems laukams, bus naudojamos visoms naujai sukurtoms siuntoms arba jos bus įtrauktos į esamas siuntas jų konsolidacijos metu. Kai dviejų siuntų lauke, pasirinktame šių siuntų konsolidacijai, yra tos pačios reikšmės, siuntos konsoliduojamos. Tas pats principas taikomas visiems tolesniems pasirinktiems konsolidacijos laukams. Jei reikšmės skiriasi, antroji siunta atmetama ir pasirenkama naujai siuntai. Automatizuotą konsolidacijos procesą sudaro visų unikalių siuntos konsolidacijos laukų reikšmių derinių kūrimas ir siuntos priskyrimas atitinkamam deriniui.

Nepasirinktų laukų nepaisoma konsolidacijos proceso metu. Jei dviejų siuntų nepasirinktame lauke yra skirtingos reikšmės, laukas išvalomas (t. y. jis nustatomas kaip tuščias). Jei abiejų siuntų nepasirinktame lauke yra tos pačios reikšmės, laukas užpildomas.

Konsolidacijos laukų sąrašas (t. y. laukų, kurie bus išvalyti, jei juose yra skirtingos reikšmės) yra užprogramuotas. Sąraše yra visi laukai, inicijuoti iš pardavimo arba perkėlimo užsakymo eilutės, kai sukuriama nauja siunta. Kitaip tariant, jei laukas nėra inicijuotas iš pardavimo ar perkėlimo užsakymo eilutės, jo nepaisoma, kai nauji duomenys įtraukiami į esamą siuntą.

### <a name="release-to-warehouse-page"></a>Puslapis Išleisti į sandėlį

- Naujas apatinio tinklelio laukas parodo taikomą konsolidacijos strategiją.
- Naujas mygtukas leidžia neautomatiniu būdu pasirinkti ir (arba) perrašyti konsolidacijos strategiją.

### <a name="release-to-warehouse-command-on-the-load-planning-workbench-page"></a>Komanda Išleisti į sandėlį puslapyje Krovinio planavimo darbo sritis

- Logika buvo pakoreguota, kad naudotų taikomas konsolidacijos strategijas.
- Siuntos dabar konsoliduojamos tik viename krovinyje.

### <a name="consolidate-shipments-page"></a>Puslapis Konsoliduoti siuntas

- Panašių siuntų (t. y. kandidatų konsolidacijai) ieška buvo pakeista taip, kad ji naudotų laukus, pažymėtus siuntos konsolidacijos strategijoje.
- Skirtingų siuntų laukai, kuriuose yra skirtingos reikšmės, dabar nustatomi kaip tušti. (Anksčiau buvo naudojamos pasirinktos pagrindinės siuntos reikšmės.)

### <a name="shipment-consolidation-workbench-page"></a>Puslapis Siuntos konsolidacijos darbo sritis

- Naujos funkcijos replikuoja rankinį konsolidacijos procesą didesniu mastu.
- Dabar modulio **Sandėlio valdymas** meniu **Išleisti į sandėlį** galite atidaryti šį puslapį.
- Algoritmas analizuoja dar neišsiųstas esamas siuntas. Tada jis pasiūlo konsolidaciją, pagrįstą laukais, pasirenkamais konsolidacijos strategijose.

## <a name="comparison-of-functionality"></a>Funkcijų palyginimas

Tolesnėje lentelėje apibendrinama, kaip veikia siuntos konsolidacija, kai nenaudojate siuntos konsolidacijos strategijų ir kai jas naudojate.

| Kai siuntos konsolidacijos strategijos nenaudojamos | Kai siuntos konsolidacijos strategijos naudojamos |
|---|----|
| Netaikoma | Pardavimo arba perkėlimo siuntoms, kurios pasirinktos konsolidacijai, turi būti taikoma ta pati konsolidacijos strategija kaip ir kuriamai siuntai arba jos turi būti priskirtos atidarytai siuntai (kai įjungta parinktis **Konsoliduoti su esamomis siuntomis**). |
| Procedūra *Išleisti į sandėlį* neieško siuntos konsolidacijai esamose siuntose. Siekiant rasti siuntą konsolidacijai, naudojamos tik siuntos, kurias sukūrė dabartinis procedūros *Išleisti į sandėlį* egzempliorius. | Jei parinktis **Konsoliduoti su esamomis siuntomis** įjungta konsolidacijos strategijai, kuri šiuo metu naudojama, procedūra *Išleisti į sandėlį* ieško siuntos konsolidacijai esamose siuntose, sukurtose pagal tą pačią konsolidacijos strategiją. Todėl, jei turite dvi strategijas, pagal 2 strategiją kuriama siunta niekada nebus konsoliduojama su siunta, sukurta pagal 1 strategiją. |
| Netaikoma | Jei konsolidacijos strategijos laukų sąrašas tuščias arba jei strategijos nepavyksta rasti, kiekvienai pardavimo ar perkėlimo užsakymo eilutei sukuriama nauja siunta. |
| Tolesnis konsolidacijos laukas apibrėžia unikalų reikšmių derinį, naudojamą konsoliduoti *perkėlimo eilutės* siuntas. (Visų kitų laukų nepaisoma.)<ul><li>Užsakymo numeris (OrderNum)</li></ul> | Tolesni konsolidacijos laukai apibrėžia unikalų reikšmių derinį, naudojamą konsoliduoti *perkėlimo eilutės* siuntas. (Visų kitų laukų nepaisoma.)<ul><li>Užsakymo numeris (OrderNum)</li><li>Pristatymo gavėjas (DeliveryName)</li><li>Pašto adresas (DeliveryPostalAddress)</li><li>ISO šalies kodas (CountryRegionISOCode)</li><li>Adresas (Address)</li><li>Vieta (InventSiteId)</li><li>Sandėlis (InventLocationId)</li><li>Siuntos vežėjas (CarrierCode)</li><li>Vežėjo paslauga (CarrierServiceCode)</li><li>Pristatymo būdas (ModeCode)</li><li>Vežėjų grupė (CarrierGroupCode)</li><li>Pristatymo sąlygos (DlvTermId)</li></ul>Šie laukai yra vieninteliai laukai, kurie galimi ir inicijuojami, kai sukuriama nauja siunta. |
| Tolesni konsolidacijos laukai apibrėžia unikalų reikšmių derinį, naudojamą konsoliduoti *pardavimo eilutės* siuntas. (Visų kitų laukų nepaisoma.)<ul><li>Užsakymo numeris (OrderNum)</li><li>Kliento nuoroda (CustomerRef)</li><li>Kliento paraiška (CustomerReq)</li><li>Pristatymo sąlygos (DlvTermId)</li></ul> | Tolesni konsolidacijos laukai apibrėžia unikalų reikšmių derinį, naudojamą konsoliduoti *pardavimo eilutės* siuntas. (Visų kitų laukų nepaisoma.)<ul><li>Užsakymo numeris (OrderNum)</li><li>Sąskaitos numeris (AccountNum)</li><li>Pristatymo gavėjas (DeliveryName)</li><li>Pašto adresas (DeliveryPostalAddress)</li><li>ISO šalies kodas (CountryRegionISOCode)</li><li>Adresas (Address)</li><li>Vieta (InventSiteId)</li><li>Sandėlis (InventLocationId)</li><li>Siuntos vežėjas (CarrierCode)</li><li>Vežėjo paslauga (CarrierServiceCode)</li><li>Pristatymo būdas (ModeCode)</li><li>Vežėjų grupė (CarrierGroupCode)</li><li>Brokerio ID (BrokerCode)</li><li>Kryptis (LoadDirection)</li><li>Pristatymo sąlygos (DlvTermId)</li><li>Kliento nuoroda (CustomerRef)</li><li>Kliento paraiška (CustomerReq)</li></ul>Šie laukai yra vieninteliai laukai, kurie galimi ir inicijuojami, kai sukuriama nauja siunta. |
| Netaikoma | Tolesni *pardavimo eilutės* konsolidacijos laukai yra privalomi ir jų negalima pašalinti.<ul><li>Sąskaitos numeris (AccountNum)</li><li>Pristatymo gavėjas (DeliveryName)</li><li>Pašto adresas (DeliveryPostalAddress)</li><li>Sandėlis (InventLocationId)</li></ul>Pagal numatytuosius nustatymus šie laukai bus priskirti kuriant naują strategiją. Jų pašalinti negalima. |
| Procedūra *Krovinių išleidimas į sandėlį* puslapyje **Krovinio planavimo darbo sritis** naudoja savo atskirą kodą siuntoms ir bangoms kurti. | Siuntos konsolidacijos strategijos taikomos siekiant nustatyti, kuriuos konsolidacijos laukus reikia įvertinti. Siuntos konsoliduojamos tik viename krovinyje. |
| Neautomatiniu būdu pasirinkite **Konsoliduoti siuntas** puslapyje **Visos siuntos** ir tada pasirinkite tikslinę pagrindinę siuntą. Filtras pasiūlys visas esamas siuntas, turinčias sutampančių kelių pagrindinių laukų reikšmių. | Neautomatiniu būdu pasirinkite **Konsoliduoti siuntas** puslapyje **Visos siuntos** ir tada pasirinkite tikslinę pagrindinę siuntą. Sistema pasiūlys kitas esamas siuntas, derindama kelių pagrindinių laukų reikšmes, sukonfigūruotas atitinkamoms siuntos konsolidacijos strategijoms. |
| Galite naudoti komandą **Konsoliduoti siuntas** puslapyje **Visos siuntos** tik vienai siuntai. | Puslapis **Siuntos konsolidacijos darbo sritis** padeda rasti siuntų, kurių būsena dar nėra Išsiųsta, rinkinį. Šios siuntos analizuojamos pagal kelis pagrindinius laukus, sukonfigūruotus jūsų siuntos konsolidacijos strategijose. Siūloma konsoliduoti visas siuntas, kuriose sutampa šių laukų reikšmės.<p>Galite rankiniu būdu valdyti konsolidaciją, pašalindami siuntas iš siūlomų konsolidacijų ir (arba) įtraukdami siuntas į jas. Gali įvykti kelių tipų klaidų, bet kai kurių jų galima nepaisyti.</p> |
| **Dizaino pastaba:** procedūra *Automatinis pardavimo užsakymų išleidimas į sandėlį* išskaido pardavimo eilutes į grupes. Kiekviena grupė turi savo unikalią **ReleaseToWarehouseId** reikšmę ir yra apdorojama atskirai pagal procedūrą *Išleisti į sandėlį*. Ši procedūra sukuria naują darbą nepaisydama darbo pertraukų nustatymų. | **Dizaino pastaba:** procedūra *Automatinis pardavimo užsakymų išleidimas į sandėlį* priskiria tą pačią **ReleaseToWarehouseId** reikšmę visoms apdorojamoms pardavimo eilutėms. Procedūra *Išleisti į sandėlį* apdoroja visas pardavimo eilutes vienu metu. Norėdami užtikrinti ankstesnį veikimą, turite sukonfigūruoti darbo pertraukas kiekvienam siuntos ID. |

## <a name="additional-resources"></a>Papildomi ištekliai

- [Siuntos konsolidacijos strategijų konfigūravimas](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]