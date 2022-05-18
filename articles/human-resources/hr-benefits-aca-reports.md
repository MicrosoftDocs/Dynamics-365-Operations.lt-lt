---
title: Ataskaitų pagal įstatymą dėl prieinamos sveikatos priežiūros (ACA) generavimas
description: Prieinamos sveikatos priežiūros ataskaitos sukuria formas 1095-B ir 1095-C palaikančias **Darbdavio mandato** dalį prieinamos sveikatos priežiūros akto.
author: twheeloc
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 9ef67fba97282d1fc641f0281cd51c8ff08c65e5
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690840"
---
# <a name="generate-aca-reports"></a>ACA ataskaitų generavimas


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Prieinamos sveikatos priežiūros ataskaitos sukuria formas 1095-B ir 1095-C palaikančias **Darbdavio mandato** dalį prieinamos sveikatos priežiūros akto.

> [!NOTE]
> ACA ataskaitos yra įjungtos tik juridiniams asmenims JAV.

## <a name="getting-started"></a>Darbo pradžia

Norėdami sekti informaciją 1095-B ir 1095-C formoms, pirmiausia sukurkite vieną ir daugiau prieinamos sveikatos priežiūros aprėpties grupių. Prieinamos sveikatos priežiūros grupės rodo:

- Aprėpties pasiūlymas pateiktas darbuotojui
- Darbuotojo dalis mažiausių kaštų mėnesio premijos, jei kaštai viršija federalinį skurdo lygį
- Saugų uostą naudojamą darbuotojo, jei taikomas

Prieinamos sveikatos priežiūros aprėpties grupė jums leidžia valdyti informaciją šiems laukeliams nekeičiant kiekvieno darbuotojo įrašo, kai sąlygos nekinta. Galtie nesunkiai iš naujo paskirti prieinamos sveikatos priežiūros aprėpties grupes vienam ar keliems darbuotojams su **Masinio paskyrimo** parinktimi puslapyje.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Kelių draudimo grupės versijų išlaikymas

Galite išlaikyti kelias bet kurios aprėpties grupės versijas. Ši funkcija jums leidžia atlikti keitimus be poreikio kurti naują grupę ir paskirti jai darbuotojus. 

Jums kuriant ACA aprėpties grupes, galite kurti masių priskyrimą grupėms ir darbuotojams su **masių priskyrimo** parinktimi. Galite ir atskirai priskirti darbuotojus grupėms siekiant sekti ir pranešti ACA informaciją bei paskirti darbuotoją prienamų sveikatos priežiūros paslaugų aprėpties grupei.

Jums nereikia sekti kai kurios ACA aprėpties informacijos, tokios kaip ne pilno etato darbuotojams. Tokiu atveju, nustatykite **Pranešti aprėptį** laukelį į **Ne**. Nepaisant to, kad turite priskirti kiekvieną darbuotoją sekamai ACA informacijai į prieinamų sveikatos priežiūros paslaugų aprėpties grupę, vis dar galite keisti tolesnes parinktis bet kuriems mėnesiams, kuriems reikia kitų verčių:

- **Draudimo pasiūlymas**
- **Darbuotojui tenkanti išlaidų dalis**
- **Saugus prieglobstis**

Norėdami įvesti išlygas prieinamoms sveikatos priežiūros paslaugų grupems vertėms, rinkitės **Prieinamos sveikatos priežiūros paslaugos** nuorodą **Darbuotojo išsami informacija** puslapyje skyriuje **Papildoma informacija** esančiame **Darbuotojo skirtukas**.

## <a name="reporting-health-care-coverage"></a>Sveikatos priežiūros draudimo ataskaitos

Kartu su sveikatos draudimo aprėpties sekimu siūlomu pilno etato darbuotojams, jei darbdavys siūlo darbuotojo remiamaą draduimą sveikatos paslaugoms, už kurį darbuotojas yra įtrauktas (nepriklausomai nuo jo darbo pilnu ar ne pilnu etatu), papipldoma informacija turi būti pranešta 1095-C formoje. Kiekvienas darbuotojas (įskaitant priklausomuosius), kuriems taikomi darbdavio remiami išmokų planai, turi būti įtrauktas į tų mėnesių, kuriais planai buvo taikomi, ataskaitą. 

Galite nurodyti, ar norite, kad kiekvienas išmokų planas būtų praneštas pasirenkant **ACA ataskaitas** žymimame laukelyje.

Taip pat, jei darbuotojas pasirinko turėti išlaikytinių šiame išmokų plane, galite nurodyti išlaikytinių datas kiekvienam darbuotojui **Išlaikyti išmokas** puslapyje. Norėdami nurodyti, kad išlaikytinis yra apdraustas išmoka, rinkitės **Redaguoti** mygtuką veiksmų juostoje **Išlaikytiniai** greitame skirtuke.

Puslapyje **Priklausomųjų draudimo datų tvarkytuvas** galite nurodyti datas, kada priklausomajam buvo taikoma išmoka. Šiame puslapyje įvedus datas, puslapyje **Prižiūrėti išmokas** bus automatiškai pasirinktas žymės langelis **Apdraustas**.

## <a name="generate-1095-b-and-1095-c-forms"></a>Kurti 1095-B ir 1095-C formas

Galite taip pat kurti 1095-B ir 1095-C formas produkte ir dalyti juos visiems savo darbuotojams. Sistema gali elektroniniu būdu kurti 1095-C formas ir 1094-C IRS perdavimo failus.  

Kuriant 1095-C formą, įveskite atitinkamus mokesčių metus ir nurodykite socialinio draudimo numerius, kurie turi būti paslėpti. Jei spausdinate 1095-C formas daugiau nei 500 darbuotojų, gausite daugiau nei vieną PDF failą. Rekomenduojama padidinti į **maksimalų failo dydį** lange **Dokumentų valdymo parametrai** iki 150 MB.

## <a name="viewing-information"></a>Informacijos peržiūra

Norėdami peržiūrėti, kurie darbuotojai buvo priskirti kiekvienai draudimo grupei, kurių darbuotojų nereikia įtraukti į ataskaitą ir kurie darbuotojai nepriskirti, galite naudoti puslapį **Darbininko prieinamos sveikatos priežiūros draudimas**.

Jei bet kurios iš numatytų verčių prieinamų sveikatos priežiūros paslaugų grupė buvo viršyta, žvaigždutė pasirodys šalia pakeistos vertės. Jei visų 12 mėnesių reikšmės sutampa ir jų nebuvo nepaisoma, reikšmė bus išspausdinta stulpelyje **Visi 12 mėnesių**.

Galite taip pat prašyti lango suprasti, kurie darbuotojai buvo pažymėti kaip ACA neįtraukti. Jums nereikia sekti, ar aprėptis buvo siūloma jiems ar jiems nereikia išduoti 1095-C metų gale. Rinkitės **Ne ACA pranešami** laukelyje **Filtruoti pagal** siekiant sukurti darbuotojų sąrašą, kurie negaus 1095-C.

Taip pat, galite peržiūrėti visus darbuotjus, kurie nebuvo priskirti (**ACA ataskaitos aprėpties** laukelis tuščias) arba kurie nebuvo priskirti prieinamų sveikatos priežiūros paslaugų grupei, kuri nebegalioja pasirinktų **Metų** laukelyje.

Galite eksportuoti darbuotojų sąrašus, kurie sugeneruoti naudojant filtravimo parinktis, į „Excel“.

Jums reikia pranešti apdraustus asmenis, nes suteikiate savarankišką draudimą, galite peržiūrėti visus išlaikytinius, kurie apdrausti išmokų planais ir pažymėti kaip **ACA pranešama**. Rinkitės **Žiūrėti išlaikytinių draudimą** veiksmų juostoje.

> [!NOTE]
> Tik išmokų planai pažymėti kaip **ACA pranešami** rodomi užklausos lange.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
