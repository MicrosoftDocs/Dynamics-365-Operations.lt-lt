---
title: „Common Data Service“ objektai
description: „Microsoft Dynamics 365 Human Resources“ naudoja „Common Data Service“, kad įgalintų išplečiamumo ir integravimo scenarijus.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85dd95e8209fff28f214986f7960372db200351b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009987"
---
# <a name="common-data-service-entities"></a>„Common Data Service“ objektai

„Microsoft Dynamics 365 Human Resources“ naudoja „Common Data Service“, kad įgalintų išplečiamumo ir integravimo scenarijus.

Daugiau informacijos apie „Common Data Service“ rasite dalyje [Kas yra „Common Data Service“](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Šie „Human Resources“ objektai pasiekiami „Common Data Service“.

## <a name="benefit-entities"></a>Išmokų objektai

**Išmokos apskaičiavimo dažnumas**

| **Laukai**        | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-------------------|---------------|--------------|----------------|
| Aprašymas       | Tekstas          |              | X              |
| Dažnumo valdymas | Parinkčių rinkinys    | X            | X              |
| Yra nekintamas      | Dvi parinktys   |              | X              |
| Vardas ir pavardė              | Tekstas          | X            | X              |


**Išmokų apskaičiavimo tarifas**

| **Laukai**  | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-------------|---------------|--------------|----------------|
| Aprašymas | Tekstas          |              | X              |
| Vardas ir pavardė        | Tekstas          | X            | X              |
| TierType    | Parinkčių rinkinys    | X            | X              |


**Išmokų apskaičiavimo tarifų informacija**

| **Laukai**                             | **Duomenų tipas**  | **Būtina** | **Galimas ieškoti** |
|----------------------------------------|----------------|--------------|----------------|
| Išmokų apskaičiavimo tarifų informacijos numeris | Tekstas           | X            | X              |
| Skaičiavimo koeficiento ID                    | Peržvalga         | X            | X              |
| Įnašo metodas                    | Parinkčių rinkinys     | X            | X              |
| Galioja                              | Tik data      | X            | X              |
| Darbdavio įnašas                  | Dešimtainių dalių skaičius |              | X              |
| Galiojimo pabaiga                             | Tik data      | X            | X              |
| WorkerDeduction                        | Dešimtainių dalių skaičius |              | X              |


**Išmokų tipas**

| **Laukai**           | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|----------------------|---------------|--------------|----------------|
| ConcurrentEnrollment | Parinkčių rinkinys    |              | X              |
| Aprašymas          | Tekstas          |              | X              |
| Vardas ir pavardė                 | Tekstas          | X            | X              |
| PayrollCategory      | Parinkčių rinkinys    |              | X              |


**Išmokų planas**

| **Laukai**                               | **Duomenų tipas**  | **Būtina** | **Galimas ieškoti** |
|------------------------------------------|----------------|--------------|----------------|
| Skolos apribojimo būdas                      | Parinkčių rinkinys     |              | X              |
| Išmokos tipas                             | Peržvalga         | X            | X              |
| Įnašo apribojimo metodas                | Parinkčių rinkinys     |              | X              |
| Įnašo metodas                      | Parinkčių rinkinys     |              | X              |
| Valiuta                                 | Peržvalga         |              | X              |
| Atskaitymo pirmumas                       | Sveikasis skaičius   |              | X              |
| Numatytoji įnašo ribojimo suma        | Valiuta       |              | X              |
| Numatytojo įnašo apribojimo suma (pagrindinė) | Valiuta       |              | X              |
| Numatytojo įnašo apribojimo laikotarpis        | Parinkčių rinkinys     |              | X              |
| Numatytoji atskaitymo ribojimo suma           | Valiuta       |              | X              |
| Numatytojo atskaitymo apribojimo suma (pagrindinė)    | Valiuta       |              | X              |
| Numatytojo atskaitymo apribojimo laikotarpis           | Parinkčių rinkinys     |              | X              |
| Aprašymas                              | Tekstas           |              | X              |
| Valiutos kursas                            | Dešimtainių dalių skaičius |              | X              |
| Papildomo darbo užmokesčio vykdymas                | Dvi parinktys    |              | X              |
| Yra nurodoma pagal įstatymą dėl prieinamos sveikatos priežiūros        | Dvi parinktys    |              | X              |
| Yra sugeneruota skola                      | Dvi parinktys    |              | X              |
| Bendroji suma                              | Dvi parinktys    |              | X              |
| Pagrindinis                               | Dvi parinktys    |              | X              |
| Vardas ir pavardė                                     | Tekstas           | X            | X              |
| Poveikis atlyginimui                           | Parinkčių rinkinys     |              | X              |
| Pensijos tipas                          | Parinkčių rinkinys     |              | X              |


**Įdarbinimo objektas**

| **Laukai**                     | **Duomenų tipas**  | **Būtina** | **Galimas ieškoti** |
|--------------------------------|----------------|--------------|----------------|
| Patikslinta darbininko darbo pradžios data     | Data ir laikas  |              | X              |
| Įmonė                        | Peržvalga         | X            | X              |
| Pranešimo sumos darbdavio vnt. | Dešimtainių dalių skaičius |              | X              |
| Darbininko pranešimo vienetas        | Parinkčių rinkinys     |              | X              |
| Įdarbinimo pabaigos data            | Data ir laikas  |              | X              |
| Įdarbinimų skaičius              | Tekstas           | X            | X              |
| Įdarbinimo pradžios data          | Data ir laikas  |              | X              |
| Paskutinės darbo dienos data              | Data ir laikas  |              | X              |
| Perėjimo data                | Data ir laikas  |              | X              |
| Galioja nuo                     | Data ir laikas  | X            | X              |
| Galioja iki                       | Data ir laikas  |              | X              |
| Darbininkas                         | Peržvalga         | X            | X              |
| Darbininko pranešimo suma           | Dešimtainių dalių skaičius |              | X              |
| Darbininko darbo pradžios data             | Data ir laikas  |              | X              |
| Darbininko tipas                    | Parinkčių rinkinys     | X            | X              |
| Darbininko pranešimo vienetas          | Parinkčių rinkinys     |              | X              |

## <a name="worker-entities"></a>Darbininko subjektai

**Etninė kilmė**

| **Laukai**         | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|--------------------|---------------|--------------|----------------|
| Aprašymas        | Tekstas          |              | X              |
| Etninės kilmės pavadinimas | Tekstas          | X            | X              |


**Kalba**

| **Laukai**    | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|---------------|---------------|--------------|----------------|
| Aprašymas   | Tekstas          |              | X              |
| Kalbos pavadinimas | Tekstas          | X            | X              |


**Seniai dirbančiojo būsena**

| **Laukai**           | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|----------------------|---------------|--------------|----------------|
| Aprašymas          | Tekstas          |              | X              |
| Apsaugotas veteranas | Dvi parinktys    |              | X              |
| Kalbos pavadinimas        | Tekstas          | X            | X              |


**Darbininkas**

| **Laukai**                | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|---------------------------|---------------|--------------|----------------|
| Gimimo data                 | Tik data     |              | X              |
| Aprašymas               | Tekstas          |              | X              |
| 1 el. pašto adresas           | El. pašto adresas         |              | X              |
| 2 el. pašto adresas           | El. pašto adresas         |              | X              |
| „Facebook“ profilis         | Tekstas          |              | X              |
| Vardas                | Tekstas          |              | X              |
| Visas vardas                 | Tekstas          |              | X              |
| Giminė                    | Parinkčių rinkinys    |              | X              |
| Generavimas                | Tekstas          |              | X              |
| Kontakto el. pašto adresas yra leidžiamas  | Dvi parinktys   |              | X              |
| Kontakto telefono numeris yra leidžiamas  | Dvi parinktys   |              | X              |
| Pavardė                 | Tekstas          |              | X              |
| „LinkedIn“ profilis         | Tekstas          |              | X              |
| Vadovas                   | Peržvalga        |              | X              |
| Antras vardas               | Tekstas          |              | X              |
| Mobilusis telefonas              | Telefonas         |              | X              |
| „Office Graph“ identifikatorius   | Tekstas          |              | X              |
| Pagrindinis el. pašto adresas     | El. pašto adresas         |              | X              |
| Pagrindinis telefonas         | Telefonas         |              | X              |
| Profesija                | Tekstas          |              | X              |
| 1 socialinis tinklas          | Parinkčių rinkinys    |              | X              |
| 2 socialinis tinklas          | Parinkčių rinkinys    |              | X              |
| 1 socialinio tinklo profilis | Tekstas          |              | X              |
| 2 socialinio tinklo profilis | Tekstas          |              | X              |
| Šaltinis                    | Parinkčių rinkinys    | X            | X              |
| Būsena                    | Parinkčių rinkinys    | X            | X              |
| 1 telefonas               | Telefonas         |              | X              |
| 2 telefonas               | Telefonas         |              | X              |
| 3 telefonas               | Telefonas         |              | X              |
| „Twitter“ tapatybė          | Tekstas          |              | X              |
| Vartotojas                      | Peržvalga        |              | X              |
| Svetainės URL               | URL           |              | X              |
| Darbininkų skaičius             | Tekstas          | X            | X              |
| Darbininko tipas               | Parinkčių rinkinys    | X            | X              |
| „Yomi“ vardas           | Tekstas          |              | X              |
| „Yomi“ vardas ir pavardė            | Tekstas          |              | X              |
| „Yomi“ pavardė            | Tekstas          |              | X              |
| „Yomi“ antras vardas          | Tekstas          |              | X              |


**Darbininko adresas**

| **Laukai**           | **Duomenų tipas**  | **Būtina** | **Galimas ieškoti** |
|----------------------|----------------|--------------|----------------|
| Adreso numeris       | Tekstas           | X            | X              |
| Adreso tipas         | Parinkčių rinkinys     | X            | X              |
| Miestas                 | Tekstas           |              | X              |
| Šalis arba regionas    | Tekstas           |              | X              |
| Apskritis               | Tekstas           |              | X              |
| Faksas                  | Telefonas          |              | X              |
| Pageidaujama         | Dvi parinktys    |              | X              |
| Platuma             | Dešimtainių dalių skaičius |              | X              |
| 1 eilutė               | Tekstas           |              | X              |
| 2 eilutė               | Tekstas           |              | X              |
| 3 eilutė               | Tekstas           |              | X              |
| Ilguma            | Dešimtainių dalių skaičius |              | X              |
| Pašto indeksas          | Tekstas           |              | X              |
| Pašto dėžutė      | Tekstas           |              | X              |
| Siuntimo metodo kodas | Sveikasis skaičius   |              | X              |
| Rajonas arba apskritis    | Tekstas           |              | X              |
| 1 telefonas          | Telefonas          |              | X              |
| 2 telefonas          | Telefonas          |              | X              |
| 3 telefonas          | Telefonas          |              | X              |
| UPS zona             | Tekstas           |              | X              |
| UTC korespondavimas           | Sveikasis skaičius   |              | X              |
| Darbininkas               | Peržvalga         | X            | X              |


**Darbininko asmeninė informacija**

| Laukai                             | Duomenų tipas    | Būtinas | Galimas ieškoti |
|------------------------------------|--------------|----------|------------|
| Gimimo miestas                         | Tekstas         |          | X          |
| Gimtoji šalis / regionas            | Parinkčių rinkinys   |          | X          |
| Gimimo data                          | Tik data    |          | X          |
| Pilietybės šalis ar regionas      | Parinkčių rinkinys   |          | X          |
| Mirties data                      | Tik data    |          | X          |
| Seniai dirbančiojo neįgalumo patvirtinimo data | Tik data    |          | X          |
| Išsilavinimas                          | Tekstas         |          | X          |
| Etninė kilmė                     | Peržvalga       |          | X          |
| ExpatriateEndDate                  | Tik data    |          | X          |
| ExpatriateStartDate                | Tik data    |          | X          |
| Tėvo gimimo šalis ar regionas     | Parinkčių rinkinys   |          | X          |
| Giminė                             | Parinkčių rinkinys   |          | X          |
| Neįgalus                        | Dvi parinktys  |          | X          |
| Seniai dirbantysis su negalia                | Dvi parinktys  |          | X          |
| Ar taikoma dirbančių užsienyje nutartis?    | Dvi parinktys  |          | X          |
| Nuosekliųjų studijų studentas               | Dvi parinktys  |          | X          |
| Šeiminė padėtis                     | Parinkčių rinkinys   |          | X          |
| Karinės tarnybos pabaigos data          | Tik data    |          | X          |
| Karinės tarnybos pradžios data        | Tik data    |          | X          |
| Motinos gimimo šalis ar regionas     | Parinkčių rinkinys   |          | X          |
| Tautybės šalis arba regionas      | Parinkčių rinkinys   |          | X          |
| Gimtoji kalba                    | Peržvalga       |          | X          |
| Priklausomųjų skaičius               | Sveikasis skaičius |          |            |
| Seniai dirbančiojo būsena                     | Peržvalga       |          | X          |
| Darbininkas                             | Peržvalga       | X        | X          |
| Darbininko asmeninės informacijos numeris      | Tekstas         | X        | X          |


**Darbininko banko kodas**

| **Laukai**                 | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|----------------------------|---------------|--------------|----------------|
| Sąskaitos savininkas             | Tekstas          |              | X              |
| Sąskaitos identifikavimas     | Tekstas          |              | X              |
| Adreso aprašas        | Tekstas          |              | X              |
| Banko sąskaitos tipas          | Parinkčių rinkinys    |              | X              |
| Banko vietos kodas         | Tekstas          |              | X              |
| Filialo pavadinimas                | Tekstas          |              | X              |
| Filialo numeris              | Tekstas          |              | X              |
| Miestas                       | Tekstas          |              | X              |
| Šalis arba regionas          | Tekstas          |              | X              |
| Apskritis                     | Tekstas          |              | X              |
| Aprašymas                | Tekstas          |              | X              |
| Rajono pavadinimas              | Tekstas          |              | X              |
| El. pašto adresas                      | Tekstas          |              | X              |
| Papildomas telefonas                  | Tekstas          |              | X              |
| Faksas                        | Tekstas          |              | X              |
| IBAN                       | Tekstas          |              | X              |
| 1 eilutė                     | Tekstas          |              | X              |
| 2 eilutė                     | Tekstas          |              | X              |
| 3 eilutė                     | Tekstas          |              | X              |
| Mobilusis telefonas               | Tekstas          |              | X              |
| Asmens vardas             | Tekstas          |              | X              |
| Pašto indeksas                | Tekstas          |              | X              |
| Pašto dėžutė            | Tekstas          |              |                |
| Banko kodas             | Tekstas          |              | X              |
| Įmonės registracijos numerio tipas        | Parinkčių rinkinys    |              | X              |
| Rajonas arba apskritis          | Tekstas          |              | X              |
| SWIFT kodas                 | Tekstas          |              | X              |
| Telefonas                  | Tekstas          |              | X              |
| Telekso numeris               | Tekstas          |              | X              |
| Svetainės URL                | Tekstas          |              | X              |
| Darbininkas                     | Peržvalga        | X            | X              |
| Darbininko banko sąskaitos numeris | Tekstas          |              | X              |
| Darbininko banko sąskaitos numeris | Tekstas          | X            | X              |

**Darbininko pastovioji atlyginimo dalis**

| Laukai                                | Duomenų tipas      | Būtinas | Galimas ieškoti |
|---------------------------------------|----------------|----------|------------|
| Įmonė                               | Peržvalga         | X        | X          |
| Kompensacijos tipas                     | Parinkčių rinkinys     |          | X          |
| Valiuta                              | Peržvalga         |          | X          |
| Įsigaliojimo data                        | Tik data      |          | X          |
| Įvykis                                 | Peržvalga         | X        | X          |
| Valiutos kursas                         | Dešimtainių dalių skaičius |          | X          |
| Galiojimo data                       | Tik data      |          | X          |
| Eilutės numeris                           | Dešimtainių dalių skaičius |          | X          |
| Išmokos dažnumas                         | Peržvalga         | X        | X          |
| Užmokesčio tarifas                              | Valiuta       |          | X          |
| Užmokesčio tarifas (pagrindas)                       | Valiuta       |          | X          |
| Planas.                                  | Peržvalga         | X        | X          |
| Pozicija                              | Peržvalga         | X        | X          |
| Proceso tipas                          | Parinkčių rinkinys     | X        | X          |
| Atskaitos taško nustatymo eilutė            | Peržvalga         |          | X          |
| Darbininkas                                | Peržvalga         | X        | X          |
| Darbininko pastoviosios atlyginimo dalies numeris      | Tekstas           | X        | X          |

**Darbininko asmens tapatybės numeris**

| Laukai                 | Duomenų tipas   | Būtinas | Galimas ieškoti |
|------------------------|-------------|----------|------------|
| Aprašymas            | Tekstas        |          | X          |
| Įrašo tipas             | Tekstas        |          | X          |
| Galiojimo data        | Tik data   |          | X          |
| Identifikavimo numeris  | Tekstas        | X        | X          |
| Identifikavimo tipas    | Peržvalga      | X        | X          |
| Pagrindinis             | Dvi parinktys |          | X          |
| Išdavimo data             | Tik data   |          | X          |
| Išduodanti agentūra         | Peržvalga      | X        | X          |
| Darbininkas                 | Peržvalga      | X        | X          |


## <a name="position-entities"></a>Pareigų objektai

**Pareigos**

| **Laukai**               | **Duomenų tipas**  | **Būtina** | **Galimas ieškoti** |
|--------------------------|----------------|--------------|----------------|
| Aktyvinimas               | Data ir laikas  |              | X              |
| Galima priskirti | Data ir laikas  |              | X              |
| Skyrius               | Peržvalga         |              | X              |
| Aprašymas              | Tekstas           |              | X              |
| Viso etato ekvivalentas     | Dešimtainių dalių skaičius |              | X              |
| Pareigos                      | Peržvalga         | X            | X              |
| Pareigų numeris      | Tekstas           | X            | X              |
| Pirminės pareigos      | Peržvalga         |              | X              |
| Pareigų tipas            | Peržvalga         |              | X              |
| Išėjimas į pensiją               | Data ir laikas  |              | X              |
| Pareigos                    | Parinkčių rinkinys     |              | X              |
| Galioja nuo               | Data ir laikas  | X            | X              |
| Galioja iki                 | Data ir laikas  |              | X              |


**Pareigų tipas**

| **Laukai**         | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|--------------------|---------------|--------------|----------------|
| Klasifikacija     | Parinkčių rinkinys    |              | X              |
| Aprašymas        | Tekstas          |              | X              |
| Pareigų tipo pavadinimas | Tekstas          | X            | X              |


**Darbininko paskyrimas į pareigas**

| **Laukai**                        | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-----------------------------------|---------------|--------------|----------------|
| Pareigos                      | Peržvalga        | X            | X              |
| Darbininko paskyrimo į pareigas numeris | Tekstas          | X            | X              |
| Galioja nuo                        | Tekstas          | X            | X              |
| Galioja iki                          |               |              | X              |
| Darbininkas                            |               | X            | X              |

## <a name="job-entities"></a>Užduoties objektai

**Užduotis**

| **Laukai**                   | **Duomenų tipas**  | **Būtina** | **Galimas ieškoti** |
|------------------------------|----------------|--------------|----------------|
| Leisti neribotą pareigų skaičių    | Dvi parinktys    |              | X              |
| Numatytasis viso etato ekvivalentas | Dešimtainių dalių skaičius |              | X              |
| Aprašymas                  | Tekstas           |              | X              |
| Darbo aprašas              | Tekstas           |              | X              |
| Darbo funkcija                 | Peržvalga         |              | X              |
| Darbo tipas                     | Peržvalga         |              | X              |
| Didžiausias pozicijų skaičius  | Sveikasis skaičius   |              | X              |
| Vardas ir pavardė                         | Tekstas           | X            | X              |
| Pareigos                        | Parinkčių rinkinys     |              | X              |
| Galioja nuo                   | Data ir laikas  | X            | X              |
| Galioja iki                     | Data ir laikas  |              | X              |


**Užduoties funkcija**

| **Laukai**        | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-------------------|---------------|--------------|----------------|
| Aprašymas       | Tekstas          | X            | X              |
| Užduoties funkcijos pavadinimas | Tekstas          | X            | X              |


**Užduoties tipas**

| **Laukai**    | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|---------------|---------------|--------------|----------------|
| Aprašymas   | Tekstas          | X            | X              |
| Neapmokestinimo būsena | Parinkčių rinkinys    | X            | X              |
| Užduoties tipo pavadinimas | Tekstas          | X            | X              |

## <a name="leave-and-absence-entities"></a>Atostogų ir neatvykimų objektai

**Atostogų registracija**

| **Laukai**            | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-----------------------|---------------|--------------|----------------|
| Kaupimo datos pagrindas    | Tik data     | X            | X              |
| Kaupimo pradžios data    | Tik data     | X            | X              |
| Pasirinktinė data           | Tik data     | X            | X              |
| Kaupimas sustabdytas  | Dvi parinktys   |              | X              |
| LeaveEnrollmentNumber | Tekstas          | X            | X              |
| Atostogų planas            | Peržvalga        | X            | X              |
| Pradžios data            | Tik data     | X            | X              |
| Pakopų pagrindas            | Parinkčių rinkinys    | X            | X              |
| Darbininkas                | Peržvalga        | X            | X              |


**Banko išėjimo operacija**

| **Laukai**                    | **Duomenų tipas**  | **Būtina** | **Galimas ieškoti** |
|-------------------------------|----------------|--------------|----------------|
| Suma                        | Dešimtainių dalių skaičius | X            | X              |
| Įmonė                       | Peržvalga         | X            | X              |
| Banko išėjimo operacijos numeris | Tekstas           | X            | X              |
| Atostogų planas                    | Peržvalga         |              | X              |
| Atostogų tipas                    | Peržvalga         | X            | X              |
| Operacijos data              | Tik data      | X            | X              |
| Operacijos numeris            | Dešimtainių dalių skaičius | X            | X              |
| Operacijos tipas              | Parinkčių rinkinys     | X            | X              |
| Darbininkas                        | Peržvalga         | X            | X              |


**Atostogų planas**

| **Laukai**        | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-------------------|---------------|--------------|----------------|
| Kaupimo dažnumas | Parinkčių rinkinys    | X            | X              |
| Įmonė           | Peržvalga        | X            | X              |
| Aprašymas       | Tekstas          |              | X              |
| Atostogų tipas        | Peržvalga        | X            | X              |
| Vardas ir pavardė              | Tekstas          | X            | X              |
| Pradžios data        | Tik data     | X            | X              |


**Atostogų prašymas**

| **Laukai**           | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|----------------------|---------------|--------------|----------------|
| Komentuoti              | Tekstas          | X            | X              |
| Įmonė              | Peržvalga        | X            | X              |
| Atostogų užklausos numeris | Tekstas          |              | X              |
| Užklausos data         | Data ir laikas | X            | X              |
| Būsena               | Parinkčių rinkinys    | X            | X              |
| Darbininkas               | Peržvalga        | X            | X              |


**Atostogų užklausos informacija**

| **Laukai**                  | **Duomenų tipas**  | **Būtina** | **Galimas ieškoti** |
|-----------------------------|----------------|--------------|----------------|
| Suma                      | Dešimtainių dalių skaičius | X            | X              |
| Atostogų data                  | Data ir laikas  | X            | X              |
| Atostogų prašymas               | Peržvalga         | X            | X              |
| Atostogų užklausos informacijos numeris | Tekstas           | X            | X              |
| Atostogų tipas                  | Peržvalga         | X            | X              |


**Atostogų tipas**

| **Laukai**      | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-----------------|---------------|--------------|----------------|
| Įmonė         | Peržvalga        | X            | X              |
| Aprašymas     | Tekstas          |              | X              |
| Pajamų kodas    | Peržvalga        |              | X              |
| Atostogų tipo pavadinimas | Tekstas          | X            | X              |


**Darbo kalendorius**

| **Laukai**  | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-------------|---------------|--------------|----------------|
| Įmonė     | Peržvalga        | X            | X              |
| Aprašymas | Tekstas          |              | X              |
| Vardas ir pavardė        | Tekstas          | X            | X              |


**Darbo kalendoriaus diena**

| **Laukai**               | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|--------------------------|---------------|--------------|----------------|
| Kalendoriaus data            | Tik data     | X            | X              |
| Įmonė                  | Peržvalga        |              | X              |
| Būsena                   | Tekstas          |              | X              |
| Darbo kalendorius            | Peržvalga        | X            | X              |
| Darbo kalendoriaus dienos numeris | Tekstas          | X            | X              |


**Darbo kalendoriaus šventė**

| **Laukai**  | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-------------|---------------|--------------|----------------|
| Vardas ir pavardė        | Tekstas          |              | X              |
| Aprašymas | Tekstas          | X            | X              |


**Darbo kalendoriaus šventės eilutė**

| **Laukai**                        | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-----------------------------------|---------------|--------------|----------------|
| Šventinės dienos data                      | Tik data     | X            | X              |
| Vardas ir pavardė                              | Tekstas          |              | X              |
| Darbo kalendoriaus šventė             | Peržvalga        | X            | X              |
| Darbo kalendoriaus šventės eilutės numeris | Tekstas          | X            | X              |


**Darbo kalendoriaus laiko intervalas**

| **Laukai**                         | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|------------------------------------|---------------|--------------|----------------|
| Įmonė                            | Peržvalga        |              | X              |
| Pabaigos laikas                           | Sveikasis skaičius  |              | X              |
| Pradžios laikas                         | Sveikasis skaičius  |              | X              |
| Darbo kalendorius                      | Peržvalga        | X            | X              |
| Darbo kalendoriaus diena                  | Peržvalga        | X            | X              |
| Darbo kalendoriaus laiko intervalo numeris | Tekstas          | X            | X              |

## <a name="organization-entities"></a>Organizacijos objektai

**Įmonė**

| **Laukai**   | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|--------------|---------------|--------------|----------------|
| Įmonės kodas | Tekstas          | X            | X              |
| Vardas ir pavardė         | Tekstas          | X            | X              |


**Skyrius**

| **Laukai**        | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-------------------|---------------|--------------|----------------|
| Padalinio numeris | Tekstas          | X            | X              |
| Aprašymas       | Tekstas          |              | X              |
| Vardas ir pavardė              | Tekstas          | X            | X              |
| Pirminis padalinys | Peržvalga        |              | X              |


**Valiuta**

| **Laukai**         | **Duomenų tipas**  | **Būtina** | **Galimas ieškoti** |
|--------------------|----------------|--------------|----------------|
| Valiutos kodas      | Tekstas           | X            | X              |
| Valiutos pavadinimas      | Tekstas           | X            | X              |
| Valiutos tikslumas | Sveikasis skaičius   | X            | X              |
| Valiutos simbolis    | Tekstas           | X            | X              |
| Objekto vaizdas       | Vaizdas          |              |                |
| Valiutos kursas      | Dešimtainių dalių skaičius | X            | X              |
| Organizacija       | Peržvalga         | X            | X              |
| Būsena             | Parinkčių rinkinys     |              | X              |

## <a name="payroll-entities"></a>Algalapio objektai

**Mokėjimo ciklas**

| **Laukai**  | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-------------|---------------|--------------|----------------|
| Aprašymas | Tekstas          | X            | X              |
| Dažnumas   | Parinkčių rinkinys    | X            | X              |
| Vardas ir pavardė        | Tekstas          | X            | X              |


**Mokėjimo laikotarpis**

| **Laukai**           | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|----------------------|---------------|--------------|----------------|
| Numatytoji mokėjimo data | Tik data     |              | X              |
| Aprašymas          | Tekstas          |              | X              |
| Mokėjimo ciklas            | Ieškoti          | X            | X              |
| Mokėjimo laikotarpio numeris    | Tekstas          | X            | X              |
| Laikotarpio pabaigos data      | Tik data     | X            | X              |
| Laikotarpio pradžios data    | Tik data     | X            | X              |
| Būsena               | Parinkčių rinkinys    |              | X              |


**Algalapio pajamų kodas**

| **Laukai**              | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-------------------------|---------------|--------------|----------------|
| Aprašymas             | Tekstas          | X            | X              |
| Įtraukti į mokėjimo tipą | Parinkčių rinkinys    | X            | X              |
| Produktyvus           | Dvi parinktys   | X            | X              |
| Vardas ir pavardė                    | Tekstas          |              | X              |
| Kiekio vienetas           | Parinkčių rinkinys    |              | X              |
| Sekti FMLA valandas        | Dvi parinktys   |              | X              |


**Mokesčių regionas**

| **Laukai**        | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-------------------|---------------|--------------|----------------|
| Miestas              | Tekstas          |              | X              |
| Šalis arba regionas | Tekstas          |              | X              |
| Apskritis            | Tekstas          |              | X              |
| Vardas ir pavardė              | Tekstas          | X            | X              |
| Rajonas arba apskritis | Tekstas          |              | X              |


**Išmokų skaičiavimo dažnumo mokėjimo laikotarpis**

| **Laukai**                                      | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-------------------------------------------------|---------------|--------------|----------------|
| Išmokos apskaičiavimo dažnumas                   | Peržvalga        | X            | X              |
| Išmokų skaičiavimo dažnumo mokėjimo laikotarpio numeris | Tekstas          | X            | X              |
| Mokėjimo laikotarpis                                      | Peržvalga        | X            | X              |


**Banko sąskaitos išmoka**

| **Laukai**                       | **Duomenų tipas**  | **Būtina** | **Galimas ieškoti** |
|----------------------------------|----------------|--------------|----------------|
| Suma                           | Valiuta       |              | X              |
| Suma (bazinė)                    | Valiuta       |              | X              |
| Banko kodas                     | Peržvalga         | X            | X              |
| Banko sąskaitos išmokos numeris | Tekstas           | X            | X              |
| Įmonė                          | Peržvalga         | X            | X              |
| Valiuta                         | Peržvalga         |              | X              |
| Valiutos kursas                    | Dešimtainių dalių skaičius |              | X              |
| Likutis                     | Dvi parinktys    |              | X              |
| Pirmenybė                         | Sveikasis skaičius   |              | X              |

**Asmens identifikavimą išduodanti agentūra**

| **Laukai**           | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|----------------------|---------------|--------------|----------------|
| Adreso aprašas  | Tekstas          |              | X              |
| 1 adreso eilutė       | Tekstas          |              | X              |
| 2 adreso eilutė       | Tekstas          |              | X              |
| 3 adreso eilutė       | Tekstas          |              | X              |
| Miestas                 | Tekstas          |              | X              |
| Šalis arba regionas    | Parinkčių rinkinys    |              | X              |
| Apskritis               | Tekstas          |              | X              |
| Aprašymas          | Tekstas          |              | X              |
| El. pašto adresas                | Tekstas          |              | X              |
| Papildomas telefonas            | Tekstas          |              | X              |
| Faksas                  | Tekstas          |              | X              |
| Išduodančios agentūros pavadinimas  | Tekstas          | X            | X              |
| Mobilusis telefonas         | Tekstas          |              | X              |
| Puslapis                 | Tekstas          |              | X              |
| Pašto indeksas          | Tekstas          |              | X              |
| Pašto dėžutė      | Tekstas          |              | X              |
| SMS                  | Tekstas          |              | X              |
| Rajonas arba apskritis    | Tekstas          |              | X              |
| Telefonas            | Tekstas          |              | X              |
| Teleksas                | Tekstas          |              | X              |
| Svetainės URL          | Tekstas          |              | X              |

**Darbininko asmens tapatybės tipas**

| **Laukai**                        | **Duomenų tipas**  | **Būtina** | **Galimas ieškoti** |
|-----------------------------------|----------------|--------------|----------------|
| Leidžiamos reikšmės                    | Parinkčių rinkinys     |              | X              |
| Šalis arba regionas                 | Tekstas           |              | X              |
| Aprašymas                       | Tekstas           |              | X              |
| Fiksuotas ilgis                      | Sveikasis skaičius   |              | X              |
| Identifikavimo numerio formatas      | Tekstas           |              | X              |
| Tipas                              | Parinkčių rinkinys     |              | X              |
| Darbininko asmens tapatybės tipas | Tekstas           | X            | X              |

## <a name="fixed-compensation-entities"></a>Pastoviosios atlyginimo dalies įvykis

**Kompensavimo planas**

| **Laukai**                  | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-----------------------------|---------------|--------------|----------------|
| Įmonė                     | Peržvalga        | X            | X              |
| Kompensavimo tinklelis           | Peržvalga        |              | X              |
| Valiuta                    | Peržvalga        | X            | X              |
| Aprašymas                 | Tekstas          | X            | X              |
| Įsigaliojimo data              | Tik data     | X            | X              |
| Galiojimo data             | Tik data     | X            | X              |
| Samdos taisyklė                   | Parinkčių rinkinys    | X            | X              |
| Vardas ir pavardė                        | Tekstas          | X            | X              |
| Nepatenka į leistiną nuokrypio diapazoną      | Parinkčių rinkinys    | X            | X              |
| Išmokos dažnumas               | Peržvalga        | X            | X              |
| Leistina rekomendacija      | Dvi parinktys   | X            | X              |
| Atskaitos taško eilutės nustatymas  | Peržvalga        |              | X              |
| Tipas                        | Parinkčių rinkinys    | X            | X              |

**Kompensavimo tinklelis**

| **Laukai**                  | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-----------------------------|---------------|--------------|----------------|
| Įmonė                     | Peržvalga        | X            | X              |
| Valiuta                    | Peržvalga        |              | X              |
| Aprašymas                 | Tekstas          | X            | X              |
| Įsigaliojimo data              | Tik data     |              | X              |
| Galiojimo data             | Tik data     |              | X              |
| Vardas ir pavardė                        | Tekstas          | X            | X              |
| Atskaitos taško nustatymas       | Peržvalga        | X            | X              |
| Tipas                        | Parinkčių rinkinys    | X            | X              |

**Kompensavimo lygis**

| **Laukai**      | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-----------------|---------------|--------------|----------------|
| Aprašymas     | Tekstas          |              | X              |
| Vardas ir pavardė            | Tekstas          | X            | X              |
| Tipas            | Parinkčių rinkinys     | X            | X              |

**Kompensavimo išmokos dažnumas**

| **Laukai**                  | **Duomenų tipas**   | **Būtina** | **Galimas ieškoti** |
|-----------------------------|-----------------|--------------|----------------|
| Metinis konvertavimo koeficientas    | Dešimtainių dalių skaičius  |              | X              |
| Įmonė                     | Peržvalga          | X            | X              |
| Aprašymas                 | Tekstas            |              | X              |
| Valandinis konvertavimo koeficientas    | Dešimtainių dalių skaičius  |              | X              |
| Mėnesis konvertavimo koeficientas   | Dešimtainių dalių skaičius  |              | X              |
| Vardas ir pavardė                        | Tekstas            | X            | X              |
| Laikotarpis                      | Parinkčių rinkinys      |              | X              |
| Savaitinis konvertavimo koeficientas    | Parinkčių rinkinys      |              | X              |


**Kompensavimo atskaitos taškų nustatymas**

| **Laukai**          | **Duomenų tipas**   | **Būtina** | **Galimas ieškoti** |
|---------------------|-----------------|--------------|----------------|
| Įmonė             | Peržvalga          | X            | X              |
| Kompensacijos tipas   | Parinkčių rinkinys      | X            | X              |
| Aprašymas         | Tekstas            | X            | X              |
| Vardas ir pavardė                | Tekstas            | X            | X              |

**Kompensavimo atskaitos taškų nustatymo eilutė**

| **Laukai**            | **Duomenų tipas**   | **Būtina** | **Galimas ieškoti** |
|-----------------------|-----------------|--------------|----------------|
| Įmonė               | Peržvalga          | X            | X              |
| Aprašymas           | Tekstas            | X            | X              |
| Eilutės numeris           | Dešimtainių dalių skaičius  | X            | X              |
| Vardas ir pavardė                  | Tekstas            | X            | X              |
| Atskaitos taško nustatymas | Peržvalga          | X            | X              |

**Kompensacijos sritis**

| **Laukai**      | **Duomenų tipas** | **Būtina** | **Galimas ieškoti** |
|-----------------|---------------|--------------|----------------|
| Aprašymas     | Tekstas          | X            | X              |
| Vardas ir pavardė            | Tekstas          | X            | X              |

**Kompensavimo struktūra**

| **Laukai**                    | **Duomenų tipas**   | **Būtina** | **Galimas ieškoti** |
|-------------------------------|---------------  |--------------|----------------|
| Suma                        | Valiuta        |              | X              |
| Sumos pagrindas                   | Valiuta        |              | X              |
| Įmonė                       | Peržvalga          | X            | X              |
| Kompensavimo struktūros numeris | Tekstas            | X            | X              |
| Valiuta                      | Peržvalga          |              | X              |
| Valiutos kursas                 | Dešimtainių dalių skaičius  |              | X              |
| Tinklelis                          | Peržvalga          | X            | X              |
| Lygis                         | Peržvalga          | X            | X              |
| Atskaitos taško kontrolinis taškas               | Peržvalga          | X            | X              |
| Atskaitos taško eilutės nustatymas    | Peržvalga          | X            | X              |

**Pastoviosios atlyginimo dalies įvykis**

| **Laukai**            | **Duomenų tipas**   | **Būtina** | **Galimas ieškoti** |
|-----------------------|-----------------|--------------|----------------|
| Įmonė               | Peržvalga          | X            | X              |
| Aprašymas           | Tekstas            | X            | X              |
| Įvykio tipas            | Parinkčių rinkinys      | X            | X              |
| Aktyvus             | Dvi parinktys     | X            |                |
| Vardas ir pavardė                  | Tekstas            | X            | X              |

## <a name="entity-relationship-models"></a>Objekto ryšių modeliai

### <a name="worker"></a>Darbininkas
![Darbininkas](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Užduotis ir pareigos
![Užduotis ir pareigos](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Išmokos
![Išmokos](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensacija
![Kompensacija](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Išeiti
![Išeiti](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Darbo kalendorius
![Darbo kalendorius](./media/HCMCommon-work-calendar-entity-diagram.png)
