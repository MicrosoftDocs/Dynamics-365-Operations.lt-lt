---
title: Perskaičiuoti eilutės grynąsias sumas importuojant pardavimo užsakymus, pasiūlymus ir grąžinimus
description: Šiame straipsnyje aprašoma, ar ir kaip sistema perskaičiuoti grynąsias eilutės sumas, kai importuojami pardavimo užsakymai, pasiūlymai ir grąžinimai. Taip pat paaiškinama, kaip valdyti elgseną skirtingose "Microsoft" versijose Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 08/05/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2022-06-08
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 08b30044a93e46c9c83848b60d69c595bc774570
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335562"
---
# <a name="recalculate-line-net-amounts-when-importing-sales-orders-quotations-and-returns"></a>Perskaičiuoti eilutės grynąsias sumas importuojant pardavimo užsakymus, pasiūlymus ir grąžinimus

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, ar ir kaip sistema perskaičiuoti grynąsias eilutės sumas, kai importuojami pardavimo užsakymai, pasiūlymai ir grąžinimai. Taip pat paaiškinama, kaip valdyti elgseną skirtingose "Microsoft" versijose Dynamics 365 Supply Chain Management.

## <a name="how-updates-to-net-line-amounts-are-calculated-on-import"></a>Kaip skaičiuojami grynosios eilutės sumos naujinimai importuojant

Tiekimo grandinės valdymo 10.0.23 versijoje įvestas [604418](https://fix.lcs.dynamics.com/issue/results/?q=604418). Šis klaidosfiksas **pakeitė** sąlygas, pagal kurias eilutėje esantį grynosios sumos lauką galima atnaujinti arba perskaičiuoti, kai importuojami esamų pardavimo užsakymų, grąžinimų ir pasiūlymų atnaujinimai. Versijoje 10.0.29 šį *klaidosfiksą galite pakeisti importavimo priemonėje įjungę funkciją Skaičiuoti eilutės grynąją* sumą. Ši funkcija turi panašų poveikį, tačiau ji suteikia visuotinį parametrą, leidžiaį grįžti prie seno veikimo būdo, jei to reikia. Nors dėl naujos veikimo būdo sistema veikia daugiau, dėl to sistema gali pasiekti netikėtus rezultatus tam tikroje scenarijuose, kuriuose tenkinamos visos šios sąlygos:

- *Duomenys, kurie atnaujina esamus įrašus, importuojami naudojant pardavimo užsakymo eilutes V2*, *pardavimo pasiūlymo eilutes V2* *arba* grąžinimo užsakymo eilučių objektą naudojant Open Data Protocol (OData), įskaitant situacijas, kuriose naudojate dvigubo rašymo, importavimo / eksportavimo naudojant Excel ir kai kurias trečiosios šalies integracijas.
- [Prekybos sutarčių vertinimo strategijos](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper)**·**, kurios yra, sudaro keitimo strategiją, kuri riboja pardavimo užsakymo eilučių, pardavimo pasiūlymo eilučių ir (arba) grąžinimo užsakymo eilučių grynosios sumos lauko naujinimus.
- Importuoti duomenys **apima** eilučių lauko Grynoji **suma pakeitimus arba pakeitimus (pvz., vieneto kainą, kiekį ar nuolaidą),** dėl kurių eilučių grynosios sumos lauko vertė bus perskaičiuota vienam ar daugiau esamų eilutės įrašų.

Šiais konkrečiais scenarijais prekybos sutarties **vertinimo strategijos poveikis eilutėje apriboja grynosios sumos lauko** atnaujinimus. Šis apribojimas vadinamas pakeitimo *strategija*. Dėl šios strategijos, kai laukui redaguoti ar perskaičiuoti naudojate vartotojo sąsają, sistema paragina patvirtinti, ar norite atlikti keitimą. Tačiau kai importuojate įrašą, sistema turi pasirinkti. Prieš versijoje 10.0.23 sistema visada nepakeistų eilutės grynosios sumos, nebent gaunama eilutės grynoji suma yra 0 (nulis). Tačiau naujesnėse versijose sistema pagal poreikį visada atnaujina arba perskaičiuoja grynąją sumą, nebent nurodyta kitaip. Nors naujas veikimas yra loginis, gali kilti problemų, jei jau apdorojate procesus ar integravimą, kuris laiko senesnį veikimo būdą. Šiame straipsnyje aprašoma, kaip, jei reikia, grįžti prie seno veikimo būdo.

## <a name="control-calculations-of-line-net-amounts-in-versions-10029-and-later"></a>Valdyti eilutės grynųjų sumų skaičiavimus 10.0.29 ir vėlesnėse versijose

Tiekimo grandinės valdymo 10.0.29 versijoje įdiegta priemonė, kuri importavimo *metu vadinama Skaičiuoti eilutės grynąją sumą*. Ši funkcija įtraukia pasirinktį, kuri į puslapį Gautinų **sumų parametrai įtraukia pasirinktį** **Skaičiuoti eilutės grynąją** sumą. Ši pasirinktis leidžia pasirinkti naują arba senstelėjusį veikimo būdą, kad būtų galima apskaičiuoti grynąsias eilutės sumas importuojant.

### <a name="turn-the-calculate-line-net-amount-on-import-feature-on-or-off"></a>Įjungti arba išjungti importavimo priemonę Skaičiuoti eilutės grynąją sumą

Atnaujinus į versiją 10.0.29, *importavimo funkcijos funkcija Skaičiuoti eilutės grynąją sumą įjungta pagal numatytuosius nustatymus ir* **nauja parinktis Skaičiuoti eilutės grynąją sumą iš pradžių nustatyta kaip** Taip *.* Parametras *Taip* atitinka naują standartinį veikimą. Ji atitinka sistemos veikimą, kai priemonė išjungta, [išskyrus parametro CalculateLineAmount](#CalculateLineAmount) funkcijos atveju, kaip toliau aprašyta šiame straipsnyje. *Parametras* Joks parametras atitinka sistemos veikimą prieš versijai 10.0.23 ir pateiktas daugiausia senesnių integravimo scenarijų palaikyti.

Administratoriai gali įjungti arba *išjungti importavimo funkcijos funkciją* Skaičiuoti eilutės grynąją sumą naudodami funkcijų [valdymo darbo sritį](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="set-the-calculate-line-net-amount-option"></a>Nustatyti parinktį Skaičiuoti eilutės grynąją sumą

Kai importavimo *priemonėje įjungta parinktis* Skaičiuoti eilutės grynąją sumą, **galite nustatyti pasirinktį Skaičiuoti eilutės grynąją** sumą, atliekant šiuos veiksmus.

1. Eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.
1. Skirtuke **Kainos** eilutės **grynosios** sumos skaičiavime naudodami integravimo "FastTab **" nustatykite pasirinktį Skaičiuoti eilutės grynąją** sumą kaip vieną iš šių verčių:

    - *Taip* – sistema visada perskaičiuos ir atnaujins eilučių sumas, kai jų prireiks. (Todėl ji nepaisys prekybos sutarties vertinimo strategijos.)
    - *Ne* – jei esama ar gaunama grynoji bet kurios eilutės suma yra 0 (nulis), tos eilutės vertė perskaičiuojama remiantis kitomis vertėmis (pvz., vieneto kaina, kiekis ir nuolaida). Jei esama arba gaunama grynoji suma skiriasi nuo 0 (nulio) **ir eilutėje lauke Grynoji** suma nustatoma pakeitimo strategija, laukas nėra perskaičiuojamas ar atnaujinamas, net jei įeinantys eilutės kainos, kiekio ir (arba) nuolaidos pakeitimai gali teiti, kad eilutės suma turi būti perskaičiuota. Šis veikimo būdas atitinka versijos 10.0.22 elgseną.

### <a name="how-the-calculate-line-net-amount-on-import-feature-affects-the-calculatelineamount-parameter"></a><a name="CalculateLineAmount"></a> Kaip importavimo priemonės skaičiavimo eilutės grynoji suma veikia parametrą CalculateLineAmount

Kai importavimo *priemonėje įjungta skaičiavimo* eilutės grynoji suma, `CalculateLineAmount` parametro vertė `SalesLine` ir lentelės `SalesQuotationLine` neturi jokios įtakos. Todėl veikimo būdą visuotinai kontroliuoja parinktis **Skaičiuoti eilutės grynąją** sumą, aprašyta ankstesniame skyriuje. Todėl, kai priemonė įjungta, jūs negalite imtis jokios vertės priklausomybės `CalculateLineAmount`.

*Kai* importavimo priemonėje apskaičiuoti eilutės grynąją sumą yra išjungta, `CalculateLineAmount``SalesLine``SalesQuotationLine` lentelių parametras veikia taip, kaip tai daro tiekimo grandinės valdymo versijos nuo 10.0,23 iki 10,0,28, kaip aprašyta kitame skyriuje.

## <a name="control-line-net-amount-calculations-in-versions-10028-and-earlier"></a>Kontroliuoja eilutės grynosios sumos skaičiavimus 10.0.28 ir ankstesnėse versijose

[Kai 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418) 10.0.23 versija, atsiranda galimybė pasirinkti, kaip kiekvienas atitinkamas duomenų objektas turėtų užims, kai eilutės grynoji suma bus redaguojama ar turėjo būti perskaičiuota dėl kitų pakeitimų (pvz., atnaujintos prekės kainos). Taip valdyti galite nustatydami naują kiekvienos eilutės `CalculateLineAmount` parametrą kaip vieną iš šių importuoto failo verčių:

- **`CalculateLineAmount` = *1*** – **grynosios** sumos laukas eilutėje visada perskaičiuojamas ir atnaujinamas, nepaisant to, ar nustatyta lauko keitimo strategija ir neatsižvelgiant į gaunamos arba esamos eilutės grynosios sumos vertę.
- **`CalculateLineAmount` = *0*** – jei esama ar gaunama grynoji bet kurios eilutės suma yra 0 (nulis), tos eilutės vertė perskaičiuojama remiantis kitomis vertėmis (pvz., vieneto kaina, kiekis ir nuolaida). Jei esama arba gaunama grynoji suma skiriasi nuo 0 (nulio) **ir eilutėje nustatyta pakeitimo strategija lauke Grynoji** suma, laukas nėra perskaičiuojamas ar atnaujinamas.  

Sistemos veikimo būdas priklauso nuo jūsų tiekimo grandinės valdymo versijos:

- Versijoje 10.0.22 `CalculateLineAmount`*ir ankstesnėse versijose sistema visada veikia taip, kaip nurodyta 0* ir `CalculateLineAmount`*nėra būdo, kaip naudojant šią versiją nustatytas 1*.
- Versijose nuo 10.0.23 iki 10.0.28 `CalculateLineAmount`*sistemos meniu nurodoma kaip 1* *, kai visos eilutės importavimo faile nėra konkrečiai nustatytos kaip 0*.
