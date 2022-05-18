---
title: Automatinių operacijų sąskaitos
description: Šioje temoje paaiškinama, kaip automatinės operacijos sąskaitos naudojamos Microsoft Dynamics registruojant naudojant 365, ir pateikiami automatinių operacijų pagrindinių sąskaitų pavyzdžiai.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 275c74d673d1ba2468e23c5fa443c9272d13a184
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735266"
---
# <a name="accounts-for-automatic-transactions"></a>Automatinių operacijų sąskaitos

Automatinių **operacijų sąskaitų** puslapis (**DK &gt; registravimo &gt;** nustatymo automatinių operacijų sąskaitos) naudojamas nustatyti numatytąją pagrindinę sąskaitą, kuri naudojama kiekvienam registravimo tipui sistemoje. Nors dauguma registravimo tipų gali būti konfigūruoti moduliui bingusioje ar nuo priemonės priklausomame puslapyje, **kai kuriuos registravimo tipus galima konfigūruoti tik automatinių operacijų puslapyje Sąskaitose**.

Pavyzdžiui, galite nurodyti **pagrindinę** **·** **sąskaitą**, kuri naudojama kliento balanso registravimo tipui kliento registravimo šablono puslapio lauke Suvestinė, ir naudoti skirtingą pagrindinę sąskaitą kiekvienam kliento šablonui. Tokiu būdu galite labiau kontroliuoti registravimus. Kita vertus, klaidų sąskaitą galite nurodyti tik automatinių **operacijų sąskaitų puslapyje**.

Kai atidarote naujo **juridinio subjekto** automatinių operacijų puslapio sąskaitas, sąskaitų sąrašas bus tuščias. Dažniausiai sukonfigūruotas registravimo tipus galite įtraukti puslapyje, pasirinkdami mygtuką Kurti **numatytuosius** tipus. Tada kiekvienoje eilutėje pagrindinę sąskaitą galite pasirinkti lauke **Pagrindinė** sąskaita. Jei registravimo **tipui** paliekate tuščią pagrindinės sąskaitos lauką ir nesukonfigūravote pagrindinės sąskaitos moduliui ar funkcijai basyje, užregistruodami operaciją, kurioje naudojamas registravimo tipas, gausite klaidos pranešimą. Paprastai pranešimas bus "Registravimo tipo \[sąskaita\] nerasta".

## <a name="default-posting-types"></a>Numatytieji registravimo tipai

Toliau esančioje lentelėje pateikiami numatytųjų registravimo tipų, sukurtų **·** **automatinio operacijų puslapio sąskaitose pasirinkus Kurti numatytuosius tipus,** pavyzdžiai. Jis rodo pagrindinių sąskaitų pavyzdį ir aprašus. Ar rodyti debetą/kreditą? Stulpelis nurodo, ar operacija paprastai registruoja debetą, ar kreditą. Kai kuriais atvejais operacija gali registruoti debetą arba kreditą. Stulpelyje Kliringo sąskaita nurodoma, ar registravimo tipas yra tarpuskaitos sąskaita. Jei registravimo tipas yra tarpuskaitos sąskaita, sąskaitoje užregistruota suma automatiškai atšaukiama, kai užregistruojama vėlesnė operacija.

| Registravimo tipas | Pagrindinės sąskaitos pavyzdys | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | Aprašymas |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Skirtumas centais ataskaitų valiuta | 618160 | Papildomos išlaidos | Išlaidos | Abu | Ne | Šis registravimo tipas naudojamas, kai skirtumas centais atsiranda tada, kai operacijos suma užsienio valiuta konvertuojama į ataskaitų valiutą. |
| Skirtumas centais apskaitos valiuta | 618160 | Papildomos išlaidos | Išlaidos | Abu | Ne | Šis registravimo tipas naudojamas, kai skirtumas centais atsiranda tada, kai operacijos suma užsienio valiuta konvertuojama į apskaitos valiutą. |
| Klaidų sąskaita | 999999 | Klaidų sąskaita | Išlaidos | Abu | Ne | Šis registravimo tipas naudojamas, kai sistemoje įvyksta klaida. Sąskaita turėtų būti tikrinama kiekvieną laikotarpį ir visos klaidos turi būti išspręstos. |
| Metų laikotarpio rezultatas | 300160 | Nepaskirstytas pelnas | Kapitalas | Abu | Ne | Šis registravimo tipas **naudojamas**, kai metų pabaigos uždarymo procesas vykdomas pelno ir nuostolio tipo sąskaitų balansui perkelti į pagrindinę sąskaitą, pasirinktą metų pabaigos rezultatui. |
| Kliento mokėjimo nuolaida | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Ne | Registravimo tipas, nustatytas automatinių **operacijų sąskaitų puslapyje**, nėra naudojamas. Pagrindinė sąskaita būtina, kai mokėjimo nuolaidos sukonfigūruotos gautinose sumose.|
| Tiekėjo mokėjimo nuolaida | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Ne | Registravimo tipas, nustatytas automatinių **operacijų sąskaitų puslapyje**, nėra naudojamas. Pagrindinė sąskaita būtina, kai mokėjimo nuolaidos sukonfigūruotos mokėtinose sumose. |

## <a name="additional-posting-types"></a>Papildomi registravimo tipai

Toliau esančioje lentelėje pateikiami papildomų registravimo tipų, kuriuos reikia sukonfigūruoti, jei planuojate naudoti susijusias priemones, pavyzdžiai. Šiems registravimo tipams kitame modulyje negalima naudoti registravimo šablono konfigūracijos. Ar rodyti debetą/kreditą? Stulpelis nurodo, ar operacija paprastai registruoja debetą, ar kreditą. Kai kuriais atvejais operacija gali registruoti debetą arba kreditą. Stulpelyje Kliringo sąskaita nurodoma, ar registravimo tipas yra tarpuskaitos sąskaita. Jei registravimo tipas yra tarpuskaitos sąskaita, sąskaitoje užregistruota suma automatiškai atšaukiama, kai užregistruojama vėlesnė operacija.

| Registravimo tipas | Pagrindinės sąskaitos pavyzdys | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | Aprašymas |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Konsolidavimo skirtumo balanso sąskaita | 801200 | Pelnas ir nuostolis – perkainojimas | Išlaidos | Abu | Ne | Šis registravimo tipas naudojamas, kai atliekate konsolidaciją, į kurią įeis valiutos kurso pasikeitimas, o perkainojimo metu atsiranda centų skirtumai. |
| Pelno ir nuostolio sąskaita, skirta konsolidacijos skirtumams | 801200 | Pelnas ir nuostolis – perkainojimas | Išlaidos | Abu | Ne | Šis registravimo tipas naudojamas, kai atliekate konsolidaciją, į kurią įeis valiutos kurso pasikeitimas, o perkainojimo metu atsiranda centų skirtumai. |
| Susiję vienetų – debetas | 133500 | Gautinos sumos tarp susiję vienetų | Turtas | Debetas | Ne | Šis registravimo tipas naudojamas, kai DK puslapyje **pasirenkate** balansavimo dimensiją ir ji neturi užregistruotos operacijos balanso. |
| Susiję vienetai – kreditas | 233500 | Susiję susiję su mokėtina suma | Įsipareigojimai | Kreditas | Ne | Šis registravimo tipas naudojamas, kai DK puslapyje **pasirenkate** balansavimo dimensiją ir ji neturi užregistruotos operacijos balanso. |
