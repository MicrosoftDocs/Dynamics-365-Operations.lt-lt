---
title: Sukonfigūruotų produkto variantų produkto numerių nomenklatūros kūrimas
description: Šioje procedūroje parodoma, kaip nustatyti sukonfigūruotų produkto variantų produkto numerių nomenklatūrą ir kaip ją galima pridėti prie konfigūruojamo bendrojo produkto.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: da52385f60b2522cf358e0ceb70448479a1e5dc714ef15ba361611ed404ed852
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726830"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>Sukonfigūruotų produkto variantų produkto numerių nomenklatūros kūrimas

[!include [banner](../../includes/banner.md)]

Šioje procedūroje parodoma, kaip nustatyti sukonfigūruotų produkto variantų produkto numerių nomenklatūrą ir kaip ją galima pridėti prie konfigūruojamo bendrojo produkto. Šioje procedūroje taip pat parodoma, kaip galima kurti konfigūravimo nomenklatūrą, skirtą produkto konfigūravimo modelio komponentui. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Nauja produkto numerių nomenklatūrą yra priskiriama bendrajam produktui D0004. Paprastai šią užduotį atlieka produkto kūrėjas.

## <a name="create-a-product-number-nomenclature"></a>Produkto numerių nomenklatūros kūrimas

1. Eikite į **Produkto informacijos valdymas \> Nustatymas \> Bendroji nomenklatūra**.
1. Pasirinkite **Naujas**.
1. Lauke **Pavadinimas** įveskite reikšmę.
1. Lauke **Aprašo laukas** surinkite reikšmę.
1. Pasirinkite **Įtraukti**.
1. Pažymėkite **Produkto pagrindinį** numerį.
1. Pasirinkite **Įtraukti**.
1. Pažymėkite **Teksto konstanta**.
1. Sąraše pažymėkite pasirinktą eilutę.
1. Lauke **Tekstas** įveskite reikšmę.
1. Pasirinkite **Įtraukti**.
1. Pasirinkti **konfigūraciją**.
1. Uždarykite puslapį.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>Produkto numerių nomenklatūros priskyrimas bendrajam produktui

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Bendrieji produktai**.
1. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką **Produkto numeris** naudodami reikšmę D.
1. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.
1. Pasirinkite **Redaguoti**.
1. Pažymėkite *Taip* lauke **Naudoti nomenklatūrą**.
1. Lauke **Produkto varianto numerio nomenklatūra** įveskite arba pažymėkite reikšmę.
1. Uždarykite puslapį.
1. Uždarykite puslapį.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Produkto konfigūracijos modelio komponento nomenklatūros kūrimas

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Produkto konfigūracijos modeliai**.
1. Sąraše raskite ir pasirinkite norimą įrašą.
1. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.
1. Pasirinkite **Redaguoti**.
1. Lauke *Naudoti* onfigūracijos nomenklatūrą pasirinkite **Taip** .
1. Pasirinkite **Įtraukti**.
1. Rinkitės **Atributo vertė**.
1. Sąraše pažymėkite pasirinktą eilutę.
1. Lauke **Atributas** įveskite arba pasirinkite reikšmę.
1. Pasirinkite **Įtraukti**.
1. Pažymėkite **Teksto konstanta**.
1. Sąraše pažymėkite pasirinktą eilutę.
1. Lauke **Tekstas** įveskite reikšmę.
1. Pasirinkite **Įtraukti**.
1. Rinkitės **Atributo vertė**.
1. Sąraše pažymėkite pasirinktą eilutę.
1. Lauke **Atributas** įveskite arba pasirinkite reikšmę.
1. Pasirinkite **Įtraukti**.
1. Pažymėkite **Teksto konstanta**.
1. Sąraše pažymėkite pasirinktą eilutę.
1. Lauke **Tekstas** įveskite reikšmę.
1. Pasirinkite **Įtraukti**.
1. Rinkitės **Atributo vertė**.
1. Sąraše pažymėkite pasirinktą eilutę.
1. Lauke **Atributas** įveskite arba pasirinkite reikšmę.
1. Pasirinkite **Įtraukti**.
1. Pažymėkite **Teksto konstanta**.
1. Sąraše pažymėkite pasirinktą eilutę.
1. Lauke **Tekstas** įveskite reikšmę.
1. Pasirinkite **Įtraukti**.
1. Rinkitės **Atributo vertė**.
1. Sąraše pažymėkite pasirinktą eilutę.
1. Lauke **Atributas** įveskite arba pasirinkite reikšmę.
1. Pasirinkite **Įtraukti**.
1. Pažymėkite **Teksto konstanta**.
1. Sąraše pažymėkite pasirinktą eilutę.
1. Lauke **Tekstas** įveskite reikšmę.
1. Pasirinkite **Įtraukti**.
1. Pasirinkite **Numeravimo sekos vertę**.
1. Sąraše pažymėkite pasirinktą eilutę.
1. Lauke **Numeravimo seka** įveskite arba pasirinkite reikšmę.
1. Uždarykite puslapį.
1. Uždarykite puslapį.
1. Uždarykite puslapį.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]