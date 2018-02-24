# WEB開発
## 1.WordPress
### 1.1 プラグイン
|名　称　|	機　能　|	備　考　|
|:------|:------|:------|
|TablePress	||	枠線を設定する場合は、VK ExUnitのCSSカスタマイズ部に[このコード](#枠線設定)を設定する|
|Child Pages Shortcode|||
|Contact Form 7	|||
|Flamingo|||
|Download Monitor|||
|Email Before Download|||
|Lightning Advanced Unit|||
|Lightning Copyright Customizer||有料|
|Lightning Variety||有料|
|TinyMCE Advanced|||
|TinyMCE テンプレート|||
|VK All in One Expansion Unit|||
|WP Multibyte Patch||　|
|画像ウィジェット|||

<a name="枠線設定"></a>
## 枠線設定
/ すべてのセルに枠線を付加する /
.tablepress thead th,
.tablepress tbody tr:first-child td,
.tablepress tbody td,
.tablepress tfoot th {
border: 1px solid black !important;
}
