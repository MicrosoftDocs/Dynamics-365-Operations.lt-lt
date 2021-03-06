---
title: Sistemos administratoriai negali išvalyti užsakymų sulaikymas, nes jie nėra įgalioti
description: Sistemos administratoriai negali išvalyti užsakymų sulaikymas, nes jie nėra įgalioti.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026762"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a>Sistemos administratoriai negali išvalyti užsakymų sulaikymas, nes jie nėra įgalioti

KB numeris: 4614642

## <a name="symptoms"></a>Požymiai

Sistemos administratoriai gali išvalyti pardavimo užsakymų sulaikymas, nebent jie turi tam tikrą vaidmenį, kuris priskirtas užsakymo laikymo kodui.

## <a name="resolution"></a>Skiriamoji geba

Prieigą prie kai kurių operacijų, pvz., tarpuskaitos pardavimo užsakymų, lemia verslo strategijos nustatymas. Paprastai sistemos administratoriams neleidžiama atlikti šio tipo operacijų. 

Dažniausiai prieigą atlikti tam tikrą užduotį valdo verslo strategijos, ir tik konkretūs organizacijos asmenys patvirtinami tai užduočiai atlikti. Pavyzdžiai apima patvirtinimus, kurie yra darbo eigos patvirtinimų rezultatas ir konkrečios užduotys, kurios yra darbo eigos konfigūracijos rezultatas.

Nors darbo eiga nėra susieta su užsakymų sulaikyme, principas panašus. Atitinkamas vaidmuo nurodo tam tikrą organizacijos žmonių grupę, kuri turi teisę išvalyti užsakymų sulaikymas. Ši teisė nebūtinai turi būti suteikta visiems administratoriams, nes šis būdas pažeidžia nustatytą verslo strategiją.
