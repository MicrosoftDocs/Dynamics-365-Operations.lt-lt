---
title: Produkto konfigūravimo pagal apribojimus atributais pagrįstos pardavimo kainos
description: Šioje temoje aprašoma, kaip sukurti pardavimo kainos modelius, kurių pardavimo kainos pagrįstos komponentais ir atributais, o ne faktine komplektavimo specifikacija ir maršrutu.
author: sorenva
manager: tfehr
ms.date: 10/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2020-08-17
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 65ab96c71fa44d6acad0bcb5cd7a65321109b93d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221972"
---
# <a name="attribute-based-sales-prices-for-constraint-based-product-configuration"></a>Produkto konfigūravimo pagal apribojimus atributais pagrįstos pardavimo kainos

Šioje temoje aprašoma, kaip sukurti pardavimo kainos modelius, kurių pardavimo kainos pagrįstos komponentais ir atributais, o ne faktine komplektavimo specifikacija ir maršrutu. Galite sukurti kelis kiekvieno produkto konfigūracijos modelio pardavimo kainos modelius.

## <a name="set-relevant-product-information-management-parameters"></a>Tinkamų produkto informacijos valdymo parametrų nustatymas

Prieš pradėdami kurti kainos modelius, turite nurodyti numatytąją valiutą, naudojamą kuriant jūsų pardavimo kainos modelius. Taip pat galite pasirinkti, ar pridėti „Microsoft Excel” failą su visų užsakymo ar pasiūlymo eilučių kainos paskirstymu. Kainos paskirstymas leis bendrinti informaciją su klientais apie tai, kaip pasiekėte tam tikrą sukonfigūruoto produkto pardavimo kainą.

Norėdami nustatyti numatytąją valiutą, atlikite toliau pateiktus veiksmus.

1. Eikite į  **Produkto informacijos valdymas \> Nustatymai \> Produkto informacijos valdymo parametrai**.
1. Atidarykite skirtuką **Produktų konfigūravimo pagal apribojimus modeliai**.
1. Atidarykite išplečiamąjį sąrašą **Numatytoji valiuta** ir pasirinkite jūsų valiutą.

    ![Numatytosios produkto konfigūravimo pagal apribojimus valiutos nustatymas](media/prod-config-currency.png "Numatytosios produkto konfigūravimo pagal apribojimus valiutos nustatymas")

1. Jei norite pridėti „Excel” failą su visų užsakymo ar pasiūlymo eilučių kainos paskirstymu, dalyje **Kainos modelis** nustatykite **Pridėti** į *Taip*.

## <a name="build-your-sales-price-models"></a><a name="build-price-model"></a>Jūsų pardavimo kainos modelių kūrimas

Norėdami sukurti pardavimo kainos modelį, atlikite toliau pateiktus veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Produkto konfigūracijos modeliai**.
1. Pasirinkite paskirties produkto konfigūracijos modelį.
1. Veiksmų srityje atidarykite skirtuką **Modelis** ir grupėje **Nustatymas** pasirinkite **Kainos modeliai**.
1. Atidaromas puslapis **Kainos modeliai**.
1. Pasirinkite kainos modelį arba įtraukite naują į tinklelį.
1. Pasirinkite **Redaguoti**, kad būtų atidarytas pasirinkto modelio redagavimo puslapis, kuriame pateikiamos toliau nurodytos funkcijos.
    - Formos antraštė nurodo numatytąją valiutą ir leidžia įtraukti naujas valiutas į jūsų kainų nustatymą.
    - Kairiojoje srityje nurodyti visi produkto modelio komponentai ir vartotojo reikalavimai. Kiekviename produkto modelių medžio mazge gali būti viena bazinės kainos išraiška ir pasirinktinis išraiškos taisyklių skaičius. Išraiškos taisyklę sudaro sąlyga bei išraiška ir kiekvienoje išraiškos taisyklėje yra produkto parinktis, padedanti valdyti produkto kainą.
    - Kurdami jūsų sąlygas ir išraiškas, galite pasiekti tuos pačius operatorius, kurie pasiekiami vykdant skaičiavimus produkto modelyje. Išraiškos rengyklė taip pat palaiko ir sąlygas, ir išraiškas.
1. Pasirinkite mazgą kairiajame stulpelyje, tada naudokite ankstesniame veiksme aprašytas funkcijas, norėdami nustatyti mazgo kainodaros taisykles (taip pat žr. pavyzdį, pateiktą po šia procedūra). Pakartokite šį žingsnį su kiekvienu mazgu, jei reikia.

Toliau pateiktame pavyzdyje pateikta statinio skaičiaus 899,95 EUR bazinė kaina, kurią galima modifikuoti naudojant vieną ar daugiau toliau pateiktų penkių išraiškos taisyklių, atsižvelgiant į kliento pasirinktą konfigūraciją.

- Už baltos spintelės apdailą atimkite 59,95 EUR.
- Už kampų apsaugą pridėkite 35,95 EUR.
- Už metalines priekines groteles pridėkite 89,95 EUR.
- Už raudonmedžio spintelės apdailą pridėkite 119,95 EUR.
- Pridėkite 12,95 EUR už kiekvieną garsiakalbių aukščio vienetą.

![Kainos modelio pavyzdys](media/prod-config-rules-example.png "Kainos modelio pavyzdys")

## <a name="add-support-for-multiple-currencies"></a>Kelių valiutų palaikymo įtraukimas

Kai konfigūruojamas produktas parduodamas, sistema patikrina, ar kainos tiesiogiai nustatytos kliento valiuta. Jei taip, naudojamos tiesioginės vertės. Jei ne, sistema naudoja valiutos kursus, nustatytus pardavimo įmonei, kad numatytosios valiutos vertė būtų konvertuota į kliento valiutą.

Norėdami įtraukti tiesiogines kainas papildoma valiuta, atlikite toliau pateiktus veiksmus.

1. Atidarykite jūsų kainos modelio redagavimo puslapį, kaip nurodyta [Jūsų pardavimo kainos modelių kūrimas](#build-price-model).
1. Pasirinkite mygtuką **Įtraukti**, esantį kainos modelio antraštėje, norėdami atidaryti išplečiamąjį dialogo langą **Valiutos**, kuriame išvardytos galimos valiutos.
1. Pasirinkite valiutą, kurią norite įtraukti į išplečiamąjį dialogo langą **Valiutos**, tada pasirinkite **Gerai**.
1. Išplečiamajame sąraše **Dabartinė valiuta** dabar yra valiuta, kurią ką tik įtraukėte, ir visos kitos valiutos, kurios galėjo būti įtrauktos anksčiau. Pasirinkite jūsų naują valiutą ir atkreipkite dėmesį, kad tinklelis, esantis dalyje **Išraiškos taisyklės**, dabar apima du toliau pateiktus išraiškos laukus.
    - **Išraiška** – nurodo kainos valiuta, kuri šiuo metu pasirinkta dalyje **Dabartinė valiuta**, gavimo išraišką (arba pastovią vertę).
    - **Numatytosios išraiškos** – nurodo kainos numatytąja valiuta (nurodyta lauke **Numatytoji valiuta**) gavimo išraišką (arba pastovią vertę).

    > [!NOTE]
    > Išraiškos taisyklių laukas **Sąlyga** „priklauso” numatytajai valiutai, o tai reiškia, kad negalima modifikuoti kitų valiutų sąlygos. Taip pat negalima įtraukti naujų išraiškos taisyklių, kai valiuta, kuri nėra numatytoji valiuta, pasirinkta kaip **Numatytoji valiuta**.
1. Jei reikia, redaguokite stulpelyje **Išraiška** esančias vertes, susijusias su dabartine valiuta.

Toliau pateiktame pavyzdyje _EUR_ yra numatytoji valiuta, o _USD_ buvo įtraukta kaip papildoma valiuta.

![Modelio su keliomis valiutomis pavyzdys](media/prod-config-rules-currency-example.png "Modelio su keliomis valiutomis pavyzdys")

> [!NOTE]
> Negalite įtraukti išraiškos taisyklių, kurios yra unikalios ne numatytajai valiutai. Norėdami sukurti išraiškos taisykles, kurios būtų taikomos tik kitai valiutai nei numatytajai valiutai, nustatykite numatytąją valiutos kainos išraišką į nulį. Tada nustatykite reikiamą ne numatytosios valiutos išraišką.

## <a name="test-your-price-model"></a>Jūsų kainos modelio tikrinimas

Norėdami patikrinti, kaip pardavimo kainos veikia konfigūracijos seanso metu, atidarykite jūsų kainos modelio redagavimo puslapį, kaip aprašyta [Jūsų pardavimo kainos modelių kūrimas](#build-price-model), tada veiksmų srityje pasirinkite **Tikrinti**. Atidaromas dialogo langas **Tikrinti produkto modelį**, kuriame galite atlikti toliau pateiktus veiksmus.

- Naudokite čia siūlomus konfigūracijos parametrus, norėdami pasirinkti produkto parinktis ir pežiūrėti, kaip jos paveikia vertę, esančią dalyje **Kaina ir siuntimo data**.
- Pasirinkite **Rodyti kainos paskirstymą**, norėdami atsisiųsti „Excel” dokumentą, kuriame pateikta išsami informacija apie tai, kaip kaina buvo apskaičiuota.

![Jūsų produkto modelio tikrinimas](media/prod-config-test.png "Jūsų produkto modelio tikrinimas")

Atsisiųstoje skaičiuoklėje rodoma absoliučioji vertė ir kiekvieno aktyvaus kainos elemento įnašas procentais. Jei nustatėte kainos modelio parinktį **Pridėti** puslapyje **Produkto informacijos valdymo parametrai**, šis „Excel” lapas bus pridėtas prie užsakymo arba pasiūlymo eilutės.

![„Excel” skaičiuoklė, nurodanti kainos paskirstymą](media/prod-config-excel-example.png "„Excel” skaičiuoklė, nurodanti kainos paskirstymą")

## <a name="set-up-selection-criteria-for-price-models"></a>Kainos modelių pasirinkimo kriterijų nustatymas

Kai jūsų kainos modeliai sukurti, turite nustatyti bent vieną pasirinkimo kriterijų, pagal kurį konfigūruojant pasiūlymą ar užsakymą būtų pateiktas kainos modelis. Tai atliksite nustatydami vieną ar daugiau užklausų. Kartu su atitinkančiais pardavimo kainų modeliais užklausos suteikia daug lankstumo taikant konkrečių klientų, regionų, laikotarpių ir kitų kriterijų pardavimo kainas.

Norėdami nustatyti kainos modelių pasirinkimo kriterijus, atlikite toliau nurodytus veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Produkto konfigūracijos modeliai**.
1. Pasirinkite paskirties produkto konfigūracijos modelį.
1. Veiksmų srityje atidarykite skirtuką **Modelis** ir grupėje **Nustatymas** pasirinkite **Kainos modelio kriterijai**. Atidaromas puslapis **Kainos modelio kriterijai**.
1. Jei reikiamos užklausos eilutės dar nėra, veiksmų srityje pasirinkite **Naujas**, norėdami įtraukti naują eilutę į tinklelį ir nustatyti toliau pateiktus jos parametrus.
    - **Pavadinimas** – įveskite šios eilutės pavadinimą.
    - **Aprašas** – trumpai aprašykite užklausą ir kam ji skirta.
    - **Kainos modelis** – pasirinkite [kainos modelį](#build-price-model) (iš dabartinio konfigūracijos modelio), kurį užklausa taikys, kai ją suaktyvins.
    - **Užsakymo tipas** – pasirinkite užsakymo tipą, kuriame bus taikoma užklausa.
    - **Galioja nuo** – nurodykite pirmąją dieną, nuo kurios bus taikoma užklausa.
    - **Galioja iki** – nurodykite paskutinę dieną, iki kurios bus taikoma užklausa.

    ![Kainos modelio kriterijus](media/prod-config-price-model-criteria.png "Kainos modelio kriterijus")

1. Pasirinkite norimos nustatyti užklausos eilutę ir **veiksmų srityje** pasirinkite **Redaguoti**. Atidaromas užklausos dizaino įrankio dialogo langas. Šis įrankis veikia kaip dauguma užklausos dizaino įrankių „Supply Chain Management”. Naudokite jį, norėdami nustatyti sąlygas, kuriomis turėtų būti taikomas pasirinktos eilutės kainos modelis.

1. Pakartokite 4-5 veiksmus kiekvienai reikiamai užklausai.
    > [!TIP]
    > Galite sutaupyti laiko nukopijuodami esamą eilutę, panašią į naują, kurią reikia įtraukti. Norėdami tai atlikti, pasirinkite paskirties eilutę ir tada veiksmų srityje pasirinkite **Dubliuoti**.

1. Kai baigsite jūsų kriterijų nustatymą, suskirstykite juos tinkama tvarka sąraše **Kainos modelio kriterijai**. Norėdami perkelti eilutę, pasirinkite eilutę ir tada veiksmų srityje pasirinkite **Aukštyn** arba **Žemyn**.

    > [!IMPORTANT]
    > Konfigūracijos metu sistema pradeda ieškoti nuo sąrašo viršaus ir naudoja pirmąją užklausą, kuri sutampa su pasiūlymo ar užsakymo eilutės duomenimis. Todėl į sąrašo pradžią turite perkelti konkrečiausias užklausas. Jei į sąrašo pradžią perkelsite bendrąją užklausą, ji bus naudojama, net jei žemiau sąraše yra užklausa, skirta tiksliam ar potencialiam konfigūracijos klientui.

## <a name="set-attribute-based-sales-prices-for-the-product-model-version"></a>Produkto modelio versijos atributais pagrįstų pardavimo kainų nustatymas

Paskutinis veiksmas yra produkto modelio versijos atributais pagrįstų pardavimo kainų nurodymas. Norėdami tai atlikti, atlikite toliau pateiktus veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Produkto konfigūracijos modeliai**.
1. Pasirinkite paskirties produkto konfigūracijos modelį.
1. Veiksmų srityje atidarykite skirtuką **Modelis** ir grupėje **Produkto modelio informacija** pasirinkite **Versijos**.
1. Atidaromas puslapis **Versijos**. Įsitikinkite, kad **Kainodaros metodas** nustatytas į **Pagrįstas atributais**.
    ![Kainodaros metodo nustatymas į pagrįstą atributais](media/prod-config-versions.png "Kainodaros metodo nustatymas į pagrįstą atributais")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]