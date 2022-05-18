---
title: PVM mokėjimo kūrimas
description: PVM sudengimo ir registravimo užduoties procedūra PVM balansus sudengia PVM sąskaitose ir juos koresponduoja į PVM sudengimo sąskaitą už tam tikrą laikotarpį.
author: twheeloc
ms.date: 01/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c388a8f98cd4581abe2ec13d8922e232321e4039
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735868"
---
# <a name="create-a-sales-tax-payment"></a>PVM mokėjimo kūrimas

[!include [banner](../../includes/banner.md)]

PVM sudengimo ir registravimo užduoties procedūra PVM balansus sudengia PVM sąskaitose ir juos koresponduoja į PVM sudengimo sąskaitą už tam tikrą laikotarpį.

1. Eikite į **Mokestis > Deklaracijos > PVM > Sudengti ir užregistruoti PVM**.
2. Norėdami atidaryti **peržvalgą**, lauke Sudengimo laikotarpis pasirinkite išplečiamąjį mygtuką.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Lauke **Pradžios data** įveskite datą. Jei puslapyje **DK parametrai** nepasirenkate parinkties **įtraukti taisymus**, galima apdoroti skirtingų versijų sudengimą. **Originalas** yra pirmasis laikotarpio intervalo sudengimas, kurį laikotarpio intervalui galima apdoroti tik vieną kartą. Paskutiniai pataisymai sudengs PVM operacijas, kurios buvo užregistruotos sukūrus pradinę versiją.
5. Lauke **Operacijos data** įveskite datą.
6. Pasirinkite **Gerai**. PVM **mokėjimų ataskaita spausdinama** norint peržiūrėti sudengtas laikotarpio PVM operacijas.

Pradėdami nuo 10.0.24 **finansų** **·** **·** **versijos**, galite praleisti PVM mokėjimų ataskaitą, kuri generuojama tiesiogiai po to, kai PVM periodinė procedūra užregistruojama naudojant atskirų PVM mokėjimo ataskaitos generavimą iš PVM sudengimo funkcijos, kuri yra funkcijų valdymo darbo srityje.

Kai priemonė įgalinama, baigus sudengimo procesą, nespausdinamas joks PVM mokėjimo ataskaita. Jūs gaunate tokį pranešimą "PVM sudengimas ir registravimas baigtas. Kvitas 'xxxx, m/d/mmmm'.

Vis dar galite rankiniu būdu paleisti PVM **mokėjimo ataskaitą nueiti į TaxInquiries** > **ir reportsSales** > **mokesčių užklausasSales** > **mokesčių mokėjimai**.

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
