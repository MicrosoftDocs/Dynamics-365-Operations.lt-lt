---
title: Įplaukos ir išlaidų atidėjimai abonemento sąskaitose
description: Šiame straipsnyje paaiškinama, kaip nustatyti įplaukų ir išlaidų atidėjimus abonemento sąskaitose.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 209afd08c0c7e3cbd63ed95613b1d1dec94856f5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908102"
---
# <a name="revenue-and-expense-deferrals-in-subscription-billing"></a>Įplaukos ir išlaidų atidėjimai abonemento sąskaitose

Šiame straipsnyje paaiškinama, kaip nustatyti ir naudoti įplaukų ir išlaidų atidėjimus abonemento sąskaitose. Atidėjimo grafikai visada yra pagrįsti ir priklausomi nuo jau sukurto dokumento arba atsiskaitymo grafiko. Kadangi jos sukuriamos pagal numatytąsias vertes, jų negalima įvesti ar sukurti atskirai.

Įplaukų ir išlaidų atidėjimų nustatymo ir naudojimo procesas vyksta keliuose puslapiuose:

- Puslapyje Įplaukų **ir išlaidų atidėjimo** parametrai galite nurodyti įmonės nuostatas.
- Atidėjimų **numatytųjų parametrų** puslapyje galite nustatyti numatytąsias sąskaitas ir šablonus, naudojamus atidėjimų grafikams.
- Atidėjimo **šablonuose** ir **atidėjimo šablonų** puslapiuose pagal įvykį galite nustatyti atidėjimo grafikams naudojamus šablonus.
- **Puslapyje Visi atidėjimų grafikai galite** peržiūrėti ir redaguoti bet kurį atidėjimo grafiką.

Įplaukų ir išlaidų atidėjimus galima naudoti kartu su pasikartojančiomis sutarties sąskaitomis.

## <a name="revenue-and-expense-deferral-parameters"></a>Įplaukų ir išlaidų atidėjimo parametrai

Puslapyje **Įplaukų ir išlaidų atidėjimo** parametrai yra šie laukai.

| Laukas | Aprašymas |
|---|---| 
| **Skirtukas Grafikas** | |
| Vieno laikotarpio lygu | <p>Nurodykite, ar skaičiuojant atidėjimo grafiko laikotarpio sumą naudojamas laikotarpio dienų skaičius:</p><ul><li>**Taip** – kiekvieno laikotarpio suma yra tokia pati, neatsižvelgiant į laikotarpio dienų skaičių. Daliniai laikotarpiai (pvz., atidėjimo grafiko pradžioje arba pabaigoje) bus atiduoti.</li><li>**Ne** – suma skaičiuojama pagal kiekvieno laikotarpio dienų skaičių.</li></ul><p>Šio parametro galima nepaisyti operacijos lygyje.</p> |
| Pardavimo nuolaidos atidėjimo parinktis | <p>Nurodyti, ar sukurti atskiri nuolaidos ir pardavimo užsakymo sumų atidėjimo grafikai:</p><ul><li>**Atskiras nuolaidos grafikas** – nuolaidos suma saugoma atskirai nuo įplaukų sumos.<p>Tokiu atveju, sukūrus pardavimo užsakymą, sukuriami du atidėjimo grafikai, tada užregistruojami. Nuolaidos ir įplaukų sumos bus užregistruotos skirtingose atidėjimo sąskaitose.</p></li><li>**Sulieti nuolaidą** su įplaukomis – nuolaidos suma derinama su įplaukų suma. Sukuriamas vienas atidėjimo grafikas, o nuolaidos suma ir įplaukų suma registruojamos toje pačioje atidėjimo sąskaitoje.<p>Šiuo atveju, sukūrus pardavimo užsakymą, sukuriamas vienas atidėjimo grafikas, o tada registruojamas. Toje pačioje atidėjimo sąskaitoje registruojami ir nuolaidos suma, ir įplaukų suma.</p></li></ul><p>**Pastaba.** Norėdami taikyti nuolaidas prekėms, kurios naudoja neaprašytų įplaukų funkciją, pasirinkite parinktį **Atskirti nuolaidos grafiką**. Tada nuolaidas galima taikyti visoms prekėms, nepaisant to, ar naudojama neįskaitomos įplaukų priemonė. Jei pasirinkta **parinktis Susieti nuolaidą** su įplaukomis, nuolaidos negali būti taikomos prekėms, kurios naudoja neap sf įplaukų funkciją.</p> |
| Pirkimo nuolaidos atidėjimo parinktis | <p>Pasirinkti, ar kuriami atskiri atidėjimo grafikai nuolaidos ir pirkimo užsakymų sumoms:</p><ul><li>**Atskiras nuolaidos grafikas** – nuolaidos suma saugoma atskirai nuo išlaidų sumos.<p>Tokiu atveju, sukūrus pirkimo užsakymą, sukuriami du atidėjimo grafikai, tada užregistruojami. Nuolaidos ir išlaidų sumos registruojamos skirtingose atidėjimo sąskaitose.</p></li><li>**Sulieti nuolaidą** su įplaukomis – nuolaidos suma derinama su išlaidų suma. Sukuriamas vienas atidėjimo grafikas, o nuolaidos suma ir išlaidų suma registruojami toje pačioje atidėjimo sąskaitoje.<p>Šiuo atveju, sukūrus pirkimo užsakymą, sukuriamas vienas atidėjimo grafikas, o tada registruojamas. Toje pačioje atidėjimo sąskaitoje registruojama ir nuolaidos suma, ir išlaidų suma.</p></li></ul> |
| Konsoliduoti ankstesnius laikotarpius | <p>Nurodyti, ar atidėjimo grafiko eilutės ankstesniems laikotarpiams yra konsoliduotos:</p><ul><li>**Taip** – jei atidėjimo pradžios data yra už operacijos datą esantis laikotarpis, visos operacijos datos laikotarpio sumos sujungiamos į vieną atidėjimų grafiko eilutę.</li><li>**Ne** – visų laikotarpių sumos laikomos atskirose atidėjimo grafiko eilutėse.<p>Jei atidėjimo pradžios data yra tame pačiame laiko tarpe arba vėlesniame laiko tarpe nei operacijos data, ši pasirinktis neturi įtakos.</p></li></ul><p>Šis parametras gali būti atnaujinamas operacijos lygiu.</p> |
| Numatytoji atidėjimo pradžios data | <p>Pasirinkite taisyklę, kuri bus naudojama atidėjimo grafiko pradžios datai nustatyti:</p><ul><li>**Operacijos data** – naudokite operacijos datą kaip pradžios datą.</li><li>**Šio mėnesio pradžia** – naudoti pirmą esamo mėnesio datą kaip pradžios datą. Jei operacijos data yra pirma bet kurio mėnesio data, dabartinio mėnesio pirmoji data yra pradžios data.</li><li>**Kito mėnesio pradžia** – naudokite pirmą kito mėnesio dieną kaip pradžios datą. Jei operacijos data yra pirma, naudojama operacijos data. Kitu atveju naudojamas pirmasis kito mėnesio mėnuo.</li><li>**15 taisyklė** – jei operacijos data yra tarp pirmosios ir penkioliktos, kaip pradžios datą naudokite pirmąjį esamo mėnesio mėnesį. Jei operacijos data yra šešiolikta arba vėlesnė, kaip pradžios datą naudokite pirmą kito mėnesio datą.</li></ul><p>Šį parametrą galite atnaujinti operacijos lygyje.</p> |
| Trumpalaikio atidėjimo būdas | <p>Pasirinkite trumpalaikio atidėjimo metodą: **Nėra, Ėjimo** laikotarpiai arba **Fiksuoti** metai **·**.</p><p>|
| Atidėjimo registravimo būdas | <p>Pasirinkti metodą, naudojamą atidėjimo operacijoms kurti:</p><ul><li>**Balansas –** atidėjimo operacijoms kurti naudokite balanso registravimo metodą.</li><li>**Pelnas ir nuostolis** – atidėjimo operacijoms kurti naudokite pelno ir nuostolio registravimo metodą. Kai operacijos užregistruojamos, galite peržiūrėti SF kvitą ir pamatyti papildomus įrašus, kurie subalansuos pradinį pripažinimą ir korespondentinę sumą.</li></ul> |
| Atšaukti kredito pelną ir nuostolius | <p>**Pastaba:** šis laukas galimas tik tada, kai **lauke Atidėjimo registravimo** metodas nustatyta reikšmė **Pelnas ir nuostolis**.</p><p>Nurodyti, ar pelno ir nuostolio sumos atšaukiamos, kai atšaukimas, nutraukimas arba grąžinimas taikomi atsiskaitymo grafikui arba pardavimo užsakymui:</p><ul><li>**Taip** – atšaukite pelno ir nuostolio sumas ir atidėjimo grafikui taikykite kredito koregavimo sumą.<p>Jei atšaukimas vyksta pusiau sąskaitų pateikimo laikotarpiu, sumos yra perskaičiuojamos.</p></li><li>**Ne** – pelno ir nuostolio atšaukimo operacija nekurta, kai atšaukimas, nutraukimas arba grąžinimas netaikomas atsiskaitymo grafikui arba pardavimo užsakymui.</li></ul> |
| **Skirtukas Atpažinimas** | |
| Automatiškai registruoti bendruosius žurnalus | <p>Nurodykite, ar žurnalo įrašai, sukurti pagal įplaukų ir išlaidų atidėjimus, registruojami automatiškai:</p><ul><li>**Taip** – automatiškai užregistruoti žurnalo įrašus, sukurtus pagal įplaukų ir išlaidų atidėjimus.<p>**Patarimas:** pasirinkę **Taip** galite išvengti apskaitos nenuoseklumo, atsiradusio dėl neautomatinio kvitų pakeitimų.</p></li><li>**Ne** – žurnalo įrašai, kuriuos sukūrė įplaukų ir išlaidų atidėjimai, nėra registruojami automatiškai. Turite neautomatiniu būdu užregistruoti bet kuriuos žurnalus.</li></ul> |
| Pateikti pripažinimo žurnalo suvestinę | <p>Nurodykite, ar atpažinimo kvitai konsoliduojami pagal numatytuosius nustatymus:</p><ul><li>**Taip** – kurti vieną kvitą visoms atpažinimo eilutėms, kurių data ta pati. Visos kvito eilutės, kurių sąskaita ta pati, konsoliduojamos į vieną eilutę.</li><li>**Ne** – kurti kvitą kiekvienai atpažinimo eilutei.</li></ul><p>Šį parametrą galite atnaujinti atpažinimo **apdorojimo** puslapyje.</p> |
| Numatytasis žurnalo pavadinimas | Pasirinkite žurnalų, sukurtų iš įplaukų ir išlaidų atidėjimo procesų, pvz., atpažinimo apdorojimo, pavadinimą. |
| Pripažinimo žurnalo eilutės aprašas | <p>Pasirinkite aprašymą, kuris rodomas žurnalo kvito eilutės aprašyme:</p><ul><li>**Planuoti eilutės datas** – žurnalo eilutės aprašyme rodyti grafiko eilutės datas.</li><li>**Rodoma operacijos informacija** – rodyti iciavimo operacijos informaciją žurnalo eilutės aprašyme.<p>**Pavyzdys:** USMF-0001, CIV-00839, programinės įrangos įplaukos</p></li></ul> |
| **Skirtukas Numeracijos** | Naudokite šį skirtuką, norėdami nustatyti numatytąsias nuomos numeracijų vertes. Numeracijos generavimo vedlys naudojamas numeracijoms automatiškai generuoti ir priskirti. Numeracijos keisti nereikia, nebent sugeneruotas numeracijas norite keisti rankiniu būdu. |
| Grafiko numeris | Numeris, kuris naudojamas atidėjimo grafikams. |

## <a name="deferral-templates"></a>Atidėjimo šablonai

Naudokite atidėjimų **šablonų** puslapį norėdami nustatyti tiesiogiai suplanuotus šablonus, naudojamus atidėjimo grafikams.

Štai keletas šablono naudojimo pranašumai:

* Atidėjimo ilgis apskaičiuojamas automatiškai.
* Leidžiate atidėjimo grafikus, kuriuose yra laikotarpių, kuriuose atpažinimas praleistas.
* Atidėjimus galite automatizuoti priskirdami šabloną produktui, produktų grupei, produkto kategorijai, klientams arba klientų grupei. Šablono priskyrimas atliekamas atidėjimų **numatytųjų nustatymų** puslapyje.

Galimi keli laikotarpių dažnumai šablonams: dienos, mėnesio arba ataskaitiniams laikotarpiams.

Šablono eilutes sudaro tipas (Atpažintas **arba** **Praleistas**) ir laikotarpio ilgis. Atidėjimo grafiko eilutėse praleistų eilučių suma yra 0 (nulis). Taip gali būti naudinga, jei nenorite atpažinti visų laikotarpių įplaukų.

### <a name="create-a-deferral-template"></a>Kurti atidėjimo šabloną

Norėdami kurti atidėjimo šabloną, atlikite šiuos veiksmus.

1. Atidėjimo **šablonų** puslapyje pasirinkite **Naujas**.
2. **Lauke Šablonas** įveskite pavadinimą.
3. Lauke **Aprašas** įveskite aprašą.
4. Lauke Laikotarpio **dažnis** pasirinkite laikotarpio dažnį.
5. **Norėdami** į eilučių sąrašą įtraukti eilutę, pasirinkite Įtraukti, o jei norite pridėti eilutę, esančią sąrašo apačioje, **pasirinkite** Pridėti.
6. **Lauke Tipas** pasirinkite laikotarpio tipą.
7. **Lauke Laikotarpio** ilgis nurodykite laikotarpio ilgį.
8. Kiekvienai papildomai eilutei, kurios reikia, pakartokite 5–7 veiksmus.
9. Pasirinkite **Įrašyti**.

## <a name="deferral-defaults"></a>Numatytieji atidėjimo nustatymai

Naudokite atidėjimų **numatytųjų parametrų puslapį, norėdami nustatyti numatytąsias prekių atidėjimo sąskaitas ir priskirti atidėjimo prekėms numatytuosius** šablonus. Taip pat galite nustatyti mokesčių atidėjimo sąskaitas ir priskirti atidėjimo išlaidų šablonus.

**Atidėti pagal prekę**

Operacijoms, kurios turi prekę (pvz., pardavimo užsakymus), galite priskirti sąskaitas ir šablonus konkrečioms prekėms ir klientams. Atidėti operacijas šie parametrai bus naudojami kaip numatytosios vertės. Kad operacijos atidėjimas būtų galimas pagal numatytuosius nustatymus, prekes turite nustatyti **atidėjimo prekių** puslapyje.

**Atidėti pagal sąskaitą**

Galite nurodyti atidėjimo sąskaitas operacijoms, kuriose nėra prekių (pvz., bendrųjų žurnalų). Kai šios sąskaitos naudojamos operacijos eilutėje, operacija automatiškai pažymima kaip atidėta. Atitinkamas šablonas ir atpažinimo sąskaita bus priskirti operacijos eilutei.

**Visi operacijų tipai (pvz., skirtukuose Pardavimo užsakymas, Pirkimas ir Bendra žurnalai)**

Puslapio sąskaitos yra pagrindinės sąskaitos, kurios neturi finansinių dimensijų. Atpažinimo sąskaitos finansinės dimensijos yra iš kliento ar prekės, remiantis jūsų organizacija.

Kiekviena šablono eilutė turi turėti tiesios eilutės šabloną arba įvykiu pagrįstą šabloną. Negali būti abiejų.

### <a name="for-sales-orders"></a>Pardavimo užsakymams

Norėdami nurodyti pardavimo užsakymų numatytąsias atidėjimo vertes, atlikite šiuos veiksmus.

1. Skirtuke **Pardavimo** užsakymas pasirinkite atidėjimo tipą.
2. Pasirinkite **Įtraukti** eilutei įtraukti.
3. **Lauke Prekės kodas** pasirinkite prekės kodą. Prekės kodas nustato, kaip taikomos atidėjimo numatytosios vertės.
4. Nurodykite, kaip taikomas prekės kodas:

    * Jei lauke **Prekės kodas** nustatyta Lentelė **arba** **Grupė**, lauke Prekės ryšys **pasirinkite prekės** ryšį.
    * Jei lauke **Prekės kodas** nustatyta **Kategorija**, pasirinkite kategorijos ryšį kategorijos **ryšiui**.
    * Jei laukas **Prekės kodas** nustatytas kaip **Visi**, numatytosios vertės taikomos visiems taikomiems įrašams.

5. Nurodykite, kaip taikomas sąskaitos kodas:

    * Jei laukas **Sąskaitos** kodas nustatytas kaip **Lentelė** arba **Grupė**, pasirinkite sąskaitos ryšį lauke **Sąskaitos** ryšys.
    * Jei laukas **Sąskaitos kodas** nustatytas kaip **Visi**, sąskaita taikoma visiems įrašams.

6. **Lauke Pagrindinė** sąskaita pasirinkite atidėjimo pagrindinę sąskaitą.
7. Jei laukas **Atidėjimo registravimo** **metodas** nustatytas kaip Pelnas ir nuostolis, **pasirinkite pradinių įplaukų sąskaitą lauke Pradinių įplaukų sąskaita** **ir įplaukų korespondentinę sąskaitą lauke Įplaukų korespondentinė** sąskaita.
8. Jei laukas **Trumpalaikis atidėjimo** **·** **metodas** nustatytas kaip Esantys laikotarpiai arba Fiksuoti metai, **trumpalaikio atidėjimo sąskaitą pasirinkite lauke Trumpalaikio atidėjimo** sąskaita.
9. Norėdami pridėti eilutę, šablonui **galite** pasirinkti Įtraukti.
10. **Lauke Prekės kodas** pasirinkite prekės kodą.
11. Nurodykite, kaip taikomas prekės kodas:

    * Jei lauke **Prekės kodas** nustatyta Lentelė **arba** **Grupė**, lauke Prekės ryšys **pasirinkite prekės** ryšį.
    * Jei lauke **Prekės kodas** nustatyta **Kategorija**, kategorijos ryšio lauke pasirinkite kategorijos **ryšį**.
    * Jei laukas **Prekės kodas** nustatytas kaip **Visi**, numatytosios vertės taikomos visiems taikomiems įrašams.

12. Nurodykite, kaip taikomas sąskaitos kodas:

    * Jei laukas **Sąskaitos** kodas nustatytas kaip **Lentelė** arba **Grupė**, pasirinkite sąskaitos ryšį lauke **Sąskaitos** ryšys.
    * Jei laukas **Sąskaitos kodas** nustatytas kaip **Visi**, sąskaita taikoma visiems taikomiems įrašams.
    * Pasirinkite tiesiogiai tiesios eilutės šabloną tiesios **eilutės** šablono lauke arba įvykiu pagrįstą šabloną **įvykio šablono** lauke.

13. Pasirinkite **Įrašyti**.

### <a name="for-purchase-orders"></a>Pirkimo užsakymams

Norėdami nurodyti numatytąsias atidėjimo vertes pirkimo užsakymams, atlikite šiuos veiksmus.

1. **Skirtuke Pirkimas** pasirinkite atidėjimo tipą.
2. Pasirinkite **Įtraukti** eilutei įtraukti.
3. **Lauke Prekės kodas** pasirinkite prekės kodą.
4. Nurodykite, kaip taikomas prekės kodas:

    * Jei lauke **Prekės kodas** nustatyta Lentelė **arba** **Grupė**, lauke Prekės ryšys **pasirinkite prekės** ryšį.
    * Jei lauke **Prekės kodas** nustatyta **Kategorija**, kategorijos ryšio lauke pasirinkite kategorijos **ryšį**.
    * Jei laukas **Prekės kodas** nustatytas kaip **Visi**, numatytosios vertės taikomos visiems taikomiems įrašams.

5. Nurodykite, kaip taikomas sąskaitos kodas:

    * Jei laukas **Sąskaitos** kodas nustatytas kaip **Lentelė** arba **Grupė**, pasirinkite sąskaitos ryšį lauke **Sąskaitos** ryšys.
    * Jei laukas **Sąskaitos kodas** nustatytas kaip **Visi**, sąskaita taikoma visiems taikomiems įrašams.

6. **Lauke Pagrindinė** sąskaita pasirinkite atidėjimo pagrindinę sąskaitą.
7. Jei laukas **Atidėjimo registravimo** **metodas** nustatytas kaip Pelnas ir nuostolis, **pasirinkite pradinių įplaukų sąskaitą lauke Pradinių įplaukų sąskaita** **ir įplaukų korespondentinę sąskaitą lauke Įplaukų korespondentinė** sąskaita.
8. Jei laukas **Trumpalaikis atidėjimo** **·** **metodas** nustatytas kaip Esantys laikotarpiai arba Fiksuoti metai, **trumpalaikio atidėjimo sąskaitą pasirinkite lauke Trumpalaikio atidėjimo** sąskaita.
9. Norėdami pridėti eilutę, šablonui **pasirinkite** Įtraukti. 
10. **Lauke Prekės kodas** pasirinkite prekės kodą.
11. Nurodykite, kaip taikomas prekės kodas:

    * Jei lauke **Prekės kodas** nustatyta Lentelė **arba** **Grupė**, lauke Prekės ryšys **pasirinkite prekės** ryšį.
    * Jei lauke **Prekės kodas** nustatyta **Kategorija**, kategorijos ryšio lauke pasirinkite kategorijos **ryšį**.
    * Jei laukas **Prekės kodas** nustatytas kaip **Visi**, numatytosios vertės taikomos visiems taikomiems įrašams.

12. Nurodykite, kaip taikomas sąskaitos kodas:

    * Jei laukas **Sąskaitos** kodas nustatytas kaip **Lentelė** arba **Grupė**, pasirinkite sąskaitos ryšį sąskaitos **ryšiui**.
    * Jei laukas **Sąskaitos kodas** nustatytas kaip **Visi**, sąskaita taikoma visiems taikomiems įrašams.
    * Pasirinkite tiesiogiai tiesios eilutės šabloną tiesios **eilutės** šablono lauke arba įvykiu pagrįstą šabloną **įvykio šablono** lauke.

13. Pasirinkite **Įrašyti**.

### <a name="for-general-journals"></a>Bendr. žurnalams

Norėdami nurodyti bendrojo žurnalo įrašų atidėjimo numatytąsias vertes, atlikite šiuos veiksmus.

1. Pasirinkite skirtuką **Bendrasis žurnalas**.
2. Norėdami įtraukti eilutę, atidėjimui **pasirinkite** Įtraukti.
3. Jei laukas **Trumpalaikis atidėjimo** **·** **metodas** nustatytas kaip Esantys laikotarpiai arba Fiksuoti metai, **trumpalaikio atidėjimo sąskaitą pasirinkite lauke Trumpalaikio atidėjimo** sąskaita.
4. **Lauke Atidėjimo** sąskaita pasirinkite atidėjimo sąskaitą.
5. Lauke Atpažinimo **sąskaita** pasirinkite atpažinimo sąskaitą.
6. Jei laukas **Atidėjimo registravimo** **metodas** nustatytas kaip Pelnas ir nuostolis, **pasirinkite pradinių įplaukų sąskaitą lauke Pradinių įplaukų sąskaita** **ir įplaukų korespondentinę sąskaitą lauke Įplaukų korespondentinė** sąskaita.
7. Pasirinkite tiesiogiai tiesios eilutės šabloną tiesios **eilutės** šablono lauke arba įvykiu pagrįstą šabloną **įvykio šablono** lauke.
8. Pasirinkite **Įrašyti**.

### <a name="for-free-text-invoices"></a>Laisvos formos SF

Norėdami nurodyti laisvos formos SF atidėjimo numatytąsias vertes, atlikite šiuos veiksmus.

1. Pasirinkite skirtuką **Laisvos formos** SF.
2. Norėdami įtraukti eilutę, atidėjimui **pasirinkite** Įtraukti.
3. Nurodykite, kaip taikomas sąskaitos kodas:

    * Jei laukas **Sąskaitos** kodas nustatytas kaip **Lentelė** arba **Grupė**, pasirinkite sąskaitos ryšį lauke **Sąskaitos** ryšys.
    * Jei laukas **Sąskaitos kodas** nustatytas kaip **Visi**, sąskaitos kodas taikomas visiems taikomiems įrašams.

4. **Lauke Atidėjimo** sąskaita pasirinkite atidėjimo sąskaitą.
5. Jei laukas **Trumpalaikis atidėjimo** **·** **metodas** nustatytas kaip Esantys laikotarpiai arba Fiksuoti metai, **trumpalaikio atidėjimo sąskaitą pasirinkite lauke Trumpalaikio atidėjimo** sąskaita.
6. Lauke Atpažinimo **sąskaita** pasirinkite atpažinimo sąskaitą.
7. Jei laukas **Atidėjimo registravimo** **metodas** nustatytas kaip Pelnas ir nuostolis, **pasirinkite pradinių įplaukų sąskaitą lauke Pradinių įplaukų sąskaita** **ir įplaukų korespondentinę sąskaitą lauke Įplaukų korespondentinė** sąskaita.
8. Pasirinkite tiesiogiai tiesios eilutės šabloną tiesios **eilutės** šablono lauke arba įvykiu pagrįstą šabloną **įvykio šablono** lauke.
9. Pasirinkite **Įrašyti**.

### <a name="for-invoice-journals"></a>SF žurnalams

Norėdami nurodyti SF žurnalo įrašų atidėjimo numatytąsias vertes, atlikite šiuos veiksmus.

1. Pasirinkite skirtuką **SF žurnalas**.
2. Norėdami įtraukti eilutę, atidėjimui **pasirinkite** Įtraukti.
3. Nurodykite, kaip taikomas sąskaitos kodas:

    * Jei laukas **Sąskaitos** kodas nustatytas kaip **Lentelė** arba **Grupė**, pasirinkite sąskaitos ryšį lauke **Sąskaitos** ryšys.
    * Jei laukas **Sąskaitos kodas** nustatytas kaip **Visi**, sąskaitos kodas taikomas visiems taikomiems įrašams.

4. **Lauke Atidėjimo** sąskaita pasirinkite atidėjimo sąskaitą.
5. Jei laukas **Trumpalaikis atidėjimo** **·** **metodas** nustatytas kaip Esantys laikotarpiai arba Fiksuoti metai, **trumpalaikio atidėjimo sąskaitą pasirinkite lauke Trumpalaikio atidėjimo** sąskaita.
6. Lauke Atpažinimo **sąskaita** pasirinkite atpažinimo sąskaitą.
7. Jei laukas **Atidėjimo registravimo** **metodas** nustatytas kaip Pelnas ir nuostolis, **pasirinkite pradinių įplaukų sąskaitą lauke Pradinių įplaukų sąskaita** **ir įplaukų korespondentinę sąskaitą lauke Įplaukų korespondentinė** sąskaita.
8. Pasirinkite tiesiogiai tiesios eilutės šabloną tiesios **eilutės** šablono lauke arba įvykiu pagrįstą šabloną **įvykio šablono** lauke.
9. Pasirinkite **Įrašyti**.

### <a name="items-that-are-deferred-by-default"></a>Pagal numatytuosius nustatymus atidėtos prekės

Norėdami nurodyti **, kurios prekės atidėtos pagal numatytuosius** nustatymus, naudokite atidėtas prekes. Galite nustatyti operacijų tipus, kurių prekės bus atidėtos. Galite nurodyti, ar viena prekė atidėta, ar visa prekių grupė ar kategorija.

Kai nustatote prekes kaip atidėtas, pasirinkite numatytąsias sąskaitas ir šablonus **atidėjimo numatytųjų nustatymų** puslapyje. Jei sąskaitos ir šablonai nepasirinkti, operacijos eilutės, kuriose įvestos prekės, nebus atidėtos.

Prekėms, kurios atidėtos pagal pardavimo ar pirkimo kategoriją, su ja susietos, atidėjimo parametrai yra pagrįsti kategorija. Tačiau, jei kategorija nėra pasirinkta kategorijos **ryšio** lauke, naudojami aukštesnio rango kategorijos atidėjimo parametrai. Pavyzdžiui, įtraukiate namų vaizdo įrašų **pardavimo** kategoriją, o ne pardavimo internetu **kategoriją**. Kai pridedate atidėjimo prekę, kuri susieta **su išlaidų kategorija**, **prekei naudojami pagrindinio vaizdo** įrašo atidėjimo parametrai.

### <a name="set-up-deferred-items"></a>Nustatyti atidėtas prekes

Norėdami nustatyti prekes, kurios atidėtos pagal numatytuosius nustatymus, atlikite šiuos veiksmus.

1. Atidėtų **pagal numatytuosius nustatymus** prekių puslapyje pasirinkite norimą skirtuką: **Pardavimo užsakymas** arba **Pirkimas**.
2. Pasirinkite **Įtraukti** eilutei įtraukti.
3. **Lauke Prekės kodas** pasirinkite prekės kodą.
4. Nurodykite, kaip taikomas prekės kodas:

    * Jei lauke **Prekės kodas** nustatyta Grupė **arba** **Lentelė**, lauke Prekės ryšys pasirinkite **prekės** ryšį.
    * Jei lauke **Prekės kodas** nustatyta **Kategorija**, kategorijos ryšio lauke pasirinkite kategorijos **ryšį**.

5. Kiekvienai papildomai eilutei, kurios reikia, pakartokite 2–4 žingsnius.
6. Pasirinkite **Įrašyti**.

## <a name="deferred-charges"></a>Atidėti mokesčiai

Norėdami nurodyti **, kuriuos mokesčius atidėti pagal** numatytuosius nustatymus, naudokite atidėjimo išlaidų puslapį.

> [!NOTE]
> * Šiuo metu atidėjimo išlaidas galima naudoti tik pardavimo užsakymams.
> * Išlaidos gali būti atidėtos tik eilutės lygiu. Norėdami atidėti išlaidas pardavimo užsakymo antraštės lygiu, galite nustatyti juos kaip atidėtą prekę atskiroje pardavimo užsakymo eilutėje.
> * Norėdami atidėti laisvos formos SF mokestį, turite įvesti mokestį kaip atskirą atidėtos SF eilutę.
> * Šios funkcijos negalima naudoti palaikymo mokesčiams ir įplaukų skaidymo funkcijai.

### <a name="set-up-deferred-charges"></a>Nustatyti atidėtus mokesčius

Norėdami nustatyti atidėtus mokesčius, atlikite šiuos veiksmus.

1. Puslapyje Atidėjimo **mokesčiai** pasirinkite Įtraukti **, kad** įtraukumėte eilutę.
2. **Lauke Mokesčio kodas** pasirinkite išlaidų kodą.
3. Lauke Išlaidų **ryšys** pasirinkite išlaidų ryšį.
4. Kiekvienai papildomai eilutei, kurios reikia, pakartokite 1–3 veiksmus.
5. Pasirinkite **Įrašyti**.

## <a name="event-based-deferral-templates"></a>Įvykiais grįsti atidėjimo šablonai

Naudokite atidėjimo **pagal įvykį šablonų** puslapį norėdami nustatyti atidėjimo šablonus, pagrįstus įvykiu, kuriuos galite naudoti atidėjimo **operacijose ir priskirti atidėjimų numatytųjų nustatymų** puslapyje.

### <a name="create-an-event-based-template"></a>Įvykio šablono kūrimas

Norėdami kurti atidėjimo šablono įvykį, atlikite šiuos veiksmus.

1. Įvykio pagrįstame **atidėjimo šablonų** puslapyje pasirinkite **Naujas**.
2. **Lauke Šablonas** įveskite unikalų šablono pavadinimą.
3. Lauke **Aprašas** įveskite aprašą.
4. **Lauke Paskirstymo tipas** pasirinkite paskirstymo tipą:

    * **Kintama** suma – paskirstykite konkrečią sumą kiekvienai įvestai eilutei.
    * **Lygi suma** – paskirstykite tą pačią sumą kiekvienai įvestai eilutei. 
    * **Procentas** – paskirstykite sumą, kuri remiasi procentine verte, kuri įvedama kiekvienai eilutei.
    * **Baigimo procentas** – kiekvienai įvestai eilutei priskirti kaupiamąją užbaigimo vertę.
    * **Kintamas** kiekis – paskirstykite konkretų kiekį kiekvienai įvestai eilutei.

5. Nustatykite **pasirinktį** **Kurti** atskirus įvykius vienetui kaip Taip, jei norite, kad kiekviena įvykio eilutė būtų padalyta tolygiai pagal SF operacijos vienetų skaičių. Nustatykite ją **kaip** Ne, jei nenorite skaidyti įvykio eilučių.
6. Lauke Galiojimo **pabaigos sąskaita** pasirinkite galiojimo pabaigos sąskaitą.
7. **Norėdami** į eilučių sąrašą įtraukti eilutę, pasirinkite Įtraukti, o jei norite pridėti eilutę, esančią sąrašo apačioje, **pasirinkite** Pridėti.
8. **Lauke Aprašymas** įveskite įvykio aprašymą.
9. Jei lauke **Paskirstymo tipas** nustatyta Procentinė **reikšmė**, nurodykite paskirstymo procentą lauke **Paskirstymo** procentas. Procentas turi būti nuo 0 (nulio) iki 100. Jei paliekate lauką **Paskirstymo procentas** tuščią, procentas laikomas 0. Visų procentų suma rodoma puslapio apačioje lauke **Bendrasis** procentas ir turi būti lygi 100.
10. Lauke Mėnesių **pabaigos data** nurodykite mėnesių skaičių, nuo kada galioja įvykis. Remiantis šia verte automatiškai įvedama operacijos atidėjimo galiojimo data.
11. Pažymėti žymės langelį **Atpažinti užregistrus**, kad operacijos registravimo metu įplaukos būtų automatiškai atpažįstamos. Jei žymės langelį išvalote, įplaukos turi būti atpažintos rankiniu būdu.
12. Lauke Atpažinimo **sąskaita** pasirinkite įvykio atpažinimo sąskaitą, jei įvykis naudoja kitą sąskaitą nei visas atidėjimo grafikas. Šis laukas naudojamas kartu su žymės langeliu **Atpažinti užregistrėjus**.
13. Kiekvienai papildomai eilutei, kurios jums reikia, pakartokite veiksmus nuo 7 iki 12.
14. Pasirinkite **Įrašyti**.
