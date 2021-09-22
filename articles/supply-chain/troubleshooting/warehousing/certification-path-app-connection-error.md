---
title: Nustatant programos ryšį įvyko sertifikato maršruto klaida
description: Jei „Warehouse Management“ programoje rodoma klaida "Nepavyko rasti sertifikavimo maršruto patikimumo prieraišo", naudokite šį puslapį, norėdami išspręsti problemą arba dirbti su problema.
author: ivanv-microsoft
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: WMA
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e4a36874ac4982c9c92a7dcc17c13c7c7c02bf8c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477095"
---
# <a name="trust-anchor-for-certification-path-not-found-when-setting-up-app-connection"></a>Atnaujinant ir perkeliant į WMS nepavyko rasti nustatant programos ryšį

## <a name="symptoms"></a>Požymiai

Bandant prisijungti prie „Supply Chain Management“, „Warehouse Management“ programa gali parodyti tokį klaidos pranešimą:

> Gaunu tolesnį klaidos pranešimą: „java.security.cert.certPathValidatorException: Pasitikėjimo inkaras sertifikavimo keliui nerastas.

Ši problema gali paveikti įrenginius, kurių ypatybės tokios:

- **OS versija**: „Android“ 4.4.x (pvz., „Zebra“ TC55). Tai nėra naujų versijų „Android“ problema.
- **„Supply Chain Management“ vieta**: debesis
- **Ryšio režimas**: kliento slaptos ar sertifikato

## <a name="possible-cause"></a>Galima priežastis

„Microsoft" galėjo atnaujinti serverio SSL sertifikatus, naudojamus „Supply Chain Management“. Todėl šakninis sertifikatas ir (arba) vienas iš tarpinių sertifikatų galėjo būti pakeisti, todėl naujas sertifikatas nėra patikimos mobiliojo įrenginio sistemos sertifikatų sąraše. Naujesnės versijos „Android“ automatiškai atnaujina patikimų sertifikatų sąrašus, bet „Android“ 4.4.x ne.

## <a name="resolution"></a>Sprendimas

Norėdami išspręsti šią problemą, pabandykite atlikti tolesnius veiksmus:

- Norėdami atnaujinti kiekvieną reikiamą įrenginį, naudokite toliau skyriuje apibūdintą problemos sprendimą.
- Gali būti, kad norėdami gauti sistemos patikimos sertifikavimo tarnybos (CA) sertifikatų atnaujinimą, gali būti įmanoma *susisiekti* su „Zebra" arba „Google". Tačiau mes to nepatvirtinome.
- Jei galima, apsvarstykite galimybę pakeisti senesnius įrenginius įrenginiais, kurių versija naujesnė „Android“ (čia patikimi CA sertifikatai atnaujinami automatiškai).

### <a name="workaround"></a>Apėjimo būdas

#### <a name="step-1-export-the-new-root-certificate-from-supply-chain-management"></a>1 žingsnis: eksportuoti naują šakninį sertifikatą iš „Supply Chain Management“

Rankiniu būdu atsisiųsti naują šakninį sertifikatą naudojant interneto naršyklę atliekant šiuos veiksmus:

1. Prisiregistruokite prie „Dynamics" „Supply Chain Management“ ir atidarykite priekinį puslapį.

1. Naršyklės adresų juostoje pasirinkite užrakto piktogramą, kad atidarytumėte **dialogo langą Vieta**.
1. Dialogo lange pasirinkite **Sertifikatas (galioja),** kad atidarytumėte **sertifikato** langą Sertifikatas.
1. Atidarykite **sertifikato lango** skirtuką **Sertifikato** maršrutas.
1. Pasirinkti aukščiausią hierarchijoje rodomą sertifikatą. (tai yra šakninis sertifikatas).
1. Atidarykite **Išsamios informacijos** skirtuką **Sertifikato** maršrutas.
1. Skirtuko **Išsami informacija** apačioje pasirinkite mygtuką Kopijuoti į **failą**.
1. Atidaroma **sertifikato eksportavimo vedlys**. Pasirinkite **Pirmyn**, kad tęstumėte.
1. Atidaroma **eksportavimo failo formato** puslapis. Pasirinkite **DER užkoduotą dvejetainį X.509 (.CER)**. Tada rinkitės **Pirmyn**, kad tęstumėte.
1. Atidaromi **failai, kuriuos** reikia eksportuoti, nurodykite failo vardą ir vietą. Tada rinkitės **Pirmyn**, kad tęstumėte.
1. Atidaromas **sertifikato eksportavimo vedlio** puslapis, kuriame rodomi jūsų eksportavimo rezultatai. Pasirinkite **Baigti**.

#### <a name="step-2-install-the-downloaded-certificate-onto-the-affected-devices"></a>2 žingsnis: atsisiųstą sertifikatą įdiekite į paveiktus įrenginius

Įdiekite atsisiųstą sertifikatą, atlikdami šiuos veiksmus:

1. Perkelkite ankstesniu veiksmu atsisiųstą sertifikatą į įrenginį, kurį norite atnaujinti. Pavyzdžiui, norėdami, kad failas būtų prieinamas jūsų įrenginiui, galite naudoti SD kortelę arba tinklo ryšį.
1. Atidarykite įrenginio saugos parametrus ir pasirinkite meniu pasirinktį, norėdami įdiegti sertifikatą iš failo. (Tikslūs šio žingsnio veiksmai priklauso nuo įrenginio ir OS versijos.)
1. Naujasis sertifikatas dabar turi būti rodomas **patikimo** sertifikato skirtuke Vartotojas.
1. Šią procedūrą kartokite nustatydami kiekvieną paveiktą įtaisą.
