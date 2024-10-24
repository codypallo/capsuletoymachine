
# How to Format an A-Frame-Based eBook for the Capsule Toy Machine

To create an A-Frame-based eBook for the Capsule Toy Machine, the process involves packaging your **WebXR content** in a way that is both accessible offline and served via a local server. The format used for this is the **ePub file**, a common format for eBooks that can be repurposed to hold the necessary files for running an A-Frame experience.

---

## 1. A-Frame Project Structure

Start by developing your A-Frame project. Your WebXR content should be organized in the following structure:

```
/my-aframe-project
│
├── /assets                # Folder containing images, 3D models, textures, sounds, etc.
├── /js                    # Folder containing custom JavaScript code for interactions.
├── index.html             # Main A-Frame HTML file where the XR experience is defined.
├── manifest.json          # A manifest file describing the structure and metadata of the ePub.
└── style.css              # Optional CSS for styling your WebXR experience.
```

---

## 2. Manifest File (manifest.json)

Every ePub needs a **manifest.json** file at its root to describe the contents of your A-Frame eBook. This file will tell the Capsule Toy Machine how to handle the content.

Here’s an example of a simple **manifest.json** file:

```json
{
  "title": "My A-Frame WebXR eBook",
  "author": "Your Name",
  "language": "en",
  "version": "1.0",
  "content": [
    {
      "path": "index.html",
      "type": "text/html"
    },
    {
      "path": "assets/model.glb",
      "type": "model/gltf-binary"
    },
    {
      "path": "js/script.js",
      "type": "application/javascript"
    }
  ],
  "metadata": {
    "description": "An interactive WebXR experience built with A-Frame.",
    "keywords": ["WebXR", "A-Frame", "VR", "eBook"],
    "category": "Virtual Reality"
  }
}
```

---

## 3. Packaging the Project as an ePub

Once your A-Frame project is organized and ready, you can **package it as an ePub** file by following these steps:

1. **Create a ZIP Archive**:
   - Zip all the files in your project directory, including the **manifest.json**, **index.html**, and any assets (e.g., 3D models, images, and scripts).
   
   Example command:
   ```bash
   zip -r my-aframe-project.zip *
   ```

2. **Rename the ZIP File**:
   - Change the `.zip` file extension to `.epub`. This is crucial because the Capsule Toy Machine reads ePub files as XR applications.
   
   Example command:
   ```bash
   mv my-aframe-project.zip my-aframe-project.epub
   ```

---

## 4. Distribute or Deploy

Once your project is packaged as an ePub file, it can be:

- **Distributed Physically**: You can store it on an SD card or similar media for distribution.
- **Shared Digitally**: The ePub can be uploaded to a platform like GitHub, from where users can download and use it on their Capsule Toy Machine.

---

## 5. Serving the ePub on Capsule Toy Machine

When the Capsule Toy Machine loads the ePub, it will:
- **Unpack the ePub**: The ePub file will be treated as a zip archive and unpacked to a local server instance.
- **Serve the content**: The **index.html** file will be served locally through the device's WiFi gateway, allowing up to 100 users to connect and experience the WebXR content offline.

---

## Example Project Structure Inside the ePub

Once packaged as an ePub file, the project structure would look like this inside:

```
/my-aframe-project.epub
│
├── /assets
├── /js
├── index.html
├── manifest.json
└── style.css
```

---

## Conclusion

Creating an A-Frame-based ePub for the Capsule Toy Machine involves packaging a well-structured A-Frame WebXR project into an ePub format. The manifest file is key to ensuring the content is served correctly, and by renaming the zipped project to `.epub`, you make it accessible through the Capsule Toy Machine's local server. This format makes it easy to distribute your XR apps both digitally and physically.
