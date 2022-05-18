---
title: Atsargų operacijų informacija
description: Šioje temoje pateikta operacijų informacijos puslapio, kuriame rodoma pasirinktos atsargų operacijos informacija, apžvalga.
author: rachel-profitt
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventTrans, InventTransDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: fd1416f21ce15dc832dd41ea4110c93bf5bb41a2
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735880"
---
# <a name="inventory-transaction-details"></a>Atsargų operacijų informacija

Norėdami peržiūrėti **išsamią informaciją** apie bet kurią pasirinktą atsargų operaciją, naudokite operacijų informacijos puslapį.

## <a name="open-the-transaction-details-page"></a>Atidaryti operacijos informacijos puslapį

Norėdami atidaryti puslapį **Operacijų informacija**, atlikite šiuos veiksmus.

1. Eikite **į Atsargų valdymo \> užklausas ir ataskaitas \> Operacijos**.
1. Pasirinkite operaciją, kurią norite tikrinti.
1. Veiksmų srityje pasirinkite operacijos **informaciją**.

## <a name="fasttabs-overview"></a>"FastTab" peržiūra

Operacijų **informacijos puslapis** yra padalintas į keletą "FastTab". Toliau pateikiamoje lentelėje aprašoma kiekvieno "FastTab" paskirtis.

| FastTab | Aprašymas |
|---|---|
| Bendra | Šioje "FastTab" rodoma pagrindinė informacija apie pasirinktas atsargų operacijas. Be laukų, kurie rodomi atsargų **operacijų** puslapyje, jame yra ir papildomi laukai, kurie aprašomi toliau šioje temoje. |
| Atnaujinimas | Šiame "FastTab" rodoma informacija, susijusi su pasirinktos atsargų operacijos faktiniais, finansiniais ir sudengimo aspektais. Kai kurie laukai gali būti tušti, tai priklauso nuo dabartinės operacijos būsenos. Tačiau šie laukai bus automatiškai nustatomi registruojant operacijas. Kartu su laukais, kurie rodomi atsargų **operacijų** puslapyje, šiame "FastTab" yra papildomi laukai, kurie aprašomi toliau šioje temoje. |
| Registravimas DK | Šiame "FastTab" rodomas registravimo tipas ir DK sąskaita, naudojami faktiniam atnaujinimų, finansinio atnaujinimo, faktinių įplaukų, faktinių išlaidų, finansinių įplaukų ir finansinių išlaidų, susijusių su pasirinkta atsargų operacija, metu. |
| Nuorodos | Šioje "FastTab" rodoma papildoma informacija apie šaltinio operaciją, sukūrusią pasirinktą atsargų operaciją. Pavyzdžiui, ši informacija gali apimti pirkimo ar pardavimo užsakymo duomenis. |
| Susijusi informacija | Šioje "FastTab" rodoma papildoma informacija apie pasirinktas atsargų operacijas. Šie laukai gali būti nustatyti, jei nenaudojate kai kurių funkcijų, pvz., įsigijimo kategorijų ar projektų. |
| Finansinės dimensijos – faktinės | Šiame "FastTab" rodomos finansinių dimensijų vertės, kurios buvo naudojamos registruojant faktiškai atnaujinimą. Jei faktinis atnaujinimas neužregistruotas, laukai bus tušti. |
| Finansinės dimensijos – finansinės | Šiame "FastTab" rodomos finansinių dimensijų vertės, kurios buvo naudojamos registruojant finansinį atnaujinimą. Jei finansinis atnaujinimas neužregistruotas, laukai bus tušti. |
| Atsargų dimensijos | Šiame "FastTab" rodomos atsargų dimensijų vertės, kurios priskirtos pasirinktai atsargų operacijai. Šios vertės apima vietą, sandėlį, dydį, spalvą, konfigūraciją, vietą, paketo numerį, serijos numerį, atsargų būseną, numerio lentelę ir savininką. |

## <a name="fields-on-the-general-fasttab"></a>Laukai bendrajame "FastTab"

Toliau pateikiamoje lentelėje aprašomi bendrosios **"** FastTab" laukai, kurie taip pat nerodomi **atsargų operacijų** puslapyje.

| Laukas | Aprašymas |
|---|---|
| Šalis | Pasirinktos atsargų operacijos susijusios šalies pavadinimas. Pavyzdžiui, pirkimo užsakymo operacija rodo tiekėjo pavadinimą pirkimo užsakyme, o pardavimo užsakymo operacija rodo kliento vardą. Šis laukas negalimas visų tipų atsargų operacijoms. |
| Atsargų nuoroda | Jei kita atsargų operacija yra susijusi su pasirinkta atsargų operacija, tos kitos operacijos tipas. Pavyzdžiui, jei pirkimo užsakymas pažymėtas pagal pardavimo užsakymą, **pirkimo** užsakymo operacijos atsargų nuorodos laukas bus nustatytas kaip Pardavimo *užsakymas*. Tiesioginio pristatymo užsakymų ir vidinės įmonės užsakymų žymėjimas automatiškai. Naudojant žymėjimą su *kitais* *nei* standartinės išlaidos ir slankusis vidurkis įkainojimo metodais, sistema sukurs sudengimų ir tikslių pažymėtų operacijų koregavimus. Tokiu būdu galite pasiekti "faktines" įkainojimo išlaidas, kurios nepaiso "pirmasis į, pirmasis iš" (FIFO) logikos; paskutinė į, paskutinė iš (LIFO); arba svertinis vidurkis. |
| Atsargų numeris | Konkreti operacija, susijusi su pasirinkta atsargų operacija. Pavyzdžiui, jei pirkimo užsakymas pažymėtas pagal pardavimo užsakymą, **pirkimo** užsakymo operacijos atsargų numerio laukas bus nustatytas kaip pardavimo užsakymo numeris. |
| Projekto ID | Jei pasirinkta atsargų operacija yra susijusi su projektu, šiame lauke nustatomas projekto numeris. |
| Partijos numeris | Unikalus partijos ID, kurį sistema priskyrė parinktai atsargų operacijai. |
| Nuoroda į partiją | Jei kita atsargų operacija yra susijusi su pasirinkta atsargų operacija, tos kitos operacijos partijos ID. Pavyzdžiui, jei pirkimo užsakymas pažymėtas pagal pardavimo užsakymą, **·** **pirkimo užsakymo operacijos laukas Nuoroda į partiją bus pardavimo užsakymo eilutės atsargų operacijos partijos ID** vertė. |
| Dimensijos numeris | Unikalus ID, nurodantis visų atsargų dimensijų verčių, priskirtų parinktai atsargų operacijai, derinį. |
| Atvira vertė | Vertė, nurodanti, ar pasirinkta atsargų operacija sudengta atsargų uždarymo proceso metu. Jei šis laukas nustatytas kaip *Taip*, operacija nesudengta. |
| Numatoma data | Gavimo operacijų data, kai numatomas atsargų gavimas. Pavyzdžiui, šis laukas gali rodyti numatomą gavimo datą atsargų blokavimo užsakyme arba pristatymo datą pirkimo užsakymo eilutėje. |
| Atsargų data | Šis laukas nustatomas, kai gavimo užsakyme buvo atlikta registracijos operacija prieš registruojant remiantis faktiniu gavimu. |
| Nefinansinis perkėlimas | Vertė, nurodanti, ar pasirinkta atsargų operacija yra nefinansinis perkėlimas. Nefinansinis perkėlimas įvyksta, kai atsargų dimensijų pakeitimas prekių modelių grupės puslapyje **nėra finansiškai sekamas**. |
| Perkėlimo partijos ID | Jei pasirinkta atsargų operacija yra nefinansinis perkėlimas, šiame lauke nustatoma kitos atsargų operacijos, **su kuria sudengiama pasirinkta operacija, partijos ID** vertė. |

## <a name="fields-on-the-updates-fasttab"></a>Naujinimų "FastTab" laukai

Toliau pateikiamoje lentelėje aprašomi Naujinimų **"** FastTab" laukai, kurie taip pat nerodomi **atsargų operacijų** puslapyje.

| Laukas | Aprašymas |
|---|---|
| Faktinis kvitas | Kvito numeris iš DK, kurioje buvo sugeneruotas pasirinktos atsargų operacijos faktinis registravimas. |
| Maršrutas | Maršrutas, susijęs su pasirinkta atsargų operacija. Šis laukas nustatomas tik gamybos išrinkimo dokumentų operacijoms, kai komplektavimo specifikacija (KS) arba formulės eilutė yra susijusi su konkrečia preke. |
| Važtaraštis | Įvestas pirkimo užsakymo gavimo dokumento operacijos važtaraščio numeris. |
| Faktinių išlaidų suma | Faktinio atnaujinimo suma, užregistruota DK. Standartiniam produktui ši suma nurodo standartinę savikainą. Kitiems įkainojimo metodams registravimo metu jis pateikia produkto svertinį vidurkį. |
| Fakt. įplaukos | Atidėtų įplaukų suma, užregistruota DK, kad būtų faktiškai atnaujinta. |
| Krovinio ID | Jei dabartinė operacija susijusi su transportavimo valdymo kroviniu, šiame lauke rodomas unikalus krovinio, į kurį įtraukta prekė, numeris. |
| Faktiškai užregistruota | Vertė, nurodanti, ar pasirinkta atsargų operacija buvo faktiškai užregistruota. Jei dabartinė operacija užregistruota DK, bus ir faktinis kvitas. |
| Finansiškai užregistruota | Vertė, nurodanti, ar pasirinkta atsargų operacija finansiškai užregistruota. Jei dabartinė operacija užregistruota DK, bus ir finansinis kvitas. |
| Užregistruotos faktinės išlaidos | Vertė, nurodanti, ar buvo užregistruoti faktiniai mokesčiai, susiję su pasirinkta atsargų operacija. |
| Užregistruotos finansinės išlaidos | Vertė, nurodanti, ar buvo užregistruoti finansiniai mokesčiai, susiję su pasirinkta atsargų operacija. |
| Fin. kvitas | Kvito numeris DK, kurioje buvo sugeneruotas finansinis registravimas. |
| Sąskaita faktūra | Sugeneruotas SF numeris, pavyzdžiui, pirkimo ar pardavimo užsakymo. |
| Koregavimas | Suma, pakoreguota pasirinktoje atsargų operacijoje, per atsargų uždarymo ir koregavimo procesą. |
| Pelnas ir nuostolis, užregistruota suma | Pasirinktos atsargų operacijos suma, užregistruota pelno ir nuostolio išraše. |
| Neužregistruota SF | Susijusio pirkimo užsakymo SF numeris, rodomas laukiančio **tiekėjo SF** puslapyje. |
| Fin. uždaryta | Data, kai operacija visiškai sudengta. |
| Padengtas ES kiekis | Esamo svorio kiekis, kurį padengia sudengimas. |
| Sudengtas kiekis | Pasirinktos atsargų operacijos kiekis, sudengtas. |
| Sudengta  suma | Pasirinktos atsargų operacijos vertė, sudengta. |
