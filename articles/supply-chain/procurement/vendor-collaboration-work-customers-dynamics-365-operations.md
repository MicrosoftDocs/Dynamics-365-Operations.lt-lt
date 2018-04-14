---
title: "Tiekėjo bendradarbiavimas su klientais"
description: "Šioje temoje aprašoma, kaip galite naudoti tiekėjo bendradarbiavimą programoje „Microsoft Dynamics 365 for Finance and Operations“, norėdami dirbti su PU ir stebėti konsignacijos atsargas."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4252112272e2f86c2c18dc399a713bf652e4228e
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="vendor-collaboration-with-customers"></a>Tiekėjo bendradarbiavimas su klientais

[!INCLUDE [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip galite naudoti tiekėjo bendradarbiavimą, norėdami dirbti su klientais programoje „Microsoft Dynamics 365 for Finance and Operations“. Tiekėjai gali atlikti tam tikrus verslo procesus toliau nurodytose darbo srityse.

- **Pirkimo užsakymo patvirtinimas** – pirkimo užsakymų (PU) stebėjimas ir reagavimas į juos.
- **Tiekėjų kainos siūlymas** – pasiūlymo patvirtinimų (RFQ) peržiūra ir reagavimas į juos įvedant kainos siūlymus.
- **Tiekėjo informacija** – tiekėjo bendrųjų duomenų peržiūra ir naujinimas.
- **SF išrašymas** – darbas su SF. Šioje temoje neaptariama darbo sritis **SF išrašymas**. Jei reikia daugiau informacijos apie šią darbo sritį, žr. temą [Tiekėjo bendradarbiavimo SF išrašymo darbo sritis](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md).

Tiekėjai taip pat gali stebėti informaciją apie konsignacijos atsargas.

## <a name="working-with-pos-in-the-purchase-order-confirmation-workspace"></a>Darbas su PU darbo srityje Pirkimo užsakymo patvirtinimas

Naudojant darbo sritį **Pirkimo užsakymo patvirtinimas** galima reaguoti į peržiūrai atsiųstus PU. Joje taip pat galima peržiūrėti informaciją apie PU, laukiančius kliento veiksmų, ir PU, kurie buvo patvirtinti, bet vis dar yra atviri.

Darbo srityje **Pirkimo užsakymo patvirtinimas** pateikiami trys sąrašai.

- **Pirkimo užsakymai, kuriuos reikia peržiūrėti** – šiame sąraše pateikiami jums atsiųsti PU, kurių atžvilgiu reikia atlikti veiksmus. Atlikus veiksmą PU sąraše neberodomas. Jei klientas atsiunčia jums naują PU versiją, o jūs dar neatsakėte į ankstesniąją, rodoma tik naujausia versija.
- **Laukiama kliento veiksmo** – šiame sąraše rodomi visi PU, į kuriuos atsakėte, bet kurių klientas dar nepatvirtino. Jei priėmėte PU, galite jį stebėti šiame sąraše tol, kol būsena pasikeičia į **Patvirtintas**. Jei PU atmetėte arba priėmėte atlikę keitimų, galite stebėti PU čia tol, kol klientas atsiųs naują versiją.
- **Atviri patvirtinti pirkimo užsakymai** – šiame sąraše yra visi jūsų sąskaitos PU, kurių būsena yra **Patvirtintas**. Kai pagal PU gauti visi produktai arba paslaugos, PU dingsta iš sąrašo.

Dirbdami su PU galite naudoti su toliau nurodytus puslapius.

- **Pirkimo užsakymai, kuriuos galima peržiūrėti** – šiame puslapyje pateikiama ta pati informacija kaip darbo srities sąraše **Pirkimo užsakymai, kuriuos galima peržiūrėti**. Peržiūrėkite pirmiau šioje temoje pateiktą aprašymą.
- **Pirkimo užsakymo tiekėjo patvirtinimo retrospektyva** – šiame puslapyje yra visi tiekėjui išsiųsti PU ir visos PU versijos. Jame taip pat yra visi atsakymai, kuriuos tiekėjas grąžino.
- **Atviri patvirtinti pirkimo užsakymai** – šiame puslapyje pateikiama ta pati informacija kaip darbo srities sąraše **Atviri patvirtinti pirkimo užsakymai**. Peržiūrėkite pirmiau šioje temoje pateiktą aprašymą.
- **Visi patvirtinti pirkimo užsakymai** – šiame puslapyje yra visi patvirtinti PU. Šiame puslapyje pateikti PU apie PU, kurių paslaugos arba produktai yra gauti. Šį sąrašą galite naudoti norėdami stebėti, kurių PU SF galite siųsti.

### <a name="responding-to-pos"></a>Atsakymas į PU

PU, kuriuos klientas jums išsiunčia peržiūrėti, pateikiami darbo srityje **Pirkimų užsakymų patvirtinimas** ir puslapyje **Pirkimo užsakymai, kuriuos reikia peržiūrėti**. Atidarę PU galėsite jį priimti, atmesti ar priimti su pakeitimais. Gali būti priedų PU antraštėje arba atskirose eilutėse. Taip pat galite pridėti informaciją prie atsakymo PU antraštėje arba atskirose eilutėse. Pavyzdžiui, galite pasiūlyti vienos eilutės prekės pakaitalą.

Galite peržiūrėti ir spausdinti PU kaip PDF failą, naudodami parinktį **Peržiūrėti / spausdinti**. Taip pat galite naudoti veiksmą **Rodyti dimensijas**, galite slėpti arba rodyti šiuos dimensijų stulpelius: **Vietovė**, **Sandėlis**, **Spalva**, **Dydis**, **Stilius** ir **Konfigūracija**. 

Jei naudojate parinktį **Priimti su pakeitimais**, galite priimti arba atmesti atskiras eilutes. Taip pat galite atlikti toliau nurodytus eilučių pakeitimus.

- Keisti datas arba kiekius. Norėdami naujinti patvirtintą pristatymo datą visose eilutėse, naudokite PU antraštės parinktį **Naujinti pristatymo datą**.
- Suskaldykite eilutes naudodami skirtingas pristatymo datas arba kiekius.
- Pakeisti prekę. Įveskite prekės aprašymą ir prekės numerį lauke **Išorinis**, kuris yra dalyje **Eilutės informacija**.

Negalima keisti kainodaros informacijos arba išlaidų, bet galima siūlyti tokius keitimus naudojant pastabas.

Jei klientas jums atsiunčia naują PU versiją, versija bus pateikta su priedėliu, kuris nurodys, kad PU yra modifikuota anksčiau išsiųsto PU versija. Puslapyje **Pirkimo užsakymo tiekėjo patvirtinimo retrospektyva** galite sekti kiekvieno užsakymo retrospektyvą.

## <a name="monitoring-consignment-inventory"></a>Konsignacijos atsargų sekimas

Jei naudojate konsignacijos atsargas, galite naudoti tiekėjo bendradarbiavimo sąsają, norėdami peržiūrėti informaciją tolesniuose puslapiuose.

- **Pirkimo užsakymai, kuriuose naudojamos konsignacijos atsargos** – konsignacijos atsargų PU generuojami klientui perėmus atsargų nuosavybės teises. Šie konsignacijos PU rodomi tik šiame puslapyje. Jie neįtraukiami į puslapį **Visi patvirtinti pirkimo užsakymai**.
- **Produktai, gauti iš konsignacijos atsargų** – šiame puslapyje pateikiamos visos operacijos, kuriose produktų nuosavybės teisės buvo perduoto įmonei, kuri naudoja atsargas. Galite naudoti šią informaciją kliento SF išrašyti.
- **Turimos konsignacijos atsargos** – šiame puslapyje rodomos turimos, jūsų įmonei priklausančios konsignacijos atsargos, bet esančios klientų sandėlyje.

## <a name="working-with-rfqs-in-the-vendor-bidding-workspace"></a>Darbas su RFQ darbo srityje Tiekėjų kainos siūlymas

Darbo srityje **Tiekėjų kainos siūlymas** galite peržiūrėti RFQ, į kuriuos įmonė buvo paprašyta atsakyti. Taip pat galite į RFQ atsakyti. 

Darbo srityje taip pat nurodomi visi RFQ, pralaimėjote arba laimėjote. Be to, jei sukonfigūruota sistemos viešasis sektorius, darbo srityje rodomi RFQ, kurie yra viešai pasiekiami.

### <a name="viewing-rfqs"></a>RFQ vaizdavimas

Atidarykite darbo sritį **Tiekėjų kainos siūlymas**, norėdami pasiekti toliau nurodytą informaciją.

- Pasirinkite **Nauji kvietimai siūlyti kainą**, kad pamatytumėte RFQ, į kuriuos jūsų įmonė buvo paprašyta atsakyti. Ten galite peržiūrėti RFQ ir pradėti kainos siūlymo procesą. Taip pat galite peržiūrėti pakeistus RFQ, už kuriuos reikia pasiūlyti naują kainą.
- Pasirinkite **Grąžinti kainos pasiūlymai**, kad pamatytumėte kliento grąžintus RFQ ir galėtumėte pateikti daugiau informacijos arba atnaujinti kainos siūlymą.
- Pasirinkite **Apdorojami kainos pasiūlymai**, kad pamatytumėte RFQ, su kuriais jūs arba jūsų įmonės kontaktinis asmuo dirbo, bet kurie dar nepateikti.
- Pasirinkite **Pasirinkti kainos pasiūlymai**, kad pamatytumėte, kada klientui buvo suteikta bent viena eilutės prekė jūsų kainos pasiūlyme.
- Pasirinkite **Prarasti kainos pasiūlymai**, kad pamatytumėte kainos siūlymus, kai visos eilutės buvo atmestos.
- Pasirinkite saitą **Pasiūlymo patvirtinimas**, kad pamatytumėte visų tiekėjo RFQ kvietimų ir bet kokių pateiktų kainos siūlymų sąrašą. Puslapyje **Pasiūlymų patvirtinimas** pateikiami visi RFQ, kurie susiję su tiekėju. Galite ieškoti pagal būseną.
- Pasirinkite saitą **Atmesti kainos siūlymai**, kad pamatytumėte visų RFQ, kai tiekėjo kontaktinis asmuo atsisakė siūlyti kainą.

### <a name="working-with-rfqs-that-are-publicly-available"></a>Darbas su viešai pasiekiamais RFQ

Žmonės, dirbantys viešajame sektoriuje, gali pamatyti atvirus ir nebegaliojančius RFQ, kurie yra viešai pasiekiami.

- Pasirinkite nuorodą **Atviri paskelbti pasiūlymų patvirtinimai**, kad pamatytumėte atvirų RFQ, kurie yra viešai pasiekiami, sąrašą. Atviras RFQ yra RFQ, kurio galiojimas dar nesibaigė. RFQ antraštėje galite peržiūrėti galiojimo pabaigos datą ir laiką.

    Jei buvote pakviesti siūlyti kainą, galite rasti tą patį RFQ puslapyje **Nauji kvietimai siūlyti kainą**. Galbūt kartais norėsite siūlyti kainą už atvirą RFQ, kai nesate pakviesti siūlyti kainos. Tokiu atveju galėsite patys pakviesti save, jei klientas įjungė RFQ atvejo savęs pakvietimo funkciją.

- Pasirinkite nuorodą **Uždaryti paskelbti pasiūlymų patvirtinimai**, kad pamatytumėte uždarytų RFQ, kurie yra viešai pasiekiami, sąrašą. Uždarytas RFQ yra nebegaliojantis RFQ. RFQ antraštėje galite peržiūrėti galiojimo pabaigos datą ir laiką.

    Uždarytame RFQ rodomi visi tiekėjų kainos siūlymai iki eilutės lygio. Kai siūlymai patvirtinami arba atmetami, ši informacija nurodoma uždarytame RFQ. Taip pat pateikiami visi priedai, įtraukti į kainos siūlymą.

**Pastaba:** ši funkciją galima naudoti tik kai įjungta viešojo sektoriaus konfigūracija.

### <a name="bidding"></a>Kainos siūlymas

- Spustelėkite **Siūlyti kainą**, kad pradėtumėte RFQ kainos siūlymą.

    Kai įjungtas RFQ antraštės ir eilučių kainos siūlymo laukų redagavimas, kainos siūlymą galite įvesti tiesiogiai eilučių tinklelyje. Taip pat turite atsižvelgti į bet kokią papildomą kainos siūlymo informaciją, kuri turi būti įtraukta į eilutės informaciją.

    Kai pradedate dirbti su kainos siūlymu, jis pasirodo dalyje **Apdorojami kainos pasiūlymai**.

    Kainos siūlymą įrašyti galite bet kada iki galiojimo pabaigos datos. Tada galite grįžti vėliau ir baigti bei pateikti kainos siūlymą. Pateikę kainos siūlymą, galite jį atšaukti ir atnaujinti iki galiojimo pabaigos datos.

- Pasirinkite **Atkurti iš RFQ**, norėdami iš naujo nustatyti jūsų įvestus kainos siūlymo duomenis ir atkurti pradinį RFQ. Galite iš naujo nustatyti antraštę arba eilutę.
- Eilučių tinklelyje pasirinkite **Įtraukti pakaitą** arba **Šalinti pakaitą**, kad dirbtumėte su pakaitais.

    Kai kuriuose RFQ galima teikti alternatyvius kainos siūlymus. Galite nurodyti tik tipo **Kategorija** eilučių alternatyvius kainos siūlymus, nes tam tikrų prekių negalima įtraukti kaip pakaitų. 

- Pasirinkite **RFQ priedas** arba **RFQ eilučių priedas**, kad atidarytumėte bet kurį priedą, kurį klientas įtraukė į RFQ. Pasirinkite **Kainos siūlymų priedai** arba **Kainos siūlymų eilučių priedai**, kad nusiųstumėte priedus kartu su kainos siūlymu.

    Gali būti klausimynų, į kuriuos turėsite atsakyti, prieš galėdami pateikti kainos siūlymą.

- Pasirinkite **Atmesti**, jei nenorite siūlyti kainos. Kai pasirenkate **Atmesti**, negalite atšaukti veiksmo ir įvesti kainos siūlymo.

Jei RFQ pakeistas, turite įvesti naują kainos siūlymą. Informaciją apie pakeitimą galite rasti RFQ puslapio skirtuke **Pakeitimai**. Pakeisti RFQ rodomi puslapyje **Nauji kvietimai siūlyti kainą**.

## <a name="accessing-vendor-master-data-in-the-vendor-information-workspace"></a>Prieiga prie tiekėjo bendrųjų duomenų darbo srityje Tiekėjo informacija

Kaip tiekėjas galite pasiekti dalį informacijos, kurią klientas tvarko pagrindiniame tiekėjo įraše. Taigi, galite atnaujinti informaciją. Jei norite naujinti informaciją, jums turi būti priskirtas tiekėjo administratoriaus (išorinis) vaidmuo.

Pasiekiama informacija: tiekėjo pavadinimas, adresai, kontaktinė informacija, kontaktiniai asmenys ir jų kontaktinė informacija, identifikavimo numeriai, mokesčių mokėtojų kodai, įsigijimo kategorijos, kurias naudodamas tiekėjas gali parduoti prekes ar paslaugas klientui, ir informacija apie sertifikatus.

## <a name="see-also"></a>Taip pat žiūrėkite

[Tiekėjo bendradarbiavimo vartotojų valdymas](manage-vendor-collaboration-users.md)

