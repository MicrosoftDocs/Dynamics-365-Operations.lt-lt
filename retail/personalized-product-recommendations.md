---
title: "Asmeninį produktų rekomendacijų apžvalga"
description: "Dynamics 365 operacijoms, produkto rekomendacijos gali būti rodomi atsiranda pardavimo (PV) įrenginį. Rekomendacijos yra elementų, kad klientas gali būti domina pagal jų pirkimo istoriją, prekes į savo pageidavimų sąrašus ir daiktų, kad kitiems klientams įsigyti internetu ir plytų ir skiedinio parduotuvėse. Mažmeninės prekybos su didelės katalogai, rekomendacijas padėti klientui produkto aptikimo. Pademonstruotų produktų, orientuojasi į kliento interesus ir pirkimo įpročius, produkto rekomendacijos gali padėti mažmenininkams viršų pardavimas ir kryžminio parduoti, ir gali padidinti klientų išlaikymas. Dynamics 365 operacijoms, produkto rekomendacijos yra powered pažinimo tarnybų ir Microsoft Azure mašinos mokymosi."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: af1f4ba1ed5efe0e35d08d37d09e7ada4a4c1b7a
ms.lasthandoff: 03/31/2017


---

# <a name="personalized-product-recommendations-overview"></a>Asmeninį produktų rekomendacijų apžvalga

Dynamics 365 operacijoms, produkto rekomendacijos gali būti rodomi atsiranda pardavimo (PV) įrenginį. Rekomendacijos yra elementų, kad klientas gali būti domina pagal jų pirkimo istoriją, prekes į savo pageidavimų sąrašus ir daiktų, kad kitiems klientams įsigyti internetu ir plytų ir skiedinio parduotuvėse. Mažmeninės prekybos su didelės katalogai, rekomendacijas padėti klientui produkto aptikimo. Pademonstruotų produktų, orientuojasi į kliento interesus ir pirkimo įpročius, produkto rekomendacijos gali padėti mažmenininkams viršų pardavimas ir kryžminio parduoti, ir gali padidinti klientų išlaikymas. Dynamics 365 operacijoms, produkto rekomendacijos yra powered pažinimo tarnybų ir Microsoft Azure mašinos mokymosi.

<a name="scenarios"></a>Scenarijai
---------

Produktų rekomendacijos yra įgalintas šių POS scenarijų. Jie debesis POS ir modernus EKA (MPOS).

1.  Dėl to **informacija apie** puslapis:

-   Jei parduotuvėje susieti apsilankymus su **informacija apie** puslapį, kai žiūri į ankstesnes operacijas per skirtingus kanalus, rekomendacija variklis siūlo papildomas elementai, kurie yra linkę būti perkami kartu.
-   Jei parduotuvėje susieti prideda klientą į operaciją ir tada apsilanko per **informacija apie** puslapyje, rekomendacija variklis suteikia pritaikytas rekomendacijas, naudojant kliento operacijų istorija.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

1.  Dėl to **operacija** puslapis:

-   Rekomendacija variklis rodo elementus, atsižvelgiant į visą sąrašą prekių į krepšelį.
-   Jei parduotuvėje susieti prideda klientą į operaciją, rekomendacija variklis suteikia asmeninių rekomendacijų, naudojant kliento operacijų istorija ir elementų sąrašas į krepšelį.

**Pastaba** Rodyti rekomendacijas dėl **operacija** puslapyje, agentas turi atnaujinti ekrano išdėstymas Dynamics 365 operacijoms. Į **rekomendacijų** kontrolė turi būti atsisakyta į į **operacija** puslapis. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

1.  Dėl to **Kontaktinis asmuo** puslapis:
    -   Rekomendacija variklis siūlo prekes pagal vartotojo ID bei kliento pageidavimų sąrašo elementus.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>Konfigūruoti Dynamics 365 operacijoms, kad POS rekomendacijos
Norėdami nustatyti produkto rekomendacijos, jums reikia atlikti šiuos veiksmus.

1.  Įsitikinkite, kad pasirinkote teisingą **juridinis asmuo**.
2.  Eikite į **įmonės parduotuvė**, pasirinkite **mažmeninė prekyba**, ir tada spustelėkite **atnaujinti**. ** ** tai naudoja parodomojoje versijoje (ar savo duomenis) iš savo veiklos duomenų bazės ir perkelti jį į įmonės parduotuvėje.
3.  Pasirenkama: Rodyti rekomendacijas operacijų ekrane, eikite į ** ekrano išdėstymas, **pasirinkti ekrano išdėstymas, pradėti, **ekrano išdėstymas dizaineris**,** ** ir tada lašas į ** rekomendacijas valdymo ** ten, kur reikia.
4.  Eikite į **mažmeninė prekyba parametrai**, pasirinkite **sistemos mokymosi**, pasirinkite ** taip ** pagal **įgalinti POS rekomendacijas**.
5.  Norėdami pamatyti rekomendacijas EKA, globalinis konfigūracijos užduotį vykdyti **1110**. Siekiant atspindėti pakeitimus POS ekranas maketo konstruktorių, kanalo konfigūracijos užduotį vykdyti **1070**.

## <a name="how-does-it-work"></a>[]()Kaip tai veikia?
Kai atnaujinate į **įmonės parduotuvė** subjektas, šių veiksmų vyksta.

-   Duomenų formatu, pažinimo tarnybos ekstrahuojamas Dynamics 365 operacijų veiklos duomenų bazės ir išsiųstas į įmonės parduotuvę.
-   Duomenys naudojami iš Azure duomenų fabrikas (ADF) išvalyti duomenis naudodami avilio scenarijus ADF veiklą. Nuvalytos duomenys yra laikomi blob saugyklų.
-   Pažinimo paslaugų API naudoja duomenis iš blob saugyklų mokyti rekomendacija pavyzdys.

Kai įjungiate **sudaryti rekomendacijas** ir paleiskite konfigūravimo darbus, šių veiksmų vyksta.

-   Modelis kredencialus ir ID yra įlaipinami iš API ir saugomi Dynamics "365" operacijų veiklos duomenų bazę, AOS Web.config, ir taip pat mažmeninės prekybos Server.
-   Modelis kredencialus ir ID yra prieinama CRT, kad ragina produkto rekomendacijos iš debesies POS ir MPOS prijungties režimu gali būti gerbiamas.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Pridėti rekomendacijas valdymo operacijų puslapio POS įrenginį](add-recommendations-control-pos-screen.md)


