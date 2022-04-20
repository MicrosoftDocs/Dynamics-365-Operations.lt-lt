---
title: Globalizavimo funkcijos kūrimas
description: Šioje temoje paaiškinama, kaip sukurti globalizavimo funkciją.
author: dkalyuzh
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 94038b0eb412632c348081bbf467f44310d9e955
ms.sourcegitcommit: 6109fc2fe5f407363bb6f240d64b7214657f5914
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/15/2022
ms.locfileid: "8603031"
---
# <a name="create-a-globalization-feature"></a>Globalizavimo funkcijos kūrimas

[!include [banner](../includes/banner.md)]

Galite sukurti elektroninių SF išrašymo priemonę nuo pradžių arba galite ją pagrįsti esama priemone. Kai kuriate priemonę nuo pradžių, turite rankiniu būdu pridėti elektroninių ataskaitų (ER) konfigūracijas ir kitus komponentus, pvz., funkcijų nustatymą ir programos nustatymo informaciją. Kai kuriate priemonę, pagrįstą esama priemone, nauja funkcija perima visas pagrindinės funkcijos konfigūracijas ir parametrus. Galite peržiūrėti, ką iš pagrindinės priemonės nukopijuota į naują priemonę.

## <a name="create-a-feature-from-scratch"></a>Sukurti funkciją nuo pradžių

Šiame skyriuje paaiškinama, kaip sukurti elektroninių SF išrašymo funkciją, kai visuotiniame saugykloje nėra nė viena globalizavimo funkcija, skirta jūsų verslo scenarijams už lango.

Norėdami sukurti elektroninę SF išrašymo priemonę, atlikite šiuos veiksmus.

1. Prisijungti prie savo reguliavimo kongigūravimo paslaugų (RCS) paskyros.
2. RCS pasirinkus dalį **Funkcijos**, esančią darbo srityje **Funkcijos**, pasirinkite plytelę **Elektroninių SF priedas**.
3. Išplečiamajame **dialogo lange pasirinkite Įtraukti, tada pasirinkite naujos** funkcijos pasirinktį **.**
4. Įveskite elektroninių SF išrašymo priemonės pavadinimą ir aprašymą.
5. Pasirinkite **Sukurti funkciją**. Dešinėje puslapio pusėje rodoma pirmoji naujos funkcijos versija, kurios būsena – Juodraštis **·**.

    Tada turite pridėti ER konfigūracijas ir priemonių nustatymus. Prieš įtraukdami naujas arba esamas ER formato konfigūracijas, įsitikinkite, kad jos yra jūsų vietinėje RCS saugykloje.

6. Pasirinkite elektroninių SF išrašymo priemonę, su kurią dirbate.
7. Skirtuke **Konfigūracijos** pasirinkite **Įtraukti**.
8. Konfigūracijos tinklelyje **naršykite** ir pasirinkite formato konfigūracijas, kurių reikia pardavimo galimybių apdorojimui (pvz., norėdami generuoti elektroninių SF failus arba apdoroti atsakymus iš išorinių žiniatinklio tarnybų).
9. Pasirinkite **Gerai**. Dabar galite naudoti konfigūracijas pardavimo galimybių apdorojimo veiksmams. Daugiau informacijos ieškokite Darbas [su konfigūracijoje](e-invoicing-work-configurations.md).
10. Norėdami pridėti elektroninės SF išrašymo priemonės nustatymą, sukurkite **ją naujos** priemonės puslapio **skirtuke Nustatymai**. Daugiau informacijos ieškokite Darbas [su funkcijų nustatymais](e-invoicing-feature-setup.md).
11. Užbaikite nustatymą ir įdiekite elektroninių SF išrašymo funkciją aptarnavimo aplinkoje. Norėdami gauti daugiau informacijos, žr [. Atlikta, paskelbti ir įdiegti globalizavimo funkciją](e-invoicing-complete-publish-deploy-globalization-feature.md).

### <a name="create-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Kurti failo formato konfigūracijas, išvestas iš esamo SF modelio

Šį skyrių galite praleisti, jei nereikia kurti ER konfigūracijų, tačiau esamas versijas galite vėl naudoti kaip pagrindą.

Šioje procedūroje aprašoma, kaip sukurti rinkmenos formato konfigūracijas, reikalingas naujai elektroninio SF išrašymo funkcijai, kurią norite sukurti. Sukurkite elektroninės SF failo formato konfigūraciją ir bet kokias kitas rinkmenos formato konfigūracijas, reikalingas jūsų naujai elektroninių SF išrašymo funkcijai.

1. Prisijunkite prie jūsų RCS abonemento.
2. Darbo srityje **Elektroninės ataskaitos** pasirinkite plytelę **Ataskaitų konfigūracijos**.
3. Pasirinkite SF **modelį arba** Brazilijos scenarijų pasirinkite **iždo modelį**.
4. Pasirinkite **Kurti konfigūraciją**, tada išplečiamajame dialogo lange pasirinkite pasirinktį **Formatas pagal duomenų modelio SF**.
5. Įveskite paketo pavadinimą ir formato konfigūracijos aprašymą.
6. Lauke **Formato tipas** pasirinkite failo plėtinio tipą.
7. Duomenų modelio **apibrėžimo lauke** pasirinkite šakninį struktūrą, su kurią susiesite formatą. Pavyzdžiui, **InvoiceCustomer** naudojamas kliento SF formatams.
8. Pasirinkite **Kurti konfigūraciją**.
9. Pasirinkite naują formato konfigūraciją.
10. Pasirinkite **konstruktorių** ir naudodami formato kūrimo įrankį konfigūruokite rinkmenos maketą, kad jis atitiktų rinkmenos formato specifikacijas.
11. Uždarykite puslapį.
12. Elemente **Versijos** rinkitės **Keisti būseną** \> **Užbaigta**.
13. Pasirinkite **Keisti būseną**\> **Bendrai** naudoti, kad būtų publikuojate formato konfigūraciją visuotiniame saugykloje.

Naujos failo formato konfigūracijos turi būti bendrai naudojamos Microsoft domene, kad jas galėtų suvartoti elektroninių SF išrašymo tarnyba.

1. Pasirinkite formato konfigūraciją, su kurią dirbate. Konfigūracijos būsena turi būti **Bendrai** naudojama.
2. Skirtuke **Versijos** pasirinkite **Išplėstinis bendrinimas** \> **visuotinė saugykla**.
3. Skirtuke **Bendrinama su** pasirinkite **Organizacija**.
4. Norėdami bendrai **naudoti** formato konfigūraciją su **Microsoft microsoft.com**, lauke Parametrai įveskite pavadinimą.
5. Pasirinkite **Gerai**.

## <a name="create-a-feature-that-is-based-on-an-existing-feature"></a>Sukurkite priemonę, pagrįstą esama funkcija

1. Prisijunkite prie jūsų RCS abonemento.
2. RCS pasirinkus dalį **Funkcijos**, esančią darbo srityje **Funkcijos**, pasirinkite plytelę **Elektroninių SF priedas**.
3. Konfigūracijos teikėjo **lauke patikrinkite**, ar pasirinktas aktyvus konfigūracijos teikėjas. Tokiu būdu nauja elektroninių SF išrašymo priemonė bus rodoma sąraše po to, kai ji bus sukurta. Jei aktyvus konfigūravimo teikėjas nėra pasirinktas, nauja funkcija bus filtruojama iš sąrašo.
4. Pasirinkite **Įtrauki**, tada išplečiamojo dialogo lango lauke pasirinkite **Pagrįstas esama versija** parinktį.
5. Įveskite funkcijos pavadinimą ir aprašymą.
6. **Lauke Bazinė priemonė** pasirinkite pagrindinę priemonės versiją.
7. Pasirinkite **Sukurti funkciją**. Priemonė sukurta ir jos būsena yra **Juodraštis**.
8. Peržiūrėkite funkcijų komponentus, kad nustatytumėte, kurie naujiniai yra reikalingi:

    - Peržiūrėti konfigūracijas, jei reikia pritaikyti ER formatus ir jų susiejimą su priemonės versijos formato susiejimais.
    - Peržiūrėkite nustatymą, jei reikia pritaikyti funkcijos versijos **skirtuką** Veiksmai, **·** **Pritaikymo** taisyklės arba Kintamieji.

9. Užbaikite nustatymą ir įdiekite elektroninių SF išrašymo funkciją aptarnavimo aplinkoje. Norėdami gauti daugiau informacijos, žr [. Atlikta, paskelbti ir įdiegti globalizavimo funkciją](e-invoicing-complete-publish-deploy-globalization-feature.md).
