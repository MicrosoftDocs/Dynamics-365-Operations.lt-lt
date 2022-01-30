---
title: Kurti išlaidų kodus
description: Šioje temoje paaiškinama, kaip konfigūruoti mokėtinų sumų ir gautinų sumų mokesčių kodus.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MarkupTable
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 034be190890a67fd0921d40fffdc704b9d6d5df7
ms.sourcegitcommit: 5bfd6511d710deb539b4030eb0e9c48d25513595
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/19/2022
ms.locfileid: "8014114"
---
# <a name="create-charges-codes"></a>Kurti išlaidų kodus

Šioje temoje paaiškinama, kaip konfigūruoti mokėtinų sumų ir gautinų sumų mokesčių kodus. Jei jūsų organizacija reikalauja, kad pardavimo arba pirkimo sumos būtų sekamos kartu su pardavimo arba pirkimo užsakymo eilučių prekėmis, šiam tikslui galite naudoti išlaidų kodus. Pavyzdžiui, jūs mokate transportą ir draudimą pagal pirkimo užsakymą, o šios sumos pirkimo užsakyme nurodomos atskirai. Tokiu atveju galite nurodyti, ar sumos registruojamos išlaidų sąskaitose, ar pridėtos prie prekių išlaidų.

## <a name="set-up-charges-codes-for-accounts-receivable"></a>Nustatyti gautinų sumų mokesčių kodus

Norėdami kurti gautinų sumų mokesčių kodus, atlikite šiuos veiksmus.

1. Eikite **į gautinų** &gt; **sumų mokesčių nustatymo** &gt; **mokesčių kodą**.
2. Pasirinkite **Nauja**.
3. Lauke **Išlaidų** kodas įveskite išlaidų kodą.
3. Lauke **Aprašymas** įveskite išlaidų aprašymą.
4. Pasirinktinai: **lauke Prekės PVM grupė pasirinkite PVM** grupę.
5. **·**"FastTab" registravimas nurodykite, kaip mokestis turėtų būti automatiškai debetuojamas ir kredituojamas.
6. Jei DK sąskaitą pasirinkote kaip debeto tipą arba kredito tipą, nurodykite registravimo tipą laukuose Registravimas ir nurodykite pagrindinę sąskaitą **sąskaitos** **·** **laukuose**.

### <a name="example"></a>Pavyzdys

Mokestį moka jūsų klientas. Todėl jis pridedamas prie bendrųjų pardavimo užsakymo sumų. Nustatykite šią registravimo informaciją:

- Norėdami SF išlaidas įtraukti į kliento kodą, debeto skyriaus lauke Tipas **pasirinkite** **·** **Klientas**/tiekėjas.
- Kredito **skyriaus** lauke **Tipas pasirinkite** DK **sąskaitą**. Tada lauke Sąskaita **pasirinkite** pagrindinę įplaukų iš SF mokesčių sąskaitą.

> [!NOTE]
> Jei pasirinkto kodo debeto tipas arba kredito tipas yra DK sąskaita **arba** **prekė**, galite įvesti kitą išlaidų operacijos valiutą.

Galite spausdinti išlaidų tekstą klientui priskirta kalba. Norėdami nurodyti išlaidų kodo tekstą kitomis kalbomis, pasirinkite **Vertimai**.

## <a name="set-up-charges-codes-for-accounts-payable"></a>Nustatyti mokėtinų sumų išlaidų kodus

Norėdami kurti mokėtinų sumų mokesčių kodus, atlikite šiuos veiksmus.

1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Eikite **į mokėtinų** &gt; **sumų išlaidų** **nustatymo mokesčių** &gt; **kodą**.
    - Eikite **į įsigijimo ir išlaidų nustatymo išlaidų** &gt; **·** &gt; **·** &gt; **kodą**.

2. Pasirinkite **Nauja**.
3. Lauke **Išlaidų** kodas įveskite išlaidų kodą.
3. Lauke **Aprašymas** įveskite išlaidų aprašymą.
4. Pasirinktinai: **lauke Prekės PVM grupė pasirinkite PVM** grupę.
5. Pasirinktinai: lauke **Maksimali suma įveskite** maksimalią leistiną išlaidų kodo sumą.

    Šis laukas naudojamas tiekėjo SF išlaidoms tikrinti. Norėdami įgalinti išlaidų tikrinimą, mokėtinų sumų parametrų puslapio skirtuke SF tikrinimas pažymėkite žymės langelį Įgalinti **SF** **·** **gretinimo** tikrinimą.

    > [!IMPORTANT]
    > Norėdami tikrinti SF išlaidas, taip pat turite sukurti strategijos taisyklės tipo egzempliorių, pagrįstą konkrečios tiekėjo SF strategijos mokesčiais.

6. **·**"FastTab" registravimas nurodykite, kaip mokestis turėtų būti automatiškai debetuojamas ir kredituojamas.
7. Jei pasirinkote DK sąskaitą kaip debeto tipą arba kredito tipą, nurodykite registravimo tipą laukuose Debeto registravimas ir Kredito registravimas bei nurodykite pagrindinę sąskaitą laukuose Debeto sąskaita **ir** Kredito **·** **·** **·** **sąskaita**.
8. Norėdami įjungti SF išlaidų verčių, kuriose yra atitinkamos pirkimo užsakymo antraštės ar eilučių išlaidos, palyginimą, pažymėkite žymės langelį Palyginti pirkimo užsakymo ir **SF** vertes.

### <a name="example"></a>Pavyzdys

Galite įrašyti išlaidas kaip išlaidas, kaip bendrą pirkimo užsakymo arba tiekėjo SF sumą. Norėdami nustatyti registravimo informaciją, atlikite šiuos veiksmus. 

- Norėdami SF išlaidas įtraukti į tiekėjo kodą, kredito skyriaus lauke Tipas **pasirinkite** **·** **Klientas**/tiekėjas.
- Debeto **skyriaus** lauke **Tipas pasirinkite DK** **sąskaitą**. Tada lauke **Sąskaita** pasirinkite pagrindinę išlaidų sąskaitą iš SF mokesčių.

Norėdami nustatyti registravimo informaciją, kad vieneto mokestis būtų pridėtas prie prekės išlaidų, atlikite šiuos veiksmus.

- Norėdami SF išlaidas įtraukti į tiekėjo kodą, kredito skyriaus lauke Tipas **pasirinkite** **·** **Klientas**/tiekėjas.
- Norėdami pridėti išlaidas prie prekės išlaidų, lauke Tipas **pasirinkite** **·** **Prekė**.

> [!NOTE]
> Galbūt norėsite naudoti valiutą, kuri skiriasi nuo pirkimo užsakyme arba SF nurodytos valiutos. Galite įvesti kitą valiutą, jei pasirinkto kodo debeto tipas arba kredito tipas yra **DK sąskaita** arba **prekė**.

Galite spausdinti išlaidų tekstą klientui priskirta kalba. Norėdami nurodyti išlaidų kodo tekstą kitomis kalbomis, pasirinkite **Vertimai**.
