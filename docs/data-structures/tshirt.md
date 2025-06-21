### Fit

| attribute_name       | type | description                         |
|----------------------|------|-------------------------------------|
| total_length         | Map  | 衣服の後ろ中心から裾までの長さ      |
| chest_width          | Map  | 両脇下の幅（胸囲）                  |
| bottom_width         | Map  | 裾部分の幅                          |
| sleeve_length        | Map  | 肩先から袖口までの長さ              |
| armhole              | Map  | 袖ぐりの周囲長                      |
| sleeve_opening       | Map  | 袖口の幅                            |
| neck_rib_length      | Map  | 襟リブ部分の幅                      |
| neck_opening         | Map  | 襟ぐりの開き幅                      |
| shoulder_to_shoulder | Map  | 左右肩先間の直線距離                |
| description          | Map  | 備考                                |

=== "total_length"

    ```ts
    total_length: {
        xss: number, xs: number, s: number, m: number, l: number, xl: number, xxl: number
    }
    ```

=== "chest_width"

    ```ts
    chest_width: {
        xss: number, xs: number, s: number, m: number, l: number, xl: number, xxl: number
    }
    ```

=== "bottom_width"

    ```ts
    bottom_width: {
        xss: number, xs: number, s: number, m: number, l: number, xl: number, xxl: number
    }
    ```

=== "sleeve_length"

    ```ts
    sleeve_length: {
        xss: number, xs: number, s: number, m: number, l: number, xl: number, xxl: number
    }
    ```

=== "armhole"

    ```ts
    armhole: {
        xss: number, xs: number, s: number, m: number, l: number, xl: number, xxl: number
    }
    ```

=== "sleeve_opening"

    ```ts
    sleeve_opening: {
        xss: number, xs: number, s: number, m: number, l: number, xl: number, xxl: number
    }
    ```

=== "neck_rib_length"

    ```ts
    neck_rib_length: {
        xss: number, xs: number, s: number, m: number, l: number, xl: number, xxl: number
    }
    ```

=== "shoulder_to_shoulder"

    ```ts
    armhole: {
        xss: number, xs: number, s: number, m: number, l: number, xl: number, xxl: number
    }
    ```

=== "description"

    ```ts
    description: {
        description: "string",
        file: {
            name: "string",
            key: "string"
        }
    }
    ```


### Fabric

| attribute_name | type | description |
| -------------- | ---- | ----------- |
| materials | List | 最大3つまで |
| sub_materials | List | 最大3つまで |

=== "materials"

    ```ts
    materials: {
        row_material: "string",
        thickness: "string",
        colourway: {
            pantone: "string",
            hex: "string"
        },
        description: {
            description: "string",
            file: {
                name: "string",
                key: "string"
            }
        }
    }[]
    ```

=== "sub_materials"

    ```ts
    materials: {
        row_material: "string",
        colourway: {
            pantone: "string",
            hex: "string"
        },
        description: {
            description: "string",
            file: {
                name: "string",
                key: "string"
            }
        }
    }[]
    ```

### Tag

| attribute_name | type | description |
| -------------- | ---- | ----------- |
| is_label | Bool | ラベルを作成するか |
| send_label | Bool | ラベルを工場へ発送するか |
| is_custom | Bool | サイズをカスタムするか |
| material | String | |
| colourway | Map | |
| label_style | Bool | ラベルのスタイル |
| description | Map | |

=== "colourway"

    ```ts
    colourway: {
        pantone: "string",
        hex: "string"
    }
    ```

=== "description"

    ```ts
    description: {
        description: "string",
        file: {
            name: "string",
            key: "string"
        }
    }
    ```

### Care Label

| attribute_name | type | description |
| -------------- | ---- | ----------- |
| has_logo | Bool | ロゴをつけるか |
| default_logo | Bool | デフォルトのロゴか |
| file | Map | ロゴファイル |
| description | Map | 備考 |

### OEM Points

| attribute_name | type | description |
| -------------- | ---- | ----------- |
| oem_points | List | 最大3つまで |

=== "oem_points"

    ```ts
    oem_points: {
        oem_point: "string",
        file: {
            name: "string",
            key: "string"
        }
    }[]
    ```

### Sample

| attribute_name | type | description |
| -------------- | ---- | ----------- |
| sample | Bool | サンプルの作成有無 |
| quantity | Map | 発注量 |

=== "quantity"

    ```ts
    quantity: {
        xss: number, xs: number, s: number, m: number, l: number, xl: number, xxl: number
    }
    ```

### Main Production

| attribute_name | type | description |
| -------------- | ---- | ----------- |
| quantity | Map | 発注量 |
| delivery_date | String | 納期（YYYY/MM/DD） |

=== "quantity"

    ```ts
    quantity: {
        xss: number, xs: number, s: number, m: number, l: number, xl: number, xxl: number
    }
    ```

### Information

| attribute_name | type | description |
| -------------- | ---- | ----------- |
| contact| Map | 連絡先情報 |
| billing_address | Map | 請求先住所 |
| shipping_address | Map | 配送先住所 |

=== "contact"

    ```ts
    contact: {
        first_name: "string",
        last_name: "string",
        phone_number: "string",
        email: "string"
    }
    ```

=== "billing_address"

    ```ts
    billing_address: {
        country: "string",
        state: "string",
        city: "string",
        address_line_1: "string",
        address_line_2: "string",
        zip_code: "string"
    }
    ```

=== "shipping_address"

    ```ts
    shipping_address: {
        country: "string",
        state: "string",
        city: "string",
        address_line_1: "string",
        address_line_2: "string",
        zip_code: "string"
    }
    ```