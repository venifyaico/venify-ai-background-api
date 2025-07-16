# Venify AI Background Removal API

A powerful and developer-friendly API to remove or edit image backgrounds in real-time using AI. Built for web apps, e-commerce, design tools, and image processing pipelines, the API supports **five background modes**: `remove`, `blur`, `color`, `gradient`, and `shadow`.

---

![photo_6030874124085216505_y (1)](https://github.com/user-attachments/assets/50d0a423-b629-4546-b208-5ea742df7af2)


## Why Use This API?

The **Image Background API** is fast, accurate, and easy to integrate. Whether you're building a photo editor, a virtual fitting room, or a product uploader, this tool helps you produce pixel-perfect results in milliseconds.

### Key Benefits:
- Real-time performance
- Over 95% IOU accuracy with AI segmentation
- Handles complex edges like hair, hands, transparent zones
- Smart cropping with `crop=1`
- GDPR-compliant (no image storage)
- Affordable for startups, scalable for enterprises

---

## Get Started

You can try the API directly here:

👉 RapidAPI – [Venify AI Background Removal](https://rapidapi.com/venify-venify-default/api/ai-background-removal3)

---
## Postman Collection: Venify AI Background Removal API
This Postman collection includes ready-to-use requests for all five background editing modes supported by the Venify AI Background Removal API, including:

- `remove` – Transparent background
- `blur` – Adjustable blur strength
- `color` – Solid background color
- `gradient` – Linear, radial, or rectangle gradients
- `shadow` – Drop shadow background

### How to Use

- Download [the collection JSON](./Venify_Background_Removal_API.postman_collection.json) or clone this repo
- Open Postman and click “Import”.
- Select the file: Venify_Background_Removal_API.postman_collection.json
- Add your RapidAPI key in the headers or use an environment variable.
- Start sending requests and previewing image responses.

---

## API Features

### 1. `Remove` — Background Removal


Remove the background from any image while preserving fine details. Returns a transparent PNG.

**Optional:**  
- `crop=1` to auto-crop tightly around the subject  
- `crop=0` or omit it to keep original image dimensions


**Crop= 0**
<img width="1000" height="330" alt="venify_702215884" src="https://github.com/user-attachments/assets/a5650132-4b55-40ac-8afd-021c463028fe" />

**Crop= 1**
<img width="1000" height="352" alt="venify_802505541" src="https://github.com/user-attachments/assets/6677925f-dd38-4467-a1c4-52e788bf2e4f" />

**Code Snippets**
```shell
curl --request POST 
	--url https://ai-background-removal3.p.rapidapi.com/api/v1/remove_background 
	--header 'Content-Type: multipart/form-data' 
	--header 'x-rapidapi-host: ai-background-removal3.p.rapidapi.com' 
	--header 'x-rapidapi-key: c4aa9d8050msh393f2cffed2b882p1bcae1jsnaccfb235705e' 
	--form 'image=image.jpg' 
	--form crop=0
 ```
<br/>

### 2. `Blur` — Blur Background
Applies a natural background blur, ideal for profile pictures and product focus.
blur_strength from 1 (softest) to 10 (strongest)


<img width="975" height="400" alt="venify_085415800" src="https://github.com/user-attachments/assets/22ad4db9-58dc-4c24-94bb-4a06de891ecf" />


**Code Snippets**
```shell
curl --request POST 
	--url https://ai-background-removal3.p.rapidapi.com/api/v1/blur_background 
	--header 'Content-Type: multipart/form-data' 
	--header 'x-rapidapi-host: ai-background-removal3.p.rapidapi.com' 
	--header 'x-rapidapi-key: c4aa9d8050msh393f2cffed2b882p1bcae1jsnaccfb235705e' 
	--form 'image=image.jpg' 
	--form blur_strength=7
```
<br/>

### 3. `Color` — Solid Color Background
Replace the background with a hex or RGB color. Useful for brand consistency, standardization, and visual clarity.


<img width="952" height="391" alt="venify_521500411" src="https://github.com/user-attachments/assets/b9c56c3b-5c7f-45da-8be8-e7a218fb1cc6" />

**Code Snippets**
```shell
curl --request POST 
	--url https://ai-background-removal3.p.rapidapi.com/api/v1/color_background 
	--header 'Content-Type: multipart/form-data' 
	--header 'x-rapidapi-host: ai-background-removal3.p.rapidapi.com' 
	--header 'x-rapidapi-key: c4aa9d8050msh393f2cffed2b882p1bcae1jsnaccfb235705e' 
	--form 'image=image.jpg' 
	--form 'color=#ff0000'
```
<br/>

### 4. `Gradient` — Gradient Background
Swap the background with a custom gradient.

Supports three different gradient types: **linear, radial, or rectangular**


<img width="840" height="398" alt="venify_000485481" src="https://github.com/user-attachments/assets/41c5e448-aa15-4b56-b254-0a0a1b33a6c4" />

**Code Snippets**
```shell
curl --request POST 
	--url https://ai-background-removal3.p.rapidapi.com/api/v1/gradient_background 
	--header 'Content-Type: multipart/form-data' 
	--header 'x-rapidapi-host: ai-background-removal3.p.rapidapi.com' 
	--header 'x-rapidapi-key: c4aa9d8050msh393f2cffed2b882p1bcae1jsnaccfb235705e' 
	--form 'image=image.jpg' 
	--form 'colors=["#ff0000", "#0000ff"]' 
	--form direction=rect
```
<br/>

### 5. `Shadow` — Add Realistic Shadow
Applies a natural-looking drop shadow under the subject, making the image pop.

Users can choose from these 25 different styles:

**["outer-tl" / "outer-t" / "outer-tr" / "outer-l" / "outer-center" / "outer-r" / "outer-bl" / "outer-b" / "outer-br" / "inner-tl" / "inner-t" / "inner-tr" / "inner-l" / "inner-center" / "inner-r" / "inner-bl" / "inner-b" / "inner-br" / "persp-br" / "persp-bl" / "persp-tr" / "persp-tl" / "persp-right" / "persp-left" / "persp-below"]**


<img width="3413" height="2016" alt="Copy of Untitled545" src="https://github.com/user-attachments/assets/f500ab05-ccdf-4022-8722-db056dc25e43" />


**Code Snippets**
```shell
curl --request POST 
	--url https://ai-background-removal3.p.rapidapi.com/api/v1/shadow_background 
	--header 'Content-Type: multipart/form-data' 
	--header 'x-rapidapi-host: ai-background-removal3.p.rapidapi.com' 
	--header 'x-rapidapi-key: c4aa9d8050msh393f2cffed2b882p1bcae1jsnaccfb235705e' 
	--form 'image=image.jpg' 
	--form style=outer-br 
	--form 'shadow_color=#ffffff' 
	--form opacity=0.5 
	--form blur=12 
	--form distance=50
```


##  Use Cases
E-commerce product images

Profile picture optimization

Virtual try-on tools

Creative and design apps

AR/VR and smart image pipelines


## License
This API is provided by [Venify on RapidAPI](https://rapidapi.com/venify-venify-default/api/ai-background-removal3). Please refer to their usage terms, pricing, and limits.
