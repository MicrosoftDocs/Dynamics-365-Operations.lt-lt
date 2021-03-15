---
title: Priežiūros planai
description: Šioje temoje aptariami priežiūros planai skiltyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9ec4929e9ea608318b83a2ae6033c4b25855f4dd
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/28/2021
ms.locfileid: "5077555"
---
# <a name="maintenance-plans"></a>Priežiūros planai

[!include [banner](../../includes/banner.md)]

Priežiūros planas – tai iš anksto suplanuotos prevencinės priežiūros užduoties vykdymas turtui. Priežiūros planai gali būti susiję su turtu, turto tipais, funkcinėmis vietomis arba funkcinių vietų tipais, tačiau pirmiausiai turite sukurti priežiūros planus, kurie bus naudojami jūsų įmonėje.

Priežiūros planas gali turėti daugiau nei vieną priežiūros plano eilutę. Priežiūros plano eilutėje yra nurodyti priežiūros plano tipas ir intervalas. Galimi du priežiūros plano eilutės tipai:

- Laikas
- Skaitiklis

Priežiūros plano eilučių tipas Laikas naudojamas periodiškai planuojamai priežiūrai, kuri vykdoma nustatytu laiko intervalu. Priežiūros plano eilučių tipas Skaitiklis naudojamas suplanuotai priežiūrai ar atsakomajai priežiūrai, paremtai turto skaitiklio registravimais. Priežiūros planas gali apimti kelias abiejų tipų priežiūros plano eilutes.

>[!NOTE]
>Jei turto skaitiklio tipui nėra registruotų skaitiklio reikšmių, priežiūros plano eilutės praleidžiamos.

Pirmiausia turite sukurti priežiūros planus, kurių reikia prevencinėms priežiūros užduotims atlikti, ir pasirinkti turto tipus, turtą, funkcinės vietos tipus ir funkcines vietas, susijusias su kiekvienu priežiūros planu. Po to, jei reikia, taip pat galite pridėti priežiūros planus prie turto arba funkcinės vietos, o tai pasiekiama tokiu būdu: **Visas turtas** \> pasirinkite turtą \> **Turto priežiūros planai** „FastTab” arba **Visos funkcinės vietos** \> pasirinkti funkcinę vietą \> **Priežiūros planai** „FastTab”.

Jei pridėsite priežiūros planą prie turto tipų arba funkcinės vietos tipų, tokiu atveju, kuriant naują turtą ar funkcines vietas, nurodžius tuos turto arba funkcinės vietos tipus, priežiūros plane automatiškai bus užpildomi turtas arba funkcinė vieta. Ryšio su priežiūros planu pradžios data bus dabartinė data, todėl gali reikėti ją koreguoti.

## <a name="set-up-maintenance-plans"></a>Nustatyti priežiūros planus

Šiame skyriuje aprašoma, kaip nustatyti priežiūros plano eilutes ir pateikiami pavyzdžiai, kaip galima jomis naudotis.

1. Eikite į **Turto valdymas \> Konfigūracija \> Prevencinė priežiūra \> Priežiūros planai**.

1. Pasirinkite **Nauja** kurti naujai sekai.

1. Lauke **Priežiūros seka** įterpkite ID, o lauke **Pavadinimas** – pavadinimą.

1. Lauke **Plano data** įterpkite pradžios datą, nuo kurios pradedamas kurti priežiūros planas. Atkreipkite dėmesį, kad pagal laiką pagrįstose priežiūros plano eilutėse gali būti kitos plano datos.

1. Norėdami suaktyvinti priežiūros planą, pasirinkite Taip perjungiklyje **Aktyvus**.

    >[!NOTE]
    >Jei išjungsite priežiūros planą, priežiūros grafike nebus kuriami jokie grafiko pranešimai, kai vykdysite suplanuotą priežiūros plano užduotį.

1. Laukai **Leistino nuokrypio dienos prieš** ir **Leistino nuokrypio dienos po** siejasi su priežiūros plano eilutėmis, kuriose pažymėtas **Sulaikyti persidengiančias priežiūros užduotis** žymės langelis (žiūrėkite 17 veiksmą). Laukai Leistinas nuokrypis yra naudojami ilginti intervalą dienomis, kuriame, jei keli priežiūros planai persidengia, planuojant priežiūros planą didžiausios apimties užduotis sukuriama priežiūros grafiko eilutėje, o dažniau vykdomos persidengiančios užduotys praleidžiamos kuriant priežiūros planą. Įveskite dienų skaičių į lauką **Leistino nuokrypio dienos prieš**, pvz., „2“.

1. Jei įterpėte reikšmę **Leistinos nuokrypio dienos prieš**, taip pat įveskite dienų skaičių į lauką **Leistino nuokrypio dienos po**, pvz., „2“.

    >[!NOTE]
    >Pavyzdys, aprašytas šiame ir ankstesniame veiksme, reiškia, kad jei kelios priežiūros plano eilutės persidengia ir pasirenkama **Sulaikyti persidengiančias priežiūros užduotis** vienai ar daugiau eilutei, intervalas, kai priežiūros grafiko eilutės yra praleidžiamos, yra ištęsiamas daugiausiai iki penkių dienų (pradžios data priežiūros grafiko eilutėje numatoma *ir* dvi dienas prieš, *ir* dvi dienas po šios datos).

1. Grupės laukuose **Išsami informacija** „FastTab“ **Išsami informacija** rodo priežiūros plano eilučių, nustatytų pagal priežiūros planą, skaičių ir turto bei funkcinių vietų, susijusių su priežiūros planu, skaičių.

1. „FastTab“ **Eilutės** pasirinkite **Įtraukti laiko eilutę** arba **įtraukti turto skaitiklio eilutę** naujos priežiūros plano eilutės sukūrimui.

1. Įterpkite aprašą į eilutę lauke **Darbo užsakymo aprašas**. Aprašas yra perkeliamas į susijusius darbo užsakymus.

1. Pasirinkite užduoties tipą, su kuriuo susieta priežiūros plano eilutė, lauke **Priežiūros užduoties tipas**.

1. Laukuose **Priežiūros užduoties tipo variantas** ir **Prekybos šaka** pasirinkite variantą ir prekybos šaką, susijusią su priežiūros užduoties tipu.

1. Laukuose **Baigti per dienas** ir **Baigti per valandas** galite įterpti numatomą pabaigos datą dienomis arba valandomis. Numatoma pabaigos data įterpiama atitinkamai kaip ir numatoma pradžios data, kuri apskaičiuojama kuriant priežiūros grafiko eilutes. Pavyzdžiui, galite įterpti „7“ į lauką **Baigti per dienas**, kad nurodytumėte, jog susijusi užduotis turi būti atlikta per savaitę nuo numatomos pradžios datos.

1. Lauke **intervalo tipas** pasirinkite intervalo tipą, kurį norite naudoti priežiūros plano eilutėje, pvz., „Pasikartoja...“ arba „Kartą...“. Toliau pateiktoje lentelėje žr. dėl intervalo ir eilutės tipų ryšių aprašo [Intervalo tipų apžvalga](#interval-types).

1. Laukas **Laikotarpis** susijęs tik su laiku grindžiamais eilučių tipais. Pasirinkite laikotarpio tipą, susijusį su laikotarpio dažniu.

1. Lauke **Laikotarpio dažnis** įterpkite skaičių, kiek kartų eilutė turėtų būti naudojama prevencinėms priežiūros užduotims planuoti. Pavyzdys: Jei sukūrėte eilutę, kurios tipas „Skaitiklis“, ir jūsų skaitiklis yra gamybos kiekis, o šiame lauke įterpėte numerį „20 000“, naujos priežiūros sekų eilutės sukuriamos atliekant prevencinį priežiūros planavimą kaskart, kai tikimasi pagaminti dar 20 000 prekių.

1. Žymės laukelis **Sulaikyti persidengiančias priežiūros užduotis** susijęs su laiku ir skaitikliu grindžiamais eilučių tipais. Pasirinkite žymės langelį, kad būtų panaikinti sukurti tą pačią datą priežiūros grafiko įrašai. Tai svarbu, jei, pavyzdžiui, jūs sukūrėte 1 mėnesio tikrinimo eilutę, 6 mėnesių tikrinimo eilutę ir 1 metų tikrinimo eilutę. Norėdami atlikti 1 metų patikrinimą, norėsite, kad būtų atliktas tik vienas patikrinimas, o ne kiti du patikrinimai, kurie taip pat patenka į laiko intervalą. Norėdami nustatyti, kad šis pavyzdys būtų teisingas, nustatykite 1 metų patikros eilutę kaip pirmąją eilutę, 6 mėnesio eilutę kaip antrą eilutę ir 1 mėnesio eilutę kaip trečią eilutę ir pasirinkite **Sulaikyti persidengiančias priežiūros užduotis** žymės langelį 1 mėnesio ir 6 mėnesių eilutėms. Taip užtikrinsite, kad kai pasieksite 1 metų žymą, vieno mėnesio ir šešių mėnesių patikrinimai būtų praleisti, o priežiūros grafiko eilutė būtų sukurta tik 1 metų patikrinimo eilutei.

    >[!NOTE]
    >Šiame veiksme aprašytas pavyzdys parodo, kad sudėtingiausia užduotis, kurioje yra daugiausiai užduočių ir kuri atliekamas nedažnai, turi būti visada įterptas į pirmąją eilutę. Dažniau pasitaikančios užduotys įterpiamos kaip atskiros eilutės dažnio tvarka – dažniausiai pasitaikančios užduotys bus sąrašo apačioje.

1. Laukas **Skaitiklis** susijęs tik su skaitikliu grindžiamais eilučių tipais. Pasirinkite eilutėje naudotiną skaitiklio tipą. Jei skaitiklio tipas neaktyvus susijusiame turte, priežiūros plano eilutė nenurodoma.

1. Laukas **Turto skaitiklio laiko riba dienomis** yra susijęs tik su skaitikliu grindžiamais eilučių tipais. Įveskite skaičių, nurodantį, kiek dienų atgal skaitiklio registravimų reikia tikrinti, kai kuriamas priežiūros plano grafikas. Tai reiškia, kiek toli atgal bus tikrinami duomenys (nuo esamų skaitiklio registravimų), naudojami apskaičiuoti tendenciją, nustatančią, kiek priežiūros grafiko eilučių buvo sukurta.

    >*Pavyzdys:* jei skaitiklio registravimai turi būti atlikti kartą per mėnesį, šiame lauke galite įterpti numerį „365“, nes priežiūros plano grafikas visada bus paremtas paskutiniaisiais 12 mėnesių ir taip sukurs priežiūros grafiko eilutes pagal praėjusių metų tendenciją. Kita vertus, jei šiame lauke įterpsite skaičių „10“, galite tikėtis, kad skaitiklio registravimai bus dažnesni, pvz., kasdien. Tai reiškia, kad planuojant priežiūros planą, skaitiklio registravimai per pastarąsias 10 dienų naudojami kaip priežiūros grafiko eilučių planavimo pagrindas.

1. Laukas **Planuoti datą** susijęs tik su laiku grindžiamais eilučių tipais. Jei priežiūros plano eilutėje yra kita planavimo data nei visame priežiūros plane, pasirinkite datą lauko **Planuoti datą** eilutėje.

1. Lauke **Aptarnavimo lygis** galite pasirinkti darbo užsakymo aptarnavimo lygį, kaip papildomą apribojimą priežiūros plano eilutėje, – naudotinas kaip darbo užsakymų aptarnavimo lygis.

1. Pažymėkite žymės langelį **Kurti automatiškai** jei norite, kad sudarant priežiūros planus darbo užsakymas būtų kuriamas automatiškai pagal pasirinktą priežiūros plano eilutę.

1. Jei pažymėjote žymės langelį **Kurti automatiškai**, galite pasirinkti automatiškai sukurto darbo užsakymo tipą lauke **Darbo užsakymo tipas**. Jei pažymėjote žymės langelį **Kurti automatiškai** ir nepasirenkate darbo užsakymo tipo šiame lauke, bus naudojamas darbo užsakymo tipas, pasirinktas **Turto valdymas \> Sąranka \> Turto valdymo parametrai \> Darbo užsakymai** nuorodos \> **Prevencinis darbo užsakymo tipas** lauke.

1. Naudokite laukus **Sezonas nuo** ir **Sezonas iki**, siekiant per 12 mėnesių laikotarpį sukurti pakartotiną laiku pagrįstą priežiūros plano eilutę. *Pavyzdys:* įrangai, naudojamai ekologiškiems plotams prižiūrėti, reikia aptarnavimo kiekvieną pavasarį iš anksto nustatytu laikotarpiu. Įterpti laikotarpio pradžios datą, kuri bus kartojama lauke **Sezonas nuo**.

1. Įterpti laikotarpio pabaigos datą, kuri bus kartojama lauke **Sezonas iki**.

1. Lauke **Numatytasis laikotarpis** rodomas dabartinis kartotinas laikotarpis. Kai dabartinis laikotarpis pasibaigs ir prasidės kiti metai, šiame lauke rodomas laikotarpis bus atnaujintas, kad atitiktų kitą pasikartojančios sekos laikotarpį.

1. „FastTab“ **Turtas** pasirinkite turtą, kuris turėtų būti susietas su priežiūros planu:

1. Iš „FastTab“ **Turto tipai** pasirinkite turto tipus, kurie turėtų būti susieti su priežiūros planu:

1. Iš „FastTab“ **Funkcinės vietos** pasirinkite funkcines vietas, kurios turėtų būti susietos su priežiūros planu: Jei reikia, galite nustatyti konkretesnę sąranką pasirinkdami susijusį turto tipą, gamintoją ir modelį.

1. Iš „FastTab“ **Funkcinės vietos tipų** pasirinkite funkcinės vietos tipus, kurie turėtų būti susieti su priežiūros planu:

>[!NOTE]
>Kai neautomatiniu būdu sukuriami darbo užsakymai turtui, kuriam taikoma tiekėjo garantija, rodomas dialogo langas, kad vartotojas žinotų apie garantiją. Darbo užsakymo kūrimas vėliau gali būti atšauktas. Garantinis čekis neįtraukiamas automatiškai sukurtuose darbo užsakymuose.

<a id="interval-types"></a>

## <a name="interval-types-overview"></a>Intervalo tipų apžvalga

| Intervalo tipas ir aprašymas | Eilutės tipas: Laikas | Eilutės tipas: Skaitiklis |
|---|---|---|
| **Intervalo tipas: Kartojamas nuo plano datos** – skaičiavimas pradedamas nuo naudojamo plano datos. Kai planuojate priežiūros planus, pasiekus intervalą, sukuriamos priežiūros grafiko eilutės. | Priežiūros plano eilutei naudojama reikšmė iš **Plano data**. Jei eilutėje nėra pasirinkta plano data, naudojama priežiūros planui naudojama reikšmė iš **Plano data.**. Pavyzdys: jei lauke **Laikotarpio dažnis** įterpiamas numeris „3“ ir pasirenkama Taip lauke **Laikotarpis**, nauja priežiūros grafiko eilutė bus sukuriama kas 3 metus. | Priežiūros planui naudojama reikšmė iš **Plano data**. Jei skaitiklis buvo pakeistas, naujausia pakeitimo data yra naudojama kaip plano data. |
| **Intervalo tipas: Kartojamas nuo pradžios datos** – skaičiavimas pradedamas nuo turto ryšio pradžios datos. Data pasirenkama iš **Visas turtas** išsamios informacijos rodinyje \> **Turto priežiūros planai** „FastTab” lauke \> **Pradžios data** arba **Visos funkcinės vietos** išsamios informacijos rodinyje, \> **Priežiūros planai** „FastTab” \> **Pradžios data** lauke. Kai planuojate priežiūros planus, pasiekus intervalą, sukuriama nauja priežiūros grafiko eilutė. | Turtui arba funkcinei vietai naudojama priežiūros plano eilutės pradžios data. Jei šis laukas tuščias, priežiūros planui naudojama reikšmė iš **Plano data**. | Turtui arba funkcinei vietai naudojama priežiūros plano eilutės pradžios data. Jei šis laukas tuščias, priežiūros planui naudojama reikšmė iš **Plano data**. |
| **Intervalo tipas: Kartojamas nuo paskutinio darbo užsakymo** – skaičiavimas prasideda nuo paskutinio darbo užsakymo, kuris buvo atliktas turtui su konkrečiu priežiūros užduoties tipo / priežiūros užduoties tipo varianto / prekybos deriniu, faktinės pabaigos datos ir laiko. Ši data ir laikas rodomi lauke **Faktinė pabaiga**, esančiame išsamios informacijos rodinyje **Visi darbo užsakymai**. | Turto su konkrečiu priežiūros užduoties tipo / priežiūros užduoties tipo varianto / prekybos deriniu faktinė baigto darbo užsakymo pabaigos data ir laikas. Jei nesurastas baigtas darbo užsakymas, tada naudojama viena iš datų, iš anksčiau aprašyto intervalo tipo „Kartojamas nuo pradžios datos“. | Turto *ir* priežiūros užduoties tipo / priežiūros užduoties tipo varianto / prekybos derinio faktinė baigto darbo užsakymo pabaigos data ir laikas. yra naudojama. Jei darbo užsakyme pabaigos data ir laikas yra nenurodytas, tada naudojama viena iš datų, iš anksčiau aprašyto intervalo tipo „Kartojamas nuo pradžios datos“. |
| **Intervalo tipas: Kartą nuo plano datos** žr. ankstesnį intervalo tipo „Kartojamas nuo plano datos“ aprašą. Vienintelis šio intervalo tipo skirtumas – jis naudotinas tik vieną kartą. | Žr. ankstesnį intervalo tipo „Kartojamas nuo plano datos“ aprašą. Šis intervalas paprastai naudojamas vienkartiniai priežiūrai ar aptarnavimo užduočiai. | Žr. ankstesnį intervalo tipo „Kartojamas nuo plano datos“ aprašą. Šis intervalas paprastai naudojamas vienkartiniai priežiūrai ar aptarnavimo užduočiai. **1 Pastaba.** Šis intervalo tipas yra aktualus tik tada, kai skaitiklis pakeičiamas kiekvieną kartą vykdant priežiūros ar aptarnavimo užduotį. Jeigu dėl kokių nors priežasčių skaitiklis buvo pakeistas prieš planuojamo intervalo pabaigą, skaičiuojamas naujas užduoties laikas nuo skaitiklio pakeitimo. **2 Pastaba.** Jei skaitiklis pakeičiamas atliekant priežiūros ar aptarnavimo užduotį, šis intervalo tipas veikia kaip ankstesnis intervalo tipas „Kartojamas nuo plano datos“. |
| **Intervalo tipas: Kartą nuo pradžios datos** žr. ankstesnį intervalo tipo „Kartojamas nuo pradžios datos“ aprašą. Vienintelis šio intervalo tipo skirtumas – jis naudotinas tik vieną kartą. | Žr. ankstesnį intervalo tipo „Kartojamas nuo pradžios datos“ aprašą. Šis intervalas paprastai naudojamas vienkartiniai priežiūrai ar aptarnavimo užduočiai. | Žr. ankstesnį intervalo tipo „Kartojamas nuo pradžios datos“ aprašą. Šis intervalas paprastai naudojamas vienkartiniai priežiūrai ar aptarnavimo užduočiai. Anksčiau minėta **1 pastaba** irgi taikoma šiam intervalo tipui. **3 Pastaba.** Jei skaitiklis pakeičiamas atliekant priežiūros ar aptarnavimo užduotį, šis intervalo tipas veikia kaip ankstesnis intervalo tipas „Kartojamas nuo pradžios datos“. |
| **Intervalo tipas: Pasiekus viršutinę ribą** nurodytas intervalo tipas, susijęs tik su skaitikliais ir yra naudojamas, siekiant nurodyti viršutinę ribą, nustatytą priežiūros plano eilutėje. Priežiūros grafiko įrašuose bus numatyta skaitiklio registravimo pradžios data ir laikas, t. y. šie įrašai bus sukurti su numatoma pradžios data, kuri yra lygi sistemos datai arba yra ankstesnė už ją. | Netaikoma | Skaitiklio intervalas nurodo viršutinę ribą. Jei ši riba viršijama kuriant skaitiklio registraciją, priežiūros grafiko eilutė sukuriama, kai planuojate profilaktinę priežiūrą. |
| **Intervalo tipas: Pasiekus apatinę ribą** nurodytas intervalo tipas, susijęs tik su skaitikliais ir yra naudojamas, siekiant nurodyti apatinę ribą, nustatytą priežiūros plano eilutėje. Priežiūros grafiko įrašuose bus numatyta skaitiklio registravimo pradžios data ir laikas, t. y. šie įrašai bus sukurti su numatoma pradžios data, kuri yra lygi sistemos datai arba yra ankstesnė už ją. | Netaikoma | Skaitiklio intervalas nurodo apatinę ribą. Jei ši riba pasiekiama kuriant skaitiklio registravimą, priežiūros grafiko eilutė sukuriama, kai planuojate profilaktinę priežiūrą. |
| **Intervalo tipas: Susietas nuo pradžios datos** datos – šis intervalo tipas sukuria priežiūros grafiko eilutę tik vieną kartą. Priežiūros plane gali būti daugiau priežiūros plano eilučių, naudojančių šį intervalo tipą, ir šios eilutės yra susietos. Paprastai sukuriate priežiūros planą, kuriame yra tik šio intervalo tipo eilutės. Priežiūros grafiko eilutės sukuriamos identifikuojant priežiūros plano eilutę, kurioje yra pirmoji numatoma pradžios data ir laikas. | Žr. ankstesnį intervalo tipo „Kartą nuo pradžios datos“ aprašą. Pavyzdys: galite sukurti dvi aptarnavimo užduoties priežiūros plano eilutes, skirtas automobiliui: viena, laiku grindžiama, eilutė su 1 metų laikotarpiu ir viena eilutė, kuri ribojama iki 25 000 km. Yra sukuriama priežiūros grafiko eilutė, skirta pirmiau pasiektai ribai. Šiam eilutės tipui sukuriate eilutę su 1 metų laikotarpiu. | Žr. ankstesnį intervalo tipo „Kartą nuo pradžios datos“ aprašą. Pavyzdys: galite sukurti dvi aptarnavimo užduoties priežiūros plano eilutes, skirtas automobiliui: viena, laiku grindžiama, eilutė su 1 metų laikotarpiu ir viena eilutė, kuri ribojama iki 25 000 km. Yra sukuriama priežiūros grafiko eilutė, skirta pirmiau pasiektai ribai. Šiam eilutės tipui sukuriate eilutę su 25 000 km riba. Pavyzdys, kaip sukurti dvi skaitiklio eilutes: taip pat galite nustatyti priežiūros planą, kuriame yra dvi susijusios eilutės, kuriose pirmoje eilutėje yra 10 000 prekių kiekio riba, o antroji eilutė susijusi su įrenginiu arba darbo centru, kuriam reikia aptarnavimo po 3 000 veiklos val. |
| **Intervalo tipas: Susietas su paskutiniu darbo užsakymu** užsakymu – šis intervalo tipas sukuria naujas priežiūros grafiko eilutes po kiekvieno atlikto darbo užsakymo. Priežiūros plane gali būti daugiau eilučių, naudojančių šį intervalo tipą, ir šios eilutės yra susietos. Paprastai sukuriate priežiūros planą, kuriame yra tik šio intervalo tipo priežiūros plano eilutės. Priežiūros grafiko eilutės sukuriamos identifikuojant priežiūros plano eilutę, kurioje yra pirmoji numatoma pradžios data ir laikas. | Šis intervalo tipas iš esmės veikia kaip anksčiau aprašytasis „Susietas su pradžios data“. Vienintelis skirtumas – data, kuria remiasi intervalo tipas. Naudojama faktinė data ir laikas iš paskutinio atlikto darbo užsakymo turtui *ir* priežiūros užduoties tipui / priežiūros užduoties tipo variantui / prekybos šakų deriniui. | Šis intervalo tipas iš esmės veikia kaip anksčiau aprašytasis „Susietas su pradžios data“. Vienintelis skirtumas – data, kuria remiasi intervalo tipas. Naudojama faktinė data ir laikas iš paskutinio atlikto darbo užsakymo turtui *ir* priežiūros užduoties tipui / priežiūros užduoties tipo variantui / prekybos šakų deriniui. |
| **Intervalo tipas: Pakartoti sukauptai vertei (tik skaitiklis)** Paleidus priežiūros planą, kaskart, kai turto skaitiklio sukaupta vertė pasiekia ar net viršija laikotarpio dažnį, bus sukurta suplanuota priežiūros eilutė. (Laikotarpio dažnis apibrėžiamas priežiūros plano eilutėje.)<p>Daugiau informacijos apie tai, kaip įgalinti ir naudoti šią funkciją, žiūrėkite šios temos skyriuje [Skaitikliu paremti priežiūros patobulinimai](#counter-based-maintenance). | Netaikoma | **Pavyzdys:** Nustatytas turto AK-101 valandinis skaitiklis. Turtui taip pat nustatoma turto plano eilutė. Šios eilutės intervalo tipas yra *Pakartoti sukauptai vertei (tik skaitiklis)*, o laikotarpio dažnis *yra 1000*. Vykdant priežiūros planą, suplanuota priežiūros eilutė bus sugeneruota, kai bendra skaitiklio vertė viršys 1000 valandų. Tada, kai bendra skaitiklio vertė viršys 2000 valandų, bus sugeneruota kita suplanuota priežiūros eilutė ir taip toliau kiekvienam 1000 papildomų valandų. |
| **Intervalo tipas: Vieną kartą sukauptai vertei (tik skaitiklis)** Paleidus priežiūros planą, bus sukurta suplanuota priežiūros eilutė, kai turto skaitiklio sukaupta vertė pasieks laikotarpio dažnį, apibrėžtą priežiūros plano eilutėje.<p>Daugiau informacijos apie tai, kaip įgalinti ir naudoti šią funkciją, žiūrėkite [Skaitikliu paremti priežiūros patobulinimai](#counter-based-maintenance) skyriuje. | Netaikoma | **Pavyzdys:** Nustatytas turto AK-101 valandinis skaitiklis. Turtui taip pat nustatoma turto plano eilutė. Šios eilutės intervalo tipas yra *Vieną kartą sukauptai vertei (tik skaitiklis)*, o laikotarpio dažnis *yra 1000*. Vykdant priežiūros planą, suplanuota priežiūros eilutė bus sugeneruota, kai bendra skaitiklio vertė viršys 1000 valandų. |

>[!NOTE]
>Kai priežiūros grafiko eilutės kuriamos pagal laiku grindžiamas priežiūros plano eilutes, numatomas laikas visuomet yra dienos pradžioje. Skaitikliu grindžiamoms priežiūros plano eilutėms numatomas laikas gali būti bet kada dieną.

Toliau rasite laiku ir skaitikliu grindžiamų priežiūros plano eilučių sąrankos pavyzdžius:

**1 pavyzdys – laiku grindžiama priežiūros plano eilutė:** Tepimo užduotis gali būti nustatyta fiksuotame intervale, kuris įvyksta kartą per savaitę. Todėl lauke **Intervalo tipas** pasirinkite „Kartojamas nuo plano datos“. Žr. pavyzdį toliau esančiame paveikslėlyje.

![Paslaugų užduotis nustatyta fiksuotu intervalu, įvykstanti kartą per savaitę](media/02-preventive-maintenance.png "Paslaugų užduotis nustatyta fiksuotu intervalu, įvykstanti kartą per savaitę")

**2 pavyzdys – laiku grindžiama priežiūros plano eilutė:** Patikrinimo užduotis gali būti nustatyta atlikti maždaug kartą per savaitę. Todėl lauke **Intervalo tipas** pasirinkite „Kartojamas nuo paskutinio darbo užsakymo“. Žr. pavyzdį toliau esančiame paveikslėlyje.

![Tikrinimo užduotis, nustatyta atlikti maždaug kartą per savaitę](media/03-preventive-maintenance.png "Tikrinimo užduotis, nustatyta atlikti maždaug kartą per savaitę")

**3 pavyzdys – skaitikliu grindžiama priežiūros plano eilutė:** Toliau esančiame paveikslėlyje vaizduojamas valandų skaitiklis, kuriam sukuriama nauja priežiūros grafiko eilutė kaskart praėjus 250 val. Šios skaitikliu grindžiamos eilutės intervalo tipas yra „Kartojamas nuo pradžios datos“. Pradžios data pasirenkama iš susijusio turto pradžios datos išsamios informacijos rodinio **Visas turtas** „FastTab” \> **Turto priežiūros planai** lauko \> **Pradžios data** arba išsamios informacijos rodinio **Funkcinė vieta** „FastTab“ \> **Priežiūros planai** lauko \> **Pradžios data**. Tai yra *prevencinio* priežiūros plano pavyzdys, nes priežiūros grafiko eilutė automatiškai sukuriama kiekvienąkart pasiekus ribinę vertę (+ 250).

![Valandinis skaitiklis, periodiškai kuriantis priežiūros grafiko eilutes](media/04-preventive-maintenance.png "Valandinis skaitiklis, periodiškai kuriantis priežiūros grafiko eilutes")

**4 pavyzdys – skaitikliu grindžiama priežiūros plano eilutė:** Toliau esančiame paveikslėlyje vaizduojamas skaitiklio reikšmės sumažėjimas, matuojant stabdžių trinkelės nusidėvėjimą. Priežiūros grafiko eilutė sukuriama, kai stabdžių trinkelei fiksuojama žemesnė kaip 20 mm skaitiklio registracija. Šis skaitikliu paremtos eilutės intervalo tipas atitinka „Kartą pasiekus apatinę ribą“ arba „Kartą nuo paskutinės pradžios datos“. Tai yra *atsakomojo* priežiūros plano pavyzdys, nes priežiūros grafiko eilutė automatiškai nesukuriama, kol matuojant nėra registruojama žemiau 20 mm.

![Skaitiklio vertės sumažėjimas, matuojant stabdžių kaladėlių susidėvėjimą](media/05-preventive-maintenance.png "Skaitiklio vertės sumažėjimas, matuojant stabdžių kaladėlių susidėvėjimą")

**5 pavyzdys – skaitikliu grindžiama priežiūros plano eilutė:** Toliau esančiame paveikslėlyje vaizduojamas skaitiklis, kurio ribinė reikšmė yra -18 °C. Priežiūros grafiko eilutė sukuriama, kai atliekamas skaitiklio registravimas virš –18 ° Celsijaus. Šios skaitikliu grindžiamos eilutės intervalo tipas yra „Kartą pasiekus viršutinę ribą“. Tai yra *atsakomojo* priežiūros plano pavyzdys, nes priežiūros grafiko eilutė automatiškai nesukuriama, kol matuojant nėra registruojama aukštesnė nei –18 ° Celsijaus temperatūra.

![Skaitiklis, kurio ribinė vertė yra -18° C](media/06-preventive-maintenance.png "Skaitiklis, kurio ribinė vertė yra -18° C")

- Kai sukuriate naują turtą ir šis turtas naudoja turto tipą, susijusį su priežiūros planu, tas planas automatiškai įterpiamas į **Visi objektai \> Turto priežiūros planai** „FastTab“. Be to, lauke **Numatytasis turto tipas**, „FastTab“ **Priežiūros planai**, bus automatiškai įterpti į susijusius priežiūros planus.
- Jei į **Priežiūros planai** įtraukiate arba pašalinate turto tipus arba funkcinių vietų tipus, šis keitimas bus skirtas tik naujam turtui, sukurtam atlikus pakeitimą.
- Jei į **Priežiūros planai** įtraukiate ar pašalinate turtą arba funkcines vietas, šis keitimas bus automatiškai atnaujintas **Visas turtas \> Turto priežiūros planai** „FastTab“ arba **Visos funkcinės vietos \> Priežiūros planai** „FastTab“.

Toliau pateiktame paveikslėlyje pateiktas priežiūros plano „Sunkvežimio priežiūra“ pavyzdys puslapyje **Priežiūros planai**.

![Sunkvežimio paslaugos priežiūros plano pavyzdys](media/07-preventive-maintenance.png "Sunkvežimio paslaugos priežiūros plano pavyzdys")

## <a name="add-a-maintenance-plan-to-an-asset"></a>Įtraukti priežiūros planą į turtą

1. Eikite į **Turto valdymas \> Bendra \> Turtas \> Visas turtas** arba **Aktyvus turtas**.

1. Pasirinkite turtą, kuriam norite nustatyti priežiūros planą ir pasirinkite **Redaguoti**.

1. „FastTab“ **Turto priežiūros planai** pasirinkite **Įtraukti eilutę** priežiūros plano įtraukimui į turtą.

1. Lauke **Priežiūros planas** pasirinkite atitinkamą priežiūros planą.

1. Lauke **Pradžios data** pasirinkite pradžios datą, nuo kurios pradedamas kurti prevencinis priežiūros planas. 

1. Pasirinkite **Įrašyti**. Laukas **Aktyvus** atnaujinamas automatiškai.

Toliau pateiktame paveikslėlyje pateiktas priežiūros planų, sukonfigūruotų turtui puslapyje **Visas turtas**, pavyzdys.

![Priežiūros plano, nustatyto turtui, pavyzdys](media/08-preventive-maintenance.png "Priežiūros plano, nustatyto turtui, pavyzdys")

<a id="counter-based-maintenance"></a>

## <a name="counter-based-maintenance-enhancements"></a>Skaitikliu pagrįsti priežiūros patobulinimai

> [!IMPORTANT]
> Šiame skyriuje aprašytos funkcijos yra galimos kaip peržiūros versijos leidimo dalis. Turinys ir funkcijos gali būti keičiami. Norėdami apie peržiūros leidimus gauti daugiau informacijos, žr. [DUK apie vienos versijos paslaugų naujinimus](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).

Priemonė *Skaitikliu pagrįsti priežiūros patobulinimai* turi šias funkcijas:

- Parinktį automatiškai įterpti skaitiklį su verte *0 (nulis)* sukūrus turtą. Ši parinktis gali būti naudinga, kai naudojate prognozinę priežiūrą, pagrįstą skaitikliais. Kai funkcija *Skaitikliu pagrįsti priežiūros patobulinimai* nenaudojama, skaitikliai su verte *0 (nulis)* turi būti įterpti rankiniu būdu.
- Galimybę sukonfigūruoti skaitiklį taip, kad jis automatiškai būtų nustatytas iš naujo, baigus darbo užsakymą. Ši funkcija naudinga, kai norite planuoti priežiūrą pagal sukauptą vertę nuo paskutinio užbaigto darbo užsakymo.
- Naują priežiūros plano intervalo tipą, pavadintą *Pakartoti sukauptai vertei (tik skaitiklis)*. Šis tipas suaktyvina priežiūrą kiekvieną kartą, kai bendras skaitiklis pakartotinai pasiekia konkrečią vertę. Pavyzdžiui, priežiūra gali būti suaktyvinta kas 10 000 valandų. Daugiau informacijos žiūrėkite ankstesniame šios temos skyriuje [Intervalo tipų apžvalga](#interval-types).
- Kitą priežiūros plano intervalo tipą, pavadintą *Vieną kartą sukauptai vertei (tik skaitiklis)*. Šis tipas suaktyvina priežiūrą, kai bendras skaitiklis pasiekia konkrečią vertę, pavyzdžiui 8000 valandų. Daugiau informacijos žiūrėkite [Intervalo tipų apžvalga](#interval-types) skyriuje.

### <a name="turn-on-the-counter-based-maintenance-enhancements-feature"></a>Skaitikliu pagrįstų priežiūros patobulinimų funkcijos įjungimas

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Turto valdymas*
- **Funkcijos pavadinimas:** *(Peržiūros versija) Skaitikliu pagrįsti priežiūros patobulinimai*

### <a name="create-and-initialize-counters-when-an-asset-is-created"></a>Skaitiklių kūrimas ir inicijavimas turto kūrimo metu

Kiekvieną kartą, kai kuriate turtą, susiję turto skaitikliai, kurių pradinė vertė yra lygi *0 (nuliui),* gali būti sukuriami automatiškai su sąlyga, kad nustatysite savo sistemą ir sukursite turtą tinkamai.

1. Eikite į **Turto valdymas \> Sąranka \> Turto tipai**.
1. Įsitikinkite, kad turite turto tipą, kuris taikomas jūsų planuojamam naujam turtui. Sukurkite turto tipą, kaip reikalaujama. Įsitikinkite, kad **Skaitikliai** „FastTab” pasirinkti visi reikiami skaitikliai.
1. Eikite į **Turto valdymas \> Sąranka \> Turto tipai \> Skaitikliai**.
1. Įsitikinkite, kad kiekvieno atitinkamo skaitiklio laukas **Bendras suvestinis rodiklis** nustatytas į *Suma*.
1. Puslapyje **Visas turtas** sukurkite turtą.
1. Nustatykite lauką **Turto tipas** į tokį turto tipą, kurį nustatėte arba sukūrėte 2 veiksmu.
1. Užbaikite naujo turto nustatymą, kaip reikalaujama.
1. Eikite į **Turto valdymas \> Užklausos \> Turtas \> Skaitikliai**. Turėtumėte rasti inicijuotus skaitiklius, kurie nustatyti jūsų naujam turtui.

> [!NOTE]
> Kai sukuriami inicijuoti turto skaitikliai, daroma prielaida, kad turtas niekada nebuvo panaudotas prieš jo įtraukimą į sistemą. Kai priežiūros grafikas vykdomas pirmą kartą, skaičiavime naudojama data ir *0 (nulinė)* skaitiklio vertė kaip būsimos priežiūros skaičiavimo bazinė linija. Jei turtas nebuvo naujas, įtraukiant jį į sistemą, galite rankiniu būdu koreguoti skaitiklio vertę, kad ji atitiktų faktinę skaitiklio vertę. Norėdami koreguoti skaitiklio vertę, atidarykite atitinkamą turtą puslapyje **Visas turtas** ir tada veiksmų srities skirtuko **Turtas** grupėje **Profilaktinė** pasirinkite **Skaitikliai**. Puslapyje **Turto skaitikliai** pasirinktam turtui koreguokite vertę stulpelyje **Vertė** pradiniam skaitiklio įrašui, kaip reikalaujama.

### <a name="automatically-reset-a-counter-value"></a>Automatinis skaitiklio vertės nustatymas iš naujo

Galite konfigūruoti sistemą taip, kad ji automatiškai iš naujo nustatytų skaitiklį kiekvieną kartą, kai atitinkamas darbo užsakymas pasieks pasirinktą būsenos vertę.

1. Eikite į **Turto valdymas \> Konfigūracija \> Prevencinė priežiūra \> Priežiūros planai**.
1. Iš sąrašo srities pasirinkite priežiūros planą. Skaitiklio nustatymas iš naujo bus taikomas visam turtui, naudojančiam šį planą.
1. Skyriuje **Eilutės** raskite turto skaitiklio eilutę, kurios skaitiklį norite nustatyti iš naujo, ir pažymėkite žymės langelį **Nustatyti skaitiklį iš naujo** tai eilutei. (Turto skaitiklio eilučių vertė yra **Skaitiklio** stulpelyje). (Skaitiklis, nurodytas tame stulpelyje, yra skaitiklis, kuris bus iš naujo nustatytas susijusiam turtui.)
1. Eikite į **Turto valdymas \> Sąranka \> Darbo užsakymai \> Ciklo būsenos**.
1. Sąrašo srityje pasirinkite darbo užsakymo ciklo būseną, kada reikia nustatyti iš naujo atitinkamą skaitiklį.
1. „FastTab“ **Bendra** nustatykite parinktį **Nustatyti skaitiklį iš naujo** į *Taip*.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]