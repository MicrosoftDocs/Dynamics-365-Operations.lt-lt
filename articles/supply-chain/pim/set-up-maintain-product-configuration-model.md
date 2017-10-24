---
title: "Produkto konfigūracijos modelio nustatymas"
description: "Šiame straipsnyje aprašomi produkto konfigūracijos modelio nustatymo ir kūrimo veiksmai."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 4051
ms.assetid: 00df5537-b148-4e32-a248-3e35876ad4e1
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dd4346f8b2f253721df23fbcff71e3a0e78bb2cc
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-a-product-configuration-model"></a>Produkto konfigūracijos modelio nustatymas

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašomi produkto konfigūracijos modelio nustatymo ir kūrimo veiksmai.

| Užduotis                                                        | aprašymas                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bendrojo produkto kūrimas.                                    | Kurti bendrąjį produktą iš sąrašo **Bendrasis produktas**. Išleiskite bendrąjį produktą į visas susijusias įmones. Kaip bendrojo produkto, kuris naudojamas kaip produkto konfigūracijos modelio arba subkomponento versija, konfigūracijos technologiją būtina pasirinkti **Konfigūravimas pagal apribojimus**, o konfigūracijos dimensiją reikia pasirinkti tik produkto dimensijų grupei. |
| Komponentų kūrimas.                                          | Komponentus kurkite puslapyje **Komponentai**. Komponentai yra produkto konfigūracijos modelio kūrimo blokai ir juos galima pakartotinai naudoti keliuose produktų konfigūravimo modeliuose.                                                                                                                                                                                                                      |
| Atributų tipų kūrimas.                                     | Atributų tipus kurkite puslapyje **Atributų tipai**. Atributų tipai nustato visų atributų, kurie naudojami produkto konfigūracijos modeliuose, duomenų tipų rinkinius. **Bulio logikos**, **teksto** su fiksuotu sąrašu ir **sveikųjų skaičių** su diapazonu tipų atributuose išvardytos reikšmės, galimos konfigūruojant produkto variantą pagal produktų konfigūravimo modelį.       |
| Produkto konfigūracijos modelio kūrimas.                       | Kurkite produkto konfigūracijos modelį puslapyje **Naujas produkto konfigūracijos modelis**.                                                                                                                                                                                                                                                                                                              |
| Atributų įtraukimas į produkto konfigūracijos modelį.            | Sukurkite atributą puslapio **Produkto konfigūravimo pagal apribojimus modelio informacija** „FastTab“ skirtuke **Atributai**. Atributais vadinamos produkto konfigūracijos modelio funkcijos.                                                                                                                                                                                                       |
| Apribojimų įtraukimas į produkto konfigūracijos modelį.           | Sukurkite apribojimus puslapio **Produkto konfigūravimo pagal apribojimus modelio informacija** „FastTab“ skirtuke **Apribojimai**. Apribojimai yra apribojimai, kuriuos turi atitikti produkto konfigūracija. Apribojimai yra išraiškos arba lentelės apribojimai.                                                                                                                                 |
| Subkomponentų įtraukimas į produktų konfigūravimo modelį.         | Sukurkite subkomponentus puslapio **Produkto konfigūravimo pagal apribojimus modelio informacija** „FastTab“ skirtuke **Subkomponentai**. Subkomponentai yra susiję su komponentais ir yra susieti su prekėmis, atitinkančiomis subkomponentą.                                                                                                                                                                       |
| Vartotojo reikalavimų įtraukimas į produktų konfigūravimo modelį.     | Vartotojo reikalavimai yra panašūs į subkomponentus, bet jie nesusiejami su prekėmis. Apie vartotojo reikalavimus galite galvoti kaip apie fiktyvią KS. Visos KS eilutės arba maršruto operacijos, esančios tiesiogiai dalyje vartotojo reikalavimas, bus sutrauktos į pagrindinį komponentą.                                                                                                                       |
| KS eilučių įtraukimas į produkto konfigūracijos modelį.             | Sukurkite KS eilutes puslapio **Produkto konfigūravimo pagal apribojimus modelio informacija** „FastTab“ skirtuke **KS eilutės**. KS eilutės atitinka dalį, būtiną norint sukurti produkto variantą.                                                                                                                                                                                                 |
| Maršruto operacijų įtraukimas į produktų konfigūravimo modelį.      | Sukurkite maršruto operacijas puslapio **Produkto konfigūravimo pagal apribojimus modelio informacija** „FastTab“ skirtuke **Maršruto operacijos**. Maršruto operacijos atitinka veiksmų sekos veiksmą, atliekamą siekiant sukurti produkto variantą.                                                                                                                                                    |
| Produkto konfigūracijos modelio aktyvios versijos kūrimas. | Sukurkite produkto konfigūracijos modelio aktyvią versiją puslapyje **Versijos**. Versija yra ryšys tarp produkto konfigūracijos modelio ir bendrojo produkto. Produkto konfigūracijos modelis, turintis aktyvią versiją, gali būti konfigūruojamas naudojant pardavimo užsakymą, pardavimo pasiūlymą, pirkimo užsakymą arba gamybos užsakymą.                                                               |
| Produkto konfigūracijos modelio tikrinimas.                         | Tikrinkite produkto konfigūracijos modelį puslapyje **Produkto konfigūravimo pagal apribojimus modelio informacija** arba **Produkto konfigūracijos modelių sąrašas**. Produkto konfigūracijos modelio tikrinimo procedūra imituoja produkto modelio konfigūracijos procesą, vykstantį tvarkant užsakymus.                                                                                                |
| Produkto konfigūracijos modelio šablonų kūrimas.                | Kurkite produkto konfigūracijos modelio šabloną puslapyje **Konfigūravimo šablonai**. Konfigūravimo šablone yra produktų konfigūravimo modelio atributų vertės. Atributo vertes pasirinkite puslapyje **Konfigūruoti eilutę**. Galite pasirinkti įkelti produkto modelio konfigūravimo šabloną atlikdami produkto modelio konfigūravimą.                                                   |
| Prekės konfigūravimas.                                          | Produkto konfigūracijos modeliai gali būti konfigūruojami naudojant pardavimo užsakymą, pardavimo pasiūlymą, pirkimo užsakymą arba gamybos užsakymą.                                                                                                                                                                                                                                                                           |






