# Brat Generator REST API

![Stars](https://img.shields.io/github/stars/xodobyte/brat-generator?style=for-the-badge) 
![Forks](https://img.shields.io/github/forks/xodobyte/brat-generator?style=for-the-badge) 
![Issues](https://img.shields.io/github/issues/xodobyte/brat-generator?style=for-the-badge) 
![Repo Size](https://img.shields.io/github/repo-size/xodobyte/brat-generator?style=for-the-badge)

**All Rights Reserved © xodobyte**  
This API generates custom "Brat" style images with emoji support.  

---

## 📌 Description
The Brat Generator REST API allows you to generate stylized text images in **WebP** format using a custom "Brat" font and Apple Emoji font.  
Perfect for meme text, stylized branding, or custom text art.

---

## 🔗 Endpoint
> The final hosted endpoint will be provided upon deployment.  
For now, the development endpoint looks like this:

```
GET /api/brat?text=YOUR_TEXT
```

---

## 📥 Query Parameters

| Parameter | Required | Type   | Description |
|-----------|----------|--------|-------------|
| `text`    | Yes      | String | The text you want to render into a Brat-style image. Supports emojis. |

---

## 📤 Response Format

**Successful Response (HTTP 200)**:
```json
{
  "creator": "xodobyte",
  "success": true,
  "format": "webp",
  "data": "data:image/webp;base64,..."
}
```

**Error Response (HTTP 400 or 500)**:
```json
{
  "creator": "xodobyte",
  "success": false,
  "error": "Description of error"
}
```

---

## 🖋 Font Information
- **BratFont** → Custom font for stylized text.
- **AppleEmoji** → Emoji rendering.

The API automatically detects and renders emojis differently from text.

---

## ⚠️ Terms of Use
- **All Rights Reserved © xodobyte**.
- Do not attempt to run, copy, or reverse-engineer this API locally.
- Access is strictly through the provided hosted endpoint.

---

## 🛠 Example Usage
```
GET /api/brat?text=HELLO%20WORLD%20🔥
```
Returns a base64-encoded WebP image.

---

Made with ❤️ by **xodobyte**
