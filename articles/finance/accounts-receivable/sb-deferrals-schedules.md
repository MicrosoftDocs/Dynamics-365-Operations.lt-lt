---
title: Įplaukų ir išlaidų atidėjimų grafikai
description: Šioje temoje aprašomi įplaukų ir išlaidų atidėjimų atidėjimų grafikai.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 9135ac733496a0c5d79669c35972c273c209f81d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685983"
---
# <a name="deferral-schedules"></a>Atidėjimo grafikai

Atidėjimo grafikai kuriami po operacijos registravimo.

Galite naudoti visų **atidėjimų grafikų arba** aktyvių **atidėjimų grafikų** puslapį norėdami peržiūrėti atidėjimo grafiko informaciją. Rodoma informacija priklauso nuo atidėjimo grafiko tipo (tiesiogiai eilutė arba pagrįsta įvykiu) ir operacijos tipo. Joje yra atidėjimo grafiko eilutės ir visos atidėjimo grafiko sumos. Galite naudoti šį puslapį atidėjimo grafikui modifikuoti.

## <a name="recognize-revenue"></a>Pripažinti įplaukas

> [!NOTE]
> - Norėdami atpažinti vieno atidėjimo grafiko įplaukas, pradėkite nuo 1 veiksmo.
> - Norėdami atpažinti kelių grafikų įplaukas, pradėkite 2 žingsnyje.

1. Visų atidėjimų grafikų puslapyje, grafiko **eilučių tinklelyje**, pasirinkite eilutes, kurias norite atpažinti, ir pasirinkite **Atpažinti**.**·**
2. Atpažinimo **apdorojimo puslapyje** nustatykite lauke Atpažinimo **veiksmas** galite kurti atpažinimo **žurnalą**.
3. **Galutinę datą pasirinkite** galutinę datą. Apdorojant bus įtrauktos tik tos eilutės, kurių pabaigos data yra ankstesnė arba tokia pati kaip pasirinkta galutinė data.
4. Pasirinkite **Filtras** ir pridėkite duomenų filtrus, kad sąraše būtų rodomas tik norimų įrašų diapazonas.
5. Norėdami **peržiūrėti eilutes,** pasirinkite Peržiūra.
6. Eilučių sąraše pasirinkite visas eilutes, kurių nenorite apdoroti, tada pasirinkite **Pašalinti**.
7. Pasirinkite, ar norite susumuoti atpažinimo žurnalo įrašą.
8. Operacijos datos **skyriuje** galite perrašyti operacijos datą su konkrečia data, kad būtų galima apdoroti operaciją. Gali būti nurodyta uždarytų laikotarpių operacijos data.
9. Norėdami atlikti apdorojimą kaip paketo dalį, pasirinkite **Paketas**. Paketinio **vykdymo dialogo** lange nustatykite paketo parametrus, o tada pasirinkite Gerai, **norėdami** grįžti į atpažinimo **apdorojimo** puslapį. Įplaukų pripažinimas bus apdorotas vėliau, kai bus apdorojamas paketas.
10. Pasirinkite **procesą**. Jei įtraukote operaciją į paketą, visos eilutės bus apdorotos iš karto. Kitaip eilutės bus apdorotos, kai bus apdorotas paketas.

## <a name="modify-a-schedule"></a>Modifikuoti grafiką

Norėdami modifikuoti atidėjimo grafiką, atlikite šiuos veiksmus.

1. Puslapyje Visi **atidėjimų grafikai** pasirinkite atidėjimų grafiką, tada pasirinkite Apskaitos modifikavimo **\> grafiką**.
2. Puslapyje Modifikuoti **grafiką** redaguokite norimas keisti pasirinktis. Atsižvelgiant į atidėjimo grafiką, visų pasirinkčių redaguoti negalėsite.
3. Pasirinkite **Peržiūra**, norėdami peržiūrėti atidėjimo grafiko pakeitimus.
4. Pasirinkite **Gerai**.

### <a name="straight-line-deferral-schedules"></a>Tiesiogiai suplanuoti atidėjimo grafikai

Jei atidėjimo grafike nėra nei atpažinto, nei išoriškai užregistruotų eilučių, galite modifikuoti visą atidėjimo grafiką, įskaitant pradžios datą.

Jei atidėjimo grafike yra nei atpažinto, nei išoriškai užregistruotų eilučių, o jūs modifikuojate atidėjimo grafiką, atidėjimo grafiko veikimo būdas priklauso nuo atpažinto eilučių perskaičiavimo datos ir atidėjimo pabaigos datos. Pagal numatytuosius nustatymus pirmasis neatpažintas laikotarpis apibrėžia atidėjimo pabaigos datą.

Norėdami naudoti atpažinimo datą, grafiko pradžios lauke pasirinkite vieną **iš šių** verčių: 
- **Catch Up** – suma, kai perskaičiuojamos visos atpažintos eilutės.
- **Atšaukimas** – visos eilutės po perskaičiavimo datos atšaukiamos naudojant nurodytą žurnalo pavadinimą ir registravimo datą. Tada perskaičiuojama suma po perskaičiavimo datos.

Jei šablonas naudojamas, praleistų laikotarpių nepaisoma ir šablonas naudojamas tik pabaigos datai apskaičiuoti.

### <a name="event-based-deferral-schedules"></a>Įvykiais pagrįsti atidėjimo grafikai

Įvykiu pagrįstame atidėjimo grafike galite modifikuoti visas nepripažintas eilutes.

Jei atidėjimo grafike yra kokių nors atpažinto ar išoriškai užregistruotų eilučių, negalima modifikuoti atidėjimo grafiko šablono ir paskirstymo tipo. Kai modifikuojate esamą atidėjimo grafiką, negalite pakeisti lauko Kurti **atskirus įvykius vieneto vertei**.

Jei eilutė atpažįstama arba registruojama išoriškai, pažymėtas **žymės** langelis Atpažintas.

## <a name="modify-a-deferral-or-recognition-account"></a>Modifikuoti atidėjimo arba atpažinimo sąskaitą

Norėdami modifikuoti atidėjimo grafiko atidėjimo arba atpažinimo sąskaitą, atlikite šiuos veiksmus.

1. Puslapyje Visi **atidėjimų grafikai** pasirinkite atidėjimų grafiką, tada pasirinkite Apskaitos **modifikavimo \> sąskaitą**.
2. Puslapyje Modifikuoti **sąskaitą** pasirinkite sąskaitą, kurią norite keisti (atidėjimas, trumpalaikis ar atpažinimas).
3. **Lauke Nauja sąskaita** pasirinkite naują sąskaitą.
4. Pasirinkti, ar sąskaitos pakeitimai sukurs koregavimo žurnalo įrašus.
5. Jei ankstesniame veiksme **nustatėte** pasirinktį Taip, **lauke** Žurnalo pavadinimas pasirinkite žurnalo pavadinimą, tada operacijos datą nurodykite lauke **Operacijos** data.
6. Pasirinkite **Gerai**.

## <a name="put-a-deferral-schedule-on-hold"></a>Sulaikyti atidėjimo grafiką

Norėdami sulaikyti atidėjimo grafiką, atlikite šiuos veiksmus.

1. Puslapyje Visi **atidėjimų grafikai** pasirinkite atidėjimų grafiką, tada pasirinkite Sulaikyti **\> vietą**.
2. Puslapyje Vietos **sulaikymas** pasirinkite, ar norite perkelti balansą iš atidėjimo sąskaitos, ar iš sulaikytos sąskaitos.
3. Jei pasirinkote perkelti balansą, **pasirinkite** žurnalo pavadinimą lauke Žurnalo pavadinimas, **pasirinkite sulaikytą sąskaitą lauke Sulaikyta sąskaita** **ir nurodykite operacijos datą lauke Operacijos** data.
4. Pasirinkite **Gerai**.

## <a name="remove-a-hold-from-a-deferral-schedule"></a>Šalinti sulaikymas iš atidėjimo grafiko

Norėdami pašalinti atidėjimo grafiką iš sulaikymo, atlikite šiuos veiksmus.

1. Sąraše Visi **atidėjimų grafikai** pasirinkite atidėjimų grafiką, tada pasirinkite Sulaikyti šalinimą **\>**.
2. Lauke Žurnalo **pavadinimas** pasirinkite žurnalo pavadinimą.
3. **Lauke Operacijos data** nurodykite operacijos datą.
4. Pasirinkite **Gerai**.

## <a name="cancel-unrecognized-amounts"></a>Atšaukti neatpažintas sumas

> [!NOTE]
> Į šį procesą neįtraukiamos visos eilutės, kurios jau buvo atpažinto ar išoriškai užregistruotos.

Norėdami atšaukti nepripažintas atidėjimo grafiko sumas, atlikite šiuos veiksmus.

1. Puslapyje Visi **atidėjimų grafikai** pasirinkite atidėjimų grafiką, tada pasirinkite **Atšaukti \> nepripažintas sumas**.
2. Puslapyje Atšaukti **nepripažintą sumą** pasirinkite, ar norite sukurti atšaukimo įrašus.
3. Jei pasirinkote kurti atšaukimo įrašus, **pasirinkite** žurnalo pavadinimą lauke Žurnalo pavadinimas, **pasirinkite atšaukimo sąskaitą lauke Atšaukimo** sąskaita ir **nurodykite operacijos datą lauke Operacijos** data.
4. Pasirinkite **Gerai**.

## <a name="cancel-a-completed-schedule"></a>Baigto grafiko atšaukimas

Naudokite puslapį Visi **atidėjimų grafikai, norėdami atšaukti bet kokias atpažįstamas ar išoriškai užregistruotas sumas** ir atšaukti atidėjimų grafiką, kad išvengtumėte tolesnio atpažinimo.

Norėdami atšaukti visą atidėjimo grafiką, atlikite šiuos veiksmus.

1. Puslapyje Visi **atidėjimų grafikai** pasirinkite atidėjimo grafiką, tada pasirinkite Atšaukti baigtą **\> grafiką**.
2. Užbaigto **grafiko atšaukimo** puslapyje pasirinkite, ar norite sukurti atšaukimo įrašus.
3. Jei pasirinkote kurti atšaukimo įrašus, **pasirinkite** žurnalo pavadinimą lauke Žurnalo pavadinimas, **pasirinkite** sąskaitą lauke Atšaukimo sąskaita ir **nurodykite operacijos datą lauke Operacijos** data.
4. Pasirinkite **Gerai**.

## <a name="reverse-transactions"></a>Atšaukti operacijas

> [!NOTE]
> - Norėdami atšaukti vieno atidėjimo grafiko įplaukų pripažinimą, pradėkite 1 veiksmą.
> - Norėdami atšaukti įplaukų pripažinimą keliems grafikams, pradėkite nuo 2 veiksmo.

1. **Visų atidėjimų grafikų** puslapyje, **grafiko eilučių tinklelyje**, pasirinkite eilutes, kurių norite neatpažinti, ir pasirinkite **Atšaukti**.
2. Atpažinimo **apdorojimo puslapyje** nustatykite lauke Atpažinimo **veiksmas** pakeiskite atpažinimo **žurnalą**.
3. **Galutinę datą pasirinkite** galutinę datą. Apdorojant bus įtrauktos tik tos eilutės, kurių pabaigos data yra ankstesnė arba tokia pati kaip nurodyta galutinė data.
4. Pasirinkite **Filtras** ir pridėkite duomenų filtrus, kad sąraše būtų rodomas tik norimų įrašų diapazonas.
5. Norėdami **peržiūrėti eilutes,** pasirinkite Peržiūra.
6. Eilučių sąraše pasirinkite visas eilutes, kurių nenorite apdoroti, tada pasirinkite **Pašalinti**.
7. Laukai **Pavadinimas** ir **aprašymas** automatiškai atnaujinami numatytuoju žurnalo pavadinimu ir aprašymu. Jei reikia, vertes galima keisti. Taip pat galite pasirinkti, ar norite susumuoti pripažinimo žurnalo įrašą.
8. Operacijos datos **skyriuje** galite perrašyti operacijos datą su konkrečia data, kad būtų galima apdoroti operaciją. Gali būti nurodyta uždarytų laikotarpių operacijos data.
9. Norėdami atlikti apdorojimą kaip paketo dalį, pasirinkite **Paketas**. Paketinio **vykdymo dialogo** lange nustatykite paketo parametrus, o tada pasirinkite Gerai, **norėdami** grįžti į atpažinimo **apdorojimo** puslapį. Atvirkštinis įplaukų pripažinimas bus apdorotas vėliau, kai paketas bus apdorotas.
10. Pasirinkite **Gerai**. Jei įtraukote operaciją į paketą, visos eilutės bus apdorotos iš karto. Kitaip eilutės bus apdorotos, kai bus apdorotas paketas.

## <a name="apply-or-unapply-a-credit-note"></a>Taikyti arba netaikomi kredito pažymą

Norėdami taikyti kredito pažymą, atlikite šiuos veiksmus.

> [!NOTE]
> Kai **kuriate** **·** **kredito pažymą pardavimo užsakymo operacijos atidėjimo puslapyje ir nustatote esamo grafiko koregavimo pasirinktį kaip Taip**, kredito pažyma automatiškai taikoma grafikui, kai užregistruojama kredito pažyma.

1. **Puslapyje Visi atidėjimų grafikai** pasirinkite atidėjimo grafiką.
2. Sąraše Kredito **koregavimas** pasirinkite eilutę, tada pasirinkite **Taikyti**.
3. Puslapyje Taikyti **kredito pažymą (atidėjimus)** **·** **nurodykite perskaičiavimo datą lauke Perskaičiavimo data ir pabaigos datą pabaigos datos** lauke.
4. Antraščių **sąraše** pasirinkite pardavimo užsakymą **, kuriame** yra kredito pažymų.
5. **Eilučių sąraše** pasirinkite eilutę.
6. Pasirinkite **Gerai**.
7. Pasirinkite **Taip**.

> [!NOTE]
> Norėdami taikyti kredito pažymą kelioms atskiroms prekėms iš skirtingų SF, turite pakartoti šiuos veiksmus.

Norėdami iš naujo taikyti kredito pažymą, atlikite šiuos veiksmus.

1. **Puslapyje Visi atidėjimų grafikai** pasirinkite atidėjimo grafiką.
2. Sąraše Kredito **koregavimas** pasirinkite SF, tada – **Unapply**.
3. Pasirinkite **Taip**.

## <a name="fields"></a>Laukai

Visų **atidėjimų grafikų puslapyje** yra šie laukai.

| Laukai | Aprašymas |
|--------|-------------|
| **Antraštė** | |
| **Grafikas** | |
| Paskirstymo tipas | Paskirstymo tipas, kai atidėjimai pagrįsti įvykiu: procentas **arba** **suma**. |
| Perklasifikavimo data | <p>Vėliausia data, kai buvo apdorotas trumpalaikis atidėjimo grafiko perklasifikavimas. Ši data atnaujinama kiekvieną kartą, kai atidėjimo **grafike naudojamas** trumpalaikis įvykio perklasifikavimas.</p>Šis laukas galimas tik tada, kai naudojamas ėjimo laikotarpis arba fiksuotų metų trumpalaikis atidėjimo metodas. |
| **Sąskaita** | |
| Atidėjimo sąskaita | Sąskaita, naudojama atidėjimo sumai. |
| Pripažinimo sąskaita | Sąskaita, naudojama atpažinimo sumai. |
| Pripažinimo tipas | Atpažinimo tipas. |
| Paskirstymo tipas | Paskirstymo tipas. |
| **Operacija** | |
| Kūrimo šaltinis | Šaltinis, iš kurios buvo sukurta operacija. |
| Operacijos tipas | Operacijos tipas. |
| Pardavimo užsakymas | Pardavimo užsakymo numeris. |
| Sąskaita faktūra | Sąskaitos faktūros numeris. |
| Elementas | Prekės numeris. |
| **Atsiskaitymo grafikas** | |
| Atsiskaitymo grafiko numeris | Atitinkamo atsiskaitymo grafiko numeris. |
| Atsiskaitymo eilutės būsena | Atitinkamo atsiskaitymo grafiko eilutės elemento būsena. |
| Išorinės nuorodos | Informacija apie išorines nuorodas iš sąskaitų pateikimo grafiko: **išorinis** ir **eilutės numeris**. |
| Sumos | <p>Atidėjimo grafiko sumos:</p><ul><li>**Ilgalaikis –** ilgalaikių atidėtų sumų suma. Ši vertė galima **tik** **tada, kai nustatytas trumpalaikio atidėjimo metodo laukas Nėra** **puslapyje Įplaukų ir išlaidų atidėjimų** parametrai arba trumpalaikių išlaidų suma yra didesnė nei 0 (nulis).</li><li>**Trumpalaikis** – trumpalaikių atidėtų sumų suma. Ši vertė galima **tik** **tada, kai nustatytas trumpalaikio atidėjimo metodo laukas Nėra** **puslapyje Įplaukų ir išlaidų atidėjimų** parametrai arba trumpalaikių išlaidų suma yra didesnė nei 0 (nulis).</li><li>**Nežinoma –** visų eilučių neatpažintų sumų suma.</li><li>**Užsispyriniai** – išoriškai užregistruotų sumų visose eilutėse suma.</li><li>**Atpažinta** – visų eilučių atpažinų sumų suma.</li><li>**Išoriškai užregistruota ir atpažinta** – iš išorės užregistruotų ir atpažinų visų eilučių sumų suma.</li><li>**Bendroji suma** – visų eilučių sumų suma.</li></ul> |
| **Grafiko eilutės** | |
| Eilutė | Eilutės eilės numeris. |
| Atidėjimo pradžios data | Atidėjimo grafiko pradžios data. |
| Atidėjimo pabaigos data | Atidėjimo grafiko pabaigos data. |
| Suma | Atidėjimo suma. |
| Išoriškai užregistruota | Vertė, nurodanti, ar eilutė buvo užregistruota išoriškai. |
| Pripažinta | Vertė, kuri nurodo, ar eilutė buvo atpažinta. |
| Žurnalo numeris | Paketo, kuriame buvo atpažinta suma, numeris. |
| Įvykio aprašas | Įvykio aprašymas. Šis laukas galimas tik atidėjimo pagal įvykį grafikams. |
| **Kredito koregavimai** | |
| Sąskaita faktūra | <p>Sąskaitos faktūros numeris.</p><p>Vertė nurodo kredito pažymos koregavimo SF, kuri jau buvo pritaikyta atidėjimo grafike.</p> |
| Taikyta suma | Kredito koregavimo suma, jau taikyta atidėjimo grafikui. |
| Pritaikyta data | Data, kada buvo pritaikytas kredito koregavimas. |
| **Koregavimas** | Koregavimo vertės rodomos tik tada, jei atidėjimo grafikui buvo apdorota kredito pažyma. Jei kredito pažyma nebuvo apdorota, šios vertės paslėptos. |
| Koregavimo suma | Bendroji koregavimo suma, apskaičiuota kaip pradinė *suma* – grafiko *suma*. |
| Pradinė pabaigos data | Pradinė atidėjimo grafiko pabaigos data. |
| Pradinė grafiko suma | Pradinio atidėjimo grafiko bendroji suma. |
