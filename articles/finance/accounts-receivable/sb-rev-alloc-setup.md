---
title: Nustatyti kelių elementų įplaukų paskirstymą
description: Šioje temoje aprašoma, kaip nustatyti kelių elementų įplaukų paskirstymo parametrus abonemento sąskaitose.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: e422b16d1c4505b2837bb282918ecada902b806e
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2022
ms.locfileid: "8566567"
---
# <a name="set-up-multiple-element-revenue-allocation"></a>Nustatyti kelių elementų įplaukų paskirstymą

Kelių elementų įplaukų paskirstymas leidžia nustatyti skirtingus šablonus, naudojamus įplaukoms apskaičiuoti ir paskirstyti keliose prekėse. Ši funkcija gali padėti jums laikytis apskaitos standartų kodifikavimo temos 606 (ASC 606) ir / arba 15 tarptautinių finansinių ataskaitų standarto (IFRS 15).

## <a name="multiple-element-revenue-allocation-parameters"></a>Kelių elementų įplaukų paskirstymo parametrai

Naudokite kelių **elementų įplaukų paskirstymo parametrų** puslapį, kad nustatyti kelių elementų įplaukų paskirstymo parametrus.

### <a name="standalone-selling-price-origin"></a>Atskiros prekės pardavimo kainos kilmė

Atskiras **pardavimo kainos kilmės laukas** nustato, iš kur gaunama atskira pardavimo kaina. Vertę galite atnaujinti puslapyje Prekės **atskira pardavimo kaina ir** operacijoje. Galimos toliau nurodytos pasirinktys.

| Parinktis | Aprašymas |
|--------|-------------|
| Suma | Atskira pardavimo kaina yra suma, kurią nurodote, yra didesnė nei 0 (nulis). Jei reikia, suma konvertuojama tarp funkcinių ir keliomis valiutomis. |
| Bazinė pardavimo kaina | Atskira pardavimo kaina sutampa su bazine prekės pardavimo kaina. |
| Sąskaitos faktūros kaina | Atskira pardavimo kaina sutampa su prekės SF kaina. |
| Prekės procentas | Atskira pardavimo kaina nurodoma kaip procentinė vertė ir skaičiuojama remiantis prekės kaina. Jei pasirinksite šią pasirinktį, nurodykite numatytąjį procentą. |
| Paskirstyti likutinę sumą | <p>Atskirą pardavimo kainą kilmė apskaičiuojama *kaip* bendroji pirminės prekės sutarties vertė – *bendroji atskira antrinių prekių pardavimo kaina*:</p><ul><li>*Bendroji pirminės prekės sutarties vertė yra* grynoji arba išrašytų sąskaitų suma.</li><li>*Bendroji atskira antrinių* prekių pardavimo kaina yra bendroji visų antrinių prekių išplėstinės ar sutarties atskira pardavimo kaina, išskyrus antrųjų prekių, kurios naudoja šią atskirą pardavimo kainos kilmę.</li></ul><p>Jei apskaičiuota suma yra neigiama, suma nustatoma 0 (nulis).</p><p>**Pastaba: šią** pasirinktį galima pasirinkti tik vienam antriniam elementui išskaidytoje įplaukų skaidymo metu.</p> |
| Jokia | Atskira pardavimo kaina kilmė yra grindžiama antriniais elementais. Ši pasirinktis taikoma prekėms, kurios įplaukų skaidymo šablone apibrėžtos kaip pirminės prekės. Jei pažymėtas **žymės langelis** Įplaukų skaidymo, ši pasirinktis automatiškai pasirinkta ir parametro pakeisti negalima. |
| Pirminės sąskaitos faktūros kainos procentas | Atskirą pardavimo kainą kilmė yra pirminės prekės SF kainos procentas. Numatytąją vertę galite keisti. Ši pasirinktis galima tik antriniams elementams įplaukų skaidymo šablone. |
| Pirminės standartinės kainos procentas | Standartinės pardavimo kainos kilmė yra standartinės pirminės prekės kainos procentas. Numatytąją vertę galite keisti. Ši pasirinktis galima tik antriniams elementams įplaukų skaidymo šablone. Tai numatytoji antrinių prekių pasirinktis. **·** **·** **·** **Kai** antrinių prekių pasirinktis pakeičiama iš pirminės standartinės kainos procentinės dalies į Pirminės SF kainos procentas arba iš Pirminės SF kainos procentinės dalies į Pirminės standartinės kainos procentas, apskaičiuotos vertės taip pat atnaujinamos. |

### <a name="account-for-revenue-allocation-rounding-differences"></a>Atsižvelgti į įplaukų paskirstymo apvalinimo skirtumus

Įplaukų **paskirstymo apvalinimo skirtumų lauko** sąskaita nurodo sąskaitą, kuri naudojama bet kokiems sutarties įplaukų sumos apvalinimo koregavimams įrašyti. Jis galimas, kai naudojamas periodinis sutarties atsiskaitymas.

## <a name="item-standalone-selling-price"></a>Atskira prekės pardavimo kaina

Norėdami nurodyti **prekės kilmę ir atskirą pardavimo** kainą, naudokite atskirą prekės pardavimo kainos puslapį. Šiame puslapyje nurodytos vertės naudojamos kaip **numatytosios** vertės kelių elementų įplaukų paskirstyme ir periodiniame sutarties sąskaitų išrašymo puslapyje Įplaukų paskirstymas.

### <a name="specify-item-standalone-selling-price"></a>Nurodyti prekės atskirą pardavimo kainą

Norėdami nurodyti atskirą prekės kainą, atlikite šiuos veiksmus.

1. **Atskiras prekės pardavimo kainos** puslapis, **atskiras** pardavimo kainos kilmės laukas, pasirinkite atskirą pardavimo kainą.
2. Atlikite vieną iš šių veiksmų, atsižvelgdami į vertę, kurią pasirinkote skirtuko **pardavimo kainos kilmės** lauke:

    * Jei pasirinkote **Prekės procentas**, nurodykite procentą lauke **Procentas**.
    * Jei pasirinkote **Suma**, nurodykite sumą atskiras **pardavimo kainos** lauke.

2. Kiekvienos į sąrašą norimos įtraukti prekės pasirinkite **Įtraukti**.
3. **Lauke Prekės kodas** pasirinkite prekės kodą. **Lauke Prekės ryšys** pasirinkite prekės ryšį. Prekėms, kurių žymės **langelis** Įplaukų skaidymo žymės langelis išvalytas, pasirinktas prekės kodo ir prekės ryšio derinys turi būti unikalus.
4. Jei reikia, pakeiskite atskirą **pardavimo kainos kilmės, atskirą** **·** **pardavimo** kainą arba procento lauką.
5. Kiekvienos pirminės prekės, kurią norite įtraukti į sąrašą, atveju pasirinkite **Įtraukti**.
6. **Lauke Prekės kodas** pasirinkite prekės kodą. **Lauke Prekės ryšys** pasirinkite prekės ryšį.
7. Pažymėkite žymės langelį **Įplaukų skaidymo**.
8. **Lauke Prekės ryšys** pasirinkite prekės ryšį. Sąrašas atnaujinamas pirmine preke ir visomis antriniomis prekėmis.
9. **Pakeiskite** atskirą pardavimo kainos kilmės numatytąją vertę, pirminės standartinės kainos procentą, **·** **pirminės** SF kainos procentą arba, jei reikia, **paskirstykite** likučio sumos lauką.
10. Norėdami pridėti keletą prekių vienu metu, pasirinkite **Įtraukti prekes**.
11. Atnaujinti užklausą, kad būtų galima pasirinkti prekių, kurias norite įtraukti, diapazoną.
12. Pasirinkite **Gerai**, peržiūrėkite pridėtų prekių sąrašą ir pasirinkite **Gerai**.

### <a name="fields"></a>Laukai

Prekės **atskirą pardavimo kainos puslapį** sudaro šie laukai.

| Laukas | Aprašymas |
|-------|-------------|
| Atskiros prekės pardavimo kainos kilmė | <p>Pasirinkite atskirą pardavimo kainos kilmę:</p><ul><li>**Suma** – atskira pardavimo kaina yra suma, kurią nurodote, kuri yra didesnė nei 0 (nulis). Jei reikia, suma konvertuojama tarp funkcinių ir keliomis valiutomis.</li><li>**Bazinė pardavimo** kaina – atskira pardavimo kaina atitinka prekės bazinę pardavimo kainą.</li><li>**SF kaina** – atskira pardavimo kaina atitinka prekės SF kainą.</li><li>**Prekės procentas** – atskira pardavimo kaina nurodoma kaip procentinė vertė ir skaičiuojama remiantis prekės kaina. Jei pasirinksite šią pasirinktį, nurodykite numatytąjį procentą.</li></ul>**Paskirstyti likutinę** sumą – *atskira* pardavimo kaina apskaičiuojama kaip bendroji pirminės prekės sutarties vertė – *bendroji atskira antrinių prekių pardavimo kaina*:</p><ul><li>*Bendroji pirminės prekės sutarties vertė yra* grynoji arba išrašytų sąskaitų suma.</li><li>*Bendroji atskira antrinių* prekių pardavimo kaina yra bendroji visų antrinių prekių išplėstinės ar sutarties atskira pardavimo kaina, išskyrus antrųjų prekių, kurios naudoja šią atskirą pardavimo kainos kilmę.</li></ul><p>Jei apskaičiuota suma yra neigiama, suma nustatoma 0 (nulis).</p><p>**Pastaba: šią** pasirinktį galima pasirinkti tik vienam antriniam elementui išskaidytoje įplaukų skaidymo metu.</p></li><li>**Nėra** – atskira pardavimo kaina kilmė – priklauso nuo antrinių prekių. Ši pasirinktis taikoma prekėms, kurios įplaukų skaidymo šablone apibrėžtos kaip pirminės prekės. Jei pažymėtas **žymės langelis** Įplaukų skaidymo, ši pasirinktis automatiškai pasirinkta ir parametro pakeisti negalima.</li><li>**Pirminės SF kainos procentas** – atskira pardavimo kaina yra pagrindinės prekės SF kainos procentas. Numatytąją vertę galite keisti. Ši pasirinktis galima tik antriniams elementams įplaukų skaidymo šablone.</li><li>**Pirminės standartinės kainos** procentas – atskira pardavimo kaina yra standartinės pirminės prekės kainos procentas. Numatytąją vertę galite keisti. Ši pasirinktis galima tik antriniams elementams įplaukų skaidymo šablone. Tai numatytoji antrinių prekių pasirinktis. **·** **·** **·** **Kai** antrinių prekių pasirinktis pakeičiama iš pirminės standartinės kainos procentinės dalies į Pirminės SF kainos procentas arba iš Pirminės SF kainos procentinės dalies į Pirminės standartinės kainos procentas, apskaičiuotos vertės taip pat atnaujinamos.</li></ul> |
| Atskira pardavimo kaina | Nurodykite atskirą prekės pardavimo kainą. Šis laukas galimas, kai **atskiras pardavimo kainos kilmės** laukas nustatytas kaip **Suma**. |
| Procentas | Nurodyti atskirą pardavimo kainos procentą. Šis laukas galimas, kai **atskiras** **pardavimo** kainos kilmės laukas nustatytas į Prekės procentas, **·** **Pirminės SF kainos procentas arba Pirminės standartinės kainos procentas.** |
| Įplaukų padalijimas | <p>Nurodyti, ar eilutėje naudojamas įplaukų skaidymas:</p><ul><li>**Pasirinkta** – prekių ryšių lauke galima pasirinkti tik tas prekes, kurių įplaukų skaidymo **šablonas nustatytas**. Šį žymės langelį galima pažymėti tik įplaukų skaidymo šablono pirminėms prekėms.</li><li>**Išvalyta** – prekė yra standartinė prekė, kuri nenaudojo įplaukų skaidymo.</li></ul> |
| Ryšys | Simbolis nurodo, ar įplaukų skaidymo metu prekė yra pirminė, ar pirminė prekė. |
| Prekės kodas | <p>Pasirinkti prekės kodą: Lentelė **arba** **Grupė**.</p><p>Jei pažymėtas **žymės langelis** Įplaukų skaidymo, šis laukas **nustatytas** kaip Lentelė ir vertės keisti negalima.</p> |
| Prekės ryšys | <p>Pasirinkite prekės numerį.</p><p>Jei pažymėtas žymės **langelis Įplaukų** skaidymo, galima pasirinkti tik tas prekes, kurios yra pagrindinės prekės, kurias galima pasirinkti pagal įplaukų skaidymo šabloną. Kai pasirenkama pirminė prekė, sąrašas automatiškai atnaujinamas naudojant tos pirminės prekės antinamas prekes.</p> |
| Pirminė prekė | Šiame lauke rodomas pirminės prekės prekės numeris. Antrinių prekių, išskaidytų įplaukų metu, joje rodomas pirminės prekės numeris. |

## <a name="mea-templates"></a>MEA šablonai

Norėdami sukurti **ir redaguoti kelių** elementų išdėstymo (MEA) šablonų ID, naudokite MEA šablonų puslapį. Šie YD yra naudojami įplaukų paskirstymo **puslapyje,** norint sugrupuoti prekes.

### <a name="create-a-template"></a>Kurti šabloną

Norėdami nustatyti MEA šabloną, atlikite šiuos veiksmus.

1. **MEA šablonų** puslapyje pasirinkite **Naujas**.
1. Į MEA **šablono ID** lauką įveskite unikalų ID.
1. Lauke **Aprašas** įveskite aprašą.
1. Lauke Atidėtų **sutarčių įplaukų** sąskaita pasirinkite sąskaitą, kurią norite naudoti žurnalo įrašams, kai kuriama MEA sutarties SF. Šis laukas galimas, kai įjungtas ir naudojamas periodinis sutarties atsiskaitymas.
1. Pasirinkite **Įrašyti**.
