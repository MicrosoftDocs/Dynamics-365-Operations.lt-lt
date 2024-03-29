---
title: Pavojingų medžiagų apžvalga
description: Šiame straipsnyje pateikiama priemonių, susijusių su pavojingomis medžiagomis tvarkant ir dokumentuojant produkto informacijos valdymą ir sandėlio valdymą, apžvalga.
author: t-benebo
ms.date: 06/10/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: c2cae4cb65dd163e9fbf1d24cff5a0a040e3ce3a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905811"
---
# <a name="hazardous-materials-overview"></a>Pavojingų medžiagų apžvalga

[!include [banner](../includes/banner.md)]

Jog atitiktų siuntimo ir transportavimo nuostatas, organizacijos, siunčiančios medžiagas, klasifikuojamas kaip pavojingos prekės, į savo siuntas privalo įtraukti papildomus popierinius dokumentus. Pavojingų medžiagų funkcija leidžia klientams saugoti informaciją, susijusią su paleistomis prekėmis. Ši informacija gali būti naudojama ruošiant siuntimo dokumentus. Organizacija, siunčianti pavojingas prekes, privalo turėti savo siuntimo proceso valdymo procesus ir procedūras. „Microsoft Dynamics 365 Supply Chain Management” yra tik įrankis, galintis padėti generuoti reikalingus dokumentus.

Ši diagrama iliustruoja veiksmus, reikalingus pavojingų medžiagų funkcijos nustatymui ir naudojimui.

![Pavojingų medžiagos funkcijos nustatymas ir naudojimas.](media/hazmat-overview.png "Pavojingų medžiagų funkcijos nustatymas ir naudojimas")

Pavojingų medžiagų funkcija yra nustatoma Produkto informacijos valdyme ir pateikia dokumentus, kuriuos galima atsispausdinti per Sandėlio valdymą. Taigi, apskritai kalbant, minėtos sritys yra dvi pagrindinės sritys, kuriose Jūs peržiūrėsite, nustatysite ir naudosite šią funkciją:

- **Produkto informacijos valdymas** – nustatyti kodus, kurie bus taikomi išleistam produktui.
- **Sandėlio valdymas** – darbas su papildomais dokumentais, kurie bus atspausdinti siuntoms.

> [!IMPORTANT]
> Pavojingų medžiagų funkcijos Supply Chain Management suteikia naudingų produkto informacijos laukų kolekciją ir susijusią funkciją, galinčią padėti Jums įrašyti ir nurodyti informaciją, susijusią su Jūsų pavojingais produktais. Šios funkcijos taip pat gali padėti jums kurti ir spausdinti siuntimo dokumentus, kuriuose yra tam tikra informacija apie bet kokias pavojingas medžiagas, kurias siunčiate. Tačiau sistema automatiškai neatitiks visų nuostatų, taikomų jūsų šalyje arba regione. Nors šios priemonės skirtos tam, kad būtų lengviau laikytis bendrųjų nuostatų, jos nėra pakankamos ar garantuotos tokiomis būti. Jūsų organizacija yra atsakinga už visų taikomų nuostatų žinojimą ir visų jų laikymuisi būtinų veiksmų atlikimą.

## <a name="product-information-management"></a>Produkto informacijos valdymas

Produkto informacijos valdymas pateikia nustatymo lentelių diapazoną, kuriame Jūs galite įvesti nuorodos informaciją apie įvairius pavojingų prekių sąrašus sausumos, oro ir jūros transportu.

Į šias bendrąsias nuostatas buvo atsižvelgta kuriant šią funkciją:

- **ADR** – nuostatos, susijusios su tarptautiniu pavojingų krovinių vežimu keliais
- **CFR 49** – pavojingų krovinių gabenimo Jungtinėse Valstijose nuostatos
- **IMDG** – Tarptautinis jūra gabenamų pavojingų krovinių (IMDG) kodeksas
- **IATA** – Tarptautinės oro transporto asociacijos (IATA) pavojingų prekių gabenimo nuostatos

Kiekvienas nuostatų rinkinys pateikia standartizuotus pavojingų prekių sąrašus ir nuorodų kodus. Taigi, Supply Chain Management pateikia tų sąrašų bendrųjų kodų nuorodų lentelę. Kiekvienas sąrašas turi kelius unikalius kodus, kuriuos Jūs galite apibrėžti.

Norėdami gauti daugiau informacijos apie tai, kaip nustatyti pavojingos medžiagos taisykles ir vertes, ir kaip priskirti vertes atitinkamiems produktams, žr. šiuos straipsnius:

- [Pavojingų medžiagų nustatymas](hazmat-setup.md)
- [Pavojingos medžiagos produktuose, siuntose ir kroviniuose](hazmat-items.md)

## <a name="warehouse-management"></a>Sandėlio valdymas

Kai ruošite siuntą Sandėlio valdyme, galėsite atspausdinti kelias naujas ataskaitas, naudojančias informaciją, kurią nustatėte Produkto informacijos valdyme. Norėdami gauti daugiau informacijos apie galimas ataskaitas ir kaip jas naudoti, žr. [Pavojingų medžiagų užklausos ir ataskaitos](hazmat-reports.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]