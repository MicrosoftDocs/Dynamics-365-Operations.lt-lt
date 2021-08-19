---
title: Kodėl negalima atšaukti šios operacijos?
description: Šioje temoje aprašomos skirtingos priežastys, dėl kurių operacijų negalima atšaukti. Joje taip pat pateikiami šios problemos sprendimai.
author: kweekley
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 869832f085ee91f6c1fee53dad508cf5e54535627dadd6fb59a7586b03c8ec3b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719739"
---
# <a name="why-cant-i-reverse-this-transaction"></a>Kodėl negalima atšaukti šios operacijos?

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos skirtingos priežastys, dėl kurių operacijų negalima atšaukti. Joje taip pat pateikiami šios problemos sprendimai.

## <a name="symptom"></a>Požymis

Organizacijos gali susidurti su situacijomis, kuriose jos turi atšaukti užregistruotas operacijas. Kartais sistema apsaugo jas nuo šių operacijų atšaukimo. Dėl to gali būti pateikti du klausimai:

- Kodėl negalima atšaukti šios operacijos?
- Kaip masinio atšaukimo funkcija veikia šį elgseną?

## <a name="resolution"></a>Sprendimas

Prieš atšaukiant operacijas, jos turi atitikti konkrečius kriterijus. Likusiuose šios temos skyriuose pateikiama kiekvieno modulio tikrinimas. Nors ši tema susitelkia apie operacijas, kai kurias sąvokas ir tikrinimą galima taikyti „Microsoft Dynamics 365 Finance“ kitoms programoms, pvz. „Dynamics 365 Supply Chain Management“.

Be to, vieta, kurioje atšaukiama operacija, gali turėti įtakos tam, ar ją galima atšaukti. Pavyzdžiui, tiekėjo mokėjimą, kuris užregistruotas kaip čekis, galima atšaukti tik iš banko sąskaitų **operacijų** puslapio skyriaus Čekiai. Kvito operacijų **puslapio DK atšaukti** negalima.

Jei **kelių dokumentų** funkcijos (taip pat vadinamos masinio atšaukimo funkcija) masinis atšaukimas įjungtas **funkcijų valdymo** darbo srityje, tai veikia tai, kiek operacijų gali būti atšaukta ir kur jas galima atšaukti. Ši funkcija suteikia dviejų išmokų, kai ji įjungta:

- Kai kuriems operacijų tipams vienu metu galima pasirinkti ir atšaukti daugiau nei vieną operaciją iš žurnalo, kuriame ji buvo užregistruota, arba iš **kvito operacijų** puslapio. Tačiau prieš įjungant funkciją atskiros operacijos turi būti atšaukiamos. Prieš pradedant taikyti šią priemonę, operacijas vienu metu reikia atšaukti po vieną.
- *Kai kurias* papildomos knygos operacijas galima atšaukti iš žurnalo (bendrojo žurnalo) arba **kvito operacijų** puslapio. Papildomos knygos puslapyje jų atšaukti nereikia. Pavyzdžiui, tiekėjo SF žurnalą anksčiau galima atšaukti tik iš **puslapio Tiekėjo** operacijos. Tačiau dabar jį taip pat galima atšaukti iš DK, iš žurnalo ar **kvito operacijų** puslapio. Kiekviename šios temos skyriuje paaiškinami operacijų tipai, kuriems ši išmoka netaikoma.

Masinio atšaukimo funkcija neleidžia **atšaukti** daugiau operacijų tipų. Jei operacijos tipo anksčiau nepavyko atšaukti, vis tiek jo negalima atšaukti, kai ši funkcija įjungta. Pavyzdžiui, pirkimo užsakymo tiekėjo SF atšaukti negalima, nepaisant to, ar įjungta masinio atšaukimo funkcija.

Daugiau informacijos apie masinio atšaukimo priemonę ieškokite [atšaukimo žurnalo registravimą](reverse-journal-posting.md).

## <a name="general-ledger"></a>Didžioji knyga

DK koregavimai įvedami tik naudojant DK sąskaitas. Todėl jos atnaujina tik DK.

Jei masinio atšaukimo priemonė išjungta, dauguma DK koregavimų gali būti atšaukiami atskirai iš **DK puslapio \<main account\>** Operacijos (**LedgerTransAccount**). (Tikslus puslapio pavadinimas skiriasi, atsižvelgiant į pasirinktą pagrindinę sąskaitą.) Puslapyje rodoma kiekviena operacija, užregistruota pagrindinėje sąskaitoje. Jis paprastai atidaromas bandomojo balanso **sąrašo puslapyje** arba pasirenkant **operacijas** kvito **operacijų puslapyje**.

Jei masinio atšaukimo funkcija įjungta, vienas ar daugiau DK kvitų dabar gali būti atšaukti iš kvitų operacijų puslapio ir iš žurnalo, iš kurių **operacija buvo** užregistruota. Išimtys yra DK užsienio valiutos kurso pasikeitimo, konsolidavimo ir uždarymo metų pabaigoje operacijos. Šios operacijos atšaukiamos iš puslapių, iš kurių buvo vykdomas metų pabaigos uždarymas.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Operacijų priežastis, dėl kurių negalima atšaukti

Operacijų negalima atšaukti dėl šių priežasčių:

- Pagrindinis žurnalas:

    - Ataskaitinis laikotarpis sulaikytas arba visam laikui uždarytas:

        - Jei atšaukimo data yra ne atviras ataskaitinis laikotarpis, operacijos atšaukti negalima.
        - Jei operacija palaiko atšaukimo datos įrašą, operacija vis tiek gali būti atšaukta keičiant atšaukimo datą į atvirą laikotarpį.

    - Metų uždarymo procesas buvo atliktas:

        - Operacijos apskaitos data yra finansiniai metai, kurie buvo per metų pabaigos uždarymą. Nors finansinių metų laikotarpis vis dar gali būti atviras, operacijos negalima atšaukti, jei finansinių metų pabaigos uždarymo procesas buvo vykdomas. Finansinių metų būsena skiriasi nuo laikotarpių.
        - Metų pabaigos uždarymas gali būti atšauktas, tada operacija gali būti atšaukta. Šis būdas gali būti ne pasirinktis. Gali būti lengviau rankiniu būdu įvesti atšaukimo operaciją į atvirą uždarytų finansinių metų arba kitų finansinių metų laikotarpį, atsižvelgiant į finansinio uždarymo proceso būseną. Jei nauja operacija užregistruojama finansinių metų atvirame laiko tarpe, kuris buvo vykdomas metų pabaigos uždarymo procese, metų pabaigos uždarymą reikia vykdyti iš naujo.

    - Operacijos atšaukimas jau vyksta:

        - Jei operacija atšaukiama, šis procesas turi būti užbaigtas. Atskiro atšaukimo proceso atlikti negalima. 
        - Kai atšaukimas baigtas, atšauktą operaciją galima atšaukti dar kartą (tai yra, atšaukimas gali būti atšauktas).

    - DK sudengimas:

        - Jei viena ar daugiau operacijos eilučių sudengtos DK naudojant DK sudengimų periodinę užduotį **Dk nustatymai** periodinė užduotis (**DK \> Periodinės užduotys \> DK nustatymai**), todėl, kad įrašas yra LedgerTransSettlement lentelėje, perlaida negali grąžinta.
        - Knygos sudengimas uždarymas gali būti atšauktas, tada kvitas gali būti atšauktas.

    - Vidinė įmonė:

        - Jei operacija yra vidinės įmonės operacija, jos atšaukti negalima.
        - Operacija nėra vidinės įmonės operacija, bet **registruojama** terminas iki arba "terminas nuo" pagrindinėje sąskaitoje, kuri buvo nurodyta vidinės **įmonės nustatymo** puslapyje.

    - Kaupimai:

        - Jei sukauptas DK kvitas atšaukiamas, sukauptas įrašas ir visos atitinkamos kaupimo tarpinės operacijos bus atšauktos.
        - Atskirų kaupimo antrinių operacijų atšaukti negalima.

- Įplaukų pripažinimo žurnalai:

    - Apyvartos atpažinimo operacijų atšaukti negalima.
    - Kai įplaukos pripažįstamos naudojant įplaukų pripažinimo žurnalą, kvitas registruojamas tik į DK sąskaitas. Dėl to, puslapiuose, **kvito operacijos**, operacijos rodomos taip tarsi jos būtų tik DK įrašai.

- Užsienio valiutos kurso pasikeitimas:

    - Užsienio valiutos kurso pasikeitimo operacijas galima atšaukti, bet tik iš DK užsienio **valiutos kurso pasikeitimo** puslapio, iš kurių buvo vykdomas perkainojimas.
    - Atšaukimas gali būti užbaigtas tik tada, jei jis užregistruotas atviras ataskaitinis laikotarpis.

- Konsolidacija:

    - Konsolidavimo operacijas galima atšaukti, bet tik iš **konsolidavimo operacijų** puslapio.
    - Atšaukimas gali būti užbaigtas tik tada, jei jis užregistruotas atviras ataskaitinis laikotarpis.

- Metų pabaigos uždarymas:

    - Uždarymo metų pabaigoje operacijas (uždarymo ir atidarymo operacijas) galima atšaukti šiais būdais:

        - Jei DK uždarymo metų pabaigoje patobulinimų funkcija išjungta, dialogo lange **Metų pabaigos uždarymas** pasirinkite parinktį **Anuliuoti ankstesnį uždarymą** langą.
        - Jei DK metų pabaigos patobulinimų funkcija įjungta, pasirinkite įmonės ir finansinių metų įrašus, kurie buvo sukurti metų pabaigos uždarymui **Metų pabaigos uždarymui** puslapyje ir tada rinkitės **Atšaukti metų pabaigos uždarymą**.

    - Atkreipkite dėmesį, kad metų pabaigos uždarymas iš tikrųjų panaikina uždarymo ir atidarymo operacijas. Atšaukimo kvitas niekada neregistruojamas.

## <a name="accounts-payable"></a>Mokėtinos sumos

Kelių operacijų tipai atnaujina mokėtinų sumų papildomos knygos operacijas. Pavyzdžiai gali būti tiekėjo SF, tiekėjo SF žurnalai ir išlaidų ataskaitos.

Jei masinio atšaukimo priemonė išjungta, operacijas galima atšaukti atskirai iš SF **Tiekėjo operacijų** puslapio arba iš mokėjimo čekiu **Banko sąskaitos** puslapio.

Jei masinio atšaukimo funkcija įjungta, vienas ar daugiau sąskaitų mokėtinų operacijų kvitų dabar gali būti atšaukti iš kvitų operacijų puslapio ir iš žurnalo, iš kurių **operacija buvo** užregistruota. Tačiau tiekėjo mokėjimus vis dar galima atšaukti tik iš banko sąskaitos. Be to, tiekėjo operacijų negalima atšaukti iš **Operacijos \<main account\>** puslapis DK. Juos galima atšaukti tik **kvitų operacijų** puslapyje.

Atkreipkite dėmesį, kad kai kurių operacijų iš viso negalima atšaukti. Pavyzdžiai apima pirkimo užsakymo tiekėjo SF ir elektroninius tiekėjo mokėjimus.

### <a name="reasons-why-vouchers-cant-be-reversed"></a>Operacijų priežastys, kodėl kvitų negalima atšaukti

Kvitų negalima atšaukti dėl šių priežasčių:

- Ataskaitinis laikotarpis sulaikytas arba visam laikui uždarytas:

    - Jei atšaukimo data yra ne atviras ataskaitinis laikotarpis, operacijos atšaukti negalima.
    - Jei operacija palaiko atšaukimo datos įrašą, operacija vis tiek gali būti atšaukta keičiant atšaukimo datą į atvirą laikotarpį.

- DK uždarymo procesas buvo atliktas:

    - Operacijos apskaitos data yra finansiniai metai, kurie buvo per DK pabaigos uždarymą. Nors finansinių metų laikotarpis vis dar gali būti atviras, operacijos negalima atšaukti, jei finansinių metų pabaigos uždarymo procesas buvo vykdomas. Finansinių metų būsena skiriasi nuo laikotarpių.
    - Metų pabaigos uždarymas gali būti atšauktas, tada operacija gali būti atšaukta. Šis būdas gali būti ne pasirinktis. Gali būti lengviau rankiniu būdu įvesti atšaukimo operaciją į atvirą uždarytų finansinių metų arba kitų finansinių metų laikotarpį, atsižvelgiant į finansinio uždarymo proceso būseną. Jei nauja operacija užregistruojama finansinių metų atvirame laiko tarpe, kuris buvo vykdomas metų pabaigos uždarymo procese, metų pabaigos uždarymą reikia vykdyti iš naujo.

- Papildomos knygos žurnalo įrašas nepervestas į DK:

    - Ši priežastis taikoma tik ne pirkimo užsakymo tiekėjo SF.
    - Naudokite dar **neperduotų papildomos knygos žurnalo** įrašų puslapį, kad perkelt būtų galima perkelti įrašą į DK. Ne pirkimo užsakymo tiekėjo SF tada galima atšaukti iš **tiekėjo operacijų** puslapio.

- Atsiskaitymas:

    - Operacija (pvz., SF arba mokėjimas) sudengta arba pažymėta sudengti.

        - Galite patikrinti, ar operacija sudengiama arba pažymėta sudengti, tiekėjo operacijų puslapyje pasirinkdami **Peržiūrėti sudengimų** arba **Sudengimo \> sudengimo retrospektyvą** on **Tiekėjo perlaidas** puslapyje.
        - Sudengimą taip pat galite atšaukti iš tiekėjo **operacijų puslapio** puslapyje (**Sudengimas \> neįdengimas atstatytas**), jei viena iš operacijų turi būti atšaukta.

- Kvite yra daugiau nei viena papildomos knygos operacija, įvesta naudojant tą patį kvito numerį (Vienas kvito išdavimas).
- SĄSKAITA faktūra nebuvo patvirtinta:

    - Jei **sąskaitos** faktūros žymės langelis Patvirtinimas neparinktas, SF atšaukti negalima.

        - Šiuo atveju patvirtinimas nurodo ne darbo eigos proceso patvirtinimus, o **Patvirtinimą** pasirinktį. Ši pasirinktis naudojama norint neleisti apmokėti SF. Paprastai naudojama tiekėjo SF registro SF.

- Operacija yra sąskaitos baseine:

    - Telkinio SF negalima atšaukti tiesiogiai iš **tiekėjo operacijų** puslapio. Todėl jis turi būti atšauktas SF patvirtinimo žurnalo **puslapio atšaukimo proceso** metu.

- Yra pataisyta pirminė SF (Indijos lokalizavimas).
- Operacijos paprastojo vekselio būsena yra **Pervesta SF**.
- Operacija naudojama daliniam mokesčių sudengimo metu.
- Operacijoje yra tiekėjo kodas, bet ji atšaukiama iš neteisingo puslapio, pvz., **puslapio \<main account\>** operacijos:

    - Todėl siūloma, net jei įjungta masinio atšaukimo funkcija, kai kurios papildomos knygos operacijos gali būti atšauktos tik iš konkrečių puslapių.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Operacijų, kurių negalima atšaukti, tipai

Tolesni perlaidų tipai negali būti grąžinti:

- Užsienio valiutos kurso pasikeitimas:

    - Kitaip nei DK užsienio valiutos pervertinimas, gautinos lėšos ir mokėtinos lėšos užsienio valiuta negali būti grąžinamos. Vietoj to, perkainojimas turi būti vykdomas vėl naudojant SF datą. Šiuo atveju perkainojimas naudoja SF datos valiutos kursą, iš esmės dėl to negautas pelnas ar nuostolis iš esmės tampa 0 (nulis). Todėl rezultatas panašus į ankstesnio perkainojimo atšaukimo rezultatą. Tačiau atminkite, kad ta pati suma nebus atšaukta, jei SF būtų pakeistas numatytasis valiutos kursas.

- Pirkimo užsakymo tiekėjo sąskaita:

    - Norint atšaukti tiekėjo SF, turi būti sukurta kredito pažyma. Daugiau informacijos apie tai, kaip sukurti atšaukimo operaciją, ieškokite [pirkimo grąžinimo užsakymo kūrimas](../../supply-chain/procurement/tasks/create-purchase-return-order.md).

- Paprastasis vekselis
- Banko kredito laiško eksportavimo siuntimas

## <a name="accounts-receivable"></a>Gautinos sumos

Keli operacijų tipai naujinti lėšos gautinos papildomi DK. Pavyzdžiai apima kliento SF iš pardavimo užsakymų, klientų SF, kurios įvedamos per bendrąjį žurnalą, laisvos formos SF, klientų mokėjimus ir nurašymes.

Jei masinio atšaukimo priemonė išjungta, operacijas galima atšaukti atskirai iš SF **Klientų operacijų** puslapio arba iš mokėjimo čekiu **Banko sąskaitos** indėliams puslapio. Informacijos apie tai, kaip atšaukti mokėjimą, žr. [grynųjų pinigų ir banko valdymo](cant-reverse-transctns.md#cash-and-bank-management) skyrių toliau šioje temoje.

Jei masinio atšaukimo funkcija įjungta, vienas ar daugiau sąskaitų gautinų operacijų kvitų dabar gali būti atšaukti iš kvitų operacijų puslapio ir iš žurnalo, iš kurių **operacija buvo** užregistruota. Tačiau depozitus vis dar galima atšaukti tik iš banko sąskaitos, o laisvos formos SF galima atšaukti tik iš tinklalapio (jei funkcija, leidžianti taisyti, įjungta). Taip pat, kliento operacijos dar gali būti grąžintos iš **Operacijos \<main account\>** puslapis DK. Nepaisant to, juos galima atšaukti tik **kvitų operacijų** puslapyje.

Atkreipkite dėmesį, kad kai kurių operacijų iš viso negalima atšaukti. Pavyzdžiai gali būti pardavimo užsakymo kliento SF ir nurašymi.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Operacijų priežastis, dėl kurių negalima atšaukti

Operacijų negalima atšaukti dėl šių priežasčių:

- Ataskaitinis laikotarpis sulaikytas arba visam laikui uždarytas:

    - Jei atšaukimo data yra ne atviras ataskaitinis laikotarpis, operacijos atšaukti negalima.
    - Jei operacija palaiko atšaukimo datos įrašą, operacija vis tiek gali būti atšaukta keičiant atšaukimo datą į atvirą laikotarpį.

- DK uždarymo procesas buvo atliktas:

    - Operacijos apskaitos data yra finansiniai metai, kurie buvo per DK pabaigos uždarymą. Nors finansinių metų laikotarpis vis dar gali būti atviras, operacijos negalima atšaukti, jei finansinių metų pabaigos uždarymo procesas buvo vykdomas. Finansinių metų būsena skiriasi nuo laikotarpių.
    - Metų pabaigos uždarymas gali būti atšauktas, tada operacija gali būti atšaukta. Šis būdas gali būti ne pasirinktis. Gali būti lengviau rankiniu būdu įvesti atšaukimo operaciją į atvirą uždarytų finansinių metų arba kitų finansinių metų laikotarpį, atsižvelgiant į finansinio uždarymo proceso būseną. Jei nauja operacija užregistruojama finansinių metų atvirame laiko tarpe, kuris buvo vykdomas metų pabaigos uždarymo procese, metų pabaigos uždarymą reikia vykdyti iš naujo.

- Papildomos knygos žurnalo įrašas nepervestas į DK:

    - Ši priežastis taikoma tik laisvos formos SF.
    - Naudokite dar **neperduotų papildomos knygos žurnalo** įrašų puslapį, kad perkelt būtų galima perkelti įrašą į DK. Laisvos formos SF galima atšaukti arba taisyti, jei įgalinta pataisymų funkcija.

- Atsiskaitymas:

    - Operacija (pvz., SF arba mokėjimas) sudengta arba pažymėta sudengti.

        - Galite patikrinti, ar operacija sudengiama arba pažymėta sudengti, tiekėjo operacijų puslapyje pasirinkdami **Peržiūrėti sudengimų** arba **Sudengimo \> sudengimo retrospektyvą** on **Kliento perlaidas** puslapyje.
        - Sudengimą taip pat galite atšaukti iš tiekėjo **Klientų puslapio** puslapyje (**Sudengimas \> neįdengimas atstatytas**), jei viena iš operacijų turi būti atšaukta.

- Perlaidose yra daugiau nei viena papildomos knygos operacija, įvesta naudojant tą patį kvito numerį (Vienas kvito išdavimas).
- SĄSKAITA faktūra nebuvo patvirtinta:

    - Jei **sąskaitos** faktūros žymės langelis Patvirtinimas neparinktas, SF atšaukti negalima.

        - Šiuo atveju patvirtinimas nurodo ne darbo eigos proceso patvirtinimus, o **Patvirtinimą** kvitų eilutės. Ši pasirinktis naudojama norint neleisti apmokėti SF. Nors ši pasirinktis paprastai naudojama mokėtinose sumose, tai taip pat galima gautinų sumų SF, kurios įvedamos per žurnalus.

- Yra pataisyta pirminė SF (Indijos lokalizavimas).
- Operacijoje yra kliento kodas, bet ji atšaukiama iš neteisingo puslapio, pvz., **puslapio \<main account\>** operacijos:

    - Todėl siūloma, net jei įjungta masinio atšaukimo funkcija, kai kurios papildomos knygos operacijos gali būti atšauktos tik iš konkrečių puslapių.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Operacijų, kurių negalima atšaukti, tipai

Tolesni perlaidų tipai negali būti grąžinti:

- Užsienio valiutos kurso pasikeitimas:

    - Kitaip nei DK užsienio valiutos pervertinimas, gautinos lėšos ir mokėtinos lėšos užsienio valiuta negali būti grąžinamos. Vietoj to, perkainojimas turi būti vykdomas vėl naudojant SF datą. Šiuo atveju perkainojimas naudoja SF datos valiutos kursą, iš esmės dėl to negautas pelnas ar nuostolis iš esmės tampa 0 (nulis). Todėl rezultatas panašus į ankstesnio perkainojimo atšaukimo rezultatą. Tačiau atminkite, kad ta pati suma nebus atšaukta, jei SF būtų pakeistas numatytasis valiutos kursas.

- Operacija, pakoreguojanti išskaitomų mokesčių
- Pardavimo užsakymo kliento sąskaita:

    - Norint atšaukti ar grąžinti tiekėjo SF, turi būti sukurta operacijos pažyma. Informacijos apie tai, kaip sukurti atšaukimo operaciją, ieškokite [Pardavimo grąžinimai](../../supply-chain/warehousing/sales-returns.md).

- Įsakomasis vekselis
- Lėšų registro operacijos
- Išplėstinis koregavimas
- Delspinigių pažyma
- Surinkimo laiškas
- Banko kredito sąskaitos
- Eksporto siuntimas
- Įplaukų pripažinimo žurnalai:

    - Kai pripažįstate apyvartą per apyvartos pripažinimo žurnalą, kvitai yra talpinami į DK sąskaitas. Todėl jie pasirodo taip pat, kaip jeigu yra tik DK įrašai. Šių įrašų atšaukti negalima, nes įplaukų grafikas nebuvo atidarytas iš naujo, kad būtų galima atpažinti įplaukas dar kartą.

## <a name="cash-and-bank-management"></a>Grynųjų pinigų ir banko valdymas

Keli operacijų tipai atnaujina banko papildomos knygos informaciją naudojant bendrąjį žurnalą. Pavyzdžiai apima tiekėjo mokėjimus, klientų mokėjimus ir banko pervedimus.

Jei masinio atšaukimo priemonė išjungta, operacijas galima atšaukti atskirai iš SF **Banko sąskaitos** puslapio kvito ir indėliai ar iš **Klientų sąskaitos** klientams puslapio.

Jei masinio atšaukimo funkcija įjungta, vienas ar daugiau sąskaitų mokėjimų operacijų kvitų dabar gali būti atšaukti iš kvitų operacijų puslapio ir iš žurnalo, iš kurių **operacija buvo** užregistruota. Tačiau indėlius vis dar galima atšaukti tik iš banko sąskaitos. Taip pat, banko operacijos dar gali būti grąžintos iš DK **Operacijos \<main account\>** puslapis DK. Nepaisant to, juos galima atšaukti tik **kvitų operacijų** puslapyje.

Atkreipkite dėmesį, kad kai kurių operacijų iš viso negalima atšaukti. Pavyzdžiai apima elektroninius tiekėjo mokėjimus.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Operacijų priežastis, dėl kurių negalima atšaukti

Operacijų negalima atšaukti dėl šių priežasčių:

- Ataskaitinis laikotarpis sulaikytas arba visam laikui uždarytas:

    - Jei atšaukimo data yra ne atviras ataskaitinis laikotarpis, operacijos atšaukti negalima.
    - Jei operacija palaiko atšaukimo datos įrašą, operacija vis tiek gali būti atšaukta keičiant atšaukimo datą į atvirą laikotarpį.

- DK uždarymo procesas buvo atliktas:

    - Operacijos apskaitos data yra finansiniai metai, kurie buvo per DK pabaigos uždarymą. Nors finansinių metų laikotarpis vis dar gali būti atviras, operacijos negalima atšaukti, jei finansinių metų pabaigos uždarymo procesas buvo vykdomas. Finansinių metų būsena skiriasi nuo laikotarpių.
    - Metų pabaigos uždarymas gali būti atšauktas, tada operacija gali būti atšaukta. Šis būdas gali būti ne pasirinktis. Gali būti lengviau rankiniu būdu įvesti atšaukimo operaciją į atvirą uždarytų finansinių metų arba kitų finansinių metų laikotarpį, atsižvelgiant į finansinio uždarymo proceso būseną. Jei nauja operacija užregistruojama finansinių metų atvirame laiko tarpe, kuris buvo vykdomas metų pabaigos uždarymo procese, metų pabaigos uždarymą reikia vykdyti iš naujo.

- Atsiskaitymas:

    - Operacija (pvz., SF arba mokėjimas) sudengta arba pažymėta sudengti.

        - Galite patikrinti, ar operacija sudengiama arba pažymėta sudengti, tiekėjo operacijų puslapyje pasirinkdami **Peržiūrėti sudengimų** ar **Sudengimo \> Tiekėjo perlaidos** puslapio **Tiekėjo perlaidos** ar **Kliento perlaidas** puslapio.
        - Sudengimą taip pat galite atšaukti iš tiekėjo **Klientų perlaidos** ar **Kliento perlaidos** puslapio (**Sudengimas \> neįdengimas atstatytas**), jei viena iš operacijų turi būti atšaukta.

- Perlaidose yra daugiau nei viena papildomos knygos operacija, įvesta naudojant tą patį kvito numerį (Vienas kvito išdavimas).
- Tarpinės operacijos:

    - Jei operacija susijusi su tarpmu mokėjimu, jos atšaukti negalima.
    - Jei tarpinis mokėjimas turi būti atšauktas, pirmiausia mokėjimas turi būti išvalytas iš tarpinės sąskaitos į banką. Tada mokėjimą galima atšaukti, jei jis atitinka kitus tikrinimo kriterijus.

- Operaciją sudaro banko sąskaita, bet ji atšaukiama puslapyje **Perlaidos \<main account\>** puslapyje ar iš netinkamo papildomame DK, tokiame Gautinos lėšos ar Gautinos sąskaitos:

    - Todėl siūloma, net jei įjungta masinio atšaukimo funkcija, kai kurios papildomos knygos operacijos gali būti atšauktos tik iš konkrečių puslapių.

- Banko užsienio valiutos kurso pasikeitimas:

    - Banko užsienio valiutos kurso pasikeitimas negali būti grąžintas. Tačiau atšaukimas gali būti neleidžiamas, jei užbaigsite atšaukimo veiksmus chronologine tvarka. Pavyzdžiui, jei kovo ir balandžio mėnesį buvo įvykdytas perkainojimas, kovo perkainojimo negalima atšaukti, kol nebus atšauktas balandžio perkainojimas.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Operacijų, kurių negalima atšaukti, tipai

Tolesni perlaidų tipai negali būti grąžinti:

- Tiekėjo mokėjimai, atlikti kaip elektroniniai lėšų pervedimai (EFT)
- Paprastieji vekseliai
- Įsakomieji vekseliai

## <a name="fixed-assets"></a>Ilgalaikis turtas

Keli operacijų tipai atnaujina ilgalaikio turto papildomos knygos informaciją. Pavyzdžiai gali būti įsigijimai ir nusidėvėjimas.

Jei masinio atšaukimo priemonė išjungta, operacijas galima atšaukti atskirai nuo tiekėjo operacijų puslapio, iš ilgalaikio **Kliento operacijos** puslapyje iš **Ilgalaikio turto operacijos** puslapio ar iš Turto lizingavimo priklausomai nuo operacijos tipo.

Jei masinio atšaukimo funkcija įjungta, vienas ar daugiau ilgalaikio turto operacijų kvitų dabar gali būti atšaukti iš kvitų operacijų puslapio ir iš žurnalo, iš kurių **Kvito perlaidos** užregistruota.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Operacijų priežastis, dėl kurių negalima atšaukti

Operacijų negalima atšaukti dėl šių priežasčių:

- Ataskaitinis laikotarpis sulaikytas arba visam laikui uždarytas:

    - Jei atšaukimo data yra ne atviras ataskaitinis laikotarpis, operacijos atšaukti negalima.
    - Jei operacija palaiko atšaukimo datos įrašą, operacija vis tiek gali būti atšaukta keičiant atšaukimo datą į atvirą laikotarpį.

- DK uždarymo procesas buvo atliktas:

    - Operacijos apskaitos data yra finansiniai metai, kurie buvo per DK pabaigos uždarymą. Nors finansinių metų laikotarpis vis dar gali būti atviras, operacijos negalima atšaukti, jei finansinių metų pabaigos uždarymo procesas buvo vykdomas. Finansinių metų būsena skiriasi nuo laikotarpių.
    - Metų pabaigos uždarymas gali būti atšauktas, tada operacija gali būti atšaukta. Šis būdas gali būti ne pasirinktis. Gali būti lengviau rankiniu būdu įvesti atšaukimo operaciją į atvirą uždarytų finansinių metų arba kitų finansinių metų laikotarpį, atsižvelgiant į finansinio uždarymo proceso būseną. Jei nauja operacija užregistruojama finansinių metų atvirame laiko tarpe, kuris buvo vykdomas metų pabaigos uždarymo procese, metų pabaigos uždarymą reikia vykdyti iš naujo.

- Įsigijimai:

    - Jei pirkimo užsakymo tiekėjo SF buvo įsigyta, atšaukimas turi būti atliktas įvedant tiekėjo kredito pažymą. Daugiau informacijos apie tai, kaip įvesti atšaukimo operacijas, ieškokite [pirkimo grąžinimo užsakymo kūrimas](../../supply-chain/procurement/tasks/create-purchase-return-order.md).
    - Įsigijimas įvyko projekto operacijoje.
    - Užregistrus turto nusidėvėjimą, įsigijimo atšaukti negalima. Nusidėvėjimas turi būti atšauktas prieš atšaukiant įsigijimą.
    - Jei ilgalaikio turto vertinimo modelio arba nusidėvėjimo knygos būsena nėra atidaryta, operacijos atšaukti negalima.

- Likvidavimas:

    - Likvidavimas atliekamas naudojant laisvos formos SF:

        - Laisvos formos SF koregavimas blokuojamas, jei joje yra ilgalaikis turtas. Tačiau jei turtas likviduojamas žurnale, laisvos formos SF gali būti atšaukta iš ilgalaikio turto įrašo.

    - Jei ilgalaikio turto vertinimo modelio arba nusidėvėjimo knygos būsena nėra atidaryta, operacijos atšaukti negalima.

- Nusidėvėjimas:

    - Nusidėvėjimas **gali būti** atšauktas, jei registruojamas ir vėlesnis nusidėvėjimas. Tačiau jūs gausite perspėjimą, nes šis būdas nėra geriausia praktika.
    - Jei ilgalaikio turto vertinimo modelio arba nusidėvėjimo knygos būsena nėra atidaryta, operacijos atšaukti negalima.

- Yra konkretaus turto ir turto knygos operacijų (arba atšaukų operacijų) kvito operacijos data ar vėliau.
- Operaciją sudaro turto sąskaita, bet ji atšaukiama puslapyje **Perlaidos \<main account\>** puslapyje ar iš netinkamo papildomame DK, tokiame Gautinos lėšos ar Gautinos sąskaitos:

    - Todėl siūloma, net jei įjungta masinio atšaukimo funkcija, kai kurios papildomos knygos operacijos gali būti atšauktos tik iš konkrečių puslapių.
    - Jeigu įsigijimas įvyksta ne pirkimo užsakymo tiekėjo SF arba tiekėjo SF žurnale, jį galima atšaukti tik iš mokėtinų sumų **tiekėjo operacijų** puslapio.
    - Jei turtas įsigytas iš turto pagal turto psl., jis gali būti atšauktas iš **Turto įsipareigojimų** operacijų puslapio.
