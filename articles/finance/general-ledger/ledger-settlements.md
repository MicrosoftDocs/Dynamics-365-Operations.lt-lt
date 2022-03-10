---
title: DK sudengimai
description: Šioje temoje paaiškinama, kaip, naudojantis DK sudengimų puslapiu, sudengti DK operacijas ir atšaukti sudengimus.
author: kweekley
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: e98b012210338e7f18cb874eefbc8a023aa4428b
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075329"
---
# <a name="ledger-settlements"></a>DK sudengimai

[!include [banner](../includes/banner.md)]

Didžiosios knygos atsiskaitymas – tai debeto ir kredito operacijų derinimo procesas didžiojoje knygoje. Debeto ir kredito sumų apmokėjimas naudojamas DK sąskaitos likučiui suderinti su išsamiomis tą likutį sudarančiomis operacijomis.

Apmokėtos operacijos gali būti neįtrauktos į užklausas ir ataskaitas. Tokiu būdu lengviau analizuoti atidarytas didžiosios knygos operacijas, kurios sudaro didžiosios knygos sąskaitos likutį.

> [!IMPORTANT] 
> Moduliai mokėtinos sumos (AP) ir gautinos sumos (AR) taip pat turi sąskaitų faktūrų apmokėjimą ir mokėjimus. Kai atsiskaitoma AR ir AP antrinėse knygose, atitinkami knygos įrašai nėra automatiškai apmokami.

## <a name="ledger-settlement-features"></a>Didžiosios knygos atsiskaitymo ypatumai
„Microsoft“.Dynamics 365 Finance versija 10.0.21, **Įgalinti išplėstinį DK atsiskaitymą** parinktis buvo pašalinta iš **Didžiosios knygos parametrai** puslapį. Išplėstinis DK atsiskaitymas dabar visada įjungtas.
„Finance“ 10.0.25 versijoje **Supratimas tarp atsiskaitymo knygoje ir uždarymo metų pabaigoje** buvo pristatyta funkcija. Ši funkcija pakeičia pagrindines ir Didžiosios knygos atsiskaitymo, ir Didžiosios knygos metų pabaigos uždarymo funkcijas. Prieš įjungdami šią funkciją **Funkcijų valdymas** darbo vieta, žr.[Supratimas tarp atsiskaitymo knygoje ir uždarymo metų pabaigoje](awareness-between-ledger-settlement-year-end-close.md).

## <a name="set-up-ledger-settlement"></a>Nustatyti DK atsiskaitymą
Turite pasirinkti pagrindines sąskaitas, už kurias norite atlikti atsiskaitymą. Yra du būdai, kaip pasirinkti šias pagrindines paskyras.

1. Eiti į **Didžioji knyga** > **Didžiosios knygos nustatymas** > **Didžiosios knygos parametrai**.
2. Ant **Didžiosios knygos atsiskaitymai** skirtuke pasirinkite sąskaitų planus, iš kurių norite pasirinkti pagrindines sąskaitas.
3. Pasirinkite pagrindines sąskaitas, už kurias atsiskaitysite knygoje. Kadangi sąskaitų planai yra globalūs, visos įmonės, kurioms priskirti pasirinkti sąskaitų planai, turės tas pačias pagrindines sąskaitas, kurios bus parinktos atsiskaitymui knygoje.

  Arba

1. Eiti į **Didžioji knyga** > **Periodinės užduotys** > **Didžiosios knygos atsiskaitymai**.
2. Pasirinkite **Didžiosios knygos atsiskaitymo sąskaitos**.
3. Dialogo lange pasirinkite sąskaitų planus ir pagrindines sąskaitas, už kurias atsiskaitysite knygoje. Šis dialogo langas yra nuoroda. Visos pagrindinės paskyros, kurias čia pridėsite, taip pat atsispindės **Didžiosios knygos parametrai** puslapį.

Galite naudoti tas pačias pagrindines procedūras, kad bet kuriuo metu pašalintumėte pagrindines sąskaitas iš atsiskaitymo iš knygos. Pagrindinės sąskaitos pašalinimas neturi įtakos ankstesniems knygos atsiskaitymams. Tačiau pagrindinė sąskaita ir operacijos nebebus rodomos **Didžiosios knygos atsiskaitymas** puslapį.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Sudengti operacijas
Norėdami sudengti DK operacijas, atlikite toliau nurodytus veiksmus.

1. Eiti į **Didžioji knyga** > **Periodinės užduotys** > **Didžiosios knygos atsiskaitymai**.
2. Nustatyti puslapio viršuje esančius filtrus:

    - Pasirinkite datos diapazoną. Arba pasirinkite datos intervalo kodą, kad automatiškai užpildytumėte dienų seką. Nerekomenduojame atlikti atsiskaitymų knygoje už operacijas, kurios apima fiskalinius metus.
    - Jei reikia, pakeiskite paskelbimo sluoksnį. Negalite apmokėti operacijų, kurios yra skirtinguose registravimo sluoksniuose.
    - Norėdami atskirai rodyti pagrindinę sąskaitą ir dimensijas, pasirinkite finansinių dimensijų rinkinį.

3. Pasirinkite **Rodyti operacijas**, kad būtų rodomos visos jūsų nustatytus filtrus atitinkančios operacijos ir nustatant ankstesniame skyriuje pateiktą sąskaitų plano sąrašą nurodytų sąskaitų sąrašas.

    - Pakeitus bet kurį filtrą arba dimensijų rinkinius, būtina dar kartą pasirinkti **Rodyti operacijas**.
    - Norėdami filtruoti operacijas į atskirą pagrindinę sąskaitą, naudokite filtrą **Didžiosios knygos sąskaita** lauke. Nerekomenduojame atsiskaityti knygoje už operacijas, kurios registruojamos į skirtingas pagrindines sąskaitas.

4. Pasirinkite eilutes atsiskaitymui. Vertė **Pasirinkta suma** puslapio viršuje esantis laukas didėja arba mažėja, kad atspindėtų bendrą sumą pasirinktose eilutėse.
5. Kai baigsite pasirinkti operacijas, pasirinkite **Pažymėti pasirinktą**. Kiekvienai pasirinktai operacijai rodoma varnelė **Pažymėtas** stulpelyje. Be to, vertė **Pažymėta suma** virš tinklelio esantis laukas didėja arba mažėja, kad atspindėtų bendrą sumą pažymėtose eilutėse.
6. Kai reikšmė **Pažymėta suma** laukas yra **0** (nulis), pasirinkite **Atsiskaityti už pažymėtas operacijas**. Pažymėtų operacijų būsena atnaujinama į **Sudengta**.

    > [!IMPORTANT]
    > Visos operacijos, kurias pažymėjote kaip atsiskaityti už aktyvų juridinį asmenį, bus apmokėtos, net jei jos šiuo metu nerodomos Didžiosios knygos atsiskaitymo puslapyje, nes pritaikėte filtrą.

## <a name="make-transactions-easier-to-find"></a>Lengvesnė operacijų paieška
The **Didžiosios knygos atsiskaitymai** puslapyje yra galimybių, kurios palengvina atsiskaitymui reikalingų operacijų peržiūrą.

- Naudoti **Pažymėtas** filtras, kad filtruotumėte operacijas pagal tai, ar **Pažymėtas** jiems pažymėtas žymės langelis.
- Naudoti **Būsena** filtrą, kad filtruotumėte operacijas pagal jų būseną.
- Pasirinkite **Rūšiuoti pagal absoliučią sumą** rūšiuoti sumas pagal absoliučią vertę. Tokiu būdu galite sugrupuoti debetus ir kreditus, kurių suma yra tokia pati.

## <a name="reverse-a-settlement"></a>Sudengimo atšaukimas
Galite atšaukti per klaida atliktą sudengimą.

1. Atlikite 1–3 veiksmus [Atlikti sandorius](#settle-transactions) skyriuje, kad būtų rodomos jus dominančios operacijos.
2. Filtre **Būsena** pasirinkite **Sudengta**.
3. Pasirinkite eilutes, kurias norite pakeisti.
4. Pasirinkite **Atvirkščiai pažymėti sandoriai**. Visų operacijų, turinčių tą patį atsiskaitymo ID, būsena atnaujinama į **Neišspręstas**.

    > [!IMPORTANT]
    > Visos operacijos, turinčios tą patį atsiskaitymo ID, bus anuliuotos, net jei jos nepažymėtos. Pavyzdžiui, buvo pažymėtos ir sutvarkytos keturios eilutės. Visos keturios eilutės turi tą patį atsiskaitymo ID. Jei pažymėsite vieną iš šių keturių eilučių ir pasirinksite **Atvirkščiai pažymėti sandoriai**, visos keturios eilutės bus apverstos.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
