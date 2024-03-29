---
title: Atsargų žurnalų patvirtinimo darbo eigos
description: Šiame straipsnyje aprašoma, kaip nustatyti ir naudoti įvairių tipų faktinių atsargų operacijų atsargų žurnalo patvirtinimo darbo eigas. Atsargų žurnalo darbo srautai padeda užtikrinti, kad tik patvirtinti atsargų žurnalai būtų viešinami perlaidose.
author: yufeihuang
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTableWorkflowDropDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-07-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3a97eaeae24850282c39196a61e3baa29307aa93
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334662"
---
# <a name="inventory-journal-approval-workflows"></a>Atsargų žurnalų patvirtinimo darbo eigos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti ir naudoti įvairių tipų faktinių atsargų operacijų atsargų patvirtinimo darbo eigas, pvz., gavimą ir gavimą, atsargų perkėlimą, komplektavimo specifikacijas (KS) ir faktinių atsargų suderinimą. Atsargų žurnalo darbo srautai padeda užtikrinti, kad tik patvirtinti atsargų žurnalai būtų viešinami perlaidose.

> [!NOTE]
> Atsargų žurnalo darbo srautai taikomi tik perlaidoms įrašytoms naudojant atsargų tvarkymo modulį. Jie neveikia su atsargų žurnalais, kurie yra sukurti iš atsargų valdymo modulio.

## <a name="turn-the-inventory-journal-approval-workflows-feature-on-or-off"></a>Įjungti arba išjungti atsargų žurnalo patvirtinimo darbo eigos funkciją

Jei norite naudoti šią funkciją, ją turite įjungti savo sistemoje. Kaip ir tiekimo grandinės valdymo versija 10.0.21, funkcija įjungiama pagal numatytąjį nustatymą. Kaip ir tiekimo grandinės valdymo versija 10.0.29, ši funkcija yra privaloma ir jos išjungti negalima. Jei naudojate senesnę nei 10.0.29 versiją, tada *·*[administratoriai gali įjungti arba išjungti šią funkciją ieškodami atsargų žurnalo patvirtinimo darbo eigos funkcijos funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo srityje.

## <a name="create-your-inventory-journal-approval-workflows"></a>Sukurkite savo atsargų žurnalo tvirtinimo darbo srautus

Šios funkcijos nustatymui, turite sukurti darbo srautą kiekvienam atsargų žurnalo tipui, kurį norite kontroliuoti. Kadangi skirtingi atsargų žurnalų tipai gali turėti skirtingas patvirtinimo hierarchijas ir darbo srauto žingsnius, galite konfigūruoti individualius darbo srautus kiekvienam inventoriaus žurnalo tipui.

Darbo srautai palaiko versijos kontroliavimą ir kiekvienas darbo srautas turi ID ir aktyvią versiją. Galite pasirinkite, ar aktyvuoti kiekvieną naują darbo srauto versiją nedelsiant po sukūrimo ar laikyti ją neaktyvią. Jei jums reikia kitokių darbo srautų tam pačiam žurnalo tipui, tuomet sukurkite keletą darbo srautų vienam žurnalo tipui ir tuomet priskirkite kiekvieną jų skirtingam žurnalo pavadinimu, kuris naudoja tą tipą.

Siekiant sukurti savo atsargų žurnalo tvirtinimo darbo srautus:

1. Eikite į **Atsargų valdymas \> Nustatymas\> Atsargų valdymo darbo srautai**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Pasirinkite atsargų žurnalo tipą, kuriam norite nustatyti darbo srautą:
    - **Atsargų žymės skaičiavimo žurnalas**
    - **Atsargų nuosavybės pakeitimo žurnalas**
    - **Atsargų perkėlimo žurnalas**
    - **Atsargų perkėlimo žurnalas**
    - **Atsargos skaičiavimo žurnalas**
    - **Atsargos KS žurnalas**
    - **Atsargų koregavimo žurnalas**

    ![Darbo srauto teksto laukelio sukūrimas.](media/journal-workflow-create-workflow.png "Darbo srauto teksto laukelio sukūrimas")

1. Darbo srauto redagavimo programa įsijungia jūsų mašinoje. (Jūsų taip pat gali būti prašoma patvirtinti šį veiksmą.). Naudokite jį suplanuoti jūsų darbo srautą, kaip norite. Dėl informacijos apie tai, kaip naudoti darbo srauto redaktorių, žr. [Darbo srauto sistemos peržiūra](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).
1. Išsaugojus ir uždarius darbo srauto redaktoriaus programą, turite pasirinkti, ar aktyvuoti šį darbo srauto versiją ar laikysite ją neaktyvią.

> [!NOTE]
> Darbo srautai pateikia versijos valdymą, kuris reiškia, kad jūs galite peržiūrėti versijų sąrašą, kurį sukūrėte ir pasirinkote, priklausomai nuo to, kuris veikia. Tam, kad peržiūrėtumėte esamas versijas ir pasirinktumėte, kurią aktyvuoti, pasirinkite darbo srautą sąraše **Atsargų valdymo darbo srautų** puslapis. Veiksmų juostoje atidarykite **Darbo srauto** skirtuką ir pasirinkite **Versijos**. Tik viena versija gali būti įjungta vienu metu kiekvienam darbo srauto ID.

## <a name="assign-approval-workflows-to-inventory-journal-names"></a>Priskirkite patvirtinimo darbo srautus prie atsargų žurnalo pavadinimų

Kitas žingsnis yra priskirti atsargų žurnalo darbo srautus prie kiekvieno atsargų žurnalo pavadinimo. Kiekvienam atsargų žurnalo tipui, galite nustatyti keletą inventorių žurnalų pavadinimų.

Siekiant susieti inventoriaus žurnalų darbo srautus su inventoriaus žurnalo pavadinimu:

1. Eikite į **Atsargų valdymas \> Nustatymas \> Žurnalo pavadinimai \> Atsargos**.
1. Pasirinkite žurnalo pavadinimą iš sąrašo stulpelio tam, kad atidarytumėte jo nustatymų puslapį.
1. **Bendras** „FastTab“, nustatykite **Darbo srauto patvirtinimo** parinktį į **Taip**. Jei esate skatinamas patvirtinti veiksmą, pasirinkite **Taip**.

    ![Priskirti darbo srautą prie žurnalo pavadinimo.](media/journal-workflow-journal-name.png "Priskirti darbo srautą prie žurnalo pavadinimo")

1. Atidarykite **Darbo srauto** išplečiamąjį sąrašą ir pasirinkite tinkamą darbo srautą. Sąrašas rodo visus aktyvius darbo srautus, kuriuos sukūrėte naudodami darbo srauto redagavimo programą.

## <a name="create-an-inventory-journal-and-send-it-for-approval"></a>Sukurkite atsargų žurnalą ir nusiųskite patvirtinimą

Po to, kai susiesite atsargų žurnalo pavadinimą su jį atitinkančiu atsargų žurnalo patvirtinimo darbo srautu, jums reikės sukurti naują atsargų žurnalą, kuris naudos pavadinimą ir tuomet nusiųs šiuos žurnalus patvirtinimui naudojant darbo srautą. Jūs negalėsite publikuoti inventoriaus žurnalo tol, kol jis nebus patvirtintas sukonfigūruotame darbo sraute.

1. Naršymo juostoje, išplėskite **Atsargų valdymas \> Žurnalo įrašai \> Elementai** ir tuomet pasirinkite atsargų žurnalo tipą.
1. Pasirinkite **Naujas**, kad sukurtumėte naują savo pasirinkto tipo žurnalą.
1. **Atsargų žurnalo sukūrimo** teksto langas atsidaro. Užpildykite formas, kaip būtina ir tuomet pasirinkite **Gerai** žurnalo įrašymui.
1. Pabaikite žurnalą, kaip būtina.
1. Kai kuriate ar atidarote atsargų žurnalą su patvirtinimo darbo srautu susietu su juo,**Darbo srauto** mygtukas bus įjungtas veiksmų juostoje. Kai jūs esate pasiruošę pateikti žurnalą patvirtinimui, pasirinkite **Darbo srauto** mygtuką tam, kad atidarytumėte iškrentantį teksto laukelį ir tuomet pasirinkite **Pateikti**. Patvirtinimo užklausa tuomet nukreipiama atitinkamam patvirtintojui, kuris bus perspėjamas naudoti pranešimo metodą, sukonfigūruotą darbo srautui.

    ![Pateikti žurnalą tvirtinti.](media/journal-workflow-inventory-journal.png "Pateikti žurnalą tvirtinti")

Tam, kad atšauktumėte patvirtinimo prašymą, atidarykite atitinkamą žurnalą, pasirinkite **Darbo srauto** mygtuką ir tuomet pasirinkite **Atšaukti**. Jis atstatys darbo srautą.

Kai jūsų žurnalas yra patvirtintas, galėsite jį publikuoti. Žurnalo publikavimui, pasirinkite **Publikuoti** veiksmų juostoje. Jei **Publikuoti** mygtukas nėra aktyvus, žurnalas dar nėra patvirtintas.

## <a name="respond-to-an-inventory-journal-approval-request"></a>Atsakykite į atsargų žurnalo patvirtinimo užklausą

Jei esate tvirtintojas, turėtumėte gauti žinutę kas kartą, kai jūsų tvirtinimas yra reikalingas (kaip sukonfigūruota atitinkamame darbo sraute). Tuomet galite patvirtinti ar atmesti žurnalo patvirtinimo užklausą atlikdami šiuos veiksmus:

1. Naršymo juostoje, išplėskite **Atsargų valdymas \> Žurnalo įrašai \> Elementai** ir tuomet pasirinkite atsargų žurnalo tipą.
1. Atidarykite atitinkamą žurnalą jo peržiūrai.
1. Pasirinkite **Darbo srauto** mygtuką veiksmų juostoje, kurią norite atidaryti iškrentančiame teksto lauke. Pasirinkite vieną iš toliau pateiktų:
    - **Patvirtinti** - Prašymo patvirtinimui.
    - **Atmesti** - Užklausos atmetimui.
    - **Daugiau \> Užklausos keitimas** - Žinutės nusiuntimui į užklausą, prašantį juos pakeisti kai ką konkretaus ir tuomet pateikti dar kartą.
    - **Daugiau \> Perleisti** - Patvirtinimo perleidimas kitam naudotojui.
    - **Daugiau \> Atšaukti** - Prašymo patvirtinimo atšaukimas (atšaukia darbo srautą).
    - **Daugiau \> Darbo srauto istorija** - Peržiūrėti šio patvirtinimo darbo srauto istoriją iki dabar.

## <a name="review-the-approval-history"></a>Peržiūrėti patvirtinimo istoriją

Taip pat, kaip ir su kitais darbo srautų tipais, galite naudoti **Darbo srauto istorijos** puslapį tam, kad peržiūrėtumėte darbo srauto istorijos patvirtinimą bet kuriam žurnalui.

Tam, kad peržiūrėtumėte žurnalo darbo srauto istoriją:

1. Naršymo juostoje, išplėskite **Atsargų valdymas \> Žurnalo įrašai \> Elementai** ir tuomet pasirinkite atsargų žurnalo tipą.
1. Atidarykite atitinkamą žurnalą.
1. Pasirinkite **Darbo srauto** mygtuką veiksmų juostoje, kurią norite atidaryti iškrentančiame teksto lauke. Pasirinkite **Darbo srauto**. - Norėdami gauti daugiau informacijos, žr. [Peržiūrėti darbo srauto istoriją](../../fin-ops-core/fin-ops/organization-administration/tasks/view-workflow-history.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]