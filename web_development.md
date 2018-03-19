# WEB開発
## 1.WordPress
### 1.1 プラグイン
|名　称　|	機　能　|	備　考　|
|:------|:------|:------|
|TablePress	||	枠線を設定する場合は、VK ExUnitのCSSカスタマイズ部に[このコード（枠線設定）](#枠線設定)を設定する|
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
## 2.スパム対策
### 2.1 添付ファイルページを使ったスパムメール
- WordPressでは「メディア」や投稿画面の「メディアを追加」から挿入した画像は自動的に添付ファイルページが作られ、個別のページとして表示ができるようになる。このため、このページへのコメントが許可される状態となってしまう。コメントをできないようにするため、「添付ファイルページにアクセスされても添付元の投稿などにリダイレクト（自動的に移動）するようにする」という対策をおこなう。
- 具体的にはattachment.php（添付ファイルテンプレート）を追加する。
- 記述コードは以下

~~~
<?php
//添付元（投稿、ページなど）のある添付ファイルページの場合、添付元にリダイレクト
if ( $post->post_parent ) {
	wp_redirec( get_permalink( $post->post_parent ), 301 );
}
//添付元（投稿、ページなど）のない添付ファイルページの場合、トップページにリダイレクト
else {
	wp_redirect( home_url(), 302 );
}
~~~

<a name="枠線設定"></a>
## 枠線設定
/ すべてのセルに枠線を付加する /
.tablepress thead th,
.tablepress tbody tr:first-child td,
.tablepress tbody td,
.tablepress tfoot th {
border: 1px solid black !important;
}
