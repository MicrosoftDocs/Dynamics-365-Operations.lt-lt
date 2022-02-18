---
title: Apdorojimo problemos kyla įdiegus masto vieneto sandėlio darbo krūvį
description: Šioje temoje aprašomos problemos, kurios gali kilti netrukus po to, kai yra įdiegtas masto vieneto sandėlio darbo krūvis, ir patariama, kaip jas išspręsti.
author: perlynne
ms.date: 1/13/2022
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningWorkbench, WHSOutboundLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-01-13
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f589ffed61b695f471989ab1dd693f30cd5d5262
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071783"
---
# <a name="processing-issues-occur-after-a-scale-unit-warehouse-workload-is-installed"></a>Apdorojimo problemos kyla įdiegus masto vieneto sandėlio darbo krūvį

Šioje temoje aprašomos problemos, kurios gali kilti netrukus po to, kai yra įdiegtas masto vieneto sandėlio darbo krūvis, ir patariama, kaip jas išspręsti.

## <a name="issue-1-error-after-a-load-is-released-from-a-load-planning-workbench"></a>1 problema: klaida po to, kai apkrova pašalinama iš apkrovos planavimo darbastalio

### <a name="symptoms-of-issue-1"></a>1 problemos simptomai

Kai atleidžiate krovinį iš **Krovinių planavimo darbastalis** arba **Išeinančių apkrovų planavimo darbastalis** puslapyje, gaunate klaidos pranešimą, kurio forma yra tokia:

> Registruojant krovinį %1, buvo užfiksuota išimtis. Krovinio išleisti nepavyko.
> 
> ATNAUJINTI PRIEŽIŪROS LENTELĖS RINKINĮ...
> 
> Negalima redaguoti siuntos įrašo (WHSShipmentTable). Siuntos ID:...

Štai tikras pavyzdys, kuriame yra duomenų pavyzdžiai:

> Pagauta išimtis skelbiant krovinį USMF-000033, krovinio atleisti nepavyko.
Sesija 5133 (administratorius)
>
> ATNAUJINTI WHSSHIPMENT TABLE SET ORDERNUM=?,RECVERSION=?,MODIFIEDDATETIME=?,MODIFIEDBY=? KUR ((RECID=?) IR (RECVERSION=?))  
> [Microsoft][ODBC tvarkyklė 17, skirta SQL serveriui][SQL serveris]Mastelio rinkinys @@ bandė atnaujinti įrašus, priklausančius mastelio rinkiniui @A.  
> Object Server Azure:
>
> Negalima redaguoti siuntos įrašo (WHSShipmentTable). Siuntos ID: USMF-000031, USMF-000033. SQL duomenų bazė pranešė apie klaidą.

### <a name="cause-of-issue-1"></a>1 problemos priežastis

Ši problema gali kilti, jei diegiant mastelio vieneto sandėlio darbo krūvį yra toks sąlygų derinys:

- Sistema apima nepaleistą krovinį, kai kelios eilutės yra susietos su skirtingais užsakymais, o kai kurios krovinio eilutės nėra susietos su siunta.
- Sistema sukurta naudoti siuntų konsolidavimą.

Naudojant paskirstytą hibridinę topologiją, kiekvienas krovinio ir siuntos įrašas yra pažymėtas kaip priklausantis konkrečiam masto vienetui arba centrui. Kai atleidžiate krovinį iš **Krovinių planavimo darbastalis** puslapyje, sistema pakeičia priskirtą nuosavybės teisę. Tačiau dėl anksčiau išvardytų sąlygų sistema gali nesugebėti išspręsti duomenų nuosavybės teisės. Todėl nepavyksta išleisti krovinio į sandėlį.

### <a name="resolution-of-issue-1"></a>1 problemos sprendimas

Prieš išleisdami į sandėlį, padalykite krovinį į du mažesnius krovinius.

## <a name="issue-2-error-while-a-wave-is-processed-on-a-scale-unit"></a>2 problema: klaida apdorojant bangą mastelio vienete

### <a name="symptoms-of-issue-2"></a>2 problemos simptomai

Kai apdorojate bangą mastelio vienete, gaunate klaidos pranešimą, kurio forma yra tokia:

> Negalite keisti įkrovos eilutės su RecId =%1, įkelti id=%2 nes jis vis dar priklauso įmonės centrui. Įsitikinkite, kad atitinkamas siunčiamas krovinys buvo išleistas į mastelio įrenginį ir taip sukurtos sandėlio užsakymo eilutės.

Štai tikras pavyzdys, kuriame yra duomenų pavyzdžiai:

> Darbo „Execute Wave“ informacijos žurnalas USMF-000000012 (9223377668365210)  
> Užduoties informacijos žurnalas Vykdyti bangą USMF-000000012 (9223377668370462)  
> Negalite keisti įkrovos eilutės su RecId = 68719478242, load id= USMF-000034, nes ji vis dar priklauso įmonės centrui. Įsitikinkite, kad atitinkamas siunčiamas krovinys buvo išleistas į mastelio įrenginį ir taip sukurtos sandėlio užsakymo eilutės.

### <a name="cause-of-issue-2"></a>2 problemos priežastis

Naudojant paskirstytą hibridinę topologiją, krovinio ir siuntos duomenų nuosavybės teisė priskiriama konkrečiam masto vienetui arba centrui. Tikimasi, kad atliekant bangavimo apdorojimą duomenų nuosavybės teisė bus priskirta mastelio vienetui.

Kai įdiegiate masto vieneto sandėlio darbo krūvį, jei atidaryta siunta susieta su kroviniu ir banga, sistema negali valdyti duomenų nuosavybės. Todėl skalės bloke nepavyksta apdoroti bangų.

### <a name="resolution-of-issue-2"></a>2 klausimo sprendimas

Paleiskite krovinį į sandėlį nuo stebulės.

## <a name="troubleshoot-issues-by-viewing-a-records-ownership-and-destination"></a>Išspręskite triktis peržiūrėdami įrašo nuosavybės teisę ir paskirties vietą

Paskirstytoje hibridinėje topologijoje daugelio tipų įrašai pažymėti kaip priklausantys konkrečiam mastelio vienetui arba centrui. Kai pereinate prie paskirstytos hibridinės topologijos ir (arba) nustatote naują masto vieneto sandėlio darbo krūvį, sistema priskiria nuosavybės teisę kiekvienam atitinkamam įrašui. Šis procesas kartais gali sukelti klaidų arba netikėtų rezultatų. Todėl informacija apie įrašo nuosavybės teisę ir perdavimo paskirties vietą gali padėti išspręsti problemas, kylančias atlikus tokio tipo pakeitimus.

Atlikite šiuos veiksmus, kad peržiūrėtumėte įrašo nuosavybės teisę ir perdavimo paskirties vietą.

1. Atidarykite atitinkamą įrašą.
1. Veiksmų srityje, ant **Galimybės** skirtuke **Įrašykite informaciją** grupę, pasirinkite **Rodyti visus laukus**.
1. Pasirodžiusiame puslapyje rodomos visų laukų, galimų pasirinktam įrašui, reikšmės. Peržiūrėkite šiuos laukus:

    - **SYSSCALEUNITID** – Šiame lauke rodomas dabartinis įrašo savininkas.
    - **SYSTARGETSCALEUNITID** – Šiame lauke rodomas stebulės arba mastelio vieneto, į kurį bus perkeltas įrašas, mastelio vieneto ID, kai dabartinis savininkas baigs su juo dirbti. Šio lauko reikšmę naudoja paketinės užduotys, kurios valdo tokio tipo procesus. Nors šis laukas nėra tiesiogiai susijęs su nuosavybės teise, nuosavybės teisė gali pasikeisti, kai įrašas perduodamas. Kai kuriais atvejais šis laukas bus tuščias.
