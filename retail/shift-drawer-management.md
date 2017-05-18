---
title: "Pamainos ir kasos stalčių valdymas"
description: "Šiame straipsnyje paaiškinta, kaip nustatyti ir naudoti dviejų tipų mažmeninės prekybos elektroninio kasos aparato (EKA) pamainas – bendrai naudojamą ir atskirą. Bendrai naudojimas pamainas keliose vietose gali naudoti keli vartotojai, o atskiras pamainas vienu metu gali naudoti tik vienas darbuotojas."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: bca8431e88ea73060c75774ae55611f95016e9a1
ms.contentlocale: lt-lt
ms.lasthandoff: 04/26/2017


---

# <a name="shift-and-cash-drawer-management"></a>Pamainos ir kasos stalčių valdymas

[!include[banner](includes/banner.md)]


Šiame straipsnyje paaiškinta, kaip nustatyti ir naudoti dviejų tipų mažmeninės prekybos elektroninio kasos aparato (EKA) pamainas – bendrai naudojamą ir atskirą. Bendrai naudojimas pamainas keliose vietose gali naudoti keli vartotojai, o atskiras pamainas vienu metu gali naudoti tik vienas darbuotojas.

Galimi du mažmeninės prekybos elektroninio kasos aparato (EKA) pamainų tipai: atskira ir bendrai naudojama. Atskiras pamainas vienu metu gali naudoti tik vienas darbuotojas. Bendrai naudojimas pamainas gali naudoti keli vartotojai keliose vietose. Todėl parduotuvėje galima veiksmingai sukurti keliems vartotojams skirtą vieną pamainą.

## <a name="standalone-shifts"></a>Atskiros pamainos
Atskiros pamainos naudojamos tradiciniu, pastoviu POS scenarijumi, kada kiekvieno EKA registro grynieji pinigai yra suderinamos atskirai. Pvz., parduotuvės aplinkoje paprastai yra keli fiksuoti EKA registrai, o kasininkas priskirtas kiekvienam registrui. Šiuo atveju kiekvienas registras greičiausiai naudoja atskirą pamainą, o kasininkas yra atsakingas už to registro kasos stalčiaus skyrelį arba fizinės formos grynuosius pinigus. Atskira pamaina apima visą veiklą tame registre per kasininko darbo pamainą. Veiklos gali apimti į kasos stalčiaus skyrelį padėtos sumos atidarymą, visas grynųjų pinigų išėmimo ir įdėjimo operacijas, pvz., inkasavimus ir srauto įrašą, ir mokėjimo priemonių deklaravimą pamainai pasibaigus.

### <a name="set-up-a-stand-alone-shift"></a>Atskiros pamainos nustatymas

Atskira pamaina priskiriama kasos stalčiaus lygyje. Šioje procedūroje paaiškinama, kaip nustatyt atskirą pamainą EKA registre.

1.  Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Kanalo nustatymas** &gt; **EKA nustatymas** &gt; **EKA šablonai** &gt; **Aparatūros šablonai**.
2.  Pasirinkite naudotiną atskirtos pamainos aparatūros šabloną.
3.  „FastTab“ **Stalčius** patikrinkite, ar parinktis **Bendrai naudojamos pamainos stalčius** yra nustatyta į **Ne**.
4.  Spustelėkite **Įrašyti**.
5.  Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Kanalo nustatymas** &gt; **EKA nustatymas** &gt; **Registrai**.
6.  Pasirinkite registrą, kuriam reikalinga atskira pamaina, ir tada spustelėkite **Redaguoti**.
7.  Lauke **Aparatūros šablonas** pasirinkite aparatūros šabloną, kurį pasirinkote atlikdami 2 veiksmą.
8.  Spustelėkite **Įrašyti**.
9.  Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikas**.
10. Pasirinkite **1090** pasiskirstymo grafiką, o tada spustelėkite **Vykdyti dabar**, kad sinchronizuotumėte EKA keitimus.

### <a name="use-a-stand-alone-shift"></a>Atskiros pamainos naudojimas

1.  Prisijunkite prie EKA.
2.  Jei neatidaryta jokia pamaina, pasirinkite **Atidaryti naują pamainą**.
3.  Pasirinkite operaciją **Deklaruoti pradinę sumą** ir nurodykite grynųjų pinigų sumą, kuri bus įtraukta į kasos stalčiaus skyrelį darbo dienos pradžioje.
4.  Atlikite keletą operacijų.
5.  Pasibaigus dienai pasirinkite **Deklaruoti mokėjimo priemonę**, kad deklaruotumėte kasos stalčiuje likusią grynųjų pinigų sumą.
6.  Įveskite grynųjų pinigų sumą, o tada spustelėkite **Įrašyti**, kad įrašytumėte mokėjimo priemonės deklaravimą.
7.  Pasirinkite **Uždaryti pamainą**, kad uždarytumėte pamainą.

**Pastaba.** Pamainos metu galima atlikti kitas operacijas, priklausomai nuo vykdomų verslo procesų. Galima atlikti operacijas **Pinigų įnešimas į kasą**, **Inkasavimas** ir **Mokėjimo priemonės šalinimas**, norint dienos metu arba prieš uždarant pamainą iš kasos stalčiaus skyrelio išimti pinigus. Jei kasos stalčiaus skyrelyje yra per mažai pinigų, galima naudoti operaciją **Srauto įrašas**, norint į kasos stalčiaus skyrelį įdėti grynųjų pinigų.

## <a name="shared-shifts"></a>Bendrai naudojamos pamainos
Bendrai naudojama pamaina naudojama tada, kai visą darbo dieną keli kasininkai bendrai naudoja kasos stalčių arba kasos stalčių rinkinį. Paprastai bendrai naudojama pamaina yra naudojama mobiliojoje EKA aplinkoje. Mobiliojoje aplinkoje nė vienas kasininkas nėra priskirtas arba atsakingas už vieną kasos stalčių. Visi kasininkai turi turėti galimybę užregistruoti pardavimą ir įdėti pinigų į artimiausią kasos aparatą. Tokiu atveju kasos stalčiai, kuriuos kasininkai bendrai naudoja, įtraukiami į bendrai naudojamą pamainą. Visi bendrai naudojamos pamainos kasos stalčiai įtraukiami į vieną pamainą, kad būtų galima vykdyti su grynųjų pinigų valdymu susijusias tos pamainos veiklas. Todėl pradinė pamainos suma turėtų apimti visuose į bendrai naudojamą pamainą įtrauktuose kasos stalčiuose esančią grynųjų pinigų sumą. Taip pat mokėjimo priemonės deklaravimas bus visuose į bendrai naudojamą pamainą įtrauktuose kasos stalčiuose esanti grynųjų pinigų suma. **Pastaba:** kiekvienoje parduotuvėje vienu metu galima atidaryti tik vieną bendrai naudojamą pamainą. Toje pačioje parduotuvėje galima naudoti bendrai naudojamas pamainas ir atskiras pamainas.

### <a name="set-up-a-shared-shift"></a>Bendrai naudojamos pamainos nustatymas

1.  Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Kanalo nustatymas** &gt; **EKA nustatymas** &gt; **EKA šablonai** &gt; **Aparatūros šablonai**.
2.  Pasirinkite naudotiną bendrai naudojamos pamainos aparatūros šabloną.
3.  „FastTab“ **Stalčius** parinktį **Bendrai naudojamos pamainos stalčius** nustatykite į **Taip**.
4.  Spustelėkite **Įrašyti**.
5.  Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Kanalo nustatymas** &gt; **EKA nustatymas** &gt; **Registrai**.
6.  Pasirinkite registrą, kuriam reikalinga bendrai naudojama pamaina, ir tada spustelėkite **Redaguoti**.
7.  Lauke **Aparatūros šablonas** pasirinkite aparatūros šabloną, kurį pasirinkote atlikdami 2 veiksmą.
8.  Spustelėkite **Įrašyti**.
9.  Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikas**.
10. Pasirinkite **1090** pasiskirstymo grafiką, o tada spustelėkite **Vykdyti dabar**, kad sinchronizuotumėte EKA keitimus.

### <a name="use-a-shared-shift"></a>Bendrai naudojamos pamainos naudojimas

1.  Prisijunkite prie EKA.
2.  Jei dar EKA dar neprijungtas prie aparatūros stoties, pasirinkite **Su stalčiumi nesusijusi operacija**, o tada pasirinkite operaciją **Pasirinkti aparatūros stotį**, kad suaktyvintumėte bendrai naudojamos pamainos aparatūros stotį. Šį veiksmą reikia atlikti tik pirmą kartą registrą įtraukiant į bendrai naudojamos pamainos aplinką.
3.  Atsijunkite nuo EKA ir vėl prisijunkite.
4.  Pasirinkite **Kurti naują pamainą**.
5.  Pasirinkite **Deklaruoti pradinę sumą**.
6.  Įveskite visų parduotuvės kasos stalčių, įtrauktų į bendrai naudojamą pamainą, pradinę sumą, o tada spustelėkite **Įrašyti**.
    -   Norėdami pradinės sumos dalį įtraukti į kiekvieną paskesnį kasos stalčių, naudokite operaciją **Pasirinkti aparatūros stotį**, kad suaktyvintumėte aparatūros stotį.
    -   Norėdami į konkretų kasos stalčių įtraukti kasos stalčiaus skyrelį, naudokite operaciją **Atidaryti stalčių**.
    -   Tęskite, kol visose bendrai naudojamos pamainos kasos stalčiuose bus reikiama pradinės sumos dalis.

7.  Pasibaigus dienai atidarykite kiekvieną kasos stalčių ir išimkite grynuosius pinigus.
8.  Išėmę grynuosius pinigus iš paskutinio kasos stalčiaus, suskaičiuokite visų kasos stalčių grynuosius pinigus.
9.  Naudokite operaciją **Deklaruoti mokėjimo priemonę**, kad deklaruotumėte bendrą grynųjų pinigų sumą visuose bendrai naudojamos pamainos kasos stalčiuose.
10. Naudokite operaciją **Uždaryti pamainą**, kad uždarytumėte bendrai naudojamą pamainą.





