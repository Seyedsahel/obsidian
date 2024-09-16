#### setup format Vue :
##### in src/
``` main.js
import "./assets/main.css";

  

import { createApp } from "vue";

import App from "./App.vue";

import router from "./router";

  

const app = createApp(App);

  

app.use(router);

  

app.mount("#app");
```

router is a file called index.js in src/router more routing details [[router]]
more detail of app in [[App]]

