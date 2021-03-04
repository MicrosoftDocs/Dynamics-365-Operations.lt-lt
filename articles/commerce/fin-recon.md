---
title: Finansinis suderinimas mažmeninės prekybos parduotuvėse
description: Šioje temoje aprašomas finansinis derinimas mažmeninės prekybos parduotuvių EKA punktuose, skirtose „Microsoft Dynamics 365 Commerce”.
author: anpurush
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5d0520f35391f76b52fd8a333033b0d7ba4f7fe1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414236"
---
# <a name="financial-reconciliation-in-retail-stores"></a>Finansinis suderinimas mažmeninės prekybos parduotuvėse

[!include [banner](includes/banner.md)]

„Microsoft Dynamics 365 Commerce” versijoje 10.0.10 ir ankstesnėse versijose, pardavimo vietos (EKA) kliento teikiamos funkcijos, kurios numato dienos pabaigos procesus mažmeninės prekybos parduotuvėse, leidžia parduotuvių darbuotojams ir parduotuvių vadovams atlikti dienos pabaigos operacijas. Pavyzdžiui, jie gali atlikti mokėjimo priemonių deklaracijas, anoniminių uždarymų pamainas, derinti pamainų operacijas ir uždaryti pamainas. Tačiau EKA nėra galimybių baigti finansinę pamainų informaciją, kad būtų galima registruoti finansus „Commerce” būstinėje. Paprastai parduotuvių vadovai yra atsakingi už šios užduoties baigimą. Prieš jiems išsiregistruojant iš pamainos, jie turi peržiūrėti informaciją, atlikti visus reikalingus taisymus ir baigti tos pamainos bendrąsias sumas. Tada baigtos sumos turėtų būti registruojamos „Commerce” būstinės finansiniuose moduliuose.

Be to, „Commerce” 10.0.10 ir ankstesnėse versijose, parduotuvių vadovai gali peržiūrėti ir atlikti tam tikrus išrašo eilučių koregavimus „Commerce” būstinėje. Tačiau sugebėjimas yra ribotas, o parduotuvės vadovai retai turi prieigą prie „Commerce” būstinės kliento. Be to, finansinio mažmeninės prekybos išrašo peržiūra ir derinimas gali būti atliekamas tik tada, kai ataskaitos kuriamos „Commerce” būstinėje. Tačiau šis procesas paprastai yra naktinis procesas. Todėl parduotuvės vadovai turi palaukti, kol baigsis pamaina, kai „Commerce” būstinėje sukuriamos finansinės mažmeninės prekybos ataskaitos.

„Commerce” 10.0.11 ir vėlesnėse versijose parduotuvės vadovai gali peržiūrėti, koreguoti ir baigti savo pamainas pačioje EKA kliento programoje. Šie duomenys naudojami norint kurti ir registruoti finansinius mažmeninės prekybos išrašus „Commerce” būstinėje.

> [!NOTE]
> Funkcija, susijusi su finansiniu derinimu mažmeninės prekybos parduotuvėse veikia tik, jei yra įjungta kūrimo funkcija paremta informacijos santrauka. Daugiau informacijos rasite [Užsakymo, paremto informacijos santrauka, kūrimas mažais etapais, skirtas mažmeninės prekybos operacijoms](trickle-feed.md).

## <a name="set-up-financial-reconciliation"></a>Finansinio derinimo nustatymas

Atlikite šiuos veiksmus norėdami naudotis finansinio suderinimo funkcija.

1. **Funkcijų valdymas** darbo srityje įjunkite **Mažmeninės prekybos ataskaitos – Informacijos santrauka mažais etapais** funkciją.
1. EKA funkcijų profilį, skirtą atitinkamai parduotuvei, nustatykite **Įjungti finansinį derinimą parduotuvėje** parinktį į **Taip**.

## <a name="more-information-about-financial-reconciliation"></a>Daugiau informacijos apie finansinį suderinimą

Kai yra įjungta finansinio suderinimo funkcija, kai kurie parametrai, apibrėžti **Ataskaita/uždarymas** „FastTab” skirtuke **Mažmeninės prekybos parduotuvės** puslapio „Commerce” būstinėje yra sinchronizuojami pagal kanalo duomenų bazę. Vykdomas tas pats skaičiavimo kriterijų ir sumų ribų rinkinys, naudojamas mažmeninės prekybos ataskaitose.

Kai **Baigti pamainą** operacija pradedama, sistema patikrina, ar sugretintos sistemos apskaičiuotos sumos ir deklaruotos sumos sutampa. Jei jie skiriasi, o skirtumas viršija nurodytas ribines vertes, vartotojas yra paraginamas ir gali atlikti būtinus koregavimus.

Galima atlikti kiekvienos mokėjimo priemonės koregavimus. Kai mokėjimo priemonė pasirenkama, vartotojas gali peržiūrėti įvairių operacijų tipų bendrąsias sumas ir redaguoti konkretaus operacijos tipo bendrąsias sumas. Redaguojant sistema parodo pradinę apskaičiuotą sumą ir perrašytą tos operacijos tipo sumą. Redagavimo proceso metu vartotojas taip pat gali fiksuoti pastabas. Pastabas galima naudoti audito tikslais.

Vartotojai gali nepaisyti tikrinimo raginimų ir pranešimų, o gali baigti pamainą. Tačiau, jei vartotojas ignoruoja tikrinimo raginimus, atsiranda tie patys klausimai, kuriuos reikės nustatyti, kai pamaina registruoja finansinius išrašus „Commerce” būstinėje.

EKA **Baigti pamainą** operacija taip pat patikrina, kad visos autonominės duomenų bazės operacijos sinchronizuojamos su kanalo duomenų baze. Jei operacijos nesinchronizuojamos, vartotojas gauna įspėjamąjį pranešimą, nes dėl šios situacijos sistemos sumos gali būti klaidingai apskaičiuotos. Tokiu atveju vartotojas gali baigti **Baigti pamainą** operaciją ir pabandyti sinchronizuoti autonomines duomenų bazės operacijas su kanalo duomenų baze. Taip pat vartotojas gali neautomatiniu būdu koreguoti sistemos apskaičiuotas sumas, kad atsiskaitytų už nesinchronizuotas operacijas, kad teisingas finansinių skaičių rinkinys būtų baigtas ir užregistruotas. 

Kai informacijos santraukos mažais etapais registracija yra naudojama, kad operacijų registracija atskiriama nuo finansų registracijas, galite suderinti trūkstamų autonominių operacijų sistemos apskaičiuotų sumas. Tokiu būdu užtikrinate, kad finansai visada būtų apskaitomi ir registruojami tinkamai, neatsižvelgiant į trūkstamas operacijas. Autonominės operacijos gali būti sinchronizuojamos su kanalo duomenų baze ir „Commerce” būstine, o vėliau užregistruojamos atskirai nuo finansų registravimų.

Pamainos finansinio suderinimo išsami informacija sinchronizuojama su „Commerce” būstine naudojant P užduotį.

„Commerce” būstinės finansinės mažmeninės prekybos išrašuose nepateiktos apskaičiuotos sumos, kad būtų parodyta išrašų eilučių išsami informacija. Vietoj to, baigtos sumos EKA kliente naudojamos kurti ir registruoti finansines mažmeninės prekybos ataskaitas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]