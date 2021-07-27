---
title: Indijos mokesčių, atskaitonų šaltinyje (TDS), peržiūra
description: Šioje temoje pateikiama išsami informacija apie Indijos mokestis, išskaičiuotas šaltinyje (TDS). TDS dokumentacijoje yra šios galimybės funkcijos.
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 8064f10978712fc474dd72a5b5bdd9a445606d7a
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/03/2021
ms.locfileid: "6337726"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a>Indijos mokesčių, atskaitonų šaltinyje (TDS), peržiūra

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama išsami informacija apie Indijos mokestis, išskaičiuotas šaltinyje (TDS).

TDS dokumentacijoje yra šios galimybės funkcijos. Taip pat paaiškinama, kaip atlikti pagrindinį TDS nustatymą, skaičiuoti TDS operacijas, užbaigti TDS sudengimo procesą, įrašyti TDS sertifikatų numerius ir generuoti TDS užklausas, TDS išrašus ir TDS sertifikatus. Dokumente yra šios temos:

- [Pagrindinis nustatymas TDS](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [Formulės konstruktoriaus ir ribinės ribos funkcija, naudojama TDS skaičiuoti](apac-ind-TDS-Formula-designer.md)
- [SF, mokėjimų, paprastųjų vekselių ir vidinės įmonės operacijų TDS skaičiavimas](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [Periodinio TDS sudengimo procesas ir TDS sumų sudengimas TDS valdžios institucijos tiekėjams](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [TDS sertifikatų numerių ir datų įrašymas ir atnaujinimas](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a>Įvadas į TDS

Pagal 1961 m. Pajamų mokestį paslaugos gavėjas atskaičiuoja pajamų mokestį išankstinio mokėjimo arba kredito apskaitos metu, t. y. tas, kuris įvyksta anksčiau. Asmuo, kuris atlieka mokėjimą, turi atskaityti mokesčio sumą ir sumokėti tik grynąjį balansą paslaugos teikėjui. TDS taikomas paslaugoms, kurias nurodo vyriausybė, ir mokestis atskaitomas naudojant tarifus, kuriuos nurodo vyriausybė laikotarpiui. Atskaitymo tarifas priklauso nuo objekto, kuris gauna mokėjimą arba teikia paslaugą, būsenos. Būsenos apima **Atskirą**, **Hindu neatskirtą šeimą** (**HUF**), **Bendrovę**, **Firmą**, **Asmenų asociacijas** (**AOP**), **Asmenų subjektą** (**BOI**) ir **Vietos įstaigą**.

Šiose sekcijose pateikiamas paslaugų, kurios taikomos TDS, sąrašas, kaip nurodyta Indijos Vyriausybės.

**Gyventojų**

- Pajamos iš atlyginimų (192 skyriuje)
- Pajamos iš palūkanų už vertybiniais popierius (193 skyrius)
- Pajamos iš dividendų (194 skyriuje)
- Pajamos iš palūkanų (194A skyriuje)
- Pajamos iš loterių arba anfiltrų (194B skyriuje)
- Laimėjimai iš mėn. ir t. t. (Skyriuje 194BB)
- Rangovai ir subrangovai (194C sekcijoje)
- Draudimo komisiniai (194D skyriuje)
- Pajamos iš įmokų pagal šalies įrašymo schemą (194EE skyriuje)
- Pajamos iš socialinio fondo arba UI (194F skyriuje)
- Komisiniai, skirtuko, prizo ir pan., pardavimo ar kt. (194G skyriuje)
- Komisinių arba brokerio tarpininkavimo mokėjimas (pagal 194 H skyrių)
- Nuoma (194I skyrius)
- Profesinė paslauga (pagal 194J skyrių)
- Pajamos iš vienetų (194K skyriuje)
- Tam tikros nuosavybės įsigijimo kompensacijos mokėjimas (194LA skyriuje)

**Ne gyventojų**

- Mokėjimai nenuo gyventojo sporto šakų asociacijai (194E skyriuje)
- Kitos sumos (195 skyriuje)
- Pajamos, atsižvelgiant į ne nuolatiniams vienetus (196A skyriuje)

    - Pajamos iš Indijos įmonės užsienio valiutos obligacijų ar akcijų (196C skyriuje)
    - Užsienio investuotojo pajamos iš apsaugos (196D skyriuje)
    - Atlyginimas ir visos kitos teigiamos pajamos iš bet kurio darbuotojo pajamoms (192 skyrius)
    - Vertybiniai popieriai (193 skyrius)
    - Palūkanos, kurios nėra palūkanos už vertybiniais popieriais (194A skyrius)
    - Mokėjimai rangovams ir subrangovams (194C skyrius)
    - Laimėjimai iš Yra arba kryžminių kodų (194B skyrius)
    - Laimėjimai iš žirgų lenktynių (194BB skyrius)
    - Draudimo komisiniai, padengiantys visus mokėjimus draudimo verslui įsigyti (194D skyrius)
    - Bet kokios palūkanos, kurios nėra palūkanos už vertybiniai popieriaii, mokėtini nenuodentiniams gyventojams, nėra įmonė ar užsienio įmonė (195 skyrius)
    - Mokėjimas nerezidentams sporto šakoms, įskaitant sporto asociacijas ar institucijas. Jei nenuo gyventojas yra sporto šakininkas, reikia atlikti mokėjimus už skelbimus ir straipsnius bet kurioje Indijoje laikraščiuose, žurnaluose ir t. t. įtrauktas į (194E skyrius)
    - Mokėjimas pagal NSS \[nacionalinių taupomųjų lėšų schemą\] (194EE skyrius)
    - Vienetų perpirkti pagal abipusius fondus arba UTI mokėjimas (194F skyrius)
    - Komisinių arba brokerio tarpininkavimo mokėjimas (pagal 194 H skyrių)
    - Nuomos mokėjimas (194I skyrius)
    - Mokesčių už profesines ar technines paslaugas mokėjimas (194J skyrius)
    - „Stockiest", platintojų, pirkėjų ir lėktuvų transporto transporto, įskaitant lėktuvo" (194G skyrius), komisiniai, įsakomasis ar prizas už šiuos bilietus
    - Pajamos iš vienetų, nupirktų užsienio valiuta, arba ilgalaikio kapitalo pelnas iš tokio vienetų, nupirktų užsienio valiuta, perkėlimo (196B skyrius)
    - Bet kokių pajamų mokėjimas ne nuolatiniams gyventojams palūkanų ar dividendų už obligacijas ir akcijas (196C skyrius)

TDS yra skaičiuojama pagal pirkimą, pardavimą, pardavimo grąžinimą, kredito pažymas, ilgalaikio turto įsigijimus, išankstinius apmokėjimus, išankstinius mokėjimus, paprastus vekselius, darbų mokesčius ir vidinės įmonės operacijas.

> [!NOTE]
> Dabartiniame Indijos mokesčių scenarijuje TDS nėra skaičiuojamas pagal pardavimo operacijas. Tačiau sistema apima atidėjimus, pagal kurias apskaičiuojamas pardavimo, ypač vidinės įmonės operacijų, susigrąžinamas TDS.

Skaičiuojant TDS visada atsižvelgiama į ribinę vertę ir išimties ribinę vertę, kuri nustatyta TDS komponentui.

Turi būti paleistas periodinis TDS sudengimo procesas ir TDS mokėjimai turi būti sudengti TDS institucijų tiekėjams.

Iš tiekėjų ar klientų gautų TDS sertifikatų numerius ir datas galima įrašyti ir atnaujinti. Be to, 26Q formas ir 27Q ketvirčio išrašus bei TDS 16A sertifikatą galima generuoti finansuose.

## <a name="setting-up-and-working-with-tds"></a>Nustatymas ir darbas su TDS

Toliau pateikiama nustatymo ir darbo su TDS proceso apžvalga:

1. **TDS nustatyumai:**

    - Parametrų nustatymas:

        - DK parametruose suaktyvinkite su TDS susijusius parametrus.
        - DK parametruose nustatykite išskaitomų mokesčių mokėjimų numeraciją.
        - Parametrų mokėtinos sąskaitose ir gautinose sąskaitose nustatymas.

    - Pagrindinė sąranka:

        - Nustatykite įmonės, klientų ir tiekėjų TDS registracijos numerius.
        - Nustatyti TDS elemento grupes.
        - Nustatykite TDS komponentus, pridėkite TDS komponentų grupes ir nustatykite jų ribinę vertę ir išimties ribą.
        - Nustatyti TDS institucijas.
        - TDS sudengimo laikotarpių nustatymas.
        - Nustatykite TDS mokesčių kodus ir pridėkite prie jų TDS komponentus.
        - Nustatykite TDS grupes ir pridėkite prie jų TDS mokesčių kodus.
        - Formulės konstruktoriuje nurodykite formulę, pagal kurią skaičiuojamas TDS grupės TDS.
        - Įrašykite TDS koncesijos sertifikato numerius.

    - DK sąskaitos ir įmonės nustatymas:

        - Nustatykite TDS mokėtinas ir gautinas DK sąskaitas.
        - Nustatykite įmonės mokesčių atskaitymo ir rinkinio sąskaitos numerį (TAN) ir atskaitymo tipo kategoriją.

    - Kitas nustatymas:

        - Nustatyti mokėjimo grafiką, kuriame yra TDS paskirstymas.
        - Nustatykite mokėjimo mokesčių tipą mokėjimams TDS institucijai.
        - Nustatyti informaciją apie TDS grupes, nuolatinius sąskaitų numerius (PAN) ir TN tiekėjams ir klientams.

2. **TDS skaičiavimas operacijose:**

    - SF ir mokėjimai
    - Paprastieji vekseliai
    - Išankstinis mokėjimas
    - Išankstiniai mokėjimai

3. **TDS atsiskaitymas**

    - Periodinio TDS sudengimo procesas
    - TDS mokėjimų TDS valdžios tiekėjams sudengimas ir TDS išdavimo generavimas

4. **TDS užklausos, išrašai ir sertifikatas:**

    - TDS sertifikato numerių ir datų įrašas ir naujinimas.
    - Generuoti TDS užklausą ir užregistruotą TDS užklausą.
    - Generuoti 27A formą, 26Q formą ir 27Q TDS formą ir ketvirčio el.TDS išrašus.
    - Kurti 16A TDS sertifikato formą.
