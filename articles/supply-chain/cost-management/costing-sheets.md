---
title: Įkainojimo lapai
description: Įkainojimo lapo nustatymas apima du tikslus. Pirmasis tikslas yra apibrėžti informacijos rodymo formatą parduotų prekių savikainai, informacijai apie pagamintą prekę ar gamybos užsakymui. Suformatuotas rodinys vadinamas įkainojimo lapu. Antrasis tikslas yra apibrėžti netiesioginių išlaidų apskaičiavimo pagrindą. Įkainojimo lapo nustatymas pagrįstas išlaidų grupės funkcija informacijai rodyti ir netiesioginių išlaidų skaičiavimo formulėms. Šiame straipsnyje aprašomi du įkainojimo lapo nustatymo tikslai.
author: AndersGirke
ms.date: 11/18/2021
ms.topic: article
ms.search.form: CostSheetDesigner, CostSheetCalculationFactor
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53201
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64b8a9b8b29193f25e706e52424de2af3454aec8
ms.sourcegitcommit: f11ad8d7ee8a4d2ee1a1bb601622b50e14955c4a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/18/2021
ms.locfileid: "7825363"
---
# <a name="costing-sheets"></a>Įkainojimo lapai

[!include [banner](../includes/banner.md)]

Įkainojimo lapo nustatymas apima du tikslus. Pirmasis tikslas yra apibrėžti informacijos rodymo formatą parduotų prekių savikainai, informacijai apie pagamintą prekę ar gamybos užsakymui. Suformatuotas rodinys vadinamas įkainojimo lapu. Antrasis tikslas yra apibrėžti netiesioginių išlaidų apskaičiavimo pagrindą. Įkainojimo lapo nustatymas pagrįstas išlaidų grupės funkcija informacijai rodyti ir netiesioginių išlaidų skaičiavimo formulėms. Šiame straipsnyje aprašomi du įkainojimo lapo nustatymo tikslai. 

Šioje lentelėje išvardijimo ne programos saugos vaidmenys, kurie gali pasiekti įkainojimo lapus, įskaitant prieigos prie kiekvieno vaidmens lygį pagal numatytuosius parametrus.

| Vaidmuo | Prieiga
|---|---|
| Apskaitos vadovas | Redagavimas |
| Atsargų apskaitos buhalteris | Peržiūrėti |
| Atsargų apskaitininkas | Peržiūrėti |

Įkainojimo lapas yra suformatuotas informacijos apie parduotų gaminamos prekės arba gamybos užsakymo prekių savikainą rodinys. Kai nustatote įkainojimo lapą, nurodote informacijos formatą ir apibrėžiate netiesioginių išlaidų skaičiavimo pagrindą. Įkainojimo lapo nustatymas pagrįstas išlaidų grupės funkcijomis informacijai rodyti ir netiesioginių išlaidų skaičiavimo formulėms. Toliau pateikiama daugiau informacijos apie du įkainojimo lapo nustatymo tikslus.

- **Apibrėžti įkainojimo lapo formatą.** Vartotojo apibrėžiamas išlaidų lapo formatas nustato išlaidų, kurias sudaro pagamintos prekės parduotų prekių savikaina, segmentavimą. Pavyzdžiui, informaciją apie prekės parduotų prekių savikainą galima segmentuoti į medžiagą, darbą ir pridėtines išlaidas pagal išlaidų grupes. Šios išlaidų grupės yra priskiriamos prekėms, išlaidų kategorijoms nukreipimo operacijoms ir netiesioginių išlaidų apskaičiavimo formulėms. Įkainojimo lapo formatui paprastai reikia tarpinių sumų, kai norima apibrėžti keletą išlaidų grupių. Pavyzdžiui, galima agreguoti keletą išlaidų grupių, kurios susijusios su medžiaga. Išlaidų lapo formato apibrėžimas yra laisvai pasirenkamas, tačiau išlaidų lapo formatas turi būti apibrėžtas, jei skaičiuojamos netiesioginės išlaidos.
- **Aprašykite netiesioginių išlaidų apskaičiavimo pagrindą.** Netiesioginės išlaidos atspindi pridėtines gamybos išlaidas, susijusias su pagamintos prekės gamyba. Netiesioginių išlaidų skaičiavimo formulė gali būti išreikšta kaip papildomas mokestis arba tarifas. Papildomas mokestis pateikiamas vertės procentu, o tarifas yra suma per nukreipimo operacijos valandą. Išlaidų grupė apibrėžia skaičiavimo formulės pagrindą, pvz., 100 % papildomas darbo išlaidų grupės išlaidas arba 50,00 USD mašinų išlaidų grupės valandinį tarifą. Siekiant apibrėžti skaičiavimo formulę ir jos išlaidų grupės pagrindą, norint nustatyti išlaidų lapą būtina identifikuoti išlaidų grupę, kuri nurodo pridėtines išlaidas, ir pasirinkti naudoti papildomo mokesčio arba tarifo metodą.

Kiekviena skaičiavimo formulė turi būti įvesta kaip išlaidų įrašas. Išlaidų įrašą sudaro nustatyta įkainojimo versija, papildomo mokesčio procentas arba tarifo suma, išlaidų grupės pagrindas, būsena ir galiojimo data. Kai pirmą kartą įvedamas išlaidų įrašas, jo būsena yra **Laukiantis** ir jis turi įsigaliojimo datą. Kai išlaidų įrašą suaktyvinate, būsena atnaujinama ir įrašas būna dabartinis aktyvus įrašas, o įsigaliojimo data atnaujinama į aktyvinimo datą. Išlaidų įrašas taip pat gali nurodyti konkrečios teritorijos skaičiavimo formulės teritoriją. Taip pat lauką **Teritorija** galite palikti tuščią, jei norite nurodyti, kad skaičiavimo formulė yra visos įmonės formulė. Išlaidų įrašą pasirinktinai gali sudaryti nustatyta prekė arba prekių grupė, kai skaičiavimo formulė pažymėta kaip formulė, skirta vienai prekei. 

Šiuo metu aktyvūs išlaidų įrašai netiesioginių išlaidų skaičiavimo formulėse naudojami gamybos užsakymo išlaidoms įvertinti. Jie taip pat naudojami skaičiuojant faktines išlaidas, susijusias su faktiniu laiko ir medžiagų suvartojimu. Laukiančių išlaidų įrašai naudojami būsimiems komplektavimo specifikacijų (KS) skaičiavimams. 

Dvi išlaidų versijos blokavimo strategijos nustato, ar laukiančios išlaidos gali būti tvarkomos ir ar galima pradėti laukiančias išlaidas. Norėdami leisti tvarkyti duomenis, o vėliau neleisti tvarkyti išlaidų duomenų įkainojimo versijoje, naudokite blokavimo strategijas. 

Apibrėžus išlaidų lapo formatą ir netiesioginių išlaidų skaičiavimus, reikia atlikti atskirą veiksmą informacijai patikrinti ir išsaugoti. Įkainojimo lapas pateikia visos įmonės formatą, skirtą nuolat rodyti parduotų prekių išlaidų informaciją. 

Įkainojimo lapas rodomas kaip puslapio **Skaičiuoti prekės savikainą** dalis. Įkainojimo lapas gali būti rodomas gaminamos prekės apskaičiuotų išlaidų įrašui puslapyje **Prekės kaina** arba konkretaus užsakymo skaičiavimo įrašui puslapyje **KS skaičiavimo rezultatai**. Taip pat jis gali būti rodomas kaip gamybos užsakymo puslapio **Kainos skaičiavimas** dalis.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
