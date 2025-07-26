
# 🚀 React Native + NativeWind Starter

This repository provides a clean starter template for building **React Native** apps with **NativeWind** (Tailwind CSS for React Native).

## 📦 Tech Stack

- ⚛️ React Native (via Expo or CLI)
- 🌬️ NativeWind (Tailwind CSS)
- 💅 Utility-first styling
- 🔧 TypeScript (optional)

---

## 🛠️ Getting Started

### 1. Create a new React Native project

Using Expo:

```bash
npx create-expo-app myapp
cd myapp
```

---

### 2. Install NativeWind & Tailwind dependencies

```bash
npm install nativewind
npm install -D tailwindcss
```

If you're using TypeScript, also add:

```bash
npm install -D @types/react @types/react-native
```

---

### 3. Create the Tailwind config

```bash
npx tailwindcss init
```

Then update the `tailwind.config.js`:

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{js,jsx,ts,tsx}"],
  presets: [require("nativewind/preset")],
  theme: {
    extend: {},
  },
  future: {
    hoverOnlyWhenSupported: true,
  },
  plugins: [],
};

```

---

### 4. Configure Babel (if not Expo)

In `babel.config.js`, add `"nativewind/babel"` to plugins:

```js
module.exports = function (api) {
  api.cache(true);
  return {
    presets: [
      ["babel-preset-expo", { jsxImportSource: "nativewind" }],
      "nativewind/babel",
    ],
  };
};

```

---

### 5. Use Tailwind Classes in Components

Now you're ready to use utility classes:

```tsx
// App.js or App.tsx
import { Text, View } from 'react-native';

export default function App() {
  return (
    <View className="flex-1 items-center justify-center bg-white">
      <Text className="text-lg font-bold text-blue-600">Hello NativeWind!</Text>
    </View>
  );
}
```

---

## ✅ Features

- Fully configured Tailwind-style utilities
- Works with Expo or bare React Native CLI
- Great developer experience and fast styling

---

## 📚 Docs

- [NativeWind Docs](https://www.nativewind.dev/)
- [Tailwind CSS Docs](https://tailwindcss.com/)
- [React Native Docs](https://reactnative.dev/)

---


## 🔥 Troubleshooting

- Make sure your `tailwind.config.js` includes the correct `content` paths.
- If styles don't show up, restart the dev server with `npx expo start -c` or `npx react-native start --reset-cache`.

---

## 📝 License

MIT

---

## 💡 Author

Made with ❤️ by [Pranay Bhatkar]
