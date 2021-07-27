---
title: Pripažinti atidėtas įplaukas
description: Šioje temoje pateikiama informacija apie tai, kaip pripažinti įplaukas naudojant įplaukų pripažinimo funkciją.
author: kweekley
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: cafe28e0aa71d623a728829ff1bf71bef5a132b0
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347205"
---
# <a name="recognize-deferred-revenue"></a>Pripažinti atidėtas įplaukas

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Įplaukų pripažinimo funkcija negali būti įjungta naudojant funkcijų valdymą. Dabar norėdami ją įjungti, turite naudoti konfigūracijos raktus.

Šioje temoje aprašomas pajamų pripažinimo procesas įplaukų pripažinimo grafike. Po to kai pardavimo užsakymui užregistruojama SF, kiekvienai pardavimo užsakymo eilutei, turinčiai įplaukų grafiką, sukuriamas įplaukų pripažinimo grafikas. Įplaukų grafikas eilutėje yra naudojamas nustatyti, ar eilutės įplaukos turėtų būti atidėtos.

## <a name="view-revenue-recognition-schedule-details"></a>Peržiūrėti įplaukų pripažinimo grafiko informaciją

Yra du būdai pasiekti įplaukų pripažinimo grafiko informaciją.

- Galite atidaryti įplaukų pripažinimo grafiką tiesiai pardavimo užsakyme, kurio SF jau išrašyta. Tokiu atveju įplaukų grafiko informacija yra filtruojama rodyti tik pasirinkto pardavimo užsakymo informaciją. Šis būdas naudingas, kai tikrinate pardavimo užsakymo grafiko informaciją.
- Galite atidaryti įplaukų pripažinimo grafiką puslapyje **Įplaukų pripažinimas \> Periodinės užduotys**. Šis būdas dažnai naudojamas, kai įplaukos pripažįstamos laikotarpio pabaigoje. Pirmą kartą atidarius puslapį, informacija nerodoma. Norėdami apibrėžti rodytinos grafiko informacijos kriterijus, naudokite filtrus virš tinklelio. Galite filtruoti SF datas įvesdami datų intervalą, pardavimo užsakymą, klientą, projekto ID arba būseną.

[![Puslapio Įplaukų grafikai iliustracija.](./media/revenue-recognition-schedule-page.png)](./media/revenue-recognition-schedule-page.png)

**Finansinė dimensija** „FastTab“ po tinkleliu rodo pardavimo užsakymo eilutės finansines dimensijas. Į šias dimensijas atsižvelgta registruojant atidėtas įplaukas. Į jas taip pat atsižvelgiama pripažįstant įplaukas. Naudojamos dimensijų reikšmės priklauso nuo sąskaitos struktūros, priskirtos įplaukų ir atidėtų įplaukų pagrindinėms sąskaitoms.

## <a name="recognize-revenue"></a>Pripažinti įplaukas

Įplaukos pripažįstamos vykdant procesą **Kurti žurnalą** puslapyje **Pripažinti įplaukas**. Šį puslapį galite atidaryti pardavimo užsakyme arba **Periodinėse užduotyje**. Jei procesas vykdomas pardavimo užsakyme, pripažįstamos tik pasirinkto pardavimo užsakymo pajamos. Dažniausiai vietoj to procesas vykdomas **Periodinėse užduotyse** ir jo metu pripažįstamos visų užregistruotų pardavimo užsakymų SF įplaukos.

Norėdami apibrėžti įplaukų pasirinkimo ir registravimo kriterijus, pasirinkite **Kurti žurnalą**, kad atidarytumėte dialogo langą **Kurti žurnalą**.

[![Kurti žurnalą: parametrų parinktys.](./media/revenue-recognition-create-journal.png)](./media/revenue-recognition-create-journal.png)

Norėdami apibrėžti registravimo datą, naudojamą pripažįstant įplaukas, dialogo lange naudokite **Apdorojimo data** lauko grupės parinktis. Pasirinkę **Pasirinkti datą**, galite įvesti registravimo datą lauke **Operacijos data**. Pasirinkus **Įplaukų grafiko data**, operacijos data nenaudojama. Vietoj to lauko **Pripažinimo data** reikšmė kiekvienoje grafiko eilutėje naudojama kaip registravimo data.

Toliau, lauke **Nuo datos** įveskite datą, nuo kurios pripažįstamos įplaukos. Visos grafiko eilutės, kuriose pripažinimo data sutampa su „nuo“ data arba yra už ją ankstesnė, bus pripažįstamos, jei jos nebus sulaikytos.

Baigę nustatyti datas, dialogo lange pasirinkite **GERAI** žurnalui sukurti. Gausite informacinį pranešimą, kuriame nurodomas sukurtų operacijų skaičius ir žurnalas, kuriame jos buvo sukurtos. Žurnalas nėra automatiškai registruojamas. Todėl įplaukų pripažinimo valdytojas turi laiko patvirtinti, kurios grafiko eilutės yra pripažįstamos.

Po proceso vykdymo grafike esančios eilutės, kurios buvo perkeltos į žurnalą, pažymimos kaip **Apdorota**. Vėliavėlė **Apdorota** rodo, kad eilutės buvo perkeltos į žurnalą, tačiau jos gali būti registruojamos arba neregistruojamos. Užregistravus įplaukų pripažinimo žurnalą, vėliavėlė **Apdorota** lieka. Panaikinus įplaukų pripažinimo žurnalą arba eilutę, vėliavėlė **Apdorota** pašalinama. Tokiu atveju, eilutę galima pripažinti dar kartą vykdant procesą **Kurti žurnalą**.

[![Įplaukų pripažinimo grafikų puslapis.](./media/revenue-recognition-rev-recog-schedule-02.png)](./media/revenue-recognition-rev-recog-schedule-02.png)

Puslapyje **Įplaukų pripažinimo žurnalas** (**Įplaukų pripažinimas \> Žurnalo įrašai \> Įplaukų pripažinimo žurnalas**) atidarykite **Eilutės** informacijai apie tai, kas pripažįstama, peržiūrėti. Kiekvienai pripažįstamai grafiko eilutei visada sukuriama atskira operacija, net jei visos eilutės yra registruojamos tą pačią dieną naudojant tas pačias DK sąskaitas.

[![Žurnalo kvito puslapis.](./media/revenue-recognition-journal-voucher.png)](./media/revenue-recognition-journal-voucher.png)

Stulpelyje **Sąskaita** rodoma atidėtų įplaukų DK sąskaita. Šios DK sąskaitos redaguoti negalima. Šis apribojimas padeda garantuoti, kad bus paskiriama teisinga atidėtų įplaukų DK sąskaita. Ši DK sąskaita nėra patikrinta pagal sąskaitos struktūrą, nes ji galėjo pasikeisti po paskutinio registravimo nurodytoje įplaukų DK sąskaitoje.

Stulpelyje **Korespondentinė sąskaita** rodoma įplaukų DK sąskaita. Pagal numatytuosius nustatymus įplaukų DK sąskaita paimta iš atsargų registravimo profilių, o finansinės dimensijos paimtos iš pardavimo užsakymo eilutės. DK sąskaita patikrinama pagal esamą sąskaitos struktūrą. Tačiau ji gali būti redaguojama, jei sąskaitos struktūra pasikeitė ir reikia papildomų finansinių dimensijų.

Numatytoji suma yra iš atitinkamos grafiko eilutės ir jos keisti negalima.

Pagal numatytuosius nustatymus, jei pardavimo užsakyme yra kelios valiutos, valiutos kursas nustatomas į SF valiutos kursą. Taip padedama garantuoti, kad sumos apskaitos valiuta ir ataskaitų valiuta yra visiškai paskirtos. Dėl apvalinimo paskutinės grafiko eilutės valiutos kursas gali šiek tiek skirtis nuo SF nurodyto kurso.

Užregistravus įplaukų pripažinimo žurnalą, grafike įvedamas kvitas. Jei yra daugiau nei vienas tos pačios grafiko eilutės kvitas, eilutėje pasirodo žvaigždutė (\*). Norėdami peržiūrėti toje eilutėje užregistruotus kvitus, pasirinkite **Kvitų operacijos**.

## <a name="modify-the-revenue-recognition-schedule-details"></a>Modifikuoti įplaukų pripažinimo grafiko informaciją

Daugumos įplaukų grafiko duomenų išsamios informacijos redaguoti negalima. Į grafiką negalima įtraukti naujų eilučių, o esamų eilučių negalima ištrinti. Kiekvienos pardavimo užsakymo eilutės įplaukų grafiko informacija turi būti išlaikyta, kad būtų galima garantuoti, jog per tam tikrą laikotarpį organizacija pripažins tą pačią sumą, kuri buvo atidėta.

### <a name="edit-schedule-lines"></a>Redaguoti grafiko eilutes

Kai kuriuos pakeitimus grafiko eilutėse leidžiama atlikti. Eilutėse galima keisti šiuos laukus:

- **Sulaikyta** – šią vėliavėlę galima nustatyti arba išvalyti prieš apdorojant eilutę. Norėdami išvalyti vėliavėlę, pasirinkite eilutę ir tada pasirinkite **Šalinti sulaikymą**. Įplaukų negalima pripažinti sulaikytose eilutėse. Eilutes galima automatiškai sulaikyti, jei įplaukų grafikas yra nustatytas automatiniams sulaikymams.

    [![Įplaukų grafikai – redaguoti grafiko eilutes.](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)

- **Pripažinimo data** – pripažinimo datą galima keisti prieš apdorojant eilutę. Vykdant procesą, kurio metu sukuriamas įplaukų pripažinimo žurnalas, lauke **Pripažinti įplaukas nuo datos** įvedama data. Ši data yra lyginama su data, esančia lauke **Pripažinimo data**, kad būtų galima nustatyti, kurias eilutes reikia pripažinti.
- **Suma, kurią reikia išleisti** – sumą, kuri bus išleista, galima keisti prieš apdorojant eilutę. Galite sumažinti pripažintų įplaukų sumą, tačiau negalite jos padidinti. Šis laukas leidžia organizacijai pripažinti dalį įplaukų pripažinimo dieną. Jei suma keičiama, lauke **Likusi suma** nurodyta suma rodo, kiek įplaukų vis dar reikia pripažinti.
- **Išleistinas kiekis** – jei įplaukų grafikas nustatomas vienam įvykiui ar vienam mėnesiui, lauke **Išleistinas kiekis** rodomas pardavimo užsakymo eilutės kiekis. Šis laukas taip pat gali būti redaguojamas ir yra kitas būdas pripažinti dalį įplaukų. Pavyzdžiui, jei kiekis eilutėje yra 5, galite jį perrašyti, kad būtų mažiau nei 5. Suma lauke **Suma, kurią reikia išleisti** atnaujinama proporcingai.

### <a name="update-contract-terms"></a>Naujinti sutarties sąlygas

Išsami įplaukų grafiko informacija sudaroma remiantis įplaukų grafiku, priskirtu pardavimo užsakymo eilutei, kai registruojama SF. Jei pardavimo užsakymo eilutėje esantis įplaukų grafikas yra neteisingas, jo, išrašius pardavimo užsakymo SF, pakeisti negalima. Norėdami pakeisti įplaukų grafiką, naudokite mygtuką **Naujinti sutarties sąlygas**. Įplaukų grafiką galima pakeisti prieš pripažįstant įplaukas arba po to.

Norėdami pakeisti grafiką, pasirinkite bet kurią keičiamos prekės grafiko eilutę. Tolesnėje iliustracijoje pasirinkta prekės S0008, užregistruotos naudojant 12 mėnesių įplaukų grafiką, eilutė. Pasirinkus **Naujinti sutarties sąlygas**, dialogo lange rodomos sutarties pradžios ir pabaigos datos bei įplaukų grafikas.

[![Sutarties pradžios ir pabaigos datos.](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)

Pakeiskite sutarties pradžios ir pabaigos datas taip, kad jos atspindėtų teisingą datų intervalą. Keičiant datų intervalą, lauke **Pasikartojimų skaičius** esanti reikšmė turi atitikti įplaukų grafiką, apibrėžtą sistemoje. Šiame pavyzdyje, kadangi sutartis buvo pakeista į 24 mėnesių sutartį, turi būti nustatytas 24 mėnesių įplaukų grafikas. Kadangi yra 24 mėnesių įplaukų grafikas, jis įvedamas pagal numatytuosius nustatymus, ir sutartį galima keisti. Jei nėra įplaukų grafiko, turinčio atitinkamą įvykių skaičių, sutarties keisti negalima. Baigę naujinti sutarties sąlygas ir įplaukų grafiką, dialogo lange pasirinkite **GERAI**, kad išsaugotumėte pakeitimus.

[![Atnaujintas sutarties datų intervalas.](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)

Sutarties pakeitimai turi tokią įtaką įplaukų grafiko informacijai:

- Jei už produktą įplaukos nebuvo pripažintos, visa ankstesnė grafiko informacija bus pašalinta ir pakeista nauja įplaukų grafiko informacija. Pavyzdžiui, prekė S0008 iš pradžių turėjo 12 eilučių grafiko informacijoje. Remiantis naujuoju įplaukų grafiku, šios 12 eilučių pašalinamos ir pakeičiamos 24 eilutėmis.
- Jei įplaukos buvo pripažintos už produktą, kai kurios įplaukos buvo neteisingai pripažintos, nes pripažinimas buvo pagrįstas neteisingu įplaukų grafiku. Remiantis naujuoju grafiku, šios eilutės turi būti atšaukiamos ir pripažįstamos dar kartą. Tokiu atveju, sukuriamos naujos įplaukų grafiko eilutės, kurių pradinėmis pripažinimo datomis sumos yra neigiamos. Tada sukuriamos naujos eilutės sumoms pripažinti pagal naują įplaukų grafiką. Pavyzdžiui, 2019 m. rugpjūčio 8 d. pripažinote įplaukas už 10,53 USD. 2019 m. rugsėjo 8 d. pripažinote įplaukas už 13,16 USD. Todėl tomis pačiomis datomis sukuriamos dvi naujos eilutės. Viena eilutė skirta 10,53 USD, o kita eilutė skirta 13,16 USD. Tada sukuriamos dvidešimt keturios naujos eilutės ir joms paskirstomos visos 160,61 USD atidėtos įplaukos. Galite registruoti atšaukimo eilutes vykdydami procesą **Kurti žurnalą**.

[![Įplaukų pripažinimo grafikas.](./media/revenue-recognition-rev-recog-schedule-03.png)](./media/revenue-recognition-rev-recog-schedule-03.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]