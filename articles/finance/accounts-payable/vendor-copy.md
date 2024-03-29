---
title: Tiekėjų kopijavimas naudojant bendrinamas numeracijas
description: Šiame straipsnyje paaiškinama, kaip, naudojant bendrinamas numeracijas, tiekėją nukopijuoti į kitą juridinį subjektą, bet išlaikyti tą patį tiekėjo ID.
author: sunfzam
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7b7285cdf454955656c4fb20c3abf68f3f9c39dc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904907"
---
# <a name="copy-vendors-by-using-shared-number-sequences"></a>Tiekėjų kopijavimas naudojant bendrinamas numeracijas

[!include [banner](../includes/banner.md)]

Naudodami bendrinamas numeracijas, galite priskirti tiekėjų ID. Bendrinamos numeracijos taip pat leidžia tiekėjus iš vieno juridinio subjekto kopijuoti į kitą juridinį subjektą, bet naudoti tuos pačius tiekėjų ID abiejuose juridiniuose subjektuose.

## <a name="setup"></a>Sąranka

Ši funkcija suaktyvinama, kai, naudodami bendrinamą numeraciją, priskiriate tiekėjų ID. Tą pačią numeraciją turite naudoti kiekviename juridiniame subjekte, į kurį norite nukopijuoti tiekėją. Kiekvieno juridinio subjekto tiekėjo numeracija keičiama puslapyje **Mokėtinų sumų parametrai**. Pasirinkite **Mokėtinos sumos** \> **Sąranka** \> **Mokėtinų sumų parametrai**, tada – skirtuką **Numeracijos**.

Tiekėjų numeracijas taip pat galite nustatyti kiekvienai tiekėjų grupei. Šios numeracijos taip pat turi būti bendrinamos. Pirmiausia naudojama tiekėjų grupės numeracija. Jei tiekėjų grupės numeracijų nenurodyta, naudojama numeracija, nurodyta puslapyje **Mokėtinų sumų parametrai**.

Tiekėjus kopijuoti tarp juridinių subjektų taip pat galite, jei naudojate neautomatinius tiekėjų ID. Tačiau, jei tiekėją bandysite nukopijuoti į juridinį subjektą, kuriame tiekėjo ID jau yra, kopijavimo procesas nebus pradėtas.

## <a name="copy-a-vendor"></a>Tiekėjo kopijavimas

Norėdami kopijuoti tiekėją, sąrašo puslapyje **Visi tiekėjai** pasirinkite **Naujas**, kad atidarytumėte puslapį **Visi tiekėjai, naujas įrašas**. Naujasis tiekėjo ID nėra priskiriamas iš karto. Ankstesnėse versijose buvo kitaip. Kadangi dar nepasirinkote tiekėjų grupės, negalima nustatyti teisingos naudotinos numeracijos. Be to, ji negali nustatyti, ar bandote sukurti naują tiekėją, ar tiekėją kopijuoti. Todėl tiekėjo ID nepriskiriamas tol, kol puslapio apačioje nepasirenkate **Įrašyti**.

Jei kuriate naują tiekėją, galite įprastai toliau užpildyti visus laukus. Baigus ir pasirinkus **Įrašyti**, tiekėjo ID bus priskirtas automatiškai. O neautomatinių numeracijų atveju matysite, kad buvo panaudotas jūsų neautomatinis tiekėjo ID.

Norėdami nukopijuoti tiekėją, lauke **Vardas** įveskite vieną ar kelis simbolius, atitinkančius jūsų ieškomą tiekėją. Ieškos dialogo lange rodomas šalių, kurios gali būti jūsų ieškomas tiekėjas, sąrašas. Kai pasirenkate vieną iš šalių, dešinėje dialogo lango pusėje pasirodo papildoma tolesnė informacija.

- Skirtuke **Bendra** rodomas šalies telefono numeris ir adresas.
- Skirtuke **Vaidmenys** rodomi vaidmenys, kuriuos gali turėti pasirinkta šalis, ir juridinis subjektas, kuriame ji turi kiekvieną vaidmenį.
- Skirtuke **Mokesčių registracijos ID** rodomi šaliai priskirti mokesčių registracijos ID.

Šalį galite kopijuoti tik tada, jei ji turi tiekėjo vaidmenį ir jei tą vaidmenį ji turi juridiniame subjekte, kuris nėra dabartinis juridinis subjektas. Radę šiuos kriterijus atitinkančią šalį, atlikite šiuos veiksmus.

1. Pasirodo parinktis **Kopijuoti tiekėją**. Pagal numatytuosius parametrus ši parinktis yra nustatyta kaip **Ne**. Norėdami tiekėją nukopijuoti į dabartinį juridinį subjektą, parinktį nustatykite kaip **Taip**. 
2. Pasirodo laukas **Juridinis subjektas**. Pasirinkite juridinį subjektą, iš kurio kopijuoti tiekėją. Jei tiekėjas yra tik viename juridiniame subjekte, pagal numatytuosius parametrus laukas nustatomas kaip tas juridinis subjektas.
3. Pasirinkite **Pasirinkti**. Sukuriamas naujas tiekėjas.

## <a name="validation"></a>Patikrinimas

Nukopijavus tiekėją, bus bandoma įrašyti naujojo tiekėjo informaciją. Vykdomos patikros, kuriomis tikrinama, ar nukopijuoti duomenys yra tinkami. Apie kiekvieną nesėkmingą patikrą gaunate klaidos pranešimą. Klaidų pranešimuose paaiškinama, kokią informaciją reikia atnaujinti. Tiekėjo kopijos negalima įrašyti tol, kol neištaisote visų tikrinimo klaidų.

## <a name="copy-a-vendor-by-using-the-tax-exempt-number-search-feature"></a>Tiekėjo kopijavimas naudojant funkciją Neapmokestinimo kodo ieška

Tiekėjus taip pat galite kopijuoti naudodami funkciją **Neapmokestinimo kodo** ieška grupėje **Registracija**, kurią galima rasti skirtuke **Tiekėjas**, esančiame puslapio **Visi tiekėjai** veiksmų srityje. Pasirodžiusiame dialogo lange **Neapmokestinimo kodo ieška** rodomi neapmokestinimo kodai, tiekėjo ID, tiekėjo pavadinimas / vardas ir (arba) pavardė bei juridinis subjektas, kuriame naudojamas neapmokestinimo ID. Tiekėją galite kopijuoti tik tada, jei jis yra juridiniame subjekte, kuris nėra dabartinis juridinis subjektas. Pasirinkę šį kriterijų atitinkantį tiekėją, atlikite šiuos veiksmus.

1. Pasirodo parinktis **Kopijuoti tiekėją**. Pagal numatytuosius parametrus ši parinktis yra nustatyta kaip **Ne**. Norėdami tiekėją nukopijuoti į dabartinį juridinį subjektą, parinktį nustatykite kaip **Taip**.
2. Pasirinkite **Pasirinkti**. Sukuriamas naujas tiekėjas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
