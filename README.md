# nRF54L15評価F/W開発 (BLEデバイス)

## 開発環境

- 開発言語 ... C言語
- RTOS ... [Zephyr](https://www.zephyrproject.org/)🔗
- ツールチェイン ... [nRF Connect SDK Toolchain V3.1.1](https://github.com/nrfconnect/sdk-nrf/releases/tag/v3.1.1)🔗
- SDK ... [nRF Connect SDK V3.1.1](https://github.com/nrfconnect/sdk-nrf/releases/tag/v3.1.1)🔗
- ライブラリ ... [platform-seeedboards](https://github.com/Seeed-Studio/platform-seeedboards)🔗

## nRF54L15のスペック

> [!IMPORTANT]
> リファレンスはNordic作成の[データシート Ver1.0](https://docs-be.nordicsemi.com/bundle/ps_nrf54L15/page/pdf/nRF54L15_nRF54L10_nRF54L05_Datasheet_v1.0.pdf)🔗


- SoC
  - [nRF54L15](https://www.nordicsemi.jp/products/nrf54l15)🔗
    - 📍**CPU**📊
      - **メイン** ... **ARM Cortex-M33** @128 MHz📊
        - FPU ... **単精度FPU**📊
      - **コプロセッサ** ... FLPR VFP (**RISC-V RV32EMC**)  @128 MHz📊
    - **📍メモリ💾**
      - **NVM ... 1.5 MB💾**
      - SRAM ... 256 KB💾
    - **📍無線機能🛜**
      - **BLE 6.0**🛜
      - **NFC🛜**
      - **Thread🛜**
      - **Zigbee🛜**
      - **Matter🛜**
      - Amazon Sidewalk🛜
      - Nordic独自2.4 GHzプロトコル🛜
    - **📍ペリフェラル機能⚡**
      - **GPIO** x35本⚡
      - **PWM** x3ch (各4本)⚡
      - **DMA** x14チャネル⚡
      - **I2C**(TWI) x4本 @400 KHz⚡
      - **SPI** x2本⚡
        - HS-SPI x1本 @32 MHz⚡
        - 標準SPI x1本⚡
      - **UART** x2本⚡
        - HS-UART x1本 @4 Mbps⚡
        - 標準UART x1本⚡
      - **I2S** x2本⚡
      - **ADC** x8本⚡
        - モード(４モード搭載)
          - 10bit @2 Msps
          - 12bit @250 ksps
          - 14bit @31.25 ksps
          - 設定可能なオーバーサンプリングレート
      - ~~**DAC**~~ N/A⚡
      - **タイマー** x5本⏰️
        - **汎用タイマー** x4本 ⏰️
          - 8 / 16 / 24 / 32bitで可変
        - **WDT** x2本🐶⏰️
        - **RTC** x1本⏰️
      - **暗号機能** 🔐
        - CRACEN (Cryptographic accelerator engine)
          - **AES 128 / 192 / 256-bit**機能🔐
          - **ハッシュ関数** (MD5 / SHA1 / SHA224 / SHA256 / SHA384 / SHA512 / HMAC)機能🔐
          - **公開鍵暗号化エンジン(PKE)** 機能🔐
          - **公開鍵生成(IKG)** 機能🔐
          - **ECC (楕円曲線暗号)** 機能🔐
          - **RNG (乱数生成器)** 機能🔐
            - ⚠️PRNGの疑似乱数か、TRNGの真性乱数かは記載なくどっちか不明

## 参考文献

- [Seeed Studio XIAO nRF54L15(Sense) 入門ガイド](https://wiki.seeedstudio.com/ja/xiao_nrf54l15_sense_getting_started/)🔗
- [nRF Connect SDK 環境構築方法(V3.0.0編)](https://www.kgdev.co.jp/column/nordic-column0048/)🔗
- [nRF54L15 開発導入情報](https://www.kgdev.co.jp/column/nordic-column0050/)🔗
