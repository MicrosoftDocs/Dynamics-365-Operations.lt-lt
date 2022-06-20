---
title: Naudojimo valdymo skelbimų skelbimų lentos
description: Šiame straipsnyje paaiškinama, kaip naudoti naudojimo valdymo skelbimų skelbimų skydą, norint stebėti elektroninių SF išrašymo paslaugos naudojimą ir toliau bus suderinama.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3fad2acea373e96092208ce06edb31f1a862912d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875977"
---
# <a name="usage-management-dashboard"></a>Naudojimo valdymo skelbimų skelbimų lentos

[!include [banner](../includes/banner.md)]

Naudojimo **valdymo skelbimų** funkcija padeda stebėti elektroninių SF išrašymo tarnybos naudojimą, todėl jūsų organizacija gali toliau naudoti savo organizaciją kas mėnesį. Atitikimas nustatomas apskaičiuojant pateikimo apimtį ir lyginant jį su įsigytu pateikimų kiekiu, norint nustatyti bet kokius nuokrypius tarp įsigyto tūrio ir naudomo tūrio.

Skelbimų srityje yra šie indikatoriai:

- Vienas išlaidų indikatorius, kurį galite naudoti licencijos atitikimo tikslais stebėti suvartojimą:

    - Naudojimas per mėnesį (eksportas)

- Trys veikimo indikatoriai, kuriuos galite naudoti norėdami sekti elektroninių SF išrašymo paslaugos naudojimą valdymo tikslais:

    - Naudojimas pagal funkciją
    - Naudojimas pagal aplinką
    - Naudojimas per mėnesį (importas)

## <a name="measurement-scope"></a>Matavimo tikslas

- Matavimo vienetai: 

    Naudojimo **valdymo skelbimų** skelbimų srityje pateikiamas verslo dokumentai ir importuotos elektroninės SF.

- Organizacija: 

    Skaičiavimas susumuojamas Microsoft Dynamics pagal jūsų organizacijos nuomininkų ID, neatsižvelgiant į 365 Dynamics 365 Supply Chain Management finansų egzempliorių skaičių arba juridinių subjektų skaičių, kur elektroninių SF išrašymo paslauga įgalinta.


## <a name="indicator-usage-per-month-export"></a>Indikatorius: naudojimas per mėnesį (eksportas)

Šis indikatorius pateikia informaciją apie elektronines SF, kurias jūsų organizacija išrašo nustatytą laikotarpį.

### <a name="scope"></a>Aprėptis
- Verslo dokumentų, pateiktų iš „Electronic Invoicing“ ir „ Supply Chain Management“ į elektroninių SF išrašymo paslaugą, skaičius neatsižvelgiant į eilučių, kurios yra tuose verslo dokumentuose, skaičių.
- Pateiktų verslo dokumentų, kuriuos sėkmingai apdorojo elektroninių SF išrašymo tarnyba, skaičius. Dokumentas laikomas sėkmingai apdorotu, kai baigiamas veiksmų srautas, apibrėžtas funkcijos nustatyme.

> [!NOTE]
> Kai elektroninė SF pateikiama išorinei žiniatinklio tarnybai, skaičiavimas nepriklauso nuo žiniatinklio tarnybos apdorojimo rezultatų (priimta, atmesta arba schemos tikrinimo klaida). Jei žiniatinklio tarnyba gavo ir atsakė į elektroninių SF išrašymo tarnybos užklausą, pateikimas laikomas galiojančiu inventorizacija.

- **Išimtis:** verslo dokumentai neskaičiuojami, jei jie iš naujo pateikiami iš finansų ir „Supply Chain Management“ į „Electronic Invoicing“ tarnybą, pvz., scenarijuose, kuriuose norint pakeisti elektroninės SF būseną reikia iš naujo pateikti tą patį verslo dokumentą. Pvz., Brazilijos elektroninės SF išdavimas skaičiuojamas kaip galiojantis, bet jo atšaukimo užklausa neskaičiuojama.


### <a name="calculation"></a>Skaičiavimas

Balanso skaičiavimas apskaičiuojamas taip:

Balansas = Laisvas + Nupirkta – Naudojama

Kur:

- Laisvas:
  
    Nemokamas verslo dokumentų kiekis, kurį klientas gali pateikti per mėnesį. Joje yra 100 verslo dokumentų, kuriuos galima pateikti elektroninių SF išrašymo tarnybai, paketas. Laisvas tūris nėra kaupiamas ir bet koks likęs balansas nėra sumuojamas į kitą laikotarpį.
  
- Nupirkta:
  
    Joje yra 1000 verslo dokumentų, kuriuos galima pateikti elektroninių SF išrašymo tarnybai, paketas. Šis paketas turi būti įsigytas jūsų organizacijai kas mėnesį. Įsigytas tūris nėra kaupiamas ir bet koks likęs balansas nėra sumuojamas į kitą laikotarpį.
  
- Naudojamas: 

    Verslo dokumentų pateikimo elektroninių SF išrašymo tarnybai pagal apibrėžtus kriterijus skaičius.
   
> [!IMPORTANT]
> Jei jūsų organizacija planuoja viršyti 100 laisvos formos pateikimų per mėnesį apimtį, pirkite didžiausią apimtį, taip užtikrinsite, kad išliktų suderinama su Elektroninių SF išrašymo tarnybos Microsoft licencijavimo strategija.
>
> Šiuo metu įsigytas kiekis turi būti įvestas rankiniu būdu, atsižvelgiant į įsigijimo datą, kaip keletą pakuočių iš 1000 pateikimų.

## <a name="indicator-usage-by-feature"></a>Indikatorius: naudojimas pagal priemonę

Šis indikatorius rodo elektroninių SF išrašymo priemonių naudojimą elektroninių SF išdavimui nustatytą laikotarpį.

- Skaičiavimas:
  
    Naudota = skaičius, kiek kartų kiekviena elektroninio SF išrašymo priemonė buvo naudojama pateikiant verslo dokumentus elektroninių SF išrašymo tarnybai.

## <a name="indicator-usage-by-environment"></a>Indikatorius: naudojimas pagal aplinką

Šis indikatorius rodo elektroninių SF išrašymo paslaugų aplinkos naudojimą apibrėžtu laikotarpiu.

- Skaičiavimas:
    
    Naudota = skaičius, kiek kartų kiekviena elektroninio SF išrašymo tarnybos aplinka buvo naudojama pateikiant verslo dokumentus elektroninių SF išrašymo tarnybai.

## <a name="indicator-usage-per-month-import"></a>Indikatorius: naudojimas per mėnesį (importas)

Šis indikatorius rodo elektroninių SF pagal elektroninių SF išrašymo paslaugą „Finance and Supply Chain Management“ per nurodytą laikotarpį.

- Aprėptis:

    Elektroninės SF, importuojamos į „Finance and Supply Chain Management“, neatsižvelgiant į eilučių, kurias sudaro tos elektroninės SF, skaičių.

- Skaičiavimas:

    Gauta = importuotų elektroninių SF į „Finance and Supply Chain Management“.

## <a name="functions"></a>Funkcijos
### <a name="purchase"></a>Pirkimas

Skirtuke **Mėnesio naudojimas (eksportas)** pasirinkite **Pirkimas** norėdami rankiniu būdu užregistruoti įsigytų pateikimų sumą.

Nurodytą datą pasirinkite **Nauja** ir įveskite tą datą **įsigytų** pakuočių skaičių.

**Kiekis** yra skaičiuojamas taip:

Kiekis = Pakuotės * 1000

Apskaičiuotas **kiekis** rodomas pirkta **naudojant** indikatorių Naudojimas **mėnesiui (eksportas)**.

### <a name="update"></a>Atnaujinimas

Veiksmų srityje pasirinkite **Naujinti,** kad būtų atnaujinti skaičiavimai ir atnaujinti duomenys, rodomi puslapyje ir diagramoje.

### <a name="reset-history-data"></a>Iš naujo nustatyti istorijos duomenis

Veiksmų srityje pasirinkite Iš naujo nustatyti **retrospektyvos duomenis**, kad atnaujinumėte duomenų bazę, iš kurios skaičiuojami indikatoriai.




> [!NOTE]
> Naudojimo **valdymo skelbimų** skelbimų srityje nerodyti piniginės sumos. Vietoj to ji rodo tik suskaičiuotų pateikimų ir importuotų dokumentų apimtį.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
