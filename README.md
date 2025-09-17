# csv2xml

## 📖 簡介
此工具會將已填寫完成的 `.csv` 轉換為 **C-CURE** 格式的 `.xml`。  

## ⚠️ 注意
1. 目前僅支援最多 **`5` 個許可表** 的填入。
2. 建議在使用前，先於系統中完善以下物件：
    - 🚪`Door`
    - 📁`Group`
        - 🧑‍🤝‍🧑`GroupMember`
    - 🪪`Clearance`
        - 📋`ClearanceItem`

---

## 🚀 如何使用
1. **填寫** 📝 `Import_Personnel.csv`
   
    | 範例 | FirstName | LastName | CardNumber | Text1 | Text2  | Text3 | ClearanceKey1 | ClearanceKey2 | ClearanceKey3 | ClearanceKey4 | ClearanceKey5 |
    |----|-----------|----------|------------|-------|--------|-------|---------------|---------------|---------------|---------------|---------------|
    | 1  | 小明        | 王        | 358621     | EE    | LIT    | 1     | 70001         | 70002         | 70003         | 70004         | 70005         |
    | 2  | 小華        | 陳        | 358622     | GG    | AKA    | 2     | 70004         | 70005         | 70006         | 70007         | 70008         |

2. **執行** ▶️ `csv2xml.exe`  
3. **完成並輸出** 📇 `Import_Personnel.xml`
    ```xml
    <CrossFire culture-info="zh-TW" platform-version="3.0.0" product-version="3.0.0">
    <SoftwareHouse.NextGen.Common.SecurityObjects.Personnel ImportMode="Default">
        <FirstName>小明</FirstName>
        <LastName>王</LastName>
        <Text1>EE</Text1>
        <Text2>LIT</Text2>
        <Text3>1</Text3>
        <SoftwareHouse.NextGen.Common.SecurityObjects.Credential ImportMode="Default">
        <CardNumber>358621</CardNumber>
        </SoftwareHouse.NextGen.Common.SecurityObjects.Credential>
        <SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair ImportMode="Default">
        <ClearanceKey>70001</ClearanceKey>
        </SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair>
        <SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair ImportMode="Default">
        <ClearanceKey>70002</ClearanceKey>
        </SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair>
        <SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair ImportMode="Default">
        <ClearanceKey>70003</ClearanceKey>
        </SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair>
        <SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair ImportMode="Default">
        <ClearanceKey>70004</ClearanceKey>
        </SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair>
        <SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair ImportMode="Default">
        <ClearanceKey>70005</ClearanceKey>
        </SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair>
    </SoftwareHouse.NextGen.Common.SecurityObjects.Personnel>
    <SoftwareHouse.NextGen.Common.SecurityObjects.Personnel ImportMode="Default">
        <FirstName>小華</FirstName>
        <LastName>	陳</LastName>
        <Text1>GG</Text1>
        <Text2>AKA</Text2>
        <Text3>2</Text3>
        <SoftwareHouse.NextGen.Common.SecurityObjects.Credential ImportMode="Default">
        <CardNumber>358622</CardNumber>
        </SoftwareHouse.NextGen.Common.SecurityObjects.Credential>
        <SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair ImportMode="Default">
        <ClearanceKey>70006</ClearanceKey>
        </SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair>
        <SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair ImportMode="Default">
        <ClearanceKey>70007</ClearanceKey>
        </SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair>
        <SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair ImportMode="Default">
        <ClearanceKey>70008</ClearanceKey>
        </SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair>
        <SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair ImportMode="Default">
        <ClearanceKey>70009</ClearanceKey>
        </SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair>
        <SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair ImportMode="Default">
        <ClearanceKey>70010</ClearanceKey>
        </SoftwareHouse.NextGen.Common.SecurityObjects.PersonnelClearancePair>
    </SoftwareHouse.NextGen.Common.SecurityObjects.Personnel>
    </CrossFire>
    ```
4. **使用** `Administration Workstation` > `Configration` > `Data Import` 的 `XML 模式` 將資料導入