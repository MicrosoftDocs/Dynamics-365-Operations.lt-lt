---
title: Tiekėjų kopijavimas naudojant bendrinamas numeracijas
description: Šioje temoje paaiškinama, kaip, naudojant bendrinamas numeracijas, tiekėją nukopijuoti į kitą juridinį subjektą, bet išlaikyti tą patį tiekėjo ID.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 320487c451dd63ca861a13fc490e60d561486e0b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979218"
---
# <a name="copy-vendors-by-using-shared-number-sequences"></a>Tiekėjų kopijavimas naudojant bendrinamas numeracijas

[!include [banner](../includes/banner.md)]

Naudodami bendrinamas numeracijas, galite priskirti tiekėjų ID. Bendrinamos numeracijos taip pat leidžia tiekėjus iš vieno juridinio subjekto kopijuoti į kitą juridinį subjektą, bet naudoti tuos pačius tiekėjų ID abiejuose juridiniuose subjektuose.

## <a name="setup"></a>Sąranka

Ši funkcija suaktyvinama, kai, naudodami bendrinamą numeraciją, priskiriate tiekėjų ID. Tą pačią numeraciją turite naudoti kiekviename juridiniame subjekte, į kurį norite nukopijuoti tiekėją. Kiekvieno juridinio subjekto tiekėjo numeracija keičiama puslapyje **Mokėtinų sumų parametrai**. Pasirinkite **Mokėtinos sumos** \> **Sąranka** \> **Mokėtinų sumų parametrai**, tada – skirtuką **Numeracijos**.

Tiekėjų numeracijas taip pat galite nustatyti kiekvienai tiekėjų grupei. Šios numeracijos taip pat turi būti bendrinamos. Pirmiausia naudojama tiekėjų grupės numeracija. Jei tiekėjų grupės numeracijų nenurodyta, naudojama numeracija, nurodyta puslapyje **Mokėtinų sumų parametrai**.

Tiekėjus kopijuoti tarp juridinių subjektų taip pat galite, jei naudojate neautomatinius tiekėjų ID. Tačiau, jei tiekėją bandysite nukopijuoti į juridinį subjektą, kuriame tiekėjo ID jau yra, kopijavimo procesas nebus pradėtas.

## <a name="copy-a-vendor"></a>Tiekėjo kopijavimas

Norėdami kopijuoti tiekėją, sąrašo puslapyje **Visi tiekėjai** pasirinkite **Naujas**, kad atidarytumėte puslapį **Visi tiekėjai, naujas įrašas**. Atkreipkite dėmesį, kad naujasis tiekėjo ID nėra priskiriamas iš karto. Ankstesnėse versijose buvo kitaip. Kadangi dar nepasirinkote tiekėjų grupės, sistema negali nustatyti teisingos naudotinos numeracijos. Be to, ji negali nustatyti, ar bandote sukurti naują tiekėją, ar tiekėją kopijuoti. Todėl tiekėjo ID nepriskiriamas tol, kol puslapio apačioje nepasirenkate **Įrašyti**.

Jei kuriate naują tiekėją, galite įprastai toliau užpildyti visus laukus. Baigę ir pasirinkę **Įrašyti** matysite, kad tiekėjo ID buvo priskirtas automatiškai. O neautomatinių numeracijų atveju matysite, kad buvo panaudotas jūsų neautomatinis tiekėjo ID.

Norėdami nukopijuoti tiekėją, lauke **Vardas** įveskite vieną ar kelis simbolius, atitinkančius jūsų ieškomą tiekėją. Ieškos dialogo lange rodomas šalių, kurios gali būti jūsų ieškomas tiekėjas, sąrašas. Kai pasirenkate vieną iš šalių, dešinėje dialogo lango pusėje pasirodo papildoma tolesnė informacija.

- Skirtuke **Bendra** rodomas šalies telefono numeris ir adresas.
- Skirtuke **Vaidmenys** rodomi vaidmenys, kuriuos gali turėti pasirinkta šalis, ir juridinis subjektas, kuriame ji turi kiekvieną vaidmenį.
- Skirtuke **Mokesčių registracijos ID** rodomi šaliai priskirti mokesčių registracijos ID.

Šalį galite kopijuoti tik tada, jei ji turi tiekėjo vaidmenį ir jei tą vaidmenį ji turi juridiniame subjekte, kuris nėra dabartinis juridinis subjektas. Radę šiuos kriterijus atitinkančią šalį, atlikite šiuos veiksmus.

1. Pasirodo parinktis **Kopijuoti tiekėją**. Pagal numatytuosius parametrus ši parinktis yra nustatyta kaip **Ne**. Norėdami tiekėją nukopijuoti į dabartinį juridinį subjektą, parinktį nustatykite kaip **Taip**. 
2. Pasirodo laukas **Juridinis subjektas**. Pasirinkite juridinį subjektą, iš kurio kopijuoti tiekėją. Jei tiekėjas yra tik viename juridiniame subjekte, pagal numatytuosius parametrus laukas nustatomas kaip tas juridinis subjektas.
3. Pasirinkite **Pasirinkti**. Sukuriamas naujas tiekėjas.

## <a name="validation"></a>Tikrinimas

Kai kopijuojate tiekėją, sistema bando įrašyti naujojo tiekėjo informaciją. Vykdomos patikros, kuriomis tikrinama, ar nukopijuoti duomenys yra tinkami. Apie kiekvieną nesėkmingą patikrą gaunate klaidos pranešimą. Klaidų pranešimuose paaiškinama, kokią informaciją reikia atnaujinti. Tiekėjo kopijos negalima įrašyti tol, kol neištaisote visų tikrinimo klaidų.

## <a name="copy-a-vendor-by-using-the-tax-exempt-number-search-feature"></a>Tiekėjo kopijavimas naudojant funkciją Neapmokestinimo kodo ieška

Tiekėjus taip pat galite kopijuoti naudodami funkciją Neapmokestinimo kodo ieška, esančią puslapio **Visi tiekėjai** veiksmų srities skirtuko **Tiekėjas** grupėje **Registracija**. Pasirodžiusiame dialogo lange **Neapmokestinimo kodo ieška** rodomi neapmokestinimo kodai, tiekėjo ID, tiekėjo pavadinimas / vardas ir (arba) pavardė bei juridinis subjektas, kuriame naudojamas neapmokestinimo ID. Tiekėją galite kopijuoti tik tada, jei jis yra juridiniame subjekte, kuris nėra dabartinis juridinis subjektas. Pasirinkę šį kriterijų atitinkantį tiekėją, atlikite šiuos veiksmus.

1. Pasirodo parinktis **Kopijuoti tiekėją**. Pagal numatytuosius parametrus ši parinktis yra nustatyta kaip **Ne**. Norėdami tiekėją nukopijuoti į dabartinį juridinį subjektą, parinktį nustatykite kaip **Taip**.
2. Pasirinkite **Pasirinkti**. Sukuriamas naujas tiekėjas.
