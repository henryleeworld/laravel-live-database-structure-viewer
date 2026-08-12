# Laravel 13 即時資料庫結構描述檢視器

引入 albertoarena 的 laravel-truss 套件來擴增即時資料庫結構描述檢視器，資料庫結構描述是一種邏輯結構，該結構定義資料在資料庫中的組織方式，關聯式資料庫和某些非關聯式資料庫使用結構描述來描述其資料的結構、資料的互連以及內部程序。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 執行 __Artisan__ 指令的 __migrate__ 來執行所有未完成的遷移。
```sh
$ php artisan migrate
```
- 在瀏覽器中輸入已定義的路由 URL 來訪問，例如：http://127.0.0.1:8000。
- 你可以經由 `/truss` 來進行資料庫結構描述檢視。

----

## 畫面截圖
![](https://i.imgur.com/mWYrY8F.png)
> 掃描即時資料庫結構，並在內部直接渲染成可捲動、可縮放的實體關係圖，無需開啟任何資料庫用戶端，就能一眼看出資料表之間的實際連結
