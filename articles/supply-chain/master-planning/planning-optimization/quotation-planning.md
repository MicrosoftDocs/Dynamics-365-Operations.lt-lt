---
title: Planai, pagrįsti pasiūlymais ir komercinio pasiūlymo pasiūlymais
description: Šiame straipsnyje aprašoma, kaip nustatyti bendrąjį planavimą, siekiant atsižvelgti į pasiūlymus ir pasiūlymų patvirtinimus (KPK), kai generuojami suplanuoti užsakymai.
author: t-benebo
ms.date: 09/20/2022
ms.topic: article
ms.search.form: SalesQuotationListPage, ReqPlanSched, SalesQuotationTable, smmOpportunityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-20
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: eaeb3c26a562c1daebe8296b26077ee5a3223e4d
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690165"
---
# <a name="plan-based-on-quotations-and-rfqs"></a>Planas, paremtas pasiūlymais ir RFQ

[!include [banner](../../includes/banner.md)]

Pasiūlymai ir pasiūlymų patvirtinimai (KPK) reiškia galimus arba net tikėtinus būsimus užsakymus. Todėl, svarbu juos apsvarstyti bendrojo planavimo metu, kad papildomas tiekimas galėtų būti planuojamas remiantis esamais komercinio pasiūlymo pasiūlymais ir tikimybe, kad kiekvienas pasiūlymas taps faktiniu užsakymu. Šiame straipsnyje aprašoma, kaip nustatyti bendrąjį planavimą, siekiant atsižvelgti į pasiūlymus ir komercinio pasiūlymo užklausas generuojant suplanuotus užsakymus.

## <a name="set-up-master-planning-to-consider-sales-quotations-andor-rfqs"></a>Nustatyti bendrąjį planavimą siekiant atsižvelgti į pardavimo pasiūlymus ir ( arba) RFQ

Naudokite šią procedūrą, norėdami nustatyti bendrąjį planavimą pardavimo pasiūlymams ir /arba RFQ atsižvelgti.

1. Pereikite prie bendrojo **planavimo nustatymo \> bendrojo \> planavimo \> planų**.
1. Pasirinkite esamą planą sąrašo srityje arba veiksmų srityje pasirinkite **Naujas**, kad sukurtumėte naują.
1. „FastTab“ **Bendra** nustatykite toliau pateikiamus laukus.

    - **Įtraukti pardavimo pasiūlymus –** nustatykite šią pasirinktį *kaip Taip,* jei norite atsižvelgti į pardavimo pasiūlymus, kai vykdomas dabartinis planas. Nustatykite, kad jų *būtų* nepaisoma.
    - **Tikimybės %** – nustatykite minimalų pasitikėjimo lygį, kurio reikia, kad pasiūlymas būtų įtrauktas į bendrąjį planavimą. Bendrojo planavimo skaičiavimas apims visus pasiūlymus, kurie buvo sukurti iš galimybių, kurių tikimybės procentas ar didesnis. Norėdami įtraukti visus pasiūlymus, įskaitant pasiūlymus, kurių tikimybė nepriskirta jiems arba su jais nėra susijusios jokios galimybės, nustatykite šį *lauką kaip 0* (nulis). Daugiau informacijos apie pasiūlymų tikimybes ieškokite kitame skyriuje.
    - **Įtraukti pasiūlymų patvirtinimus – nustatykite** šią pasirinktį kaip *Taip,* jei norite atsižvelgti į KPK, kai vykdomas dabartinis planas. Nustatykite, kad jų *būtų* nepaisoma. Jei pasirinksite atsižvelgti į KPK, sistema sukurs jiems suplanuotus pirkimo užsakymus, tačiau nenu nurodys tiekėjo, kol nebus išspręstas RFQ. RFQ sukurti suplanuoti pirkimo užsakymai gali turėti įtakos kitų suplanuotų užsakymų kiekiams.

1. Toliau savo bendrąjį planą nustatykite įprastu būdu.

## <a name="assign-and-view-probabilities-for-quotations"></a>Priskirti ir peržiūrėti pasiūlymų tikimybes

Kaip buvo nurodyta ankstesniame skyriuje, pagrindiniame plane bus nagrinėtos tik tos pasiūlymai, kurie atitinka arba viršija plano nustatytą tikimybės ribinę vertę (jei nustatyta ribinė reikšmė). Tačiau tikimybė tiesiogiai kiekviename pasiūlyme nėra nustatoma. Vietoj to, jis perimamas iš galimybės, kuri buvo naudojama generuojant pasiūlymą. Todėl pasiūlymuose, **kurie** kuriami tiesiogiai puslapyje Visi pasiūlymai, jiems nebus priskirta tikimybė ar su jais susieta galimybė, ir į juos niekada nebus atsižvelgiama naudojant bendrąjį planavimą (**nebent laukas Tikimybė %** *nustatytas kaip 0*\[\] nulis). Norint, kad jam būtų priskirta tikimybė, iš galimybės turi būti sugeneruotas pasiūlymas.

### <a name="create-a-quotation-from-an-opportunity"></a>Galimybės pasiūlymo kūrimas

Naudokite šią procedūrą tikimybei priskirti galimybei ir tada iš tos galimybės sukurti pasiūlymą.

1. Eiti į **pardavimo ir rinkodaros \> ryšių \> galimybes \> visos galimybės**.
1. Pasirinkite esamą galimybę arba veiksmų srityje **pasirinkite** Nauja, kad sukurtumėte naują.
1. Užpildykite galimybės puslapį, kad identifik kursite norimą galimybę. Būtinai nustatykite atitinkamą **tikimybės** lauko reikšmę. Tik šiuose pagrindiniuose planuose, kurie nustatyti šios vertės arba didesnio tikimybei ieškoti, bus apsvarstyti pasiūlymus, kurie generuojami pagal šią galimybę.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Veiksmų srities skirtuke Galimybė, **naujoje** grupėje, **·** **pasirinkite Pardavimo arba Projekto** pasiūlymą, atsižvelgdami į pasiūlymo tipą, kurį norite sukurti.**·**
1. Dialogo lange **Kurti** pasiūlymą nustatykite laukus taip, kaip jums reikia, tada pasirinkite **Gerai**.
1. Sukuriamas ir atidaromas naujas pasiūlymas. Norėdami pridėti **pardavimo** eilutes arba projekto eilutes, jei reikia pasiūlymo turiniui nustatyti, "FastTab" eilutėse naudokite įrankių juostą.
1. Veiksmų srityje pasirinkite **Įrašyti**. Tada uždarykite pasiūlymą.

### <a name="view-the-probability-that-is-assigned-to-a-quotation"></a>Peržiūrėti tikimybę, kuri priskirta pasiūlymui

Vienintelis būdas peržiūrėti tikimybę, kuri priskirta pasiūlymui, yra atidaryti galimybę, kuri buvo naudojama tam pasiūlymui sukurti, kaip aprašyta toliau pateiktoje procedūroje.

1. Eikite **į Pardavimo ir \> rinkodaros pardavimo pasiūlymus \> Visi pasiūlymai**.
1. Jei galimybės **ID stulpelis** nerodomas (jis paslėptas numatytoje įdiegtyje), norėdami jį laikinai parodyti, atlikite šiuos veiksmus. (Arba palikti **Galimas galimybės ID** stulpelis, sukurkite įrašytą [rodinį](../../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json), kuriame jis yra.)

    1. Tinklelyje pasirinkite ir laikykite (arba spustelėkite dešiniuoju pelės mygtuku) ir pasirinkite Įterpti **stulpelius**.
    1. Įterpimo **stulpelių** dialogo lange raskite **eilutę, kurioje** *Lauko* laukas nustatytas kaip Galimybė, **ir pažymėkite** tos eilutės žymės langelį Pasirinkti.
    1. Pasirinkite **Atnaujinti**, jei norite įtraukti pasirinktą stulpelį į **puslapį Visi** pasiūlymai.

1. Tinklelyje raskite atitinkamo pasiūlymo eilutę. Tada stulpelyje **Galimybės ID** pasirinkite tos eilutės vertę.

    > [!NOTE]
    > Jei ieškote projekto pasiūlymo, gali reikėti pasirinkti pasiūlymo tipo stulpelio **antraštę** ir išvalyti jo filtrą. Numatyta, kad šis filtras nustatomas taip, kad būtų rodomi tik pardavimo pasiūlymai.

1. Atidaryta susijusi galimybė. Dabar galite peržiūrėti ir redaguoti tikimybės **vertę** taip, kaip jums reikia.
