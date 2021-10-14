---
title: Matavimo vienetų valdymas
description: Ši tema aprašo, kaip apibrėžti matavimo vienetą, pateikti vieneto vertimus ir jo aprašą ir apibrėžti susijusių vienetų konvertavimo taisykles.
author: t-benebo
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e13897396810507bb4b2cbb415b873eb3dd7f4e8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565525"
---
# <a name="manage-units-of-measure"></a>Matavimo vienetų valdymas

[!include [banner](../../includes/banner.md)]

Ši tema aprašo, kaip apibrėžti matavimo vienetą, pateikti vieneto vertimus ir jo aprašą ir apibrėžti susijusių vienetų konvertavimo taisykles.

## <a name="open-the-units-page"></a>Atidarykite vienetų puslapį

Norėdami sukurti ir dirbti su jūsų sistemoje galimais matavimo vienetais, eikite į Organizacijos **administravimo \> vienetų \> nustatymo \>** vienetus.

Likusiuose šios temos skyriuose aprašoma, ką galima padaryti **vienetų** puslapyje.

## <a name="create-standard-units-and-conversions"></a>Standartinių vienetų ir konvertavimų kūrimas

Jei jūsų sistemoje dar nėra dažniausiai naudojamų metrinės sistemos ir (arba) JAV įprastinio sistemos (USCS) matavimo vienetų, vieneto nustatymo vedlys gali padėti greitai pradėti pradedant nuo pagrindinių vienetų apibrėžimų ir konvertavimų. Norėdami užbaigti vedlį, veiksmų srityje pasirinkite Vienetų kūrimo vedlys, tada **vykdykite** ekrano instrukcijas.

## <a name="create-or-edit-a-unit-of-measure"></a>Kurti ar redaguoti matavimo vienetą

Norėdami kurti arba redaguoti matavimo vienetą, atlikite šiuos veiksmus.

1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Norėdami redaguoti esamą vienetą, pasirinkite jį sąrašo srityje.
    - Norėdami sukurti naują vienetą, pasirinkite **Nauja** veiksmų juostoje.

1. Naujojo įrašo antraštėje nustatykite toliau pateiktus laukus:

    - **Vienetas** – įveskite identifikatorių arba simbolį, naudotiį vienetą nurodyti sistemos kalba. Šis ID arba simbolis paprastai yra įprasta vieneto santrumpa, pvz., *kiekvienai* arba *centimetro* cm.
    - **Aprašas** – Įveskite matavimo vieneto aprašomąjį pavadinimą sistemos kalba. Šis pavadinimas paprastai yra visas vieneto pavadinimas, pvz., *Kiekvienas* arba *Centimetras*.

1. „FastTab“ **Bendra** nustatykite toliau pateikiamus laukus.<!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - **Vieneto** klasė – pasirinkite vieneto matavimo ypatybę (pvz., ilgį, sritį, masę arba kiekį).
    - **Vienetų sistema** – pasirinkite matavimo sistemą, kuriai priklauso vienetas (*Metriniai vienetai* arba *Jungtinių Valstijų pasirinktiniai* vienetai).
    - **Pagrindinis** vienetas – nustatykite šią *pasirinktį kaip Taip* , jei norite dabartinį vienetą naudoti kaip pagrindinį vieneto klasės vienetą. Šiuo atveju vienetų klasėje turite nurodyti tik pagrindinio vieneto ir kiekvieno papildomo vieneto konvertavimo koeficientą. Sistema gali konvertuoti visus tos vieneto klasės vienetus. Todėl lengviau nustatyti konvertavimą.

        Pavyzdžiui, jei galonas yra pagrindinis tūrio vieneto klasės vienetas, turite nustatyti tik konvertavimo koeficientus iš litro į galoną ir *iš* pinto į galoną. Sistema taip pat gali konvertuoti iš kvorto į pint.

        Vienoje vieneto klasėje gali būti tik vienas pagrindinis vienetas.

    - **Sistemos** vienetas – nustatykite šią *pasirinktį kaip Taip* , jei norite dabartinį vienetą naudoti kaip prisiimtus visus matavimus klasės vienete. Pavyzdžiui, jei laukas, kuris naudojamas kiekiui įvesti, neleidžia nurodyti vieneto (jei vartotojas nepasirinko vieneto), sistema naudoja vienetą, kuris nustatytas kaip kiekio vieneto klasės sistemos *vienetas*. Vienoje vieneto klasėje gali būti tik vienas sistemos vienetas.
    - **Dešimtainis tikslumas – nurodykite dešimtainių dalių vietų, kurios yra nurodytos dabartiniam vienetui arba kurias reikia** apvalinti, skaičių.

1. Veiksmų srityje pasirinkite **Įrašyti**.

## <a name="define-unit-translations"></a>Apibrėžti vieneto vertimus

Norėdami nurodyti ID arba simbolio vertimus ir matavimo vieneto aprašymą, atlikite šiuos veiksmus.

1. Sukurkite arba pasirinkite vienetą, į lauką kursite vertimus.
1. Veiksmų srityje pasirinkite **Vieneto tekstai**.

    Rodomas **puslapis** Vieneto tekstai. Šį puslapį naudojate pasirinkto vieneto ID arba simbolio vertimams nustatyti. Tada šiuos vertimus galima naudoti išoriniuose dokumentuose kliento ar tiekėjo kalba.

1. Veiksmų srityje pasirinkite **Naujas**.
1. **Kalba** – laukelyje pasirinkite kalbą norėdami išversti vieneto ID ar simbolį.
1. Į **lauką** Tekstas įveskite vieneto ID arba simbolio vertimą pasirinkta kalba.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Uždarykite puslapį.
1. **Veiksmų srityje** pasirinkite **Išversti vienetų aprašai**.

    Rodomas **išverstų vienetų** aprašų puslapis. Šį puslapį naudojate norėdami nustatyti pasirinkto vieneto aprašus konkrečia kalba.

1. Veiksmų srityje pasirinkite **Naujas**.
1. **Kalba** – laukelyje pasirinkite kalbą norėdami išversti vieneto ID ar aprašą.
1. Į **Aprašą** Tekstas įveskite vieneto ID arba aprašo vertimą pasirinkta kalba.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Uždarykite puslapį.

## <a name="define-unit-conversion-rules"></a>Apibrėžti vieneto konvertavimo taisykles

Norėdami nustatyti konvertavimo tarp matavimo vienetų taisykles, atlikite šiuos veiksmus.

1. Sukurkite arba pasirinkite vienetą norėdami nustatyti vertimo taisykles.
1. Veiksmų srityje pasirinkite **Vieneto pavertimas**.

    Atidaromas puslapis **Vienetų konvertavimas**. Naudojate šį puslapį, kad nustatytumėte pasirinkto vieneto keitimą į ir iš kitų vienetų vieneto klasėje.

1. Pasirinkite vieną iš šių skirtukų priklausomai nuo konvertavimo tipo, kurį norite nustatyti:

    - **Standartiniai konvertavimai** – nustatyti standartines konvertavimo taisykles visiems produktams.
    - **Konvertavimai klasės viduje** – nustatyti su konkrečiu produktu taikomas tos pačios vieneto klasės vienetų konvertavimo taisykles.
    - **Konvertavimai klasės viduje** – nustatyti su konkrečiu produktu taikomas tos pačios vieneto klasės vienetų konvertavimo taisykles.

1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Norėdami sukurti naują keitimą, pasirinkite **Nauja** įrankių juostoje.
    - Norėdami redaguoti esamą konvertavimą, pasirinkite konvertavimą tinklelyje ir įrankių **juostoje** pasirinkite Redaguoti.

1. Pasirodžiusiame iškritusiame teksto lange nustatykite tolesnius laukus:

    - **Produktas** – pasirinkite konkretų produktą, kurį taikomas konvertavimas. Šis laukas galimas tik konvertavimams tarp klasių ir tarp klasių.
    - **Formulės** maketas – palikti šį lauką nustatytą kaip *Paprastas,* kad būtų nurodytas paprastas konvertavimas, turintis vieną koeficientą. Norėdami nustatyti *sudėtingesnę* lygtį, nustatykite ją išplėstiniu nustatymu. Išplėstinių lygčių formatas skiriasi, atsižvelgiant į vieneto klasę.
    - **Nuo vieneto** – šiame lauke rodomas pasirinktas vienetas. Paprastai vertės keisti nereikia. (Jei vertę pakeisite, turite atidaryti langą **Pasirinkto vieneto** vienetų konvertavimo puslapis, kuriame galite peržiūrėti naują konvertavimą jį įrašius.)
    - **Į vienetą** – pasirinkite vienetą, į jį konvertuoti.
    - **Apvalinimas** – pasirinkti, kaip apvalinti trupmenas, remiantis pasirinkto vieneto **Dešimtainio tikslumo** pasirinkto vieneto vertė (*Iki artimiausios*, *Aukštyn*, ar *Žemyn*).
    - **Konvertavimo formulė – naudoti likusius laukus išplečiamojo dialogo lango viršuje, norint nurodyti dviejų** vienetų konvertavimo formulę. Galimi laukai skiriasi atsižvelgiant į pasirinktą vieneto klasę ir formulės maketą.

1. Pasirinkite **Gerai**.
1. Uždarykite puslapį.

> [!TIP]
> Taip pat galite nustatyti vieneto konvertavimą produkto variantui. Dėl išsamesnės informacijos, žr. [Produkto varianto matavimo vieneto konvertavimas](../uom-conversion-per-product-variant.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
