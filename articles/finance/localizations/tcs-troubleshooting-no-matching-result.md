---
title: Nerasta atitinkančių rezultatų
description: Šioje temoje paaiškinama, kaip atlikti trikčių šalinimo klaidą "Nepavyko rasti sutampančių rezultatų" mokesčių skaičiavimo serijosvce.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: c1a343b0b74645d40b0a2582749968cc0a56afd7
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648153"
---
# <a name="no-matching-result-could-be-found"></a>Nerasta atitinkančių rezultatų

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinami trikčių diagnostikos veiksmai, kuriuos galite atlikti, jei mokesčių skaičiavimo paslaugoje gaunate klaidą "Atitinkančių rezultatų nerasta".

## <a name="symptom"></a>Požymis

Gaunate šį klaidos pranešimą: "Antraštė / eilutės - 1, mokesčių grupė, nerasta jokio sutampančių rezultatų."

```json
======================Tax service calculation result JSON:===========================
{
    "taxDocument": {
        "Header": [
            {
                "Lines": [
                    {
                        ...
                        "Errors": [
                            {
                                "Code": "TaxSetup20000",
                                "Message": "Header/Lines - 1, Tax group applicability, no matching result could be found."
                            }
                        ],
                        "Adjustment": null
                    }
                ],
                "Measures": {
                    ...
                },
                ...
            }
        ]
    },
    ...
}
```

## <a name="cause"></a>Priežastis

Problema kyla, kai reguliavimo konfigūracijos tarnybos (RCS) funkcijos nustatymas yra neteisingas.

## <a name="troubleshoot"></a>Šalinti triktis

1. Atsisiųsti trikčių diagnostikos failą. Daugiau informacijos ieškokite trikčių [šalinimo derinimo režimo įgalinimas](tcs-troubleshooting-enable-debug-mode.md).
2. Palyginkite mokesčių tarnybos skaičiavimo įvestį su priemonės nustatymu, kad išspręskite nustatymo problemą.

    Šiame pavyzdyje rodoma mokesčių tarnybos skaičiavimo įvestis.

    ```json
    ===============================Tax service calculation input JSON:=====================================
    {
        "TaxableDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            ...
                        }
                    ],
                    "Business Process": "Sales",
                    "Ship From Zip Code": "30159",
                }
            ]
        },
        "Parameter": {
            ...
        },
        "Adjustment": {
            "Lines": {}
        }
    }
    ```

    Šioje lentelėje išvardijamos mokesčių grupės taikomumas RCS.

    | Antraštė. Verslo procesas | Eilutės. Verslo vienetas | Antraštė. Siųsti iš pašto kodo | Mokesčių grupė |
    |-------------------------|---------------------|---------------------------|-----------|
    | Žurnalas                 |                     |                           | Grupė A   |
    | Pardavimas                   |                     | 30160                     | Grupė B   |

    Pagal mokesčių tarnybos apskaičiavimo įvestį, **·** **verslo** proceso vertė antraštėje yra Pardavimas, **·** **o siuntimo iš pašto kodo vertė antraštėje yra 30159**. Ši įvestis pagrįsta RCS taikomumo taisyklių nustatymu. Kadangi nėra atitinkamos eilutės, įvyksta klaida.

    > [!NOTE]
    > Jei pritaikymo taisyklės vertė tuščia, taisyklė taikoma bet kuriai vertei.

## <a name="mitigation"></a>Mažinimo priemonė

Norėdami sumažinti klaidą, atlikite šiuos veiksmus.

1. RCS eikite į **globalizavimo priemonių** \>**mokesčių skaičiavimą**.
2. Sukurkite naują priemonės versiją.
3. Pridėkite atitinkamos informacijos eilutę.

    | Antraštė. Verslo procesas | Eilutės. Verslo vienetas | Antraštė. Siųsti iš pašto kodo| Mokesčių grupė |
    |-------------------------|---------------------|--------------------------|-----------|
    | Žurnalas                 |                     |                          | Grupė A   |
    | Pardavimas                   |                     | 30160                    | Grupė B   |
    | Pardavimas                   |                     | 30159                    | Grupė B   |

4. Publikuoti priemonių nustatymo versiją.
5. Microsoft Dynamics 365 finansuose eikite į **Mokesčių nustatymo** \> **·** \> **mokesčių konfigūracijos** \> **mokesčių skaičiavimo parametrus** ir pasirinkite naują versiją.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
