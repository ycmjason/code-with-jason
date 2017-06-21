# 咩係 coding?
Coding （又或者叫「寫 program」、「programming」）係一種特異功能，學識左你就可以命令電腦做哂所有重複垃雜野，解決日常遇到的問題，實踐你的發達大計，拓展新生活，升職加人工，買車買樓。（利申：我乜都買唔起）

Coding 其實就係寫一堆 instructions 叫電腦做野 。而果堆 instructions 就叫做 code。你喺電腦見到的一切，背後都係由一堆 code 去控制。

Coding 可以用唔同的 programming language 。而唔同的 programming language，分別就在於唔同的syntax、寫法、思考方式，但係最終都可以解決同一個問題。

唔明？等我拿個貼身啲的比喻，繁體中文「我愛你」同簡體中文「我爱你」，意思一樣，但係寫法、讀法等等就唔同了。

想知多啲？睇下面extra reading啦！

--------------------------------

## Extra reading

### Machine code
電腦其實好蠢，識做的野好少。電腦只係識分 1 同 0，好好好簡單咁講，條電線有電就係 1 ，冇電就係 0。

我地成日見到電腦有分 32-bit 同 64-bit，其實就係講緊一個 instruction 用幾多個 bit 去表達（即係用幾多個 0 同 1）。例如，如果我地有部 5-bit 電腦，果啲 instructions 可能就會係：
```
Our 5-bit instruction set:
0xxyy - xx + yy
1xxyy - xx * yy
```

當然，xx 同 yy 會係 binary（二進制）。

跟據我地的 instruction set，`00110` 就代表緊 `01 + 10 = 11 = 3` 了。

More examples:
```
01100 - 11 + 00 = 3 + 0 = 3
10101 - 01 * 01 = 1 * 1 = 1
11111 - 11 * 11 = 3 * 3 = 9
...
```

呢啲用 0 同 1 去組成的 instructions，叫做 machine code，係唯一電腦睇得明的野。

### Programming languages
見到果啲 1010 係咪好唔開胃呢？因為 machine code 太難用了，所以有其他比較容易明白的 programming languages。果啲 programming language 寫完之後電腦係唔能夠理解的，要把佢地 compile 去 machine code，者係翻譯做 machine code，電腦先識得點 run。

我地可以自己發明一套 programming language 俾上面的 instruction set：
```
ADD a b - 0(a)(b)
MUL a b - 1(a)(b)
```
呢次 `a` 同 `b` 係正常數字，而 `(a)` 同 `(b)` 就係佢地的 binary。

`ADD 1 2` 用番我地上面的 instruction set，compile 左之後就會係 `00110` 了。
