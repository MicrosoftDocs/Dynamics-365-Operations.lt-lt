---
title: Elektroninio kasos aparato (EKA) operacijos, prisijungus ir neprisijungus prie interneto
description: Šioje temoje pateikiama informacija apie elektroninio kasos aparato (EKA) veikimą „Dynamics 365 Commerce“. Joje nurodoma, kur programoje galima iškviesti operacijas ir ar jos pasiekiamos neprisijungus.
author: jblucher
ms.date: 11/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-09-27
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 88daca466e0e01bf3870b6eeee0628e0c159fea3
ms.sourcegitcommit: 971456c197820421f108ad7345001cc1b6c99949
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/01/2021
ms.locfileid: "7875482"
---
# <a name="online-and-offline-point-of-sale-pos-operations"></a>Elektroninio kasos aparato (EKA) operacijos, prisijungus ir neprisijungus prie interneto

[!include [banner](includes/banner.md)]

Dauguma veiksmų, kuriuos vartotojai imsis pardavimo punkte (EKA), yra laikomi operacijomis. Operacijos sukonfigūruojamos ir valdomos „Dynamics 365 Commerce“ tarnybiniame biure. Į EKA mygtukyną galima įtraukti daug operacijų. Tada vartotojai, norėdami iškviesti operacijas ir atlikti jų teikiama funkciją, gali pasirinkti mygtukus. Kitos operacijos yra pagrindinės EKA programos dalis ir yra iškviečiamos naudojant ekrano mygtukus arba kaip kitos darbo eigos ar procesų dalis.

Šioje lentelėje pateikiama išsami informacija apie operacijas, kurias galima atlikti „Modern POS“ ir „Cloud POS“. Joje taip pat nurodoma, kur programoje galima iškviesti operacijas ir ar jos pasiekiamos EKA veikiant autonominiu režimu.

Kai kurių operacijų šiuo metu negalima atlikti „Modern POS“ ar „Cloud POS“. Kai kurios iš šių operacijų yra būdingos vietai ir joms reikalingi papildomi plėtiniai ir konfigūracija. Kitos operacijos yra „Microsoft Dynamics AX 2012“ operacijos, kurios šiuo metu nepalaikomos.

Toliau pateiktuose stulpeliuose nurodoma, kur galima iškviesti operacijas.

- **Mygtukynas** – operacija gali būti priskirta EKA mygtukynams, priklausantiems EKA ekrano maketui.
- **Operacijos ekranas** – operacija gali būti paleidžiama naudojant EKA mygtukynus, sukonfigūruotus EKA operacijos ekrane.
- **Darbo pradžios ekranas** – operacija gali būti paleidžiama naudojant EKA mygtukynus, sukonfigūruotus EKA darbo pradžios ekrane.

> [!NOTE]
> Toliau išvardytos operacijos taikomos naujausiai „Commerce“ versijai. Kai kurios operacijos galėjo būti pakeistos arba gali būti nepasiekiamos ankstesnėse versijose.

| ID | Operacija | aprašymas | Mygtukynas | Operacijos ekranas | Darbo pradžios ekranas | Pasiekiama neprisijungus | Būdingos vietai |
|----|-----------|-------------|-------------|--------------------|----------------|-------------------|-----------------|
| 707 | Aktyvinti įrenginį | Dabartinį įrenginį suaktyvinkite leisdami patvirtintam vartotojui pateikti prisijungimo informaciją ir priskirti įrenginį bei aparato ID. | Ne | Ne | Ne | Ne | Ne |
| 134 | Įtraukti priskyrimą | Pridėkite iš anksto pasirinktą priskyrimą operacijai. Pasirinkite priskyrimą puslapyje **Mygtuko ypatybės**. | Taip | Taip | Ne | Taip | Ne |
| 135 | Įtraukti priskyrimą iš sąrašo | Įtraukite priskyrimą į operaciją pasirinkdami ją iš sąrašo. | Taip | Taip | Taip | Taip | Ne |
| 137 | Kliento priskyrimo įtraukimas | Įtraukite kliento priskyrimą puslapyje **Kliento informacija**. | Ne | Ne | Ne | Taip | Ne |
| 138 | Kliento priskyrimo pašalinimas | Pašalinkite priskyrimą puslapyje **Kliento informacija**. | Ne | Ne | Ne | Taip | Ne |
| 643 | Įtraukti kupono kodą | Įtraukite kuponą įvesdami jo kodą į EKA. | Taip | Taip | Ne | Taip | Ne |
| 141 | Įtraukti antraštės išlaidas | Įtraukti papildomą mokestį į užsakymo antraštę. | Taip | Taip | Ne | Ne| Ne |
| 141 | Įtraukti eilutės išlaidas | Įtraukti papildomą mokestį į pasirinktą pardavimo eilutę. | Taip | Taip | Ne | Ne| Ne |
| 117 | Įtraukti lojalumo kortelę | Paraginkite vartotoją įvesti lojalumo kortelės numerį, kuris bus įtrauktas į esamą operaciją. | Taip | Taip | Ne | Taip | Ne |
| 136 | Įtraukti serijos numerį | Ši operacija leidžia vartotojui nurodyti tuo metu pasirinkto produkto serijos numerį. | Taip | Taip | Ne | Taip | Ne |
| 1214 | Pridėti siuntimo adresą | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Ne |
| 519 | Įtraukti į dovanų kortelę | Įtraukti pinigus į nurodytą dovanų kortelę. | Taip | Taip | Ne | Ne | Ne |
| 6000 | Leisti praleisti fiskalinę registraciją | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Taip |
| 1212 | Inkasavimas | Įrašyti į banką siunčiamą pinigų sumą ir kitą informaciją, pvz., banko maišelio numerį. | Taip | Taip | Taip | Taip | Ne |
| 923 | Banko sumų tikrinimas | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Taip |
| 915 | Tuščia operacija | Operacija atliekama spustelėjant tinkinamą mygtuką, kurį programinės įrangos kūrėjas gali programiškai pakeisti, pritaikydamas bet kuriai verslui būtinai konkrečiai operacijai atlikti. | Taip | Taip | Taip | Taip | Ne |
| 1053 | Uždaryti pamainą anonimiškai | Esamą pamainą nustatykite į uždaryta anonimiškai ir atjunkite vartotoją. Anonimiškai uždarius pamainą, negalima atlikti papildomų operacijų, bet galima atlikti stalčių operacijas, pvz., pašalinti mokėjimo priemonę mokėjimo priemonių deklaravimą. | Taip | Taip | Taip | Ne | Ne |
| 310 | Skaičiuoti sumą | Kai nuolaidos skaičiavimas vėluoja, ši operacija inicijuoja dabartinės operacijos apskaičiavimą. | Taip | Taip | Ne | Taip | Ne |
| 642 | Tiekti visus produktus | Visų eilučių pristatymo režimą nustatykite į **Carryout**. | Taip | Taip | Ne | Taip\* | Ne |
| 641 | Tiekti pasirinktus produktus | Pasirinktų eilučių pristatymo režimą nustatykite į **Carryout**. | Taip | Taip | Ne | Taip\* | Ne |
| 647 | Keisti pristatymo režimą | Keisti pristatymo būdą iš anksto sukonfigūruotose siuntimo pardavimo eilutėse. | Taip | Taip | Ne | Ne| Ne |
| 1215 | Keisti slaptažodį | Ši operacija leidžia EKA vartotojams keisti jų slaptažodį. | Taip | Taip | Taip | Ne | Ne |
| 123 | Keisti matavimo vienetą | Pakeiskite pasirinktos eilutės elemento matavimo vienetą. | Taip | Taip | Ne | Taip | Ne |
| 639 | Išvalyti numatytąjį operacijos pardavimo atstovą | Pašalinkite komisinių pardavimo grupę (pardavimo ats.) iš operacijos. | Taip | Taip | Ne | Taip | Ne |
| 106 | Valyti kiekį | Kiekį tuo metu pasirinktoje eilutėje iš naujo nustatykite į **1**. | Taip | Taip | Ne | Taip | Ne |
| 640 | Išvalyti pardavimo atstovą eilutėje | Pašalinkite komisinių pardavimo grupę (pardavimo ats.) iš tuo metu pasirinktos eilutės. | Taip | Taip | Ne | Taip | Ne |
| 121 | Išvalyti pardavėją | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Ne |
| 1055 | Uždaryti pamainą | Uždarykite dabartinę pamainą, atsispausdinkite Z ataskaitą ir atjunkite vartotoją iš sistemos. | Taip | Taip | Taip | Ne | Ne |
| 139 | Užbaigti operaciją | Ragina vartotojus pasirinkti mokėjimo būdą | Taip | Taip | Ne | Taip | Ne |
| 925 | Kopijuoti banko čekį | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Taip |
| 620 | Kurti kliento užsakymą | Konvertuokite EKA operaciją kliento užsakymui. | Taip | Taip | Ne | Taip\* | Ne |
| 621 | Kurti pasiūlymą | Konvertuokite EKA operaciją pardavimo pasiūlymui. | Taip | Taip | Ne | Taip\* | Ne |
| 636 | Sukurkite mažmeninės prekybos operaciją | Kurti standartinę pardavimo operaciją, kai numatytoji EKA – kurti klientų užsakymus. | Taip | Taip | Ne | Taip | Ne |
| 600 | Klientas | Įtraukite į operaciją konkretų klientą. | Ne | Ne | Ne | Taip | Ne |
| 1100 | Kliento kodo depozitas | Atlikti mokėjimą į kliento sąskaitą. | Taip | Taip | Taip | Taip | Taip |
| 612 | Kliento įtraukimas | Kurti naują kliento įrašą. | Taip | Taip | Taip | Taip+ | Ne |
| 603 | Kliento informacijos išvalymas | Pašalinkite klientą iš esamos operacijos. | Taip | Taip | Ne | Taip | Ne |
| 602 | Kliento ieška | Ieškoti kliento įrašo EKA naršant kliento ieškos puslapyje. | Taip | Taip | Taip | Taip | Ne |
| 609 | Kliento operacijos | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Ne |
| 917 | Duomenų bazės ryšio būsena | Peržiūrėti dabartinius ryšio parametrus ir perjungti tinklo ir autonominius režimus. | Taip | Taip | Taip | Taip | Ne |
| 1200 | Deklaruoti pradinę sumą | Dienos arba pamainos pradžioje deklaruoti kasos stalčiuje esančią sumą. | Taip | Taip | Taip | Taip | Ne |
| 132 | Depozito perrašymas | Perrašykite numatytąjį kliento užsakymų depozitą. | Taip | Taip | Ne | Taip\* | Ne |
| 913 | Išjungti kūrimo režimą | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Ne |
| 912 | Įjungti kūrimo režimą | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Ne |
| 1217 | Išskaidyti rinkinius | Išskaidykite rinkinį į komponentų produktus. | Taip | Taip | Taip | Taip | Ne |
| 624 | Rodyti grąžinimo sumas | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Taip |
| 513 | Rodyti bendrąją sumą | Rodyti operacijos balansą kliento ekrane. | Taip | Taip | Taip | Taip | Ne |
| 623 | Redaguoti klientą | Redaguoti dabartinio kliento informaciją. | Taip | Taip | Ne | Ne | Ne |
| 614 | Redaguoti kliento užsakymą | Atšaukite pasirinktą užsakymą, kad jį būtų galima modifikuoti EKA. | Ne | Ne | Ne | Ne | Ne |
| 615 | Redaguoti pasiūlymą | Atšaukite pasirinktą pasiūlymą, kad jį būtų galima modifikuoti EKA. | Ne | Ne | Ne | Ne | Ne |
| 518 | Išlaidų sąskaitos | Įrašyti pinigus, paimtus iš kasos stalčiaus kaip atsitiktines išlaidas. | Taip | Taip | Taip | Taip | Ne |
| 919 | Išplėstinė registracija | Priskirkite arba pašalinkite teisę prisijungti nuskaitydami brūkšninį kodą arba perbraukdami kortelę. | Taip | Taip | Taip | Taip | Ne |
| 1201 | Nefiksuotas įrašas | Į dabartinį stalčių arba pamainą įtraukti papildomų pinigų. | Taip | Taip | Taip | Taip | Ne |
| 1218 | Priversti atrakinti išorinį elementą | Sistema naudoja šią operaciją aparato viduje esantiems EKA periferiniams įrenginiams atrakinti. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Ne |
| 520 | Dovanų kortelės likutis | Rodomas dovanų kortelės likutis. | Taip | Taip | Ne | Ne | Ne |
| 708 | Išjungti įrenginį | Išjunkite dabartinį įrenginį, kad jo nebūtų galima naudoti kaip EKA registro. | Ne | Ne | Ne | Ne | Ne |
| 804 | Gaunamos operacijos | Prieiga prie gaunamų parduotuvės atsargų valdymo funkcijų. | Taip | Ne | Taip | Ne| Ne |
| 517 | Pajamų sąskaitos | Įrašyti pinigus, įdėtus į kasos stalčių dėl bet kurios priežasties, išskyrus pirkimą. | Taip | Taip | Taip | Taip | Ne |
| 801 | Atsargų peržvalga | Ieškokite pasiekiamo, užsakyme pateikto ir prieinamų atsargų (ATP) kiekio, esančio dabartinėje parduotuvėje ir kitose pasiekiamose vietose. | Taip | Taip | Taip | Ne | Ne |
| 122 | SF komentaras | Įveskite komentarą apie dabartinę operaciją. | Taip | Taip | Ne | Taip | Ne |
| 511 | Išduoti kredito pažymą | Išduokite kredito pažymą, kad vietoje grąžinimo pateiktumėte kvitą. | Taip | Taip | Ne | Ne | Ne |
| 512 | Išduoti dovanų kortelę | Išduokite naują nurodytam kiekiui skirtą dovanų kortelę. | Taip | Taip | Ne | Ne | Ne |
| 625 | Išduoti lojalumo kortelę | Išduokite lojalumo kortelę klientui, kad klientas galėtų dalyvauti parduotuvės lojalumo programoje. | Taip | Taip | Taip | Ne | Ne |
| 300 | Eilutės nuolaidos suma | Įvesti operacijos eilutės prekės nuolaidos sumą. Ši operacija atliekama tik su prekėmis, kurioms taikoma nuolaida, ir tik nurodytos nuolaidos ribose. | Taip | Taip | Ne | Taip | Ne |
| 301 | Eilutės nuolaida procentais | Įvesti operacijos eilutės prekės nuolaidos procentą. Ši operacija atliekama tik su prekėmis, kurioms taikoma nuolaida, ir tik nurodytos nuolaidos ribose. | Taip | Taip | Ne | Taip | Ne |
| 703 | Užrakto registras | Užrakinkite dabartinį aparatą, kad juo nebūtų galima naudotis, bet neatjunkite dabartinio vartotojo. | Ne | Ne | Ne | Taip | Ne |
| 701 | Išsiregistruoti | Atjunkite dabartį vartotoją iš aparato. | Taip | Taip | Taip | Taip | Ne |
| 521 | Lojalumo kortelės taškų balansas | Rodomas nurodytos lojalumo kortelės taškų balansas. | Taip | Taip | Ne | Ne | Ne |
| 142 | Valdyti mokesčius | Peržiūrėti ir valdyti operacijai taikomus papildomus mokesčius. | Taip | Taip | Ne | Ne| Ne |
| 918 | Valdyti pamainas | Rodomas aktyvių, sustabdytų ir anonimiškai uždarytų pamainų sąrašas. | Taip | Taip | Taip | Ne | Ne |
| 914 | Minimizuoti EKA langą | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Ne |
| 1000 | Atidaryti stalčių | Atlikite operaciją „Neparduodama“ ir atidarykite tuo metu pasirinktą kasos stalčių. | Taip | Taip | Taip | Taip | Ne |
| 928 | Užsakymo įvykdymas | Ši operacija suteikia galimybę vartotojui paimti, supakuoti, siųsti arba atšaukti parduotuvėje paimtinus užsakymus. | Taip | Taip | Taip | Ne | Ne |
| 805 | Siuntimo operacija | Naudoti siunčiamų perkėlimo užsakymų siuntų valdymo funkcijas. | Taip | Ne | Taip | Ne| Ne |
| 129 | Nepaisyti eilutės produkto mokesčio | Perrašykite pasirinktoje eilutėje pateiktos prekės mokestį ir naudokite kitą nurodytą mokestį. | Taip | Taip | Ne | Taip | Ne |
| 130 | Nepaisyti eilutės produkto mokesčio iš sąrašo | Perrašykite pasirinktoje eilutėje pateiktos prekės mokestį ir naudokite mokestį, kurį vartotojas pasirenka iš sąrašo. | Taip | Taip | Ne | Taip | Ne |
| 127 | Perrašyti operacijos mokestį | Perrašykite operacijos mokestį ir naudoti kitą nurodytą mokestį. | Taip | Taip | Ne | Taip | Ne |
| 128 | Perrašyti operacijos mokestį iš sąrašo | Perrašykite operacijos mokestį ir naudokite mokestį, kurį vartotojas pasirenka iš sąrašo. | Taip | Taip | Ne | Taip | Ne |
| 131 | Važtaraštis | Sukurkite pasirinkto užsakymo važtaraštį. | Ne | Ne | Ne | Ne | Ne |
| 710 | Susieti aparatūros stotį | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Ne |
| 201 | Mokėti kortele | Patvirtinkite mokėjimą kortele, pvz., kredito arba debeto kortele. | Taip | Taip | Ne | Taip | Ne |
| 200 | Mokėti grynaisiais | Priimti mokėjimą grynaisiais pinigais. | Taip | Taip | Ne | Taip | Ne |
| 206 | Greitas atsiskaitymas grynaisiais | Užbaikite operaciją vienu palietimu ir patvirtinkite sumą grynaisiais pinigais (tikslus keitimas). | Taip | Taip | Ne | Taip | Ne |
| 204 | Mokėti čekiu | Priimti mokėjimą čekiu. | Taip | Taip | Ne | Taip | Ne |
| 213 | Mokėti kredito pažyma | Patvirtinkite parduotuvės išduotą kredito pažymą (kvitą). | Taip | Taip | Ne | Ne | Ne |
| 203 | Mokėti valiuta | Priima mokėjimą įvairiomis valiutomis. | Taip | Taip | Ne | Taip | Ne |
| 202 | Mokėti kliento kodas | Mokestį už operaciją išskaičiuokite iš kliento sąskaitos. Šis mokėjimo būdo netinka naudoti kliento užsakymo depozitams. | Taip | Taip | Ne | Ne | Ne |
| 214 | Mokėti dovanų kortele | Patvirtinkite parduotuvės išduotą dovanų kortelę. | Taip | Taip | Ne | Ne | Ne |
| 207 | Mokėti lojalumo kortele | Patvirtinkite mokėjimą lojalumo kortele ir panaudokite sukauptus taškus tam skirtiems produktams. | Taip | Taip | Ne | Ne | Ne |
| 634 | Mokėjimų retrospektyva | Rodoma kliento esamo užsakymo mokėjimo retrospektyva. | Taip | Taip | Ne | Ne | Ne |
| 803 | Paėmimas ir gavimas | Atidarykite puslapį **Paėmimas ir gavimas**, kuriame galite pasirinkti paimti parduotuvėje esančius ar priimti į ją gaunamus užsakymus. | Taip | Taip | Taip | Ne | Ne |
| 632 | Paimti visus produktus | Nustatykite visų eilučių įvykdymo būdą į **Paėmimas parduotuvėje**. | Taip | Taip | Ne | Taip\* | Ne |
| 631 | Paimti pasirinktus produktus | Nustatykite pasirinktų eilučių įvykdymo būdą į **Paėmimas parduotuvėje**. | Taip | Taip | Ne | Taip\* | Ne |
| 400 | Laikinasis meniu | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Ne |
| 101 | Kainos tikrinimas | Ši operacija leidžia vartotojui ieškoti nurodyto produkto kainos. | Taip | Taip | Taip | Taip | Ne |
| 104 | Kainos perrašymas | Perrašykite produkto kainą, jei produkte nustatyta leisti perrašyti kainas. | Taip | Taip | Ne | Taip | Ne |
| 1058 | Spausdinti fiskalinį X | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Taip |
| 1059 | Spausdinti fiskalinį Z | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Taip |
| 927 | Spausdinti prekės etiketę | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Ne |
| 926 | Spausdinti lentynos etiketę | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Ne |
| 1056 | Spausdinti X | Spausdinkite dabartinės pamainos X ataskaitą. | Taip | Taip | Taip | Ne | Ne |
| 103 | Produkto komentaras | Įtraukti pasirinktos operacijos eilutės prekės aprašą. | Taip | Taip | Ne | Taip | Ne |
| 100 | Produkto pardavimas | Įtraukite nurodytą produktą į operaciją. | Taip | Taip | Taip | Taip | Ne |
| 108 | Produktų paieška | Ieškokite produkto pereidami į EKA produktų ieškos puslapį. | Taip | Taip | Taip | Taip | Ne |
| 633 | Pasiūlymo galiojimo data | Peržiūrėkite arba modifikuokite pardavimo pasiūlymo galiojimo datą. | Taip | Taip | Ne | Taip\* | Ne |
| 627 | Perskaičiuoti | Perskaičiuokite visas kliento užsakymo eilutes ir mokesčius, kuriems taikoma dabartinė konfigūracija. | Taip | Taip | Ne | Taip\* | Ne |
| 143 | Perskaičiuoti mokesčius | Perskaičiuoti užsakymui taikomas automatines išlaidas. | Taip | Taip | Ne | Ne| Ne |
| 515 | Atšaukti užsakymą | Ieškoti klientų užsakymų ir pardavimo pasiūlymų ir jų atšaukti. | Taip | Taip | Taip | Ne | Ne |
| 504 | Atšaukti operaciją | Atšaukti anksčiau sustabdytą operaciją iš dabartinės parduotuvės. | Taip | Taip | Ne | Taip‡ | Ne |
| 305 | Panaudoti lojalumo taškus | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Taip |
| 635 | Grąžinti siuntimo išlaidas | Grąž grąž inkite siuntimo išlaidas atšauktame užsakyme. | Ne | Ne | Ne | Ne | Ne |
| 644 | Pašalinti kupono kodą | Paraginkite vartotoją pašalinti kuponus juos pasirenkant iš kuponų, susietų su operacija, sąrašo. | Taip | Taip | Ne | Taip | Ne |
| 1057 | Perspausdinti Z | Iš naujo atsispausdinkite ankstesnės arba pasirinktos pamainos Z ataskaitą. | Taip | Taip | Taip | Ne | Ne |
| 1216 | Įveskite naują slaptažodį | Ši operacija leidžia vartotojui, turinčiam slaptažodžio nustatymo iš naujo teisę, iš naujo nustatyti kito darbuotojo slaptažodį naudojant laikinąjį slaptažodį. | Taip | Taip | Taip | Ne | Ne |
| 1219 | URL atidarymas EKA | Atidarykite administratoriaus sukonfigūruotą URL EKA. | Taip | Taip | Taip | Taip | Ne |
| 109 | Grąžinti produktą | Atlikti konkrečių produktų grąžinimo operaciją. Kitas nuskaitytas produktas rodomas kaip grąžintas produktas, kurio kiekis ir kaina yra neigiami. | Taip | Taip | Ne | Taip | Ne |
| 114 | Grąžinimo operacija | Atšaukite ankstesnę operaciją pagal kvito numerį, kad grąžintumėte kelis arba visus produktus. | Taip | Taip | Taip | Taip§ | Ne |
| 1211 | Pinigų įnešimas į įmonės kasą | Įnešti pinigus į įmonės kasą, perkeldamas juos iš kasos aparato į seifą. | Taip | Taip | Taip | Taip | Ne |
| 516 | Pardavimo sąskaita faktūra | Ši operacija leidžia vartotojui atlikti mokėjimus pagal pasirinktą pardavimo sąskaitą faktūrą. | Taip | Taip | Ne | Ne | Ne |
| 502 | Pardavėjas | **EKA** nustatykite kliento užsakymų pardavimo užsakymo pardavimo takerę. | Taip | Taip | Ne | Taip\* | Ne |
| 2000 | Grafiko valdymas | Ši operacija dar nepalaikoma. | Taip | Taip | Taip | Ne | Ne |
| 2001 | Grafiko užklausos | Ši operacija dar nepalaikoma. | Taip | Taip | Taip | Ne | Ne |
| 622 | Ieškoti užsakymų | Ši operacija leidžia vartotojams iš anksto sukonfigūruoti EKA mygtukus, kad būtų galima ieškoti pagal prekę, klientą arba kategoriją. | Taip | Taip | Taip | Taip | Ne |
| 1213 | Ieškoti siuntimo adreso | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Ne |
| 709 | Pasirinkti „hardware station“ | Pasirinkite aparatūros stotį iš galimų aparatūros stočių sąrašo. | Taip | Taip | Taip | Taip | Ne |
| 637 | Nustatyti numatytąjį operacijos pardavimo atstovą | Pasirinkti vieną iš tinkamų komisinių pardavimo grupių (pard. ats.) kaip numatytąjį eilučių, kurios bus pridėtos vėliau, pardavimo atstovų. | Taip | Taip | Ne | Taip | Ne |
| 105 | Nustatyti kiekį | Pakeisti operacijos eilutės prekės kiekį. | Taip | Taip | Ne | Taip | Ne |
| 638 | Nustatyti pardavimo atstovą eilutėje | Pasirinkti vieną iš dabar pasirinktos eilutės tinkamų komisinių pardavimo grupių (pard. ats.) | Taip | Taip | Ne | Taip | Ne |
| 630 | Siųsti visus produktus | Įvykdymo režimą visoms eilutėms nustatykite į **Siuntimas**. | Taip | Taip | Ne | Taip\* | Ne |
| 629 | Siųsti pasirinktus produktus | Pasirinktų eilučių įvykdymo režimą nustatykite į **Siuntimas**. | Taip | Taip | Ne | Taip\* | Ne |
| 115 | Rodyti žurnalą | Rodomas parduotuvės žurnalas. Galite peržiūrėti operacijas, perspausdinti kvitus ir dovanų kvitus ir atšaukti grąžinimą. | Taip | Taip | Taip | Taip\*\* | Ne |
| 802 | Inventorizacija | Kurti arba modifikuoti faktinių atsargų arba ciklų skaičiavimo inventorizacijos žurnalus. | Taip | Taip | Taip | Ne | Ne |
| 401 | Submeniu | Ši operacija perkelia vartotoją į kitą susietą mygtukyną. | Taip | Taip | Taip | Taip | Ne |
| 1054 | Sustabdyti pamainą | Sustabdykite esamą pamainą, kad esamame aparate būtų galima suaktyvinti naują arba kitą pamainą. | Taip | Taip | Taip | Ne | Ne |
| 503 | Sustabdyti operaciją | Sustabdykite esamą pardavimo operaciją, kad vėliau parduotuvėje ją būtų galima atšaukti. | Taip | Taip | Ne | Taip‡ | Ne |
| 1004 | Užduočių įrašymo priemonė | Atidarykite užduočių įrašymo priemonę, kad galėtumėte įrašyti EKA procedūros veiksmus. | Ne | Ne | Ne | Taip | Ne |
| 1052 | Mokėjimo priemonių deklaravimas | Nurodykite kiekvieno apskaičiuotos mokėjimo būdo pinigų sumą stalčiuje. | Taip | Taip | Taip | Taip | Ne |
| 1210 | Mokėjimo priemonės šalinimas | Pašalinti pinigus iš dabartinio stalčiaus arba pamainos. | Taip | Taip | Taip | Taip | Ne |
| 920 | Laikrodis | Darbo pamainų ir pertraukų kontrolinis paspauskite klavišą. | Taip | Taip | Taip | Ne | Ne |
| 302 | Bendroji nuolaidos suma | Įveskite operacijos nuolaidos sumą. Ši operacija naudojama tik su prekėmis, kurioms taikoma nuolaida, ir tik nurodytos nuolaidos ribose. | Taip | Taip | Ne | Taip | Ne |
| 303 | Bendroji nuolaidos suma procentais | Įveskite operacijos nuolaidos procentą. Ši operacija naudojama tik su prekėmis, kurioms taikoma nuolaida, ir tik nurodytos nuolaidos ribose. | Taip | Taip | Ne | Taip | Ne |
| 501 | Operacijos komentaras | Įtraukite komentarą į esamą operaciją. | Taip | Taip | Ne | Taip | Ne |
| 922 | Peržiūrėti produkto informaciją | Atidarykite tuo metu pasirinkto eilutės elemento produkto informacijos puslapį. | Taip | Taip | Ne | Taip | Ne |
| 1003 | Ataskaitų peržiūra | Rodomos dabartiniam vartotojui sukonfigūruotos ataskaitos. | Taip | Taip | Taip | Ne | Ne |
| 921 | Peržiūrėti laikrodžio įrašus | Rodomi visų parduotuvės darbuotojų laikrodžių įrašai. | Taip | Taip | Taip | Ne | Ne |
| 211 | Anuliuoti mokėjimą | Anuliuokite tuo metu pasirinktą operacijos mokėjimo eilutę. | Taip | Taip | Ne | Taip | Ne |
| 102 | Anuliuoti produktą | Anuliuokite tuo metu pasirinktą operacijos eilutės elementą. | Taip | Taip | Ne | Taip | Ne |
| 500 | Anuliuoti operaciją | Anuliuokite dabartinę operaciją. | Taip | Taip | Ne | Taip | Ne |
| 916 | „Windows“ darbo eigos programavimo platforma | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Ne |
| 924 | Banko kortelių X ataskaita | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Taip |
| 311 | Pašalinkite sistemos nuolaidas iš perlaidų | Pašalinkite visas sistemos taikomas nuolaidas, įskaitant kuponu pagrįstas nuolaidas iš perlaidos. Tai nepašalina rankinių nuolaidų. | Taip | Taip | Taip | Taip | Ne |
| 312 | Pakartotinio taikymo sistemos nuolaidos | Pakartotinio taikymo sistemos nuolaidos perlaidoje, jei jos yra pašalintos naudojant **Pašalinti sistemos nuolaidas iš perlaidos** operacijos. | Taip | Taip | Taip | Taip | Ne |

\* Ši operacija pasiekiama tik veikiant autonominiam režimui, kai sukuriamas kliento užsakymas arba pardavimo pasiūlymas, ir tik tada, jei EKA funkcijų profilyje sukonfigūruotas kliento užsakymų ir pardavimo pasiūlymų kūrimas. Šios operacijos atlikti negalima, kai užsakymai kuriami naudojant „Real-time Service“ arba kai užsakymai yra atšaukiami ar redaguojami.

† Operaciją veikiant autonominiam režimui galima atlikti tik tada, kai EKA funkcijų profilyje sukonfigūruota leisti kurti klientus autonominiu režimu.

‡ Kai EKA veikia autonominiu režimu, sustabdytas operacijas galima atšaukti tik apsilankius esamo aparato autonominėje duomenų bazėje. Vartotojai negali sustabdyti ir atšaukti operacijų visuose aparatuose.

§ Kai EKA veikia autonominiu režimu, galima atšaukti tik esamoje autonominėje duomenų bazėje esančias grąžinimo operacijas.

\*\* Kai EKA veikia autonominiu režimu, žurnale rodomos tik esamame autonominiame duomenų bazės kanale esančios operacijos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
