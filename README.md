# Comic-Tube 📚🎨

> A hybrid comic-hosting and interactive streaming platform bridging a **Unity (C#)** frontend with a **MERN Stack** backend.

Comic-Tube allows creators to host, stream, and enhance comics with interactive elements such as ambient background music, sound effects, and visual panel transitions.

---

## 🔗 Repository Links

* **Backend (MERN Stack):** [Comic-Tube Repository](https://github.com/sambuigps/Comic-Tube)
* **Frontend (Unity Engine):** [Comic-Tube-Unity Repository](https://github.com/sambuigps/Comic-Tube-Unity)

---

## 🌟 Key Features

* **Interactive Frontend (Unity):** Statically typed C# viewer supporting custom sound effects, panel animations, and dynamic camera transitions.
* **RESTful Backend (MERN):** Scalable Express & Node.js API with MongoDB schemas for handling comic metadata, asset uploads, and user authentication.
* **Creator Suite:** Tools for authors to attach audio triggers, VFX, and timeline markers directly to panel coordinates.
* **Cross-Platform Compatibility:** Designed to render responsive interactive web viewers via Unity WebGL and standalone targets.

---

## 🏗️ Architecture Overview

```text
├── Frontend (Unity / C#)
│   └── Assets/              # C# Scripts, Shaders, UI & Audio Assets
│
└── Backend (MERN Stack)
    ├── config/              # Database & Auth configuration
    ├── controllers/         # API Controllers for upload & stream endpoints
    ├── models/              # MongoDB Schemas (Users, Comics, Panels)
    ├── routes/              # RESTful API Routes
    ├── services/            # API services for upload & stream endpoints
    └── index.js             # Node/Express Entry Point
```

---

## 🚀 Getting Started

### Prerequisites

Ensure you have the following installed locally:
* [Node.js](https://nodejs.org/) (v18 or higher)
* [MongoDB](https://www.mongodb.com/) (Local instance or Atlas URI)
* [Unity Hub](https://unity.com/) (Recommended version: `2022.3 LTS` or newer)

---

### Installation & Setup

#### 1. Backend Setup
```bash
# Clone the backend repository
git clone https://github.com/Sukhman3125/Comic-Tube.git
cd Comic-Tube

# Install dependencies
npm install

# Create environment configuration
cp .env.example .env
```

Configure your `.env` file:
```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
```

Start the server:
```bash
npm run dev
```

#### 2. Frontend Setup (Unity)
```bash
# Clone the Unity repository
git clone https://github.com/sambuigps/Comic-Tube-Unity.git
```

1. Open **Unity Hub** and select **Add project from disk**.
2. Select the cloned `Comic-Tube-Unity` folder.
3. Open the project and navigate to `Assets/Scenes/MainViewer.unity`.
4. Ensure your API endpoint base URL in `NetworkManager.cs` points to `http://localhost:5000/api`.

---

## 🤝 Contributing

Contributions are welcome! Follow these steps to contribute:

1. **Fork** the repository.
2. Create a new branch: `git checkout -b feature/your-feature-name`.
3. Commit your changes: `git commit -m 'Add some feature'`.
4. Push to the branch: `git push origin feature/your-feature-name`.
5. Open a **Pull Request**.

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
