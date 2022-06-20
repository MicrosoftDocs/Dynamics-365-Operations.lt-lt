---
title: Nuomų valdymas per nuomos importavimo sistemą
description: Šiame straipsnyje paaiškinama, kaip naudoti nuomos importo sistemą norint vienu metu koreguoti kelias nuomas.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeaseImportHeader
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8cf81ccf61e62ac49e6cb90d13ca5fe50147cc76
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894970"
---
# <a name="manage-leases-through-the-lease-import-framework"></a>Nuomų valdymas per nuomos importavimo sistemą

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip naudoti nuomos importavimo sistemą, kad vienu veiksmu būtų galima koreguoti kelias nuomas. Naudodami šią funkciją galite sutaupyti laiko ir taip pat galite užtikrinti tikslesnius koregavimus, sumažindami žmogiškosios klaidos galimybę. Be to, šią galimybę galima prijungti Microsoft Dynamics 365 finansų su išoriniais duomenų subjektais, kad duomenys būtų efektyviai įkeliami.

Gali būti naudojami šie duomenų objektai, siekiant integruoti turto nuomą su išorinėmis sistemomis.

- Nuomos paruošimas
- Mokėjimo sutarties sudarymas
- Vykdomosios sutarties paruošimas

Galite naudoti importavimo procesą, norėdami koreguoti nuomą, atnaujinti nefinansinę informaciją arba pridėti naujų nuomos išlaidų. Galite peržiūrėti ir redaguoti nuomos duomenis prieš juos importuodami.

Sistema gali vykdyti šiuos tris procesus, naudodama nuomos importavimo paketą.

| Proceso tipas  | aprašymas |
|---------------|-------------|
| Pridėti įrašą    | Perkelta nuoma, kurios proceso tipas yra šis, sukuria nuomą sistemoje. Kad būtų galima patvirtinti mokėjimus, turi būti patvirtinta neautomatiniu būdu, o pradinis pripažinimo žurnalo įrašas turi būti registruojamas neautomatiniu būdu po perkėlimo. |
| Atnaujinti įrašą | Perkelta nuomos sutartis, kurios šio proceso tipo atnaujinimo lauko vertės jau yra sistemoje. Atnaujinami tik tie laukai, kurie pasirinkti puslapyje **Atnaujinimo laukų pasirinkimas**. Rekomenduojame pasirinkti nefinansinius laukus puslapyje **Atnaujinimo laukų pasirinkimas**, nes šio proceso tipas nekoreguoja nuomos. |
| Koreguoti įrašą | Perkelta nuoma, kurios proceso tipas yra šis, koreguoja nuomą. Dėl šio pakeitimo finansinė nuoma keičiama. Po to, kai nuoma apdorojama, sistema sukuria naują įmokų grafiką naudodama naujus duomenis iš nuomos importavimo paketo. Sistema nepatvirtina darbo grafiko arba įrašo pataisymų žurnalo įrašą. |

Po to, kai informacija įkeliama naudojant darbo sritį **Duomenų valdymas**, atidarykite puslapį **Importavimo antraštė** (**Turto nuoma \> Nuomos importavimo sistema \> Importavimo antraštė**). Šiame puslapyje pateikiami visi anksčiau nurodyti trys duomenų objektai.

Norėdami peržiūrėti nuomos išdėstymo duomenis prieš vykdydami apdorojimą, pasirinkite **Išdėstymo duomenys**.

Funkcija lyginti leidžia palyginti įrašą, kurį importuojate, su atitinkamu įrašu, kuris jau yra jūsų sistemoje. Norėdami palyginti atskirą nuomos įrašą, pasirinkite nuomą ir pasirinkite **Lyginti**. Turite atlikti šį veiksmą, kad būtų sugeneruota ataskaita **Skirtumai**, prieš perkeldami nuomos įrašus. Funkcija lyginti sulygina išdėstymo duomenų vertes su nuomos, kuri šiuo metu yra sistemoje, vertėmis.

> [!NOTE]
> Funkcija Palyginti neveiks, jei nuomos proceso tipas yra **Įtraukti įrašą**, kadangi nėra ko palyginti su šia nuoma.
>
> Norėdami palyginti kelias nuomas tuo pačiu metu, pasirinkite **Turto nuoma \> Nuomos importavimo sistema \> Periodiškai** ir pasirinkite **Palyginti**.

Kiekvienam objektui galite peržiūrėti skirtumus tarp to, kas šiuo metu yra sistemoje, ir kas yra išdėstymo lentelėse. Kiekvienam išdėstymo lentelės objektui pasirinkite **Peržiūrėti skirtumus**. Pasirodys dialogo langas, rodantis dabartinę vertę ir siūlomą išdėstymo vertę.

Taip pat galite atnaujinti išdėstymo vertę pakeisdami ją stulpelyje **Nauja reikšmė** ir tada pasirinkdami **Atnaujinti išdėstymą**.

Norėdami užtikrinti, kad įrašus būtų galima įtraukti į sistemą neįkeliant klaidų, galite patvirtinti nuomą. Prieš perkeliant nuomos įrašą, sistema vykdo kelis tikrinimus, siekdama užtikrinti, kad įrašas bus sėkmingai importuotas. Norėdami patikrinti atskirą nuomą, pasirinkite **Patikrinti**.

> [!NOTE]
> Norėdami patikrinti kelias nuomas tuo pačiu metu, pasirinkite **Turto nuoma \> Nuomos importavimo sistema \> Periodiškai** ir pasirinkite **Tikrinti**.

Norėdami apdoroti atskirą nuomą, puslapyje **Importavimo antraštė** pasirinkite **Perkelti nuomos įrašus**. Kai perkeliama nuoma, sistema atlieka veiksmą, kuris nurodytas lauke **Proceso tipas**.

> [!NOTE]
> Norėdami perkelti kelias nuomas tuo pačiu metu, pasirinkite **Turto nuoma \> Nuomos importavimo sistema \> Periodiškai** ir pasirinkite **Perkelti**.

Palyginus nuomas, galite vykdyti ataskaitą, kad peržiūrėtumėte kiekvienos nuomos, įtrauktos į importavimo ID, skirtumus. Norėdami paleisti vienos nuomos ataskaitą, pasirinkite nuomos duomenis, o tada pasirinkite **Lyginti ir peržiūrėti ataskaitą \> Skirtumų ataskaita**.

> [!NOTE]
> Norėdami palyginti kelias nuomas tuo pačiu metu, pasirinkite **Turto nuoma \> Nuomos importavimo sistema \> Periodiškai** ir tada – **Palyginti**. 

## <a name="set-up-update-fields"></a>Atnaujinamų laukų nustatymas

Jei naudojate nuomos importavimo sistemą norėdami atnaujinti nuomą, o proceso tipas yra **Atnaujinti įrašą**, galite pasirinkti konkrečius atnaujintinus laukus.

1. Pasirinkite **Turto nuoma \> Nuomos importavimo sistema \> Sąranka \> Atnaujinimo laukų pasirinkimas**.
2. Pasirodžiusiame puslapyje pasirinkite atnaujintus laukus ir pasirinkite žalią rodyklę, kad perkeltumėte jas į sąrašą **Pasirinkti laukai**. Tik sąrašo **Pasirinkti laukai** laukai gali būti atnaujinami naudojant nuomos importavimo paketą.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
