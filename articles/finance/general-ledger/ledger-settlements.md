---
title: DK sudengimai
description: Šiame straipsnyje paaiškinama, kaip naudoti DK sudengimų puslapį DK operacijoms sudengti ir sudengti atvirkštinei tvarkai atlikti.
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
ms.openlocfilehash: 39fd6c6677565a4b1e9a9bf6f43a4c630cb5e07b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902493"
---
# <a name="ledger-settlements"></a>DK sudengimai

[!include [banner](../includes/banner.md)]

DK sudengimas yra debeto ir kredito operacijų gretinimo DK procesas. Debeto ir kredito sumų sudengimas naudojamas dk sąskaitos balansui suderinti su išsamiomis tą balansą sudaromomis operacijomis.

Sudengtos operacijos gali būti neįtrauktos į užklausas ir ataskaitas. Tokiu būdu yra lengviau analizuoti atviras DK operacijas, kurios sudaro DK sąskaitos balansą.

> [!IMPORTANT] 
> Taip pat moduliuose Mokėtinos sumos (AP) ir gautinos sumos (AR) yra SF ir mokėjimų sudengimas. Kai sudengimas vyksta AR ir AP papildomose knygose, atitinkami DK įrašai nėra sudengti automatiškai.

## <a name="ledger-settlement-features"></a>DK sudengimo priemonės
Microsoft Dynamics 365 finansų versijoje 10.0.21 **iš** **DK parametrų puslapio buvo pašalinta parinktis Įgalinti išplėstinį DK sudengimą.** Išplėstinis DK sudengimas visada įgalintas.
Finansų versijoje 10.0.25 buvo **pristatyta DK sudengimo ir uždarymo metų** pabaigos priemonės supratimo priemonė. Ši priemonė pakeičia pagrindines DK sudengimo ir DK metų pabaigos uždarymo funkcijas. Prieš įgalindami šią funkciją funkcijų valdymo darbo **srityje**, žr. Supratimas [tarp DK sudengimo ir uždarymo metų pabaigoje](awareness-between-ledger-settlement-year-end-close.md).

## <a name="set-up-ledger-settlement"></a>NUSTATYTI DK sudengimą
Turite pasirinkti pagrindines sąskaitas, kurių DK sudengimą norite atlikti. Šias pagrindines sąskaitas galima pasirinkti dviem būdais.

1. Eikite **į DK** > **nustatymo** > **DK parametrus**.
2. Skirtuke **DK sudengimų** pasirinkite sąskaitų planą, iš kurio norite pasirinkti pagrindines sąskaitas.
3. Pasirinkite pagrindines sąskaitas, kurių DK sudengimą norite atlikti. Kadangi sąskaitų plano duomenys yra visuotiniai, visos įmonės, kurioms priskirti pasirinkti sąskaitų planą, turės tas pačias pagrindines sąskaitas, pasirinktas DK sudengti.

  Arba

1. Eiti į DK **periodinių** > **užduočių DK** > **sudengimą**.
2. Pasirinkti **DK sudengimo sąskaitas**.
3. Dialogo lange pasirinkite sąskaitų diagramas ir pagrindines sąskaitas, kurių DK sudengimą norite atlikti. Šis dialogo langas yra nuoroda. Visos čia pridėtos pagrindinės sąskaitos taip pat bus parodytos DK **parametrų** puslapyje.

Norėdami bet kada pašalinti pagrindines sąskaitas iš DK sudengimo, galite naudoti tas pačias pagrindines procedūras. Pagrindinės sąskaitos pašalinimas neturi įtakos ankstesniams DK sudengimų mainams. Tačiau pagrindinė sąskaita ir operacijos daugiau nebus rodomos DK sudengimo **puslapyje**.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Sudengti operacijas
Norėdami sudengti DK operacijas, atlikite toliau nurodytus veiksmus.

1. Eiti į DK **periodinių** > **užduočių DK** > **sudengimą**.
2. Nustatyti puslapio viršuje esančius filtrus:

    - Pasirinkite datos diapazoną. Arba galite pasirinkti datos intervalo kodą, kad datų diapazonas būtų automatiškai užpildomas. Mes nerekomenduojame atlikti DK sudengimo operacijoms, kurios per keletą finansinių metų.
    - Jei reikia, pakeiskite registravimo sluoksnį. Negalima sudengti operacijų, kurios yra skirtinguose registravimo sluoksniuose.
    - Norėdami pagrindinę sąskaitą ir dimensijas rodyti atskirai, pasirinkite finansinių dimensijų rinkinį.

3. Pasirinkite **Rodyti operacijas**, kad būtų rodomos visos jūsų nustatytus filtrus atitinkančios operacijos ir nustatant ankstesniame skyriuje pateiktą sąskaitų plano sąrašą nurodytų sąskaitų sąrašas.

    - Pakeitus bet kurį filtrą arba dimensijų rinkinius, būtina dar kartą pasirinkti **Rodyti operacijas**.
    - Norėdami filtruoti operacijas atskiroje pagrindinėje sąskaitoje, naudokite dk sąskaitos **lauko** filtrą. Patariame atlikti DK sudengimų operacijų, kurios užregistruotos skirtingose pagrindinėse sąskaitose.

4. Pasirinkti eilutes sudengti. Puslapio viršuje esanti **lauko Pasirinkta** suma vertė didėja arba mažina, kad atspindėtų bendrą sumą pasirinktose eilutėse.
5. Baigę pasirinkti operacijas, pasirinkite Žymėti **pasirinktą**. Kiekvienai pažymėtai operacijai stulpelyje Pažymėta rodoma **varnelė**. Be to, reikšmė lauke Pažymėta **suma virš** tinklelio didėja arba mažėja, kad atspindėtų bendrą sumą pažymėtose eilutėse.
6. Kai pažymėto sumos lauko **vertė yra** **0 (nulis**), pasirinkite Sudengti **pažymėtas operacijas**. Pažymėtų operacijų būsena atnaujinama į **Sudengta**.

    > [!IMPORTANT]
    > Visos operacijos, kurias pažymėjote sudengti aktyviam juridiniam subjektui, bus sudengtos, net jei jos dabar nerodomas DK sudengimo puslapyje, nes pritaikėte filtrą.

## <a name="make-transactions-easier-to-find"></a>Lengvesnė operacijų paieška
DK **sudengimų** puslapyje yra galimybių, kurios padeda lengviau peržiūrėti operacijas, reikalingas sudengti.

- Naudokite pažymėtą **filtrą** operacijoms filtruoti, atsižvelgiant **į tai, ar** pažymėtas jų žymės langelis.
- Naudokite būsenos **filtrą** operacijoms filtruoti pagal jų būseną.
- Norėdami **surūšiuoti sumas pagal** absoliučią vertę, pasirinkite Rūšiuoti pagal absoliučią sumą. Tokiu būdu galite grupuoti debetus ir kreditus, kurių suma ta pati.

## <a name="reverse-a-settlement"></a>Sudengimo atšaukimas
Galite atšaukti per klaida atliktą sudengimą.

1. Norėdami parodyti jus dominaas operacijas, atlikite 1–3 [veiksmus](#settle-transactions), skyriuje Sudengti operacijas.
2. Filtre **Būsena** pasirinkite **Sudengta**.
3. Pasirinkti atšaukimo eilutes.
4. Pasirinkti Atšaukti **pažymėtas operacijas**. Visų operacijų, kurių sudengimo ID toks pats, būsena atnaujinama į **Nesudengta**.

    > [!IMPORTANT]
    > Visos operacijos, kurios turi tą patį sudengimo ID, bus atšauktos, net jei jos nepažymėtos. Pavyzdžiui, keturios eilutės pažymėtos ir sudengtos. Visos keturios eilutės turi tą patį sudengimo ID. Jei vieną iš tų keturių eilučių pažymėsite ir pasirinksite **Atšaukti pažymėtas operacijas**, visos keturios eilutės bus atšauktos.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
