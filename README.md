# rp2040-zero-oscilloscope
[ken551](https://github.com/ken551/rp2040-zero-oscilloscope/)様の公開データに対して、パターンカット、空中配線が不要なように修正を実施。

[picoLabo](https://picolabo.org/)様によるRaspberry Pi Pico オシロスコープと同等のものを、Waveshare社の[RP2040-Zero](https://www.waveshare.com/wiki/RP2040-Zero)を使って実現する、RP2040-Zero-オシロスコープ の回路図です。

> [!CAUTION]
> 本バージョン基板（v1）は回路の**配線ミス**があり、**パターンカット・空中配線**が必須です。
>![](doc/img/patterncut.dio.svg)

上記パターンカット、空中配線の対策をKICAD回路図、配線修正を実施。

## **注意**
本バージョンの回路には**間違いがあります。**  
→間違いを回路図、配線に対して修正。
 間違いがある対象部品名についても、誤りと推測されるので修正。XC6201P332MR-G→XC6902N331MR-G

## 回路図
[picoLabo](https://picolabo.org/)様の[Raspberry Pi Pico用オシロスコープ基板DIYキット PL2302KIT](https://picolabo.org/pl2302kit/)をベースにしています。小サイズ化のため、ベースの回路図から以下のように変更しています。

* アナログ入力をAC/DC両対応からDCのみに限定
* デジタル入力を8ch→4chに削減
* 信号出力端子を削除

### 使用ライブラリ
* [RP2040-Zero-KiCAD](https://github.com/dj505/RP2040-Zero-KiCAD) (by @dj505)