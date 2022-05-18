---
title: Pusmečio nusidėvėjimo konvencijos metodika
description: Šioje temoje aprašomas metodas, kurį ilgalaikis turtas naudoja nusidėvėjimui apskaičiuoti pagal pusmečio konvenciją, apskaičiuojančią šešių mėnesių nusidėvėjimą per pirmuosius ir paskutiniuosius metus, kai turtas eksploatuojamas.
author: moaamer
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: fb15a293bb8cec1b4faba7bcbd29eb4df7916786
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/06/2022
ms.locfileid: "8720398"
---
# <a name="half-year-depreciation-convention-methodology"></a>Pusmečio nusidėvėjimo konvencijos metodika

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje aprašomas ilgalaikio turto metodas, naudojamas norint apskaičiuoti nusidėvėjimą naudojant pusmečio konvenciją. Pusmečio konvencija apskaičiuoja šešių mėnesių nusidėvėjimą per pirmuosius ir paskutiniuosius metus, kai turtas eksploatuojamas. Daugiau informacijos apie nusidėvėjimo konvencijas žr. [Nusidėvėjimo metodai ir konvencijos](Fixed-asset-depreciation-conventions.md). 

Naudojant šešių mėnesių nusidėvėjimo konvenciją, sistema naudoja įsigijimo metus arba metus, kuriais turtas buvo atiduotas eksploatuoti, tada apskaičiuoja penkerių metų nusidėvėjimą nuo tų metų ir prideda šešis mėnesius. Norėdami iliustruoti šį procesą, įsivaizduokite turtą, kuris buvo įsigytas už 50 000 ir atiduotas eksploatuoti 2020 m. balandžio mėn. Tarkime, kad turto dėvėjimo laikas yra penkeri metai.

Pirmieji eksploatavimo metai pasibaigs 2020 m. gruodžio mėn., o tai reiškia, kad turto penkerių metų dėvėjimo laikas pasibaigs 2024 m. gruodžio mėn. Pusmečio nusidėvėjimo konvencija pridės šešis mėnesius prie turto dėvėjimo laiko, o tai reiškia, kad jo dėvėjimo laikas pasibaigs 2025 m. birželio mėn. 

> Metinis nusidėvėjimas: 50 000 / 5 = 10 000, mėnesinis nusidėvėjimas: 10 000 / 12 = 833,33 <br>
> Pirmųjų metų nusidėvėjimas: 10 000 / 2 = 5 000, vėlesnis mėnesinis nusidėvėjimas: 5 000 / 9 = 555,56

   [![Pusmečio nusidėvėjimo konvencijos nusidėvėjimo grafikas.](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)

Išplėsti nusidėvėjimo laikotarpiai, kuriuos pradeda pusmečio konvencija, leidžia tiksliau paskirstyti nusidėvėjimą. Šešių mėnesių konvencija tolygiai nurodo nusidėvėjimo išlaidas, o tai naudinga pelno ir nuostolio išrašo ataskaitose.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
