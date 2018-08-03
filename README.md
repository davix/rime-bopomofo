# 原生注音

配方： ℞ **`bopomofo-native`**

[Rime自帶的注音輸入方案](https://github.com/rime/rime-bopomofo)依賴漢語拼音方案。其表面使用註音符號，內部實現是將其轉換爲拼音，並使用拼音碼表找字。

通常使用沒問題。但由於內部使用拼音，
- 按鍵實際爲英文字母。在大千式佈局下輸入“勹”，回車後爲“1”。不像拼音那樣內外一致。
- bopomofo方案內部需將註音轉換爲拼音。只知註音不知拼音的方案設計者修改scheme時很難理解，或需學習拼音才行。
- 拼音是在註音基礎上使用英文字母的方案。有若干特殊簡化規則，如`iou = iu`, 如`y, w`等。內部直接使用註音更簡單。
- 註音本質上無需依賴拼音。

`bopomofo-native`是原生的不基於拼音的Rime註音方案。它採用獨立的基於註音符號的碼表。

碼表是在[地球拼音](https://github.com/rime/rime-terra-pinyin)的基礎上，將拼音轉化爲註音而成。

## 安裝

本方案不依賴任何拼音方案

[東風破](https://github.com/rime/plum) 安裝口令： `bash rime-install davix/rime-bopomofo-native`

授權條款：見 [LICENSE](LICENSE)
