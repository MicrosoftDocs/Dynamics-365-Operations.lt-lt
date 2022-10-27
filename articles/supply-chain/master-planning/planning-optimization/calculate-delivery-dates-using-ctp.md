---
title: Pardavimo užsakymo pristatymo datų skaičiavimas naudojant CTP
description: Galėsite pateikti atsargų (CTP) funkcionalumą ir suteikti klientams realias datas, kada galite pateikti tam tikras prekes. Šiame straipsnyje aprašoma, kaip nustatyti ir naudoti CTP kiekvienam planavimo moduliui (planavimo optimizavimas ir įtaisytasis modulis).
author: t-benebo
ms.date: 07/20/2022
ms.topic: article
ms.search.form: SalesAvailableDlvDates, SalesTable, CustParameters, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-20
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 3b8e3dc9f0e7aaf019aa4d7284458206e7daadb2
ms.sourcegitcommit: 86c0562ce1ecdf7937125c0f5a6771f178b459e7
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/24/2022
ms.locfileid: "9714866"
---
# <a name="calculate-sales-order-delivery-dates-using-ctp"></a>Pardavimo užsakymo pristatymo datų skaičiavimas naudojant CTP

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Galėsite pateikti atsargų (CTP) funkcionalumą ir suteikti klientams realias datas, kada galite pateikti tam tikras prekes. Galima pateikti kiekvienos pardavimo eilutės datą, atsižvelgiant į turimas atsargas, gamybos pajėgumą ir transportavimo laiką.

CTP išplečia [prieinamų atsargų](../../sales-marketing/delivery-dates-available-promise-calculations.md) (ATP) funkcijas, atsižvelgdama į pajėgumų informaciją. Kadangi ATP atsižvelgiama tik į medžiagų prieinamumą ir laiko neribotus pajėgumo išteklius, CTP atsižvelgiama į medžiagų ir pajėgumų prieinamumą. Todėl jis pateikia realesnius vaizdą apie tai, ar poreikis gali būti patenkintas per nurodytą laikotarpį.

CTP šiek tiek veikia kitaip, priklausomai nuo bendrojo planavimo modulio, kurį naudojate (planavimo optimizavimas arba įtaisytasis modulis). Šiame straipsnyje aprašoma, kaip nustatyti jį kiekvienam moduliui. CTP planavimo optimizavimui šiuo metu palaiko tik CTP scenarijų, kuriuos palaiko įtaisytasis variklis, subgrupį.

## <a name="turn-on-ctp-for-planning-optimization"></a>Įjungti planavimo optimizavimo CTP

Visada galima naudoti įtaisyto bendrojo planavimo modulio CTP. Tačiau jei norite naudoti CTP planavimo optimizavimui, jis turi būti įjungtas jūsų sistemai. Administratoriai gali naudoti [funkcijos valdymas](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Bendrasis planavimas*
- **Priemonės pavadinimas:** *(peržiūra) CTP planavimo optimizavimui*

## <a name="how-ctp-compares-to-atp"></a>Kaip CTP palyginama su ATP

CTP ir ATP yra panašūs, tačiau CTP dažnai gali pateikti tikslesnius rezultatus, kaip parodyta toliau pateiktame pavyzdyje.

Prekė A yra prekė, sudaryta iš B ir C prekių, o prekių A kiekis yra 0 (nulis). Jei atP patikrinsite tik medžiagas, ATP kiekis taip pat bus 0 (nulis). Tačiau jei patikrinsite CTP, sistema patikrins B ir C prekių prieinamumą, patikrins išteklius, reikalingus jiems padaryti preke A preke ir apskaičiuos, kiek prekių A gali būti padaryta. Be to, pagal CTP skaičiavimą galima patikrinti išteklius ir medžiagas, kurių reikia norint sukurti daugiau prekių B ir C, ir naudoti jas, kad būtų daugiau prekių A.

CTP skaičiavimas, kurį atliekant atsižvelgiama į medžiagas ir išteklius, gali rodyti didesnį kiekį nei skaičiavimas, skirtas tik medžiagoms tikrinti, ypač kai tikrinama prekė yra surinkimo pagal užsakymą prekė. Kitaip tariant, CTP funkcija remiasi išskleidimo funkcija ir gali būti paleista pasirinktoje pardavimo užsakymo eilutėje, kad būtų galima apskaičiuoti numatomą pristatymo datą.

## <a name="how-ctp-differs-depending-on-the-master-planning-engine-that-you-use"></a>Kaip CTP skiriasi atsižvelgiant į jūsų naudojamas bendrojo planavimo sistemą

Šioje lentelėje apibendrinami skirtumai tarp įtaisyto bendrojo planavimo modulio CTP planavimo optimizavimo ir CTP.

| Elementas | Planavimo optimizavimas | Įtaisytasis bendrojo planavimo modulis |
|---|---|---|
| **Užsakymų,** užsakymo eilučių ir produktų pristatymo datos valdymo parametras | *CTP planavimo optimizavimui* | *Ctp* |
| Skaičiavimo laikas | Skaičiavimas suaktyvinamas paleidus dinaminį planą kaip suplanuotą užduotį. | Kiekvieną kartą, kai įvedate ar atnaujinate pardavimo užsakymo eilutę, skaičiavimas yra nedelsiant suaktyvinamas. |
| **Planavimo optimizavimo būsenos lauko vertės** CTP | <p>Rodoma užsakymų *ir užsakymo* eilučių, kuriose dinaminis planas nebuvo paleistas nuo tada, kai užsakymai ir eilutės buvo sukurti arba paskutinį kartą atnaujinti, nepasiruošta.</p><p>Rodoma paruoštų *užsakymų* ir eilučių vertė, kai CTP buvo naudojama norint apskaičiuoti patvirtintas pristatymo datas, vykdant dinaminį planą.</p> | Visada rodoma *parengta* vertė. |

## <a name="set-default-delivery-date-control-methods"></a><a name="default-methods"></a> Nustatyti numatytuosius pristatymo datos valdymo metodus

Sistema gali naudoti bet kurį iš kelių metodų kiekvieno užsakymo ir užsakymo eilutės pristatymo datos įvertinimui apskaičiuoti. Pristatymo datos valdymo metodą, kurį norite naudoti dažniausiai kaip visuotinį numatytąjį metodą, turėtumėte nustatyti. Taip pat galite nustatyti atskirus kiekvieno produkto nepaisymus. Vėliau, pagal jūsų reikalą, galėsite nepaisyti numatytųjų kiekvienos užsakymo ir (arba) užsakymo eilutės metodų.

### <a name="set-the-global-default-delivery-date-control"></a><a name="global-default"></a> Nustatyti visuotinės numatytosios pristatymo datos valdymą

Numatytasis pristatymo datos valdymo metodas bus taikomas visoms naujose užsakymo eilutėse, kuriose netaikomas perrašymo principas. Norėdami pasirinkti vieną, atlikite šiuos veiksmus.

1. Eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.
1. Skirtuke **Siuntos**, **pristatymo** valdymo "FastTab", **pristatymo** datos valdymo lauke, pasirinkite metodą, kurį norite naudoti kaip numatytąjį įmonės metodą:

    - *Nėra* – neskaičiuoti pristatymo datų.
    - *Pardavimo vykdymo laikas* – pardavimo vykdymo laikas yra laikas tarp pardavimo užsakymo sukūrimo ir prekių siuntimo. Pristatymo datos skaičiavimas pagrįstas numatytuoju dienų skaičiumi, bet nenagrinėkime atsargų prieinamumo, žinomo poreikio ar suplanuoto tiekimo.
    - *ATP* – ATP yra prekės kiekis, kuris yra galimas ir gali būti pažadėtas klientui konkrečią dieną. Skaičiuojant ATP, apimamos nefiksuotos atsargos, vykdymo laikai, suplanuoti gavimai ir išdavimai.
    - *ATP + išdavimo laiko* rezervas – siuntimo data lygi ATP datai, pridėjus prekės išdavimo maržą. Išdavimo laiko rezervas yra laikas, reikalingas prekes paruošti siuntimui.
    - *CTP* – naudokite CTP skaičiavimą, kurį pateikė įtaisytasis bendrojo planavimo modulis. Jei naudojate planavimo optimizavimą, *CTP* pristatymo datos valdymo metodas neleidžiamas, todėl jį pasirinkus bus įvyko klaida skaičiuojant.
    - *CTP planavimo optimizavimui* – naudokite CTP skaičiavimą, kuris pateikiamas planavimo optimizavimo. Ši pasirinktis neturi jokios įtakos, jei naudojate įtaisytą bendrojo planavimo sistemą.

### <a name="set-delivery-date-control-overrides-for-individual-products"></a>Nustatyti atskirų produktų pristatymo datos valdymo nepaisymus

Galite priskirti tam tikrų produktų, kurių pristatymo datos valdymo metodą norite naudoti ne tai, kas nustatyta kaip jūsų visuotinis numatytasis metodas, nepaisymus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Pasirinkite norimą nustatyti produktą.
1. Veiksmų juostoje **Valdyti inventorių** skirtuke, **Užsakymo nustatymai** grupėje, rinkitės **Numatyto užsakymo nustatymai**.
1. Skirtuko Pardavimo **užsakymas "** FastTab" Puslapyje Numatytieji **užsakymo** parametrai nustatykite parinktį **Perrašyti pristatymo valdymą** kaip *Taip*.
1. **Lauke Pristatymo datos valdymas** pasirinkite pasirinktam produktui naudosimo metodą. Galimos tos pačios pasirinktys, kurios aprašytos [skyriuje Nustatyti visuotinę numatytąją](#global-default) pristatymo datą.

## <a name="schedule-ctp-for-planning-optimization-calculations"></a><a name="batch-job"></a> Planuoti CTP planavimo optimizavimo skaičiavimams

Kai naudojate CTP planavimo optimizavimui atlikti, turite paleisti dinaminį planą, kad sistema paleistų CTP skaičiavimus, o tada nustatyti visų atitinkamų užsakymų patvirtintas siuntimo ir gavimo datas. Į planą turi būti įtrauktos visos prekės, kurių siuntimo ir gavimo datos patvirtintos. (Kai naudojate CTP įtaisytam planavimo moduliui, CTP skaičiavimai nedelsiant atliekami vietoje. Todėl nereikia vykdyti dinaminį planą, kad būtų rodomi CTP rezultatai.)

Norint užtikrinti, kad datos galimos visiems vartotojams laiku, rekomenduojame nustatyti paketines užduotis, kad atitinkami planai būtų paleidžiami pasikartojančiai. Pavyzdžiui, paketinė užduotis, kuri nustatyta vykdyti dinaminį planą kas 30 minučių, patvirtintų siuntų ir gavimo datas nustato kas 30 minučių. Todėl vartotojai, kurie įves ir importuos užsakymus, turės laukti ne daugiau kaip 30 minučių, kad gautų patvirtintą siuntimo ir gavimo datą.

Norėdami nustatyti paketinę užduotį, kad pagal reguliarų planą būtų vykdomas dinaminis planas, atlikite šiuos veiksmus.

1. Pereikite prie bendrojo **planavimo \> Bendrojo planavimo \> Bendrojo \> planavimo**.
1. Dialogo lange **Bendrojo planavimo** parametrai "**FastTab**" nustatykite bendrojo **plano** lauką kaip dinaminį planą, kurį norite vykdyti.
1. Dalyje Vykdyti **fone "FastTab"** nustatykite paketinio vykdymo **parinktį** *Taip*.
1. Pasirinkite **Pasikartojimas** ir, jei reikia, nustatykite grafiką.
1. Pasirinkite **Gerai grafikui** įrašyti.
1. Pasirinkite **Gerai,** norėdami sukurti paketinę užduotį ir uždaryti dialogo langą.

## <a name="use-ctp-for-built-in-master-planning"></a>Naudoti CTP integruojant bendrąjį planavimą

### <a name="create-a-new-order-by-using-ctp-for-built-in-master-planning"></a>Kurti naują užsakymą naudojant CTP įtaisytam bendrojo planavimo užsakymui

Kiekvieną kartą, kai pridedate naują pardavimo užsakymą arba užsakymo eilutę, sistema jai priskiria numatytąjį pristatymo datos valdymo metodą. Užsakymo antraštė visada prasideda visuotiniu numatytuoju metodu. Jei perrašymo užduotis priskiriama prie užsakytos prekės, nauja užsakymo eilutė naudos šį nepaisymus. Kitu atveju naujoje užsakymo eilutėje taip pat bus naudojamas visuotinis numatytasis metodas. Todėl numatytuosius metodus turėtumėte nustatyti taip, kad jie atitiktų dažniausiai naudojamas pristatymo datos kontrolės metodą. Sukūrę užsakymą, užsakymo antraštėje ir (arba) užsakymo eilutės lygyje galite nepaisyti numatytojo metodo, jei to reikalaujate. Daugiau informacijos rasite Nustatyti numatytuosius [pristatymo datos valdymo metodus ir](#default-methods) Keisti [esamus pardavimo užsakymus, kad būtų galima naudoti CTP](#change-orders).

### <a name="view-confirmed-delivery-dates-when-you-use-ctp-for-built-in-master-planning"></a>Peržiūrėti patvirtintas pristatymo datas, kai CTP naudojama įtaisytam bendrojo planavimo metu

Jei naudojate integruotą bendrojo planavimo įrenginį, CTP skaičiavimai taikomi užsakymams ir (**arba**) užsakymų eilutėms, kur pristatymo datos valdymo laukas nustatytas kaip *CTP*.

Pardavimo eilutėms, kuriose CTP naudojamas įtaisytas bendrasis planavimas, kaskart įrašant pardavimo eilutę **sistema** **automatiškai** nustato laukus Patvirtinta siuntimo data ir Patvirtinta gavimo data. Jei vėliau pakeisite pardavimo eilutę (pvz., pakeisite jos kiekį ar svetaines), datos bus nedelsiant perskaičiuotos.

- Norėdami peržiūrėti patvirtintas pardavimo užsakymo eilutės pristatymo datas, atidarykite pardavimo užsakymą ir pasirinkite pardavimo eilutę. Tada eilutės informacijos **"FastTab"**, skirtuke **Pristatymas**, peržiūrėkite patvirtintas siuntimo **datos ir** patvirtintos **gavimo datos** vertes.
- Norėdami peržiūrėti viso užsakymo patvirtintas pristatymo datas, atidarykite pardavimo užsakymą ir pasirinkite antraštės **rodinį**. Tada skirtuko pristatyme **"** FastTab" peržiūrėkite patvirtintas siuntimo **datos ir** patvirtintos **gavimo datos** vertes.

## <a name="use-ctp-for-planning-optimization"></a>Naudoti CTP planavimo optimizavimui

### <a name="create-a-new-order-by-using-ctp-for-planning-optimization"></a>Kurti naują užsakymą naudojant CTP planavimo optimizavimui atlikti

Kiekvieną kartą, kai pridedate naują pardavimo užsakymą arba užsakymo eilutę, sistema jai priskiria numatytąjį pristatymo datos valdymo metodą. Užsakymo antraštė visada prasideda visuotiniu numatytuoju metodu. Jei perrašymo užduotis priskiriama prie užsakytos prekės, nauja užsakymo eilutė naudos šį nepaisymus. Kitu atveju naujoje užsakymo eilutėje taip pat bus naudojamas visuotinis numatytasis metodas. Todėl numatytuosius metodus turėtumėte nustatyti taip, kad jie atitiktų dažniausiai naudojamas pristatymo datos kontrolės metodą. Sukūrę užsakymą, užsakymo antraštėje ir (arba) užsakymo eilutės lygyje galite nepaisyti numatytojo metodo, jei to reikalaujate. Daugiau informacijos rasite Nustatyti numatytuosius [pristatymo datos valdymo metodus ir](#default-methods) Keisti [esamus pardavimo užsakymus, kad būtų galima naudoti CTP](#change-orders).

### <a name="view-confirmed-delivery-dates-when-using-ctp-for-planning-optimization"></a>Peržiūrėti patvirtintas pristatymo datas naudojant CTP planavimo optimizavimui

Jei naudojate planavimo optimizavimą, CTP skaičiavimai taikomi užsakymams ir (**·** *arba) užsakymų eilutėms, kurių pristatymo datos valdymo laukas nustatytas kaip CTP planavimo optimizavimui.*

Pardavimo eilučių, kurios naudoja CTP planavimo optimizavimui atlikti, **·** **laukai** Patvirtinta siuntimo data ir Patvirtinta gavimo data bus tušti, kol galėsite vykdyti atitinkamą dinaminį planą (paprastai naudojant periodinę paketinę užduotį). Tada jos automatiškai nustatomos. Daugiau informacijos ieškokite planavimo [optimizavimo skaičiavimų CTP grafike](#batch-job).

Planavimo **optimizavimo būsenos lauke** CTP nurodo, ar kiekvienai eilutei, kuri naudoja CTP planavimo optimizavimui, buvo apskaičiuotos patvirtintos datos. Lauke rodoma eilučių ir užsakymų *,* kurių patvirtintos pristatymo datos dar neskaičiuojamos arba dėl kitų pakeitimų nebegalioja, vertė. Joje rodoma apskaičiuota paruoštų *eilučių* ir užsakymų vertė. Galite peržiūrėti kiekvienos eilutės ir viso užsakymo būseną.

- Norėdami peržiūrėti pardavimo užsakymo eilutės būseną, atidarykite pardavimo užsakymą ir pasirinkite pardavimo eilutę. Tada eilutės informacijos **"** FastTab", skirtuke **Pristatymas**, peržiūrėkite **planavimo optimizavimo būsenos** vertės CTP. Eilutės **laukai Patvirtinta** siuntimo **data ir Patvirtinta** gavimo data taip pat rodomi šiame skirtuke juos apskaičiavus.
- Norėdami peržiūrėti viso užsakymo būseną, atidarykite pardavimo užsakymą ir pasirinkite antraštės **rodinį**. Tada pristatymo "**FastTab**" peržiūrėkite planavimo optimizavimo **būsenos** vertės CTP. Apskaičiuotos **užsakymo** patvirtintos **siuntimo ir** patvirtintos gavimo datos taip pat rodomos šiame skirtuke.

<!-- KFM: The following text may be untrue and needs to be reviewed with the PM for next revision:

The sales orders that are *Ready* or *Not ready* are shown in the **All sales orders** list page. You can check the sales order that are *Ready* or *Not ready* from the sales order list page by filtering on this new status field.

-->

> [!NOTE]
> - Jei atnaujinsite pardavimo užsakymo eilutę po to, kai CTP planavimo optimizavimui apskaičiuotos patvirtintos datos, sistema išvalys datas iki kito atitinkamo dinaminio plano vykdymo.
> - Jei redaguojate susijusius parametrus, kurie gali paveikti esamas patvirtintas datas (pavyzdžiui, pakeisdami gamybos laiką, rezervavimus ar žymėjimus), turėtumėte išvalyti atitinkamų esamų užsakymų patvirtintas datas. Dėl šio veiksmo kiekvienos susijusios eilutės būsena bus pakeista į *Neparuošta*. Savo ruožtu dėl šio pakeitimo sistema perskaičiuos patvirtintas datas, kai kitą kartą galėsite naudoti dinaminį planą.

## <a name="change-existing-sales-orders-so-that-they-use-ctp"></a><a name="change-orders"></a> Keisti esamus pardavimo užsakymus, kad jie galėtų naudoti CTP

Bet kurio atviro **užsakymo pristatymo datos** valdymo vertę galite bet kada pakeisti. Jei reikia, vertę galite keisti antraštės lygyje ir(arba) kiekvienoje eilutėje.

### <a name="change-to-ctp-at-the-order-header-level"></a>Pakeisti į CTP užsakymo antraštės lygyje

<!-- KFM: Would be nice to mention how changing this setting on the header affects the individual lines. -->

Norėdami pakeisti užsakymą taip, kad jis naudoja CTP užsakymo antraštės lygmenyje, atlikite šiuos žingsnius.

1. Eikite į **Gautinos sumos \> Užsakymai \> Visi pardavimo užsakymai**.
1. Atidarykite pardavimo užsakymą, kurį norite nustatyti, arba sukurkite naują.
1. Pasirinkite **Antraštė**, jei norite atidaryti antraštės informaciją pardavimo **užsakymo informacijos** puslapyje.
1. Pristatymo "**FastTab**" nustatykite **vieną** iš šių pristatymo datos valdymo lauko verčių, atsižvelgdami į jūsų naudojate planavimo sistemą:

    - *CTP* – naudokite CTP skaičiavimą, kurį pateikė įtaisytasis bendrojo planavimo modulis. Jei naudojate planavimo optimizavimą, *CTP* pristatymo datos valdymo metodas neleidžiamas. Todėl jei pasirinksite šią vertę, bus klaida skaičiuojant.
    - *CTP planavimo optimizavimui* – naudokite CTP skaičiavimą, kuris pateikiamas planavimo optimizavimo. Šis parametras neturi jokios įtakos, jei naudojate įtaisytą bendrojo planavimo sistemą.

<!-- KFM: Additional dialogs are shown here. Review these with the PM and expand this procedure at next revision. -->
1. Pasirinkite **Gerai** keitimo pritaikymui.

### <a name="change-to-ctp-at-the-order-line-level"></a>Pakeisti į CTP užsakymo eilutės lygiu

Jei sukūrėte užsakymo eilutę naudodami kitą pristatymo datos valdymo metodą, bet kuriuo metu galite pakeisti į CTP. Keitimai, atlikti eilutės lygyje, neturi įtakos jokioms kitoms eilutėms. Tačiau dėl jų bendros užsakymo pristatymo datos gali būti perkeltos į priekį arba atgal, atsižvelgiant į tai, kaip pasikeičia kiekvienas atnaujintas eilutės skaičiavimas. <!-- KFM: Confirm this intro at next revision -->

Norėdami pakeisti užsakymą taip, kad jis naudojamas CTP įtaisytam bendrojo planavimo metu eilutės lygiu, atlikite šiuos veiksmus.

1. Eikite į **Gautinos sumos \> Užsakymai \> Visi pardavimo užsakymai**.
1. Atidarykite pardavimo užsakymą, kurį norite nustatyti, arba sukurkite naują.
1. Išsamios pardavimo **užsakymo informacijos** puslapio pardavimo užsakymo **eilutės** "FastTab" pasirinkite pardavimo užsakymo eilutę, kurią norite nustatyti.
1. Eilutės informacijos **"** FastTab", **skirtuke** Pristatymas, **nustatykite** lauką Pristatymo datos valdymas, viena iš šių verčių, atsižvelgiant į jūsų naudojate planavimo mašinų:

    - *CTP* – naudokite CTP skaičiavimą, kurį pateikė įtaisytasis bendrojo planavimo modulis. Jei naudojate planavimo optimizavimą, *CTP* pristatymo datos valdymo metodas neleidžiamas. Todėl jei pasirinksite šią vertę, bus klaida skaičiuojant.
    - *CTP planavimo optimizavimui* – naudokite CTP skaičiavimą, kuris pateikiamas planavimo optimizavimo. Šis parametras neturi jokios įtakos, jei naudojate įtaisytą bendrojo planavimo sistemą.

    Atsiranda **dialogo langas Galimos siuntimo ir** gavimo datos, rodomos galimos siuntimo ir gavimo datos. Šis dialogo langas veikia taip pat kaip užsakymo eilutėse, kaip aprašyta ankstesniame skyriuje.

1. Veiksmų srityje pasirinkite **Įrašyti**.
