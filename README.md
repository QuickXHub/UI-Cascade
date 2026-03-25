# UI Cascade

> นี้จะเป็๋นการบอกวิธีการใช้ UI Cascade 

[Example](https://github.com/QuickXHub/UI-Cascade/blob/main/Example.lua)

## สำคัญ ถ้าไม่ใช้รัน UI ไม่ติด
```lua
local function import(owner, repo, version, file)
    local tag = (version == "latest" and "latest/download" or "download/"..version)

    return loadstring(game:HttpGetAsync(("https://github.com/%s/%s/releases/%s/%s"):format(owner, repo, tag, file)), file)()
end

local cascade = import("biggaboy212", "Cascade", "latest", "dist.luau")

local app = cascade.New({
    WindowPill = true,
    Theme = cascade.Themes.Light, -- เปลื่ยนได้ มีแค่ Dark กับ Light
    Accent = cascade.Accents.Blue, -- เปลื่ยนได้ มีหลายสี
})
