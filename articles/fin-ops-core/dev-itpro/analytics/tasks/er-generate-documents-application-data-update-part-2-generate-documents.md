---
title: Konfigūracijų, skirtų generuoti dokumentus, kuriuose yra prašymų duomenys, kūrimas
description: Šiame straipsnyje aprašoma, kaip sukurti elektroninių ataskaitų (ER) konfigūracijas, kad būtų galima sugeneruoti elektroninį dokumentą. (1 dalis – konfigūracijų importavimas).
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8494f54c6f84e63e75469aa9d80d090c050b0f7f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290551"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a>Konfigūracijų, skirtų generuoti dokumentus, kuriuose yra prašymų duomenys, kūrimas

[!include [banner](../../includes/banner.md)]

Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (1 dalis – importuoti konfigūracijas)“.



Veiksmai šioje procedūroje paaiškina, kaip kurti elektroninių ataskaitų (ER) konfigūraciją, norint generuoti elektroninį dokumentą. Šios procedūros metu vykdoma ER importuota formato konfigūracija, sukurta pavyzdinei įmonei „Litware, Inc.“, kad būtų galima generuoti elektroninius dokumentus.



Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo. Šiuos veiksmus galima atlikti naudojant DEMF duomenų rinkinį. 



Prieš pradėdami pakeisti šalies kontekstą DEMF įmonei iš DEU (Vokietija) į BEL (Belgija). Spustelėkite Organizacijos administravimas > Organizacijos > Juridiniai subjektai, kad atnaujintumėte šalies kodą juridinio subjekto DEMF pagrindiniame adrese. Paleiskite programą iš naujo.


## <a name="run-imported-er-format"></a>Paleiskite importuotą ER formatą
1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
2. Medyje išplėskite „Intrastat (model)“.
3. Medyje pasirinkite „Intrastat (model)\Intrastat (format)“.
4. Spustelėkite Vykdyti.
    * Paleiskite ER formato konfigūracijos juodraščio versiją, norėdami generuoti Intrastat ataskaitą.  
5. Lauke Įveskite failo pavadinimą įveskite „intrastat.xml“.
    * Nurodykite failo vardą.  
6. Spustelėkite GERAI.
    * Peržiūrėkite sugeneruotą XML failą.  
7. Uždarykite puslapį.
8. Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.
    * Atidarykite šią formą, kad peržiūrėtumėte Intrastat operacijas, kurios yra įtrauktos sugeneruotą elektroninį dokumentą.  
9. Spustelėkite Intrastat archyvas.
    * Kadangi įvykdytame ER formate nėra jokių programos duomenų atnaujinimo parametrų, informacija apie užpildytą Intrastat ataskaitą nesuarchyvuota.  
10. Uždarykite puslapį.
11. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
