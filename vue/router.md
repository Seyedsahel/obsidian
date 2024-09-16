file index.js in src/router
```index.js
import { createRouter, createWebHistory } from "vue-router";

import SplashView from "@/views/SplashView.vue";

import HomeView from "@/views/HomeView.vue";

import AnalysisView from "@/views/AnalysisView.vue";

import AppView from "@/views/AppView.vue";

import CategoryView from "@/views/CategoryView.vue";

import ProfileView from "@/views/ProfileView.vue";

  

const router = createRouter({

    history: createWebHistory(import.meta.env.BASE_URL),

    routes: [

        {

            path: "/",

            component: SplashView,

        },

        {

            path: "/app",

            component: AppView,

            redirect: "/app/home",

            children: [

                {

                    path: "home",

                    component: HomeView,

                },

                {

                    path: "category",

                    component: CategoryView,

                },

                {

                    path: "analysis",

                    component: AnalysisView,

                },

                {

                    path: "profile",

                    component: ProfileView,

                },

            ],

        },

    ],

});

  

export default router;
```

with this template we have path and sub path
