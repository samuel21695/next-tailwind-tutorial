# next-tailwind-tutorial

Installation

## Install Tailwind CSS with Next.js
### Setting up Tailwind CSS in a Next.js project.


### 1 Create your project
Start by creating a new Next.js project if you don’t have one set up already. The most common approach is to use Create Next App.

```
npx create-next-app@latest my-project --typescript --eslint
cd my-project
```
### 2 Install Tailwind CSS
Install tailwindcss and its peer dependencies via npm, and then run the init command to generate both tailwind.config.js and postcss.config.js.

```
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

### 3 Configure your template paths
Add the paths to all of your template files in your tailwind.config.js file.

tailwind.config.js

```
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./app/**/*.{js,ts,jsx,tsx,mdx}",
    "./pages/**/*.{js,ts,jsx,tsx,mdx}",
    "./components/**/*.{js,ts,jsx,tsx,mdx}",
 
    // Or if using `src` directory:
    "./src/**/*.{js,ts,jsx,tsx,mdx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

### 4 Add the Tailwind directives to your CSS
Add the @tailwind directives for each of Tailwind’s layers to your globals.css file.

globals.css

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### 5 Start your build process
Run your build process with npm run dev.

```
npm run dev
```

### 6 Start using Tailwind in your project
Start using Tailwind’s utility classes to style your content.

index.tsx

```
export default function Home() {
  return (
    <h1 className="text-3xl font-bold underline">
      Hello world!
    </h1>
  )
}
```N
