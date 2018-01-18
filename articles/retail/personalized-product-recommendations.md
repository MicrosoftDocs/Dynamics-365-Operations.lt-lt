---
title: "Personalizuotų produktų rekomendacijų apžvalga"
description: "Šioje temoje pateikiama informacija apie „Dynamics 365 for Retail“ produkto rekomendacijas, kurios gali būti rodomos elektroninio kasos aparato (EKA) įrenginyje."
author: ashishmsft
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 64f0a9a44b97a9980f8d1b76ff158f1ac9cbc114
ms.openlocfilehash: 942d6225a46b108ea39d3b8e4376b644c128ae6d
ms.contentlocale: lt-lt
ms.lasthandoff: 11/14/2017

---

# <a name="personalized-product-recommendations-overview"></a>Personalizuotų produktų rekomendacijų apžvalga

[!include[banner](includes/banner.md)]


> [!NOTE]
> Šią funkciją dabar galima naudoti tik smėlio dėžės ir gamybos (plataus pasiekiamumo) visuotinio diegimo topologijose. 

Programoje „Dynamics 365 for Retail“ produkto rekomendacijos gali būti rodomos elektroninio kasos aparato (EKA) įrenginyje. Rekomendacijos –tai prekės, kurios gali sudominti klientą atsižvelgiant į jo pirkimo istoriją, prekės, kurias klientas įtraukė į savo norų sąrašą, ir prekės, kurias kiti klientai įsigijo internetu ir įprastose parduotuvėse. Mažmenininkų, turinčių didelius prekių katalogus, klientams rekomendacijos padeda surasti produktus. Kadangi pateikiant produkto rekomendacijas demonstruojami į kliento pomėgius ir pirkimo įpročius orientuoti produktai, mažmenininkams tai gali padėti atlikti papildomą ir kryžminį pardavimą ir išsaugoti klientus. Naudojant „Dynamics 365 for Retail“ produkto rekomendacijos pateikiamos pagal pažintines paslaugas ir „Microsoft Azure“ mašininį mokymą.


<a name="scenarios"></a>Scenarijai
---------

Produktų rekomendacijas galima naudoti taikant toliau nurodytus EKA scenarijus. Juos rasite naudodami „Cloud POS“ arba „Modern POS“ (MPOS).

1.  Puslapyje **Produkto informacija**:

-   Jeigu parduotuvės atstovas puslapyje **Produkto informacija** apsilanko skirtinguose kanaluose žiūrėdamas į ankstesnes operacijas, rekomendacijų variklis siūlo kitų prekių, kurios gali būti perkamos papildomai.
-   Jei parduotuvės atstovas į operaciją įtraukia klientą, o po to apsilanko puslapyje **Produkto informacija**, naudodamas kliento operacijų istoriją ir krepšelyje esančių prekių sąrašą rekomendacijų variklis pateikia personalizuotas rekomendacijas.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  Puslapyje **Operacija**:

-   Rekomendacijų variklis siūlo prekes atsižvelgdamas į visą krepšelyje esančių prekių sąrašą.
-   Jei parduotuvės atstovas į operaciją įtraukia klientą, naudodamas kliento operacijų istoriją ir krepšelyje esančių prekių sąrašą rekomendacijų variklis pateikia asmenines rekomendacijas.

> [!NOTE]
> Norėdamas, kad rekomendacijos būtų rodomos puslapyje **Operacija**, pardavėjas turi atnaujinti „Dynamics 365 for Retail“ ekrano išdėstymą. Valdiklis **Rekomendacijos** turi būti perkeliamas į puslapį **Operacija**. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  Puslapyje **Kliento informacija**:
    -   Rekomendacijų variklis siūlo prekes atsižvelgdamas į vartotojo ID ir kliento norų sąraše esančias prekes.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a>Sukonfigūruokite „Dynamics 365 for Retail“, kad būtų leidžiamos EKA rekomendacijos
Norėdami nustatyti produktų rekomendacijas turite atlikti toliau nurodytus veiksmus.

1.  Įsitikinkite, kad pasirinkote tinkamą **Juridinį subjektą**.
2.  Eikite į **Objekto parduotuvė**, pasirinkite **Mažmeninės prekybos pardavimai**, tada spustelėkite **Atnaujinti**. Taip demonstraciniai duomenys (arba jūsų duomenys) bus naudojami iš jūsų operacinės duomenų bazės ir perkeliami į objektų saugyklą.
3.  Nebūtina: norėdami, kad rekomendacijos būtų rodomos operacijos ekrane, eikite į dalį **Ekrano išdėstymas**, pasirinkite savo ekrano išdėstymą, paleiskite **ekrano išdėstymo kūrimo priemonę**, o po to kur reikia perkelkite **rekomendacijų** valdiklį.

4.  Eikite į **Mažmeninės prekybos parametrai**, pasirinkite **Mašininis mokymas**, dalyje **Įjungti EKA rekomendacijas** pasirinkite **Taip**.
5.  Norėdami pamatyti rekomendacijas naudodami EKA, paleiskite visuotinės konfigūracijos užduotį **1110**. Norėdami, kad būtų rodomi EKA ekrano išdėstymo kūrimo priemonei atlikti pakeitimai, paleiskite kanalo konfigūracijos užduotį **1070**.

## <a name="how-does-it-work"></a>[]()Kaip tai veikia?
Atnaujinus objektą **Objekto parduotuvė** atliekami toliau nurodyti veiksmai.

-   Pažintinėms paslaugoms reikiamu formatu pateikti duomenys ištraukiami iš „Dynamics 365 for Retail“ operacinės duomenų bazės ir siunčiami į objekto parduotuvę.
-   Duomenis naudoja programa „Azure Data Factory“ (ADF), kuri išvalo juos kaip ADF veiklų dalį naudodama „Hive“ scenarijus. Išvalyti duomenys saugomi didelių dvejetainių objektų saugykloje.
-   Iš didelių dvejetainių objektų saugyklos gautus duomenis naudoja pažintinių paslaugų API, kad paruoštų rekomendacijos modelį.

Kai įjungiate **Įjungti rekomendacijas** ir paleidžiate konfigūracijos užduotis, atliekami toliau nurodyti veiksmai.

-   Iš API gaunami modelio kredencialai ir ID, kurie saugomi „Dynamics 365 for Retail“ operacinėje duomenų bazėje, AOS skirtame web.config ir mažmeninės prekybos serveryje.
-   Modelio kredencialais ir ID gali naudotis CRT, kad būtų galima apmokėti naudojant internetinį režimą iš „Cloud POS“ ir MPOS atliktus skambučius dėl produkto rekomendacijų.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Rekomendacijų valdiklio įtraukimas į EKA įrenginio operacijų puslapį](add-recommendations-control-pos-screen.md)




