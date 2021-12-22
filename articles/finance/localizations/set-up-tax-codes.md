---
title: Nustatyti mokesčių kodus
description: Šioje temoje paaiškinama, kaip nustatyti mokesčių kodus Mokesčių skaičiavimo paslaugoje.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 8bdb194e7d8b704d1e58d3c25bf2e1f6bff1ba00
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883910"
---
# <a name="set-up-tax-codes"></a>Nustatyti mokesčių kodus

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti mokesčių kodus Mokesčių skaičiavimo tarnybose. Ją sudaro paprasto scenarijaus nustatymas, siekiant, kad mokesčio kodas veiktų, ir informacija apie kai kurias išplėstas mokesčių kodo funkcijas sudėtinguose scenarijuose.

> [!IMPORTANT]
> Mokesčių kodų nustatymas mokesčių skaičiavimo paslaugoje yra juridinis subjektas – agnostinis. Šį nustatymą reguliavimo konfigūracijos tarnybos (RCS) galite užbaigti tik vieną kartą. Mokesčių kodai automatiškai sinchronizuojami su Dynamics 365 Finance "Microsoft", kai įgalinate pasirinkto juridinio subjekto mokesčių skaičiavimo paslaugą finansuose.

## <a name="simple-setup"></a>Paprastas nustatymas

Norėdami naudoti mokesčio kodą paprastoje scenarijuje, pvz., scenarijuje, kuriame yra tik vienas mokesčio tarifas, atlikite šiuos veiksmus.

1. Prisijungti prie [reguliavimo konfigūracijos tarnybos](https://marketing.configure.global.dynamics.com/).
2. Eikite **į darbo sričių** \> **globalizavimo priemones Mokesčių** \> **skaičiavimas.**
3. Pasirinkite priemonę ir versiją, kurią norite nustatyti, ir pasirinkite **Redaguoti**.
4. Skirtuke **Bendra** pasirinkite Konfigūracijos **versija**.
5. Skirtuke **Mokesčių kodai** **pasirinkite** Įtraukti, tada įveskite mokesčio kodą ir aprašymą.
6. Pasirinkite **Skaičiavimo** kilmę. Skaičiavimo šaltinis yra metodų grupė, nurodyta jūsų pasirinktoje mokesčių konfigūracijos versijoje. Šiame paprastame scenarijuje pasirinkite **Pagal grynąją** sumą.
7. Pasirinkite **Įrašyti**. Daugiau laukų tampa galimi, remiantis jūsų pasirinkta skaičiavimo kilme.
8. Norėdami pridėti **vieną šio mokesčio kodo mokesčio** **tarifą, "FastTab"** tarifuose pasirinkite Įtraukti.
9. Pasirinkite **Įrašyti**.

## <a name="calculation-origin"></a>Apskaičiavimo pagrindas

Skaičiavimo šaltinis nurodo, kaip apskaičiuojama mokesčio pagrindinė suma ir mokesčio suma. Jį sukonfigūravo elektroninės ataskaitos **darbo** srityje konfigūravimas. Šios vertės galimos lauke **Skaičiavimo** šaltinis:

- Pagal grynąją sumą
- Pagal sumą su mokesčiais
- Pagal kiekį
- Pagal maržą
- Mokestis nuo mokesčio

### <a name="by-net-amount"></a>Pagal grynąją sumą

Jei lauke Skaičiavimo šaltinis pasirenkate Pagal grynąją sumą, mokesčio suma apskaičiuojama kaip pirkimo ar pardavimo sumos procentas, neįtraukiant **visų** kitų mokesčių **kodų**.

Pavyzdžiui, mokesčio tarifas yra 25 proc., SF eilutėje rodomas 10 prekių kiekis po 1,00 ir klientui leidžiama 10 procentų eilutės nuolaida. Šiuo atveju sumos skaičiuojamos taip:

- **Grynoji suma:** (10 × 1,00) – 10 procentų = 9,00 
- **PVM:** 9,00 × 25 procentų = 2,25 
- **Bendra SF suma:** 9,00 + 2,25 = 11,25

### <a name="by-gross-amount"></a>Pagal sumą su mokesčiais

Jei lauke **Skaičiavimo šaltinis** pasirenkate Pagal bendrą sumą, mokesčio suma skaičiuojama kaip bendrojo pardavimo sumos **procentas**. Bendra suma yra eilutės grynoji suma plius visi eilutės mokesčiai ir mokesčiai, išskyrus vieną mokestį, kai skaičiavimo kilmės laukas nustatytas **kaip** Pagal bendrą **sumą**.

Pavyzdžiui, mokesčių institucija nustato prekei specialius muito mokesčius. Muito mokesčio sumos pridedamas prie grynosios sumos prieš skaičiuojant mokestį. Naudojami šie mokesčių kodai:

- **1 muito** mokestis – tarifas yra 10 procentų, **ir naudojamas grynosios sumos skaičiavimo** metodas.
- **2 muito** mokestis – tarifas yra 20 procentų, **ir naudojamas grynosios sumos skaičiavimo** metodas.
- **Mokesčio** tarifas – tarifas yra 25 procentai, **ir naudojamas bendrosios sumos skaičiavimo** metodas.

Jei grynoji suma yra 10,00, 1 muito mokesčio suma yra 1.00 (10.00 × 10 procentų), o 2 muito mokesčio suma yra 2.00 (10.00 × 20 procentų). Šiuo atveju sumos skaičiuojamos taip: 

- **Bendroji suma: grynoji suma + 1 muito mokesčio suma + 2 muito mokesčio suma** = 10,00 + 1,00 + 2,00 = 13,00 
- **Mokesčio suma:** 13,00 × 25 procentų = 3,25 
- **Bendra muito mokesčių suma:** 1,00 + 2,00 + 3,25 = 6,25 
- **Bendra SF suma:** 10,00 + 6,25 = 16,25

### <a name="by-quantity"></a>Pagal kiekį

Jei pasirenkate kiekį Pagal lauke Skaičiavimo šaltinis, mokesčio suma skaičiuojama kaip fiksuota vieneto suma ir dauginama iš dokumento **eilutėje** **įvesto** kiekio. Vieneto suma nurodoma **Tarifų** "FastTab".

Pavyzdžiui, vieneto mokesčio kodas nustatomas kaip 1,20. Pardavimo SF eilutėje parduodama 25 prekės vienetai. Šiuo atveju mokesčio suma apskaičiuojama kaip 25 × 1,20 = 30,00.

### <a name="by-margin"></a>Pagal maržą

Jei lauke **Skaičiavimas** pasirenkate **Maržą**, mokesčių suma skaičiuojama kaip pardavimo maržos procentas. Pardavimo marža – tai pardavimo suma, iš kurios atimama išlaidų suma. Šis skaičiavimo metodas taikomas tik pardavimo operacijoms.

Pavyzdžiui, mokesčio tarifas yra 25 proc., SF eilutėje rodomas 10 prekių kiekis po 10,00 ir prekės savikaina yra 6. Šiuo atveju sumos skaičiuojamos taip:

- **Pardavimo marža:** 10 × ( 10,00 – 6,00) = 40,00
- **Mokesčio suma:** 40,00 × 25 procentai = 10,00
- **Bendra SF suma:** 100,00 + 10,00 = 110,00

### <a name="tax-on-tax"></a>Mokestis nuo mokesčio

Jei pasirenkate mokestį mokesčiui skaičiavimo kilmės lauke, PVM yra skaičiuojamas kaip visų kitų tos pačios **dokumento eilutės mokesčių sumų** **procentas**.

Pavyzdžiui, naudojami šie mokesčių kodai:

- **1 muito** mokestis – tarifas yra 10 procentų, **ir naudojamas grynosios sumos skaičiavimo** metodas.
- **2 muito** mokestis – tarifas yra 20 procentų, **ir naudojamas grynosios sumos skaičiavimo** metodas.
- **Muito mokestis** – tarifas yra 25 procentai, **ir naudojamas mokesčio apskaičiavimo** metodas.

Šiuo atveju sumos skaičiuojamos taip:

- **Grynoji suma:** 10,00 
- **1 muito mokestis:** 10,00 × 10 procentų = 1,00 
- **2 muito mokestis:** 10,00 × 20 procentų = 2,00 
- **Muito mokesčio mokestis:** 3,00 × 25 procentų = 0,75
- **Bendra mokesčių suma:** 1,00 + 2,00 + 0,75 = 3,75 
- **Bendra SF suma:** 10,00 + 3,75 = 13,75

## <a name="advanced-functionality"></a>Išplėstinės funkcijos

Šiame skyriuje paaiškinamos kai kurios išplėstinės mokesčių kodo nustatymo funkcijos sudėtinguose scenarijuose.

### <a name="tax-exemption"></a>Atleidimas nuo mokesčio

Jei bendrajame "FastTab" nustatote pasirinktį Atleista nuo mokesčio, mokesčio suma visada bus nepaisoma **į** **·** **0** (nulis), neatsižvelgiant į faktinį mokesčio tarifą.

Norėdami nurodyti **lengvatos** priežastį, galite nustatyti lauką Neapmokestinimo kodas. 

Galite įjungti neapmokestinimo kodo lauko pagrindinių **duomenų** peržvalgą. Tada galite pasirinkti iš neapmokestinimo kodų verčių, apibrėžtų dalyje Finansai. Informacijos apie tai, kaip įgalinti pagrindinių duomenų peržvalgą, [ieškokite Įgalinti mokesčių skaičiavimo konfigūracijos pagrindinių duomenų peržvalgą.](tax-service-set-up-environment-master-data-lookup.md)

Pavyzdžiui, mokesčio tarifas yra 25 proc., o mokesčio kode pasirinktis Neapmokestinama **nustatyta** kaip **Taip**. SF eilutėje rodoma 10 prekių ir kiekviena po 1,00, o klientui leidžiama 10% eilutės nuolaida. Šiuo atveju sumos skaičiuojamos taip:

- **Grynoji suma:** (10 × 1,00) – 10 procentų = 9,00 
- **PVM:** 0,00 
- **Bendra SF suma:** 9,00 + 0,00 = 9,00

### <a name="use-tax"></a>Naudojimo mokestis

Jei bendrajame "FastTab" nustatote parinktį Naudojimo mokestis kaip Taip, mokesčio suma bus registruojama mokėtino naudojimo mokesčio sąskaitoje, **·** **·** **·** **o** ne **tiekėjo sumoje** sąskaitoje.

Pvz., mokesčio tarifas yra 25 proc., o parinktis Ar naudojimo mokestis mokesčio kode **nustatyta** kaip **Taip**. SF eilutėje rodoma 10 prekių ir kiekviena po 1,00, o klientui leidžiama 10% eilutės nuolaida. Šiuo atveju sumos skaičiuojamos taip:

- **Grynoji suma:** (10 × 1,00) – 10 procentų = 9,00 
- **Naudojimo mokestis:** 9,00 × 25 procentų = 2,25
- **Bendra SF suma:** 9,00 + 0,00 = 9,00

> [!IMPORTANT]
> Jeigu abi pasirinktis Yra neapmokestinama, o parinktis Naudojimo mokestis mokesčio kode nustatyta kaip Taip, kodas bus pripažintas kaip neapmokestinamas pardavimo operacijoms ir naudojimo mokestis **pirkimo** **·** **operacijoms**.

### <a name="reverse-charges"></a>Atvirkštiniai mokesčiai

Jei **bendrajame** "FastTab" nustatote parinktį Yra **atvirkštinis** **mokestis kaip** Taip, mokesčių tarifą galima konfigūruoti kaip neigiamą. Atvirkštinio apmokestinimo scenarijui rekomenduojame nustatyti du mokesčių kodus: vieną, kuris turi teigiamą mokesčio tarifą, o kitą – neigiamą mokesčio tarifą. Abiejų mokesčių kodų tarifo vertė turi būti tokia pati, o parinktis Yra atvirkštinis apmokestinimas mokesčių kode, kuriame **yra** neigiamas mokesčio **tarifas**, turi būti nustatyta kaip Taip. Daugiau informacijos apie „Finance“ mokėjimo atšaukimas rasite PVM / [GST schemos atvirkštinio apmokestinimo](emea-reverse-charge.md) mechanizmą.

Pavyzdžiui, du mokesčių kodai yra nustatomi vienoje SF eilutėje. Vienas mokesčio tarifas yra 25 procentai. Kitas mokesčio tarifas yra -25 proc., o antrojo mokesčio kodo parinktis **Yra** nustatyta kaip **Taip**. SF eilutėje rodoma 10 prekių (po 1,00). Šiuo atveju sumos skaičiuojamos taip:

- **Grynoji suma:** (10 × 1,00) = 10,00 
- **1 mokesčio kodas:** 10,00 × 25 procentai = 2,50
- **Mokesčio kodas 2:** 10 × -25 procentų = -2,50
- **Bendra SF suma:** 10,00 + 2,50 -2,50 = 10,00

### <a name="exclusion-from-base-amount-calculations"></a>Pašalinimas iš bazinės sumos skaičiavimų

Jei **bendrajame** **·** **"FastTab" nustatote parinktį Pašalinti iš bazinės sumos skaičiavimo kaip Taip, apskaičiuota mokesčio kodo mokesčio suma neįtraukiama į kitų mokesčių kodų skaičiavimų pagrindinę sumą kainos įskaitos** scenarijuje.

Daugiau informacijos rasite Kainų [mokesčio skaičiavimas, kai įgalintas kainos su](global-exclude-from-tax-base-amount-calculation.md) mokesčiais.

### <a name="rates"></a>Tarifai

Kurso **FastTab** galite nurodyti skirtingus mokesčių tarifus skirtingiems mokesčio pagrindo diapazonams. Apskaičiuodama mokesčio sumą mokesčių skaičiavimo tarnyba visada naudoja tarifą, kuris atitinka mokesčio pagrindą.

Pavyzdžiui, mokesčių tarifai gali būti konfigūruoti, kaip parodyta pateiktoje lentelėje.

| Minimali suma | Didžiausia suma | Mokesčio tarifas   |
| -------------- | -------------- | ---------- |
| 0              | 1000          | 10 procentų |
| 1000          | 5000          | 15 procentų |
| 5000          | 10,000         | 20 procentų |
| 10,000         | 0              | 30 procentų |

Šiuo atveju mokesčio suma apskaičiuojama tokiu būdu:

- Jei mokesčio bazinė suma yra 300,00, mokesčio tarifas yra 10 procentų, o mokesčio suma yra 300,00 × 10 procentų = 30,00.
- Jei mokesčio bazinė suma yra 3000,00, mokesčio tarifas yra 15 procentų, o mokesčio suma yra 3000,00 × 15 procentų = 450,00.
- Jei mokesčio bazinė suma yra 6000,00, mokesčio tarifas yra 20 procentų, o mokesčio suma yra 6000,00 × 10 procentų = 1200,00.
- Jei mokesčio bazinė suma yra 20,000.00, mokesčio tarifas yra 30 procentų, o mokesčio suma yra 20,000.00 × 30 procentų = 6 000,00.

> [!NOTE]
> Jei mokesčio bazinė suma gali sutapti su maksimalia vienos eilutės suma ir mažiausia suma kitoje eilutėje, pagrindui bus naudojamas mokesčio tarifas, kuris atitinka minimalią pagrindą. Pavyzdžiui, jei mokesčio bazinė suma yra 1000,00, mokesčio tarifas yra 15 procentų, o mokesčio suma yra 1000,00 × 15 procentų = 150,00.

### <a name="limits"></a>Ribos

Jei mokesčio suma patenka į minimalų/maksimalų diapazoną, Limitų FastTab galite nurodyti mokesčio ribas, kad būtų nepaisoma **apskaičiuotos** mokesčio sumos.

- Jei apskaičiuota mokesčio suma yra didesnė arba lygi maksimaliai mokesčio sumai, kuri sukonfigūruota "FastTab" Ribos, galutinė mokesčio suma yra lygi **maksimaliai** mokesčio sumai.
- Jei apskaičiuota mokesčio suma yra mažesnė nei minimali mokesčio suma, sukonfigūruota "FastTab" Ribos, galutinė mokesčio suma yra **0** (nulis).

Pvz., mokesčių limitai konfigūruoti taip:

- **Minimali mokesčio suma:** 100 
- **Maksimali mokesčio suma:** 1000

Jei apskaičiuota mokesčio suma yra 2000, galutinė mokesčio suma yra 1000.

Jei apskaičiuota mokesčio suma yra 500, galutinė mokesčio suma yra 500.

Jei apskaičiuota mokesčio suma yra 80, galutinė mokesčio suma yra 0 (nulis).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
