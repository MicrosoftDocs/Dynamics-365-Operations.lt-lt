---
title: Pavojingų medžiagų apžvalga
description: Šioje temoje pateikiama funkcijų, susijusių su pavojingų medžiagų tvarkymu ir fiksavimu produkto informacijos valdymo ir sandėlio valdymo metu, apžvalga.
author: dasani-madipalli
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 15edf61cba03a57b9b4d2c939228fd064b797942
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829383"
---
# <a name="hazardous-materials-overview"></a>Pavojingų medžiagų apžvalga

[!include [banner](../includes/banner.md)]

Jog atitiktų siuntimo ir transportavimo nuostatas, organizacijos, siunčiančios medžiagas, klasifikuojamas kaip pavojingos prekės, į savo siuntas privalo įtraukti papildomus popierinius dokumentus. Pavojingų medžiagų funkcija leidžia klientams saugoti informaciją, susijusią su paleistomis prekėmis. Ši informacija gali būti naudojama ruošiant siuntimo dokumentus. Organizacija, siunčianti pavojingas prekes, privalo turėti savo siuntimo proceso valdymo procesus ir procedūras. „Microsoft Dynamics 365 Supply Chain Management” yra tik įrankis, galintis padėti generuoti reikalingus dokumentus.

Ši diagrama iliustruoja veiksmus, reikalingus pavojingų medžiagų funkcijos nustatymui ir naudojimui.

![Pavojingų medžiagos funkcijos nustatymas ir naudojimas](media/hazmat-overview.png "Pavojingų medžiagų funkcijos nustatymas ir naudojimas")

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

Daugiau informacijos apie tai, kaip nustatyti pavojingų medžiagų nuostatas ir reikšmes ir kaip priskirti reikšmes atitinkamiems produktams, žr. šias temas:

- [Pavojingų medžiagų nustatymas](hazmat-setup.md)
- [Pavojingos medžiagos produktuose, siuntose ir kroviniuose](hazmat-items.md)

## <a name="warehouse-management"></a>Sandėlio valdymas

Kai ruošite siuntą Sandėlio valdyme, galėsite atspausdinti kelias naujas ataskaitas, naudojančias informaciją, kurią nustatėte Produkto informacijos valdyme. Norėdami gauti daugiau informacijos apie galimas ataskaitas ir kaip jas naudoti, žr. [Pavojingų medžiagų užklausos ir ataskaitos](hazmat-reports.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]