<div align="center">

# WDS-Translation-Mod

使用frida實現對World Dai Star**安卓版本遊戲**的翻譯功能。

</div>

## 聲明
> [!WARNING]  
> 本倉庫內的代碼與資源僅供學習與參考。若使用者因使用本Mod而引發的任何直接或間接的後果、損失或法律責任，均與作者無關，由使用者自行承擔全部風險。

## 編譯方式

所需依賴:
```
Java
Node
Python
adb
frida-gadget 
apktool
```

執行
```shell
# Install dependencies
npm install
# Build dist/_.js
npm run build
# Build apks
py buildapk.py
```

## 安裝方式
```shell
# apks在 /apk/signed/ 資料夾下
adb install-multiple base_signed.apk config_signed.apk unity_signed.apk
```

## 配置

你可以使用以下方式進行該Mod的配置修改。
- 在首次運行後產生的`Android/data/包名/Moded/config.json`中
- 在[src/config.ts](https://github.com/Cpk0521/WDS-Translation-Mod/blob/main/src/config.ts#L11-L15)檔案中修改並重新編譯

配置說明:
| 名稱 | 說明 |
|---------------------|---------------------|
| isEnableTranslation | 是否啟用翻譯。 |
| TranslationPath | 翻譯csv文件的網址。**`{EPID}`為劇情id，必須填寫並大寫。** |

