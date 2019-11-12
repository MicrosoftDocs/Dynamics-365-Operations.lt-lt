---
title: Produkto gavimas pagal pirkimo užsakymą
description: Šioje temoje aprašomos įvairios produktų registravimo kaip baigtų produktų parinktys.
author: FrankDahl
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 93113
ms.assetid: d4ec3e86-fce2-4546-911b-e0acf64c8887
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b01e7e8e79061c7a306f00f041413cc1c5185cfe
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572272"
---
# <a name="product-receipt-against-purchase-orders"></a>Produkto gavimas pagal pirkimo užsakymą

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos įvairios produktų registravimo kaip baigtų produktų parinktys.

Produkto gavimas yra procesas, kurio metu užregistruojama, kurie užsakyti produktai buvo gauti, kad būtų galima apdoroti pirkimo užsakymo (PU) eilutes ir išrašyti SF. Kai kuriais atvejais vykdoma išankstinė produktų registracija, tais atvejais, kai papildoma iš tiekėjo gauta informacija užregistruojama prieš produktų gavimą. Kai produktai pristatomi, jie pirmiausia pažymimi kaip **Užregistruoti**. Tada gali būti vykdomi papildomi produktų apdorojimo procesai, pavyzdžiui, kokybės valdymas, kol galiausiai jie pažymimi kaip **Gauti**.

## <a name="preregistration-asn"></a>Išankstinė registracija (ASN)
Tiekėjai gali bendrinti informaciją apie produktus, kurie bus siunčiami. Tokiu atveju galite produktus užregistruoti iš anksto ir įrašyti šią informaciją prieš produktų gavimą. Iš anksto registruodami produktus galite sumažinti darbus, būtinus atlikti prekių registravimo ir gavimo metu. Tiekėjai gali pateikti produkto informaciją elektroniniu būdu naudodami išankstinį siuntimo pranešimą (ASN), kuris tada yra automatiškai įrašomas į sistemą. ASN informacija apima siunčiamų produktų kiekį ir datą, kada jie bus siunčiami. ASN taip pat gali apimti kitą informaciją, pvz., paketo arba serijos numerius. ASN registracija vykdomu modulyje **Transportavimo valdymas**.

## <a name="registration"></a>Registracija
Produkto gavimo registracija dažnai vykdoma sandėlio atvežimo rampose. Ji atliekama naudojant rankinį įrenginį arba gavimo žurnalus. Produkto gavimą taip pat galite užregistruoti neautomatiniu būdu, puslapyje **Pirkimo užsakymas** naudodami veiksmą **Registravimas**. Abiem atvejais produktai yra pažymimi kaip **Užregistruoti**. Atkreipkite dėmesį, kad produktai dar nėra pažymimi kaip **Gauti**.  

Sandėlyje gali būti vykdoma gautų produktų kokybės patikra, prieš perkeliant juos į atsargas. Norint atlikti kokybės patikrą, galima naudoti kokybės užsakymus arba sulaikymo užsakymus. Jei naudojami kokybės užsakymai, galima procesą sukonfigūruoti, kad rezervavimo būdu produktai būtų laikinai užblokuoti, kol jie yra tikrinami. Jei naudojami sulaikymo užsakymai, produktai yra perkeliami į kitą sandėlį patikrai vykdyti. Šis sandėlis vadinamas sulaikymo sandėliu. Vykdant abu kokybės tikrinimo procesus, kai kurios prekės gali būti nurašytos, nes jos neatitiko kokybės reikalavimų arba kokybės tikrintojai atliko produkto pavyzdžio ardomąjį bandymą.

## <a name="product-receipt"></a>Gavimo dokumentas
Dažniausiai puslapio **Pirkimo užsakymai** veiksmas **Produkto gavimo kvitas** naudojamas, kad PU produktai būtų pažymėti kaip **Gauti**. Puslapyje **Produkto gavimo kvito registravimas** pateikiama yra įvairių kiekio, kuris yra apskaitomos kaip gautas, parinkčių. Pvz., lauką **Kiekis** galite nustatyti į parinktį **Užsakytas kiekis** arba **Dabartinio gavimo kiekis**. Jei buvo vykdomas sandėlio gavimo procesas, šis laukas dažnai nustatomas į parinktį **Užregistruotas kiekis**. Kiekius galima modifikuoti kiekvienoje užsakymo eilutėje, kuri pažymėta kaip **Gauta**, kad būtų apskaityti visi neatitikimai, pvz., pristatymo trūkumas ir pristatymo perviršis. Produkto gavimo metu turite nurodyti produkto gavimo kvito identifikatorių, kuris paprastai yra nuoroda į važtaraštį, gautą iš tiekėjo. Šis identifikatorius reikalingas apskaitai atlikti, nes jis suteikia galimybę tiekėjo važtaraščius patikrinti arba audituoti pagal tai, kas buvo pristatyta, ir pagal apskaitytas atsargas arba išlaidas.  

PU galima sukurti produktams, kurie nėra skirti perkelti į atsargas, bet yra laikomi išlaidomis. Ši kategorija apima užsakymo eilutes, kuriose produktai yra pažymėti kaip **Nelaikoma atsargose** pagal jų atsargų modelio grupę, ir eilutes, kuriose naudojamos įsigijimo kategorijos. Tokiu atveju prekių pristatymo registravimo ir gavimo sandėlyje procesai gali būti nevykdomi. Tada veiksmas **Produkto gavimo kvitas** yra naudojamas gavimui tiesiai į PU įrašyti, o gavimas yra pagrįstas užsakytu kiekiu, o ne užregistruotu kiekiu.  

Galite kurti PU eilutes, kuriose suaktyvinta parinktis **Naujas ilgalaikis turtas**. Ši parinktis nurodo, kad pirkimas turėtų būti laikomas ilgalaikiu turtu, o ne atsargomis. Tokiu atveju sukonfigūruotos ilgalaikio turto nustatymo taisyklės nustato, ar produkto arba kategorijos pirkimas viršija konkrečias ribines reikšmes ir todėl turi būti apskaitomas kaip turtas bei jam reikia vykdyti ilgalaikio turto valdymo procesą. Taip pat galima vykdyti pirkimus, skirtus esamam ilgalaikiam turtui. Tokiu atveju suma yra koreguojama atitinkamai.  

Galite pasirinkti kelis užsakymus ir kartu apdoroti visų užsakymų gavimą. Šis metodas nėra labai dažnai naudojamas, bet jį naudoti gali būti naudinga, jei tiekėjas konsolidavo siuntas į vieną krovinį. Perkamo produkto gavimo metu galima atlikti suminių naujinimų. Suminiai naujinimai suteikia galimybę vieną tiekėjo važtaraštį užregistruoti daugiau nei vienam PU.  

PU galima kurti iš pardavimo užsakymo, kuriame pažymėta parinktis **Tiesioginis pristatymas**. Naudojant tiesioginį pristatymą, produktai niekada nepristatomi į jūsų sandėlį, bet yra tiesiogiai siunčiami iš tiekėjo klientui. Tokiu atveju gavimas paprastai užregistruojamas tiesiai PU. Gavimą galima atlikti automatiškai, pvz., naudojant elektroninių duomenų apsikeitimo (EDI) integraciją su tiekėju. Jei PU yra vidinės įmonės PU, Tiekimo grandinės valdymas siuntimo metu automatizuoja vidinės įmonės pardavimo užsakymo gavimą. Naudojant tiesioginį pristatymą, produktai vis tiek apskaitomi kaip atsargos, nors jie fiziškai nėra pristatomi į sandėlį. Todėl, kai PU užregistruojamas produkto gavimas, pardavimo užsakymas yra automatiškai atnaujinamas pridedant važtaraštį, kad bendras atsargų pokytis būtų 0 (nulis). Naudojant tiesioginį pristatymą, išankstinė registracija nereikalinga. Jei naudojate sandėlius, kuriuose galima naudoti sandėlio valdymo funkciją, numerio lentelės registravimo reikalavimą galite apeiti nurodydami virtualų sandėlį. Šis sandėlis nurodomas produkto lauke **Tiesioginio pristatymo sandėlis**. 

PU apdorojus produkto gavimą, PU būsena nustatoma kaip **Gauta**, siekiant nurodyti, kad galima apdoroti užsakymo SF. Galite peržiūrėti informaciją apie jau gautus produktus puslapyje **Produktų gavimo žurnalai**.  

Šį puslapį galite daryti iš puslapio **Pirkimo užsakymas** veiksmų grupės **Gavimas**. Žurnalų informacija apima informaciją apie kiekius, datas ir dimensijas.

<a name="additional-resources"></a>Papildomi ištekliai
--------

[Pirkimo užsakymo apžvalga](purchase-order-overview.md)

[Pirkimo užsakymo kūrimas](purchase-order-creation.md)

[Pirkimo užsakymo patvirtinimas](purchase-order-approval-confirmation.md)

[Tiekėjo SF apžvalga](../../financials/accounts-payable/vendor-invoices-overview.md)



