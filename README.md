# 🧠 Venify AI Background Removal API

A powerful and developer-friendly API to remove or edit image backgrounds in real-time using AI. Built for web apps, e-commerce, design tools, and image processing pipelines, the API supports **five background modes**: `remove`, `blur`, `color`, `gradient`, and `shadow`.

---

## 🚀 Why Use This API?

The **Image Background API** is fast, accurate, and easy to integrate. Whether you're building a photo editor, a virtual fitting room, or a product uploader, this tool helps you produce pixel-perfect results in milliseconds.

### 🔑 Key Benefits:
- ⚡ Real-time performance
- 🧠 Over 95% IOU accuracy with AI segmentation
- 🖼️ Handles complex edges like hair, hands, transparent zones
- 📏 Smart cropping with `crop=1`
- 🔐 GDPR-compliant (no image storage)
- 💸 Affordable for startups, scalable for enterprises

---

## 🔗 Get Started

You can try the API directly here:

👉 RapidAPI – [Venify AI Background Removal](https://rapidapi.com/venify-venify-default/api/ai-background-removal3)

---

## ✨ API Features

### 1. 🧼 `remove` — Background Removal


Remove the background from any image while preserving fine details. Returns a transparent PNG.

**Optional:**  
- `crop=1` to auto-crop tightly around the subject  
- `crop=0` or omit it to keep original image dimensions


**Crop= 0**
<img width="1000" height="330" alt="venify_702215884" src="https://github.com/user-attachments/assets/a5650132-4b55-40ac-8afd-021c463028fe" />

**Crop= 1**
<img width="1000" height="352" alt="venify_802505541" src="https://github.com/user-attachments/assets/6677925f-dd38-4467-a1c4-52e788bf2e4f" />

### 2. 🌫️ `blur` — Blur Background
Applies a natural background blur, ideal for profile pictures and product focus.
blur_strength from 1 (softest) to 10 (strongest), **Default is 7**

**Example:**  
```bash
blur_strength=5
```
<img width="975" height="400" alt="venify_085415800" src="https://github.com/user-attachments/assets/22ad4db9-58dc-4c24-94bb-4a06de891ecf" />


### 3. 🎨 `color` — Solid Color Background
Replace the background with a hex or RGB color. Useful for brand consistency, standardization, and visual clarity.

**Example:**

```bash
color=#ffffff
```
<img width="952" height="391" alt="venify_521500411" src="https://github.com/user-attachments/assets/b9c56c3b-5c7f-45da-8be8-e7a218fb1cc6" />


### 4. 🌈 `gradient` — Gradient Background
Swap the background with a custom gradient.

**Supports:**

gradient_type: linear, radial, or rectangular

**Example of colors and direction:**

```bash
direction=linear
colors=#ff0000,#00ffcc
```
<img width="840" height="398" alt="venify_000485481" src="https://github.com/user-attachments/assets/41c5e448-aa15-4b56-b254-0a0a1b33a6c4" />



### 5. 🕶️ `shadow` — Add Realistic Shadow
Applies a natural-looking drop shadow under the subject, making the image pop.

**Default Variables:**
```bash
shadow_color=#ffffff
opacity=0.5
blur=12
distance=15
```


## 📦 Use Cases
E-commerce product images

Profile picture optimization

Virtual try-on tools

Creative and design apps

AR/VR and smart image pipelines


## 📄 License
This API is provided by [Venify on RapidAPI](https://rapidapi.com/venify-venify-default/api/ai-background-removal3). Please refer to their usage terms, pricing, and limits.
