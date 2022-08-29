---
title: Tiekėjo PVM registro data
description: Šiame straipsnyje pateikiama informacija apie funkciją tiekėjo PVM registro įgalinimo datai
author: AdamTrukawka
ms.date: 01/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: global
ms.author: atrukawk
ms.search.validFrom: 2022-01-15
ms.dyn365.ops.version: AX 10.0.24
ms.custom: intro-internal
ms.openlocfilehash: 4af770427f5b19eaf2a129b26d54aeacc6c2f148
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278285"
---
# <a name="date-of-vendor-vat-register"></a>Tiekėjo PVM registro data

Microsoft Dynamics 365 10.0.24 **finansų** versijoje tiekėjo SF galima naudoti naują tiekėjo PVM registro lauko datą. Šis laukas nurodo apmokestinamo pirkimo tiekimo datą.

Norėdami įgalinti naują lauką, **eikite** į funkcijų valdymo darbo sritį, **suraskite** ir pasirinkite funkciją Įgalinti tiekėjo PVM registro datą tiekėjo SF, tada dabar **pasirinkite Įgalinti**.

Iš tiekėjų gaunamos SF gali būti dviejų datų: data, kai tiekėjas išdavė SF, ir apmokestinamo tiekimo data (tai yra data, kai tiekėjas išdavė mokėtiną pridėtinės vertės mokestį [PVM). Kai kuriuose scenarijuose šios dvi datos gali skirtis.

Galite atskaičiuoti gaunamą PVM sumą pirkimo SF ir įtraukti tą SF į PVM ataskaitas vėliau, tą dieną, kuri skiriasi nuo anksčiau paminėtų datų. Šią datą kontroliuoja vietos įstatymų taisyklės dėl kai kurių scenarijų atidėto gaunamo PVM atskaitymo. Skiriasi pagal šalį arba regioną.

Kai kurios PVM ataskaitos, pavyzdžiui [, PVM](emea-cze-vat-declaration-tax-declaration-model.md#vat-control-statement) kontrolės išrašo ataskaita Čekijos Respublika, reikalauja, kad būtų pranešama pirkimo dokumento apmokestinamo tiekimo data. Ši data turi būti paskelbta taip, kad mokesčių inspekcija galėtų suderinti PVM ataskaitas tarp kitų šalių.

Finansuose galite nurodyti datas toliau esančiuose laukuose:

- **SF data** – data, kada tiekėjas išdavė SF.
- **PVM registro data** – pirkimo SF PVM sumos atskaitymo data.
- **Tiekėjo PVM registro data** – tiekėjo apmokestinamo tiekimo data.
- **Gavimo dokumento data** – data, kai gavote SF.

Šie laukai yra įtraukti į šiuos puslapius:

- Tiekėjo SF
- Tiekėjo SF registras
- Tiekėjo SF patvirtinimas
- Tiekėjo SF žurnalas

Užregistrę tiekėjo SF, galite peržiūrėti datas SF žurnalo **ir** tiekėjo **operacijų** puslapiuose.
