---
title: Pagerinti ER sprendimų našumą, nes bus sumažintas vykdymo metu išrinktų lentelės laukų skaičius
description: Šioje temoje paaiškinama, kaip galite padėti pagerinti našumą, sumažinę lentelių laukų, išrinktų vykdymo metu, skaičių.
author: NickSelin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: dd192a7718ac4fd8bcb636ede6c005ca29ee5f08
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811833"
---
# <a name="improve-performance-of-er-solutions-by-reducing-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Pagerinti ER sprendimų našumą, nes bus sumažintas vykdymo metu išrinktų lentelės laukų skaičius

[!include[banner](../includes/banner.md)]

Galite kurti elektroninių [ataskaitų](general-electronic-reporting.md) (ER) [formatus,](er-overview-components.md#format-components-for-outgoing-electronic-documents) kurie generuoja siunčiamus dokumentus įvairiais formatais. Kai dokumentas sugeneruotas, ER formatas išk taigi duomenų šaltinius, kurie buvo sukonfigūruoti atitinkamame ER modelio [susiejime](er-overview-components.md#model-mapping-component). Norėdami konfigūruoti prieigą prie programų lentelių, užklausų arba įrašų gavimo objektų, galite naudoti lentelės įrašų tipo ER *duomenų šaltinius*. Pagal numatytuosius nustatymus lentelės įrašų *tipo* duomenų šaltinis nuskaito visų prašomų įrašų laukų vertes. Tačiau šį duomenų šaltinio tipą galite konfigūruoti, kad jis rastos tik tos lauko vertės, kurios reikalingos vykdomame ER formate. Ši konfigūracija padeda sumažinti programos serverio, kuris nuskaito duomenis ir toliau registruoja duomenų kaupimą talpykloje, atminties suvartojimą.

Norėdami daugiau sužinoti, kaip riboti lentelių *įrašų* tipo duomenų šaltinių išrinktų laukų sąrašą, užpildykite pavyzdį šioje temoje.

## <a name="example-reduce-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Pavyzdys: sumažinti lentelės laukų, kurie surenkami vykdymo metu, skaičių

Šios procedūros rodo, kaip vartotojas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenyje gali konfigūruoti ER modelio išdėstymą, kad išrinktų tik laukus, kurie reikalingi ER formatui paleisti, kad būtų sumažintas programos serverio atminties suvartojimas.

Šias procedūras galima atlikti JAV dolerių įmonėje **"** Microsoft Dynamics 365 Finance". Kodavimas nebūtinas.

Norėdami baigti šį pavyzdį turite turėti prieigą prie **JAVMF įmonės** vienam iš šių vaidmenų:

- Elektroninės ataskaitos funkcijų konsultantas
- Sistemos administratorius

Šiame pavyzdyje jūs naudosite ER [konfigūracijas](general-electronic-reporting.md#Configuration), kurios pateiktos Litware **, Inc.** pavyzdžio įmonei. Įsitikinkite, kad **Litware, Inc.** (`http://www.litware.com`) PAVYZDŽIO įmonės konfigūracijos teikėjas yra įtrauktas į ER sistemos sąrašą ir kad jis pažymėtas kaip **Aktyvus**. Jei šio konfigūracijos teikėjo nėra arba **jei** jis nepažymėtas kaip Aktyvus, [atlikite konfigūracijos teikėjo kūrimo veiksmus ir pažymėkite jį kaip aktyvų](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-the-er-framework"></a>ER sistemos konfigūracija

Atlikite veiksmus, aprašytus skyriuje [Konfigūruoti ER sistemą](er-quick-start2-customize-report.md#ConfigureFramework), kad nustatytumėte minimalų ER parametrų rinkinį. Prieš pradėdami naudoti ER sistemą, norėdami modifikuoti pateiktos ER sprendimo duomenų šaltinius, turite užbaigti šį nustatymą.

### <a name="import-the-sample-er-configurations"></a>Pavyzdinių ER konfigūracijų importavimas

Jei dar nebaigėte [pavyzdžio, naudodami naujo ER dizaino sprendimą, norėdami išspausdinti pasirinktinę ataskaitos temą, atsisiųskite ir vietoje saugokite toliau nurodytų ER](er-quick-start1-new-solution.md) sprendimo konfigūracijų XML failus.

| Turinio aprašas            | Failo vardas |
|--------------------------------|-----------|
| ER duomenų modelio konfigūracija    | [Klausimynų modelis.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) |
| ER modelio susiejimo konfigūracija | [Klausimynų susiejimas.versija.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) |
| ER formato konfigūracija        | [Klausimynų formatas.versija.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) |

Tada atlikite šiuos veiksmus, kad į savo finansų egzempliorių įkeltumėte pateiktą ER sprendimo konfigūraciją.

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Pasirinkite **Ataskaitų konfigūracijos**.
3. Konfigūracijos puslapyje **importuokite** ER duomenų modelio konfigūraciją.

    1. Pasirinkite **Keitimas** ir pasirinkite **Įkelti iš XML failo**.
    2. Pasirinkite **Naršyti**, rasti ir pasirinkti **failą Questionnaires model.version.1.xml**, tada pasirinkite **Gerai**.

4. Importuoti ER modelio susiejimo konfigūraciją.

    1. Pasirinkite **Keitimas** ir pasirinkite **Įkelti iš XML failo**.
    2. Pasirinkite **Naršyti**, rasti ir pasirinkti klausimynų **susiejimą.1.1.xml** failą, tada pasirinkite **Gerai**.

5. Importuoti ER formato konfigūraciją.

    1. Pasirinkite **Keitimas** ir pasirinkite **Įkelti iš XML failo**.
    2. Pasirinkite **Naršyti**, rasti ir pasirinkti klausimynų **formatą.1.1.xml** rinkmena, tada pasirinkite **Gerai**.

6. Konfigūracijos medyje išplėskite **klausimynų modelį**.
7. Peržiūrėkite importuotų ER konfigūracijų sąrašą konfigūracijos medyje.

    ![Konfigūracijų puslapyje peržiūrimas importuotų ER konfigūracijų sąrašas.](./media/er-reduce-fetched-fields-number-configurations.png)

### <a name="review-the-provided-er-model-mapping"></a>Peržiūrėti pateiktą ER modelio susiejimą

1. **Konfigūracijos puslapyje pasirinkti** klausimynų **susiejimą**.
2. Veiksmų srityje pasirinkite **Dizaino įrankis**.
3. Modelio ir **duomenų šaltinio susiejimo puslapyje pasirinkite** Konstruktorius **·**.
4. Modelio susiejimo **dizainerio puslapyje** veiksmų srityje pasirinkite Grupės rodinys, norėdami **įjungti** grupės **rodinį**.
5. Duomenų modelio **srityje išplėskite** **klausimyną**.

    Atkreipkite dėmesį **, kad** klausimyno duomenų šaltinis sukonfigūruotas pasiekti `KMCollection` programos lentelę.

6. Duomenų šaltinių srityje išplėskite Lentelės **įrašų** **klausimyno** \>**laukus**.\>**·**

    Atkreipkite dėmesį, kiek laukų `KMCollection` iš programos lentelės rodyti lentelės **įrašų** tipo Klausimyno *duomenų* šaltinis.

    ![Modelio susiejimo dizaino puslapio, kai įjungtas grupės rodinys, susiejimo modelio susiejimo puslapio peržiūra.](./media/er-reduce-fetched-fields-number-mapping1.png)

7. Norėdami išjungti grupės rodinį, veiksmų **srityje** vėl pasirinkite **Grupės** rodinys, tada pasirinkite **Rodyti viską** \> **, tik susieti**.

    Atkreipkite dėmesį, kad `KMCollection` ER duomenų modelyje **Klausimyno įrašų** sąrašui užpildyti naudojami keli programos lentelės laukai:

    - `Active`
    - `Description`
    - `questionMode`
    - `kmCollectionId`

    ![Modelio susiejimo konstruktoriaus puslapyje peržiūrimas pateiktas modelių susiejimas, kai grupės rodinys yra išjungtas.](./media/er-reduce-fetched-fields-number-mapping2.png)

### <a name="turn-on-the-er-performance-trace"></a>ER našumo sekimo įjungimas

Norėdami nustatyti ER vartotojo [parametrus, kurie įgalina sekti ER komponentų vykdymą, atlikite veiksmus, aprašytus dalyje Įjungti ER](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) našumo sekimą.

### <a name="run-the-provided-er-format-by-using-the-provided-model-mapping"></a>Naudoti pateiktą ER formatą naudojant pateiktą modelio susiejimą

Norėdami paleisti pateiktą [vieno klausimyno ER formatą iš konfigūracijos puslapio, vykdykite veiksmus, kuriuos vykdo ER](er-quick-start1-new-solution.md#RunFormatFromER)**sukurtas** formatas.

### <a name="review-the-execution-trace-of-the-first-run"></a>Peržiūrėti pirmojo vykdymo sekimą

1. Eikite į **Organizacijos administravimo** \> **elektronines \> ataskaitų konfigūracijas.**
2. Konfigūracijos puslapyje **išplėskite** klausimynų **modelį ir** pasirinkite Klausimynų **konvertavimas**.

    > [!NOTE]
    > Išsami "FastTab" **versijų** informacija rodo, kad pasirinkote klausimynų susiejimo konfigūracijos juodraščio **versiją**. Todėl galite modifikuoti šio modelio susiejimo turinį.

3. Veiksmų srityje pasirinkite **Dizaino įrankis**.
4. Modelio ir **duomenų šaltinio susiejimo puslapyje pasirinkite** Konstruktorius **·**.
5. Puslapio **Modelio susiejimo dizaino įrankis** veiksmų srityje pasirinkite **Našumo sekimas**.
6. Našumo sekimo **rezultatų parametrų dialogo** lange pasirinkite sekimą, kuris buvo sugeneruotas paskutinio formato vykdymo metu.

    ![Sekimo pasirinkimas dialogo lange Našumo sekimo rezultatų parametrai.](./media/er-reduce-fetched-fields-number-select-trace-1.png)

7. Pasirinkite **Gerai**. 
8. Informacijos FastTab **filtruoti** klausimyno **maršrutą**, kuris nurodo klausimyno **duomenų** šaltinį.
9. Peržiūrėkite išsamią duomenų bazės užklausos, sugeneruotos iškvietus klausimyno **duomenų** šaltinį, informaciją.

    Atkreipkite dėmesį, kad visi programos `KMCollection` lentelės laukai išrinkti apdorojimo metu, kai buvo iškviestas **klausimyno** duomenų šaltinis.

    ![Modelio susiejimo dizainerio puslapyje peržiūrima duomenų bazės užklausos informacija.](./media/er-reduce-fetched-fields-number-query1.png)

### <a name="modify-the-provided-er-model-mapping"></a>Modifikuoti pateiktą ER modelių susiejimą

1. Modelio susiejimo **dizaino įrankio** puslapio duomenų **šaltinių** srityje pasirinkite **klausimyno** duomenų šaltinį.
2. Duomenų šaltinių **srityje** pasirinkite **Redaguoti**.
3. **Duomenų šaltinio ypatybės dialogo** lange pasirinkite Pasirinkti laukus, **·**`KMCollection`**kad** nurodydami nurodomos programos lentelės, kuri bus išrinkta apdorojimo metu iškviedžius redaguojamą klausimyno duomenų šaltinį, laukų sąrašą.

    ![Pasirinkus laukus duomenų šaltinio ypatybės dialogo lange pradedama konfigūruoti laukų, kurie bus surastos iš programos lentelės naudojant redaguojamą duomenų šaltinį, sąrašą.](./media/er-reduce-fetched-fields-number-select-fields1.png)

4. Puslapyje Pasirinkti **laukus pasirinkite Automatinis** pripildimas **·**.

    Pasirinktų **laukų** sąrašas užpildomas automatiškai, remiantis iš anksto sukonfigūruotais modelio susiejimo artefaktais. Į sąrašą įtraukiami visi nurodytų lentelių laukai ir ryšiai, paminėti bet kuriame modelio susiejimo, formulės ar duomenų šaltinyje.

    ![Konfigūruojamas laukų, kurie bus surastos iš programos lentelės puslapyje Pasirinkti laukus, sąrašas.](./media/er-reduce-fetched-fields-number-select-fields2.png)

5. Pasirinkite **Įrašyti** ir uždarykite puslapį **Pasirinkti** laukus.
6. Pasirinkite **Gerai**, kad būtų išsaugoti atlikti duomenų šaltinio parametrų keitimai.
7. Veiksmų srityje pasirinkite Rodyti **viską**.

    Atkreipkite dėmesį **, kad** klausimyno duomenų šaltinyje dabar rodomas tekstas **\<Fields are filtered\>**. Šis tekstas nurodo, kad duomenų šaltinis sukonfigūruotas surasti ribotą laukų skaičių iš nurodytos programos lentelės.

    ![Atnaujinto modelio susiejimo peržiūra modelio susiejimo dizaino įrankio puslapyje.](./media/er-reduce-fetched-fields-number-mapping3.png)

8. Pasirinkite **Įrašyti**, kad būtų išsaugoti redaguojamo modelio susiejimo pakeitimai.

    > [!NOTE]
    > Vykdymo metu ER analizuoja pridėtus ryšius ir prideda visus laukus, kurie naudojami duomenų bazės užklausoje, net jei šie laukai nebuvo konkrečiai įtraukti į išrinktų laukų sąrašą dizaino metu.

### <a name="run-the-provided-er-format-by-using-the-updated-model-mapping"></a>Naudoti pateiktą ER formatą naudojant atnaujintą modelio susiejimą

Norėdami paleisti pateiktą [vieno klausimyno ER formatą iš konfigūracijos puslapio, vykdykite veiksmus, kuriuos vykdo ER](er-quick-start1-new-solution.md#RunFormatFromER)**sukurtas** formatas.

### <a name="review-the-execution-trace-of-the-second-run"></a>Peržiūrėti antrojo vykdymo sekimą

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Konfigūracijos puslapyje **išplėskite** klausimynų **modelį ir** pasirinkite Klausimynų **konvertavimas**.
3. Veiksmų srityje pasirinkite **Dizaino įrankis**.
4. Modelio ir **duomenų šaltinio susiejimo puslapyje pasirinkite** Konstruktorius **·**.
5. Puslapio **Modelio susiejimo dizaino įrankis** veiksmų srityje pasirinkite **Našumo sekimas**.
6. Našumo sekimo **rezultatų parametrų dialogo** lange pasirinkite sekimą, kuris buvo sugeneruotas paskutinio formato vykdymo metu.
7. Pasirinkite **Gerai**.
8. Informacijos FastTab **filtruoti** klausimyno **maršrutą**, kuris nurodo klausimyno **duomenų** šaltinį.
9. Peržiūrėkite išsamią duomenų bazės užklausos, sugeneruotos iškvietus klausimyno **duomenų** šaltinį, informaciją.

    Atkreipkite dėmesį, kad tik `KMCollection`**laukai**, kurie būtini norint užpildyti duomenų šaltinį, buvo išrinkti apdorojimo metu iš programos lentelės, kai buvo iškviestas klausimyno duomenų šaltinis.

    > [!NOTE]
    > Kai kurie laukai, pvz., skaidinio ID laukai, duomenų srities ID ir įrašo ID, automatiškai įtraukiami į finansų programos duomenų valdymo sistemą.

    ![Peržiūrima atnaujinto modelio susiejimo duomenų bazės užklausos informacija modelio susiejimo dizaino įrankio puslapyje.](./media/er-reduce-fetched-fields-number-query2.png)

Šią techniką galite naudoti norėdami sumažinti išrinktų įrašų skaičių, kai turite sumažinti atminties suvartojimą paleisdami ER modelio susiejimą ir ER formatą.

## <a name="limitations"></a>Apribojimai

*Kai* apribosite duomenų šaltinio, kurio tipas Lentelės įrašai, išrinktų laukų skaičių, negalite naudoti programos lentelės, kurią nurodo duomenų šaltinis, metodų, nes programos metaduomenys pateikia informacijos apie lentelės laukus, kurių reikia norint iškviesti šiuos metodus.

## <a name="usage-notes"></a>Naudojimo pastabos

Nors automatinio **pripildymo** komanda automatiškai įtraukia laukus, ji automatiškai panaikina anksčiau pridėtus laukus, net jei jie nebenaudojami redaguojamo modelio susiejimo susiejimuose, formulėse ir duomenų šaltiniuose.

Kai pasirenkate Automatinį **pripildą**, ER analizuoja susiejimus, formules ir duomenų šaltinius, kuriuos redaguojamas modelio susiejimas buvo jums atidarius redaguoti. Jei keičiate redaguojamo modelio susiejimo susiejimus, formules ir duomenų šaltinius ir **norite** naudoti komandą Automatiškai papildyti, uždarykite modelio susiejimo konstruktorių ir iš naujo jį atidarykite, kad galėtumėte redaguoti savo modelio išdėstymą. 

## <a name="additional-resources"></a>Papildomi ištekliai

- [ER formatų vykdymo sekimas siekiant diagnozuoti našumo problemas](trace-execution-er-troubleshoot-perf.md)
- [ER konfigūracijų našumo trikčių šalinimas](er-troubleshoot-perf-issues-in-configurations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
