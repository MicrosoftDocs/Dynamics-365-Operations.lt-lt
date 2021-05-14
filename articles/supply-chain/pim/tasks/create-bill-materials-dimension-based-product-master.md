---
title: Dimensijomis paremto bendrojo produkto komplektavimo specifikacijos kūrimas
description: Norėdami atlikti šią procedūrą, turite būti atlikę ankstesnius 4 šios aštuonių įrašų sekos vadovus.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920710"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Dimensijomis paremto bendrojo produkto komplektavimo specifikacijos kūrimas

[!include [banner](../../includes/banner.md)]

Norėdami atlikti šią procedūrą, turite būti atlikę ankstesnius 4 šios aštuonių įrašų sekos vadovus. Pirmaisiais 4 įrašais nustatomi duomenys, kurių reikia norint atlikti šią procedūrą. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Šią užduotį paprastai atlieka produkto kūrėjas.

## <a name="select-the-product"></a>Produkto pasirinkimas

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Sąraše pažymėkite pasirinktą eilutę.
    * Raskite išleistą bendrąjį produktą su konfigūravimo pagal dimensijas technologija, kurį sukūrėte pirmajame šios sekos užduočių vadove.  
1. Veiksmų srityje pasirinkite **Inžinierius**.
1. Pasirinkti **BOM versijas**.

## <a name="create-new-bom-and-bom-version"></a>Naujos KS ir KS versijos kūrimas

1. Pasirinkite **Naujas**.
1. Pasirinkite **BOM ir BOM** versiją.
1. Lauke **Pavadinimas** įveskite reikšmę.
    * Vietos nustatymas  
    * Atlikdami šią procedūrą konkrečios KS vietos nenustatome.  
1. Pasirinkite **Gerai**.
1. Pasirinkite **Naujas**.
    * Atlikdami šią procedūrą, į KS įtrauksime keturias eilutes. Dviejose eilutėse nurodomos laidų parinktys ir dviejose eilutėse nurodomos spintelių parinktys.  
1. Sąraše pažymėkite pasirinktą eilutę.
1. Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.
    * Pasirinkite prekės numerį A0001, HDMI 6 pėd. laidai.  
1. Lauke **Konfigūracijos grupė** įveskite arba pasirinkite reikšmę.
    * Pasirinkite laido konfigūracijos grupę, sukurtą 4-ajame šios sekos vadove.  
1. Pasirinkite **Naujas**.
    * Pasirinkite prekės numerį A0002, HDMI 12 pėd. laidai.  
1. Sąraše pažymėkite pasirinktą eilutę.
1. Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.
1. Lauke **Konfigūracijos grupė** įveskite arba pasirinkite reikšmę.
    * Vėl pasirinkite laido konfigūracijos grupę.  
1. Pasirinkite **Naujas**.
1. Sąraše pažymėkite pasirinktą eilutę.
1. Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.
    * Pasirinkite prekės numerį D0002 Spintelė.  
1. Lauke **Konfigūracijos grupė** įveskite arba pasirinkite reikšmę.
    * Pasirinkite spintos konfigūracijos grupę šiai BOM eilutei.  
1. Pasirinkite **Naujas**.
1. Sąraše pažymėkite pasirinktą eilutę.
1. Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.
    * Kaip paskutinę KS eilutę pasirinkite prekės numerį M0007 StandartinėSpintelė.  
1. Lauke **Konfigūracijos grupė** įveskite arba pasirinkite reikšmę.
    * Pasirinkite paskutinės BOM eilutės spintelių konfigūracijos grupę.  

## <a name="approve-and-activate"></a>Patvirtinti ir aktyvinti

1. Uždarykite puslapį.
1. Pasirinkite **Patvirtinti**.
1. Lauke **Patvirtino** įveskite arba pasirinkite vertę.
1. Rinkitės *Taip* laukelyje **Ar norite patvirtinti ir medžiagų važtaraštį?**.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Aktyvinti**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]