---
title: Failų importavimas XML formatu su pasirinktiniais atributais
description: Šioje temoje pateikiama informacija apie tai, kaip kuriami ER formatai, kurie nurodo XML atributus, kad būtų analizuojami gaunami elektroniniai dokumentai XML formatu.
author: NickSelin
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 81156cf13e003a67fde0a73bdcd69b2c997f23a33c464fad82132f7768f8a99f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757302"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a>Failų importavimas XML formatu su pasirinktiniais atributais

[!include [banner](../includes/banner.md)]

Galite sukurti elektroninių ataskaitų (ER) formatus, skirtus analizuoti gaunamus elektroninius dokumentus XML formatu. Sukurtame ER formate tam tikri XML elementų atributai gali būti nurodyti kaip pasirinktiniai. Taigi galėsite tinkamai tvarkyti gaunamus failus naudodami tokius XML atributus arba jų nenaudodami. Tada galite naudoti šių failų turinį programos duomenims atnaujinti.

Norėdami daugiau sužinoti apie šią funkciją, atlikite veiksmus, aprašytus temoje [(RCS) XML formato failų su pasirinktiniais atributais importavimas](tasks/import-files-xml-format-optional-attributes.md), kuri yra verslo proceso 7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677) dalis. Šį užduočių vedlį ir susietus failų pavyzdžius galite atsisiųsti iš [„Microsoft“ atsisiuntimo centras](https://go.microsoft.com/fwlink/?linkid=874684).


| Turinio aprašas       | Failas                                                         |
|---------------------------|--------------------------------------------------------------|
| Failo pavyzdys XML formatu | IncomingDocumentToLearnHowToHandleOptionalAttributes.xml     |
| Užduočių vedikliai                | RCS XML formato failų su pasirinktiniais atributais importavimas.axtr |


Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali kurti ER formato konfigūraciją, naudojamą importuojant XML formato failus, kuriuose yra pasirinktinių atributų. Norint atlikti šiuos veiksmus, pirmiausia reikia atlikti veiksmus, nurodytus procedūroje [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md). Prieš pradėdami, atsisiųskite ir vietiniame diske išsaugokite failą IncomingDocumentToLearnHowToHandleOptionalAttributes.xml iš „Microsoft“ atsisiuntimo centro (https://go.microsoft.com/fwlink/?linkid=874684).

1. Eikite į **Organizacijos administravimas** > **Darbo sritys** > **Elektroninės ataskaitos**.
2. Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**. Jei nematote šio konfigūracijos teikėjo, atlikite veiksmus, nurodytus temoje [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Spustelėkite **Ataskaitų konfigūracijos**.

## <a name="create-a-new-data-model-configuration"></a>Sukurti naują duomenų modelio konfigūraciją
1. Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą.
2. Lauke **Pavadinimas** įveskite „xml failo importavimo modelis“.
3. Spustelėkite **Sukurti konfigūraciją**.
4. Spustelėkite **Konstruktorius**.
5. Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.
6. Lauke **Pavadinimas** įveskite „Šaknis“.
7. Spustelėkite **Pridėti**.
8. Spustelėdami **Naujas** atidarykite išplečiamąjį dialogo langą.
9. Lauke **Pavadinimas** įveskite „Sąrašas“.
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
1. Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą.
2. Lauke **Naujas** įveskite „Formatas pagal duomenų modelį xml failo importavimo modelis“.
3. Lauke **Pavadinimas** įveskite „xml failo importavimo formatas“. 
4. Lauke **Palaikomas duomenų importavimas** pasirinkite **Taip**.
5. Spustelėkite **Sukurti konfigūraciją**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Formato, skirto analizuoti gaunamą XML formato failą, kūrimas
1. Spustelėkite **Konstruktorius**.
2. Spustelėdami **Įtraukti šakninį elementą** atidarykite išplečiamąjį dialogo langą.
3. Medyje pasirinkite **XML \ Elementas**.
4. Lauke **Pavadinimas** įveskite „šaknis“.
5. Spustelėkite **Gerai**.
6. Spustelėdami **Įtraukti** atidarykite išplečiamąjį dialogo langą.
7. Medyje pasirinkite **XML \ Elementas**.
8. Lauke **Pavadinimas** įveskite „dokumentas“.
9. Lauke **Daugialypumas** pasirinkite **Vienas daug**.
10.    Spustelėkite **Gerai**.
11.    Medyje pasirinkite **root\document**.
12.    Spustelėdami **Įtraukti** atidarykite išplečiamąjį dialogo langą.
13.    Medyje pasirinkite **XML \ Atributas**.
14.    Lauke **Pavadinimas** įveskite „id“.
15.    Spustelėkite **Gerai**.
16.    Spustelėkite **Įrašyti**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Formato susiejimo, skirto įrašyti išanalizuotą informaciją į duomenų modelį, kūrimas
1.    Spustelėkite **Susieti formatą su modeliu**.
2.    Spustelėkite **Naujas**.
3.    Lauke **Apibrėžtis** įveskite arba pasirinkite reikšmę.
4.    Lauke **Pavadinimas** įveskite „Susiejimas“.
5.    Spustelėkite **Įrašyti**.
6.    Spustelėkite **Konstruktorius**.
7.    Medyje išplėskite **format**.
8.    Medyje išplėskite **format\root: XML Element(root)**.
9.    Medyje pasirinkite **format\root: XML Element(root)\document: XML Element 1..* (dokumentas)**.
10.    Spustelėkite **Susieti**.
11.    Medyje išplėskite **format\root: XML Element(root)\document: XML Element 1..* (dokumentas)**.
12.    Medyje pasirinkite **format\root: XML Element(root)\document: XML Element 1..* (dokumentas)\id**.
13.    Medyje išplėskite **List = format.root.document**.
14.    Medyje pasirinkite **List = format.root.document\Code**.
15.    Spustelėkite **Susieti**.
16.    Spustelėkite **Įrašyti**.
17.    Uždarykite puslapį.

## <a name="run-format-mapping"></a>Formato susiejimo vykdymas
1. Spustelėkite **Vykdyti**.
2. Spustelėkite **Naršyti** ir pasirinkite failą **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
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
5. Peržiūrėkite sugeneruotą failą. Atkreipkite dėmesį, kad tas pats failas buvo importuotas kaip formato dizainas. Dabar elemento „dokumentas“ atributą „ID“ laikykite pasirinktiniu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]