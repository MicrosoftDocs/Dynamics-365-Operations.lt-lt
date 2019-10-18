---
title: Parduotuvės atsargų valdymas
description: Šioje temoje aprašyti dokumentų, kuriuos galite naudoti atsargoms valdyti, tipai.
author: rubencdelgado
manager: AnnBe
ms.date: 04/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c5da94e02b2381bbd058221567172cd428931c45
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024688"
---
# <a name="store-inventory-management"></a>Parduotuvės atsargų valdymas

[!include [banner](includes/banner.md)]

Dirbant su atsargų programoje „Dynamics 365 Retail“ ir naudojant EKA programą, svarbu atminti, kad atsargų dimensijų ir tam tikrų atsargų prekių tipų palaikymas EKA yra ribotas.

EKA sprendimas nepalaiko tolesnių prekių konfigūracijų.

- KS prekės (išskyrus rinkinio produktus, kurie naudoja keletą KS struktūros komponentų)
- Esamo svorio prekės
- Paketo valdomos prekės

Šiuo metu EKA programa nepalaiko toliau nurodytų dimensijų EKA.

- Paketo sekimo dimensija
- Savininko dimensija

EKA sprendimas ribotai palaiko toliau nurodytas dimensijas. Ribotas palaikymas nurodo, kad EKA gali nustatyti kai kurių iš šių dimensijų numatytąsias reikšmes į atsargų operacijas automatiškai, atsižvelgiant į sandėlio / parduotuvės sąrankos konfigūraciją. EKA dimensijų išsamiai nepalaikys, kaip jos yra palaikomos, jei į ERP neautomatiniu būdu įvedama į pardavimo operacija. 

- **Sandėlio vieta** – Vartotojai negalės valdyti priimančio sandėlio vietos prekėms, gautoms į parduotuvės sandėlį, kai parduotuvė nesukonfigūruota naudoti sandėlio valdymo procesą. Šioms prekėms bus naudojama numatytoji priėmimo vieta, nurodyta parduotuvės sandėlyje. Jei parduotuvės sandėlio valdymo procesas buvo įjungtas, bus pradėtas ribotas palaikymas, raginantis vartotoją pasirinkti priėmimo vietą visam priėmimui. Parduotuvėje parduodamos prekės bus visada parduodamos numatytoje mažmeninės prekybos vietoje, nurodytoje parduotuvės sandėlio sąrankoje. Grąžinamų atsargų tvarkymo vietą galima valdyti nurodant numatytąją grąžinimo vietą parduotuvės sandėlyje arba pagal grąžinimo priežasties kodus, nurodytus grąžinimo vietos politikoje.
- **Numerio lentelė** – numerio lentelės taikomos tik kai parametras **Naudoti sandėlio valdymo procesą** įjungtas prekės ir parduotuvės sandėlyje. EKA atveju, jei atsargos priimamos į parduotuvės sandėlį, kuriame įgalintas sandėlio valdymo procesas, ir pasirinkta prekės priėmimo vieta susieta su vietos profiliu, kuriam būtina numerio lentelės kontrolė, EKA programa sistemiškai taikys numerio lentelę priėmimo linijai. EKA vartotojai negalės keisti arba valdyti šio numerio lentelės datos. Jei būtinas visapusiškas numerio lentelės valdymas, siūlome parduotuvei naudoti WMS mobiliąją programą arba biuro ERP klientą šių prekių priėmimui valdyti.
- **Serijos numeris** – EKA programa turi ribotą palaikymą vienam serijos numeriui registruoti operacijos pardavimo linijoje užsakymams, sukurtiems EKA su eilutėmis išdėstytomis prekėmis. Šis serijos numeris nėra patikrintas pagal užregistruotus atsargose jau esančius serijos numerius. Jei pardavimo užsakymas sukurtas skambučių centro kanale arba įvykdytas per ERP ir keli serijos numeriai yra registruojami vienoje pardavimo eilutėje vykdant ERP vykdymo procesą, šie serijos numeriai negalės būti taikomi arba patikrinti, jei šių užsakymų grąžinimas yra apdorojamas EKA.
- **Atsargų būsena** – prekėms, kurios naudoja sandėlio valdymo procesą ir kurioms reikalinga atsargų būsena, šis būsenos laukas negali būti nustatytas arba modifikuotas EKA programoje. Numatytoji atsargų būsena, nurodyta parduotuvės sandėlio konfigūracijoje, bus naudojama, kai prekės gaunamos į atsargas.

> [!NOTE]
> Visos organizacijos turi patikrinti prekių konfigūracijas naudodamos EKA programavimo ar tikrinimo aplinkoje prieš jas diegdamos gamyboje. Tikrinkite prekes atlikdami reguliarias grynųjų pinigų pardavimo operacijas ir kurdami klientų užsakymus (jei taikoma) per EKA su savo prekėmis. Tikrinimas turi apimti išsamaus išrašo registravimo procesus tikrinimo aplinkoje ir patikrinimą, ar nėra problemų.
>
> Prekių konfigūravimas tokiu būdu, kurio nepalaiko EKA programa, tinkamai nepatikrinus, išrašo registravimo proceso metu gali kilti gamybos problemų ir jas išspręsti gali būti sudėtinga. Partnerio arba kliento programos tinkinimai gali būti taikomi pasirinktinai, kad šie registravimo procesai būtų sėkmingai užbaigti. Jei tinkinimai nėra būtini, organizacijos turi užtikrinti, kad produktų konfigūracijos būtų atliekamos tokiu būdu, kurį palaiko standartinė EKA programa / užsakymo kūrimas / išrašo registravimo procesas.

## <a name="purchase-orders"></a>Pirkimo užsakymai

Pirkimo užsakymai kuriami pagrindiniame biure. Jei į pirkimo užsakymo antraštę įtraukiamas mažmeninės prekybos sandėlis, užsakymą parduotuvėje galima gauti naudojant „Modern POS“ (MPOS) arba „Cloud POS“ per operaciją **Paėmimas / gavimas**. Kai iš parduotuvė priimti kiekiai įvedami į pirkimo užsakymo dokumento EKA lauką **Gauti dabar**, juos galima įrašyti vietoje arba užfiksuoti. Šių duomenų įrašymas vietoje neturi poveikio turimoms atsargoms. Įrašyti rekomenduojama, tik jei vartotojas nėra pasiruošęs registruoti gavimo kvito būstinėje ir tiesiog reikia būdo laikinai išsaugoti anksčiau įvestus duomenis **Gauti dabar**. Taip duomenys Gauti dabar įrašomi vietinėje vartotojo kanalo duomenų bazėje. Kai dokumentas apdorojamas naudojant parinktį **Fiksuoti**, duomenys **Gauti dabar** siunčiami į būstinę ir pirkimo užsakymo kvitas užregistruojamas. 

## <a name="transfer-orders"></a>Perkėlimo užsakymai

Perdavimo užsakyme galima nurodyti, kad prekes galima išsiųsti tik iš konkrečios parduotuvės arba kur jus jos bus priimtos. Jei EKA vartotojas yra perdavimo užsakymo siuntimo sandėlys, jis galės įvesti **Siųsti dabar** kiekius programoje EKA. Siunčiančios parduotuvės gali būti įrašytos vietoje arba užfiksuotos. Įrašius vietoje perdavimo užsakymas būstinėje neatnaujinamas. Įrašyti rekomenduojama, tik jei vartotojas nėra pasiruošęs registruoti siuntimo kvito būstinėje ir reikia būdo laikinai išsaugoti anksčiau įvestus duomenis **Siųsti dabar**. Kai parduotuvė pasiruošusi patvirtinti siuntimą, reikia pasirinkti parinktį **Fiksuoti**. Taip išsiunčiamas būstinės perdavimo užsakymo siuntinys, kad priimantis sandėlys galės priimti pagal jį. 

Jei EKA vartotojas yra perdavimo užsakymo priėmimo sandėlys, jis galės įvesti **Gauti dabar** kiekius programoje EKA. Priimančios parduotuvės gali būti įrašytos vietoje arba užfiksuotos. Įrašyti rekomenduojama, tik jei vartotojas nėra pasiruošęs registruoti gavimo kvito būstinėje ir reikia būdo laikinai išsaugoti anksčiau įvestus duomenis **Gauti dabar**. Taip duomenys Gauti dabar įrašomi vietinėje vartotojo kanalo duomenų bazėje. Kai dokumentas apdorojamas naudojant parinktį **Fiksuoti**, duomenys **Gauti dabar** siunčiami į būstinę ir perdavimo užsakymo kvitas užregistruojamas. Svarbu turėti omenyje, kad priimančiai parduotuvei bus galima tik fiksuoti gaunamus kiekius, kurie neviršija siunčiamų kiekių. Bandymas gauti perdavimo užsakymo kiekius, kurie dar nebuvo išsiųsti, sukels klaidas ir priėmimas nebus fiksuotas būstinėje.

## <a name="stock-counts"></a>Inventorizacijos

Inventorizacijos gali būti planinės arba neplaninės. Planinės inventorizacijos inicijuojamos pagrindiniame biure, kuris nurodo, kurias prekes reikia skaičiuoti. Pagrindinis biuras sukuria inventorizavimo dokumentą, kurį galima gauti parduotuvėje, kurioje faktinių turimų atsargų kiekiai įvedami į MPOS arba debesies EKA. Neplaninės inventorizacijos inicijuojamos parduotuvėje, o faktinių turimų atsargų kiekiai atnaujinami MPOS arba debesies EKA. Skirtingai nei planinės inventorizacijos, neplaninės inventorizacijos neturi iš anksto apibrėžto prekių sąrašo. Alikus bet kurio tipo inventorizaciją, ji fiksuojama ir siunčiama į pagrindinį biurą. Pagrindiniame biure inventorizacija patikrinama ir registruojama atskiru veiksmu.

## <a name="inventory-lookup"></a>Atsargų peržvalga

Dabar keliose parduotuvėse ir sandėliuose turimą produktų kiekį galima peržiūrėti **atsargų peržvalgos** puslapyje. Neskaitant dabartinio turimo kiekio, galima pamatyti kiekvienos atskiros parduotuvės būsimus prieinamų atsargų (ATP) kiekius. Norėdami tai padaryti pasirinkite parduotuvę, kurios ATP norite peržiūrėti, ir tada spustelėkite **Rodyti parduotuvės pasiekiamumą**.
