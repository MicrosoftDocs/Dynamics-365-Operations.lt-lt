---
title: Naujo transportavimo valdymo mechanizmo kūrimas
description: Šioje temoje aprašoma, kaip sukurti naują transportavimo valdymo modulį, kuris bus sukurtas dalyje „Dynamics 365 Supply Chain Management“.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSGenericEngine, TMSRateEngine, TMSMileageEngine, TMSEngineParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 51661
ms.assetid: 0473acef-755e-4b42-acf5-5e5aa902dc0e
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88661b6a974e2bd60f78e38d49a08d3290008b8b
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/19/2021
ms.locfileid: "7652049"
---
# <a name="create-a-new-transportation-management-engine"></a>Naujo transportavimo valdymo mechanizmo kūrimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip sukurti naują transportavimo valdymo modulį, kuris bus sukurtas dalyje „Dynamics 365 Supply Chain Management“. 

Transportavimo valdymo mechanizmai (TMS) apibrėžia logiką, naudojamą generuojant ir apdorojant transportavimo tarifus modulyje Transportavimo valdymas. „Supply Chain Management“ suteikia keletą skirtingų modulių tipų, kurie apskaičiuoja skirtingus parametrus, pvz., tarifus, tranzito laikus ir zonų, kurios bus pereitos tranzito metu, skaičių. Šiame straipsnyje paaiškinama, kaip naudoti programavimo aplinką kartu su „Supply Chain Management“ kūrimo įrankiais, siekiant sukurti ir įdiegti naują TMS tinklą, ir kaip nustatyti jį „Microsoft Visual Studio“ operacijose. Daugiau informacijos apie variklius rasite [Transportavimo valdymo mechanizmai](transportation-management-engines.md).

## <a name="create-a-new-tms-engine"></a>Kurti naują TMS variklį

Šiame skyriuje paaiškinama, kaip sukurti klasių biblioteką, kurioje yra TMS modulio diegimas, ir kaip ją nurodyti iš „Supply Chain Management“ modelio.

1. Norėdami diegti naujus sistemas, turite turėti modelį, kuriame bus modeliai. Meniu **Dynamics 365**&gt;**Modelių valdymas** spustelėkite **Kurti modelį** sukurkite naują modelį. Pirmame modelio kūrimo **vedlio puslapyje** pavadinkite modelį **TMSEngines**. 

   [![Modelio kūrimas.](./media/012.png)](./media/012.png)

2. Kitame puslapyje pasirinkite **Kurti naują pakuotę**. 

   [![Naujo paketo kūrimas.](./media/021.png)](./media/021.png)

3. Kitame puslapyje pasirinkite nurodyti norimą **ApplicationSuite** modelį. (**ApplicationPlatform** modelis bus iš anksto pasirinktas.) 

   [![Modelio, kurį norite nurodyti, pasirinkimas.](./media/032.png)](./media/032.png)

4. Kitame puslapyje spustelėkite **Baigti** kad patvirtintumėte naujo modelio kūrimą. 

   [![Modelio kūrimo užbaigimas.](./media/042.png)](./media/042.png)

5. Naujame teoryje sukurkite naują „Supply Chain Management“ projektą ir pavadinkite jį **TMSThirdParty**. Projekto ypatybėse nustatykite projekto modelį **TMSEngines**.
6. Prie savo sprendimo pridėkite naują C\# klasės biblioteką ir pavadinkite ją **ThirdPartyTMSEngines**.
7. ThirdPartyTMSEngines projekte pridėkite nuorodas į „Supply Chain Management“ konkrečius rinkinius:
   -   Programų rinkiniai, kurie įgalina nurodyti X++ tipus. Šiuos rinkinius galima rasti šiose vietose. \[Paketų šaknis\] yra vietos, kurioje padėti visi įdiegti rinkiniai, maršrutas, pvz., C:\\Paketai.

        ```xpp
        [Packages root]\ApplicationPlatform\bin\Dynamics.AX.ApplicationPlatform.dll
        [Packages root]\ApplicationFoundation\bin\Dynamics.AX.ApplicationFoundation.dll
        [Packages root]\ApplicationSuite\bin\Dynamics.AX.ApplicationSuite.dll
        ```
        
   -   Sistemos rinkiniai, kurie įgalina prieigą prie duomenų, LINQ ir pagalbinių funkcijų. Visus šiuos rinkinius galima rasti \[pakuočių šakninėje\]\\talpyklose.

        ```xpp 
        Microsoft.Dynamics.ApplicationPlatform.Environment.dll
        Microsoft.Dynamics.AX.Data.Core.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.AdoNet.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll
        Microsoft.Dynamics.AX.Server.Core.dll
        Microsoft.Dynamics.AX.Xpp.AxShared.dll
        Microsoft.Dynamics.AX.Xpp.Support.dll
        ```

   -   Pagrindinis TMS rinkinys (kuriame yra sistemų) ir TMS pagrindinis rinkinys (kuriame yra pagalbos priemonės, konstantos, duomenų perkėlimo klasės apibrėžimai ir t. t.). Šiuos rinkinius galima rasti šiose vietose.

        ```xpp
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.dll
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.Base.dll
        ```
8. Pervardyti C\# klasę, kuri automatiškai sugeneruota ThirdPartyTMSEngines projekte į **SampleRatingEngine**.
9. Įdiegti sistemą. Kadangi šiame pavyzdyje kuriamas tarifo modulis, perimame iš tarifų modulių pagrindinės klasės. Bazinė klasė įdiegia daugumą tarifo ir pavarų sąsajos (**TMSFwkIRateEngine**). Tiesiog turime įdiegti tarifo metodą. Jei norite, kad šis pavyzdys būtų paprastas, mes užregistruosime šį metodą 100 eilutėse pagal už kodą išseks 100. Galite sukurti sistemas, kurios įdiegia bet kurią iš sistemų sąsajų, pvz., **TMSFwkIAccessorialEngine**. Visos modulio sąsajos yra nustatytos X++.

    ```xpp
    namespace ThirdPartyTMSEngines
    {
        using Dynamics.AX.Application;
        using Microsoft.Dynamics.Ax.Tms.Base.Data;
        using Microsoft.Dynamics.Ax.Tms.Base.Utility;
        using Microsoft.Dynamics.Ax.Tms.Bll;
        using System.Xml.Linq;
        public class SampleRatingEngine : BaseRateEngine
        {
            public override RatingDto rate(TmsTransactionFacade transactionFacade, XElement shipment, TMSRateMasterCode rateMasterCode)
            {
               XElement re = shipment.RetrieveOrCreateRatingEntity(this.RatingDto);
               re.AddRate(TmsRateType.Rate, 100);
               return this.RatingDto;
            }
        }
    }
    ```

10. Kurti sprendimą.
11. Įtraukite naują nuorodą į TMSThirdParty projektą. Nuoroda turi nurodyti ThirdPartyTMSEngines projektą. Kai baigiate, sprendimas turėtų taip atrodyti. 

    [![Sprendimas, kuris apima nuorodą į TMSThirdParty projektą.](./media/052.png)](./media/052.png)

12. Kurti sprendimą. Patikrinkite, ar nauja biblioteka yra **Programos** sprendimą nuorodų mazge. 

    [![Nauja biblioteka programos naršyklės nuorodų mazge.](./media/061.png)](./media/061.png)

## <a name="deploy-the-tms-engine-as-a-package"></a>Diegti TMS paketą kaip paketą

Vienas būdas diegti trečiosios šalies TMS sistemas yra per diegimo paketą. Šis būdas rekomenduojamas gamybos aplinkoje. Programavimo aplinkoje galite rankiniu būdu nukopijuoti rinkinius, kaip aprašyta kitame skyriuje "TMS modulio nustatyti „Supply Chain Management.“ Norėdami rankiniu būdu talpint variklį kaip paketą, atlikite tolesnius veiksmus.

1. Meniu **Dynamics 365** &gt; **Talpinti** meniu spauskite <strong>Kurti talpinimo paketą</strong>.
2. Dialogo lange **Kurti diegimo paketą** pasirinkite TMSEngines modelį ir įveskite maršrutą, kur norite saugoti savo pakuotės failus. 

   [![TMSEngines modelio pasirinkimas.](./media/071.png)](./media/071.png)

3. Dabar galite diegti paketą paskirties aplinkoje. Jei norite sužinoti, žr. [kaip diegti paketą,](../../fin-ops-core/dev-itpro/deployment/install-deployable-package.md).

## <a name="set-up-the-tms-engine-in-supply-chain-management"></a>TMS variklio konfigūravimas „Supply Chain Management”

Šiame skyriuje paaiškinama, kaip nustatyti „Supply Chain Management“, kad būtų naudojamas TMS modulis, ir parodyta, kaip naujasis mūsų sukurtas variklis naudojamas perkant tarifą. Šioje skyriuje pavyzdys naudoja USMF demonstracinių duomenų įmonę.

1. Sukurkite naują, kaip nurodyta skyriuje „Kurti naują TMS variklis".
2. Kurti savo sprendimą.
3. Nukopijuokite gautą surinkimą į tiekimo „Supply Chain Management“ dvejetainę vietą \[AOSWebRoot\]talpykloje. **Pastaba:** šis veiksmas taikomas tik programavimo aplinkoje. Gamybos aplinkoje turite įdiegti diegimo pakete. Norėdami gauti daugiau instrukcijų, žr. ankstesniame skyriuje „TMS modulio kaip paketo diegimas."
4. „Supply Chain Management“ puslapyje **Tarifo valdymas** sukurkite naują vertinimo grandinę. Variklis turi nurodyti modulio rinkinį, kuris sukurtas kuriant modulio klasių biblioteką ir jūsų įdiegėte modulio klasę. 

   [![Tarifo valdymo puslapyje kuriamas naujas vertinimo modulis.](./media/081.png)](./media/081.png)

5. Sukurkite siuntos vežėją, kuris naudoja pavyzdinio tarifo vežėją. Kadangi mūsų sistema nenaudos jokių duomenų, jums nereikia priskirti pagrindinio tarifo. 

   [![Kurti naują siuntų vežėją.](./media/092.png)](./media/092.png)

6. Tarifo **Maršruto darbo vietos** puslapyje spustelėkite **Tarifo cechas**. Iš SampleCarrier turėtumėte matyti 100,00 tarifą, kaip parodyta pateiktoje ekrano nuotraukoje. Šiame pavyzdyje mes naudojame maršruto iš sandėlio 24 į klientą US-004 tarifą. Tačiau, kadangi tarifas yra už codetas, visada bus 100,00 tarifas.

   [![Tarifo ir maršruto darbo sritis.](./media/101.png)](./media/101.png)

## <a name="tips-and-tricks"></a>Patarimai

- Jei naudojate „Supply Chain Management“ kūrimo įrankius, naudinga į savo sprendimą įtraukti naują projektą. Jei nustatote šį projektą kaip savo paleisties projektą ir pradedate derinimo seansą, galite derinti ir X++, ir C\# kodą pačiame derinimo seanse.
- Kiekvieną kartą, kai keičiate ir perkompiliuokite savo ThirdPartyTMSEngines projektą, turite rankiniu būdu nukopijuoti gautą surinkimą į dvejetainę vietą arba diegti diegimo paketu. Kitu atveju galite vykdyti naudodami pasenusią surinkimą.
- Apdorojus TMS-specific operacijas „Supply Chain Management“, informacinių interneto paslaugų (IIS) darbuotojo procesas gali užrakinti ThirdPartyTMSEngines surinkimą, kad jo būtų galima atnaujinti. Tokiu atveju iš naujo paleiskite w3svc procesą.

### <a name="whitepaper"></a>Techninė Dokumentacija

Norėdami gauti daugiau informacijos, atsisiųskite šią techninę dokumentaciją (sukurtą AX2012 palaikymui, tačiau vis dar taikoma „Dynamics 365 Supply Chain Management”)

- [Transportavimo valdymo sistemų diegimas ir diegimas](https://download.microsoft.com/download/b/5/f/b5ff8fef-3918-4c1d-92d5-b67eb0971684/ImplementingAndDeployingTransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]