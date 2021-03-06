---
title: Pradinio kliento mokėjimo prognozavimo modelio įvertinimas (peržiūros versija)
description: Šioje temoje aprašomi veiksmai, kuriuos galite atlikti, kad suprastumėte kliento mokėjimo prognozavimo modelį ir įvertintumėte jo efektyvumą.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 014684595c7cd65383dc12d9eec2dd8ea7b8c20f
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186743"
---
# <a name="evaluate-the-initial-customer-payment-prediction-model-preview"></a>Pradinio kliento mokėjimo prognozavimo modelio įvertinimas (peržiūros versija)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje paaiškinama, kaip įvertinti prognozavimo modelį po to, kai įjungiate „Finance Insights”, o tada sugeneruojate ir apmokote savo pirmąjį modelį. Šioje temoje nagrinėjami kliento mokėjimo prognozavimo modeliai. Joje temoje aprašomi veiksmai, kuriuos galite atlikti, kad suprastumėte kliento mokėjimo prognozavimo modelį ir įvertintumėte jo efektyvumą.

## <a name="getting-details-about-the-model"></a>Informacijos apie modelį gavimas

„Microsoft Dynamics 365 Finance“ puslapyje **„Finance Insights” parametrai** prie tikslumo rezultato atsiranda saitas **Tikslinti modelį**.

[![Saitas Tikslinti modelį](./media/prediction-model.png)](./media/prediction-model.png)

Šis saitas perkelia į „AI Builder“, kuriame galite daugiau sužinoti apie dabartinį modelį ir taip pat jį patobulinti. Toliau pateiktame paveikslėlyje parodytas atidarytas puslapis.

[![AI Builder](./media/what-to-predict.png)](./media/what-to-predict.png)

Atidarytame puslapyje rodoma tolesnė informacija.

- Skiltyje **Našumas** modelio našumo įvertinimas nurodo modelio kokybę. Daugiau informacijos apie šį įvertinimą žr. [Prognozavimo modelio našumas](/ai-builder/prediction-performance) „AI Builder“ dokumentacijoje.
- Skiltyje **Svarbiausi duomenys** nurodoma, kiek svarbūs skirtingi modelio duomenų įvesties tipai. Galite įvertinti šį sąrašą ir atitinkamus procentus, norėdami nustatyti, ar informacija atitinka tai, ką žinote apie savo verslą ir rinką.

    [![Prognozavimo modelio duomenų skiltys Našumas ir Svarbiausi duomenys](./media/models.png)](./media/models.png)

- Skiltyje **Našumas** pasirinkite **Peržiūrėti išsamią informaciją**, norėdami sužinoti daugiau apie įvertinimą ir kitus aspektus. Toliau pateiktoje iliustracijoje pateikiama išsami informacija, kuri rodo, kad modelis naudoja mažiau informacijos, nei rekomenduotina. Todėl sistema sugeneravo įspėjamąjį pranešimą.

    [![Įspėjimai dėl modelio našumą](./media/details.png)](./media/details.png)

## <a name="digging-deeper"></a>Išsamesnė informacija

Nors tikslumas yra geras modelio vertinimo atspirties taškas, o našumo įvertinimas suteikia perspektyvą, „AI Builder“ suteikia išsamesnę metriką, kurią galite naudoti vertindami. Norėdami atsisiųsti išsamią informaciją, skiltyje **Našumas** pasirinkite elipsės mygtuką (**...**), esantį greta mygtuko **Naudoti modelį**, tada pasirinkite **Atsisiųsti išsamią metriką**.

[![Komanda Atsisiųsti išsamią metriką](./media/performance.png)](./media/performance.png)

Toliau pateiktame paveikslėlyje parodytas formatas, kuriuo galite atsisiųsti duomenis.

[![Atsisiunčiamų duomenų formatas](./media/data-format.png)](./media/data-format.png)

Norint giliau išanalizuoti rezultatus, geriausia pradėti peržiūrint metriką „Painiavos matrica“. Pavyzdžiui, čia pateikti duomenys, kurie rodomi šioje metrikoje ankstesnėje iliustracijoje.

`{"name": "Confusion Matrix", "value": {"schema_type": "confusion_matrix", "schema_version": "1.0.0", "data": {"class_labels": ["0", "1", "2"], "matrix": [[71, 9, 21], [5, 0, 27], [2, 0, 45]]}}, "type": "dictionaryNumericalList", "isGlobalScore": false}`

Šiuos duomenis galite išplėsti, kaip nurodyta toliau.

| &nbsp;                   | Prognozuojama laiku | Prognozuojamas vėlavimas | Prognozuojamas žymus vėlavimas |
|--------------------------|-------------------|----------------|---------------------|
| Faktinis mokėjimas laiku   | **71**            | 0              | 21                  |
| Faktinis vėluojantis mokėjimas      | 5                 | **0**          | 27                  |
| Faktinis žymiai vėluojantis mokėjimas | 2                 | 0              | **45**              |

Painiavos matrica parodo atsitiktinai pasirinkto tikrinimo duomenų rinkinio rezultatus iš mokymo proceso. Kadangi šios uždarytos SF nebuvo naudojamos modeliui apmokyti, jos yra geri modelio tikrinimo atvejai. Be to, kadangi faktinė SF būsena yra žinoma, modelio našumas taip pat gali būti matomas.

Pirmiausia raskite dažniausią faktinę vertę. Nors ši vertė gali būti visiškai suderinta su bendruoju duomenų rinkiniu, tai pagrįstas apytikslis skaičius. Šiuo atveju **Faktinis mokėjimas laiku** taikomas 92 iš 171 SF ir yra dažniausiai pasitaikanti faktinė vertė. Todėl šis modelis yra geras. Jei ką tik atspėjote, kad visos SF bus laiku, būtumėte teisūs 92 iš 171 karto (t. y. 54 procentai).

Svarbu, kad suprastumėte, kaip jūsų duomenų rinkinys yra subalansuotas. Šiuo atveju 92 iš 171 SF buvo apmokėtos laiku, 32 apmokėtos pavėluotai, o 47 – labai pavėluotai. Šios vertės rodo pagrįstai subalansuotą duomenų rinkinį, nes kiekvienoje klasifikacijoje yra svarbių rezultatų. Jei vienoje iš padėčių yra vos keli rezultatai, tai mašininio mokymo modeliui gali būti sudėtinga.

Modelio tikslumas nurodo tikslių tikrinimo duomenų rinkinio prognozių skaičių. Šios tikslios prognozės yra vertės, kurios ankstesniame pavyzdyje rodomos paryškintuoju šriftu. Šiuo atveju vertės nurodo apskaičiuotą 67,8 procento tikslumą (= \[71 + 0 + 45\] ÷ 171) apskaičiuotą tikslumą. Ši vertė yra 14 procentų pagerėjimas virš bazinio 54 procentų spėjimo ir tai yra modelio kokybės rodiklis.

Jei atidžiau pažvelgsite į painiavos matricą, pastebėsite, kad modelis gerai nuspėja laiku atliekamus ir vėluojančius SF mokėjimus. Tačiau jis suklydo dėl visų 32 SF, kurios buvo faktiškai apmokėtos vėliau (bet ne žymiai vėliau). Šis rezultatas rodo, kad reikia papildomai modelį tikrinti ir tobulinti.

Skaičius, nurodantis modelio našumą geriau nei tikslumas, yra F1 makro rezultatas. Šis rezultatas įvertina kiekvienos klasifikacijos būsenos rezultatus (laiku, pavėluotai ir žymiai pavėluotai). Pavyzdžiui, čia pateikti duomenys, kurie rodomi F1 makro metrikoje ankstesnėje iliustracijoje.

`{"name": "F1 Macro", "value": 0.4927170868347339, "type": "percentage", "isGlobalScore": false}`

Šiuo atveju F1 makro rezultatas (maždaug 49,3 procento) nurodo, kad modelis nepateikia veiksmingų prognozių kiekvienoje būsenoje, nepaisant bendro tikslumo rezultato, kuris atrodo pakankamai aukštas.

## <a name="improving-the-model"></a>Modelio tobulinimas

Geriau supratę savo pirmo modelio rezultatus, galbūt norėsite patobulinti modelį įtraukdami arba pašalindami funkcijų stulpelius arba filtruodami bet kurias duomenų rinkinio dalis, kurios nepalaiko tikslių prognozių. Uždarykite „AI Builder“, tada naudokite saitą **Tobulinti modelį** programoje „Dynamics 365 Finance“, kad iš naujo paleistumėte „AI Builder“ procesą. Galite eksperimentuoti su skirtingomis charakteristikomis, nedarydami įtakos publikuotame modelyje. Publikuotame modelyje poveikis daromas tik pasirinkus **Publikuoti**. Atminkite, kad jūsų „Dynamics 365 Finance“ egzemplioriuje naudojamas vienas modelis. Todėl prieš publikuodami turite kruopščiai patikrinti bet kokį naują modelį.

## <a name="for-more-information"></a>Daugiau informacijos

Daugiau informacijos apie tai, kaip įvertinti prognozavimo modelius, žr. [Mašininio mokymo modelių rezultatai](/confusion-matrix.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
