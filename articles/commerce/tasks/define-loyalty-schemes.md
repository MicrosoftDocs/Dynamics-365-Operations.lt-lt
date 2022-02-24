---
title: " Nustatyti lojalumo planus"
description: Ši procedūra nurodo, kaip nustatyti lojalumo planą.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2bec8653c05d7684202c0e63d049ddb517e12834
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414388"
---
# <a name="define-loyalty-schemes"></a> Nustatyti lojalumo planus

[!include [banner](../includes/banner.md)]

Ši procedūra nurodo, kaip nustatyti lojalumo planą. Lojalumo planai yra lojalumo programos atlygio uždarbio ir naudojimo taisyklės. Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.

1. Eikite į Mažmeninė prekyba ir prekyba > Klientai > Lojalumas > Lojalumo planai.
2. Spustelėkite Naujas.
3. Lauke Plano ID įveskite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Galima sukurti kelias lojalumo programos lojalumo schemas. Lojalumo programos gali būti skirtos visiems kanalams arba tik kanalų poaibiui.  
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Spustelėkite Įrašyti.
9. Spustelėkite Pridėti eilutę.
10. Lauke Veiklos tipas pasirinkite parinktį.
    * Pasirinkite Produktų pirkimas pagal sumą, jei norite, kad klientai atlygio taškus gautų už tai, kiek išleidžia. Pasirinkite Produktų pirkimas pagal kiekį, jei norite, kad klientai atlygio taškus gautų už tai, kiek produktų perka.  Pasirinkite Pardavimo operacijų skaičius, jei norite, kad klientai gautų atlygį už kiekvieną pardavimo operaciją, nepaisant, kas arba kiek perkama.  
    * Pasirinkite kategoriją. Kategorija riboja produktų, kuriems šį atlygio taisyklė taikoma, skaičių.  
    * Palikite šį lauką tuščią, jei norite, kad atlygio taisyklė būtų taikoma visiems produktams.  
11. Lauke Veiklos suma / kiekis įveskite skaičių.
    *  Jei veiklos tipas yra Pardavimo operacijų skaičius, visada turėtumėte naudoti reikšmę „1,0“. Veiklos tipas yra Pirkimas pagal sumą arba Pirkimas pagal kiekį, operacijos, kurių vertė yra mažesnė už įvestą vertę, atlygio taisyklės nesuaktyvins. Pavyzdžiui, jei veiklos tipas yra Pirkimas pagal sumą, o jūs įvedate „10,00“, tada ši atlygio taisyklė neskirs taškų pardavimo operacijai, kurios vertė „9,00“.  
12. Lauke Veiklos valiuta įveskite reikšmę.
13. Lauke Atlygio taškų ID spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
14. Sąraše spustelėkite saitą pasirinktoje eilutėje.
15. Lauke Atlygio taškai įveskite skaičių.
    * Sumos tipo gautos atlygio taškų sumos bus įrašomos su dešimtainėmis dalimis. Pvz., jei uždarbio taisyklė nurodo skirti 1 atlygio tašką už 1 išleistą Kanados dolerį, o klientas išleido 1,25 Kanados dolerio, tada klientas gaus 1,25 atlygio taškų. Kiekio tipo gautos atlygio taškų sumos bus įrašomos tik sveikaisiais skaičiais. Pvz., jei uždarbio taisyklė nurodo skirti 1 atlygio tašką už 1 išleistą Kanados dolerį, o klientas išleido 1,25 Kanados dolerio, tada klientas gaus 1,0 atlygio taškų.  
16. Spustelėkite Įrašyti.
17. Spustelėkite Pridėti eilutę.
    * Apmokėjimo taisyklės naudojamos, kai naudojamas lojalumo mokėjimo būdas.  
18. Lauke Atlygio taškų ID spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Rodomi tik išnaudojami atlygio taškai.  
19. Sąraše spustelėkite saitą pasirinktoje eilutėje.
20. Lauke Atlygio taškai įveskite skaičių.
21. Lauke Naudojimo tipas pasirinkite parinktį.
    * Pasirinkus Mokėjimas pagal sumą, lauko Suma arba kiekis reikšmė bus laikoma valiutos verte. Šiuo atveju mokėjimo valiutos vieneto naudojamų atlygio taškų suma yra fiksuotas dydis. Pasirinkus Mokėjimas pagal kiekį, lauko Suma arba kiekis reikšmė bus laikoma kiekio verte. Šiuo atveju prekės kiekio naudojamų atlygio taškų suma yra fiksuotas dydis, tačiau valiutos suma gali skirtis, jei skiriasi to pačio kiekio kaina, sumokėta už prekes naudojant atlygio už lojalumą taškus. Lojalumo taškų nuolaidos apmokėjimo tipą galima naudoti tik jei įjungtas šaliai / regionui būdingų funkcijų konfigūracijos raktas „Rusija“, o EKA funkcijų šablonų ISO kodas yra „RU“.  
    * Pasirinkite kategoriją. Kategorija riboja produktų, kuriems šį naudojimo taisyklė taikoma, skaičių.  
    * Palikite šį lauką tuščią, jei norite, kad naudojimo taisyklė būtų taikoma visiems produktams.  
22. Lauke Suma arba kiekis įveskite skaičių.
23. Lauke Valiuta surinkite reikšmę.
24. Spustelėkite Įrašyti.
25. Spustelėkite Pridėti eilutę.
    * Turimų organizacijos mazgų sąraše pasirinkite vieną ar daugiau mazgų ir perkelkite juos į sąrašą Pasirinkti organizacijos mazgai, spustelėdami rodyklę tarp abiejų sąrašų.  
26. Spustelėkite GERAI.
27. Spustelėkite Įrašyti.
    * Bet kada pakeitę lojalumo plano kanalus, turite paleisti užduotį Apdoroti lojalumo planus. Tokiu būdu bus atnaujinti kanalų lojalumo planai.  

