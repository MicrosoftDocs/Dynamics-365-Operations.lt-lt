---
title: Eksperimentavimas „Dynamics 365 Commerce”
description: Eksperimentavimas leidžia kurti, redaguoti ir valdyti puslapio maketų bei turinio apdorojimo būdus svetainių daryklėje. Palaikomas visapusis eksperimentavimas el. prekybos puslapiuose ir puslapyje esančiuose objektuose.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: overview
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1ef877072ba7ffe1b0326cf8d526b512b5ab30b8
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946219"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Eksperimentavimas „Dynamics 365 Commerce”
Naudokite „Dynamics 365 Commerce” eksperimentavimą, norėdami patvirtinti jūsų „e-Commerce” puslapių efektyvumo hipotezes ir priimti patikimus, duomenimis pagrįstus sprendimus. „Commerce” palaiko A / B tikrinimą puslapiuose, moduliuose ir fragmentuose bei leidžia įvertinti siūlomų svetainės pakeitimų poveikį.

„Commerce” svetainių daryklėje galite kurti, redaguoti ir valdyti puslapių bei turinio apdorojimo būdus, vadinamus **variacijomis**. „Commerce” integruojama su trečiųjų šalių paslaugomis, kurias galite naudoti eksperimentams ir apdorojimo užduotims kurti. „Commerce” užfiksuoti realiojo laiko įvykių srautai leidžia atlikti analizę, nurodančią eksperimento rezultatus trečiosios šalies paslaugoje. Tada galite panaudoti šią analizę, norėdami patvirtinti arba paneigti jūsų hipotezę.

## <a name="set-up-prerequisites"></a>Būtinųjų sąlygų nustatymas

1. **Gaukite tinkamą „Commerce” versiją** – atnaujinkite jūsų modulių biblioteką, interneto kanalo išplečiamumo programinės įrangos kūrimo rinkinį (SDK) ir „Commerce Scale Unit” į „Commerce” 10.0.13 arba naujesnę versiją.
1. **Nustatykite eksperimento jungtį** – eksperimento jungtis leidžia „Commerce” prisijungti prie trečiųjų šalių paslaugų ir gauti eksperimentų sąrašą siekiant nustatyti, kada vartotojui parodyti eksperimentą. Galite įsigyti trečiosios šalies jungtį iš [„AppSource”](https://appsource.microsoft.com). Sekite leidėjo pateiktas nustatymo instrukcijas. Taip pat galite naudoti „Commerce” bandymo jungtį, norėdami patikrinti eksperimento darbo eigą, nekonfigūruodami išorinės paslaugos. Daugiau informacijos žr. [Jungčių konfigūravimas ir įjungimas](e-commerce-extensibility/connectors.md). 
1. **Įjunkite "Commerce**" buhalteriacijos priemonių vėliavėlę – **\>** **galite įgalinti dialogo parametrų funkciją nuomininkų lygiu, nueiti į nuomininkų parametrų funkcijas arba svetainės lygį nueiti į svetainės parametrų \> funkcijas**. Jei norite pradėti kurti modulio **variacijas**, įjunkite vėliavėlę Jo vėliavėlė. Išjungus šią vėliavėlę, sustabdomas visų eksperimentų rodymas vartotojams ir pašalinamos visos svetainių daryklės redagavimo funkcijos.
    
## <a name="experimentation-lifecycle"></a>Eksperimento ciklas

Eksperimento nustatymas, variacijų kūrimas ir eksperimento vykdymas yra kartotinis procesas. Toliau pateiktoje diagramoje rodomas eksperimento ciklas „Commerce” ir trečiosios šalies paslaugoje. 

[ ![Eksperimento ciklas.](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Norėdami daugiau sužinoti apie kiekvieną atlikimo proceso žingsnį, remkitės šiais straipsniais.
- [Eksperimento hipotezės ir metrikos nustatymas](experimentation-identify.md)
- [Eksperimento nustatymas](experimentation-setup.md)
- [Eksperimento prijungimas ir redagavimas](experimentation-connect-edit.md)
- [Eksperimento peržiūra ir publikavimas](experimentation-preview-publish.md)
- [Eksperimento vykdymas ir stebėjimas](experimentation-run-monitor.md)
- [Variacijos perkėlimas į aukštesnį lygį ir eksperimento užbaigimas](experimentation-review-complete.md)

> [!NOTE]
> Norėdami sužinoti, kurioje ciklo vietoje yra eksperimentas, svetainių daryklės kairiojoje naršymo srityje pasirinkite **Eksperimentai**. Rodomas eksperimentų sąrašas su kiekvieno eksperimento būsena „Commerce” ir trečiosios šalies paslaugoje. Daugiau informacijos žr. [Eksperimento būsenos peržiūra](experimentation-status.md).

## <a name="next-step"></a>Kitas veiksmas
[Eksperimento hipotezės ir sėkmės metrikos nustatymas](experimentation-identify.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
