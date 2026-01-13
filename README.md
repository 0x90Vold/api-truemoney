# 🧧 TrueMoney Voucher API

> **Api รับซอง TrueMoney**  
> ใช้งานง่าย รวดเร็ว ปลอดภัย ฟรี 100%

🌐 **Live Demo:** [https://twal.vibewithlukkid.xyz/](https://twal.vibewithlukkid.xyz/)

![Verify Engine](https://img.shields.io/badge/Verify-Engine-green?style=flat-square) ![Uptime](https://img.shields.io/badge/Uptime-99.9%25-success?style=flat-square) ![Developer](https://img.shields.io/badge/Developed_by-Lukkid-orange?style=flat-square)

---

## 📖 วิธีใช้งาน (Usage)

สามารถเรียกใช้งาน API ได้ง่ายๆ ผ่าน **GET Request**:

### 1. Endpoint

```http
GET /api/flow
```

### 2. Parameters (พารามิเตอร์)

| Parameter | Type   | Required | Description |
|-----------|--------|----------|-------------|
| `voucher` | String | ✅ Yes    | ลิงก์ซองของขวัญ (เช่น `https://gift.truemoney.com/...` หรือรหัสซอง) |
| `mobile`  | String | ✅ Yes    | เบอร์โทรศัพท์ที่จะรับเงิน (10 หลัก) |

### 3. ตัวอย่างการเรียกใช้ (Example)

**CURL:**
```bash
curl -X GET "https://twal.vibewithlukkid.xyz/api/flow?voucher={LINK_CODE}&mobile={phone}"
```

**JavaScript (Fetch):**
```javascript
const response = await fetch('https://twal.vibewithlukkid.xyz/api/flow?voucher=7iP...&mobile={phone}');
const data = await response.json();
console.log(data);
```

### 4. ตัวอย่าง Response (JSON)

```json
{
  "status": {
    "code": "SUCCESS",
    "message": "success"
  },
  "data": {
    "my_ticket": null,
    "owner_profile": {
      "full_name": "สมชาย ***"
    },
    "redeemer_profile": null,
    "tickets": [],
    "voucher": {
      "amount_baht": "100.00",
      "available": 1,
      "detail": "",
      "expire_date": 1767225600000,
      "link": "a1b2c3d4e5f6g7h8i9j0...",
      "member": 5,
      "redeemed": 2,
      "redeemed_amount_baht": "40.00",
      "status": "active",
      "type": "F",
      "voucher_id": "12345678901234567"
    }
  }
}
```

---
<p align="center">
  © 2026 Developed by <strong>Lukkid</strong> • 100% Free
</p>
