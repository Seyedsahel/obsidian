npm install -D tailwindcss@latest postcss@latest autoprefixer@latest 

npx tailwindcss init -p

in tailwind.js.config :
```
content: ["./index.html", "./src/**/*.{vue,js,ts}"],
```

in src/assests/base.css:
```
@tailwind base;

@tailwind components;

@tailwind utilities;
```
