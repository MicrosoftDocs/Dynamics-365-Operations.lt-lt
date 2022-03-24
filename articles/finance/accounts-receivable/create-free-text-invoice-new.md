---
title: Laisvos formos sąskaitos faktūros kūrimas
description: Šioje temoje paaiškinama, kaip kurti laisvos formos SF.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 6e9578d9b2d61f241ab5e92fc9740b88b80969f6
ms.sourcegitcommit: 411874545d7c326fc4aa877948a059371f0ccb3c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/07/2022
ms.locfileid: "8392890"
---
# <a name="create-a-free-text-invoice"></a>Laisvos formos sąskaitos faktūros kūrimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip kurti laisvos formos SF. Procedūrai atlikti naudokite demonstracinių duomenų įmonę **USMF**.

## <a name="create-a-free-text-invoice"></a>Kurti laisvos formos SF

1. Eikite į **Gautos paskyros (ar pardavimų sąskaitų knyga) \> Sąskaitos \> Visos nemokamo teksto sąskaitos**.
2. Pasirinkite **Naujas**.
3. Lauke **Kliento sąskaita** pasirinkite reikšmę.

    * Pagal numatytuosius parametrus paskyra, pasirinkta kaip kliento sąskaita, naudojama kaip SF sąskaita.
    * Jei SF neužregistruota, pirmoji apskaitos būsena yra **Vykdoma**.
    * SF numeris bus priskirtas užregistravus SF.
    * Jei naudojate bendros mokėjimų eurais erdvės (SEPA) įgaliojimus, jums pasirinkus kliento sąskaitą, tiesioginio debeto įgaliojimas įvedamas automatiškai.

4. Lauke **Aprašas** įveskite reikšmę.
5. Lauke **Pagrindinė sąskaita** nurodykite sąskaitos numerį be dimensijų. Dimensijas įvesite vėliau šioje temoje.

    Norėdami rasti savo sąskaitą, taip pat galite įvesti vieną ar kelis pagrindinės sąskaitos simbolius ir naudoti peržvalgą.

6. Pasirinkite „FastTab“ **Eilutės informacija**, kad į pagrindinę sąskaitą įtrauktumėte dimensijų.
7. Pasirinkite skirtuką **Finansinių dimensijų eilutė**.

    * Nurodytos tik pasirinktos eilutės dimensijos.
    * PVM grupė užpildoma iš kliento duomenų. Jei klientas neturi PVM grupės, naudojama PVM grupė iš pagrindinės sąskaitos.
    * Prekių PVM grupė automatiškai užpildoma pagal pagrindinę sąskaitą. Jei pagrindinė sąskaita neturi prekių PVM grupės, naudojama prekių PVM grupė, nurodyta DK PVM parametruose.

8. Pasirinktinai: lauke **Kiekis** įveskite skaičių.
9. Pasirinktinai: Lauke **Vieneto kaina** įveskite skaičių.

    Suma skaičiuojama kaip kiekis, padaugintas iš vieneto kainos. Tačiau to skaičiavimo galite nepaisyti įvesdami sumą.

10. Pasirinkite **PVM**, kad peržiūrėtumėte apskaičiuotą SF PVM.

    Galite peržiūrėti PVM sumas šiame puslapyje, arba galite pakeisti sumas skirtuke **Koregavimas**.

11. Pasirinkite **Gerai**.
12. Pasirinkite **Išlaidos**, kad į SF įtrauktumėte išlaidas.
13. Lauke **Išlaidų kodas** įveskite reikšmę.
14. Lauke **Išlaidų vertė** įveskite skaičių.
15. Uždarykite puslapį.
16. Pasirinkę **Bendrosios sumos**, galėsite peržiūrėti suvestinės SF informaciją ir bendrąsias sumas.
17. Pasirinkite **Uždaryti**.
18. Pasirinkite **Registruoti**, kad užregistruotumėte SF. Vis dar turėsite galimybę atšaukti prieš užregistruodami faktiškai.

    * Galite pakeisti SF spausdinimo laiką. Pasirinkite **Dabartinis**, kad būtų spausdinama kiekviena sąskaita faktūra ją atnaujinus. Pasirinkite **Vėliau**, norėdami spausdinti, kai atnaujinamos visos sąskaitos faktūros.
    * Norėdami keisti tai, kaip kliento kredito limitas yra tikrinamas prieš registruojant SF, pakeiskite reikšmę lauke **Kredito limito tipas**.
    * Galite pasirinkti **sustabdyti** **laisvos** formos SF registravimą, kai įvyksta klaida gautinų sumų parametrų puslapio atnaujinimų skirtuke (**Gautinų sumų sumos >> gautinų sumų parametrus).** Jei **norite** sustabdyti laisvos **formos SF registravimą pirmą** kartą nustatant klaidos parametrą, pasirinkite Taip, jei norite sustabdyti laisvos formos SF registravimą įvykstant klaidai. Jei registravimas pakete bus sustabdytas registravimo procesas, o paketo būsena bus nustatyta kaip **Klaida**. Jei ši parinktis nepasirinkta, registravimo procesas praleis SF, į problemą, kurios metu bus registruojama klaida, ir toliau registruos papildomas SF. Registruojant pakete, registravimo klaida neužkirs kelio registruoti kitų SF. Paketo būsena bus **Baigta**. Paketinių užduočių retrospektyvoje bus galima peržiūrėti išsamią registravimo proceso ataskaitą.
    * Norėdami spausdinti SF, nustatykite parinktį į **Taip**.
    * Norėdami registruoti SF, nustatykite parinktį į **Taip**. Galite spausdinti SF jos neregistruodami.

19. Pasirinkite **Gerai**.

## <a name="copy-lines"></a>Kopijuoti eilutes
Norėdami kopijuoti laisvos formos sąskaitos faktūros eilutes, pasirinkite vieną ar kelias eilutes, tada pasirinkite **Kopijuoti pasirinktas eilutes**. Galite nurodyti kopijų skaičių, taip pat galite kopijuoti pastabas ir priedus. Paskirstymus galite kopijuoti arba leisti juos sukurti iš naujo registruojant.

Nukopijavę eilutes, galite pagal poreikį redaguoti informaciją.

## <a name="create-a-free-text-invoice-from-a-template"></a>Laisvos formos sąskaitos faktūros kūrimas pagal šabloną
Laisvos formos sąskaitą faktūrą galite kurti pagal šabloną. Skirtuke **Sąskaita faktūra** pasirinkę **Nauja pagal šabloną**, galite pasirinkti naujosios laisvos formos sąskaitos faktūros šablono pavadinimą ir kliento sąskaitą. Numatytąsias reikšmes, pvz., mokėjimo sąlygas ir kliento mokėjimo būdą, galima automatiškai užpildyti iš kliento duomenų arba galima naudoti šablone įrašytas reikšmes.

Bus sukurta nauja laisvos formos SF ir galėsite redaguoti norimas reikšmes.

## <a name="resetting-the-workflow-status-for-free-text-invoices-from-unrecoverable-to-draft"></a>Laisvos formos sąskaitų faktūrų darbo eigos būsenos nustatymas iš naujo iš Nepataisoma į Juodraštis
Bus nurodyta darbo eigos egzemplioriaus, kuris buvo sustabdytas dėl neištaisomos klaidos, būsena **Neištaisoma**. Kai kliento laisvos formos SF darbo eigos būsena **yra** Nepataisoma, **galite** iš naujo nustatyti ją į Juodraštis, **darbo eigos veiksmuose pasirinkdami** Atšaukti. Tada galite redaguoti kliento laisvos formos SF. Ši funkcija galima, **jei laisvos formos SF darbo eigos būsenos nustatymas iš naujo nuo nepataisomos iki juodraščio parametro funkcijų valdymo puslapyje įjungtas** **·**.

Naudodamiesi puslapiu **Tiekėjo SF darbo eigos būsenos nustatymas iš naujo** galite iš naujo nustatyti darbo eigos būseną **Juodraštis**. Galite atidaryti šį puslapį iš laisvos **formos SF arba** bendrosios **> Užklausų formos> eigą**. Norėdami iš naujo nustatyti darbo eigos būseną į **Juodraštis**, pasirinkite **Atšaukti**. Taip pat galite iš naujo nustatyti darbo eigos **būseną** **·** **į Juodraštis, pasirinkdami veiksmą Atšaukti** laisvos formos **SF puslapyje arba Visų laisvos formos SF** puslapyje. Iš naujo nustačius darbo eigos būseną **į** Juodraštis, ją galima redaguoti laisvos **formos SF** puslapyje.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
