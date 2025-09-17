# csv2xml

## 📖 簡介
此工具會將已填寫完成的 `.csv` 轉換為 **C-CURE** 格式的 `.xml`。  
建議在使用前，先於系統中完善以下物件：

- 🚪 `Door`
- 📁 `Group`
- 🧑‍🤝‍🧑 `GroupMember`
- 🪪 `Clearance`
- 📋 `ClearanceItem`

之後再透過本專案的輸出導入人員物件。

## ⚠️ 限制
目前僅支援最多 **`5` 個許可表** 的填入。

---

## 🚀 如何使用
1. **填寫** 📝 `Import_Personnel.csv`
   
    | 範例 | FirstName | LastName | CardNumber | Text1 | Text2  | Text3 | ClearanceKey1 | ClearanceKey2 | ClearanceKey3 | ClearanceKey4 | ClearanceKey5 |
    |----|-----------|----------|------------|-------|--------|-------|---------------|---------------|---------------|---------------|---------------|
    | 1  | 小明        | 王        | 358621     | EE    | LIT    | 1     | 70001         | 70002         | 70003         | 70004         | 70005         |
    | 2  | 小華        | 陳        | 358622     | GG    | AKA    | 2     | 70004         | 70005         | 70006         | 70007         | 70008         |

2. **執行** ▶️ `csv2xml.exe`  
3. **完成並輸出** 📂 `Import_Personnel.xml`
