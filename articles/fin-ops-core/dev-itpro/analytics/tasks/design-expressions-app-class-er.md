---
title: ER išraiškų kūrimas siekiant iškviesti programos klasių metodus
description: Šiame straipsnyje aprašoma, kaip pakartotinai naudoti esamą programos logiką elektroninėse ataskaitų konfigūracijose, iškvieindami reikiamus programos klasių metodus.
author: kfend
ms.date: 11/02/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21c24cee15e9a0fd11838b5b8fd816e4aaed9a93
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267849"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>ER išraiškų kūrimas siekiant iškviesti programos klasių metodus

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip pakartotinai [naudoti esamas elektroninių ataskaitų (ER)](../general-electronic-reporting.md) konfigūracijų programos logikas, iškvieindami reikiamus programos klasių metodus ER išraiškose. Klasių argumentų vertes galima dinamiškai apibrėžti vykdyklėje. Pavyzdžiui, vertės gali būti pagrįstos analizatoriaus dokumento informacija, siekiant užtikrinti jo teisingumą.

Pavyzdžiui, šiame straipsnyje jūs kurkite procesą, kuris išanalizuotų gaunamus banko išrašus programos duomenims atnaujinti. Gaunamus banko išrašus gausite kaip teksto (.txt) failus, kuriuose yra tarptautiniai banko sąskaitos numerio (IBAN) kodai. Kaip banko išrašų importavimo proceso dalį turite patikrinti IBAN kodo teisingumą naudodami jau turimą logiką.

## <a name="prerequisites"></a>Būtinieji komponentai

Šiame straipsnyje nurodytos procedūros skirtos vartotojams, kuriems buvo priskirtas sistemos administratoriaus **arba elektroninių** ataskaitų **kūrėjo** vaidmuo.

Procedūras galima atlikti naudojant bet kurį duomenų rinkinį.

Norėdami juos užbaigti, turite atsisiųsti ir įrašyti šį failą: [SampleIncomingMessage.txt](https://download.microsoft.com/download/8/0/a/80adbc89-f23c-46d9-9241-e0f19125c04b/SampleIncomingMessage.txt).

Šiame straipsnyje sukuriate reikalingas Litware, Inc. pavyzdžio įmonės ER konfigūracijas. Todėl prieš vykdydami šiame straipsnyje nurodytas procedūras, turite atlikti šiuos veiksmus.

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Lokalizavimo **konfigūracijų puslapyje** patikrinkite, **ar Litware, Inc.** pavyzdinė įmonė yra ir pažymėtas kaip aktyvus konfigūravimo paslaugų teikėjas. Jei nematote šio konfigūracijos teikėjo, pirmiausia turite atlikti konfigūracijos teikėjų [kūrimo veiksmus ir pažymėti juos kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-a-new-er-model-configuration"></a>Importuoti naują ER modelio konfigūraciją

1. Konfigūracijos puslapio **Lokalizavimas skyriuje** Konfigūracijos **teikėjai pasirinkite** "Microsoft **" konfigūracijos teikėjo išklotąją** dalį.
2. Pasirinkite **Saugyklos**.
3. Puslapyje Lokalizavimo **saugyklos pasirinkite** Rodyti **filtrus**.
4. Norėdami pasirinkti visuotinės saugyklos įrašą, pridėkite pavadinimo **filtro** lauką.
5. Lauke Pavadinimas **įveskite** Visuotinis **·**. Tada pasirinkite apima **filtro** operatorių.
6. Pasirinkite **Taikyti**.
7. Pasirinkite **[Atidaryti](../er-download-configurations-global-repo.md#open-configurations-repository)**, kad peržiūrėtumėte pasirinktos saugyklos ER konfigūracijų sąrašą.
8. **Konfigūracijos saugyklos puslapio** konfigūracijos medyje pasirinkite Mokėjimo **modelį**.
9. Jei mygtukas **Importuoti** galimas, FastTab **versijos** pažymėkite jį, o tada pasirinkite **Taip**.

    Jei mygtukas **Importuoti** negalimas, jau importavote pasirinktą mokėjimo modelio **ER konfigūracijos** versiją.

10. Uždarykite **konfigūracijos saugyklos** puslapį, tada uždarykite **lokalizavimo saugyklos** puslapį.

## <a name="add-a-new-er-format-configuration"></a>Įtraukite naują ER formato konfigūraciją

Įtraukite naują ER formatą, kad galėtumėte analizuoti gaunamus banko išrašus TXT formatu.

1. Puslapyje Lokalizavimo **konfigūracijos pasirinkite** ataskaitų konfigūracijų **išklotines** dalies.
2. **Konfigūracijos puslapio** konfigūracijos medyje, kairiajame lange, **pasirinkite Mokėjimo modelį**.
3. Pasirinkite **Kurti konfigūraciją**. 
4. Išplečiamajame dialogo lange atlikite toliau nurodytus veiksmus.

    1. Lauke **Naujas** įveskite **Formatas pagal duomenų modelį PaymentModel**.
    2. Lauke Pavadinimas **įveskite** banko išrašo **importavimo formatą (pavyzdį).**
    3. Lauke Palaikomas **duomenų importavimas** pasirinkite **Taip**.
    4. Jei **norite baigti** konfigūracijos sukūrimą, pasirinkite Kurti konfigūraciją.

## <a name="design-the-er-format-configuration--format"></a>ER formato konfigūracijos kūrimas – formatas

Kurti ER formatą, nurodantį numatomą išorinio failo struktūrą TXT formatu.

1. Įtrauktai banko **išrašo importavimo formato (pavyzdžio)** formato konfigūracijai pasirinkite **Konstruktorius**.
2. Formato dizainerio **puslapio**, kuris yra kairiojoje srityje esančioje formato struktūros medyje, pasirinkite Įtraukti **šakninį.**
3. Atsiradusiame dialogo lange atlikite toliau nurodytus veiksmus:

    1. Medyje pasirinkite Text **Sequence, kad\\ įtraukumėte** sekos formato **komponentą**.
    2. Lauke Pavadinimas **įveskite Šaknis** **.**
    3. **Lauke Specialūs simboliai** pasirinkite Nauja eilutė – **Windows (CR LF)**. Remiantis šiuo parametru, kiekviena analizatoriaus failo eilutė bus laikoma atskiru įrašu.
    4. Pasirinkite **Gerai**.

4. Pasirinkite **Įtraukti**.
5. Atsiradusiame dialogo lange atlikite toliau nurodytus veiksmus:

    1. Medyje pasirinkite Teksto **\\ seka**.
    2. Lauke Pavadinimas **įveskite** **Eilutes**.
    3. Lauke **Daugialypumas** pasirinkite **Vienas daug**. Pagal šį parametrą, analizatoriaus faile bus bent viena eilutė.
    4. Pasirinkite **Gerai**.

6. Medyje pasirinkite Šakninės **eilutės\\**, tada pasirinkite Įtraukti **seką**.
7. Atsiradusiame dialogo lange atlikite toliau nurodytus veiksmus:

    1. **Lauke Pavadinimas** įveskite **Laukus**.
    2. Lauke Daugiamatis **pasirinkite** Tiksliai **vienas**.
    3. Pasirinkite **Gerai**.

8. Medyje pasirinkite šakninių **eilučių\\\\ laukus**, tada pasirinkite **Įtraukti**.
9. Atsiradusiame dialogo lange atlikite toliau nurodytus veiksmus:

    1. Medyje pasirinkite Teksto **\\ eilutę**.
    2. Lauke Pavadinimas **įveskite** **IBAN**.
    3. Pasirinkite **Gerai**.

10. Pasirinkite **Įrašyti**.

Dabar konfigūracija nustatoma taip, kad kiekvienoje analizatoriaus failo eilutėje būtų tik IBAN kodas.

![Banko išrašo importavimo formato (pavyzdžio) formato konfigūracija formato konstruktoriaus puslapyje.](../media/design-expressions-app-class-er-01.png)

## <a name="design-the-er-format-configuration--mapping-to-a-data-model"></a>ER formato konfigūracijos kūrimas – susiejimas su duomenų modeliu

Sukurkite ER formato susiejimą, kuris naudoja analizatoriaus failo informaciją duomenų modeliui užpildyti.

1. Veiksmų srities **puslapyje** Formato konstruktorius pasirinkite Susieti **formatą su modeliu**.
2. **Modelio ir duomenų šaltinio susiejimo** puslapyje, veiksmų srityje, pasirinkite **Naujas**.
3. Apibrėžimo **lauke** pasirinkite **BankToCustomerDebitCreditNotificationInitiation**.
4. Lauke Pavadinimas **įveskite** Susiejimas **su duomenų modeliu**.
5. Pasirinkite **Įrašyti**.
6. Pasirinkite **Dizaino įrankis**.
7. Modelio susiejimo **dizainerio** puslapio duomenų šaltinio **tipų medyje** pasirinkite **Dynamics 365 for Operations\\ Klasė**.
8. Duomenų šaltinių **skyriuje pasirinkite** Įtraukti šakninį **kodą**, kad įtraukumėte duomenų šaltinį, kuris iškies esamą IBAN kodų tikrinimo programos logiką.
9. Atsiradusiame dialogo lange atlikite toliau nurodytus veiksmus:

    1. Lauke Pavadinimas **įveskite** Čekio **\_ kodai**.
    2. Klasės lauke **įveskite** arba pasirinkite **ISO7064**.
    3. Pasirinkite **Gerai**.

10. Duomenų šaltinio **tipų medyje** atlikite šiuos veiksmus:

    1. Išplėskite formato **duomenų** šaltinį.
    2. Išplėskite **formato\\ šakninį: seka(šakninė)**.
    3. Išplėskite **formato\\ šakninį: seka (šakninės)\\ eilutės: 1 seka.\* (eilutės).**
    4. Išplėskite **formato šakninį: seka (šakninės)\\ eilutės: 1 seka.\\ (eilutės)\* laukai: seka 1..1 (laukai\\**).

11. Duomenų modelio **medyje** atlikite šiuos veiksmus:

    1. Išplėskite **duomenų** modelio lauką Mokėjimai.
    2. Išplėskite **mokėjimų\\ kreditoriaus sąskaitą (CreditorAccount)**.
    3. Išplėsti **mokėjimų kreditoriaus\\ sąskaitos (Kreditoriaus sąskaitos)identifikavimą\\**.
    4. Išplėskite **mokėjimų kreditoriaus sąskaitą (Kreditoriaus sąskaitos)Identifikavimo\\\\ IBAN\\**.

12. Norėdami sukonfigūruoto formato komponentus susieti su duomenų modelio laukais, atlikite šiuos veiksmus:

    1. Pasirinkite **formatą\\ Šaknis: seka (šakninės)\\ eilutės: 1 seka.\* (eilutės).**
    2. Pasirinkite **mokėjimus**.
    3. Pasirinkite **Susieti**. Remiantis šiuo parametru, kiekviena analizatoriaus failo eilutė bus laikoma vienu mokėjimu.
    4. Pasirinkite **formatą\\ Šaknis: Seka (šakninės)\\ eilutės: 1 seka.\* (eilutės)\\ Laukai: seka 1..1 (laukai)\\ IBAN: eilutė(IBAN)**.
    5. Pasirinkite **mokėjimų kreditoriaus\\ sąskaitą (Kreditoriaus sąskaitos)Identifikavimo\\\\ IBAN**.
    6. Pasirinkite **Susieti**. Remiantis šiuo parametru, **į duomenų modelio IBAN** lauką bus įrašoma reikšmė iš analizatoriaus failo.

    ![Formato komponentų susiejimas su duomenų modelio laukais modelio susiejimo dizaino įrankio puslapyje.](../media/design-expressions-app-class-er-02.png)

13. Skirtuke **Tikrinimas atlikite šiuos veiksmus, norėdami įtraukti tikrinimo taisyklę, kuri rodo klaidos pranešimą bet kuriai analizatoriaus failo eilutei,**[kurioje yra netinkamas](../general-electronic-reporting-formula-designer.md#Validation) IBAN kodas:

    1. Pasirinkite **Naujas**, tada pasirinkite Redaguoti **sąlygą**.
    2. Duomenų šaltinio **medžio formulės dizaino įrankio puslapyje išplėskite duomenų šaltinio tikrinimo kodų duomenų šaltinį,** **·** **kuris nurodo ISO7064 programos\_ klasę,** **kad būtų galima peržiūrėti galimų šios klasės metodų sąrašą.**
    3. Pasirinkite **Čekių\_\\ kodai verifyMOD1271\_ 36**.
    4. Pasirinkite **Įtraukti duomenų šaltinį**.
    5. Formulės lauke **įveskite** šią išraišką: patikrinkite [kodus](../general-electronic-reporting-formula-designer.md#Binding).verifyMOD1271 **\_\_ 36 (formatas). Root.Rows.Fields.IBAN)**.
    6. Pasirinkite **Įrašyti** ir uždarykite puslapį.
    7. Pasirinkite **Redaguoti pranešimą**.
    8. Formulės dizainerio **puslapio** formulės **lauke** įveskite **CONCATENATE(Rastas netinkamas IBAN kodas:&nbsp;", formatas. Root.Rows.Fields.IBAN)**.
    9. Pasirinkite **Įrašyti** ir uždarykite puslapį.

    Atsižvelgiant į šiuos parametrus, *[tikrinimo sąlyga grąžins bet kurio netinkamo IBAN](../er-formula-supported-data-types-primitive.md#boolean)* kodo FALSE **, iškviesdamas esamą ISO7064\_** **programos klasės verifyMOD1271** 36 metodą. Atkreipkite dėmesį, kad IBAN kodo vertė vykdyklėje yra dinamiškai apibrėžta kaip skambinimo metodo argumentas, paremtas analizės teksto failo turiniu.

    ![Tikrinimo taisyklė modelio susiejimo konstruktoriaus puslapyje.](../media/design-expressions-app-class-er-03.png)

14. Pasirinkite **Įrašyti**.
15. Uždarykite modelio **susiejimo dizaino** įrankio puslapį, tada uždarykite modelio **ir duomenų šaltinio susiejimo** puslapį.

## <a name="run-the-format-mapping"></a>Paleisti formato susiejimą

Norėdami patikrinti, vykdykite formato susiejimą naudodami anksčiau atsisiųstą failą SampleIncomingMessage.txt. Sugeneruotoje išeigaje bus duomenys, kurie importuoti iš pasirinkto teksto failo ir realiuoju importavimo metu prievaduoti į pasirinktinį duomenų modelį.

1. Modelio ir **duomenų šaltinio susiejimo puslapyje** pasirinkite **Vykdyti**.
2. Elektroninės ataskaitos **parametrų puslapyje** pasirinkite Naršyti **,** **pereikite prie failo SampleIncomingMessage.txt, kurį jūs atsisiųstas**, ir pasirinkite jį.
3. Pasirinkite **Gerai**.
4. Atkreipkite dėmesį **, kad modelio ir duomenų šaltinio susiejimo** puslapyje rodomas klaidos pranešimas apie netinkamą IBAN kodą.

    ![Modelio ir duomenų šaltinio susiejimo puslapyje vykdant formato susiejimą rezultatas.](../media/design-expressions-app-class-er-04.png)

5. Peržiūrėkite išvestį XML formatu, kuriuo rodomi iš pasirinkto failo importuoti ir į duomenų modelį perkelti duomenys. Atkreipkite dėmesį, kad tik trys importuoto teksto failo eilutės apdorotos be klaidų. 4 interneto IBAN kodas yra netinkamas ir buvo praleistas.

    ![XML išvestis.](../media/design-expressions-app-class-er-05.png)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
