# UHD630 FrameBuffer Patch

## Overview


|        | Port                | Index       | Type        | Bus ID | Bus ID | Bus ID | Bus ID | Bus ID | Bus ID | Bus ID | Bus ID | Bus ID | Bus ID | Bus ID | Bus ID | Bus ID | Bus ID | Bus ID | Bus ID | Bus ID | Bus ID | Bus ID | Bus ID |
| :----- | :------------------ | :---------- | :---------- | :----- | :----- | :----- | :----- | :----- | :----- | :----- | :----- | :----- | :----- | :----- | :----- | :----- | :----- | :----- | :----- | :----- | :----- | :----- | :----- |
|        | 0x05                | 3           | DP          | 0x01   | 0x02   | 0x01   | 0x01   | 0x01   | 0x02   | 0x02   | 0x02   | 0x04   | 0x04   | 0x04   | 0x04   | 0x05   | 0x05   | 0x05   | 0x05   | 0x06   | 0x06   | 0x06   | 0x06   |
|        | 0x06                | 1           | HDMI        | 0x02   | 0x01   | 0x04   | 0x05   | 0x06   | 0x04   | 0x05   | 0x06   | 0x01   | 0x02   | 0x05   | 0x06   | 0x01   | 0x02   | 0x04   | 0x06   | 0x01   | 0x02   | 0x04   | 0x05   |
|        | 0x07                | 2           | HDMI        | 0x06   | 0x06   | 0x02   | 0x02   | 0x02   | 0x01   | 0x01   | 0x01   | 0x02   | 0x01   | 0x01   | 0x01   | 0x02   | 0x01   | 0x01   | 0x01   | 0x02   | 0x01   | 0x01   | 0x01   |
| Remark | Port 0x05,0x06,0x07 | Index 1,2,3 | HDMI/DP/DVI | X      | X      | V      | V      | V      | X      | X      | X      | X      | V      | X      | X      | X      | V      | X      | X      | X      | V      | X      | X      |

## Single Monitor

```plist
<key>PciRoot(0x0)/Pci(0x2,0x0)</key>
<dict>
  <key>AAPL,ig-platform-id</key>
  <data>BwCbPg==</data>
  <key>AAPL,slot-name</key>
  <string>Internal@0,2,0</string>
  <key>device-id</key>
  <data>mD4AAA==</data>
  <key>device_type</key>
  <string>VGA compatible controller</string>
  <key>enable-hdmi-dividers-fix</key>
  <data>AQAAAA==</data>
  <key>enable-hdmi20</key>
  <data>AQAAAA==</data>
  <key>enable-lspcon-support</key>
  <data>AQAAAA==</data>
  <key>framebuffer-con0-busid</key>
  <data>AgAAAA==</data>
  <key>framebuffer-con0-enable</key>
  <data>AQAAAA==</data>
  <key>framebuffer-con0-index</key>
  <data>AgAAAA==</data>
  <key>framebuffer-con0-pipe</key>
  <data>EgAAAA==</data>
  <key>framebuffer-con0-type</key>
  <data>AAgAAA==</data>
  <key>framebuffer-con1-enable</key>
  <data>AQAAAA==</data>
  <key>framebuffer-con1-index</key>
  <data>AwAAAA==</data>
  <key>framebuffer-con1-pipe</key>
  <data>EgAAAA==</data>
  <key>framebuffer-con2-busid</key>
  <data>AQAAAA==</data>
  <key>framebuffer-con2-enable</key>
  <data>AQAAAA==</data>
  <key>framebuffer-con2-has-lspcon</key>
  <data>AQAAAA==</data>
  <key>framebuffer-con2-index</key>
  <data>AQAAAA==</data>
  <key>framebuffer-con2-pipe</key>
  <data>EgAAAA==</data>
  <key>framebuffer-con2-preferred-lspcon-mode</key>
  <data>AQAAAA==</data>
  <key>framebuffer-patch-enable</key>
  <data>AQAAAA==</data>
  <key>framebuffer-unifiedmem</key>
  <data>AAAAgA==</data>
  <key>hda-gfx</key>
  <string>onboard-2</string>
  <key>model</key>
  <string>Intel UHD Graphics 630</string>
</dict>
```

## Dual Monitor

### 3e9b0000

 > Note: There is a brief splash screen when the main monitor is switched on and off

  ```plist
  <key>PciRoot(0x0)/Pci(0x2,0x0)</key>
  <dict>
    <key>AAPL,GfxYTile</key>
    <data>AQAAAA==</data>
    <key>AAPL,ig-platform-id</key>
    <data>AACbPg==</data>
    <key>AAPL,slot-name</key>
    <string>Internal@0,2,0</string>
    <key>device-id</key>
    <data>mz4AAA==</data>
    <key>device_type</key>
    <string>VGA compatible controller</string>
    <key>enable-hdmi-dividers-fix</key>
    <data>AQAAAA==</data>
    <key>enable-hdmi20</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-busid</key>
    <data>BAAAAA==</data>
    <key>framebuffer-con0-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-flags</key>
    <data>mAAAAA==</data>
    <key>framebuffer-con0-index</key>
    <data>AAAAAA==</data>
    <key>framebuffer-con0-pipe</key>
    <data>EgAAAA==</data>
    <key>framebuffer-con0-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con1-busid</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con1-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con1-flags</key>
    <data>hwEAAA==</data>
    <key>framebuffer-con1-index</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con1-pipe</key>
    <data>EgAAAA==</data>
    <key>framebuffer-con1-type</key>
    <data>AAQAAA==</data>
    <key>framebuffer-con2-busid</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con2-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-flags</key>
    <data>hwEAAA==</data>
    <key>framebuffer-con2-index</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con2-pipe</key>
    <data>EgAAAA==</data>
    <key>framebuffer-con2-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-fbmem</key>
    <data>AAAAAA==</data>
    <key>framebuffer-patch-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-stolenmem</key>
    <data>AACQAw==</data>
    <key>framebuffer-unifiedmem</key>
    <data>AAAAgA==</data>
    <key>hda-gfx</key>
    <string>onboard-1</string>
    <key>model</key>
    <string>Intel UHD Graphics 630</string>
  </dict>
  ```

### 3e9b0007

> Note: Not perfect, the HDMI output screen has a green screen for about one second during startup.

- `config-9b-01-04-02`

  ```plist
  <key>PciRoot(0x0)/Pci(0x2,0x0)</key>
  <dict>
    <key>AAPL,ig-platform-id</key>
    <data>BwCbPg==</data>
    <key>AAPL,slot-name</key>
    <string>Internal@0,2,0</string>
    <key>device-id</key>
    <data>mz4AAA==</data>
    <key>device_type</key>
    <string>VGA compatible controller</string>
    <key>enable-hdmi20</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-busid</key>
    <data>BAAAAA==</data>
    <key>framebuffer-con0-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-index</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con1-busid</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con1-index</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con2-busid</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-index</key>
    <data>AwAAAA==</data>
    <key>framebuffer-con2-type</key>
    <data>AAQAAA==</data>
    <key>framebuffer-patch-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-unifiedmem</key>
    <data>AAAAgA==</data>
    <key>model</key>
    <string>Intel UHD Graphics 630</string>
  </dict>
  ```

- `config-9b-01-05-02`

  ```plist
  <key>PciRoot(0x0)/Pci(0x2,0x0)</key>
  <dict>
    <key>AAPL,ig-platform-id</key>
    <data>BwCbPg==</data>
    <key>AAPL,slot-name</key>
    <string>Internal@0,2,0</string>
    <key>device-id</key>
    <data>mz4AAA==</data>
    <key>device_type</key>
    <string>VGA compatible controller</string>
    <key>enable-hdmi20</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-busid</key>
    <data>BQAAAA==</data>
    <key>framebuffer-con0-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-index</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con1-busid</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con1-index</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con2-busid</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-index</key>
    <data>AwAAAA==</data>
    <key>framebuffer-con2-type</key>
    <data>AAQAAA==</data>
    <key>framebuffer-patch-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-unifiedmem</key>
    <data>AAAAgA==</data>
    <key>model</key>
    <string>Intel UHD Graphics 630</string>
  </dict>
  ```

- `config-9b-01-06-02`

  ```plist
  <key>PciRoot(0x0)/Pci(0x2,0x0)</key>
  <dict>
    <key>AAPL,ig-platform-id</key>
    <data>BwCbPg==</data>
    <key>AAPL,slot-name</key>
    <string>Internal@0,2,0</string>
    <key>device-id</key>
    <data>mz4AAA==</data>
    <key>device_type</key>
    <string>VGA compatible controller</string>
    <key>enable-hdmi20</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-busid</key>
    <data>BgAAAA==</data>
    <key>framebuffer-con0-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-index</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con1-busid</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con1-index</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con2-busid</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-index</key>
    <data>AwAAAA==</data>
    <key>framebuffer-con2-type</key>
    <data>AAQAAA==</data>
    <key>framebuffer-patch-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-unifiedmem</key>
    <data>AAAAgA==</data>
    <key>model</key>
    <string>Intel UHD Graphics 630</string>
  </dict>
  ```

- `config-9b-04-02-01`

  ```plist
  <key>PciRoot(0x0)/Pci(0x2,0x0)</key>
  <dict>
    <key>AAPL,ig-platform-id</key>
    <data>BwCbPg==</data>
    <key>AAPL,slot-name</key>
    <string>Internal@0,2,0</string>
    <key>device-id</key>
    <data>mz4AAA==</data>
    <key>device_type</key>
    <string>VGA compatible controller</string>
    <key>enable-hdmi20</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-busid</key>
    <data>BAAAAA==</data>
    <key>framebuffer-con0-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-index</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-type</key>
    <data>AAQAAA==</data>
    <key>framebuffer-con1-busid</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con1-index</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con2-busid</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-index</key>
    <data>AwAAAA==</data>
    <key>framebuffer-con2-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-patch-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-unifiedmem</key>
    <data>AAAAgA==</data>
    <key>model</key>
    <string>Intel UHD Graphics 630</string>
  </dict>
  ```

- `config-9b-05-02-01`

  ```plist
  <key>PciRoot(0x0)/Pci(0x2,0x0)</key>
  <dict>
    <key>AAPL,ig-platform-id</key>
    <data>BwCbPg==</data>
    <key>AAPL,slot-name</key>
    <string>Internal@0,2,0</string>
    <key>device-id</key>
    <data>mz4AAA==</data>
    <key>device_type</key>
    <string>VGA compatible controller</string>
    <key>enable-hdmi20</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-busid</key>
    <data>BQAAAA==</data>
    <key>framebuffer-con0-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-index</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-type</key>
    <data>AAQAAA==</data>
    <key>framebuffer-con1-busid</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con1-index</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con2-busid</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-index</key>
    <data>AwAAAA==</data>
    <key>framebuffer-con2-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-patch-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-unifiedmem</key>
    <data>AAAAgA==</data>
    <key>model</key>
    <string>Intel UHD Graphics 630</string>
  </dict>
  ```

- `config-9b-06-02-01`

  ```plist
  <key>PciRoot(0x0)/Pci(0x2,0x0)</key>
  <dict>
    <key>AAPL,ig-platform-id</key>
    <data>BwCbPg==</data>
    <key>AAPL,slot-name</key>
    <string>Internal@0,2,0</string>
    <key>device-id</key>
    <data>mz4AAA==</data>
    <key>device_type</key>
    <string>VGA compatible controller</string>
    <key>enable-hdmi20</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-busid</key>
    <data>BgAAAA==</data>
    <key>framebuffer-con0-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-index</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-type</key>
    <data>AAQAAA==</data>
    <key>framebuffer-con1-busid</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con1-index</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con2-busid</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-index</key>
    <data>AwAAAA==</data>
    <key>framebuffer-con2-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-patch-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-unifiedmem</key>
    <data>AAAAgA==</data>
    <key>model</key>
    <string>Intel UHD Graphics 630</string>
  </dict>
  ```

- `config-98-01-04-02`

  ```plist
  <key>PciRoot(0x0)/Pci(0x2,0x0)</key>
  <dict>
    <key>AAPL,ig-platform-id</key>
    <data>BwCbPg==</data>
    <key>AAPL,slot-name</key>
    <string>Internal@0,2,0</string>
    <key>device-id</key>
    <data>mD4AAA==</data>
    <key>device_type</key>
    <string>VGA compatible controller</string>
    <key>enable-hdmi20</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-busid</key>
    <data>BAAAAA==</data>
    <key>framebuffer-con0-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-index</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con1-busid</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con1-index</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con2-busid</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-index</key>
    <data>AwAAAA==</data>
    <key>framebuffer-con2-type</key>
    <data>AAQAAA==</data>
    <key>framebuffer-patch-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-unifiedmem</key>
    <data>AAAAgA==</data>
    <key>model</key>
    <string>Intel UHD Graphics 630</string>
  </dict>
  ```

- `config-98-01-05-02`

  ```plist
  <key>PciRoot(0x0)/Pci(0x2,0x0)</key>
  <dict>
    <key>AAPL,ig-platform-id</key>
    <data>BwCbPg==</data>
    <key>AAPL,slot-name</key>
    <string>Internal@0,2,0</string>
    <key>device-id</key>
    <data>mD4AAA==</data>
    <key>device_type</key>
    <string>VGA compatible controller</string>
    <key>enable-hdmi20</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-busid</key>
    <data>BQAAAA==</data>
    <key>framebuffer-con0-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-index</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con1-busid</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con1-index</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con2-busid</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-index</key>
    <data>AwAAAA==</data>
    <key>framebuffer-con2-type</key>
    <data>AAQAAA==</data>
    <key>framebuffer-patch-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-unifiedmem</key>
    <data>AAAAgA==</data>
    <key>model</key>
    <string>Intel UHD Graphics 630</string>
  </dict>
  ```

- `config-98-01-06-02`

  ```plist
  <key>PciRoot(0x0)/Pci(0x2,0x0)</key>
  <dict>
    <key>AAPL,ig-platform-id</key>
    <data>BwCbPg==</data>
    <key>AAPL,slot-name</key>
    <string>Internal@0,2,0</string>
    <key>device-id</key>
    <data>mD4AAA==</data>
    <key>device_type</key>
    <string>VGA compatible controller</string>
    <key>enable-hdmi20</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-busid</key>
    <data>BgAAAA==</data>
    <key>framebuffer-con0-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-index</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con1-busid</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con1-index</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con2-busid</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-index</key>
    <data>AwAAAA==</data>
    <key>framebuffer-con2-type</key>
    <data>AAQAAA==</data>
    <key>framebuffer-patch-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-unifiedmem</key>
    <data>AAAAgA==</data>
    <key>model</key>
    <string>Intel UHD Graphics 630</string>
  </dict>
  ```

- `config-98-04-02-01`

  ```plist
  <key>PciRoot(0x0)/Pci(0x2,0x0)</key>
  <dict>
    <key>AAPL,ig-platform-id</key>
    <data>BwCbPg==</data>
    <key>AAPL,slot-name</key>
    <string>Internal@0,2,0</string>
    <key>device-id</key>
    <data>mD4AAA==</data>
    <key>device_type</key>
    <string>VGA compatible controller</string>
    <key>enable-hdmi20</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-busid</key>
    <data>BAAAAA==</data>
    <key>framebuffer-con0-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-index</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-type</key>
    <data>AAQAAA==</data>
    <key>framebuffer-con1-busid</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con1-index</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con2-busid</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-index</key>
    <data>AwAAAA==</data>
    <key>framebuffer-con2-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-patch-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-unifiedmem</key>
    <data>AAAAgA==</data>
    <key>model</key>
    <string>Intel UHD Graphics 630</string>
  </dict>
  ```

- `config-98-05-02-01`

  ```plist
  <key>PciRoot(0x0)/Pci(0x2,0x0)</key>
  <dict>
    <key>AAPL,ig-platform-id</key>
    <data>BwCbPg==</data>
    <key>AAPL,slot-name</key>
    <string>Internal@0,2,0</string>
    <key>device-id</key>
    <data>mD4AAA==</data>
    <key>device_type</key>
    <string>VGA compatible controller</string>
    <key>enable-hdmi20</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-busid</key>
    <data>BQAAAA==</data>
    <key>framebuffer-con0-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-index</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-type</key>
    <data>AAQAAA==</data>
    <key>framebuffer-con1-busid</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con1-index</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con2-busid</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-index</key>
    <data>AwAAAA==</data>
    <key>framebuffer-con2-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-patch-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-unifiedmem</key>
    <data>AAAAgA==</data>
    <key>model</key>
    <string>Intel UHD Graphics 630</string>
  </dict>
  ```

- `config-98-06-02-01`

  ```plist
  <key>PciRoot(0x0)/Pci(0x2,0x0)</key>
  <dict>
    <key>AAPL,ig-platform-id</key>
    <data>BwCbPg==</data>
    <key>AAPL,slot-name</key>
    <string>Internal@0,2,0</string>
    <key>device-id</key>
    <data>mD4AAA==</data>
    <key>device_type</key>
    <string>VGA compatible controller</string>
    <key>enable-hdmi20</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-busid</key>
    <data>BgAAAA==</data>
    <key>framebuffer-con0-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-index</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con0-type</key>
    <data>AAQAAA==</data>
    <key>framebuffer-con1-busid</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con1-index</key>
    <data>AgAAAA==</data>
    <key>framebuffer-con1-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-con2-busid</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-con2-index</key>
    <data>AwAAAA==</data>
    <key>framebuffer-con2-type</key>
    <data>AAgAAA==</data>
    <key>framebuffer-patch-enable</key>
    <data>AQAAAA==</data>
    <key>framebuffer-unifiedmem</key>
    <data>AAAAgA==</data>
    <key>model</key>
    <string>Intel UHD Graphics 630</string>
  </dict>
  ```