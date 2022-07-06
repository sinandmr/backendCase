
# Deepcase Backend Developer Case


## API Kullanımı

#### Giriş Yap

```http
  POST /api/user/login
```

| Veri | Tip     | Açıklama                       |
| :-------- | :------- | :-------------------------------- |
| `username`      | `string` | Kullanıcı adı |
| `password`      | `string` | Şifre |

#### Kayıt Ol

```http
  POST /api/user/register
```

| Veri | Tip     | Açıklama                       |
| :-------- | :------- | :-------------------------------- |
| `name`      | `string` | İsim |
| `username`      | `string` | Kullanıcı adı |
| `password`      | `string` | Şifre |

---
#### Tüm ürünleri getir

```http
  GET /api/product
```

| Authorization | Tip     | Açıklama                |
| :-------- | :------- | :------------------------- |
| `Bearer Token` | `Token` | Login olduktan sonra verilen token |

#### Ürün Ekle

```http
  POST /api/product
```

| Authorization | Tip     | Açıklama                |
| :-------- | :------- | :------------------------- |
| `Bearer Token` | `Token` | Login olduktan sonra verilen token |

| Veri | Tip     | Açıklama                       |
| :-------- | :------- | :-------------------------------- |
| `name`      | `string` | Ürün adı |
| `price`      | `integer` | Ürün fiyatı |



#### Ürün Güncelle

```http
  PUT /api/product/:id
```

| Authorization | Tip     | Açıklama                |
| :-------- | :------- | :------------------------- |
| `Bearer Token` | `Token` | Login olduktan sonra verilen token |

| Veri | Tip     | Açıklama                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `integer` | Ürün ID (parametre olarak gönderilir) |
| `price`      | `integer` | Ürün fiyatı |
| `status`      | `string` | "active" veya "passive" değerlerini alır. |


#### Ürün Sil

```http
  DELETE /api/product/:id
```

| Authorization | Tip     | Açıklama                |
| :-------- | :------- | :------------------------- |
| `Bearer Token` | `Token` | Login olduktan sonra verilen token |

| Veri | Tip     | Açıklama                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `integer` | Ürün ID (parametre olarak gönderilir) |

  
## Kullanılan Teknolojiler

**Sunucu:** Node, Express, PostgreSQL

**Docker** ile deploy edildi.

  
## Bilgisayarınızda Çalıştırın

Projeyi klonlayın

```bash
  git clone https://github.com/sinandmr/backendCase.git
```

Proje dizinine gidin

```bash
  cd deepcase
```

Docker ile projeyi build edin

```bash
  docker build .
```

Tekrar docker ile compose build edin

```bash
  docker compose build
```

Gerekli image dosyalarını indirmek için de son olarak aşağıdaki komutu çalıştırın.

```bash
  docker compose up
```

Bu aşamadan sonra API endpointlerine **http://localhost:4000** adresinden ulaşabilirsiniz.
  
## Postman

```bash
  https://www.postman.com/collections/523f4523d18a4aecaa90
```

Yukarıdaki linki **Postman** uygulamasından **File -> Import -> Link** seçeneği ile import etmeniz gerekmektedir.
Bu sayede API'yi body verilerini yazmaya uğraşmadan kullanabilirsiniz.
  
