---
title: Kokybės valdymo bandymo instrumentai
description: Šioje temoje aprašoma, kaip sukurti tikrinimo priemones, kurias galima naudoti kokybės užsakymų „Microsoft Dynamics 365 Supply Chain Management“ bandymams.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39624a9f00829e551fe3790a024155b6104318ef5cc1c582ab263c3868462063
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774107"
---
# <a name="quality-management-test-instruments"></a>Kokybės valdymo bandymo instrumentai

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip sukurti tikrinimo priemones, kurias galima naudoti kokybės užsakymų „Microsoft Dynamics 365 Supply Chain Management“ bandymams.

Naudokitės bandymo instrumentų puslapiu, norėdami nurodyti ir peržiūrėti informaciją apie **įrenginius**, naudojamus kokybės užsakymų bandymams vykdyti. Bandymo instrumentai pasirinktini. Tačiau jie gali padėti kokybės darbuotojams žinoti, kurį įrenginį ar įrankį jie turėtų naudoti atlikdami konkretų testą.

## <a name="test-instrument-example"></a>Bandymo prietaiso pavyzdys

Atliekate įvairius elektros komponentų bandymus. Kai kurie bandymai yra skirti komponentų išeigai, vienas bandymas skirtas jų temperatūrai, o vienas bandymas skirtas jų svoriui. Kiekvienam bandymui atlikti naudojami skirtingi įrankiai, įrenginiai arba įranga. Pavyzdžiui, kasos skaitiklis yra naudojamas matuoti pagal kilometrelį, temperatūrai matuoti naudojamas skaitiklis, o svarstyklės naudojamos svoriui matuoti. Galite konfigūruoti kiekvieną iš šių įrenginių kaip tikrinimo prietaisą ir nurodyti matavimo vienetą, į kurį turi būti įrašyti tikrinimo rezultatai. Pvz., kasos skaitiklio rezultatai įrašomi į kilogramus, o už svarus arba kilogramus neįrašomi į metrą, o rezultatai iš svarų ar kilogramų įrašomi fiksuotais laipsniais Fahrenheit arba degrees.

## <a name="create-a-test-instrument"></a>Naujo testavimo kūrimas

1. Pasirinkite **Atsargų valdymas \> Sąranka \> Kokybės kontrolė \> Instrumentų testas**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį. Tada nustatykite šiuos laukus naujai eilutei:

    - **Bandymo instrumentas** – įveskite unikalų tikrinimo prietaiso ID arba pavadinimą.
    - **Aprašas** – įveskite išsamų bandymo instrumento aprašą.
    - **Vienetas** – pasirinkite vienetą, kuris bus matavimo vienetas. Tikslumo **laukas** nustatomas automatiškai, remiantis jūsų pasirinktu vienetu.

1. Uždarykite puslapį.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Kokybės valdymo bandymas](quality-tests.md)
- [Kokybės valdymo bandymo grupės](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
