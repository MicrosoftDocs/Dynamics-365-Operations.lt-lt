---
title: Trikčių šalinimo gerinimo ir perkėlimas į papildomą sandėlio valdymą
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti naujindami ir perkeldami siekiant pagerinti sandėlio valdymą.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 953b828667a01157767c3ca79349fe972b0fbe9b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826400"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>Trikčių šalinimo gerinimo ir perkėlimas į papildomą sandėlio valdymą

[!include [banner](../includes/banner.md)]

Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti naujindami ir perkeldami siekiant pagerinti sandėlio valdymą.

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>Gaunu tolesnį klaidos pranešimą: „java.security.cert.certPathValidatorException: Pasitikėjimo inkaras sertifikavimo keliui nerastas."

### <a name="issue-description"></a>Problemos aprašas

Gavote šį klaidos pranešimą sandėlio valdymo mobiliųjų įrenginių programėlėje, kadangi „Android“ 8+ vietinėse aplinkose nepasitikima savaime prisijungusiais sertifikatais.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Naudokite išorės (viešąją) seritfikavimo įstaigą (CA). Šios trikties pašalinimas yra prieinamas sandėlio programose 1.9.0.0 versijoje. Daugiau informacijos apie šią problemą ir kaip ją išspręsti rasite [Sandėlio valdymo mobiliųjų įrenginių programėlės ryšio trikčių diagnostika](troubleshoot-warehouse-app-connection.md).

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>Kas yra patvirtintas procesas perkėlimui iš pagrindinio sandėliavimo į pagerintą sandėliavimą?

### <a name="issue-description"></a>Problemos aprašas

Dabar vykdote sandėliavimo/inventoriaus valdymą ir naudojate pagrindines sandėlio funkcijas ir norite perkelti pagerintą sandeliavimą tam, kad pasinaudotumėte mobiliuoju įrenginiu, bangomis ir darbu geriau. Nepaisant to, patiriate trikčių bandydami padaryti šį perkėlimą. Pavyzdžiui, negali pakeisti savo produktų taip, kad jie naudotų talpinimo matmenis (vietą, sandėlį ir vietą), nes produktai turi perlaidas jų atžvilgiu. Dėl to, privalote išmokti patvirtintą procesą perkėlimui iš pagrindinio sandėliavimo į pagerintą sandėliavimą.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Dėl daugiau informacijos apie procesą perkėlimui iš pagrindinio sandėliavimo į pagerintą sandėliavimą, žr. tolesnius tinklaraščio įrašus ir dokumentus:

- [Įjungti sandėlio valdymo procesą esantiems elementams ir sandėliams](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [„Microsoft Dynamics AX“ perkėlimas WMS į naują R3 sandėlį ir gabenimo funkcijos](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [WMSI/WMS2 elemento perkėlimas](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [Sandėlio valdymo pagerinimas iš „Microsoft Dynamics“ AX 2012 iki „Supply Chain Management“](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]