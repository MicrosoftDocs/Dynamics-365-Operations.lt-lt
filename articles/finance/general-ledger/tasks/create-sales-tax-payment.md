---
title: PVM mokėjimo kūrimas
description: PVM sudengimo ir registravimo užduoties procedūra PVM balansus sudengia PVM sąskaitose ir juos koresponduoja į PVM sudengimo sąskaitą už tam tikrą laikotarpį.
author: twheeloc
ms.date: 10/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54132ca4775482b4a06ff7e73125e804aff40cb4
ms.sourcegitcommit: f8b597b09157d934b62bd5fb9a4d05b8f82b5a0e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/26/2021
ms.locfileid: "7700118"
---
# <a name="create-a-sales-tax-payment"></a>PVM mokėjimo kūrimas

[!include [banner](../../includes/banner.md)]

PVM sudengimo ir registravimo užduoties procedūra PVM balansus sudengia PVM sąskaitose ir juos koresponduoja į PVM sudengimo sąskaitą už tam tikrą laikotarpį.

1. Eikite į **Mokestis > Deklaracijos > PVM > Sudengti ir užregistruoti PVM**.
2. Lauke **Sudengimo laikotarpis** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Lauke **Pradžios data** įveskite datą.
    - Jei puslapyje **DK parametrai** nepasirenkate parinkties **įtraukti taisymus**, galima apdoroti skirtingų versijų sudengimą. Pradinis yra pirmasis laikotarpio intervalo sudengimas, ir jį galima apdoroti tik vieną kartą per laikotarpio intervalą. Funkcija Paskutiniai pataisymai sudengs tas PVM operacijas, kurios užregistruotos sukūrus pradinę versiją.
5. Lauke **Operacijos data** įveskite datą.
6. Spustelėkite **Gerai**.

## <a name="performance-consideration"></a>Našumo pastabos

PVM mokėjimo procedūra gali užtrukti. Pagrindiniai faktoriai, paveikiantys procedūros našumą, yra sudengimo laikotarpio SF skaičius ir įrašų, kurie turi būti užregistruoti PVM sudengimo kvite, skaičius. Norėdami padidinti našumą, galite pasirinkti apeiti kai kurias funkcijas, kurių jums nereikia jūsų procese.

### <a name="enable-the-sales-tax-payment-performance-improvement-feature"></a>Įjungti PVM mokėjimo našumo tobulinimo funkciją

PVM mokėjimo našumo patobulinimo funkcija gali padėti pagerinti PVM mokėjimo procedūros efektyvumą, sukaupdami vieną eilutę, apskaitos valiutos sumą ir ataskaitų valiutos sumą PVM mokėjimo kvito eilutėse, kuriose yra **ta pati pagrindinė sąskaita, DK dimensija ir** valiuta.

1. Eikite į **Sistemos administravimas** \> **Darbo sritys** \> **Funkcijų valdymas**.
2. Skirtuke **Viskas** ieškokite ir pasirinkite **PVM mokėjimo našumo tobulinimą**.
3. Pasirinkite **Įjungti**.

### <a name="prevent-generation-of-offset-tax-transactions"></a>Neleisti atitinkamų mokesčių operacijų generavimo

Pagal numatytuosius nustatymus PVM mokėjimo kvitas užregistruoja korespondentinę PVM operaciją pagal kiekvieną PVM operaciją, sudengtą PVM mokėjimo procedūros metu. Šios korespondentinės PVM operacijos yra įtrauktos į **PVM / DK suderinimo** ataskaitą. Jie rodo neapmokėtą PVM operacijų balansą, kuris laikotarpio metu nesudengtas.

Tačiau korespondentinės PVM operacijos gali padidinti PVM mokėjimo procedūros neefektyvias paslaugas. Todėl skrydžio pavadinimas **TaxReportGenOffsetTaxTransPerRecordSetFlighting** gali būti suaktyvintas pagal poreikį. Šis skrydžio laikas gali padėti gerinti šalių ir regionų, išskyrus Tailandą, Lenkija, Vengrija, Lietuva, Malaizijos, Indija, Italija, Rusija, Čekijos Respublika, Estija ir Latvija, korespondentinės mokesčių operacijos generavimo našumą.

> [!NOTE]
> Jei mokesčių operacijos lentelėje yra pritaikytų laukų, skrydžio suaktyvinti negalima.

Kadangi **PVM / DK suderinimo** ataskaita paprastai naudojama tik vidinės kontrolės tikslais ir nėra būtina daugelyje mokesčių operacijų, galite pasirinkti negeneruoti korespondentinių PVM operacijų PVM mokėjimo kvite.

1. Pasirinkite **Mokestis** \> **Netiesioginiai mokesčiai** \> **PVM** \> **PVM sudengimo laikotarpiai**.
2. Pasirinkite atsiskaitymo laikotarpis.
3. **Bendrajame** „FastTab" nustatykite parinktį **Apsaugoti nuo korespondentinės mokesčių operacijos** generavimo kaip **Taip**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
