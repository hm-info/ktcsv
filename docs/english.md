# KT803 KT808 Csv File Description

| **Column Name in the Work File** | **Information** | **Definition** |
|----------------------------------|------------------|----------------|
| **id** | Part ID | Each part has a unique ID. |
| **code** | Profile code | The profile code defined on the profile page. Revolver positions are determined based on the profile code. |
| **DATA2** | Part barcode | Unique part barcode. When scanned, it matches the part in this column. |
| **DATA11** | Outer wing height | Hinge positions are calculated based on the wing height. For a 2000 mm wing, DATA11 should be 2000. |
| **DATA12** | Opening direction (left/right), number of hinges | Since the hinge direction and positions will change, left or right opening is required. Hinge drilling and screwing positions are adjusted on the operations page. From the beginning to the end of the profile, hinge positions are defined on the operations page. Macros H0101XX and H0102XX are fixed; only the accessory code (XX) can vary. |
| **DATA13** | Threshold type | This is the threshold code from the Threshold page. Hinge positions change depending on threshold height. |
| **DATA14** | Door handle position | Distance from the bottom of the profile to the handle position. For a 1000 mm handle position, DATA14 value should be 1000. |
| **DATA15** | Hinge color, espagnolette type, hinge type | Hinge color is written for informational purposes. The espagnolette type is defined on the lock gear page and is only available in sash machines. The hinge type is defined on the operations page. |
| **DATA16** | Transom | Should be selected if there is a mullion in the profile. 0: No transom, 1: Transom exists. |

---

**Example for DATA12:**

- H010103 : Left Opening, 3 Hinges  
- H010104 : Left Opening, 4 Hinges  
- H010203 : Right Opening, 3 Hinges  
- H010204 : Right Opening, 4 Hinges  

**Explanation:**  
H : Fixed, 01 : Tool code, 02 : Operation code (01 = Left, 02 = Right), 03 : Accessory code  

---

**Example for DATA15:**

- White|KUBU French Master|Hinge1 → White color, lock gear code "KUBU French Master", hinge type "Hinge1"

---

**Work file example ----->>>** [KT8xx](./data.csv)
