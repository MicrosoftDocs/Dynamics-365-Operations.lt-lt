---
title: "Mažmeninės prekybos kanalo fiskalinė integracija"
description: "Šioje temoje pateikta „Retail POS“ fiskalinės integracijos apžvalga."
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: lt-lt
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a>Mažmeninės prekybos kanalo fiskalinė integracija

[!include [banner](../includes/banner.md)]

Šioje temoje apžvelgiama fiskalinės integracijos funkcija, kuria galima naudotis „Microsoft Dynamics 365 for Retail“. Ši fiskalinės integracijos funkcija yra sistema, naudojama tam, kad būtų laikomasi vietos fiskalinių įstatymų, kurių tikslas – užkirsti kelią sukčiavimams mažmeninės prekybos versle. Toliau išvardijami įprasti scenarijai, kurių atveju būtų galima naudotis fiskaline integracija.

- Fiskalinio kvito spausdinimo ir jo pateikimo klientui atveju.
- Užtikrinant su naudojantis EKA atliktais pardavimais ir grąžinimais susijusios informacijos perdavimą institucijos teikiamai išorinei paslaugai.
- Naudojantis institucijos įgaliotu skaitmeniniu parašu užtikrinama duomenų apsauga.

Šioje temoje pateikiama patarimų, kaip nustatyti fiskalinę integraciją, kad vartotojai galėtų atlikti toliau nurodytas užduotis. 

- Konfigūruoti fiskalines jungtis, kurios yra fiskalinės registracijos tikslais naudojami fiskaliniai įrenginiai arba paslaugos, pvz., įrašymas, skaitmeniniai parašai ir saugus finansinių duomenų pateikimas.
- Konfigūruoti dokumentų teikėją, nuo kurio priklauso išvesties metodas ir finansinių dokumentų kūrimo algoritmas.
- Konfigūruoti fiskalinės registracijos procesą, nuo kurio priklauso veiksmų seka ir atliekant kiekvieną veiksmą naudojamų jungčių grupė.
- Priskirti fiskalinės registracijos procesus EKA funkcijų profiliams.
- Priskirti jungties techninius profilius aparatūros profiliams (vietinėms fiskalinėms jungtims) arba EKA funkcijų profiliams (kito tipo fiskalinėms jungtims).

## <a name="fiscal-integration-execution-flow"></a>Fiskalinės integracijos vykdymo eiga
Pagal toliau pateiktą scenarijų rodoma bendroji fiskalinės integracijos vykdymo eiga.

1. Fiskalinės registracijos proceso pradžia.
  
   Atlikus kai kuriuos veiksmus, kai reikia atlikti fiskalinę registraciją, pvz., užbaigus mažmeninės prekybos operaciją, fiskalinės registracijos procesas susietas su dabartiniu EKA funkcijų profiliu.

1. Suraskite fiskalinę jungtį.
   
   Sistema suranda kiekvieno į fiskalinės registracijos procesą įtraukto fiskalinės registracijos veiksmo atitikmenį fiskalinių jungčių sąraše. Konkrečioje šių jungčių grupėje įtrauktas funkcinis profilis, taip pat pateikiamas jungčių, kurių techninis profilis susietas su dabartiniu aparatūros profiliu (tik jei jungties tipas **Vietinė**) arba su dabartiniu EKA funkcijų profiliu (kito tipo jungtims).
   
1. Atlikite fiskalinę integraciją.

   Sistema vykdo visus reikiamus su surasta jungtimi susieto rinkinio nurodytus veiksmus. Tai atliekama pagal ankstesniame šios jungties veiksme rastus funkcinio profilio ir techninio profilio parametrus.

## <a name="setup-needed-before-using-fiscal-integration"></a>Prieš naudojantis fiskaline integracija būtina atlikti sąranka
Prieš naudodamiesi fiskalinės integracijos funkcija, turėtumėte nurodyti toliau išvardytus parametrus.

- Puslapyje **Mažmeninės prekybos parametrai** nurodykite fiskalinio funkcinio profilio numeraciją.
  
- Puslapyje **Bendrai naudojami mažmeninės prekybos parametrai** nurodykite toliau nurodytų elementų numeraciją.
  
  - Fiskalinio techninio profilio numeris
  - Fiskalinių jungčių grupės numeris
  - Registracijos proceso numeris

- Dalyje **Mažmeninė prekyba > Kanalų sąranka > Fiskalinė integracija > Fiskalinės jungtys** sukurkite kiekvieno įrenginio arba paslaugos, kuria planuojate naudotis fiskalinės integracijos tikslais, jungtį **Fiskalinė jungtis**.

-  Dalyje **Mažmeninė prekyba > Kanalų sąranka > Fiskalinė integracija > Fiskalinių dokumentų teikėjai** sukurkite visų fiskalinių jungčių teikėją **Fiskalinių dokumentų teikėjas**. Duomenų susiejimas laikomas fiskalinio dokumento teikėjo dalis. Norėdami nustatyti skirtingus tos pačios jungties duomenų susiejimus (pvz., nuo būsenos priklausančius reguliatorius), turėtumėte sukurti skirtingus fiskalinių dokumentų teikėjus.

- Dalyje **Mažmeninė prekyba > Kanalų sąranka > Fiskalinė integracija > Jungties funkciniai profiliai** sukurkite kiekvieno fiskalinio dokumento teikėjo profilį **Jungties funkcinis profilis**.
  - Pasirinkite jungties pavadinimą.
  - Pasirinkite dokumento teikėją.
  - Skirtuke **Paslaugos nustatymas** nurodykite PVM tarifų parametrus.
  - Skirtuke **Duomenų susiejimas** nurodykite PVM kodų susiejimą ir mokėjimo priemonės tipo susiejimą.

  #### <a name="examples"></a>Pavyzdžiai 

  |  | Formatuoti | Pavyzdys | 
  |--------|--------|--------|
  | PVM tarifų parametrai | vertė : VATrate | 1 : 2000, 2 : 1800 |
  | PVM kodų susiejimas | VATcode : vertė | vat20 : 1, vat18 : 2 |
  | Mokėjimo priemonės tipų susiejimas | TenderTyp : vertė | Grynieji pinigai : 1, Kortelė : 2 |

- Dalyje **Mažmeninė prekyba > Kanalų sąranka > Fiskalnė integracija > Fiskalinių jungčių grupė** sukurkite grupes **Fiskalinių jungčių grupės**. Jungčių grupė yra su identiškas funkcijas atliekančiomis ir tame pačiame fiskalinės registracijos proceso etape naudojamomis fiskalinėmis jungtimis susietų funkcinių profilių subrinkinys.

   - Į jungčių grupę įtraukite funkcinių profilių. Puslapyje **Funkciniai profiliai** spustelėkite **Įtraukti** ir pasirinkite profilio numerį.
   - Jei norite sustabdyti funkcinių profilių naudojimą, nustatykite funkcijos **Išjungti** parinktį **Taip**. 
   
     Šis pakeitimas taikomas tik dabartinei jungčių grupei. Kitose jungčių grupėse galite ir toliau naudoti tą patį funkcinį profilį.

     >[!NOTE]
     > Kiekviena fiskalinė jungčių grupės jungtis gali turėti tik vieną funkcinį profilį.

- Dalyje **Mažmeninė prekyba > Kanalų sąranka > Fiskalinė integracija > Jungties techniniai profiliai** sukurkite kiekvienos fiskalinės jungties profilį **Jungties techninis profilis**.
  - Pasirinkite jungties pavadinimą.
  - Pasirinkite jungties tipą. 
      - **Vietinė** – nustatykite šį tipą vietiniame įrenginyje įdiegtiems fiziniams įrenginiams arba programoms.
      - **Vidinė** – nustatykite šį tipą prie „Retail Server“ prijungtiems fiskaliniams įrenginiams ir paslaugoms.
      - **Išorinė** – mokesčių inspekcijos teikiamoms išorinėms fiskalinėms paslaugoms, pvz., žiniatinklio portalui.
    
  - Skirtuke **Ryšys** nurodykite parametrus.

      
 >[!NOTE]
 > Bus įkelta atnaujinta pirmiau įkeltų funkcinio ir techninio profilių konfigūracijos versija. Jei atitinkama jungtis arba atitinkamas dokumento teikėjas jau naudojami, apie tai bus pranešta. Pagal numatytuosius nustatymus bus saugomi visi neautomatiškai atlikti funkcinių ir techninių profilių pakeitimai. Norėdami perrašyti šiuos profilius naudodami numatytąjį konfigūracijos parametrų rinkinį, puslapyje **Funkciniai jungčių profiliai** ir puslapyje **Techniniai jungčių profiliai** spustelėkite **Naujinti**.
 
- Dalyje **Mažmeninė prekyba > Kanalų sąranka > Fiskalinė integracija > Fiskalinės registracijos procesai** sukurkite kiekvieno unikalaus fiskalinės integracijos proceso procesą **Fiskalinės registracijos procesas**. Registracijos procesas nusakomas registracijos veiksmų seka ir kiekvienam veiksmui naudojama jungčių grupe. 
  
  - Į procesą įtraukite registracijos veiksmus.
      - Spustelėkite **Įtraukti**.
      - Pasirinkite jungties tipą.
      
      >[!NOTE]
      > Šiame lauke nurodoma, kur sistema ieškos techninio profilio jungties (aparatūros profilių jungties tipo **Vietinė** arba, jei tai EKA funkcijų profiliai – kito tipo fiskalinių jungčių).
      
   - Pasirinkite jungties grupę.
   
     >[!NOTE]
     > Spustelėję **Tikrinti** patikrinkite registracijos proceso struktūros vientisumą. Tikrinimus rekomenduojama atlikti toliau išvardytais atvejais.
       >- Naujam registracijos procesui užbaigus atlikti visus nustatymus, įskaitant susiejimą su EKA funkcijų profiliais ir aparatūros profiliais.
       >- Atlikus esamo registracijos proceso atnaujinimus.

-  Dalyje **Mažmeninė prekyba > Kanalų sąranka > EKA sąranka > EKA profiliai > Funkcijų profiliai** susiekite fiskalinės registracijos procesus su EKA funkcijų profiliais.
   - Skirtuke **Fiskalinės registracijos procesas** spustelėkite **Redaguoti** ir pasirinkite numerį **Proceso numeris**.
- Dalyje **Mažmeninė prekyba > Kanalų sąranka > EKA sąranka > EKA profiliai > Aparatūros profiliai** jungčių techninius profilius susiekite su aparatūros profiliais.
   - Skirtuke **Fiskalinis techninis profilis** spustelėkite **Redaguoti**, paskui – **Naujas**.
   - Lauke **Profilio numeris** pasirinkite jungties techninį profilį.
   
     >[!NOTE]
     > Galite įtraukti kelis aparatūros profilio techninius profilius. Tačiau tai nepalaikoma, jei aparatūros profilis turi daugiau nei vieną sankirtą su bet kuria jungčių grupe. Norint išvengti neteisingų parametrų, atnaujinus visus aparatūros profilius rekomenduojama patikrinti registracijos procesą.

