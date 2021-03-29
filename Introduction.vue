<template>
    <div class="introduction-container">
        <span class="main-header-title">
            Introduction
        </span>
        <span class="main-subheader-title">
            Getting started with a flexible component set Provue for rapid development complex feature-rich UI for modern Web.
        </span>
        <span class="main-accentheader-title">
            Micro frontend or monolith?
        </span>
        <span>
            Micro Frontends
            <a href="https://micro-frontends.org/">(link)</a>
            it new area in frontend development that aim to split frontend in small parts.
            Ideally, parts have to be fully isolated apart but it not easy because the application can have common environment options, css and so on.
            Of course, also can have issues with routing and intercommunication between small parts.
            But all issues can be solved and at end of the day, you can get the opportunity to separate your monolith frontend between teams and increase pace development.
            <br />
            Our goal tries to solve as many as possible issues related to Micro Frontends with a component set Provue.
            As a foundation, we decided to select the library Vue.js.
            Single File Component that Vue.js suggest it our opition ideal fit for implement Micro Frontends because all parts - template, css, script and required dependencies defined in one file.
            Components have flexible parent-children communication methods.
            Children's components can be lazy-loaded.
        </span>
        <span class="main-accentheader-title">
            Component separation
        </span>
        <span>
            As you know from previous section Micro Frontends have few issues that need to be solved. One from that issues will be solved way separate
            all components on two parts - state and view.
            State keeps logic and state using as controller (in terms MVC). View keeps methods for drawing html.
            Why it need it separation? As nature Micro Frontends keep thing small separated. Idea behind separation that you can use "common components" with
            same api but you feel free change it visual representation in different small parts of you application.
        </span>
        <span class="main-accentheader-title">
            Quick start
        </span>
    </div>
</template>

<script>
export default async function () {
    return {
        name: `App`,
        data() {
            return {
            }
        },
        methods: {
        },
        components: {
        }
    }
}
</script>

<style>
.introduction-container {
    display: flex;
    flex-direction: column;
}
</style>