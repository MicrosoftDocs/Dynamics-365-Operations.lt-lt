---
title: EKA operacijos, prisijungus ir neprisijungus prie interneto
description: "Šioje temoje pateikiama informacija apie elektroninio kasos aparato (EKA) veikimą „Microsoft Dynamics 365 for Retail“. Joje nurodoma, kur programoje galima iškviesti operacijas ir ar jos pasiekiamos neprisijungus."
author: jblucher
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-09-27
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 8a24f8adc4f7886a1f942d83f7a4eb12e7034fcd
ms.openlocfilehash: d8cf283321b81c377498cd449b098f8fac1fe01f
ms.contentlocale: lt-lt
ms.lasthandoff: 03/22/2018

---

# <a name="pos-operations-online-and-offline"></a>EKA operacijos, prisijungus ir neprisijungus prie interneto

[!include [banner](includes/banner.md)]

Dauguma vartotojo elektroniniame kasos aparate (EKA) atliekamų veiksmų laikomi operacijomis. Operacijos sukonfigūruojamos ir valdomos „Microsoft Dynamics 365 for Retail“ tarnybiniame biure. Į EKA mygtukyną galima įtraukti daug operacijų. Tada vartotojai, norėdami iškviesti operacijas ir atlikti jų teikiama funkciją, gali pasirinkti mygtukus. Kitos operacijos yra pagrindinės EKA programos dalis ir yra iškviečiamos naudojant ekrano mygtukus arba kaip kitos darbo eigos ar procesų dalis.

Šioje lentelėje pateikiama informacija apie operacijas, pasiekiamas „Retail Modern POS“ ir „Retail“ skirtoje „Cloud POS for Dynamics 365“. Joje taip pat nurodoma, kur programoje galima iškviesti operacijas ir ar jos pasiekiamos EKA veikiant autonominiu režimu.

Kai kurios operacijos šiuo metu nepasiekiamos „Retail Modern POS“ arba „Retail“ skirtoje „Cloud POS for Dynamics 365“. Kai kurios iš šių operacijų yra būdingos vietai ir joms reikalingi papildomi plėtiniai ir konfigūracija. Kitos operacijos yra „Microsoft Dynamics AX 2012“ operacijos, kurios šiuo metu nepalaikomos.

Toliau pateiktuose stulpeliuose nurodoma, kur galima iškviesti operacijas.

- **Mygtukynas** – operacija gali būti priskirta EKA mygtukynams, priklausantiems EKA ekrano maketui.
- **Operacijos ekranas** – operacija gali būti paleidžiama naudojant EKA mygtukynus, sukonfigūruotus EKA operacijos ekrane.
- **Darbo pradžios ekranas** – operacija gali būti paleidžiama naudojant EKA mygtukynus, sukonfigūruotus EKA darbo pradžios ekrane.

Pastaba. Toliau išvardytos operacijos taikomos naujausiai „Dynamics 365 for Retail‟ versijai. Kai kurios operacijos galėjo būti pakeistos arba gali būti nepasiekiamos ankstesnėse versijose.

| ID | Operacija | aprašymas | Mygtukynas | Operacijos ekranas | Darbo pradžios ekranas | Pasiekiama neprisijungus | Būdingos vietai |
|----|-----------|-------------|-------------|--------------------|----------------|-------------------|-----------------|
| 707 | Aktyvinti įrenginį | Dabartinį įrenginį suaktyvinkite leisdami patvirtintam vartotojui pateikti prisijungimo informaciją ir priskirti įrenginį bei aparato ID. | Nr. | Nr. | Nr. | Nr. | Nr. |
| 134 | Įtraukti priskyrimą | Pridėkite iš anksto pasirinktą priskyrimą operacijai. Pasirinkite priskyrimą puslapyje **Mygtuko ypatybės**. | Taip | Taip | Nr. | Taip | Nr. |
| 135 | Įtraukti priskyrimą iš sąrašo | Įtraukite priskyrimą į operaciją pasirinkdami ją iš sąrašo. | Taip | Taip | Taip | Taip | Nr. |
| 643 | Įtraukti kupono kodą | Įtraukite kuponą įvesdami jo kodą į EKA. | Taip | Taip | Nr. | Taip | Nr. |
| 117 | Įtraukti lojalumo kortelę | Paraginkite vartotoją įvesti lojalumo kortelės numerį, kuris bus įtrauktas į esamą operaciją. | Taip | Taip | Nr. | Taip | Nr. |
| 136 | Įtraukti serijos numerį | Ši operacija leidžia vartotojui nurodyti tuo metu pasirinkto produkto serijos numerį. | Taip | Taip | Nr. | Taip | Nr. |
| 1214 | Pridėti siuntimo adresą | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Nr. |
| 519 | Įtraukti į dovanų kortelę | Įtraukti pinigus į nurodytą dovanų kortelę. | Taip | Taip | Nr. | Nr. | Nr. |
| 6000 | Leisti praleisti fiskalinę registraciją | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Taip |
| 1212 | Inkasavimas | Įrašyti į banką siunčiamą pinigų sumą ir kitą informaciją, pvz., banko maišelio numerį. | Taip | Taip | Taip | Taip | Nr. |
| 923 | Banko sumų tikrinimas | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Taip |
| 915 | Tuščia operacija | Operacija atliekama spustelėjant tinkinamą mygtuką, kurį programinės įrangos kūrėjas gali programiškai pakeisti, pritaikydamas bet kuriai verslui būtinai konkrečiai operacijai atlikti. | Taip | Taip | Taip | Taip | Nr. |
| 1053 | Uždaryti pamainą anonimiškai | Esamą pamainą nustatykite į uždaryta anonimiškai ir atjunkite vartotoją. Anonimiškai uždarius pamainą, negalima atlikti papildomų operacijų, bet galima atlikti stalčių operacijas, pvz., pašalinti mokėjimo priemonę mokėjimo priemonių deklaravimą. | Taip | Taip | Taip | Nr. | Nr. |
| 310 | Skaičiuoti sumą | Kai nuolaidos skaičiavimas vėluoja, ši operacija inicijuoja dabartinės operacijos apskaičiavimą. | Taip | Taip | Nr. | Taip | Nr. |
| 642 | Tiekti visus produktus | Visų eilučių pristatymo režimą nustatykite į **Carryout**. | Taip | Taip | Nr. | Taip\* | Nr. |
| 641 | Tiekti pasirinktus produktus | Pasirinktų eilučių pristatymo režimą nustatykite į **Carryout**. | Taip | Taip | Nr. | Taip\* | Nr. |
| 1215 | Keisti slaptažodį | Ši operacija leidžia EKA vartotojui keisti savo slaptažodį. | Taip | Taip | Taip | Nr. | Nr. |
| 123 | Keisti matavimo vienetą | Pakeiskite pasirinktos eilutės elemento matavimo vienetą. | Taip | Taip | Nr. | Taip | Nr. |
| 639 | Išvalyti numatytąjį operacijos pardavimo atstovą | Pašalinkite komisinių pardavimo grupę (pardavimo ats.) iš operacijos. | Taip | Taip | Nr. | Taip | Nr. |
| 106 | Valyti kiekį | Kiekį tuo metu pasirinktoje eilutėje iš naujo nustatykite į **1**. | Taip | Taip | Nr. | Taip | Nr. |
| 640 | Išvalyti pardavimo atstovą eilutėje | Pašalinkite komisinių pardavimo grupę (pardavimo ats.) iš tuo metu pasirinktos eilutės. | Taip | Taip | Nr. | Taip | Nr. |
| 121 | Išvalyti pardavėją | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Nr. |
| 1055 | Uždaryti pamainą | Uždarykite dabartinę pamainą, atsispausdinkite Z ataskaitą ir atjunkite vartotoją iš sistemos. | Taip | Taip | Taip | Nr. | Nr. |
| 925 | Kopijuoti banko čekį | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Taip |
| 620 | Kurti kliento užsakymą | Konvertuokite EKA operaciją kliento užsakymui. | Taip | Taip | Nr. | Taip\* | Nr. |
| 621 | Kurti pasiūlymą | Konvertuokite EKA operaciją pardavimo pasiūlymui. | Taip | Taip | Nr. | Taip\* | Nr. |
| 636 | Sukurkite mažmeninės prekybos operaciją | Ši operacija leidžia vartotojui sukurti standartinę pardavimo operaciją, kai numatytoji EKA veiksena naudojama kliento užsakymams kurti. | Taip | Taip | Nr. | Taip | Nr. |
| 600 | Klientas | Įtraukite į operaciją konkretų klientą. | Nr. | Nr. | Nr. | Taip | Nr. |
| 1100 | Kliento kodo depozitas | Atlikti mokėjimą į kliento sąskaitą. | Taip | Taip | Taip | Taip | Taip |
| 612 | Kliento įtraukimas | Ši operacija leidžia vartotojui sukurti naują kliento įrašą. | Taip | Taip | Taip | Taip+ | Nr. |
| 603 | Kliento informacijos išvalymas | Pašalinkite klientą iš esamos operacijos. | Taip | Taip | Nr. | Taip | Nr. |
| 602 | Kliento ieška | Ši operacija leidžia vartotojui ieškoti kliento įrašo apsilankius EKA kliento ieškos puslapyje. | Taip | Taip | Taip | Taip | Nr. |
| 609 | Kliento operacijos | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Nr. |
| 917 | Duomenų bazės ryšio būsena | Ši operacija leidžia vartotojui peržiūrėti esamus ryšio parametrus ir iš interneto režimo perjungti autonominį režimą. | Taip | Taip | Taip | Taip | Nr. |
| 1200 | Deklaruoti pradinę sumą | Dienos arba pamainos pradžioje deklaruoti kasos stalčiuje esančią sumą. | Taip | Taip | Taip | Taip | Nr. |
| 132 | Depozito perrašymas | Perrašykite numatytąjį kliento užsakymų depozitą. | Taip | Taip | Nr. | Taip\* | Nr. |
| 913 | Išjungti kūrimo režimą | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Nr. |
| 912 | Įjungti kūrimo režimą | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Nr. |
| 1217 | Išskaidyti rinkinius | Išskaidykite rinkinį į komponentų produktus. | Taip | Taip | Taip | Taip | Nr. |
| 624 | Rodyti grąžinimo sumas | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Taip |
| 513 | Rodyti bendrąją sumą | Rodyti operacijos balansą kliento ekrane. | Taip | Taip | Taip | Taip | Nr. |
| 623 | Redaguoti klientą | Redaguoti dabartinio kliento informaciją. | Taip | Taip | Nr. | Nr. | Nr. |
| 614 | Redaguoti kliento užsakymą | Atšaukite pasirinktą užsakymą, kad jį būtų galima modifikuoti EKA. | Nr. | Nr. | Nr. | Nr. | Nr. |
| 615 | Redaguoti pasiūlymą | Atšaukite pasirinktą pasiūlymą, kad jį būtų galima modifikuoti EKA. | Nr. | Nr. | Nr. | Nr. | Nr. |
| 518 | Išlaidų sąskaitos | Įrašyti pinigus, paimtus iš kasos stalčiaus kaip atsitiktines išlaidas. | Taip | Taip | Taip | Taip | Nr. |
| 919 | Išplėstinė registracija | Priskirkite arba pašalinkite teisę prisijungti nuskaitydami brūkšninį kodą arba perbraukdami kortelę. | Taip | Taip | Taip | Nr. | Nr. |
| 1 201 | Nefiksuotas įrašas | Ši operacija suteikia vartotojui galimybę įtraukti papildomų pinigų į esamą stalčių ar pamainą. | Taip | Taip | Taip | Taip | Nr. |
| 1218 | Priversti atrakinti išorinį elementą | Sistema naudoja šią operaciją aparato viduje esantiems EKA periferiniams įrenginiams atrakinti. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Nr. |
| 520 | Dovanų kortelės likutis | Rodomas dovanų kortelės likutis. | Taip | Taip | Nr. | Nr. | Nr. |
| 708 | Išjungti įrenginį | Išjunkite dabartinį įrenginį, kad jo nebūtų galima naudoti kaip POS aparato. | Nr. | Nr. | Nr. | Nr. | Nr. |
| 517 | Pajamų sąskaitos | Įrašyti pinigus, įdėtus į kasos stalčių dėl bet kurios priežasties, išskyrus pirkimą. | Taip | Taip | Taip | Taip | Nr. |
| 801 | Atsargų peržvalga | Ieškokite pasiekiamo, užsakyme pateikto ir prieinamų atsargų (ATP) kiekio, esančio dabartinėje parduotuvėje ir kitose pasiekiamose vietose. | Taip | Taip | Taip | Nr. | Nr. |
| 122 | SF komentaras | Ši operacija leidžia vartotojui įvesti komentarą apie dabartinę operaciją. | Taip | Taip | Nr. | Taip | Nr. |
| 511 | Išduoti kredito pažymą | Išduokite kredito pažymą, kad vietoje grąžinimo pateiktumėte kvitą. | Taip | Taip | Nr. | Nr. | Nr. |
| 512 | Išduoti dovanų kortelę | Išduokite naują nurodytam kiekiui skirtą dovanų kortelę. | Taip | Taip | Nr. | Nr. | Nr. |
| 625 | Išduoti lojalumo kortelę | Išduokite lojalumo kortelę klientui, kad klientas galėtų dalyvauti parduotuvės lojalumo programoje. | Taip | Taip | Taip | Nr. | Nr. |
| 300 | Eilutės nuolaidos suma | Įvesti operacijos eilutės prekės nuolaidos sumą. Ši operacija atliekama tik su prekėmis, kurioms taikoma nuolaida, ir tik nurodytos nuolaidos ribose. | Taip | Taip | Nr. | Taip | Nr. |
| 301 | Eilutės nuolaida procentais | Įvesti operacijos eilutės prekės nuolaidos procentą. Ši operacija atliekama tik su prekėmis, kurioms taikoma nuolaida, ir tik nurodytos nuolaidos ribose. | Taip | Taip | Nr. | Taip | Nr. |
| 703 | Užrakto registras | Užrakinkite dabartinį aparatą, kad juo nebūtų galima naudotis, bet neatjunkite dabartinio vartotojo. | Nr. | Nr. | Nr. | Taip | Nr. |
| 701 | Išsiregistruoti | Atjunkite dabartį vartotoją iš aparato. | Taip | Taip | Taip | Taip | Nr. |
| 521 | Lojalumo kortelės taškų balansas | Rodomas nurodytos lojalumo kortelės taškų balansas. | Taip | Taip | Nr. | Nr. | Nr. |
| 918 | Valdyti pamainas | Rodomas aktyvių, sustabdytų ir anonimiškai uždarytų pamainų sąrašas. | Taip | Taip | Taip | Nr. | Nr. |
| 914 | Minimizuoti EKA langą | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Nr. |
| 1000 | Atidaryti stalčių | Atlikite operaciją „Neparduodama“ ir atidarykite tuo metu pasirinktą kasos stalčių. | Taip | Taip | Taip | Taip | Nr. |
| 928 | Užsakymo įvykdymas | Ši operacija suteikia galimybę vartotojui paimti, supakuoti, siųsti arba atšaukti parduotuvėje paimtinus užsakymus. | Taip | Taip | Taip | Nr. | Nr. |
| 129 | Nepaisyti eilutės produkto mokesčio | Perrašykite pasirinktoje eilutėje pateiktos prekės mokestį ir naudokite kitą nurodytą mokestį. | Taip | Taip | Nr. | Taip | Nr. |
| 130 | Nepaisyti eilutės produkto mokesčio iš sąrašo | Perrašykite pasirinktoje eilutėje pateiktos prekės mokestį ir naudokite mokestį, kurį vartotojas pasirenka iš sąrašo. | Taip | Taip | Nr. | Taip | Nr. |
| 127 | Perrašyti operacijos mokestį | Perrašykite operacijos mokestį ir naudoti kitą nurodytą mokestį. | Taip | Taip | Nr. | Taip | Nr. |
| 128 | Perrašyti operacijos mokestį iš sąrašo | Perrašykite operacijos mokestį ir naudokite mokestį, kurį vartotojas pasirenka iš sąrašo. | Taip | Taip | Nr. | Taip | Nr. |
| 131 | Važtaraštis | Sukurkite pasirinkto užsakymo važtaraštį. | Nr. | Nr. | Nr. | Nr. | Nr. |
| 710 | Susieti aparatūros stotį | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Nr. |
| 201 | Mokėti kortele | Patvirtinkite mokėjimą kortele, pvz., kredito arba debeto kortele. | Taip | Taip | Nr. | Taip | Nr. |
| 200 | Mokėti grynaisiais | Priimti mokėjimą grynaisiais pinigais. | Taip | Taip | Nr. | Taip | Nr. |
| 206 | Greitas atsiskaitymas grynaisiais | Užbaikite operaciją vienu palietimu ir patvirtinkite sumą grynaisiais pinigais (tikslus keitimas). | Taip | Taip | Nr. | Taip | Nr. |
| 204 | Mokėti čekiu | Priimti mokėjimą čekiu. | Taip | Taip | Nr. | Taip | Nr. |
| 213 | Mokėti kredito pažyma | Patvirtinkite parduotuvės išduotą kredito pažymą (kvitą). | Taip | Taip | Nr. | Nr. | Nr. |
| 203 | Mokėti valiuta | Priima mokėjimą įvairiomis valiutomis. | Taip | Taip | Nr. | Taip | Nr. |
| 202 | Mokėti kliento kodas | Mokestį už operaciją išskaičiuokite iš kliento sąskaitos. Šis mokėjimo būdo netinka naudoti kliento užsakymo depozitams. | Taip | Taip | Nr. | Nr. | Nr. |
| 214 | Mokėti dovanų kortele | Patvirtinkite parduotuvės išduotą dovanų kortelę. | Taip | Taip | Nr. | Nr. | Nr. |
| 207 | Mokėti lojalumo kortele | Patvirtinkite mokėjimą lojalumo kortele ir panaudokite sukauptus taškus tam skirtiems produktams. | Taip | Taip | Nr. | Nr. | Nr. |
| 634 | Mokėjimų retrospektyva | Rodoma kliento esamo užsakymo mokėjimo retrospektyva. | Taip | Taip | Nr. | Nr. | Nr. |
| 803 | Paėmimas ir gavimas | Atidarykite puslapį **Paėmimas ir gavimas**, kuriame galite pasirinkti paimti parduotuvėje esančius ar priimti į ją gaunamus užsakymus. | Taip | Taip | Taip | Nr. | Nr. |
| 632 | Paimti visus produktus | Nustatykite visų eilučių įvykdymo būdą į **Paėmimas parduotuvėje**. | Taip | Taip | Nr. | Taip\* | Nr. |
| 631 | Paimti pasirinktus produktus | Nustatykite pasirinktų eilučių įvykdymo būdą į **Paėmimas parduotuvėje**. | Taip | Taip | Nr. | Taip\* | Nr. |
| 400 | Laikinasis meniu | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Nr. |
| 101 | Kainos tikrinimas | Ši operacija leidžia vartotojui ieškoti nurodyto produkto kainos. | Taip | Taip | Taip | Taip | Nr. |
| 104 | Kainos perrašymas | Perrašykite produkto kainą, jei produkte nustatyta leisti perrašyti kainas. | Taip | Taip | Nr. | Taip | Nr. |
| 1058 | Spausdinti fiskalinį X | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Taip |
| 1059 | Spausdinti fiskalinį Z | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Taip |
| 927 | Spausdinti prekės etiketę | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Nr. |
| 926 | Spausdinti lentynos etiketę | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Nr. |
| 1056 | Spausdinti X | Spausdinkite dabartinės pamainos X ataskaitą. | Taip | Taip | Taip | Nr. | Nr. |
| 103 | Produkto komentaras | Įtraukti pasirinktos operacijos eilutės prekės aprašą. | Taip | Taip | Nr. | Taip | Nr. |
| 100 | Produkto pardavimas | Įtraukite nurodytą produktą į operaciją. | Taip | Taip | Taip | Taip | Nr. |
| 108 | Produktų paieška | Ši operacija leidžia vartotojui ieškoti produkto apsilankius EKA produkto ieškos puslapyje. | Taip | Taip | Taip | Taip | Nr. |
| 633 | Pasiūlymo galiojimo data | Ši operacija leidžia vartotojui peržiūrėti arba modifikuoti pardavimo pasiūlymo galiojimo datą. | Taip | Taip | Nr. | Taip\* | Nr. |
| 627 | Perskaičiuoti | Perskaičiuokite visas kliento užsakymo eilutes ir mokesčius, kuriems taikoma dabartinė konfigūracija. | Taip | Taip | Nr. | Taip\* | Nr. |
| 515 | Atšaukti užsakymą | Ši operacija leidžia vartotojui ieškoti kliento užsakymų ir juos bei pardavimo pasiūlymus atšaukti. | Taip | Taip | Taip | Nr. | Nr. |
| 504 | Atšaukti operaciją | Ši operacija leidžia vartotojui atšaukti anksčiau sustabdytą operaciją dabartinėje parduotuvėje. | Taip | Taip | Nr. | Taip‡ | Nr. |
| 305 | Panaudoti lojalumo taškus | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Taip |
| 635 | Grąžinti siuntimo išlaidas | Ši operacija leidžia vartotojui grąžinti atšaukto užsakymo siuntimo mokesčius. | Nr. | Nr. | Nr. | Nr. | Nr. |
| 644 | Pašalinti kupono kodą | Paraginkite vartotoją pašalinti kuponus juos pasirenkant iš kuponų, susietų su operacija, sąrašo. | Taip | Taip | Nr. | Taip | Nr. |
| 1057 | Perspausdinti Z | Iš naujo atsispausdinkite ankstesnės arba pasirinktos pamainos Z ataskaitą. | Taip | Taip | Taip | Nr. | Nr. |
| 1216 | Įveskite naują slaptažodį | Ši operacija leidžia vartotojui, turinčiam slaptažodžio nustatymo iš naujo teisę, iš naujo nustatyti kito darbuotojo slaptažodį naudojant laikinąjį slaptažodį. | Taip | Taip | Taip | Nr. | Nr. |
| 109 | Grąžinti produktą | Atlikti konkrečių produktų grąžinimo operaciją. Kitas nuskaitytas produktas rodomas kaip grąžintas produktas, kurio kiekis ir kaina yra neigiami. | Taip | Taip | Nr. | Taip | Nr. |
| 114 | Grąžinimo operacija | Atšaukite ankstesnę operaciją pagal kvito numerį, kad grąžintumėte kelis arba visus produktus. | Taip | Taip | Taip | Taip§ | Nr. |
| 1211 | Pinigų įnešimas į įmonės kasą | Įnešti pinigus į įmonės kasą, perkeldamas juos iš kasos aparato į seifą. | Taip | Taip | Taip | Taip | Nr. |
| 516 | Pardavimo sąskaita faktūra | Ši operacija leidžia vartotojui atlikti mokėjimus pagal pasirinktą pardavimo sąskaitą faktūrą. | Taip | Taip | Nr. | Nr. | Nr. |
| 502 | Pardavėjas | Ši operacija leidžia vartotojui EKA nustatyti vertę **Pardavimo priėmėjas** kliento užsakymų pardavimo užsakyme. | Taip | Taip | Nr. | Taip\* | Nr. |
| 2000 | Grafiko valdymas | Ši operacija leidžia vartotojams kurti, modifikuoti arba peržiūrėti darbuotojo grafikus. | Taip | Taip | Taip | Nr. | Nr. |
| 2001 | Grafiko užklausos | Ši operacija leidžia vartotojui pateikti prašymą išleisti iš darbo, apsikeisti pamainomis arba pasiūlyti pamainas kitiems darbuotojams. | Taip | Taip | Taip | Nr. | Nr. |
| 622 | Ieška | Ši operacija leidžia vartotojams iš anksto sukonfigūruoti EKA mygtukus, kad būtų galima ieškoti pagal prekę, klientą arba kategoriją. | Taip | Taip | Taip | Taip | Nr. |
| 1213 | Ieškoti siuntimo adreso | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Nr. |
| 709 | Pasirinkti aparatūros stotį | Ši operacija leidžia vartotojui pasirinkti aparatūros stotį iš pasiekiamų aparatūros stočių sąrašo. | Taip | Taip | Taip | Taip | Nr. |
| 637 | Nustatyti numatytąjį operacijos pardavimo atstovą | Ši operacija leidžia vartotojui pasirinkti vieną galimų komisinių pardavimų grupių (pardavimo ats.) kaip numatytąjį pardavimo atstovą vėliau pridedamoms eilutėms. | Taip | Taip | Nr. | Taip | Nr. |
| 105 | Nustatyti kiekį | Pakeisti operacijos eilutės prekės kiekį. | Taip | Taip | Nr. | Taip | Nr. |
| 638 | Nustatyti pardavimo atstovą eilutėje | Ši operacija leidžia vartotojui pasirinkti vieną galimų komisinių pardavimų grupių (pardavimo ats.) pasirinktai eilutei. | Taip | Taip | Nr. | Taip | Nr. |
| 630 | Siųsti visus produktus | Įvykdymo režimą visoms eilutėms nustatykite į **Siuntimas**. | Taip | Taip | Nr. | Taip\* | Nr. |
| 629 | Siųsti pasirinktus produktus | Pasirinktų eilučių įvykdymo režimą nustatykite į **Siuntimas**. | Taip | Taip | Nr. | Taip\* | Nr. |
| 115 | Rodyti žurnalą | Rodomas parduotuvės žurnalas. Galite peržiūrėti operacijas, perspausdinti kvitus ir dovanų kvitus ir atšaukti grąžinimą. | Taip | Taip | Taip | Taip\*\* | Nr. |
| 802 | Inventorizacija | Ši operacija leidžia vartotojui kurti arba modifikuoti faktinių atsargų arba ciklo skaičiavimo inventorizacijos žurnalus. | Taip | Taip | Taip | Nr. | Nr. |
| 401 | Submeniu | Ši operacija perkelia vartotoją į kitą susietą mygtukyną. | Taip | Taip | Taip | Taip | Nr. |
| 1054 | Sustabdyti pamainą | Sustabdykite esamą pamainą, kad esamame aparate būtų galima suaktyvinti naują arba kitą pamainą. | Taip | Taip | Taip | Nr. | Nr. |
| 503 | Sustabdyti operaciją | Sustabdykite esamą pardavimo operaciją, kad vėliau parduotuvėje ją būtų galima atšaukti. | Taip | Taip | Nr. | Taip‡ | Nr. |
| 1004 | Užduočių įrašymo priemonė | Atidarykite užduočių įrašymo priemonę, kad galėtumėte įrašyti EKA procedūros veiksmus. | Nr. | Nr. | Nr. | Taip | Nr. |
| 1052 | Mokėjimo priemonių deklaravimas | Ši operacija leidžia vartotojui nurodyti kiekvieno apskaičiuoto mokėjimo būdo pinigų sumą, esančią stalčiuje. | Taip | Taip | Taip | Taip | Nr. |
| 1210 | Mokėjimo priemonės šalinimas | Ši operacija suteikia vartotojui galimybę pašalinti pinigus iš esamo stalčiaus ar pamainos. | Taip | Taip | Taip | Taip | Nr. |
| 920 | Laikrodis | Ši operacija leidžia vartotojams pažymėti atvykimą ir išvykimą iš darbo pamainų ir pertraukų. | Taip | Taip | Taip | Nr. | Nr. |
| 302 | Bendroji nuolaidos suma | Įveskite operacijos nuolaidos sumą. Ši operacija naudojama tik su prekėmis, kurioms taikoma nuolaida, ir tik nurodytos nuolaidos ribose. | Taip | Taip | Nr. | Taip | Nr. |
| 303 | Bendroji nuolaidos suma procentais | Įveskite operacijos nuolaidos procentą. Ši operacija naudojama tik su prekėmis, kurioms taikoma nuolaida, ir tik nurodytos nuolaidos ribose. | Taip | Taip | Nr. | Taip | Nr. |
| 501 | Operacijos komentaras | Įtraukite komentarą į esamą operaciją. | Taip | Taip | Nr. | Taip | Nr. |
| 922 | Peržiūrėti produkto informaciją | Atidarykite tuo metu pasirinkto eilutės elemento produkto informacijos puslapį. | Taip | Taip | Nr. | Taip | Nr. |
| 1003 | Ataskaitų peržiūra | Rodomos dabartiniam vartotojui sukonfigūruotos ataskaitos. | Taip | Taip | Taip | Nr. | Nr. |
| 921 | Peržiūrėti laikrodžio įrašus | Rodomi visų parduotuvės darbuotojų laikrodžių įrašai. | Taip | Taip | Taip | Nr. | Nr. |
| 211 | Anuliuoti mokėjimą | Anuliuokite tuo metu pasirinktą operacijos mokėjimo eilutę. | Taip | Taip | Nr. | Taip | Nr. |
| 102 | Anuliuoti produktą | Anuliuokite tuo metu pasirinktą operacijos eilutės elementą. | Taip | Taip | Nr. | Taip | Nr. |
| 500 | Anuliuoti operaciją | Anuliuokite dabartinę operaciją. | Taip | Taip | Nr. | Taip | Nr. |
| 916 | „Windows“ darbo eigos programavimo platforma | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Nr. |
| 924 | Banko kortelių X ataskaita | Ši operacija nepalaikoma. | Netaikoma | Netaikoma | Netaikoma | Netaikoma | Taip |

\* Ši operacija pasiekiama tik veikiant autonominiam režimui, kai sukuriamas kliento užsakymas arba pardavimo pasiūlymas, ir tik tada, jei EKA funkcijų profilyje sukonfigūruotas kliento užsakymų ir pardavimo pasiūlymų kūrimas. Šios operacijos atlikti negalima, kai užsakymai kuriami naudojant „Real-time Service“ arba kai užsakymai yra atšaukiami ar redaguojami.

† Operaciją veikiant autonominiam režimui galima atlikti tik tada, kai EKA funkcijų profilyje sukonfigūruota leisti kurti klientus autonominiu režimu.

‡ Kai EKA veikia autonominiu režimu, sustabdytas operacijas galima atšaukti tik apsilankius esamo aparato autonominėje duomenų bazėje. Vartotojai negali sustabdyti ir atšaukti operacijų visuose aparatuose.

§ Kai EKA veikia autonominiu režimu, galima atšaukti tik esamoje autonominėje duomenų bazėje esančias grąžinimo operacijas.

\*\* Kai EKA veikia autonominiu režimu, žurnale rodomos tik esamame autonominiame duomenų bazės kanale esančios operacijos.

