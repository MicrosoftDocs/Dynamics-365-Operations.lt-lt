---
title: (RCS) Failų importavimas XML formatu su pasirinktiniais atributais
description: Šiame straipsnyje pateikiama informacija apie tai, kaip vartotojas gali sukurti ER formato konfigūraciją, kad galėtų importuoti failus XML formatu, kuriame yra pasirinktinių atributų.
author: kfend
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: 5254a3d631129d0e41fcd37a341b54f97cfe6a9e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290011"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a>(RCS) Failų importavimas XML formatu su pasirinktiniais atributais

[!include [banner](../../includes/banner.md)]

Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali kurti ER formato konfigūraciją, naudojamą importuojant XML formato failus, kuriuose yra pasirinktinių atributų. Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“. Prieš pradėdami, atsisiųskite ir vietiniame diske išsaugokite failą IncomingDocumentToLearnHowToHandleOptionalAttributes.xml iš [„Microsoft“ atsisiuntimo centro](https://go.microsoft.com/fwlink/?linkid=874684).

1.    Eikite į **Visos darbo sritys** > **Elektroninės ataskaitos**.
2.    Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**. Jei nematote šio konfigūracijos teikėjo, atlikite procedūros [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md) veiksmus.
3.    Spustelėkite **Ataskaitų konfigūracijos**.

## <a name="create-a-new-data-model-configuration"></a>Sukurti naują duomenų modelio konfigūraciją
1.    Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą.
2.    Lauke **Pavadinimas** įveskite „xml failo importavimo modelis“.
3.    Spustelėkite **Sukurti konfigūraciją**.
4.    Spustelėkite **Konstruktorius**.
5.    Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.
6.    Lauke **Pavadinimas** įveskite „Šaknis“.
7.    Spustelėkite **Pridėti**.
8.    Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.
9.    Lauke **Pavadinimas** įveskite „Sąrašas“.
10.    Lauke **Elemento tipas** pasirinkite **Įrašų sąrašas**.
11.    Spustelėkite **Pridėti**.
12.    Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.
13.    Lauke **Pavadinimas** įveskite „Kodas“.
14.    Lauke **Elemento tipas** pasirinkite **Eilutė**.
15.    Spustelėkite **Pridėti**.
16.    Spustelėkite **Įrašyti**.
17.    Uždarykite puslapį.
18.    Spustelėkite **Keisti būseną**.
19.    Spustelėkite **Baigta**.
20.    Spustelėkite **Gerai**.

## <a name="create-a-format-for-data-import"></a>Duomenų importavimo formato kūrimas
1.    Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą.
2.    Lauke **Naujas** įveskite „Formatas pagal duomenų modelį xml failo importavimo modelis“.
3.    Lauke **Pavadinimas** įveskite „XML failo importavimo formatas“.
4.    Lauke **Palaikomas duomenų importavimas** pasirinkite **Taip**.
5.    Spustelėkite **Sukurti konfigūraciją**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Formato, skirto analizuoti gaunamą XML formato failą, kūrimas
1.    Spustelėkite **Konstruktorius**.
2.    Spustelėdami **Įtraukti šakninį elementą** atidarykite išplečiamąjį dialogo langą.
3.    Medyje pasirinkite **XML \ Elementas**.
4.    Lauke **Pavadinimas** įveskite „šaknis“.
5.    Spustelėkite **Gerai**.
6.    Spustelėdami **Įtraukti** atidarykite išplečiamąjį dialogo langą.
7.    Medyje pasirinkite **XML \ Elementas**.
8.    Lauke **Pavadinimas** įveskite „dokumentas“.
9.    Lauke **Daugialypumas** pasirinkite **Vienas daug**.
10.    Spustelėkite **Gerai**.
11.    Medyje pasirinkite **root\document**.
12.    Spustelėdami **Įtraukti** atidarykite išplečiamąjį dialogo langą.
13.    Medyje pasirinkite **XML \ Atributas**.
14.    Lauke **Pavadinimas** įveskite „ID“.
15.    Spustelėkite **Gerai**.
16.    Spustelėkite **Įrašyti**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Formato susiejimo, skirto įrašyti išanalizuotą informaciją į duomenų modelį, kūrimas
1. Spustelėkite **Susieti formatą su modeliu**.
2. Spustelėkite **Naujas**.
3. Lauke **Apibrėžtis** įveskite arba pasirinkite reikšmę.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Lauke **Pavadinimas** įveskite „Susiejimas“.
6. Spustelėkite **Įrašyti**.
7. Spustelėkite **Konstruktorius**.
8. Medyje išplėskite **format**.
9. Medyje išplėskite **format\root: XML Element(root)**.
10.    Medyje pasirinkite **format\root: XML Element(root)\document: XML Element 1..* (dokumentas)**.
11.    Spustelėkite **Susieti**.
12.    Medyje išplėskite **format\root: XML Element(root)\document: XML Element 1..* (dokumentas)**.
13.    Medyje pasirinkite **format\root: XML Element(root)\document: XML Element 1..* (dokumentas)\id**.
14.    Medyje išplėskite **List = format.root.document**.
15.    Medyje pasirinkite **List = format.root.document\Code**.
16.    Spustelėkite **Susieti**.
17.    Spustelėkite **Įrašyti**.
18.    Uždarykite puslapį.
 
## <a name="run-format-mapping"></a>Formato susiejimo vykdymas
1. Spustelėkite **Vykdyti**.
2. Spustelėkite **Naršyti** ir pasirinkite **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
3. Spustelėkite **Gerai**.

> [!NOTE]
> Pasirinktas failas nebuvo importuotas, nes kuriant formatus manoma, kad esama elemento „dokumentas“ atributo „id“, bet importuotame faile tokio atributo nėra.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Formato struktūros, skirtos tvarkyti XML atributą kaip pasirinktinį, modifikavimas
1. Uždarykite puslapį.
2. Medyje išplėskite **root\document**.
3. Medyje pasirinkite **root\document\id**.
4. Lauke **Tuščia trūkstamo atributo eilutė** pasirinkite **Taip**.
5. Spustelėkite **Įrašyti**.
 
## <a name="run-format-mapping-to-test-changes"></a>Formato susiejimo vykdymas siekiant patikrinti keitimus
1. Spustelėkite **Susieti formatą su modeliu**.
2. Spustelėkite **Vykdyti**.
3. Spustelėkite **Naršyti** ir pasirinkite failą **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
4. Spustelėkite **Gerai**.
5. Peržiūrėkite sugeneruotą failą. 

> [!NOTE]
> Tas pats failas buvo importuotas kaip formato dizainas. Dabar elemento „dokumentas“ atributą „ID“ laikykite pasirinktinu.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
