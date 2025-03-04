# 見出し1
## 見出し2
### 見出し3
#### 見出し4
##### 見出し5
###### 見出し6

## 引用

> 引用です。  
> 引用です。
>
>> 二重引用です。  
>> 二重引用です。

## 警告文

!!! Note
    これはノートです。

!!! Tip
    ヒントです。

!!! Warning
    これは警告です
    
!!! Danger
    これは危険です。

!!! Success
    これは成功です。

!!! Failure
    これは失敗です。

!!! Bug
    これはバグです。

!!! summary
    これは概要です。

## コード記法

### 短文・単語単位
`新しい朝が来た`  

### 複数行
```
新しい朝が来た
希望の朝だ喜びに胸を開け
大空あおげラジオの声に
健やかな胸をこの香る風に
開けよそれ
```

## 文字修飾

改行は末尾に半角スペースを2文字入れます。  
*italic* または _斜文字_  
**bold** または __太字__  
***bold*** または ___強調___

## 水平線

***
アスタリスクを3つ  

---
ハイフンを3つ  

___
アンダースコアを3つ  

## リンク

[表示文字](リンクURL "Title属性")でリンクを記述できます  
[定義文字]:URL "Title属性"で定義参照も出来ます  

[google](https://www.google.co.jp/ "ぐーぐる")と[yahoo](https://www.yahoo.co.jp/ "やふー")  
[あっちにgoogle][google]（その他の文章）[こっちにyahoo][yahoo]  
URL( https://www.google.co.jp/ )だけではリンクは作成されない。  
サイト内は[mdファイル](index.md)の指定で変換できます。

[google]: https://www.google.co.jp/ "ぐーぐるさん"
[yahoo]: https://www.yahoo.co.jp/ (やふーさん)

## テーブル

markdown形式
| header1 | header2 | header3 |
|---|---|
| a | b | c |

| First Header | Second Header | Third Header |
| ------------ | ------------- | ------------ |
| Content Cell | Content Cell  | Content Cell |
| Content Cell | Content Cell  | Content Cell |

| First Header | Second Header | Third Header |
| ------------ | ------------- | ------------ |
| Content Cell | Content Cell  | Content Cell<br>改行 |
| Content Cell | Content Cell  | Content Cell |

## 画像

![alt文字列](画像URL “title文字列”)で画像が表示されます。
ハイパーリンクと同じように外部参照も利用できます。

![赤](docs/img/sample_red.png "赤色")

![青][blue]
[blue]:docs/img/sample_blue.png "青色"

[![緑](docs/img/sample_green.png "緑色ファイルにリンク")](docs/img/sample_green.png)

[![黄](docs/img/sample_yellow.png "黄色ファイルにリンク")][yellow]
[yellow]: docs/img/sample_yellow.png "黄色"

## キーボードアイコン

[指定できるキーコードの参考](https://facelessuser.github.io/pymdown-extensions/extensions/keys/)

```bash
++ctrl+alt+delete++
```
++ctrl+alt+delete++

## コードハイライト

```python
def greeting():
    print("Hello, World")
greeting()
```