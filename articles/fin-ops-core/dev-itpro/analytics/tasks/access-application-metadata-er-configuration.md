---
title: Prieiga prie programos metaduomenų naudojant ER konfigūraciją
description: Šioje temoje paaiškinama, kaip „Regulatory configuration service“ vartotojas gali kurti naują elektroninės ataskaitos modelio susiejimą naudodamas metaduomenis.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58697148ecf83f4962bd64a221945b6d911e11a6
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093310"
---
# <a name="access-application-metadata-by-using-er-configuration"></a>Prieiga prie programos metaduomenų naudojant ER konfigūraciją

[!include [banner](../../includes/banner.md)]

Toliau nurodyti veiksmai paaiškina, kaip „Regulatory configuration service“ (RCS) vartotojas, turintis sistemos administratoriaus arba elektroninės ataskaitos kūrėjo vaidmenį, gali kurti naują elektroninės ataskaitos (ER) modelio susiejimą naudodamas programos metaduomenis. Programos metaduomenys bus pasiekiami naudojant ER metaduomenų konfigūraciją, kurioje yra metaduomenų pavyzdžių rinkinys, skirtas užsienio prekybos operacijoms pasiekti. Norint atlikti šiuos veiksmus, pirmiausia RCS reikia atlikti temos [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md) procedūros veiksmus. Tada reikia atlikti temoje [Programos metaduomenų, kurie bus naudojami RCS, paruošimas](prepare-application-metadata-rcs.md) nurodytus veiksmus.

## <a name="prerequisites"></a>Būtinieji komponentai
1. Eikite į **Visos darbo sritys** > **Elektroninės ataskaitos**. 
2. Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**. Jei nematote šio konfigūracijos teikėjo, atlikite procedūros [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md) veiksmus. 

## <a name="import-metadata-configuration"></a>Metaduomenų konfigūracijos importavimas 
1. Spustelėkite **Metaduomenų konfigūracijos**. 
2. Importuokite ER metaduomenų konfigūraciją, kurioje yra metaduomenys, kurie sukonfigūruoti generuoti elektroninius dokumentus, skirtus užsienio prekybos įmonėms. Ši ER metaduomenų konfigūracija eksportuota kaip XML failas ir atlikti [Programos metaduomenų, kurie bus naudojami RCS, paruošimas](prepare-application-metadata-rcs.md) procedūros veiksmai. 
3. Spustelėkite **Keitimas**. 
4. Spustelėkite **Įkelti iš XML failo**. 
5. Spustelėkite **Naršyti** ir pasirinkite failą Užsienio prekybos metaduomenys.xml. 
6. Spustelėkite **Gerai**. 
7. Uždarykite puslapį. 

## <a name="create-data-model-configuration"></a>Duomenų modelio konfigūracijos kūrimas
1. Spustelėkite **Ataskaitų konfigūracijos**. 
2. Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą. 
3. Lauke **Pavadinimas** įveskite Užsienio prekybos modelis. 
4. Spustelėkite **Sukurti konfigūraciją**. 
5. Spustelėkite **Konstruktorius**. 
6. Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą. 
7. Lauke **Pavadinimas** įveskite „Šaknis“. 
8. Spustelėkite **Pridėti**. 
9. Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą. 
10.    Lauke **Pavadinimas** įveskite Operacija. 
11.    Lauke **Elemento tipas** pasirinkite **Įrašų sąrašas**. 
12.    Spustelėkite **Pridėti**. 
13.    Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą. 
14.    Lauke **Pavadinimas** įveskite Prekės kodas. 
15.    Lauke **Elemento tipas** pasirinkite **Eilutė**. 
16.    Spustelėkite **Pridėti**. 
17.    Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą. 
18.    Lauke **Pavadinimas** įveskite Sąskaitos faktūros suma. 
19.    Lauke **Elemento tipas** pasirinkite **Realusis skaičius**. 
20.    Spustelėkite **Pridėti**. 
21.    Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą. 
22.    Lauke **Pavadinimas** įveskite Data. 
23.    Lauke **Elemento tipas** pasirinkite **Data**. 
24.    Spustelėkite **Pridėti**. 
25.    Spustelėkite **Šakninė nuoroda**. 
26.    Spustelėkite **Gerai**. 
27.    Spustelėkite **Įrašyti**. 
28.    Uždarykite puslapį. 
29.    Spustelėkite **Keisti būseną**. 
30.    Spustelėkite **Baigta**. 
31.    Spustelėkite **Gerai**. 

## <a name="create-model-mapping-configuration"></a>Modelio susiejimo konfigūracijos kūrimas 
1. Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą. 
2. Lauke **Naujas** įveskite Modelio susiejimas remiantis duomenų modeliu Užsienio prekybos modelis. 
3. Lauke **Pavadinimas** įveskite Užsienio prekybos susiejimas. 
4. Spustelėkite **Sukurti konfigūraciją**. 
5. Išplėskite sekciją **Būtinieji komponentai**. 
6. Spustelėkite **Redaguoti**. 
7. Spustelėkite **Naujas**. 
8. Sąraše pažymėkite pasirinktą eilutę. 
9. Lauke **Būtinojo komponento tipas** pasirinkite **Konfigūracija**. 
10.    Pasirinkite konfigūraciją **Užsienio prekybos metaduomenys**. 
11.    Spustelėkite **Įrašyti**. 
12.    Įtraukėme nuorodą į konfigūracijos „Užsienio prekybos metaduomenys“ 1 versiją. Kuriant šį modelio susiejimą bus siūlomi šios konfigūracijos programos metaduomenys. 
13.    Uždarykite puslapį. 
14.    Spustelėkite **Konstruktorius**. 
15.    Spustelėkite **Konstruktorius**. 
16.    Medyje pasirinkite **Dynamics 365 for Operations\Lentelės įrašai**. 
17.    Spustelėkite **Įtraukti šakninį elementą**. 
18.    Lauke **Pavadinimas** įveskite Intrastat. 
19.    Pasirinkite **Intrastat** lentelės įrašus. 
20.    Spustelėkite **Gerai**. 

> [!NOTE]
> Siūlytos tik 2 lentelės, nes tik 2 lentelės buvo įtrauktos į šiuo metų naudojamų metaduomenų rinkinį. 

21.    Spustelėkite **Susieti**. 
22.    Medyje išplėskite **Intrastat**. 
23.    Medyje pasirinkite **Intrastat\AmountMST**. 
24.    Medyje išplėskite **Operacija = Intrastat**. 
25.    Medyje pasirinkite **Operacija = Intrastat\Sąskaitos faktūros suma**. 
26.    Spustelėkite **Susieti**. 
27.    Medyje pasirinkite **Intrastat\TransDate**. 
28.    Medyje pasirinkite **Operacija = Intrastat\Data**. 
29.    Spustelėkite **Susieti**. 
30.    Medyje išplėskite **Intrastat\>Ryšiai**. 
31.    Medyje išplėskite **Intrastat\>Ryšiai\IntrastatCommodity**. 
32.    Medyje pasirinkite **Intrastat\>Ryšiai\IntrastatCommodity\Kodas**. 
33.    Medyje pasirinkite **Operacija = Intrastat\Prekės kodas**. 
34.    Spustelėkite **Susieti**. 
35.    Spustelėkite **Tikrinti**. 

> [!NOTE]
> Sėkmingai susiejome duomenų modelio elementus su duomenų šaltinių elementais, kurie aprašomi naudojant programos metaduomenų informaciją iš nurodytos ER metaduomenų konfigūracijos. 
36.    Spustelėkite **Įrašyti**. 
37.    Uždarykite puslapį. 
38.    Uždarykite puslapį. 
39.    Kai reikia, galite išplėsti esamą metaduomenų rinkinį ir eksportuoti naują baigtos versijos ER metaduomenų konfigūraciją. Tada galite importuoti ją į RCS ir atnaujinti sukonfigūruoto modelio susiejimo konfigūracijos būtinuosius komponentus, nurodančius naują importuotų metaduomenų konfigūracijos versiją. 

> [!NOTE]
> Tai yra vienintelis būdas gauti informaciją apie programos metaduomenis, prieinamas naudojant vietinėje sistemoje įdiegtas programas (kai naudojamas vietos verslo duomenų (LBD) arba vietinio diegimo modelis).
        
