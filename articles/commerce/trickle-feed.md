---
title: Nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas parduotuvių operacijoms
description: Šioje temoje aprašomas nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas operacijoms „Microsoft Dynamics 365 Commerce”.
author: analpert
ms.date: 12/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3a7fd8698d7123403cf9092a4a4bf810595d795b
ms.sourcegitcommit: f82372b1e9bf67d055fd265b68ee6d0d2f10d533
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/14/2021
ms.locfileid: "7921250"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Nuolatiniu duomenų perdavimu mažais kiekiais pagrįstas užsakymų kūrimas, skirtas parduotuvių operacijoms

[!include [banner](includes/banner.md)]

Jei naudojama „Microsoft Dynamics 365 Commerce“ 10.0.5 ir naujesnė versija, rekomenduojame visus išrašų registravimo procesus perkelti į nuolatiniu duomenų perdavimu mažais kiekiais pagrįsto išrašų registravimo procesus. Su nuolatinio duomenų perdavimo mažais kiekiais funkcijos naudojimu yra siejama didelė našumo ir verslo nauda. Pardavimo operacijos apdorojamos visą dieną. Mokėjimo priemonės ir grynųjų pinigų valdymo operacijos apdorojamos finansinėje ataskaitoje dienos pabaigoje. Naudojant nuolatinio duomenų perdavimo mažais kiekiais funkciją nuolat apdorojami pardavimo užsakymai, sąskaitos faktūros ir mokėjimai. Todėl atsargos, įplaukos ir mokėjimai gali būti atnaujinami ir atpažįstami beveik realiuoju laiku.

## <a name="use-trickle-feed-based-posting"></a>Nuolatiniu duomenų perdavimu mažais kiekiais pagrįsto registravimo naudojimas

> [!IMPORTANT]
> Prieš įjungdami nuolatiniu duomenų perdavimu mažais kiekiais pagrįstą registravimą, turite įsitikinti, kad nėra apskaičiuotų ir neužregistruotų išrašų. Prieš įjungdami funkciją užregistruokite visus išrašus. Darbo srityje **Parduotuvės finansai** galite patikrinti, ar yra atvirų išrašų.

Norėdami įjungti mažmeninės prekybos operacijų nuolatiniu duomenų perdavimu mažais kiekiais pagrįstą registravimą, darbo srityje **Funkcijų valdymas** įjunkite funkciją **Mažmeninės prekybos išrašai – duomenų perdavimas mažais kiekiais**. Išrašai bus padalinti į du tipus: operacijų išrašai ir finansinės ataskaitos.

### <a name="transactional-statements"></a>Operacijos išrašai

Numatyta, kad operacijos išrašų apdorojimas būtų vykdoma dideliu dažniu visą dieną, kad dokumentai būtų sukuriami operacijas įkėlus į „Commerce“ būstinę. Operacijos įkeliamos iš parduotuvių į „Commerce“ būstinę paleidus **P užduotį**. Taip pat turite paleisti užduotį **Tikrinti parduotuvės operacijas**, kad patikrintumėte operacijas ir jas būtų galima naudoti operacijų išraše.

Suplanuokite, kad šios užduotys būtų vykdomos labai dažnai:

- Norėdami apskaičiuoti operacijų išrašų duomenis, paleiskite užduotį **Atlikti operacijų išrašų paketinį skaičiavimą** (**„Retail“ ir „Commerce“ \> „Retail“ ir „Commerce“ IT \> EKA registravimas \> Atlikti operacijų išrašų paketinį registravimą**). Atliekant šią užduotį visos neužregistruotos ir patvirtintos operacijos paimamos ir įtraukiamos į naują operacijų išrašą.
- Norėdami atlikti paketinį operacijų išrašų registravimą, paleiskite užduotį **Atlikti operacijų išrašų paketinį registravimą** (**„Retail“ ir „Commerce“ \> „Retail“ ir „Commerce“ IT \> EKA registravimas \> Atlikti operacijų išrašų paketinį registravimą**). Atliekant šią užduotį bus paleistas registravimo procesas ir sukurti pardavimo užsakymai, pardavimo sąskaitos faktūros, mokėjimų žurnalai, nuolaidų žurnalai ir neužregistruotų išrašų, kuriuose nėra klaidų, pajamų ir išlaidų operacijos. 

### <a name="financial-statements"></a>Finansinės ataskaitos

Finansinės ataskaitos apdorojimas turi būti atliekamas dienos pabaigoje. Šio tipo išrašų apdorojimas palaiko tik uždarymo metodą **Pamaina** ir paims tik uždarytas pamainas. Išrašai apsiriboja finansiniu derinimu. Bus sukurti tik mokėjimo priemonių apskaičiuotos sumos ir operacijos sumos skirtumo sumų žurnalai ir kitų grynųjų pinigų valdymo operacijų žurnalai.

Planuokite šių finansinės ataskaitos užduočių pradžios ir pabaigos laikus pagal numatomą dienos pabaigą:

- Norėdami apskaičiuoti finansinę ataskaitą, paleiskite užduotį **Atlikti finansinių ataskaitų paketinį skaičiavimą** (**„Retail“ ir „Commerce“ \> „Retail“ ir „Commerce“ IT \> EKA registravimas \> Atlikti finansinių ataskaitų paketinį skaičiavimą**). Atliekant šią užduotį visos neužregistruotos finansinės operacijos bus surinktos ir įtrauktos į naują finansinę ataskaitą.
- Norėdami atlikti finansinių ataskaitų paketinį registravimą, paleiskite užduotį **Atlikti finansinių ataskaitų paketinį registravimą** (**„Retail“ ir „Commerce“ \> „Retail“ ir „Commerce“ IT \> EKA registravimas \> Atlikti finansinių ataskaitų paketinį registravimą**).

### <a name="manually-create-statements"></a>Išrašų kūrimas rankiniu būdu

Operacijų ir finansinių ataskaitų tipus galima kurti ir rankiniu būdu. 

1. Eikite į **„Retail“ ir „Commerce“ \> Kanalai \> Parduotuvės** ir pasirinkite **Išrašai**. 
2. Pasirinkite **Naujas** ir tada pasirinkite išrašo tipą, kurį norite sukurti. Puslapyje **Išrašai** esančiuose laukuose bus rodomi duomenys, kurie yra tiesiogiai susiję su pasirinktu išrašo tipu, ir dalyje **Išrašų grupė** esantys veiksmai nurodys tiesiogiai susijusius veiksmus.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
