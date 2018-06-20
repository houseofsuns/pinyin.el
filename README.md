# 汉字转拼音

## API

### `(pinyin HANZI &optional (STYLE 'TONE))`

``` emacs-lisp
(pinyin ?中)
;; => ("zhōng" "zhòng")

(pinyin ?中 'NORMAL)
;; => ("zhong" "zhong")

(pinyin ?中 'TONE2)
;; => ("zho1ng" "zho4ng")

(pinyin ?中 'TONE3)
;; => ("zhong1" "zhong4")

```

#### 拼音风格

| 风格   | 说明                                                       | 举例                |
|--------|------------------------------------------------------------|---------------------|
| NORMAL | 普通风格，不带声调                                         | 中国 -> zhong guo   |
| TONE   | 标准声调风格，拼音声调在韵母第一个字母上（默认风格）       | 中国 -> zhōng guó   |
| TONE2  | 声调风格2，即拼音声调在各个韵母之后，用数字 [1-4] 进行表示 | 中国 -> zho1ng guo2 |
| TONE3  | 声调风格3，即拼音声调在各个拼音之后，用数字 [1-4] 进行表示 | 中国 -> zhong1 guo2 |
