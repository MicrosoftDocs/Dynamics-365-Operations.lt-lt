---
title: Klientų kopijavimas naudojant bendrinamas numeracijas
description: Šioje temoje paaiškinama, kaip, naudojant bendrinamas numeracijas, klientą nukopijuoti į kitą juridinį subjektą, bet išlaikyti tą patį kliento ID.
author: mikefalkner
manager: aolson
ms.date: 08/31/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7a1e6c6e3a995ad745522d58960e850d72c2ee57
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556277"
---
# <a name="copy-customers-by-using-shared-number-sequences"></a>Klientų kopijavimas naudojant bendrinamas numeracijas

[!include [banner](../includes/banner.md)]

Naudodami bendrinamas numeracijas, galite priskirti klientų ID. Bendrinamos numeracijos taip pat leidžia klientus iš vieno juridinio subjekto kopijuoti į kitą juridinį subjektą, bet naudoti tuos pačius klientų ID abiejuose juridiniuose subjektuose.

## <a name="setup"></a>Sąranka

Ši funkcija suaktyvinama, kai, naudodami bendrinamą numeraciją, priskiriate klientų ID. Tą pačią numeraciją turite naudoti kiekviename juridiniame subjekte, į kurį norite nukopijuoti klientą. Kiekvieno juridinio subjekto kliento numeracija keičiama puslapyje **Gautinų sumų parametrai**. Pasirinkite **Gautinos sumos** \> **Parametrai** tada – skirtuką **Numeracijos**.

Klientų numeracijas taip pat galite nustatyti kiekvienai klientų grupei. Šios numeracijos taip pat turi būti bendrinamos. Pirmiausia naudojama klientų grupės numeracija. Jei klientų grupės numeracijų nenurodyta, naudojama numeracija, nurodyta puslapyje **Gautinų sumų parametrai**.

Klientus kopijuoti tarp juridinių subjektų taip pat galite, jei naudojate neautomatinius klientų ID. Tačiau, jei klientą bandysite nukopijuoti į juridinį subjektą, kuriame kliento ID jau yra, kopijavimo procesas nebus pradėtas.

## <a name="copy-a-customer"></a>Kliento kopijavimas

Norėdami kopijuoti klientą, sąrašo puslapyje **Visi klientai** pasirinkite **Naujas**, kad atidarytumėte dialogo langą **Kliento kūrimas**. Atkreipkite dėmesį, kad naujasis kliento ID nėra priskiriamas iš karto. Ankstesnėse „Microsoft Dynamics 365 for Finance and Operations“ versijose buvo kitaip. Kadangi dar nepasirinkote klientų grupės, sistema negali nustatyti teisingos naudotinos numeracijos. Be to, ji negali nustatyti, ar bandote sukurti naują klientą, ar klientą kopijuoti. Todėl kliento ID nepriskiriamas tol, kol dialogo lango apačioje nepasirenkate **Įrašyti**.

Jei kuriate naują klientą, galite įprastai toliau užpildyti visus laukus. Baigę ir pasirinkę **Įrašyti** matysite, kad kliento ID buvo priskirtas automatiškai. O neautomatinių numeracijų atveju matysite, kad buvo panaudotas jūsų neautomatinis kliento ID.

Norėdami nukopijuoti klientą, lauke **Vardas** įveskite vieną ar kelis simbolius, atitinkančius jūsų ieškomą klientą. Ieškos dialogo lange rodomas šalių, kurios gali būti jūsų ieškomas klientas, sąrašas. Kai pasirenkate vieną iš šalių, dešinėje dialogo lango pusėje pasirodo papildoma tolesnė informacija.

- Skirtuke **Bendra** rodomas šalies telefono numeris ir adresas.
- Skirtuke **Vaidmenys** rodomi vaidmenys, kuriuos gali turėti pasirinkta šalis, ir juridinis subjektas, kuriame ji turi kiekvieną vaidmenį.
- Skirtuke **Mokesčių registracijos ID** rodomi šaliai priskirti mokesčių registracijos ID.

Šalį galite kopijuoti tik tada, jei ji turi kliento vaidmenį ir jei tą vaidmenį ji turi juridiniame subjekte, kuris nėra dabartinis juridinis subjektas. Radę šiuos kriterijus atitinkančią šalį, atlikite šiuos veiksmus.

1. Pasirodo parinktis **Kopijuoti klientą**. Pagal numatytuosius parametrus ši parinktis yra nustatyta kaip **Ne**. Norėdami klientą nukopijuoti į dabartinį juridinį subjektą, parinktį nustatykite kaip **Taip**. 
2. Pasirodo laukas **Juridinis subjektas**. Pasirinkite juridinį subjektą, iš kurio kopijuoti klientą. Jei klientas yra tik viename juridiniame subjekte, pagal numatytuosius parametrus laukas nustatomas kaip tas juridinis subjektas.
3. Pasirinkite **Pasirinkti**. Sukuriamas naujas klientas.

## <a name="validation"></a>Tikrinimas

Kai kopijuojate klientą, sistema bando įrašyti naujojo kliento informaciją. Vykdomos patikros, kuriomis tikrinama, ar nukopijuoti duomenys yra tinkami. Apie kiekvieną nesėkmingą patikrą gaunate klaidos pranešimą. Klaidų pranešimuose paaiškinama, kokią informaciją reikia atnaujinti. Kliento kopijos negalima įrašyti tol, kol neištaisote visų tikrinimo klaidų.

## <a name="copy-a-customer-by-using-tax-exempt-number-search-feature"></a>Kliento kopijavimas naudojant neapmokestinimo kodo ieškos funkciją

Klientus taip pat galite kopijuoti naudodami funkciją Neapmokestinimo kodo ieška, esančią puslapio **Visi klientai** veiksmų srities skirtuko **Klientas** grupėje **Registracija**. Pasirodžiusiame dialogo lange **Neapmokestinimo kodo ieška** rodomi neapmokestinimo kodai, kliento ID, kliento pavadinimas / vardas ir (arba) pavardė bei juridinis subjektas, kuriame naudojamas neapmokestinimo ID. Klientą galite kopijuoti tik tada, jei jis yra juridiniame subjekte, kuris nėra dabartinis juridinis subjektas. Pasirinkę šį kriterijų atitinkantį klientą, atlikite šiuos veiksmus.

1. Pasirodo parinktis **Kopijuoti klientą**. Pagal numatytuosius parametrus ši parinktis yra nustatyta kaip **Ne**. Norėdami klientą nukopijuoti į dabartinį juridinį subjektą, parinktį nustatykite kaip **Taip**. 
2. Pasirinkite **Pasirinkti**. Sukuriamas naujas klientas.
