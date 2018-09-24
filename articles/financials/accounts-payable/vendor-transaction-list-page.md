---
title: "Puslapis Tiekėjo operacijų sąrašas"
description: "Šioje temoje pateikiama informacija apie puslapį Tiekėjo operacijų sąrašas, skirtas „Microsoft Dynamics 365 for Finance and Operations“"
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: 1ef7d97f059801f2fb2c0d451546b57055208f81
ms.contentlocale: lt-lt
ms.lasthandoff: 08/31/2018

---

# <a name="vendor-transaction-list-page"></a>Puslapis Tiekėjo operacijų sąrašas

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Peržiūrėti sudengimus

Veiksmų srities skirtukas **Sudengimų peržiūra** suteikia greitą prieigą prie sudengimų retrospektyvos ir papildomos informacijos apie visą sudengimo operaciją. Taip pat galite peržiūrėti papildomas operacijas, susijusias su pasirinkta operacija, nes jos buvo įtrauktos į tą patį sudengimą arba nes jos yra mokėjimai, sukurti tame pačiame mokėjimo žurnale.

1. Pasirinkite **Mokėtinos sumos \> Visi tiekėjai**.
2. Pasirinkite operacijų turintį tiekėją, tada pasirinkite **Tiekėjas \> Operacijos**.
3. Pasirinkite operaciją, kurią norite tikrinti.
4. Veiksmų srityje pasirinkite skirtuką **Sudengimų peržiūra**.

    Atsidaro dialogo langas **Sudengimų peržiūra** ir jame rodomos pasirinktos operacijos bei visi jomis sudengti dokumentai. Šia dialogo langas panašus į sudengimo restrospektyvos rodinį, tačiau jame pateikti visi susiję dokumentai.

5. Šiame dialogo lange galite atlikti įvairias užduotis. Pasirinkite vieną arba daugiau kvitų, o tada pasirinkite vieną iš toliau nurodytų meniu.

   - **Peržiūrėti apskaitą** – rodomi visi su pasirinktu dokumentu susiję kvitai. Pasirinkite **Uždaryti** norėdami uždaryti dialogo langą.
   - **Eksportuoti** – eksportuokite pasirinktus kvitus į „Microsoft Excel“.
   - **Peržiūrėti susijusius mokėjimus** – rodomos visos mokėjimų žurnalo operacijos, sukurtos mokėjimo žurnale, kuris susijęs su pasirinktu dokumentu. Be to, rodomi visi sudengimai, susiję su tais mokėjimais. Taip pat šio meniu žymė pasikeičia į **Sudengimų peržiūra**. Pasirinkite **Sudengimų peržiūra**, kad būtų rodomos tik operacijos, kurios buvo rodomos, kai pirmą kartą atidarėte dialogo langą **Sudengimų peržiūra**.
    - **Operacijų sudengimas** – šis meniu rodomas, jei pradinis pasirinktas dokumentas nebuvo visiškai sudengtas. Jį pasirinkus pasirodo dialogo langas **Operacijų sudengimas**, kuriame galite pasirinkti sudengimo operacijas.
    - **Sudengimų anuliavimas** – šis meniu rodomas, jei pradinis pasirinktas dokumentas buvo visiškai sudengtas. Jį pasirinkus pasirodo dialogo langas **Sudengimų anuliavimas**, kuriame galite atšaukti atliktus to dokumento sudengimus.

