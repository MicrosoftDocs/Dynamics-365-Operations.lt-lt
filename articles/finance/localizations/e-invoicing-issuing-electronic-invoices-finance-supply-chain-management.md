---
title: Išduokite elektroniens sąskaitas „Finance and Supply Chain Management“
description: Ši tema paaiškina, kaip išduoti elektronines sąskaitas „Microsoft Dynamics 365 Finance“ ir „Dynamics 365 Supply Chain Management“ per elektroininių sąskaitų priedus.
author: gionoder
ms.date: 03/29/2021
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
ms.openlocfilehash: 24909c2a2505724c159e939535c1d57cb66e48629862bebb32b3d72c0eb06c97
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752131"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Elektroninių SF išdavimas „Finance“ ir „Supply Chain Management“

[!include [banner](../includes/banner.md)]

Ši tema paaiškina, kaip išduoti elektronines sąskaitas „Microsoft Dynamics 365 Finance“ ir „Dynamics 365 Supply Chain Management“ per elektroininių sąskaitų priedus.


## <a name="feature-activation"></a>Funkcijų aktyvinimas

Norėdami išduoti elektroninės sąskaitas per elektroninių sąskaitų priedą, turite įjungti funkciją „Finance“ ir „Supply Chain Management”.

Kiekviena funkcija atitinka konkrečią elektroninių sąskaitų funkciją, kuri atitinka elektroninių sąskaitų reikalavimus konkrečiai šaliai / regionui.

Tolesnėje lentelėje parodytas funkcijų sąrašas, kurį gali palaikyti elektroninės sąskaitos priedas.

| Pavadinimas / vardas ir (arba) pavardė                                              | Šalis/regionas |
|---------------------------------------------------|----------------|
|Austrijos elektroninė sąskaita faktūra                        |Austrija         |
|Belgijos elektroninė sąskaita faktūra                         |Belgija         |
|„NF-e Federal“ – Brazilijos elektroninė sąskaita faktūra       |Brazilija          |
|NFS-e – Brazilijos paslaugų (miesto) elektroninė sąskaita faktūra|Brazilija          |
|Danijos elektroninė sąskaita faktūra                          |Danija         |
|Egipto elektroninė sąskaita faktūra                        |Egiptas           |
|Estijos elektroninė sąskaita faktūra                        |Estija         |
|Suomijos elektroninė sąskaita faktūra                         |Suomija         |
|Prancūzijos elektroninė sąskaita faktūra                          |Prancūzija          |
|Vokietijos elektroninė sąskaita faktūra                          |Vokietija         |
|PEPPOL – visuotinė elektroninė sąskaita faktūra                 |Bendroji          |
|Italijos elektroninė sąskaita faktūra                         |Italija           |
|CFDI – Meksikos elektroninė sąskaita faktūra                  |Meksika          |
|Nyderlandų elektroninė sąskaita faktūra                           |Olandija     |
|Norvegijos elektroninė sąskaita faktūra                       |Norvegija          |
|Ispanijos elektroninė sąskaita faktūra                         |Ispanija           |

Kai naudojama senesnė elektroninių SF išrašymo funkcija, kuri palaikoma šalies / regiono lokalizavimo aprėptyje, aktyvinus vieną iš šių funkcijų išjungiama senesnė funkcija ir įjungiamos elektroninės SF, kurios išduodamos naudojant elektroninių SF išrašymo priedą.

> [!IMPORTANT]
> Kai elektroninių SF išrašymo integravimo priemonė yra įgalinta, numatyta, kad nauja elektroninių SF išrašymo funkcija išsijungia. Funkcijos sąvoką galima naudoti norint pasirinktinai įgalinti naują juridinių subjektų patirtį, naudojant šaliai / regionui būdingas funkcijas. Parinktis **Visuotinis** valdo naują likusių šalių / regionų, kurie nėra įvardyti lentelėje, patirtį.

## <a name="submit-electronic-documents"></a>Pateikti elektroninius dokumentus

Elektroninių dokumentų pateikimo procesas atspindi vieną „Finance and Supply Chain Management“ ir elektroninio SF išrašymo ryšio tašką. Kiekvieno pateikimo įvykio metu ryšio srautai abiem kryptimis:

- **Iš „Finance and Supply Chain Management“ į elektroninių SF išrašymo priedo** – „Finance and Supply Chain Management“ sąskaitos faktūros siunčiamos į elektroninių SF išrašymo priedą. Jei reikia, jie taip pat siunčia kintamųjų, kurie sukonfigūruoti kaip elektroninių SF išrašymo priemonių dalis, turinį.
- **Iš elektroninių SF išrašymo priedo prie „Finance and Supply Chain Management“**– atsižvelgiant į elektroninių SF išrašymo priemonę, „Finance and Supply Chain Management“ gauna atnaujinimus iš elektroninių SF išrašymo papildomos informacijos apie anksčiau pateiktų SF apdorojimo rezultatus. Jie taip pat gauna kintamųjų, kurie sukonfigūruoti kaip elektroninių SF išrašymo priemonių dalis, turinį.

Norėdami pateikti elektroninius dokumentus prie elektroninių SF išrašymo priedo, „Finance and Supply Chain Management“ srityje eikite į **Organizacijos administravimas &gt; Periodiniai &gt; elektroniniai dokumentai &gt; Pateikti elektroninius dokumentus**.

Pradinis taškas yra užregistruota SF. Ši SF gali būti iš skirtingų kilmės šaltinių, pvz., pardavimo užsakymų, projekto SF arba laisvos formos SF.

Pateikimo procesą galima paleisti rankiniu būdu arba fone.

- **Rankinis vykdymas**– norėdami vykdyti neautomatiniu būdu, turite naudoti **Filtras** parinktį siekiant nurodyti dokumentų, kuriuos reikia pateikti, diapazoną. Puslapyje **Filtrai** galite konfigūruoti savo užklausą, kad pasirinktumėte užregistruotas SF, kurios turi būti pateiktos. Pasirinkę rankiniu būdu turite pradėti apdorojimo vykdymą ir palaukti, kol bus baigta vykdyti. Kai apdorojimas baigtas, veiksmų centro pranešimas rodo sėkmingai pateiktų elektroninių dokumentų skaičių.
- **Fono vykdymas** – fono vykdymas vykdomas nereikalaujant prisiregistruoti arba palikti atidarytą pateikimo dialogo langą. Galite suplanuoti vykdymą ir nustatyti vykdymo dažnumą.

## <a name="view-the-submission-logs"></a>Visų pateikimo žurnalų peržiūra

„Finance and Supply Chain Management“ srityje galite naudoti pateikimo žurnalus norėdami peržiūrėti pateikimo į elektroninių SF išrašymo priedą apdorojimo rezultatus. Eikite į **Organizacijos administravimas &gt; Periodiniai &gt; elektroniniai dokumentai &gt; Elektroninis dokumento pateikimas** ir tada **Dokumento tipas** pasirinkite vertę, pagal kurią bus filtruojamas žurnaluose rodomas SF tipas.

Galimos trys pateikimo būsenos:

- **Suplanuotas** – elektroninio SF išrašymo priedas, gautas iš „Finance and Supply Chain Management“ ir elektroninių SF išrašymo priemonės apdorojimas.
- **Baigta** – elektroninių SF išrašymo priedas sėkmingai apdorojo elektroninių SF išrašymo priemonę, kaip ji buvo sukonfigūruota ją vykdyti.
- **Nepavyko** – apdorojant elektroninių SF išrašymo priemonę įvyko elektroninio SF išrašymo priedo klaida arba jis buvo sustabdytas išimties.

> [!IMPORTANT]
> Pateikimo būsena nurodo apdorojimo, kurį elektroninio SF išrašymo priedas daro elektroninių SF išrašymo priemonėje, būseną. Ji nepaiso elektroninės SF galutinės būsenos.
>
> Pavyzdžiui, jei elektroninė SF turi būti pateikta išorinei žiniatinklio tarnybai patvirtinti, pateikimo būsena gali būti **Baigta**, tačiau elektroninės SF būsena gali būti **Atmesta**. Tokiu atveju, elektroninių SF išrašymo priedas sėkmingai apdorojo elektroninių SF išrašymo priemonę, kaip ji buvo sukonfigūruota apdoroti funkciją. Tačiau elektroninė SF buvo atmesta, nes ji neatitinka kriterijų, kuriuos žiniatinklio tarnyba nustatė SF patvirtinti.

Pateikimo žurnaluose yra šios papildomos funkcijos:

- **Pateikimo informacija** – peržiūrėkite išsamią pagrindinio pateikimo informaciją. Vizualizacija rodo visą veiksmų, kurie sukonfigūruoti naudojant elektroninio SF išrašymo priemonę, vykdymo žurnalą. Taip pat vartotojai gali atsisiųsti failus, kurie sukurti apdorojimo metu. Scenarijuose, kuriuose SF turi patvirtinti išorinė žiniatinklio tarnyba, vartotojai gali peržiūrėti SF būseną.
- **Susiję pateikimai** – peržiūrėti išsamią informaciją apie antrinius pateikimus.
- **Atšaukti pateikimus** – ši funkcija įgalina specialų pateikimo procesą scenarijuose, kuriuose elektroninę SF turi patvirtinti išorinė žiniatinklio tarnyba. Jis nurodo elektroninių SF išrašymo papildinį, kad žiniatinklio tarnybai būtų siunčiamas konkretus pranešimas, skirtas atšaukti patvirtintų elektroninių SF būseną žiniatinklio tarnybos duomenų bazėje.
- **Iš naujo pateikti dokumentą** – iš naujo pateikti elektroninį dokumentą, kuris jau buvo pateiktas elektroninio SF išrašymo priedui. Puslapyje **Pateikimo informacija** sukuriamas visiškai naujas žurnalas.
- **Siųsti susijusį pateikimą**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
