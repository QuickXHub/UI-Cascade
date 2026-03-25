<div align="center">

  <img src="https://img.shields.io/github/v/release/QuickXHub/UI-Cascade?style=for-the-badge&color=00ff9d" alt="Latest Release" />
  <img src="https://img.shields.io/github/stars/QuickXHub/UI-Cascade?style=for-the-badge&color=ff69b4" alt="Stars" />
  <img src="https://img.shields.io/github/forks/QuickXHub/UI-Cascade?style=for-the-badge&color=00bfff" alt="Forks" />
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge" alt="License" />

  <h1>🌊 UI Cascade</h1>
  <p><strong>UI Library สำหรับ Roblox ที่สวยแบบ macOS Sequoia</strong><br>
  Retained-mode • Fully Typed • สวย • ใช้งานง่าย • โมเดิร์น</p>

  ![Cascade Preview](https://via.placeholder.com/800x450/1e1e2e/89b4fa?text=Cascade+UI+Preview+—+macOS+Sequoia+Style)

</div>

---

## ✨ คุณสมบัติเด่น

- 🎨 ออกแบบมาในสไตล์ **macOS Sequoia** (สวยสะอาด ตา ไม่รก)
- 🔄 Retained-mode UI (จัดการสถานะให้อัตโนมัติ)
- 📘 **Fully Typed API** — เขียนโค้ดแล้ว IntelliSense ดีมาก
- 🌗 รองรับ **Light Theme** และ **Dark Theme**
- 🌈 หลายสี Accent ให้เลือก (Blue, Red, Green, Purple, Pink, Orange ฯลฯ)
- ⚡ API ระดับสูง เรียบง่าย ไม่บวม
- 🚀 เร็วและเบา เหมาะสำหรับทำ UI ระดับโปร
- 📦 รองรับการโหลดผ่าน GitHub Releases (ไม่ต้องใช้ Wally ก็ได้)

---

## 📥 การติดตั้ง (วิธีที่แนะนำ)

```lua
-- ฟังก์ชันช่วยโหลด Library (สำคัญมาก!)
local function import(owner, repo, version, file)
    local tag = (version == "latest" and "latest/download" or "download/"..version)
    return loadstring(game:HttpGetAsync(("https://github.com/%s/%s/releases/%s/%s"):format(owner, repo, tag, file)), file)()
end

-- โหลด Cascade เวอร์ชันล่าสุด
local cascade = import("biggaboy212", "Cascade", "latest", "dist.luau")
