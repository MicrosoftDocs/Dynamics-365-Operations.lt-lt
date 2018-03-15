---
title: "Konfigūracijos taisyklės"
description: "Šiame straipsnyje pateikiama bendra informacija apie konfigūravimo taisykles. Konfigūravimo taisyklėmis apibrėžiami ryšiai tarp komplektavimo specifikacijos (KS) produktų, kurie naudoja konfigūravimo pagal dimensijas technologiją."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: bc8e606cdc0bc5a45321c67ce9b089059f226df2
ms.contentlocale: lt-lt
ms.lasthandoff: 02/07/2018

---

# <a name="configuration-rules"></a>Konfigūracijos taisyklės

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikiama bendra informacija apie konfigūravimo taisykles. Konfigūravimo taisyklėmis apibrėžiami ryšiai tarp komplektavimo specifikacijos (KS) produktų, kurie naudoja konfigūravimo pagal dimensijas technologiją.

Konfigūracijos taisyklės galimos nurodžius konfigūravimą pagal dimensijas. Konfigūracijos taisyklės naudojamos komplektavimo specifikacijoje (KS) įgalinti arba uždrausti konkrečias prekių kombinacijas. Sukūrus KS ir atitinkamas prekes priskyrus jų atitinkamoms konfigūracijos grupėms, galima nustatyti vieną ar daugiau konfigūracijos taisyklių. Jei dvi prekės susijusios viena su kita, siekiant užtikrinti įtraukimą naudojamas operatorius **Pasirinkti**. Jei dvi prekės yra nesuderinamos, siekiant užtikrinti neįtraukimą naudojamas operatorius **Atsisakyti pasirinkimo**.  

**Pastaba.** Ši informacija taikoma tik bendriesiems produktams, kuriuose naudojama konfigūravimo pagal dimensijas technologija.  

Vėliau pakeistos konfigūracijos taisyklės neturi įtakos esamoms konfigūracijoms. Kita vertus, svarbu, kad taisykles nustatytumėte prieš nustatydami konfigūraciją ir patikrintumėte taisykles, jei manote, kad jos galėjo būti pakeistos.  

**Pastaba.** Taikant metodą **Pasirinkti** išvestinės konfigūracijos grupė, prekės numeris ir konfigūracija pasirenkami automatiškai. Taikant metodą **Atsisakyti pasirinkimo** išvestinės konfigūracijos grupės, prekės numerio ir konfigūracijos pasirinkti negalima.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Produktų konfigūravimas pagal dimensijas](dimension-based-product-configuration.md)




