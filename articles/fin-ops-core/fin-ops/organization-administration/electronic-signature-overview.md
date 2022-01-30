---
title: Elektroninių parašų apžvalga
description: Šiame straipsnyje apžvelgiami elektroniniai parašai ir aprašoma, kaip juos naudoti.
author: maertenm
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.custom:
- "13611"
- intro-internal
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9f80ecef043a697d288fed99e3118e268d4f993
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983647"
---
# <a name="electronic-signatures-overview"></a>Elektroninių parašų apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje apžvelgiami elektroniniai parašai ir aprašoma, kaip juos naudoti.

## <a name="what-is-an-electronic-signature"></a>Kas yra elektroninis parašas?

Elektroninis parašas patvirtina asmens, kuris ketina pradėti ar patvirtinti skaičiavimo procesą, tapatybę. Kai kuriose pramonės šakose elektroninis parašas turi tokią pat teisinę galią kaip parašas ranka.

Elektroniniai parašai yra reglamentus atitinkantis reikalavimas kai kurioms reguliuojamoms pramonės šakoms, pvz., vaistų, maisto ir gėrimų, aviacijos ir gynybos. Jie taip pat būtini siekiant vykdyti JAV Maisto ir vaistų administracijos (FDA) 21 CFR 11 dalies nuostatas.

> [!NOTE]
> Elektroninis parašas nėra tas pat, kas skaitmeninis parašas. Elektroninis parašas yra tiesiog pasirašymo ranka pakaitas, o skaitmeninis parašas suteikia papildomų saugos priemonių. Skaitmeninis parašas gali padėti nustatyti, ar kitas vartotojas arba procesas mėgino piktavališkai pakeisti duomenis. Skaitmeninį parašą taip pat galima patikrinti, o šio tikrinimo negali paneigti sertifikato, kuris buvo naudojamas pasirašyti duomenis, savininkas. Kaip aprašyta toliau, elektroniniuose parašuose yra įdiegtos skaitmeninio parašo funkcijos.

## <a name="electronic-signatures"></a>Elektroniniai parašai

Galite naudoti elektroninius parašus svarbiems verslo procesams. Kai kuriuose procesuose yra įdiegtos elektroninio parašo galimybės. Taip pat galite sukurti pasirinktinius parašo reikalavimus bet kuriai duomenų bazės lentelei ir laukui.

Elektroniniuose parašuose yra įdiegtos skaitmeninio parašo funkcijos. Kiekvienas dokumentus pasirašantis vartotojas turi įsigyti galiojantį kriptografijos sertifikatą. Pasirašant dokumentą patikrinamas su tuo sertifikatu susietas privatusis raktas. Elektroninio parašo informacija įrašoma į žurnalą, kad būtų galima sekti įrašą. Norėdami nustatyti elektroninius parašus, žr. dalį [Elektroninių parašų nustatymas](tasks/set-up-electronic-signatures.md).

## <a name="users-who-require-access-to-electronic-signatures"></a>Vartotojai, kuriems reikia prieigos prie elektroninių parašų

Trijų tipų vartotojams paprastai reikia saugumo prieigos prie elektroninių parašų: elektroninio parašo administratoriams, pasirašantiems ir elektroninio parašo auditoriams.

### <a name="electronic-signature-administrator"></a>Elektroninio parašo administratorius

Elektroninio parašo administratorius nustato parašo reikalavimus, bendruosius parametrus, tvirtintojus ir gauna įspėjimus, kai parašų patikrinti nepavyksta. Pagal numatytuosius nustatymus, vartotojas, kuris priklauso saugos vaidmeniui **Informacinių technologijų vadovas**, turi teisę administruoti elektroninius parašus.

### <a name="signer"></a>Pasirašantysis

Pasirašantysis elektroniniu būdu pasirašo dokumentus ir procesus, kuriems reikalingi parašai. Pagal numatytuosius nustatymus, vartotojas, kuris priklauso **Sistemos vartotojas** saugos vaidmeniui, turi teisę pasirašyti dokumentus elektroniniu būdu.

> [!NOTE]
> Pasirašančiajam gali reikėti papildomų teisių norint pasiekti duomenis, susijusius su pasirašomu dokumentu arba procesu. Vartotojas, kuris pakeičia duomenis ir turi pasirašyti tuos pakeitimus, turi turėti teisę keisti duomenis. Vartotojas, kuris pasirašo kito vartotojo vardu, negali reikalauti prieigos prie duomenų. Tokios rūšies vartotojo pavyzdys yra vadovas, kuris pasirašo darbuotojo pakeitimus.

### <a name="electronic-signature-auditor"></a>Elektroninio parašo auditorius

Elektroninio parašo auditorius peržiūri duomenų bazės žurnalą ir parašų peržiūros žurnalą, esantį duomenų bazės žurnale. Pagal numatytuosius nustatymus, vartotojas, kuris priklauso saugos vaidmeniui **Informacinių technologijų vadovas**, turi teisę audituoti elektroninius parašus.

Jei naudojate ne vaidmenį **Informacinių technologijų vadovas**, įsitikinkite, kad vaidmeniui priskiriamos nurodytos teisės:

- Peržiūrėti elektroninio parašo triktis
- Peržiūrėti duomenų bazės žurnalą

## <a name="signing-documents-electronically"></a>Dokumentų pasirašymas elektroniniu būdu

### <a name="get-a-certificate"></a>Sertifikato gavimas

Prieš pasirašydami dokumentus elektroniniu būdu, turite prašyti sertifikato.

> [!NOTE]
> Sertifikatams kurti ir elektroniniam pasirašymui įgalinti naudojamos Microsoft SQL Server funkcijos. Nereikia jokio papildomo sertifikato arba viešųjų raktų sistemos infrastruktūros (PKI).

Kai prašote sertifikato, jums sukuriamas viešasis raktas ir privatusis raktas. Privatusis raktas šifruojamas naudojant tik jums žinomą slaptažodį. Kai dokumentą pasirašote elektroniniu būdu, jūsų tapatybė patikrinama įvedant slaptažodį.

Norėdami prašyti sertifikato, puslapio **Parinktys** skirtuke **Sąskaitos** spustelėkite **Gauti sertifikatą**.

Turite įvesti ir patvirtinti slaptažodį, kurį naudosite pasirašydami. Slaptažodis naudojamas apsaugoti jūsų privatųjį raktą ir leisti naudoti jūsų sertifikatą. Šis slaptažodis nesaugomas duomenų bazėje, jo negali žinoti niekas kitas, net administratorius.

Jeigu pamiršote su savo sertifikatu susietą slaptažodį, sertifikatą reikia atkurti. Sertifikato nustatymas iš naujo neturi įtakos dokumentams, kuriuos pasirašėte naudodami ankstesnį sertifikatą. Norėdami iš naujo nustatyti sertifikatą, puslapyje **Parinktys** spustelėkite **Nustatyti iš naujo sertifikatą**.

### <a name="sign-a-document-electronically"></a>Dokumento pasirašymas elektroniniu būdu

Puslapis **Dokumento pasirašymas** rodomas, kai atliekate keitimą, kuriam reikalingas elektroninis parašas.

1. Puslapyje **Dokumento pasirašymas** spustelėkite skirtuką **Dokumentas**, norėdami peržiūrėti dokumento keitimus.
2. Skirtuke **Parašas** pasirinkite priežasties kodą.
3. Įveskite komentarą, jei komentaras yra būtinas.
4. Jeigu jūsų vartotojo ID nerodomas lauke **Pasirašantysis**, pasirinkite jį iš sąrašo.
5. Įveskite savo buvimo vietą, jei ši informacija yra reikalinga.
6. Spustelėkite **GERAI**.

### <a name="sign-for-another-users-changes"></a>Kito vartotojo atliktų keitimų pasirašymas

Kartais galite norėti, kad vartotojas pasirašytų už kito vartotojo keitimus. Pavyzdžiui, darbuotojo atliktus komplektavimo specifikacijos (KS) keitimus gali reikėti pasirašyti vadovui. Taikykite šią procedūrą norėdami vartotoją paskirti pasirašyti už kitą vartotoją.

> [!NOTE]
> Kai vienas vartotojas pasirašo už kito vartotojo keitimą, parašas turi būti pateiktas keitimą atlikusio vartotojo darbo vietoje. Vartotojas negalės įrašyti keitimo, kol nebus pasirašyta.

Norėdami paskirti tvirtintojus, atlikite toliau nurodytus veiksmus.

1. Puslapio **Parinktys** skirtuke **Sąskaitos** spustelėkite **Paskirti tvirtintoją**.
2. Lauke **Tvirtintojo vartotojo ID** pasirinkite vartotojo, kuris turi pasirašyti kito vartotojo keitimus, ID.
3. Lauke **Vartotojo, už kurį pasirašoma, ID** pasirinkite vartotojo, kurio keitimai turi būti pasirašyti, ID.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]